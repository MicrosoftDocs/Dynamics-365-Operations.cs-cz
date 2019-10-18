---
title: Namapování dimenze prvku nákladů
description: Kontrolor nákladů může tento postup použít k mapování dimenze prvku nákladů k dimenzi nákladového prvku u právnické osoby MXMF.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 346c64ffb19e320d0babf886c15f1b46959b4f32
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176785"
---
# <a name="map-a-cost-element-dimension"></a><span data-ttu-id="1e8b6-103">Namapování dimenze prvku nákladů</span><span class="sxs-lookup"><span data-stu-id="1e8b6-103">Map a cost element dimension</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1e8b6-104">Kontrolor nákladů může tento postup použít k mapování dimenze prvku nákladů k dimenzi nákladového prvku u právnické osoby MXMF.</span><span class="sxs-lookup"><span data-stu-id="1e8b6-104">A cost controller can use this procedure to map a cost element dimension to a cost element dimension in the MXMF legal entity.</span></span> <span data-ttu-id="1e8b6-105">Tento záznam používá v ukázkových datech společnost USP2.</span><span class="sxs-lookup"><span data-stu-id="1e8b6-105">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="1e8b6-106">Přejděte na položky Nákladové účetnictví > Dimenze > Dimenze prvku nákladů.</span><span class="sxs-lookup"><span data-stu-id="1e8b6-106">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="1e8b6-107">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="1e8b6-107">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1e8b6-108">V tomto příkladu vyberte Nákladové elementy.</span><span class="sxs-lookup"><span data-stu-id="1e8b6-108">For this example, select Cost elements.</span></span>  
3. <span data-ttu-id="1e8b6-109">Klikněte na Mapování dimenzí.</span><span class="sxs-lookup"><span data-stu-id="1e8b6-109">Click Dimension mappings.</span></span>
4. <span data-ttu-id="1e8b6-110">Klikněte na Konfigurovat mapování z této dimenze.</span><span class="sxs-lookup"><span data-stu-id="1e8b6-110">Click Configure mappings from this dimension.</span></span>
5. <span data-ttu-id="1e8b6-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1e8b6-111">Click New.</span></span>
6. <span data-ttu-id="1e8b6-112">V poli Do dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1e8b6-112">In the To dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="1e8b6-113">V tomto příkladu vyberte Nákladové elementy MXMF.</span><span class="sxs-lookup"><span data-stu-id="1e8b6-113">For this example, select MXMF Cost elements.</span></span>  
7. <span data-ttu-id="1e8b6-114">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1e8b6-114">Click New.</span></span>
8. <span data-ttu-id="1e8b6-115">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="1e8b6-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="1e8b6-116">V poli Od členu dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1e8b6-116">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="1e8b6-117">V tomto příkladu vyberte člena dimenze – 606400 Telefonní a faxové náklady.</span><span class="sxs-lookup"><span data-stu-id="1e8b6-117">For this example, select dimension member 606400 Telephone & Fax Expense.</span></span>  
10. <span data-ttu-id="1e8b6-118">V poli Po člen dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1e8b6-118">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="1e8b6-119">V tomto příkladu vyberte člena dimenze 6001004 Telefon.</span><span class="sxs-lookup"><span data-stu-id="1e8b6-119">For this example, select dimension member 6001004 Telefono.</span></span>  
11. <span data-ttu-id="1e8b6-120">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1e8b6-120">Click Save.</span></span>

