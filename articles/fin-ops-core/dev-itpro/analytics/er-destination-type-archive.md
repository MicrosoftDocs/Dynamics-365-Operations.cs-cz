---
title: Typ cílového místa elektronického výkaznictví archivu
description: Toto téma obsahuje informace o tom, jak konfigurovat cíl archivu pro každou komponentu SLOŽKA nebo SOUBOR formátu elektronického výkaznictví, který je nakonfigurován pro generování odchozích dokumentů.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 15611a4f0000ca5ccb0ac3f4012251d5bf5689ec
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019668"
---
# <span data-ttu-id="41017-103"><a name="ArchiveDestinationType">Cíl archivace</a></span><span class="sxs-lookup"><span data-stu-id="41017-103"><a name="ArchiveDestinationType">Archive destination</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41017-104">Můžete konfigurovat cíl archivu pro každou komponentu SLOŽKA nebo SOUBOR formátu elektronického výkaznictví, který je nakonfigurován pro generování odchozích dokumentů.</span><span class="sxs-lookup"><span data-stu-id="41017-104">You can configure an archive destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="41017-105">Vygenerovaný dokument je na základě nastavení cíle uložen jako příloha záznamu seznamu úloh elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="41017-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span>

<span data-ttu-id="41017-106">Tuto možnost můžete použít k odeslání vygenerovaného dokumentu do složky Microsoft SharePoint nebo úložiště Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="41017-106">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="41017-107">Nastavením **Povoleno** na **Ano** dojde k odeslání výstupu do cíle, který je definován pro vybraný typ dokumentu.</span><span class="sxs-lookup"><span data-stu-id="41017-107">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="41017-108">K dispozici pro výběr jsou pouze typy dokumentu, kde je skupina nastavena na **Soubor**.</span><span class="sxs-lookup"><span data-stu-id="41017-108">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="41017-109">[Typy](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) dokumentů definujete pomocí **Správa organizace** \> **Správa dokumentů** \> **Typy dokumentů**.</span><span class="sxs-lookup"><span data-stu-id="41017-109">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="41017-110">Konfigurace pro cíle EV je stejná, jako nastavení pro systém správy dokumentů.</span><span class="sxs-lookup"><span data-stu-id="41017-110">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="41017-111">[![Stránka typu dokumentu](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="41017-111">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="41017-112">Umístění určuje, kde bude soubor uložen.</span><span class="sxs-lookup"><span data-stu-id="41017-112">The location determines where the file is saved.</span></span> <span data-ttu-id="41017-113">Po povolení cíle **Archiv** lze výsledky uložit do archivu úloh.</span><span class="sxs-lookup"><span data-stu-id="41017-113">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="41017-114">Výsledky můžete zobrazit pod **Správa organizace** \> **Elektronické výkaznictví** \> **Archivované úlohy elektronického výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="41017-114">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="41017-115">Vyberte typ dokumentu pro archiv úloh přechodem na **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví** \> **Parametry elektronického výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="41017-115">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="41017-116">Další informace získáte v tématu [Konfigurace rámce elektronického výkaznictví](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span><span class="sxs-lookup"><span data-stu-id="41017-116">For more information, [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="41017-117">SharePoint</span><span class="sxs-lookup"><span data-stu-id="41017-117">SharePoint</span></span>

<span data-ttu-id="41017-118">Soubor můžete uložit do určené složky SharePoint.</span><span class="sxs-lookup"><span data-stu-id="41017-118">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="41017-119">Výchozí server SharePoint definujete v nabídce **Správa organizace** \> **Správa dokumentu** \> **Parametry správy dokumentů**.</span><span class="sxs-lookup"><span data-stu-id="41017-119">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="41017-120">Na kartě **SharePoint** nakonfigurujte složku SharePoint.</span><span class="sxs-lookup"><span data-stu-id="41017-120">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="41017-121">Poté ji můžete vybrat jako složku, do které bude uložen výstup elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="41017-121">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="41017-122">V tomto typu dokumentu musí být vybráno místo **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="41017-122">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="41017-123">[![Výběr složky služby SharePoint](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="41017-123">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="41017-124">Úložiště Azure</span><span class="sxs-lookup"><span data-stu-id="41017-124">Azure Storage</span></span>

<span data-ttu-id="41017-125">Pokud je umístění typu dokumentu nastaveno na **Azure storage**, můžete soubor uložit do úložiště Azure.</span><span class="sxs-lookup"><span data-stu-id="41017-125">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="41017-126">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="41017-126">Additional resources</span></span>

- [<span data-ttu-id="41017-127">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="41017-127">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="41017-128">Místa určení elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="41017-128">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="41017-129">Konfigurace správy dokumentů</span><span class="sxs-lookup"><span data-stu-id="41017-129">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
