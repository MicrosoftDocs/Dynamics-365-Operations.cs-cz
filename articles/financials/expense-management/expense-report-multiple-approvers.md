---
title: Sestavy výdajů a více schvalovatelů
description: Toto téma obsahuje informace o sestavách výdajů, které vyžadují schválení více než jednou osobou.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1483de5405895d60f0cb302ab622758b2b05d2ca
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566977"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="ce9fe-103">Sestavy výdajů a více schvalovatelů</span><span class="sxs-lookup"><span data-stu-id="ce9fe-103">Expense reports and multiple approvers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce9fe-104">V závislosti na zásadách schvalování výdajů ve vaší organizaci může být zapotřebí ke schválení sestavy výdajů odeslané zaměstnancem více než jedna osoba.</span><span class="sxs-lookup"><span data-stu-id="ce9fe-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="ce9fe-105">Při nastavování procesu workflowu pro schválení sestavy výdajů můžete přidat prvky workflowu, které obsahují úkoly nebo kroky pro jednoho nebo více schvalovatelů sestavy výdajů.</span><span class="sxs-lookup"><span data-stu-id="ce9fe-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="ce9fe-106">Můžete například vyžadovat, aby všechny sestavy výdajů schvaloval nejprve manažer zaměstnance, který sestavu odeslal, a poté koordinátorem závazků.</span><span class="sxs-lookup"><span data-stu-id="ce9fe-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="ce9fe-107">Pokud se rozhodnete požadovat více schvalovatelů sestav výdajů, můžete přidat prvky workflowu některým z následujících způsobů:</span><span class="sxs-lookup"><span data-stu-id="ce9fe-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="ce9fe-108">Přidáte jeden prvek schválení o jednom kroku.</span><span class="sxs-lookup"><span data-stu-id="ce9fe-108">Add one approval element that has one step.</span></span> <span data-ttu-id="ce9fe-109">Krok může například vyžadovat, aby bylo vyúčtování výdajů přiřazeno do skupiny uživatelů a aby bylo schváleno 50 procenty členů skupiny uživatelů.</span><span class="sxs-lookup"><span data-stu-id="ce9fe-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="ce9fe-110">Přidáte jeden prvek s více kroky.</span><span class="sxs-lookup"><span data-stu-id="ce9fe-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="ce9fe-111">Prvek schválení může například obsahovat následující kroky:</span><span class="sxs-lookup"><span data-stu-id="ce9fe-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="ce9fe-112">Manažer zaměstnance, který odeslal sestavu výdajů, toto vyúčtování schválí.</span><span class="sxs-lookup"><span data-stu-id="ce9fe-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="ce9fe-113">Úředník závazků ověří účtenky a položky sestavy výdajů.</span><span class="sxs-lookup"><span data-stu-id="ce9fe-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="ce9fe-114">Vlastník rozpočtu schválí vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="ce9fe-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="ce9fe-115">Přidáte více prvků schválení, z nichž každý obsahuje jeden krok.</span><span class="sxs-lookup"><span data-stu-id="ce9fe-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="ce9fe-116">Například můžete přidat samostatný prvek schválení pro každý z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="ce9fe-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="ce9fe-117">Manažer zaměstnance schválí vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="ce9fe-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="ce9fe-118">Vlastník rozpočtu schválí vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="ce9fe-118">The budget owner approves the expense report.</span></span>
