---
title: Typ cílového místa elektronického výkaznictví archivu
description: Toto téma obsahuje informace o tom, jak konfigurovat cíl archivu pro každou komponentu SLOŽKA nebo SOUBOR formátu elektronického výkaznictví, který je nakonfigurován pro generování odchozích dokumentů.
author: NickSelin
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 3dee7ec614ec1372feaa1150f5e4ebb14c32f60e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679671"
---
# <a name="archive-er-destination-type"></a><span data-ttu-id="54150-103">Typ cílového místa elektronického výkaznictví archivu</span><span class="sxs-lookup"><span data-stu-id="54150-103">Archive ER destination type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54150-104">Můžete konfigurovat cíl archivu pro každou komponentu **Složka** nebo **Soubor** formátu elektronického výkaznictví, který je nakonfigurován pro generování odchozích dokumentů.</span><span class="sxs-lookup"><span data-stu-id="54150-104">You can configure an archive destination for each **Folder** or **File** component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="54150-105">Vygenerovaný dokument je na základě nastavení cíle uložen jako příloha záznamu seznamu úloh elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="54150-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span> <span data-ttu-id="54150-106">Výsledky můžete zobrazit přechodem do nabídky **Správa organizace** \> **Elektronické výkaznictví** \> **Úlohy elektronického výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="54150-106">To view the results, go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>

<span data-ttu-id="54150-107">Tuto možnost můžete použít k odeslání vygenerovaného dokumentu do složky Microsoft SharePoint nebo úložiště Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="54150-107">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="54150-108">Nastavením **Povoleno** na **Ano** dojde k odeslání výstupu do cíle, který je definován pro vybraný typ dokumentu.</span><span class="sxs-lookup"><span data-stu-id="54150-108">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="54150-109">K dispozici pro výběr jsou pouze typy dokumentu, kde je skupina nastavena na **Soubor**.</span><span class="sxs-lookup"><span data-stu-id="54150-109">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="54150-110">[Typy](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) dokumentů definujete pomocí **Správa organizace** \> **Správa dokumentů** \> **Typy dokumentů**.</span><span class="sxs-lookup"><span data-stu-id="54150-110">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="54150-111">Konfigurace pro cíle EV je stejná, jako nastavení pro systém správy dokumentů.</span><span class="sxs-lookup"><span data-stu-id="54150-111">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="54150-112">[![Stránka typu dokumentu](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="54150-112">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="54150-113">Umístění určuje, kde bude soubor uložen.</span><span class="sxs-lookup"><span data-stu-id="54150-113">The location determines where the file is saved.</span></span> <span data-ttu-id="54150-114">Po povolení cíle **Archiv** lze výsledky uložit do archivu úloh.</span><span class="sxs-lookup"><span data-stu-id="54150-114">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="54150-115">Výsledky můžete zobrazit pod **Správa organizace** \> **Elektronické výkaznictví** \> **Archivované úlohy elektronického výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="54150-115">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="54150-116">Vyberte typ dokumentu pro archiv úloh přechodem na **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví** \> **Parametry elektronického výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="54150-116">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="54150-117">Další informace získáte v tématu [Konfigurace rámce elektronického výkaznictví](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span><span class="sxs-lookup"><span data-stu-id="54150-117">For more information, see [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="54150-118">SharePoint</span><span class="sxs-lookup"><span data-stu-id="54150-118">SharePoint</span></span>

<span data-ttu-id="54150-119">Soubor můžete uložit do určené složky SharePoint.</span><span class="sxs-lookup"><span data-stu-id="54150-119">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="54150-120">Výchozí server SharePoint definujete v nabídce **Správa organizace** \> **Správa dokumentu** \> **Parametry správy dokumentů**.</span><span class="sxs-lookup"><span data-stu-id="54150-120">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="54150-121">Na kartě **SharePoint** nakonfigurujte složku SharePoint.</span><span class="sxs-lookup"><span data-stu-id="54150-121">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="54150-122">Poté ji můžete vybrat jako složku, do které bude uložen výstup elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="54150-122">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="54150-123">V tomto typu dokumentu musí být vybráno místo **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="54150-123">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="54150-124">[![Výběr složky služby SharePoint](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="54150-124">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="54150-125">Úložiště Azure</span><span class="sxs-lookup"><span data-stu-id="54150-125">Azure Storage</span></span>

<span data-ttu-id="54150-126">Pokud je umístění typu dokumentu nastaveno na **Azure storage**, můžete soubor uložit do úložiště Azure.</span><span class="sxs-lookup"><span data-stu-id="54150-126">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

> [!NOTE] 
> <span data-ttu-id="54150-127">Architektura ER trvale ukládá soubory v úložišti objektů Azure Blob na rozdíl od architektury správy dat, která aplikuje sedmidenní zásadu uchovávání dokumentů, které musí být zpracovány.</span><span class="sxs-lookup"><span data-stu-id="54150-127">The ER framework permanently stores files in Azure Blob storage unlike the Data management framework that applies the seven-day retention policy for documents that must be processed.</span></span> <span data-ttu-id="54150-128">Další informace najdete v tématech [Rozhraní API pro získání stavu zprávy](../data-entities/recurring-integrations.md#api-for-getting-message-status) a [Rozhraní API pro kontrolu stavu](../data-entities/data-management-api.md#status-check-api).</span><span class="sxs-lookup"><span data-stu-id="54150-128">For more information, see [API for getting message status](../data-entities/recurring-integrations.md#api-for-getting-message-status) and [Status check API](../data-entities/data-management-api.md#status-check-api).</span></span> <span data-ttu-id="54150-129">Soubory související s ER budou uloženy v úložišti Azure Blob jako přílohy záznamů tabulky aplikace, pokud to bude nutné.</span><span class="sxs-lookup"><span data-stu-id="54150-129">The ER-related files will be stored in Azure Blob storage as attachments of application table records as long as necessary.</span></span> <span data-ttu-id="54150-130">Jeden soubor bude odstraněn z úložiště Azure Blob spolu se záznamem tabulky aplikace, ke kterému byl tento soubor připojen.</span><span class="sxs-lookup"><span data-stu-id="54150-130">A single file will be deleted from Azure Blob storage along with the application table record that this file was attached to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="54150-131">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="54150-131">Additional resources</span></span>

- [<span data-ttu-id="54150-132">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="54150-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="54150-133">Místa určení elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="54150-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="54150-134">Konfigurace správy dokumentů</span><span class="sxs-lookup"><span data-stu-id="54150-134">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
