---
title: Definice zásad výdajů
description: Můžete definovat zásady výdajů, které musí pracovníci dodržovat při zadávání a odesílání sestav výdajů a cestovních žádanek v aplikaci Microsoft Dynamics 365 for Finance and Operations.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04eaff110fea021ddee32be650be540894eb703b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "342424"
---
# <a name="expense-policies"></a><span data-ttu-id="8d30b-103">Zásady výdajů</span><span class="sxs-lookup"><span data-stu-id="8d30b-103">Expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d30b-104">Můžete definovat zásady, které musí pracovníci dodržovat při zadávání a odesílání sestav výdajů a cestovních žádanek.</span><span class="sxs-lookup"><span data-stu-id="8d30b-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="8d30b-105">Implementací zásad výdajů budete moci efektivně spravovat výdaje.</span><span class="sxs-lookup"><span data-stu-id="8d30b-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="8d30b-106">Můžete například nastavit zásadu pro výdaje za hotel v New Yorku, která stanoví, že výdaje nesmí přesáhnout 250 USD za jeden nocleh.</span><span class="sxs-lookup"><span data-stu-id="8d30b-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="8d30b-107">Pokud pracovník odešle sestavu výdajů nebo cestovní žádanku, ve kterém sazba za pokoj přesáhne tuto částku, systém oznámí</span><span class="sxs-lookup"><span data-stu-id="8d30b-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="8d30b-108">pracovníkovi, že částka zásad pro výdaje byla překročena</span><span class="sxs-lookup"><span data-stu-id="8d30b-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="8d30b-109">Můžete konfigurovat zprávu, kterou zaměstnanec obdrží při</span><span class="sxs-lookup"><span data-stu-id="8d30b-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="8d30b-110">definování zásady.</span><span class="sxs-lookup"><span data-stu-id="8d30b-110">define the policy.</span></span>      
        
<span data-ttu-id="8d30b-111">Můžete definovat tři typy zásad:</span><span class="sxs-lookup"><span data-stu-id="8d30b-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="8d30b-112">Upozornění - Umožňuje pracovníkovi odeslat výkaz výdajů nebo cestovní žádanku, ale výdaje budou označeny pro všechny schvalující osoby a</span><span class="sxs-lookup"><span data-stu-id="8d30b-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="8d30b-113">pro pozdější vykazování.</span><span class="sxs-lookup"><span data-stu-id="8d30b-113">for later reporting.</span></span>        

- <span data-ttu-id="8d30b-114">Chyba – Požaduje po pracovníkovi opravit výdaje, aby byly v souladu se zásadou před odesláním sestavy výdajů nebo cestovní žádanky.</span><span class="sxs-lookup"><span data-stu-id="8d30b-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
  - <span data-ttu-id="8d30b-115">Zdůvodnění – Požaduje po pracovníkovi nebo manažerovi zadat odůvodnění částky přesahující zásadu před odesláním sestavy výdajů nebo cestovní žádanky.</span><span class="sxs-lookup"><span data-stu-id="8d30b-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        
 
  <span data-ttu-id="8d30b-116">Můžete také nastavit rozsah dat, pro které jsou zásady výdajů platné.</span><span class="sxs-lookup"><span data-stu-id="8d30b-116">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="8d30b-117">Například letenky pro lety z Dánska</span><span class="sxs-lookup"><span data-stu-id="8d30b-117">For example, airline fares for flights between Denmark</span></span>      
  <span data-ttu-id="8d30b-118">do New York City mohou být během cestovní špičky v průběhu dovolených drahé.</span><span class="sxs-lookup"><span data-stu-id="8d30b-118">and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="8d30b-119">Můžete definovat pravidlo pro ceny letenek, které bude omezovat</span><span class="sxs-lookup"><span data-stu-id="8d30b-119">You can define a flight expense rule that restricts the</span></span>      
  <span data-ttu-id="8d30b-120">náklady na lety do New York City na 5000 DKK, a také zadat, že toto pravidlo má platit od 15. března</span><span class="sxs-lookup"><span data-stu-id="8d30b-120">cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and</span></span>      
  <span data-ttu-id="8d30b-121">do 15. září.</span><span class="sxs-lookup"><span data-stu-id="8d30b-121">September 15.</span></span>
