---
title: Náhled a publikování experimentu
description: Toto téma popisuje, jak zobrazit náhled a publikovat experiment z Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 91e2e4840a2d53f195d881279050b6415d48b070
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930157"
---
# <a name="preview-and-publish-an-experiment"></a><span data-ttu-id="f3e28-103">Náhled a publikování experimentu</span><span class="sxs-lookup"><span data-stu-id="f3e28-103">Preview and publish an experiment</span></span>

<span data-ttu-id="f3e28-104">Toto téma popisuje, jak můžete zobrazit náhled a publikovat experiment v Dynamics 365 Commerce poté, co jste [připojili experiment a upravili varianty](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="f3e28-104">This topic describes how to preview and publish your experiment in Dynamics 365 Commerce after you've [connected your experiment and edited your variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="f3e28-105">Následující schéma znázorňuje všechny kroky, které zahrnuje nastavení a spuštění experimentu na webu elektronického obchodu v Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f3e28-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="f3e28-106">Další kroky jsou popsány v samostatných tématech.</span><span class="sxs-lookup"><span data-stu-id="f3e28-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="f3e28-107">[ ![Cesta uživatele experimentováním – náhled a publikování](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="f3e28-107">[ ![Experimentation user journey - Preview & Publish](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span></span>

## <a name="preview-your-experiment-variations"></a><span data-ttu-id="f3e28-108">Náhled variant experimentu</span><span class="sxs-lookup"><span data-stu-id="f3e28-108">Preview your experiment variations</span></span>
<span data-ttu-id="f3e28-109">Můžete si prohlédnout náhled svých variant a dál je upravovat, dokud nebudou vypadat tak, jak chcete.</span><span class="sxs-lookup"><span data-stu-id="f3e28-109">You can preview your variations and continue editing them until they look the way you want them to.</span></span>

1. <span data-ttu-id="f3e28-110">V konfigurátoru webů vyberte v rozevírací nabídce variant pod panelem příkazů obsah, jehož náhled chcete zobrazit.</span><span class="sxs-lookup"><span data-stu-id="f3e28-110">In site builder, use the variations drop-down menu below the command bar to select the content you want to preview.</span></span> 
1. <span data-ttu-id="f3e28-111">Na horním panelu vyberte **Náhled** .</span><span class="sxs-lookup"><span data-stu-id="f3e28-111">Select **Preview** in the top bar.</span></span> <span data-ttu-id="f3e28-112">Zobrazí se náhled, jak bude obsah po publikování vypadat.</span><span class="sxs-lookup"><span data-stu-id="f3e28-112">A preview of what the content will look like when it's published is displayed.</span></span>
1. <span data-ttu-id="f3e28-113">Když budete chtít zobrazit jinou variantu, vyberte ji z rozevíracího seznamu variant a pak znovu vyberte **Náhled** .</span><span class="sxs-lookup"><span data-stu-id="f3e28-113">To preview a different variation, select it from the variation drop-down and select **Preview** again.</span></span>

## <a name="publish-your-experiment"></a><span data-ttu-id="f3e28-114">Publikování experimentu</span><span class="sxs-lookup"><span data-stu-id="f3e28-114">Publish your experiment</span></span>
<span data-ttu-id="f3e28-115">Pokud k publikování experimentů na živý web nepoužíváte skupinu publikování a chcete experiment publikovat okamžitě, vyberte **Publikovat** na panelu příkazů.</span><span class="sxs-lookup"><span data-stu-id="f3e28-115">If you aren't using a publish group to schedule when your experiment goes live and you want to publish immediately, select **Publish** in the command bar.</span></span> <span data-ttu-id="f3e28-116">Budou publikovány všechny varianty, které patří k danému experimentu.</span><span class="sxs-lookup"><span data-stu-id="f3e28-116">All variations that belong to the experiment will be published.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="f3e28-117">Pokud má stránka nepublikovanou adresu URL, musíte nejprve publikovat adresu URL, jinak nebude pro uživatele vašeho webu viditelná.</span><span class="sxs-lookup"><span data-stu-id="f3e28-117">If the page has an unpublished URL, you must first publish the URL or it won't be visible to your website users.</span></span> <span data-ttu-id="f3e28-118">Podrobnosti najdete v tématu [Uložení, náhled a publikování stránky](save-preview-publish-page.md).</span><span class="sxs-lookup"><span data-stu-id="f3e28-118">For details, see [Save, preview, and publish a page](save-preview-publish-page.md).</span></span>
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a><span data-ttu-id="f3e28-119">Naplánování publikování experimentu na živý web pomocí skupin publikování</span><span class="sxs-lookup"><span data-stu-id="f3e28-119">Use publish groups to schedule when your experiment goes live</span></span>
<span data-ttu-id="f3e28-120">Publikování variant vytvořených v konfigurátoru webů můžete naplánovat pomocí skupiny publikování.</span><span class="sxs-lookup"><span data-stu-id="f3e28-120">Variations created in site builder can be scheduled for publishing by using a publish group.</span></span> <span data-ttu-id="f3e28-121">V rámci skupiny publikování můžete připojit stránku nebo fragment ke svému experimentu tak, že přejdete na kartu **Experimenty** nebo **Stránky** nebo **Fragmenty** . Další informace najdete v tématu [Připojení experimentu a úpravy variant](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="f3e28-121">Within a publish group, you can connect a page or fragment to your experiment by going to the **Experiments** tab or the **Pages** or **Fragments** tab. For more information, see [Connect an experiment and edit variations](experimentation-connect-edit.md) topic.</span></span> <span data-ttu-id="f3e28-122">Informace o skupinách publikování najdete v tématu [Práce se skupinami publikování](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="f3e28-122">For information about publish groups, see [Work with publish groups](publish-groups.md).</span></span>

<span data-ttu-id="f3e28-123">Při používání skupin publikování s experimenty je třeba brát v úvahu několik důležitých aspektů.</span><span class="sxs-lookup"><span data-stu-id="f3e28-123">When using publish groups with experiments, there are some important considerations to be aware of.</span></span>
- <span data-ttu-id="f3e28-124">Když do skupiny publikování přidáte stránku nebo fragment se spuštěným experimentem, bude ve skupině publikování tento experiment ze stránky nebo fragmentu odebrán.</span><span class="sxs-lookup"><span data-stu-id="f3e28-124">When you add a page or fragment that has an experiment running on it to a publish group, the experiment will be removed from the page or fragment in the publish group.</span></span>
- <span data-ttu-id="f3e28-125">Experimenty, které jsou připojeny ke stránkám na živém webu, nejsou dostupné pro stránky ve skupinách publikování a naopak.</span><span class="sxs-lookup"><span data-stu-id="f3e28-125">Experiments that are connected to pages in a live site aren't available to pages within publish groups and vice-versa.</span></span> <span data-ttu-id="f3e28-126">Podobně platí, že stránky, na kterých jsou spuštěné experimenty na živém webu, nejsou dostupné jiným experimentům ve skupinách publikování a naopak.</span><span class="sxs-lookup"><span data-stu-id="f3e28-126">Similarly, pages that have experiments running on them in a live site aren't available to other experiments in publish groups and vice versa.</span></span>
- <span data-ttu-id="f3e28-127">Při publikování nebo při plánování skupiny publikování je publikován veškerý obsah ve skupině publikování bez ohledu na to, jestli je k této skupině publikování přidružený nějaký experiment.</span><span class="sxs-lookup"><span data-stu-id="f3e28-127">When you publish or schedule a publish group, all content in the publish group is published, regardless of whether there's an experiment associated with the publish group.</span></span>
- <span data-ttu-id="f3e28-128">Protože skupina publikování přetrvává i poté, co byla publikována na živém webu, experimenty ve skupině pro publikování přetrvávají také.</span><span class="sxs-lookup"><span data-stu-id="f3e28-128">Because a publish group continues to persist after it's been published to a live site, experiments in the publish group will also persist.</span></span> <span data-ttu-id="f3e28-129">Proto nebudete moct přidružit další experimenty ke stejné stránce nebo fragmentu.</span><span class="sxs-lookup"><span data-stu-id="f3e28-129">Therefore, you won't be able to associate other experiments with the same page or fragment.</span></span> <span data-ttu-id="f3e28-130">Chcete-li se tomuto omezení vyhnout, odstraňte všechny skupiny pro publikování s přetrvávajícími experimenty.</span><span class="sxs-lookup"><span data-stu-id="f3e28-130">To avoid this limitation, delete any publish groups with persisting experiments.</span></span> <span data-ttu-id="f3e28-131">Podobně, pokud chcete odstranit experiment na živém webu, který existuje také ve skupině publikování, nejprve ho ze skupiny publikování odstraňte.</span><span class="sxs-lookup"><span data-stu-id="f3e28-131">Similarly, if you want to delete an experiment in a live site that also exists in a publish group, delete it from the publish group first.</span></span>

## <a name="previous-step"></a><span data-ttu-id="f3e28-132">Předchozí krok</span><span class="sxs-lookup"><span data-stu-id="f3e28-132">Previous step</span></span>
[<span data-ttu-id="f3e28-133">Připojení a úpravy experimentu</span><span class="sxs-lookup"><span data-stu-id="f3e28-133">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

## <a name="next-step"></a><span data-ttu-id="f3e28-134">Další krok</span><span class="sxs-lookup"><span data-stu-id="f3e28-134">Next step</span></span>
[<span data-ttu-id="f3e28-135">Spuštění a monitorování experimentu</span><span class="sxs-lookup"><span data-stu-id="f3e28-135">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
