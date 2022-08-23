---
ms.openlocfilehash: a20971ac9a44c409363bbce6cd8b8343f16d800f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274198"
---
# <a name="deployment-guidelines-for-the-control-unit-integration-sample-for-sweden-legacy"></a>Pokyny k nasazení ukázkové integrace kontrolní jednotky pro Švédsko (starší verze)
---

nadpis: Pokyny k nasazení ukázkové integrace kontrolní jednotky pro Švédsko (starší verze) [!include [banner](../includes/banner.md)]
popis: Tento článek obsahuje pokyny k nasazení ukázkové integrace kontrolní jednotky pro Švédsko ze sady Retail SDK

autor: EvgenyPopovMBS Tento článek obsahuje pokyny pro nasazení ukázkové integrace kontrolní jednotky pro Švédsko ze sady SDK (Software Development Kit) pro Retail na vývojářském virtuálním počítači (VM) v Microsoft Dynamics Lifecycle Services (LCS). Další informace o této ukázkové fiskální integraci naleznete v tématu [Ukázka integrace kontrolní jednotky pro Švédsko](emea-swe-fi-sample.md). ms.date: 20.12.2021

ms.topic: article Ukázka fiskální integrace pro Švédsko je součástí sady Retail SDK. Informace o instalaci a použití sady SDK naleznete v tématu [Architektura sady SDK (Software Development Kit) pro Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md). Tento příklad sestává z rozšíření pro Commerce Runtime (CRT), hardwarovou stanici a pokladní místo (POS). Ke spuštění tohoto příkladu musíte změnit a sestavit projekty CRT, hardwarové stanice a POS. Doporučujeme používat nemodifikovanou sadu Retail SDK k provedení změn, které jsou popsány v tomto článku. Rovněž doporučujeme používat systém správy zdrojového kódu, jako je Azure DevOps, kde žádné soubory nebyly dosud změněny.
publikum: Uživatel aplikace, vývojář, IT profesionál

ms.reviewer: v-chgriffin
## <a name="development-environment"></a>Vývojové prostředí
ms.search.region: Globální

ms.author: josaw Tento postup slouží k nastavení vývojového prostředí, abyste mohli testovat a rozšířit vzorek.
ms.search.validFrom: 1. 3. 2019

### <a name="enable-crt-extensions"></a>Povolení rozšíření CRT
---


Komponenty rozšíření CRT jsou součástí ukázek CRT. Pro dokončení následujících postupů otevřete řešení **CommerceRuntimeSamples.sln** v umístění **RetailSdk\\SampleExtensions\\CommerceRuntime**.
2. Povolte rozšíření aktuální ukázky hardwarové stanice přidáním následujícího řádku do sekce **composition** v konfiguračním souboru **HardwareStation.Extension.config**.


#### <a name="documentprovidercleancashsample-component"></a>Komponenta DocumentProvider.CleanCashSample
    ``` xml

    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
1. Vyhledejte projekt **Runtime.Extensions.DocumentProvider.CleanCashSample** a vytvořte jej.
    ```
2. In the **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll** assembly file.

3. Copy the assembly file to the CRT extensions folder:
3. Make the following changes in the **Customization.settings** package customization configuration file under the **BuildTools** folder:


    - **Commerce Scale Unit:** Copy the file to the **\\bin\\ext** folder under the Internet Information Services (IIS) Commerce Scale Unit site location.
    - Remove the following line to exclude the earlier Hardware station extension from deployable packages.
    - **Local CRT on Modern POS:** Copy the file to the **\\ext** folder under the local CRT client broker location.


        ``` xml
4. Find the extension configuration file for CRT:
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample.dll" />

        ```
    - **Commerce Scale Unit:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Commerce Scale Unit site location.

    - **Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.
    - Add the following lines to include the current sample Hardware station extension in deployable packages.


