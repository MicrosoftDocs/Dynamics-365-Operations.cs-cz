---
title: Výkon výpočtu daně ovlivňuje transakce
description: Toto téma poskytuje informace o řešení potíží, které souvisejí s výkonem výpočtu daně a jeho účinkem na transakce.
author: shtao
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 6fce4e2cb8c5507769533a875e23ccc4531abf51
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020132"
---
# <a name="tax-calculation-performance-affects-transactions"></a><span data-ttu-id="3bdb5-103">Výkon výpočtu daně ovlivňuje transakce</span><span class="sxs-lookup"><span data-stu-id="3bdb5-103">Tax calculation performance affects transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3bdb5-104">Někdy je transakce ovlivněna problémy s výkonem, které má výpočet daně.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-104">Sometimes, a transaction is affected by performance issues that tax calculation is having.</span></span> <span data-ttu-id="3bdb5-105">Chcete-li tento problém vyřešit, postupujte podle pokynů v následujících částech.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="review-the-transaction-line-count"></a><span data-ttu-id="3bdb5-106">Kontrola počtu řádků transakce</span><span class="sxs-lookup"><span data-stu-id="3bdb5-106">Review the transaction line count</span></span>

<span data-ttu-id="3bdb5-107">Určete, zda má transakce velký počet řádků (například více než několik set).</span><span class="sxs-lookup"><span data-stu-id="3bdb5-107">Determine whether the transaction has a large number of lines (for example, more than several hundred).</span></span> <span data-ttu-id="3bdb5-108">Pokud nemá, přejděte k další části.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-108">If it doesn't, move on to the next section.</span></span> <span data-ttu-id="3bdb5-109">Pokud má transakce několik stovek řádků, odložte výpočet daně.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-109">If the transaction does have several hundred lines, delay the tax calculation.</span></span> <span data-ttu-id="3bdb5-110">Další informace viz [Povolení výpočtu opožděné daně v denících](enable-delayed-tax-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="3bdb5-110">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span> 

<span data-ttu-id="3bdb5-111">Dále můžete určit, zda je splněna některá z následujících podmínek:</span><span class="sxs-lookup"><span data-stu-id="3bdb5-111">Next, you can determine whether any of the following conditions are met:</span></span>

- <span data-ttu-id="3bdb5-112">Dochází k transakcím importu z velkých souborů.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-112">There are import transactions from large files.</span></span>
- <span data-ttu-id="3bdb5-113">Více relací zpracovává stejnou transakci výpočtu daně současně.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-113">Multiple sessions process the same transaction tax calculation at the same time.</span></span>
- <span data-ttu-id="3bdb5-114">Transakce má více řádků a zobrazení se aktualizují v reálném čase.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-114">The transaction has multiple lines, and the views are updated in real time.</span></span> <span data-ttu-id="3bdb5-115">Například pole **Vypočítaná částka prodejní daně** na stránce **Hlavní deník** se aktualizuje v reálném čase při změně polí řádku.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-115">For example, the **Calculated sales tax amount** field on the **General journal** page is updated in real time when a line's fields are changed.</span></span>

   <span data-ttu-id="3bdb5-116">[![Pole Vypočítaná částka prodejní daně na stránce dokladu deníku](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="3bdb5-116">[![Calculated sales tax amount field on the Jounal voucher page](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span></span>

<span data-ttu-id="3bdb5-117">Pokud je některá z těchto podmínek splněna, odložte výpočet daně.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-117">If any of these conditions are met, delay the tax calculation.</span></span>

## <a name="review-the-call-stack"></a><span data-ttu-id="3bdb5-118">Kontrola zásobníku volání</span><span class="sxs-lookup"><span data-stu-id="3bdb5-118">Review the call stack</span></span>

<span data-ttu-id="3bdb5-119">Zkontrolujte zásobník volání a určete, zda je výpočet daně volán vícekrát.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-119">Review the call stack to determine whether tax calculation is called multiple times.</span></span> <span data-ttu-id="3bdb5-120">Pokud není, přejděte k další části.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-120">If it isn't, move on to the next section.</span></span> <span data-ttu-id="3bdb5-121">Pokud je zásobník volání volán vícekrát, postupujte podle těchto kroků a snižte počty výpočtu daně.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-121">If the call stack is called multiple times, follow these steps to help reduce the tax calculation times.</span></span>

1. <span data-ttu-id="3bdb5-122">Pokud deník zvažoval transakci, odložte výpočet daně.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-122">If the journal has considered the transaction, delay the tax calculation.</span></span> <span data-ttu-id="3bdb5-123">Další informace viz [Povolení výpočtu opožděné daně v denících](enable-delayed-tax-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="3bdb5-123">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span>
2. <span data-ttu-id="3bdb5-124">Pokud je transakcí nákupní objednávka a verze aplikace je pozdější než 10.0.15, můžete odložit výpočet daně až do konečného výpočtu povolením testování pro **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-124">If the transaction is a purchase order, and the application version is later than 10.0.15, you can delay the tax calculation until the final calculation by enabling the flighting for **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span></span>

## <a name="review-the-call-stack-timeline"></a><span data-ttu-id="3bdb5-125">Kontrola časové osy zásobníku volání</span><span class="sxs-lookup"><span data-stu-id="3bdb5-125">Review the call stack timeline</span></span>

<span data-ttu-id="3bdb5-126">Zkontrolujte časovou osu zásobníku volání a zjistěte, zda existují následující problémy.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-126">Review the call stack timeline to determine whether the following issues exist.</span></span> <span data-ttu-id="3bdb5-127">Pokud ano, povolte testování pro možnost **TaxUncommittedDoIsolateScopeFlighting**, abyste problém vyřešili.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-127">If they do, enable the flighting for **TaxUncommittedDoIsolateScopeFlighting** to fix the issue.</span></span>

- <span data-ttu-id="3bdb5-128">Transakce způsobí, že systém přestane reagovat, dokud relace neskončí.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-128">The transaction causes the system to stop responding until the session ends.</span></span> <span data-ttu-id="3bdb5-129">Transakce proto nemůže vypočítat výsledek daně.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-129">Therefore, the transaction can't calculate the tax result.</span></span> <span data-ttu-id="3bdb5-130">Následující obrázek ukazuje okno se zprávou „Relace skončila“, kterou obdržíte.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-130">The following illustration shows the "Session ended" message box that you receive.</span></span>

    <span data-ttu-id="3bdb5-131">[![Zpráva o skončení relace](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="3bdb5-131">[![Session ended message](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span></span>

- <span data-ttu-id="3bdb5-132">Metody **TaxUncommitted** trvají déle než jiné metody.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-132">The **TaxUncommitted** methods take more time than other methods.</span></span> <span data-ttu-id="3bdb5-133">Například na následujícím obrázku trvá metoda **TaxUncommitted::updateTaxUncommitted()** 43 347,42 sekundy, ale jiné metody trvají 0,09 sekundy.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-133">For example, in the following illustration, the **TaxUncommitted::updateTaxUncommitted()** method takes 43,347.42 seconds, but other methods take 0.09 seconds.</span></span>

    <span data-ttu-id="3bdb5-134">[![Trvání metod](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="3bdb5-134">[![Method durations](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span></span>

## <a name="customizing-and-calling-tax-calculation"></a><span data-ttu-id="3bdb5-135">Přizpůsobení a volání výpočtu daně</span><span class="sxs-lookup"><span data-stu-id="3bdb5-135">Customizing and calling tax calculation</span></span>

<span data-ttu-id="3bdb5-136">Když přizpůsobujete, nevolejte výpočet daně metodou **insert()** nebo **update()** pro každý řádek.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-136">When you customize, don't call tax calculation at the **insert()** or **update()** method for each line.</span></span> <span data-ttu-id="3bdb5-137">Výpočet daně by měl být vyvolán na úrovni transakce.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-137">Tax calculation should be called at the transaction level.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="3bdb5-138">Zjištění, zda existuje přizpůsobení</span><span class="sxs-lookup"><span data-stu-id="3bdb5-138">Determine whether customization exists</span></span>

<span data-ttu-id="3bdb5-139">Pokud jste dokončili kroky v předchozích částech, ale problém se vám nepodařilo vyřešit, zjistěte, zda existuje přizpůsobení.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-139">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="3bdb5-140">Pokud neexistuje žádné přizpůsobení, vytvořte požadavek na službu Microsoft pro další podporu.</span><span class="sxs-lookup"><span data-stu-id="3bdb5-140">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
