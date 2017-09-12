--- 
title: "Vytvoření metody hodnocení pro požadavky na nabídku"
description: "Tato procedura popisuje způsob vytváření metody hodnocení."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6d72678db60254801c6c899f4d405f1c59de8d65
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-scoring-method-for-rfqs"></a><span data-ttu-id="0860f-103">Vytvoření metody hodnocení pro požadavky na nabídku</span><span class="sxs-lookup"><span data-stu-id="0860f-103">Create a scoring method for RFQs</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0860f-104">Tato procedura popisuje způsob vytváření metody hodnocení.</span><span class="sxs-lookup"><span data-stu-id="0860f-104">This procedure shows you how to create a scoring method.</span></span> <span data-ttu-id="0860f-105">Metoda hodnocení je sada kritérií, které lze použít k porovnání nabídek, které jsou odesílány v odpovědi na požadavek na nabídku.</span><span class="sxs-lookup"><span data-stu-id="0860f-105">A scoring method is a set of criteria that can be used to compare bids that are sent in reply to a request for quotation (RFQ).</span></span> <span data-ttu-id="0860f-106">Můžete chtít například ohodnotit dřívější výkonnost dodavatele nebo zhodnotit, zda je společnost šetrná vůči životnímu prostředí či zda se s ní dobře spolupracuje nebo srovnat hodnocení na základě ceny.</span><span class="sxs-lookup"><span data-stu-id="0860f-106">For example, you might want to rate a vendor on past performance, or rate whether the company is environmentally friendly or a good collaborator, or you might want to compare bids based on price.</span></span> <span data-ttu-id="0860f-107">Metodu hodnocení lze přidružit k typu oslovení jako výchozí metodu hodnocení pro požadavek na nabídku tohoto typu.</span><span class="sxs-lookup"><span data-stu-id="0860f-107">The scoring method can be associated with a solicitation type as the default scoring method for RFQs of that type.</span></span> <span data-ttu-id="0860f-108">Tyto úkoly obvykle provádějí vedoucí nákupu.</span><span class="sxs-lookup"><span data-stu-id="0860f-108">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="0860f-109">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="0860f-109">You can use this procedure in demo data company USMF or on your own data.</span></span>

1. <span data-ttu-id="0860f-110">Přejděte na Zásobování a zdroje > Nastavení > Požadavek na nabídku > Metoda hodnocení.</span><span class="sxs-lookup"><span data-stu-id="0860f-110">Go to Procurement and sourcing > Setup > Request for quotation > Scoring method.</span></span>
2. <span data-ttu-id="0860f-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="0860f-111">Click New.</span></span>
3. <span data-ttu-id="0860f-112">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="0860f-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="0860f-113">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="0860f-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0860f-114">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="0860f-114">Click Save.</span></span>
6. <span data-ttu-id="0860f-115">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="0860f-115">Click New.</span></span>
7. <span data-ttu-id="0860f-116">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="0860f-116">In the Name field, type a value.</span></span>
8. <span data-ttu-id="0860f-117">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="0860f-117">In the Description field, type a value.</span></span>
    * <span data-ttu-id="0860f-118">Tento popis se zobrazí spolu s názvem metody hodnocení po výběru metody hodnocení pro požadavek na nabídku.</span><span class="sxs-lookup"><span data-stu-id="0860f-118">This description is shown along with the scoring method name when a scoring method is selected for an RFQ.</span></span>  
9. <span data-ttu-id="0860f-119">V poli Rozsah od zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="0860f-119">In the Range from field, enter a number.</span></span>
    * <span data-ttu-id="0860f-120">Rozsah omezuje možnosti, které může pracovník zásobování zadat jako hodnocení.</span><span class="sxs-lookup"><span data-stu-id="0860f-120">The range limits what the procurement professional can enter as a score.</span></span> <span data-ttu-id="0860f-121">Pokud existuje více kritérií hodnocení v požadavku na nabídku, zadaná hodnocení jsou navzájem přidána a je k dispozici součet umožňující srovnání nabídek.</span><span class="sxs-lookup"><span data-stu-id="0860f-121">When there are multiple scoring criteria on an RFQ, the scores that have been entered are added to each other and the sum is made available to allow the bids to be compared.</span></span>  
10. <span data-ttu-id="0860f-122">V poli Rozsah do zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="0860f-122">In the Range to field, enter a number.</span></span>
11. <span data-ttu-id="0860f-123">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="0860f-123">Click New.</span></span>
12. <span data-ttu-id="0860f-124">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="0860f-124">In the Name field, type a value.</span></span>
13. <span data-ttu-id="0860f-125">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="0860f-125">In the Description field, type a value.</span></span>
14. <span data-ttu-id="0860f-126">V poli Rozsah od zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="0860f-126">In the Range from field, enter a number.</span></span>
15. <span data-ttu-id="0860f-127">V poli Rozsah do zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="0860f-127">In the Range to field, enter a number.</span></span>


