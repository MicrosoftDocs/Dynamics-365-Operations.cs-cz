---
title: Import a export hodnocení a recenzí
description: Tento článek popisuje, jak importovat a exportovat hodnocení a recenze produktů v Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: f369e3cd208cdfba816f817ead75374ee6982912
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271928"
---
# <a name="import-and-export-ratings-and-reviews"></a>Import a export hodnocení a recenzí

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak importovat a exportovat hodnocení a recenze produktů v Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce nabízí [hodnocení a recenze](ratings-reviews-overview.md) jako omnikanálové řešení. Když přepnete na řešení hodnocení a recenzí Dynamics 365 Commerce, možná budete chtít přesunout svá stávající data hodnocení a recenzí na platformu Commerce. Můžete také exportovat data hodnocení a recenzí z Commerce na základě vašich obchodních požadavků. Konektor Power Automate umožňuje importovat hodnocení a recenze do Commerce a exportovat je z Commerce.

> [!NOTE]
> Informace o tom, jak začít s logickými toky v Power Automate, viz [Vytvoření cloudového toku v Power Automate](/power-automate/get-started-logic-flow).

## <a name="prerequisites"></a>Předpoklady

Než budete moci importovat a exportovat hodnocení a recenze, musíte splnit následující předpoklady:

- Řešení hodnocení a recenzí musí být povoleno pro váš web elektronického obchodu na platformě Commerce. Více informací viz [Přihlásit se k používání hodnocení a recenzí](opt-in-ratings-reviews.md).
- Konektor Power App pro hodnocení a recenze Dynamics 365 musí být nakonfigurován tak, aby umožňoval akce „odeslat recenze“ nebo „exportovat recenze“ v Power Automate. Více informací viz [Dynamics 365 Commerce – hodnocení a recenze (Preview)](/connectors/dynamics365ratingsre/).
- Ověření mezi službami (S2S) musí být nakonfigurováno tak, aby bezpečně volalo rozhraní API hodnocení a recenzí zvenčí Commerce. Další informace viz [Konfigurace ověřování mezi službami](service-to-service-auth.md).

## <a name="import-ratings-and-reviews"></a>Import hodnocení a recenzí

Chcete-li importovat data hodnocení a recenzí ze svého stávajícího systému do Commerce, musíte přidat konektor Power Automate hodnocení a recenzí Dynamics 365 k existujícímu nebo novému toku Power Automate. Více informací viz [Dynamics 365 Commerce – hodnocení a recenze (Preview)](/connectors/dynamics365ratingsre/).

> [!IMPORTANT]
> Provedení této procedury vyžaduje [konfiguraci ověřování S2S](service-to-service-auth.md).

Pro import hodnocení a recenzí do Commerce pomocí konektoru Power Automate hodnocení a recenzí Dynamics 365 postupujte podle těchto kroků.

1. Vyberte akci **Odeslat uživatelskou recenzi**.
1. Navažte spojení pomocí údajů aplikace Azure Active Directory (Azure AD), které byly vytvořeny při konfiguraci ověřování S2S. Další informace viz [Konfigurace ověřování mezi službami](service-to-service-auth.md).
1. Akce **Odeslat uživatelskou recenzi** bere recenze po jedné. Proto akci opakujte. Použijte zdrojové recenze jako seznam k odeslání hromadných recenzí.
    
## <a name="export-ratings-and-reviews"></a>Export hodnocení a recenzí

Chcete-li exportovat data hodnocení a recenzí z Commerce, musíte přidat konektor Power Automate hodnocení a recenzí Dynamics 365 k existujícímu nebo novému toku Power Automate. Více informací viz [Dynamics 365 Commerce – hodnocení a recenze (Preview)](/connectors/dynamics365ratingsre/).

Pro export hodnocení a recenzí z Commerce pomocí konektoru Power Automate hodnocení a recenzí Dynamics 365 postupujte podle těchto kroků.

1. Vyberte akci **Exportovat všechny recenze**.
1. Proveďte akci. 

## <a name="additional-resources"></a>Další prostředky

[Přehled hodnocení a recenzí](ratings-reviews-overview.md)

[Připojení k používání hodnocení a recenzí](opt-in-ratings-reviews.md)

[Správa hodnocení a recenzí](manage-reviews.md)

[Konfigurace hodnocení a recenzí](configure-ratings-reviews.md)

[Synchronizace hodnocení produktů](sync-product-ratings.md)

[Povolit ruční publikování hodnocení a recenzí moderátorem](manual-publish-rating-reviews.md)

[Konfigurace ověřování mezi službami](service-to-service-auth.md)

[Nejčastější dotazy k hodnocení a recenzím](ratings-reviews-faq.md)
