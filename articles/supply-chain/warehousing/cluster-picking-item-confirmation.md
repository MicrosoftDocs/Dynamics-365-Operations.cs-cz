---
title: Potvrzení produktu pro výdej v seskupení
description: Toto téma popisuje, jak nastavíte ověření položek s výdejem v seskupení.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e30022377cb02e7516cb98f48dc12e4f9e2ce172
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233024"
---
# <a name="product-confirmation-for-cluster-picking"></a><span data-ttu-id="7c2eb-103">Potvrzení produktu pro výdej v seskupení</span><span class="sxs-lookup"><span data-stu-id="7c2eb-103">Product confirmation for cluster picking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c2eb-104">Výdej v seskupení umožňuje vyskladnění položek pro několik objednávek současně.</span><span class="sxs-lookup"><span data-stu-id="7c2eb-104">Cluster picking allows you to pick items for several orders at the same time.</span></span> <span data-ttu-id="7c2eb-105">Při použití výdeje v seskupení je velmi důležité potvrzení položek k ověření položek, které jsou přidány do seskupení.</span><span class="sxs-lookup"><span data-stu-id="7c2eb-105">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="7c2eb-106">Při výdeji v seskupení můžete ověřit položky během procesu výdeje v seskupení.</span><span class="sxs-lookup"><span data-stu-id="7c2eb-106">You can verify items in cluster picking during the cluster picking process.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="7c2eb-107">Kdy se to používá</span><span class="sxs-lookup"><span data-stu-id="7c2eb-107">Where it applies</span></span>

<span data-ttu-id="7c2eb-108">Ověření položek pro výdej v seskupení funguje stejně jako při ověření položek v procesu výdeje bez seskupení.</span><span class="sxs-lookup"><span data-stu-id="7c2eb-108">Item verification for cluster picking works the same way as when you verify items in a non-cluster picking processes.</span></span> <span data-ttu-id="7c2eb-109">Nastavení vychází z nastavení čárového kódu produktu.</span><span class="sxs-lookup"><span data-stu-id="7c2eb-109">The setup is based on the product bar code setup.</span></span>

## <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="7c2eb-110">Nastavení ověření položek s výdejem v seskupení</span><span class="sxs-lookup"><span data-stu-id="7c2eb-110">Set up item verification with cluster picking</span></span>

1. <span data-ttu-id="7c2eb-111">V položce nabídky mobilního zařízení otevřete formulář nastavení pro potvrzení práce: **Řízení skladu** > **Řízení skladu** > **Nastavení** > **Mobilní zařízení** > **Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="7c2eb-111">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span>
1. <span data-ttu-id="7c2eb-112">Z položky nabídky mobilního zařízení otevřete **Nastavení potvrzení práce**.</span><span class="sxs-lookup"><span data-stu-id="7c2eb-112">From the mobile device menu item, open **Work confirmation setup**.</span></span>

|        <span data-ttu-id="7c2eb-113">Parametr</span><span class="sxs-lookup"><span data-stu-id="7c2eb-113">Option</span></span>        |                                    <span data-ttu-id="7c2eb-114">popis</span><span class="sxs-lookup"><span data-stu-id="7c2eb-114">Description</span></span>                                    |
|----------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7c2eb-115">Potvrzení produktu</span><span class="sxs-lookup"><span data-stu-id="7c2eb-115">Product confirmation</span></span> | <span data-ttu-id="7c2eb-116">Umožňuje vám ověřit jednotlivé skladové položky z mobilního zařízení při naskenování.</span><span class="sxs-lookup"><span data-stu-id="7c2eb-116">Allows you to verify each piece of inventory from the mobile device when scanned.</span></span> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]