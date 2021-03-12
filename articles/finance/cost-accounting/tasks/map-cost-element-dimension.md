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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5570d7cf2a8139d7959cb708d306e8b91065ed1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990660"
---
# <a name="map-a-cost-element-dimension"></a><span data-ttu-id="58dc9-103">Namapování dimenze prvku nákladů</span><span class="sxs-lookup"><span data-stu-id="58dc9-103">Map a cost element dimension</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="58dc9-104">Kontrolor nákladů může tento postup použít k mapování dimenze prvku nákladů k dimenzi nákladového prvku u právnické osoby MXMF.</span><span class="sxs-lookup"><span data-stu-id="58dc9-104">A cost controller can use this procedure to map a cost element dimension to a cost element dimension in the MXMF legal entity.</span></span> <span data-ttu-id="58dc9-105">Tento záznam používá v ukázkových datech společnost USP2.</span><span class="sxs-lookup"><span data-stu-id="58dc9-105">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="58dc9-106">Přejděte na položky Nákladové účetnictví > Dimenze > Dimenze prvku nákladů.</span><span class="sxs-lookup"><span data-stu-id="58dc9-106">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="58dc9-107">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="58dc9-107">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="58dc9-108">V tomto příkladu vyberte Nákladové elementy.</span><span class="sxs-lookup"><span data-stu-id="58dc9-108">For this example, select Cost elements.</span></span>  
3. <span data-ttu-id="58dc9-109">Klikněte na Mapování dimenzí.</span><span class="sxs-lookup"><span data-stu-id="58dc9-109">Click Dimension mappings.</span></span>
4. <span data-ttu-id="58dc9-110">Klikněte na Konfigurovat mapování z této dimenze.</span><span class="sxs-lookup"><span data-stu-id="58dc9-110">Click Configure mappings from this dimension.</span></span>
5. <span data-ttu-id="58dc9-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="58dc9-111">Click New.</span></span>
6. <span data-ttu-id="58dc9-112">V poli Do dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="58dc9-112">In the To dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="58dc9-113">V tomto příkladu vyberte Nákladové elementy MXMF.</span><span class="sxs-lookup"><span data-stu-id="58dc9-113">For this example, select MXMF Cost elements.</span></span>  
7. <span data-ttu-id="58dc9-114">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="58dc9-114">Click New.</span></span>
8. <span data-ttu-id="58dc9-115">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="58dc9-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="58dc9-116">V poli Od členu dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="58dc9-116">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="58dc9-117">V tomto příkladu vyberte člena dimenze – 606400 Telefonní a faxové náklady.</span><span class="sxs-lookup"><span data-stu-id="58dc9-117">For this example, select dimension member 606400 Telephone & Fax Expense.</span></span>  
10. <span data-ttu-id="58dc9-118">V poli Po člen dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="58dc9-118">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="58dc9-119">V tomto příkladu vyberte člena dimenze 6001004 Telefon.</span><span class="sxs-lookup"><span data-stu-id="58dc9-119">For this example, select dimension member 6001004 Telefono.</span></span>  
11. <span data-ttu-id="58dc9-120">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="58dc9-120">Click Save.</span></span>

