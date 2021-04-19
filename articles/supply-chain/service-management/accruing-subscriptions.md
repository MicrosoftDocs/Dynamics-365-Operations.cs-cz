---
title: Časové rozlišení předplatného
description: U předplatného servisu ručně rozlišujete výnosy do období následujících po datu, kdy jste fakturovali transakci poplatku.
author: ShylaThompson
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d6f2f69b7093e5408b016f4a69792b28c70f57f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824671"
---
# <a name="accruing-subscriptions"></a><span data-ttu-id="387c9-103">Časové rozlišení předplatného</span><span class="sxs-lookup"><span data-stu-id="387c9-103">Accruing subscriptions</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="387c9-104">U předplatného servisu ručně rozlišujete výnosy do období následujících po datu, kdy jste fakturovali transakci poplatku.</span><span class="sxs-lookup"><span data-stu-id="387c9-104">With service subscriptions, you manually accrue revenue in the periods following the date when you invoiced a fee transaction.</span></span>

<span data-ttu-id="387c9-105">Období časového rozlišení jsou vytvořena pro pro fakturační období, které jste nastavili pro poplatek předplatného, a jsou založena na kódu období předplatného.</span><span class="sxs-lookup"><span data-stu-id="387c9-105">Accrual periods are created for the invoice period that you set up for the subscription fee, and the accrual periods are based on the period code of the subscription.</span></span>

<span data-ttu-id="387c9-106">Můžete provádět časové rozlišení a stornovat časově rozlišené výnosy.</span><span class="sxs-lookup"><span data-stu-id="387c9-106">You can accrue and reverse accrued revenue.</span></span>

## <a name="reverse-accruals-of-credit-amounts"></a><span data-ttu-id="387c9-107">Stornovat časové rozlišení v částkách kreditu</span><span class="sxs-lookup"><span data-stu-id="387c9-107">Reverse accruals of credit amounts</span></span>

<span data-ttu-id="387c9-108">Při připsání fakturovaných částek předplatného na stranu Dal můžete použít dvě metody stornování časově rozlišených částek:</span><span class="sxs-lookup"><span data-stu-id="387c9-108">If you credit invoiced subscription amounts, you can use two methods to reverse the accrual amounts:</span></span>

  - <span data-ttu-id="387c9-109">Před vytvořením návrhu dobropisu pro transakci můžete stornovat každou transakci časového rozlišení výnosů zvlášť.</span><span class="sxs-lookup"><span data-stu-id="387c9-109">You can reverse each accrued revenue transaction individually before you create the credit note proposal for the transaction.</span></span> <span data-ttu-id="387c9-110">Toto je ruční metoda.</span><span class="sxs-lookup"><span data-stu-id="387c9-110">This is the manual method.</span></span> <span data-ttu-id="387c9-111">(ruční)</span><span class="sxs-lookup"><span data-stu-id="387c9-111">(manual)</span></span>

  - <span data-ttu-id="387c9-112">Můžete časově rozlišené částky stornovat k datu zaúčtování dobropisu nebo k původnímu datu zaúčtování časového rozlišení.</span><span class="sxs-lookup"><span data-stu-id="387c9-112">You can have the accrued amounts reversed on the date where the credit note is posted or on the original posting date of the accrual.</span></span>

