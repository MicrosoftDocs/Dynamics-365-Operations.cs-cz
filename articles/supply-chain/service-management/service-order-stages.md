---
title: "Fáze servisních zakázek"
description: "Definováním fází servisní zakázky a jejich přiřazením k zaměstnancům můžete řídit tok servisní zakázky pomocí jednotlivých úloh, které provádějí různé osoby v rámci servisní organizace."
author: YuyuScheller
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAStageTable
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
ms.openlocfilehash: 9aa90dfcfc4b30d6cb4fa7ed4e6faaf505548d41
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="service-order-stages"></a><span data-ttu-id="01fee-103">Fáze servisních zakázek</span><span class="sxs-lookup"><span data-stu-id="01fee-103">Service order stages</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="01fee-104">Můžete nastavit fáze pro servisní zakázku a definovat tak úkoly, které musí být dokončeny, pořadí, ve kterém jsou dokončeny, a zaměstnance, kteří odpovídají za toto dokončení.</span><span class="sxs-lookup"><span data-stu-id="01fee-104">You can set up stages for a service order to define the tasks that must be completed, the order in which they are completed, and the workers who are responsible for completing them.</span></span> <span data-ttu-id="01fee-105">Definováním fází servisní zakázky a jejich přiřazením k zaměstnancům můžete řídit tok servisní zakázky pomocí jednotlivých úloh, které provádějí různé osoby v rámci servisní organizace.</span><span class="sxs-lookup"><span data-stu-id="01fee-105">By defining the stages for a service order and assigning them to workers, you can control the flow of a service order through the tasks that various people perform in the service organization.</span></span> <span data-ttu-id="01fee-106">Posloupnost fází musí obsahovat počáteční fázi.</span><span class="sxs-lookup"><span data-stu-id="01fee-106">The sequence of stages must include an initial stage.</span></span>

<span data-ttu-id="01fee-107">Můžete také definovat akce, které jsou povoleny v každé fázi.</span><span class="sxs-lookup"><span data-stu-id="01fee-107">You can also define the actions that are permitted at each stage.</span></span> <span data-ttu-id="01fee-108">Příklad zrušením zaškrtnutí políčka **Zaúčtovat** ve všech fázích mimo konečné fáze zabráníte zaúčtování servisních zakázek dříve, než projdou celou úplnou posloupností fází.</span><span class="sxs-lookup"><span data-stu-id="01fee-108">For example, if you clear the **Post** check box for all stages except the final stage, you prevent any service orders from being posted before the service orders are processed through the complete sequence of stages.</span></span>

## <a name="branching-in-service-order-stages"></a><span data-ttu-id="01fee-109">Větvení fází v servisní zakázce</span><span class="sxs-lookup"><span data-stu-id="01fee-109">Branching in service order stages</span></span>

<span data-ttu-id="01fee-110">Při nastavování servisní fáze můžete vytvořit více možností nebo větví dostupných pro výběr v další fázi služby.</span><span class="sxs-lookup"><span data-stu-id="01fee-110">When you set up a service stage, you can create multiple options, or branches, to select from for the next service stage.</span></span> <span data-ttu-id="01fee-111">Všechny větve, které jste vytvořili, lze vybírat při dokončení počáteční fáze.</span><span class="sxs-lookup"><span data-stu-id="01fee-111">All the branches that you create are available to select from when the initial stage is completed.</span></span> <span data-ttu-id="01fee-112">Například můžete nastavit **Plánování** jako počáteční fázi.</span><span class="sxs-lookup"><span data-stu-id="01fee-112">For example, you set up **Planning** as an initial stage.</span></span> <span data-ttu-id="01fee-113">Vytvořte dvě fáze s názvem **Probíhá** a **Zrušeno** a poté vyberte **Plánování** jako jejich nadřazenou fázi.</span><span class="sxs-lookup"><span data-stu-id="01fee-113">You create two stages named **In process** and **Cancel**, and then select **Planning** as the parent for them.</span></span> <span data-ttu-id="01fee-114">Přiřaďte fázi **Plánování** k prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="01fee-114">You assign the **Planning** stage to sales order.</span></span> <span data-ttu-id="01fee-115">Po dokončení fáze plánování pro prodejní objednávku můžete vybrat fázi **Probíhá** (pokud je prodejní objednávka připravena pro práci), nebo se můžete rozhodnout vybrat fázi **Zrušeno** (pokud je prodejní objednávka zrušena).</span><span class="sxs-lookup"><span data-stu-id="01fee-115">When the planning stage for the sales order is completed, you can select the **In process** stage if the sales order is ready to work on, or you can select the **Cancel** stage if the sales order is canceled.</span></span>

## <a name="see-also"></a><span data-ttu-id="01fee-116">Viz také</span><span class="sxs-lookup"><span data-stu-id="01fee-116">See also</span></span>

[<span data-ttu-id="01fee-117">Nastavit fáze servisních zakázek</span><span class="sxs-lookup"><span data-stu-id="01fee-117">Set up service order stages</span></span>](set-up-service-order-stages.md)

[<span data-ttu-id="01fee-118">Změna fáze servisní zakázky</span><span class="sxs-lookup"><span data-stu-id="01fee-118">Change the service order stage</span></span>](change-service-order-stage.md)

  



