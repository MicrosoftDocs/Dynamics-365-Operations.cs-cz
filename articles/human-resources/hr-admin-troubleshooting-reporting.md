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
ms.openlocfilehash: 5d47524033bf39a1db6b22b28ee3fcc65348829c
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431008"
---
# <a name="reporting-options"></a><span data-ttu-id="4da03-103">Možnosti vykazování</span><span class="sxs-lookup"><span data-stu-id="4da03-103">Reporting options</span></span>

<span data-ttu-id="4da03-104">**Podrobnosti o prostředí**</span><span class="sxs-lookup"><span data-stu-id="4da03-104">**Environment details**</span></span>

<span data-ttu-id="4da03-105">Tento problém se vztahuje na všechna prostředí.</span><span class="sxs-lookup"><span data-stu-id="4da03-105">This issue applies to all environments.</span></span>

<span data-ttu-id="4da03-106">**Příznak**</span><span class="sxs-lookup"><span data-stu-id="4da03-106">**Symptom**</span></span>

<span data-ttu-id="4da03-107">Zákazník chce přizpůsobit sestavy aplikace Dynamics 365 Human Resources nebo vytvořit nové sestavy.</span><span class="sxs-lookup"><span data-stu-id="4da03-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="4da03-108">**Výdej**</span><span class="sxs-lookup"><span data-stu-id="4da03-108">**Issue**</span></span>

<span data-ttu-id="4da03-109">Uživatel nemůže přizpůsobit integrované sestavy Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="4da03-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="4da03-110">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="4da03-110">**Solution**</span></span>

- <span data-ttu-id="4da03-111">Data aplikace Human Resources, která přecházejí do Common Data Service, lze vykazovat prostřednictvím konektoru Power Apps Common Data Service do Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="4da03-111">The Human Resources data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="4da03-112">Všimněte si, že Common Data Service obsahuje podmnožinu dat aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4da03-112">Note that Common Data Service contains a subset of Human Resources data.</span></span> <span data-ttu-id="4da03-113">Další informace o Power BI a řídicích panelech uvádí téma [Vytváření sestav a řídicích panelů Power BI pomocí Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="4da03-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="4da03-114">Elektronické výkaznictví je k dispozici pro některé sestavy v aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4da03-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="4da03-115">Přizpůsobení požadované zákazníky lze provádět pomocí možností konfigurace elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="4da03-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="4da03-116">Data lze exportovat do aplikace Microsoft Excel nebo Microsoft Word pomocí různých datových entit, které aplikace Human Resources nabízí prostřednictvím integrace s Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="4da03-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="4da03-117">**Dlouhodobé řešení**</span><span class="sxs-lookup"><span data-stu-id="4da03-117">**Long-term solution**</span></span>

<span data-ttu-id="4da03-118">Další možnosti Power BI budou k dispozici a více dat a entit se stane součástí Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4da03-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
