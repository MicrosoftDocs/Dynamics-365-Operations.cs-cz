---
title: Spuštění a monitorování experimentu
description: Toto téma popisuje, jak spustit a monitorovat experiment ve službě třetí strany. Popisuje také, jak můžete provádět změny variant po spuštění experimentu.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 956a9168ed7bf9282d9eeec39587d8e1f2d1856c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224875"
---
# <a name="run-and-monitor-an-experiment"></a><span data-ttu-id="431f3-104">Spuštění a monitorování experimentu</span><span class="sxs-lookup"><span data-stu-id="431f3-104">Run and monitor an experiment</span></span>

<span data-ttu-id="431f3-105">Toto téma popisuje, jak můžete spustit a monitorovat experiment v aplikaci třetí strany a jak můžete v případě potřeby měnit varianty.</span><span class="sxs-lookup"><span data-stu-id="431f3-105">This topic describes how to run and monitor your experiment in a third-party app, and change variations if needed.</span></span> <span data-ttu-id="431f3-106">Než provedete kroky v tomto tématu, budete nejprve muset [publikovat](experimentation-preview-publish.md) váš experiment v Commerce.</span><span class="sxs-lookup"><span data-stu-id="431f3-106">Before you complete the steps in this topic, you'll first need to [publish](experimentation-preview-publish.md) your experiment in Commerce.</span></span> 

<span data-ttu-id="431f3-107">Následující schéma znázorňuje všechny kroky, které zahrnuje nastavení a spuštění experimentu na webu elektronického obchodu v Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="431f3-107">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="431f3-108">Další kroky jsou popsány v samostatných tématech.</span><span class="sxs-lookup"><span data-stu-id="431f3-108">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="431f3-109">[ ![Cesta uživatele experimentováním – spuštění a monitorování](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="431f3-109">[ ![Experimentation user journey - Run & Monitor](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span></span>

<span data-ttu-id="431f3-110">Jakmile své varianty publikujete, jsou provedeny všechny kroky, které musíte provést v Commerce, abyste mohli experiment spustit.</span><span class="sxs-lookup"><span data-stu-id="431f3-110">After you publish your variations, all of the steps you need to do in Commerce to run your experiment are complete.</span></span> <span data-ttu-id="431f3-111">Dalším krokem je určení, která varianta se má zobrazit jednotlivým uživatelům, když budou požadovat zobrazení stránky.</span><span class="sxs-lookup"><span data-stu-id="431f3-111">The next step is determining which variation to show to each user when they request a page.</span></span> <span data-ttu-id="431f3-112">Toto rozhodnutí dělá služba třetí strany, ale nejprve musíte v této službě experiment aktivovat.</span><span class="sxs-lookup"><span data-stu-id="431f3-112">The third-party service makes that determination, but first you have to activate the experiment within the service.</span></span> <span data-ttu-id="431f3-113">Vzhledem k tomu, že kroky pro aktivaci experimentu se u jednotlivých služeb liší, budete muset postupovat podle pokynů vaší služby nebo poskytovatele.</span><span class="sxs-lookup"><span data-stu-id="431f3-113">Since the steps for activating an experiment vary from service to service, you'll need to follow the instructions included with your service or provider.</span></span> <span data-ttu-id="431f3-114">Pokud experiment není aktivován, uvidí uživatelé pouze výchozí verzi stránky (nezobrazí se žádné varianty).</span><span class="sxs-lookup"><span data-stu-id="431f3-114">If the experiment is not activated, users will only see the default version of the page (no variations will be displayed).</span></span>

<span data-ttu-id="431f3-115">Experiment budete muset nechat běžet dostatečně dlouho, aby se shromáždila data pro statisticky platné výsledky.</span><span class="sxs-lookup"><span data-stu-id="431f3-115">You'll need to keep the experiment running long enough to gather data for statistically valid results.</span></span> <span data-ttu-id="431f3-116">Pomocí služby třetí strany můžete během experimentu monitorovat data experimentu a analýzu.</span><span class="sxs-lookup"><span data-stu-id="431f3-116">Use the third-party service to monitor the experiment-related data and analytics while the experiment is running.</span></span>

## <a name="adjust-your-variations"></a><span data-ttu-id="431f3-117">Úprava variant</span><span class="sxs-lookup"><span data-stu-id="431f3-117">Adjust your variations</span></span>
<span data-ttu-id="431f3-118">Pokud budete z nějakého důvodu potřebovat své varianty upravit, postupujte podle pokynů níže.</span><span class="sxs-lookup"><span data-stu-id="431f3-118">If for any reason you need to modify your variations, follow the steps below.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="431f3-119">Pokud provedete změny v živém experimentu v Commerce nebo ve službě třetí strany, může to významně ovlivnit výsledky.</span><span class="sxs-lookup"><span data-stu-id="431f3-119">If you make changes to a live experiment in Commerce or the third-party service, your results may be significantly impacted.</span></span> <span data-ttu-id="431f3-120">V případě zásadních změn zvažte, jestli není lepší nechat experiment proběhnout a pak vytvořit nový experiment.</span><span class="sxs-lookup"><span data-stu-id="431f3-120">Consider letting the experiment run its course and then creating a new experiment for major changes.</span></span>

1. <span data-ttu-id="431f3-121">V konfigurátoru webů Commerce vyberte **Experimenty** v levém navigačním podokně a poté vyberte experiment.</span><span class="sxs-lookup"><span data-stu-id="431f3-121">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
1. <span data-ttu-id="431f3-122">V rozevírací nabídce vyberte variantu, kterou chcete aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="431f3-122">Select the variation you want to update from the drop-down menu.</span></span>
1. <span data-ttu-id="431f3-123">Proveďte libovolné potřebné změny, pak zobrazte náhled a varianty publikujte.</span><span class="sxs-lookup"><span data-stu-id="431f3-123">Make any needed changes, and then preview and publish the variations.</span></span> <span data-ttu-id="431f3-124">Další informace najdete v tématu [Náhled a publikování experimentu](experimentation-preview-publish.md).</span><span class="sxs-lookup"><span data-stu-id="431f3-124">For more information, see [Preview and publish an experiment](experimentation-preview-publish.md).</span></span>
1. <span data-ttu-id="431f3-125">Přejděte do služby třetí strany a proveďte všechny změny související s nastavením experimentu.</span><span class="sxs-lookup"><span data-stu-id="431f3-125">Go to the third-party service to make any experiment setup-related changes.</span></span>
    
## <a name="previous-step"></a><span data-ttu-id="431f3-126">Předchozí krok</span><span class="sxs-lookup"><span data-stu-id="431f3-126">Previous step</span></span>
[<span data-ttu-id="431f3-127">Náhled a publikování experimentu</span><span class="sxs-lookup"><span data-stu-id="431f3-127">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)

## <a name="next-step"></a><span data-ttu-id="431f3-128">Další krok</span><span class="sxs-lookup"><span data-stu-id="431f3-128">Next step</span></span>
[<span data-ttu-id="431f3-129">Povýšení varianty a dokončení experimentu</span><span class="sxs-lookup"><span data-stu-id="431f3-129">Promote a variation and complete an experiment</span></span>](experimentation-review-complete.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]