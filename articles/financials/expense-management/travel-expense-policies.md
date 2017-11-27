---
title: "Definice zásad výdajů"
description: "Můžete definovat zásady výdajů, které musí pracovníci dodržovat při zadávání a odesílání sestav výdajů a cestovních žádanek v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: saraschi2
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9a5ce1a3b6519b510c9f5aa5618ab91f77a2d91a
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="expense-policies"></a><span data-ttu-id="85b9a-103">Zásady výdajů</span><span class="sxs-lookup"><span data-stu-id="85b9a-103">Expense policies</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="85b9a-104">Můžete definovat zásady, které musí pracovníci dodržovat při zadávání a odesílání sestav výdajů a cestovních žádanek.</span><span class="sxs-lookup"><span data-stu-id="85b9a-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span> <span data-ttu-id="85b9a-105">Implementací zásad výdajů budete moci efektivně spravovat výdaje.</span><span class="sxs-lookup"><span data-stu-id="85b9a-105">Implementing expense policies can help you manage expenses effectively.</span></span> 

<span data-ttu-id="85b9a-106">Můžete například nastavit zásadu pro výdaje za hotel v New Yorku, která stanoví, že výdaje nesmí přesáhnout 250 USD za jeden nocleh.</span><span class="sxs-lookup"><span data-stu-id="85b9a-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span> <span data-ttu-id="85b9a-107">Pokud pracovník odešle sestavu výdajů nebo cestovní žádanku, ve kterých cena za pokoj překročí tuto částku, systém upozorní pracovníka, že překročil částku zásady nastavenou pro výdaje.</span><span class="sxs-lookup"><span data-stu-id="85b9a-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="85b9a-108">Můžete konfigurovat zprávu, kterou zaměstnanec obdrží při definování zásady.</span><span class="sxs-lookup"><span data-stu-id="85b9a-108">You can configure the message that the worker will receive when you define the policy.</span></span> 

<span data-ttu-id="85b9a-109">Můžete definovat tři typy zásad:</span><span class="sxs-lookup"><span data-stu-id="85b9a-109">You can define three types of policies:</span></span> 

 - <span data-ttu-id="85b9a-110">Upozornění - Umožňuje pracovníkovi odeslat výkaz výdajů nebo cestovní žádanku, ale výdaje budou označeny pro všechny schvalující osoby a</span><span class="sxs-lookup"><span data-stu-id="85b9a-110">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>  
 <span data-ttu-id="85b9a-111">pro pozdější vykazování.</span><span class="sxs-lookup"><span data-stu-id="85b9a-111">for later reporting.</span></span> 
 - <span data-ttu-id="85b9a-112">Chyba – Požaduje po pracovníkovi opravit výdaje, aby byly v souladu se zásadou před odesláním sestavy výdajů nebo cestovní žádanky.</span><span class="sxs-lookup"><span data-stu-id="85b9a-112">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span> 
 - <span data-ttu-id="85b9a-113">Zdůvodnění – Požaduje po pracovníkovi nebo manažerovi zadat odůvodnění částky přesahující zásadu před odesláním sestavy výdajů nebo cestovní žádanky.</span><span class="sxs-lookup"><span data-stu-id="85b9a-113">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span> 

<span data-ttu-id="85b9a-114">Můžete také nastavit rozsah dat, pro které jsou zásady výdajů platné.</span><span class="sxs-lookup"><span data-stu-id="85b9a-114">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="85b9a-115">Například ceny letenek pro lety mezi Dánskem a New Yorkem mohou být během vrcholné prázdninové sezóny drahé.</span><span class="sxs-lookup"><span data-stu-id="85b9a-115">For example, airline fares for flights between Denmark and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="85b9a-116">Můžete definovat pravidlo výdajů pro lety, které omezuje náklady na lety do New Yorku až do výše 5000 DKK, a můžete specifikovat, že toto pravidlo bude platné od 15. března do 15. září.</span><span class="sxs-lookup"><span data-stu-id="85b9a-116">You can define a flight expense rule that restricts the cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and September 15.</span></span> 

