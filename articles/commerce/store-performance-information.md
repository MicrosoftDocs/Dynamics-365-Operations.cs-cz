---
title: Analýza výkonnosti obchodu
description: Tento článek vysvětluje použití analýzy v paměti a v reálném čase pro přístup, prohlížení a získání přehledu o výkonu obchodu na základě vašich dat z aplikace Dynamics 365 Commerce.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelReport, RetailChannelManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 57811
ms.assetid: 495a66f0-491a-4688-842d-51c33c37676f
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8d95bb0927de5a1906efe180cb9e725c380a724f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021880"
---
# <a name="analyze-store-performance"></a><span data-ttu-id="f7200-103">Analýza výkonnosti obchodu</span><span class="sxs-lookup"><span data-stu-id="f7200-103">Analyze store performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f7200-104">Tento článek vysvětluje použití analýzy v paměti a v reálném čase pro přístup, prohlížení a získání přehledu o výkonu obchodu na základě vašich dat z aplikace Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f7200-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about store performance, based on your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="f7200-105">V rámci aplikace Retail mohou uživatelé studovat výkon v reálném čase v rámci rozdílných úrovní organizační hierarchie ve vybraném období otevřením sestavy **Souhrn kanálu** připravené okamžitě z některého z následujících umístění:</span><span class="sxs-lookup"><span data-stu-id="f7200-105">As part of Retail, users can study store performance in real time across different levels of the organization hierarchy over a selected period by opening the out-of-box **Channel summary** report from any of the following locations:</span></span>

- <span data-ttu-id="f7200-106">Pracovní prostor **Řízení maloobchodu** &gt; **Maloobchod** &gt; **Kanály** &gt; **Řízení maloobchodu** &gt; **Sestavy** &gt; **Sestava souhrnu kanálu**</span><span class="sxs-lookup"><span data-stu-id="f7200-106">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="f7200-107">Pracovní prostor **Finance maloobchodu** &gt; **Maloobchod** &gt; **Kanály** &gt; **Finance maloobchodu** &gt; **Sestavy** &gt; **Sestava souhrnu kanálu**</span><span class="sxs-lookup"><span data-stu-id="f7200-107">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="f7200-108">Část **Dotazy a sestavy** &gt; **Maloobchod** &gt; **Dotazy a sestavy** &gt; **Prodejní sestavy** &gt; **Sestava souhrnu kanálu**</span><span class="sxs-lookup"><span data-stu-id="f7200-108">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel summary report**</span></span>

<span data-ttu-id="f7200-109">Tato sestava poskytuje snímek následujícího souhrnu v rámci výkonnosti obchodu:</span><span class="sxs-lookup"><span data-stu-id="f7200-109">This report provides a snapshot of following summaries as part of store performance:</span></span>

- <span data-ttu-id="f7200-110">Souhrn hrubých prodejů</span><span class="sxs-lookup"><span data-stu-id="f7200-110">Gross sales summary</span></span>
- <span data-ttu-id="f7200-111">Souhrn typu úhrad</span><span class="sxs-lookup"><span data-stu-id="f7200-111">Tender type summary</span></span>
- <span data-ttu-id="f7200-112">Souhrn daně</span><span class="sxs-lookup"><span data-stu-id="f7200-112">Tax summary</span></span>
- <span data-ttu-id="f7200-113">Souhrn přepisů ceny</span><span class="sxs-lookup"><span data-stu-id="f7200-113">Price overrides summary</span></span>
- <span data-ttu-id="f7200-114">Souhrn slev</span><span class="sxs-lookup"><span data-stu-id="f7200-114">Discounts summary</span></span>
