---
title: Povolení integrace Dynamics 365 Commerce a Microsoft Teams
description: Tento článek popisuje, jak povolit integraci Microsoft Dynamics 365 Commerce a Microsoft Teams.
author: gvrmohanreddy
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 505e3854818e4d5b73fc1a22724be16036300c3b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872821"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>Povolení integrace Dynamics 365 Commerce a Microsoft Teams

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak povolit integraci Microsoft Dynamics 365 Commerce a Microsoft Teams.

Chcete-li zřídit Teams s informacemi z Dynamics 365 Commerce a synchronizovat funkce správy úkolů mezi Teams a aplikací POS (point of sale), musíte povolit integrační funkce v Commerce Headquarters.

> [!NOTE]
> Když povolíte integraci Teams, souhlasíte se sdílením svých dat s Teams. Data sdílená s Teams se mohou nacházet v jiné zemi než vaše data aplikace Commerce a mohou podléhat různým standardům dodržování předpisů. Další informace naleznete v tématu [Microsoft Trust Center](https://www.microsoft.com/trust-center). Informace o zásadách ochrany osobních údajů společnosti Microsoft najdete v [Prohlášení společnosti Microsoft o ochraně osobních údajů](https://aka.ms/privacy).

## <a name="enable-teams-integration"></a>Povolení integrace Teams

Než budete moci povolit integraci Microsoft Teams s aplikací Commerce, musíte zaregistrovat aplikaci Teams se svým klientem na portálu Azure.

Pokud chcete zaregistrovat aplikaci Teams se svým klientem na portálu Azure, postupujte takto.

1. Postupujte podle pokynů v části [Rychlý start: registrace aplikace pomocí platformy identity Microsoft](/azure/active-directory/develop/quickstart-register-app) k registraci aplikace Teams se svým klientem na portálu Azure.
1. Na kartě **Registrace aplikace** vyberte aplikaci, kterou jste vytvořili v předchozím kroku. Poté na kartě **Autentizace** vyberte **Přidat platformu**.
1. V dialogovém okně vyberte **Web**. Poté v poli **Adresy URL přesměrování** zadejte adresu URL ve formátu **\<HQUrl\>/oauth**. Část **\<HQUrl\>** nahraďte adresou URL vaší centrály Commerce (např. `https://hxennugbjtweufmdeo385f47fadb6aa9a0aos.cloudax.int.dynamics.com/oauth`).
1. Na stránce **Přehled** pro registrovanou aplikaci zkopírujte hodnotu **ID aplikace (klienta)**. Tuto hodnotu použijete v příští části k povolení integrace Teams v centrále Commerce.
1. Podle pokynů v části [Přidání tajného klíče klienta](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret) přidejte tajný klíč klienta. Poté zkopírujte **Hodnotu tajného klíče** pro klienta. Tuto hodnotu použijete v příští části k povolení integrace Teams v centrále Commerce.
1. Vyberte **Oprávnění API** a poté vyberte **Přidat oprávnění**.
1. V dialogu **Vyžádat oprávnění API** vyberte **Microsoft Graph**, vyberte **Delegovaná oprávnění**, rozbalte uzel **Skupina**, vyberte **Group.ReadWrite.All** a poté vyberte **Přidat oprávnění**.
1. V dialogu **Vyžádat oprávnění API** vyberte **Přidat oprávnění**, vyberte **Microsoft Graph**, vyberte **Oprávnění aplikace**, rozbalte uzel **Skupina**, vyberte **Group.ReadWrite.All** a poté vyberte **Přidat oprávnění**.
1. V dialogu **Vyžádat oprávnění API** vyberte **Přidat oprávnění**. Na kartě **Rozhraní API používaná mojí organizací** vyhledejte položku **Microsoft Teams Retail Service** a vyberte ji.
1. Vyberte **Delegovaná oprávnění**, rozbalte uzel **TaskPublishing**, vyberte **TaskPublishing.ReadWrite.All** a poté vyberte **Přidat oprávnění**. Více informací najdete v tématu [Konfigurace klientské aplikace pro přístup k webovému rozhraní API](/azure/active-directory/develop/quickstart-configure-app-access-web-apis).

Chcete-li povolit integraci Teams v Commerce Headquarters, postupujte takto.

1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Konfigurace integrace Microsoft Teams**.
1. V podokně akcí vyberte **Upravit**.
1. Nastavte možnost **Povolit integraci Microsoft Teams** na **Ano**.
1. V poli **ID aplikace** zadejte hodnotu **ID aplikace (klienta)**, kterou jste získali při registraci aplikace Teams na portálu Azure.
1. V poli **Klíč aplikace** zadejte **Hodnotu tajného klíče**, kterou jste získali při přidání tajného klíče na portálu Azure.
1. V podokně akcí vyberte **Uložit**.

Následující obrázek ukazuje příklad konfigurace integrace Teams v Commerce Headquarters.

![Konfigurace integrace Teams v Commerce Headquarters.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a>Zákaz integrace Teams

Chcete-li zakázat integraci Microsoft Teams v Commerce Headquarters, postupujte takto.

1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Konfigurace integrace Microsoft Teams**.
1. V podokně akcí vyberte **Upravit**.
3. Nastavte možnost **Povolit integraci Microsoft Teams** na **Ne**.
4. Vymažte hodnoty z polí **ID aplikace** a **Klíč aplikace**.
1. V podokně akcí vyberte **Uložit**.

> [!NOTE]
> Po zákazu integrace Teams s Commerce již POS terminály nebudou zobrazovat úkoly, které jsou publikovány z aplikace Teams.

## <a name="additional-resources"></a>Další prostředky

[Přehled integrace Dynamics 365 Commerce a Microsoft Teams](commerce-teams-integration.md)

[Zřízení Microsoft Teams z Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Synchronizace správy úkolů mezi Microsoft Teams a Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Správa uživatelských rolí v Microsoft Teams](manage-user-roles-teams.md)

[Mapování obchodů a týmů, pokud v Microsoft Teams již existují přednastavené týmy](map-stores-existing-teams.md)

[Nejčastější dotazy k integraci Dynamics 365 Commerce a Microsoft Teams](teams-integration-faq.md)
