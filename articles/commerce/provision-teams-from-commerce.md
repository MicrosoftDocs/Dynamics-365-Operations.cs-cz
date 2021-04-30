---
title: Zřízení Microsoft Teams z Dynamics 365 Commerce
description: Toto téma popisuje, jak zřídit Microsoft Teams pomocí organizačních dat z Dynamics 365 Commerce.
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
ms.openlocfilehash: ba7c74942735b723d1015dc4da0068fbb631bc6b
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908897"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a><span data-ttu-id="a5d0e-103">Zřízení Microsoft Teams z Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a5d0e-103">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a5d0e-104">Toto téma popisuje, jak zřídit Microsoft Teams pomocí organizačních dat z Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-104">This topic describes how to provision Microsoft Teams by using organizational data from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a5d0e-105">Dynamics 365 Commerce nabízí snadný způsob zřízení Teams, pokud jste tam dosud nenastavili týmy pro své maloobchodní prodejny.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-105">Dynamics 365 Commerce offers an easy way to provision Teams if you haven't yet set up teams for your retail stores there.</span></span> <span data-ttu-id="a5d0e-106">Využíváním výhod dobře definovaných informací z Commerce, které chcete použít v Teams, můžete svým zaměstnancům obchodu pomoci začít pracovat v Teams.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-106">By taking advantage of well-defined information from Commerce that you want to use in Teams, you can help your store employees get started in Teams.</span></span> <span data-ttu-id="a5d0e-107">Mezi tyto informace patří hierarchie organizace, názvy obchodů, informace o zaměstnancích a účty Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="a5d0e-107">This information includes the organizational hierarchy, store names, employee information, and Azure Active Directory (Azure AD) accounts.</span></span> 

<span data-ttu-id="a5d0e-108">Proces zřizování Teams má dva hlavní kroky:</span><span class="sxs-lookup"><span data-stu-id="a5d0e-108">The process of provisioning Teams has two main steps:</span></span>

1. <span data-ttu-id="a5d0e-109">V aplikaci Teams vytvořte tým pro každý maloobchod a přidejte pracovníky obchodu jako členy příslušného týmu.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-109">In Teams, create a team for each retail store, and add store workers as members of the appropriate team.</span></span> <span data-ttu-id="a5d0e-110">Pokud je zaměstnanec přidružen k více než jednomu maloobchodu, odráží tuto skutečnost členství v týmu.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-110">If an employee is associated with more than one retail store, team membership will reflect that fact.</span></span> <span data-ttu-id="a5d0e-111">Bude vytvořen komunikační tým, který jako členy bude zahrnovat regionální manažery, aby pomohl publikovat úkoly z Teams.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-111">A communications team that includes regional managers as members will be created to help publish tasks from Teams.</span></span>
1. <span data-ttu-id="a5d0e-112">Nahrajte svou organizační hierarchii z Commerce do Teams.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-112">Upload your organizational hierarchy from Commerce to Teams.</span></span>

## <a name="provision-teams-in-commerce-headquarters"></a><span data-ttu-id="a5d0e-113">Zřízení Teams v Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="a5d0e-113">Provision Teams in Commerce headquarters</span></span>

<span data-ttu-id="a5d0e-114">Před zřízením Microsoft Teams proveďte tyto úkoly:</span><span class="sxs-lookup"><span data-stu-id="a5d0e-114">Before you provision Microsoft Teams, complete these tasks:</span></span>

- <span data-ttu-id="a5d0e-115">Potvrďte, že všichni regionální manažeři byli jmenováni správci komunikace.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-115">Confirm that all regional managers have been made communications managers.</span></span>
- <span data-ttu-id="a5d0e-116">Potvrďte, že účet Azure každého manažera a pracovníka obchodu byl přidružen k záznamu pracovníka tohoto manažera nebo pracovníka v Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-116">Confirm that the Azure account of every store manager and worker has been associated with that manager's or worker's worker record in Commerce headquarters.</span></span>

