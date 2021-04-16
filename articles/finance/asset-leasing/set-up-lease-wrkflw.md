---
title: Nastavení pracovních postupů schvalování leasingu
description: V tématu je vysvětleno, jak nastavit pracovní postup schválení, který bude spuštěn při vytvoření nového leasingu.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4d5416b3b24d5fbb3ac46afb3c672212d41d42d5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827547"
---
# <a name="set-up-lease-approval-workflows"></a><span data-ttu-id="c8539-103">Nastavení pracovních postupů schvalování leasingu</span><span class="sxs-lookup"><span data-stu-id="c8539-103">Set up lease approval workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8539-104">V tématu je vysvětleno, jak nastavit pracovní postup schválení, který bude spuštěn při vytvoření nového leasingu.</span><span class="sxs-lookup"><span data-stu-id="c8539-104">The topic explains how to set up an approval workflow that will run when a new lease is created.</span></span> <span data-ttu-id="c8539-105">Informace o tom, jak používat pracovní postup, najdete v části [Použití pracovních postupů schvalování leasingu](use-create-lease-wrkflw.md).</span><span class="sxs-lookup"><span data-stu-id="c8539-105">For information about how to use the workflow, see [Use lease approval workflows](use-create-lease-wrkflw.md).</span></span> 

1. <span data-ttu-id="c8539-106">Přejděte na **Leasing majetku \> Nastavení \> Pracovní postup leasingu**.</span><span class="sxs-lookup"><span data-stu-id="c8539-106">Go to **Asset leasing \> Setup \> Lease workflow**.</span></span>
2. <span data-ttu-id="c8539-107">Na stránce **Pracovní postup leasingu** zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="c8539-107">On the **Lease workflow** page, select **New**.</span></span>
3. <span data-ttu-id="c8539-108">V zobrazeném dialogovém okně v části **Typ pracovního postupu** vyberte odkaz **Pracovní postup pronájmu**.</span><span class="sxs-lookup"><span data-stu-id="c8539-108">In the dialog box that appears, under **Workflow type**, select the **Lease workflow** link.</span></span>

    <span data-ttu-id="c8539-109">Aplikace je otevřena.</span><span class="sxs-lookup"><span data-stu-id="c8539-109">The application is opened.</span></span> <span data-ttu-id="c8539-110">Po spuštění se přihlaste k Azure Active Directory (Azure AD), abyste byli přesměrováni do aplikace pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="c8539-110">After it runs, sign in to Azure Active Directory (Azure AD) to be redirected to the workflow application.</span></span>

4. <span data-ttu-id="c8539-111">Přetáhněte prvek **Schválení pracovního postupu leasingu** do pracovního toku.</span><span class="sxs-lookup"><span data-stu-id="c8539-111">Drag the **Lease workflow approval** element onto the workflow.</span></span>
5. <span data-ttu-id="c8539-112">Připojte jeden uzel ze **Start** do **Schválení pracovního postupu leasingu**.</span><span class="sxs-lookup"><span data-stu-id="c8539-112">Connect one node from **Start** to **Lease workflow approval**.</span></span> <span data-ttu-id="c8539-113">Pak připojte **Schválení pracovního postupu leasingu** na **Konec**.</span><span class="sxs-lookup"><span data-stu-id="c8539-113">Then connect **Lease workflow approval** to **End**.</span></span>
6. <span data-ttu-id="c8539-114">Dvakrát klikněte na **Schválení pracovního postupu leasingu**.</span><span class="sxs-lookup"><span data-stu-id="c8539-114">Double-click **Lease workflow approval**.</span></span>
7. <span data-ttu-id="c8539-115">Vyberte **Vlastnosti** a poté v části **Základní nastavení** zadejte název pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="c8539-115">Select **Properties**, and then, under **Basic settings**, enter a name for the workflow.</span></span>

    <span data-ttu-id="c8539-116">Na této stránce můžete také nastavit další parametry pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="c8539-116">On this page, you can also set more parameters for the workflow.</span></span> <span data-ttu-id="c8539-117">Pokud jste zapnuli **Automatické akce**, systém automaticky provede konkrétní akci.</span><span class="sxs-lookup"><span data-stu-id="c8539-117">If you've turned on **Automatic actions**, the system will automatically take a specific action.</span></span> <span data-ttu-id="c8539-118">Oznámení lze zasílat, pokud jsou uvedena na kartě **Oznámení**. Na kartě **Pokročilé nastavení** můžete určit konečného schvalovatele, nastavit časový limit a určit konkrétní akce, které je třeba dokončit.</span><span class="sxs-lookup"><span data-stu-id="c8539-118">Notifications can be sent if they are specified on the **Notifications** tab. On the **Advanced settings** tab, you can specify a final approver, set a time limit, and designate specific actions that must be completed.</span></span>

8. <span data-ttu-id="c8539-119">Po dokončení nastavení parametrů pracovního postupu vyberte **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="c8539-119">When you've finished setting the workflow parameters, select **Close**.</span></span>
9. <span data-ttu-id="c8539-120">Vyberte **Krok 1** a poté vyberte **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="c8539-120">Select **Step 1**, and then select **Properties**.</span></span>
10. <span data-ttu-id="c8539-121">V části **Základní nastavení** zadejte název kroku, vytvořte předmět pro schválení a zadejte pokyny ke schválení.</span><span class="sxs-lookup"><span data-stu-id="c8539-121">Under **Basic settings**, enter a name for the step, create a subject line for the approval, and specify instructions for the approval.</span></span>
11. <span data-ttu-id="c8539-122">Na stránce **Úkol** vyberte typ přiřazení.</span><span class="sxs-lookup"><span data-stu-id="c8539-122">On the **Assignment** page, select the assignment type.</span></span>
12. <span data-ttu-id="c8539-123">Chcete-li ke schválení přiřadit konkrétní uživatele, vyberte **Uživatel**, vyberte uživatele, kteří schvalují leasing, a poté vyberte **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="c8539-123">To assign specific users to the approval, select **User**, select the users who approve leases, and then select **Close**.</span></span>
13. <span data-ttu-id="c8539-124">Vyberte **Uložit a zavřít** k vytvoření pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="c8539-124">Select **Save and close** to create the workflow.</span></span> <span data-ttu-id="c8539-125">Po zobrazení výzvy vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8539-125">Then, when you're prompted, select **OK**.</span></span>
14. <span data-ttu-id="c8539-126">Na stránce **Vytvořit pracovní postup** zvolte **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="c8539-126">On the **Create workflow** page, select **Close**.</span></span>
14. <span data-ttu-id="c8539-127">Vyberte nový pracovní postup a pak vyberte **Verze**.</span><span class="sxs-lookup"><span data-stu-id="c8539-127">Select the new workflow, and then select **Versions**.</span></span> <span data-ttu-id="c8539-128">Poté vyberte **Aktivovat** pro zajištění, aby byl pracovní postup aktivní.</span><span class="sxs-lookup"><span data-stu-id="c8539-128">Then select **Make active** to ensure that the workflow is active.</span></span>
15. <span data-ttu-id="c8539-129">Vyberte **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="c8539-129">Select **Close**.</span></span> <span data-ttu-id="c8539-130">Zobrazí se nová aktivní verze.</span><span class="sxs-lookup"><span data-stu-id="c8539-130">The new active version appears.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]