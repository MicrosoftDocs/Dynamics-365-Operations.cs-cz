---
title: Analýza příchozích dokumentů ve formátu Excel
description: Toto téma obsahuje informace o vytváření formátů elektronického výkaznictví pro analýzu obsahu v příchozích souborech aplikace Microsoft Excel.
author: NickSelin
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 0c41a062d817307adb2889d3678764f1ea4066e2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755173"
---
# <a name="parse-incoming-documents-in-excel-format"></a><span data-ttu-id="d1c2e-103">Analýza příchozích dokumentů ve formátu Excel</span><span class="sxs-lookup"><span data-stu-id="d1c2e-103">Parse incoming documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d1c2e-104">Můžete navrhovat formáty elektronického výkaznictví pro analýzu příchozích souborů aplikace Microsoft Excel, které představují data v sešitech aplikace Microsoft Excel (soubory ve formátu XLSX).</span><span class="sxs-lookup"><span data-stu-id="d1c2e-104">You can design Electronic reporting (ER) formats to parse incoming Microsoft Excel files that represent data in Microsoft Excel workbooks (files in XLSX format).</span></span> <span data-ttu-id="d1c2e-105">Poté můžete obsah z těchto souborů použít k aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="d1c2e-105">You can then use the content from these files to update application data.</span></span> <span data-ttu-id="d1c2e-106">Je to užitečné, když:</span><span class="sxs-lookup"><span data-stu-id="d1c2e-106">This is useful if you:</span></span>

- <span data-ttu-id="d1c2e-107">Navrhujete nový model a formát a chcete ho otestovat v běhu.</span><span class="sxs-lookup"><span data-stu-id="d1c2e-107">Design a new model and format and want to test them at run-time.</span></span> <span data-ttu-id="d1c2e-108">V tomto případě bude Excel simulovat data skutečné aplikace.</span><span class="sxs-lookup"><span data-stu-id="d1c2e-108">In this case, Excel will simulate the actual application data.</span></span>
- <span data-ttu-id="d1c2e-109">Spravujete data za vaší aplikací v aplikaci Excel a chcete tato data importovat pro odeslání konkrétní sestavy.</span><span class="sxs-lookup"><span data-stu-id="d1c2e-109">Manage data beyond your application in Excel and want to import this data to submit a specific report.</span></span>

<span data-ttu-id="d1c2e-110">Pro další informace o této funkci si přehrajte průvodce úloh **ER import dat ze souboru aplikace Microsoft Excel (část 1: Návrh formátu)** a **ER import dat ze souboru aplikace Microsoft Excel (část 2: Import dat)** (části 7.5.4.3 komponent Pořízení/Vývoj IT služby/řešení (10677) obchodního procesu).</span><span class="sxs-lookup"><span data-stu-id="d1c2e-110">To learn more about this feature, play the task guides **ER Import data from a Microsoft Excel file (Part 1: Design format)** and **ER Import data from a Microsoft Excel file (Part 2: Import data)** (parts of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span> <span data-ttu-id="d1c2e-111">Tyto průvodci záznamem úloh vám ukáží, jak lze analyzovat příchozí Excel soubor pomocí ER formátu pro import informací z příchozích dokumentů a aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="d1c2e-111">These task guides walk through how the incoming Excel file can be parsed by using the ER format to import information from incoming documents and update application data.</span></span> <span data-ttu-id="d1c2e-112">Průvodce záznamem úloh můžete stáhnout z [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="d1c2e-112">You can download the task guide files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

<span data-ttu-id="d1c2e-113">Pro dokončení průvodce záznamem úloh stáhněte následující soubory.</span><span class="sxs-lookup"><span data-stu-id="d1c2e-113">Download the following files to complete the task guides mentioned above.</span></span>

| <span data-ttu-id="d1c2e-114">Popis obsahu</span><span class="sxs-lookup"><span data-stu-id="d1c2e-114">Content description</span></span>                         | <span data-ttu-id="d1c2e-115">Soubor</span><span class="sxs-lookup"><span data-stu-id="d1c2e-115">File</span></span>                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="d1c2e-116">Příchozí soubor ve formátu XLSX - šablona</span><span class="sxs-lookup"><span data-stu-id="d1c2e-116">Incoming file in .XLSX format - template</span></span>    | [<span data-ttu-id="d1c2e-117">1099import-template.xlsx</span><span class="sxs-lookup"><span data-stu-id="d1c2e-117">1099import-template.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
| <span data-ttu-id="d1c2e-118">Příchozí soubor ve formátu XLSX - vzorová data</span><span class="sxs-lookup"><span data-stu-id="d1c2e-118">Incoming file in .XLSX format - sample data</span></span> | [<span data-ttu-id="d1c2e-119">1099import-data.xlsx</span><span class="sxs-lookup"><span data-stu-id="d1c2e-119">1099import-data.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)     |

<span data-ttu-id="d1c2e-120">Pokud jste si ještě nepřehráli následujícího průvodce záznamem úloh [ER – Vytvoření požadovaných konfigurací pro import dat z externího souboru](./tasks/er-required-configurations-import-data.md) v aktuální aplikaci Finance and Operations, stáhněte si následující soubor.</span><span class="sxs-lookup"><span data-stu-id="d1c2e-120">If you have not yet played the following task guide, [ER Create required configurations to import data from an external file](./tasks/er-required-configurations-import-data.md) in the current Finance and Operations application, download the following file.</span></span>

| <span data-ttu-id="d1c2e-121">Popis obsahu</span><span class="sxs-lookup"><span data-stu-id="d1c2e-121">Content description</span></span>    | <span data-ttu-id="d1c2e-122">Soubor</span><span class="sxs-lookup"><span data-stu-id="d1c2e-122">File</span></span>                                                            |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d1c2e-123">Konfigurace modelu ER</span><span class="sxs-lookup"><span data-stu-id="d1c2e-123">ER model configuration</span></span> | [<span data-ttu-id="d1c2e-124">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="d1c2e-124">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]