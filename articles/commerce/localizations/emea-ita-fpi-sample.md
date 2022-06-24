---
title: Vzor integrace fiskální tiskárny pro Itálii
description: V tomto článku je uveden přehled ukázkové fiskální integrace pro Itálii v Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2018-11-1
ms.openlocfilehash: 2aa1851fe5fe447ba2dd4640be9881b37e54216e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909383"
---
# <a name="fiscal-printer-integration-sample-for-italy"></a>Vzor integrace fiskální tiskárny pro Itálii

[!include[banner](../includes/banner.md)]

V tomto článku je uveden přehled ukázkové fiskální integrace pro Itálii v Microsoft Dynamics 365 Commerce.

Funkce Commerce pro Itálii zahrnuje ukázkovou integraci pokladního místa (POS) s fiskální tiskárnou. Ukázka rozšiřuje [funkce fiskální integrace](fiscal-integration-for-retail-channel.md), aby to fungovaly s [tiskárnami Epson FP-90III](https://www.epson.it/products/sd/pos-printer/epson-fp-90iii-series) a umožňuje komunikaci s fiskální tiskárnou v režimu webového serveru prostřednictvím webové služby EpsonFPMate pomocí rozhraní Fiscal ePOS-Print API. Ukázka podporuje pouze režim Registratore Telematico (RT). Ukázka je poskytnuta ve formě zdrojového kódu a je součástí sady software development kit (SDK) pro maloobchod.

Společnost Microsoft nevydává žádný hardware, software nebo dokumentaci společnosti Epson. Pro informace, jak získat fiskální tiskárnu a jak ji obsluhovat, kontaktujte společnost [Epson Italia S.p.A](https://www.epson.it).

## <a name="scenarios"></a>Scénáře

Následující scénáře uvádějí ukázku integrace fiskální tiskárny pro Itálii.

- Prodejní scénáře:

    - Tisk fiskální příjemky pro prodej typu cash-and-carry a vratky.
    - Zachycení odpovědi z fiskální tiskárny a její uložení do databáze kanálů.
    - Daně:

        - Mapování na daňové kódy (oddělení) fiskální tiskárny.
        - Přenos mapovaných dat daní do fiskální tiskárny.
        - Tisk daní na fiskální příjemku.

    - Platby:

        - Mapování na způsoby fiskální tiskárny.
        - Tisk plateb na fiskální příjemku.
        - Tisk informací o změně.

    - Tisk slev řádku.
    - Dárkové poukazy:

        - Vyloučení vydaného/přeúčtovaného dárkového poukazu z fiskální příjemky pro prodej.
        - Tisk platby, která jako běžný způsob platby používá dárkový poukaz.

    - Tisk fiskálních příjemek pro operace zákaznických objednávek:

        - Pro zálohu objednávky zákazníka se nevytiskne fiskální příjemka.
        - Tisk fiskální příjemky pro řádky převzetí na hybridní zákaznické objednávce.
        - Tisk fiskální příjemky pro operaci vyzvednutí zákaznické objednávky.
        - Tisk fiskální příjemky pro vratku.

    - Tisk čárového kódu pro číslo příjemky na fiskální příjemku.
    - Tisk [informací o odběrateli](emea-ita-customer-information.md), který je zadán pro prodejní transakci na fiskání příjemku. Příkladem této informace je kód loterie zákazníka. 

- Výpisy na konci dne (fiskální X a fiskální Z sestavy).
- Zpracování chyb, jako jsou následující možnosti:

    - Opakujte fiskální registraci, pokud je to možné, například když fiskální tiskárna není připojena, není připravena nebo neodpovídá, v tiskárně došel papír nebo došlo k uvíznutí papíru.
    - Odložte fiskální registraci.
    - Přeskočte daňovou registraci nebo označte transakci jako registrovanou a zahrňte informační kódy pro zaznamenání důvodu chyby a dalších informací.
    - Před otevřením nové transakce prodeje nebo dokončením transakce prodeje zkontrolujte dostupnost fiskální tiskárny.

### <a name="gift-cards"></a>Dárkové poukazy

Ukázka integrace fiskální tiskárny implementuje následující pravidla pro dárkové poukazy:

- Vyloučení řádků prodeje, které souvisejí s operacemi *Vydání dárkového poukazu* a *Přidání na dárkový poukaz* z fiskální příjemky.
- Netiskněte fiskální příjemku, pokud obsahuje pouze řádky dárkových poukazů.
- Odečtení celkové částky dárkových poukazů, které jsou vydány nebo znovu účtovány v transakci z řádků platby fiskální příjemky.
- Uložení vypočítaných úprav plateb do databáze kanálů s odkazem na odpovídající fiskální transakci.
- Platba dárkovým poukazem je považována za běžnou platbu.

### <a name="customer-deposits-and-customer-order-deposits"></a>Vklady odběratele a vklady objednávky odběratele

Ukázka integrace fiskální tiskárny implementuje následující pravidla, která souvisí s vklady odběratele a vklady objednávky odběratelů:

- Netiskněte fiskální příjemku, pokud je transakce vkladem odběratele.
- Netiskněte fiskální příjemku, pokud transakce obsahuje pouze vklad objednávky odběratele nebo refundaci vkladu objednávky odběratele.
- Tisk částky dříve zaplacené zálohy na fiskální příjemku pro operaci vyzvednutí objednávky odběratele.
- Odečtení částky zálohy na objednávce odběratele z platebních řádků, když je vytvořena hybridní objednávka odběratele.
- Uložení vypočítaných úprav plateb do databáze kanálů s odkazem na fiskální transakci pro hybridní zákaznickou objednávku.

### <a name="limitations-of-the-sample"></a>Omezení vzorku

- Služba fiskální tiskárny podporuje pouze scénáře, kde je součástí ceny daň z prodeje. Proto musí být možnost **Ceny zahrnují DPH** nastavena na **Ano** pro obchody a odběratele.
- Denní sestavy (fiskální X a fiskální Z) se tisknou ve formátu, který je součástí firmwaru fiskální tiskárny.
- Fiskální tiskárna nepodporuje smíšené transakce. Možnost **Zakázat smíšené prodeje a vratky na jedné příjemce** by měla být nastavena na **Ano** v profilech funkcí POS.
- Ukázka podporuje integraci pouze s fiskální tiskárnou, která pracuje v režimu Registratore Telematico (RT).

## <a name="set-up-fiscal-integration-for-italy"></a>Nastavení fiskální integrace pro Itálii

Ukázka integrace fiskální tiskárny pro Itálii je založena na [funkci fiskální integrace](fiscal-integration-for-retail-channel.md) a je součástí řešení Retail SDK. Ukázka se nachází ve složce **src\\FiscalIntegration\\EpsonFP90IIISample** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (například [ukázka ve verzi/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample)). Ukázka [se skládá](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) ze zprostředkovatele fiskálního dokumentu, což je rozšíření řešení Commerce Runtime (CRT) a fiskálního konektoru, který je rozšířením hardwarové stanice Commerce. Další informace o použití sady Retail SDK naleznete v části [Architektura Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) a [Nastavení kanálu sestavení pro sadu SDK nezávislého balení](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Kvůli omezením [nového modelu nezávislého balíčku a rozšíření](../dev-itpro/build-pipeline.md) jej v současné době nelze pro tuto ukázku fiskální integrace použít. Musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači (VM) v Microsoft Dynamics Lifecycle Services (LCS). Další informace viz [Pokyny k nasazení ukázkové integrace fiskální tiskárny pro Itálii (starší verze)](emea-ita-fpi-sample-sdk.md).
>
> Podpora nového modelu nezávislého balení a rozšíření pro vzorky fiskální integrace je plánována pro pozdější verze.

Postupujte podle kroků pro nastavení fiskální integrace popsané v části [Nastavení fiskální integrace pro kanály Commerce](setting-up-fiscal-integration-for-retail-channel.md).

1. [Nastavení procesu fiskální registrace](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Kromě toho si všimněte nastavení pro proces fiskální registrace, která jsou [specifická pro tuto ukázku integrace fiskální tiskárny](#set-up-the-registration-process).
1. [Nastavení fiskální textů pro slevy](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).
1. [Nastavení zpracování chyb](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Nastavení fiskálních sestav X/ Z z POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Povolit ruční provedení zápisu odložené daňové registrace](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Nastavení funkcí pro správu informací o odběrateli v POS](emea-ita-customer-information.md#setup).
1. [Konfigurace komponent kanálu](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Nastavení procesu registrace

Pokud chcete povolit registrační proces, postupujte pomocí následujících kroků pro nastavení centrály Commerce. Další informace viz [Nastavení fiskální integrace pro obchodní kanály](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Stáhněte si konfigurační soubory pro poskytovatele fiskálních dokumentů a fiskální konektor:

    1. Otevřete úložiště [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Vyberte správnou verzi větve vydání podle vaší verze SDK/aplikace (například **[vydání/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Otevřete **src \> FiscalIntegration \> EpsonFP90IIISample**.
    1. Stáhněte si konfigurační soubor poskytovatele fiskálních dokumentů v umístění **CommerceRuntime \> DocumentProvider.EpsonFP90IIISample \> Configuration \> DocumentProviderEpsonFP90IIISample.xml** (například [soubor pro vydání/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/CommerceRuntime/DocumentProvider.EpsonFP90IIISample/Configuration/DocumentProviderEpsonFP90IIISample.xml)).
    1. Stáhněte si konfigurační soubor konektoru v umístění **HardwareStation \> EpsonFP90IIIFiscalDeviceSample \> Configuration \> ConnectorEpsonFP90IIISample.xml** (například [soubor pro vydání/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/HardwareStation/EpsonFP90IIIFiscalDeviceSample/Configuration/ConnectorEpsonFP90IIISample.xml).

    > [!WARNING]
    > Kvůli omezením [nového modelu nezávislého balíčku a rozšíření](../dev-itpro/build-pipeline.md) jej v současné době nelze pro tuto ukázku fiskální integrace použít. Musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači v LCS. Konfigurační soubory pro tuto ukázku fiskální integrace jsou umístěny v následujících složkách Retail SDK na vývojářském virtuálním počítači v LCS:
    >
    > - **Konfigurační soubor poskytovatele fiskálních dokumentů:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extension.DocumentProvider.EpsonFP90IIISample\\Configuration\\DocumentProviderEpsonFP90IIISample.xml
    > - **Konfigurační soubor fiskálního konektoru:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EpsonFP90IIIFiscalDeviceSample\\Configuration\\ConnectorEpsonFP90IIISample.xml
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

- **Mapování typu úhrady** – Mapování platebních metod, které jsou pro obchod nakonfigurovány, na typy plateb, které podporuje fiskální tiskárna. Následující příkad ukazuje výchozí mapování.

    ```JSON
    {"PaymentMethods": [
        {"StorePaymentMethod":"1", "PrinterPaymentType":"0", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"3", "PrinterPaymentType":"2", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"4", "PrinterPaymentType":"2", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"6", "PrinterPaymentType":"0", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"8", "PrinterPaymentType":"6", "PrinterPaymentIndex":"01"}
        ],
        "DepositPaymentMethod": {"PrinterPaymentType":"2", "PrinterPaymentIndex":"00"}}
    ```

    Zde je vysvětlení atributů v tomto mapování:

    - **StorePaymentMethod** je způsob platby, který je nastaven pro obchod, v umístění **Retail a Commerce \> Nastavení kanálu \> Platební metody \> Platební metody**.
    - **PrinterPaymentType** a **PrinterPaymentIndex** jsou odpovídající typ platby a index, které jsou definovány v dokumentaci k fiskální tiskárně Epson.
    - **DepositPayment Method** se používá k zadání typu platby tiskárny a indexu pro část částky vyzvednutí objednávky odběratele, která je vyrovnána vkladem objednávky odběratele.

    Následující tabulka ukazuje, jak ukázkové mapování platebních metod odpovídá platebním metodám obchodu, které jsou konfigurovány ve standardních ukázkových datech.

    | Způsob platby | Název způsobu platby |
    |----------------|---------------------|
    | 1              | Hotovost                |
    | 3              | Karta                |
    | 4              | Účet zákazníka    |
    | 6              | Měna            |
    | 8              | Dárkový poukaz           |

    Musíte upravit vzorové mapování podle platebních metod, které jsou nakonfigurovány ve vaší aplikaci.

- **Typ čárového kódu pro číslo příjemky** – Typ čárového kódu, který se používá k zobrazení čísla příjemky na fiskální příjemce. Výchozí mapování je **CODE128**.
- **Tisk fiskálních dat v záhlaví příjemky** – Pokud je tento parametr zapnutý, informace o obchodu se vytisknou na příjemku. Tyto informace zahrnují název, adresu a daňové identifikační číslo obchodu, a jméno pokladníka.
- **Mapování oddělení fiskálních tiskárny** – Mapování oddělení fiskální tiskárny na sazby daně z přidané hodnoty (DPH), osvobození od DPH a typy produktů. Následující příkad ukazuje výchozí mapování.

    ```JSON
    {"Departments": [
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"01"},
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"02"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"03"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"04"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"05"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"06"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"07"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"08"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"09"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"10"},
        {"VATRate":"0000", "VATExemptNature":"NS", "ProductType":"0", "DepartmentNumber":"99"}]}
    ```

    Zde je vysvětlení atributů v tomto mapování:

    - **VATRate** je podporovaná sazba DPH, která je nakonfigurována jako kód DPH. Hodnota v mapování má dvě desetinná místa, ale žádný desetinný oddělovač. Například **2200** představuje 22 procent a **1000** představuje 10 procent.
    - **VATExemptNature** je použitelná pouze v případech, kdy sazba DPH je 0 (nula), včetně případů, kdy daň neexistuje. V současné době je **VATExemptNature** podporováno pouze u dárkových poukazů a hodnota v mapování musí odpovídat hodnotě vlastnosti **VATExemptNatureForGiftCard** v konfiguračním souboru XML.
    - **ProductType** je typ produktu. Hodnota **0** představuje zboží a hodnota **1** představuje služby.
    - **DepartmentNumber** je číslo oddělení, které je konfigurováno v tiskárně a odpovídá předchozím třem atributům.

    Ukázkové mapování musíte upravit podle sazeb DPH, které jsou nakonfigurovány ve vaší aplikaci, a odpovídajících oddělení, která jsou nakonfigurována ve vaší fiskální tiskárně.

- **Osvobození od DPH pro dárkový poukaz** – Osvobození od DPH, které se bude uplatňovat při vydání nebo opětovném doplnění dárkového poukazu. Hodnota musí odpovídat nějaké položce v mapování oddělení fiskální tiskárny. Výchozí mapování je **NS**.
- **Povolit bezplatné položky** – Pokud je tento parametr zapnutý, je povolen speciální typ úpravy slevy *omaggio* pro položky, které mají 100procentní slevu.
- **Informační kód pro původ vratky** – Informační kód, který se používá k zachycení původu transakce vrácení, pokud není poskytnuta žádná původní příjemka. Tento parametr se používá společně s parametry **Informační kód pro původní datum prodeje** a **Mapování původu vratky** pro generování správné zprávy ve fiskální příjemce o původu transakce vrácení, pokud neexistuje žádná původní prodejní transakce. 

    Tento informační kód by měl být nakonfigurován tak, aby uživateli umožnil vybrat nebo zadat jeden z možných původů vrácení ve vašich obchodech. Lze jej například nakonfigurovat jako seznam dílčích kódů (například **Vratka z webu** nebo **Vratka z veřejného terminálu**). Parametr **Mapování původu vratky** se pak používá k převodu hodnoty informačního kódu na příkaz pro fiskální tiskárnu.

    Informační kód, který je vybrán pro parametr **Informační kód pro původ vratky**, musí být nakonfigurován jako povinný informační kód, který je aktivován jednou za prodejní transakci. Musí být přiřazen jako informační kód **Vrátit produkt** v profilu funkcí POS, aby se aktivoval, když je spuštěna operace **Vrátit produkt**.

    Pro toto mapování není zadána žádná výchozí hodnota. Musíte vybrat informační kód, který je nakonfigurován ve vaší aplikaci.

- **Informační kód pro původní datum prodeje** – Informační kód, který se používá k zachycení původního data prodeje pro transakci vrácení, pokud není poskytnuta žádná původní příjemka. Tento parametr se používá společně s parametry **Informační kód pro původ vratky** a **Mapování původu vratky** pro generování správné zprávy ve fiskální příjemce o původu transakce vrácení, pokud neexistuje žádná původní prodejní transakce.

    Informační kód musí být nakonfigurován tak, aby pole **Typ vstupu** bylo nastaveno jako **Datum**. Musí být nakonfigurován jako povinný informační kód, který se aktivuje jednou za prodejní transakci. Měl by být přiřazen také jako **Propojený informační kód** pro informační kód, který je vybrán pro parametr **Informační kód pro původ vratky**, takže se dva informační kódy aktivují jeden po druhém.

    Pro toto mapování není zadána žádná výchozí hodnota. Musíte vybrat informační kód, který je nakonfigurován ve vaší aplikaci.

- **Mapování původu vratky** – Mapování původů vratek, které se používá k tisku původu transakce vrácení, pokud není poskytnuta žádná původní příjemka. Tento parametr se používá společně s parametry **Informační kód pro původ vratky** a **Informační kód pro původní datum prodeje** pro generování správné zprávy ve fiskální příjemce o původu transakce vrácení, pokud neexistuje žádná původní prodejní transakce. Následující příkad ukazuje výchozí mapování.

    ```JSON
    {"ReturnOrigins": [
        {"ReturnOrigin":"1", "PrinterReturnOrigin":"POS"},
        {"ReturnOrigin":"2", "PrinterReturnOrigin":"ND"}
        ],
        "PrinterReturnOriginWithoutFiscalData":"POS"}
    ```

    Zde je vysvětlení atributů v tomto mapování:

    - **ReturnOrigin** je jedním z možných původů vratek ve vašich obchodech. Hodnota musí odpovídat hodnotě parametru **Informační kód pro původ vrácení**.
    - **PrinterReturnOrigin** je jedním z původů vratek, které fiskální tiskárna přijímá (**POS**, **VR** nebo **ND**).
    - **PrinterReturnOriginWithoutFiscalData** je původ vratky, který fiskální tiskárna přijímá a který odpovídá transakci vrácení, která je propojena s původní prodejní transakcí, která nemá propojená fiskální data, protože nebyla registrována prostřednictvím fiskální tiskárny. V tomto případě je původní datum prodeje identifikováno jako datum původní prodejní transakce.

Následující výchozí mapování dat jsou zastaralá a jsou uchovávána pouze z důvodu zpětné kompatibility:

- Mapování kódů daně z přidané hodnoty (DPH)
- Typ platby vkladu

#### <a name="fiscal-connector-settings"></a>Nastavení fiskálního konektoru

Následující nastavení jsou součástí konfigurace fiskálního konektoru, který je poskytován jako ukázka fiskální integrace:

- **Adresa koncového bodu** – adresa URL tiskárny.
- **Synchronizace data a času** – Hodnota, která určuje, zda se musí datum a čas tiskárny synchronizovat s připojenou hardwarovou stanicí.

### <a name="configure-channel-components"></a>Konfigurace komponent kanálu

> [!WARNING]
> Kvůli omezením [nového modelu nezávislého balíčku a rozšíření](../dev-itpro/build-pipeline.md) jej v současné době nelze pro tuto ukázku fiskální integrace použít. Musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači v LCS. Další informace viz [Pokyny k nasazení ukázkové integrace fiskální tiskárny pro Itálii (starší verze)](emea-ita-fpi-sample-sdk.md).
>
> Podpora nového modelu nezávislého balení a rozšíření pro vzorky fiskální integrace je plánována pro pozdější verze.

#### <a name="set-up-the-development-environment"></a>Nastavení vývojového prostředí

Tento postup slouží k nastavení vývojového prostředí, abyste mohli testovat a rozšířit ukázku.

1. Naklonujte nebo stáhněte úložiště [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions). Vyberte správnou verzi větve vydání podle vaší verze SDK/aplikace. Další informace viz [Stažení ukázek Retail SDK a referenčních balíčků z GitHub a NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Otevřete řešení integrace fiskální tiskárny v umístění **Dynamics365Commerce.Solutions\\FiscalIntegration\\EpsonFP90IIISample\\EpsonFP90IIISample.sln** a sestavte jej.
1. Nainstalujte rozšíření CRT:

    1. Vyhledejte instalační program rozšíření CRT:

        - **Commerce Scale Unit:** Ve složce **EpsonFP90IIISample\\ScaleUnit\\ScaleUnit.EpsonFP90III.Installer\\bin\\Debug\\net461** vyhledejte instalační program **ScaleUnit.EpsonFP90III.Installer**.
        - **Místní CRT v Modern POS:** Ve složce **EpsonFP90IIISample\\ModernPOS\\ModernPOS.EpsonFP90III.Installer\\bin\\Debug\\net461** vyhledejte instalační program **ModernPOS.EpsonFP90III.Installer**.

    1. Spusťte instalační program rozšíření CRT z příkazového řádku:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.EpsonFP90III.Installer.exe install --verbosity 0
            ```

        - **Místní CRT v Modern POS:**

            ```Console
            ModernPOS.EpsonFP90III.Installer.exe install --verbosity 0
            ```

1. Instalace rozšíření hardwarové stanice:

    1. Ve složce **EpsonFP90IIISample\\HardwareStation\\HardwareStation.EpsonFP90III.Installer\\bin\\Debug\\net461** vyhledejte instalační program **HardwareStation.EpsonFP90III.Installer**.
    1. Spusťte instalační program rozšíření z příkazového řádku:

        ```Console
        HardwareStation.EpsonFP90III.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Produkční prostředí

Postupujte podle kroků v části [Nastavení kanálu buildu pro ukázku fiskální integrace](fiscal-integration-sample-build-pipeline.md), kterými vygenerujete a uvolníte nasaditelné balíčky Cloud Scale Unit a samoobslužné nasaditelné balíčky pro ukázku fiskální integrace. Soubor YAML šablony **EpsonFP90III build-pipeline.yml** se nachází ve složce **Pipeline\\YAML_Files** úložiště [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-extensions"></a>Návrh rozšíření

Ukázka integrace fiskální tiskárny pro Itálii je založena na [funkci fiskální integrace](fiscal-integration-for-retail-channel.md) a je součástí řešení Retail SDK. Ukázka se nachází ve složce **src\\FiscalIntegration\\EpsonFP90IIISample** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (například [ukázka ve verzi/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample)). Ukázka [se skládá](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) ze zprostředkovatele fiskálního dokumentu, což je rozšíření řešení CRT a fiskálního konektoru, který je rozšířením hardwarové stanice Commerce. Další informace o použití sady Retail SDK naleznete v části [Architektura Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) a [Nastavení kanálu sestavení pro sadu SDK nezávislého balení](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Kvůli omezením [nového modelu nezávislého balíčku a rozšíření](../dev-itpro/build-pipeline.md) jej v současné době nelze pro tuto ukázku fiskální integrace použít. Musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači v LCS. Další informace viz [Pokyny k nasazení ukázkové integrace fiskální tiskárny pro Itálii (starší verze)](emea-ita-fpi-sample-sdk.md). Podpora nového modelu nezávislého balení a rozšíření pro vzorky fiskální integrace je plánována pro pozdější verze.

### <a name="commerce-runtime-extension-design"></a>Návrh obchodního rozšíření doby běhu

Účelem rozšíření je, ab poskytovatel daňového dokumentu generoval dokumenty specifické pro tiskárnu a zpracovával odpovědi z fiskální tiskárny.

#### <a name="request-handler"></a>Obslužná rutina požadavku

Obslužná rutina požadavků **DocumentProviderEpsonFP90III** je vstupním bodem pro požadavek na generování dokumentů z fiskální tiskárny.

Tato rutina je zděděna z rozhraní **INamedRequestHandler**. Metoda **HandlerName** je odpovědná za vrácení názvu obslužné rutiny. Název obslužné rutiny by měl odpovídat názvu poskytovatele dokumentu zprostředkovatele zadanému v centrále Commerce.

Konektor podporuje následující požadavky:

- **GetFiscalDocumentDocumentProviderRequest** – tento požadavek obsahuje informace o dokladu, o němž by měl být vygenerován dokument. Vrátí dokument specifický pro tiskárnu, který má být registrován ve fiskální tiskárně.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – tento požadavek vrací seznam událostí, k jejichž odběru se uživatelé přihlašují. Aktuálně jsou podporovány následující události: prodej, tisk X sestavy a tisk Z sestavy.

#### <a name="configuration"></a>Konfigurace

Konfigurační soubor pro poskytovatele fiskálních dokumentů se nachází v umístění **src\\FiscalIntegration\\EpsonFP90IIISample\\CommerceRuntime\\DocumentProvider.EpsonFP90IIISample\\Configuration\\DocumentProviderEpsonFP90IIISample.xml** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Tento soubor slouží k povolení nastavení pro zprostředkovatele dokumentu ke konfiguraci z centrály Commerce. Formát souboru je v souladu s požadavky na konfiguraci fiskální integrace.

### <a name="hardware-station-extension-design"></a>Design rozšíření hardwarové stanice

Účelem rozšíření je fiskální konektor určený ke komunikaci s fiskální tiskárnou. Toto rozšíření používá protokol HTTP k odesílání dokumentů, které rozšíření CRT generuje pro fiskální tiskárnu. Také zpracovává odpovědi, které jsou přijaty z fiskální tiskárny.

#### <a name="request-handler"></a>Obslužná rutina požadavku

Obslužná rutina požadavku **EpsonFP90IIISample** je vstupní bod pro zpracování požadavku na fiskální periferní zařízení.

Tato rutina je zděděna z rozhraní **INamedRequestHandler**. Metoda **HandlerName** je odpovědná za vrácení názvu obslužné rutiny. Název obslužné rutiny by měl odpovídat názvu poskytovatele dokumentu fiskálního konektoru zadanému v centrále Commerce.

Konektor podporuje následující požadavky:

- **SubmitDocumentFiscalDeviceRequest** – tento požadavek odesílá dokumenty tiskárně a vrací odpověď z fiskální tiskárny.
- **IsReadyFiscalDeviceRequest** – tento požadavek se používá pro kontrolu stavu zařízení.
- **InitializeFiscalDeviceRequest** – tento požadavek se používá pro inicializaci tiskárny.

#### <a name="configuration"></a>Konfigurace

Konfigurační soubor pro fiskální konektor se nachází v umístění **src\\FiscalIntegration\\EpsonFP90IIISample\\HardwareStation\\EpsonFP90IIIFiscalDeviceSample\\Configuration\\ConnectorEpsonFP90IIISample.xml** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Tento soubor slouží k povolení nastavení pro konektor ke konfiguraci z centrály Commerce. Formát souboru je v souladu s požadavky na konfiguraci fiskální integrace.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
