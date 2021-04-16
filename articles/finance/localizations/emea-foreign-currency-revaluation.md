---
title: Přecenění cizí měny pro bankovní účty
description: Toto téma obsahuje informace o přecenění cizí měny pro bankovní účty.
author: panolte
ms.date: 03/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 11464
ms.search.region: Czech Republic, Estonia, Latvia, Lithuania, Poland
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 00ddba2ddc9351590e16b167cc0be06ba89cc377
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826095"
---
# <a name="foreign-currency-revaluation-for-bank-accounts"></a><span data-ttu-id="d3b32-103">Přecenění cizí měny pro bankovní účty</span><span class="sxs-lookup"><span data-stu-id="d3b32-103">Foreign currency revaluation for bank accounts</span></span>

[!include [banner](../includes/banner.md)]

## <a name="revalue-foreign-currency-amounts-for-bank-account-transactions"></a><span data-ttu-id="d3b32-104">Přecenění částek v cizí měně pro transakce bankovního účtu</span><span class="sxs-lookup"><span data-stu-id="d3b32-104">Revalue foreign currency amounts for bank account transactions</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3b32-105">Tato část se vztahuje pouze na právnické osoby, které mají primární adresu v Polsku.</span><span class="sxs-lookup"><span data-stu-id="d3b32-105">This section applies only to legal entities that have a primary address in Poland.</span></span>

<span data-ttu-id="d3b32-106">Přecenění částek v cizí měně můžete provést pro bankovní transakce.</span><span class="sxs-lookup"><span data-stu-id="d3b32-106">You can revalue foreign currency amounts for bank transactions.</span></span> <span data-ttu-id="d3b32-107">Poté můžete vytvořit sestavu pro zobrazení bankovních transakcí, které mají úpravy pro přecenění cizí měny.</span><span class="sxs-lookup"><span data-stu-id="d3b32-107">You can then create a report to view the bank transactions that have adjustments for foreign currency revaluations.</span></span>

1. <span data-ttu-id="d3b32-108">Vyberte **Řízení hotovosti a banky** &gt; **pravidelné úlohy** &gt; **Banka - kurzové vyrovnání (FIFO/LIFO)**.</span><span class="sxs-lookup"><span data-stu-id="d3b32-108">Select **Cash and bank management** &gt; **Periodic tasks** &gt; **Bank - Exchange adjustment (FIFO/LIFO)**.</span></span>
2. <span data-ttu-id="d3b32-109">Do pole **K datu** zadejte koncové datum přecenění.</span><span class="sxs-lookup"><span data-stu-id="d3b32-109">In the **On date** field, enter an end date for the revaluation.</span></span> <span data-ttu-id="d3b32-110">Výpočet zahrnuje pouze transakce s datem, které je před zadaným datem.</span><span class="sxs-lookup"><span data-stu-id="d3b32-110">The calculation includes only transactions that have a date that is before the specified date.</span></span>
3. <span data-ttu-id="d3b32-111">Vyberte **záznamy, které chcete zahrnout** &gt; **filtr** &gt; **přidat** k přidání bankovního účtu.</span><span class="sxs-lookup"><span data-stu-id="d3b32-111">Select **Records to include** &gt; **Filter** &gt; **Add** to add a bank account.</span></span> <span data-ttu-id="d3b32-112">Pokud nezadáte bankovní účet, jsou přeceněny částky pro všechny bankovní účty.</span><span class="sxs-lookup"><span data-stu-id="d3b32-112">If you don't specify a bank account, amounts are revalued for all bank accounts.</span></span>
4. <span data-ttu-id="d3b32-113">Vyberte **OK** a stránku dotazu zavřete.</span><span class="sxs-lookup"><span data-stu-id="d3b32-113">Select **OK** to close the query page.</span></span>
5. <span data-ttu-id="d3b32-114">Na stránce **Přecenění cizí měny** zaškrtněte políčko **Přepočet** k přecenění částek v cizí měně pro všechna otevřená období.</span><span class="sxs-lookup"><span data-stu-id="d3b32-114">On the **Foreign currency revaluation** page, select the **Recalculation** check box to revalue foreign currency amounts for all open periods.</span></span>

