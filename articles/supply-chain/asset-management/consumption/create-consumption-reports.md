---
title: Vytvoření sestav spotřeby
description: Toto téma vysvětluje, jak vytvořit sestavy spotřeby v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: eecfb101af9a91f515aab221181c54d53e358a68
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652418"
---
# <a name="create-consumption-reports"></a><span data-ttu-id="c792e-103">Vytvoření sestav spotřeby</span><span class="sxs-lookup"><span data-stu-id="c792e-103">Create consumption reports</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c792e-104">Pokud jste vytvořili a zaúčtovali registrace spotřeby na pracovních příkazech ve správě majetku, budou k dispozici dvě sestavy pro zobrazení podrobností o spotřebě.</span><span class="sxs-lookup"><span data-stu-id="c792e-104">When you've created and posted consumption registrations on work orders in Asset Management, two reports are available to display consumption details.</span></span>


## <a name="asset-consumption-report"></a><span data-ttu-id="c792e-105">Sestava spotřeby majetku</span><span class="sxs-lookup"><span data-stu-id="c792e-105">Asset consumption report</span></span>

<span data-ttu-id="c792e-106">Pokud jste zaúčtovali spotřebu v pracovních příkazech, můžete vytisknout sestavu spotřeby majetku.</span><span class="sxs-lookup"><span data-stu-id="c792e-106">When you have posted consumption on work orders, you can print an asset consumption report.</span></span> <span data-ttu-id="c792e-107">V sestavě jsou uvedeny hodiny, hodinové náklady, náklady na položku a výdaje zaúčtované v majetku.</span><span class="sxs-lookup"><span data-stu-id="c792e-107">The report displays hours, hour costs, item costs, and expenses posted on assets.</span></span>

1. <span data-ttu-id="c792e-108">Klikněte na **Správa majetku** > **Sestavy** > **Majetek** > **Spotřeba majetku**.</span><span class="sxs-lookup"><span data-stu-id="c792e-108">Click **Asset management** > **Reports** > **Assets** > **Asset consumption**.</span></span>

2. <span data-ttu-id="c792e-109">V dialogovém okně **Spotřeba majetku** vyberte parametry a úroveň podrobností, které chcete zobrazit, výběrem možnosti **Ano** na příslušných přepínačích a vložením úrovně funkčního místa do sekce **Zobrazit**.</span><span class="sxs-lookup"><span data-stu-id="c792e-109">In the **Asset consumption** dialog, select the parameters and detail level you want to see by selecting **Yes** on the relevant toggle buttons, and inserting a functional location level in the **Show** section.</span></span>
    - <span data-ttu-id="c792e-110">V poli **Úrovně** určete, jak detailní mají být řádky majetku v případě funkčních míst.</span><span class="sxs-lookup"><span data-stu-id="c792e-110">You can use the **Levels** field to indicate how detailed you want the asset lines to be regarding functional locations.</span></span> 
    
        <span data-ttu-id="c792e-111">Pokud například do pole zadáte číslo „1“ a máte strukturu funkčních míst o více úrovních, budou na nejvyšší úrovni zobrazeny všechny majetky pro funkční místo, a proto lze řádek navýšit z funkčních míst na nižší úrovni.</span><span class="sxs-lookup"><span data-stu-id="c792e-111">For example, if you enter the number "1" in the field, and you have a multi-level functional location structure, all assets for a functional location will be shown on the top level, and therefore a line may be added up from functional locations located at a lower level.</span></span> 
        
        <span data-ttu-id="c792e-112">Pokud do pole **Úrovně** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechnymajetky na všech úrovních funkčních míst, ke kterým se vztahují.</span><span class="sxs-lookup"><span data-stu-id="c792e-112">If you enter the number "0" in the **Levels** field, you will see a detailed result showing all assets on all the functional location levels to which they are related.</span></span> 
        
    - <span data-ttu-id="c792e-113">Chcete-li zobrazit součty jednotlivých dílčích majetků v sestavě, vyberte možnost **Ano** na přepínači **Součet na veškerém dílčím majetku**.</span><span class="sxs-lookup"><span data-stu-id="c792e-113">Select **Yes** on the **Sum on all sub assets** toggle button to see sums for each sub asset in the report.</span></span>

