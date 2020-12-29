---
title: Přehled vytvoření workflow
description: Toto téma vysvětluje postup při vytváření workflowu.
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: 23fe13f7e3c7e8138b690c96fafc075c4700a60f
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693299"
---
# <a name="create-workflows-overview"></a><span data-ttu-id="b74a1-103">Přehled vytvoření workflow</span><span class="sxs-lookup"><span data-stu-id="b74a1-103">Create workflows overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b74a1-104">Toto téma vysvětluje postup při vytváření workflowu.</span><span class="sxs-lookup"><span data-stu-id="b74a1-104">This topic explains how to create a workflow.</span></span>

## <a name="open-the-workflow-editor"></a><span data-ttu-id="b74a1-105">Otevřete editor workflowu</span><span class="sxs-lookup"><span data-stu-id="b74a1-105">Open the workflow editor</span></span>

<span data-ttu-id="b74a1-106">Modul, ve kterém pracujete, určí typy workflow, které můžete vytvořit.</span><span class="sxs-lookup"><span data-stu-id="b74a1-106">The module that you're working in determines the types of workflow that you can create.</span></span> <span data-ttu-id="b74a1-107">Podle následujících kroků vyberte typ workflowu k vytvoření a otevření editoru workflowu.</span><span class="sxs-lookup"><span data-stu-id="b74a1-107">Follow these steps to select the type of workflow to create and open the workflow editor.</span></span>

1. <span data-ttu-id="b74a1-108">Otevřete modul, pro který chcete vytvořit nový workflow.</span><span class="sxs-lookup"><span data-stu-id="b74a1-108">Open the module that you want to create a new workflow for.</span></span> <span data-ttu-id="b74a1-109">Když například chcete vytvořit workflow pro nákupní žádanky, klepněte na **Zásobování a zdroje**.</span><span class="sxs-lookup"><span data-stu-id="b74a1-109">For example, to create a workflow for purchase requisitions, click **Procurement and sourcing**.</span></span>
2. <span data-ttu-id="b74a1-110">Klikněte na **Nastavení** &gt; **\[Název modulu\] workflowy**.</span><span class="sxs-lookup"><span data-stu-id="b74a1-110">Click **Setup** &gt; **\[Module name\] workflows**.</span></span>
3. <span data-ttu-id="b74a1-111">Na stránce seznamu, která se zobrazí, v podokně akcí klikněte na kartu klikněte na **Nový**.</span><span class="sxs-lookup"><span data-stu-id="b74a1-111">On the list page that appears, on the Action Pane, click **New**.</span></span>
4. <span data-ttu-id="b74a1-112">Na stránce **Vytvořit workflow** vyberte typ workflowu, který chcete vytvořit, a klepněte na tlačítko **Vytvořit workflow**.</span><span class="sxs-lookup"><span data-stu-id="b74a1-112">On the **Create workflow** page, select the type of workflow to create, and then click **Create workflow**.</span></span> <span data-ttu-id="b74a1-113">Otevře se editor workflowu.</span><span class="sxs-lookup"><span data-stu-id="b74a1-113">The workflow editor appears.</span></span> <span data-ttu-id="b74a1-114">Při navrhování workflowu postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="b74a1-114">You can now use the following procedures to design the workflow.</span></span>

## <a name="drag-workflow-elements-onto-the-canvas"></a><span data-ttu-id="b74a1-115">Přetáhněte prvky workflowu na plátno</span><span class="sxs-lookup"><span data-stu-id="b74a1-115">Drag workflow elements onto the canvas</span></span>

<span data-ttu-id="b74a1-116">Oblast **Prvky workflowu** editoru workflowu obsahuje prvky, které můžete přiřadit k workflowu.</span><span class="sxs-lookup"><span data-stu-id="b74a1-116">The **Workflow elements** area of the workflow editor contains the elements that you can add to your workflow.</span></span> <span data-ttu-id="b74a1-117">Prvky do workflowu přidáte tak, že je přetáhnete na plátno.</span><span class="sxs-lookup"><span data-stu-id="b74a1-117">To add elements to the workflow, drag them onto the canvas.</span></span>

