---
title: Vytvoření vztahů předmětů servisu
description: Toto téma popisuje postup vytvoření vztahů předmětů servisu pro servisní smlouvu a zakázku.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 380514b6e95292597d3eb52ce191d1e282e154ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965898"
---
# <a name="create-service-object-relations"></a><span data-ttu-id="6c7ef-103">Vytvoření vztahů předmětů servisu</span><span class="sxs-lookup"><span data-stu-id="6c7ef-103">Create service object relations</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6c7ef-104">Toto téma popisuje postup vytvoření vztahů předmětů servisu pro servisní smlouvu a zakázku.</span><span class="sxs-lookup"><span data-stu-id="6c7ef-104">This topic describes how to create service object relations for a service agreement and a service order.</span></span> <span data-ttu-id="6c7ef-105">Při vytvoření vztahu předmětu servisu připojíte předmět servisu k servisní smlouvě nebo zakázce.</span><span class="sxs-lookup"><span data-stu-id="6c7ef-105">When you a create service object relation, you associate the service object to a service agreement or service order.</span></span> <span data-ttu-id="6c7ef-106">Pokud zákazník vyžádá servis položky, která je předmět servisu, můžete vybrat předmět servisu ze seznamu vztahů předmětu servisu.</span><span class="sxs-lookup"><span data-stu-id="6c7ef-106">When a customer requests service for an item that is a service object, you can select the service object from the list of service object relations.</span></span>

## <a name="create-a-service-object-relation-for-a-service-agreement"></a><span data-ttu-id="6c7ef-107">Vytvoření vztahu předmětů služeb pro servisní smlouvu</span><span class="sxs-lookup"><span data-stu-id="6c7ef-107">Create a service object relation for a service agreement</span></span>

<span data-ttu-id="6c7ef-108">Pomocí následujících kroků můžete vytvořit vztah předmětu servisu pro servisní smlouvu:</span><span class="sxs-lookup"><span data-stu-id="6c7ef-108">Use the following steps to create a service object relation for a service agreement:</span></span>

1.  <span data-ttu-id="6c7ef-109">Klikněte na **Správa servisu** \> **Obecné** \> **Servisní smlouvy** \> **Servisní smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="6c7ef-109">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="6c7ef-110">V seznamu **Servisní smlouvy** vyberte existující servisní smlouvu nebo klepněte na tlačítko **Nová** a vytvořte novou servisní smlouvu.</span><span class="sxs-lookup"><span data-stu-id="6c7ef-110">In the **Service agreements** list, select an existing service agreement, or click **New** to create a new service agreement.</span></span>

3.  <span data-ttu-id="6c7ef-111">Ve formuláři **Servisní smlouvy** v **podokně akcí** na kartě **Servisní smlouva** ve skupině **Vztahy** klikněte na **Objekty servisu**.</span><span class="sxs-lookup"><span data-stu-id="6c7ef-111">In the **Service agreements** form, on the **Action Pane**, on the **Service agreement** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="6c7ef-112">Ve formuláři **Objekty servisu** klikněte na možnost **Nový** a vyberte předmět servisu pro tuto servisní smlouvu.</span><span class="sxs-lookup"><span data-stu-id="6c7ef-112">In the **Service objects** form, click **New**, and then select a service object for this service agreement.</span></span>

5.  <span data-ttu-id="6c7ef-113">Chcete-li k servisní smlouvě připojit šablony kusovníku, klepněte na položku **Funkce** a vyberte **Připojit kusovník šablony**.</span><span class="sxs-lookup"><span data-stu-id="6c7ef-113">To assign a template bill of materials (BOM) to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="6c7ef-114">Ve formuláři **Vybrat kusovník šablony** v poli **Kusovník šablony** vyberte šablonu.</span><span class="sxs-lookup"><span data-stu-id="6c7ef-114">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 

## <a name="create-a-service-object-relation-for-a-service-order"></a><span data-ttu-id="6c7ef-115">Vytvoření vztahu předmětů služeb pro servisní objednávku</span><span class="sxs-lookup"><span data-stu-id="6c7ef-115">Create a service object relation for a service order</span></span>

<span data-ttu-id="6c7ef-116">Pomocí následujících kroků můžete vytvořit vztah předmětu servisu pro servisní objednávku:</span><span class="sxs-lookup"><span data-stu-id="6c7ef-116">Use the following steps to create a service object relation for a service order:</span></span>

1.  <span data-ttu-id="6c7ef-117">Klikněte na uzel **Řízení služeb** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="6c7ef-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="6c7ef-118">V seznamu **Servisní zakázky** vyberte existující servisní zakázku nebo vytvořte novou zakázku.</span><span class="sxs-lookup"><span data-stu-id="6c7ef-118">In the **Service orders** list, select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="6c7ef-119">Ve formuláři **Servisní zakázky** v **podokně akcí** na kartě **Servisní zakázka** ve skupině **Vztahy** klikněte na **Objekty servisu**.</span><span class="sxs-lookup"><span data-stu-id="6c7ef-119">In the **Service orders** form, on the **Action Pane**, on the **Service order** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="6c7ef-120">Ve formuláři **Objekty servisu** klikněte na možnost **Nový** a vyberte předmět servisu pro tuto servisní zakázku.</span><span class="sxs-lookup"><span data-stu-id="6c7ef-120">In the **Service objects** form, click **New**, and then select a service object for this service order.</span></span>

5.  <span data-ttu-id="6c7ef-121">Chcete-li k servisní smlouvě připojit šablony kusovníku, klepněte na položku **Funkce** a vyberte **Připojit kusovník šablony**.</span><span class="sxs-lookup"><span data-stu-id="6c7ef-121">To assign a template BOM to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="6c7ef-122">Ve formuláři **Vybrat kusovník šablony** v poli **Kusovník šablony** vyberte šablonu.</span><span class="sxs-lookup"><span data-stu-id="6c7ef-122">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 


## <a name="see-also"></a><span data-ttu-id="6c7ef-123">Viz také</span><span class="sxs-lookup"><span data-stu-id="6c7ef-123">See also</span></span>

[<span data-ttu-id="6c7ef-124">Přehled předmětů servisu</span><span class="sxs-lookup"><span data-stu-id="6c7ef-124">Service objects overview</span></span>](service-objects.md)

[<span data-ttu-id="6c7ef-125">Vztahy předmětu servisu</span><span class="sxs-lookup"><span data-stu-id="6c7ef-125">Service object relations</span></span>](service-object-relations.md)

[<span data-ttu-id="6c7ef-126">Kusovníky šablony</span><span class="sxs-lookup"><span data-stu-id="6c7ef-126">Template BOMs</span></span>](template-boms.md)

  


