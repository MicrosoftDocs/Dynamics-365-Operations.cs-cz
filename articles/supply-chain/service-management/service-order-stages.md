---
title: Fáze servisních zakázek
description: Definováním fází servisní zakázky a jejich přiřazením k zaměstnancům můžete řídit tok servisní zakázky pomocí jednotlivých úloh, které provádějí různé osoby v rámci servisní organizace.
author: ShylaThompson
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c46d4bb43c8f59a0ef55963ac9b453491a6112b0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817502"
---
# <a name="service-order-stages"></a><span data-ttu-id="75140-103">Fáze servisních zakázek</span><span class="sxs-lookup"><span data-stu-id="75140-103">Service order stages</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="75140-104">Můžete nastavit fáze pro servisní zakázku a definovat tak úkoly, které musí být dokončeny, pořadí, ve kterém jsou dokončeny, a zaměstnance, kteří odpovídají za toto dokončení.</span><span class="sxs-lookup"><span data-stu-id="75140-104">You can set up stages for a service order to define the tasks that must be completed, the order in which they are completed, and the workers who are responsible for completing them.</span></span> <span data-ttu-id="75140-105">Definováním fází servisní zakázky a jejich přiřazením k zaměstnancům můžete řídit tok servisní zakázky pomocí jednotlivých úloh, které provádějí různé osoby v rámci servisní organizace.</span><span class="sxs-lookup"><span data-stu-id="75140-105">By defining the stages for a service order and assigning them to workers, you can control the flow of a service order through the tasks that various people perform in the service organization.</span></span> <span data-ttu-id="75140-106">Posloupnost fází musí obsahovat počáteční fázi.</span><span class="sxs-lookup"><span data-stu-id="75140-106">The sequence of stages must include an initial stage.</span></span>

<span data-ttu-id="75140-107">Můžete také definovat akce, které jsou povoleny v každé fázi.</span><span class="sxs-lookup"><span data-stu-id="75140-107">You can also define the actions that are permitted at each stage.</span></span> <span data-ttu-id="75140-108">Příklad zrušením zaškrtnutí políčka **Zaúčtovat** ve všech fázích mimo konečné fáze zabráníte zaúčtování servisních zakázek dříve, než projdou celou úplnou posloupností fází.</span><span class="sxs-lookup"><span data-stu-id="75140-108">For example, if you clear the **Post** check box for all stages except the final stage, you prevent any service orders from being posted before the service orders are processed through the complete sequence of stages.</span></span>

## <a name="branching-in-service-order-stages"></a><span data-ttu-id="75140-109">Větvení fází v servisní zakázce</span><span class="sxs-lookup"><span data-stu-id="75140-109">Branching in service order stages</span></span>

<span data-ttu-id="75140-110">Při nastavování servisní fáze můžete vytvořit více možností nebo větví dostupných pro výběr v další fázi služby.</span><span class="sxs-lookup"><span data-stu-id="75140-110">When you set up a service stage, you can create multiple options, or branches, to select from for the next service stage.</span></span> <span data-ttu-id="75140-111">Všechny větve, které jste vytvořili, lze vybírat při dokončení počáteční fáze.</span><span class="sxs-lookup"><span data-stu-id="75140-111">All the branches that you create are available to select from when the initial stage is completed.</span></span> <span data-ttu-id="75140-112">Například můžete nastavit **Plánování** jako počáteční fázi.</span><span class="sxs-lookup"><span data-stu-id="75140-112">For example, you set up **Planning** as an initial stage.</span></span> <span data-ttu-id="75140-113">Vytvořte dvě fáze s názvem **Probíhá** a **Zrušeno** a poté vyberte **Plánování** jako jejich nadřazenou fázi.</span><span class="sxs-lookup"><span data-stu-id="75140-113">You create two stages named **In process** and **Cancel**, and then select **Planning** as the parent for them.</span></span> <span data-ttu-id="75140-114">Přiřaďte fázi **Plánování** k prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="75140-114">You assign the **Planning** stage to sales order.</span></span> <span data-ttu-id="75140-115">Po dokončení fáze plánování pro prodejní objednávku můžete vybrat fázi **Probíhá** (pokud je prodejní objednávka připravena pro práci), nebo se můžete rozhodnout vybrat fázi **Zrušeno** (pokud je prodejní objednávka zrušena).</span><span class="sxs-lookup"><span data-stu-id="75140-115">When the planning stage for the sales order is completed, you can select the **In process** stage if the sales order is ready to work on, or you can select the **Cancel** stage if the sales order is canceled.</span></span>

## <a name="see-also"></a><span data-ttu-id="75140-116">Viz také</span><span class="sxs-lookup"><span data-stu-id="75140-116">See also</span></span>

[<span data-ttu-id="75140-117">Nastavit fáze servisních zakázek</span><span class="sxs-lookup"><span data-stu-id="75140-117">Set up service order stages</span></span>](set-up-service-order-stages.md)

[<span data-ttu-id="75140-118">Změna fáze servisní zakázky</span><span class="sxs-lookup"><span data-stu-id="75140-118">Change the service order stage</span></span>](change-service-order-stage.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]