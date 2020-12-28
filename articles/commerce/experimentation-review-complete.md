---
title: Povýšení varianty a dokončení experimentu
description: Toto téma popisuje, jak povýšit úspěšnou variantu a dokončit experiment v Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
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
ms.openlocfilehash: c7da601323663d4c1ea76f7cad7bdab8e7632d1c
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/22/2020
ms.locfileid: "4410926"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="1251b-103">Povýšení varianty a dokončení experimentu</span><span class="sxs-lookup"><span data-stu-id="1251b-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="1251b-104">Toto téma popisuje, jak můžete povýšit variantu, která ve vašem experimentu přinesla nejlepší výsledky, a jak experiment dokončit.</span><span class="sxs-lookup"><span data-stu-id="1251b-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="1251b-105">Následující schéma znázorňuje všechny kroky, které zahrnuje nastavení a spuštění experimentu na webu elektronického obchodu v Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1251b-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="1251b-106">Další kroky jsou popsány v samostatných tématech.</span><span class="sxs-lookup"><span data-stu-id="1251b-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="1251b-107">[ ![Cesta uživatele experimentováním – kontrola a dokončení](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="1251b-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="1251b-108">Po [spuštění experimentu](experimentation-run-monitor.md) a shromáždění dostatečných dat, abyste mohli určit, kterou variantu chcete používat na živém webu, můžete danou variantu povýšit a experiment ukončit.</span><span class="sxs-lookup"><span data-stu-id="1251b-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="1251b-109">Povýšení varianty</span><span class="sxs-lookup"><span data-stu-id="1251b-109">Promote a variation</span></span>
<span data-ttu-id="1251b-110">Pomocí dat a analýz souvisejících s daným experimentem ve službě třetí strany se můžete rozhodnout, která varianta přinesla nejlepší výsledky.</span><span class="sxs-lookup"><span data-stu-id="1251b-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="1251b-111">Můžete jej pak propagovat nahrazením aktuálního obsahu na živém webu vítěznou variantou, aby byl dostupný všem uživatelům vašeho webu.</span><span class="sxs-lookup"><span data-stu-id="1251b-111">You can then promote it by replacing the current content on the live site with the winning variation so that it's available to all users of your website.</span></span>

<span data-ttu-id="1251b-112">Chcete-li propagovat vítěznou variantu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="1251b-112">To promote the winning variation, follow these steps.</span></span> 

1. <span data-ttu-id="1251b-113">V konfigurátoru webů Commerce vyberte **Experimenty** v levém navigačním podokně a poté vyberte experiment.</span><span class="sxs-lookup"><span data-stu-id="1251b-113">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span>
1. <span data-ttu-id="1251b-114">Na panelu nástrojů vyberte **Dokončit experiment**.</span><span class="sxs-lookup"><span data-stu-id="1251b-114">On the command bar, select **Complete experiment**.</span></span>
1. <span data-ttu-id="1251b-115">V nabídce dialogového okna **Dokončení experimentu** vyberte **Zkontrolovat data experimentu**.</span><span class="sxs-lookup"><span data-stu-id="1251b-115">In the **Complete the experiment** dialog box, select **Review the experiment data**.</span></span> <span data-ttu-id="1251b-116">Otevře se služba třetí strany, ve které můžete ověřit metriku a určit, která varianta fungovala nejlépe.</span><span class="sxs-lookup"><span data-stu-id="1251b-116">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="1251b-117">V nabídce dialogového okna **Dokončení experimentu** vyberte vítěznou variantu a pak vyberte **Další**.</span><span class="sxs-lookup"><span data-stu-id="1251b-117">In the **Complete the experiment** dialog box, select the winning variation, and then select **Next**.</span></span>
1. <span data-ttu-id="1251b-118">Otevřete službu třetí strany a experiment zastavte.</span><span class="sxs-lookup"><span data-stu-id="1251b-118">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="1251b-119">V konfigurátoru webů vyberte **Dokončit**, pokud chcete přepsat původní živou stránku a publikovat vítěznou variantu tak, aby byla dostupná všem uživatelům vašeho webu.</span><span class="sxs-lookup"><span data-stu-id="1251b-119">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="1251b-120">Pokud se rozhodnete zachovat aktuální aktivní živou stránku a žádnou variantu nepublikovat, vyberte **Znovu publikovat původní stránku**.</span><span class="sxs-lookup"><span data-stu-id="1251b-120">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="1251b-121">Odstranění experimentu</span><span class="sxs-lookup"><span data-stu-id="1251b-121">Delete your experiment</span></span>
<span data-ttu-id="1251b-122">I když odstranění dokončeného experimentu v Commerce není vyžadováno, můžete ho odstranit, abyste ušetřili místo nebo vyčistili svůj pracovní prostor.</span><span class="sxs-lookup"><span data-stu-id="1251b-122">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> 

<span data-ttu-id="1251b-123">Chcete-li odstranit experiment v nástroji pro tvorbu obchodních webů, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="1251b-123">To delete an experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="1251b-124">Vyberte **Experimenty** v levém navigačním podokně a poté vyberte experiment.</span><span class="sxs-lookup"><span data-stu-id="1251b-124">Select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="1251b-125">Pokud je experiment stále aktivní, před pokračováním zastavte tento experiment ve službě třetí strany.</span><span class="sxs-lookup"><span data-stu-id="1251b-125">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="1251b-126">Na panelu přílazů vyberte **Zrušit publikování** a odeberete obsah varianty ze živého webu.</span><span class="sxs-lookup"><span data-stu-id="1251b-126">On the command bar, select **Unpublish**  to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="1251b-127">Vyberte **Odstranit** a experiment smažete.</span><span class="sxs-lookup"><span data-stu-id="1251b-127">Select **Delete** to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="1251b-128">Předchozí krok</span><span class="sxs-lookup"><span data-stu-id="1251b-128">Previous step</span></span>
[<span data-ttu-id="1251b-129">Spuštění a monitorování experimentu</span><span class="sxs-lookup"><span data-stu-id="1251b-129">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
