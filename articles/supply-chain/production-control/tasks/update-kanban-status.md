---
title: Aktualizace stavu kanbanu
description: Pokud dojde omylem k vyprázdnění kanbanu nebo přijatý kanban musí být prázdný, je nutné aktualizovat stav kanbanu.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1161e642f8b3b1cd0a2568e0745caa6db5fe5afb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980982"
---
# <a name="update-kanban-status"></a><span data-ttu-id="a3af4-103">Aktualizace stavu kanbanu</span><span class="sxs-lookup"><span data-stu-id="a3af4-103">Update kanban status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a3af4-104">Pokud dojde omylem k vyprázdnění kanbanu nebo přijatý kanban musí být prázdný, je nutné aktualizovat stav kanbanu.</span><span class="sxs-lookup"><span data-stu-id="a3af4-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="a3af4-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="a3af4-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a3af4-106">Tento postup je určen pro vedoucího dílny.</span><span class="sxs-lookup"><span data-stu-id="a3af4-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="a3af4-107">Vyhledejte kanban.</span><span class="sxs-lookup"><span data-stu-id="a3af4-107">Find the kanban.</span></span>
1. <span data-ttu-id="a3af4-108">Přejděte na Řízení výroby > Kanban > Kanbany.</span><span class="sxs-lookup"><span data-stu-id="a3af4-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="a3af4-109">Otevřete filtr sloupce Stav manipulační jednotky.</span><span class="sxs-lookup"><span data-stu-id="a3af4-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="a3af4-110">Klikněte na tlačítko Vymazat.</span><span class="sxs-lookup"><span data-stu-id="a3af4-110">Click Clear.</span></span>
    * <span data-ttu-id="a3af4-111">To obnoví hodnoty filtrů.</span><span class="sxs-lookup"><span data-stu-id="a3af4-111">This resets the filters.</span></span>  
4. <span data-ttu-id="a3af4-112">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="a3af4-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a3af4-113">Můžete například filtrovat pole Číslo karty pomocí hodnoty „000149“.</span><span class="sxs-lookup"><span data-stu-id="a3af4-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="a3af4-114">Změna stavu Vyprázdněno na Přijato</span><span class="sxs-lookup"><span data-stu-id="a3af4-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="a3af4-115">Klikněte na Stornovat prázdnou manipulační jednotku.</span><span class="sxs-lookup"><span data-stu-id="a3af4-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="a3af4-116">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="a3af4-116">Click OK.</span></span>
    * <span data-ttu-id="a3af4-117">Všimněte si, že stav manipulační jednotky je Přijato.</span><span class="sxs-lookup"><span data-stu-id="a3af4-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="a3af4-118">Změna stavu Přijato na Vyprázdněno</span><span class="sxs-lookup"><span data-stu-id="a3af4-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="a3af4-119">Klikněte na Prázdný kanban.</span><span class="sxs-lookup"><span data-stu-id="a3af4-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="a3af4-120">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="a3af4-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a3af4-121">Všimněte si, že stav manipulační jednotky je Vyprázdněno.</span><span class="sxs-lookup"><span data-stu-id="a3af4-121">Notice that the Handling unit status is Emptied.</span></span>  