3. <span data-ttu-id="c792e-114">V části **Data** vyberte časový interval.</span><span class="sxs-lookup"><span data-stu-id="c792e-114">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="c792e-115">Na záložce s náhledem **Cíl** vyberte, zda chcete sestavu zobrazit na obrazovce, vytisknout nebo ji uložit jako soubor nebo e-mail.</span><span class="sxs-lookup"><span data-stu-id="c792e-115">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="c792e-116">V případě potřeby můžete vybrat konkrétní majetek, který se má v sestavě zobrazit.</span><span class="sxs-lookup"><span data-stu-id="c792e-116">If required, you can select specific assets to be displayed in the report.</span></span> <span data-ttu-id="c792e-117">Na záložce s náhledem **Záznamy k zahrnutí** klikněte na možnost **Filtr** a přidejte majetek, který chcete zahrnout do sestavy.</span><span class="sxs-lookup"><span data-stu-id="c792e-117">On the **Records to include** FastTab, click **Filter**, and add the assets you want to include in the report.</span></span>

6. <span data-ttu-id="c792e-118">Klepnutím na tlačítko **OK** sestavu vygenerujte.</span><span class="sxs-lookup"><span data-stu-id="c792e-118">Click **OK** to generate the report.</span></span>


## <a name="work-order-consumption-report"></a><span data-ttu-id="c792e-119">Sestava spotřeby pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="c792e-119">Work order consumption report</span></span>

<span data-ttu-id="c792e-120">Pokud jste zaúčtovali spotřebu v pracovních příkazech, můžete vytisknout sestavu spotřeby pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="c792e-120">When you have posted consumption on work orders, you can print a work order consumption report.</span></span> <span data-ttu-id="c792e-121">V sestavě jsou uvedeny hodiny, hodinové náklady, náklady na položku a výdaje zaúčtované na pracovním příkazu.</span><span class="sxs-lookup"><span data-stu-id="c792e-121">The report displays hours, hour costs, item costs, and expenses posted on work orders.</span></span>

1. <span data-ttu-id="c792e-122">Klikněte na možnost **Správa majetku** > **Sestavy** > **Pracovní příkazy** > **Spotřeba pracovních příkazů**.</span><span class="sxs-lookup"><span data-stu-id="c792e-122">Click **Asset management** > **Reports** > **Work orders** > **Work order consumption**.</span></span>

2. <span data-ttu-id="c792e-123">V dialogovém okně **Spotřeba pracovního příkazu** vyberte parametry, které chcete zahrnout do sestavy, výběrem možnosti **Ano** v příslušných přepínacích tlačítkách v části **Zobrazit**.</span><span class="sxs-lookup"><span data-stu-id="c792e-123">In the **Work order consumption** dialog, select the parameters you want to include in the report by selecting **Yes** on the relevant toggle buttons in the **Show** section.</span></span>

3. <span data-ttu-id="c792e-124">V části **Data** vyberte časový interval.</span><span class="sxs-lookup"><span data-stu-id="c792e-124">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="c792e-125">Na záložce s náhledem **Cíl** vyberte, zda chcete sestavu zobrazit na obrazovce, vytisknout nebo ji uložit jako soubor nebo e-mail.</span><span class="sxs-lookup"><span data-stu-id="c792e-125">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="c792e-126">V případě potřeby můžete vybrat konkrétní pracovní příkazy, které se mají v sestavě zobrazit.</span><span class="sxs-lookup"><span data-stu-id="c792e-126">If required, you can select specific work orders to be displayed in the report.</span></span> <span data-ttu-id="c792e-127">Na záložce s náhledem **Záznamy k zahrnutí** klikněte na možnost **Filtr** a přidejte pracovní příkazy, které chcete zahrnout do sestavy.</span><span class="sxs-lookup"><span data-stu-id="c792e-127">On the **Records to include** FastTab, click **Filter**, and add the work orders you want to include in the report.</span></span>

6. <span data-ttu-id="c792e-128">Klepnutím na tlačítko **OK** sestavu vygenerujte.</span><span class="sxs-lookup"><span data-stu-id="c792e-128">Click **OK** to generate the report.</span></span>


>[!NOTE]
><span data-ttu-id="c792e-129">Můžete také vygenerovat [sestavu pracovních příkazů](../work-orders/work-order-report.md), která obsahuje další podrobnosti o pracovním příkazu.</span><span class="sxs-lookup"><span data-stu-id="c792e-129">You can also generate a [work order report](../work-orders/work-order-report.md), which contains more work order details.</span></span>

