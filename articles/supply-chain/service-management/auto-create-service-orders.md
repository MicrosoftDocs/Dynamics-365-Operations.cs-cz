---
title: "Automaticky vytvářené servisní zakázky"
description: "Servisní zakázky generujete na základě servisních smluv pro platné období servisní smlouvy."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 0189a9f99ffbb6ed2387211ba9e3b9f3bcdb3b52
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---

# <a name="automatically-create-service-orders"></a><span data-ttu-id="f8f0a-103">Automaticky vytvářené servisní zakázky</span><span class="sxs-lookup"><span data-stu-id="f8f0a-103">Automatically create service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f8f0a-104">Servisní zakázky generujete na základě servisních smluv pro platné období servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="f8f0a-104">You can generate service orders that are based on a service agreement for the valid period of the service agreement.</span></span>

<span data-ttu-id="f8f0a-105">Všechny servisní zakázky, které generujete ze servisní smlouvy, jsou k dané servisní smlouvě přiřazeny.</span><span class="sxs-lookup"><span data-stu-id="f8f0a-105">The service orders that you generate from a service agreement are all attached to the service agreement.</span></span>

<span data-ttu-id="f8f0a-106">Servisní objednávky jsou automaticky generovány z následujících nastavení:</span><span class="sxs-lookup"><span data-stu-id="f8f0a-106">Service orders are generated automatically from the following settings:</span></span>

  - <span data-ttu-id="f8f0a-107">Jedná se o interval servisní smlouvy nastavený na řádcích servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="f8f0a-107">The service agreement interval that is set up in the service agreement lines.</span></span> <span data-ttu-id="f8f0a-108">Interval servisní smlouvy indikuje frekvenci, s jakou jsou vytvářeny řádky servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="f8f0a-108">The service agreement interval indicates the frequency that service-order lines are created.</span></span> <span data-ttu-id="f8f0a-109">Další informace o servisních intervalech naleznete v tématu [servisní intervaly](service-intervals.md).</span><span class="sxs-lookup"><span data-stu-id="f8f0a-109">For more information, see [Service intervals](service-intervals.md).</span></span>

  - <span data-ttu-id="f8f0a-110">Jedná se o období zadané za účelem definování servisního období v polích **Od data** a **Do data** ve formuláři **Vytvořit servisní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="f8f0a-110">The period that you specify to define the service period in the **From date** and **To date** fields in the **Create service orders** form.</span></span> <span data-ttu-id="f8f0a-111">Další informace naleznete v tématu [Automatické vytváření servisních zakázek](create-service-orders-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="f8f0a-111">For more information, see [Create service orders automatically](create-service-orders-automatically.md).</span></span>

  - <span data-ttu-id="f8f0a-112">Možnost **Kombinovat servisní zakázky** v záhlaví servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="f8f0a-112">The **Combine service orders** option on the service agreement header.</span></span> <span data-ttu-id="f8f0a-113">Tato možnost definuje, zda jsou řádky servisní zakázky generovány v servisní smlouvě, a slučuje servisní zakázky podle zaměstnance, servisní úlohy, předmětu servisu nebo servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="f8f0a-113">This option defines whether service order lines generated from a service agreement, combines service orders according to employee, service task, service object, or service agreement.</span></span> <span data-ttu-id="f8f0a-114">Další informace o kombinování servisních zakázek naleznete v tématu [Kombinování servisních zakázek](combine-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="f8f0a-114">For more information, see [Combine service orders](combine-service-orders.md).</span></span>

  - <span data-ttu-id="f8f0a-115">Jedná se o možnost **Časové okno** na řádku servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="f8f0a-115">The **Time window** option on the service agreement line.</span></span> <span data-ttu-id="f8f0a-116">Dané časové okno definuje, jak daleko lze přesunout řádek servisní zakázky ve vztahu k jeho vypočtenému datu.</span><span class="sxs-lookup"><span data-stu-id="f8f0a-116">The time window defines how far a service order line can move with regard to its calculated date.</span></span> <span data-ttu-id="f8f0a-117">Další informace naleznete v tématu [Časová okna](time-windows.md)..</span><span class="sxs-lookup"><span data-stu-id="f8f0a-117">For more information, see [Time windows](time-windows.md).</span></span>


> [!NOTE]
> <P><span data-ttu-id="f8f0a-118">Pokud není den zadaný pro servisní zakázku otevřen v kalendáři vybraném ve formuláři <STRONG>Parametry správy služby</STRONG>, obdržíte zprávu informující o konfliktu kalendáře.</span><span class="sxs-lookup"><span data-stu-id="f8f0a-118">If the day that is specified for a service order is not open in the calendar that you have selected in the <STRONG>Service management parameters</STRONG> form, a message will indicate that there is a calendar conflict.</span></span> <span data-ttu-id="f8f0a-119">Tuto zprávu můžete bezpečně ignorovat a k vytvoření servisní zakázky dojde, přestože je daný den v kalendáři zavřený.</span><span class="sxs-lookup"><span data-stu-id="f8f0a-119">You can safely ignore the message; the service order will be created, even though the day is closed on the calendar.</span></span></P>

## <a name="example-1"></a><span data-ttu-id="f8f0a-120">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="f8f0a-120">Example 1</span></span>

<span data-ttu-id="f8f0a-121">Servisní smlouva je platná od 1. ledna 2012 až 31. prosince 2012.</span><span class="sxs-lookup"><span data-stu-id="f8f0a-121">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="f8f0a-122">Pokud servisní období zadané ve formuláři **vytváření servisních zakázek** je od 1. listopad 2012 až 1. února 2013, vytvoří se servisní zakázky od 1. listopad 2012 až 31. prosince 2012.</span><span class="sxs-lookup"><span data-stu-id="f8f0a-122">If the service period that you specify in the **Create service orders** form is from November 1, 2012 until February 1, 2013, service orders are created from November 1, 2012 until December 31, 2012.</span></span>

## <a name="example-2"></a><span data-ttu-id="f8f0a-123">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="f8f0a-123">Example 2</span></span>

<span data-ttu-id="f8f0a-124">Servisní smlouva je platná od 1. ledna 2012 až 31. prosince 2012.</span><span class="sxs-lookup"><span data-stu-id="f8f0a-124">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="f8f0a-125">K této servisní smlouvě jsou připojeny dva řádky servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="f8f0a-125">Two service agreement lines are attached to the service agreement.</span></span> <span data-ttu-id="f8f0a-126">První řádek servisní smlouvy má počáteční datum 2. ledna 2012 a koncové datum 1. března 2012.</span><span class="sxs-lookup"><span data-stu-id="f8f0a-126">The first service agreement line has a starting date on January 2, 2012 and an ending date on March 1, 2012.</span></span> <span data-ttu-id="f8f0a-127">Druhý řádek servisní smlouvy má počáteční datum 1. dubna 2012 a koncové datum 31. prosince 2012.</span><span class="sxs-lookup"><span data-stu-id="f8f0a-127">The second service agreement line has a starting date on April 1, 2012 and an ending date on December 31, 2012.</span></span> <span data-ttu-id="f8f0a-128">Můžete určit období ve formuláři **vytváření servisních zakázek** od1. října 2012 do 31. prosince 2012.</span><span class="sxs-lookup"><span data-stu-id="f8f0a-128">You specify a period in the **Create service orders** form that is from October 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="f8f0a-129">Servisní zakázky budou tedy generovány pouze pro druhý řádek smlouvy, protože počáteční a koncové datum prvního řádku smlouvy se nachází mimo období zadané pro servisní zakázku.</span><span class="sxs-lookup"><span data-stu-id="f8f0a-129">Therefore, service orders are generated only for the second agreement line, because the starting date and ending date of the first agreement line are before the period that you specified for the service order.</span></span>

  



