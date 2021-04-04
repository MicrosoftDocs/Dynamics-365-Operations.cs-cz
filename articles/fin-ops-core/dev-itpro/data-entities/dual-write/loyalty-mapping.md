---
title: Věrnostní karty a odměny zákazníka
description: Tohle téma popisuje integraci údajů o věrnostních kartách odběratelů a bodů odměňování v duálním zápisu.
author: RamaKrishnamoorthy
manager: AnnBe
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
ms.openlocfilehash: 39e1d5b0a73b198b164e51a18222dbd985192070
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568021"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="8a9b6-103">Věrnostní karty a odměny zákazníka</span><span class="sxs-lookup"><span data-stu-id="8a9b6-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8a9b6-104">Podniky klasifikují zákazníky a poskytující sofistikované služby na základě vzorců nakupování a utrácení zákazníků.</span><span class="sxs-lookup"><span data-stu-id="8a9b6-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="8a9b6-105">Například Dynamics 365 Commerce má infrastrukturu a funkce pro podporu a zpracování věrnostních karety zákazníků, bodů odměny, věrnostních cen a nákupů založených na cenách.</span><span class="sxs-lookup"><span data-stu-id="8a9b6-105">For example, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="8a9b6-106">Když se data o věrnostních kartách zákazníků a body odměny v Commerce synchronizují do Dataverse, aplikace pro zapojení zákazníka mohou tato data použít.</span><span class="sxs-lookup"><span data-stu-id="8a9b6-106">When data about customer loyalty cards and reward points in Commerce is synced to Dataverse, customer engagement apps can use that data.</span></span> <span data-ttu-id="8a9b6-107">Například uživatelé Dynamics 365 Customer Service mohou pomocí těchto dat poskytovat stejně propracované služby prostřednictvím technické podpory.</span><span class="sxs-lookup"><span data-stu-id="8a9b6-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="8a9b6-108">Šablony</span><span class="sxs-lookup"><span data-stu-id="8a9b6-108">Templates</span></span>

| <span data-ttu-id="8a9b6-109">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8a9b6-109">Finance and Operations apps</span></span> | <span data-ttu-id="8a9b6-110">Modelem řízené aplikace v Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="8a9b6-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="8a9b6-111">popis</span><span class="sxs-lookup"><span data-stu-id="8a9b6-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="8a9b6-112">Věrnostní karta</span><span class="sxs-lookup"><span data-stu-id="8a9b6-112">Loyalty card</span></span>                | <span data-ttu-id="8a9b6-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="8a9b6-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="8a9b6-114">Tato šablona synchronizuje informace o věrnostních kartách zákazníků.</span><span class="sxs-lookup"><span data-stu-id="8a9b6-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="8a9b6-115">Body věrnostní odměny</span><span class="sxs-lookup"><span data-stu-id="8a9b6-115">Loyalty reward points</span></span>       | <span data-ttu-id="8a9b6-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="8a9b6-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="8a9b6-117">Tato šablona synchronizuje informace o bodech odměn zákazníků.</span><span class="sxs-lookup"><span data-stu-id="8a9b6-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]