## <a name="create-a-report-to-view-bank-transactions-that-have-adjustments-for-foreign-currency-revaluations"></a><span data-ttu-id="d3b32-115">Vytvořte sestavu pro zobrazení bankovních transakcí, které mají úpravy pro přecenění cizí měny.</span><span class="sxs-lookup"><span data-stu-id="d3b32-115">Create a report to view bank transactions that have adjustments for foreign currency revaluations</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3b32-116">Tato část se vztahuje pouze na právnické osoby, které mají primární adresu v Polsku.</span><span class="sxs-lookup"><span data-stu-id="d3b32-116">This section applies only to legal entities that have a primary address in Poland.</span></span>

1. <span data-ttu-id="d3b32-117">Vyberte **řízení hotovosti a banky** &gt; **dotazy a sestavy** &gt; **banka – sestava kurzového vyrovnání**.</span><span class="sxs-lookup"><span data-stu-id="d3b32-117">Select **Cash and bank management** &gt; **Inquiries and reports** &gt; **Bank - Exchange adjustment report**.</span></span>
2. <span data-ttu-id="d3b32-118">Vyberte **záznamy, které chcete zahrnout** &gt; **filtr** k vyhledání jednoho nebo více bankovních účtů, pro které mají být zobrazeny údaje.</span><span class="sxs-lookup"><span data-stu-id="d3b32-118">Select **Records to include** &gt; **Filter** to find one or more bank accounts to view information for.</span></span>
3. <span data-ttu-id="d3b32-119">Volitelné: V poli **Bankovní účet** vyberte bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="d3b32-119">Optional: In the **Bank account** field, select a bank account.</span></span> <span data-ttu-id="d3b32-120">Pokud toto pole ponecháte prázdné, bude sestava zahrnovat podrobnosti bankovních transakcí pro všechny bankovní účty.</span><span class="sxs-lookup"><span data-stu-id="d3b32-120">If you leave this field blank, the report includes bank transaction details for all bank accounts.</span></span>
4. <span data-ttu-id="d3b32-121">Klepnutím na tlačítko **OK** sestavu vygenerujte.</span><span class="sxs-lookup"><span data-stu-id="d3b32-121">Select **OK** to generate the report.</span></span> 

## <a name="calculate-exchange-rate-adjustments-for-bank-account-transactions"></a><span data-ttu-id="d3b32-122">Výpočet vyrovnání kurzových rozdílů pro transakce bankovního účtu</span><span class="sxs-lookup"><span data-stu-id="d3b32-122">Calculate exchange rate adjustments for bank account transactions</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3b32-123">Tato část se vztahuje pouze na právnické osoby, které mají primární adresu v České republice, Estonsku, Litvě nebo Lotyšsku.</span><span class="sxs-lookup"><span data-stu-id="d3b32-123">This section applies only to legal entities that have a primary address in the Czech Republic, Estonia, Lithuania, or Latvia.</span></span>

<span data-ttu-id="d3b32-124">Musíte přecenit a upravit bankovní účty, pokud je mezi zúčtovací měnou a měnou vykazování rozdíl směnného kurzu.</span><span class="sxs-lookup"><span data-stu-id="d3b32-124">You must revalue and adjust bank accounts if there is a difference in the exchange rate between the accounting currency and the reporting currency.</span></span> <span data-ttu-id="d3b32-125">Pomocí této úlohy můžete vypočítat správný zůstatek ve zúčtovací měně a v měně pro vykazování pro bankovní účty.</span><span class="sxs-lookup"><span data-stu-id="d3b32-125">This task helps you calculate the correct balance in both the accounting currency and the reporting currency for the bank accounts.</span></span>

