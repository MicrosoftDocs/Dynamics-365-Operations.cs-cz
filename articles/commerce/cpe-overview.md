---
title: Přehled prostředí náhledu Commerce
description: Toto téma poskytuje přehled o prostředí náhledu v řešení Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
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
ms.openlocfilehash: 901583afde4739be5313fa129ff0e52f11326881
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906063"
---
# <a name="commerce-preview-environment-overview"></a><span data-ttu-id="b6335-103">Přehled prostředí náhledu Commerce</span><span class="sxs-lookup"><span data-stu-id="b6335-103">Commerce preview environment overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b6335-104">Toto téma poskytuje přehled o prostředí náhledu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b6335-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="overview"></a><span data-ttu-id="b6335-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="b6335-105">Overview</span></span>

<span data-ttu-id="b6335-106">Prostředí náhledu produktu Commerce je volitelné komplexní prostředí pro zobrazení náhledu produktu Dynamics 365 Commerce, které potenciálním zákazníkům umožňuje vyzkoušet produkt Commerce před jeho veřejným vydáním.</span><span class="sxs-lookup"><span data-stu-id="b6335-106">The Commerce preview environment is an optional end-to-end preview environment of Dynamics 365 Commerce that lets potential customers try out the Commerce product before its general release to the public.</span></span>

<span data-ttu-id="b6335-107">Kromě menších omezení, která neovlivňují funkce nebo funkčnost, poskytuje prostředí náhledu produktu Commerce kompletní zkušenost s tímto produktem a mohou je používat zákazníci a partneři k implementaci pro vyhodnocení produktu, poskytnutí zpětné vazby a analýze přizpůsobení nebo nedostatků.</span><span class="sxs-lookup"><span data-stu-id="b6335-107">Aside from some minor limitations that don't affect features or functionality, the Commerce preview environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-preview-environment"></a><span data-ttu-id="b6335-108">Omezení prostředí náhledu Commerce</span><span class="sxs-lookup"><span data-stu-id="b6335-108">Limitations of the Commerce preview environment</span></span>

<span data-ttu-id="b6335-109">I když prostředí náhledu Commerce nabízí úplnou sadu funkcí a funkčnosti Commerce, existuje několik menších omezení:</span><span class="sxs-lookup"><span data-stu-id="b6335-109">Although the Commerce preview environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="b6335-110">Přestože prostředí náhledu Commerce nemá žádná zeměpisná omezení, součásti prostředí, jako například aplikace Retail Cloud Scale Unit (rcsu) a e-commerce, lze zřizovat pouze ve Spojených státech.</span><span class="sxs-lookup"><span data-stu-id="b6335-110">Although the Commerce preview environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, can be provisioned only in the United States.</span></span>
- <span data-ttu-id="b6335-111">Použití prostředí náhledu Commerce je omezeno na 30 dní od data, kdy je zřízeno prostředí e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="b6335-111">Use of the Commerce preview environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="b6335-112">Prostředí náhledu Commerce je možné úspěšně nasadit a inicializovat pouze v prostředí, ve kterém je použita ukázková topologie, kde jsou všechny součásti prostředí nasazeny na jednom virtuálním počítači (VM).</span><span class="sxs-lookup"><span data-stu-id="b6335-112">The Commerce preview environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed in a single virtual machine (VM).</span></span> <span data-ttu-id="b6335-113">Hlavní omezení této topologie OneBox VM je počet uživatelů, které může prostředí náhledu současně podporovat.</span><span class="sxs-lookup"><span data-stu-id="b6335-113">The main limitation of this OneBox VM topology is the number of concurrent users that the preview environment can support.</span></span>
- <span data-ttu-id="b6335-114">Prostředí náhledu Commerce je možné posoudit pouze do doby, kdy bude produkt Commerce dostupný široké veřejnosti.</span><span class="sxs-lookup"><span data-stu-id="b6335-114">The Commerce preview environment can be evaluated only until the general availability (GA) of the Commerce product.</span></span> <span data-ttu-id="b6335-115">Nová ukázková prostředí budou k dispozici po vydání pro širokou veřejnost.</span><span class="sxs-lookup"><span data-stu-id="b6335-115">New demo environments will be available after GA.</span></span>

## <a name="get-started"></a><span data-ttu-id="b6335-116">Začínáme</span><span class="sxs-lookup"><span data-stu-id="b6335-116">Get started</span></span>

<span data-ttu-id="b6335-117">Chcete-li zřizovat prostředí pro náhled Commerce, získáte informace v části [Zřízení prostředí náhledu Commerce](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="b6335-117">To provision the Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b6335-118">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="b6335-118">Additional resources</span></span>

[<span data-ttu-id="b6335-119">Zřízení prostředí náhledu Commerce</span><span class="sxs-lookup"><span data-stu-id="b6335-119">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="b6335-120">Konfigurovat prostředí náhledu Commerce</span><span class="sxs-lookup"><span data-stu-id="b6335-120">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="b6335-121">Nastavení volitelných funkcí pro prostředí náhledu Commerce</span><span class="sxs-lookup"><span data-stu-id="b6335-121">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="b6335-122">Často kladené dotazy k prostředí náhledu Commerce</span><span class="sxs-lookup"><span data-stu-id="b6335-122">Commerce preview environment FAQ</span></span>](cpe-faq.md)
