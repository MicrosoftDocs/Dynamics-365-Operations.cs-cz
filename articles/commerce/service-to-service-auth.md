---
title: Konfigurace ověřování mezi službami
description: Toto téma popisuje, jak nakonfigurovat ověřování mezi službami v Microsoft Dynamics 365 Commerce pro bezpečné volání API služeb pro hodnocení a recenze.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: da780de5f15d72bdac85a261eae809125c830260
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968510"
---
# <a name="configure-service-to-service-authentication"></a>Konfigurace ověřování mezi službami

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak nakonfigurovat ověřování mezi službami (S2S) v Microsoft Dynamics 365 Commerce pro bezpečné volání API služeb pro hodnocení a recenze.

Dynamics 365 Commerce nabízí [hodnocení a recenze](ratings-reviews-overview.md) jako omnikanálové řešení. Toto řešení umožňuje přístup k servisním API z místo mimo Commerce, aby šlo provádět různé úkoly. Tyto úkoly zahrnují import hodnocení a recenzí z vašeho externího systému do Commerce a export hodnocení a recenzí z Commerce. Chcete-li Commerce umožnit bezpečné volání rozhraní API pro hodnocení a recenze, musíte nejprve nakonfigurovat ověřování S2S provedením postupů v tomto tématu.

## <a name="add-a-new-app-registration"></a>Přidání nové registrace aplikace

Před přidáním nové registrace aplikace musíte vytvořit aplikaci pomocí [Azure Portal](https://portal.azure.com). Chcete-li zaregistrovat aplikaci v Azure Active Directory (Azure AD) a povolit ověřování, postupujte podle kroků v [Použít Azure Active Directory s vlastním konektorem v Power Automate](/connectors/custom-connectors/azure-active-directory-authentication).

Shromážděte následující ID z Azure Portal. Tato ID budete potřebovat v následujících krocích.

- ID aplikace klienta
- ID adresáře klienta (tenanta)

Novou registraci aplikace přidáte v konfigurátoru webů Commerce tímto postupem.

1. Přejděte na **Domů \> Recenze \> Nastavení**.
1. V části **Ověřování mezi službami (S2S)** vyberte **Spravovat**.

    ![Tlačítko Spravovat v části Ověřování mezi službami (S2S) v konfigurátoru webů Commerce.](media/Ratings-reviews-settings-service-to-service-authentication.png)

1. V podokně **Záznamy aplikace S2S**, které se zobrazí vpravo, vyberte **Přidat novou registraci aplikace S2S**.
1. V dialogovém okně **Přidat záznam aplikace S2S** zadejte požadované údaje. Použijte hodnoty z registrace aplikace Azure.

    - **Název** – Zadejte název aplikace (například **Aplikace Fabrikam**).
    - **ID aplikace klienta** – Zadejte ID aplikace (například **00000000-0000-0000-0000-000000000000**).
    - **ID adresáře (tenanta)** – Zadejte ID adresáře (např. **00000000-0000-0000-0000-000000000000**).

    ![Dialogové okno Přidat záznam aplikace S2S konfigurátoru webů Commerce.](media/Ratings-reviews-settings-S2S-APP-entry.png)

1. Vyberte **Odeslat**. Nyní by se měl zobrazit název vaší aplikace S2S v seznamu v podokně **Záznamy aplikace S2S**.
1. Zavřete podokno **Záznamy aplikace S2S**.
1. Zvolte možnost **Uložit**.

## <a name="edit-an-existing-app-registration"></a>Úprava existující registrace aplikace

Stávající registraci aplikace upravíte v konfigurátoru webů Commerce tímto postupem.

1. Přejděte na **Domů \> Recenze \> Nastavení**.
1. V části **Ověřování mezi službami (S2S)** vyberte **Spravovat**.
1. V podokně **Záznamy aplikace S2S** vyberte symbol tužky vedle položky, kterou chcete upravit.
1. Aktualizujte hodnoty v polích **Název**, **ID aplikace klienta** a **ID adresáře (tenanta)** podle potřeby.
1. Vyberte **Odeslat**.
1. Zavřete podokno **Záznamy aplikace S2S**.
1. Zvolte možnost **Uložit**.

## <a name="remove-an-existing-app-registration"></a>Odebrání existující registrace aplikace

Stávající registraci aplikace odeberete v konfigurátoru webů Commerce tímto postupem.

1. Přejděte na **Domů \> Recenze \> Nastavení**.
1. V části **Ověřování mezi službami (S2S)** vyberte **Spravovat**.
1. V podokně **Záznamy aplikace S2S** vyberte symbol koše vedle položky, kterou chcete odebrat. Záznam je odstraněn ze seznamu.
1. Zavřete podokno **Záznamy aplikace S2S**.
1. Zvolte možnost **Uložit**.

## <a name="additional-resources"></a>Další prostředky

[Přehled hodnocení a recenzí](ratings-reviews-overview.md)

[Připojení k používání hodnocení a recenzí](opt-in-ratings-reviews.md)

[Správa hodnocení a recenzí](manage-reviews.md)

[Konfigurace hodnocení a recenzí](configure-ratings-reviews.md)

[Synchronizace hodnocení produktů](sync-product-ratings.md)

[Povolit ruční publikování hodnocení a recenzí moderátorem](manual-publish-rating-reviews.md)

[Import a export hodnocení a recenzí](import-export-reviews.md)

[Nejčastější dotazy k hodnocení a recenzím](ratings-reviews-faq.md) 