## <a name="connect-the-elements"></a><span data-ttu-id="b74a1-118">Připojení prvků</span><span class="sxs-lookup"><span data-stu-id="b74a1-118">Connect the elements</span></span>

<span data-ttu-id="b74a1-119">Jeden prvek workflowu k jinému připojíte podržením ukazatele nad prvkem, dokud se neobjeví spojovací body.</span><span class="sxs-lookup"><span data-stu-id="b74a1-119">To connect one workflow element to another, hold the pointer over an element until connection points appear.</span></span> <span data-ttu-id="b74a1-120">Klikněte na spojovací bod a přetáhněte jej na jiný prvek.</span><span class="sxs-lookup"><span data-stu-id="b74a1-120">Click a connection point, and drag it to another element.</span></span> <span data-ttu-id="b74a1-121">Nezapomeňte spojit všechny prvky.</span><span class="sxs-lookup"><span data-stu-id="b74a1-121">Be sure to connect all the elements.</span></span>

## <a name="configure-the-properties-of-the-workflow"></a><span data-ttu-id="b74a1-122">Konfigurace vlastností workflowu</span><span class="sxs-lookup"><span data-stu-id="b74a1-122">Configure the properties of the workflow</span></span>

<span data-ttu-id="b74a1-123">Nakonfigurujte vlastnosti workflowu pomocí následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="b74a1-123">Follow these steps to configure the properties of the workflow.</span></span>

1. <span data-ttu-id="b74a1-124">Klepnutím na plátno se ujistěte, že není vybrán žádný prvek workflowu.</span><span class="sxs-lookup"><span data-stu-id="b74a1-124">Click the canvas to make sure that no workflow element is selected.</span></span>
2. <span data-ttu-id="b74a1-125">Kliknutím na **Vlastnosti** otevřete formulář **Vlastnosti** pro workflow.</span><span class="sxs-lookup"><span data-stu-id="b74a1-125">Click **Properties** to open the **Properties** page for the workflow.</span></span>
3. <span data-ttu-id="b74a1-126">Postupujte podle pokynů v tématu [Konfigurace vlastností workflow](configure-workflow-properties.md).</span><span class="sxs-lookup"><span data-stu-id="b74a1-126">Follow the procedures in the [Configure workflow properties](configure-workflow-properties.md) topic.</span></span>

## <a name="configure-the-elements-of-the-workflow"></a><span data-ttu-id="b74a1-127">Konfigurace prvků workflowu</span><span class="sxs-lookup"><span data-stu-id="b74a1-127">Configure the elements of the workflow</span></span>

<span data-ttu-id="b74a1-128">Nakonfigurujte každý prvek, který jste přetáhli na plátno.</span><span class="sxs-lookup"><span data-stu-id="b74a1-128">Configure each element that you dragged onto the canvas.</span></span> <span data-ttu-id="b74a1-129">Další informace o konfiguraci jednotlivých prvků workflowu naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="b74a1-129">For information about how to configure each workflow element, see the following topics:</span></span>

