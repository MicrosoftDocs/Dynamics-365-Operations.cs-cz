---
title: "Vytváření servisních smluv"
description: "Toto téma popisuje použití funkcí v modulech Správa servisu a Řízení projektů a účetnictví k vytváření servisních smluv."
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5447787ea0f6b0c83e43fa5f0a4e18db9361f04c
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="create-service-agreements"></a><span data-ttu-id="2a58e-103">Vytváření servisních smluv</span><span class="sxs-lookup"><span data-stu-id="2a58e-103">Create service agreements</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="2a58e-104">Toto téma popisuje použití funkcí v modulech Správa servisu a Řízení projektů a účetnictví k vytváření servisních smluv.</span><span class="sxs-lookup"><span data-stu-id="2a58e-104">This topic describes how to use features in the Service management and the Project management and accounting modules to create service agreements.</span></span>

## <a name="create-a-service-agreement-from-service-management"></a><span data-ttu-id="2a58e-105">Vytvoření servisní smlouvy z modulu Řízení servisu</span><span class="sxs-lookup"><span data-stu-id="2a58e-105">Create a service agreement from Service management</span></span>

1. <span data-ttu-id="2a58e-106">Přejděte na **Správa servisu**.</span><span class="sxs-lookup"><span data-stu-id="2a58e-106">Navigate to **Service management**.</span></span>
2. <span data-ttu-id="2a58e-107">Kliknutím na **Servisní smlouvy** vytvořte nový řádek servisní smlouvy v záhlaví stránky.</span><span class="sxs-lookup"><span data-stu-id="2a58e-107">Click **Service agreements** to create a new service agreement line in the page header.</span></span> 
3. <span data-ttu-id="2a58e-108">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="2a58e-108">Click **New**.</span></span> <span data-ttu-id="2a58e-109">Zadejte popis, vyberte odkaz na projekt v poli **ID projektu** a vyplňte zbývající pole a řádky servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="2a58e-109">Enter a description, select a reference to a project in the **Project ID** field, and fill in the rest of the fields and lines for the service agreement.</span></span> <span data-ttu-id="2a58e-110">Klikněte na tlačítko **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="2a58e-110">Click **Save**.</span></span>
4. <span data-ttu-id="2a58e-111">Klikněte na kartu **Vztahy** a výběrem možnosti **Předměty servisu** nebo **Servisní úlohy** vytvořte vztahy předmětů servisu nebo vztahy servisních úloh pro servisní smlouvu.</span><span class="sxs-lookup"><span data-stu-id="2a58e-111">On the **Relations** tab, select **Service objects** or **Service tasks** to create service object relations or service task relations for the service agreement.</span></span> <span data-ttu-id="2a58e-112">Servisní předměty a úlohy, pro které jste vytvořili vztahy, lze přidružit k řádkům na servisní smlouvě.</span><span class="sxs-lookup"><span data-stu-id="2a58e-112">The service objects and tasks that you have created relations for can be attached on the lines of the service agreement.</span></span>
5. <span data-ttu-id="2a58e-113">V dolní části stránky vytvořte řádky servisní smlouvy. Tuto akci provedete zkopírováním řádků ze šablony servisu, použitím jiné servisní smlouvy nebo ručním vytvořením řádků servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="2a58e-113">In the lower half of the page, create service agreement lines by copying lines from a service template, another service agreement, or manually creating the service-agreement lines.</span></span>

> [!NOTE]
> <span data-ttu-id="2a58e-114">Pokud do servisní smlouvy zkopírujete řádky z jiné servisní smlouvy, můžete určit, zda chcete také zkopírovat vztahy předmětu servisu a servisní úlohy.</span><span class="sxs-lookup"><span data-stu-id="2a58e-114">If you copy lines into the service agreement from another service agreement, you can indicate whether you also want to copy service object and service task relations.</span></span> <span data-ttu-id="2a58e-115">Jestliže tyto vztahy zkopírujete, dojde k jejich přidání ke stávajícím vztahům v servisní smlouvě.</span><span class="sxs-lookup"><span data-stu-id="2a58e-115">If you copy these relations, they are added to any existing relations on the service agreement.</span></span> <span data-ttu-id="2a58e-116">Pokud zkopírujete řádky servisní smlouvy ze šablony servisu, vztahy servis-objekt a servis-úloha se zkopírují automaticky jako vztahy servis-objekt a servis-úloha v nových řádcích servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="2a58e-116">If you copy service-agreement lines from a service template, the service-object and service-task relations are automatically copied as service-object relations and service-task relations on the new service-agreement lines.</span></span>

## <a name="create-service-agreement-lines-manually"></a><span data-ttu-id="2a58e-117">Ruční vytvoření řádků servisní smlouvy</span><span class="sxs-lookup"><span data-stu-id="2a58e-117">Create service agreement lines manually</span></span>

1. <span data-ttu-id="2a58e-118">Ze stránky **Servisní smlouvy** přidejte mřížce řádků řádek servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="2a58e-118">From the **Service agreements** page, add a service agreement line in the lines grid.</span></span> 
2. <span data-ttu-id="2a58e-119">Do řádku servisní smlouvy zadejte příslušné informace.</span><span class="sxs-lookup"><span data-stu-id="2a58e-119">Enter the appropriate information for the service agreement line.</span></span> 
3. <span data-ttu-id="2a58e-120">Řádek uložte stiskem kláves **CTRL+S** a zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2a58e-120">Press **CTRL+S** to save the line, and then close the page.</span></span>

## <a name="create-a-service-agreement-from-project"></a><span data-ttu-id="2a58e-121">Vytvoření servisní smlouvy z projektu</span><span class="sxs-lookup"><span data-stu-id="2a58e-121">Create a service agreement from Project</span></span>

1. <span data-ttu-id="2a58e-122">Klikněte na **Řízení a účetnictví projektů**.</span><span class="sxs-lookup"><span data-stu-id="2a58e-122">Click **Project management and accounting**.</span></span>
2. <span data-ttu-id="2a58e-123">Klikněte na **Všechny projekty**.</span><span class="sxs-lookup"><span data-stu-id="2a58e-123">Click **All projects**.</span></span>
3. <span data-ttu-id="2a58e-124">Vyberte projekt ze seznamu.</span><span class="sxs-lookup"><span data-stu-id="2a58e-124">Select the project from the list.</span></span>
4. <span data-ttu-id="2a58e-125">V **podokně akcí** klikněte na **Spravovat**.</span><span class="sxs-lookup"><span data-stu-id="2a58e-125">On the **Action Pane**, click **Manage**.</span></span> <span data-ttu-id="2a58e-126">Ve skupině **Nová akce** klikněte na tlačítko **Servis** a vyberte **Servisní smlouva**.</span><span class="sxs-lookup"><span data-stu-id="2a58e-126">In the **New** Action group, click **Service** and select **Service agreement**.</span></span>
5. <span data-ttu-id="2a58e-127">Postupujte podle kroků v části s názvem **Vytvoření servisní smlouvy** popsané dříve v tomto tématu pro zadání odkazu na projekt.</span><span class="sxs-lookup"><span data-stu-id="2a58e-127">Follow the steps in the section titled **Create a service agreement** as described earlier in this topic to enter the project reference.</span></span>


## <a name="related-topics"></a><span data-ttu-id="2a58e-128">Související témata</span><span class="sxs-lookup"><span data-stu-id="2a58e-128">Related topics</span></span>

[<span data-ttu-id="2a58e-129">Servisní smlouvy </span><span class="sxs-lookup"><span data-stu-id="2a58e-129">Service agreements</span></span>](service-agreements.md)



