---
title: Věrnostní karty a odměny zákazníka
description: Tohle téma popisuje integraci údajů o věrnostních kartách odběratelů a bodů odměňování v duálním zápisu.
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
ms.openlocfilehash: 28872e9510394cf3d5cee151798d4130b8b6fe27
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683491"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="24972-103">Věrnostní karty a odměny zákazníka</span><span class="sxs-lookup"><span data-stu-id="24972-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="24972-104">Podniky klasifikují zákazníky a poskytující sofistikované služby na základě vzorců nakupování a utrácení zákazníků.</span><span class="sxs-lookup"><span data-stu-id="24972-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="24972-105">Například Dynamics 365 Commerce má infrastrukturu a funkce pro podporu a zpracování věrnostních karety zákazníků, bodů odměny, věrnostních cen a nákupů založených na cenách.</span><span class="sxs-lookup"><span data-stu-id="24972-105">For example, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="24972-106">Když se data o věrnostních kartách zákazníků a body odměny v Commerce synchronizují do Dataverse, aplikace pro zapojení zákazníka mohou tato data použít.</span><span class="sxs-lookup"><span data-stu-id="24972-106">When data about customer loyalty cards and reward points in Commerce is synced to Dataverse, customer engagement apps can use that data.</span></span> <span data-ttu-id="24972-107">Například uživatelé Dynamics 365 Customer Service mohou pomocí těchto dat poskytovat stejně propracované služby prostřednictvím technické podpory.</span><span class="sxs-lookup"><span data-stu-id="24972-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="24972-108">Šablony</span><span class="sxs-lookup"><span data-stu-id="24972-108">Templates</span></span>

| <span data-ttu-id="24972-109">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="24972-109">Finance and Operations apps</span></span> | <span data-ttu-id="24972-110">Modelem řízené aplikace v Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="24972-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="24972-111">popis</span><span class="sxs-lookup"><span data-stu-id="24972-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="24972-112">Věrnostní karta</span><span class="sxs-lookup"><span data-stu-id="24972-112">Loyalty card</span></span>                | <span data-ttu-id="24972-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="24972-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="24972-114">Tato šablona synchronizuje informace o věrnostních kartách zákazníků.</span><span class="sxs-lookup"><span data-stu-id="24972-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="24972-115">Body věrnostní odměny</span><span class="sxs-lookup"><span data-stu-id="24972-115">Loyalty reward points</span></span>       | <span data-ttu-id="24972-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="24972-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="24972-117">Tato šablona synchronizuje informace o bodech odměn zákazníků.</span><span class="sxs-lookup"><span data-stu-id="24972-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
