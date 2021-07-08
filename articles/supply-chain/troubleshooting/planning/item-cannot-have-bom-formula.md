---
title: Položka nemůže mít kusovník ani recepturu
description: Když se pokusíte potvrdit objednávku, během ověřování položky se zobrazí chybová zpráva. Uvádí, že položka nemůže mít kusovník (BOM) ani recepturu.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294029"
---
# <a name="item-cant-have-a-bom-or-formula"></a><span data-ttu-id="2ba30-104">Položka nemůže mít kusovník ani recepturu</span><span class="sxs-lookup"><span data-stu-id="2ba30-104">Item can't have a BOM or formula</span></span>

<span data-ttu-id="2ba30-105">Kód chyby: PRO2614</span><span class="sxs-lookup"><span data-stu-id="2ba30-105">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="2ba30-106">Příznaky</span><span class="sxs-lookup"><span data-stu-id="2ba30-106">Symptoms</span></span>

<span data-ttu-id="2ba30-107">Když se pokusíte vyřídit objednávku, během ověřování položky se zobrazí následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="2ba30-107">When you try to firm an order, you receive the following error message during item validation:</span></span>

> <span data-ttu-id="2ba30-108">Položka nemůže mít kusovník ani recepturu</span><span class="sxs-lookup"><span data-stu-id="2ba30-108">Item cannot have a BOM or formula</span></span>

## <a name="resolution"></a><span data-ttu-id="2ba30-109">Řešení</span><span class="sxs-lookup"><span data-stu-id="2ba30-109">Resolution</span></span>

<span data-ttu-id="2ba30-110">Položky, které mají kusovník nebo recepturu, musí mít typ *Položka plánování*, *Kusovník* nebo *receptura*.</span><span class="sxs-lookup"><span data-stu-id="2ba30-110">Items that have a bill of materials (BOM) or formula must be of the *Planning item*, *BOM*, or *formula* type.</span></span> <span data-ttu-id="2ba30-111">Chcete-li změnit typ položky, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="2ba30-111">To change the type of an item, follow these steps.</span></span>

1. <span data-ttu-id="2ba30-112">Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="2ba30-112">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="2ba30-113">Otevřete relevantní produkt.</span><span class="sxs-lookup"><span data-stu-id="2ba30-113">Open the relevant product.</span></span>
1. <span data-ttu-id="2ba30-114">Na pevné záložce **Technik** nastavte pole **Typ výroby** na *Položka plánování*, *Kusovník* nebo *receptura*.</span><span class="sxs-lookup"><span data-stu-id="2ba30-114">On the **Engineer** FastTab, set the **Production type** field to *Planning item*, *BOM*, or *formula*.</span></span>
