---
title: Globalizační služby Dynamics 365
description: Toto téma poskytuje přehled globalizačních služeb Microsoft Dynamics 365.
author: JaneA07
manager: AnnBe
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8c6f3b7fb4dec0dffe55014e9e2d60620dc3b193
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893041"
---
# <a name="dynamics-365-globalization-services"></a><span data-ttu-id="83524-103">Globalizační služby Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="83524-103">Dynamics 365 globalization services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83524-104">Následující globalizační služby lze nakonfigurovat tak, aby rozšířily možnosti, které existují v některých online službách Microsoft Dynamics 365:</span><span class="sxs-lookup"><span data-stu-id="83524-104">The following globalization services can be configured to extend the capabilities that exist in some Microsoft Dynamics 365 online services:</span></span>

- <span data-ttu-id="83524-105">**Regulatory Configuration Service (RCS)** podporuje konfiguraci různých typů elektronických dokumentů a zpráv.</span><span class="sxs-lookup"><span data-stu-id="83524-105">**Regulatory Configuration Service (RCS)** supports the configuration of different types of electronic documents and reports.</span></span> <span data-ttu-id="83524-106">RCS poskytuje vylepšenou verzi návrháře elektronického výkaznictví (ER), kde je úložiště konfigurace samostatnou službou.</span><span class="sxs-lookup"><span data-stu-id="83524-106">RCS provides an enhanced version of the Electronic reporting (ER) designer where the configuration repository is a standalone service.</span></span> <span data-ttu-id="83524-107">Další informace viz [Regulatory Configuration Service](rcs-overview.md).</span><span class="sxs-lookup"><span data-stu-id="83524-107">For more information, see [Regulatory Configuration Service](rcs-overview.md).</span></span>
- <span data-ttu-id="83524-108">**Elektronická fakturace** sdružuje konfigurovatelné formáty pro transformace, digitální podpisy a konfigurovatelné integrace pro připojení k externím webovým službám, včetně certifikace a zpracování odpovědí.</span><span class="sxs-lookup"><span data-stu-id="83524-108">**Electronic Invoicing** brings together configurable formats for transformations, digital signatures, and configurable integrations for connectivity with external web services, including certification and response handling.</span></span> <span data-ttu-id="83524-109">Další informace získáte v tématu [Elektronická fakturace](e-invoicing-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="83524-109">For more information, see [Electronic Invoicing](e-invoicing-service-overview.md).</span></span>
- <span data-ttu-id="83524-110">**Výpočet daně** poskytuje zvýšenou flexibilitu podporou více daňových identifikačních čísel, určování daňových zákonů, návrháře výpočtu daní a modulu runtime, který vyhovuje celosvětovým komplexním daňovým předpisům.</span><span class="sxs-lookup"><span data-stu-id="83524-110">**Tax Calculation** provides enhanced flexibility by supporting multiple tax IDs, tax code determination, the tax calculation designer, and a runtime engine to comply with complex tax regulations worldwide.</span></span> <span data-ttu-id="83524-111">Další informace naleznete v tématu [Výpočet daně](global-tax-calcuation-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="83524-111">For more information, see [Tax Calculation](global-tax-calcuation-service-overview.md).</span></span>

<span data-ttu-id="83524-112">Tyto globalizační služby poskytují okamžitou integraci s následujícími online službami Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="83524-112">These globalization services provide out-of-box integration with the following Dynamics 365 online services.</span></span>

| <span data-ttu-id="83524-113">Online služba</span><span class="sxs-lookup"><span data-stu-id="83524-113">Online service</span></span> | <span data-ttu-id="83524-114">RCS</span><span class="sxs-lookup"><span data-stu-id="83524-114">RCS</span></span> | <span data-ttu-id="83524-115">Elektronická fakturace</span><span class="sxs-lookup"><span data-stu-id="83524-115">Electronic Invoicing</span></span> | <span data-ttu-id="83524-116">Výpočet daně (Preview)</span><span class="sxs-lookup"><span data-stu-id="83524-116">Tax Calculation (Preview)</span></span> |
|----------------|-----|----------------------|---------------------------|
| <span data-ttu-id="83524-117">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="83524-117">Dynamics 365 Finance</span></span> | <span data-ttu-id="83524-118">Ano</span><span class="sxs-lookup"><span data-stu-id="83524-118">Yes</span></span> | <span data-ttu-id="83524-119">Ano</span><span class="sxs-lookup"><span data-stu-id="83524-119">Yes</span></span> | <span data-ttu-id="83524-120">Ano</span><span class="sxs-lookup"><span data-stu-id="83524-120">Yes</span></span> | 
| <span data-ttu-id="83524-121">Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="83524-121">Dynamics 365 Supply Chain Management</span></span> | <span data-ttu-id="83524-122">Ano</span><span class="sxs-lookup"><span data-stu-id="83524-122">Yes</span></span> | <span data-ttu-id="83524-123">Ano</span><span class="sxs-lookup"><span data-stu-id="83524-123">Yes</span></span> | <span data-ttu-id="83524-124">Ano</span><span class="sxs-lookup"><span data-stu-id="83524-124">Yes</span></span> | 
| <span data-ttu-id="83524-125">Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="83524-125">Dynamics 365 Project Operations</span></span> | <span data-ttu-id="83524-126">Ano</span><span class="sxs-lookup"><span data-stu-id="83524-126">Yes</span></span> | <span data-ttu-id="83524-127">Ano</span><span class="sxs-lookup"><span data-stu-id="83524-127">Yes</span></span> | <span data-ttu-id="83524-128">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="83524-128">Not applicable</span></span> | 
| <span data-ttu-id="83524-129">Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="83524-129">Dynamics 365 Commerce</span></span> | <span data-ttu-id="83524-130">Ano</span><span class="sxs-lookup"><span data-stu-id="83524-130">Yes</span></span> | <span data-ttu-id="83524-131">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="83524-131">Not applicable</span></span> | <span data-ttu-id="83524-132">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="83524-132">Not applicable</span></span> | 

> [!NOTE]
> <span data-ttu-id="83524-133">Z důvodu rozdílů v dostupnosti geografických lokalit Azure (geos) pro RCS může konfigurace této služby způsobit, že se údaje o zákaznících přenesou mimo geografickou oblast vybranou pro příslušnou online službu Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="83524-133">Because of differences in the availability of Azure geographic locations (geos) for RCS, configuration of this service might cause customer data to be transferred outside the geo that is selected for the applicable Dynamics 365 online service.</span></span> <span data-ttu-id="83524-134">Další informace najdete v části [Dynamics 365 a Power Platform: Dostupnost, umístění dat, jazyk a lokalizace](https://aka.ms/rcs/D365Productavailabilityguide).</span><span class="sxs-lookup"><span data-stu-id="83524-134">For more information, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/rcs/D365Productavailabilityguide).</span></span>