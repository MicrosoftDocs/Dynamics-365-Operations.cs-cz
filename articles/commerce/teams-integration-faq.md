---
title: Nejčastější dotazy k integraci Dynamics 365 Commerce a Microsoft Teams
description: Toto téma obsahuje odpovědi na časté dotazy související s integrací Microsoft Dynamics 365 Commerce a Microsoft Teams.
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
ms.openlocfilehash: 26e1dc53126c0615332457aa785415c4c7112bbd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842630"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a><span data-ttu-id="7914e-103">Nejčastější dotazy k integraci Dynamics 365 Commerce a Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7914e-103">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="7914e-104">Toto téma obsahuje odpovědi na časté dotazy související s integrací Microsoft Dynamics 365 Commerce a Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="7914e-104">This topic provides answers to frequently asked questions regarding Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a><span data-ttu-id="7914e-105">Kdo se v obchodě stane vlastníkem týmu při zřizování Teams z Commerce?</span><span class="sxs-lookup"><span data-stu-id="7914e-105">Who in the store becomes an owner of a team while provisioning Teams from Commerce?</span></span> 

<span data-ttu-id="7914e-106">Všichni správci obchodů jsou automaticky přidáni jako vlastníci do příslušné skupiny týmu, aby mohli provádět operace, jako je přidání soukromého kanálu a přidání nebo odstranění členů.</span><span class="sxs-lookup"><span data-stu-id="7914e-106">All store managers are automatically added as owners to the corresponding team group so that they can perform operations such as adding a private channel and adding or deleting members.</span></span> 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a><span data-ttu-id="7914e-107">Jak přiřadit roli „manažer komunikace“ zaměstnanci v centrále Commerce?</span><span class="sxs-lookup"><span data-stu-id="7914e-107">How do I assign the "communications manager" role to an employee in Commerce headquarters?</span></span> 

<span data-ttu-id="7914e-108">Manažeři komunikace v Microsoft Teams mají schopnost vytvářet a publikovat seznamy úkolů.</span><span class="sxs-lookup"><span data-stu-id="7914e-108">Communication managers in Microsoft Teams have the ability to create and publish task lists.</span></span> <span data-ttu-id="7914e-109">Zaměstnanci organizace, kteří mají být manažery komunikace, musí mít v centrále Commerce přiřazenu roli „manažer maloobchodních úkolů“.</span><span class="sxs-lookup"><span data-stu-id="7914e-109">Organization employees who need to become communication managers must have the "retail task manager" role assigned to them in Commerce headquarters.</span></span>

<span data-ttu-id="7914e-110">Chcete-li přiřadit roli manažera maloobchodních úloh zaměstnanci v centrále Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="7914e-110">To assign the retail task manager role to an employee in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="7914e-111">Přejděte na **Retail a Commerce \> Zaměstnanci \> Uživatelé**.</span><span class="sxs-lookup"><span data-stu-id="7914e-111">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="7914e-112">Vyberte zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="7914e-112">Select an employee.</span></span>
1. <span data-ttu-id="7914e-113">Na pevné záložce **Role uživatele** vyberte možnost **Přiřadit role**.</span><span class="sxs-lookup"><span data-stu-id="7914e-113">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="7914e-114">V dialogovém okně **Přiřadit uživateli role** vyberte roli **Manažer maloobchodních úkolů** a pak tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="7914e-114">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a><span data-ttu-id="7914e-115">Jak zpřístupním konkrétní organizační hierarchii, aby ji bylo možné odeslat do Microsoft Teams?</span><span class="sxs-lookup"><span data-stu-id="7914e-115">How do I make a specific organization hierarchy available to upload into Microsoft Teams?</span></span>

<span data-ttu-id="7914e-116">V centrále Commerce je hierarchie každé organizace přidružena k jednomu či více účelům.</span><span class="sxs-lookup"><span data-stu-id="7914e-116">In Commerce headquarters, every organization's hierarchy is associated with one or more purposes.</span></span> <span data-ttu-id="7914e-117">Ujistěte se, že hierarchie, kterou chcete zřídit v Microsoft Teams, má přidružen účet **Vykazování Retail**, jak ukazuje následující obrázek s příkladem.</span><span class="sxs-lookup"><span data-stu-id="7914e-117">Make sure the hierarchy that you want to provision into Microsoft Teams has the **Retail reporting** purpose associated with it, as shown in the following example image.</span></span> 

