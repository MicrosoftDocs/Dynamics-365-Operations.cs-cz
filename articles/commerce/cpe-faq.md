---
title: Časté otázky týkající se prostředí vyhodnocení Dynamics 365 Commerce
description: V tomto tématu jsou odpovědi na časté otázky týkající se prostředí vyhodnocení Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 637714e28b9f8f4aa66e251e709d8f78bff2739d
ms.sourcegitcommit: 5175e3fae432016246244cf70fe05465f43de88c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/17/2020
ms.locfileid: "3599746"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a><span data-ttu-id="b3f1d-103">Časté otázky týkající se prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b3f1d-103">Dynamics 365 Commerce evaluation environment FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b3f1d-104">V tomto tématu jsou odpovědi na časté otázky týkající se prostředí vyhodnocení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-104">This topic provides answers to frequently asked questions about the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="b3f1d-105">**Můžeme použít prostředí vyhodnocení Commerce jako úložiště elektronického obchodu pro zákazníky, kteří aktuálně implementují program Retail?**</span><span class="sxs-lookup"><span data-stu-id="b3f1d-105">**Can we use the Commerce evaluation environment as an e-Commerce storefront for customers that currently implement Retail?**</span></span>

<span data-ttu-id="b3f1d-106">Č.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-106">No.</span></span> <span data-ttu-id="b3f1d-107">Prostředí vyhodnocení obchodu je pouze pro hodnocení.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-107">The Commerce evaluation environment is only for evaluation.</span></span> <span data-ttu-id="b3f1d-108">Pokud požadujete prostředí pro zákazníka, který implementuje program Retail, kontaktujte společnost Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-108">If you require an environment for a customer that implements Retail, contact Microsoft.</span></span>

<span data-ttu-id="b3f1d-109">**Je možné použít prostředí vyhodnocení Commerce ke zřizování funkcí elektronického obchodování nad rámec existující aplikace nebo prostředí, které implementuje program Retail?**</span><span class="sxs-lookup"><span data-stu-id="b3f1d-109">**Can the Commerce evaluation environment be used to provision the e-Commerce features on top of an existing application/environment that implements Retail?**</span></span>

<span data-ttu-id="b3f1d-110">Ne (většinou).</span><span class="sxs-lookup"><span data-stu-id="b3f1d-110">No (mostly).</span></span> <span data-ttu-id="b3f1d-111">Komponenty vyhodnocení obchodu jsou k dispozici pouze v prostředích, která odpovídají konfiguracím specifikovaným v příručce pro předpoklady a zajišťování.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-111">The Commerce evaluation components are available only to environments that match the configurations that are specified in the prerequisites and provisioning guide.</span></span> <span data-ttu-id="b3f1d-112">Požadovaná základní ukázková data navíc nebudou dostupná v prostředích, která byla nasazena s počátečním vydáním starším než 10.0.8.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-112">Additionally, the required base demo data won't be available in environments that were deployed with an initial release that is earlier than 10.0.8.</span></span> 

<span data-ttu-id="b3f1d-113">**Jaké náklady jsou zahrnuty v nasazení prostředí vyhodnocení Commerce v Microsoft Azure prostřednictvím Microsoft Dynamics Lifecycle Services (LCS)?**</span><span class="sxs-lookup"><span data-stu-id="b3f1d-113">**What costs are involved in deploying the Commerce evaluation environment on Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**</span></span>

<span data-ttu-id="b3f1d-114">Tradiční demo prostředí ústředí Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce (virtuální stroj \[VM \]) bude hostována ve vašem předplatném služby Azure.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-114">A traditional Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce headquarters demo environment (virtual machine \[VM\]) will be hosted in your Azure subscription.</span></span> <span data-ttu-id="b3f1d-115">K odhadu těchto nákladů [můžete použít kalkulačku cen Azure](https://azure.microsoft.com/pricing/calculator/).</span><span class="sxs-lookup"><span data-stu-id="b3f1d-115">You can use the [Azure pricing calculator](https://azure.microsoft.com/pricing/calculator/) to estimate this cost.</span></span>

<span data-ttu-id="b3f1d-116">Ostatní komponenty, jako je Commerce Scale Unit, Tvůrce webu Commerce a váš web elektronického obchodu, budou k dispozici jako software jako služba (SaaS) a budou hostovány společností Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-116">Other components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site will be available as software as a service (SaaS) and hosted by Microsoft.</span></span>

<span data-ttu-id="b3f1d-117">**Které oblasti Azure jsou aktuálně podporovány v prostředí vyhodnocení Commerce?**</span><span class="sxs-lookup"><span data-stu-id="b3f1d-117">**Which Azure geographies are currently supported for the Commerce evaluation environment?**</span></span>

<span data-ttu-id="b3f1d-118">Prostředí vyhodnocení Commerce je možné nasadit pouze v severoamerické zeměpisné oblasti.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-118">The Commerce evaluation environment can be deployed only in the North America geography.</span></span>

<span data-ttu-id="b3f1d-119">**Existuje virtuální pevný disk (VHD) s možností stažení, který má kompletní možnost virtuálního počítače OneBox (VM)?**</span><span class="sxs-lookup"><span data-stu-id="b3f1d-119">**Is there a downloadable virtual hard disk (VHD) that has the complete OneBox virtual machine (VM) option?**</span></span>

<span data-ttu-id="b3f1d-120">Dynamics 365 Commerce a Commerce Scale Unit jsou kompletní software jako služba (SaaS) a musí být hostovány v cloudu.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-120">Dynamics 365 Commerce and Commerce Scale Unit are completely software as a service (SaaS) and must be cloud-hosted.</span></span>

<span data-ttu-id="b3f1d-121">**Jak dlouho je možné používat prostředí vyhodnocení Commerce?**</span><span class="sxs-lookup"><span data-stu-id="b3f1d-121">**How long can the Commerce evaluation environment be used?**</span></span>

<span data-ttu-id="b3f1d-122">Prostředí vyhodnocení Commerce má lhůtu 30 dnů ode dne, kdy jsou poskytovány komponenty SaaS, jako je Commerce Scale Unit, Tvůrce webu Commerce a váš web e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-122">The Commerce evaluation environment has a 30-day time limit from the date when SaaS components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site are provisioned.</span></span>

<span data-ttu-id="b3f1d-123">**Lze prodloužit časový limit pro prostředí vyhodnocení Commerce?**</span><span class="sxs-lookup"><span data-stu-id="b3f1d-123">**Can I extend the time limit for my Commerce evaluation environment?**</span></span>

<span data-ttu-id="b3f1d-124">Prodloužení lhůty je výjimkou z normy a posuzuje se případ od případu.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-124">Extension of the time limit is an exception to the norm and is considered on a case-by-case basis.</span></span> <span data-ttu-id="b3f1d-125">Měli byste se obrátit na svého partnera společnosti Microsoft s žádostí o pomoc.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-125">You should reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b3f1d-126">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="b3f1d-126">Additional resources</span></span>

[<span data-ttu-id="b3f1d-127">Přehled prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b3f1d-127">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="b3f1d-128">Zřízení prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b3f1d-128">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="b3f1d-129">Konfigurace prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b3f1d-129">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="b3f1d-130">Konfigurovat BOPIS v prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b3f1d-130">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="b3f1d-131">Konfigurace volitelných funkcí pro prostředí vyhodnocení aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b3f1d-131">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)
