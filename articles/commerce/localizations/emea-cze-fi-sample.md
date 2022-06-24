---
title: Ukázka integrace fiskální služby pro Českou republiku
description: V tomto článku je uveden přehled fiskální integrace pro Českou republiku v Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-4-1
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: d255b03242a4cb7a72cef1e8e6fab901ecf953e6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910491"
---
# <a name="fiscal-registration-service-integration-sample-for-the-czech-republic"></a>Ukázka integrace fiskální služby pro Českou republiku

[!include[banner](../includes/banner.md)]

V tomto článku je uveden přehled fiskální integrace pro Českou republiku v Microsoft Dynamics 365 Commerce.

Pro účely splnění fiskálních požadavků na registrační pokladny v České republice obsahuje funkce Dynamics 365 Commerce pro Českou republiku vzorovou integraci pokladního místa (POS) s externí fiskální registrační službou. Vzorek rozšiřuje [funkci fiskální integrace](fiscal-integration-for-retail-channel.md). Je založena na řešení [EFR (Electronic Fiscal Register)](https://efsta.org/sicherheitsloesungen/) od [EFSTA](https://efsta.org/) a umožňuje komunikaci se službou EFR přes protokol HTTPS. Služba EFR zajišťuje elektronickou registraci prodeje (EET - Elektronická evidence tržeb), tj. online převodu prodejních údajů do fiskální webové služby daňových úřadů.

Služba EFR by měla být hostována hardwarovou stanicí Commerce nebo samostatným počítačem, se kterým se lze propojit z hardwarové stanice. Ukázka je poskytnuta ve formě zdrojového kódu a je součástí sady software development kit (SDK) pro maloobchod.

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

### <a name="gift-cards"></a>Dárkové poukazy

Ukázka integrace daňové registrační služby implementuje následující pravidla související s dárkovými poukazy.

- Řádky prodeje, které souvisejí s operacemi *Vydat dárkový poukaz* nebo *Přidat k dárkovému poukazu* v prodejních transakcích jsou označeny zvláštním atributem při registraci transakce v daňové registrační službě.
- Platba dárkovým poukazem je považována za běžnou platbu a je označena zvláštním atributem při registraci transakce ve službě daňové registrace

### <a name="customer-account-deposits-and-customer-order-deposits"></a>Vklady na účet odběratele a vklady objednávky odběratele

Ukázka integrace daňové registrační služby implementuje následující pravidla, která souvisí s vklady na účtu odběratele a vklady objednávky odběratelů.

- Transakce související s vkladem na účet odběratele nebo je vklad objednávky zákazníka registrována ve službě daňové registrace jako samostatný řádek transakce a je označen zvláštním atributem. Skupina DPH zálohy je zadána v tomto řádku.
- Při vytvoření hybridní objednávky odběratele, tedy objednávky odběratele, která obsahuje produkty, které lze převést mimo obchod odběratelem a k produktům, které budou vyzvednuty nebo expedovány, obsahuje transakce registrovaná ve službě daňové registrace obsahuje řádky pro produkty, které jsou prováděny, a také řádku objednávky vkladu.
- Platba z účtu zákazníka je považována za běžnou platbu a je označena zvláštním atributem při registraci transakce ve službě daňové registrace
- Částka vkladu objednávky odběratele použitá na objednávce odběratele v operaci Vyzvednout je považována za běžnou platbu a je označena zvláštním atributem při registraci transakce daňové registrace služby.

### <a name="offline-registration"></a>Offline registrace

Pokud se nezdaří službě daňové registrace přenášet data transakce fiskálních webové služby finančního úřadu (například z důvodu limitu odezvy) a chcete dostat potvrzení z webové služby (to znamená fiskální identifikační kód transakce), generuje místní podpis transakce a zahrne ho jako speciální kód chyby v odpovědi. Služba daňové registrace znovu odešle transakce v původní objednávce na pozadí ihned po obnovení síťového připojení.

### <a name="limitations-of-the-sample"></a>Omezení vzorku

Služba daňové registrace podporuje pouze scénáře, kde je součástí ceny daň z prodeje. Proto musí být možnost **Ceny zahrnují DPH** nastavena na **Ano** pro obchody a odběratele.

## <a name="set-up-commerce-for-the-czech-republic"></a>Natavení aplikace Commerce pro Českou republiku

Tato část popisuje nastavení Commerce, která jsou specifická a doporučená pro Českou republiku. Další informace naleznete v tématu [Domovská stránka Commerce](../index.md).

Chcete-li použít funkci specifickou pro Českou republiku, je nutné zadat následující nastavení.

- V primární adrese právnické osoby nastavte pole **země/oblasti** na **CZE** (Česká republika).
- V profilu funkce POS každého obchodu, který se nachází v rámci České republiky, nastavte pole **kód ISO** na **CZ** (Česká republika).

Zadejte také následující nastavení pro Českou republiku. Po dokončení instalace musíte spustit příslušné distribuční úlohy.

### <a name="set-up-vat-per-czech-republic-requirements"></a>Nastavení DPH dle požadavků pro Českou republiku


Musíte vytvořit kódy DPH, skupiny daní DPH a skupiny DPH za zboží. Musíte také nastavit informace o DPH pro produkty a služby. Další informace o způsobu nastavení a použití funkcí DPH získáte v části [Přehled DPH](../../finance/general-ledger/indirect-taxes-overview.md).

### <a name="set-up-stores"></a>Nastavení obchodů

Na stránce **Všechny obchody** aktualizujte podrobnosti o obchodu. Je nutné konkrétně nastavit následující parametry.

- V poli **Skupina DPH** zadejte skupinu DPH, kterou chcete použít pro prodeje výchozímu odběrateli.
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
| cs       | 900003  | PKP                    |
| cs       | 900004  | FIK                    |
| cs       | 900005  | Informace                   |
| cs       | 900006  | Pořadové číslo        |

Na stránce **Vlastní pole** přidejte následující záznamy popisků vlastního pole rozvržení účtenky. Upozorňujeme, že hodnoty **ID textu titulku** musí odpovídat hodnotám **ID textu**, které jste zadali na stránce **jazykový text**:

| Název                 | Typ    | ID textu titulku |
|----------------------|---------|-----------------|
| TLT                  | Účtenka | 900001          |
| SEC                  | Účtenka | 900002          |
| SIGN                 | Účtenka | 900003          |
| FISCAL               | Účtenka | 900004          |
| INFO                 | Příjemka | 900005          |
| CONTINUOUSNUMBER     | Příjemka | 900006          |

> [!NOTE]
> Je důležité, abyste zadali správné názvy vlastních polí, jak jsou uvedeny v předcházející tabulce. Nesprávný název vlastního pole způsobí chybějící data v příjemkách.

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

Další informace o tom, jak pracovat s formáty příjemek, naleznete v tématu [Nastavení a návrh formátů příjmu](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-the-czech-republic"></a>Nastavení fiskální integrace pro Českou republiku

Ukázka integrace služby fiskální registrace pro Českou republiku je založena na [funkci fiskální integrace](fiscal-integration-for-retail-channel.md) a je součástí řešení Retail SDK. Ukázka se nachází ve složce **src\\FiscalIntegration\\Efr** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (například [ukázka ve verzi/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Ukázka [se skládá](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) ze zprostředkovatele fiskálního dokumentu, což je rozšíření řešení Commerce Runtime (CRT) a fiskálního konektoru, který je rozšířením hardwarové stanice Commerce. Další informace o použití sady Retail SDK naleznete v části [Architektura Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) a [Nastavení kanálu sestavení pro sadu SDK nezávislého balení](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Kvůli omezením [nového modelu nezávislého balíčku a rozšíření](../dev-itpro/build-pipeline.md) jej v současné době nelze pro tuto ukázku fiskální integrace použít. Musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači (VM) v Microsoft Dynamics Lifecycle Services (LCS). Další informace viz [Pokyny k nasazení ukázkové fiskální integrace pro Českou republiku (starší verze)](emea-cze-fi-sample-sdk.md).
>
> Podpora nového modelu nezávislého balení a rozšíření pro vzorky fiskální integrace je plánována pro pozdější verze.

Postupujte podle kroků pro nastavení fiskální integrace popsané v části [Nastavení fiskální integrace pro kanály Commerce](setting-up-fiscal-integration-for-retail-channel.md):

1. [Nastavení procesu fiskální registrace](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Kromě toho si všimněte nastavení pro proces fiskální registrace, který je [specifický pro tuto ukázku služby fiskální registrace](#set-up-the-registration-process).
1. [Nastavení zpracování chyb](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Povolit ruční provedení zápisu odložené daňové registrace](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurace komponent kanálu](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Nastavení procesu registrace

Pokud chcete povolit registrační proces, postupujte pomocí následujících kroků pro nastavení centrály Commerce. Další informace viz [Nastavení fiskální integrace pro obchodní kanály](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Stáhněte si konfigurační soubory pro poskytovatele fiskálních dokumentů a fiskální konektor:

    1. Otevřete úložiště [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Vyberte správnou verzi větve vydání podle vaší verze SDK/aplikace (například **[vydání/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Otevřete **src \> FiscalIntegration \> Efr**.
    1. Stáhněte si konfigurační soubor poskytovatele fiskálních dokumentů v umístění **Configurations \> DocumentProviders \> DocumentProviderFiscalEFRSampleCzech.xml** (například [soubor k vydání/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleCzech.xml)).
    1. Stáhněte si konfigurační soubor fiskálního konektoru v umístění **Configurations \> Connectors \> ConnectorEFRSample.xml** (například [soubor k vydání/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Kvůli omezením [nového modelu nezávislého balíčku a rozšíření](../dev-itpro/build-pipeline.md) jej v současné době nelze pro tuto ukázku fiskální integrace použít. Musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači v LCS. Konfigurační soubory pro tuto ukázku fiskální integrace jsou umístěny v následujících složkách Retail SDK na vývojářském virtuálním počítači v LCS:
    >
    > - **Konfigurační soubor poskytovatele fiskálních dokkumentů:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration\\DocumentProviderFiscalEFRSampleCzech.xml
    > - **Konfigurační soubor fiskálního konektoru:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration\\ConnectorEFRSample.xml
    > 
    > Podpora nového modelu nezávislého balení a rozšíření pro vzorky fiskální integrace je plánována pro pozdější verze.

1. Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry \> Sdílené parametry obchodu**. Na kartě **Obecné** nastavte možnost **Povolit fiskální integraci** na **Ano**.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Poskytovatelé fiskálních dokumentů** a načtěte konfigurační soubor poskytovatele fiskálního dokumentu, který jste stáhli dříve.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Fiskální konektory** a načtěte konfigurační soubor fiskálního konektoru, který jste stáhli dříve.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Funkční profily Connector**. Vytvořte nový funkční profil konektoru. Vyberte poskytovatele dokumentu a dříve načtený konektor. Podle potřeby aktualizujte [nastavení mapování dat](#default-data-mapping).
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Technické profily Connector**. Vytvořte nový technický profil konektoru a vyberte fiskální konektor, který jste načetli předtím. Podle potřeby aktualizujte [nastavení konektoru](#fiscal-connector-settings).
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Skupiny fiskálního konektoru**. Vytvořte novou skupinu fiskálního konektoru pro funkční profil konektoru, který jste vytvořili předtím.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Proces fiskální registrace**. Vytvořte nový procesu daňové registrace a krok procesu fiskální registrace a vyberte skupinu fiskálního konektoru, kterou jste předtím vytvořili.
1. Přejděte na **Maloobchodní a velkoobchodní prodej \> Instalace kanálu \> Nastavení POS \> Profily POS \> Funkční profily**. Vyberte funkční profil, který je připojena k obchodu, kde by měl být aktivován proces registrace. Na pevné záložce **Proces fiskální registrace** vyberte proces fiskální registrace, který jste předtím vytvořili.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Nastavení POS \> Profily POS \> Hardwarové profily**. Vyberte hardwarový profil spojený s hardwarovou stanicí, ke které bude připojena fiskální tiskárna. Na pevné záložce **Fiskální příslušenství** vyberte technický profil konektoru, který jste vytvořili dříve.
1. Spusťte plán distribuce (**Retail a Commerce \> IT Retail a Commerce \> plán distribuce**) a vyberte úlohy **1070** a **1090** k přenosu dat do databáze kanálů.

#### <a name="default-data-mapping"></a>Výchozí mapování dat

Následující výchozí mapování dat je součástí konfigurace poskytovatele fiskálního dokumentu, který je poskytován jako ukázka fiskální integrace:

- **Mapování sazeb daně z přidané hodnoty (DPH).** – Mapování procentních hodnot daně, které jsou nastaveny pro kódy daně z prodeje, na atribut **TaxG** (daňová skupina) v požadavcích zasílaných fiskální službě. Zde je výchozí mapování:

    ```
    A: 21.00; B: 15.00; C: 10.00; Z: 0.00
    ```

    První složka v každém páru představuje daňovou skupinu DPH, která je podporována službou fiskální registrace EFR. Druhá složka představuje odpovídající sazbu DPH. Další informace o skupinách DPH, které EFR podporuje pro Českou republiku, viz [Reference k EFR](https://public.efsta.net/efr/).

- **Výchozí mapování skupiny DPH** – Jakékoli částky DPH, které nelze mapovat na některou z předem určených skupin DPH, budou připsány výchozí (základní) skupině DPH. Zde je výchozí mapování:

    ```
    A
    ```

- **Mapování skupiny DPH vkladu** – Částky zálohy odběratele a zálohy objednávky odběratele budou připsány skupině DPH zálohy. Zde je výchozí mapování:

    ```
    Z
    ```

#### <a name="fiscal-connector-settings"></a>Nastavení fiskálního konektoru

Následující nastavení jsou součástí konfigurace fiskálního konektoru, který je poskytován jako ukázka fiskální integrace:

- **Adresa koncového bodu** – adresa URL služby daňové registrace.
- **Časový limit** – doba v milisekundách, po kterou bude fiskální konektor čekat na odpověď ze služby fiskální registrace.

### <a name="configure-channel-components"></a>Konfigurace komponent kanálu

> [!WARNING]
> Kvůli omezením [nového modelu nezávislého balíčku a rozšíření](../dev-itpro/build-pipeline.md) jej v současné době nelze pro tuto ukázku fiskální integrace použít. Musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači v LCS. Další informace viz [Pokyny k nasazení ukázkové fiskální integrace pro Českou republiku (starší verze)](emea-cze-fi-sample-sdk.md).
>
> Podpora nového modelu nezávislého balení a rozšíření pro vzorky fiskální integrace je plánována pro pozdější verze.

#### <a name="set-up-the-development-environment"></a>Nastavení vývojového prostředí

Tento postup slouží k nastavení vývojového prostředí, abyste mohli testovat a rozšířit ukázku.

1. Naklonujte nebo stáhněte úložiště [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions). Vyberte správnou verzi větve vydání podle vaší verze SDK/aplikace. Další informace viz [Stažení ukázek Retail SDK a referenčních balíčků z GitHub a NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Otevřete řešení EFR v umístění **Dynamics365Commerce.Solutions\\FiscalIntegration\\Efr\\EFR.sln** a sestavte jej.
1. Nainstalujte rozšíření CRT:

    1. Vyhledejte instalační program rozšíření CRT:

        - **Commerce Scale Unit:** Ve složce **Efr\\ScaleUnit\\ScaleUnit.EFR.Installer\\bin\\Debug\\net461** vyhledejte instalační program **ScaleUnit.EFR.Installer**.
        - **Místní CRT v Modern POS:** Ve složce **Efr\\ModernPOS\\ModernPOS.EFR.Installer\\bin\\Debug\\net461** vyhledejte instalační program **ModernPOS.EFR.Installer**.

    1. Spusťte instalační program rozšíření CRT z příkazového řádku:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **Místní CRT v Modern POS:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. Instalace rozšíření fiskálních konektorů:

    Rozšíření fiskálního konektoru můžete nainstalovat na [hardwarové stanici](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) nebo [registru POS](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

    1. Instalace rozšíření hardwarové stanice:

        1. Ve složce **Efr\\HardwareStation\\HardwareStation.EFR.Installer\\bin\\Debug\\net461** vyhledejte instalační program **HardwareStation.EFR.Installer**.
        1. Spusťte instalační program rozšíření z příkazového řádku spuštěním následujícího příkazu.

            ```Console
            HardwareStation.EFR.Installer.exe install --verbosity 0
            ```

    1. Nainstalujte rozšíření POS:

        1. Otevřete vzorové řešení fiskálního konektoru POS na adrese **Dynamics365Commerce.Solutions\\FiscalIntegration\\PosFiscalConnectorSample\\Contoso.PosFiscalConnectorSample.sln** a sestavte ho.
        1. Ve složce **PosFiscalConnectorSample\\StoreCommerce.Installer\\bin\\Debug\\net461** vyhledejte instalační program **Contoso.PosFiscalConnectorSample.StoreCommerce.Installer**.
        1. Spusťte instalační program rozšíření z příkazového řádku spuštěním následujícího příkazu.

            ```Console
            Contoso.PosFiscalConnectorSample.StoreCommerce.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>Produkční prostředí

Postupujte podle kroků v části [Nastavení kanálu buildu pro ukázku fiskální integrace](fiscal-integration-sample-build-pipeline.md), kterými vygenerujete a uvolníte nasaditelné balíčky Cloud Scale Unit a samoobslužné nasaditelné balíčky pro ukázku fiskální integrace. Soubor YAML šablony **EFR build-pipeline.yml** se nachází ve složce **Pipeline\\YAML_Files** úložiště [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-extensions"></a>Návrh rozšíření

Ukázka integrace služby fiskální registrace pro Českou republiku je založena na [funkci fiskální integrace](fiscal-integration-for-retail-channel.md) a je součástí řešení Retail SDK. Ukázka se nachází ve složce **src\\FiscalIntegration\\Efr** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (například [ukázka ve verzi/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Ukázka [se skládá](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) ze zprostředkovatele fiskálního dokumentu, což je rozšíření řešení CRT a fiskálního konektoru, který je rozšířením hardwarové stanice Commerce. Další informace o použití sady Retail SDK naleznete v části [Architektura Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) a [Nastavení kanálu sestavení pro sadu SDK nezávislého balení](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Kvůli omezením [nového modelu nezávislého balíčku a rozšíření](../dev-itpro/build-pipeline.md) jej v současné době nelze pro tuto ukázku fiskální integrace použít. Musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači v LCS. Další informace viz [Pokyny k nasazení ukázkové fiskální integrace pro Českou republiku (starší verze)](emea-cze-fi-sample-sdk.md). Podpora nového modelu nezávislého balení a rozšíření pro vzorky fiskální integrace je plánována pro pozdější verze.

### <a name="commerce-runtime-extension-design"></a>Návrh obchodního rozšíření doby běhu

Účelem rozšíření je, ab poskytovatel daňového dokumentu generoval dokumenty specifické pro službu a zpracovával odpovědi z daňové registrační služby.

#### <a name="request-handler"></a>Obslužná rutina požadavku

Existuje jedna obslužná rutina požadavku **DocumentProviderEFRFiscalCZE** pro zprostředkovatele dokumentu, která slouží ke generování fiskálních dokumentů pro službu daňové registrace.

Tato rutina je zděděna z rozhraní **INamedRequestHandler**. Metoda **HandlerName** je odpovědná za vrácení názvu obslužné rutiny. Název obslužné rutiny by měl odpovídat názvu poskytovatele dokumentu zprostředkovatele zadanému v centrále Commerce.

Konektor podporuje následující požadavky.

- **GetFiscalDocumentDocumentProviderRequest** – tento požadavek obsahuje informace o dokladu, o němž by měl být vygenerován dokument. Vrátí dokument specifický pro službu, který má být registrován ve službě daňové registrace.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – tento požadavek vrací seznam událostí, k jejichž odběru se uživatelé přihlašují. V současné době jsou podporovány tyto události: prodeje, účet zákazníka, vklady a vklady objednávky odběratele.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – tento požadavek vrací odpověď daňové registrační služby. Tato odpověď je serializován tak, aby tvořila řetězec připravený k uložení.

#### <a name="configuration"></a>Konfigurace

Konfigurační soubor pro poskytovatele fiskálních dokumentů se nachází v umístění **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders\\DocumentProviderFiscalEFRSampleCzech.xml** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Tento soubor slouží k povolení konfigurace nastavení zprostředkovatele fiskálního dokumentu z centrály Commerce. Formát souboru je v souladu s požadavky na konfiguraci fiskální integrace.

### <a name="hardware-station-extension-design"></a>Design rozšíření hardwarové stanice

Účelem rozšíření je fiskální konektor určený ke komunikaci se službou daňové registrace. Rozšíření hardwarové stanice používá protokol HTTP k odesílání dokumentů, které rozšíření  CRT generuje pro daňovou registrační službu. Také zpracovává odpovědi, které jsou přijaty ze služby daňové registrace.

#### <a name="request-handler"></a>Obslužná rutina požadavku

Obslužná rutina požadavku **EFRHandler** je vstupní bod pro práci s požadavky služby daňové registrace.

Tato rutina je zděděna z rozhraní **INamedRequestHandler**. Metoda **HandlerName** je odpovědná za vrácení názvu obslužné rutiny. Název obslužné rutiny by měl odpovídat názvu poskytovatele dokumentu fiskálního konektoru zadanému v centrále Commerce.

Konektor podporuje následující požadavky.

- **SubmitDocumentFiscalDeviceRequest** – tento požadavek odesílá dokumenty službě daňové registrace a z ní vrátí odpověď.
- **IsReadyFiscalDeviceRequest** – tento požadavek se používá pro kontrolu stavu služby daňové registrace.
- **InitializeFiscalDeviceRequest** – tento požadavek se používá pro inicializaci stavu služby daňové registrace.

#### <a name="configuration"></a>Konfigurace

Konfigurační soubor pro fiskální konektor se nachází v umístění **src\\FiscalIntegration\\Efr\\Configurations\\Connectors\\ConnectorEFRSample.xml** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repository. Tento soubor slouží k povolení nastavení pro fiskální konektor ke konfiguraci z centrály Commerce. Formát souboru je v souladu s požadavky na konfiguraci fiskální integrace.

### <a name="pos-fiscal-connector-extension-design"></a>Návrh rozšíření fiskálních konektorů POS

Účelem rozšíření fiskálního konektoru POS je komunikace se službou daňové registrace z POS. Ke komunikaci využívá protokol HTTPS.

#### <a name="fiscal-connector-factory"></a>Továrna fiskálního konektoru

Továrna fiskálního konektoru mapuje název konektoru na implementaci fiskálního konektoru a je umístěna v souboru **Pos.Extension\\Connectors\\FiscalConnectorFactory.ts**. Název konektoru musí odpovídat názvu poskytovatele dokumentu fiskálního konektoru zadanému v centrále Commerce.

#### <a name="efr-fiscal-connector"></a>Fiskální konektor EFR

Fiskální konektor EFR je umístěn v souboru **Pos.Extension\\Connectors\\Efr\\EfrFiscalConnector.ts**. Implementuje rozhraní **IFiscalConnector**, které podporuje následující požadavky:

- **FiscalRegisterSubmitDocumentClientRequest** – tento požadavek odesílá dokumenty službě daňové registrace a z ní vrátí odpověď.
- **FiscalRegisterIsReadyClientRequest** – tento požadavek se používá pro kontrolu stavu služby daňové registrace.
- **FiscalRegisterInitializeClientRequest** – tento požadavek se používá pro inicializaci stavu služby daňové registrace.

#### <a name="configuration"></a>Konfigurace

Konfigurace se nachází ve složce **src\\FiscalIntegration\\Efr\\Configurations\\Connectors** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Tento soubor slouží k povolení nastavení pro fiskální konektor ke konfiguraci z centrály Commerce. Formát souboru je v souladu s požadavky na konfiguraci fiskální integrace. Jsou přidána následující nastavení:

- **Adresa koncového bodu** – adresa URL služby daňové registrace.
- **Časový limit** – doba v milisekundách (ms), po kterou bude čekat konektor na odpověď od služby daňové registrace.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
