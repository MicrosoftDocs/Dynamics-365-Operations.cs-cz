---
title: Nastavení přiřazení dodatečných služeb
description: Tento postup popisuje, jak nastavíte přiřazení doplňkové služby.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f0ea4a3914b7214dcceb22595809eaa3118a0ca
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987273"
---
# <a name="set-up-accessorial-assignments"></a><span data-ttu-id="0a534-103">Nastavení přiřazení dodatečných služeb</span><span class="sxs-lookup"><span data-stu-id="0a534-103">Set up accessorial assignments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0a534-104">Tento postup popisuje, jak nastavíte přiřazení doplňkové služby.</span><span class="sxs-lookup"><span data-stu-id="0a534-104">This procedure shows how to set up an accessorial assignment.</span></span> <span data-ttu-id="0a534-105">To obvykle provádí koordinátor přepravy.</span><span class="sxs-lookup"><span data-stu-id="0a534-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="0a534-106">Před použitím této příručky je nutné spustit příručku "Nastavení poplatků za dodatečnou službu centra a základní dodatečné služby".</span><span class="sxs-lookup"><span data-stu-id="0a534-106">Before you use this guide you need to run the "Set up hub accessorial charges and accessorial masters" guide.</span></span>


## <a name="set-up-accessorial-assignment"></a><span data-ttu-id="0a534-107">Nastavení přiřazení dodatečné služby</span><span class="sxs-lookup"><span data-stu-id="0a534-107">Set up Accessorial assignment</span></span>
1. <span data-ttu-id="0a534-108">Přejděte do nabídky Správa přepravy > Nastavení > Ohodnocení > Přiřazení dodatečných služeb.</span><span class="sxs-lookup"><span data-stu-id="0a534-108">Go to Transportation management > Setup > Rating > Accessorial assignments.</span></span>
2. <span data-ttu-id="0a534-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="0a534-109">Click New.</span></span>
3. <span data-ttu-id="0a534-110">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="0a534-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="0a534-111">Přepněte rozšíření oddílu Podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="0a534-111">Toggle the expansion of the Details section.</span></span>
5. <span data-ttu-id="0a534-112">V poli Centrum kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0a534-112">In the Hub field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="0a534-113">V seznamu vyberte centrum, pro které jste vytvořili hlavní dodatečnou službu během spuštění průvodce "Nastavení poplatků za dodatečnou službu centra a základní dodatečné služby".</span><span class="sxs-lookup"><span data-stu-id="0a534-113">In the list, select the Hub that you created an accessorial master for when you ran the "Set up hub accessorial charges and accessorial masters" guide.</span></span> 
7. <span data-ttu-id="0a534-114">V poli ID dodatečné služby centra kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0a534-114">In the Hub accessorial ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="0a534-115">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0a534-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0a534-116">Přepněte rozšíření oddílu Kritéria.</span><span class="sxs-lookup"><span data-stu-id="0a534-116">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="0a534-117">V části Kritéria můžete vybrat přesná kritéria pro případ, kdy mají být použity náklady, a to na základě toho, které hodnoty jsou zde k dispozici.</span><span class="sxs-lookup"><span data-stu-id="0a534-117">In the Criteria section you can choose the exact criteria for when the charge should apply, based on the different values offered here.</span></span>  
10. <span data-ttu-id="0a534-118">Nastavte možnost Vždy použít na Ano.</span><span class="sxs-lookup"><span data-stu-id="0a534-118">Set the Always apply option to Yes.</span></span>
11. <span data-ttu-id="0a534-119">Vyberte volbu v poli Úroveň přiřazení doplňkové služby.</span><span class="sxs-lookup"><span data-stu-id="0a534-119">In the Accessorial assignment level field, select an option.</span></span>
12. <span data-ttu-id="0a534-120">Přepněte rozšíření oddílu Výpočet.</span><span class="sxs-lookup"><span data-stu-id="0a534-120">Toggle the expansion of the Calculation section.</span></span>
13. <span data-ttu-id="0a534-121">Vyberte možnost Jednotný v poli Typ poplatku za dodatečné služby.</span><span class="sxs-lookup"><span data-stu-id="0a534-121">In the Accessorial fee type field, select 'Flat'.</span></span>
    * <span data-ttu-id="0a534-122">Typ Poplatek za dodatečné služby určuje způsob výpočtu skutečných nákladů.</span><span class="sxs-lookup"><span data-stu-id="0a534-122">The Accessorial fee type determines how to calculate the actual charge.</span></span> <span data-ttu-id="0a534-123">V tomto příkladu se jedná o paušální náklady.</span><span class="sxs-lookup"><span data-stu-id="0a534-123">In this example it's a flat charge.</span></span>  
14. <span data-ttu-id="0a534-124">V poli Poplatek za dodatečné služby zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="0a534-124">In the Accessorial fee field, enter a number.</span></span>
15. <span data-ttu-id="0a534-125">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="0a534-125">Click Save.</span></span>

