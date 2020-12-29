---
title: Značení zásob s optimalizací plánování
description: Toto téma poskytuje informace o možnostech, které jsou k dispozici pro označení zásob v potvrzených objednávkách, když používáte optimalizaci plánování.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 99a52c03e519384955d68d7101a7b73b7e9a7af6
ms.sourcegitcommit: fe21a3a98dcf6fe4eb9351941493f2c0443d8696
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672175"
---
# <a name="inventory-marking-with-planning-optimization"></a><span data-ttu-id="ca5fb-103">Značení zásob s optimalizací plánování</span><span class="sxs-lookup"><span data-stu-id="ca5fb-103">Inventory marking with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ca5fb-104">Toto téma poskytuje informace o možnostech, které jsou k dispozici pro označení zásob v potvrzených objednávkách, když používáte optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="ca5fb-104">This topic provides information about the options that are available for marking inventory in firmed orders when you use Planning Optimization.</span></span>

<span data-ttu-id="ca5fb-105">*Označení* slouží k propojení nabídky a poptávky.</span><span class="sxs-lookup"><span data-stu-id="ca5fb-105">*Marking* is used to link supply and demand.</span></span> <span data-ttu-id="ca5fb-106">Připomíná to *doložení*, které označuje, jak hlavní plánování očekává pokrytí poptávky.</span><span class="sxs-lookup"><span data-stu-id="ca5fb-106">It resembles *pegging*, which indicates how master planning expects to cover demand.</span></span> <span data-ttu-id="ca5fb-107">Z hlediska plánování je hlavní rozdíl v tom, že značení je trvalejší než doložení.</span><span class="sxs-lookup"><span data-stu-id="ca5fb-107">From a planning point of view, the main difference is that marking is more permanent than pegging.</span></span>

<span data-ttu-id="ca5fb-108">Značení bylo zavedeno na podporu speciálních scénářů výpočtu nákladů pro metody FIFO a LIFO.</span><span class="sxs-lookup"><span data-stu-id="ca5fb-108">Marking was introduced to support special costing scenarios for first in, first out (FIFO) and last in, first out (LIFO).</span></span> <span data-ttu-id="ca5fb-109">Nyní se však také používá pro některé scénáře bez výpočtu nákladů.</span><span class="sxs-lookup"><span data-stu-id="ca5fb-109">However, it's now also used for some non-costing scenarios.</span></span> <span data-ttu-id="ca5fb-110">Označení mezi nabídkou a poptávkou je volitelné a téměř trvalé.</span><span class="sxs-lookup"><span data-stu-id="ca5fb-110">Marking between supply and demand is optional and almost permanent.</span></span> <span data-ttu-id="ca5fb-111">Označení může uživatel odstranit ručně nebo ho lze odstranit spuštěním rozpadu řádku prodejní objednávky, kde je vybrána možnost **Odstranit označení**.</span><span class="sxs-lookup"><span data-stu-id="ca5fb-111">Marking can be removed manually by a user, or it can be removed by running a sales order line explosion where the **Remove marking** option is selected.</span></span>

<span data-ttu-id="ca5fb-112">Doložení je řízeno hlavním plánováním během pokrytí, aby se propojila poptávka s požadovanou nabídkou.</span><span class="sxs-lookup"><span data-stu-id="ca5fb-112">Pegging is controlled by master planning during coverage to link demand with the required supply.</span></span> <span data-ttu-id="ca5fb-113">Doložení lze aktualizovat pro každé spuštění plánování, aby se optimalizovala nabídka, která je nutná k pokrytí poptávky.</span><span class="sxs-lookup"><span data-stu-id="ca5fb-113">Pegging can be updated for each planning run to optimize the supply that is required to cover demand.</span></span> <span data-ttu-id="ca5fb-114">Když hlavní plánování aktualizuje informace o doložení, respektuje jakékoli stávající označení.</span><span class="sxs-lookup"><span data-stu-id="ca5fb-114">When master planning updates pegging information, it respects any existing marking.</span></span>

