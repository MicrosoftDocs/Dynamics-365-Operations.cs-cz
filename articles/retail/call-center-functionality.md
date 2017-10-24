---
title: "Funkce kontaktního střediska"
description: "Tento článek obsahuje přehled o prodejní funkci kontaktního střediska v aplikaci Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 00d24e9933d087f150ec5270da94ad911423824d
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="call-center-functionality"></a><span data-ttu-id="8a9d8-103">Funkce kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="8a9d8-103">Call center functionality</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="8a9d8-104">Tento článek obsahuje přehled o prodejní funkci kontaktního střediska v aplikaci Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="8a9d8-104">This article provides an overview of the call center sales functionality in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="8a9d8-105">Dynamics 365 for Retail podporuje také kontaktní střediska jako typ maloobchodní sítě.</span><span class="sxs-lookup"><span data-stu-id="8a9d8-105">Dynamics 365 for Retail supports call centers as a type of retail channel.</span></span> <span data-ttu-id="8a9d8-106">V kontaktním středisku pracovníci zpracovávají zakázky od odběratele telefonicky a vytvářejí prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="8a9d8-106">In a call center, workers take orders from customers over the phone and create sales orders.</span></span> <span data-ttu-id="8a9d8-107">Funkce kontaktního střediska obsahuje funkce, které slouží k usnadnění telefonních objednávek a odběratelského servisu během celého procesu splnění zakázek.</span><span class="sxs-lookup"><span data-stu-id="8a9d8-107">Call center functionality includes features that are designed to make it easier to take phone orders and handle customer service throughout the order fulfillment process.</span></span> <span data-ttu-id="8a9d8-108">Například mohou pracovníci kontaktního střediska přímo zadat informace o platbách do prodejní objednávky a před odesláním objednávky mohou zobrazit podrobný přehled nákladů a plateb.</span><span class="sxs-lookup"><span data-stu-id="8a9d8-108">For example, call center workers can enter payment information directly into the sales order, and can view a detailed summary of charges and payments before they submit the order.</span></span> <span data-ttu-id="8a9d8-109">Pracovníci mají také možnosti pro kontrolu cen a přístup k různým datům o odběratelích, produktech a cenách ze stránky **Prodejní objednávka**.</span><span class="sxs-lookup"><span data-stu-id="8a9d8-109">Workers also have options for controlling pricing, and can access various data about customers, products, and prices from the **Sales order** page.</span></span> <span data-ttu-id="8a9d8-110">Kontaktní střediska mají navíc také rozšířenou funkci ke sledování stavu historie a objednávek.</span><span class="sxs-lookup"><span data-stu-id="8a9d8-110">Additionally, call centers have enhanced functionality for tracking customer history and order status.</span></span> <span data-ttu-id="8a9d8-111">Každé kontaktní středisko může mít vlastní uživatele, platební metody, cenové skupiny, finanční dimenze a způsoby dodání.</span><span class="sxs-lookup"><span data-stu-id="8a9d8-111">Each call center can have its own users, payment methods, price groups, financial dimensions, and modes of delivery.</span></span> <span data-ttu-id="8a9d8-112">Tyto možnosti lze nakonfigurovat při vytváření kontaktního střediska.</span><span class="sxs-lookup"><span data-stu-id="8a9d8-112">You can configure these options when you create the call center.</span></span> <span data-ttu-id="8a9d8-113">Kromě toho můžete využít stránku **Kontaktní středisko** pro povolení nebo zakázání následujících skupin funkcí, které jsou jedinečné pro kontaktní střediska:</span><span class="sxs-lookup"><span data-stu-id="8a9d8-113">Additionally, you can use the **Call center** page to enable or disable the following groups of features that are unique to call centers:</span></span>

-   <span data-ttu-id="8a9d8-114">**Dokončení objednávky** – tato skupina obsahuje funkce, které se vztahují k platbám a dokončení objednávek na stránce **Prodejní objednávka**.</span><span class="sxs-lookup"><span data-stu-id="8a9d8-114">**Order completion** – This group includes features that are related to payments and order completion on the **Sales order** page.</span></span>
-   <span data-ttu-id="8a9d8-115">**Směrovaný prodej** – tato skupina obsahuje funkce, které souvisejí se zdrojovými kódy, skripty a požadavky na katalog.</span><span class="sxs-lookup"><span data-stu-id="8a9d8-115">**Directed selling** – This group includes features that are related to source codes, scripts, and catalog requests.</span></span>

