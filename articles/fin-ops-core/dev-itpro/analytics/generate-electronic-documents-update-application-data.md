---
title: Generování elektronických dokumentů a aktualizace dat aplikace pomocí elektronického výkaznictví
description: Můžete vytvářet formáty elektronického výkaznictví (ER), které lze použít v aplikaci ke generování odchozích elektronických dokumentů.
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ae3405a882ac37fd9758d8ff0902896562fa06b
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093866"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a><span data-ttu-id="97c96-103">Generování elektronických dokumentů a aktualizace dat aplikace pomocí elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="97c96-103">Generate electronic documents and update application data by using ER</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97c96-104">Můžete vytvářet formáty elektronického výkaznictví (ER), které lze použít v aplikaci ke generování odchozích elektronických dokumentů.</span><span class="sxs-lookup"><span data-stu-id="97c96-104">You can design Electronic reporting (ER) formats that can be used in the application to generate outgoing electronic documents.</span></span> <span data-ttu-id="97c96-105">Můžete vytvořit také formáty ER, které analyzují příchozí elektronické dokumenty, a použít jejich obsah k aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="97c96-105">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span>

<span data-ttu-id="97c96-106">Pomocí této funkce lze použít jeden formát ER pro generování odchozích elektronických dokumentů a následné aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="97c96-106">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="97c96-107">Tuto funkci lze využít v těchto případech:</span><span class="sxs-lookup"><span data-stu-id="97c96-107">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="97c96-108">Abyste zabránili opakovanému použití dat aplikace u dalších procesů, můžete je označit hned poté, co budou využita k vygenerování elektronických dokumentů.</span><span class="sxs-lookup"><span data-stu-id="97c96-108">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="97c96-109">Můžete například označit platební transakce jako zpracované ihned po jejich začlenění do vygenerované zprávy o platbě.</span><span class="sxs-lookup"><span data-stu-id="97c96-109">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="97c96-110">Můžete uložit podrobnosti o zpracování elektronických dokumentů vygenerovaných pomocí logiky ER.</span><span class="sxs-lookup"><span data-stu-id="97c96-110">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="97c96-111">Může se jednat například o jedinečnou identifikaci zpráv o platbě vygenerovanou pomocí výrazu ER.</span><span class="sxs-lookup"><span data-stu-id="97c96-111">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="97c96-112">Výraz je založen na informacích zadaných v dialogovém okně ER při spuštění formátu ER za účelem vygenerování dokumentů.</span><span class="sxs-lookup"><span data-stu-id="97c96-112">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="97c96-113">Další informace o této funkci získáte v průvodcích záznamem úloh pro generování dokumentů ER s aktualizací dat aplikace (součást obchodního procesu 7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)), které vás provedou procesy výkaznictví a archivace Intrastat.</span><span class="sxs-lookup"><span data-stu-id="97c96-113">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="97c96-114">K dokončení některých kroků v průvodcích jsou nutné následující soubory.</span><span class="sxs-lookup"><span data-stu-id="97c96-114">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="97c96-115">Stáhněte si je a uložte je do místního počítače.</span><span class="sxs-lookup"><span data-stu-id="97c96-115">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="97c96-116">Konfigurace modelu dat ER: Intrastat (model)</span><span class="sxs-lookup"><span data-stu-id="97c96-116">ER data model configuration: Intrastat (model)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="97c96-117">Konfigurace mapování modelu ER: Intrastat (mapování)</span><span class="sxs-lookup"><span data-stu-id="97c96-117">ER model mapping configuration: Intrastat (mapping)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="97c96-118">Konfigurace formátu ER: Intrastat (formát)</span><span class="sxs-lookup"><span data-stu-id="97c96-118">ER format configuration: Intrastat (format)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
