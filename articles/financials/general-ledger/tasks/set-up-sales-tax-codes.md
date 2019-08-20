---
title: Nastavit kódy DPH
description: Toto téma vysvětluje, jak nastavit kódy DPH v aplikaci Dynamics 365 for Finance and Operations.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3419c6b569093d717158e80bd9bc01054d82bff9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834823"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="71af1-103">Nastavit kódy DPH</span><span class="sxs-lookup"><span data-stu-id="71af1-103">Set up sales tax codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="71af1-104">Toto téma vysvětluje, jak nastavit kódy DPH v aplikaci Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="71af1-104">This topic explains how to set up sales tax codes in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="71af1-105">Kódy DPH se vytvoří pro každou nepřímou daň nebo clo, které je právnická osoba povinna vypočítávat, shromažďovat o nich informace a platit je finančním úřadům.</span><span class="sxs-lookup"><span data-stu-id="71af1-105">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="71af1-106">Tento úkol využívá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="71af1-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="71af1-107">Přejděte na **Navigační podokno > Daň > Nepřímé daně > DPH > Kódy DPH**.</span><span class="sxs-lookup"><span data-stu-id="71af1-107">Go to **Navigation pane > Tax > Indirect taxes > Sales tax > Sales tax codes**.</span></span>
2. <span data-ttu-id="71af1-108">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="71af1-108">Select **New**.</span></span>
3. <span data-ttu-id="71af1-109">V poli Kód **prodejní daně** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="71af1-109">In the **Sales tax code** field, type a value.</span></span>
4. <span data-ttu-id="71af1-110">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="71af1-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="71af1-111">Vyberte **Období vyrovnání** otevření rozbalovacího seznamu a určete, pro které finanční úřady a v jakých intervalech je tato DPH vykazována a zaplacena.</span><span class="sxs-lookup"><span data-stu-id="71af1-111">Select a **Settlement period** by opening the pull-down list to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="71af1-112">Vyberte možnost **Skupina zaúčtování hl. knihy** a určete hlavní účty pro zaúčtování DPH do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="71af1-112">Select a **Ledger posting group** to specify the main accounts to post sales tax to the general ledger.</span></span>
7. <span data-ttu-id="71af1-113">Rozbalte pevnou záložku **Výpočet**.</span><span class="sxs-lookup"><span data-stu-id="71af1-113">Expand the **Calculation** FastTab.</span></span> <span data-ttu-id="71af1-114">Ta obsahuje několik polí určujících způsob výpočtu částky DPH.</span><span class="sxs-lookup"><span data-stu-id="71af1-114">This includes multiple fields that control how sales tax amounts will be calculated.</span></span> <span data-ttu-id="71af1-115">Vyplňte tato pole podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="71af1-115">Fill these fields out as needed.</span></span>  
8. <span data-ttu-id="71af1-116">V **Podokně akcí** v horní části rozhraní vyberte **Kód DPH**.</span><span class="sxs-lookup"><span data-stu-id="71af1-116">On the **Action Pane** at the top of the interface, select **Sales tax code**.</span></span>
9. <span data-ttu-id="71af1-117">Vyberte **Hodnoty**.</span><span class="sxs-lookup"><span data-stu-id="71af1-117">Select **Values**.</span></span>
10. <span data-ttu-id="71af1-118">Zadejte hodnotu tohoto daňového kódu do sloupce **hodnota**.</span><span class="sxs-lookup"><span data-stu-id="71af1-118">Enter the value for this tax code in the **value** column.</span></span>
    - <span data-ttu-id="71af1-119">Pokud je vybrána možnost Částka za jednotku, hodnota na pevné záložce **Výpočet** v poli Zdroj se vynásobí množstvím v transakci a vypočítá se částka DPH.</span><span class="sxs-lookup"><span data-stu-id="71af1-119">On the **Calculation** FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="71af1-120">Pokud kód daně není daní na základě jednotky, hodnota je procentuální a použije se pro Původ pro tento kód daně k výpočtu částky DPH.</span><span class="sxs-lookup"><span data-stu-id="71af1-120">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
11. <span data-ttu-id="71af1-121">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="71af1-121">Select **Save**.</span></span>
12. <span data-ttu-id="71af1-122">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="71af1-122">Close the page.</span></span>
13. <span data-ttu-id="71af1-123">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="71af1-123">Select **Save**.</span></span>

