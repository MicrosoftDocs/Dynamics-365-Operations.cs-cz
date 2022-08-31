---
title: Ukázka integrace fiskální služby pro Rakousko
description: V tomto článku je uveden přehled ukázkové fiskální integrace pro Rakousko v Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 08/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: da4deb37b260ffa2a68e2a36aef01965cbf098b2
ms.sourcegitcommit: 0feb5d0b06e04f99903069ff2801577be86b8555
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/18/2022
ms.locfileid: "9313794"
---
# <a name="fiscal-registration-service-integration-sample-for-austria"></a>Ukázka integrace fiskální služby pro Rakousko

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

V tomto článku je uveden přehled ukázkové fiskální integrace pro Rakousko v Microsoft Dynamics 365 Commerce.

Pro účely splnění fiskálních požadavků na registrační pokladny v Rakousku obsahuje funkce Dynamics 365 Retail pro Rakousko vzorovou integraci pokladního místa (POS) s externí fiskální registrační službou. Vzorek rozšiřuje [funkci fiskální integrace](fiscal-integration-for-retail-channel.md). Je založena na řešení [EFR (Electronic Fiscal Register)](https://www.efsta.eu/at/fiskalloesungen/oesterreich) od [EFSTA](https://www.efsta.eu/at/) a umožňuje komunikaci se službou EFR přes protokol HTTPS. Služba EFR by měla být hostitelem hardwarové stanice pro maloobchod nebo samostatný počítač, se kterým se lze propojit z hardwarové stanice. Ukázka je poskytnuta ve formě zdrojového kódu a je součástí sady Retail software development kit (SDK).

Společnost Microsoft nevydává žádný hardware, software nebo dokumentaci k EFSTA. Informace o tom, jak řešení EFR získat a provozovat, vám poskytne [EFSTA](https://www.efsta.eu/at/kontakt).

## <a name="scenarios"></a>Scénáře

Následující scénáře uvádějí ukázku integrace fiskální registrační služby pro Rakousko.

- Registrace transakcí v hotovosti ve službě daňové registrace:

    - Odešlete podrobná data transakce do služby daňové registrace. Tyto údaje obsahují informace o řádku prodeje a informace o slevách, platbách a daních
    - Zaznamenejte odpověď z daňové registrační služby. Tato odpověď obsahuje digitální podpis a odkaz na registrovanou transakci.
    - Registrace daní a jejich mapování na daňové kódy služby fiskální registrace.
    - Vytisknutí kódu QR pro registrovanou transakci na příjemce.

- Registrace operací dárkových poukazů a vkladů odběratelů jako nehotovostních transakcí ve službě fiskální registrace:

    - Vydejte nebo přidejte peníze na dárkový poukaz.
    - Zaregistrujte vklad na účet odběratele.
    - Registrace vkladu na objednávku odběratele.

- Registrace neprodejních transakcí a událostí jako nehotovostních transakcí ve službě fiskální registrace:

    - Otevření a zavření směny
    - Počáteční částka, zadání plovoucího zůstatku a odstranění úhrady
    - Přepsání ceny
    - Přepsání daně
    - Tisknout kopii účtenky
    - Otevřít zásuvku
    - Tisknout sestavu X
    - Tisknout sestavu Z

- Tisk výpisů na konci dne (sestavy X/Z), které mají pole specifická pro Rakousko:

    - Celkový počet produktů nebo služeb, které byly dodány zákazníkům
    - Rozpis tržeb podle daňové sazby
    - Rozpis plateb podle pokladníka / obsluhy pokladny
    - Cenové slevy a vratky, které snižují denní prodeje
    - Nulové prodeje (dárky)

- Zpracování chyb, jako jsou následující možnosti:

    - Opakujte fiskální registraci, pokud to je možné, například když není k dispozici služba fiskální registrace, není připravena nebo nereaguje.
    - Odložte fiskální registraci.
    - Přeskočte daňovou registraci nebo označte transakci jako registrovanou a zahrňte informační kódy pro zaznamenání důvodu chyby a dalších informací.
    - Zkontrolujte dostupnost služby daňové registrace, dříve než otevřete novou transakci prodeje nebo ji dokončíte.

### <a name="gift-cards"></a>Dárkové poukazy

Ukázka integrace daňové registrační služby implementuje následující pravidla související s dárkovými poukazy:

- Vyloučení řádků prodeje, které souvisejí s operacemi *Vydání dárkového poukazu* a *Přidání na dárkový poukaz* z hotovostní transakce. Registrace těchto řádků jako samostatné bezhotovostní transakce ve službě fiskální registrace namísto jejich registrace jako součásti hotovostní transakce.
- Nevytištění rozpisu daňové skupiny a QR kódu, pokud příjemka obsahuje pouze řádky dárkového poukazu.
- Vytištění celkové částky dárkových poukazů, které jsou vydány nebo znovu účtovány v transakci, odděleně od částky hotovostní transakce na příjemce.
- Uložení vypočítaných úprav plateb do databáze kanálů s odkazem na odpovídající fiskální transakci.
- Platba dárkovým poukazem je považována za běžnou platbu.

### <a name="customer-deposits-and-customer-order-deposits"></a>Vklady odběratele a vklady objednávky odběratele

Ukázka integrace daňové registrační služby implementuje následující pravidla, která souvisí s vklady odběratele a vklady objednávky odběratelů:

- Registrace bezhotovostní transakce, pokud je transakce vkladem odběratele.
- Registrace bezhotovostní transakce, pokud transakce obsahuje pouze vklad objednávky odběratele nebo refundaci vkladu objednávky odběratele.
- Odečtení částky zálohy na objednávce odběratele z platebních řádků, když je vytvořena hybridní objednávka odběratele.
- Uložení vypočítaných úprav plateb do databáze kanálů s odkazem na fiskální transakci pro hybridní zákaznickou objednávku.

### <a name="limitations-of-the-sample"></a>Omezení vzorku

Služba daňové registrace podporuje pouze scénáře, kde je součástí ceny daň z prodeje. Proto musí být možnost **Ceny zahrnují DPH** nastavena na **Ano** pro obchody a odběratele.

## <a name="set-up-commerce-for-austria"></a>Natavení aplikace Commerce pro Rakousko

Tato část popisuje nastavení Commerce, která jsou specifická a doporučená pro Rakousko. Další informace o nastavení naleznete v tématu [Domovská stránka Commerce](../index.md).

Chcete-li použít funkci specifickou pro Rakousko, je nutné zadat následující nastavení:

- V primární adrese právnické osoby nastavte pole **Země/oblast** na **AUT** (Rakousko).
- V profilu funkce POS každého obchodu, který se nachází v rámci Rakouska, nastavte pole **kód ISO** na **AT** (Rakousko).

Zadejte také následující nastavení pro Rakousko. Po dokončení instalace musíte spustit příslušné distribuční úlohy.

### <a name="enable-features-for-austria"></a>Povolit funkce pro Rakousko

V pracovním prostoru **Správa funkcí** musíte povolit následující funkce:

- (Rakousko) Povolit další události auditu v POS
- (Rakousko) Povolit dodatečné informace ve výpisech na konci dne v POS

### <a name="set-up-vat-per-austrian-requirements"></a>Nastavení DPH podle rakouských požadavků

Musíte vytvořit kódy DPH, skupiny daní DPH a skupiny DPH za zboží. Musíte také nastavit informace o DPH pro produkty a služby. Další informace o způsobu nastavení a použití funkcí DPH získáte v části [Přehled DPH](../../finance/general-ledger/indirect-taxes-overview.md).

Na příjemky můžete vytisknout zkrácený kód daně z obratu (například „A“ nebo „B“). Chcete-li tuto funkci zpřístupnit, nastavte pole **Kód tisku** na stránce **Kódy DPH**.

### <a name="set-up-stores"></a>Nastavení obchodů

Na stránce **Všechny obchody** aktualizujte podrobnosti o obchodu. Je nutné konkrétně nastavit následující parametry:

- V poli **Skupina DPH** zadejte skupinu DPH, kterou chcete použít pro prodeje výchozímu odběrateli.
- Nastavte možnost **Ceny jsou včetně DPH** na **Ano**.
- V poli **název** zadejte název společnosti. Tato změna pomáhá zajistit, že se název společnosti zobrazí na dokladu o prodeji. Případně můžete přidat název společnosti na prodejní doklad jako volný text.
- Nastavte **daňové identifikační číslo (DIČ)** na identifikační číslo společnosti. Tato změna pomáhá zajistit, že se identifikační číslo společnosti zobrazí na dokladu o prodeji. Případně můžete přidat identifikační číslo společnosti na prodejní doklad jako volný text.

### <a name="set-up-functionality-profiles"></a>Nastavení funkčních profilů

Nastavte funkční profily POS:

- Na pevné záložce **Číslování dokladů** nastavte číslování dokladů vytvořením nebo aktualizací záznamů pro typy příjmových transakcí **Prodej**, **Prodejní objednávka** a **Vrácení**.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Nakonfigurujte vlastní pole tak, aby bylo možné použít je ve formátech příjemky pro prodejní příjemky

Můžete konfigurovat jazykový text a vlastní pole, která se používají ve formátech příjemky POS. Výchozí společnost uživatele, který vytvoří nastavení příjmu, musí být stejná právnická osoba, pro kterou se vytváří nastavení text jazyka. Alternativně lze vytvořit texty ve stejném jazyce, které mají být vytvořeny ve výchozí společnosti uživatele a právnické osobě prodejny, pro kterou se nastavení vytváří.

Na stránce **jazykový text** přidejte následující záznamy popisků vlastního pole rozvržení účtenky. Upozorňujeme, že hodnoty **ID jazyka**, **ID textu** a **Text**, které jsou zobrazeny v tabulce, jsou jenom příklady. Lze je změnit tak, aby splňovaly vaše požadavky. Hodnoty **ID textu**, které budete používat, však musí být jedinečné a musí být rovny nebo větší než 900001.

Přidejte následující štítky POS do oddílu **POS** v poli **Jazykový text** z tabulky:

| ID jazyka | ID textu | Text                      |
|-------------|---------|---------------------------|
| cs       | 900001  | QR kód                   |
| cs       | 900002  | Průběžné číslo         |
| cs       | 900003  | Tiskový kód maloobchodní daně     |
| cs       | 900004  | Celkem (prodej)             |
| cs       | 900005  | Celková daň (prodej)         |
| cs       | 900006  | Celková částka včetně daně (prodej) |
| cs       | 900007  | Částka daně (prodej)        |
| cs       | 900008  | Daňový základ (prodej)         |

Na stránce **Vlastní pole** přidejte následující záznamy popisků vlastního pole rozvržení účtenky. Upozorňujeme, že hodnoty **ID textu titulku** musí odpovídat hodnotám **ID textu**, které jste zadali na stránce **jazykový text**:

| Název                 | Typ    | ID textu titulku |
|----------------------|---------|-----------------|
| QRCODE               | Příjemka | 900001          |
| CONTINUOUSNUMBER     | Příjemka | 900002          |
| RETAILPRINTCODE      | Příjemka | 900003          |
| SALESTOTAL           | Příjemka | 900004          |
| SALESTOTALTAX        | Příjemka | 900005          |
| SALESTOTALINCLUDETAX | Příjemka | 900006          |
| SALESTAXAMOUNT       | Příjemka | 900007          |
| SALESTAXBASIS        | Příjemka | 900008          |

> [!NOTE]
> Je důležité, abyste zadali správné názvy vlastních polí, jak jsou uvedeny v předcházející tabulce. Nesprávný název vlastního pole způsobí chybějící data v příjemkách.

### <a name="configure-receipt-formats"></a>Konfigurace formátů příjemky

Pro každý požadovaný formát příjemky změňte hodnotu pole **Chování tisku** na **vždy tisknout**.

V Návrháři formátu příjemky přidejte následující vlastní pole do příslušných oddílů příjemky. Všimněte si, že názvy polí odpovídají jazykovým textům, které jste definovali v předchozím oddílu.

- **Záhlaví:** Přidejte následující pole:

    - Pole **Název obchodu** a **Daňové identifikační číslo**, která umožňují vytisknout na příjemky název a identifikační číslo společnosti. Případně můžete přidat název společnosti a číslo identity do rozvržení jako volný text.
    - Pole **Adresa obchodu**, **Datum**, **Čas 24H**, **Číslo příjemky**, a **Číslo registrační pokladny**.
    - Pole **Průběžné číslo**, která identifikují počet hotovostních transakcí daňové registrace služby.

- **Řádky:** Přidejte následující pole:

    - **Název položky**
    - **Množ**.
    - **Celková cena s daní**
    - Pole **Tiskový kód maloobchodní daně**, které slouží k vytištění zkráceného kódu, který odpovídá kódu DPH, který se vztahuje k položce.

- **Zápatí:** Přidejte následující pole:

    - Pole platby, aby se vytiskly částky platby pro každou metodu platby. Například přidejte pole **název úhrady** a **Částka úhrady** na jeden řádek rozvržení.
    - Skupina polí **Prodej celkem**:

        - Pole **Celkem (prodej)**, které slouží k vytisknutí celkové částky hotovostního prodeje příjemky. Částka neobsahuje daň. Operace záloh a dárkových poukazů jsou vyloučeny.
        - Pole **Celková částka včetně daně (prodej)**, které slouží k vytisknutí celkové částky hotovostního prodeje příjemky. Částka zahrnuje daň. Operace záloh a dárkových poukazů jsou vyloučeny.
        - Pole **Celková daň (prodej)**, které slouží k vytisknutí celkové částky daně pro hotovostní prodeje. Operace záloh a dárkových poukazů jsou vyloučeny.

    - Skupina polí **Daňový rozpis**. Všechna pole v této skupině polí musí být vytištěna na jednom samostatném řádku.

        - Pole **DIČ**, což je standardní pole, které umožňuje vytisknout souhrn DPH pro každý kód DPH. Toto pole musí být přidáno na nový řádek.
        - Pole **Procento daně**, což je standardní pole, které se používá k tisku platné daňové sazby pro kód DPH.
        - Pole **Daňový základ (prodej)**, které slouží k vytisknutí celkové částky hotovostního prodeje pro kód DPH. Operace záloh a dárkových poukazů jsou vyloučeny.
        - Pole **Částka daně (prodej)**, které slouží k vytisknutí částky daně pro hotovostní prodeje pro kód DPH.
        - Pole **Tiskový kód maloobchodní daně**, které slouží k vytištění zkráceného kódu, který odpovídá kódu DPH.

    - Pole **QR kód**, které slouží k vytištění odkazu na evidovanou hotovostní transakci ve formě QR kódu.

        > [!NOTE]
        > Hodnota **QR kód** je načtena z odpovědi fiskálního registru. EFR vrací QR kód ve své odpovědi pouze v případě, že je hodnota pole **Atributy** v konfiguraci EFR popsána v dokumentaci EFSTA. Formát QR kódu v poli **Atributy** v konfiguraci EFR musí být nastaven na **BMP**.

Další informace o tom, jak pracovat s formáty příjemek, naleznete v tématu [Nastavení a návrh formátů příjmu](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-austria"></a>Nastavení fiskální integrace pro Rakousko

Ukázka integrace služby fiskální registrace pro Rakousko je založena na [funkci fiskální integrace](fiscal-integration-for-retail-channel.md) a je součástí řešení Commerce SDK. Ukázka rozšíření POS se nachází ve složce **src\\FiscalIntegration\\Efr** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). [Ukázka](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) se skládá ze zprostředkovatele fiskálního dokumentu, což je rozšíření řešení Commerce Runtime (CRT) a fiskálního konektoru, který je rozšířením hardwarové stanice Commerce. Další informace o tom, jak používat Commerce SDK, viz [Stáhněte si ukázky Commerce SDK a referenční balíčky z GitHub a NuGet](../dev-itpro/retail-sdk/sdk-github.md) a [Nastavte kanál buildu pro SDK nezávislého balení](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Ukázka integrace služby fiskální registrace pro Rakousko je k dispozici v Commerce SDK od verze Commerce 10.0.29. Ve verzi Commerce 10.0.28 nebo starší musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači (VM) v Microsoft Dynamics Lifecycle Services (LCS). Další informace viz [Pokyny k nasazení ukázkové fiskální integrace pro Rakousko (starší verze)](emea-aut-fi-sample-sdk.md).

Postupujte podle kroků pro nastavení fiskální integrace popsané v části [Nastavení fiskální integrace pro kanály Commerce](setting-up-fiscal-integration-for-retail-channel.md):

1. [Nastavení procesu fiskální registrace](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Kromě toho si všimněte nastavení pro proces fiskální registrace, který je [specifický pro tuto ukázku služby fiskální registrace](#set-up-the-registration-process).
1. [Nastavení zpracování chyb](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Povolit ruční provedení zápisu odložené daňové registrace](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurace komponent kanálu](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Nastavení procesu registrace

Pokud chcete povolit registrační proces, postupujte pomocí následujících kroků pro nastavení centrály Commerce. Další informace viz [Nastavení fiskální integrace pro obchodní kanály](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Stáhněte si konfigurační soubory pro poskytovatele fiskálních dokumentů a fiskální konektor:

    1. Otevřete úložiště [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Vyberte správnou verzi větve vydání podle vaší verze SDK/aplikace.
    1. Otevřete **src \> FiscalIntegration \> Efr**.
    1. Otevřete **Konfigurace \> DocumentProviders** a stáhněte si konfigurační soubory poskytovatele fiskálních dokumentů: 

        - DocumentProviderFiscalEFRSampleAustria.xml
        - DocumentProviderNonFiscalEFRSampleAustria.xml

    1. Stáhněte si konfigurační soubor fiskálního konektoru v umístění **Configurations \> Connectors \> ConnectorEFRSample.xml**.

    > [!NOTE]
    > Ve verzi Commerce 10.0.28 nebo starší musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači v LCS. Konfigurační soubory pro tuto ukázku fiskální integrace jsou umístěny v následujících složkách Retail SDK na vývojářském virtuálním počítači v LCS:
    >
    > - **Konfigurační soubor poskytovatele fiskálního dokumentu:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration
    > - **Konfigurační soubor fiskálního konektoru:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration

1. Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry \> Sdílené parametry obchodu**. Na kartě **Obecné** nastavte možnost **Povolit fiskální integraci** na **Ano**.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Poskytovatelé fiskálních dokumentů** a načtěte konfigurační soubory poskytovatele fiskálního dokumentu, které jste stáhli dříve.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Fiskální konektory** a načtěte konfigurační soubor fiskálního konektoru, který jste stáhli dříve.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Funkční profily Connector**. Vytvořte dva nové funkční profily konektoru, jeden pro každého poskytovatele fiskálních dokumentů, kterého jste načetli dříve, a vyberte fiskální konektor, který jste načetli dříve. Podle potřeby aktualizujte [nastavení mapování dat](#default-data-mapping).
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Technické profily Connector**. Vytvořte nový technický profil konektoru a vyberte fiskální konektor, který jste načetli předtím. Podle potřeby aktualizujte [nastavení konektoru](#fiscal-connector-settings).
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Skupiny fiskálního konektoru**. Vytvořte dvé nové skupiny fiskálního konektoru pro každý funkční profil konektoru, který jste vytvořili předtím.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Proces fiskální registrace**. Vytvořte nový proces fiskální registrace a dva kroky procesu fiskální registrace a vyberte skupiny fiskálního konektoru, které jste předtím vytvořili.
1. Přejděte na **Maloobchodní a velkoobchodní prodej \> Instalace kanálu \> Nastavení POS \> Profily POS \> Funkční profily**. Vyberte funkční profil, který je připojena k obchodu, kde by měl být aktivován proces registrace. Na pevné záložce **Proces fiskální registrace** vyberte proces fiskální registrace, který jste předtím vytvořili. Chcete-li povolit registraci nefiskálních událostí v POS, na záložce s náhledem **Funkce** v sekci **POS** nastavte možnost **Audit** na **Ano**.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Nastavení POS \> Profily POS \> Hardwarové profily**. Vyberte hardwarový profil spojený s hardwarovou stanicí, ke které bude připojena fiskální registrační služba. Na pevné záložce **Fiskální příslušenství** vyberte technický profil konektoru, který jste vytvořili dříve.
1. Spusťte plán distribuce (**Retail a Commerce \> IT Retail a Commerce \> plán distribuce**) a vyberte úlohy **1070** a **1090** k přenosu dat do databáze kanálů.

#### <a name="default-data-mapping"></a>Výchozí mapování dat

Následující výchozí mapování dat je součástí konfigurace poskytovatele fiskálního dokumentu, který je poskytován jako ukázka fiskální integrace:

- **Mapování sazeb daně z přidané hodnoty (DPH).** – Mapování procentních hodnot daně, které jsou nastaveny pro kódy daně z prodeje, na atribut **TaxG** (daňová skupina) v požadavcích zasílaných fiskální službě. Zde je výchozí mapování:

    ```
    A: 20.00; B: 10.00; C: 13.00; D: 0.00; E: 19.00; F: 7.00
    ```

    První složka v každém páru představuje daňovou skupinu DPH, která je podporována službou fiskální registrace EFR. Druhá složka představuje odpovídající sazbu DPH. Další informace o skupinách DPH, které EFR podporuje pro Rakousko, viz [Reference k EFR](https://public.efsta.net/efr/).

#### <a name="fiscal-connector-settings"></a>Nastavení fiskálního konektoru

Následující nastavení jsou součástí konfigurace fiskálního konektoru, který je poskytován jako ukázka fiskální integrace:

- **Adresa koncového bodu** – adresa URL služby daňové registrace.
- **Časový limit zařízení** – doba v milisekundách, po kterou bude fiskální konektor čekat na odpověď ze služby fiskální registrace.
- **Zobrazit oznámení o fiskální registraci** – Tento příznak určuje, zda se mají operátorovi zobrazovat oznámení vrácená službou fiskální registrace.

### <a name="configure-channel-components"></a>Konfigurace komponent kanálu

> [!NOTE]
> - Ukázka integrace služby fiskální registrace pro Rakousko je k dispozici v Commerce SDK od verze Commerce 10.0.29. Ve verzi Commerce 10.0.28 nebo starší musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači v LCS. Další informace viz [Pokyny k nasazení ukázkové fiskální integrace pro Rakousko (starší verze)](emea-aut-fi-sample-sdk.md).
> - Ukázky Commerce, které jsou nasazeny ve vašem prostředí, se automaticky neaktualizují, když na komponenty Commerce použijete aktualizace služeb nebo kvality. Musíte ručně aktualizovat požadované vzorky.

#### <a name="set-up-the-development-environment"></a>Nastavení vývojového prostředí

Tento postup slouží k nastavení vývojového prostředí, abyste mohli testovat a rozšířit ukázku.

1. Naklonujte nebo stáhněte úložiště [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions). Vyberte správnou verzi větve vydání podle vaší verze SDK/aplikace. Další informace viz [Stažení ukázek Commerce SDK a referenčních balíčků z GitHub a NuGet](../dev-itpro/retail-sdk/sdk-github.md).
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

Ukázka integrace služby fiskální registrace pro Rakousko je založena na [funkci fiskální integrace](fiscal-integration-for-retail-channel.md) a je součástí řešení Commerce SDK. Ukázka rozšíření POS se nachází ve složce **src\\FiscalIntegration\\Efr** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Ukázka [se skládá](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) ze zprostředkovatele fiskálního dokumentu, což je rozšíření řešení CRT a fiskálního konektoru, který je rozšířením hardwarové stanice Commerce. Další informace o tom, jak používat Commerce SDK, viz [Stáhněte si ukázky Commerce SDK a referenční balíčky z GitHub a NuGet](../dev-itpro/retail-sdk/retail-sdk-overview.md) a [Nastavte kanál buildu pro SDK nezávislého balení](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Ukázka integrace služby fiskální registrace pro Rakousko je k dispozici v Commerce SDK od verze Commerce 10.0.29. Ve verzi Commerce 10.0.28 nebo starší musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači v LCS. Další informace viz [Pokyny k nasazení ukázkové fiskální integrace pro Rakousko (starší verze)](emea-aut-fi-sample-sdk.md).

### <a name="commerce-runtime-extension-design"></a>Návrh obchodního rozšíření doby běhu 

Účelem rozšíření je, ab poskytovatel daňového dokumentu generoval dokumenty specifické pro službu a zpracovával odpovědi z daňové registrační služby.

#### <a name="request-handler"></a>Obslužná rutina požadavku

Pro poskytovatele dokumentů existují dvě obslužné rutiny:

- **DocumentProviderEFRFiscalAUT** – Tato obslužná rutina se používá ke generování fiskálních dokumentů pro službu fiskální registrace.
- **DocumentProviderEFRNonFiscalAUT** – Tato obslužná rutina se používá ke generování nefiskálních dokumentů pro službu fiskální registrace.

Tyto obslužné rutiny jsou zděděny z rozhraní **INamedRequestHandler**. Metoda **HandlerName** je odpovědná za vrácení názvu obslužné rutiny. Název obslužné rutiny by měl odpovídat názvu poskytovatele dokumentu zprostředkovatele zadanému v centrále Commerce.

Konektor podporuje následující požadavky:

- **GetFiscalDocumentDocumentProviderRequest** – tento požadavek obsahuje informace o dokladu, o němž by měl být vygenerován dokument. Vrátí dokument specifický pro službu, který má být registrován ve službě daňové registrace.
- **GetNonFiscalDocumentDocumentProviderRequest** – tento požadavek obsahuje informace o nefiskálním dokladu, o němž by měl být vygenerován dokument. Vrátí dokument specifický pro službu, který má být registrován ve službě daňové registrace.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – tento požadavek vrací seznam událostí, k jejichž odběru se uživatelé přihlašují. V současné době jsou podporovány následující události: prodej, tisk sestavy X, tisk sestavy Z, vklady účtu odběratele, vklady zákaznických objednávek, události auditu a neprodejní transakce.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – tento požadavek vrací odpověď daňové registrační služby. Tato odpověď je serializován tak, aby tvořila řetězec připravený k uložení.

#### <a name="configuration"></a>Konfigurace

Konfigurační soubory pro poskytovatele fiskálních dokumentů se nachází ve složce **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders** v úložišti [řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/):

- **DocumentProviderFiscalEFRSampleAustria** – Konfigurační soubor fiskálních dokumentů pro poskytovatele fiskálního dokumentu.
- **DocumentProviderNonFiscalEFRSampleAustria** – Konfigurační soubor fiskálních dokumentů pro poskytovatele nefiskálního dokumentu.

Tyto soubory slouží k povolení konfigurace nastavení zprostředkovatele fiskálního dokumentu z centrály Commerce. Formát souboru je v souladu s požadavky na konfiguraci fiskální integrace.

### <a name="hardware-station-extension-design"></a>Design rozšíření hardwarové stanice

Účelem rozšíření fiskálního konektoru je komunikace se službou daňové registrace. Rozšíření hardwarové stanice používá protokoly HTTP a HTTPS k odesílání dokumentů, které rozšíření CRT generuje pro daňovou registrační službu. Také zpracovává odpovědi, které jsou přijaty ze služby daňové registrace.

#### <a name="request-handler"></a>Obslužná rutina požadavku

Obslužná rutina požadavku **EFRHandler** je vstupní bod pro práci s požadavky služby daňové registrace.

Tato rutina je zděděna z rozhraní **INamedRequestHandler**. Metoda **HandlerName** je odpovědná za vrácení názvu obslužné rutiny. Název obslužné rutiny by měl odpovídat názvu poskytovatele dokumentu fiskálního konektoru zadanému v centrále Commerce.

Fiskální konektor podporuje následující požadavky:

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
