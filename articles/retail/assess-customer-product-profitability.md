---
title: "Posouzení ziskovosti z hlediska odběratelů a produktů"
description: "Tento článek vysvětluje použití analýzy v paměti a v reálném čase pro přístup, prohlížení a získání přehledu o ziskovosti z hlediska odběratelů a produktů na základě vašich dat z aplikace Microsoft Dynamics 365 for Retail."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: SysOperationsTemplateForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: dd6fb75b4ea7a82e179c236ea4bb7f2fd2ce6cb8
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="de237-103">Vyhodnocení ziskovosti z hlediska odběratelů a produktů</span><span class="sxs-lookup"><span data-stu-id="de237-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="de237-104">Tento článek vysvětluje použití analýzy v paměti a v reálném čase pro přístup, prohlížení a získání přehledu o ziskovosti z hlediska odběratelů a produktů na základě vašich dat z aplikace Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="de237-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Microsoft Dynamics 365 for Retail data.</span></span> 

<span data-ttu-id="de237-105">V rámci aplikace Dynamics 365 for Retail mohou uživatelé studovat ziskovost nejlepších odběratelů (10-100) v rámci rozdílných úrovní organizační hierarchie na základě jednoho z následujících kritérií:</span><span class="sxs-lookup"><span data-stu-id="de237-105">As part of Dynamics 365 for Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

-   <span data-ttu-id="de237-106">Prodejní částka</span><span class="sxs-lookup"><span data-stu-id="de237-106">Sales amount</span></span>
-   <span data-ttu-id="de237-107">Množství</span><span class="sxs-lookup"><span data-stu-id="de237-107">Quantity</span></span>
-   <span data-ttu-id="de237-108">Marže hrubého zisku</span><span class="sxs-lookup"><span data-stu-id="de237-108">Gross profit margin</span></span>
-   <span data-ttu-id="de237-109">Procento marže</span><span class="sxs-lookup"><span data-stu-id="de237-109">Margin percentage</span></span>

<span data-ttu-id="de237-110">Pro toto hodnocení lze použít sestavu **Nejlepší odběratelé**, která je ihned k dispozici po otevření některého z následujících umístění:</span><span class="sxs-lookup"><span data-stu-id="de237-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

-   <span data-ttu-id="de237-111">Pracovní prostor **Řízení maloobchodu** &gt; **Maloobchod** &gt; **Kanály** &gt; **Řízení maloobchodu** &gt; **Sestavy** &gt; **Sestava nejlepších odběratelů**</span><span class="sxs-lookup"><span data-stu-id="de237-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
-   <span data-ttu-id="de237-112">Část **Dotazy a sestavy** &gt; **Maloobchod** &gt; **Dotazy a sestavy** &gt; **Prodejní sestavy** &gt; **Sestava nejlepších odběratelů**</span><span class="sxs-lookup"><span data-stu-id="de237-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="de237-113">Stejně tak mohou uživatelé studovat ziskovost nejlepších produktů (10-100) v rámci rozdílných úrovní organizační hierarchie na základě jednoho z následujících kritérií:</span><span class="sxs-lookup"><span data-stu-id="de237-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

-   <span data-ttu-id="de237-114">Prodejní částka</span><span class="sxs-lookup"><span data-stu-id="de237-114">Sales amount</span></span>
-   <span data-ttu-id="de237-115">Množství</span><span class="sxs-lookup"><span data-stu-id="de237-115">Quantity</span></span>
-   <span data-ttu-id="de237-116">Marže hrubého zisku</span><span class="sxs-lookup"><span data-stu-id="de237-116">Gross profit margin</span></span>
-   <span data-ttu-id="de237-117">Procento marže</span><span class="sxs-lookup"><span data-stu-id="de237-117">Margin percentage</span></span>

<span data-ttu-id="de237-118">Pro toto hodnocení lze použít sestavu **Nejlepší produkty**, která je ihned k dispozici po otevření některého z následujících umístění:</span><span class="sxs-lookup"><span data-stu-id="de237-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

-   <span data-ttu-id="de237-119">Pracovní prostor **Řízení maloobchodu** &gt; **Maloobchod** &gt; **Kanály** &gt; **Řízení maloobchodu** &gt; **Sestavy** &gt; **Sestava nejlepších produktů**</span><span class="sxs-lookup"><span data-stu-id="de237-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
-   <span data-ttu-id="de237-120">Pracovní prostor **Správa kategorií a produktů** &gt; **Maloobchod** &gt; **Produkty a kategorie** &gt; **Řízení maloobchodu** &gt; **Sestavy** &gt; **Sestava nejlepších produktů**</span><span class="sxs-lookup"><span data-stu-id="de237-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
-   <span data-ttu-id="de237-121">Část **Dotazy a sestavy** &gt; **Maloobchod** &gt; **Dotazy a sestavy** &gt; **Prodejní sestavy** &gt; **Sestava nejlepších produktů**</span><span class="sxs-lookup"><span data-stu-id="de237-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>




