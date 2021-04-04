---
title: Typ cílového místa elektronického výkaznictví tiskárny
description: Toto téma vysvětluje, jak nakonfigurovat cíl tiskárny pro každou SLOŽKU nebo SOUBOR ve formátu elektronického výkaznictví (ER).
author: NickSelin
manager: AnnBe
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 19613d9dfba21d591d96a2df45bedb80c043b3a7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561943"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a><span data-ttu-id="68709-103">Cílové místo tiskárny</span><span class="sxs-lookup"><span data-stu-id="68709-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68709-104">Vygenerovaný dokument můžete odeslat přímo do síťové tiskárny pro přímý tisk.</span><span class="sxs-lookup"><span data-stu-id="68709-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="68709-105">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="68709-105">Prerequisites</span></span>

<span data-ttu-id="68709-106">Dříve než začnete, je nutné nainstalovat a nakonfigurovat směrovacího agenta dokumentů a poté zaregistrovat síťové tiskárny.</span><span class="sxs-lookup"><span data-stu-id="68709-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="68709-107">Více informací naleznete v části [Instalace agenta směrování dokumentu pro aktivaci síťového tisku](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span><span class="sxs-lookup"><span data-stu-id="68709-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="68709-108">Zpřístupnění cíle tiskárny</span><span class="sxs-lookup"><span data-stu-id="68709-108">Make the Printer destination available</span></span>

<span data-ttu-id="68709-109">Chcete-li zpřístupnit cíl **tiskárny** v aktuální instanci Microsoft Dynamics 365 Finance, přejděte do do pracovního prostoru **Správa funkcí** a zapněte následující funkce v tomto pořadí:</span><span class="sxs-lookup"><span data-stu-id="68709-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="68709-110">Převod odchozích dokumentů elektronického výkaznictví z formátů Microsoft Office do formátu PDF</span><span class="sxs-lookup"><span data-stu-id="68709-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="68709-111">Agent pro směrování dokumentů jako cílové umístění elektronického výkaznictví pro odchozí dokumenty</span><span class="sxs-lookup"><span data-stu-id="68709-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="68709-112">[![Zapnutí cíle tiskárny elektronického výkaznictví ve správě funkcí](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="68709-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="68709-113">Použitelnost</span><span class="sxs-lookup"><span data-stu-id="68709-113">Applicability</span></span>

<span data-ttu-id="68709-114">Cíl **tiskárny** lze konfigurovat pouze pro součásti souboru, které jsou použity ke generování výstupu ve formátu tisknutelného PDF (PDF Merger nebo prvky formátu souboru PDF) nebo formátu Microsoft Office Excel/Word.</span><span class="sxs-lookup"><span data-stu-id="68709-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="68709-115">Když je výstup generován ve formátu PDF, je odeslán do tiskárny.</span><span class="sxs-lookup"><span data-stu-id="68709-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="68709-116">Když je výstup generován ve formátu Microsoft Office, je automaticky převeden do formátu PDF a poté odeslán do tiskárny.</span><span class="sxs-lookup"><span data-stu-id="68709-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="68709-117">Omezení</span><span class="sxs-lookup"><span data-stu-id="68709-117">Limitations</span></span>

<span data-ttu-id="68709-118">Cíl **tiskárny** je implementován pouze pro nasazení v cloudu.</span><span class="sxs-lookup"><span data-stu-id="68709-118">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="68709-119">Použití cíle tiskárny</span><span class="sxs-lookup"><span data-stu-id="68709-119">Use the Printer destination</span></span>

1. <span data-ttu-id="68709-120">Chcete-li odeslat vygenerovaný dokument do tiskárny, nastavte možnost **povoleno** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="68709-120">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="68709-121">V poli **Název tiskárny** vyberte požadovanou síťovou tiskárnu.</span><span class="sxs-lookup"><span data-stu-id="68709-121">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="68709-122">Chcete nastavit ukládání v tiskovém archivu, nastavte možnost **Uložit do tiskového archivu?** na **Ano**, aby byl k dispozici pro další tisk.</span><span class="sxs-lookup"><span data-stu-id="68709-122">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="68709-123">Chcete-li získat přístup k archivovanému výstupu později, přejděte na **Správa organizace** \> **Dotazy a sestavy** \> **Archive sestav**.</span><span class="sxs-lookup"><span data-stu-id="68709-123">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="68709-124">[![Použití cíle tiskárny](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="68709-124">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="68709-125">Pokud konfigurujete cíl **tiskárny**, možnost **převést do PDF** není nutné mít zapnutou.</span><span class="sxs-lookup"><span data-stu-id="68709-125">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="68709-126">Převod souboru PDF pro účely tisku bude proveden i v případě, že je tato možnost vypnuta.</span><span class="sxs-lookup"><span data-stu-id="68709-126">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

<span data-ttu-id="68709-127">Chcete-li při tisku odchozího dokumentu ve formátu aplikace Excel použít určitou [orientaci stránky](electronic-reporting-destinations.md#SelectPdfPageOrientation), je nutné zapnout možnost **převést na PDF**.</span><span class="sxs-lookup"><span data-stu-id="68709-127">To use a specific [page orientation](electronic-reporting-destinations.md#SelectPdfPageOrientation) when you print an outbound document in Excel format, you must turn on the **Convert to PDF** option.</span></span> <span data-ttu-id="68709-128">Nastavíte-li volbu **převést na PDF** na hodnotu **Ano**, zpřístupní se pole **Orientace stránky**.</span><span class="sxs-lookup"><span data-stu-id="68709-128">When you set the **Convert to PDF** option to **Yes**, the **Page orientation** field becomes available.</span></span> <span data-ttu-id="68709-129">V poli **Orientace stránky** můžete vybrat orientaci stránky.</span><span class="sxs-lookup"><span data-stu-id="68709-129">In the **Page orientation** field, you can select a page orientation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68709-130">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="68709-130">Additional resources</span></span>

- [<span data-ttu-id="68709-131">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="68709-131">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="68709-132">Místa určení elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="68709-132">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
