---
title: Pokyny k nasazení ukázkové integrace fiskální tiskárny pro Polsko (starší verze)
description: Tento článek obsahuje pokyny pro nasazení ukázky integrace fiskální tiskárny pro Polsko ze sady SDK (Software Development Kit) pro Microsoft Dynamics 365 Commerce Retail.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 883f09f73e3b372d6896b6702e54e2e664cff4d7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286519"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-poland-legacy"></a>Pokyny k nasazení ukázkové integrace fiskální tiskárny pro Polsko (starší verze)

[!include[banner](../includes/banner.md)]

Tento článek obsahuje pokyny pro nasazení ukázkové integrace fiskální tiskárny pro Polsko ze sady SDK (Software Development Kit) pro Microsoft Dynamics 365 Commerce Retail na vývojářském virtuálním počítači (VM) v Microsoft Dynamics Lifecycle Services (LCS). Další informace o této ukázkové fiskální integraci naleznete v tématu [Ukázka integrace fiskální tiskárny pro Polsko](emea-pol-fpi-sample.md). 

Ukázka fiskální integrace pro Polsko je součástí sady Retail SDK. Informace o instalaci a použití sady SDK naleznete v tématu [Architektura sady SDK (Software Development Kit) pro Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md). Tato ukázka sestává z rozšíření pro CRT (Commerce Runtime) a hardwarovou stanici. Ke spuštění tohoto příkladu musíte změnit a sestavit projekty CRT a hardwarové stanice. Doporučujeme používat nemodifikovanou sadu Retail SDK k provedení změn, které jsou popsány v tomto článku. Rovněž doporučujeme používat systém správy zdrojového kódu, jako je Azure DevOps, kde žádné soubory nebyly dosud změněny.

## <a name="development-environment"></a>Vývojové prostředí

Tento postup slouží k nastavení vývojového prostředí, abyste mohli testovat a rozšířit vzorek.

### <a name="commerce-runtime-extension-components"></a>Komponenty rozšíření pro Commerce Runtime

Komponenty rozšíření CRT jsou součástí sady SDK pro Retail. Pro dokončení následujících postupů otevřete řešení **CommerceRuntimeSamples.sln** v umístění **RetailSdk\\SampleExtensions\\CommerceRuntime**.

1. Vyhledejte projekt **Runtime.Extensions.DocumentProvider.PosnetSample** a vytvořte jej.
2. Ve složce **Runtime.Extensions.DocumentProvider.PosnetSample\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Commerce Scale Unit::** Zkopírujte soubor do složky **\\bin\\ext** v umístění webu Internet Information Services (IIS) Commerce Scale Unit.
    - **Místní CRT v Modern POS:** Zkopírujte soubor do složky **\\ext** v umístění místního makléře klienta CRT.

4. Najděte konfigurační soubor rozšíření pro CRT:

    - **Commerce Scale Unit:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Commerce Scale Unit:.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

5. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
    ```

6. Restartujte službu Commerce:

    - **Commerce Scale Unit:** Restartujte web služby Commerce ze správce internetové informační služby (IIS).
    - **Zprostředkovatel klienta:** Ukončete proces **dllhost.exe** ve Správci úloh a poté restartujte Modern POS.

### <a name="hardware-station-extension-components"></a>Komponenty rozšíření hardwarové stanice

Komponenty rozšíření hardwarové stanice jsou součástí sady SDK pro Retail. Pro dokončení následujících postupů otevřete řešení **HardwareStationSamples.sln** v části **RetailSdk\\SampleExtensions\\HardwareStation**.

1. Vyhledejte projekt **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample** a vytvořte jej.
2. Ve složce **Extension.Posnet.ThermalFVFiscalPrinterSample\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll**.
3. Zkopírujte soubor sestavení do nasazeného počítače hardwarové stanice:

    - **Vzdálená hardwarové stanice:** Zkopírujte soubor do složky **bin** v umístění webu hardwarové stanice IIS. Zkopírujte knihovny ovladačů tiskárny (**libposcmbth.dll**, **libcmbth\_serial.dll** a **cmbth\_pl.lng**).

4. Vyhledejte konfigurační soubor rozšíření hardwarové stanice. Název souboru je **HardwareStation.Extension.config**:

    - **Vzdálená hardwarová stanice:** Soubor se nachází pod umístěním webu hardwarové stanice IIS.

5. Přidejte následující řádek do oddílu **composition** konfiguračního souboru.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
    ```

6. Restartujte službu hardwarové stanice:

    - **Vzdálená hardwarová stanice:** Restartujte web hardwarové stanice ze správce internetové informační služby IIS.

## <a name="production-environment"></a>Produkční prostředí

V přechozím postupu jste povolili rozšíření, která jsou součástí ukázky integrace služby fiskální registrace. Kromě toho musíte provést následující postup k vytvoření balíčků pro nasazení, které obsahují komponenty Commerce a použití těchto balíčků v produkčním prostředí.

1. Proveďte následující změny v balíčku konfiguračních souborů ve složce **RetailSdk\\Assets**:

    - V konfiguračních souborech **commerceruntime.ext.config** a **CommerceRuntime.MPOSOffline.Ext.config** přidejte následující řádek do části **composition**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
        ```

    - V konfiguračním souboru **HardwareStation.Extension.config** přidejte následující řádek do oddílu **composition**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
        ```

