---
title: Posouzení ziskovosti z hlediska odběratelů a produktů
description: Tento článek vysvětluje použití analýzy v paměti a v reálném čase pro přístup, prohlížení a získání přehledu o ziskovosti z hlediska odběratelů a produktů na základě vašich dat z aplikace Dynamics 365 Commerce.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: 3218a29995791ce0d9a42d5b6d898d6e548f0f1d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021822"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="ae663-103">Vyhodnocení ziskovosti odběratelů a produktů</span><span class="sxs-lookup"><span data-stu-id="ae663-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ae663-104">Tento článek vysvětluje použití analýzy v paměti a v reálném čase pro přístup, prohlížení a získání přehledu o ziskovosti z hlediska odběratelů a produktů na základě vašich dat z aplikace Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ae663-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="ae663-105">V rámci aplikace Commerce mohou uživatelé studovat ziskovost nejlepších odběratelů (10-100) v rámci rozdílných úrovní organizační hierarchie na základě jednoho z následujících kritérií:</span><span class="sxs-lookup"><span data-stu-id="ae663-105">As part of Commerce, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="ae663-106">Prodejní částka</span><span class="sxs-lookup"><span data-stu-id="ae663-106">Sales amount</span></span>
- <span data-ttu-id="ae663-107">Množství</span><span class="sxs-lookup"><span data-stu-id="ae663-107">Quantity</span></span>
- <span data-ttu-id="ae663-108">Marže hrubého zisku</span><span class="sxs-lookup"><span data-stu-id="ae663-108">Gross profit margin</span></span>
- <span data-ttu-id="ae663-109">Procento marže</span><span class="sxs-lookup"><span data-stu-id="ae663-109">Margin percentage</span></span>

<span data-ttu-id="ae663-110">Pro toto hodnocení lze použít sestavu **Nejlepší odběratelé**, která je ihned k dispozici po otevření některého z následujících umístění:</span><span class="sxs-lookup"><span data-stu-id="ae663-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="ae663-111">Pracovní prostor **Řízení obchodu** &gt; **Retail and Commerce** &gt; **Kanály** &gt; **Řízení obchodu** &gt; **Sestavy** &gt; **Sestava nejlepších odběratelů**</span><span class="sxs-lookup"><span data-stu-id="ae663-111">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="ae663-112">Sekce **Dotazy a sestavy** &gt; **Retail and Commerce** &gt; **Dotazy a sestavy** &gt; **Prodejní sestavy** &gt; **Sestava nejlepších odběratelů**</span><span class="sxs-lookup"><span data-stu-id="ae663-112">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="ae663-113">Stejně tak mohou uživatelé studovat ziskovost nejlepších produktů (10-100) v rámci rozdílných úrovní organizační hierarchie na základě jednoho z následujících kritérií:</span><span class="sxs-lookup"><span data-stu-id="ae663-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="ae663-114">Prodejní částka</span><span class="sxs-lookup"><span data-stu-id="ae663-114">Sales amount</span></span>
- <span data-ttu-id="ae663-115">Množství</span><span class="sxs-lookup"><span data-stu-id="ae663-115">Quantity</span></span>
- <span data-ttu-id="ae663-116">Marže hrubého zisku</span><span class="sxs-lookup"><span data-stu-id="ae663-116">Gross profit margin</span></span>
- <span data-ttu-id="ae663-117">Procento marže</span><span class="sxs-lookup"><span data-stu-id="ae663-117">Margin percentage</span></span>

<span data-ttu-id="ae663-118">Pro toto hodnocení lze použít sestavu **Nejlepší produkty**, která je ihned k dispozici po otevření některého z následujících umístění:</span><span class="sxs-lookup"><span data-stu-id="ae663-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="ae663-119">Pracovní prostor **Řízení obchodu** &gt; **Retail and Commerce** &gt; **Kanály** &gt; **Řízení obchodu** &gt; **Sestavy** &gt; **Sestava nejlepších produktů**</span><span class="sxs-lookup"><span data-stu-id="ae663-119">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="ae663-120">Pracovní prostor **Správa kategorií a produktů** &gt; **Retail and Commerce** &gt; **Produkty a kategorie** &gt; **Řízení obchodu** &gt; **Sestavy** &gt; **Sestava nejlepších produktů**</span><span class="sxs-lookup"><span data-stu-id="ae663-120">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Products and categories** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="ae663-121">Sekce **Dotazy a sestavy** &gt; **Retail and Commerce** &gt; **Dotazy a sestavy** &gt; **Prodejní sestavy** &gt; **Sestava nejlepších produktů**</span><span class="sxs-lookup"><span data-stu-id="ae663-121">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>
