---
title: Řízení nákladů závad majetku
description: Toto téma popisuje kontrolu nákladů na závady majetku v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.openlocfilehash: 3c34180ad99db29147587bb002aaa6badc918717
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652234"
---
# <a name="asset-fault-cost-control"></a><span data-ttu-id="7edb4-103">Řízení nákladů závad majetku</span><span class="sxs-lookup"><span data-stu-id="7edb4-103">Asset fault cost control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="7edb4-104">V modulu Správa majetku můžete vypočítat náklady na registrace závad majetku pro získání přehledu o skutečných nákladech ve srovnání s rozpočtovými náklady.</span><span class="sxs-lookup"><span data-stu-id="7edb4-104">In Asset Management, you can calculate costs on asset fault registrations to get an overview of actual costs compared to budget costs.</span></span> <span data-ttu-id="7edb4-105">Skutečné náklady jsou založeny na zaúčtovaných transakcích.</span><span class="sxs-lookup"><span data-stu-id="7edb4-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="7edb4-106">Datum je datum závady, kdy byl zaznamenán příznak.</span><span class="sxs-lookup"><span data-stu-id="7edb4-106">The date is the fault date on which the symptom was recorded.</span></span>

1. <span data-ttu-id="7edb4-107">Klikněte na **Správa majetku** > **Dotazy** > **Závada majetku** > **Řízení nákladů závad majetku**.</span><span class="sxs-lookup"><span data-stu-id="7edb4-107">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault cost control**.</span></span>

2. <span data-ttu-id="7edb4-108">V dialogovém okně **Řízení nákladů závad majetku** zvolte sadu finančních dimenzí, která bude v případě potřeby zahrnuta do výpočtu.</span><span class="sxs-lookup"><span data-stu-id="7edb4-108">In the **Asset fault cost control** dialog, select a financial dimension set to be included in the calculation, if required.</span></span>

4. <span data-ttu-id="7edb4-109">Nechcete-li zobrazit výsledky obsahující nulové náklady, vyberte možnost Ano na přepínacím tlačítku **Přeskočit nulu**.</span><span class="sxs-lookup"><span data-stu-id="7edb4-109">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="7edb4-110">V poli **Úroveň** určete, jak detailní mají být řádky řízení nákladů v případě funkčních míst.</span><span class="sxs-lookup"><span data-stu-id="7edb4-110">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="7edb4-111">Pokud například do pole zadáte číslo „1“ a máte strukturu funkčních míst o více úrovních, budou na nejvyšší úrovni zobrazeny všechny řádky řízení nákladů závad majetku pro funkční místo, a proto lze hodiny na řádku navýšit z funkčních míst na nižší úrovni.</span><span class="sxs-lookup"><span data-stu-id="7edb4-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="7edb4-112">Pokud do pole **Úroveň** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechny řádky řízení nákladů závad majetku na všech úrovních funkčních míst, ke kterým se vztahují.</span><span class="sxs-lookup"><span data-stu-id="7edb4-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault cost control lines on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="7edb4-113">Chcete-li hledání omezit, můžete vybrat konkrétní majetek, data závad a příčiny závad na záložce s náhledem **Záznamy, které mají být zahrnuty**.</span><span class="sxs-lookup"><span data-stu-id="7edb4-113">If you want to limit the search, you can select specific assets, fault dates, and fault causes on the **Records to include** FastTab.</span></span>

7. <span data-ttu-id="7edb4-114">Výpočet zahájíte klepnutím na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="7edb4-114">Click **OK** to start the calculation.</span></span>

8. <span data-ttu-id="7edb4-115">Ve skupině **Seskupit podle** klikněte na odpovídající tlačítka pro zobrazení požadované úrovně podrobností výpočtu.</span><span class="sxs-lookup"><span data-stu-id="7edb4-115">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="7edb4-116">Vybraná tlačítka **Seskupit podle** jsou zvýrazněna.</span><span class="sxs-lookup"><span data-stu-id="7edb4-116">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="7edb4-117">Kliknutím na tlačítko jej aktivujte nebo deaktivujte.</span><span class="sxs-lookup"><span data-stu-id="7edb4-117">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="7edb4-118">Příklad</span><span class="sxs-lookup"><span data-stu-id="7edb4-118">Example</span></span>

<span data-ttu-id="7edb4-119">V tomto příkladu je zobrazen výpočet kontroly nákladů majetku.</span><span class="sxs-lookup"><span data-stu-id="7edb4-119">This example shows an asset fault cost control calculation.</span></span>

- <span data-ttu-id="7edb4-120">V poli **Původní rozpočet** jsou uvedeny rozpočtové náklady z prognózy pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="7edb4-120">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="7edb4-121">Pole **Skutečné náklady** zobrazuje zaúčtované náklady na pracovních příkazech.</span><span class="sxs-lookup"><span data-stu-id="7edb4-121">The **Actual cost** field shows posted costs on work orders.</span></span> 
- <span data-ttu-id="7edb4-122">Pole **Potvrzené náklady** zobrazuje celkové množství nákladů, které vaše společnost potvrdila ve vztahu k pracovním příkazům.</span><span class="sxs-lookup"><span data-stu-id="7edb4-122">The **Committed cost** field shows total costs that your company is committed to in relation to work orders.</span></span>

    ![Obrázek č. 1](media/05-controlling-and-reporting.png)

<span data-ttu-id="7edb4-124">Více informací o nastavení závad získáte v části [Správa závad](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="7edb4-124">For information about how to set up faults, see the [Fault management](../setup-for-work-orders/fault-management.md) topic.</span></span>
