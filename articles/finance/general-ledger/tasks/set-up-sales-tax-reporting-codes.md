---
title: Nastavit kódy vykazování DPH
description: Kódy vykazování DPH odkazují na číslo pole v sestavě DPH.
author: twheeloc
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4751256858da417ec9bb1b7d9ccd16fb6bef1cac
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185927"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="28aa5-103">Nastavit kódy vykazování DPH</span><span class="sxs-lookup"><span data-stu-id="28aa5-103">Set up sales tax reporting codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="28aa5-104">Kódy vykazování DPH odkazují na číslo pole v sestavě DPH.</span><span class="sxs-lookup"><span data-stu-id="28aa5-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="28aa5-105">Používají se na rozvržení sestav specifických podle země a platby DPH podle kódu sestavy pro tisk částek DPH za období vyrovnání sečtené podle kódu vykazování.</span><span class="sxs-lookup"><span data-stu-id="28aa5-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="28aa5-106">Jakmile vytvoříte kódy vykazování DPH, můžete na ně odkázat kódy na pevné záložce Nastavení sestavy na stránce Kódy DPH.</span><span class="sxs-lookup"><span data-stu-id="28aa5-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="28aa5-107">Tento záznam používá ukázkovou společnost DEMF.</span><span class="sxs-lookup"><span data-stu-id="28aa5-107">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="28aa5-108">V **Navigačním podokně** přejděte na **Daň > Nepřímé daně > DPH > Kódy vykazování DPH**.</span><span class="sxs-lookup"><span data-stu-id="28aa5-108">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="28aa5-109">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="28aa5-109">Click **New**.</span></span>
3. <span data-ttu-id="28aa5-110">Vyberte rozvržení sestavy, do které patří kód vykazování.</span><span class="sxs-lookup"><span data-stu-id="28aa5-110">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="28aa5-111">Toto rozvržení slouží k filtrování dostupných kódů vykazování pro kód DPH.</span><span class="sxs-lookup"><span data-stu-id="28aa5-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="28aa5-112">Každý kód DPH patří do období vyrovnání, které patří finančnímu úřadu používajícímu rozvržení sestavy.</span><span class="sxs-lookup"><span data-stu-id="28aa5-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="28aa5-113">Zadejte číslo do pole **Kód vykazování-**.</span><span class="sxs-lookup"><span data-stu-id="28aa5-113">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="28aa5-114">V poli **Text sestavy** zadejte popis, který se zobrazí v sestavách.</span><span class="sxs-lookup"><span data-stu-id="28aa5-114">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="28aa5-115">V poli **Stručný popis** zadejte popis pro interní účely.</span><span class="sxs-lookup"><span data-stu-id="28aa5-115">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="28aa5-116">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="28aa5-116">Click **Save**.</span></span>

