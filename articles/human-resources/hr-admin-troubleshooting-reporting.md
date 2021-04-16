---
title: Možnosti vykazování
description: Tento článek vysvětluje postup řešení problému, kdy zákazník chce přizpůsobit sestavy aplikace Microsoft Dynamics 365 Human Resources nebo vytvořit nové sestavy.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2d0fc6b2d4af6ad021943717645bfff7a27797a8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803889"
---
# <a name="reporting-options"></a><span data-ttu-id="67973-103">Možnosti vykazování</span><span class="sxs-lookup"><span data-stu-id="67973-103">Reporting options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="67973-104">**Podrobnosti o prostředí**</span><span class="sxs-lookup"><span data-stu-id="67973-104">**Environment details**</span></span>

<span data-ttu-id="67973-105">Tento problém se vztahuje na všechna prostředí.</span><span class="sxs-lookup"><span data-stu-id="67973-105">This issue applies to all environments.</span></span>

<span data-ttu-id="67973-106">**Příznak**</span><span class="sxs-lookup"><span data-stu-id="67973-106">**Symptom**</span></span>

<span data-ttu-id="67973-107">Zákazník chce přizpůsobit sestavy aplikace Dynamics 365 Human Resources nebo vytvořit nové sestavy.</span><span class="sxs-lookup"><span data-stu-id="67973-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="67973-108">**Výdej**</span><span class="sxs-lookup"><span data-stu-id="67973-108">**Issue**</span></span>

<span data-ttu-id="67973-109">Uživatel nemůže přizpůsobit integrované sestavy Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="67973-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="67973-110">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="67973-110">**Solution**</span></span>

- <span data-ttu-id="67973-111">Data aplikace Human Resources, která přecházejí do Dataverse, lze vykazovat prostřednictvím konektoru Power Apps Dataverse do Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="67973-111">The Human Resources data that flows to Dataverse can be reported on via the Power Apps Dataverse connector to Power BI Desktop.</span></span> <span data-ttu-id="67973-112">Všimněte si, že Dataverse obsahuje podmnožinu dat aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="67973-112">Note that Dataverse contains a subset of Human Resources data.</span></span> <span data-ttu-id="67973-113">Další informace o Power BI a řídicích panelech uvádí téma [Vytváření sestav a řídicích panelů Power BI pomocí Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="67973-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="67973-114">Elektronické výkaznictví je k dispozici pro některé sestavy v aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="67973-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="67973-115">Přizpůsobení požadované zákazníky lze provádět pomocí možností konfigurace elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="67973-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="67973-116">Data lze exportovat do aplikace Microsoft Excel nebo Microsoft Word pomocí různých datových entit, které aplikace Human Resources nabízí prostřednictvím integrace s Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="67973-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="67973-117">**Dlouhodobé řešení**</span><span class="sxs-lookup"><span data-stu-id="67973-117">**Long-term solution**</span></span>

<span data-ttu-id="67973-118">Další možnosti Power BI budou k dispozici a více dat a entit se stane součástí Dataverse.</span><span class="sxs-lookup"><span data-stu-id="67973-118">Additional Power BI options will be available, and more data and entities will be part of Dataverse.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]