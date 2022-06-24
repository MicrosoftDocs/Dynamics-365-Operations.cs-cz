---
title: Ukázka integrace kontrolní jednotky pro Švédsko
description: V tomto článku je uveden přehled ukázkové fiskální integrace pro Švédsko v Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-10-08
ms.openlocfilehash: 11ce0b146f2e64092b0d03dc7416660d76380cd0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885395"
---
# <a name="control-unit-integration-sample-for-sweden"></a>Ukázka integrace kontrolní jednotky pro Švédsko

[!include [banner](../includes/banner.md)]

V tomto článku je uveden přehled ukázkové fiskální integrace pro Švédsko v Microsoft Dynamics 365 Commerce.

> [!NOTE]
> Tato ukázková funkce fiskální integrace nahrazuje předchozí [ukázku integrace POS s kontrolními jednotkami pro Švédsko](retail-sdk-control-unit-sample.md). Dřívější ukázka nevyužívá výhody [rámce fiskální integrace](./fiscal-integration-for-retail-channel.md) a v pozdějších aktualizacích nebude mít podporu. Informace, jak migrovat z dřívější ukázky na ukázku odpovídající verzi Dynamics 365 Commerce **10.0.22 a starší** viz [Migrace z dřívější ukázkové integrace](emea-swe-fi-sample-sdk.md#migrating-from-the-earlier-integration-sample).

Komerční funkce pro Švédsko zahrnuje ukázkovou integraci pokladního místa (POS) s fiskálními zařízeními specifickými pro Švédsko, která jsou známá jako *kontrolní jednotky*. Tato ukázka rozšiřuje [funkci fiskální integrace](fiscal-integration-for-retail-channel.md). Předpokládá se, že kontrolní jednotka je fyzicky připojena k hardwarové stanici, se kterou je POS spárováno. Ukázka například používá aplikační programovací rozhraní (API) kontrolní jednotky [CleanCash Type A](https://www.retailinnovation.se/produkter) společnosti Retail Innovation HTT AB. Používá se verze 1.1.4 CleanCash API.

Ukázka je poskytnuta ve formě zdrojového kódu a je součástí sady software development kit (SDK) pro maloobchod.

Společnost Microsoft nevydává žádný hardware, software nebo dokumentaci společnosti Retail Innovation HTT AB. Pro další informace, jak získat kontrolní jednotku a jak ji obsluhovat, získáte kontaktováním společnosti [Retail Innovation HTT AB](https://www.retailinnovation.se/).

## <a name="scenarios"></a>Scénáře

Ukázka integrace kontrolní jednotky pro Švédsko zahrnuje následující funkce:

- Prodeje, vratky a kopie příjemek jsou automaticky registrovány v kontrolní jednotce, která je připojena k hardwarové stanici spárované s POS.
- Kontrolní kód a výrobní číslo kontrolní jednotky pro registrovanou transakci jsou zachyceny z kontrolní jednotky a uloženy v transakci. Tato data se také označují jako *fiskální odezva*. Fiskální odezvu lze zobrazit na stránce **Transakce obchodu**.
- Do rozložení příjemky lze přidat vlastní pole pro kontrolní kód a výrobní číslo kontrolní jednotky. Tímto způsobem můžete vytisknout fiskální odezvu pro transakci na příjemku.
- Fiskální odezva na transakci je uvedena na sestavě kanálu **Elektronický deník (Švédsko)**.
- K dispozici je několik možností zpracování chyb. Několik příkladů:

    - Opakování fiskální registrace, pokud je to možné. Fiskální registraci můžete opakovat, pokud například kontrolní jednotka není připojena, není připravena nebo nereaguje.
    - Odložte fiskální registraci.
    - Přeskočte daňovou registraci nebo označte transakci jako registrovanou a zahrňte informační kódy pro zaznamenání důvodu chyby a dalších informací.
    - Před otevřením nové transakce prodeje nebo dokončením transakce prodeje ověřte dostupnost kontrolní jednotky.

### <a name="limitations-of-the-sample"></a>Omezení vzorku

Ukázka integrace kontrolní jednotky pro Švédsko aktuálně nepodporuje scénáře zákaznických objednávek.

## <a name="setting-up-the-integration-with-control-units"></a>Nastavení integrace s kontrolními jednotkami

Další informace o nastavení, které je vyžadováno pro Švédsko, viz [Nastavení Commerce pro Švédsko](./emea-swe-cash-registers.md#setting-up-commerce-for-sweden).

### <a name="configuring-swedenspecific-receipts"></a>Konfigurace příjemek specifických pro Švédsko

#### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Nakonfigurujte vlastní pole tak, aby bylo možné použít je ve formátech příjemky pro prodejní příjemky

Můžete konfigurovat jazykový text a vlastní pole, která se používají ve formátech příjemky POS. Výchozí společnost uživatele, který vytvoří nastavení příjmu, musí být stejná právnická osoba, pro kterou se vytváří nastavení text jazyka. Alternativně lze vytvořit texty ve stejném jazyce, které mají být vytvořeny ve výchozí společnosti uživatele a právnické osobě prodejny, pro kterou se nastavení vytváří.

Na stránce **jazykový text** přidejte následující záznamy popisků vlastního pole rozvržení účtenky. Upozorňujeme, že hodnoty **ID jazyka**, **ID textu** a **Text**, které jsou zobrazeny v tabulce, jsou jenom příklady. Lze je změnit tak, aby splňovaly vaše požadavky. Hodnoty **ID textu**, které budete používat, však musí být jedinečné a musí být rovny nebo větší než 900001.

Přidejte následující štítky POS do oddílu **POS** na stránce **Text jazyka**.

| ID jazyka | ID textu | Text                  |
|-------------|---------|-----------------------|
| cs       | 900001  | Registrace kontrolního kódu |
| cs       | 900002  | Registrace zařízení       |

Na stránce **Vlastní pole** přidejte následující záznamy popisků vlastního pole rozvržení účtenky. Upozorňujeme, že hodnoty **ID textu titulku** musí odpovídat hodnotám **ID textu**, které jste zadali na stránce **Text jazyka**.

| Název                         | Typ    | ID textu titulku |
|------------------------------|---------|-----------------|
| SE_FISCALREGISTERCONTROLCODE | Příjemka | 900001          |
| SE_FISCALREGISTERID          | Příjemka | 900002          |

> [!NOTE]
> Je důležité, abyste zadali správné názvy vlastních polí, jak jsou uvedeny v tabulce výše. Nesprávný název vlastního pole způsobí chybějící data v příjemkách.

#### <a name="configure-receipt-formats"></a>Konfigurace formátů příjemky

Pro každý poožadovaný formát příjemky změňte hodnotu pole **Chování tisku** na **Vždy tisknout**.

V Návrháři formátu příjemky přidejte následující vlastní pole do sekce **Zápatí**. Všimněte si, že názvy polí odpovídají jazykovým textům, které jste definovali v předchozím oddílu v tomto článku.

- **Registrace kontrolního kódu** – Toto pole vytiskne kontrolní kód.
- **Registrace zařízení** – Toto pole vytiskne výrobní číslo kontrolní jednotky.

Další informace o tom, jak pracovat s formáty příjemek, naleznete v tématu [Šablony pro příjemky a tisk](../receipt-templates-printing.md).

### <a name="set-up-fiscal-integration-for-sweden"></a>Nastavení fiskální integrace pro Švédsko

Ukázka integrace kontrolní jednotky pro Švédsko je založena na [funkci fiskální integrace](fiscal-integration-for-retail-channel.md) a je součástí řešení Retail SDK. Ukázka se nachází ve složce **src\\FiscalIntegration\\CleanCash** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (například [ukázka ve verzi/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Ukázka [se skládá](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) ze zprostředkovatele fiskálního dokumentu, což je rozšíření řešení Commerce Runtime (CRT) a fiskálního konektoru, který je rozšířením hardwarové stanice Commerce. Další informace o použití sady Retail SDK naleznete v části [Architektura Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) a [Nastavení kanálu sestavení pro sadu SDK nezávislého balení](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Kvůli omezením [nového modelu nezávislého balíčku a rozšíření](../dev-itpro/build-pipeline.md) jej v současné době nelze pro tuto ukázku fiskální integrace použít. Musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači (VM) v Microsoft Dynamics Lifecycle Services (LCS). Další informace viz [Pokyny k nasazení ukázkové integrace kontrolní jednotky pro Švédsko (starší verze)](emea-swe-fi-sample-sdk.md).
>
> Podpora nového modelu nezávislého balení a rozšíření pro vzorky fiskální integrace je plánována pro pozdější verze.

Postupujte podle kroků pro nastavení fiskální integrace popsané v části [Nastavení fiskální integrace pro kanály Commerce](setting-up-fiscal-integration-for-retail-channel.md).

1. [Nastavení procesu fiskální registrace](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Také si všimněte nastaveních pro proces fiskální registrace, který je [specifický pro tuto ukázku integrace kontrolní jednotky](#set-up-the-registration-process).
1. [Nastavení zpracování chyb](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Povolit ruční provedení zápisu odložené daňové registrace](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurace komponent kanálu](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Nastavení procesu registrace

Pokud chcete povolit registrační proces, postupujte pomocí následujících kroků pro nastavení centrály Commerce. Další informace viz [Nastavení fiskální integrace pro obchodní kanály](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Stáhněte si konfigurační soubory pro poskytovatele fiskálních dokumentů a fiskální konektor:

    1. Otevřete úložiště [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Vyberte správnou verzi větve vydání podle vaší verze SDK/aplikace (například **[vydání/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Otevřete **src \> FiscalIntegration \> CleanCash**.
    1. Stáhněte si konfigurační soubor poskytovatele fiskálních dokumentů v umístění **CommerceRuntime \> DocumentProvider.CleanCashSample \> Configuration \> DocumentProviderFiscalCleanCashSample.xml** (například [soubor pro vydání/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/CommerceRuntime/DocumentProvider.CleanCashSample/Configuration/DocumentProviderFiscalCleanCashSample.xml)).
    1. Stáhněte si konfigurační soubor konektoru v umístění **HardwareStation \> Connector.CleanCashSample \> Configuration \> ConnectorCleanCashSample.xml** (například [soubor pro vydání/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/HardwareStation/Connector.CleanCashSample/Configuration/ConnectorCleanCashSample.xml)).

    > [!WARNING]
    > Kvůli omezením [nového modelu nezávislého balíčku a rozšíření](../dev-itpro/build-pipeline.md) jej v současné době nelze pro tuto ukázku fiskální integrace použít. Musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači v LCS. Konfigurační soubory pro tuto ukázku fiskální integrace jsou umístěny v následujících složkách Retail SDK na vývojářském virtuálním počítači v LCS:
    >
    > - **Konfigurační soubor poskytovatele fiskálních dokumentů:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.CleanCashSample\\Configuration\\DocumentProviderFiscalCleanCashSample.xml
    > - **Konfigurační soubor fiskálního konektoru:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.CleanCashSample\\Configuration\\ConnectorCleanCashSample.xml
    > 
    > Podpora nového modelu nezávislého balení a rozšíření pro vzorky fiskální integrace je plánována pro pozdější verze.

1. Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry \> Sdílené parametry obchodu**. Na kartě **Obecné** nastavte možnost **Povolit fiskální integraci** na **Ano**.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Poskytovatelé fiskálních dokumentů** a načtěte konfigurační soubor poskytovatele fiskálního dokumentu, který jste stáhli dříve.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Fiskální konektory** a načtěte konfigurační soubor fiskálního konektoru, který jste stáhli dříve.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Funkční profily Connector**. Vytvořte nový funkční profil konektoru. Vyberte poskytovatele dokumentu a dříve načtený konektor. Podle potřeby aktualizujte [nastavení mapování dat](#default-data-mapping).
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Technické profily Connector**. Vytvořte nový technický profil konektoru a vyberte fiskální konektor, který jste načetli předtím. Podle potřeby aktualizujte [nastavení konektoru](#fiscal-connector-settings).
6. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Skupiny fiskálního konektoru**. Vytvořte novou skupinu fiskálního konektoru pro funkční profil konektoru, který jste vytvořili předtím.
7. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Proces fiskální registrace**. Vytvořte nový procesu daňové registrace a krok procesu fiskální registrace a vyberte skupinu fiskálního konektoru, kterou jste předtím vytvořili.
8. Přejděte na **Maloobchodní a velkoobchodní prodej \> Instalace kanálu \> Nastavení POS \> Profily POS \> Funkční profily**. Vyberte funkční profil, který je připojena k obchodu, kde by měl být aktivován proces registrace. Na pevné záložce **Proces fiskální registrace** vyberte proces fiskální registrace, který jste předtím vytvořili.
9. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Nastavení POS \> Profily POS \> Hardwarové profily**. Vyberte hardwarový profil spojený s hardwarovou stanicí, ke které bude připojena fiskální tiskárna. Na pevné záložce **Fiskální příslušenství** vyberte technický profil konektoru, který jste vytvořili dříve.
10. Spusťte plán distribuce (**Retail a Commerce \> IT Retail a Commerce \> plán distribuce**) a vyberte úlohy **1070** a **1090** k přenosu dat do databáze kanálů.

#### <a name="default-data-mapping"></a>Výchozí mapování dat

Následující výchozí mapování dat je součástí konfigurace poskytovatele fiskálního dokumentu, který je poskytován jako ukázka fiskální integrace:

- **Mapování kódu daně z přidané hodnoty (DPH)** – Toto mapování nastavuje kódy daně z přidané hodnoty (DPH) specifické pro zařízení na odpovídající kódy daně z prodeje. Mapování kódu DPH by mělo mít následující formát:

    ```
    1 : code1 ; 2 : code2
    ```

    Zde je vysvětlení tohoto formátu:

    - *1* a *2* jsou kódy DPH specifické pro zařízení.
    - Jako oddělovač se používá středník (;).
    - *code1* a *code2* jsou kódy daně z prodeje, které se konfigurují v centrále Commerce. Musíte upravit vzorové mapování podle daňových kódů, které jsou nakonfigurovány ve vaší aplikaci.

    Kontrolní jednotky podporují až čtyři různé kódy DPH. Mapování kódu DPH lze tedy nastavit následujícím způsobem:

    ```
    1 : code1 ; 2 : code2 ; 3 : code3 ; 4 : code4
    ```

    > [!NOTE]
    > Více kódů DPH lze namapovat na stejný kód DPH pro konkrétní zařízení.

#### <a name="fiscal-connector-settings"></a>Nastavení fiskálního konektoru

Následující nastavení jsou součástí konfigurace fiskálního konektoru, který je poskytován jako ukázka fiskální integrace:

- **Řetězec připojení** – Nastavení připojení kontrolní jednotky.
- **Časový limit** – doba v milisekundách, po kterou bude čekat ovladač na odpověď z kontrolní jednotky.

### <a name="configure-channel-components"></a>Konfigurace komponent kanálu

> [!WARNING]
> Kvůli omezením [nového modelu nezávislého balíčku a rozšíření](../dev-itpro/build-pipeline.md) jej v současné době nelze pro tuto ukázku fiskální integrace použít. Musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači v LCS. Další informace viz [Pokyny k nasazení ukázkové integrace kontrolní jednotky pro Švédsko (starší verze)](emea-swe-fi-sample-sdk.md).
>
> Podpora nového modelu nezávislého balení a rozšíření pro vzorky fiskální integrace je plánována pro pozdější verze.

#### <a name="set-up-the-development-environment"></a>Nastavení vývojového prostředí

Tento postup slouží k nastavení vývojového prostředí, abyste mohli testovat a rozšířit ukázku.

1. Naklonujte nebo stáhněte úložiště [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions). Vyberte správnou verzi větve vydání podle vaší verze SDK/aplikace. Další informace viz [Stažení ukázek Retail SDK a referenčních balíčků z GitHub a NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Otevřete řešení integrace kontrolní jednotky v umístění **Dynamics365Commerce.Solutions\\FiscalIntegration\\CleanCash\\CleanCash.sln** a sestavte jej.
1. Nainstalujte rozšíření CRT:

    1. Vyhledejte instalační program rozšíření CRT:

        - **Commerce Scale Unit:** Ve složce **CleanCash\\ScaleUnit\\ScaleUnit.CleanCash.Installer\\bin\\Debug\\net461** vyhledejte instalační program **ScaleUnit.CleanCash.Installer**.
        - **Místní CRT v Modern POS:** Ve složce **CleanCash\\ModernPOS\\ModernPOS.CleanCash.Installer\\bin\\Debug\\net461** vyhledejte instalační program **ModernPOS.CleanCash.Installer**.

    2. Spusťte instalační program rozšíření CRT z příkazového řádku:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.CleanCash.Installer.exe install --verbosity 0
            ```

        - **Místní CRT v Modern POS:**

            ```Console
            ModernPOS.CleanCash.Installer.exe install --verbosity 0
            ```

1. Instalace rozšíření hardwarové stanice:

    1. Ve složce **CleanCash\\HardwareStation\\HardwareStation.CleanCash.Installer\\bin\\Debug\\net461** vyhledejte instalační program **HardwareStation.CleanCash.Installer**.
    1. Spusťte instalační program rozšíření z příkazového řádku:

        ```Console
        HardwareStation.CleanCash.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Produkční prostředí

Postupujte podle kroků v části [Nastavení kanálu buildu pro ukázku fiskální integrace](fiscal-integration-sample-build-pipeline.md), kterými vygenerujete a uvolníte nasaditelné balíčky Cloud Scale Unit a samoobslužné nasaditelné balíčky pro ukázku fiskální integrace. Soubor YAML šablony **CleanCash build-pipeline.yml** se nachází ve složce **Pipeline\\YAML_Files** úložiště [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-the-extensions"></a>Návrh rozšíření

Ukázka integrace kontrolní jednotky pro Švédsko je založena na [funkci fiskální integrace](fiscal-integration-for-retail-channel.md) a je součástí řešení Retail SDK. Ukázka se nachází ve složce **src\\FiscalIntegration\\CleanCash** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (například [ukázka ve verzi/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Ukázka [se skládá](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) ze zprostředkovatele fiskálního dokumentu, což je rozšíření řešení CRT a fiskálního konektoru, který je rozšířením hardwarové stanice Commerce. Další informace o použití sady Retail SDK naleznete v části [Architektura Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) a [Nastavení kanálu sestavení pro sadu SDK nezávislého balení](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Kvůli omezením [nového modelu nezávislého balíčku a rozšíření](../dev-itpro/build-pipeline.md) jej v současné době nelze pro tuto ukázku fiskální integrace použít. Musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači v LCS. Další informace viz [Pokyny k nasazení ukázkové integrace kontrolní jednotky pro Švédsko (starší verze)](emea-swe-fi-sample-sdk.md). Podpora nového modelu nezávislého balení a rozšíření pro vzorky fiskální integrace je plánována pro pozdější verze.

### <a name="crt-extension-design"></a>Návrh rozšíření CRT

Účelem rozšíření je, aby poskytovatel fiskálního dokumentu generoval dokumenty specifické pro službu a zpracovával odpovědi z kontrolní jednotky.

#### <a name="request-handler"></a>Obslužná rutina požadavku

Pro poskytovatele dokumentů existuje jedna obslužná rutina požadavků **DocumentProviderCleanCash**. Tato obslužná rutina se používá ke generování fiskálních dokumentů pro kontrolní jednotku.

Tato rutina je zděděna z rozhraní **INamedRequestHandler**. Metoda **HandlerName** je odpovědná za vrácení názvu obslužné rutiny. Název obslužné rutiny by měl odpovídat názvu poskytovatele dokumentu zprostředkovatele zadanému v centrále Commerce.

Konektor podporuje následující požadavky:

- **GetFiscalDocumentDocumentProviderRequest** – tento požadavek obsahuje informace o dokladu, o němž by měl být vygenerován dokument. Vrátí dokument specifický pro službu, který má být registrován v kontrolní jednotce.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – tento požadavek vrací seznam událostí, k jejichž odběru se uživatelé přihlašují. V současné době jsou podporovány prodejní akce a akce auditu.

#### <a name="configuration"></a>Konfigurace

Konfigurační soubor pro poskytovatele fiskálních dokumentů se nachází v umístění **src\\FiscalIntegration\\CleanCash\\CommerceRuntime\\DocumentProvider.CleanCashSample\\Configuration\\DocumentProviderFiscalCleanCashSample.xml** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Tento soubor slouží k povolení nastavení pro zprostředkovatele dokumentu ke konfiguraci z centrály Commerce. Formát souboru je v souladu s požadavky na konfiguraci fiskální integrace.

### <a name="hardware-station-extension-design"></a>Design rozšíření hardwarové stanice

Účelem rozšíření je fiskální konektor určený ke komunikaci s kontrolní jednotkou. Používá protokol HTTP k odesílání dokumentů, které rozšíření  CRT generuje pro kontrolní jednotku. Také zpracovává odpovědi, které jsou přijaty z kontrolní jednotky.

#### <a name="request-handler"></a>Obslužná rutina požadavku

Obslužná rutina požadavku **CleanCashHandler** je vstupní bod pro práci s požadavky do kontrolní jednotky.

Tato rutina je zděděna z rozhraní **INamedRequestHandler**. Metoda **HandlerName** je odpovědná za vrácení názvu obslužné rutiny. Název obslužné rutiny by měl odpovídat názvu poskytovatele dokumentu fiskálního konektoru zadanému v centrále Commerce.

Konektor podporuje následující požadavky:

- **SubmitDocumentFiscalDeviceRequest** – tento požadavek odesílá dokumenty do kontrolní jednotky a vrátí z ní odpověď.
- **IsReadyFiscalDeviceRequest** – tento požadavek se používá pro kontrolu stavu kontrolní jednotky.
- **InitializeFiscalDeviceRequest** – tento požadavek se používá pro inicializaci kontrolní jednotky.

#### <a name="configuration"></a>Konfigurace

Konfigurační soubor pro fiskální konektor se nachází v umístění **src\\FiscalIntegration\\CleanCash\\HardwareStation\\Connector.CleanCashSample\\Configuration\\ConnectorCleanCashSample.xml** v úložišti [Řešení Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Tento soubor slouží k povolení nastavení pro fiskální konektor ke konfiguraci z centrály Commerce. Formát souboru je v souladu s požadavky na konfiguraci fiskální integrace.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
