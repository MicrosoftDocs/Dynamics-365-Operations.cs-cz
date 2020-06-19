---
title: Zásady způsobilosti k zaměstnaneckým výhodám
description: Tento článek obsahuje informace o zásadách pro nároky na zaměstnanecké výhody, které vám umožní definovat, kdo má nárok na specifické zaměstnanecké výhody.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: fd4def17bf60ae2812927221c45547c5ac379f2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430824"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="38be8-103">Zásady způsobilosti k zaměstnaneckým výhodám</span><span class="sxs-lookup"><span data-stu-id="38be8-103">Benefit eligibility policies</span></span>

<span data-ttu-id="38be8-104">Tento článek obsahuje informace o zásadách pro nároky na zaměstnanecké výhody, které vám umožní definovat, kdo má nárok na specifické zaměstnanecké výhody.</span><span class="sxs-lookup"><span data-stu-id="38be8-104">This article provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="38be8-105">Při vytváření zaměstnaneckých výhod rozhodnete, které výhody budou k dispozici pro které zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="38be8-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="38be8-106">V následující tabulce jsou uvedeny příklady výhod, které může být zpřístupnit konkrétním zaměstnancům.</span><span class="sxs-lookup"><span data-stu-id="38be8-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="38be8-107">Zaměstnanecká výhoda</span><span class="sxs-lookup"><span data-stu-id="38be8-107">Benefit</span></span>          | <span data-ttu-id="38be8-108">Pro koho je výhoda dostupná</span><span class="sxs-lookup"><span data-stu-id="38be8-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="38be8-109">Zdravotní pojištění</span><span class="sxs-lookup"><span data-stu-id="38be8-109">Health insurance</span></span> | <span data-ttu-id="38be8-110">Všichni zaměstnanci</span><span class="sxs-lookup"><span data-stu-id="38be8-110">All employees</span></span>                   |
| <span data-ttu-id="38be8-111">Mobilní telefon</span><span class="sxs-lookup"><span data-stu-id="38be8-111">Mobile phone</span></span>     | <span data-ttu-id="38be8-112">Prodavači, vedení</span><span class="sxs-lookup"><span data-stu-id="38be8-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="38be8-113">Parkovací průkazy</span><span class="sxs-lookup"><span data-stu-id="38be8-113">Parking passes</span></span>   | <span data-ttu-id="38be8-114">Výkonné orgány</span><span class="sxs-lookup"><span data-stu-id="38be8-114">Executives</span></span>                      |

<span data-ttu-id="38be8-115">Následující komponenty se používají k vytváření pravidel způsobilosti:</span><span class="sxs-lookup"><span data-stu-id="38be8-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="38be8-116">Typy pravidel zásad</span><span class="sxs-lookup"><span data-stu-id="38be8-116">Policy rule types</span></span>
-   <span data-ttu-id="38be8-117">Zásady způsobilosti k zaměstnaneckým výhodám</span><span class="sxs-lookup"><span data-stu-id="38be8-117">Benefit eligibility policies</span></span>

<span data-ttu-id="38be8-118">Typy pravidel zásad definují parametry dotazů použitých při vývoji specifických pravidel zásad.</span><span class="sxs-lookup"><span data-stu-id="38be8-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="38be8-119">Po vytvoření typů pravidel zásad můžete vytvořit zásady nároků na zaměstnanecké výhody.</span><span class="sxs-lookup"><span data-stu-id="38be8-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="38be8-120">Zásady vám umožní vytvořit kolekci pravidel, která se vztahují na jednu nebo více právnických osob.</span><span class="sxs-lookup"><span data-stu-id="38be8-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="38be8-121">V rámci každé zásady můžete zobrazit všechny typy pravidel zásad nároků na zaměstnanecké výhody, které jste předtím vytvořili.</span><span class="sxs-lookup"><span data-stu-id="38be8-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="38be8-122">Můžete definovat rozsah pravidla v pravidle.</span><span class="sxs-lookup"><span data-stu-id="38be8-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="38be8-123">Pokud například vytvoříte typ pravidla zásad nároků zaměstnanecké výhody s názvem **Výkonný**, lze zadat pravidla v rámci dané zásady.</span><span class="sxs-lookup"><span data-stu-id="38be8-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="38be8-124">V tomto příkladu může pravidlo vyžadovat, že všechny funkce obsahující slovo „výkonný” se zahrnou v pravidle.</span><span class="sxs-lookup"><span data-stu-id="38be8-124">In this example, the rule might state that any job title that contains the word "executive" should be included in the rule.</span></span> <span data-ttu-id="38be8-125">Po definování parametrů pravidla nebo pravidel, která jsou zahrnuta v pravidle, můžete přiřadit konkrétní pravidla k zaměstnanecké výhodě.</span><span class="sxs-lookup"><span data-stu-id="38be8-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>




