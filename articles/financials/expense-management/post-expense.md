---
title: "Zaúčtování sestavy výdajů"
description: "Toto téma vysvětluje, jak zaúčtovat sestavu výdajů do hlavní knihy."
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: cc3aae061038202ec4f314654d9149c31e2575bb
ms.contentlocale: cs-cz
ms.lasthandoff: 03/13/2018

---

# <a name="post-an-expense-report"></a><span data-ttu-id="1c9ce-103">Zaúčtování sestavy výdajů</span><span class="sxs-lookup"><span data-stu-id="1c9ce-103">Post an expense report</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1c9ce-104">Po schválení a převedení sestavy výdajů do hlavního deníku lze sestavu zaúčtovat do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="1c9ce-104">After an expense report has been approved and transferred to the general journal, it can be posted to the general ledger.</span></span> <span data-ttu-id="1c9ce-105">Při zaúčtování sestavy výdajů se identifikují výdaje s nárokem na vrácení DPH.</span><span class="sxs-lookup"><span data-stu-id="1c9ce-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="1c9ce-106">Zaměstnanci, který je zodpovědný za ověření sestavy výdajů, je přiřazen úkol ověření a vrácení plateb DPH.</span><span class="sxs-lookup"><span data-stu-id="1c9ce-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="1c9ce-107">Pokud jsou výdaje v sestavě výdajů účtovány jiné společnosti, než je společnost zaměstnávající konkrétního zaměstnance, musíte ověřit společnost, které mají být výdaje proplaceny, a společnost, která výdaje dluží.</span><span class="sxs-lookup"><span data-stu-id="1c9ce-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify the company that those expenses are owed to and the company that the expenses are owed from.</span></span> <span data-ttu-id="1c9ce-108">Například zaměstnanec, který odeslal sestavu výdajů, pracuje pro společnost DAT, ale účtoval výdaj společnosti DIR.</span><span class="sxs-lookup"><span data-stu-id="1c9ce-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="1c9ce-109">V takovém případě DAT je společnost, vůči které jsou výdaje dlužny, a DIR je společnost, která výdaje dluží.</span><span class="sxs-lookup"><span data-stu-id="1c9ce-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="1c9ce-110">Po ověření těchto řádků deníku lze zaúčtovat řádky výdajů do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="1c9ce-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="1c9ce-111">Chcete-li zaúčtovat sestavu výdajů, na stránce **Schválené sestavy výdajů** vyberte sestavu výdajů a poté vyberte v podokně akcí **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="1c9ce-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="1c9ce-112">Současně lze rovněž zaúčtovat všechny sestavy výdajů v seznamu.</span><span class="sxs-lookup"><span data-stu-id="1c9ce-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="1c9ce-113">Vyberte všechny sestavy výdajů a vyberte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="1c9ce-113">Select all the expense reports, and then select **Post**.</span></span>

