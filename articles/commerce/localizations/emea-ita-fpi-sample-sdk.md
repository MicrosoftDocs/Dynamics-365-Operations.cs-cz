---
title: Pokyny k nasazení ukázkové integrace fiskální tiskárny pro Itálii (starší verze)
description: Toto téma obsahuje pokyny pro nasazení ukázky integrace fiskální tiskárny pro Itálii ze sady SDK (Software Development Kit) pro Microsoft Dynamics 365 Commerce Retail.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 93aca34239affb41998f4309d7c03f29f7b5f003
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076879"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-italy-legacy"></a>Pokyny k nasazení ukázkové integrace fiskální tiskárny pro Itálii (starší verze)

[!include[banner](../includes/banner.md)]

Toto téma obsahuje pokyny pro nasazení ukázkové integrace fiskální tiskárny pro Itálii ze sady SDK (Software Development Kit) pro Microsoft Dynamics 365 Commerce Retail na vývojářském virtuálním počítači (VM) v Microsoft Dynamics Lifecycle Services (LCS). Další informace o této ukázkové fiskální integraci naleznete v tématu [Ukázka integrace fiskální tiskárny pro Itálii](emea-ita-fpi-sample.md). 

Ukázka fiskální integrace pro Itálii je součástí sady Retail SDK. Informace o instalaci a použití sady SDK naleznete v tématu [Architektura sady SDK (Software Development Kit) pro Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md). Tato ukázka sestává z rozšíření pro CRT (Commerce Runtime) a hardwarovou stanici. Ke spuštění tohoto příkladu musíte změnit a sestavit projekty CRT a hardwarové stanice. Doporučujeme používat nemodifikovanou sadu Retail SDK k provedení změn, které jsou popsány v tomto tématu. Rovněž doporučujeme používat systém správy zdrojového kódu, jako je Azure DevOps, kde žádné soubory nebyly dosud změněny.

## <a name="development-environment"></a>Vývojové prostředí

Tento postup slouží k nastavení vývojového prostředí, abyste mohli testovat a rozšířit vzorek.

### <a name="commerce-runtime-extension-components"></a>Komponenty rozšíření pro Commerce Runtime

Komponenty rozšíření CRT jsou součástí sady SDK pro Retail. Pro dokončení následujících postupů otevřete řešení **CommerceRuntimeSamples.sln** v umístění **RetailSdk\\SampleExtensions\\CommerceRuntime**.

1. Vyhledejte projekt **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample** a vytvořte jej.
2. Ve složce **Extensions.DocumentProvider.EpsonFP90IIISample\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Commerce Scale Unit::** Zkopírujte soubor do složky **\\bin\\ext** v umístění webu Internet Information Services (IIS) Commerce Scale Unit.
    - **Místní CRT v Modern POS:** Zkopírujte soubor do složky **\\ext** v umístění místního makléře klienta CRT.

4. Najděte konfigurační soubor rozšíření pro CRT:

    - **Commerce Scale Unit:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Commerce Scale Unit:.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

5. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
    ```

6. Restartujte Commerce Scale Unit:

    - **Commerce Scale Unit:** Restartujte web Commerce Scale Unit ze správce internetové informační služby (IIS).
    - **Zprostředkovatel klienta:** Ukončete proces **dllhost.exe** ve Správci úloh a poté restartujte Modern POS.

### <a name="hardware-station-extension-components"></a>Komponenty rozšíření hardwarové stanice

Komponenty rozšíření hardwarové stanice jsou součástí sady SDK pro Retail. Pro dokončení následujících postupů otevřete řešení **HardwareStationSamples.sln** v části **RetailSdk\\SampleExtensions\\HardwareStation**.

1. Vyhledejte projekt **HardwareStation.Extensions.EpsonFP90IIIFiscalDeviceSample** a vytvořte jej.
2. Ve složce **Extensions.EpsonFP90IIIFiscalDeviceSample\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll**.
3. Zkopírujte soubor sestavení do nasazeného počítače hardwarové stanice:

    - **Vzdálená hardwarové stanice:** Zkopírujte soubor do složky **bin** v umístění webu hardwarové stanice IIS.
    - **Místní hardwarová stanice:** Zkopírujte soubor do stanice zprostředkovatele klienta Modern POS.

4. Vyhledejte konfigurační soubor rozšíření hardwarové stanice. Název souboru je **HardwareStation.Extension.config**:

    - **Vzdálená hardwarová stanice:** Soubor se nachází pod umístěním webu hardwarové stanice IIS.
    - **Místní hardwarová stanice:** Soubor se nachází v umístění zprostředkovatele klienta Modern POS.

5. Přidejte následující sekci do oddílu **composition** konfiguračního souboru.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
    ```

6. Restartujte službu hardwarové stanice:

    - **Vzdálená hardwarová stanice:** Restartujte web hardwarové stanice ze správce internetové informační služby IIS.
    - **Místní hardwarová stanice:** Ukončete proces **dllhost.exe** ve Správci úloh a poté restartujte Modern POS.

## <a name="production-environment"></a>Produkční prostředí

Následujícím postupem vytvoříte balíčky pro nasazení, které obsahují komponenty Commerce, a použijete tyto balíčky v provozním prostředí.

