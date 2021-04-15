---
title: Věrnostní karty a odměny zákazníka
description: Tohle téma popisuje integraci údajů o věrnostních kartách odběratelů a bodů odměňování v duálním zápisu.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d2c3845c1a7371d9e992495246e8dd0eb8631020
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747980"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="a7ce7-103">Věrnostní karty a odměny zákazníka</span><span class="sxs-lookup"><span data-stu-id="a7ce7-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a7ce7-104">Podniky klasifikují zákazníky a poskytující sofistikované služby na základě vzorců nakupování a utrácení zákazníků.</span><span class="sxs-lookup"><span data-stu-id="a7ce7-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="a7ce7-105">Například Dynamics 365 Commerce má infrastrukturu a funkce pro podporu a zpracování věrnostních karety zákazníků, bodů odměny, věrnostních cen a nákupů založených na cenách.</span><span class="sxs-lookup"><span data-stu-id="a7ce7-105">For example, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="a7ce7-106">Když se data o věrnostních kartách zákazníků a body odměny v Commerce synchronizují do Dataverse, aplikace pro zapojení zákazníka mohou tato data použít.</span><span class="sxs-lookup"><span data-stu-id="a7ce7-106">When data about customer loyalty cards and reward points in Commerce is synced to Dataverse, customer engagement apps can use that data.</span></span> <span data-ttu-id="a7ce7-107">Například uživatelé Dynamics 365 Customer Service mohou pomocí těchto dat poskytovat stejně propracované služby prostřednictvím technické podpory.</span><span class="sxs-lookup"><span data-stu-id="a7ce7-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="a7ce7-108">Šablony</span><span class="sxs-lookup"><span data-stu-id="a7ce7-108">Templates</span></span>

| <span data-ttu-id="a7ce7-109">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a7ce7-109">Finance and Operations apps</span></span> | <span data-ttu-id="a7ce7-110">Modelem řízené aplikace v Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a7ce7-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="a7ce7-111">popis</span><span class="sxs-lookup"><span data-stu-id="a7ce7-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="a7ce7-112">Věrnostní karta</span><span class="sxs-lookup"><span data-stu-id="a7ce7-112">Loyalty card</span></span>                | <span data-ttu-id="a7ce7-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="a7ce7-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="a7ce7-114">Tato šablona synchronizuje informace o věrnostních kartách zákazníků.</span><span class="sxs-lookup"><span data-stu-id="a7ce7-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="a7ce7-115">Body věrnostní odměny</span><span class="sxs-lookup"><span data-stu-id="a7ce7-115">Loyalty reward points</span></span>       | <span data-ttu-id="a7ce7-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="a7ce7-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="a7ce7-117">Tato šablona synchronizuje informace o bodech odměn zákazníků.</span><span class="sxs-lookup"><span data-stu-id="a7ce7-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]