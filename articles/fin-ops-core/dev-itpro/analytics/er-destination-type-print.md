---
title: Typ cílového místa elektronického výkaznictví tiskárny
description: Toto téma vysvětluje, jak můžete konfigurovat cíl tiskárny pro každou komponentu SLOŽKA nebo SOUBOR formátu elektronického výkaznictví, který je nakonfigurován pro generování odchozích dokumentů buď v PDF nebo formátech Microsoft Office (Excel nebo Word).
author: NickSelin
manager: AnnBe
ms.date: 01/16/2020
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
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 58e067baa130458e3a8e788d978604f208140a03
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019667"
---
# <a name="PrinterDestinationType"></a><span data-ttu-id="ef342-103">Cílové místo tiskárny</span><span class="sxs-lookup"><span data-stu-id="ef342-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef342-104">Vygenerovaný dokument můžete odeslat přímo do síťové tiskárny pro přímý tisk.</span><span class="sxs-lookup"><span data-stu-id="ef342-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ef342-105">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="ef342-105">Prerequisites</span></span>

<span data-ttu-id="ef342-106">Dříve než začnete, je nutné nainstalovat a nakonfigurovat směrovacího agenta dokumentů a poté zaregistrovat síťové tiskárny.</span><span class="sxs-lookup"><span data-stu-id="ef342-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="ef342-107">Více informací naleznete v části [Instalace agenta směrování dokumentu pro aktivaci síťového tisku](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span><span class="sxs-lookup"><span data-stu-id="ef342-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="ef342-108">Zpřístupnění cíle tiskárny</span><span class="sxs-lookup"><span data-stu-id="ef342-108">Make the Printer destination available</span></span>

<span data-ttu-id="ef342-109">Chcete-li zpřístupnit cíl **tiskárny** v aktuální instanci Microsoft Dynamics 365 Finance, přejděte do do pracovního prostoru **Správa funkcí** a zapněte následující funkce v tomto pořadí:</span><span class="sxs-lookup"><span data-stu-id="ef342-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="ef342-110">Převod odchozích dokumentů elektronického výkaznictví z formátů Microsoft Office do formátu PDF</span><span class="sxs-lookup"><span data-stu-id="ef342-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="ef342-111">Agent pro směrování dokumentů jako cílové umístění elektronického výkaznictví pro odchozí dokumenty</span><span class="sxs-lookup"><span data-stu-id="ef342-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="ef342-112">[![Zapnutí cíle tiskárny elektronického výkaznictví ve správě funkcí](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="ef342-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="ef342-113">Použitelnost</span><span class="sxs-lookup"><span data-stu-id="ef342-113">Applicability</span></span>

<span data-ttu-id="ef342-114">Cíl **tiskárny** lze konfigurovat pouze pro součásti souboru, které jsou použity ke generování výstupu ve formátu tisknutelného PDF (PDF Merger nebo prvky formátu souboru PDF) nebo formátu Microsoft Office Excel/Word.</span><span class="sxs-lookup"><span data-stu-id="ef342-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="ef342-115">Když je výstup generován ve formátu PDF, je odeslán do tiskárny.</span><span class="sxs-lookup"><span data-stu-id="ef342-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="ef342-116">Když je výstup generován ve formátu Microsoft Office, je automaticky převeden do formátu PDF a poté odeslán do tiskárny.</span><span class="sxs-lookup"><span data-stu-id="ef342-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="ef342-117">Omezení</span><span class="sxs-lookup"><span data-stu-id="ef342-117">Limitations</span></span>

<span data-ttu-id="ef342-118">Tato funkce je funkcí Preview a podléhá podmínkám použití, které jsou popsány v [doplňujících podmínkách použití pro funkce Preview Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2105274).</span><span class="sxs-lookup"><span data-stu-id="ef342-118">This feature is a preview feature and is subject to the terms of use that are described in [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://go.microsoft.com/fwlink/?linkid=2105274).</span></span>

<span data-ttu-id="ef342-119">Cíl **tiskárny** je implementován pouze pro nasazení v cloudu.</span><span class="sxs-lookup"><span data-stu-id="ef342-119">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="ef342-120">Použití cíle tiskárny</span><span class="sxs-lookup"><span data-stu-id="ef342-120">Use the Printer destination</span></span>

1. <span data-ttu-id="ef342-121">Chcete-li odeslat vygenerovaný dokument do tiskárny, nastavte možnost **povoleno** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="ef342-121">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="ef342-122">V poli **Název tiskárny** vyberte požadovanou síťovou tiskárnu.</span><span class="sxs-lookup"><span data-stu-id="ef342-122">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="ef342-123">Chcete nastavit ukládání v tiskovém archivu, nastavte možnost **Uložit do tiskového archivu?** na **Ano**, aby byl k dispozici pro další tisk.</span><span class="sxs-lookup"><span data-stu-id="ef342-123">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="ef342-124">Chcete-li získat přístup k archivovanému výstupu později, přejděte na **Správa organizace** \> **Dotazy a sestavy** \> **Archive sestav**.</span><span class="sxs-lookup"><span data-stu-id="ef342-124">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="ef342-125">[![Použití cíle tiskárny](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="ef342-125">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="ef342-126">Pokud konfigurujete cíl **tiskárny**, možnost **převést do PDF** není nutné mít zapnutou.</span><span class="sxs-lookup"><span data-stu-id="ef342-126">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="ef342-127">Převod souboru PDF pro účely tisku bude proveden i v případě, že je tato možnost vypnuta.</span><span class="sxs-lookup"><span data-stu-id="ef342-127">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ef342-128">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="ef342-128">Additional resources</span></span>

- [<span data-ttu-id="ef342-129">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="ef342-129">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="ef342-130">Místa určení elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="ef342-130">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