- [<span data-ttu-id="b74a1-130">Konfigurace ručních úloh ve workflow</span><span class="sxs-lookup"><span data-stu-id="b74a1-130">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
- [<span data-ttu-id="b74a1-131">Konfigurace automatizovaných úloh ve workflowu</span><span class="sxs-lookup"><span data-stu-id="b74a1-131">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
- [<span data-ttu-id="b74a1-132">Konfigurace schvalovacích procesů ve workflowu</span><span class="sxs-lookup"><span data-stu-id="b74a1-132">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
- [<span data-ttu-id="b74a1-133">Konfigurace schvalovacích kroků ve workflowu</span><span class="sxs-lookup"><span data-stu-id="b74a1-133">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
- [<span data-ttu-id="b74a1-134">Konfigurace ručních rozhodnutí ve workflow</span><span class="sxs-lookup"><span data-stu-id="b74a1-134">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
- [<span data-ttu-id="b74a1-135">Konfigurace podmíněných rozhodnutí ve workflow</span><span class="sxs-lookup"><span data-stu-id="b74a1-135">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
- [<span data-ttu-id="b74a1-136">Konfigurace paralelních větví ve workflow</span><span class="sxs-lookup"><span data-stu-id="b74a1-136">Configure parallel branches in a workflow</span></span>](configure-parallel-activity-workflow.md)
- [<span data-ttu-id="b74a1-137">Konfigurace paralelní větve</span><span class="sxs-lookup"><span data-stu-id="b74a1-137">Configure a parallel branch</span></span>](configure-parallel-branch-workflow.md)
- [<span data-ttu-id="b74a1-138">Konfigurace workflow položky řádku</span><span class="sxs-lookup"><span data-stu-id="b74a1-138">Configure line-item workflows</span></span>](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a><span data-ttu-id="b74a1-139">Vyřešení chyb nebo varování</span><span class="sxs-lookup"><span data-stu-id="b74a1-139">Resolve any errors or warnings</span></span>

<span data-ttu-id="b74a1-140">Podokno **Chyby a varování** v dolní části editoru workflowu zobrazuje zprávy, které byly vygenerovány pro workflow.</span><span class="sxs-lookup"><span data-stu-id="b74a1-140">The **Errors and warnings** pane at the bottom of the workflow editor shows messages that have been generated for the workflow.</span></span> <span data-ttu-id="b74a1-141">Pokud chcete vyhledat prvek, kde došlo k chybě nebo upozornění, poklepejte na chybu nebo upozornění.</span><span class="sxs-lookup"><span data-stu-id="b74a1-141">To find the element where an error or warning occurred, double-click the error or warning message.</span></span> <span data-ttu-id="b74a1-142">Předtím, než je možné aktivovat workflow, musí být vyřešeny všechny chyby a upozornění.</span><span class="sxs-lookup"><span data-stu-id="b74a1-142">You must resolve all errors and warnings before you can make the workflow active.</span></span>

## <a name="save-and-activate-the-workflow"></a><span data-ttu-id="b74a1-143">Uložení a aktivace workflowu</span><span class="sxs-lookup"><span data-stu-id="b74a1-143">Save and activate the workflow</span></span>

<span data-ttu-id="b74a1-144">Až budete připraveni uložit a aktivovat workflow, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="b74a1-144">When you're ready to save and activate the workflow, follow these steps.</span></span>

1. <span data-ttu-id="b74a1-145">Kliknutím na tlačítko **Uložit a zavřít** zavřete editor workflowu a otevřete formulář **Uložit workflow**.</span><span class="sxs-lookup"><span data-stu-id="b74a1-145">Click **Save and close** to close the workflow editor and open the **Save workflow** page.</span></span>
2. <span data-ttu-id="b74a1-146">Zadejte komentáře ke změnám provedeným v daném workflowu a potom klikněte na **OK**.</span><span class="sxs-lookup"><span data-stu-id="b74a1-146">Enter comments about the changes that you've made to the workflow, and then click **OK**.</span></span>
3. <span data-ttu-id="b74a1-147">Pokud byly vyřešeny všechny chyby a upozornění, zobrazí se stránka **Aktivovat workflow**.</span><span class="sxs-lookup"><span data-stu-id="b74a1-147">If all errors and warnings have been resolved, the **Activate workflow** page appears.</span></span> <span data-ttu-id="b74a1-148">Vyberte některou z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="b74a1-148">Select one of the following options:</span></span>

    - <span data-ttu-id="b74a1-149">Pokud chcete aktivovat tuto verzi workflowu, klepněte na tlačítko **Aktivovat novou verzi**.</span><span class="sxs-lookup"><span data-stu-id="b74a1-149">To activate this version of the workflow, click **Activate the new version**.</span></span> <span data-ttu-id="b74a1-150">Když je workflow aktivní, uživatelé do něj mohou odesílat dokumenty ke zpracování a schválení.</span><span class="sxs-lookup"><span data-stu-id="b74a1-150">When a workflow is active, users can submit documents to it for processing.</span></span>
    - <span data-ttu-id="b74a1-151">Pokud nechcete tuto verzi aktivovat, klepněte na tlačítko **Neaktivovat novou verzi**.</span><span class="sxs-lookup"><span data-stu-id="b74a1-151">If you don't want to activate this version, click **Do not activate the new version**.</span></span> <span data-ttu-id="b74a1-152">Workflow můžete aktivovat později.</span><span class="sxs-lookup"><span data-stu-id="b74a1-152">You can activate the workflow later.</span></span>
