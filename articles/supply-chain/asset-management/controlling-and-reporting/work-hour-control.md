---
title: Kontrola pracovní doby
description: Tohle téma popisuje kontrolu pracovní doby v modulu Správa majetku.
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
ms.openlocfilehash: 1a59b4bbf1a4612cea1ba3bd536ba4b018fc621f
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652326"
---
# <a name="work-hour-control"></a><span data-ttu-id="98f9a-103">Kontrola pracovní doby</span><span class="sxs-lookup"><span data-stu-id="98f9a-103">Work hour control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="98f9a-104">V modulu Správa majetku můžete vypočítat počet hodin pro získání přehledu o skutečných hodinách ve srovnání s rozpočtovými hodinami na majetku, funkčních místech nebo pracovních příkazech.</span><span class="sxs-lookup"><span data-stu-id="98f9a-104">In Asset Management, you can calculate hours to get an overview of actual hours compared to budget hours on assets, functional locations, or work orders.</span></span> <span data-ttu-id="98f9a-105">Skutečné hodiny jsou založeny na zaúčtovaných transakcích.</span><span class="sxs-lookup"><span data-stu-id="98f9a-105">Actual hours are based on posted transactions.</span></span>

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="98f9a-106">Řízení pracovní doby pro majetek, funkční místa a pracovní příkazy</span><span class="sxs-lookup"><span data-stu-id="98f9a-106">Work hour control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="98f9a-107">Výpočty vytvořené pro majetek, funkční místa a pracovní příkazy jsou téměř totožné.</span><span class="sxs-lookup"><span data-stu-id="98f9a-107">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="98f9a-108">Jediný rozdíl je to, že pro majetek a funkční místa lze do výpočtu zahrnout i dílčí majetek a dílčí skladová místa.</span><span class="sxs-lookup"><span data-stu-id="98f9a-108">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="98f9a-109">Datum je datum transakce, kdy byla zaznamenána registrace.</span><span class="sxs-lookup"><span data-stu-id="98f9a-109">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="98f9a-110">Klepněte na položku **Správa majetku** > **Dotazy** > **Majetek** > **Řízení hodin majetku** nebo **Řízení hodin funkčního místa** nebo **Správa majetku** > **Dotazy** > **pracovní příkazy** > **Řízení hodin na pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="98f9a-110">Click **Asset management** > **Inquiries** > **Assets** > **Asset hour control** or **Functional location hour control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order hour control**.</span></span>

2. <span data-ttu-id="98f9a-111">V dialogovém okně **Řízení hodin majetku**.</span><span class="sxs-lookup"><span data-stu-id="98f9a-111">In the **Asset hour control** dialog, .</span></span>

3. <span data-ttu-id="98f9a-112">V dialogovém okně **Řízení hodin majetku** / **Řízení hodin funkčního místa** / **Řízení hodin pracovního příkazu** vyberte období, které má být vypočteno v polích **Od data** a **Do data**.</span><span class="sxs-lookup"><span data-stu-id="98f9a-112">In the **Asset hour control** / **Functional location hour control** / **Work order hour control** dialog, select a period to be calculated in the **From date** and **To date** fields.</span></span>

4. <span data-ttu-id="98f9a-113">V případě potřeby vyberte **Sadu finančních dimenzí**, která má být zahrnuta do výpočtu.</span><span class="sxs-lookup"><span data-stu-id="98f9a-113">If required, select a **Financial dimension set** to be included in the calculation.</span></span>

5. <span data-ttu-id="98f9a-114">Nechcete-li zobrazit výsledky obsahující nula hodin, vyberte možnost Ano na přepínacím tlačítku **Přeskočit nulu**.</span><span class="sxs-lookup"><span data-stu-id="98f9a-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results containing zero hours.</span></span>

6. <span data-ttu-id="98f9a-115">V poli **Úroveň** určete, jak detailní mají být řádky řízení hodin v případě funkčních míst.</span><span class="sxs-lookup"><span data-stu-id="98f9a-115">You can use the **Level** field to indicate how detailed you want the hour control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="98f9a-116">Pokud například do pole zadáte číslo „1“ a máte hierarchii funkčních míst o více úrovních, budou na nejvyšší úrovni zobrazeny všechny řádky řízení hodin pro funkční místo, a proto lze navýšit hodiny na řádku z funkčních míst na nižší úrovni.</span><span class="sxs-lookup"><span data-stu-id="98f9a-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all hour control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="98f9a-117">Pokud do pole **Úroveň** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechny řádky řízení hodin na všech úrovních funkčních míst, ke kterým se vztahují.</span><span class="sxs-lookup"><span data-stu-id="98f9a-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all hour control lines on all the functional location levels to which they are related.</span></span>