<span data-ttu-id="a5d0e-117">Chcete-li zřídit Teams v Commerce Headquarters, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-117">To provision Teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a5d0e-118">Přejděte na **Retail a Commerce \> Nastavení kanálu \> Konfigurace integrace Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-118">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="a5d0e-119">V podokně akcí vyberte **Zřídit Teams**.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-119">On the Action Pane, select **Provision teams**.</span></span> <span data-ttu-id="a5d0e-120">Vytvoří se dávková úloha, která je pojmenována **Zřídit Teams**.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-120">A batch job that is named **Teams provision** is created.</span></span>
1. <span data-ttu-id="a5d0e-121">Přejděte na **Správa systému \> Dotazy \> Dávkové úlohy** a vyhledejte nejnovější úlohu s popisem **Zřízení Teams**.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-121">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="a5d0e-122">Počkejte, až se tato úloha dokončí.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-122">Wait until this job has finished running.</span></span>

> [!TIP]
> <span data-ttu-id="a5d0e-123">Pokud žádný z vašich regionálních manažerů, manažerů obchodů a pracovníků obchodů nebyl přidružen k licenci Teams, může se zobrazit následující chybová zpráva: „Nepodařilo se načíst použitelné kategorie SKU pro uživatele.“</span><span class="sxs-lookup"><span data-stu-id="a5d0e-123">If none of your regional managers, store managers, and store workers have been associated with a Teams license, you might receive the following error message: "Failed to retrieve appliable Sku categories for the user."</span></span> <span data-ttu-id="a5d0e-124">Chcete-li problém vyřešit, vyberte **Synchronizovat týmy a členy** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-124">To correct the issue, select **Sync teams and members** on the Action Pane.</span></span>

