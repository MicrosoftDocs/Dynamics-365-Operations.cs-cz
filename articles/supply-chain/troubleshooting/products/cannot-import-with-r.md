---
title: Položku nelze importovat pomocí entity Vydané produkty V2
description: Položku nelze importovat pomocí entity Vydané produkty V2.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026329"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a><span data-ttu-id="3af84-103">Položku nelze importovat pomocí entity Vydané produkty V2</span><span class="sxs-lookup"><span data-stu-id="3af84-103">You can't import an item by using the Released products V2 entity</span></span>

<span data-ttu-id="3af84-104">Číslo článku znalostní báze: 4611825</span><span class="sxs-lookup"><span data-stu-id="3af84-104">KB number: 4611825</span></span>

## <a name="symptoms"></a><span data-ttu-id="3af84-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="3af84-105">Symptoms</span></span>

<span data-ttu-id="3af84-106">Když se pokusíte importovat položku pomocí entity *Vydané produkty V2*, zobrazí se chybová zpráva podobná následujícímu příkladu:</span><span class="sxs-lookup"><span data-stu-id="3af84-106">When you try to import an item by using the *Released products V2* entity, you receive an error message that resembles the following example:</span></span>

> <span data-ttu-id="3af84-107">Nelze vytvořit záznam ve skupinách Položky - sledovací dimenze (EcoResTrackingDimensionGroupItem).</span><span class="sxs-lookup"><span data-stu-id="3af84-107">Cannot create a record in Items - tracking dimension groups (EcoResTrackingDimensionGroupItem).</span></span> <span data-ttu-id="3af84-108">Číslo položky: 2040663, dávka.</span><span class="sxs-lookup"><span data-stu-id="3af84-108">Item number: 2040663, Batch.</span></span> <span data-ttu-id="3af84-109">Záznam již existuje.</span><span class="sxs-lookup"><span data-stu-id="3af84-109">The record already exists.</span></span>

## <a name="resolution"></a><span data-ttu-id="3af84-110">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="3af84-110">Resolution</span></span>

<span data-ttu-id="3af84-111">Chcete-li importovat nově vydané produkty, musíte použít entitu *Vydání produktu V2* místo entity *Vydané produkty V2*.</span><span class="sxs-lookup"><span data-stu-id="3af84-111">To import new released products, you must use the *Released product creation V2* entity instead of the *Released products V2* entity.</span></span>
