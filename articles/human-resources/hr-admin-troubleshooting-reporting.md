---
title: Možnosti vykazování
description: Tento článek vysvětluje postup řešení problému, kdy zákazník chce přizpůsobit sestavy aplikace Microsoft Dynamics 365 Human Resources nebo vytvořit nové sestavy.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
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
ms.openlocfilehash: 830c8c32128a8dfc1b009557afb272e48ae3a1ff
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111752"
---
# <a name="reporting-options"></a><span data-ttu-id="36f92-103">Možnosti vykazování</span><span class="sxs-lookup"><span data-stu-id="36f92-103">Reporting options</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="36f92-104">**Podrobnosti o prostředí**</span><span class="sxs-lookup"><span data-stu-id="36f92-104">**Environment details**</span></span>

<span data-ttu-id="36f92-105">Tento problém se vztahuje na všechna prostředí.</span><span class="sxs-lookup"><span data-stu-id="36f92-105">This issue applies to all environments.</span></span>

<span data-ttu-id="36f92-106">**Příznak**</span><span class="sxs-lookup"><span data-stu-id="36f92-106">**Symptom**</span></span>

<span data-ttu-id="36f92-107">Zákazník chce přizpůsobit sestavy aplikace Dynamics 365 Human Resources nebo vytvořit nové sestavy.</span><span class="sxs-lookup"><span data-stu-id="36f92-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="36f92-108">**Výdej**</span><span class="sxs-lookup"><span data-stu-id="36f92-108">**Issue**</span></span>

<span data-ttu-id="36f92-109">Uživatel nemůže přizpůsobit integrované sestavy Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="36f92-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="36f92-110">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="36f92-110">**Solution**</span></span>

- <span data-ttu-id="36f92-111">Data aplikace Human Resources, která přecházejí do Dataverse, lze vykazovat prostřednictvím konektoru Power Apps Dataverse do Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="36f92-111">The Human Resources data that flows to Dataverse can be reported on via the Power Apps Dataverse connector to Power BI Desktop.</span></span> <span data-ttu-id="36f92-112">Všimněte si, že Dataverse obsahuje podmnožinu dat aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="36f92-112">Note that Dataverse contains a subset of Human Resources data.</span></span> <span data-ttu-id="36f92-113">Další informace o Power BI a řídicích panelech uvádí téma [Vytváření sestav a řídicích panelů Power BI pomocí Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="36f92-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="36f92-114">Elektronické výkaznictví je k dispozici pro některé sestavy v aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="36f92-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="36f92-115">Přizpůsobení požadované zákazníky lze provádět pomocí možností konfigurace elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="36f92-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="36f92-116">Data lze exportovat do aplikace Microsoft Excel nebo Microsoft Word pomocí různých datových entit, které aplikace Human Resources nabízí prostřednictvím integrace s Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="36f92-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="36f92-117">**Dlouhodobé řešení**</span><span class="sxs-lookup"><span data-stu-id="36f92-117">**Long-term solution**</span></span>

<span data-ttu-id="36f92-118">Další možnosti Power BI budou k dispozici a více dat a entit se stane součástí Dataverse.</span><span class="sxs-lookup"><span data-stu-id="36f92-118">Additional Power BI options will be available, and more data and entities will be part of Dataverse.</span></span>
