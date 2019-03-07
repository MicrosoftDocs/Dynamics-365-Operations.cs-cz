---
title: Odstraňování problémů s rozpočtováním pozice
description: Tento článek obsahuje odpovědí na otázky, které můžete mít při konfiguraci rozpočtování pozice. Řeší časté otázky týkající se vytváření prvků rozpočtových nákladů, skupin kompenzací a kompenzačních mřížek.
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0800a4a7c92a1a5f4d4f66bb37032eacccc4cb4e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "367103"
---
# <a name="position-budgeting-troubleshooting"></a><span data-ttu-id="0391d-104">Odstraňování problémů s rozpočtováním pozice</span><span class="sxs-lookup"><span data-stu-id="0391d-104">Position budgeting troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0391d-105">Tento článek obsahuje odpovědí na otázky, které můžete mít při konfiguraci rozpočtování pozice.</span><span class="sxs-lookup"><span data-stu-id="0391d-105">This article provides answers to questions that you might have when you configure position budgeting.</span></span> <span data-ttu-id="0391d-106">Řeší časté otázky týkající se vytváření prvků rozpočtových nákladů, skupin kompenzací a kompenzačních mřížek.</span><span class="sxs-lookup"><span data-stu-id="0391d-106">It addresses frequently asked questions about how to create budget cost elements, compensation groups, and compensation grids.</span></span> 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a><span data-ttu-id="0391d-107">Proč nelze najít stránku s pozicí prognózy v modulu Lidské zdroje?</span><span class="sxs-lookup"><span data-stu-id="0391d-107">Why can’t I find the forecast position page in Human resources?</span></span>
---------------------------------------------------------------

<span data-ttu-id="0391d-108">Pozice prognózy byly přesunuty do modulu Rozpočtování.</span><span class="sxs-lookup"><span data-stu-id="0391d-108">Forecast positions have been moved to Budgeting.</span></span>