<span data-ttu-id="387c9-113">Další informace naleznete v tématu [Parametry předplatného (formulář)](https://technet.microsoft.com/library/aa619615.aspx).</span><span class="sxs-lookup"><span data-stu-id="387c9-113">For more information, see [Subscription parameters (form)](https://technet.microsoft.com/library/aa619615.aspx).</span></span>

## <a name="setup-requirements"></a><span data-ttu-id="387c9-114">Nastavit požadavky</span><span class="sxs-lookup"><span data-stu-id="387c9-114">Setup requirements</span></span>

<span data-ttu-id="387c9-115">Chcete-li časově rozlišovat výnosy, ověřte, zda jsou splněny následující datové požadavky:</span><span class="sxs-lookup"><span data-stu-id="387c9-115">To accrue revenue, make sure that the following data requirements are met:</span></span>

## <a name="account-setup"></a><span data-ttu-id="387c9-116">Nastavení účtu</span><span class="sxs-lookup"><span data-stu-id="387c9-116">Account setup</span></span>

<span data-ttu-id="387c9-117">V modulu **Project** musí být nastaveny účty **Časově rozlišený výnos – předplatné** a **NV – předplatné**.</span><span class="sxs-lookup"><span data-stu-id="387c9-117">The **WIP - subscription** and the **Accrued revenue - subscription** accounts must be set up in the **Project** module.</span></span>

<span data-ttu-id="387c9-118">Při zaúčtování časově rozlišeného výnosu se časově rozlišená částka připíše na stranu MD účtu **Nedokončená výroba - předplatné** a časově rozlišená částka na stranu Dal účtu **Časově rozlišené výnosy – předplatné**.</span><span class="sxs-lookup"><span data-stu-id="387c9-118">When you post accrued revenue, the **WIP - subscription** account is debited with the accrual amount, and the **Accrued revenue - subscription** account is credited with the accrual amount.</span></span>

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a><span data-ttu-id="387c9-119">Nastavení účtů pro časové rozlišení výnosu předplatného</span><span class="sxs-lookup"><span data-stu-id="387c9-119">Set up accounts for accrual of subscription revenue</span></span>

1.  <span data-ttu-id="387c9-120">Klepněte na tlačítko **Řízení a účetnictví projektu** \> **Nastavení** \> **Zaúčtování** \> **Nastavení zaúčtování v hlavní knize**.</span><span class="sxs-lookup"><span data-stu-id="387c9-120">Click **Project management and accounting** \> **Setup** \> **Posting** \> **Ledger posting setup**.</span></span>

2.  <span data-ttu-id="387c9-121">Klepněte na kartu **Výnosové účty** a vyberte **nedokončená výroba – předplatné** nebo **časově rozlišené výnosy – předplatné** k nastavení účtů.</span><span class="sxs-lookup"><span data-stu-id="387c9-121">Click the **Revenue accounts** tab, and select **WIP - subscription** or **Accrued revenue - subscription** to set up the accounts.</span></span>

## <a name="subscription-group-setup"></a><span data-ttu-id="387c9-122">Nastavení skupiny předplatného</span><span class="sxs-lookup"><span data-stu-id="387c9-122">Subscription group setup</span></span>

<span data-ttu-id="387c9-123">Aby bylo možné časově rozlišovat výnosy předplatného, musí být zaškrtnuto políčko **časově rozlišené výnosy**.</span><span class="sxs-lookup"><span data-stu-id="387c9-123">To be able to accrue revenue for subscriptions, the **Accrue revenue** check box must be selected.</span></span> <span data-ttu-id="387c9-124">Nachází se ve formuláři **skupiny předplatného** skupiny, která je připojena k předplatnému.</span><span class="sxs-lookup"><span data-stu-id="387c9-124">This is found on the **Subscription groups** form for the group that is attached to the subscription.</span></span> <span data-ttu-id="387c9-125">Klikněte na uzel **Řízení služeb** \> **Nastavení** \> **Servisní zakázky** \> **Skupiny předplatného**.</span><span class="sxs-lookup"><span data-stu-id="387c9-125">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="enable-revenue-accrual-on-a-subscription-group"></a><span data-ttu-id="387c9-126">Povolení časového rozlišení výnosů u skupiny předplatného</span><span class="sxs-lookup"><span data-stu-id="387c9-126">Enable revenue accrual on a subscription group</span></span>

1.  <span data-ttu-id="387c9-127">Klikněte na uzel **Řízení služeb** \> **Nastavení** \> **Servisní zakázky** \> **Skupiny předplatného**.</span><span class="sxs-lookup"><span data-stu-id="387c9-127">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="periods"></a><span data-ttu-id="387c9-128">Období</span><span class="sxs-lookup"><span data-stu-id="387c9-128">Periods</span></span>

<span data-ttu-id="387c9-129">Musíte nastavit kód fakturačního období.</span><span class="sxs-lookup"><span data-stu-id="387c9-129">You must set up an invoicing period code.</span></span> <span data-ttu-id="387c9-130">Pokud nechcete časově rozlišovat výnosy ve stejných časových obdobích, která používáte k fakturaci, musíte rovněž nastavit období časového rozlišení.</span><span class="sxs-lookup"><span data-stu-id="387c9-130">Unless you want to accrue revenue in the same time intervals as you use for invoicing, you must also set up an accrual period.</span></span>

<span data-ttu-id="387c9-131">V následující tabulce získáte přehled o možných obdobích časového rozlišení, která lze nastavit pro různá fakturační období:</span><span class="sxs-lookup"><span data-stu-id="387c9-131">The following table provides an overview of which accrual periods can be set up for each invoicing period:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="387c9-132">Fakturační období</span><span class="sxs-lookup"><span data-stu-id="387c9-132">Invoicing period</span></span></p></th>
<th><p><span data-ttu-id="387c9-133">Období časového rozlišení</span><span class="sxs-lookup"><span data-stu-id="387c9-133">Accrual period</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="387c9-134"><strong>Roky</strong></span><span class="sxs-lookup"><span data-stu-id="387c9-134"><strong>Years</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="387c9-135"><strong>Roky</strong></span><span class="sxs-lookup"><span data-stu-id="387c9-135"><strong>Years</strong></span></span></p></li>
<li><p><span data-ttu-id="387c9-136"><strong>Čtvrtletí</strong></span><span class="sxs-lookup"><span data-stu-id="387c9-136"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="387c9-137"><strong>Měsíc</strong></span><span class="sxs-lookup"><span data-stu-id="387c9-137"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="387c9-138"><strong>Den</strong></span><span class="sxs-lookup"><span data-stu-id="387c9-138"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="387c9-139"><strong>Čtvrtletí</strong></span><span class="sxs-lookup"><span data-stu-id="387c9-139"><strong>Quarter</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="387c9-140"><strong>Čtvrtletí</strong></span><span class="sxs-lookup"><span data-stu-id="387c9-140"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="387c9-141"><strong>Měsíc</strong></span><span class="sxs-lookup"><span data-stu-id="387c9-141"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="387c9-142"><strong>Den</strong></span><span class="sxs-lookup"><span data-stu-id="387c9-142"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="387c9-143"><strong>Měsíc</strong></span><span class="sxs-lookup"><span data-stu-id="387c9-143"><strong>Month</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="387c9-144"><strong>Měsíc</strong></span><span class="sxs-lookup"><span data-stu-id="387c9-144"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="387c9-145"><strong>Den</strong></span><span class="sxs-lookup"><span data-stu-id="387c9-145"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="387c9-146"><strong>Týden</strong></span><span class="sxs-lookup"><span data-stu-id="387c9-146"><strong>Week</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="387c9-147"><strong>Den</strong></span><span class="sxs-lookup"><span data-stu-id="387c9-147"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="387c9-148"><strong>Den</strong></span><span class="sxs-lookup"><span data-stu-id="387c9-148"><strong>Day</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="387c9-149"><strong>Den</strong></span><span class="sxs-lookup"><span data-stu-id="387c9-149"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="387c9-150">Nastavení fakturačního období je povinnou součástí celého nastavení skupiny předplatného.</span><span class="sxs-lookup"><span data-stu-id="387c9-150">Setting up the invoicing period is a mandatory part of the overall subscription group setup.</span></span> <span data-ttu-id="387c9-151">Můžete se rozhodnout, zda chcete také nastavit období časového rozlišení pro skupinu předplatného.</span><span class="sxs-lookup"><span data-stu-id="387c9-151">You can decide whether to also set up an accrual period for the subscription group.</span></span> <span data-ttu-id="387c9-152">Pokud nastavíte období časového rozlišení pro skupinu předplatného ,je toto období navrženo v poli **Kód období**.</span><span class="sxs-lookup"><span data-stu-id="387c9-152">If you set up an accrual period for the subscription group, this period is suggested in the **Period code** field.</span></span> <span data-ttu-id="387c9-153">Toto pole se nachází ve formuláři **časově rozlišené výnosy předplatného** při časovém rozlišení výnosů předplatného.</span><span class="sxs-lookup"><span data-stu-id="387c9-153">This field is found in the **Accrue subscription revenue** form, when you accrue subscription revenue.</span></span> <span data-ttu-id="387c9-154">Období časového rozlišení je však nepovinná informace o skupině předplatného.</span><span class="sxs-lookup"><span data-stu-id="387c9-154">However, the accrual period is optional information about the subscription group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="387c9-155">K otevření formuláře <STRONG>Časové rozlišení předplatného</STRONG> použijte následující cestu.</span><span class="sxs-lookup"><span data-stu-id="387c9-155">Use the following path to open the <STRONG>Accrue subscription revenue</STRONG> form.</span></span> <span data-ttu-id="387c9-156">Klikněte na uzel <STRONG>Řízení služeb</STRONG> &gt; <STRONG>Pravidelné</STRONG> &gt; <STRONG>Servisní odběry</STRONG> &gt; <STRONG>Všechna předplatná služby</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="387c9-156">Click <STRONG>Service management</STRONG> &gt; <STRONG>Periodic</STRONG> &gt; <STRONG>Service subscriptions</STRONG> &gt; <STRONG>Accrue subscription revenue</STRONG>.</span></span></P>


## <a name="transactions"></a><span data-ttu-id="387c9-157">Transakce</span><span class="sxs-lookup"><span data-stu-id="387c9-157">Transactions</span></span>

<span data-ttu-id="387c9-158">Můžete určit počet transakcí hlavní knihy, které jsou vytvořeny při zaúčtování časově rozlišeného výnosu.</span><span class="sxs-lookup"><span data-stu-id="387c9-158">You can control the number of ledger transactions that are created when you post accrued revenue.</span></span> <span data-ttu-id="387c9-159">U předplatného definujte, zda transakce hlavní knihy mají být vytvořeny jako celek nebo podle řádku.</span><span class="sxs-lookup"><span data-stu-id="387c9-159">On subscriptions, define if the ledger transactions should be created as a total or per line.</span></span>

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a><span data-ttu-id="387c9-160">Určení úrovně zobrazovaných podrobností o zaúčtování pro časově rozlišené transakce</span><span class="sxs-lookup"><span data-stu-id="387c9-160">Specify the level of posting details to display for accrued transactions</span></span>

1.  <span data-ttu-id="387c9-161">Klikněte na **Řízení a účetnictví projektů** \> **Nastavení** \> **Parametry modulu Řízení a účetnictví projektu**.</span><span class="sxs-lookup"><span data-stu-id="387c9-161">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="387c9-162">Na kartě **Finanční** v poli **Faktura** vyberte **Celkem** nebo **řádek**.</span><span class="sxs-lookup"><span data-stu-id="387c9-162">On the **Financial** tab, in the **Invoice** field, select **Total** or **Line**.</span></span>


## <a name="see-also"></a><span data-ttu-id="387c9-163">Viz také</span><span class="sxs-lookup"><span data-stu-id="387c9-163">See also</span></span>

[<span data-ttu-id="387c9-164">Časově rozlišit výnosy z předplatného</span><span class="sxs-lookup"><span data-stu-id="387c9-164">Accrue subscription revenue</span></span>](accrue-subscription-revenue.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]