---
title: Analýza příchozích dokumentů ve formátu Excel
description: Toto téma obsahuje informace o vytváření formátů elektronického výkaznictví pro analýzu obsahu v příchozích souborech aplikace Microsoft Excel.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
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
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 490a9325be25908564a40478a1ee29feea67fc02
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545046"
---
# <a name="parse-incoming-documents-in-excel-format"></a><span data-ttu-id="84ecd-103">Analýza příchozích dokumentů ve formátu Excel</span><span class="sxs-lookup"><span data-stu-id="84ecd-103">Parse incoming documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="84ecd-104">Můžete navrhovat formáty elektronického výkaznictví pro analýzu příchozích souborů aplikace Microsoft Excel, které představují data v sešitech aplikace Microsoft Excel (soubory ve formátu XLSX).</span><span class="sxs-lookup"><span data-stu-id="84ecd-104">You can design Electronic reporting (ER) formats to parse incoming Microsoft Excel files that represent data in Microsoft Excel workbooks (files in XLSX format).</span></span> <span data-ttu-id="84ecd-105">Poté můžete obsah z těchto souborů použít k aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="84ecd-105">You can then use the content from these files to update application data.</span></span> <span data-ttu-id="84ecd-106">Je to užitečné, když:</span><span class="sxs-lookup"><span data-stu-id="84ecd-106">This is useful if you:</span></span>

- <span data-ttu-id="84ecd-107">Navrhujete nový model a formát a chcete ho otestovat v běhu.</span><span class="sxs-lookup"><span data-stu-id="84ecd-107">Design a new model and format and want to test them at run-time.</span></span> <span data-ttu-id="84ecd-108">V tomto případě bude Excel simulovat data skutečné aplikace.</span><span class="sxs-lookup"><span data-stu-id="84ecd-108">In this case, Excel will simulate the actual application data.</span></span>
- <span data-ttu-id="84ecd-109">Spravujete data za vaší aplikací v aplikaci Excel a chcete tato data importovat pro odeslání konkrétní sestavy.</span><span class="sxs-lookup"><span data-stu-id="84ecd-109">Manage data beyond your application in Excel and want to import this data to submit a specific report.</span></span>

<span data-ttu-id="84ecd-110">Pro další informace o této funkci si přehrajte průvodce úloh **ER import dat ze souboru aplikace Microsoft Excel (část 1: Návrh formátu)** a **ER import dat ze souboru aplikace Microsoft Excel (část 2: Import dat)** (části 7.5.4.3 komponent Pořízení/Vývoj IT služby/řešení (10677) obchodního procesu).</span><span class="sxs-lookup"><span data-stu-id="84ecd-110">To learn more about this feature, play the task guides **ER Import data from a Microsoft Excel file (Part 1: Design format)** and **ER Import data from a Microsoft Excel file (Part 2: Import data)** (parts of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span> <span data-ttu-id="84ecd-111">Tyto průvodci záznamem úloh vám ukáží, jak lze analyzovat příchozí Excel soubor pomocí ER formátu pro import informací z příchozích dokumentů a aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="84ecd-111">These task guides walk through how the incoming Excel file can be parsed by using the ER format to import information from incoming documents and update application data.</span></span> <span data-ttu-id="84ecd-112">Průvodce záznamem úloh můžete stáhnout z [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="84ecd-112">You can download the task guide files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

<span data-ttu-id="84ecd-113">Pro dokončení průvodce záznamem úloh stáhněte následující soubory.</span><span class="sxs-lookup"><span data-stu-id="84ecd-113">Download the following files to complete the task guides mentioned above.</span></span>

| <span data-ttu-id="84ecd-114">Popis obsahu</span><span class="sxs-lookup"><span data-stu-id="84ecd-114">Content description</span></span>                         | <span data-ttu-id="84ecd-115">Soubor</span><span class="sxs-lookup"><span data-stu-id="84ecd-115">File</span></span>                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="84ecd-116">Příchozí soubor ve formátu XLSX - šablona</span><span class="sxs-lookup"><span data-stu-id="84ecd-116">Incoming file in .XLSX format - template</span></span>    | [<span data-ttu-id="84ecd-117">1099import-template.xlsx</span><span class="sxs-lookup"><span data-stu-id="84ecd-117">1099import-template.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
| <span data-ttu-id="84ecd-118">Příchozí soubor ve formátu XLSX - vzorová data</span><span class="sxs-lookup"><span data-stu-id="84ecd-118">Incoming file in .XLSX format - sample data</span></span> | [<span data-ttu-id="84ecd-119">1099import-data.xlsx</span><span class="sxs-lookup"><span data-stu-id="84ecd-119">1099import-data.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)     |

<span data-ttu-id="84ecd-120">Pokud jste si ještě nepřehráli následující průvodce záznamem úloh [ER vytvoření požadované konfigurace pro import dat z externího souboru](./tasks/er-required-configurations-import-data.md) v aktuální aplikaci Dynamics 365 for Finance and Operations, stáhněte si následující soubor.</span><span class="sxs-lookup"><span data-stu-id="84ecd-120">If you have not yet played the following task guide, [ER Create required configurations to import data from an external file](./tasks/er-required-configurations-import-data.md) in the current Dynamics 365 for Finance and Operation application, download the following file.</span></span>

| <span data-ttu-id="84ecd-121">Popis obsahu</span><span class="sxs-lookup"><span data-stu-id="84ecd-121">Content description</span></span>    | <span data-ttu-id="84ecd-122">Soubor</span><span class="sxs-lookup"><span data-stu-id="84ecd-122">File</span></span>                                                            |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="84ecd-123">Konfigurace modelu ER</span><span class="sxs-lookup"><span data-stu-id="84ecd-123">ER model configuration</span></span> | [<span data-ttu-id="84ecd-124">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="84ecd-124">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
