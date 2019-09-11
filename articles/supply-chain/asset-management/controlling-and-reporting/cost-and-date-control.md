---
title: Kontrola data a nákladů
description: Toto téma popisuje kontrolu data a nákladů v modulu Správa majetku.
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
ms.openlocfilehash: 2bcd1584f6a858f7589387fbfe96267b7c16176a
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918388"
---
# <a name="cost-and-date-control"></a><span data-ttu-id="2f9bb-103">Kontrola data a nákladů</span><span class="sxs-lookup"><span data-stu-id="2f9bb-103">Cost and date control</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="2f9bb-104">V modulu Správa majetku můžete vypočítat náklady pro získání přehledu o skutečných nákladech ve srovnání s rozpočtovými náklady na majetku, funkčních místech a pracovních příkazech.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-104">In Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on assets, functional locations, and work orders.</span></span> <span data-ttu-id="2f9bb-105">Skutečné náklady jsou založeny na zaúčtovaných transakcích.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="2f9bb-106">Výpočet data lze provést také v případě, že chcete porovnat plánovaná počáteční a koncová data se skutečným počátečním a koncovým datem na pracovních příkazech.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-106">You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.</span></span>

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="2f9bb-107">Řízení nákadů pro majetek, funkční místa a pracovní příkazy</span><span class="sxs-lookup"><span data-stu-id="2f9bb-107">Cost control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="2f9bb-108">Výpočty vytvořené pro majetek, funkční místa a pracovní příkazy jsou téměř totožné.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-108">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="2f9bb-109">Jediný rozdíl je to, že pro majetek a funkční místa lze do výpočtu zahrnout i dílčí majetek a dílčí skladová místa.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-109">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="2f9bb-110">Datum je datum transakce, kdy byla zaznamenána registrace.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-110">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="2f9bb-111">Klepněte na položku **Správa majetku** > **Dotazy** > **Majetek** > **Řízení nákladů majetku** nebo **Řízení v funkčního místa** nebo **Správa majetku** > **Dotazy** > **pracovní příkazy** > **Řízení nákladů pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-111">Click **Asset management** > **Inquiries** > **Assets** > **Asset cost control** or **Functional location cost control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order cost control**.</span></span>

2. <span data-ttu-id="2f9bb-112">V dialogovém okně **Řízení nákladů majetku** / **Řízení nákladů funkčního místa** / **Řízení nákladů pracovního příkazu** vyberte období, které má být vypočítáno.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-112">In the **Asset cost control** / **Functional location cost control** / **Work order cost control** dialog, select a period to be calculated.</span></span>

3. <span data-ttu-id="2f9bb-113">V případě potřeby vyberte sadu finančních dimenzí, která má být zahrnuta do výpočtu.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-113">If required, select a financial dimension set to be included in the calculation.</span></span>

4. <span data-ttu-id="2f9bb-114">Nechcete-li zobrazit výsledky obsahující nulové náklady, vyberte možnost Ano na přepínacím tlačítku **Přeskočit nulu**.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="2f9bb-115">V poli **Úroveň** určete, jak detailní mají být řádky řízení nákladů v případě funkčních míst.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-115">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> <span data-ttu-id="2f9bb-116">Pokud například do pole zadáte číslo „1“ a máte hierarchii funkčních míst o více úrovních, budou na nejvyšší úrovni zobrazeny všechny řádky řízení nákladů pro funkční místo, a proto lze navýšit hodiny na řádku z funkčních míst na nižší úrovni.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="2f9bb-117">Pokud do pole **Úroveň** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechny řádky řízení nákladů na všech úrovních funkčních míst, ke kterým se vztahují.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="2f9bb-118">Chcete-li do výpočtu zahrnout tento sloupec, vyberte Ano na přepínači **Zobrazit otevřené potvrzené náklady**.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-118">Select "Yes" on the **Show open committed cost** toggle button if you want to include that column in the calculation.</span></span>

7. <span data-ttu-id="2f9bb-119">Chcete-li zobrazit náklady související s dílčími aktivy jako samostatné řádky, vyberte možnost Ano na přepínacím tlačítku **Zahrnout dílčí aktiva**.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-119">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="2f9bb-120">Chcete-li hledání omezit, můžete vybrat konkrétní majetek/funkční skladová místa/pracovní příkazy na pevné záložce **Záznamy, které mají být zahrnuty**.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-120">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="2f9bb-121">Výpočet zahájíte klepnutím na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-121">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="2f9bb-122">Následující obrázek ukazuje příklad dialogového okna **Řízení nákladů majetku**.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-122">The figure below shows an example of the **Asset cost control** dialog.</span></span>

![Obrázek č. 1](media/01-controlling-and-reporting.png)

10. <span data-ttu-id="2f9bb-124">Na stránce **Řízení hodin majetku**, ve skupinách podokna akce **Seskupit podle...** vyberte odpovídající tlačítka pro zobrazení požadované úrovně podrobností výpočtu.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-124">In the **Group by...** action pane groups on the **Asset cost control** page, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="2f9bb-125">Vybraná tlačítka podokna akcí jsou zvýrazněna.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-125">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="2f9bb-126">Kliknutím na tlačítko jej aktivujte nebo deaktivujte.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-126">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="2f9bb-127">Následující obrázek ukazuje příklad výpočtu výsledků v možnoti **Řízení nákladů majetku**.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-127">The figure below shows an example of calculation results in **Asset cost control**.</span></span>

![Obrázek č. 2](media/02-controlling-and-reporting.png)

