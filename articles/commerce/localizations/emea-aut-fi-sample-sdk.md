---
title: Pokyny k nasazení ukázkové integrace služby fiskální registrace pro Rakousko (starší verze)
description: Tento článek obsahuje pokyny pro nasazení ukázky fiskální integrace pro Rakousko ze sady SDK (Software Development Kit) pro Microsoft Dynamics 365 Commerce Retail.
author: EvgenyPopovMBS
ms.date: 08/17/2022
ms.topic: article
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 8d41dfb359a71f24d0cb0c5aa0114225cd28fe59
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473991"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-austria-legacy"></a>Pokyny k nasazení ukázkové integrace služby fiskální registrace pro Rakousko (starší verze)

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Pokyny v tomto článku musíte dodržovat pouze v případě, že používáte Microsoft Dynamics 365 Commerce verze 10.0.28 nebo starší. Od verze Commerce 10.0.29 je ukázka integrace služby fiskální registrace pro Rakousko je k dispozici v Commerce software development kit (SDK). Další informace naleznete v tématu [Konfigurace komponent kanálů](./emea-aut-fi-sample.md#configure-channel-components).

Tento článek obsahuje pokyny pro nasazení ukázkové integrace služby fiskální registrace pro Rakousko z Dynamics 365 Commerce Retail SDK na vývojářském virtuálním počítači (VM) v Microsoft Dynamics Lifecycle Services (LCS). Další informace o této ukázkové fiskální integraci naleznete v tématu [Ukázka integrace služby fiskální registrace pro Rakousko](emea-aut-fi-sample.md). 

Ukázka fiskální integrace pro Rakousko je součástí sady Retail SDK. Informace o instalaci a použití sady SDK naleznete v tématu [Architektura sady SDK (Software Development Kit) pro Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md). Ukázka fiskální integrace sestává z rozšíření pro Commerce Runtime (CRT), hardwarovou stanici a pokladní místo (POS). Ke spuštění tohoto příkladu musíte změnit a sestavit projekty CRT, hardwarové stanice a POS. Doporučujeme používat nemodifikovanou sadu Retail SDK k provedení změn, které jsou popsány v tomto článku. Rovněž doporučujeme používat systém správy zdrojového kódu, jako je Azure DevOps, kde žádné soubory nebyly dosud změněny.

## <a name="development-environment"></a>Vývojové prostředí

Tento postup slouží k nastavení vývojového prostředí, abyste mohli testovat a rozšířit vzorek.

### <a name="enable-commerce-runtime-extensions"></a>Povolit rozšíření služby Commerce runtime

Komponenty rozšíření CRT jsou součástí ukázek CRT. Pro dokončení následujících postupů otevřete řešení **CommerceRuntimeSamples.sln** v umístění **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="documentproviderefrsample-component"></a>Komponenta DocumentProvider.EFRSample

1. Najděte projekt **Runtime.Extensions.DocumentProvider.EFRSample** a vytvořte ho.
2. Ve složce **Runtime.Extensions.DocumentProvider.EFRSample\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Commerce Scale Unit::** Zkopírujte soubor do složky **\\bin\\ext** v umístění webu Internet Information Services (IIS) Commerce Scale Unit.
    - **Místní CRT v Modern POS:** Zkopírujte soubor do složky **\\ext** v umístění místního makléře klienta CRT.

4. Najděte konfigurační soubor rozšíření pro CRT:

    - **Commerce Scale Unit:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Commerce Scale Unit:.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

5. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>Komponenta DocumentProvider.DataModelEFR

1. Najděte projekt **Runtime.Extensions.DocumentProvider.DataModelEFR** a vytvořte ho.
2. Ve složce **Runtime.Extensions.DocumentProvider.DataModelEFR\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Commerce Scale Unit::** Zkopírujte soubor do složky **\\bin\\ext** v umístění webu ISS Commerce Scale Unit.
    - **Místní CRT v Modern POS:** Zkopírujte soubor do složky **\\ext** v umístění místního makléře klienta CRT.

4. Najděte konfigurační soubor rozšíření pro CRT:

    - **Commerce Scale Unit:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Commerce Scale Unit:.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

5. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>Konfigurační soubor rozšíření

1. Najděte konfigurační soubor rozšíření pro CRT:

    - **Commerce Scale Unit:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Commerce Scale Unit:.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

2. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>Zapnutí rozšíření fiskálních konektorů

Rozšíření fiskálního konektoru můžete zapnout na [hardwarové stanici](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) nebo [registru POS](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

#### <a name="enable-hardware-station-extensions"></a>Povolení rozšíření hardwarové stanice

Komponenty rozšíření hardwarové stanice jsou součástí ukázek hardwarové stanice. Pro dokončení následujících postupů otevřete řešení **HardwareStationSamples.sln** v části **RetailSdk\\SampleExtensions\\HardwareStation**.

##### <a name="efrsample-component"></a>Komponenta EFRSample

1. Najděte projekt **HardwareStation.Extension.EFRSample** a vytvořte ho.
2. Ve složce **Extension.EFRSample\\bin\\Debug** vyhledejte následující soubory sestavení:

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

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

#### <a name="enable-pos-extensions"></a>Zapnutí rozšíření POS

Ukázka rozšíření POS se nachází ve složce **src\\FiscalIntegration\\PosFiscalConnectorSample** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/).

Chcete-li používat ukázku rozšíření POS ve starší sadě SDK, postupujte takto.

1. Zkopírujte složku **Pos.Extension** do POS složky **Extensions** starší sady SDK (např. `C:\RetailSDK\src\POS\Extensions`).
1. Přejmenujte kopii složky **Pos.Extension** **PosFiscalConnector**.
1. Odeberte následující složky a soubory ze složky **PosFiscalConnector**:

    - bin
    - DataService
    - devDependencies
    - Knihovny
    - obj
    - Contoso.PosFiscalConnectorSample.Pos.csproj
    - RetailServerEdmxModel.g.xml
    - tsconfig.json

1. Otevřete řešení **CloudPos.sln** nebo **ModernPos.sln**.
1. Do projektu **Pos.Extensions** zahrňte složku **PosFiscalConnector**.
1. Otevřete soubor **extensions.json** a přidejte rozšíření **PosFiscalConnector**.
1. Sestavte sadu SDK.

### <a name="enable-modern-pos-extension-components"></a>Povolení komponent rozšíření Modern POS

1. Otevřete řešení **ModernPOS.sln** v umístění **RetailSdk\\POS** a ujistěte se, že jej lze zkompilovat bez chyb. Kromě toho se ujistěte, že můžete spustit Modern POS z aplikace Visual Studio pomocí příkazu **Run**.

    > [!NOTE]
    > Modern POS se nesmí přizpůsobovat. Musíte povolit nástroj Řízení uživatelských účtů (UAC) a podle potřeby odinstalovat dříve nainstalované instance Modern POS.

2. Povolte rozšíření, která mají být načtena v souboru **extensions.json**, přidáním následujících řádků.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > Další informace a ukázky, které ukazují, jak zahrnout složky zdrojového kódu a povolit načítání rozšíření, naleznete v pokynech v souboru readme.md v projektu **Pos.Extensions**.

3. Znovu sestavte řešení.
4. Spusťte Modern POS v ladicím programu a otestujte funkčnost.

### <a name="enable-cloud-pos-extension-components"></a>Povolení komponent rozšíření Cloud POS

1. Otevřete řešení **CloudPOS.sln** v umístění **RetailSdk\\POS** a ujistěte se, že jej lze zkompilovat bez chyb.
2. Povolte rozšíření, která mají být načtena v souboru **extensions.json**, přidáním následujících řádků.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > Další informace a ukázky, které ukazují, jak zahrnout složky zdrojového kódu a povolit načítání rozšíření, naleznete v pokynech v souboru readme.md v projektu **Pos.Extensions**.

3. Znovu sestavte řešení.
4. Spusťte řešení příkazem **Run** a postupujte podle kroků v příručce Retail SDK.

## <a name="production-environment"></a>Produkční prostředí

Předchozí postup umožňuje rozšíření, která jsou součástí ukázky integraci vzorku služby daňové registrace. Kromě toho musíte provést následující postup k vytvoření balíčků pro nasazení, které obsahují komponenty Commerce a použití těchto balíčků v produkčním prostředí.

1. Proveďte následující změny v balíčku konfiguračních souborů ve složce **RetailSdk\\Assets**:

    - V konfiguračních souborech **commerceruntime.ext.config** a **CommerceRuntime.MPOSOffline.Ext.config** přidejte následující řádky do části **composition**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
        ```

    - V konfiguračním souboru **HardwareStation.Extension.config** přidejte následující řádek do oddílu **composition**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

2. Proveďte následující změny v konfiguračním souboru balíčku přizpůsobení **Customization.settings** ve složce **BuildTools**:

    - Přidejte následující řádky pro zahrnutí rozšíření CRT do nasaditelných balíčků.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Přidáte následující řádek pro zahrnutí rozšíření hardwarové stanice do balíčků pro nasazení.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Spuste příkazový řádek MSBuild pro program Visual Studio a spusťte **msbuild** ve složce Retail SDK pro vytvoření balíčků k nasazení.
4. Balíčky použijte pomocí služby LCS nebo ručně. Další informace naleznete v tématu [Vytvoření balíčků pro nasazení](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Proveďte všechny požadované úkoly nastavení, které jsou popsány v části [Nastavení Commerce pro Rakousko](emea-aut-fi-sample.md#set-up-commerce-for-austria).

## <a name="design-of-extensions"></a>Návrh rozšíření

Ukázka integrace služby fiskální registrace pro Rakousko je založena na [funkci fiskální integrace](fiscal-integration-for-retail-channel.md). Další informace o návrhu řešení fiskální integrace naleznete v tématu [Přehled návrhu ukázky fiskální integrace](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Návrh obchodního rozšíření doby běhu

Účelem rozšíření je, ab poskytovatel daňového dokumentu generoval dokumenty specifické pro službu a zpracovával odpovědi z daňové registrační služby.

Rozšíření CRT je **Runtime.Extensions.DocumentProvider.EFRSample**.

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

Konfigurační soubory se nachází ve složce **Konfigurace** projektu rozšíření:

- **DocumentProviderFiscalEFRSampleAustria** – Pro fiskální dokumenty.
- **DocumentProviderNonFiscalEFRSampleAustria** – Pro nefiskální dokumenty.

Tyto soubory slouží k povolení nastavení pro zprostředkovatele dokumentu ke konfiguraci z centrály Commerce. Formát souboru je v souladu s požadavky na konfiguraci fiskální integrace. Jsou přidána následující nastavení:

- Mapování sazeb DPH

### <a name="hardware-station-extension-design"></a>Design rozšíření hardwarové stanice

Účelem rozšíření fiskálního konektoru je komunikace se službou daňové registrace. Rozšíření hardwarové stanice má název **HardwareStation.Extension.EFRSample**. Používá protokol HTTP nebo HTTPS k odesílání dokumentů, které rozšíření CRT generuje pro daňovou registrační službu. Také zpracovává odpovědi, které jsou přijaty ze služby daňové registrace.

#### <a name="request-handler"></a>Obslužná rutina požadavku

Obslužná rutina požadavku **EFRHandler** je vstupní bod pro práci s požadavky služby daňové registrace.

Tato rutina je zděděna z rozhraní **INamedRequestHandler**. Metoda **HandlerName** je odpovědná za vrácení názvu obslužné rutiny. Název obslužné rutiny by měl odpovídat názvu poskytovatele dokumentu fiskálního konektoru zadanému v centrále Commerce.

Konektor podporuje následující požadavky:

- **SubmitDocumentFiscalDeviceRequest** – tento požadavek odesílá dokumenty službě daňové registrace a z ní vrátí odpověď.
- **IsReadyFiscalDeviceRequest** – tento požadavek se používá pro kontrolu stavu služby daňové registrace.
- **InitializeFiscalDeviceRequest** – tento požadavek se používá pro inicializaci stavu služby daňové registrace.

#### <a name="configuration"></a>Konfigurace

Konfigurační soubor se nachází ve složce **Konfigurace** projektu rozšíření. Tento soubor slouží k povolení nastavení pro fiskální konektor ke konfiguraci z centrály Commerce. Formát souboru je v souladu s požadavky na konfiguraci fiskální integrace. Jsou přidána následující nastavení:

- **Adresa koncového bodu** – adresa URL služby daňové registrace.
- **Časový limit** – doba v milisekundách, po kterou bude čekat ovladač na odpověď od služby daňové registrace.

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
