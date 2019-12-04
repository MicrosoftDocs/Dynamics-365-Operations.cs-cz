---
title: Vytvoření šablony procesu náboru v aplikaci Attract
description: Toto téma poskytuje informace o způsobu vytvoření šablony procesu náboru v aplikaci Attract.
author: andreabichsel
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.openlocfilehash: 82046d43cf7366b760c140bdb8b017337b4f41da
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832551"
---
# <a name="create-a-hiring-process-template-in-attract"></a><span data-ttu-id="a9934-103">Vytvoření šablony procesu náboru v aplikaci Attract</span><span class="sxs-lookup"><span data-stu-id="a9934-103">Create a hiring process template in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a9934-104">*Šablona náborového procesu* obsahuje všechny aktivity, které mají být zahrnuty jako součást náborového procesu pro práci.</span><span class="sxs-lookup"><span data-stu-id="a9934-104">A *hiring process template* contains all the activities that should be included as part of the hiring process for a job.</span></span> <span data-ttu-id="a9934-105">Toto téma popisuje prvky šablony procesu v aplikaci Microsoft Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="a9934-105">This topic describes the elements of a process template in Microsoft Dynamics 365 Talent: Attract.</span></span> <span data-ttu-id="a9934-106">Také vysvětluje, jakým způsobem vytvořit šablonu.</span><span class="sxs-lookup"><span data-stu-id="a9934-106">It also explains how to create a template.</span></span>

> [!NOTE]
> <span data-ttu-id="a9934-107">Vytvoření šablony je součástí doplňku komplexního náboru pro Attract.</span><span class="sxs-lookup"><span data-stu-id="a9934-107">Template creation is part of the Comprehensive Hiring Add-on for Attract.</span></span>

## <a name="template-management"></a><span data-ttu-id="a9934-108">Správa šablony</span><span class="sxs-lookup"><span data-stu-id="a9934-108">Template management</span></span>

<span data-ttu-id="a9934-109">Organizace mohou rozhodnout, zda členové týmu nebo pouze správci mohou v aplikaci Attract vytvářet šablony procesů.</span><span class="sxs-lookup"><span data-stu-id="a9934-109">Organizations can decide whether team members or only admins can create process templates in Attract.</span></span> <span data-ttu-id="a9934-110">Chcete-li nakonfigurovat správu šablon, přejděte na **Centrum pro správu** \> **Správa šablony**.</span><span class="sxs-lookup"><span data-stu-id="a9934-110">To configure template management, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="a9934-111">Chcete-li nechat členy týmu vytvořit své vlastní šablony, zapněte správu šablony.</span><span class="sxs-lookup"><span data-stu-id="a9934-111">To let team members create their own templates, turn on template management.</span></span> <span data-ttu-id="a9934-112">Pokud správu šablony nezapnete, mohou šablony vytvářet pouze správci šablony.</span><span class="sxs-lookup"><span data-stu-id="a9934-112">If you don't turn on template management, only admins can create templates.</span></span>

## <a name="default-template"></a><span data-ttu-id="a9934-113">Výchozí šablona</span><span class="sxs-lookup"><span data-stu-id="a9934-113">Default template</span></span>

<span data-ttu-id="a9934-114">Pouze správci mohou nastavit výchozí šablonu.</span><span class="sxs-lookup"><span data-stu-id="a9934-114">Only admins can set the default template.</span></span> <span data-ttu-id="a9934-115">Výchozí šablona se používá tehdy, když není při vytváření práce vybrána šablona.</span><span class="sxs-lookup"><span data-stu-id="a9934-115">The default template is used if a template isn't selected when a job is created.</span></span> <span data-ttu-id="a9934-116">Chcete-li nastavit výchozí šablonu, přejděte na **Centrum pro správu** \> **Správa šablony**.</span><span class="sxs-lookup"><span data-stu-id="a9934-116">To set the default template, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="a9934-117">Na kartě šablony, která má být výchozí šablonou, vyberte tlačítko se třemi tečkami (**...**) a poté vyberte **Nastavit jako výchozí**.</span><span class="sxs-lookup"><span data-stu-id="a9934-117">On the card for the template that should be the default template, select the ellipsis button (**...**), and then select **Set as default**.</span></span>

## <a name="create-a-process-template"></a><span data-ttu-id="a9934-118">Vytvoření šablony procesu</span><span class="sxs-lookup"><span data-stu-id="a9934-118">Create a process template</span></span>

