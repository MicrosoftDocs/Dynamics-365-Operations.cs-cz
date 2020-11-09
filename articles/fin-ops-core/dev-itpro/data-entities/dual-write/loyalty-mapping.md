---
title: Věrnostní karty a odměny zákazníka
description: Tohle téma popisuje integraci údajů o věrnostních kartách odběratelů a bodů odměňování mezi aplikacemi Finance and Operations a Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 24ce08bb6cba9c74075151bafe0b07509fbdf73d
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998007"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="e18fc-103">Věrnostní karty a odměny zákazníka</span><span class="sxs-lookup"><span data-stu-id="e18fc-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="e18fc-104">Podniky klasifikují zákazníky a poskytující sofistikované služby na základě vzorců nakupování a utrácení zákazníků.</span><span class="sxs-lookup"><span data-stu-id="e18fc-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="e18fc-105">V sadě aplikací Microsoft Dynamics 365 má Dynamics 365 Commerce infrastrukturu a funkce pro podporu a zpracování věrnostních karety zákazníků, bodů odměny, věrnostních cen a nákupů založených na cenách.</span><span class="sxs-lookup"><span data-stu-id="e18fc-105">In the Microsoft Dynamics 365 suite of applications, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="e18fc-106">Když se data o věrnostních kartách zákazníků a body odměny v Commerce synchronizují s Common Data Service, modelem řízené aplikace Dynamics 365 mohou tato data použít.</span><span class="sxs-lookup"><span data-stu-id="e18fc-106">When data about customer loyalty cards and reward points in Commerce is synced to Common Data service, model-driven apps in Dynamics 365 can use that data.</span></span> <span data-ttu-id="e18fc-107">Například uživatelé Dynamics 365 Customer Service mohou pomocí těchto dat poskytovat stejně propracované služby prostřednictvím technické podpory.</span><span class="sxs-lookup"><span data-stu-id="e18fc-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="e18fc-108">Šablony</span><span class="sxs-lookup"><span data-stu-id="e18fc-108">Templates</span></span>

| <span data-ttu-id="e18fc-109">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e18fc-109">Finance and Operations apps</span></span> | <span data-ttu-id="e18fc-110">Modelem řízené aplikace v Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="e18fc-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="e18fc-111">popis</span><span class="sxs-lookup"><span data-stu-id="e18fc-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="e18fc-112">Věrnostní karta</span><span class="sxs-lookup"><span data-stu-id="e18fc-112">Loyalty card</span></span>                | <span data-ttu-id="e18fc-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="e18fc-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="e18fc-114">Tato šablona synchronizuje informace o věrnostních kartách zákazníků.</span><span class="sxs-lookup"><span data-stu-id="e18fc-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="e18fc-115">Body věrnostní odměny</span><span class="sxs-lookup"><span data-stu-id="e18fc-115">Loyalty reward points</span></span>       | <span data-ttu-id="e18fc-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="e18fc-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="e18fc-117">Tato šablona synchronizuje informace o bodech odměn zákazníků.</span><span class="sxs-lookup"><span data-stu-id="e18fc-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
