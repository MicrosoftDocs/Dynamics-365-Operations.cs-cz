---
title: Pokyny k nasazení registračních pokladen pro Norsko
description: Tento článek poskytuje návod, jak povolit funkce pokladny pro lokalizaci Microsoft Dynamics 365 Commerce pro Norsko.
author: EvgenyPopovMBS
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 9149e9da7222699e9ca996b69e56fff07b77a737
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/24/2022
ms.locfileid: "9345984"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a>Pokyny k nasazení registračních pokladen pro Norsko

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> Kroky popsané v tomto článku byste měli implementovat pouze v případě, že používáte Microsoft Dynamics 365 Commerce verze 10.0.29 nebo novější. Ve verzi Commerce 10.0.28 nebo starší musíte použít předchozí verzi Retail software development kit (SDK) na vývojářském virtuálním počítači (VM) v Microsoft Dynamics Lifecycle Services (LCS). Další informace viz [Pokyny k nasazení registračních pokladen pro Norsko (staré)](./emea-nor-loc-deployment-guidelines.md). Pokud používáte Commerce verze 10.0.28 nebo starší a migrujete na Commerce verze 10.0.29 nebo novější, musíte postupovat podle kroků v [Migrujte ze starší funkce Commerce pro Norsko](./emea-nor-fi-migration.md).

Tento článek poskytuje návod, jak povolit funkce pokladny pro lokalizaci Commerce pro Norsko. Lokalizace se skládá z několika rozšíření komponent, které vám umožňují provádět akce, například tisknout vlastní pole na příjemky, registrovat dodatečné události auditu, prodejní transakce a platební transakce v pokladním místě (POS), digitálně podepisovat prodejní transakce a tisknout sestavy X a Z v místních formátech. Další informace o lokalizaci pro Norsko viz [Funkce registrační pokladny pro Norsko](./emea-nor-cash-registers.md). Další informace o konfiguraci Commerce pro Norsko viz [Nastavení Commerce pro Norsko](./emea-nor-cash-registers.md#setting-up-commerce-for-norway).

## <a name="set-up-fiscal-registration-for-norway"></a>Nastavení fiskální registrace pro Norsko

Ukázka fiskální registrace pro Norsko je založena na [funkci fiskální integrace](fiscal-integration-for-retail-channel.md) a je součástí řešení Commerce SDK. Ukázka rozšíření POS se nachází ve složce **src\\FiscalIntegration\\SequentialSignatureNorway** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). [Ukázka](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) obsahuje poskytovatele fiskálních dokumentů a fiskálního konektoru, což jsou rozšíření modulu Commerce Runtime (CRT). Další informace o tom, jak používat Commerce SDK, viz [Stáhněte si ukázky Commerce SDK a referenční balíčky z GitHub a NuGet](../dev-itpro/retail-sdk/sdk-github.md) a [Nastavte kanál buildu pro SDK nezávislého balení](../dev-itpro/build-pipeline.md).

Postupujte podle kroků pro nastavení fiskální registrace popsané v části [Nastavení fiskální integrace pro kanály Commerce](./setting-up-fiscal-integration-for-retail-channel.md):

