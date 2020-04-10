---
title: Odhad výrobní zakázky
description: Tento proces můžete spustit pomocí ukázkových dat společnosti USMF nebo pomocí sady vlastních dat.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f1e99d7c84171e4affe59fb896a7e93c2a328740
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146760"
---
# <a name="estimate-a-production-order"></a><span data-ttu-id="95140-103">Odhad výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="95140-103">Estimate a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="95140-104">Tento proces můžete spustit pomocí ukázkových dat společnosti USMF nebo pomocí sady vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="95140-104">You can run this procedure by using the USMF demo data company or your own data set.</span></span> <span data-ttu-id="95140-105">V obou případech je třeba mít otevřenou výrobní zakázku, která má status Vytvořeno.</span><span class="sxs-lookup"><span data-stu-id="95140-105">In both cases, you need to have an open production order that has the Created status.</span></span> <span data-ttu-id="95140-106">Jedná se o druhou proceduru ze sedmi, která vysvětluje životního cyklus výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="95140-106">This is the second procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="estimate-a-production-order"></a><span data-ttu-id="95140-107">Odhad výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="95140-107">Estimate a production order</span></span>
1. <span data-ttu-id="95140-108">Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="95140-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="95140-109">V mřížce vyberte zakázku, která má stav Vytvořeno.</span><span class="sxs-lookup"><span data-stu-id="95140-109">Select an order that has the Created status in the grid.</span></span>
3. <span data-ttu-id="95140-110">V podokně akcí klikněte na položku Výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="95140-110">On the Action Pane, click Production order.</span></span>
4. <span data-ttu-id="95140-111">Klepněte na Odhad.</span><span class="sxs-lookup"><span data-stu-id="95140-111">Click Estimate.</span></span>
    * <span data-ttu-id="95140-112">V tomto kroku se počítají odhadované náklady jednotlivé výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="95140-112">In this step, the estimated costs of a single production order is calculated.</span></span>   
5. <span data-ttu-id="95140-113">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="95140-113">Click OK.</span></span>

## <a name="view-the-calculation-details"></a><span data-ttu-id="95140-114">Zobrazení podrobností výpočtu</span><span class="sxs-lookup"><span data-stu-id="95140-114">View the calculation details</span></span>
1. <span data-ttu-id="95140-115">V podokně akcí klikněte na možnost Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="95140-115">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="95140-116">Klepněte na Zobrazit podrobnosti výpočtu.</span><span class="sxs-lookup"><span data-stu-id="95140-116">Click View calculation details.</span></span>
    * <span data-ttu-id="95140-117">Na této stránce se zobrazuje rozúčtování nákladů.</span><span class="sxs-lookup"><span data-stu-id="95140-117">This page displays the cost breakdown.</span></span> <span data-ttu-id="95140-118">Například v prvním řádku můžete zobrazit celkovou cenu nákladů za jednotku hotového výrobku.</span><span class="sxs-lookup"><span data-stu-id="95140-118">For example, you can view the total cost price per unit for the finished product in the first row.</span></span> <span data-ttu-id="95140-119">Následující řádky obsahují náklady na základě kusovníku, výrobního postupu a nepřímých nákladů.</span><span class="sxs-lookup"><span data-stu-id="95140-119">The subsequent rows contain costs according to the bill of materials, production route, and indirect costs.</span></span>  