## <a name="why-cant-i-delete-a-budget-cost-element"></a><span data-ttu-id="0391d-109">Proč nelze odstranit prvek rozpočtových nákladů?</span><span class="sxs-lookup"><span data-stu-id="0391d-109">Why can’t I delete a budget cost element?</span></span>
<span data-ttu-id="0391d-110">Nelze odstranit prvek rozpočtových nákladů, který je přiřazen k jedné pozici prognózy.</span><span class="sxs-lookup"><span data-stu-id="0391d-110">You can’t delete a budget cost element that is assigned to a forecast position.</span></span> <span data-ttu-id="0391d-111">Před odstraněním prvku rozpočtových nákladů jej odeberte ze všech pozic prognózy.</span><span class="sxs-lookup"><span data-stu-id="0391d-111">Before you can delete a budget cost element, you must remove it from all forecast positions.</span></span> <span data-ttu-id="0391d-112">**Tip:** Pokud chcete vyhledat všechny pozice, ke kterým je přiřazen prvek rozpočtových nákladů, vyberte nákladový prvek na stránce **Prvky rozpočtových nákladů** a klepněte na tlačítko **Aktualizovat pozice**.</span><span class="sxs-lookup"><span data-stu-id="0391d-112">**Tip:** To find all the positions that a budget cost element is assigned to, select the cost element on the **Budget cost elements** page, and then click **Update positions**.</span></span> <span data-ttu-id="0391d-113">Pozice, které používají nákladový prvek, jsou uvedeny v horní mřížce.</span><span class="sxs-lookup"><span data-stu-id="0391d-113">The positions that use the cost element are listed in the upper grid.</span></span>

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a><span data-ttu-id="0391d-114">Jak je možné odebrat nákladový prvek z několika pozic prognózy bez jejich jednotlivého otevření?</span><span class="sxs-lookup"><span data-stu-id="0391d-114">How can I remove a cost element from multiple forecast positions without opening each one?</span></span>
<span data-ttu-id="0391d-115">Prvek nákladů nelze odstranit.</span><span class="sxs-lookup"><span data-stu-id="0391d-115">You can’t remove a cost element.</span></span> <span data-ttu-id="0391d-116">Pokud ale změníte počáteční a koncové datum tak, aby spadalo mimo data cyklu plánování rozpočtu, nebude již přiřazen pozicím prognóz v daném cyklu plánování rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="0391d-116">However, if you change the start and end dates so that they are outside the budget planning cycle dates, the cost element will no longer be assigned to the forecast positions in that budget planning cycle.</span></span> <span data-ttu-id="0391d-117">Chcete-li provést tuto změnu, otevřete prvek rozpočtových nákladů a poté na pevné záložce **Výpočet nákladů** klepněte na tlačítko **Změnit data** a změňte datum začátku platnosti nebo datum vypršení platnosti.</span><span class="sxs-lookup"><span data-stu-id="0391d-117">To make this change, open the budget cost element, and then, on the **Cost calculation** FastTab, click **Change dates**, and change the effective date or expiration date.</span></span> <span data-ttu-id="0391d-118">Klepnutím na **OK** automaticky aktualizujete všechny pozice prognózy, ke kterým je přiřazen nákladový prvek.</span><span class="sxs-lookup"><span data-stu-id="0391d-118">Then click **OK** to automatically update all forecast positions that the cost element is assigned to.</span></span> <span data-ttu-id="0391d-119">**Tip:** Pokud použijete tuto metodu, pamatujte, že dojde k odebrání prvku rozpočtových nákladů ze **VŠECH** pozic prognózy, ve kterých počáteční a koncové datum již není v příslušném rozsahu.</span><span class="sxs-lookup"><span data-stu-id="0391d-119">**Tip:** If you use this method, be aware that it removes the budget cost element from **all** forecast positions where the start and end dates are no longer within the appropriate range.</span></span> <span data-ttu-id="0391d-120">Pokud to nemáte v úmyslu, bude třeba otevřít jednotlivé pozice prognózy, ze kterých chcete odebrat prvek rozpočtových nákladů, a provést změny ručně.</span><span class="sxs-lookup"><span data-stu-id="0391d-120">If this effect isn't what you intend, you must open each forecast position that you want to remove the budget cost element from and manually make the change.</span></span>

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a><span data-ttu-id="0391d-121">Proč nelze zadat roční částku na pevné kartě výpočtu nákladů prvku rozpočtových nákladů?</span><span class="sxs-lookup"><span data-stu-id="0391d-121">Why can’t I enter an annual amount on the Cost calculation FastTab for the budget cost element?</span></span>
<span data-ttu-id="0391d-122">Nelze zadat roční částku, pokud existují prvky rozpočtových nákladů na pevné kartě **Základ výpočtu**, protože systém vyžaduje pro výpočet hodnoty procento.</span><span class="sxs-lookup"><span data-stu-id="0391d-122">You can’t enter an annual amount if there are budget cost elements on the **Calculation basis** FastTab, because the system requires a percentage in order to calculate the value.</span></span> <span data-ttu-id="0391d-123">Odeberte všechny prvky rozpočtových nákladů z pevné karty **Základ výpočtu**, chcete-li tuto hodnotu měnit.</span><span class="sxs-lookup"><span data-stu-id="0391d-123">To change the value, remove all budget cost elements from the **Calculation basis** FastTab.</span></span>

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a><span data-ttu-id="0391d-124">Proč nelze změnit typ rozpočtových nákladů z hodnoty „příjmový“ na jiný typ rozpočtových nákladů?</span><span class="sxs-lookup"><span data-stu-id="0391d-124">Why can’t I change the budget cost type from earning to another budget cost type?</span></span>
<span data-ttu-id="0391d-125">Některé prvky rozpočtových nákladů používají nákladový prvek typu „příjmový“ jako základ pro výpočty.</span><span class="sxs-lookup"><span data-stu-id="0391d-125">Some budget cost elements use the earning cost element as a calculation basis.</span></span> <span data-ttu-id="0391d-126">Chcete-li změnit pole **Typ rozpočtových nákladů**, odeberte prvek nákladový příjmů z pevné záložky **Základ výpočtu** u všech prvků rozpočtových nákladů.</span><span class="sxs-lookup"><span data-stu-id="0391d-126">To change the **Budget cost type** field, remove the earning cost element from the **Calculation basis** FastTab of all budget cost elements.</span></span>

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a><span data-ttu-id="0391d-127">Proč nelze změnit datum řádků prvku rozpočtových nákladů pro prvek rozpočtových nákladů?</span><span class="sxs-lookup"><span data-stu-id="0391d-127">Why can’t I change the date on budget cost element lines for a budget cost element?</span></span>
<span data-ttu-id="0391d-128">Datum na řádku prvku rozpočtových nákladů při použití prvku rozpočtových nákladů v pozici prognózy nelze změnit.</span><span class="sxs-lookup"><span data-stu-id="0391d-128">You can’t change the date on the budget cost element line when a budget cost element is used by a forecast position.</span></span> <span data-ttu-id="0391d-129">Důvodem je, že je třeba zajistit, aby pozice prognóz byly vždy v souladu s pokyny prvku rozpočtových nákladů.</span><span class="sxs-lookup"><span data-stu-id="0391d-129">This limitation helps guarantee that the forecast positions are always within the guidelines of the budget cost element.</span></span> <span data-ttu-id="0391d-130">Pokud chcete změnit datum, na pevné záložce **Výpočet nákladů** klepněte na tlačítko **Změnit data** a zadejte nové datum.</span><span class="sxs-lookup"><span data-stu-id="0391d-130">To change the date, on the **Cost calculation** FastTab, click **Change dates**, and enter the new dates.</span></span> <span data-ttu-id="0391d-131">Klepnutím na **OK** aktualizujete pozice, ke kterým je přiřazen nákladový prvek.</span><span class="sxs-lookup"><span data-stu-id="0391d-131">Then click **OK** to update the positions that the cost element is assigned to.</span></span>

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a><span data-ttu-id="0391d-132">Proč nelze změnit náklady pro prvek rozpočtových nákladů na stránce skupiny kompenzace?</span><span class="sxs-lookup"><span data-stu-id="0391d-132">Why can’t I change the costs for a budget cost element on the Compensation group page?</span></span>
<span data-ttu-id="0391d-133">Prvky rozpočtových nákladů můžete vytvářet a měnit pouze na stránce **Prvky rozpočtových nákladů**.</span><span class="sxs-lookup"><span data-stu-id="0391d-133">You can create and change budget cost elements only on the **Budget cost elements** page.</span></span>

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a><span data-ttu-id="0391d-134">Proč se zobrazila chybová zpráva při změně data pro nákladový prvek v pozici prognózy?</span><span class="sxs-lookup"><span data-stu-id="0391d-134">Why do I receive an error message when I change the dates for a cost element on a forecast position?</span></span>
<span data-ttu-id="0391d-135">Data na řádku nákladového prvku pozice prognózy musí spadat do následujících rozsahů:</span><span class="sxs-lookup"><span data-stu-id="0391d-135">The dates on the forecast position cost element line must be within the following ranges:</span></span>

-   <span data-ttu-id="0391d-136">Data aktivace a vyřazení pozice.</span><span class="sxs-lookup"><span data-stu-id="0391d-136">The activation and retirement dates of the position.</span></span>
-   <span data-ttu-id="0391d-137">Data aktivace a vypršení platnosti prvku rozpočtových nákladů.</span><span class="sxs-lookup"><span data-stu-id="0391d-137">The activation and expiration dates of the budget cost element.</span></span>
-   <span data-ttu-id="0391d-138">Datum zahájení a ukončení rozpočtového cyklu, který j přidruženy k procesu plánování rozpočtu pozice prognózy.</span><span class="sxs-lookup"><span data-stu-id="0391d-138">The start and end dates of the budget cycle that is associated with the budget planning process of the forecast position.</span></span>




