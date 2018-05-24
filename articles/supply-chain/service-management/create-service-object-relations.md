---
title: "Vytvoření vztahů předmětů servisu"
description: "Toto téma popisuje postup vytvoření vztahů předmětů servisu pro servisní smlouvu a zakázku."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c27070436139f784af690900a3f1ab108a809d03
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="create-service-object-relations"></a><span data-ttu-id="c1c80-103">Vytvoření vztahů předmětů servisu</span><span class="sxs-lookup"><span data-stu-id="c1c80-103">Create service object relations</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="c1c80-104">Toto téma popisuje postup vytvoření vztahů předmětů servisu pro servisní smlouvu a zakázku.</span><span class="sxs-lookup"><span data-stu-id="c1c80-104">This topic describes how to create service object relations for a service agreement and a service order.</span></span> <span data-ttu-id="c1c80-105">Při vytvoření vztahu předmětu servisu připojíte předmět servisu k servisní smlouvě nebo zakázce.</span><span class="sxs-lookup"><span data-stu-id="c1c80-105">When you a create service object relation, you associate the service object to a service agreement or service order.</span></span> <span data-ttu-id="c1c80-106">Pokud zákazník vyžádá servis položky, která je předmět servisu, můžete vybrat předmět servisu ze seznamu vztahů předmětu servisu.</span><span class="sxs-lookup"><span data-stu-id="c1c80-106">When a customer requests service for an item that is a service object, you can select the service object from the list of service object relations.</span></span>

## <a name="create-a-service-object-relation-for-a-service-agreement"></a><span data-ttu-id="c1c80-107">Vytvoření vztahu předmětů služeb pro servisní smlouvu</span><span class="sxs-lookup"><span data-stu-id="c1c80-107">Create a service object relation for a service agreement</span></span>

<span data-ttu-id="c1c80-108">Pomocí následujících kroků můžete vytvořit vztah předmětu servisu pro servisní smlouvu:</span><span class="sxs-lookup"><span data-stu-id="c1c80-108">Use the following steps to create a service object relation for a service agreement:</span></span>

1.  <span data-ttu-id="c1c80-109">Klikněte na **Správa servisu** \> **Obecné** \> **Servisní smlouvy** \> **Servisní smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="c1c80-109">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="c1c80-110">V seznamu **Servisní smlouvy** vyberte existující servisní smlouvu nebo klepněte na tlačítko **Nová** a vytvořte novou servisní smlouvu.</span><span class="sxs-lookup"><span data-stu-id="c1c80-110">In the **Service agreements** list, select an existing service agreement, or click **New** to create a new service agreement.</span></span>

3.  <span data-ttu-id="c1c80-111">Ve formuláři **Servisní smlouvy** v **podokně akcí** na kartě **Servisní smlouva** ve skupině **Vztahy** klikněte na **Objekty servisu**.</span><span class="sxs-lookup"><span data-stu-id="c1c80-111">In the **Service agreements** form, on the **Action Pane**, on the **Service agreement** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="c1c80-112">Ve formuláři **Objekty servisu** klikněte na možnost **Nový** a vyberte předmět servisu pro tuto servisní smlouvu.</span><span class="sxs-lookup"><span data-stu-id="c1c80-112">In the **Service objects** form, click **New**, and then select a service object for this service agreement.</span></span>

5.  <span data-ttu-id="c1c80-113">Chcete-li k servisní smlouvě připojit šablony kusovníku, klepněte na položku **Funkce** a vyberte **Připojit kusovník šablony**.</span><span class="sxs-lookup"><span data-stu-id="c1c80-113">To assign a template bill of materials (BOM) to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="c1c80-114">Ve formuláři **Vybrat kusovník šablony** v poli **Kusovník šablony** vyberte šablonu.</span><span class="sxs-lookup"><span data-stu-id="c1c80-114">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 

## <a name="create-a-service-object-relation-for-a-service-order"></a><span data-ttu-id="c1c80-115">Vytvoření vztahu předmětů služeb pro servisní objednávku</span><span class="sxs-lookup"><span data-stu-id="c1c80-115">Create a service object relation for a service order</span></span>

<span data-ttu-id="c1c80-116">Pomocí následujících kroků můžete vytvořit vztah předmětu servisu pro servisní objednávku:</span><span class="sxs-lookup"><span data-stu-id="c1c80-116">Use the following steps to create a service object relation for a service order:</span></span>

1.  <span data-ttu-id="c1c80-117">Klikněte na uzel **Řízení služeb** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="c1c80-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="c1c80-118">V seznamu **Servisní zakázky** vyberte existující servisní zakázku nebo vytvořte novou zakázku.</span><span class="sxs-lookup"><span data-stu-id="c1c80-118">In the **Service orders** list, select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="c1c80-119">Ve formuláři **Servisní zakázky** v **podokně akcí** na kartě **Servisní zakázka** ve skupině **Vztahy** klikněte na **Objekty servisu**.</span><span class="sxs-lookup"><span data-stu-id="c1c80-119">In the **Service orders** form, on the **Action Pane**, on the **Service order** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="c1c80-120">Ve formuláři **Objekty servisu** klikněte na možnost **Nový** a vyberte předmět servisu pro tuto servisní zakázku.</span><span class="sxs-lookup"><span data-stu-id="c1c80-120">In the **Service objects** form, click **New**, and then select a service object for this service order.</span></span>

5.  <span data-ttu-id="c1c80-121">Chcete-li k servisní smlouvě připojit šablony kusovníku, klepněte na položku **Funkce** a vyberte **Připojit kusovník šablony**.</span><span class="sxs-lookup"><span data-stu-id="c1c80-121">To assign a template BOM to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="c1c80-122">Ve formuláři **Vybrat kusovník šablony** v poli **Kusovník šablony** vyberte šablonu.</span><span class="sxs-lookup"><span data-stu-id="c1c80-122">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 


## <a name="see-also"></a><span data-ttu-id="c1c80-123">Viz také</span><span class="sxs-lookup"><span data-stu-id="c1c80-123">See also</span></span>

[<span data-ttu-id="c1c80-124">Předměty servisu</span><span class="sxs-lookup"><span data-stu-id="c1c80-124">Service objects</span></span>](service-objects.md)

[<span data-ttu-id="c1c80-125">vztahy předmětu servisu</span><span class="sxs-lookup"><span data-stu-id="c1c80-125">service object relations</span></span>](service-object-relations.md)

[<span data-ttu-id="c1c80-126">Kusovníky šablony</span><span class="sxs-lookup"><span data-stu-id="c1c80-126">Template BOMs</span></span>](template-boms.md)

  



