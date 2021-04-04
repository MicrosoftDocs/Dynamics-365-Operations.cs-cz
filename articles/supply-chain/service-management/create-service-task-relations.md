---
title: Vytvoření relací servisních úloh
description: Servisní úlohy lze přidružit servisním smlouvám nebo servisním zakázkám pro popis servisní úlohy pro dokončení pro smlouvu nebo zakázku.
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
ms.openlocfilehash: ea5952376fe30f489d385c8f8295fbf86f2af085
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470723"
---
# <a name="create-service-task-relations"></a><span data-ttu-id="ba47b-103">Vytvoření relací servisních úloh</span><span class="sxs-lookup"><span data-stu-id="ba47b-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba47b-104">Servisní úlohy lze přidružit servisním smlouvám nebo servisním zakázkám pro popis servisní úlohy pro dokončení pro smlouvu nebo zakázku.</span><span class="sxs-lookup"><span data-stu-id="ba47b-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="ba47b-105">Tyto informace se zobrazí technikům i zákazníkům.</span><span class="sxs-lookup"><span data-stu-id="ba47b-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="ba47b-106">Vytvoření relace se servisní smlouvou</span><span class="sxs-lookup"><span data-stu-id="ba47b-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="ba47b-107">Přejděte na **Správa servisu** \> **Obecné** \> **Servisní smlouvy** \> **Servisní smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="ba47b-107">Go to **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="ba47b-108">Vyberte existující servisní smlouvu nebo vytvořte novou smlouvu.</span><span class="sxs-lookup"><span data-stu-id="ba47b-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="ba47b-109">V podokně akcí vyberte tlačítko **Servisní úlohy**.</span><span class="sxs-lookup"><span data-stu-id="ba47b-109">On the Action Pane, select the **Service tasks** button.</span></span>

4.  <span data-ttu-id="ba47b-110">Ve formuláři **Servisní úlohy** vytvořte nový řádek výběrem možnosti **Nový** a pak vyberte servisní úlohu v seznamu **Servisní úloha** pro připojení servisní úlohy k servisní smlouvě.</span><span class="sxs-lookup"><span data-stu-id="ba47b-110">On the **Service tasks** form, select **New** to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="ba47b-111">Na kartě **Popis** zadejte jakékoli interní nebo externí popisy.</span><span class="sxs-lookup"><span data-stu-id="ba47b-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="ba47b-112">Zavřením formuláře uložte záznam.</span><span class="sxs-lookup"><span data-stu-id="ba47b-112">Close the form to save the record.</span></span>

<span data-ttu-id="ba47b-113">Stejným způsobem vytvořte všechny relace servisních úloh pro servisní smlouvu.</span><span class="sxs-lookup"><span data-stu-id="ba47b-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="ba47b-114">Nyní můžete tyto servisní úlohy zadat pro jakékoli připojené řádky smlouvy.</span><span class="sxs-lookup"><span data-stu-id="ba47b-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="ba47b-115">Relace servisní úlohy vytvořená na servisní smlouvě je k dispozici ve všech servisních zakázkách připojených k této servisní smlouvě.</span><span class="sxs-lookup"><span data-stu-id="ba47b-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="ba47b-116">Vytvoření relace se servisní zakázkou</span><span class="sxs-lookup"><span data-stu-id="ba47b-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="ba47b-117">Přejděte na **Správa servisu** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="ba47b-117">Go to **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="ba47b-118">Vyberte existující servisní zakázku nebo vytvořte novou zakázku.</span><span class="sxs-lookup"><span data-stu-id="ba47b-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="ba47b-119">V podokně akcí vyberte tlačítko **Servisní úlohy**.</span><span class="sxs-lookup"><span data-stu-id="ba47b-119">On the Action Pane, select the **Service tasks** button.</span></span>

4.  <span data-ttu-id="ba47b-120">Ve formuláři **Servisní úlohy** vytvořte nový řádek výběrem možnosti **Nový** a pak vyberte servisní úlohu v seznamu **Servisní úloha** pro připojení servisních úloh k servisní zakázce.</span><span class="sxs-lookup"><span data-stu-id="ba47b-120">From the **Service tasks** form, select **New** to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="ba47b-121">Na kartě **Popis** zadejte jakékoli interní nebo externí popisy.</span><span class="sxs-lookup"><span data-stu-id="ba47b-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="ba47b-122">Zavřením formuláře uložte záznam.</span><span class="sxs-lookup"><span data-stu-id="ba47b-122">Close the form to save the record.</span></span>

<span data-ttu-id="ba47b-123">Stejným způsobem vytvořte všechny relace servisních úloh pro servisní zakázku.</span><span class="sxs-lookup"><span data-stu-id="ba47b-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="ba47b-124">Nyní můžete při vytváření řádků servisní zakázky vybrat servisní úlohu, pro kterou jste vytvořili relaci.</span><span class="sxs-lookup"><span data-stu-id="ba47b-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="ba47b-125">Relace servisní úlohy vytvořená na servisní zakázce je k dispozici na konkrétní servisní zakázce.</span><span class="sxs-lookup"><span data-stu-id="ba47b-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="ba47b-126">Viz také</span><span class="sxs-lookup"><span data-stu-id="ba47b-126">See also</span></span>

[<span data-ttu-id="ba47b-127">Přehled servisních úloh</span><span class="sxs-lookup"><span data-stu-id="ba47b-127">Service tasks overview</span></span>](service-tasks.md)


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]