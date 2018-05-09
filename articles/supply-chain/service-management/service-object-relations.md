---
title: "Vztahy předmětu servisu"
description: "Mezi předmětem servisu a servisní smlouvou či zakázkou můžete vytvářet vztahy předmětů servisu."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectRelation
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
ms.openlocfilehash: 90c16653dee0614beaad8e4693c012b67a54b297
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="service-object-relations"></a><span data-ttu-id="91199-103">Vztahy předmětu servisu</span><span class="sxs-lookup"><span data-stu-id="91199-103">Service object relations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91199-104">Mezi předmětem servisu a servisní smlouvou či zakázkou můžete vytvářet vztahy předmětů servisu.</span><span class="sxs-lookup"><span data-stu-id="91199-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="91199-105">Při vytvoření vztahu připojíte předmět servisu k servisní smlouvě nebo zakázce.</span><span class="sxs-lookup"><span data-stu-id="91199-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="91199-106">Po vytvoření vztahu můžete předmět servisu připojit k libovolným řádkům servisní smlouvy nebo zakázky.</span><span class="sxs-lookup"><span data-stu-id="91199-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="91199-107">Kusovníky šablony</span><span class="sxs-lookup"><span data-stu-id="91199-107">Template BOMs</span></span>

<span data-ttu-id="91199-108">Je také možné určit šablonu kusovníku pro vztah předmětu.</span><span class="sxs-lookup"><span data-stu-id="91199-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="91199-109">Šablona kusovníku představuje kusovník předmětu, u kterého provádíte servis.</span><span class="sxs-lookup"><span data-stu-id="91199-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="91199-110">Jestliže při servisním zásahu vyměníte součástku předmětu servisu, můžete tuto změnu zaregistrovat do servisního kusovníku ve formuláři Předměty servisu.</span><span class="sxs-lookup"><span data-stu-id="91199-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="91199-111">Příklad</span><span class="sxs-lookup"><span data-stu-id="91199-111">Example</span></span>

<span data-ttu-id="91199-112">Vytváříte servisní smlouvu pro servis dvou výtahů u zákazníka.</span><span class="sxs-lookup"><span data-stu-id="91199-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="91199-113">Identifikátor servisní smlouvy je SAL-001.</span><span class="sxs-lookup"><span data-stu-id="91199-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="91199-114">Výtahy jsou nastaveny ve formuláři Předměty servisu jako předměty EL-S/1000 a EL-L/1000.</span><span class="sxs-lookup"><span data-stu-id="91199-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="91199-115">Předměty servisu EL-S/1000 a EL-L/1000 jste připojili k servisní smlouvě.</span><span class="sxs-lookup"><span data-stu-id="91199-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="91199-116">Chcete zaregistrovat změny kusovníku předmětu servisu, ke kterým došlo při výměně součástek předmětu. Připojte servisní kusovník ke vztahu předmětu servisu tak, jak je popsáno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="91199-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="91199-117">Předmět servisu</span><span class="sxs-lookup"><span data-stu-id="91199-117">Service object</span></span> | <span data-ttu-id="91199-118">Vztah – servisní smlouva</span><span class="sxs-lookup"><span data-stu-id="91199-118">Relation – Service agreement</span></span> | <span data-ttu-id="91199-119">Servisní kusovník</span><span class="sxs-lookup"><span data-stu-id="91199-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="91199-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="91199-120">EL-S/1000</span></span>      | <span data-ttu-id="91199-121">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="91199-121">ID SAL-001</span></span>                   | <span data-ttu-id="91199-122">BOM-EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="91199-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="91199-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="91199-123">EL-L/1000</span></span>      | <span data-ttu-id="91199-124">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="91199-124">ID SAL-001</span></span>                   | <span data-ttu-id="91199-125">BOM-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="91199-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="91199-126">Protože smlouva obsahuje vztahy předmětů servisu, můžete nyní vytvořit řádky servisní smlouvy s těmito předměty podle popisu zobrazeného v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="91199-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="91199-127">typ transakce</span><span class="sxs-lookup"><span data-stu-id="91199-127">Transaction type</span></span> | <span data-ttu-id="91199-128">Kategorie</span><span class="sxs-lookup"><span data-stu-id="91199-128">Category</span></span>           | <span data-ttu-id="91199-129">Předmět servisu</span><span class="sxs-lookup"><span data-stu-id="91199-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="91199-130">Hodina</span><span class="sxs-lookup"><span data-stu-id="91199-130">Hour</span></span>             | <span data-ttu-id="91199-131">Kontrola</span><span class="sxs-lookup"><span data-stu-id="91199-131">Inspection</span></span>         | <span data-ttu-id="91199-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="91199-132">EL-S/1000</span></span>      |
| <span data-ttu-id="91199-133">Hodina</span><span class="sxs-lookup"><span data-stu-id="91199-133">Hour</span></span>             | <span data-ttu-id="91199-134">Čištění převodovky</span><span class="sxs-lookup"><span data-stu-id="91199-134">Gear box cleaning</span></span>  | <span data-ttu-id="91199-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="91199-135">EL-S/1000</span></span>      |
| <span data-ttu-id="91199-136">Položka</span><span class="sxs-lookup"><span data-stu-id="91199-136">Item</span></span>             | <span data-ttu-id="91199-137">Čistící materiál</span><span class="sxs-lookup"><span data-stu-id="91199-137">Cleaning materials</span></span> | <span data-ttu-id="91199-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="91199-138">EL-S/1000</span></span>      |
| <span data-ttu-id="91199-139">Hodina</span><span class="sxs-lookup"><span data-stu-id="91199-139">Hour</span></span>             | <span data-ttu-id="91199-140">Kontrola</span><span class="sxs-lookup"><span data-stu-id="91199-140">Inspection</span></span>         | <span data-ttu-id="91199-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="91199-141">EL-L/1000</span></span>      |
| <span data-ttu-id="91199-142">Hodina</span><span class="sxs-lookup"><span data-stu-id="91199-142">Hour</span></span>             | <span data-ttu-id="91199-143">Čištění převodovky</span><span class="sxs-lookup"><span data-stu-id="91199-143">Gearbox cleaning</span></span>   | <span data-ttu-id="91199-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="91199-144">EL-L/1000</span></span>      |
| <span data-ttu-id="91199-145">Položka</span><span class="sxs-lookup"><span data-stu-id="91199-145">Item</span></span>             | <span data-ttu-id="91199-146">Čistící materiál</span><span class="sxs-lookup"><span data-stu-id="91199-146">Cleaning materials</span></span> | <span data-ttu-id="91199-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="91199-147">EL-L/1000</span></span>      |

