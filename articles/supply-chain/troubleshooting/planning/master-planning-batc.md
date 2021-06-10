---
title: Položky hlavního plánování nemůžete filtrovat podle jejich souvisejících hodnot skupiny pokrytí
description: Položky hlavního plánování nemůžete filtrovat podle jejich souvisejících hodnot skupiny pokrytí.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049457"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a><span data-ttu-id="785ba-103">Položky hlavního plánování nemůžete filtrovat podle jejich souvisejících hodnot skupiny pokrytí</span><span class="sxs-lookup"><span data-stu-id="785ba-103">You can't filter master planning items by their related coverage group values</span></span>

<span data-ttu-id="785ba-104">Číslo článku znalostní báze: 4612572</span><span class="sxs-lookup"><span data-stu-id="785ba-104">KB number: 4612572</span></span>

## <a name="symptoms"></a><span data-ttu-id="785ba-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="785ba-105">Symptoms</span></span>

<span data-ttu-id="785ba-106">Chcete filtrovat položky, které budou zahrnuty do dávkové úlohy hlavního plánování, na základě hodnot souvisejících záznamů z tabulky pokrytí položek.</span><span class="sxs-lookup"><span data-stu-id="785ba-106">You want to filter the items that will be included in a master planning batch job, based on the values of related records from the item coverage table.</span></span> <span data-ttu-id="785ba-107">(Například chcete filtrovat položky podle jejich hodnot **Prodejce** a/nebo **Skupina pokrytí**).</span><span class="sxs-lookup"><span data-stu-id="785ba-107">(For example, you want to filter items by their **Vendor** and/or **Coverage group** value).</span></span> <span data-ttu-id="785ba-108">Nastavení filtru pro dávkovou úlohu vám umožní vytvořit spojení z tabulky **Položky** do tabulky **Pokrytí položky** a poté v dotazu zadejte hodnoty polí z tabulky pokrytí položky.</span><span class="sxs-lookup"><span data-stu-id="785ba-108">The filter setup for the batch job lets you create a join from the **Items** table to the **Item coverage** table, and then specify field values from the item coverage table in your query.</span></span> <span data-ttu-id="785ba-109">Po dokončení tohoto nastavení však systém stále vytváří plánované objednávky pro celé pokrytí položky, nejen pro položky, které odpovídají zadaným hodnotám polí z tabulky pokrytí položky.</span><span class="sxs-lookup"><span data-stu-id="785ba-109">However, after you complete this setup, the system still creates planned orders for the whole item coverage, not just for the items that match the specified field values from the item coverage table.</span></span>

## <a name="resolution"></a><span data-ttu-id="785ba-110">Řešení</span><span class="sxs-lookup"><span data-stu-id="785ba-110">Resolution</span></span>

<span data-ttu-id="785ba-111">Filtr dávkové úlohy může filtrovat pouze na položky.</span><span class="sxs-lookup"><span data-stu-id="785ba-111">The batch job filter can filter only on items.</span></span> <span data-ttu-id="785ba-112">I když můžete propojení tabulky **Pokrytí položky**, nastavení filtru, které v této tabulce provedete, neovlivní výstup dotazu.</span><span class="sxs-lookup"><span data-stu-id="785ba-112">Although you can add a join to the **Item coverage** table, filter settings that you make against that table won't affect the query output.</span></span> <span data-ttu-id="785ba-113">Za běhu systém spustí plánování pro všechny skupiny pokrytí a všechny varianty, které mají filtrované položky.</span><span class="sxs-lookup"><span data-stu-id="785ba-113">At runtime, the system runs planning for all the coverage groups and all the variations that the filtered items have.</span></span> <span data-ttu-id="785ba-114">Poté, co je položka již zahrnuta v běhu, žádné skupiny pokrytí, které jsou zahrnuty ve filtru položek, neovlivní výstup plánování.</span><span class="sxs-lookup"><span data-stu-id="785ba-114">After an item is already included in the run, any coverage groups that are included in the item filter a won't affect the planning output.</span></span>
