---
title: Nastavení skupin DPH a skupin DPH položky
description: Tento záznam úkolu vás provede nastavením DPH a skupin prodejní daně položky.
author: twheeloc
manager: AnnBe
ms.date: 07-01-2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b539129e62b9b0b10df1f505cbfec5c1143138
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141619"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="edc99-103">Nastavení skupin DPH a skupin DPH položky</span><span class="sxs-lookup"><span data-stu-id="edc99-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="edc99-104">Tento záznam úkolu vás provede nastavením DPH a skupin prodejní daně položky.</span><span class="sxs-lookup"><span data-stu-id="edc99-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="edc99-105">Skupiny DPH jsou skupiny kódů DPH, které jsou připojeny k odběratelům a dodavatelům.</span><span class="sxs-lookup"><span data-stu-id="edc99-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="edc99-106">Dále jsou připojeny k účtům hlavní knihy pro transakce, které nejsou zaúčtovány pro konkrétního dodavatele ani odběratele.</span><span class="sxs-lookup"><span data-stu-id="edc99-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="edc99-107">Skupiny prodejní daně položky jsou skupiny kódů DPH, které jsou připojeny k produktům používaným jako prostředky.</span><span class="sxs-lookup"><span data-stu-id="edc99-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="edc99-108">DPH pro danou transakci se určuje podle kódů DPH zahrnutých ve skupině DPH a ve skupině DPH položky v transakci.</span><span class="sxs-lookup"><span data-stu-id="edc99-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="edc99-109">DPH je možné vypočítat pouze pokud je vybrána skupina DPH i skupina DPH položky pro každou transakci, u níž je třeba vypočítat nebo zaznamenat DPH.</span><span class="sxs-lookup"><span data-stu-id="edc99-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="edc99-110">Přejděte na **Navigační podokno > Moduly > Daň > Nepřímé daně > DPH > Skupiny DPH**.</span><span class="sxs-lookup"><span data-stu-id="edc99-110">Go to **Navigation pane > Modules > Tax > Indirect taxes > Sales tax > Sales tax groups**.</span></span>
2. <span data-ttu-id="edc99-111">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="edc99-111">Click **New**.</span></span>
3. <span data-ttu-id="edc99-112">V poli **Skupina prodejní daně** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="edc99-112">In the **Sales tax group** field, type a value.</span></span>
4. <span data-ttu-id="edc99-113">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="edc99-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="edc99-114">Přepněte rozšíření oddílu **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="edc99-114">Toggle the expansion of the **Setup** section.</span></span>
6. <span data-ttu-id="edc99-115">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="edc99-115">Click **Add**.</span></span>
7. <span data-ttu-id="edc99-116">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="edc99-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="edc99-117">V poli **Kód prodejní daně** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="edc99-117">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="edc99-118">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="edc99-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="edc99-119">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="edc99-119">Click **Save**.</span></span>
11. <span data-ttu-id="edc99-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="edc99-120">Close the page.</span></span>
12. <span data-ttu-id="edc99-121">Přejděte na **Daň > Nepřímé daně > DPH > Skupiny prodejní daně položky**.</span><span class="sxs-lookup"><span data-stu-id="edc99-121">Go to **Tax > Indirect taxes > Sales tax > Item sales tax groups**.</span></span>
13. <span data-ttu-id="edc99-122">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="edc99-122">Click **New**.</span></span>
14. <span data-ttu-id="edc99-123">V poli **Skupina DPH zboží** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="edc99-123">In the **Item sales tax group** field, type a value.</span></span>
15. <span data-ttu-id="edc99-124">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="edc99-124">In the **Description** field, type a value.</span></span>
16. <span data-ttu-id="edc99-125">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="edc99-125">Click **Add**.</span></span>
17. <span data-ttu-id="edc99-126">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="edc99-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="edc99-127">V poli **Kód prodejní daně** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="edc99-127">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="edc99-128">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="edc99-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="edc99-129">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="edc99-129">Click **Save**.</span></span>

