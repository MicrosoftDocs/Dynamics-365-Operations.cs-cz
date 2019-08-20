---
title: Definice zásad výdajů
description: Můžete definovat zásady výdajů, které musí pracovníci dodržovat při zadávání a odesílání sestav výdajů a cestovních žádanek v aplikaci Microsoft Dynamics 365 for Finance and Operations.
author: ryansandness
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26336710b277ce9594c8546f2214e152a3460204
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840882"
---
# <a name="expense-policies"></a><span data-ttu-id="610ba-103">Zásady výdajů</span><span class="sxs-lookup"><span data-stu-id="610ba-103">Expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="610ba-104">Můžete definovat zásady, které musí pracovníci dodržovat při zadávání a odesílání sestav výdajů a cestovních žádanek.</span><span class="sxs-lookup"><span data-stu-id="610ba-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="610ba-105">Implementací zásad výdajů budete moci efektivně spravovat výdaje.</span><span class="sxs-lookup"><span data-stu-id="610ba-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="610ba-106">Můžete například nastavit zásadu pro výdaje za hotel v New Yorku, která stanoví, že výdaje nesmí přesáhnout 250 USD za jeden nocleh.</span><span class="sxs-lookup"><span data-stu-id="610ba-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="610ba-107">Pokud pracovník odešle sestavu výdajů nebo cestovní žádanku, ve kterém sazba za pokoj přesáhne tuto částku, systém oznámí</span><span class="sxs-lookup"><span data-stu-id="610ba-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="610ba-108">pracovníkovi, že částka zásad pro výdaje byla překročena</span><span class="sxs-lookup"><span data-stu-id="610ba-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="610ba-109">Můžete konfigurovat zprávu, kterou zaměstnanec obdrží při</span><span class="sxs-lookup"><span data-stu-id="610ba-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="610ba-110">definování zásady.</span><span class="sxs-lookup"><span data-stu-id="610ba-110">define the policy.</span></span>      
        
<span data-ttu-id="610ba-111">Můžete definovat tři typy zásad:</span><span class="sxs-lookup"><span data-stu-id="610ba-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="610ba-112">Upozornění - Umožňuje pracovníkovi odeslat výkaz výdajů nebo cestovní žádanku, ale výdaje budou označeny pro všechny schvalující osoby a</span><span class="sxs-lookup"><span data-stu-id="610ba-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="610ba-113">pro pozdější vykazování.</span><span class="sxs-lookup"><span data-stu-id="610ba-113">for later reporting.</span></span>        

- <span data-ttu-id="610ba-114">Chyba – Požaduje po pracovníkovi opravit výdaje, aby byly v souladu se zásadou před odesláním sestavy výdajů nebo cestovní žádanky.</span><span class="sxs-lookup"><span data-stu-id="610ba-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="610ba-115">Zdůvodnění – Požaduje po pracovníkovi nebo manažerovi zadat odůvodnění částky přesahující zásadu před odesláním sestavy výdajů nebo cestovní žádanky.</span><span class="sxs-lookup"><span data-stu-id="610ba-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="610ba-116">Tipy pro zásady</span><span class="sxs-lookup"><span data-stu-id="610ba-116">Policy tips</span></span>
<span data-ttu-id="610ba-117">Zde je několik návrhů, které vám mohou pomoci při vytváření nových zásad pro správu výdajů.</span><span class="sxs-lookup"><span data-stu-id="610ba-117">Here are a few suggestions that can assist you whe creating new policies for expense management.</span></span> 
* <span data-ttu-id="610ba-118">Zásady mají časovou platnost a neuplatní se, pokud je zásada vytvořena s datem po datu, kdy došlo k výdaji.</span><span class="sxs-lookup"><span data-stu-id="610ba-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="610ba-119">Vytváříte-li například novou zásadu dnes za účelem vynucení maximálních výdajů na jídlo ve výši 50 USD, nebude možné proti této zásadě kontrolovat existující výdaje, které jste zadali včera.</span><span class="sxs-lookup"><span data-stu-id="610ba-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="610ba-120">Při vytváření zásady pro kategorii výdajů, která může být rozepsaná, zvažte přidání podmínky pro typ řádku výdajů.</span><span class="sxs-lookup"><span data-stu-id="610ba-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="610ba-121">Některé zásady, jako je například vyžadování účtenky, nemusí mít smysl pro rozepsané řádky a měly by být použity pouze na řádek záhlaví nebo na nerozepsaný řádek.</span><span class="sxs-lookup"><span data-stu-id="610ba-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="610ba-122">Kdy vyhodnotit zásady</span><span class="sxs-lookup"><span data-stu-id="610ba-122">When to evaluate policies</span></span>

<span data-ttu-id="610ba-123">V parametrech správy výdajů je k dispozici možnost vyhodnotit zásady správy výdajů při uložení řádku nebo při odeslání sestavy výdajů.</span><span class="sxs-lookup"><span data-stu-id="610ba-123">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="610ba-124">Rozhodnete-li se vyhodnocovat při uložení řádku, zajistíte, že uživatelé mají včasnější viditelnost toho, co musí udělat pro dokončení všech svých sestav výdajů najednou.</span><span class="sxs-lookup"><span data-stu-id="610ba-124">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="610ba-125">V opačném případě můžete zpozdit vyhodnocení zásady a ušetřit čas v případě, že dochází k ověření na konci během odesílání do workflow.</span><span class="sxs-lookup"><span data-stu-id="610ba-125">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
