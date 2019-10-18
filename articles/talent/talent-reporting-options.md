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
ms.openlocfilehash: 50342c847200d015a66c6f22007070bb26c6caef
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009345"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="12276-103">Možnosti vykazování v aplikaci Talent</span><span class="sxs-lookup"><span data-stu-id="12276-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="12276-104">**Podrobnosti o prostředí**</span><span class="sxs-lookup"><span data-stu-id="12276-104">**Environment details**</span></span>

<span data-ttu-id="12276-105">Tento problém se vztahuje na všechna prostředí.</span><span class="sxs-lookup"><span data-stu-id="12276-105">This issue applies to all environments.</span></span>

<span data-ttu-id="12276-106">**Příznak**</span><span class="sxs-lookup"><span data-stu-id="12276-106">**Symptom**</span></span>

<span data-ttu-id="12276-107">Zákazník chce přizpůsobit sestavy aplikace Dynamics 365 Talent nebo vytvořit nové sestavy.</span><span class="sxs-lookup"><span data-stu-id="12276-107">The customer wants to customize Microsoft Dynamics 365 Talent reports or create new reports.</span></span>

<span data-ttu-id="12276-108">**Výdej**</span><span class="sxs-lookup"><span data-stu-id="12276-108">**Issue**</span></span>

<span data-ttu-id="12276-109">Uživatel nemůže přizpůsobit integrované sestavy Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="12276-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="12276-110">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="12276-110">**Solution**</span></span>

- <span data-ttu-id="12276-111">Data aplikace Core HR, která přecházejí do Common Data Service, lze vykazovat prostřednictvím konektoru PowerApps Common Data Service do Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="12276-111">The Core HR data that flows to Common Data Service can be reported on via the PowerApps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="12276-112">Všimněte si, že Common Data Service obsahuje podmnožinu dat aplikace Core HR.</span><span class="sxs-lookup"><span data-stu-id="12276-112">Note that Common Data Service contains a subset of Core HR data.</span></span> <span data-ttu-id="12276-113">Další informace o Power BI a řídicích panelech uvádí téma [Vytváření sestav a řídicích panelů Power BI pomocí PowerApps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="12276-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="12276-114">Elektronické výkaznictví je k dispozici pro některé sestavy v aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="12276-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="12276-115">Přizpůsobení požadované zákazníky lze provádět pomocí možností konfigurace elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="12276-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="12276-116">Data lze exportovat do aplikace Microsoft Excel nebo Microsoft Word pomocí různých datových entit, které aplikace Talent nabízí prostřednictvím integrace s Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="12276-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="12276-117">**Dlouhodobé řešení**</span><span class="sxs-lookup"><span data-stu-id="12276-117">**Long-term solution**</span></span>

<span data-ttu-id="12276-118">Další možnosti Power BI budou k dispozici a více dat a entit se stane součástí Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="12276-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
