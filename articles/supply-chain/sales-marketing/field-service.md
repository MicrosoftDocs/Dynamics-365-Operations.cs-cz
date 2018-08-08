---
title: "Integrace s aplikací Microsoft Dynamics 365 for Field Service"
description: "Toto téma obsahuje přehled integrace s aplikací Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 2ef7f71dc6d58108b498ed89e9175ff2ce900cda
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="18e72-103">Integrace s aplikací Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="18e72-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="18e72-104">Microsoft Dynamics 365 for Finance and Operations umožňuje synchronizaci obchodních procesů mezi aplikací Finance and Operations a Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="18e72-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="18e72-105">Scénáře integrace jsou konfigurovány s použitím rozsáhlých šablon integrátoru dat a Common Data Service (CDS) pro umožnění synchronizace obchodních procesů.</span><span class="sxs-lookup"><span data-stu-id="18e72-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="18e72-106">[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="18e72-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="18e72-107">První fáze integrace mezi  Field Service a Finance and Operations se zaměřuje na povolení pracovních příkazů a smluv ve Field Service pro fakturaci ve Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="18e72-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="18e72-108">Podporovaný tok začíná ve Field Service, kde jsou informace z pracovních příkazů synchronizovány s Finance and Operations jako prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="18e72-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="18e72-109">V modulu Finance and Operations jsou prodejní objednávky fakturovány ke generování faktur.</span><span class="sxs-lookup"><span data-stu-id="18e72-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="18e72-110">Kromě toho jsou informace z faktur smluv ve službě Field Service synchronizovány do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="18e72-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="18e72-111">Integrátor dat Microsoft Dynamics 365 synchronizuje data pomocí upravitelné projektů.</span><span class="sxs-lookup"><span data-stu-id="18e72-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="18e72-112">Standardní šablony lze používat k vytváření projektů vlastní integrace, kde další standardní a vlastní pole a také entity, mohou být mapovány pro účely úpravy integrace a plnění konkrétních požadavků.</span><span class="sxs-lookup"><span data-stu-id="18e72-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="18e72-113">První fáze integrace mezi Field Service a Finance and Operations umožňuje synchronizaci následujících položek:</span><span class="sxs-lookup"><span data-stu-id="18e72-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="18e72-114">Produkty v modulu Finance and Operations na produkty v modulu Field Service, které zahrnují informace o typu produktu</span><span class="sxs-lookup"><span data-stu-id="18e72-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="18e72-115">Pracovní příkazy ve službě Field Service do prodejních objednávek v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="18e72-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="18e72-116">Faktury v aplikaci Field Service na volné textové faktury ve Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="18e72-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

<span data-ttu-id="18e72-117">Příklad synchronizace výrobního příkazu mezi Field Service a Finance and Operations uvádí krátké video na YouTube [Synchronizace výrobního příkazu mezi Dynamics 365 for Field Service a Finance and Operations](https://www.youtube.com/watch?v=hAB4TDVMjxU).</span><span class="sxs-lookup"><span data-stu-id="18e72-117">To see an example of how you can synchronize a work order between Field Service and Finance and Operations, watch the short YouTube video [Synchronize a work order between Dynamics 365 for Field Service and Finance and Operations](https://www.youtube.com/watch?v=hAB4TDVMjxU).</span></span>

[![](https://img.youtube.com/vi/hAB4TDVMjxU/0.jpg)](https://www.youtube.com/watch?v=hAB4TDVMjxU)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="18e72-118">Systémové požadavky aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="18e72-118">System requirements for Finance and Operations</span></span>
<span data-ttu-id="18e72-119">Integrace Field Service podporuje následující verze:</span><span class="sxs-lookup"><span data-stu-id="18e72-119">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="18e72-120">Dynamics 365 for Finance and Operations, verze 8.0 (duben 2018) nebo pozdější</span><span class="sxs-lookup"><span data-stu-id="18e72-120">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="18e72-121">Aplikace Dynamics 365 for Finance and Operations verze 8.0 (duben 2018) byla vydána v dubnu 2018 a má číslo sestavení aplikace 8.0.30.8020 s aktualizací platformy 15 (7.0.4841.35234).</span><span class="sxs-lookup"><span data-stu-id="18e72-121">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="18e72-122">Požadavky na systém pro Field Service</span><span class="sxs-lookup"><span data-stu-id="18e72-122">System requirements for Field Service</span></span>
<span data-ttu-id="18e72-123">Chcete-li použít řešení integrace Field Service, je nutné nainstalovat následující komponenty:</span><span class="sxs-lookup"><span data-stu-id="18e72-123">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="18e72-124">Microsoft Dynamics 365 for Field Service 9.0 or later</span><span class="sxs-lookup"><span data-stu-id="18e72-124">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="18e72-125">Dynamics 365 for Field Service verze 1612 (9.0.1.733) (DB 9.0.1.733) online nebo vyšší verze.</span><span class="sxs-lookup"><span data-stu-id="18e72-125">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="18e72-126">Řešení Prospect to Cash (P2C) pro Dynamics 365, verze 1.15.0.1 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="18e72-126">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="18e72-127">Řešení je k dispozici ke stažení na webech [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="18e72-127">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="18e72-128">Řešení integrace Field Service pro Dynamics 365, verze 1.0.0.0 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="18e72-128">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="18e72-129">Řešení je k dispozici ke stažení na webech [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span><span class="sxs-lookup"><span data-stu-id="18e72-129">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span></span>