7. <span data-ttu-id="98f9a-118">Chcete-li zobrazit náklady související s dílčími aktivy jako samostatné řádky, vyberte možnost Ano na přepínacím tlačítku **Zahrnout dílčí aktiva**.</span><span class="sxs-lookup"><span data-stu-id="98f9a-118">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="98f9a-119">Chcete-li hledání omezit, můžete vybrat konkrétní majetek/funkční skladová místa/pracovní příkazy na pevné záložce **Záznamy, které mají být zahrnuty**.</span><span class="sxs-lookup"><span data-stu-id="98f9a-119">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="98f9a-120">Výpočet zahájíte klepnutím na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="98f9a-120">Click **OK** to start the calculation.</span></span>

10. <span data-ttu-id="98f9a-121">Na kartě **Kontrola hodin majetku** klikněte na tlačítka **Seskupit podle** pro zobrazení požadované úrovně podrobností výpočtu.</span><span class="sxs-lookup"><span data-stu-id="98f9a-121">On the **Asset hour control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="98f9a-122">Vybraná tlačítka **Seskupit podle** jsou zvýrazněna.</span><span class="sxs-lookup"><span data-stu-id="98f9a-122">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="98f9a-123">Kliknutím na tlačítko jej aktivujte nebo deaktivujte.</span><span class="sxs-lookup"><span data-stu-id="98f9a-123">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="98f9a-124">Příklad</span><span class="sxs-lookup"><span data-stu-id="98f9a-124">Example</span></span>

<span data-ttu-id="98f9a-125">Následující snímek obrazovky ukazuje příklad výpočtu **Řízení hodin majetku**.</span><span class="sxs-lookup"><span data-stu-id="98f9a-125">The screenshot below shows an example of an **Asset hour control** calculation.</span></span>

- <span data-ttu-id="98f9a-126">V poli **Původní rozpočet** jsou uvedeny rozpočtové hodiny z prognózy pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="98f9a-126">The **Original budget** field shows budget hours from the work order forecast.</span></span> 
- <span data-ttu-id="98f9a-127">Pole **Skutečné hodiny** zobrazuje zaúčtované hodiny na pracovních příkazech.</span><span class="sxs-lookup"><span data-stu-id="98f9a-127">The **Actual hours** field shows posted hours on work orders.</span></span> 
- <span data-ttu-id="98f9a-128">Pole **Potvrzené hodiny** zobrazuje celkové množství hodin, které vaše společnost potvrdila ve vztahu k pracovním příkazům.</span><span class="sxs-lookup"><span data-stu-id="98f9a-128">The **Committed hours** field shows total amount of hours that your company is committed to in relation to work orders.</span></span>

![Příklad výpočtu kontrolního času majetku](media/04-controlling-and-reporting.png)

<span data-ttu-id="98f9a-130">Dalším způsobem provedení výpočtu hodin je vybrat více majetku v možnosti **Všechen majetek** nebo **Aktivní majetek**.</span><span class="sxs-lookup"><span data-stu-id="98f9a-130">Another way of making an hour calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="98f9a-131">Poté klikněte na tlačítko **Řízení hodin** na pevné záložce **Obecné**.</span><span class="sxs-lookup"><span data-stu-id="98f9a-131">Then you click the **Hour control** button on the **General** FastTab.</span></span> <span data-ttu-id="98f9a-132">Vybraný majetek je automaticky vložen do pole **Majetek** na pevné záložce **Záznamy, které mají být zahrnuty**.</span><span class="sxs-lookup"><span data-stu-id="98f9a-132">The selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="98f9a-133">Klikněte na tlačítko **OK** v dialogovém okně **Řízení hodin majetku** a zobrazí se výpočet pro vybraný majetek.</span><span class="sxs-lookup"><span data-stu-id="98f9a-133">Click **OK** in the **Asset hour control** dialog, and the calculation for the selected assets is shown.</span></span> <span data-ttu-id="98f9a-134">Stejný postup lze provést pro funkční místa ve volbě **Všechna funkční místa** nebo **Aktivní funkční místa** a pro pracovní příkazy ve volbě **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="98f9a-134">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>


