--- 
title: "Nastavit kódy vykazování DPH"
description: "Kódy vykazování DPH odkazují na číslo pole v sestavě DPH."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ddb7963c73aea65a9be2a56d14854430e8dff9dd
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="14048-103">Nastavit kódy vykazování DPH</span><span class="sxs-lookup"><span data-stu-id="14048-103">Set up sales tax reporting codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="14048-104">Kódy vykazování DPH odkazují na číslo pole v sestavě DPH.</span><span class="sxs-lookup"><span data-stu-id="14048-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="14048-105">Používají se na rozvržení sestav specifických podle země a platby DPH podle kódu sestavy pro tisk částek DPH za období vyrovnání sečtené podle kódu vykazování.</span><span class="sxs-lookup"><span data-stu-id="14048-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="14048-106">Jakmile vytvoříte kódy vykazování DPH, můžete na ně odkázat kódy na pevné záložce Nastavení sestavy na stránce Kódy DPH.</span><span class="sxs-lookup"><span data-stu-id="14048-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="14048-107">Tento záznam používá ukázkovou společnost DEMF.</span><span class="sxs-lookup"><span data-stu-id="14048-107">This recording uses the DEMF demo company.</span></span>



1. <span data-ttu-id="14048-108">Přejděte na Daň > Nastavení > DPH > Kódy vykazování DPH.</span><span class="sxs-lookup"><span data-stu-id="14048-108">Go to Tax > Setup > Sales tax > Sales tax reporting codes.</span></span>
2. <span data-ttu-id="14048-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="14048-109">Click New.</span></span>
3. <span data-ttu-id="14048-110">Vyberte rozvržení sestavy, do které patří kód vykazování.</span><span class="sxs-lookup"><span data-stu-id="14048-110">Select the report layout that the reporting code belongs to.</span></span>
    * <span data-ttu-id="14048-111">Toto rozvržení slouží k filtrování dostupných kódů vykazování pro kód DPH.</span><span class="sxs-lookup"><span data-stu-id="14048-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="14048-112">Každý kód DPH patří do období vyrovnání, které patří finančnímu úřadu používajícímu rozvržení sestavy.</span><span class="sxs-lookup"><span data-stu-id="14048-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="14048-113">Zadejte číslo, které odkazuje na pole v sestavě DPH.</span><span class="sxs-lookup"><span data-stu-id="14048-113">Enter a number that refers to a field on a sales tax report.</span></span>
5. <span data-ttu-id="14048-114">V poli Text sestavy zadejte popis, který se zobrazí v sestavách.</span><span class="sxs-lookup"><span data-stu-id="14048-114">In the Report text field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="14048-115">V poli Stručný popis zadejte popis pro interní účely.</span><span class="sxs-lookup"><span data-stu-id="14048-115">In the Brief description field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="14048-116">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="14048-116">Click Save.</span></span>


