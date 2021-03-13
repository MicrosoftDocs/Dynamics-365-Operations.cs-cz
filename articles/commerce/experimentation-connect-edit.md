---
title: Připojení experimentu a úpravy variant
description: Toto téma popisuje, jak připojit experiment ve službě třetí strany k Dynamics 365 Commerce a jak upravovat varianty experimentu.
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
ms.openlocfilehash: 2a33897d01dd98d446c2fb49e417abd9db9f403a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010017"
---
# <a name="connect-an-experiment-and-edit-variations"></a><span data-ttu-id="23538-103">Připojení experimentu a úpravy variant</span><span class="sxs-lookup"><span data-stu-id="23538-103">Connect an experiment and edit variations</span></span>

<span data-ttu-id="23538-104">Toto téma popisuje, jak můžete připojit experiment v Commerce a jak můžete provádět změny variant tak, aby odpovídaly vaší hypotéze.</span><span class="sxs-lookup"><span data-stu-id="23538-104">This topic describes how to connect your experiment in Commerce and make changes to your variations so that they align with your hypothesis.</span></span> 

<span data-ttu-id="23538-105">Následující schéma znázorňuje všechny kroky, které zahrnuje nastavení a spuštění experimentu na webu elektronického obchodu v Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="23538-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="23538-106">Další kroky jsou popsány v samostatných tématech.</span><span class="sxs-lookup"><span data-stu-id="23538-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="23538-107">[ ![Cesta uživatele experimentováním – připojení a úpravy](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="23538-107">[ ![Experimentation user journey - Connect & Edit](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span></span>

<span data-ttu-id="23538-108">Po [nastavení experimentu](experimentation-setup.md) ve službě třetí strany připojíte experiment v Dynamics 365 Commerce a upravíte varianty experimentu.</span><span class="sxs-lookup"><span data-stu-id="23538-108">After you've [set up your experiment](experimentation-setup.md) in a third-party service, you'll connect the experiment in Dynamics 365 Commerce and edit the experiment variations.</span></span>

## <a name="planning-considerations"></a><span data-ttu-id="23538-109">Poznámky k plánování</span><span class="sxs-lookup"><span data-stu-id="23538-109">Planning considerations</span></span>

<span data-ttu-id="23538-110">Před připojením experimentu v Commerce budete muset udělat několik rozhodnutí, která ovlivní způsob, jakým bude Commerce spravovat váš obsah.</span><span class="sxs-lookup"><span data-stu-id="23538-110">Before you connect your experiment in Commerce, you'll need to make some decisions that impact the way Commerce manages your content.</span></span>

### <a name="determine-the-scope-of-your-experiment"></a><span data-ttu-id="23538-111">Určení rozsahu experimentu</span><span class="sxs-lookup"><span data-stu-id="23538-111">Determine the scope of your experiment</span></span>
<span data-ttu-id="23538-112">Když připojíte experiment, budete vyzváni k definování rozsahu experimentu.</span><span class="sxs-lookup"><span data-stu-id="23538-112">When you connect an experiment, you are prompted to define the scope of the experiment.</span></span> <span data-ttu-id="23538-113">Experimenty jsou definovány s **částečným** rozsahem nebo s **úplným** rozsahem.</span><span class="sxs-lookup"><span data-stu-id="23538-113">Experiments are defined as **partial** scope or **entire** scope.</span></span>
- <span data-ttu-id="23538-114">Zvolte **částečný** rozsah, pokud chcete experiment provádět na konkrétní části stránky.</span><span class="sxs-lookup"><span data-stu-id="23538-114">Choose **partial** if you want to conduct an experiment on a specific portion of a page.</span></span> <span data-ttu-id="23538-115">Pokud vyberete tuto možnost, musíte určit, které moduly jsou v experimentu zahrnuty.</span><span class="sxs-lookup"><span data-stu-id="23538-115">If you select this option, you must identify which modules are included in the experiment.</span></span> <span data-ttu-id="23538-116">Změny provedené v částech výchozí stránky nebo fragmentu, které nesouvisí s experimentem, se automaticky synchronizují ve všech variantách.</span><span class="sxs-lookup"><span data-stu-id="23538-116">Changes that are made to parts of the default page or fragment that aren't related to the experiment are automatically synchronized across variations.</span></span>
- <span data-ttu-id="23538-117">Zvolte **úplný** rozsah, pokud chcete experiment provádět na celé stránce nebo v celém fragmentu.</span><span class="sxs-lookup"><span data-stu-id="23538-117">Choose **entire** if you want to conduct an experiment on an entire page or fragment.</span></span> <span data-ttu-id="23538-118">Budou vytvořeny samostatné kopie výchozí stránky nebo fragmentu.</span><span class="sxs-lookup"><span data-stu-id="23538-118">Separate copies of the default page or fragment are created.</span></span> <span data-ttu-id="23538-119">Nebudete muset vybírat, které moduly jsou v experimentu zahrnuty, protože je možné měnit celou editační plochu.</span><span class="sxs-lookup"><span data-stu-id="23538-119">You won't have to select which modules are included in the experiment because the whole editing surface is available to change.</span></span> <span data-ttu-id="23538-120">Podle potřeby můžete přidávat nebo odstraňovat moduly a měnit jejich pořadí.</span><span class="sxs-lookup"><span data-stu-id="23538-120">You can add, delete, or re-order modules as needed.</span></span> <span data-ttu-id="23538-121">Pokud jsou však provedeny nějaké změny na výchozí stránce nebo fragmentu, ke kterým je experiment přidružen, musí být tyto změny ručně synchronizovány ve všech variantách.</span><span class="sxs-lookup"><span data-stu-id="23538-121">However, if any changes are made to the default page or fragment that the experiment is associated with, those changes have to be manually synchronized across all variations.</span></span>

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> <span data-ttu-id="23538-122">Pokud experiment přidružíte ke stránce, která používá rozložení, můžete zvolit pouze **úplný** rozsah experimentu.</span><span class="sxs-lookup"><span data-stu-id="23538-122">If you associate your experiment with a page that uses a layout, you can only scope the experiment as **entire**.</span></span>

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a><span data-ttu-id="23538-123">Rozhodnutí, jestli chcete naplánovat, kdy bude experiment publikován</span><span class="sxs-lookup"><span data-stu-id="23538-123">Decide if you want to schedule when your experiment is published</span></span>
<span data-ttu-id="23538-124">Pokud chcete naplánovat, kdy bude váš experiment publikován na živém webu, ujistěte se, že obsah, který chcete k experimentu přidružit, je dostupný ve skupině publikování *před* připojením experimentu.</span><span class="sxs-lookup"><span data-stu-id="23538-124">If you want to schedule when your experiment is published to your live site, make sure the content you want to associate with the experiment is available in a publish group *before* you connect the experiment.</span></span> 

<span data-ttu-id="23538-125">Další informace o skupinách publikování najdete v tématu [Práce se skupinami publikování](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="23538-125">For more information about publish groups, refer to [Work with publish groups](publish-groups.md).</span></span>


## <a name="connect-your-experiment"></a><span data-ttu-id="23538-126">Připojení experimentu</span><span class="sxs-lookup"><span data-stu-id="23538-126">Connect your experiment</span></span>
<span data-ttu-id="23538-127">Když budete chtít experiment připojit, spustíte průvodce **Připojení experimentu**.</span><span class="sxs-lookup"><span data-stu-id="23538-127">To connect your experiment, you'll launch the **Connect experiment** wizard.</span></span> <span data-ttu-id="23538-128">Průvodce vás provede kroky potřebnými k připojení experimentu.</span><span class="sxs-lookup"><span data-stu-id="23538-128">The wizard walks you through the steps required to connect your experiment.</span></span> <span data-ttu-id="23538-129">Po dokončení průvodce je váš experiment připojen a jsou vytvořeny varianty, které je možné upravovat.</span><span class="sxs-lookup"><span data-stu-id="23538-129">When you complete the wizard, your experiment is connected and variations are created and ready to be edited.</span></span>

<span data-ttu-id="23538-130">Chcete-li zahájit připojení experimentu v nástroji pro tvorbu obchodních webů, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="23538-130">To get started connecting your experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="23538-131">Chcete-li spustit průvodce **Připojte experiment**, vyberte **Experimenty** v levém navigačním podokně a poté vyberte **Připojit**.</span><span class="sxs-lookup"><span data-stu-id="23538-131">To launch the **Connect experiment** wizard, select **Experiments** in the left navigation pane, and then select **Connect**.</span></span> <span data-ttu-id="23538-132">Alternativně můžete průvodce otevřít ze editoru stránky nebo fragmentu jeho úpravou a výběrem **Připojte experiment** na panelu příkazů.</span><span class="sxs-lookup"><span data-stu-id="23538-132">Alternatively, you can access the wizard from a page or fragment editor by editing it and selecting **Connect experiment** on the command bar.</span></span>

    > [!NOTE]
    > <span data-ttu-id="23538-133">Stránka může být připojená vždy jen k jednomu experimentu.</span><span class="sxs-lookup"><span data-stu-id="23538-133">A page can only be connected to one experiment at a time.</span></span> <span data-ttu-id="23538-134">Když budete chtít stránku připojit k jinému experimentu, nejprve odstraňte experiment, ke kterému je stránka aktuálně připojená.</span><span class="sxs-lookup"><span data-stu-id="23538-134">To connect a page to a different experiment, first delete the experiment that the page is currently connected to.</span></span>

1. <span data-ttu-id="23538-135">Zvolte stránku nebo fragment, pro které chcete experiment spustit.</span><span class="sxs-lookup"><span data-stu-id="23538-135">Choose the page or fragment you want to run your experiment on.</span></span>
1. <span data-ttu-id="23538-136">Nastavte rozsah experimentování na **částečný** nebo **úplný** na základě toho, co jste zvolili v části [Určení rozsahu experimentu](#determine-the-scope-of-your-experiment) výše.</span><span class="sxs-lookup"><span data-stu-id="23538-136">Set the experimentation scope to **partial** or **entire**, based on the choice you made in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>
    > [!NOTE]
    > <span data-ttu-id="23538-137">Příznak funkce **Experimentovat na stránkách nebo ve fragmentech** musí být povolen, pokud chcete experimentovat na celé stránce nebo v celém fragmentu.</span><span class="sxs-lookup"><span data-stu-id="23538-137">The **Experiment on pages or fragments** feature flag must be enabled if you want to experiment on a full page or fragment.</span></span> <span data-ttu-id="23538-138">Další informace najdete v tématu [Experimentování Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="23538-138">Refer to the [Experimentation in Dynamics 365 Commerce](experimentation-overview.md) topic for more information.</span></span>
    
1. <span data-ttu-id="23538-139">V posledním kroku průvodce vyberte **Vygenerovat varianty a ukončit průvodce**.</span><span class="sxs-lookup"><span data-stu-id="23538-139">In the final step of the wizard, select **Generate variations and exit wizard**.</span></span> <span data-ttu-id="23538-140">Pro experiment se vytvoří varianty.</span><span class="sxs-lookup"><span data-stu-id="23538-140">Variations are created for the experiment.</span></span> 

## <a name="edit-your-variations"></a><span data-ttu-id="23538-141">Úpravy variant</span><span class="sxs-lookup"><span data-stu-id="23538-141">Edit your variations</span></span>
<span data-ttu-id="23538-142">Po ukončení průvodce se automaticky vytvoří varianty.</span><span class="sxs-lookup"><span data-stu-id="23538-142">When you exit the wizard, variations are created for you.</span></span> 

<span data-ttu-id="23538-143">Pak můžete varianty upravovat tak, aby odrážely možnosti, které potřebujete ověřit v hypotéze experimentu.</span><span class="sxs-lookup"><span data-stu-id="23538-143">Next, you'll edit the variations so they reflect the choices that you need to verify in the experiment hypothesis.</span></span> <span data-ttu-id="23538-144">Vyberte jeden z následujících postupů, který odpovídá rozsahu, který jste pro svůj experiment vybrali v části [Určení rozsahu experimentu](#determine-the-scope-of-your-experiment) výše.</span><span class="sxs-lookup"><span data-stu-id="23538-144">Choose one of following procedures that corresponds to the scope you chose for your experiment in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>

### <a name="edit-variations-for-experiments-with-partial-scope"></a><span data-ttu-id="23538-145">Úprava variant experimentů s částečným rozsahem</span><span class="sxs-lookup"><span data-stu-id="23538-145">Edit variations for experiments with partial scope</span></span>
<span data-ttu-id="23538-146">Podle těchto kroků postupujte, pokud jste rozsah experimentu definovali jako **částečný** v průvodci **Připojení experimentu**.</span><span class="sxs-lookup"><span data-stu-id="23538-146">Follow these steps if you defined the scope of your experiment as **partial** in the **Connect experiment** wizard.</span></span>

1. <span data-ttu-id="23538-147">V zobrazení editoru použijte rozevírací nabídku variant pod panelem příkazů a upravte každou variantu podle vaší původní hypotézy.</span><span class="sxs-lookup"><span data-stu-id="23538-147">In editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> <span data-ttu-id="23538-148">Můžete také vytvořit kontrolní nebo základní variantu tak, že jednu z variant ponecháte beze změny.</span><span class="sxs-lookup"><span data-stu-id="23538-148">You may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>
1. <span data-ttu-id="23538-149">Vyberte modul, u kterého má být experiment spuštěn, vyberte tři tečky (...) a pak vyberte **Přidat do experimentu**.</span><span class="sxs-lookup"><span data-stu-id="23538-149">Select the module to be experimented on, select the ellipsis (...), and then select **Add to experiment**.</span></span>

### <a name="edit-variations-for-experiments-with-entire-scope"></a><span data-ttu-id="23538-150">Úprava variant experimentů s úplným rozsahem</span><span class="sxs-lookup"><span data-stu-id="23538-150">Edit variations for experiments with entire scope</span></span>
<span data-ttu-id="23538-151">Pokud jste rozsah experimentu definovali jako **úplný** v průvodci **Připojení experimentu**, pak v zobrazení editoru použijte rozevírací nabídku variant pod panelem příkazů a upravte každou variantu podle vaší původní hypotézy.</span><span class="sxs-lookup"><span data-stu-id="23538-151">If you defined the scope of your experiment as **entire** in the **Connect experiment** wizard, while in editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> 

> [!NOTE]
> <span data-ttu-id="23538-152">V obou případech můžete také vytvořit kontrolní nebo základní variantu tak, že jednu z variant ponecháte beze změny.</span><span class="sxs-lookup"><span data-stu-id="23538-152">In either case, you may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>

## <a name="previous-step"></a><span data-ttu-id="23538-153">Předchozí krok</span><span class="sxs-lookup"><span data-stu-id="23538-153">Previous step</span></span>
[<span data-ttu-id="23538-154">Nastavení experimentu</span><span class="sxs-lookup"><span data-stu-id="23538-154">Set up an experiment</span></span>](experimentation-setup.md) 


## <a name="next-step"></a><span data-ttu-id="23538-155">Další krok</span><span class="sxs-lookup"><span data-stu-id="23538-155">Next step</span></span>
[<span data-ttu-id="23538-156">Náhled a publikování experimentu</span><span class="sxs-lookup"><span data-stu-id="23538-156">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)