1. Proveďte kroky popsané v sekci [Vývojové prostředí](#development-environment) výše v tomto tématu.
2. Proveďte následující změny v balíčku konfiguračních souborů ve složce **RetailSdk\\Assets**:

    - V konfiguračních souborech **commerceruntime.ext.config** a **CommerceRuntime.MPOSOffline.Ext.config** přidejte následující řádek do části **composition**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
        ```

    - V konfiguračním souboru **HardwareStation.Extension.config** přidejte následující řádek do oddílu **composition**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
        ```

3. Proveďte následující změny v konfiguračním souboru balíčku přizpůsobení **Customization.settings** ve složce **BuildTools**:

    - Přidejte následující řádek pro zahrnutí rozšíření CRT do nasaditelných balíčků.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll"/>
        ```

    - Přidáte následující řádek pro zahrnutí rozšíření hardwarové stanice do balíčků pro nasazení.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll"/>
        ```

4. Spusťte příkazový řádek MSBuild pro program Visual Studio a poté spusťte **msbuild** ve složce Retail SDK pro vytvoření balíčků k nasazení.
5. Balíčky použijte pomocí služby LCS nebo ručně. Další informace naleznete v tématu [Vytvoření balíčků pro nasazení](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Návrh rozšíření

### <a name="commerce-runtime-extension-design"></a>Návrh obchodního rozšíření doby běhu

Účelem rozšíření je, ab poskytovatel daňového dokumentu generoval dokumenty specifické pro tiskárnu a zpracovával odpovědi z fiskální tiskárny.

Rozšíření CRT je **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample**.

Podrobnější informace o návrhu řešení fiskální integrace získáte v části [Ukázky procesu fiskální registrace pro fiskální zařízení a služby](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Obslužná rutina požadavku

Obslužná rutina požadavků **DocumentProviderEpsonFP90III** je vstupním bodem pro požadavek na generování dokumentů z fiskální tiskárny.

Tato rutina je zděděna z rozhraní **INamedRequestHandler**. Metoda **HandlerName** je odpovědná za vrácení názvu obslužné rutiny. Název obslužné rutiny by měl odpovídat názvu poskytovatele dokumentu zprostředkovatele zadanému v centrále Commerce.

Konektor podporuje následující požadavky:

- **GetFiscalDocumentDocumentProviderRequest** – tento požadavek obsahuje informace o dokladu, o němž by měl být vygenerován dokument. Vrátí dokument specifický pro tiskárnu, který má být registrován ve fiskální tiskárně.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – tento požadavek vrací seznam událostí, k jejichž odběru se uživatelé přihlašují. Aktuálně jsou podporovány následující události: prodej, tisk X sestavy a tisk Z sestavy.

#### <a name="configuration"></a>Konfigurace

Konfigurační soubor se nachází ve složce **Konfigurace** projektu rozšíření. Tento soubor slouží k povolení nastavení pro zprostředkovatele dokumentu ke konfiguraci z centrály Commerce. Formát souboru je v souladu s požadavky na konfiguraci fiskální integrace. Jsou přidána následující nastavení:

- Mapování kódů DPH
- Mapování sazeb DPH
- Mapování typu úhrad
- Typ čárového kódu pro číslo příjemky
- Typ platby vkladu

### <a name="hardware-station-extension-design"></a>Design rozšíření hardwarové stanice

Účelem rozšíření je fiskální konektor určený ke komunikaci s fiskální tiskárnou.

Rozšíření hardwarové stanice je **HardwareStation.Extension.EpsonFP90IIIFiscalDeviceSample**. Toto rozšíření používá protokol HTTP k odesílání dokumentů, které rozšíření CRT generuje pro fiskální tiskárnu. Také zpracovává odpovědi, které jsou přijaty z fiskální tiskárny.

#### <a name="request-handler"></a>Obslužná rutina požadavku

Obslužná rutina požadavku **EpsonFP90IIISample** je vstupní bod pro zpracování požadavků na fiskální periferní zařízení.

Tato rutina je zděděna z rozhraní **INamedRequestHandler**. Metoda **HandlerName** je odpovědná za vrácení názvu obslužné rutiny. Název obslužné rutiny by měl odpovídat názvu poskytovatele dokumentu fiskálního konektoru zadanému v centrále Commerce.

Konektor podporuje následující požadavky:

- **SubmitDocumentFiscalDeviceRequest** – tento požadavek odesílá dokumenty tiskárně a vrací odpověď z fiskální tiskárny.
- **IsReadyFiscalDeviceRequest** – tento požadavek se používá pro kontrolu stavu zařízení.
- **InitializeFiscalDeviceRequest** – tento požadavek se používá pro inicializaci tiskárny.

#### <a name="configuration"></a>Konfigurace

Konfigurační soubor se nachází ve složce **Konfigurace** projektu rozšíření. Tento soubor slouží k povolení nastavení pro konektor ke konfiguraci z centrály Commerce. Formát souboru je v souladu s požadavky na konfiguraci fiskální integrace. Jsou přidána následující nastavení:

- **Adresa koncového bodu** – adresa URL tiskárny.
- **Synchronizace data a času** – Hodnota, která určuje, zda se musí datum a čas tiskárny synchronizovat s připojenou hardwarovou stanicí.
