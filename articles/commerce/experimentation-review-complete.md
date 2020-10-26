---
title: Povýšení varianty a dokončení experimentu
description: Toto téma popisuje, jak povýšit úspěšnou variantu a dokončit experiment v Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
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
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930152"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="5ba6e-103">Povýšení varianty a dokončení experimentu</span><span class="sxs-lookup"><span data-stu-id="5ba6e-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="5ba6e-104">Toto téma popisuje, jak můžete povýšit variantu, která ve vašem experimentu přinesla nejlepší výsledky, a jak experiment dokončit.</span><span class="sxs-lookup"><span data-stu-id="5ba6e-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="5ba6e-105">Následující schéma znázorňuje všechny kroky, které zahrnuje nastavení a spuštění experimentu na webu elektronického obchodu v Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5ba6e-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="5ba6e-106">Další kroky jsou popsány v samostatných tématech.</span><span class="sxs-lookup"><span data-stu-id="5ba6e-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="5ba6e-107">[ ![Cesta uživatele experimentováním – kontrola a dokončení](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="5ba6e-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="5ba6e-108">Po [spuštění experimentu](experimentation-run-monitor.md) a shromáždění dostatečných dat, abyste mohli určit, kterou variantu chcete používat na živém webu, můžete danou variantu povýšit a experiment ukončit.</span><span class="sxs-lookup"><span data-stu-id="5ba6e-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="5ba6e-109">Povýšení varianty</span><span class="sxs-lookup"><span data-stu-id="5ba6e-109">Promote a variation</span></span>
<span data-ttu-id="5ba6e-110">Pomocí dat a analýz souvisejících s daným experimentem ve službě třetí strany se můžete rozhodnout, která varianta přinesla nejlepší výsledky.</span><span class="sxs-lookup"><span data-stu-id="5ba6e-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="5ba6e-111">Když budete chtít nahradit aktuální obsah na živém webu vítěznou variantou, aby byl dostupný všem uživatelům vašeho webu, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="5ba6e-111">To replace the current content on the live site with the winning variation so that it's available to all users of your website, do the following.</span></span> 

1. <span data-ttu-id="5ba6e-112">Přejděte na kartu **Experimenty** v konfigurátoru webů a vyberte příslušný experiment.</span><span class="sxs-lookup"><span data-stu-id="5ba6e-112">Go to the **Experiments** tab in site builder and select the experiment.</span></span>
1. <span data-ttu-id="5ba6e-113">Na horním panelu vyberte **Dokončit experiment** .</span><span class="sxs-lookup"><span data-stu-id="5ba6e-113">Select **Complete experiment** on the top bar.</span></span>
1. <span data-ttu-id="5ba6e-114">V nabídce dialogového okna **Dokončení experimentu** vyberte **Zkontrolovat data experimentu** .</span><span class="sxs-lookup"><span data-stu-id="5ba6e-114">In the **Complete the experiment** dialog menu, select **Review the experiment data** .</span></span> <span data-ttu-id="5ba6e-115">Otevře se služba třetí strany, ve které můžete ověřit metriku a určit, která varianta fungovala nejlépe.</span><span class="sxs-lookup"><span data-stu-id="5ba6e-115">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="5ba6e-116">V nabídce dialogového okna **Dokončení experimentu** v konfigurátoru webů vyberte vítěznou variantu a pak vyberte **Další** .</span><span class="sxs-lookup"><span data-stu-id="5ba6e-116">In the **Complete the experiment** dialog menu in site builder, select the winning variation and then select **Next** .</span></span>
1. <span data-ttu-id="5ba6e-117">Otevřete službu třetí strany a experiment zastavte.</span><span class="sxs-lookup"><span data-stu-id="5ba6e-117">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="5ba6e-118">V konfigurátoru webů vyberte **Dokončit** , pokud chcete přepsat původní živou stránku a publikovat vítěznou variantu tak, aby byla dostupná všem uživatelům vašeho webu.</span><span class="sxs-lookup"><span data-stu-id="5ba6e-118">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="5ba6e-119">Pokud se rozhodnete zachovat aktuální aktivní živou stránku a žádnou variantu nepublikovat, vyberte **Znovu publikovat původní stránku** .</span><span class="sxs-lookup"><span data-stu-id="5ba6e-119">If you choose to keep the current live page and not publish a variation, select **Republish the original page** .</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="5ba6e-120">Odstranění experimentu</span><span class="sxs-lookup"><span data-stu-id="5ba6e-120">Delete your experiment</span></span>
<span data-ttu-id="5ba6e-121">I když odstranění dokončeného experimentu v Commerce není vyžadováno, můžete ho odstranit, abyste ušetřili místo nebo vyčistili svůj pracovní prostor.</span><span class="sxs-lookup"><span data-stu-id="5ba6e-121">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> <span data-ttu-id="5ba6e-122">Experiment můžete odstranit následujícím postupem.</span><span class="sxs-lookup"><span data-stu-id="5ba6e-122">To delete an experiment, do the following.</span></span>

1. <span data-ttu-id="5ba6e-123">Přejděte na kartu **Experimenty** v konfigurátoru webů a vyberte příslušný experiment.</span><span class="sxs-lookup"><span data-stu-id="5ba6e-123">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="5ba6e-124">Pokud je experiment stále aktivní, před pokračováním zastavte tento experiment ve službě třetí strany.</span><span class="sxs-lookup"><span data-stu-id="5ba6e-124">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="5ba6e-125">Výběrem možnosti **Zrušit publikování** na panelu příkazů odeberete obsah varianty ze živého webu.</span><span class="sxs-lookup"><span data-stu-id="5ba6e-125">Select **Unpublish** in the command bar to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="5ba6e-126">Výběrem možnosti **Odstranit** na panelu příkazů experiment odstraníte.</span><span class="sxs-lookup"><span data-stu-id="5ba6e-126">Select **Delete** in the command bar to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="5ba6e-127">Předchozí krok</span><span class="sxs-lookup"><span data-stu-id="5ba6e-127">Previous step</span></span>
[<span data-ttu-id="5ba6e-128">Spuštění a monitorování experimentu</span><span class="sxs-lookup"><span data-stu-id="5ba6e-128">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