1. Proveďte následující změny v konfiguračním souboru balíčku přizpůsobení **Customization.settings** ve složce **BuildTools**:

    - Přidejte následující řádek pro zahrnutí rozšíření CRT do nasaditelných balíčků.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll"/>
        ```

    - Přidáte následující řádek pro zahrnutí rozšíření hardwarové stanice do balíčků pro nasazení.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll"/>
        ```

1. Spuste příkazový řádek MSBuild pro program Visual Studio a spusťte **msbuild** ve složce Retail SDK pro vytvoření balíčků k nasazení.
1. Balíčky použijte pomocí služby LCS nebo ručně. Další informace naleznete v tématu [Vytvoření balíčků pro nasazení](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Návrh rozšíření

Ukázka integrace fiskální tiskárny pro Polsko je založena na [funkci fiskální integrace](fiscal-integration-for-retail-channel.md). Další informace o návrhu řešení fiskální integrace naleznete v tématu [Přehled návrhu ukázky fiskální integrace](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Návrh obchodního rozšíření doby běhu

Účelem rozšíření je, ab poskytovatel daňového dokumentu generoval dokumenty specifické pro tiskárnu a zpracovával odpovědi z fiskální tiskárny.

Rozšíření CRT je **Runtime.Extensions.DocumentProvider.PosnetSample**. Toto rozšíření generuje sadu příkazů specifických pro tiskárnu ve formátu JavaScript Object Notation (JSON), které jsou definovány specifikací POSNET 19-3678.

Podrobnější informace o návrhu řešení fiskální integrace získáte v části [Ukázky procesu fiskální registrace pro fiskální zařízení a služby](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Obslužná rutina požadavku

Obslužná rutina požadavků **DocumentProviderPosnetProtocol** je vstupním bodem pro požadavek na generování dokumentů z fiskální tiskárny.

Tato rutina je zděděna z rozhraní **INamedRequestHandler**. Metoda **HandlerName** je odpovědná za vrácení názvu obslužné rutiny. Název obslužné rutiny by měl odpovídat názvu poskytovatele dokumentu zprostředkovatele zadanému v centrále Commerce.

Konektor podporuje následující požadavky:

- **GetFiscalDocumentDocumentProviderRequest** – tento požadavek obsahuje informace o dokladu, o němž by měl být vygenerován dokument. Vrátí dokument specifický pro tiskárnu, který má být registrován ve fiskální tiskárně.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – tento požadavek vrací seznam událostí, k jejichž odběru se uživatelé přihlašují. Aktuálně jsou podporovány následující události: prodej, tisk X sestavy a tisk Z sestavy.

#### <a name="configuration"></a>Konfigurace

Konfigurační soubor se nachází ve složce **Konfigurace** projektu rozšíření. Tento soubor slouží k povolení nastavení pro zprostředkovatele dokumentu ke konfiguraci z centrály Commerce. Formát souboru je v souladu s požadavky na konfiguraci fiskální integrace. Jsou přidána následující nastavení:

- Mapování sazeb DPH
- Mapování typu úhrad
- Typ platby vkladu

### <a name="hardware-station-extension-design"></a>Design rozšíření hardwarové stanice

Účelem rozšíření je fiskální konektor určený ke komunikaci s fiskální tiskárnou.

Rozšíření hardwarové stanice je **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample**. Toto rozšíření volá funkce ovladače POSNET k odesílání příkazů, které rozšíření CRT generuje pro fiskální tiskárnu. Řeší také chyby zařízení.

#### <a name="request-handler"></a>Obslužná rutina požadavku

Obslužná rutina požadavku **FiscalPrinterHandler** je vstupní bod pro zpracování požadavku na fiskální periferní zařízení.

Tato rutina je zděděna z rozhraní **INamedRequestHandler**. Metoda **HandlerName** je odpovědná za vrácení názvu obslužné rutiny. Název obslužné rutiny by měl odpovídat názvu poskytovatele dokumentu fiskálního konektoru zadanému v centrále Commerce.

Konektor podporuje následující požadavky:

- **SubmitDocumentFiscalDeviceRequest** – tento požadavek odesílá dokumenty tiskárně a vrací odpověď z fiskální tiskárny.
- **IsReadyFiscalDeviceRequest** – tento požadavek se používá pro kontrolu stavu zařízení.
- **InitializeFiscalDeviceRequest** – tento požadavek se používá pro inicializaci tiskárny.

#### <a name="configuration"></a>Konfigurace

Konfigurační soubor se nachází ve složce **Konfigurace** projektu rozšíření. Tento soubor slouží k povolení nastavení pro konektor ke konfiguraci z centrály Commerce. Formát souboru je v souladu s požadavky na konfiguraci fiskální integrace. Jsou přidána následující nastavení:

- **Připojovací řetězec** – Řetězec, který popisuje podrobnosti o připojení k zařízení ve formátu, který ovladač podporuje. Další informace naleznete v dokumentaci k ovladači POSNET.
- **Synchronizace data a času** – Hodnota, která určuje, zda se musí datum a čas tiskárny synchronizovat s připojenou hardwarovou stanicí.
- **Časový limit zařízení** – doba v milisekundách, po kterou bude čekat ovladač na odpověď zařízení. Další informace naleznete v dokumentaci k ovladači POSNET.