<span data-ttu-id="91199-148">Při servisním zásahu je nutné vyměnit převodovku výtahu EL-S/1000.</span><span class="sxs-lookup"><span data-stu-id="91199-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="91199-149">Otevřením nástroje Návrhář kusovníku pomocí vztahu předmětu servisu nastaveného pro aktuální servisní smlouvu proveďte výměnu součástky předmětu.</span><span class="sxs-lookup"><span data-stu-id="91199-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="91199-150">Otevření Návrháře kusovníku pomocí vztahu předmětu servisu</span><span class="sxs-lookup"><span data-stu-id="91199-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="91199-151">Servisní smlouvy</span><span class="sxs-lookup"><span data-stu-id="91199-151">Service agreements</span></span>
2. <span data-ttu-id="91199-152">Dvakrát klikněte na servisní smlouvu nebo kliknutím na možnost Servisní smlouva vytvořte novou servisní smlouvu.</span><span class="sxs-lookup"><span data-stu-id="91199-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="91199-153">Klikněte na záložku Nastavení.</span><span class="sxs-lookup"><span data-stu-id="91199-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="91199-154">Chcete-li k servisní smlouvě připojit šablonu kusovníku, klikněte na položku Předměty servisu.</span><span class="sxs-lookup"><span data-stu-id="91199-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="91199-155">Ve formuláři Předměty servisu klikněte na tlačítko Návrhář a otevřete formulář návrháře pro úpravu šablony kusovníku.</span><span class="sxs-lookup"><span data-stu-id="91199-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="91199-156">Automaticky vytvářené servisní zakázky</span><span class="sxs-lookup"><span data-stu-id="91199-156">Automatically created service orders</span></span>

<span data-ttu-id="91199-157">Vytváříte-li servisní zakázky pro servisní smlouvu automaticky, vztahy předmětů servisu ve smlouvě budou rovněž vytvořeny v servisních zakázkách.</span><span class="sxs-lookup"><span data-stu-id="91199-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>


