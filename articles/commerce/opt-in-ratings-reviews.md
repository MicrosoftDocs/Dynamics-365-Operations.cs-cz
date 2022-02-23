---
title: Připojení k používání hodnocení a recenzí
description: V tomto tématu je vysvětleno, jak se lze přihlásit k používání hodnocení a recenzí na vašem webu Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cbdb69202ebec19f4442041cfb1f99857da36d2e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410791"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Připojení k používání hodnocení a recenzí

[!include [banner](includes/banner.md)]

V tomto tématu je vysvětleno, jak se lze přihlásit k používání hodnocení a recenzí na vašem webu Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Řešení hodnocení a recenzí je omnikanálové řešení, které lze zpřístupnit v Dynamics 365 Commerce pomocí Microsoft Dynamics Lifecycle Services (LCS). LCS je portál pro správu, který maloobchodní prodejci používají ke správě svého prostředí od zařazení po vyřazení z provozu.

Chcete-li použít řešení hodnocení a recenze na webu obchodu, musíte při nasazení vašeho webu pro elektronický obchod v aplikaci souhlasit s hodnocením a recenzemi Dynamics 365 Commerce.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Připojení k používání hodnocení a recenzí

Chcete-li se přihlásit k používání hodnocení a recenzí na vašem webu, postupujte podle následujících kroků.

1. Postupujte podle kroků v [nasazení nového webu e-Commerce](deploy-ecommerce-site.md).
1. Zatímco jste stále v LCS, přejděte na **Nastavení nasazení Retail \> Další nastavení**.
1. Nastavte možnost **Povolit službu hodnocení a recenzování** na hodnotu **Ano**.
1. V poli **Skupina zabezpečení AAD pro moderátora hodnocení a recenzí (ID objektu skupiny zabezpečení)** zadejte ID skupiny zabezpečení Microsoft Azure Active Directory (Azure AD), která obsahuje moderátory hodnocení a recenzí.

    ![Připojení k používání hodnocení a recenzí](media/LCS_RnR_Preference.png)

1. Dokončete proces inicializace e-Commerce.

> [!NOTE] 
> Jste-li existujícím zákazníkem Dynamics 365 Commerce, který již nasadil server elektronického obchodu bez přijetí hodnocení a recenze a nyní chcete použít hodnocení a recenze z balíčku Dynamics 365 Commerce, odešlete požadavek na službu. Informace o postupu při odesílání žádostí o služby naleznete v tématu [Proces odeslání požadavků na službu](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json). 

## <a name="additional-resources"></a>Další zdroje

[Přehled hodnocení a recenzí](ratings-reviews-overview.md)

[Správa hodnocení a recenzí](manage-reviews.md)

[Konfigurace hodnocení a recenzí](configure-ratings-reviews.md)

[Synchronizace hodnocení produktů v Dynamics 365 Commerce](sync-product-ratings.md)


