---
title: Ukázka integrace fiskální služby pro Českou republiku
description: V tomto tématu je uveden přehled fiskální integrace pro Českou republiku.
author: josaw
manager: annbe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Czech Republic
ms.search.industry: Retail
ms.author: v-dmpere
ms.search.validFrom: 2019-4-1
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 82f7b6a0b8d6d4b517eb3480b1550b821e95ec46
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595303"
---
# <a name="fiscal-registration-service-integration-sample-for-czech-republic"></a>Ukázka integrace fiskální služby pro Českou republiku


[!include[banner](../includes/banner.md)]

## <a name="introduction"></a>Úvod

Pro účely splnění fiskálních požadavků na registrační pokladny v České republice obsahuje funkce Microsoft Dynamics 365 for Retail pro Českou republiku vzorovou integraci pokladního místa (POS) s externí fiskální registrační službou. Vzorek rozšiřuje [funkci fiskální integrace](fiscal-integration-for-retail-channel.md). Je založena na řešení [EFR (Electronic Fiscal Register)](https://efsta.org/sicherheitsloesungen/) od [EFSTA](https://efsta.org/) a umožňuje komunikaci se službou EFR přes protokol HTTPS. Služba EFR zajišťuje elektronickou registraci prodeje (EET - Elektronická evidence tržeb), tj. online převodu prodejních údajů do fiskální webové služby daňových úřadů.

Služba EFR by měla být hostitelem hardwarové stanice pro maloobchod nebo samostatný počítač, se kterým se lze propojit z hardwarové stanice. Ukázka je poskytnuta ve formě zdrojového kódu a je součástí sady software development kit (SDK) pro maloobchod.

Společnost Microsoft nevydává žádný hardware, software nebo dokumentaci k EFSTA. Informace o tom, jak řešení EFR získat a provozovat, vám poskytne [EFSTA](https://efsta.org/kontakt/).

## <a name="scenarios"></a>Scénáře

Následující scénáře uvádějí vzorek integrace fiskální registrační služby pro Českou republiku.

- Registrace transakcí v hotovosti ve službě daňové registrace.

    - Odešlete podrobná data transakce do služby daňové registrace. Tyto údaje obsahují informace o řádku prodeje a informace o slevách, platbách a daních Služba daňové registrace dále odesílá data do webové služby finančního úřadu a přijímá od ní potvrzení obsahující daňový identifikační kód transakce.
    - Zaznamenejte odpověď z daňové registrační služby. Tato odpověď obsahuje finanční údaje, například daňový identifikační kód a bezpečnostní kód transakce atd.
    - Vytiskněte finanční údaje pro registrovanou transakci na účtence.

- Registrace operací dárkových poukazů a vkladů pro odběratele ve službě daňové registrace.

    - Vydejte nebo přidejte peníze na dárkový poukaz.
    - Zaregistrujte vklad na účet odběratele.
    - Vytvořte objednávku odběratele a registrujte zálohu pro objednávku.
    - Upravte objednávku odběratele a přepište zálohu pro objednávku.
    - Zrušte objednávku odběratele a refundujte zálohu pro objednávku.

- Zpracování chyb, jako jsou následující možnosti.

    - Opakujte fiskální registraci, pokud to je možné, například když není k dispozici služba fiskální registrace, není připravena nebo nereaguje.
    - Odložte fiskální registraci.
    - Přeskočte daňovou registraci nebo označte transakci jako registrovanou a zahrňte informační kódy pro zaznamenání důvodu chyby a dalších informací.
    - Zkontrolujte dostupnost služby daňové registrace, dříve než otevřete novou transakci prodeje nebo ji dokončíte.

### <a name="default-data-mapping"></a>Výchozí mapování dat

Následující výchozí mapování dat je součástí konfigurace poskytovatele fiskálního dokumentu, který je poskytován jako fiskální vzorek integrace.

- Mapování sazeb daně z přidané hodnoty (DPH):

    *A: 21,00; B: 15,00; C: 10,00; Z: 0,00*

- Výchozí mapování skupiny DPH. Jakékoli částky DPH, které nelze mapovat na některou z předem určených skupin DPH, budou připsány výchozí (základní) skupině DPH:

    *O*

- Vložte zálohu mapování skupiny DPH. Částky zálohy odběratele a zálohy objednávky odběratele budou připsány skupině DPH zálohy:

    *Z*

### <a name="gift-cards"></a>Dárkové poukazy

Ukázka integrace daňové registrační služby implementuje následující pravidla související s dárkovými poukazy.

- Řádky prodeje, které souvisejí s operacemi *Vydat dárkový poukaz* nebo *Přidat k dárkovému poukazu* v prodejních transakcích jsou označeny zvláštním atributem při registraci transakce v daňové registrační službě.
- Platba dárkovým poukazem je považována za běžnou platbu a je označena zvláštním atributem při registraci transakce ve službě daňové registrace

### <a name="customer-account-deposits-and-customer-order-deposits"></a>Vklady na účet odběratele a vklady objednávky odběratele

Ukázka integrace daňové registrační služby implementuje následující pravidla, která souvisí s vklady na účtu odběratele a vklady objednávky odběratelů.

- Maloobchodní transakce související s vkladem na účet odběratele nebo je vklad objednávky zákazníka registrována ve službě daňové registrace jako samostatný řádek transakce a je označen zvláštním atributem. Skupina DPH zálohy je zadána v tomto řádku.
- Při vytvoření hybridní objednávky odběratele, tedy objednávky odběratele, která obsahuje produkty, které lze převést mimo obchod odběratelem a k produktům, které budou vyzvednuty nebo expedovány, obsahuje transakce registrovaná ve službě daňové registrace obsahuje řádky pro produkty, které jsou prováděny, a také řádku objednávky vkladu.
- Platba z účtu zákazníka je považována za běžnou platbu a je označena zvláštním atributem při registraci transakce ve službě daňové registrace
- Částka vkladu objednávky odběratele použitá na objednávce odběratele v operaci *Vyzvednout* je považována za běžnou platbu a je označena zvláštním atributem při registraci transakce daňové registrace služby.

### <a name="offline-registration"></a>Offline registrace

Pokud se nezdaří službě daňové registrace přenášet data transakce fiskálních webové služby finančního úřadu (například z důvodu limitu odezvy) a chcete dostat potvrzení z webové služby (to znamená fiskální identifikační kód transakce), generuje místní podpis transakce a zahrne ho jako speciální kód chyby v odpovědi. Služba daňové registrace znovu odešle transakce v původní objednávce na pozadí ihned po obnovení síťového připojení.

### <a name="limitations-of-the-sample"></a>Omezení vzorku

Služba daňové registrace podporuje pouze scénáře, kde je součástí ceny daň z prodeje. Proto musí být možnost **Ceny zahrnují DPH** nastavena na **Ano** pro maloobchodní obchody a odběratele.

## <a name="set-up-retail-for-czech-republic"></a>Natavení maloobchodu pro Českou republiku

Tato část popisuje nastavení maloobchodu, která jsou specifická a doporučená pro Českou republiku. Další informace o nastavení maloobchodních produktů získáte v [Microsoft Dynamics 365 for Retail dokumentaci](../index.md).

Chcete-li použít funkci specifickou pro český maloobchod, je nutné zadat následující nastavení.

- V primární adrese právnické osoby nastavte pole **země/oblasti** na **CZE** (Česká republika).
- V profilu funkce POS každého obchodu, který se nachází v rámci České republiky, nastavte pole **kód ISO** na **CZ** (Česká republika).

Zadejte také následující nastavení pro Českou republiku. Po dokončení instalace musíte spustit příslušné distribuční úlohy.

### <a name="set-up-vat-per-czech-republic"></a>Nastavení DPH pro Českou republiku

Musíte vytvořit kódy DPH, skupiny daní DPH a skupiny DPH za zboží. Musíte také nastavit informace o DPH pro produkty a služby. Další informace o způsobu nastavení a použití DPH v aplikaci Microsoft Dynamics 365 for Finance and Operations a v aplikaci Retail získáte v části [Přehled DPH](../../financials/general-ledger/indirect-taxes-overview.md).

### <a name="set-up-retail-stores"></a>Nastavení maloobchodních prodejen

Na stránce **všechny maloobchodní prodejny** aktualizujte podrobnosti o maloobchodu. Je nutné konkrétně nastavit následující parametry.

- V poli **Skupina DPH** zadejte skupinu DPH, kterou chcete použít pro prodeje výchozímu maloobchodnímu odběrateli.
- Nastavte možnost **Ceny jsou včetně DPH** na **Ano**.
- V poli **název** zadejte název společnosti. Tato změna pomáhá zajistit, že se název společnosti zobrazí na dokladu o prodeji. Případně můžete přidat název společnosti na prodejní doklad jako volný text.
- Nastavte **daňové identifikační číslo (DIČ)** na identifikační číslo společnosti. Tato změna pomáhá zajistit, že se identifikační číslo společnosti zobrazí na dokladu o prodeji. Případně můžete přidat identifikační číslo společnosti na prodejní doklad jako volný text.

### <a name="set-up-functionality-profiles"></a>Nastavení funkčních profilů

Nastavte funkční profily POS.

- Na pevné záložce **Číslování dokladů** nastavte číslování dokladů vytvořením nebo aktualizací záznamů pro typy příjmových transakcí **Prodej**, **Prodejní objednávka** a **Vrácení**.

### <a name="set-up-registration-numbers"></a>Nastavení registračních čísel

1. Přejděte na položky **Správa organizace \> Globální adresář \> Typy registrace \> Typy registrace**. Vytvořte nový typ registrace. Určete pole **Země/oblast** na **CZE** (Česká republika) a omezte je na organizaci.
2. Přejděte na položky **Správa organizace \> Globální adresář \> Typy registrace \> Kategorie registrace**. Vytvořte novou kategorii registrace. Vyberte typ registrace z předchozího kroku a nastavte **kategorii registrace** na **ID místa obchodu**.
3. Přejděte do nabídky **Správa organizace \> Organizace \> Provozní jednotky**. Pro každý obchod v rámci České republiky vyberte jednotku vztahující se k obchodu. Na pevné záložce **Adresa** rozbalte rozevírací seznam **Další možnosti** a vyberte **Upřesnit**. 
4. Na otevřené stránce **spravovat adresy** je nutné zadat následující nastavení.

    - Na pevné záložce **Adresa** nastavte pole **země/oblast** na **CZE**.
    - Na pevné záložce **ID registrace** vytvořte nový záznam. Vyberte dříve vytvořený typ registrace a nastavte registrační číslo.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Nakonfigurujte vlastní pole tak, aby bylo možné použít je ve formátech příjemky pro prodejní příjemky

Můžete konfigurovat jazykový text a vlastní pole, která se používají ve formátech příjemky POS. Výchozí společnost uživatele, který vytvoří nastavení příjmu, musí být stejná právnická osoba, pro kterou se vytváří nastavení text jazyka. Alternativně lze vytvořit texty ve stejném jazyce, které mají být vytvořeny ve výchozí společnosti uživatele a právnické osobě prodejny, pro kterou se nastavení vytváří.

Na stránce **jazykový text** přidejte následující záznamy popisků vlastního pole rozvržení účtenky. Upozorňujeme, že hodnoty **ID jazyka**, **ID textu** a **Text**, které jsou zobrazeny v tabulce, jsou jenom příklady. Lze je změnit tak, aby splňovaly vaše požadavky. Hodnoty **ID textu**, které budete používat, však musí být jedinečné a musí být rovny nebo větší než 900001.

Přidejte následující štítky POS do oddílu **POS** v poli **Jazykový text** z tabulky:

| ID jazyka | ID textu | Text                   |
|-------------|---------|------------------------|
| cs       | 900001  | ID provozovny/pokladny |
| cs       | 900002  | BKP                    |
| cs       | 900003  | FIK                    |
| cs       | 900004  | PKP                    |
| cs       | 900005  | Informace                   |
| cs       | 900006  | Pořadové číslo        |

Na stránce **Vlastní pole** přidejte následující záznamy popisků vlastního pole rozvržení účtenky. Upozorňujeme, že hodnoty **ID textu titulku** musí odpovídat hodnotám **ID textu**, které jste zadali na stránce **jazykový text**:

| Název                 | Typ    | ID textu titulku |
|----------------------|---------|-----------------|
| TLT                  | Účtenka | 900001          |
| SEC                  | Účtenka | 900002          |
| SIGN                 | Účtenka | 900003          |
| FISCAL               | Účtenka | 900004          |
| INFO                 | Účtenka | 900005          |
| CONTINUOUSNUMBER     | Účtenka | 900006          |

### <a name="configure-receipt-formats"></a>Konfigurace formátů příjemky

Pro každý požadovaný formát příjemky změňte hodnotu pole **Chování tisku** na **vždy tisknout**.

V Návrháři formátu příjemky přidejte následující vlastní pole do příslušných oddílů příjemky. Všimněte si, že názvy polí odpovídají jazykovým textům, které jste definovali v předchozím oddílu.

- **Záhlaví:** Přidejte následující pole.

    - **Název obchodu** a **daňové identifikační číslo**: tato pole umožňují vytisknout na účtenky název a identifikační číslo společnosti. Případně můžete přidat název společnosti a číslo identity do rozvržení jako volný text.
    - **Adresa obchodu**, **datum**, **čas 24H**, **čísla účtenky**, a **číslo registrační pokladny**.
    - **Číselná řada**: Toto pole identifikuje počet hotovostních transakcí daňové registrace služby.

- **Řádky:** Přidejte následující pole.

    - **Název položky**
    - **Množství**
    - **Celková cena s daní**

- **Zápatí:** Přidejte následující pole.

    - Pole platby, aby se vytiskly částky platby pro každou metodu platby. Například přidejte pole **název úhrady** a **Částka úhrady** na jeden řádek rozvržení.
    - **ID provozovny/pokladny**: toto pole vytiskne identifikátory obchodních prostorů a registrační pokladny.
    - **BKP**: Toto pole vytiskne bezpečnostní kód plátce daně, který přiřazuje služba daňové registrace.
    - **FIK**: toto pole vytiskne daňový identifikační kód transakce, který přiděluje webová služba daňového úřadu v případě úspěšné online registrace.
    - **PKP**: Toto pole vytiskne kód podpisu správce daně, který je generován v případě offline registrace u služby daňové registrace.
    - **Informace**: Toto pole vytiskne doplňkové informace ze služby daňové registrace.

Další informace o tom, jak pracovat s formáty příjemek, naleznete v tématu [Šablony pro příjemky a tisk](../receipt-templates-printing.md).

### <a name="configure-fiscal-integration"></a>Konfigurace fiskální integrace

Postupujte podle kroků pro nastavení fiskální integrace popsané v části [Nastavení fiskální integrace pro maloobchodní kanály](setting-up-fiscal-integration-for-retail-channel.md).

- [Nastavení procesu fiskální registrace](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Všimněte si také nastavení pro proces fiskální registrace, který je [specifický pro tuto ukázku služby fiskální registrace](#set-up-the-registration-process).
- [Nastavení zpracování chyb](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
- [Povolit ruční provedení zápisu odložené daňové registrace](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).

## <a name="deployment-guidelines-for-cash-registers-for-czech-republic"></a>Pokyny k nasazení registračních pokladen pro Českou republiku

Ukázka integrace fiskální služby pro Českou republiku je součástí sady Retail SDK. Informace o instalaci a použití sady Retail SDK naleznete v tématu [Dokumentace k Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Tento příklad sestává z rozšíření pro CRT a hardwarovou stanici. Ke spuštění tohoto příkladu musíte změnit a sestavit projekty CRT a hardwarové stanice. Doporučujeme používat nemodifikovanou sadu Retail SDK k provedení změn, které jsou popsány v tomto tématu. Rovněž doporučujeme používat zdrojový systému kontroly, jako je například Azure DevOps, kde žádné soubory nebyly dosud změněny.

Tento postup slouží k nastavení vývojového prostředí, abyste mohli testovat a rozšířit vzorek.

### <a name="enable-commerce-runtime-extensions"></a>Povolit rozšíření služby Commerce runtime

Komponenty rozšíření CRT jsou součástí ukázek CRT. Pro dokončení následujících postupů otevřete řešení CRT, **CommerceRuntimeSamples.sln**, v části **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="documentproviderefrsample-component"></a>Komponenta DocumentProvider.EFRSample

1. Najděte projekt **Runtime.Extensions.DocumentProvider.EFRSample** a vytvořte ho.
2. Ve složce **Runtime.Extensions.DocumentProvider.EFRSample\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru Microsoft Internet Information Services (IIS) Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

4. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

5. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>Komponenta DocumentProvider.DataModelEFR

1. Najděte projekt **Runtime.Extensions.DocumentProvider.DataModelEFR** a vytvořte ho.
2. Ve složce **Runtime.Extensions.DocumentProvider.DataModelEFR\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

4. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

5. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="update-extension-configuration-file"></a>Aktualizace konfiguračního souboru rozšíření

1. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

2. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
    ```

### <a name="enable-hardware-station-extensions"></a>Povolení rozšíření hardwarové stanice

Komponenty rozšíření hardwarové stanice jsou součástí ukázek hardwarové stanice. Pro dokončení následujících postupů otevřete řešení CRT, **HardwareStationSamples.sln** v části **RetailSdk\\SampleExtensions\\HardwareStation**.

#### <a name="efrsample-component"></a>Komponenta EFRSample

1. Najděte projekt **HardwareStation.Extension.EFRSample** a vytvořte ho.
2. Ve složce **Extension.EFRSample\\bin\\Debug** vyhledejte následující soubory:

    - Sestavení **Contoso.Commerce.HardwareStation.EFRSample.dll**
    - Sestavení **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll**

3. Zkopírujte soubory sestavení do složky rozšíření hardwarové stanice:

    - **Sdílená hardwarové stanice:** Zkopírujte složku **bin** pod umístění webu hardwarové stanice IIS.
    - **Vyhrazená hardwarová stanice pro Modern POS:** Zkopírujte soubory do stanice zprostředkovatele klienta Modern POS.

4. Najděte konfigurační soubor rozšíření hardwarová stanice. Název souboru je **HardwareStation.Extension.config**.

    - **Sdílená hardwarové stanice:** Soubor se nachází pod umístěním webu hardwarové stanice IIS.
    - **Vyhrazená hardwarová stanice pro Modern POS:** Soubor se nachází ve stanici zprostředkovatele klienta Modern POS.

5. Přidejte následující řádek do oddílu **composition** konfiguračního souboru.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

### <a name="set-up-the-registration-process"></a>Nastavení procesu registrace

Pokud chcete povolit registrační proces, postupujte pomocí následujících kroků pro nastavení Retail Headquarters. Další informace naleznete v tématu [Nastavení fiskálního registračního procesu](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Přejděte na možnost **Maloobchod \> Nastavení centrály \> Parametry \> Sdílené parametry maloobchodu**. Na kartě **Obecné** nastavte možnost **Povolit fiskální integraci** na **Ano**.
2. Přejděte na **Maloobchod \> Nastavení kanálu \> Fiskální integrace \> Fiskální konektory** a vyhledejte konfiguraci konektoru. Umístění souboru je **RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration\\ConnectorEFRSample.xml**.
3. Přejděte na **Maloobchod \> Nastavení kanálu \> Fiskální integrace \> Poskytovatelé fiskálních dokumentů** a vyhledejte konfiguraci poskytovatele dokumentu. Konfigurační soubor je **RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration\\DocumentProviderFiscalEFRSampleCzech.xml**.
4. Přejděte na **Maloobchod \> Nastavení kanálu \> Fiskální integrace \> Funkční profily Connector**. Vytvořte nový funkční profil konektoru. Vyberte poskytovatele dokumentu a dříve načtený konektor. Aktualizujte nastavení mapování dat podle potřeby.
5. Přejděte na **Maloobchod \> Nastavení kanálu \> Fiskální integrace \> Technické profily Connector**. Vytvořte nový technický profil konektoru a vyberte konektor, který jste načetli předtím. Aktualizujte nastavení připojení podle potřeby.
6. Přejděte na **Maloobchod \> Nastavení kanálu \> Fiskální integrace \> Skupiny fiskálního konektoru**. Vytvořte novou skupinu fiskálního konektoru pro funkční profil konektoru, který jste vytvořili předtím.
7. Přejděte na **Maloobchod \> Nastavení kanálu \> Fiskální integrace \> Proces fiskální registrace**. Vytvořte nový procesu daňové registrace, krok procesu fiskální registrace a vyberte skupinu fiskálního konektoru, kterou jste předtím vytvořili.
8. Přejděte na **Maloobchod \> Nastavení kanálu \> Nastavení POS \> Profily POS \> Funkční profily**. Vyberte funkční profil, který je připojena k obchodu, kde by měl být aktivován proces registrace. Na pevné záložce **Proces fiskální registrace** vyberte proces fiskální registrace, který jste předtím vytvořili.
9. Přejděte na **Maloobchod \> Nastavení kanálu \> Nastavení POS \> Profily POS \> Hardwarové profily**. Vyberte hardwarový profil spojený s hardwarovou stanicí, ke které bude připojena fiskální tiskárna. Na pevné záložce **Fiskální příslušenství** vyberte technický profil konektoru, který jste vytvořili dříve.
10. Spusťte plán distribuce (**maloobchod \> IT maloobchodu \> plán distribuce**) a vyberte úlohy **1070** a **1090** k přenosu dat do databáze kanálů.

### <a name="production-environment"></a>Produkční prostředí

Předchozí postup umožňuje rozšíření, která jsou součástí ukázky integraci vzorku služby daňové registrace. Kromě toho musíte provést následující postup k vytvoření balíčků pro nasazení, které obsahují komponenty maloobchodu a použití těchto balíčků v produkčním prostředí.

1. Proveďte následující změny v balíčku konfiguračních souborů ve složce **RetailSdk\\Assets**.

    - V konfiguračních souborech **commerceruntime.ext.config** a **CommerceRuntime.MPOSOffline.Ext.config** přidejte následující řádky do části **composition**.

        ``` xml 
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
        ```

    - V konfiguračním souboru **HardwareStation.Extension.config** přidejte následující řádek do oddílu **composition**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        ```

2. Proveďte následující změny v konfiguračním souboru balíčku přizpůsobení **BuildTools\\Customization.settings**.

    - Přidejte následující řádky pro zahrnutí rozšíření CRT do nasaditelných balíčků.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Přidáte následující řádek pro zahrnutí rozšíření hardwarové stanice do balíčků pro nasazení.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample" />
        ```

3. Spuste příkazový řádek MSBuild pro program Visual Studio a spusťte **msbuild** ve složce Retail SDK pro vytvoření balíčků k nasazení.
4. Balíčky použijte pomocí služby Microsoft Dynamics Lifecycle Services (LCS) nebo ručně. Další informace naleznete v tématu [Vytvoření maloobchodních balíčků pro nasazení](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Proveďte všechny požadované úkoly nastavení, které jsou popsány v části [Nastavení maloobchodu pro Českou republiku](#set-up-retail-for-czech-republic).

## <a name="design-of-extensions"></a>Návrh rozšíření

### <a name="commerce-runtime-extension-design"></a>Návrh obchodního rozšíření doby běhu

Účelem rozšíření je, ab poskytovatel daňového dokumentu generoval dokumenty specifické pro službu a zpracovával odpovědi z daňové registrační služby.

Rozšíření CRT je **Runtime.Extensions.DocumentProvider.EFRSample**.

Podrobnější informace o návrhu řešení fiskální integrace získáte v části [Ukázky procesu fiskální registrace pro fiskální zařízení](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).

#### <a name="request-handler"></a>Obslužná rutina požadavku
    
Existuje jedna obslužná rutina požadavku **DocumentProviderEFRFiscalCZE** pro zprostředkovatele dokumentu, která slouží ke generování fiskálních dokumentů pro službu daňové registrace.

Tato rutina je zděděna z rozhraní **INamedRequestHandler**. Metoda **HandlerName** je odpovědná za vrácení názvu obslužné rutiny. Název obslužné rutiny by měl odpovídat názvu poskytovatele dokumentu zprostředkovatele, zadanému v Retail Headquarters.

Konektor podporuje následující požadavky.

- **GetFiscalDocumentDocumentProviderRequest** – tento požadavek obsahuje informace o dokladu, o němž by měl být vygenerován dokument. Vrátí dokument specifický pro službu, který má být registrován ve službě daňové registrace.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – tento požadavek vrací seznam událostí, k jejichž odběru se uživatelé přihlašují. V současné době jsou podporovány tyto události: prodeje, účet zákazníka, vklady a vklady objednávky odběratele.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – tento požadavek vrací odpověď daňové registrační služby. Tato odpověď je serializován tak, aby tvořila řetězec připravený k uložení.

#### <a name="configuration"></a>Konfigurace

Konfigurační soubor **DocumentProviderFiscalEFRSampleCzech** se nachází ve složce **Konfigurace** procesu rozšíření.
Tento soubor slouží k povolení nastavení pro zprostředkovatele dokumentu ke konfiguraci z Retail Headquarters. Formát souboru je v souladu s požadavky na konfiguraci fiskální integrace. Jsou přidána následující nastavení.

- Mapování sazeb DPH
- Výchozí skupina DPH
- Skupina DPH zálohy

### <a name="hardware-station-extension-design"></a>Design rozšíření hardwarové stanice

Účelem rozšíření je fiskální konektor určený ke komunikaci se službou daňové registrace.

Rozšíření hardwarové stanice je **HardwareStation.Extension.EFRSample**. Rozšíření hardwarové stanice používá protokol HTTP k odesílání dokumentů, které rozšíření  CRT generuje pro daňovou registrační službu. Také zpracovává odpovědi, které jsou přijaty ze služby daňové registrace.

#### <a name="request-handler"></a>Obslužná rutina požadavku

Obslužná rutina požadavku **EFRHandler** je vstupní bod pro práci s požadavky služby daňové registrace.

Tato rutina je zděděna z rozhraní **INamedRequestHandler**. Metoda **HandlerName** je odpovědná za vrácení názvu obslužné rutiny. Název obslužné rutiny by měl odpovídat názvu poskytovatele dokumentu fiskálního konektoru zadanému v Retail Headquarters.

Konektor podporuje následující požadavky.

- **SubmitDocumentFiscalDeviceRequest** – tento požadavek odesílá dokumenty službě daňové registrace a z ní vrátí odpověď.
- **IsReadyFiscalDeviceRequest** – tento požadavek se používá pro kontrolu stavu služby daňové registrace.
- **InitializeFiscalDeviceRequest** – tento požadavek se používá pro inicializaci stavu služby daňové registrace.

#### <a name="configuration"></a>Konfigurace

Konfigurační soubor se nachází ve složce **Konfigurace** projektu rozšíření. Tento soubor slouží k povolení nastavení pro fiskální konektor ke konfiguraci z Retail Headquarters. Formát souboru je v souladu s požadavky na konfiguraci fiskální integrace. Jsou přidána následující nastavení.

- **Adresa koncového bodu** – adresa URL služby daňové registrace.
- **Časový limit** – doba v milisekundách, po kterou bude čekat ovladač na odpověď od služby daňové registrace.