<!-- ![Dynamics 365 Commerce - Teams integration configuration](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a><span data-ttu-id="a5d0e-125">Ověření zřízení Teams v centru pro správu Teams</span><span class="sxs-lookup"><span data-stu-id="a5d0e-125">Validate Teams provisioning in the Teams admin center</span></span>

<span data-ttu-id="a5d0e-126">Chcete-li ověřit zřízení Microsoft Teams v centru pro správu Microsoft Teams, postupujte podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-126">To validate Microsoft Teams provisioning in the Microsoft Teams admin center, follow these steps.</span></span>
    
1. <span data-ttu-id="a5d0e-127">Přejděte do [centra pro správu Teams](https://admin.teams.microsoft.com/) a přihlaste se jako správce vašeho klienta elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-127">Go to the [Teams admin center](https://admin.teams.microsoft.com/), and sign in as the administrator of your e-commerce tenant.</span></span>
1. <span data-ttu-id="a5d0e-128">V levém navigačním podokně vyberte **Teams**, rozbalte ho a poté vyberte **Spravovat týmy**.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-128">In the left navigation pane, select **Teams** to expand it, and then select **Manage teams**.</span></span>
1. <span data-ttu-id="a5d0e-129">Potvrďte, že pro každý maloobchod Commerce byl vytvořen jeden tým.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-129">Confirm that one team has been created for each Commerce retail store.</span></span>
1. <span data-ttu-id="a5d0e-130">Vyberte tým a potvrďte, že do něj byli přidáni pracovníci obchodu jako členové.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-130">Select a team, and confirm that store workers have been added to it as members.</span></span>
1. <span data-ttu-id="a5d0e-131">V levém navigačním podokně vyberte **Uživatelé** a potvrďte, že všichni zaměstnanci obchodu ve všech obchodech byli přidáni jako uživatelé.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-131">In the left navigation pane, select **Users**, and confirm that all store employees in all stores have been added as users.</span></span>

<span data-ttu-id="a5d0e-132">Následující obrázek ukazuje příklad stránky **Spravovat týmy** v centru pro správu Teams.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-132">The following illustration shows an example of the **Manage teams** page in the Teams admin center.</span></span>

![Příklad stránky Spravovat týmy v centru pro správu Teams](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a><span data-ttu-id="a5d0e-134">Nahrajte organizační hierarchii Commerce do Teams.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-134">Upload a Commerce organizational hierarchy to Teams</span></span>
    
<span data-ttu-id="a5d0e-135">Lze použít hierarchii organizace Commerce v Microsoft Teams a publikovat úkoly do všech nebo vybraných obchodů, které používají stejnou hierarchickou strukturu.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-135">The Commerce organizational hierarchy can be used in Microsoft Teams to publish tasks to all or selected stores that use the same hierarchy structure.</span></span>

<span data-ttu-id="a5d0e-136">Pokud chcete odeslat organizační hierarchii Commerce do Teams, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-136">To upload a Commerce organizational hierarchy to Teams, follow these steps.</span></span>
    
1. <span data-ttu-id="a5d0e-137">V Commerce Headquarters přejděte na možnost **Retail a Commerce \> Nastavení kanáu \> Konfigurace integrace Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-137">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="a5d0e-138">Vyberte **Stáhnout cílovou hierarchii** a potom vyberte **Maloobchody podle regionu** ke stažení souboru hodnot oddělených čárkami (CSV) hierarchie organizace.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-138">Select **Download targeting hierarchy**, and then select **Retail Stores by Region** to download a comma-separated values (CSV) file of the organizational hierarchy.</span></span>
1. <span data-ttu-id="a5d0e-139">Nainstalujte modul Microsoft Teams PowerShell podle pokynů v části [Instalace Microsoft Teams PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span><span class="sxs-lookup"><span data-stu-id="a5d0e-139">Install the Microsoft Teams PowerShell module by following the steps in [Install Microsoft Teams PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span></span>
1. <span data-ttu-id="a5d0e-140">Po zobrazení výzvy v okně Teams PowerShell se přihlaste pomocí účtu správce pro svého klienta Azure AD.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-140">When you're prompted in the Teams PowerShell window, sign in by using the administrator account for your Azure AD tenant.</span></span>
1. <span data-ttu-id="a5d0e-141">Postupujte podle pokynů v části [Nastavení cílové hierarchie týmů](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) a nahrajte soubor CSV pro cílovou hierarchii.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-141">Follow the steps in [Set up your team targeting hierarchy](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) to upload the CSV file for the targeting hierarchy.</span></span>

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a><span data-ttu-id="a5d0e-142">Ověření, že byla do Teams nahrána hierarchie organizace</span><span class="sxs-lookup"><span data-stu-id="a5d0e-142">Verify that the organizational hierarchy was uploaded to Teams</span></span>

<span data-ttu-id="a5d0e-143">Chcete-li ověřit, že byla do Microsoft Teams nahrána hierarchie organizace, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-143">To verify that the organizational hierarchy was uploaded to Microsoft Teams, follow these steps.</span></span>

1. <span data-ttu-id="a5d0e-144">Přihlaste se k Teams jako manažer komunikace.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-144">Sign in to Teams as a communications manager.</span></span>
1. <span data-ttu-id="a5d0e-145">V levém navigačním podokně vyberte **Úkoly Planner**.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-145">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="a5d0e-146">Na kartě **Publikované seznamy** vytvořte nový seznam, který má fiktivní úkol.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-146">On the **Published lists** tab, create a new list that has a dummy task.</span></span>
1. <span data-ttu-id="a5d0e-147">Zvolte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-147">Select **Publish**.</span></span> <span data-ttu-id="a5d0e-148">Hierarchie organizace by se měla objevit v dialogovém okně **Vyberte, komu publikovat**, jak je znázorněno v příkladu na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="a5d0e-148">The organizational hierarchy should appear in the **Select who to publish to** dialog box, as shown in the example in the following illustration.</span></span>

![Příklad hierarchie organizace v dialogovém okně Vyberte, komu publikovat](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a><span data-ttu-id="a5d0e-150">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="a5d0e-150">Additional resources</span></span>

[<span data-ttu-id="a5d0e-151">Přehled integrace Dynamics 365 Commerce a Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a5d0e-151">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="a5d0e-152">Povolení integrace Dynamics 365 Commerce a Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a5d0e-152">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="a5d0e-153">Synchronizace správy úkolů mezi Microsoft Teams a Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="a5d0e-153">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="a5d0e-154">Správa uživatelských rolí v Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a5d0e-154">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="a5d0e-155">Mapování obchodů a týmů, pokud v Microsoft Teams již existují přednastavené týmy</span><span class="sxs-lookup"><span data-stu-id="a5d0e-155">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="a5d0e-156">Nejčastější dotazy k integraci Dynamics 365 Commerce a Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a5d0e-156">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
