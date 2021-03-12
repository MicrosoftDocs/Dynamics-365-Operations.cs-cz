---
title: Nastavení typů výdajů
description: Toto téma vysvětluje, jak nastavit typy výdajů v leasingu majetku.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3ab31b16c6ae07466d7655832701e71092064fe1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969496"
---
# <a name="set-up-expense-types"></a><span data-ttu-id="97fee-103">Nastavení typů výdajů</span><span class="sxs-lookup"><span data-stu-id="97fee-103">Set up expense types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97fee-104">Toto téma vysvětluje, jak nastavit typy výdajů v leasingu majetku.</span><span class="sxs-lookup"><span data-stu-id="97fee-104">This topic explains how to set up expense types in Asset leasing.</span></span> <span data-ttu-id="97fee-105">Náklady, které nejsou představovány harmonogramem plateb, jsou známy jako *výdajové náklady*.</span><span class="sxs-lookup"><span data-stu-id="97fee-105">Costs that aren't represented by the payment schedule are known as *expense costs*.</span></span> <span data-ttu-id="97fee-106">Mezi příklady těchto nákladů patří majetkové daně, náklady na údržbu společného prostoru a náklady na pojištění.</span><span class="sxs-lookup"><span data-stu-id="97fee-106">Examples of these costs include property taxes, common area maintenance costs, and insurance expenses.</span></span>

## <a name="add-an-administrative-expense-type"></a><span data-ttu-id="97fee-107">Přidání typu administrativních výdajů</span><span class="sxs-lookup"><span data-stu-id="97fee-107">Add an administrative expense type</span></span>

1. <span data-ttu-id="97fee-108">Přejděte na **Leasing majetku \> Nastavení \> Typy výdajů**.</span><span class="sxs-lookup"><span data-stu-id="97fee-108">Go to **Asset leasing \> Setup \> Expense types**.</span></span>
2. <span data-ttu-id="97fee-109">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="97fee-109">Select **New**.</span></span>
3. <span data-ttu-id="97fee-110">Do příslušných polí zadejte nový typ výdajů a popis.</span><span class="sxs-lookup"><span data-stu-id="97fee-110">In the appropriate fields, enter the new expense type and a description.</span></span>

## <a name="assign-accounts-to-administrative-costs"></a><span data-ttu-id="97fee-111">Přiřazení účtů administrativním nákladům</span><span class="sxs-lookup"><span data-stu-id="97fee-111">Assign accounts to administrative costs</span></span>

<span data-ttu-id="97fee-112">Dále byste měli přidružit účty k typům výdajů.</span><span class="sxs-lookup"><span data-stu-id="97fee-112">Next, you should associate accounts with the expense types.</span></span> <span data-ttu-id="97fee-113">Z těchto účtů bude proveden odpis, když budou zaúčtovány položky plánu výdajů.</span><span class="sxs-lookup"><span data-stu-id="97fee-113">These accounts will be debited when expense schedule entries are posted.</span></span> <span data-ttu-id="97fee-114">Ofsetový účet je specifikován na řádcích **Harmonogram plateb zachraňovacích nákladů** každého leasingu.</span><span class="sxs-lookup"><span data-stu-id="97fee-114">The offset account is specified on the **Executory costs payment schedule** lines on each lease.</span></span>

1. <span data-ttu-id="97fee-115">Přejděte do nabídky **Leasing majetku \> Nastavení \> Parametry leasingu majetku**.</span><span class="sxs-lookup"><span data-stu-id="97fee-115">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="97fee-116">Na kartě **Účty** na pevné záložce **zachraňovací náklady** v poli **Typ výdaje** vyberte typ výdaje.</span><span class="sxs-lookup"><span data-stu-id="97fee-116">On the **Accounts** tab, on the **Executory costs** FastTab, in the **Expense type** field, select the expense type.</span></span>
3. <span data-ttu-id="97fee-117">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="97fee-117">Select **Add**.</span></span>
4. <span data-ttu-id="97fee-118">V poli **Typ knihy** vyberte typ knihy, který má být propojen s administrativními náklady.</span><span class="sxs-lookup"><span data-stu-id="97fee-118">In the **Book type** field, select the book type to link to the administrative costs.</span></span>

    > [!NOTE]
    > <span data-ttu-id="97fee-119">K jednomu výdajovému účtu lze připojit více typů knih.</span><span class="sxs-lookup"><span data-stu-id="97fee-119">Multiple book types can be linked to the same expense account.</span></span>

5. <span data-ttu-id="97fee-120">V poli **Kód účtu** zadejte, na které leasingy by se kniha měla vztahovat:</span><span class="sxs-lookup"><span data-stu-id="97fee-120">In the **Account code** field, specify which leases the book should be applied to:</span></span>

    - <span data-ttu-id="97fee-121">**Vše** - Aplikuje knihu pro všechny leasingy.</span><span class="sxs-lookup"><span data-stu-id="97fee-121">**All** – Apply the book to all leases.</span></span>
    - <span data-ttu-id="97fee-122">**Skupina** - Aplikuje knihu na konkrétní skupinu leasingů.</span><span class="sxs-lookup"><span data-stu-id="97fee-122">**Group** – Apply the book to a specific group of leases.</span></span>
    - <span data-ttu-id="97fee-123">**Tabulka** - Aplikuje knihu pro konkrétní leasingy.</span><span class="sxs-lookup"><span data-stu-id="97fee-123">**Table** – Apply the book to specific leases.</span></span>

6. <span data-ttu-id="97fee-124">Pokud jste vybrali **Skupina** nebo **Tabulka** v poli **Kód účtu**, vyberte číslo účtu nebo číslo skupiny v poli **Číslo účtu/skupiny**.</span><span class="sxs-lookup"><span data-stu-id="97fee-124">If you selected **Group** or **Table** in the **Account code** field, select an account number or group number in the **Account/Group number** field.</span></span>
7. <span data-ttu-id="97fee-125">V příslušných polích vyberte hlavní účet finančního leasingu a hlavní účet operativního leasingu.</span><span class="sxs-lookup"><span data-stu-id="97fee-125">In the appropriate fields, select the finance lease main account and the operating lease main account.</span></span>

<span data-ttu-id="97fee-126">Po dokončení těchto kroků můžete přidat výdaje prostřednictvím řádek **Harmonogram plateb exekutivních nákladů** na stránce **Podrobnosti o leasingu** vybraného leasingu.</span><span class="sxs-lookup"><span data-stu-id="97fee-126">When you've completed these steps, you can add expenses through the **Executory costs payment schedule** lines on the **Lease details** page of a selected lease.</span></span> <span data-ttu-id="97fee-127">Alternativně můžete přidat náklady při vytváření nového pronájmu.</span><span class="sxs-lookup"><span data-stu-id="97fee-127">Alternatively, you can add expenses when you create a new lease.</span></span>