<span data-ttu-id="a9934-119">Správci, náboroví pracovníci a náboroví manažeři mohou vytvářet šablony procesu.</span><span class="sxs-lookup"><span data-stu-id="a9934-119">Admins, recruiters, and hiring managers can create process templates.</span></span> <span data-ttu-id="a9934-120">Šablona procesu se skládá z *fází* a *aktivit*.</span><span class="sxs-lookup"><span data-stu-id="a9934-120">A process template consists of *stages* and *activities*.</span></span> <span data-ttu-id="a9934-121">Fáze seskupují dohromady jednu nebo více aktivit.</span><span class="sxs-lookup"><span data-stu-id="a9934-121">Stages group together one or more activities.</span></span> <span data-ttu-id="a9934-122">Ve výchozím nastavení má každá šablona procesu aktivity Potenciální uchazeč, Žádost a Nabídka.</span><span class="sxs-lookup"><span data-stu-id="a9934-122">By default, every process template has Prospect, Application, and Offer activities.</span></span> <span data-ttu-id="a9934-123">Fáze, které obsahují tyto činnosti, lze přejmenovat.</span><span class="sxs-lookup"><span data-stu-id="a9934-123">The stages that contain these activities can be renamed.</span></span> <span data-ttu-id="a9934-124">Můžete přidat další fáze výběrem **+ Nová fáze**.</span><span class="sxs-lookup"><span data-stu-id="a9934-124">You can add more stages by selecting **+ New Stage**.</span></span> <span data-ttu-id="a9934-125">Aktivity můžete přidávat do fáze buď jejich přetažením do příslušné fáze, nebo dvojitým kliknutím na aktivitu v seznamu aktivit.</span><span class="sxs-lookup"><span data-stu-id="a9934-125">You can add activities to a stage either by dragging them to the appropriate stage or by double-clicking them in the activity list.</span></span>

> [!NOTE]
> <span data-ttu-id="a9934-126">Názvy fází jsou viditelné pro kandidáty na stránce **Stav přihlášky**.</span><span class="sxs-lookup"><span data-stu-id="a9934-126">Stage names are visible to candidates on the **Application status** page.</span></span> <span data-ttu-id="a9934-127">Tuto skutečnost je třeba zvážit při výběru názvů fází.</span><span class="sxs-lookup"><span data-stu-id="a9934-127">You should consider this fact when you choose names for stages.</span></span>

<span data-ttu-id="a9934-128">Další informace o aktivitách naleznete v tématu [Aktivity procesu náboru](./activities-attract.md).</span><span class="sxs-lookup"><span data-stu-id="a9934-128">To learn more about activities, see [Activities in hiring processes](./activities-attract.md).</span></span>

<span data-ttu-id="a9934-129">Pro vytvoření šablony náborového procesu postupujte podle těchto kroků:</span><span class="sxs-lookup"><span data-stu-id="a9934-129">Follow these steps to create a hiring process template.</span></span>

1. <span data-ttu-id="a9934-130">Přejděte na **Šablony**.</span><span class="sxs-lookup"><span data-stu-id="a9934-130">Go to **Templates**.</span></span>
2. <span data-ttu-id="a9934-131">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="a9934-131">Select **New**.</span></span>
3. <span data-ttu-id="a9934-132">V poli **Název šablony** zadejte název šablony a pak vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="a9934-132">In the **Template name** field, enter a name for the template, and then select **Create**.</span></span>
4. <span data-ttu-id="a9934-133">V seznamu **Zvolit schvalovací proces** vyberte **Výchozí**, aby práce vyžadovala schválení.</span><span class="sxs-lookup"><span data-stu-id="a9934-133">In the **Choose the approval process** list, select **Default** to require approval for a job.</span></span>
5. <span data-ttu-id="a9934-134">Výběrem povolte nebo zakažte potenciální uchazeče.</span><span class="sxs-lookup"><span data-stu-id="a9934-134">Select to enable or disable prospects.</span></span>
6. <span data-ttu-id="a9934-135">Volitelné: Přidejte nebo odeberte fáze.</span><span class="sxs-lookup"><span data-stu-id="a9934-135">Optional: Add or remove stages.</span></span>

    - <span data-ttu-id="a9934-136">Chcete-li přidat fázi, vyberte **+ nová fáze**.</span><span class="sxs-lookup"><span data-stu-id="a9934-136">To add a stage, select **+ New Stage**.</span></span>
    - <span data-ttu-id="a9934-137">Chcete-li odebrat fázi, najeďte myší nad fázi a poté zvolte tlačítko koše, které se objeví.</span><span class="sxs-lookup"><span data-stu-id="a9934-137">To remove a stage, hover the pointer over the stage, and then select the trash can button that appears.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a9934-138">Fáze Potenciální uchazeč, Žádost a Nabídka nemohou být odstraněny, ale lze je přejmenovat.</span><span class="sxs-lookup"><span data-stu-id="a9934-138">Prospect, Application, and Offer stages can't be removed, but they can be renamed.</span></span>

7. <span data-ttu-id="a9934-139">Volitelné: Přidejte nebo odeberte aktivity.</span><span class="sxs-lookup"><span data-stu-id="a9934-139">Optional: Add or remove activities.</span></span>

    - <span data-ttu-id="a9934-140">Pokud chcete přidat aktivitu, přetáhněte ji ze seznamu aktivit na pravé straně do příslušné fáze.</span><span class="sxs-lookup"><span data-stu-id="a9934-140">To add an activity, drag it from the activity list on the right to the appropriate stage.</span></span> <span data-ttu-id="a9934-141">Případně na aktivitu dvakrát klikněte a pak vyberte fázi, do které ji chcete přidat.</span><span class="sxs-lookup"><span data-stu-id="a9934-141">Alternatively, double-click the activity, and then select the stage to add it to.</span></span>
    - <span data-ttu-id="a9934-142">Chcete-li odstranit aktivitu, rozbalte jí a pak vyberte tlačítko koše na záhlaví aktivity.</span><span class="sxs-lookup"><span data-stu-id="a9934-142">To remove an activity, expand it, and then select the trash can button on the activity header.</span></span>

8. <span data-ttu-id="a9934-143">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a9934-143">Select **Save**.</span></span>
