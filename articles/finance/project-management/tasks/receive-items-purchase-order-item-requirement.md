---
title: Přijetí položek na nákupní objednávce z požadavku na položku
description: Toto téma vysvětluje, jak přijmout položky na nákupní objednávce z požadavku na položku.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1f288a47f952a30d98a4a5b96409dc53f880d41d
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139043"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="0eb5e-103">Přijetí položek na nákupní objednávce z požadavku na položku</span><span class="sxs-lookup"><span data-stu-id="0eb5e-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0eb5e-104">Toto téma vysvětluje, jak přijmout položky na nákupní objednávce z požadavku na položku.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="0eb5e-105">Použitím požadavků zboží namísto transakcí zboží můžete naplánovat dodávku těsně před vlastním použitím zboží, vytvořit prodejní objednávku, zahrnout zboží do rámce obchodní smlouvy nebo zahrnout požadavek na zboží do provozního plánování.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="0eb5e-106">Tato úloha používá sadu dat USSI.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="0eb5e-107">V navigačním podokně přejděte na **Moduly > Řízení projektů a účetnictví > Projekty > Všechny projekty**.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="0eb5e-108">Vyberte odkaz na požadovaném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="0eb5e-109">V podokně akcí zvolte **Plán**.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="0eb5e-110">Vyberte **Požadavky položek**</span><span class="sxs-lookup"><span data-stu-id="0eb5e-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="0eb5e-111">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-111">Select **New**.</span></span>
6. <span data-ttu-id="0eb5e-112">V novém řádku vložte nebo vyberte hodnotu v poli **Číslo položky**.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="0eb5e-113">Zadejte číslo do pole **Množství**.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="0eb5e-114">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-114">Select **Save**.</span></span>
9. <span data-ttu-id="0eb5e-115">V podokně akcí vyberte **Spravovat**.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="0eb5e-116">Vyberte **Funkce**.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-116">Select **Functions**.</span></span>
11. <span data-ttu-id="0eb5e-117">Vyberte **Vytvořit nákupní objednávku**.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="0eb5e-118">Zaškrtněte políčko **Zahrnout vše**.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="0eb5e-119">V poli **Účet dodavatele** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="0eb5e-120">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-120">Select **OK**.</span></span>
15. <span data-ttu-id="0eb5e-121">V navigačním podokně přejděte na **Moduly > Závazky > Nákupní objednávky > Všechny nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="0eb5e-122">Vyberte odkaz na požadovaném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="0eb5e-123">V podokně akcí klikněte na možnost **Zakoupit**.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="0eb5e-124">Vyberte **Potvrdit**.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="0eb5e-125">V podokně akcí klikněte na možnost **Přijmout**.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="0eb5e-126">Vyberte **Příjemka produktu**.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="0eb5e-127">Zadejte hodnotu do pole **Příjemka produktu**.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="0eb5e-128">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="0eb5e-128">Select **OK**.</span></span>

