---
title: Přehled prostředí vyhodnocení aplikace Dynamics 365 Commerce
description: Toto téma poskytuje přehled o prostředí vyhodnocení Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c890d7c49b6607ab0cbad536bbf8a3649465a7c1
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193485"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a><span data-ttu-id="86874-103">Přehled prostředí vyhodnocení aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="86874-103">Dynamics 365 Commerce evaluation environment overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="86874-104">Toto téma poskytuje přehled o prostředí vyhodnocení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="86874-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

> [!NOTE]
> <span data-ttu-id="86874-105">Prostředí vyhodnocení Commerce nejsou obecně dostupná a jsou poskytována partnerům a zákazníkům na základě žádosti.</span><span class="sxs-lookup"><span data-stu-id="86874-105">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="86874-106">Podrobnější informace získáte od kontaktu společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="86874-106">For more information, reach out to your Microsoft partner contact.</span></span>

<span data-ttu-id="86874-107">Prostředí vyhodnocení Commerce je volitelné komplexní prostředí Dynamics 365 Commerce, které partnerům a potenciálním zákazníkům umožňuje vyzkoušet produkt Commerce.</span><span class="sxs-lookup"><span data-stu-id="86874-107">The Commerce evaluation environment is an optional end-to-end environment of Dynamics 365 Commerce that lets partners and potential customers try out the Commerce product.</span></span>

<span data-ttu-id="86874-108">Vyhodnocovací prostředí jsou částečně předkonfigurována, aby se snížily požadované kroky po poskytnutí.</span><span class="sxs-lookup"><span data-stu-id="86874-108">Evaluation environments are partially preconfigured to reduce the required post-provisioning steps.</span></span>

<span data-ttu-id="86874-109">Kromě menších omezení, která neovlivňují funkce nebo funkčnost, poskytuje prostředí vyhodnocení Commerce kompletní zkušenost s tímto produktem a mohou je používat zákazníci a partneři k implementaci pro vyhodnocení produktu, poskytnutí zpětné vazby a analýze přizpůsobení nebo nedostatků.</span><span class="sxs-lookup"><span data-stu-id="86874-109">Aside from some minor limitations that don't affect features or functionality, the Commerce evaluation environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-evaluation-environment"></a><span data-ttu-id="86874-110">Omezení prostředí vyhodnocení Commerce</span><span class="sxs-lookup"><span data-stu-id="86874-110">Limitations of the Commerce evaluation environment</span></span>

<span data-ttu-id="86874-111">I když prostředí vyhodnocení Commerce nabízí úplnou sadu funkcí a funkčnosti Commerce, existuje několik menších omezení:</span><span class="sxs-lookup"><span data-stu-id="86874-111">Although the Commerce evaluation environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="86874-112">Přestože prostředí vyhodnocení Commerce nemá žádná zeměpisná omezení, součásti prostředí, jako například aplikace Retail Cloud Scale Unit (rcsu) a e-commerce, by se měly zřizovat pouze ve Spojených státech.</span><span class="sxs-lookup"><span data-stu-id="86874-112">Although the Commerce evaluation environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, should be provisioned only in the United States.</span></span>
- <span data-ttu-id="86874-113">Použití prostředí vyhodnocení Commerce je omezeno na 30 dní od data, kdy je zřízeno prostředí e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="86874-113">Use of the Commerce evaluation environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="86874-114">Prostředí vyhodnocení Commerce je možné úspěšně nasadit a inicializovat pouze v prostředí, ve kterém je použita ukázková topologie, kde jsou všechny součásti prostředí nasazeny na jednom virtuálním počítači (VM) hostovaném v cloudu.</span><span class="sxs-lookup"><span data-stu-id="86874-114">The Commerce evaluation environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed on a single cloud-hosted virtual machine (VM).</span></span> <span data-ttu-id="86874-115">Hlavní omezení této topologie je počet uživatelů, které může prostředí současně podporovat.</span><span class="sxs-lookup"><span data-stu-id="86874-115">The main limitation of this topology is the number of concurrent users that the environment can support.</span></span>

## <a name="get-started"></a><span data-ttu-id="86874-116">Začínáme</span><span class="sxs-lookup"><span data-stu-id="86874-116">Get started</span></span>

<span data-ttu-id="86874-117">Chcete-li zřizovat prostředí vyhodnocení Commerce, získáte informace v části [Zřízení prostředí vyhodnocení Commerce](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="86874-117">To provision the Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="86874-118">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="86874-118">Additional resources</span></span>

[<span data-ttu-id="86874-119">Zřízení prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="86874-119">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="86874-120">Konfigurace prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="86874-120">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="86874-121">Konfigurovat BOPIS v prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="86874-121">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="86874-122">Konfigurace volitelných funkcí pro prostředí vyhodnocení aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="86874-122">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="86874-123">Časté otázky týkající se prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="86874-123">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
