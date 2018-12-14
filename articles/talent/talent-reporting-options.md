---
title: "Možnosti vykazování v aplikaci Talent"
description: "Toto téma vysvětluje postup řešení problému, kdy zákazník chce přizpůsobit sestavy aplikace Microsoft Dynamics 365 for Talent nebo vytvořit nové sestavy."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.contentlocale: cs-cz
ms.lasthandoff: 12/04/2018

---

# <a name="reporting-options-in-talent"></a><span data-ttu-id="8d5eb-103">Možnosti vykazování v aplikaci Talent</span><span class="sxs-lookup"><span data-stu-id="8d5eb-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8d5eb-104">**Podrobnosti o prostředí**</span><span class="sxs-lookup"><span data-stu-id="8d5eb-104">**Environment details**</span></span>

<span data-ttu-id="8d5eb-105">Tento problém se vztahuje na všechna prostředí.</span><span class="sxs-lookup"><span data-stu-id="8d5eb-105">This issue applies to all environments.</span></span>

<span data-ttu-id="8d5eb-106">**Příznak**</span><span class="sxs-lookup"><span data-stu-id="8d5eb-106">**Symptom**</span></span>

<span data-ttu-id="8d5eb-107">Zákazník chce přizpůsobit sestavy aplikace Microsoft Dynamics 365 Talent nebo vytvořit nové sestavy.</span><span class="sxs-lookup"><span data-stu-id="8d5eb-107">The customer wants to customize Microsoft Dynamics 365 for Talent reports or create new reports.</span></span>

<span data-ttu-id="8d5eb-108">**Problém**</span><span class="sxs-lookup"><span data-stu-id="8d5eb-108">**Issue**</span></span>

<span data-ttu-id="8d5eb-109">Uživatel nemůže přizpůsobit integrované sestavy Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="8d5eb-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="8d5eb-110">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="8d5eb-110">**Solution**</span></span>

- <span data-ttu-id="8d5eb-111">Data aplikace Core HR, která přechází do Common Data Service for Apps, lze dále vykazovat prostřednictvím konektoru PowerApps CDS do Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="8d5eb-111">The Core HR data that flows to Common Data Service for Apps can be reported on via the PowerApps CDS connector to Power BI Desktop.</span></span> <span data-ttu-id="8d5eb-112">Všimněte si, že Common Data Service for Apps obsahuje podmnožinu dat aplikace Core HR.</span><span class="sxs-lookup"><span data-stu-id="8d5eb-112">Note that Common Data Service for Apps contains a subset of Core HR data.</span></span> <span data-ttu-id="8d5eb-113">Další informace o Power BI a řídicích panelech naleznete v tématu [Vytvoření sestav a řídicích panelů Power BI pomocí PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="8d5eb-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="8d5eb-114">Elektronické výkaznictví je k dispozici pro některé sestavy v aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="8d5eb-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="8d5eb-115">Přizpůsobení požadované zákazníky lze provádět pomocí možností konfigurace elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="8d5eb-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="8d5eb-116">Data lze exportovat do aplikace Microsoft Excel nebo Microsoft Word pomocí různých datových entit, které aplikace Talent nabízí prostřednictvím integrace s Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="8d5eb-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="8d5eb-117">**Dlouhodobé řešení**</span><span class="sxs-lookup"><span data-stu-id="8d5eb-117">**Long-term solution**</span></span>

<span data-ttu-id="8d5eb-118">Další možnosti Power BI budou k dispozici a více dat a entit se stane součástí Common Data Service for Apps.</span><span class="sxs-lookup"><span data-stu-id="8d5eb-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service for Apps.</span></span>