1. [Nastavení procesu fiskální registrace](./setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Nezapomeňte si poznamenat nastavení procesu fiskální registrace, která jsou [specifická pro Norsko](#configure-the-fiscal-registration-process).
1. [Nastavení zpracování chyb](./setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Povolit ruční provedení zápisu odložené daňové registrace](./setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurace komponent kanálu](#configure-channel-components).

### <a name="configure-the-fiscal-registration-process"></a>Konfigurace procesu fiskální registrace

Podle těchto kroků povolíte proces fiskální registrace pro Norsko v centrále Commerce.

1. Stáhněte si konfigurační soubory pro poskytovatele fiskálních dokumentů a fiskální konektor ze sady Commerce SDK:

    1. Otevřete úložiště [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Otevřete poslední dostupnou větev vydání.
    1. Otevřete **src \> FiscalIntegration \> SequentialSignatureNorway \> CommerceRuntime**.
    1. Stáhněte si konfigurační soubor poskytovatele fiskálních dokumentů v umístění **DocumentProvider.SequentialSignNorway \> Configuration \> DocumentProviderSequentialSignatureNorwaySample.xml**.
    1. Stáhněte si konfigurační soubor fiskálního konektoru v umístění **Connector.SequentialSignNorway \> Configuration \> ConnectorSequentialSignatureNorwaySample.xml**.

1. Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry \> Sdílené parametry**. Na kartě **Obecné** nastavte možnost **Povolit fiskální integraci** na **Ano**.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Fiskální konektory** a načtěte konfigurační soubor fiskálního konektoru, který jste stáhli dříve.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Poskytovatelé fiskálních dokumentů** a načtěte konfigurační soubor poskytovatele fiskálního dokumentu, který jste stáhli dříve.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Funkční profily Connector**. Vytvořte nový funkční profil konektoru a vyberte poskytovatele dokumentů a konektor, které jste načetli předtím.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Technické profily Connector**. Vytvořte nový technický profil konektoru a vyberte konektor, který jste načetli předtím. Nastavte typ konektoru na **Interní**.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Skupiny fiskálního konektoru** a vytvořte novou skupinu fiskálního konektoru pro funkční profil konektoru vytvořený dříve.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Proces fiskální registrace**. Vytvořte nový procesu daňové registrace a krok procesu fiskální registrace a vyberte skupinu fiskálního konektoru, kterou jste předtím vytvořili.
1. Přejděte na **Maloobchodní a velkoobchodní prodej \> Instalace kanálu \> Nastavení POS \> Profily POS \> Funkční profily**. Vyberte funkční profil, který je připojena k obchodu, kde by měl být aktivován proces registrace. Na pevné záložce **Proces fiskální registrace** vyberte proces fiskální registrace, který jste předtím vytvořili. Na záložce s náhledem **Fiskální služby** vyberte technický profil konektoru, který jste vytvořili dříve. 
1. Přejděte na **Retail and Commerce \> IT pro Retail and Commerce \> Plán distribuce**. Otevřete plán distribuce a vyberte úlohy **1070** a **1090** pro převod dat do databáze kanálů.

### <a name="configure-the-digital-signature-parameters"></a>Konfigurace parametrů digitálního podpisu

Musíte nakonfigurovat certifikáty, které se budou používat pro digitální podepisování prodejních transakcí v obchodě. K podepisování se používá digitální certifikát, který je uložený v Azure Key Vault. V Modern POS v offline režimu lze podepisování provést také pomocí digitálního certifikátu, který je uložen v místním úložišti počítače, na kterém je Modern POS nainstalován.

Než budete moci používat digitální certifikát, který je uložen v úložišti Key Vault, je třeba provést následující kroky.

1. Úložiště Key Vault musí být vytvořeno. Doporučujeme nasadit úložiště ve stejné geografické oblasti jako Commerce Scale Unit.
1. Certifikát musí být nahrán do úložiště Key Vault jako tajný klíč řetězce base64.
1. Aplikace Application Object Server (AOS) musí být autorizována ke čtení tajných klíčů z úložiště Key Vault.

Další informace, jak pracovat s Key Vault, viz [Začínáme s Azure Key Vault](/azure/key-vault/key-vault-get-started).

Dále na stránce **Parametry úložiště Key Vault** musíte zadat parametry pro přístup k úložišti Key Vault:

- **Název** a **Popis** – Název a popis úložiště Key Vault.
- **Adresa URL úložiště Key Vault** – Adresa URL úložiště Key Vault.
- **Klient úložiště Key Vault** – ID interaktivního klienta aplikace Azure Active Directory (Azure AD), které je přidruženo k úložišti Key Vault pro účely ověřování. Tento klient by měl mít přístup ke čtení tajných klíčů z úložiště.
- **Tajný klíč úložiště Key Vault** – Tajný klíč, který je přidružen k aplikaci Azure AD, která se používá k ověřování v úložišti Key Vault.
- **Název**, **Popis** a **Odkaz na tajný klíč** – Název, popis a odkaz na tajný klíč certifikátu.

Dále musíte nakonfigurovat konektor pro vaše certifikáty, které jsou uloženy v úložišti Key Vault nebo místním úložišti certifikátů. Tento konektor se používá pro podepisování na straně kanálu.

1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Technické profily Connector**.
1. Na záložce s náhledem **Nastavení** zadejte následující parametry pro digitální podpisy:

    - **Název tajného klíče** – Vyberte název tajného klíče, který jste dříve konfigurovali na stránce **Parametry úložiště Key Vault**.
    - **Kryptografický otisk místního certifikátu** – Poskytněte kryptografický otisk pro certifikát, který je uložen lokálně.
    - **Algoritmus hash** – Zadejte jeden z kryptografických algoritmů hash, které jsou podporovány rozhraním Microsoft .NET, například **SHA1**.
    - **Název úložiště certifikátů** – Toto pole je volitelné. Slouží k určení výchozího názvu obchodu, který by se měl použít k hledání v místních certifikátech.
    - **Umístění úložiště certifikátů** – Toto pole je volitelné. Slouží k určení výchozího místa obchodu, který by se měl použít k hledání v místních certifikátech.
    - **Nejprve vyzkoušet místní certifikát** – Tuto možnost vyberte, chcete-li pro podepisování dat standardně používat certifikát z místního úložiště namísto certifikátu z úložiště Key Vault.
    - **Aktivovat kontrolu stavu** – Další informace o funkci kontroly stavu naleznete v tématu [Kontrola stavu fiskální registrace](./fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

> [!NOTE]
> - Pro Norsko je aktuálně dostupný pouze kryptografický algoritmus hash **SHA1**.
> - Výchozí název obchodu a umístění obchodu se přidávají proto, aby se zjednodušil proces hledání místních certifikátů v modulu CRT. X509StoreProvider má seznam složek, kde jsou certifikáty uloženy. Pokud není zadán výchozí název obchodu a výchozí umístění obchodu, pokusí se X509StoreProvider najít certifikát ve všech složkách ve svém seznamu.

### <a name="configure-channel-components"></a>Konfigurace komponent kanálu

#### <a name="development-environment"></a>Vývojové prostředí

Tento postup slouží k nastavení vývojového prostředí, abyste mohli testovat a rozšířit vzorek.

1. Naklonujte nebo stáhněte úložiště [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions). Vyberte správnou verzi větve vydání podle vaší verze SDK/aplikace. Další informace viz [Stažení ukázek Commerce SDK a referenčních balíčků z GitHub a NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Otevřete řešení **SequentialSignatureNorway.sln** v umístění **Dynamics365Commerce.Solutions\\FiscalIntegration\\SequentialSignatureNorway** a sestavte jej.
1. Nainstalujte rozšíření CRT:

    1. Vyhledejte instalační program rozšíření CRT:

        - **Commerce Scale Unit:** Ve složce **SequentialSignatureNorway\\ScaleUnit\\ScaleUnit.SequentialSignNorway.Installer\\bin\\Debug\\net461** vyhledejte instalátor **ScaleUnit.SequentialSignNorway.Installer**.
        - **Místní CRT v Modern POS:** Ve složce **SequentialSignatureNorway\\ModernPOS\\ModernPos.SequentialSignNorway.Installer\\bin\\Debug\\net461** vyhledejte instalátor **ModernPos.SequentialSignNorway.Installer**.

    1. Spusťte instalační program rozšíření CRT z příkazového řádku:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

        - **Místní CRT v Modern POS:**

            ```Console
            ModernPOS.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>Produkční prostředí

Postupujte podle kroků v části [Nastavení kanálu buildu pro ukázku fiskální integrace](fiscal-integration-sample-build-pipeline.md), kterými vygenerujete a uvolníte nasaditelné balíčky Cloud Scale Unit a samoobslužné nasaditelné balíčky pro ukázku fiskální integrace. Soubor YAML šablony **SequentialSignatureNorway build-pipeline.yml** se nachází ve složce **Pipeline\\YAML_Files** úložiště [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions).

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Povolení digitálního podpisu v režimu offline pro moderní POS

Chcete-li povolit digitální podpis v režimu offline pro Modern POS, musíte po aktivaci Modern POS na novém zařízení postupovat podle těchto kroků.

1. Přihlaste se do POS.
1. Na stránce **Stav připojení databáze** zkontrolujte, zda je offline databáze plně synchronizována. Když hodnota pole **Položky čekající na stažení** je **0** (nula), databáze je plně synchronizována.
1. Odhlaste se ze systému POS.
1. Chvíli počkejte, než bude offline databáze plně synchronizována.
1. Přihlaste se do POS.
1. Na stránce **Stav připojení databáze** zkontrolujte, zda je offline databáze plně synchronizována. Když hodnota pole **Čekající transakce v offline databázi** je **0** (nula), databáze je plně synchronizována.
1. Znovu otevřete Modern POS.
