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
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d27c5653d6305aad23142fa6f803134153661278
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441352"
---
# <a name="set-up-expense-types"></a><span data-ttu-id="dcb65-103">Nastavení typů výdajů</span><span class="sxs-lookup"><span data-stu-id="dcb65-103">Set up expense types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dcb65-104">Toto téma vysvětluje, jak nastavit typy výdajů v leasingu majetku.</span><span class="sxs-lookup"><span data-stu-id="dcb65-104">This topic explains how to set up expense types in Asset leasing.</span></span> <span data-ttu-id="dcb65-105">Náklady, které nejsou představovány harmonogramem plateb, jsou známy jako *výdajové náklady*.</span><span class="sxs-lookup"><span data-stu-id="dcb65-105">Costs that aren't represented by the payment schedule are known as *expense costs*.</span></span> <span data-ttu-id="dcb65-106">Mezi příklady těchto nákladů patří majetkové daně, náklady na údržbu společného prostoru a náklady na pojištění.</span><span class="sxs-lookup"><span data-stu-id="dcb65-106">Examples of these costs include property taxes, common area maintenance costs, and insurance expenses.</span></span>

## <a name="add-an-administrative-expense-type"></a><span data-ttu-id="dcb65-107">Přidání typu administrativních výdajů</span><span class="sxs-lookup"><span data-stu-id="dcb65-107">Add an administrative expense type</span></span>

1. <span data-ttu-id="dcb65-108">Přejděte na **Leasing majetku \> Nastavení \> Typy výdajů**.</span><span class="sxs-lookup"><span data-stu-id="dcb65-108">Go to **Asset leasing \> Setup \> Expense types**.</span></span>
2. <span data-ttu-id="dcb65-109">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="dcb65-109">Select **New**.</span></span>
3. <span data-ttu-id="dcb65-110">Do příslušných polí zadejte nový typ výdajů a popis.</span><span class="sxs-lookup"><span data-stu-id="dcb65-110">In the appropriate fields, enter the new expense type and a description.</span></span>

## <a name="assign-accounts-to-administrative-costs"></a><span data-ttu-id="dcb65-111">Přiřazení účtů administrativním nákladům</span><span class="sxs-lookup"><span data-stu-id="dcb65-111">Assign accounts to administrative costs</span></span>

<span data-ttu-id="dcb65-112">Dále byste měli přidružit účty k typům výdajů.</span><span class="sxs-lookup"><span data-stu-id="dcb65-112">Next, you should associate accounts with the expense types.</span></span> <span data-ttu-id="dcb65-113">Z těchto účtů bude proveden odpis, když budou zaúčtovány položky plánu výdajů.</span><span class="sxs-lookup"><span data-stu-id="dcb65-113">These accounts will be debited when expense schedule entries are posted.</span></span> <span data-ttu-id="dcb65-114">Ofsetový účet je specifikován na řádcích **Harmonogram plateb zachraňovacích nákladů** každého leasingu.</span><span class="sxs-lookup"><span data-stu-id="dcb65-114">The offset account is specified on the **Executory costs payment schedule** lines on each lease.</span></span>

1. <span data-ttu-id="dcb65-115">Přejděte do nabídky **Leasing majetku \> Nastavení \> Parametry leasingu majetku**.</span><span class="sxs-lookup"><span data-stu-id="dcb65-115">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="dcb65-116">Na kartě **Účty** na pevné záložce **zachraňovací náklady** v poli **Typ výdaje** vyberte typ výdaje.</span><span class="sxs-lookup"><span data-stu-id="dcb65-116">On the **Accounts** tab, on the **Executory costs** FastTab, in the **Expense type** field, select the expense type.</span></span>
3. <span data-ttu-id="dcb65-117">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="dcb65-117">Select **Add**.</span></span>
4. <span data-ttu-id="dcb65-118">V poli **Typ knihy** vyberte typ knihy, který má být propojen s administrativními náklady.</span><span class="sxs-lookup"><span data-stu-id="dcb65-118">In the **Book type** field, select the book type to link to the administrative costs.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dcb65-119">K jednomu výdajovému účtu lze připojit více typů knih.</span><span class="sxs-lookup"><span data-stu-id="dcb65-119">Multiple book types can be linked to the same expense account.</span></span>

5. <span data-ttu-id="dcb65-120">V poli **Kód účtu** zadejte, na které leasingy by se kniha měla vztahovat:</span><span class="sxs-lookup"><span data-stu-id="dcb65-120">In the **Account code** field, specify which leases the book should be applied to:</span></span>

    - <span data-ttu-id="dcb65-121">**Vše** - Aplikuje knihu pro všechny leasingy.</span><span class="sxs-lookup"><span data-stu-id="dcb65-121">**All** – Apply the book to all leases.</span></span>
    - <span data-ttu-id="dcb65-122">**Skupina** - Aplikuje knihu na konkrétní skupinu leasingů.</span><span class="sxs-lookup"><span data-stu-id="dcb65-122">**Group** – Apply the book to a specific group of leases.</span></span>
    - <span data-ttu-id="dcb65-123">**Tabulka** - Aplikuje knihu pro konkrétní leasingy.</span><span class="sxs-lookup"><span data-stu-id="dcb65-123">**Table** – Apply the book to specific leases.</span></span>

6. <span data-ttu-id="dcb65-124">Pokud jste vybrali **Skupina** nebo **Tabulka** v poli **Kód účtu**, vyberte číslo účtu nebo číslo skupiny v poli **Číslo účtu/skupiny**.</span><span class="sxs-lookup"><span data-stu-id="dcb65-124">If you selected **Group** or **Table** in the **Account code** field, select an account number or group number in the **Account/Group number** field.</span></span>
7. <span data-ttu-id="dcb65-125">V příslušných polích vyberte hlavní účet finančního leasingu a hlavní účet operativního leasingu.</span><span class="sxs-lookup"><span data-stu-id="dcb65-125">In the appropriate fields, select the finance lease main account and the operating lease main account.</span></span>

<span data-ttu-id="dcb65-126">Po dokončení těchto kroků můžete přidat výdaje prostřednictvím řádek **Harmonogram plateb exekutivních nákladů** na stránce **Podrobnosti o leasingu** vybraného leasingu.</span><span class="sxs-lookup"><span data-stu-id="dcb65-126">When you've completed these steps, you can add expenses through the **Executory costs payment schedule** lines on the **Lease details** page of a selected lease.</span></span> <span data-ttu-id="dcb65-127">Alternativně můžete přidat náklady při vytváření nového pronájmu.</span><span class="sxs-lookup"><span data-stu-id="dcb65-127">Alternatively, you can add expenses when you create a new lease.</span></span>
