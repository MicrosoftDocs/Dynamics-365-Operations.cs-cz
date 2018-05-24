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
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 03a932652cdd93b2a5917d0fca72809d1648b678
ms.openlocfilehash: b1acf0b64914a3199fcf44f8377e32b26f0af99e
ms.contentlocale: cs-cz
ms.lasthandoff: 04/25/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="10f44-103">Integrace s aplikací Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="10f44-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="10f44-104">Microsoft Dynamics 365 for Finance and Operations umožňuje synchronizaci obchodních procesů mezi aplikací Finance and Operations a Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="10f44-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="10f44-105">Scénáře integrace jsou konfigurovány s použitím rozsáhlých šablon integrátoru dat a Common Data Service (CDS) pro umožnění synchronizace obchodních procesů.</span><span class="sxs-lookup"><span data-stu-id="10f44-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="10f44-106">[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="10f44-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="10f44-107">První fáze integrace mezi  Field Service a Finance and Operations se zaměřuje na povolení pracovních příkazů a smluv ve Field Service pro fakturaci ve Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="10f44-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="10f44-108">Podporovaný tok začíná ve Field Service, kde jsou informace z pracovních příkazů synchronizovány s Finance and Operations jako prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="10f44-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="10f44-109">V modulu Finance and Operations jsou prodejní objednávky fakturovány ke generování faktur.</span><span class="sxs-lookup"><span data-stu-id="10f44-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="10f44-110">Kromě toho jsou informace z faktur smluv ve službě Field Service synchronizovány do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="10f44-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="10f44-111">Integrátor dat Microsoft Dynamics 365 synchronizuje data pomocí upravitelné projektů.</span><span class="sxs-lookup"><span data-stu-id="10f44-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="10f44-112">Standardní šablony lze používat k vytváření projektů vlastní integrace, kde další standardní a vlastní pole a také entity, mohou být mapovány pro účely úpravy integrace a plnění konkrétních požadavků.</span><span class="sxs-lookup"><span data-stu-id="10f44-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="10f44-113">První fáze integrace mezi Field Service a Finance and Operations umožňuje synchronizaci následujících položek:</span><span class="sxs-lookup"><span data-stu-id="10f44-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="10f44-114">Produkty v modulu Finance and Operations na produkty v modulu Field Service, které zahrnují informace o typu produktu</span><span class="sxs-lookup"><span data-stu-id="10f44-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="10f44-115">Pracovní příkazy ve službě Field Service do prodejních objednávek v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="10f44-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="10f44-116">Faktury v aplikaci Field Service na volné textové faktury ve Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="10f44-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

<span data-ttu-id="10f44-117">Pokud se chcete podívat na příklad, jak můžete synchronizovat pracovní objednávku mezi aplikací Field Service a Finance and Operations, podívejte se na krátké video na YouTube:</span><span class="sxs-lookup"><span data-stu-id="10f44-117">To see an example of how you can synchronize a work order between Field Service and Finance and Operations, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/hAB4TDVMjxU]

[<span data-ttu-id="10f44-118">Synchronizace pracovního příkazu mezi službou Field Service a aplikací Finance and Operations (video na YouTube)</span><span class="sxs-lookup"><span data-stu-id="10f44-118">Synchronize a work order between Field Service and Finance and Operations (YouTube video)</span></span>](https://youtu.be/hAB4TDVMjxU)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="10f44-119">Systémové požadavky aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="10f44-119">System requirements for Finance and Operations</span></span>
<span data-ttu-id="10f44-120">Integrace Field Service podporuje následující verze:</span><span class="sxs-lookup"><span data-stu-id="10f44-120">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="10f44-121">Dynamics 365 for Finance and Operations, verze 8.0 (duben 2018) nebo pozdější</span><span class="sxs-lookup"><span data-stu-id="10f44-121">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="10f44-122">Aplikace Dynamics 365 for Finance and Operations verze 8.0 (duben 2018) byla vydána v dubnu 2018 a má číslo sestavení aplikace 8.0.30.8020 s aktualizací platformy 15 (7.0.4841.35234).</span><span class="sxs-lookup"><span data-stu-id="10f44-122">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="10f44-123">Požadavky na systém pro Field Service</span><span class="sxs-lookup"><span data-stu-id="10f44-123">System requirements for Field Service</span></span>
<span data-ttu-id="10f44-124">Chcete-li použít řešení integrace Field Service, je nutné nainstalovat následující komponenty:</span><span class="sxs-lookup"><span data-stu-id="10f44-124">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="10f44-125">Microsoft Dynamics 365 for Field Service 9.0 or later</span><span class="sxs-lookup"><span data-stu-id="10f44-125">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="10f44-126">Dynamics 365 for Field Service verze 1612 (9.0.1.733) (DB 9.0.1.733) online nebo vyšší verze.</span><span class="sxs-lookup"><span data-stu-id="10f44-126">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="10f44-127">Řešení Prospect to Cash (P2C) pro Dynamics 365, verze 1.15.0.1 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="10f44-127">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="10f44-128">Řešení je k dispozici ke stažení na webech [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="10f44-128">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="10f44-129">Řešení integrace Field Service pro Dynamics 365, verze 1.0.0.0 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="10f44-129">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="10f44-130">Řešení je k dispozici ke stažení na webech [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span><span class="sxs-lookup"><span data-stu-id="10f44-130">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span></span>