1. <span data-ttu-id="d3b32-126">Přejděte do nabídky **Pokladna a banka** &gt; **Nastavení** &gt; **Parametry pokladny a banky**.</span><span class="sxs-lookup"><span data-stu-id="d3b32-126">Select **Cash and bank management** &gt; **Setup** &gt; **Cash and bank management parameters**.</span></span>
2. <span data-ttu-id="d3b32-127">Na kartě **Číselné řady** v poli **Reference** vyberte číselnou řadu pro referenci **Banka - úprava cizí měny**.</span><span class="sxs-lookup"><span data-stu-id="d3b32-127">On the **Number sequences** tab, in the **Reference** field, select a number sequence for the **Bank - Exchange adjustment** reference.</span></span>
3. <span data-ttu-id="d3b32-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d3b32-128">Close the page.</span></span>
4. <span data-ttu-id="d3b32-129">Vyberte **hlavní kniha** &gt; **nastavení** &gt; **měna** &gt; **směnné kurzy**.</span><span class="sxs-lookup"><span data-stu-id="d3b32-129">Select **General ledger** &gt; **Setup** &gt; **Currency** &gt; **Currency exchange rates**.</span></span> <span data-ttu-id="d3b32-130">Na stránce **Směnné kurzy v měně** můžete definovat směnný kurz mezi dvěma měnami nebo párem měn.</span><span class="sxs-lookup"><span data-stu-id="d3b32-130">On the **Currency exchange rates** page, you can define the exchange rate between two currencies or a currency pair.</span></span>
5. <span data-ttu-id="d3b32-131">Po skončení stránku zavřete.</span><span class="sxs-lookup"><span data-stu-id="d3b32-131">When you've finished, close the page.</span></span>
6. <span data-ttu-id="d3b32-132">Vyberte **hlavní kniha** &gt; **nastavení** &gt; **Hlavní kniha**.</span><span class="sxs-lookup"><span data-stu-id="d3b32-132">Select **General ledger** &gt; **Setup** &gt; **Ledger**.</span></span> <span data-ttu-id="d3b32-133">V polích **Nerealizované zisky** a **Nerealizované ztráty** vyberte hlavní účet, pro který jsou zaúčtovány směnné kurzy.</span><span class="sxs-lookup"><span data-stu-id="d3b32-133">In the **Unrealized gain** and **Unrealized loss** fields, select the main account that the exchange rates are posted for.</span></span>
7. <span data-ttu-id="d3b32-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d3b32-134">Close the page.</span></span>
8. <span data-ttu-id="d3b32-135">Vyberte **řízení hotovosti a banky** &gt; **pravidelné úlohy** &gt; **přecenění cizí měny**.</span><span class="sxs-lookup"><span data-stu-id="d3b32-135">Select **Cash and bank management** &gt; **Periodic tasks** &gt; **Foreign currency revaluation**.</span></span>
9. <span data-ttu-id="d3b32-136">V poli **K datu** vyberte datum přecenění nebo datum úpravy.</span><span class="sxs-lookup"><span data-stu-id="d3b32-136">In the **On date** field, select the revaluation date or adjustment date.</span></span>
10. <span data-ttu-id="d3b32-137">V **od měny** vyberte aktuální kód měny.</span><span class="sxs-lookup"><span data-stu-id="d3b32-137">In the **From currency** field, select the current currency code.</span></span> <span data-ttu-id="d3b32-138">V poli **Do měny** vyberte měnu, ve které se mají provádět úpravy.</span><span class="sxs-lookup"><span data-stu-id="d3b32-138">In the **To currency** field, select the currency that the adjustment should be made to.</span></span>
11. <span data-ttu-id="d3b32-139">Vyberte **záznamy, které chcete zahrnout** &gt; **filtr** bankovního účtu, a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d3b32-139">Select **Records to include** &gt; **Filter** to find the bank account, and then select **OK**.</span></span>
12. <span data-ttu-id="d3b32-140">Na stránce **přecenění cizí měny** vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d3b32-140">On the **Foreign currency revaluation** page, select **OK**.</span></span> <span data-ttu-id="d3b32-141">Vypočítá se úprava transakcí bankovního účtu ve vybraném datu.</span><span class="sxs-lookup"><span data-stu-id="d3b32-141">The adjustment for the bank account transactions on the selected date is calculated.</span></span>

> [!NOTE]
> <span data-ttu-id="d3b32-142">V hlavní knize můžete zobrazit dvě samostatné transakce: jednu pro zúčtovací měnu a druhou pro měnu vykazování.</span><span class="sxs-lookup"><span data-stu-id="d3b32-142">In the general ledger, you can view two separate transactions: one for the accounting currency and one for the reporting currency.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]