<span data-ttu-id="2f9bb-129">Dalším způsobem provedení výpočtu nákladů je vybrat více majetku v možnosti **Všechen majetek** nebo **Aktivní majetek**.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-129">Another way of making a cost calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="2f9bb-130">Poté klikněte na tlačítko **Řízení nákladů** na kartě **Obecné**. V dialogovémokně  **Řízení nákladů majetku** je vybraný majetek automaticky vložen do pole **Majetek** na záložce s náhledem **Záznamy k zahrnutí**.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-130">Then, you click the **Cost control** button on the **General** tab. In the **Asset cost control** dialog, the selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="2f9bb-131">Klikněte na **OK** a zobrazí se výpočet nákladů pro vybraný majetek.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-131">Click **OK**, and a cost calculation for the selected assets is shown.</span></span> <span data-ttu-id="2f9bb-132">Stejný postup lze provést pro funkční místa ve volbě **Všechna funkční místa** nebo **Aktivní funkční místa** a pro pracovní příkazy ve volbě **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-132">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>

>[!NOTE]
><span data-ttu-id="2f9bb-133">V poli **Původní rozpočet** jsou uvedeny rozpočtové náklady z prognózy pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-133">The **Original budget** field shows budget costs from the work order forecast.</span></span> <span data-ttu-id="2f9bb-134">Pole **Potvrzené náklady** zobrazí celkovu částku výdajů, které se právnická osoba zavázala platit.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-134">The **Committed cost** field shows the total amount of expenses that a legal entity has committed itself to pay.</span></span> <span data-ttu-id="2f9bb-135">Pole **Otevřené potvrzené náklady** zobrazuje závazky k zaplacení za položky, hodiny a služby, které byly objednány nebo přijaty, ale dosud nebyly zaplaceny.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-135">The **Open committed cost** field shows commitments to pay for items, hours, and services you have ordered or received but not yet paid for.</span></span> <span data-ttu-id="2f9bb-136">Po zaúčtování všech registrací spotřeby budou související náklady zahrnuty do pole **Skutečné náklady**.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-136">When all consumption registrations have been posted, the related costs are included in the **Actual cost** field.</span></span>

## <a name="work-order-date-control"></a><span data-ttu-id="2f9bb-137">Řízení data pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="2f9bb-137">Work order date control</span></span>

<span data-ttu-id="2f9bb-138">Na této stránce můžete získat přehled o očekávaných počátečních a koncových datech ve srovnání se skutečnými počátečními a koncovými daty na pracovních příkazech.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-138">Use this page to get an overview of expected start and end dates compared to actual start and end dates on work orders.</span></span>

1. <span data-ttu-id="2f9bb-139">Klikněte na **Správa majetku** > **Dotazy** > **Pracovní příkazy** > **Kontrola data pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-139">Click **Asset management** > **Inquiries** > **Work orders** > **Work order date control**.</span></span>

2. <span data-ttu-id="2f9bb-140">Klikněte na tlačítko **Vypočítat.**</span><span class="sxs-lookup"><span data-stu-id="2f9bb-140">Click **Calculate**.</span></span>

3. <span data-ttu-id="2f9bb-141">V poli **Funkční místo** zvolte funkční místo.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-141">Select a functional location in the **Functional location** field.</span></span>

4. <span data-ttu-id="2f9bb-142">Vložte období, pro které chcete provést výpočet v polích **Od data** a **Do data**.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-142">Insert the period for which you want to make the calculation in the **From date** and **To date** fields.</span></span> <span data-ttu-id="2f9bb-143">Budou zahrnuty všechny pracovní příkazy s očekávaným datem zahájení v daném období.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-143">All work orders with expected start within the period will be included.</span></span>

5. <span data-ttu-id="2f9bb-144">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-144">Click **OK**.</span></span>

6. <span data-ttu-id="2f9bb-145">Ve skupině podoken akcí **Seskupit podle...** klikněte na odpovídající tlačítka pro zobrazení požadované úrovně podrobností výpočtu.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-145">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="2f9bb-146">Vybraná tlačítka podokna akcí jsou zvýrazněna.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-146">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="2f9bb-147">Kliknutím na tlačítko jej aktivujte nebo deaktivujte.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-147">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="2f9bb-148">Následující obrázek ukazuje příklad výpočtu výsledků v možnoti **Kontrola data pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-148">The figure below shows an example of calculation results in **Work order date control**.</span></span>

![Obrázek č. 3](media/03-controlling-and-reporting.png)

- <span data-ttu-id="2f9bb-150">Pole **Průměrné zpoždění zahájení** zobrazuje rozdíl mezi dny plánovaného počátečního data pro pracovní příkaz ve srovnání se skutečným počátečním datem.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-150">The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date.</span></span> <span data-ttu-id="2f9bb-151">Pokud například skutečné datum zahájení bylo dva dny před plánovaným počátečním datem, zobrazí se v tomto poli -2.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-151">If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.</span></span>  
- <span data-ttu-id="2f9bb-152">Pole **Průměrné zpoždění ukončení** zobrazuje rozdíl mezi dny plánovaného koncového data pro pracovní příkaz ve srovnání se skutečným koncovým datem.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-152">The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date.</span></span> <span data-ttu-id="2f9bb-153">Pokud například skutečné datum ukončení bylo tři dny po plánovaném koncovém datu, zobrazí se v tomto poli 3.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-153">If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.</span></span>  
- <span data-ttu-id="2f9bb-154">V poli **Výskyty** se zobrazuje počet časových odchylek v závislosti na plánovaném a skutečném počátečním datu a plánovaném a skutečném koncovém datu na pracovním příkazu.</span><span class="sxs-lookup"><span data-stu-id="2f9bb-154">The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.</span></span>

