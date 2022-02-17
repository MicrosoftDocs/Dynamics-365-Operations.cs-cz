---
title: Vzor integrace fiskální tiskárny pro Polsko
description: V tomto tématu je uveden přehled ukázkové fiskální integrace pro Polsko v Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-2-1
ms.openlocfilehash: 43d9a54334d97a65a1f9a356daf54154f6c069b3
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076829"
---
# <a name="fiscal-printer-integration-sample-for-poland"></a>Vzor integrace fiskální tiskárny pro Polsko

[!include[banner](../includes/banner.md)]

V tomto tématu je uveden přehled ukázkové fiskální integrace pro Polsko v Microsoft Dynamics 365 Commerce.

Funkce Dynamics 365 Commerce pro Polsko zahrnuje ukázkovou integraci pokladního místa (POS) s fiskální tiskárnou. Ukázka rozšiřuje [funkce fiskální integrace](fiscal-integration-for-retail-channel.md) a podporuje protokol POSNET THERMAL HD 2.02 pro fiskální tiskárny od [Posnet Polska S.A.](https://www.posnet.com.pl) Ukázka umožňuje komunikaci s fiskální tiskárnou připojenou přes port COM pomocí nativního softwarového ovladače. Ten byl implementován a testován s použitím softwarového emulátoru, který Posnet poskytl pro fiskální tiskárnu Posnet Thermal HD FV EJ. Ukázka je poskytnuta ve formě zdrojového kódu a je součástí sady software development kit (SDK) pro maloobchod.

Společnost Microsoft nevydává žádný hardware, software nebo dokumentaci společnosti Posnet. Pro informace, jak získat fiskální tiskárnu a jak ji obsluhovat, kontaktujte společnost [Posnet Polska S.A.](https://www.posnet.com.pl)

## <a name="scenarios"></a>Scénáře

Následující scénáře uvádějí ukázku integrace fiskální tiskárny pro Polsko:

- Prodejní scénáře:

    - Tisk fiskální příjemky pro prodej typu cash-and-carry a vratky.
    - Zachycení odpovědi z fiskální tiskárny a její uložení do databáze kanálů.
    - Daně:

        - Mapování na daňové kódy (oddělení) fiskální tiskárny.
        - Přenos mapovaných dat daní do fiskální tiskárny.

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

    - Tisk [informací o odběrateli](emea-pol-customer-information.md), který je zadán pro prodejní transakci na fiskání příjemku. Příkladem této informace je číslo DPH zákazníka.

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
- Denní sestavy (fiskální X a fiskální Z) se tisknou pomocí vestavěného formátu *Sestava směny*.
- Tisk čárového kódu na fiskální příjemky se považuje za potenciální přizpůsobení, protože tato funkce není podporována ve vložených formátech a lze ji implementovat pouze pomocí přizpůsobitelné sestavy v **super-formátu**.
- Fiskální tiskárna nepodporuje smíšené transakce. Možnost **Zakázat smíšené prodeje a vratky na jedné příjemce** by měla být nastavena na **Ano** v profilech funkcí POS.

## <a name="set-up-fiscal-integration-for-poland"></a>Nastavení fiskální integrace pro Polsko

Ukázka integrace fiskální tiskárny pro Polsko je založena na [funkci fiskální integrace](fiscal-integration-for-retail-channel.md) a je součástí řešení Retail SDK. Ukázka se nachází ve složce **src\\FiscalIntegration\\Posnet** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (například [ukázka ve verzi/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet)). Ukázka [se skládá](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) ze zprostředkovatele fiskálního dokumentu, což je rozšíření řešení Commerce Runtime (CRT) a fiskálního konektoru, který je rozšířením hardwarové stanice Commerce. Další informace o použití sady Retail SDK naleznete v části [Architektura Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) a [Nastavení kanálu sestavení pro sadu SDK nezávislého balení](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Kvůli omezením [nového modelu nezávislého balíčku a rozšíření](../dev-itpro/build-pipeline.md) jej v současné době nelze pro tuto ukázku fiskální integrace použít. Musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači (VM) v Microsoft Dynamics Lifecycle Services (LCS). Další informace viz [Pokyny k nasazení ukázkové integrace fiskální tiskárny pro Polsko (starší verze)](emea-pol-fpi-sample-sdk.md).
>
> Podpora nového modelu nezávislého balení a rozšíření pro vzorky fiskální integrace je plánována pro pozdější verze.

Postupujte podle kroků pro nastavení fiskální integrace popsané v části [Nastavení fiskální integrace pro kanály Commerce](setting-up-fiscal-integration-for-retail-channel.md).

1. [Nastavení procesu fiskální registrace](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Kromě toho si všimněte nastavení pro proces fiskální registrace, která jsou [specifická pro tuto ukázku integrace fiskální tiskárny](#set-up-the-registration-process).
1. [Nastavení zpracování chyb](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Nastavení fiskálních sestav X/ Z z POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Povolit ruční provedení zápisu odložené daňové registrace](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurace komponent kanálu](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Nastavení procesu registrace

Pokud chcete povolit registrační proces, postupujte pomocí následujících kroků pro nastavení centrály Commerce. Další informace viz [Nastavení fiskální integrace pro obchodní kanály](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Stáhněte si konfigurační soubory pro poskytovatele fiskálních dokumentů a fiskální konektor:

    1. Otevřete úložiště [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Vyberte správnou verzi větve vydání podle vaší verze SDK/aplikace (například **[vydání/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Otevřete **src \> FiscalIntegration \> Posnet**.
    1. Stáhněte si konfigurační soubor poskytovatele fiskálních dokumentů v umístění **CommerceRuntime \> DocumentProvider.PosnetSample \> Configuration \> DocumentProviderPosnetSample.xml** (například [soubor pro vydání/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/CommerceRuntime/DocumentProvider.PosnetSample/Configuration/DocumentProviderPosnetSample.xml)).
    1. Stáhněte si konfigurační soubor konektoru v umístění **HardwareStation \> ThermalDeviceSample \> Configuration \> ConnectorPosnetThermalFVEJ.xml** (například [soubor pro vydání/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/HardwareStation/ThermalDeviceSample/Configuration/ConnectorPosnetThermalFVEJ.xml)).

    > [!WARNING]
    > Kvůli omezením [nového modelu nezávislého balíčku a rozšíření](../dev-itpro/build-pipeline.md) jej v současné době nelze pro tuto ukázku fiskální integrace použít. Musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači v LCS. Konfigurační soubory pro tuto ukázku fiskální integrace jsou umístěny v následujících složkách Retail SDK na vývojářském virtuálním počítači v LCS:
    >
    > - **Konfigurační soubor poskytovatele fiskálních dokumentů:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extension.DocumentProvider.PosnetSample\\Configuration\\DocumentProviderPosnetSample.xml
    > - **Konfigurační soubor fiskálního konektoru:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.Posnet.ThermalDeviceSample\\Configuration\\ConnectorPosnetThermalFVEJ.xml
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

- **Mapování sazeb daně z přidané hodnoty (DPH)** – Mapování procentních hodnot daně, které jsou nastaveny pro kódy DPH, na sazby DPH specifické pro fiskální tiskárnu. Zde je výchozí mapování:

    ```
    0 : 23.00 ; 1 : 8.00 ; 2 : 5.00 ; 3 : 0.00
    ```

    První komponenta v každém páru představuje číslo sazby DPH, které je nakonfigurováno ve fiskální tiskárně. Druhá složka představuje odpovídající sazbu DPH. Další informace o konfiguraci sazby DPH pro fiskální tiskárnu naleznete v dokumentaci k ovladači POSNET.

- **Mapování typu úhrady** – Mapování platebních metod, které jsou pro obchod nakonfigurovány, na formuláře plateb, které podporuje fiskální tiskárna. Zde je výchozí mapování:

    ```
    0 : 0 ; 1 : 0 ; 2 : 2 ; 3 : 2 ; 4 : 0 ; 5 : 0 ; 6 : 0 ; 7 : 2 ; 8 : 0
    ```

    První komponenta v každém páru představuje platební metodu, která je nastavena pro obchod. Druhá komponenta představuje odpovídající platební formulář, který je podporován fiskální tiskárnou. Další informace o formulářích platby podporovaných fiskální tiskárnou naleznete v dokumentaci k ovladači POSNET. Musíte upravit vzorové mapování podle platebních metod, které jsou nakonfigurovány ve vaší aplikaci.

#### <a name="fiscal-connector-settings"></a>Nastavení fiskálního konektoru

Následující nastavení jsou součástí konfigurace fiskálního konektoru, který je poskytován jako ukázka fiskální integrace:

- **Připojovací řetězec** – Řetězec, který popisuje podrobnosti o připojení k zařízení ve formátu, který ovladač podporuje. Další informace naleznete v dokumentaci k ovladači POSNET.
- **Synchronizace data a času** – Hodnota, která určuje, zda se musí datum a čas tiskárny synchronizovat s připojenou hardwarovou stanicí.
- **Časový limit zařízení** – doba v milisekundách, po kterou bude čekat ovladač na odpověď zařízení. Další informace naleznete v dokumentaci k ovladači POSNET.

### <a name="configure-channel-components"></a>Konfigurace komponent kanálu

> [!WARNING]
> Kvůli omezením [nového modelu nezávislého balíčku a rozšíření](../dev-itpro/build-pipeline.md) jej v současné době nelze pro tuto ukázku fiskální integrace použít. Musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači v LCS. Další informace viz [Pokyny k nasazení ukázkové integrace fiskální tiskárny pro Polsko (starší verze)](emea-pol-fpi-sample-sdk.md).
>
> Podpora nového modelu nezávislého balení a rozšíření pro vzorky fiskální integrace je plánována pro pozdější verze.

#### <a name="set-up-the-development-environment"></a>Nastavení vývojového prostředí

Tento postup slouží k nastavení vývojového prostředí, abyste mohli testovat a rozšířit ukázku.

1. Naklonujte nebo stáhněte úložiště [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions). Vyberte správnou verzi větve vydání podle vaší verze SDK/aplikace. Další informace viz [Stažení ukázek Retail SDK a referenčních balíčků z GitHub a NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Otevřete řešení integrace fiskální tiskárny v umístění **Dynamics365Commerce.Solutions\\FiscalIntegration\\Posnet\\Posnet.sln** a sestavte jej.
1. Nainstalujte rozšíření CRT:

    1. Vyhledejte instalační program rozšíření CRT:

        - **Commerce Scale Unit:** Ve složce **Posnet\\ScaleUnit\\ScaleUnit.Posnet.Installer\\bin\\Debug\\net461** vyhledejte instalační program **ScaleUnit.Posnet.Installer**.
        - **Místní CRT v Modern POS:** Ve složce **Posnet\\ModernPOS\\ModernPOS.Posnet.Installer\\bin\\Debug\\net461** vyhledejte instalační program **ModernPOS.Posnet.Installer**.

    1. Spusťte instalační program rozšíření CRT z příkazového řádku:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.Posnet.Installer.exe install --verbosity 0
            ```

        - **Místní CRT v Modern POS:**

            ```Console
            ModernPOS.Posnet.Installer.exe install --verbosity 0
            ```

1. Instalace rozšíření hardwarové stanice:

    1. Ve složce **Posnet\\HardwareStation\\HardwareStation.PosnetThermalFVFiscalPrinter.Installer\\bin\\Debug\\net461** vyhledejte instalační program **HardwareStation.PosnetThermalFVFiscalPrinter.Installer**.
    1. Spusťte instalační program rozšíření z příkazového řádku:

        ```Console
        HardwareStation.PosnetThermalFVFiscalPrinter.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Produkční prostředí

Postupujte podle kroků v části [Nastavení kanálu buildu pro ukázku fiskální integrace](fiscal-integration-sample-build-pipeline.md), kterými vygenerujete a uvolníte nasaditelné balíčky Cloud Scale Unit a samoobslužné nasaditelné balíčky pro ukázku fiskální integrace. Soubor YAML šablony **Posnet build-pipeline.yml** se nachází ve složce **Pipeline\\YAML_Files** úložiště [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-extensions"></a>Návrh rozšíření

Ukázka integrace fiskální tiskárny pro Polsko je založena na [funkci fiskální integrace](fiscal-integration-for-retail-channel.md) a je součástí řešení Retail SDK. Ukázka se nachází ve složce **src\\FiscalIntegration\\Posnet** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (například [ukázka ve verzi/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet)). Ukázka [se skládá](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) ze zprostředkovatele fiskálního dokumentu, což je rozšíření řešení CRT a fiskálního konektoru, který je rozšířením hardwarové stanice Commerce. Další informace o použití sady Retail SDK naleznete v části [Architektura Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) a [Nastavení kanálu sestavení pro sadu SDK nezávislého balení](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Kvůli omezením [nového modelu nezávislého balíčku a rozšíření](../dev-itpro/build-pipeline.md) jej v současné době nelze pro tuto ukázku fiskální integrace použít. Musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači v LCS. Další informace viz [Pokyny k nasazení ukázkové integrace fiskální tiskárny pro Polsko (starší verze)](emea-pol-fpi-sample-sdk.md). Podpora nového modelu nezávislého balení a rozšíření pro vzorky fiskální integrace je plánována pro pozdější verze.

### <a name="commerce-runtime-extension-design"></a>Návrh obchodního rozšíření doby běhu

Účelem rozšíření je, ab poskytovatel daňového dokumentu generoval dokumenty specifické pro tiskárnu a zpracovával odpovědi z fiskální tiskárny. Toto rozšíření generuje sadu příkazů specifických pro tiskárnu ve formátu JavaScript Object Notation (JSON), které jsou definovány specifikací POSNET 19-3678.

#### <a name="request-handler"></a>Obslužná rutina požadavku

Obslužná rutina požadavků **DocumentProviderPosnetProtocol** je vstupním bodem pro požadavek na generování dokumentů z fiskální tiskárny.

Tato rutina je zděděna z rozhraní **INamedRequestHandler**. Metoda **HandlerName** je odpovědná za vrácení názvu obslužné rutiny. Název obslužné rutiny by měl odpovídat názvu poskytovatele dokumentu zprostředkovatele zadanému v centrále Commerce.

Konektor podporuje následující požadavky:

- **GetFiscalDocumentDocumentProviderRequest** – tento požadavek obsahuje informace o dokladu, o němž by měl být vygenerován dokument. Vrátí dokument specifický pro tiskárnu, který má být registrován ve fiskální tiskárně.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – tento požadavek vrací seznam událostí, k jejichž odběru se uživatelé přihlašují. Aktuálně jsou podporovány následující události: prodej, tisk X sestavy a tisk Z sestavy.

#### <a name="configuration"></a>Konfigurace

Konfigurační soubor pro poskytovatele fiskálních dokumentů se nachází v umístění **src\\FiscalIntegration\\Posnet\\CommerceRuntime\\DocumentProvider.PosnetSample\\Configuration\\DocumentProviderPosnetSample.xml** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Tento soubor slouží k povolení konfigurace nastavení zprostředkovatele fiskálního dokumentu z centrály Commerce. Formát souboru je v souladu s požadavky na konfiguraci fiskální integrace.

### <a name="hardware-station-extension-design"></a>Design rozšíření hardwarové stanice

Účelem rozšíření je fiskální konektor určený ke komunikaci s fiskální tiskárnou. Toto rozšíření volá funkce ovladače POSNET k odesílání příkazů, které rozšíření CRT generuje pro fiskální tiskárnu. Řeší také chyby zařízení.

#### <a name="request-handler"></a>Obslužná rutina požadavku

Obslužná rutina požadavku **FiscalPrinterHandler** je vstupní bod pro zpracování požadavku na fiskální periferní zařízení.

Tato rutina je zděděna z rozhraní **INamedRequestHandler**. Metoda **HandlerName** je odpovědná za vrácení názvu obslužné rutiny. Název obslužné rutiny by měl odpovídat názvu poskytovatele dokumentu fiskálního konektoru zadanému v centrále Commerce.

Konektor podporuje následující požadavky:

- **SubmitDocumentFiscalDeviceRequest** – tento požadavek odesílá dokumenty tiskárně a vrací odpověď z fiskální tiskárny.
- **IsReadyFiscalDeviceRequest** – tento požadavek se používá pro kontrolu stavu zařízení.
- **InitializeFiscalDeviceRequest** – tento požadavek se používá pro inicializaci tiskárny.

#### <a name="configuration"></a>Konfigurace

Konfigurační soubor pro fiskální konektor se nachází v umístění **src\\FiscalIntegration\\Posnet\\HardwareStation\\ThermalDeviceSample\\Configuration\\ConnectorPosnetThermalFVEJ.xml** v úložišti [Řešení Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Tento soubor slouží k povolení nastavení pro fiskální konektor ke konfiguraci z centrály Commerce. Formát souboru je v souladu s požadavky na konfiguraci fiskální integrace.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
