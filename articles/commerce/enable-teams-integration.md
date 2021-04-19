---
title: Povolení integrace Dynamics 365 Commerce a Microsoft Teams
description: Toto téma popisuje, jak povolit integraci Microsoft Dynamics 365 Commerce a Microsoft Teams.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c0dbf7a3c7fa3532e35cac240c1abb8adbdbe489
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842626"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>Povolení integrace Dynamics 365 Commerce a Microsoft Teams

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Toto téma popisuje, jak povolit integraci Microsoft Dynamics 365 Commerce a Microsoft Teams.

Chcete-li zřídit Teams s informacemi z Dynamics 365 Commerce a synchronizovat funkce správy úkolů mezi Teams a aplikací POS (point of sale), musíte povolit integrační funkce v Commerce Headquarters.

> [!NOTE]
> Když povolíte integraci Teams, souhlasíte se sdílením svých dat s Teams. Data sdílená s Teams se mohou nacházet v jiné zemi než vaše data aplikace Commerce a mohou podléhat různým standardům dodržování předpisů. Další informace naleznete v tématu [Microsoft Trust Center](https://www.microsoft.com/trust-center). Informace o zásadách ochrany osobních údajů společnosti Microsoft najdete v [Prohlášení společnosti Microsoft o ochraně osobních údajů](https://aka.ms/privacy).

## <a name="enable-teams-integration"></a>Povolení integrace Teams

Než budete moci povolit integraci Microsoft Teams s aplikací Commerce, musíte zaregistrovat aplikaci Teams se svým klientem na portálu Azure.

Pokud chcete zaregistrovat aplikaci Teams se svým klientem na portálu Azure, postupujte takto.

1. Postupujte podle pokynů v části [Rychlý start: registrace aplikace pomocí platformy identity Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) k registraci aplikace Teams se svým klientem na portálu Azure.
1. Zkopírujte hodnotu **ID aplikace (klienta)** ze stránky **Přehled** pro registrovanou aplikaci. Tuto hodnotu použijete k povolení integrace Teams v Commerce Headquarters.
1. Zkopírujte hodnotu certifikátu, která byla zadána, když jste [přidali certifikát](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) v kroku 1. Certifikát je také známý jako veřejný klíč nebo klíč aplikace. Tuto hodnotu použijete k povolení integrace Teams v Commerce Headquarters.

Chcete-li povolit integraci Teams v Commerce Headquarters, postupujte takto.

1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Konfigurace integrace Microsoft Teams**.
1. V podokně akcí vyberte **Upravit**.
1. Nastavte možnost **Povolit integraci Microsoft Teams** na **Ano**.
1. V polích **ID aplikace** a **Klíč aplikace** zadejte hodnoty, které jste získali při registraci aplikace Teams na portálu Azure.
1. V podokně akcí vyberte **Uložit**.

Následující obrázek ukazuje příklad konfigurace integrace Teams v Commerce Headquarters.

![Konfigurace integrace Teams v Commerce Headquarters](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

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
