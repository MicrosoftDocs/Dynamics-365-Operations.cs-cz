---
title: Snížení odpisu zůstatku po rozdělení
description: Toto téma popisuje metodu, která se používá v dlouhodobém majetku k výpočtu odpisů po rozdělení majetku pomocí metody snížení zůstatku.
author: moaamer
manager: Ann Beebe
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f276f49e5b1bc2814dc851f1ad4204a151d86c43
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222376"
---
# <a name="reduce-balance-depreciation-after-a-split"></a><span data-ttu-id="a7119-103">Snížení odpisu zůstatku po rozdělení</span><span class="sxs-lookup"><span data-stu-id="a7119-103">Reduce balance depreciation after a split</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7119-104">Toto téma popisuje metodu, která se používá v Dlouhodobém majetku k výpočtu odpisů po rozdělení majetku na jiný pomocí metody snížení zůstatku.</span><span class="sxs-lookup"><span data-stu-id="a7119-104">This topic describes the method that is used in Fixed assets to calculate depreciation after an asset is split to another asset by using the reduce balance method.</span></span> <span data-ttu-id="a7119-105">Rok odpisování, který je nakonfigurován v knize majetku, je fiskální rok.</span><span class="sxs-lookup"><span data-stu-id="a7119-105">The depreciation year that is configured in the asset book is the fiscal year.</span></span> <span data-ttu-id="a7119-106">Další informace viz [Snížení odpisu zůstatku](reduce-balance-depreciation.md) a [Rozdělení dlouhodobého majetku](tasks/split-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="a7119-106">For more information, see [Reduce balance depreciation](reduce-balance-depreciation.md) and [Split a fixed asset](tasks/split-fixed-asset.md).</span></span>

<span data-ttu-id="a7119-107">Pokud rozdělíte dlouhodobý majetek během fiskálního období, které je pozdější než období, kdy byl majetek získán, odpisy sníženého zůstatku budou představovat čistou účetní hodnotu majetku (NBV) za předchozí rok.</span><span class="sxs-lookup"><span data-stu-id="a7119-107">If you split a fixed asset during a fiscal period that is later than the period when the asset was acquired, the reduced balance depreciation will account for the asset's net book value (NBV) for the previous year.</span></span> <span data-ttu-id="a7119-108">Bude také účtovat transakce úpravy akvizic a odpisů, které byly generovány z transakce, která rozděluje majetek.</span><span class="sxs-lookup"><span data-stu-id="a7119-108">It will also account for the acquisition and depreciation adjustment transactions that were generated from the transaction that split the asset.</span></span> <span data-ttu-id="a7119-109">Toto chování předpokládá, že majetek byl získán v jednom fiskálním roce a rozdělen v pozdějším fiskálním roce.</span><span class="sxs-lookup"><span data-stu-id="a7119-109">This behavior assumes that the asset was acquired in one fiscal year and split in a later fiscal year.</span></span> <span data-ttu-id="a7119-110">Částka, která musí být odepsána pro původní majetek po rozdělení, odráží NBV majetku před rozdělením majetku a transakci úpravy akvizice a odpisů, která byla zaúčtována pro rozdělení.</span><span class="sxs-lookup"><span data-stu-id="a7119-110">The amount that must be depreciated for the original asset after the split reflects the asset's NBV before the asset was split, and the acquisition and depreciation adjustment transaction that was posted for the split.</span></span>

<span data-ttu-id="a7119-111">Platí například následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="a7119-111">For example, the following conditions are in effect:</span></span>

- <span data-ttu-id="a7119-112">Fiskální období je od 30. června do 1. července.</span><span class="sxs-lookup"><span data-stu-id="a7119-112">The fiscal period is from June 30 to July 1.</span></span>
- <span data-ttu-id="a7119-113">Procento redukčního zůstatku je 18 procent a majetek je získán v červnu 2019 za pořizovací cenu 10 000 USD.</span><span class="sxs-lookup"><span data-stu-id="a7119-113">The reducing balance percentage is 18 percent, and an asset is acquired in June 2019 at an acquisition price of $10,000.</span></span>
- <span data-ttu-id="a7119-114">Odpisy prvního fiskálního roku se rovnají 18 000 USD, měsíční odpisy se rovnají 150 USD a majetek se poté odepisuje do listopadu 2019, a to ve výši 738 75 USD.</span><span class="sxs-lookup"><span data-stu-id="a7119-114">The depreciation of the first fiscal year equals $18,000, the monthly depreciation equals $150, and the asset is then depreciated until November 2019, in the amount of $738.75.</span></span>
- <span data-ttu-id="a7119-115">V listopadu 2019 je 80 procent majetku rozděleno na jiný dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="a7119-115">In November 2019, 80 percent of the asset is split to another fixed asset.</span></span>

<span data-ttu-id="a7119-116">[![Snížení odpisu zůstatku po rozdělení](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span><span class="sxs-lookup"><span data-stu-id="a7119-116">[![Reduce balance depreciation after a split](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span></span>

<span data-ttu-id="a7119-117">Částka k odpisu u původního majetku je 1 822,25 USD.</span><span class="sxs-lookup"><span data-stu-id="a7119-117">The amount to depreciate for the original asset is $1,822.25.</span></span> <span data-ttu-id="a7119-118">Tato částka se rovná NBV před zaúčtováním rozdělené transakce (9 111,25 USD) plus úprava akvizice, která je generována během účtování rozdělené transakce (-8 000 USD), plus úprava odpisů, která je generována během rozdělené transakce (711 USD).</span><span class="sxs-lookup"><span data-stu-id="a7119-118">This amount equals the NBV before the split transaction is posted ($9,111.25), plus the acquisition adjustment that is generated during posting of the split transaction (-$8,000), plus the depreciation adjustment that is generated during the split transaction ($711).</span></span> <span data-ttu-id="a7119-119">Proto je odpis za druhý rok (1 822,25 × 18 procent) ÷ 12 = 27,33 USD.</span><span class="sxs-lookup"><span data-stu-id="a7119-119">Therefore, the depreciation for the second year is (1,822.25 × 18 percent) ÷ 12 = $27.33.</span></span>

<span data-ttu-id="a7119-120">Částka k odpisu nového dlouhodobého majetku v prvním roce je (8 000 × 18 procent) ÷ 12 = 120 USD.</span><span class="sxs-lookup"><span data-stu-id="a7119-120">The amount to depreciate for the new fixed asset in the first year is (8,000 × 18 percent) ÷ 12 = $120.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]