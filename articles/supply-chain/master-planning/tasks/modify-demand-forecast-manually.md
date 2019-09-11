---
title: Ruční úprava prognózy poptávky
description: Tento postup popisuje postup úpravy prognózy pro položku.
author: ShylaThompson
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ec1edb861619bae2ae3c211720b55e170b83ec9
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916615"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="df28b-103">Ruční úprava prognózy poptávky</span><span class="sxs-lookup"><span data-stu-id="df28b-103">Modify a demand forecast manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="df28b-104">Tento postup popisuje postup úpravy prognózy pro položku.</span><span class="sxs-lookup"><span data-stu-id="df28b-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="df28b-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="df28b-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="df28b-106">Tento záznam je určen pro plánujícího produkce.</span><span class="sxs-lookup"><span data-stu-id="df28b-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="df28b-107">Upravení prognózy pro zboží</span><span class="sxs-lookup"><span data-stu-id="df28b-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="df28b-108">V **Navigačním podokně** přejděte na **Moduly > Řízení informací o produktech > Produkty > Vydané produkty**.</span><span class="sxs-lookup"><span data-stu-id="df28b-108">In the **Navigation pane**, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="df28b-109">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="df28b-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="df28b-110">Vyberte položku, u které chcete změnit typ prognózu.</span><span class="sxs-lookup"><span data-stu-id="df28b-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="df28b-111">Můžete vybrat zboží D0001.</span><span class="sxs-lookup"><span data-stu-id="df28b-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="df28b-112">V **podokně akcí** klikněte na možnost **Plán**.</span><span class="sxs-lookup"><span data-stu-id="df28b-112">On the **Action Pane**, click **Plan**.</span></span>
4. <span data-ttu-id="df28b-113">Klikněte na položku **Prognóza poptávky**.</span><span class="sxs-lookup"><span data-stu-id="df28b-113">Click **Demand forecast**.</span></span>
5. <span data-ttu-id="df28b-114">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="df28b-114">In the list, mark the selected row.</span></span> <span data-ttu-id="df28b-115">Pokud neexistují žádné řádky prognózy, vytvořte nový řádek klepnutím na Nový na panelu aplikace.</span><span class="sxs-lookup"><span data-stu-id="df28b-115">If there are no forecast lines, create a new line by clicking New on the app bar.</span></span>  
6. <span data-ttu-id="df28b-116">V poli **Prod. množství** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="df28b-116">In the **Sales quantity** field, enter a number.</span></span> <span data-ttu-id="df28b-117">Toto číslo představuje předpovídané množství položky.</span><span class="sxs-lookup"><span data-stu-id="df28b-117">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="df28b-118">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="df28b-118">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="df28b-119">Upravení prognózy v aplikaci Excel</span><span class="sxs-lookup"><span data-stu-id="df28b-119">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="df28b-120">Klikněte na možnost **Otevřít** v Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="df28b-120">Click **Open** in Microsoft Office.</span></span>
2. <span data-ttu-id="df28b-121">Klikněte na **Upravit prognózy poptávky** v aplikaci Excel.</span><span class="sxs-lookup"><span data-stu-id="df28b-121">Click **Edit Demand forecast** in Excel.</span></span> <span data-ttu-id="df28b-122">V aplikaci Excel lze přidat, odstranit a upravit řádky prognózy poptávky.</span><span class="sxs-lookup"><span data-stu-id="df28b-122">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="df28b-123">Pokud nejsou vidět data v aplikaci Excel, je třeba přihlásit se v aplikaci Microsoft Dynamics 365 for Finance and Operations  Enterprise edition s aktivní možností "Zůstat přihlášeni", a je nutné důvěřovat datovému spojení.</span><span class="sxs-lookup"><span data-stu-id="df28b-123">If you are not able to see the data in Excel, you need to sign in to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  