<span data-ttu-id="ca5fb-115">Doložení začíná zahrnutím příslušného značení, rezervací zásob na skladě a rezervací na objednávce v následujícím pořadí:</span><span class="sxs-lookup"><span data-stu-id="ca5fb-115">Pegging starts by including relevant marking, on-hand reservations, and on-order reservations, in the following sequence:</span></span>

1. <span data-ttu-id="ca5fb-116">Značení mezi poptávkou a nabídkou</span><span class="sxs-lookup"><span data-stu-id="ca5fb-116">Marking between demand and supply</span></span>
1. <span data-ttu-id="ca5fb-117">Rezervace zásob na skladě</span><span class="sxs-lookup"><span data-stu-id="ca5fb-117">On-hand reservations</span></span>
1. <span data-ttu-id="ca5fb-118">Rezervace na objednávce</span><span class="sxs-lookup"><span data-stu-id="ca5fb-118">On-order reservations</span></span>

<span data-ttu-id="ca5fb-119">Když zpracujete plánovanou objednávku, dialogové okno **Potvrzení** poskytuje pole **Aktualizovat označení**, které používáte k nastavení možností značení pro objednávky, které jsou vytvářeny během potvrzování.</span><span class="sxs-lookup"><span data-stu-id="ca5fb-119">When you firm a planned order, the **Firming** dialog box provides an **Update marking** field that you use to set marking options for the orders that are created during firming.</span></span> <span data-ttu-id="ca5fb-120">Vyberte jednu z následujících hodnot:</span><span class="sxs-lookup"><span data-stu-id="ca5fb-120">Select one of the following values:</span></span>

- <span data-ttu-id="ca5fb-121">**Ne** - Není použito žádné označení zásob.</span><span class="sxs-lookup"><span data-stu-id="ca5fb-121">**No** – No inventory marking is applied.</span></span>
- <span data-ttu-id="ca5fb-122">**Standardní** – Označení zásob se aktualizuje podle doložení.</span><span class="sxs-lookup"><span data-stu-id="ca5fb-122">**Standard** – Inventory marking is updated according to the pegging.</span></span> <span data-ttu-id="ca5fb-123">Objednávka požadavku (poptávka) se označí podle objednávky splnění (nabídka).</span><span class="sxs-lookup"><span data-stu-id="ca5fb-123">A requirement order (demand) is marked against a fulfillment order (supply).</span></span> <span data-ttu-id="ca5fb-124">Pokud na objednávce plnění zůstane nějaké množství, není označeno a referenční informace zůstanou prázdné.</span><span class="sxs-lookup"><span data-stu-id="ca5fb-124">If some quantity remains on the fulfillment order, it isn't marked, and the reference information is left blank.</span></span> <span data-ttu-id="ca5fb-125">Například pokud je prodejní objednávka na 100 ea doložena proti nákupní objednávce na 150 ea, referenční informace budou přiřazeny pouze k prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="ca5fb-125">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned only to the sales order.</span></span>
- <span data-ttu-id="ca5fb-126">**Rozšířený** – Označí se objednávka požadavku (poptávka) i objednávka splnění (nabídka) bez ohledu na to, zda v objednávce splnění zůstane nějaké množství nebo ne.</span><span class="sxs-lookup"><span data-stu-id="ca5fb-126">**Extended** – Both the requirement order (demand) and the fulfillment order (supply) are marked, regardless of any quantity that remains on the fulfillment order.</span></span> <span data-ttu-id="ca5fb-127">Například pokud je prodejní objednávka na 100 ea doložena proti nákupní objednávce na 150 ea, referenční informace budou přiřazeny jak k prodejní objednávce, tak k nákupní objednávce.</span><span class="sxs-lookup"><span data-stu-id="ca5fb-127">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned to both the sales order and the purchase order.</span></span>
