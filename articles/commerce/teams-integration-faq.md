---
title: Nejčastější dotazy k integraci Dynamics 365 Commerce a Microsoft Teams
description: Tento článek obsahuje odpovědi na časté dotazy související s integrací Microsoft Dynamics 365 Commerce a Microsoft Teams.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 02f10e446349803ce5629fed0be4176f2df2be0c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869120"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a>Nejčastější dotazy k integraci Dynamics 365 Commerce a Microsoft Teams

[!include [banner](includes/banner.md)]

Tento článek obsahuje odpovědi na časté dotazy související s integrací Microsoft Dynamics 365 Commerce a Microsoft Teams.

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a>Kdo se v obchodě stane vlastníkem týmu při zřizování Teams z Commerce? 

Všichni správci obchodů jsou automaticky přidáni jako vlastníci do příslušné skupiny týmu, aby mohli provádět operace, jako je přidání soukromého kanálu a přidání nebo odstranění členů. 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a>Jak přiřadit roli „manažer komunikace“ zaměstnanci v centrále Commerce? 

Manažeři komunikace v Microsoft Teams mají schopnost vytvářet a publikovat seznamy úkolů. Zaměstnanci organizace, kteří mají být manažery komunikace, musí mít v centrále Commerce přiřazenu roli „manažer maloobchodních úkolů“.

Chcete-li přiřadit roli manažera maloobchodních úloh zaměstnanci v centrále Commerce, postupujte takto.

1. Přejděte na **Retail a Commerce \> Zaměstnanci \> Uživatelé**.
1. Vyberte zaměstnance.
1. Na pevné záložce **Role uživatele** vyberte možnost **Přiřadit role**.
1. V dialogovém okně **Přiřadit uživateli role** vyberte roli **Manažer maloobchodních úkolů** a pak tlačítko **OK**.

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a>Jak zpřístupním konkrétní organizační hierarchii, aby ji bylo možné odeslat do Microsoft Teams?

V centrále Commerce je hierarchie každé organizace přidružena k jednomu či více účelům. Ujistěte se, že hierarchie, kterou chcete zřídit v Microsoft Teams, má přidružen účet **Vykazování Retail**, jak ukazuje následující obrázek s příkladem. 

![Příklad účelu hierarchie organizace v centrále Commerce.](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a>Jak povolím pracovníkům maloobchodních prodejen, aby se mohli přihlásit k pokladnímu místu (POS) Commerce pomocí Azure Active Directory (Azure AD)?

Informace, jak nakonfigurovat prostředí pro přihlášení k POS Commerce s ověřováním Azure AD viz [Povolení ověřování Azure Active Directory pro přihlášení k POS](aad-pos-logon.md).

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a>Jak mohu mapovat obchody a odpovídající týmy v centrále Commerce, pokud moje organizace již vytvořila týmy v Microsoft Teams?

Informace, jak mapovat obchody a týmy, pokud již týmy existují, najdete v části [Mapování obchodů a odpovídajících týmů, pokud již vaše organizace vlastní existující týmy Microsoft Teams](map-stores-existing-teams.md).

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a>Jak vymažu token Microsoft Graph API uložený v úložišti relace?

Uživatel, který se přihlásil k prodejnímu místu (POS) pomocí účtu Azure Active Directory (Azure AD) by se měl odhlásit z POS nebo zavřít aplikaci, aby se vymazalo úložiště relace. 

> [!TIP]
> Doporučeným postupem je vždy nechat pracovníky obchodu zamknout terminál POS nebo se odhlásit z relace, pokud terminál nepoužívají. 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a>Co se stane, když obchod nemá manažery?

Pokud obchod nemá manažery, pro daný obchod nebo v Teams nebude vytvořena skupina týmu. 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a>Co se stane, když manažer obchodu opustí společnost?

Kdokoli s rolí vlastníka může přidat nového manažera obchodu v centrále Commerce a znovu zřídit Teams, takže nový manažer bude mít v Teams potřebná oprávnění pro danou skupinu. 

## <a name="additional-resources"></a>Další prostředky

[Přehled integrace Dynamics 365 Commerce a Microsoft Teams](commerce-teams-integration.md)

[Povolení integrace Dynamics 365 Commerce a Microsoft Teams](enable-teams-integration.md)

[Zřízení Microsoft Teams z Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Synchronizace správy úkolů mezi Microsoft Teams a Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Správa uživatelských rolí v Microsoft Teams](manage-user-roles-teams.md)

[Mapování obchodů a týmů, pokud v Microsoft Teams již existují přednastavené týmy](map-stores-existing-teams.md)
