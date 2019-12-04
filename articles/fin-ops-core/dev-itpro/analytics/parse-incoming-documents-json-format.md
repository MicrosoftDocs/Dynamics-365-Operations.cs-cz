---
title: Analýza příchozích dokumentů ve formátu JSON
description: V tomto tématu je vysvětleno, jak nastavit formáty elektronického výkaznictví pro analýzu příchozích dokumentů ve formátu JSON.
author: kfend
manager: AnnBe
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 8be4e225507a18a92d642ff0f3a6ca3d0ff68564
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772528"
---
# <a name="parse-incoming-documents-in-json-format"></a><span data-ttu-id="3870c-103">Analýza příchozích dokumentů ve formátu JSON</span><span class="sxs-lookup"><span data-stu-id="3870c-103">Parse incoming documents in JSON format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3870c-104">Formáty elektronického výkaznictví lze navrhovat k analýze příchozích elektronických dokumentů, které reprezentují data v textovém formátu založeném na jazyku JavaScript (jinými slovy, soubory ve formátu \[JSON\]).</span><span class="sxs-lookup"><span data-stu-id="3870c-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents that represent data in a text format that is based on JavaScript (in other words, files in JavaScript Object Notation \[JSON\] format).</span></span>

<span data-ttu-id="3870c-105">Chcete-li získat další informace o této funkci, stáhněte soubory v následující tabulce a poté přehrajte průvodce záznamem úloh Vytvoření konfigurace formátu pro import dat z externího souboru JSON.</span><span class="sxs-lookup"><span data-stu-id="3870c-105">To learn more about this feature, download the files in the following table, and then play the ER Create a format configuration to import data from an external JSON file task guide.</span></span> <span data-ttu-id="3870c-106">Tento průvodce záznamem úloh ukazuje, jak lze použít formát elektronického výkaznictví k analýze příchozího souboru JSON pro aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="3870c-106">This task guide shows how an ER format can be used to parse an incoming JSON file to update application data.</span></span>

| <span data-ttu-id="3870c-107">Titul</span><span class="sxs-lookup"><span data-stu-id="3870c-107">Title</span></span>                                  | <span data-ttu-id="3870c-108">Název souboru</span><span class="sxs-lookup"><span data-stu-id="3870c-108">File name</span></span> |
|----------------------------------------|-----------|
| <span data-ttu-id="3870c-109">Konfigurace formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="3870c-109">ER format configuration</span></span>                | [<span data-ttu-id="3870c-110">Formát pro import souboru trans_JSON. XML dodavatelů</span><span class="sxs-lookup"><span data-stu-id="3870c-110">Format for importing vendors' trans_JSON.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
| <span data-ttu-id="3870c-111">Ukázka příchozího souboru ve formátu CSV</span><span class="sxs-lookup"><span data-stu-id="3870c-111">Sample of incoming file in .csv format</span></span> | [<span data-ttu-id="3870c-112">1099entries_JSON.txt</span><span class="sxs-lookup"><span data-stu-id="3870c-112">1099entries_JSON.txt</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a><span data-ttu-id="3870c-113">Požadavky</span><span class="sxs-lookup"><span data-stu-id="3870c-113">Requirements</span></span>

<span data-ttu-id="3870c-114">Před dokončením průvodce záznamem úloh Vytvoření konfigurace formátu pro import dat z externího souboru JSON je nutné splnit následující požadavky:</span><span class="sxs-lookup"><span data-stu-id="3870c-114">Before you complete the ER Create a format configuration to import data from an external JSON file task guide, the following requirement must be met:</span></span>

- <span data-ttu-id="3870c-115">Nadřazené prvky v souboru JSON mohou být pouze objektové prvky.</span><span class="sxs-lookup"><span data-stu-id="3870c-115">Parent elements in the JSON file can be only object elements.</span></span>
- <span data-ttu-id="3870c-116">Vnořené prvky pro objekt by měly být prvky vlastností, aby byla vytvořena platná struktura JSON.</span><span class="sxs-lookup"><span data-stu-id="3870c-116">Nested elements for an object should be property elements, so that a valid JSON structure is created.</span></span>
- <span data-ttu-id="3870c-117">Pole JSON mohou být pouze vnořenými prvky prvků vlastnosti objektu.</span><span class="sxs-lookup"><span data-stu-id="3870c-117">JSON arrays can be only nested elements of the property elements of an object.</span></span>
- <span data-ttu-id="3870c-118">Pole JSON mohou obsahovat pouze objekty JSON.</span><span class="sxs-lookup"><span data-stu-id="3870c-118">JSON arrays can contain only JSON objects.</span></span> <span data-ttu-id="3870c-119">Nemohou obsahovat přímé řetězcové nebo číselné hodnoty a vnořená pole.</span><span class="sxs-lookup"><span data-stu-id="3870c-119">They can't contain direct string/numeric values and nested arrays.</span></span> <span data-ttu-id="3870c-120">Prvky v těchto polích budou analyzovány v pořadí, jak jsou uvedeny ve formátu.</span><span class="sxs-lookup"><span data-stu-id="3870c-120">Elements in these arrays will be parsed in order, as they are specified in the format.</span></span> <span data-ttu-id="3870c-121">V každém objektu JSON bude zváženo nastavení násobnosti.</span><span class="sxs-lookup"><span data-stu-id="3870c-121">Multiplicity settings on each JSON object will be considered.</span></span>

<span data-ttu-id="3870c-122">Dále je nutné dokončit průvodce záznamem úloh[Vytvoření požadovaných konfigurací importu dat z externího souboru pro elektronické vykazování](tasks/er-required-configurations-import-data.md) v případě, že jste ho ještě nedokončili.</span><span class="sxs-lookup"><span data-stu-id="3870c-122">Additionally, you must complete the [ER Create required configurations to import data from an external file](tasks/er-required-configurations-import-data.md) task guide if you haven't already completed it.</span></span> <span data-ttu-id="3870c-123">Pro dokončení průvodce záznamem úloh stáhněte následující soubor.</span><span class="sxs-lookup"><span data-stu-id="3870c-123">Download the following file to complete the task guide.</span></span>

| <span data-ttu-id="3870c-124">Titul</span><span class="sxs-lookup"><span data-stu-id="3870c-124">Title</span></span>                  | <span data-ttu-id="3870c-125">Název souboru</span><span class="sxs-lookup"><span data-stu-id="3870c-125">File name</span></span> |
|------------------------|-----------|
| <span data-ttu-id="3870c-126">Konfigurace modelu ER</span><span class="sxs-lookup"><span data-stu-id="3870c-126">ER model configuration</span></span> | [<span data-ttu-id="3870c-127">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="3870c-127">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
