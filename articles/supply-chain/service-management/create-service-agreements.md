---
title: Vytváření servisních smluv
description: Toto téma popisuje použití funkcí v modulech Správa servisu a Řízení projektů a účetnictví k vytváření servisních smluv.
author: ShylaThompson
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2343d60f5960702bc05705ee2dd0994c9e2d4fc1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817646"
---
# <a name="create-service-agreements"></a><span data-ttu-id="6e657-103">Vytváření servisních smluv</span><span class="sxs-lookup"><span data-stu-id="6e657-103">Create service agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e657-104">Toto téma popisuje použití funkcí v modulech Správa servisu a Řízení projektů a účetnictví k vytváření servisních smluv.</span><span class="sxs-lookup"><span data-stu-id="6e657-104">This topic describes how to use features in the Service management and the Project management and accounting modules to create service agreements.</span></span>

## <a name="create-a-service-agreement-from-service-management"></a><span data-ttu-id="6e657-105">Vytvoření servisní smlouvy z modulu Řízení servisu</span><span class="sxs-lookup"><span data-stu-id="6e657-105">Create a service agreement from Service management</span></span>

1. <span data-ttu-id="6e657-106">Přejděte na **Správa servisu**.</span><span class="sxs-lookup"><span data-stu-id="6e657-106">Navigate to **Service management**.</span></span>
2. <span data-ttu-id="6e657-107">Výběrem možnosti **Servisní smlouvy** vytvoříte nový řádek servisní smlouvy v záhlaví stránky.</span><span class="sxs-lookup"><span data-stu-id="6e657-107">Select **Service agreements** to create a new service agreement line in the page header.</span></span> 
3. <span data-ttu-id="6e657-108">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="6e657-108">Select **New**.</span></span> <span data-ttu-id="6e657-109">Zadejte popis, vyberte odkaz na projekt v poli **ID projektu** a vyplňte zbývající pole a řádky servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="6e657-109">Enter a description, select a reference to a project in the **Project ID** field, and fill in the rest of the fields and lines for the service agreement.</span></span> <span data-ttu-id="6e657-110">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="6e657-110">Select **Save**.</span></span>
4. <span data-ttu-id="6e657-111">Klikněte na kartu **Vztahy** a výběrem možnosti **Předměty servisu** nebo **Servisní úlohy** vytvořte vztahy předmětů servisu nebo vztahy servisních úloh pro servisní smlouvu.</span><span class="sxs-lookup"><span data-stu-id="6e657-111">On the **Relations** tab, select **Service objects** or **Service tasks** to create service object relations or service task relations for the service agreement.</span></span> <span data-ttu-id="6e657-112">Servisní předměty a úlohy, pro které jste vytvořili vztahy, lze přidružit k řádkům na servisní smlouvě.</span><span class="sxs-lookup"><span data-stu-id="6e657-112">The service objects and tasks that you have created relations for can be attached on the lines of the service agreement.</span></span>
5. <span data-ttu-id="6e657-113">V dolní části stránky vytvořte řádky servisní smlouvy. Tuto akci provedete zkopírováním řádků ze šablony servisu, použitím jiné servisní smlouvy nebo ručním vytvořením řádků servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="6e657-113">In the lower half of the page, create service agreement lines by copying lines from a service template, another service agreement, or manually creating the service-agreement lines.</span></span>

> [!NOTE]
> <span data-ttu-id="6e657-114">Pokud do servisní smlouvy zkopírujete řádky z jiné servisní smlouvy, můžete určit, zda chcete také zkopírovat vztahy předmětu servisu a servisní úlohy.</span><span class="sxs-lookup"><span data-stu-id="6e657-114">If you copy lines into the service agreement from another service agreement, you can indicate whether you also want to copy service object and service task relations.</span></span> <span data-ttu-id="6e657-115">Jestliže tyto vztahy zkopírujete, dojde k jejich přidání ke stávajícím vztahům v servisní smlouvě.</span><span class="sxs-lookup"><span data-stu-id="6e657-115">If you copy these relations, they are added to any existing relations on the service agreement.</span></span> <span data-ttu-id="6e657-116">Pokud zkopírujete řádky servisní smlouvy ze šablony servisu, vztahy servis-objekt a servis-úloha se zkopírují automaticky jako vztahy servis-objekt a servis-úloha v nových řádcích servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="6e657-116">If you copy service-agreement lines from a service template, the service-object and service-task relations are automatically copied as service-object relations and service-task relations on the new service-agreement lines.</span></span>

## <a name="create-service-agreement-lines-manually"></a><span data-ttu-id="6e657-117">Ruční vytvoření řádků servisní smlouvy</span><span class="sxs-lookup"><span data-stu-id="6e657-117">Create service agreement lines manually</span></span>

1. <span data-ttu-id="6e657-118">Ze stránky **Servisní smlouvy** přidejte mřížce řádků řádek servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="6e657-118">From the **Service agreements** page, add a service agreement line in the lines grid.</span></span> 
2. <span data-ttu-id="6e657-119">Do řádku servisní smlouvy zadejte příslušné informace.</span><span class="sxs-lookup"><span data-stu-id="6e657-119">Enter the appropriate information for the service agreement line.</span></span> 
3. <span data-ttu-id="6e657-120">Výběrem možnosti **Uložit** uložte řádek a poté zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6e657-120">Select **Save** to save the line, and then close the page.</span></span>

## <a name="create-a-service-agreement-from-project"></a><span data-ttu-id="6e657-121">Vytvoření servisní smlouvy z projektu</span><span class="sxs-lookup"><span data-stu-id="6e657-121">Create a service agreement from Project</span></span>

1. <span data-ttu-id="6e657-122">Vyberte možnost **Řízení projektů a účetnictví**.</span><span class="sxs-lookup"><span data-stu-id="6e657-122">Select **Project management and accounting**.</span></span>
2. <span data-ttu-id="6e657-123">Vyberte **Všechny projekty**.</span><span class="sxs-lookup"><span data-stu-id="6e657-123">Select **All projects**.</span></span>
3. <span data-ttu-id="6e657-124">Vyberte projekt ze seznamu.</span><span class="sxs-lookup"><span data-stu-id="6e657-124">Select the project from the list.</span></span>
4. <span data-ttu-id="6e657-125">V **podokně akcí** vyberte **Spravovat**.</span><span class="sxs-lookup"><span data-stu-id="6e657-125">On the **Action Pane**, select **Manage**.</span></span> <span data-ttu-id="6e657-126">Ve skupině **Nová akce** vyberte **Servis** a vyberte **Servisní smlouva**.</span><span class="sxs-lookup"><span data-stu-id="6e657-126">In the **New** Action group, select **Service** and select **Service agreement**.</span></span>
5. <span data-ttu-id="6e657-127">Postupujte podle kroků v části s názvem **Vytvoření servisní smlouvy** popsané dříve v tomto tématu pro zadání odkazu na projekt.</span><span class="sxs-lookup"><span data-stu-id="6e657-127">Follow the steps in the section titled **Create a service agreement** as described earlier in this topic to enter the project reference.</span></span>


## <a name="related-topics"></a><span data-ttu-id="6e657-128">Související témata</span><span class="sxs-lookup"><span data-stu-id="6e657-128">Related topics</span></span>

[<span data-ttu-id="6e657-129">Přehled přípravy a zřízení servisních smluv</span><span class="sxs-lookup"><span data-stu-id="6e657-129">Develop and establish service agreements overview</span></span>](service-agreements.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]