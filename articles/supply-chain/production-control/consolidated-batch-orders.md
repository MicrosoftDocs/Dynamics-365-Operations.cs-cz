---
title: Konsolidované dávkové objednávky
description: Tento článek popisuje koncept konsolidované dávkové objednávky.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed722ba0c79afa038f1af7b4491f3ff18b052067
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246374"
---
# <a name="consolidated-batch-orders"></a><span data-ttu-id="d36b4-103">Konsolidované dávkové objednávky</span><span class="sxs-lookup"><span data-stu-id="d36b4-103">Consolidated batch orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d36b4-104">Tento článek popisuje koncept konsolidované dávkové objednávky.</span><span class="sxs-lookup"><span data-stu-id="d36b4-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="d36b4-105">Vyrobená nebalená položka je považována za nadřazenou položku, zatímco zabalená položka je považována za podřízenou položku.</span><span class="sxs-lookup"><span data-stu-id="d36b4-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="d36b4-106">Vztah mezi nebalenou položkou a zabalenou položkou je vyjádřen v převodu nebalené položky.</span><span class="sxs-lookup"><span data-stu-id="d36b4-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="d36b4-107">Tento převod nebalené položky je definován pro nebalenou položku samotnou.</span><span class="sxs-lookup"><span data-stu-id="d36b4-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="d36b4-108">Zabalené položky lze balit do kontejnerů jedné nebo více velikostí, které jsou považovány za jednu jednotku.</span><span class="sxs-lookup"><span data-stu-id="d36b4-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="d36b4-109">Při konsolidaci objednávek nebalené položky můžete zobrazit všechny související dávkové objednávky v jednom zobrazení, abyste zjistili, zda musí být dokončena nějaká zbývající práce.</span><span class="sxs-lookup"><span data-stu-id="d36b4-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="d36b4-110">Konsolidovaná dávková objednávka může obsahovat kombince následujících objednávek:</span><span class="sxs-lookup"><span data-stu-id="d36b4-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="d36b4-111">Jedna objednávka nebaleného zboží a více objednávek baleného zboží</span><span class="sxs-lookup"><span data-stu-id="d36b4-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="d36b4-112">Více objednávek nebaleného zboží a více objednávek baleného zboží</span><span class="sxs-lookup"><span data-stu-id="d36b4-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="d36b4-113">Více objednávek nebaleného zboží a jedna objednávka baleného zboží</span><span class="sxs-lookup"><span data-stu-id="d36b4-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="d36b4-114">Pouze objednávky baleného zboží</span><span class="sxs-lookup"><span data-stu-id="d36b4-114">Only packed orders</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]