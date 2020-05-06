---
title: Rozšířené filtrování RCS v RCS/globálním úložišti
description: V tomto tématu jsou popsány rozšířené možnosti filtrování pro globální úložiště RCS, které bylo vylepšeno za účelem zahrnutí dalších filtrů.
author: JaneA07
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 1913b661c46af5e34da1a2939cb2a5d5b4e46411
ms.sourcegitcommit: 7df49a85de484d013518217ba8ada6c61da4b6e4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/24/2020
ms.locfileid: "3287932"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a><span data-ttu-id="92dc4-103">Rozšířené možnosti filtrování RCS pro vyhledání konfigurací v RCSD/globálním úložišti</span><span class="sxs-lookup"><span data-stu-id="92dc4-103">RCS enhanced filtering options for finding configurations in the RCS/Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92dc4-104">V tomto tématu jsou popsány rozšířené možnosti filtrování pro globální úložiště Regulatory Configuration Services (RCS), které bylo vylepšeno za účelem zahrnutí možnosti filtrování s následujícími kritérii:</span><span class="sxs-lookup"><span data-stu-id="92dc4-104">This topic describes enhanced filtering capabilities for Regulatory Configuration Services (RCS) Global repository, which have been improved to include the ability to filter with the following criteria:</span></span> 
- <span data-ttu-id="92dc4-105">**Země/oblast** - založená na kódech ISO zemí</span><span class="sxs-lookup"><span data-stu-id="92dc4-105">**Country/region** - Based on ISO country codes</span></span>  
- <span data-ttu-id="92dc4-106">Typy **značek** pro:</span><span class="sxs-lookup"><span data-stu-id="92dc4-106">**Tags** types for:</span></span>
  - <span data-ttu-id="92dc4-107">Funkční oblast</span><span class="sxs-lookup"><span data-stu-id="92dc4-107">Functional area</span></span>
  - <span data-ttu-id="92dc4-108">Oblast funkce</span><span class="sxs-lookup"><span data-stu-id="92dc4-108">Feature area</span></span>
  - <span data-ttu-id="92dc4-109">Obor</span><span class="sxs-lookup"><span data-stu-id="92dc4-109">Industry</span></span> 
  - <span data-ttu-id="92dc4-110">Obchodní dokument</span><span class="sxs-lookup"><span data-stu-id="92dc4-110">Business document</span></span> 

<span data-ttu-id="92dc4-111">Chcete-li snadněji vyhledat konkrétní nebo související konfigurace, můžete použít filtry, a to buď jednotlivě, nebo jako skupinu.</span><span class="sxs-lookup"><span data-stu-id="92dc4-111">To make it easier to discover specific or related configurations you can apply filters, either individually or as a group.</span></span> <span data-ttu-id="92dc4-112">Chcete-li například vyhledat jediný typ nastavitelného obchodního dokumentu, který souvisí s fakturami dodavatele, můžete použít filtr **Typ obchodního dokumentu** a vyhledat tento typ dokumentu.</span><span class="sxs-lookup"><span data-stu-id="92dc4-112">For example, to find a single type of 'configurable business documents that are related to vendor invoices, you could apply a **Business document type** filter to search for that type of document.</span></span> 

<span data-ttu-id="92dc4-113">[![Oddíl filtru pro globální úložiště](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span><span class="sxs-lookup"><span data-stu-id="92dc4-113">[![Filter section for Global repository](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span></span> 

<span data-ttu-id="92dc4-114">Hledání lze dále upřesnit výběrem typu dokumentu, například faktury dodavatele a kliknutím na volbu **Použít filtr**.</span><span class="sxs-lookup"><span data-stu-id="92dc4-114">You can further refine the search by selecting document type, for example 'vendor invoice' and clicking **Apply filter**.</span></span> <span data-ttu-id="92dc4-115">V následujícím příkladu je zobrazen výsledek při filtrování dle **Typu obchodního dokumentu** s přidaným typem dokumentu.</span><span class="sxs-lookup"><span data-stu-id="92dc4-115">The following example shows the results when filtering on **Business document type** with the document type added.</span></span> 

<span data-ttu-id="92dc4-116">[![Použitý filtr a import pro typ obchodního dokumentu](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span><span class="sxs-lookup"><span data-stu-id="92dc4-116">[![Applied filter and Import for business document type](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span></span> 

<span data-ttu-id="92dc4-117">Filtrované výsledky mohou být importovány do úložiště RCS uživatelů nebo prostředí Dynamics 365 Finance, a to buď jednotlivě, nebo jako sadu.</span><span class="sxs-lookup"><span data-stu-id="92dc4-117">Filtered results can be imported into a users RCS repository or a Dynamics 365 Finance environment, either individually or as a set.</span></span> <span data-ttu-id="92dc4-118">Chcete-li to provést, vyberte skupinu konfigurací a klikněte na možnost **Importovat**.</span><span class="sxs-lookup"><span data-stu-id="92dc4-118">To do this, select the group of configurations, and click **Import**.</span></span>
