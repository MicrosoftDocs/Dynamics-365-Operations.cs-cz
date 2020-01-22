---
title: Možnosti vykazování v aplikaci Talent
description: Toto téma vysvětluje postup řešení problému, kdy zákazník chce přizpůsobit sestavy aplikace Dynamics 365 Talent nebo vytvořit nové sestavy.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 05d4a2c4314b40042ae45b4f653554bad09be4fa
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897941"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="95519-103">Možnosti vykazování v aplikaci Talent</span><span class="sxs-lookup"><span data-stu-id="95519-103">Reporting options in Talent</span></span>

<span data-ttu-id="95519-104">**Podrobnosti o prostředí**</span><span class="sxs-lookup"><span data-stu-id="95519-104">**Environment details**</span></span>

<span data-ttu-id="95519-105">Tento problém se vztahuje na všechna prostředí.</span><span class="sxs-lookup"><span data-stu-id="95519-105">This issue applies to all environments.</span></span>

<span data-ttu-id="95519-106">**Příznak**</span><span class="sxs-lookup"><span data-stu-id="95519-106">**Symptom**</span></span>

<span data-ttu-id="95519-107">Zákazník chce přizpůsobit sestavy aplikace Dynamics 365 Talent nebo vytvořit nové sestavy.</span><span class="sxs-lookup"><span data-stu-id="95519-107">The customer wants to customize Microsoft Dynamics 365 Talent reports or create new reports.</span></span>

<span data-ttu-id="95519-108">**Výdej**</span><span class="sxs-lookup"><span data-stu-id="95519-108">**Issue**</span></span>

<span data-ttu-id="95519-109">Uživatel nemůže přizpůsobit integrované sestavy Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="95519-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="95519-110">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="95519-110">**Solution**</span></span>

- <span data-ttu-id="95519-111">Data aplikace Core HR, která přecházejí do Common Data Service, lze vykazovat prostřednictvím konektoru Power Apps Common Data Service do Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="95519-111">The Core HR data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="95519-112">Všimněte si, že Common Data Service obsahuje podmnožinu dat aplikace Core HR.</span><span class="sxs-lookup"><span data-stu-id="95519-112">Note that Common Data Service contains a subset of Core HR data.</span></span> <span data-ttu-id="95519-113">Další informace o Power BI a řídicích panelech uvádí téma [Vytváření sestav a řídicích panelů Power BI pomocí Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="95519-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="95519-114">Elektronické výkaznictví je k dispozici pro některé sestavy v aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="95519-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="95519-115">Přizpůsobení požadované zákazníky lze provádět pomocí možností konfigurace elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="95519-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="95519-116">Data lze exportovat do aplikace Microsoft Excel nebo Microsoft Word pomocí různých datových entit, které aplikace Talent nabízí prostřednictvím integrace s Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="95519-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="95519-117">**Dlouhodobé řešení**</span><span class="sxs-lookup"><span data-stu-id="95519-117">**Long-term solution**</span></span>

<span data-ttu-id="95519-118">Další možnosti Power BI budou k dispozici a více dat a entit se stane součástí Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="95519-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
