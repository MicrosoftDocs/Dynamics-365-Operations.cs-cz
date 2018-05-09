--- 
title: "Nastavení skupin DPH a skupin DPH položky"
description: "Tento záznam úkolu vás provede nastavením DPH a skupin prodejní daně položky."
author: twheeloc
manager: AnnBe
ms.date: 11/10/2015
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
ms.openlocfilehash: 1214d86be5f8f5a5d1c65e25dfc0d4c046ff6e62
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="fa1e4-103">Nastavení skupin DPH a skupin DPH položky</span><span class="sxs-lookup"><span data-stu-id="fa1e4-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fa1e4-104">Tento záznam úkolu vás provede nastavením DPH a skupin prodejní daně položky.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="fa1e4-105">Skupiny DPH jsou skupiny kódů DPH, které jsou připojeny k odběratelům a dodavatelům.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="fa1e4-106">Dále jsou připojeny k účtům hlavní knihy pro transakce, které nejsou zaúčtovány pro konkrétního dodavatele ani odběratele.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="fa1e4-107">Skupiny prodejní daně položky jsou skupiny kódů DPH, které jsou připojeny k produktům používaným jako prostředky.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="fa1e4-108">DPH pro danou transakci se určuje podle kódů DPH zahrnutých ve skupině DPH a ve skupině DPH položky v transakci.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="fa1e4-109">DPH je možné vypočítat pouze pokud je vybrána skupina DPH i skupina DPH položky pro každou transakci, u níž je třeba vypočítat nebo zaznamenat DPH.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="fa1e4-110">Přejděte na Daň > Nepřímé daně > DPH > Skupiny DPH.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-110">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="fa1e4-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-111">Click New.</span></span>
3. <span data-ttu-id="fa1e4-112">V poli Skupina prodejní daně zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-112">In the Sales tax group field, type a value.</span></span>
4. <span data-ttu-id="fa1e4-113">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fa1e4-114">Přepněte rozšíření oddílu Nastavení.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-114">Toggle the expansion of the Setup section.</span></span>
6. <span data-ttu-id="fa1e4-115">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-115">Click Add.</span></span>
7. <span data-ttu-id="fa1e4-116">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="fa1e4-117">V poli Kód prodejní daně kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-117">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="fa1e4-118">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="fa1e4-119">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-119">Click Save.</span></span>
11. <span data-ttu-id="fa1e4-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-120">Close the page.</span></span>
12. <span data-ttu-id="fa1e4-121">Přejděte na Daň > Nepřímé daně > DPH > Skupiny prodejní daně položky.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-121">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
13. <span data-ttu-id="fa1e4-122">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-122">Click New.</span></span>
14. <span data-ttu-id="fa1e4-123">V poli Skupina DPH zboží zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-123">In the Item sales tax group field, type a value.</span></span>
15. <span data-ttu-id="fa1e4-124">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-124">In the Description field, type a value.</span></span>
16. <span data-ttu-id="fa1e4-125">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-125">Click Add.</span></span>
17. <span data-ttu-id="fa1e4-126">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="fa1e4-127">V poli Kód prodejní daně kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-127">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="fa1e4-128">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="fa1e4-129">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-129">Click Save.</span></span>


