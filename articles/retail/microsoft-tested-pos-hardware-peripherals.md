---
title: "Hardwarová periferní zařízení POS"
description: "Maloobchodní moderní pokladní místo (POS) a cloud POS mohou využívat širokou škálu hardwarových periferních zařízení s více rozhraními a možnostmi nasazení pro dosažení různých obchodních scénářů prodejce."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 215234
ms.assetid: 1893d4b3-e1b7-4b66-be58-0102addd5b36
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4fbfb176f2504be8aaf67992d094da1daeefeb76
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="pos-hardware-peripherals"></a><span data-ttu-id="e9daa-103">Hardwarová periferní zařízení POS</span><span class="sxs-lookup"><span data-stu-id="e9daa-103">POS hardware peripherals</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="e9daa-104">Maloobchodní moderní pokladní místo (POS) a cloud POS mohou využívat širokou škálu hardwarových periferních zařízení s více rozhraními a možnostmi nasazení pro dosažení různých obchodních scénářů prodejce.</span><span class="sxs-lookup"><span data-stu-id="e9daa-104">Retail Modern point of sale (POS) and Cloud POS can utilize a wide range of POS hardware peripherals, with multiple interfaces and deployment options to achieve a retailer’s various business scenarios.</span></span> 

<span data-ttu-id="e9daa-105">Na podporu co největšího výběru zařízení různých výrobců a modelů využívá POS standardní rozhraní jako OLE pro maloobchodní POS (OPOS), ovladače zařízení Windows a programová rozhraní aplikací POS (API) ve Windows.</span><span class="sxs-lookup"><span data-stu-id="e9daa-105">To support the widest selection of devices across manufactures and models, POS utilizes standard interfaces such as OLE for Retail POS (OPOS), Windows device drivers, and Windows point of service application program interfaces (APIs).</span></span> <span data-ttu-id="e9daa-106">Obecně platí, že POS bude na těchto zařízeních fungovat, pokud bude k dispozici vhodný ovladač.</span><span class="sxs-lookup"><span data-stu-id="e9daa-106">Generally, POS will work on these devices provided that the appropriate driver is supplied.</span></span> <span data-ttu-id="e9daa-107">Nicméně vzhledem k tomu, že se může implementace těchto standardů u jednotlivých výrobců a vývojářů softwaru lišit, často existují rozdíly v podporovaných schopnostech nebo chování.</span><span class="sxs-lookup"><span data-stu-id="e9daa-107">However, because each manufacturer and software developer’s implementation of these standards can vary, there are often differences in supported capabilities or behaviors.</span></span>

<span data-ttu-id="e9daa-108">Následující seznam obsahuje modely zařízení v každé třídě, které byly testovány interně společností Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e9daa-108">The following list includes device models, in each class, that have been tested internally by Microsoft.</span></span>

<span data-ttu-id="e9daa-109">**Zařízení OPOS**</span><span class="sxs-lookup"><span data-stu-id="e9daa-109">**OPOS devices**</span></span>

-   <span data-ttu-id="e9daa-110">Čárový kód – Motorola DS9208</span><span class="sxs-lookup"><span data-stu-id="e9daa-110">Barcode – Motorola DS9208</span></span>
-   <span data-ttu-id="e9daa-111">MSR – HP IDRA-334133, Magtek PN - 21073062</span><span class="sxs-lookup"><span data-stu-id="e9daa-111">MSR – HP IDRA-334133, Magtek PN - 21073062</span></span>
-   <span data-ttu-id="e9daa-112">LineDisplay – Epson M58DC</span><span class="sxs-lookup"><span data-stu-id="e9daa-112">LineDisplay – Epson M58DC</span></span>
-   <span data-ttu-id="e9daa-113">Pinpad – Verifone 1000SE</span><span class="sxs-lookup"><span data-stu-id="e9daa-113">Pinpad – Verifone 1000SE</span></span>
-   <span data-ttu-id="e9daa-114">Podpis – Scriptel ST1550</span><span class="sxs-lookup"><span data-stu-id="e9daa-114">Signature pad – Scriptel ST1550</span></span>
-   <span data-ttu-id="e9daa-115">Tiskárna – EPSON TM-T88IV, TMT88V</span><span class="sxs-lookup"><span data-stu-id="e9daa-115">Printer – EPSON TM-T88IV, TMT88V</span></span>
-   <span data-ttu-id="e9daa-116">Fond zásuvky s hotovostí – Star SMD2-1317BK44</span><span class="sxs-lookup"><span data-stu-id="e9daa-116">Cash drawer – Star SMD2-1317BK44</span></span>
-   <span data-ttu-id="e9daa-117">Váha – Datalogic Magellan 8400</span><span class="sxs-lookup"><span data-stu-id="e9daa-117">Scale – Datalogic Magellan 8400</span></span>

<span data-ttu-id="e9daa-118">**Platební terminál klávesnice MSR**</span><span class="sxs-lookup"><span data-stu-id="e9daa-118">**Keyboard wedge MSR**</span></span>

-   <span data-ttu-id="e9daa-119">Magtek USB</span><span class="sxs-lookup"><span data-stu-id="e9daa-119">Magtek USB</span></span>

<span data-ttu-id="e9daa-120">**Patební terminál**</span><span class="sxs-lookup"><span data-stu-id="e9daa-120">**Payment terminal**</span></span>

-   <span data-ttu-id="e9daa-121">Equinox L3500</span><span class="sxs-lookup"><span data-stu-id="e9daa-121">Equinox L3500</span></span>
-   <span data-ttu-id="e9daa-122">Verifone MX925</span><span class="sxs-lookup"><span data-stu-id="e9daa-122">Verifone MX925</span></span>

<span data-ttu-id="e9daa-123">**Síťová zařízení**</span><span class="sxs-lookup"><span data-stu-id="e9daa-123">**Network devices**</span></span>

-   <span data-ttu-id="e9daa-124">Tiskárna – Star TSP650II</span><span class="sxs-lookup"><span data-stu-id="e9daa-124">Printer – Star TSP650II</span></span>
-   <span data-ttu-id="e9daa-125">Fond zásuvky s hotovostí – APG Atwood</span><span class="sxs-lookup"><span data-stu-id="e9daa-125">Cash drawer – APG Atwood</span></span>
-   <span data-ttu-id="e9daa-126">Platební terminál – MX915, MX925</span><span class="sxs-lookup"><span data-stu-id="e9daa-126">Payment terminal – MX915, MX925</span></span>

<span data-ttu-id="e9daa-127">**MPOS pouze přímé výrobní náklady**</span><span class="sxs-lookup"><span data-stu-id="e9daa-127">**MPOS direct IPC only**</span></span>

-   <span data-ttu-id="e9daa-128">Čárový kód – Honeywell 1900, HP LS2208</span><span class="sxs-lookup"><span data-stu-id="e9daa-128">Barcode – Honeywell 1900, HP LS2208</span></span>
-   <span data-ttu-id="e9daa-129">MSR – Magtek PN - 21073075</span><span class="sxs-lookup"><span data-stu-id="e9daa-129">MSR – Magtek PN - 21073075</span></span>





