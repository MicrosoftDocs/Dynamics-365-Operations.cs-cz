---
title: Výstupní místo výroby
description: Toto téma popisuje hierarchii, která se používá k identifikaci výstupního místa výroby.
author: johanhoffmann
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 48b68c36718fa42b7f80e3ffe1f54b7efbbee8bd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814625"
---
# <a name="production-output-location"></a><span data-ttu-id="45cf9-103">Výstupní místo výroby</span><span class="sxs-lookup"><span data-stu-id="45cf9-103">Production output location</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45cf9-104">Toto téma popisuje hierarchii, která se používá k identifikaci výstupního místa výroby.</span><span class="sxs-lookup"><span data-stu-id="45cf9-104">This topic describes the hierarchy that is used to identify the production output location.</span></span>

<span data-ttu-id="45cf9-105">Výstupní místo výroby je místo, kam se nejprve uloží hotové zboží poté, co je vyrobeno.</span><span class="sxs-lookup"><span data-stu-id="45cf9-105">The production output location is the location where a finished good is first stored after it's produced.</span></span> <span data-ttu-id="45cf9-106">Tohoto skladové místo je obvykle blízko výrobního procesu, který vytváří dokončené zboží.</span><span class="sxs-lookup"><span data-stu-id="45cf9-106">Usually, this location is close to the production process that produces the finished good.</span></span> <span data-ttu-id="45cf9-107">Výstupní místo výroby se používá jako dočasné úložiště pro materiál před jeho přesunutím do oblasti expedice, skladovacího místa, vstupního místa výroby pro proces výroby směrem dolů, atd.</span><span class="sxs-lookup"><span data-stu-id="45cf9-107">The production output location is used as intermediate storage for the material before it's moved on to the shipment area, a storage location, a production input location for a downstream production process, and so on.</span></span> 

<span data-ttu-id="45cf9-108">Výchozí výstupní místo výroby je nastaveno, když je dokončené vykázáno ve výrobním příkazu nebo dávkové objednávce.</span><span class="sxs-lookup"><span data-stu-id="45cf9-108">A default production output location is set when finished goods are reported on a production order or batch order.</span></span> <span data-ttu-id="45cf9-109">Následující hierarchie se používá k identifikaci tohoto výstupního místa:</span><span class="sxs-lookup"><span data-stu-id="45cf9-109">The following hierarchy is used to identify this output location:</span></span>

1. <span data-ttu-id="45cf9-110">Použijte výstupní místo definované v záhlaví výrobní zakázky nebo dávkové objednávky.</span><span class="sxs-lookup"><span data-stu-id="45cf9-110">Use the output location that is defined on the production order or batch order header.</span></span>
2. <span data-ttu-id="45cf9-111">Pokud zde není nalezeno žádné místo, použijte výstupní místo, které je definováno ve zdroji, který byl použit v poslední operaci definované ve výrobním postupu.</span><span class="sxs-lookup"><span data-stu-id="45cf9-111">If no location is found there, use the output location that is defined on the resource that is used by the last operation that is defined in the production route.</span></span>
3. <span data-ttu-id="45cf9-112">Pokud zde není nalezeno žádné místo, použijte výstupní místo, které je definováno ve skupině zdrojů používané zdrojem, který byl použit v poslední operaci definované ve výrobním postupu.</span><span class="sxs-lookup"><span data-stu-id="45cf9-112">If no location is found there, use the output location that is defined on the resource group that is used by the resource for the last operation that is defined in the production route.</span></span>
4. <span data-ttu-id="45cf9-113">Pokud zde není nalezeno žádné místo, použijte výstupní místo, které je definováno pro sklad, který je definován pro výrobní zakázku.</span><span class="sxs-lookup"><span data-stu-id="45cf9-113">If no location is found there, use the output location that is defined on the warehouse that is defined for the production order.</span></span>

<span data-ttu-id="45cf9-114">Výchozí výstupní místo výroby je nastaveno pouze pro produkty, které se nastavují pomocí rozšířených skladových procesů.</span><span class="sxs-lookup"><span data-stu-id="45cf9-114">A default production output location is set only for products that are set up by using advanced warehouse processes.</span></span> <span data-ttu-id="45cf9-115">Když je tento typ zboží nahlášen jako dokončený, vytvoří se skladová práce typu **Odložení hotového zboží** nebo **Odložení společných a vedlejších produktů**.</span><span class="sxs-lookup"><span data-stu-id="45cf9-115">When this type of item is reported as finished, warehouse work of the **Finished goods put away** or **Co-product and by-product put away** type is created.</span></span> <span data-ttu-id="45cf9-116">Tento typ práce používá výstupní místo výroby jako místo pro výdej.</span><span class="sxs-lookup"><span data-stu-id="45cf9-116">This type of work uses the production output location as the pick location.</span></span> <span data-ttu-id="45cf9-117">Místo pro odložení je určeno směrnicemi místa.</span><span class="sxs-lookup"><span data-stu-id="45cf9-117">The put-away location is determined by the location directives.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]