<span data-ttu-id="8a9d8-116">Jakmile povolíte tyto funkce v nastavení kontaktního střediska, budou k dispozici na stránce **Prodejní objednávka** pro uživatele, kteří jsou přiřazeni ke kontaktnímu středisku.</span><span class="sxs-lookup"><span data-stu-id="8a9d8-116">After you enable these features in the call center settings, they are available on the **Sales order** page to users who are associated with the call center.</span></span> <span data-ttu-id="8a9d8-117">Většina těchto funkcí vyžaduje před použitím další konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="8a9d8-117">Most of these features require additional setup before they can be used.</span></span> <span data-ttu-id="8a9d8-118">Předtím, než mohou uživatelé vytvářet objednávky kontaktního střediska, je nutné přidat tyto uživatele do kontaktního střediska jako uživatele kontaktního střediska.</span><span class="sxs-lookup"><span data-stu-id="8a9d8-118">Before users can create call center orders, you must add those users to the call center as call center users.</span></span> <span data-ttu-id="8a9d8-119">Tento krok umožňuje konfiguraci a funkce kontaktního střediska pro konkrétní kanály.</span><span class="sxs-lookup"><span data-stu-id="8a9d8-119">This step enables the call center channel-specific configuration and functionality.</span></span> <span data-ttu-id="8a9d8-120">Zde je několik příkladů funkcí, které se zpřístupní:</span><span class="sxs-lookup"><span data-stu-id="8a9d8-120">Here are some examples of the functionality that becomes available:</span></span>

-   <span data-ttu-id="8a9d8-121">Řízený prodej nabízí možnosti konfigurace pro skripty prodeje po telefonu a obrázky produktů k nápovědě pro agenty při příjmu objednávek.</span><span class="sxs-lookup"><span data-stu-id="8a9d8-121">Guided selling provides configuration options for telesales scripts and product images to help and guide sales clerks while they take orders.</span></span>
-   <span data-ttu-id="8a9d8-122">Objednávky nelze dokončit, dokud agent nezaznamená alespoň jednu platební metodu.</span><span class="sxs-lookup"><span data-stu-id="8a9d8-122">Orders can't be completed until sales clerks have captured at least one payment method.</span></span>
-   <span data-ttu-id="8a9d8-123">Lze konfigurovat pravidla pro navyšovací a křížový prodej a vyzývat agenty k nabízení konkrétních produktů odběrateli.</span><span class="sxs-lookup"><span data-stu-id="8a9d8-123">Upsell and cross-sell rules can be configured to prompt sales clerks to promote specific products to the customer.</span></span>
-   <span data-ttu-id="8a9d8-124">Prodejní agenti mohou zaznamenat zdrojový kód katalogu, ze kterého zákazník objednává.</span><span class="sxs-lookup"><span data-stu-id="8a9d8-124">Sales clerks can capture the source code for the catalog that a customer is ordering from.</span></span>
-   <span data-ttu-id="8a9d8-125">Prodejní agenti mohou do objednávky přidat kupóny prodejce.</span><span class="sxs-lookup"><span data-stu-id="8a9d8-125">Sales clerks can add a retailer's coupons to the order.</span></span>
-   <span data-ttu-id="8a9d8-126">Prodejní agenti mohou prodávat dlouhodobé programy.</span><span class="sxs-lookup"><span data-stu-id="8a9d8-126">Sales clerks can sell continuity programs.</span></span>
-   <span data-ttu-id="8a9d8-127">Objednávka může být ručně nebo automaticky pozastavena, pokud je nutné zjišťování dalších informací předtím, než bude možné objednávku zpracovat.</span><span class="sxs-lookup"><span data-stu-id="8a9d8-127">Orders can be put on hold manually or automatically, to indicate that additional investigation is required before the order can be processed.</span></span>





