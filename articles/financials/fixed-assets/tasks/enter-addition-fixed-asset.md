---
title: Zadání příslušenství dlouhodobého majetku
description: Tento postup popisuje přidání příslušenství k existujícímu dlouhodobému majetku.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c9733f07f995dd37669f3c33fd0f082daa34dd2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566931"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="6a0f6-103">Zadání příslušenství dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="6a0f6-103">Enter an addition to a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6a0f6-104">Tento postup popisuje přidání příslušenství k existujícímu dlouhodobému majetku.</span><span class="sxs-lookup"><span data-stu-id="6a0f6-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="6a0f6-105">Účel příslušenství k dlouhodobému majetku je sledování příslušenství, údržby nebo vylepšení majetku, a je pouze informativní.</span><span class="sxs-lookup"><span data-stu-id="6a0f6-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="6a0f6-106">Veškeré změny hodnot nebo životnosti dlouhodobého majetku je nutné provést samostatně.</span><span class="sxs-lookup"><span data-stu-id="6a0f6-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   



<span data-ttu-id="6a0f6-107">Postup využívá účetní role a ukázková data pro právnické osoby USMF.</span><span class="sxs-lookup"><span data-stu-id="6a0f6-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="6a0f6-108">Přejděte do části Dlouhodobý majetek > Dlouhodobý majetek > Dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="6a0f6-108">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="6a0f6-109">V seznamu najděte a vyberte dlouhodobý majetek pro příslušenství.</span><span class="sxs-lookup"><span data-stu-id="6a0f6-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="6a0f6-110">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="6a0f6-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6a0f6-111">V podokně akcí klikněte na možnost Dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="6a0f6-111">On the Action Pane, click Fixed asset.</span></span>
5. <span data-ttu-id="6a0f6-112">Klikněte na Příslušenství dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="6a0f6-112">Click Fixed asset additions.</span></span>
6. <span data-ttu-id="6a0f6-113">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="6a0f6-113">Click New.</span></span>
7. <span data-ttu-id="6a0f6-114">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="6a0f6-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="6a0f6-115">Nastavte datum nákupu příslušenství nebo služby.</span><span class="sxs-lookup"><span data-stu-id="6a0f6-115">Set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="6a0f6-116">Zadejte cenu položky, údržby nebo jiného zlepšení majetku.</span><span class="sxs-lookup"><span data-stu-id="6a0f6-116">Enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="6a0f6-117">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="6a0f6-117">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="6a0f6-118">Celkové náklady nebudou mít vliv na hodnotu dlouhodobého majetku a slouží pouze ke sledování a informačním účelům.</span><span class="sxs-lookup"><span data-stu-id="6a0f6-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="6a0f6-119">Pokud dojde ke kapitalizaci nákladů, je nutné transakce navýšení hodnoty zaúčtovat samostatně.</span><span class="sxs-lookup"><span data-stu-id="6a0f6-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="6a0f6-120">Klikněte na záložku Obecné.</span><span class="sxs-lookup"><span data-stu-id="6a0f6-120">Click the General tab.</span></span>
    * <span data-ttu-id="6a0f6-121">Použijte možnost Prodlužuje dobu životnosti, pokud příslušenství prodlužuje dobu životnosti majetku.</span><span class="sxs-lookup"><span data-stu-id="6a0f6-121">Set Increases service life if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="6a0f6-122">Toto pole slouží pouze k informačním účelům.</span><span class="sxs-lookup"><span data-stu-id="6a0f6-122">This field is informational only.</span></span> <span data-ttu-id="6a0f6-123">Chcete-li prodloužit dobu životnosti, upravte hodnotu Doba životnosti pro Účetní odpisy a/nebo Knihy odpisů pro majetek.</span><span class="sxs-lookup"><span data-stu-id="6a0f6-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  

