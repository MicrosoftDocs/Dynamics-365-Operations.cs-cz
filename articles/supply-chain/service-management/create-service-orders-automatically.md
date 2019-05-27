---
title: Automatické vytvoření servisních zakázek
description: Servisní zakázky můžete vytvářet pro jednu nebo více servisních smluv.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee68190b117b974ff4131f5d2237d138cac1fda3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552269"
---
# <a name="create-service-orders-automatically"></a><span data-ttu-id="7464e-103">Automatické vytvoření servisních zakázek</span><span class="sxs-lookup"><span data-stu-id="7464e-103">Create service orders automatically</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="7464e-104">Servisní zakázky můžete vytvářet pro jednu nebo více servisních smluv.</span><span class="sxs-lookup"><span data-stu-id="7464e-104">You can create service orders for one service agreement or for several service agreements.</span></span> <span data-ttu-id="7464e-105">Po jejich vytvoření můžete servisní zakázky zobrazit ve formuláři **Servisní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="7464e-105">When they are created, you can view your service orders in the **Service orders** form.</span></span>

<span data-ttu-id="7464e-106">Servisní zakázky se vytvářejí pouze pro platné období servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="7464e-106">Service orders are created only for the valid period of the service agreement.</span></span> <span data-ttu-id="7464e-107">Jestliže interval, který jste stanovili ve formuláři **Vytvořit servisní zakázky**, spadá do období před počátečním datem nebo po koncovém datu servisní smlouvy, vytvoří se servisní zakázky pouze pro část intervalu, která spadá do intervalu servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="7464e-107">If the interval that you specify in the **Create service orders** form is before the starting date or after the ending date of the service agreement, service orders are created only for the part of the interval that is within the service agreement dates.</span></span>

<span data-ttu-id="7464e-108">Pokud ručně nebo automaticky vytváříte servisní zakázky v řádku servisní smlouvy, musí servisní zakázka spadat do časového období, které určuje počáteční a koncové datum definované pro daný řádek. Výjimkou je případ, kdy v řádku neuvedete koncové datum.</span><span class="sxs-lookup"><span data-stu-id="7464e-108">When you create service orders manually or automatically from the service agreement line, the service order must be in the time interval that is defined by the starting and ending dates for the line, unless you do not specify an ending date on the line.</span></span>

## <a name="create-service-orders-automatically-for-a-service-agreement"></a><span data-ttu-id="7464e-109">Automatické vytvoření servisních zakázek pro servisní smlouvu</span><span class="sxs-lookup"><span data-stu-id="7464e-109">Create service orders automatically for a service agreement</span></span>

1.  <span data-ttu-id="7464e-110">Klikněte na **Správa servisu** \> **Obecné** \> **Servisní smlouvy** \> **Servisní smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="7464e-110">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="7464e-111">Vyberte servisní smlouvu.</span><span class="sxs-lookup"><span data-stu-id="7464e-111">Select a service agreement.</span></span>

3.  <span data-ttu-id="7464e-112">Klepněte na kartu **dodat** a klikněte na **plánované servisní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="7464e-112">Click the **Deliver** tab, and then click **Planned service orders**.</span></span>

4.  <span data-ttu-id="7464e-113">Servisní období určete zadáním dat v polích **Od data** a **Do data**.</span><span class="sxs-lookup"><span data-stu-id="7464e-113">Specify dates in the **From date** and **To date** fields to define the service period.</span></span>

5.  <span data-ttu-id="7464e-114">Chcete-li zobrazit seznam servisních zakázek, které jsou vytvořeny, zaškrtněte políčko **Zobrazit informační protokol**.</span><span class="sxs-lookup"><span data-stu-id="7464e-114">Select the **Show Infolog** check box to display a list of the service orders that are created.</span></span>

6.  <span data-ttu-id="7464e-115">Vyberte typy transakcí ve skupině polí **Zahrnout typy transakcí**.</span><span class="sxs-lookup"><span data-stu-id="7464e-115">Select transaction types in the **Include transaction types** field group.</span></span> <span data-ttu-id="7464e-116">Typy transakcí představují řádky, které jsou vytvořeny v servisní smlouvě, a každý vybraný typ transakce generuje několik servisních zakázek v závislosti na servisním intervalu stanoveném na řádku servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="7464e-116">The transaction types represent the lines that are created in the service agreement, and each transaction type that you select generates several service orders, depending on the service interval that is specified on the service agreement line.</span></span>

7.  <span data-ttu-id="7464e-117">Chcete-li vytvořit libovolné servisní zakázky, které chybějí v souvislé řadě servisních zakázek, zaškrtněte políčko **Nepřetržité**.</span><span class="sxs-lookup"><span data-stu-id="7464e-117">To create any service orders that are missing from continuous series of service orders, select the **Continuous** check box.</span></span>

8.  <span data-ttu-id="7464e-118">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="7464e-118">Click **OK**.</span></span>

## <a name="create-service-orders-automatically-for-several-service-agreements"></a><span data-ttu-id="7464e-119">Automatické vytvoření servisních zakázek pro několik servisních smluv</span><span class="sxs-lookup"><span data-stu-id="7464e-119">Create service orders automatically for several service agreements</span></span>

1.  <span data-ttu-id="7464e-120">Klepněte na tlačítko **řízení servisu** \> **Periodicky** \> **servisní zakázky** \> **Vytvořit servisní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="7464e-120">Click **Service management** \> **Periodic** \> **Service orders** \> **Create service orders**.</span></span>

2.  <span data-ttu-id="7464e-121">Klepněte na tlačítko **Vybrat** k provedení výběru hodnot, které chcete přidat nebo odebrat při vytváření servisních zakázek.</span><span class="sxs-lookup"><span data-stu-id="7464e-121">Click **Select** to make selections to add or remove criteria to use to create service orders.</span></span>

3.  <span data-ttu-id="7464e-122">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="7464e-122">Click **OK**.</span></span>

## <a name="see-also"></a><span data-ttu-id="7464e-123">Viz také</span><span class="sxs-lookup"><span data-stu-id="7464e-123">See also</span></span>

[<span data-ttu-id="7464e-124">Servisní zakázky</span><span class="sxs-lookup"><span data-stu-id="7464e-124">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="7464e-125">Automaticky vytvářené servisní zakázky</span><span class="sxs-lookup"><span data-stu-id="7464e-125">Automatically creating service orders</span></span>](auto-create-service-orders.md)

  


