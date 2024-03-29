---
title: Pokyny k nasazení registračních pokladen pro Norsko (staré)
description: Tento článek je průvodce nasazením, který popisuje, jak povolit lokalizaci Microsoft Dynamics 365 Commerce pro Norsko.
author: EvgenyPopovMBS
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-2-28
ms.openlocfilehash: fb597add48ac3508a88142e63d80f405b6b5f8b4
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346038"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway-legacy"></a>Pokyny k nasazení registračních pokladen pro Norsko (staré)

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Tato ukázka funkce fiskální integrace nevyužívá výhody [rámce fiskální integrace](./fiscal-integration-for-retail-channel.md) a v pozdějších aktualizacích bude zastaralá. Místo toho byste měli použít [funkci, která je založena na rámci fiskální integrace](./emea-nor-fi-deployment.md).

Tento článek je průvodce nasazením, který popisuje, jak povolit lokalizaci Microsoft Dynamics 365 Commerce pro Norsko. Lokalizace se skládá z několika rozšíření komponent Commerce. Rozšíření vám například umožňují tisknout vlastní pole na příjemkách, registrovat dodatečné události auditu, prodejní transakce a platební transakce v pokladním místě (POS), digitálně podepisovat prodejní transakce a tisknout sestavy X a Z v místních formátech. Další informace o lokalizaci pro Norsko viz [Funkce registrační pokladny pro Norsko](./emea-nor-cash-registers.md).

