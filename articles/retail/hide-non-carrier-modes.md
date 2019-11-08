---
title: Skrytí způsobů dodání mimo dopravce z možností dodávky v POS
description: V tomto tématu je popsána možnost konfigurace, která může zabránit zobrazení režimů dodání mimo dopravce pro výběr, když jsou v aplikaci pokladní místo (POS) vytvořeny objednávky dodávky.
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 09ea83b3336b208f8af0a91025c2e6c50d64c385
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/24/2019
ms.locfileid: "2659014"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a><span data-ttu-id="fa9a2-103">Skrytí způsobů dodání mimo dopravce z možností dodávky v POS</span><span class="sxs-lookup"><span data-stu-id="fa9a2-103">Hide non-carrier delivery modes from the shipping options in POS</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="fa9a2-104">Toto téma popisuje možnost konfigurace, která je k dispozici pro aplikaci v pokladním místě (POS).</span><span class="sxs-lookup"><span data-stu-id="fa9a2-104">This topic describes a configuration option that is available for the point of sale (POS) application.</span></span> <span data-ttu-id="fa9a2-105">Tato možnost konfigurace mění chování při výběru způsobu dodání v případě, že objednávky dodávek jsou vytvořeny v POS.</span><span class="sxs-lookup"><span data-stu-id="fa9a2-105">This configuration option changes the behavior for the selection of a mode of delivery when shipment orders are created in POS.</span></span>

<span data-ttu-id="fa9a2-106">Když uživatelé vytvářejí objednávky dodávek odběratele v POS, mohou vybrat způsob dodání pro danou dodávku.</span><span class="sxs-lookup"><span data-stu-id="fa9a2-106">When users create customer shipment orders in POS, they can select a mode of delivery for the shipment.</span></span> <span data-ttu-id="fa9a2-107">Tato funkce je k dispozici bez ohledu na to, zda je právě expedována celá objednávka nebo pouze vybrané řádky.</span><span class="sxs-lookup"><span data-stu-id="fa9a2-107">This functionality is available regardless of whether the whole order is being shipped or only selected lines.</span></span>

<span data-ttu-id="fa9a2-108">Ve výchozím nastavení jsou v dialogovém okně, ve kterém je vybrán způsob dodání, zobrazeny všechny platné způsoby dodání pro kombinaci kanálu, položky a dodací adresy.</span><span class="sxs-lookup"><span data-stu-id="fa9a2-108">By default, the dialog box where a mode of delivery is selected shows all the valid modes of delivery for the combination of a channel, an item, and a delivery address.</span></span> <span data-ttu-id="fa9a2-109">Tyto způsoby dodání jsou definovány na stránce **Způsoby dodání** v Retail Headquarters (**Prodej a marketing \> Nastavení \> Distribuce \> Režimy dodání**).</span><span class="sxs-lookup"><span data-stu-id="fa9a2-109">These modes of delivery are defined on the **Modes of delivery** page in Retail Headquarters (**Sales and marketing \> Setup \> Distribution \> Modes of delivery**).</span></span> <span data-ttu-id="fa9a2-110">REžimy dodání momo dopravce, například **Carryout** nebo **Pickup**, se mohou v dialogovém okně rovněz zobrazit pro výběr.</span><span class="sxs-lookup"><span data-stu-id="fa9a2-110">"Non-carrier" modes of delivery, such as **Carryout** or **Pickup**, might also appear for selection in the dialog box.</span></span>

<span data-ttu-id="fa9a2-111">Byla však přidána funkce, která umožňuje skrýt režimy dodání mimo dopravce v dialogovém okně.</span><span class="sxs-lookup"><span data-stu-id="fa9a2-111">However, a feature has been added that lets you hide non-carrier modes of delivery in the dialog box.</span></span> <span data-ttu-id="fa9a2-112">Chcete-li tuto funkci zapnout, na stránce **Parametry maloobchodu** na kartě **Objednávky zákazníka** nastavte možnost **Zobrazit pouze režim dopravce možnosti pro dodací objednávky** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="fa9a2-112">To turn on this feature, on the **Retail parameters** page, on the **Customer orders** tab, set the **Show only carrier mode options for ship orders** option to **Yes**.</span></span> <span data-ttu-id="fa9a2-113">Po zapnutí této funkce a spuštění příslušných distribučních úloh za účelem synchronizace informací do databáze kanálů se při procesu vytváření objednávek dodávek v POS nezobrazí režimy dodání mimo dopravce jako možnost k výběru.</span><span class="sxs-lookup"><span data-stu-id="fa9a2-113">After you turn on this feature and run the appropriate distribution jobs to sync the information to the channel database, non-carrier modes of delivery won't appear for selection during the process of creating shipment orders in POS.</span></span>