5. Register the CRT change in the extension configuration file.
        ``` xml

        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
    ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        ```
    ```


#### <a name="update-modern-pos"></a>Aktualizace Modern POS
#### <a name="extension-configuration-file"></a>Konfigurační soubor rozšíření


1. Otevřete řešení **CloudPOS.sln** ve složce **RetailSdk\\POS**.
1. Najděte konfigurační soubor rozšíření pro CRT:
2. Zákaz dřívějšího rozšíření POS:


    - **Commerce Scale Unit:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Commerce Scale Unit:.
    - V souboru **tsconfig.json** přidejte složku **FiscalRegisterSample** do seznamu výjimek.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.
    - Odeberte následující řádky ze souboru **extensions.json** ve složce **RetailSDK\\POS\\Extensions**.


2. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.
        ``` json

        {
    ``` xml
            "baseUrl": "FiscalRegisterSample"
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        }
    ```
        ```


### <a name="enable-hardware-station-extensions"></a>Povolení rozšíření hardwarové stanice
3. Povolte rozšíření aktuální ukázky POS přidáním následujících řádků do souboru **extensions.json** ve složce **RetailSDK\\POS\\Extensions**.


Komponenty rozšíření hardwarové stanice jsou součástí ukázek hardwarové stanice. Pro dokončení následujících postupů otevřete řešení **HardwareStationSamples.sln** v části **RetailSdk\\SampleExtensions\\HardwareStation**.
    ``` json

    {
#### <a name="cleancash-component"></a>Komponenta CleanCash
        "extensionPackages": [

            {
1. Vyhledejte projekt **HardwareStation.Extension.CleanCashSample** a vytvořte jej.
                "baseUrl": "Microsoft/AuditEvent.SE"
2. Ve složce **Extension.CleanCashSample\\bin\\Debug** vyhledejte soubory sestavení **Contoso.Commerce.HardwareStation.CleanCashSample.dll** a **Interop.CleanCash\_1\_1.dll**.
            }
3. Zkopírujte soubory sestavení do složky rozšíření hardwarové stanice:      ]

    }
    - **Sdílená hardwarové stanice:** Zkopírujte složku **bin** pod umístění webu hardwarové stanice IIS.
    ```
    - **Dedicated hardware station on Modern POS:** Copy the files to the Modern POS client broker location.


#### Update Cloud POS
4. Find the extension configuration file for the Hardware station's extensions. The file is named **HardwareStation.Extension.config**.


1. Open the **ModernPOS.sln** solution under **RetailSdk\\POS**.
    - **Shared hardware station:** The file is under the IIS Hardware station site location.
2. Disable the earlier POS extension:
    - **Dedicated hardware station on Modern POS:** The file is under the Modern POS client broker location.


    - In the **tsconfig.json** file, add the **FiscalRegisterSample** folder to the exclude list.
5. Add the following line to the **composition** section of the configuration file.
    - Remove the following lines from the **extensions.json** file under the **RetailSDK\\POS\\Extensions** folder.


    ``` xml
        ``` json
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        {
    ```
            "baseUrl": "FiscalRegisterSample"

        }
### <a name="enable-modern-pos-extension-components"></a>Povolení komponent rozšíření Modern POS
        ```


1. Otevřete řešení **ModernPOS.sln** v umístění **RetailSdk\\POS** a ujistěte se, že jej lze zkompilovat bez chyb. Kromě toho se ujistěte, že můžete spustit Modern POS z aplikace Visual Studio pomocí příkazu **Run**.
3. Povolte rozšíření aktuální ukázky POS přidáním následujících řádků do souboru **extensions.json** ve složce **RetailSDK\\POS\\Extensions**.


    > [!NOTE]
    ``` json
    > Modern POS must not be customized. You must enable User Account Control (UAC), and you must uninstall previously installed instances of Modern POS as required.
    {

        "extensionPackages": [
2. Enable the extensions that must be loaded by adding the following lines in the **extensions.json** file.
            {

                "baseUrl": "Microsoft/AuditEvent.SE"
    ``` json
            }
    {
        ]
        "extensionPackages": [
    }
            {
    ```
                "baseUrl": "Microsoft/AuditEvent.SE"

            }
#### <a name="create-deployable-packages"></a>Vytvoření nasaditelných balíčků
        ]

    }