Tato ukázka je součástí sady SDK (Software Development Kit) pro Retail. Informace o SDK naleznete v tématu [Architektura sady SDK (Software Development Kit) pro Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Tento příklad sestává z rozšíření pro Commerce Runtime (CRT), Retail, Server a POS. Ke spuštění tohoto příkladu musíte změnit a sestavit projekty CRT, Retail, Server a POS. Doporučujeme používat nemodifikovanou sadu Retail SDK k provedení změn, které jsou popsány v tomto článku. Rovněž doporučujeme používat zdrojový systému kontroly, jako je například Microsoft Visual Studio Online (VSO), kde žádné soubory nebyly dosud změněny.

> [!NOTE]
> V Commerce 10.0.8 a vyšší je Retail Server známý jako Commerce Scale Unit. Protože se tento článek týká i několika předchozích verzí aplikace, používáme v něm *Retail Server*.
>
> Některé procesní kroky v tomto článku se liší v závislosti na verzi Commerce, kterou používáte. Další informace viz [Co je nového a co se změnilo v produktu Dynamics 365 Retail](../get-started/whats-new.md).

### <a name="using-certificate-profiles-in-commerce-channels"></a>Použití profilů certifikátů v kanálech Commerce

Ve verzích Commerce 10.0.15 a novějších můžete použít funkci [Profily certifikátů definovaných uživatelem pro maloobchodní prodejny](./certificate-profiles-for-retail-stores.md), která podporuje převzetí služeb při selhání do režimu offline, když není k dispozici ústředí Key Vault nebo Commerce. Tato funkce rozšiřuje funkci [Správa tajných kódů pro kanály Retail](../dev-itpro/manage-secrets.md).

Chcete-li používat tuto funkci v rozšíření CRT, postupujte takto.

1. Vytvořte nový projekt rozšíření CRT (typ projektu knihovny třídy C#). Použijte vzorové šablony ze sady SDK (Software Development Kit) pro Retail (RetailSDK\SampleExtensions\CommerceRuntime).

2. Přidejte vlastní obslužnou rutinu pro CertificateSignatureServiceRequest v projektu SequentialSignatureRegister.

3. Chcete-li přečíst tajné volání, použijte `GetUserDefinedSecretCertificateServiceRequest` s pomocí konstruktoru s parametrem profileId. Tím se spustí funkce pracující s nastaveními z profilů certifikátů. Na základě nastavení se certifikát načte buď z Azure Key Vault nebo z místního úložiště počítače.

    ```csharp
    GetUserDefinedSecretCertificateServiceRequest getUserDefinedSecretCertificateServiceRequest = new GetUserDefinedSecretCertificateServiceRequest(profileId: "ProfileId", secretName: null, thumbprint: null, expirationInterval: null);
    GetUserDefinedSecretCertificateServiceResponse getUserDefinedSecretCertificateServiceResponse = request.RequestContext.Execute<GetUserDefinedSecretCertificateServiceResponse>(getUserDefinedSecretCertificateServiceRequest);

    X509Certificate2 Certificate = getUserDefinedSecretCertificateServiceResponse.Certificate;
    ```

4. Po načtení certifikátu pokračujte podepisováním dat.

5. Sestavte projekt rozšíření CRT.

6. Zkopírujte výstupní knihovnu třídy a vložte ji do ...\RetailServer\webroot\bin\Ext pro ruční testování.

7. V souboru CommerceRuntime.Ext.config přidejte informace o vlastní knihovně do sekce složení rozšíření.

## <a name="development-environment"></a>Vývojové prostředí

Pomocí těchto postupů nastavíte vývojové prostředí, abyste mohli testovat a rozšířit vzorek.

### <a name="the-crt-extension-components"></a>Komponenty rozšíření CRT

Komponenty rozšíření CRT jsou součástí ukázek CRT. Pro dokončení následujících postupů otevřete řešení CRT, **CommerceRuntimeSamples.sln**, v části **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="receiptsnorway-component"></a>Komponenta ReceiptsNorway

1. Vyhledejte projekt **Runtime.Extensions.ReceiptsNorway** a vytvořte jej.
2. Ve složce **Runtime.Extensions.ReceiptsNorway\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.ReceiptsNorway.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru Microsoft Internet Information Services (IIS) Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

4. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

5. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
    ```

    > [!WARNING]
    > **Neupravujte** soubory commerceruntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

#### <a name="salespaymenttransext-component"></a>Komponenta SalesPaymentTransExt

1. Vyhledejte projekt **Runtime.Extensions.SalesPaymentTransExt** a vytvořte jej.
2. Ve složce **Extensions.SalesPaymentTransExt\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.SalesPaymentTransExt.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

4. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

5. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

    > [!WARNING]
    > **Neupravujte** soubory commerceruntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

#### <a name="xzreportsnorway-component"></a>Komponenta XZReportsNorway

1. Vyhledejte projekt **Runtime.Extensions.XZReportsNorway** a vytvořte jej.
2. Ve složce **Extensions.XZReportsNorway\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.XZReportsNorway.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

4. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

5. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
    ```

    > [!WARNING]
    > **Neupravujte** soubory commerceruntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

# <a name="application-update-4"></a>[Aktualizace aplikace 4](#tab/app-update-4)

#### <a name="registerauditevent-sample-component"></a>Ukázková komponenta RegisterAuditEvent

1. Vyhledejte projekt **Runtime.Extensions.RegisterAuditEventSample** a vytvořte jej.
2. Ve složce **Extensions.RegisterAuditEventSample\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

4. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

5. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **Neupravujte** soubory commerceruntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

#### <a name="salestransactionsignature-sample-component"></a>Ukázková komponenta SalesTransactionSignature

1. Vyhledejte projekt **Runtime.Extensions.SalesTransactionSignatureSample**.
2. Upravte soubor **App.config** zadáním kryptografického otisku, umístění úložiště a názvu úložiště pro certifikát, který chcete použít k podepisování prodejních transakcí.
3. Sestavte projekt.
4. Ve složce **Extension.SalesTransactionSignatureSample\\bin\\Debug** vyhledejte následující soubory:

    - Soubor sestavení **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - Soubor konfigurace **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. Zkopírujte soubory do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

6. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

7. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > **Neupravujte** soubory commerceruntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

# <a name="application-update-5-and-later"></a>[Aktualizace aplikace 5 a novější](#tab/app-update-5-and-later)

#### <a name="registerauditevent-sample-component"></a>Ukázková komponenta RegisterAuditEvent

1. Vyhledejte projekt **Runtime.Extensions.RegisterAuditEventSample** a vytvořte jej.
2. Ve složce **Extensions.RegisterAuditEventSample\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

4. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

5. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **Neupravujte** soubory commerceruntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

#### <a name="salestransactionsignature-sample-component"></a>Ukázková komponenta SalesTransactionSignature

1. Vyhledejte projekt **Runtime.Extensions.SalesTransactionSignatureSample**.
2. Upravte soubor **App.config** zadáním kryptografického otisku, umístění úložiště a názvu úložiště pro certifikát, který chcete použít k podepisování prodejních transakcí.
3. Sestavte projekt.
4. Ve složce **Extension.SalesTransactionSignatureSample\\bin\\Debug** vyhledejte následující soubory:

    - Soubor sestavení **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - Soubor konfigurace **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. Zkopírujte soubory do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

6. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

7. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > **Neupravujte** soubory commerceruntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

#### <a name="salestransactionsignaturesamplemessages-component"></a>Ukázková komponenta SalesTransactionSignatureSample.Messages

1. Vyhledejte projekt **Runtime.Extensions.SalesTransactionSignatureSample.Messages**.
2. Ve složce **Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

4. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

5. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
    ```

    > [!WARNING]
    > **Neupravujte** soubory commerceruntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

# <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

#### <a name="registerauditevent-sample-component"></a>Ukázková komponenta RegisterAuditEvent

1. Vyhledejte projekt **Runtime.Extensions.RegisterAuditEventSample** a vytvořte jej.
2. Ve složce **Extensions.RegisterAuditEventSample\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

4. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

5. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **Neupravujte** soubory commerceruntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

#### <a name="salestransactionsignature-sample-component"></a>Ukázková komponenta SalesTransactionSignature

1. Vyhledejte projekt **Runtime.Extensions.SalesTransactionSignatureSample**.
2. Upravte soubor **App.config** zadáním kryptografického otisku, umístění úložiště a názvu úložiště pro certifikát, který chcete použít k podepisování prodejních transakcí.
3. Sestavte projekt.
4. Ve složce **Extension.SalesTransactionSignatureSample\\bin\\Debug** vyhledejte následující soubory:

    - Soubor sestavení **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - Soubor konfigurace **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. Zkopírujte soubory do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

6. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

7. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > **Neupravujte** soubory commerceruntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

#### <a name="sequentialsignatureregistercontracts-component"></a>Komponenta SequentialSignatureRegister.Contracts

1. Vyhledejte projekt **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. Ve složce **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

# <a name="retail-732-and-later"></a>[Retail 7.3.2 a novější](#tab/retail-7-3-2)

#### <a name="registerauditevent-sample-component"></a>Ukázková komponenta RegisterAuditEvent

1. Vyhledejte projekt **Runtime.Extensions.RegisterAuditEventSample** a vytvořte jej.
2. Ve složce **Extensions.RegisterAuditEventSample\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

4. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

5. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **Neupravujte** soubory commerceruntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

#### <a name="sequentialsignatureregister-component"></a>Komponenta SequentialSignatureRegister

1. Vyhledejte projekt **Runtime.Extensions.SequentialSignatureRegister**.
2. Upravte soubor **App.config** zadáním kryptografického otisku, umístění úložiště a názvu úložiště pro certifikát, který chcete použít k podepisování prodejních transakcí.
3. Sestavte projekt.
4. Ve složce **Extension.SequentialSignatureRegister\\bin\\Debug** vyhledejte následující soubory:

    - Soubor sestavení **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - Soubor konfigurace **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. Zkopírujte soubory do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

6. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

7. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > **Neupravujte** soubory commerceruntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

#### <a name="salestransactionsignaturenorway-component"></a>Komponenta SalesTransactionSignatureNorway

1. Vyhledejte projekt **Runtime.Extensions.SalesTransactionSignatureNorway**.
2. Ve složce **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

4. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

5. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > **Neupravujte** soubory commerceruntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

#### <a name="sequentialsignatureregistercontracts-component"></a>Komponenta SequentialSignatureRegister.Contracts

1. Vyhledejte projekt **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. Ve složce **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

#### <a name="salespaymenttransextnorway-component"></a>Komponenta SalesPaymentTransExtNorway

1. Najděte projekt **Runtime.Extensions.SalesPaymentTransExtNorway** a vytvořte ho.
2. Ve složce **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

4. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

5. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > **Neupravujte** soubory commerceruntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

# <a name="retail-735-and-later"></a>[Retail 7.3.5 a novější](#tab/retail-7-3-5)

#### <a name="registerauditeventnorway-component"></a>Komponenta RegisterAuditEventNorway

1. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

2. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > **Neupravujte** soubory commerceruntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

#### <a name="sequentialsignatureregister-component"></a>Komponenta SequentialSignatureRegister

1. Vyhledejte projekt **Runtime.Extensions.SequentialSignatureRegister**.
2. Upravte soubor **App.config** zadáním kryptografického otisku, umístění úložiště a názvu úložiště pro certifikát, který chcete použít k podepisování prodejních transakcí.
3. Sestavte projekt.
4. Ve složce **Extension.SequentialSignatureRegister\\bin\\Debug** vyhledejte následující soubory:

    - Soubor sestavení **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - Soubor konfigurace **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. Zkopírujte soubory do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

6. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

7. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > **Neupravujte** soubory commerceruntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

#### <a name="salestransactionsignaturenorway-component"></a>Komponenta SalesTransactionSignatureNorway

1. Vyhledejte projekt **Runtime.Extensions.SalesTransactionSignatureNorway**.
2. Ve složce **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

4. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

5. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > **Neupravujte** soubory commerceruntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

#### <a name="sequentialsignatureregistercontracts-component"></a>Komponenta SequentialSignatureRegister.Contracts

1. Vyhledejte projekt **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. Ve složce **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

#### <a name="salespaymenttransextnorway-component"></a>Komponenta SalesPaymentTransExtNorway

1. Najděte projekt **Runtime.Extensions.SalesPaymentTransExtNorway** a vytvořte ho.
2. Ve složce **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

4. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

5. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > **Neupravujte** soubory commerceruntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

# <a name="retail-811-and-later"></a>[Retail 8.1.1 a novější](#tab/retail-8-1-1)

#### <a name="registerauditeventnorway-component"></a>Komponenta RegisterAuditEventNorway

1. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

2. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > **Neupravujte** soubory commerceruntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

#### <a name="sequentialsignatureregister-component"></a>Komponenta SequentialSignatureRegister

1. Vyhledejte projekt **Runtime.Extensions.SequentialSignatureRegister**.
2. Upravte soubor **App.config** zadáním kryptografického otisku, umístění úložiště a názvu úložiště pro certifikát, který chcete použít k podepisování prodejních transakcí.
3. Sestavte projekt.
4. Ve složce **Extension.SequentialSignatureRegister\\bin\\Debug** vyhledejte následující soubory:

    - Soubor sestavení **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - Soubor konfigurace **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. Zkopírujte soubory do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

6. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

7. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > **Neupravujte** soubory commerceruntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

#### <a name="salestransactionsignaturenorway-component"></a>Komponenta SalesTransactionSignatureNorway

1. Vyhledejte projekt **Runtime.Extensions.SalesTransactionSignatureNorway**.
2. Ve složce **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

4. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

5. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > **Neupravujte** soubory commerceruntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

#### <a name="sequentialsignatureregistercontracts-component"></a>Komponenta SequentialSignatureRegister.Contracts

1. Vyhledejte projekt **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. Ve složce **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

#### <a name="salespaymenttransextnorway-component"></a>Komponenta SalesPaymentTransExtNorway

1. Najděte projekt **Runtime.Extensions.SalesPaymentTransExtNorway** a vytvořte ho.
2. Ve složce **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření CRT:

    - **Maloobchodní server:** Zkopírujte sestavení do složky **\\bin\\ext** v umístění serveru IIS Retail Server.
    - **Místní CRT v Modern POS:** Zkopírujte sestavení do složky **\\ext** v umístění místního makléře klienta CRT.

4. Najděte konfigurační soubor rozšíření pro CRT:

    - **Server maloobchodu:** Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin\\ext.** pod umístěním webu IIS Retail Server.
    - **Místní CRT v Modern POS:** Soubor je nazván **CommerceRuntime.MPOSOffline.Ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

5. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > **Neupravujte** soubory commerceruntime.config a CommerceRuntime.MPOSOffline.config. Tyto soubory nejsou určeny k žádným přizpůsobením.

---

### <a name="the-retail-server-extension-components"></a>Komponenty rozšíření Retail Server

#### <a name="salestransactionsignature-retail-server-sample-component"></a>Ukázková komponenta SalesTransactionSignature Retail Server

1. Ve složce **RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** vyhledejte projekt **RetailServer.Extensions.SalesTransactionSignatureSample** a sestavte jej.
2. Ve složce **RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** vyhledejte soubor sestavení **Contoso.RetailServer.SalesTransactionSignatureSample.dll**.
3. Zkopírujte soubor sestavení do složky rozšíření Retail Server.

    # <a name="application-update-4"></a>[Aktualizace aplikace 4](#tab/app-update-4)

    Jde o složku **\\bin** v umístění webu IIS Retail Server.

    # <a name="application-update-5-and-later"></a>[Aktualizace aplikace 5 a novější](#tab/app-update-5-and-later)

    Jde o složku **\\bin** v umístění webu IIS Retail Server.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    Jde o složku **\\bin\\ext** v umístění webu IIS Retail Server.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 a novější](#tab/retail-7-3-2)

    Jde o složku **\\bin\\ext** v umístění webu IIS Retail Server.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 a novější](#tab/retail-7-3-5)

    Jde o složku **\\bin\\ext** v umístění webu IIS Retail Server.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 a novější](#tab/retail-8-1-1)

    Jde o složku **\\bin\\ext** v umístění webu IIS Retail Server.

    ---

4. Najděte konfigurační soubor pro Retail Server. Soubor je nazván **web.config** a je uložen v kořenové složce v umístění webu IIS Retail Server.
5. Zaregistrujte rozšíření Retail Server v sekci **extensionComposition** konfiguračního souboru.

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. Zaregistrujte závislosti rozšíření Retail Server.

    # <a name="application-update-4"></a>[Aktualizace aplikace 4](#tab/app-update-4/)

    1. Ve složce **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** vyhledejte následující soubory:

        - Soubor sestavení **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
        - Soubor konfigurace **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

    2. Zkopírujte soubory do složky **\\bin** v umístění webu IIS Retail Server.
    3. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření pro CRT. Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin** v umístění webu IIS Retail Server.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        ```

    # <a name="application-update-5-and-later"></a>[Aktualizace aplikace 5 a novější](#tab/app-update-5-and-later/)

    1. Ve složce **CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll**.
    2. Zkopírujte soubor do složky **\\bin** v umístění webu IIS Retail Server.
    3. Zaregistrujte změnu CRT v konfiguračním souboru rozšíření pro CRT. Soubor je nazván **commerceruntime.ext.config** a je uložen ve složce **bin** v umístění webu IIS Retail Server.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Nejsou vyžadovány žádné akce.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 a novější](#tab/retail-7-3-2)

    > [!NOTE]
    > Nejsou vyžadovány žádné akce.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 a novější](#tab/retail-7-3-5)

    > [!NOTE]
    > Nejsou vyžadovány žádné akce.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 a novější](#tab/retail-8-1-1)

    > [!NOTE]
    > Nejsou vyžadovány žádné akce.

    ---

### <a name="the-modern-pos-extension-components"></a>Komponenty rozšíření Modern POS

#### <a name="implement-the-proxy-code-for-offline-mode"></a>Implementace kódu proxy pro režim offline

Tato část je ekvivalentní kontroleru Retail Server, ale rozšiřuje místní CRT, které se používá, když klient není připojen.

1. V souboru **customization.settings** změňte sekci **@(RetailServerLibraryPathForProxyGeneration)** tak, aby používala nové sestavení Retail Server pro generování proxy.
2. Implementujte následující metody rozhraní ve třídě **StoreOperationsManager**. Pro první iteraci přidejte následující kód:

    # <a name="application-update-4"></a>[Aktualizace aplikace 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="application-update-5-and-later"></a>[Aktualizace aplikace 5 a novější](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Tento krok se nevztahuje na tuto verzi.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 a novější](#tab/retail-7-3-2)

    > [!NOTE]
    > Tento krok se nevztahuje na tuto verzi.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 a novější](#tab/retail-7-3-5)

    > [!NOTE]
    > Tento krok se nevztahuje na tuto verzi.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 a novější](#tab/retail-8-1-1)

    > [!NOTE]
    > Tento krok se nevztahuje na tuto verzi.

    ---

3. Chcete-li znovu vygenerovat kód proxy, sestavte složku **Proxies** z příkazového řádku příkazem **msbuild /t:Rebuild**.
4. Přeložte závislosti projektu **Proxy.RetailProxy**:

    # <a name="application-update-4"></a>[Aktualizace aplikace 4](#tab/app-update-4)

    Otevřete **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, do řešení přidejte projekt **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\CommerceRuntime.Extensions.SalesTransactionSignatureSample** a do projektu **RetailProxy** přidejte odkaz na **SalesTransactionSignatureSample**.

    # <a name="application-update-5-and-later"></a>[Aktualizace aplikace 5 a novější](#tab/app-update-5-and-later)

    Otevřete **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, do řešení přidejte projekt **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\CommerceRuntime.Extensions.SalesTransactionSignatureSample.Messages** a do projektu **RetailProxy** přidejte odkaz na **SalesTransactionSignatureSample.Messages**.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Tento krok se nevztahuje na tuto verzi.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 a novější](#tab/retail-7-3-2)

    > [!NOTE]
    > Tento krok se nevztahuje na tuto verzi.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 a novější](#tab/retail-7-3-5)

    > [!NOTE]
    > Tento krok se nevztahuje na tuto verzi.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 a novější](#tab/retail-8-1-1)

    > [!NOTE]
    > Tento krok se nevztahuje na tuto verzi.

    ---

5. Upravte metody rozhraní ve třídě **StoreOperationsManager**:

    # <a name="application-update-4"></a>[Aktualizace aplikace 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="application-update-5-and-later"></a>[Aktualizace aplikace 5 a novější](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Tento krok se nevztahuje na tuto verzi.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 a novější](#tab/retail-7-3-2)

    > [!NOTE]
    > Tento krok se nevztahuje na tuto verzi.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 a novější](#tab/retail-7-3-5)

    > [!NOTE]
    > Tento krok se nevztahuje na tuto verzi.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 a novější](#tab/retail-8-1-1)

    > [!NOTE]
    > Tento krok se nevztahuje na tuto verzi.

    ---

6. Aktualizujte soubor **dllhost.exe.config** tak, aby zprostředkovatel klienta načetl nové sestavení RetailProxy.

    ``` xml
    <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
    <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />
    ```

#### <a name="retail-proxy-extension-component-retail-731-and-later"></a>Komponenta rozšíření proxy Retail (Retail 7.3.1 a novější)

Následující postup proveďte pouze v případě, že používáte Retail 7.3.1 a novější.

1. Ve složce **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample** vyhledejte projekt **RetailServer.Extensions.SalesTransactionSignatureSample** a sestavte jej.
2. Ve složce **RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** vyhledejte soubor sestavení **Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample**.
3. Zkopírujte soubory sestavení do složky **\\ext** v umístění místního zprostředkovatele klienta CRT.
4. Zaregistrujte změnu proxy Retail v konfiguračním souboru rozšíření. Soubor je nazván **RetailProxy.MPOSOffline.ext.config** a nachází se v místní složce zprostředkovatele klienta CRT.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

#### <a name="modern-pos-extension-components"></a>Komponenty rozšíření Modern POS

1. Otevřete řešení v umístění **RetailSdk\\POS\\ModernPOS.sln** a ujistěte se, že jej lze zkompilovat bez chyb. Kromě toho se ujistěte, že můžete spustit Modern POS z aplikace Microsoft Visual Studio pomocí příkazu **Run**.

    > [!NOTE]
    > Modern POS se nesmí přizpůsobovat. Musíte povolit nástroj Řízení uživatelských účtů (UAC) a podle potřeby odinstalovat dříve nainstalované instance Modern POS.

2. Zahrňte následující existující složky zdrojového kódu do projektu **Pos.Extensions**.

    # <a name="application-update-4"></a>[Aktualizace aplikace 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Aktualizace aplikace 5 a novější](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 a novější](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 a novější](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 a novější](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. Povolte rozšíření, která mají být kompilována v **tsconfig.json**, odebráním následujících složek ze seznamu výjimek.

    # <a name="application-update-4"></a>[Aktualizace aplikace 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Aktualizace aplikace 5 a novější](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 a novější](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 a novější](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 a novější](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. Povolte rozšíření, která mají být načtena v **extensions.json**, přidáním následujících řádků do příslušných míst.

    # <a name="application-update-4"></a>[Aktualizace aplikace 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[Aktualizace aplikace 5 a novější](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 a novější](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 a novější](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 a novější](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Další informace a ukázky, které ukazují, jak zahrnout složky zdrojového kódu a povolit načítání rozšíření, naleznete v pokynech v souboru readme.md v projektu **Pos.Extensions**.

5. Znovu sestavte řešení.
6. Spusťte Modern POS v ladicím programu a otestujte funkčnost.

### <a name="cloud-pos-extension-components"></a>Komponenty rozšíření Cloud POS

1. Otevřete řešení v umístění **RetailSdk\\POS\\CloudPOS.sln** a ujistěte se, že jej lze zkompilovat bez chyb.
2. Zahrňte následující existující složky zdrojového kódu do projektu **Pos.Extensions**.

    # <a name="application-update-4"></a>[Aktualizace aplikace 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Aktualizace aplikace 5 a novější](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 a novější](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 a novější](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 a novější](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. Povolte rozšíření, která mají být kompilována v **tsconfig.json**, odebráním následujících složek ze seznamu výjimek.

    # <a name="application-update-4"></a>[Aktualizace aplikace 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Aktualizace aplikace 5 a novější](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 a novější](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 a novější](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 a novější](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. Povolte rozšíření, která mají být načtena v **extensions.json**, přidáním následujících řádků do příslušných míst.

    # <a name="application-update-4"></a>[Aktualizace aplikace 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[Aktualizace aplikace 5 a novější](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 a novější](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 a novější](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 a novější](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Další informace a ukázky, které ukazují, jak zahrnout složky zdrojového kódu a povolit načítání rozšíření, naleznete v pokynech v souboru readme.md v projektu **Pos.Extensions**.

5. Znovu sestavte řešení.
6. Spusťte řešení příkazem **Run** a postupujte podle kroků v příručce Retail SDK.
7. Otestujte funkčnost.

### <a name="set-up-required-parameters-in-headquarters"></a>Nastavení požadovaných parametrů v centrále

Další informace naleznete v tématu [Funkce registrační pokladny pro Norsko](./emea-nor-cash-registers.md).

## <a name="production-environment"></a>Produkční prostředí

Následujícím postupem vytvoříte balíčky pro nasazení, které obsahují komponenty Commerce, a použijete tyto balíčky v provozním prostředí.

1. Proveďte kroky v sekci [Komponenty rozšíření Cloud POS](#cloud-pos-extension-components) nebo [Komponenty rozšíření Modern POS](#modern-pos-extension-components) výše v tomto článku.
2. Proveďte následující změny v balíčku konfiguračních souborů ve složce **RetailSdk\\Assets**:

    1. V konfiguračních souborech **commerceruntime.ext.config** a **CommerceRuntime.MPOSOffline.Ext.config** přidejte následující řádky do sekce **composition**:

        # <a name="application-update-4"></a>[Aktualizace aplikace 4](#tab/app-update-4)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="application-update-5-and-later"></a>[Aktualizace aplikace 5 a novější](#tab/app-update-5-and-later)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 a novější](#tab/retail-7-3-2)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 a novější](#tab/retail-7-3-5)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 a novější](#tab/retail-8-1-1)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        ---

    2. Povolte přizpůsobení Commerce Proxy:

        # <a name="application-update-4"></a>[Aktualizace aplikace 4](#tab/app-update-4)

        V konfiguračním souboru **dllhost.exe.config** přidejte následující řádky do podsekce **appSettings** v sekci **configuration**.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="application-update-5-and-later"></a>[Aktualizace aplikace 5 a novější](#tab/app-update-5-and-later)

        V konfiguračním souboru **dllhost.exe.config** přidejte následující řádky do podsekce **appSettings** v sekci **configuration**.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        V konfiguračním souboru **RetailProxy.MPOSOffline.ext.config** přidejte následující řádky do sekce **composition**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 a novější](#tab/retail-7-3-2)

        V konfiguračním souboru **RetailProxy.MPOSOffline.ext.config** přidejte následující řádky do sekce **composition**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 a novější](#tab/retail-7-3-5)

        V konfiguračním souboru **RetailProxy.MPOSOffline.ext.config** přidejte následující řádky do sekce **composition**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 a novější](#tab/retail-8-1-1)

        V konfiguračním souboru **RetailProxy.MPOSOffline.ext.config** přidejte následující řádky do sekce **composition**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        ---

3. Proveďte následující změny v konfiguračním souboru balíčku přizpůsobení **Customization.settings**:

    1. Povolte přizpůsobení Retail Proxy.

        # <a name="application-update-4"></a>[Aktualizace aplikace 4](#tab/app-update-4)

        Přidejte následující řádky do sekce **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;**.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="application-update-5-and-later"></a>[Aktualizace aplikace 5 a novější](#tab/app-update-5-and-later)

        Přidejte následující řádky do sekce **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;**.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        Následující řádky přidejte do sekce **ItemGroup**, čímž zahrnete rozšíření proxy Retail do nasaditelných balíčků:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 a novější](#tab/retail-7-3-2)

        Následující řádky přidejte do sekce **ItemGroup**, čímž zahrnete rozšíření proxy Retail do nasaditelných balíčků:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 a novější](#tab/retail-7-3-5)

        Následující řádky přidejte do sekce **ItemGroup**, čímž zahrnete rozšíření proxy Retail do nasaditelných balíčků:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 a novější](#tab/retail-8-1-1)

        Následující řádky přidejte do sekce **ItemGroup**, čímž zahrnete rozšíření proxy Retail do nasaditelných balíčků:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        ---

    2. Následující řádky přidejte do sekce **ItemGroup**, čímž zahrnete rozšíření CRT do nasaditelných balíčků:

        # <a name="application-update-4"></a>[Aktualizace aplikace 4](#tab/app-update-4)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="application-update-5-and-later"></a>[Aktualizace aplikace 5 a novější](#tab/app-update-5-and-later)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 a novější](#tab/retail-7-3-2)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 a novější](#tab/retail-7-3-5)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 a novější](#tab/retail-8-1-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        ---

    3. Následující řádky přidejte do sekce **ItemGroup**, čímž zahrnete rozšíření Retail Server do nasaditelných balíčků:

        # <a name="application-update-4"></a>[Aktualizace aplikace 4](#tab/app-update-4)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        ```

        # <a name="application-update-5-and-later"></a>[Aktualizace aplikace 5 a novější](#tab/app-update-5-and-later)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 a novější](#tab/retail-7-3-2)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 a novější](#tab/retail-7-3-5)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 a novější](#tab/retail-8-1-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        ---

4. Upravte následující soubory tak, aby zahrnovaly zdrojové soubory pro Norsko v nasaditelných balíčcích:
    - Packages\_SharedPackagingProjectComponents\Sdk.ModernPos.Shared.csproj
    - Packages\RetailServer\Sdk.RetailServerSetup.proj
  
  - Pro soubor **Sdk.ModernPos.Shared.csproj** 
    - Přidejte řádek do sekce **ItemGroup**
    
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```
    > [!Note]
    > Místo <File_name>zadejte název souboru prostředků. Totéž platí pro další příklady uvedené níže.
 
    - Přidejte řádek do sekce **Target Name="CopyPackageFiles"**
       ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\nb-NO" SkipUnchangedFiles="true" />
        ```
  
  - Pro soubor **Sdk.RetailServerSetup.proj** 
    - Přidejte řádek do sekce **ItemGroup**
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```    
    - Přidejte řádek do sekce **Target Name="CopyPackageFiles"**
         ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\nb-NO" SkipUnchangedFiles="true" />
        ```    

5. Upravte konfigurační soubor certifikátu zadáním kryptografického otisku, umístění úložiště a názvu úložiště pro certifikát, který chcete použít k podepisování prodejních transakcí. Poté zkopírujte konfigurační soubor do složky **References**.

    # <a name="application-update-4"></a>[Aktualizace aplikace 4](#tab/app-update-4)

    Soubor má název **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** a nachází se v umístění **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="application-update-5-and-later"></a>[Aktualizace aplikace 5 a novější](#tab/app-update-5-and-later)

    Soubor má název **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** a nachází se v umístění **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    Soubor má název **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** a nachází se v umístění **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 a novější](#tab/retail-7-3-2)

    Soubor má název **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** a nachází se v umístění **Extensions.SequentialSignatureRegister\\bin\\Debug**.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 a novější](#tab/retail-7-3-5)

    Soubor má název **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** a nachází se v umístění **Extensions.SequentialSignatureRegister\\bin\\Debug**.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 a novější](#tab/retail-8-1-1)

    Soubor má název **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** a nachází se v umístění **Extensions.SequentialSignatureRegister\\bin\\Debug**.

    ---

6. Aktualizujte konfigurační soubor pro Retail Server. V souboru **RetailSDK\\Packages\\RetailServer\\Code\\web.config** přidejte následující řádky do sekce **extensionComposition**.

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

7. Spuštěním příkazu **msbuild** pro celou sadu Retail SDK vytvořte nasaditelné balíčky.
8. Balíčky použijte pomocí služby Microsoft Dynamics Lifecycle Services (LCS) nebo ručně. Další informace naleznete v tématu [Vytvoření balíčků pro nasazení](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Povolení digitálního podpisu v režimu offline pro moderní POS

Chcete-li povolit digitální podpis v režimu offline pro Modern POS, musíte po aktivaci Modern POS na novém zařízení postupovat podle těchto kroků.

1. Přihlaste se do POS.
2. Na stránce **Stav připojení databáze** zkontrolujte, zda je offline databáze plně synchronizována. Když hodnota pole **Položky čekající na stažení** je **0** (nula), databáze je plně synchronizována.
3. Odhlaste se ze systému POS.
4. Chvíli počkejte, než bude offline databáze plně synchronizována.
5. Přihlaste se do POS.
6. Na stránce **Stav připojení databáze** zkontrolujte, zda je offline databáze plně synchronizována. Když hodnota pole **Čekající transakce v offline databázi** je **0** (nula), databáze je plně synchronizována.
7. Restartujte Modern POS.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
