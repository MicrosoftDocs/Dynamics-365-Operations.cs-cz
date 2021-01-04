---
title: Nastavit kódy vykazování DPH
description: Kódy vykazování DPH odkazují na číslo pole uvedené v sestavě DPH.
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
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 362d30e56fe35b85d50bfa2df57364733b366fef
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646174"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="14736-103">Nastavit kódy vykazování DPH</span><span class="sxs-lookup"><span data-stu-id="14736-103">Set up sales tax reporting codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="14736-104">Kódy vykazování DPH odkazují na číslo pole uvedené v sestavě DPH.</span><span class="sxs-lookup"><span data-stu-id="14736-104">The Sales tax reporting codes refer to a field number that's listed on a sales tax report.</span></span> <span data-ttu-id="14736-105">Používají se na rozložení sestavy specifickém pro zemi.</span><span class="sxs-lookup"><span data-stu-id="14736-105">They are used on country-specific report layouts.</span></span> <span data-ttu-id="14736-106">Používají se také v sestavě platby DPH podle kódu.</span><span class="sxs-lookup"><span data-stu-id="14736-106">They're also used on the Sales tax payment by code report.</span></span> <span data-ttu-id="14736-107">Tato sestava zobrazuje částky daně z obratu za období vypořádání shrnuté pro každý kód vykazování.</span><span class="sxs-lookup"><span data-stu-id="14736-107">That report shows sales tax amounts for a settlement period summarized for each reporting code.</span></span> <span data-ttu-id="14736-108">Jakmile vytvoříte kódy vykazování DPH, můžete na ně odkazovat na pevných záložkách Nastavení sestavy, k nimž přejdete ze stránky **Kódy DPH**.</span><span class="sxs-lookup"><span data-stu-id="14736-108">After you create Sales tax reporting codes, you can refer to those codes on the Report setup FastTabs, which you can access from the **Sales tax code** page.</span></span> 

<span data-ttu-id="14736-109">Tento záznam používá ukázkovou společnost DEMF.</span><span class="sxs-lookup"><span data-stu-id="14736-109">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="14736-110">V **Navigačním podokně** přejděte na **Daň > Nepřímé daně > DPH > Kódy vykazování DPH**.</span><span class="sxs-lookup"><span data-stu-id="14736-110">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="14736-111">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="14736-111">Click **New**.</span></span>
3. <span data-ttu-id="14736-112">Vyberte rozvržení sestavy, do které patří kód vykazování.</span><span class="sxs-lookup"><span data-stu-id="14736-112">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="14736-113">Toto rozvržení slouží k filtrování dostupných kódů vykazování pro kód DPH.</span><span class="sxs-lookup"><span data-stu-id="14736-113">This layout is used to filter the available reporting codes for a sales tax code.</span></span> <span data-ttu-id="14736-114">Každý kód DPH patří do období vyrovnání, které patří finančnímu úřadu používajícímu rozvržení sestavy.</span><span class="sxs-lookup"><span data-stu-id="14736-114">Each sales tax code belongs to a settlement period, which belongs to a Sales tax authority, which uses a report layout.</span></span>  
4. <span data-ttu-id="14736-115">Zadejte číslo do pole **Kód vykazování-**.</span><span class="sxs-lookup"><span data-stu-id="14736-115">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="14736-116">V poli **Text sestavy** zadejte popis, který se zobrazí v sestavách.</span><span class="sxs-lookup"><span data-stu-id="14736-116">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="14736-117">V poli **Stručný popis** zadejte popis pro interní účely.</span><span class="sxs-lookup"><span data-stu-id="14736-117">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="14736-118">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="14736-118">Click **Save**.</span></span>