Spuštěním příkazu **msbuild** pro celou sadu Retail SDK vytvořte nasaditelné balíčky. Balíčky použijte pomocí služby LCS nebo ručně. Další informace viz [Balíček sady Retail SDK](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
    ```

    > [!NOTE]
    > For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.

3. Znovu sestavte řešení.
4. Spusťte Modern POS v ladicím programu a otestujte funkčnost.

### <a name="enable-cloud-pos-extension-components"></a>Povolení komponent rozšíření Cloud POS

1. Otevřete řešení **CloudPOS.sln** v umístění **RetailSdk\\POS** a ujistěte se, že jej lze zkompilovat bez chyb.
2. Povolte rozšíření, která musí být načtena v souboru **extensions.json**, přidáním následujících řádků.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

    > [!NOTE]
    > Další informace a ukázky, které ukazují, jak zahrnout složky zdrojového kódu a povolit načítání rozšíření, naleznete v pokynech v souboru readme.md v projektu **Pos.Extensions**.

3. Znovu sestavte řešení.
4. Spusťte řešení příkazem **Run** a postupujte podle kroků v příručce Retail SDK.

## <a name="production-environment"></a>Produkční prostředí

Předchozí postup povolí rozšíření, která představují komponenty ukázkové integrace kontrolní jednotky. Kromě toho musíte provést následující postup k vytvoření balíčků pro nasazení, které obsahují komponenty Commerce a použití těchto balíčků v produkčním prostředí.

1. Proveďte následující změny v balíčku konfiguračních souborů ve složce **RetailSdk\\Assets**:

    - V konfiguračních souborech **commerceruntime.ext.config** a **CommerceRuntime.MPOSOffline.Ext.config** přidejte následující řádky do části **composition**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        ```

    - V konfiguračním souboru **HardwareStation.Extension.config** přidejte následující řádek do oddílu **composition**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        ```

2. Proveďte následující změny v konfiguračním souboru balíčku přizpůsobení **Customization.settings** ve složce **BuildTools**:

    - Přidejte následující řádek pro zahrnutí rozšíření CRT do nasaditelných balíčků.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
        ```

    - Přidejte následující řádky pro zahrnutí rozšíření hardwarové stanice do nasaditelných balíčků.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

3. Povolte rozšíření POS přidáním následujících řádků do souboru **extensions.json** ve složce **RetailSDK\\POS\\Extensions**.

    ``` json
    {
        "extensionPackages": [
            {
            "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

4. Spuste příkazový řádek MSBuild pro program Visual Studio a spusťte **msbuild** ve složce Retail SDK pro vytvoření balíčků k nasazení.
5. Balíčky použijte pomocí služby LCS nebo ručně. Další informace naleznete v tématu [Vytvoření balíčků pro nasazení](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
6. Proveďte všechny požadované úkoly nastavení, které jsou popsány v části [Nastavení integrace s kontrolními jednotkami](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).

## <a name="design-of-the-extensions"></a>Návrh rozšíření

### <a name="crt-extension-design"></a>Návrh rozšíření CRT

Účelem rozšíření je, aby poskytovatel fiskálního dokumentu generoval dokumenty specifické pro službu a zpracovával odpovědi z kontrolní jednotky.

Rozšíření CRT je **Runtime.Extensions.DocumentProvider.CleanCashSample**.

Podrobnější informace o návrhu řešení fiskální integrace získáte v části [Ukázky procesu fiskální registrace pro fiskální zařízení a služby](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Obslužná rutina požadavku

Pro poskytovatele dokumentů existuje jedna obslužná rutina požadavků **DocumentProviderCleanCash**. Tato obslužná rutina se používá ke generování fiskálních dokumentů pro kontrolní jednotku.

Tato rutina je zděděna z rozhraní **INamedRequestHandler**. Metoda **HandlerName** je odpovědná za vrácení názvu obslužné rutiny. Název obslužné rutiny by měl odpovídat názvu poskytovatele dokumentu zprostředkovatele zadanému v centrále Commerce.

Konektor podporuje následující požadavky:

- **GetFiscalDocumentDocumentProviderRequest** – tento požadavek obsahuje informace o dokladu, o němž by měl být vygenerován dokument. Vrátí dokument specifický pro službu, který má být registrován v kontrolní jednotce.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – tento požadavek vrací seznam událostí, k jejichž odběru se uživatelé přihlašují. V současné době jsou podporovány prodejní akce a akce auditu.

#### <a name="configuration"></a>Konfigurace

Konfigurační soubor **DocumentProviderFiscalCleanCashSample** se nachází ve složce **Konfigurace** procesu rozšíření. Tento soubor slouží k povolení nastavení pro zprostředkovatele dokumentu ke konfiguraci z centrály Commerce. Formát souboru je v souladu s požadavky na konfiguraci fiskální integrace. Jsou přidána následující nastavení:

- Mapování kódů DPH

### <a name="hardware-station-extension-design"></a>Design rozšíření hardwarové stanice

Účelem rozšíření je fiskální konektor určený ke komunikaci s kontrolní jednotkou.

Rozšíření hardwarové stanice je **HardwareStation.Extension.CleanCashSample**. Používá protokol HTTP k odesílání dokumentů, které rozšíření  CRT generuje pro kontrolní jednotku. Také zpracovává odpovědi, které jsou přijaty z kontrolní jednotky.

#### <a name="request-handler"></a>Obslužná rutina požadavku

Obslužná rutina požadavku **CleanCashHandler** je vstupní bod pro práci s požadavky do kontrolní jednotky.

Tato rutina je zděděna z rozhraní **INamedRequestHandler**. Metoda **HandlerName** je odpovědná za vrácení názvu obslužné rutiny. Název obslužné rutiny by měl odpovídat názvu poskytovatele dokumentu fiskálního konektoru zadanému v centrále Commerce.

Konektor podporuje následující požadavky:

- **SubmitDocumentFiscalDeviceRequest** – tento požadavek odesílá dokumenty do kontrolní jednotky a vrátí z ní odpověď.
- **IsReadyFiscalDeviceRequest** – tento požadavek se používá pro kontrolu stavu kontrolní jednotky.
- **InitializeFiscalDeviceRequest** – tento požadavek se používá pro inicializaci kontrolní jednotky.

#### <a name="configuration"></a>Konfigurace

Konfigurační soubor se nachází ve složce **Konfigurace** projektu rozšíření. Tento soubor slouží k povolení nastavení pro fiskální konektor ke konfiguraci z centrály Commerce. Formát souboru je v souladu s požadavky na konfiguraci fiskální integrace. Jsou přidána následující nastavení:

- **Řetězec připojení** – Nastavení připojení kontrolní jednotky.
- **Časový limit** – doba v milisekundách, po kterou bude čekat ovladač na odpověď z kontrolní jednotky.

## <a name="migrating-from-the-earlier-integration-sample"></a>Migrace z dřívější ukázkové integrace

Pokud používáte dřívější [ukázkovou integraci POS s kontrolními jednotkami pro Švédsko](retail-sdk-control-unit-sample.md), možná z něj budete muset migrovat do aktuální ukázkové integrace. Chcete-li zavést změnu a v budoucnu dostávat včasné aktualizace funkcí pro Švédsko, možná budete muset upgradovat, provést drobné úpravy kódu a konfigurace v rozšířeních, která jste vytvořili, a znovu sestavit svá řešení. V logice rozšíření, kterou jste vytvořili, nejsou vyžadovány žádné velké změny. Dřívější ukázková integrace a vaše přizpůsobení budou nadále fungovat, pokud z vaší strany nebudou provedeny žádné změny. Proto můžete plánovat, připravovat se a zavádět změny svého prostředí.

### <a name="migration-process"></a>Proces migrace

Migrace z dřívější ukázkové integrace do aktuální ukázkové integrace kontrolní jednotky by měla být založena na konceptu postupné aktualizace. Jinými slovy, všechny komponenty ústředí Commerce a Commerce Scale Unit by měly být aktualizovány ještě předtím, než začnete aktualizovat komponenty POS a hardwarové stanice.

Abyste předešli situaci, kdy je událost nebo transakce podepsána dvakrát (to znamená, že je podepsána dřívějším i aktuálním rozšířením), nebo kdy událost nebo transakci nelze podepsat kvůli chybějící konfiguraci, doporučujeme vypnout všechna zařízení POS a hardwarové stanice, která používají předchozí ukázku, a poté je aktualizovat současně. Tuto simultánní aktualizaci lze provést například obchod po obchodu aktualizací funkčního profilu obchodu a hardwarového profilu hardwarové stanice.

Proces migrace by měl sestávat z následujících kroků.

1. Aktualizace komponent ústředí Commerce.
1. Aktualizace komponent Commerce Scale Unit a povolení rozšíření aktuální ukázky.
1. Ujištění, že všechny offline transakce jsou synchronizovány ze zařízení MPOS s podporou režimu offline.
1. Vypnutí všech zařízení, která používají komponenty předchozí ukázky.
1. Proveďte všechny požadované úkoly nastavení, které jsou popsány v části [Nastavení integrace s kontrolními jednotkami](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).
1. Aktualizace komponent POS a hardwarové stanice, zákaz rozšíření, která jsou součástí předchozí ukázky, a povolení rozšíření aktuální ukázky.

    > [!NOTE]
    > V závislosti na typu prostředí můžete najít další technické podrobnosti o procesu migrace v sekci [Migrace ve vývojovém prostředí](#migration-in-a-development-environment) nebo [Migrace v provozním prostředí](#migration-in-a-production-environment) v tomto článku.

### <a name="migration-in-a-development-environment"></a>Migrace ve vývojovém prostředí

#### <a name="update-crt"></a>Aktualizovat CRT

1. Vyhledejte projekt **Runtime.Extensions.DocumentProvider.CleanCashSample** a vytvořte jej.
2. Ve složce **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Commerce Scale Unit::** Zkopírujte soubor do složky **\\bin\\ext** v umístění webu ISS Commerce Scale Unit.
    - **Místní CRT v Modern POS:** Zkopírujte soubor do složky **\\ext** v umístění místního makléře klienta CRT.

4. Najděte konfigurační soubor rozšíření pro CRT:

    - **Commerce Scale Unit:** Soubor je nazván **CommerceRuntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Commerce Scale Unit:.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se ve složce **bin\\ext** v místním umístění zprostředkovatele klienta CRT.

    > [!WARNING]
    > **Neupravujte** soubory CommerceRuntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

5. Vyhledejte a odeberte dřívější rozšíření CRT z konfiguračního souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Neprovádějte tento krok, dokud neaktualizujete všechna zařízení POS, která pracují s touto instancí CRT.

6. Zaregistrujte rozšíření aktuální ukázky CRT v konfiguračním souboru rozšíření přidáním následujících řádků.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

#### <a name="update-hardware-station"></a>Aktualizace hardwarové stanice

1. Vyhledejte projekt **HardwareStation.Extension.CleanCashSample** a vytvořte jej.
2. Ve složce **Extension.CleanCashSample\\bin\\Debug** vyhledejte soubory sestavení **Contoso.Commerce.HardwareStation.CleanCashSample.dll** a **Interop.CleanCash\_1\_1.dll**.
3. Zkopírujte soubory sestavení do složky rozšíření hardwarové stanice:

    - **Sdílená hardwarové stanice:** Zkopírujte složku **bin** pod umístění webu hardwarové stanice IIS.
    - **Vyhrazená hardwarová stanice pro Modern POS:** Zkopírujte soubory do stanice zprostředkovatele klienta Modern POS.

4. Vyhledejte konfigurační soubor rozšíření **HardwareStation.Extension.config**:

    - **Vzdálená hardwarové stanice:** Soubor se nachází v umístění webu hardwarové stanice IIS.
    - **Místní hardwarová stanice pro Modern POS:** Soubor se nachází v umístění zprostředkovatele klienta Modern POS.

    > [!WARNING]
    > **Neupravujte** soubory CommerceRuntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

5. Vyhledejte a odeberte dřívější rozšíření hardwarové stanice z konfiguračního souboru rozšíření.

    # <a name="retail-73-and-earlier"></a>[Retail 7.3 a starší](#tab/retail-7-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 a novější](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Retail 10.0 a novější](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

6. Přidejte následující řádek do oddílu **composition** konfiguračního souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

#### <a name="update-modern-pos"></a>Aktualizace Modern POS

1. Otevřete řešení **CloudPOS.sln** pod **RetailSdk\\POS**.
2. Deaktivujte dřívější rozšíření POS odstraněním následujících řádků ze souboru **extensions.json**.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Povolte rozšíření aktuální ukázky POS přidáním následujících řádků do souboru **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Aktualizace Cloud POS

1. Otevřete řešení **ModernPOS.sln** pod **RetailSdk\\POS**.
2. Deaktivujte dřívější rozšíření POS odstraněním následujících řádků ze souboru **extensions.json**.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Povolte rozšíření aktuální ukázky POS přidáním následujících řádků do souboru **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

### <a name="migration-in-a-production-environment"></a>Migrace v provozním prostředí

#### <a name="update-crt"></a>Aktualizovat CRT

1. Odstraňte dřívější rozšíření CRT z konfiguračních souborů **CommerceRuntime.ext.config** a **CommerceRuntime.MPOSOffline.Ext.config** ve složce **RetailSdk\\Assets**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Neprovádějte tento krok, dokud neaktualizujete všechna zařízení POS, která pracují s touto instancí CRT.

2. Povolte rozšíření aktuální ukázky CRT provedením následujících změn v konfiguračních souborech **CommerceRuntime.ext.config** a **CommerceRuntime.MPOSOffline.Ext.config** ve složce **RetailSdk\\Assets**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

3. V konfiguračním souboru přizpůsobení balíčku **Customization.settings** ve složce **BuildTools** přidejte následující řádek pro zahrnutí rozšíření aktuální ukázky CRT v nasaditelných balíčcích.

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
    ```

#### <a name="update-hardware-station"></a>Aktualizace hardwarové stanice

1. Odeberte dřívější rozšíření hardwarové stanice změnou konfiguračního souboru **HardwareStation.Extension.config**.

    # <a name="retail-73-and-earlier"></a>[Retail 7.3 a starší](#tab/retail-7-3)

    Odeberte následující sekci z konfiguračních souborů **HardwareStation.Shared.config** a **HardwareStation.Dedicated.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 a novější](#tab/retail-7-3-1)

    Z konfiguračního souboru **HardwareStation.Extension.config** odeberte následující sekci.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Retail 10.0 a novější](#tab/retail-10-0)

    Z konfiguračního souboru **HardwareStation.Extension.config** odeberte následující sekci.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---
