---
title: Vytvoření stavu životního cyklu produktu k vyloučení produktů z hlavního plánování
description: Tento postup popisuje, jak vytvořit nový stav životního cyklu produktu s vyloučením produktů z hlavního plánování a výpočtu úrovně Kusovníku.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62de37b5a84a1771b77ef2566942b7ffe8895f16
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149934"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a><span data-ttu-id="883e9-103">Vytvoření stavu životního cyklu produktu k vyloučení produktů z hlavního plánování</span><span class="sxs-lookup"><span data-stu-id="883e9-103">Create a product lifecycle state to exclude products from Master planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="883e9-104">Tento postup popisuje, jak vytvořit nový stav životního cyklu produktu s vyloučením produktů z hlavního plánování a výpočtu úrovně Kusovníku.</span><span class="sxs-lookup"><span data-stu-id="883e9-104">This procedure shows how to create a new product lifecycle state that excludes the products from Master planning and BOM-level calculation.</span></span>


## <a name="create-an-obsolete-state"></a><span data-ttu-id="883e9-105">Vytvoření zastaralého stavu</span><span class="sxs-lookup"><span data-stu-id="883e9-105">Create an obsolete state</span></span>
1. <span data-ttu-id="883e9-106">Přejděte na Řízení informací o produktech > Nastavení > Stav životnosti produktu.</span><span class="sxs-lookup"><span data-stu-id="883e9-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="883e9-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="883e9-107">Click New.</span></span>
3. <span data-ttu-id="883e9-108">Zadejte hodnotu do pole Stav.</span><span class="sxs-lookup"><span data-stu-id="883e9-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="883e9-109">Vyberte možnost Ne v poli Je aktivní pro plánování.</span><span class="sxs-lookup"><span data-stu-id="883e9-109">Select No in the Is active for planning field.</span></span>
5. <span data-ttu-id="883e9-110">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="883e9-110">In the Description field, type a value.</span></span>

## <a name="associate-the-obsolete-state-to-a-released-product"></a><span data-ttu-id="883e9-111">Přidružení zastaralého stavu k uvolněnému produktu</span><span class="sxs-lookup"><span data-stu-id="883e9-111">Associate the obsolete state to a released product</span></span>
1. <span data-ttu-id="883e9-112">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="883e9-112">Close the page.</span></span>
2. <span data-ttu-id="883e9-113">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="883e9-113">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="883e9-114">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="883e9-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="883e9-115">Můžete například filtrovat v poli Hledat jméno pomocí hodnoty M00.</span><span class="sxs-lookup"><span data-stu-id="883e9-115">For example, filter on the Search name field with a value of 'M00'.</span></span>
4. <span data-ttu-id="883e9-116">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="883e9-116">Click Edit.</span></span>
5. <span data-ttu-id="883e9-117">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="883e9-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="883e9-118">V poli Stav cyklu životnosti produktu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="883e9-118">In the Product lifecycle state field, enter or select a value.</span></span>