![Příklad účelu hierarchie organizace v centrále Commerce](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a><span data-ttu-id="7914e-119">Jak povolím pracovníkům maloobchodních prodejen, aby se mohli přihlásit k pokladnímu místu (POS) Commerce pomocí Azure Active Directory (Azure AD)?</span><span class="sxs-lookup"><span data-stu-id="7914e-119">How do I enable retail store workers to sign in to Commerce point of sale (POS) using Azure Active Directory (Azure AD)?</span></span>

<span data-ttu-id="7914e-120">Informace, jak nakonfigurovat prostředí pro přihlášení k POS Commerce s ověřováním Azure AD viz [Povolení ověřování Azure Active Directory pro přihlášení k POS](aad-pos-logon.md).</span><span class="sxs-lookup"><span data-stu-id="7914e-120">For information about how to configure the Commerce POS sign-in experience to use Azure AD authentication, see [Enable Azure Active Directory authentication for POS sign-in](aad-pos-logon.md).</span></span>

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a><span data-ttu-id="7914e-121">Jak mohu mapovat obchody a odpovídající týmy v centrále Commerce, pokud moje organizace již vytvořila týmy v Microsoft Teams?</span><span class="sxs-lookup"><span data-stu-id="7914e-121">How do I map stores and corresponding teams in Commerce headquarters if my organization has already created teams in Microsoft Teams?</span></span>

<span data-ttu-id="7914e-122">Informace, jak mapovat obchody a týmy, pokud již týmy existují, najdete v části [Mapování obchodů a odpovídajících týmů, pokud již vaše organizace vlastní existující týmy Microsoft Teams](map-stores-existing-teams.md).</span><span class="sxs-lookup"><span data-stu-id="7914e-122">For information on how to map stores and teams if there are pre-existing teams, see [Map stores and corresponding teams if your organization has pre-existing teams in Microsoft Teams](map-stores-existing-teams.md).</span></span>

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a><span data-ttu-id="7914e-123">Jak vymažu token Microsoft Graph API uložený v úložišti relace?</span><span class="sxs-lookup"><span data-stu-id="7914e-123">How do I clear the Microsoft Graph API token stored in the session storage?</span></span>

<span data-ttu-id="7914e-124">Uživatel, který se přihlásil k prodejnímu místu (POS) pomocí účtu Azure Active Directory (Azure AD) by se měl odhlásit z POS nebo zavřít aplikaci, aby se vymazalo úložiště relace.</span><span class="sxs-lookup"><span data-stu-id="7914e-124">A user who has signed in to the point of sale (POS) with an Azure Active Directory (Azure AD) account should sign out from the POS or close the application to clear the session storage.</span></span> 

> [!TIP]
> <span data-ttu-id="7914e-125">Doporučeným postupem je vždy nechat pracovníky obchodu zamknout terminál POS nebo se odhlásit z relace, pokud terminál nepoužívají.</span><span class="sxs-lookup"><span data-stu-id="7914e-125">A recommended best practice is to always have store workers lock the POS terminal or sign out from a session when not using the terminal.</span></span> 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a><span data-ttu-id="7914e-126">Co se stane, když obchod nemá manažery?</span><span class="sxs-lookup"><span data-stu-id="7914e-126">What happens if a store doesn't have store managers?</span></span>

<span data-ttu-id="7914e-127">Pokud obchod nemá manažery, pro daný obchod nebo v Teams nebude vytvořena skupina týmu.</span><span class="sxs-lookup"><span data-stu-id="7914e-127">If a store doesn't have managers, a team group will not be created for the store or in Teams.</span></span> 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a><span data-ttu-id="7914e-128">Co se stane, když manažer obchodu opustí společnost?</span><span class="sxs-lookup"><span data-stu-id="7914e-128">What happens if a store manager leaves the company?</span></span>

<span data-ttu-id="7914e-129">Kdokoli s rolí vlastníka může přidat nového manažera obchodu v centrále Commerce a znovu zřídit Teams, takže nový manažer bude mít v Teams potřebná oprávnění pro danou skupinu.</span><span class="sxs-lookup"><span data-stu-id="7914e-129">Anyone with the owner role can add a new store manager in Commerce headquarters and reprovision Teams so that the new manager will have the necessary privileges in Teams for the group.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="7914e-130">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="7914e-130">Additional resources</span></span>

[<span data-ttu-id="7914e-131">Přehled integrace Dynamics 365 Commerce a Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7914e-131">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="7914e-132">Povolení integrace Dynamics 365 Commerce a Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7914e-132">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="7914e-133">Zřízení Microsoft Teams z Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="7914e-133">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="7914e-134">Synchronizace správy úkolů mezi Microsoft Teams a Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="7914e-134">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="7914e-135">Správa uživatelských rolí v Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7914e-135">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="7914e-136">Mapování obchodů a týmů, pokud v Microsoft Teams již existují přednastavené týmy</span><span class="sxs-lookup"><span data-stu-id="7914e-136">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)
