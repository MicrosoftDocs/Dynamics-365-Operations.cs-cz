---
title: Možnosti vykazování
description: Tento článek vysvětluje postup řešení problému, kdy zákazník chce přizpůsobit sestavy aplikace Microsoft Dynamics 365 Human Resources nebo vytvořit nové sestavy.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 9ee6dba5e37877f1c0b3b9df8306b3194ea2f3e4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008427"
---
# <a name="reporting-options"></a><span data-ttu-id="46682-103">Možnosti vykazování</span><span class="sxs-lookup"><span data-stu-id="46682-103">Reporting options</span></span>

<span data-ttu-id="46682-104">**Podrobnosti o prostředí**</span><span class="sxs-lookup"><span data-stu-id="46682-104">**Environment details**</span></span>

<span data-ttu-id="46682-105">Tento problém se vztahuje na všechna prostředí.</span><span class="sxs-lookup"><span data-stu-id="46682-105">This issue applies to all environments.</span></span>

<span data-ttu-id="46682-106">**Příznak**</span><span class="sxs-lookup"><span data-stu-id="46682-106">**Symptom**</span></span>

<span data-ttu-id="46682-107">Zákazník chce přizpůsobit sestavy aplikace Dynamics 365 Human Resources nebo vytvořit nové sestavy.</span><span class="sxs-lookup"><span data-stu-id="46682-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="46682-108">**Výdej**</span><span class="sxs-lookup"><span data-stu-id="46682-108">**Issue**</span></span>

<span data-ttu-id="46682-109">Uživatel nemůže přizpůsobit integrované sestavy Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="46682-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="46682-110">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="46682-110">**Solution**</span></span>

- <span data-ttu-id="46682-111">Data aplikace Human Resources, která přecházejí do Common Data Service, lze vykazovat prostřednictvím konektoru Power Apps Common Data Service do Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="46682-111">The Human Resources data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="46682-112">Všimněte si, že Common Data Service obsahuje podmnožinu dat aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="46682-112">Note that Common Data Service contains a subset of Human Resources data.</span></span> <span data-ttu-id="46682-113">Další informace o Power BI a řídicích panelech uvádí téma [Vytváření sestav a řídicích panelů Power BI pomocí Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="46682-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="46682-114">Elektronické výkaznictví je k dispozici pro některé sestavy v aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="46682-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="46682-115">Přizpůsobení požadované zákazníky lze provádět pomocí možností konfigurace elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="46682-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="46682-116">Data lze exportovat do aplikace Microsoft Excel nebo Microsoft Word pomocí různých datových entit, které aplikace Human Resources nabízí prostřednictvím integrace s Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="46682-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="46682-117">**Dlouhodobé řešení**</span><span class="sxs-lookup"><span data-stu-id="46682-117">**Long-term solution**</span></span>

<span data-ttu-id="46682-118">Další možnosti Power BI budou k dispozici a více dat a entit se stane součástí Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="46682-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
