---
title: Snížení počtu dnů u poplatků za odběr
description: Chcete-li omezit počet dní pro některý existující poplatek předplatného, můžete vytvořit novou transakci, v níž odeberete dobu, která již nadále nemá být součástí intervalu pro poplatek předplatného.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e8158c99d2447835f3656027fd73d7c22121536
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836079"
---
# <a name="reduce-the-days-on-subscription-fees"></a><span data-ttu-id="c0631-103">Snížení počtu dnů u poplatků za odběr</span><span class="sxs-lookup"><span data-stu-id="c0631-103">Reduce the days on subscription fees</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="c0631-104">Chcete-li omezit počet dní pro některý existující poplatek předplatného, můžete vytvořit novou transakci, v níž odeberete dobu, která již nadále nemá být součástí intervalu pro poplatek předplatného.</span><span class="sxs-lookup"><span data-stu-id="c0631-104">To reduce the number of days of an existing subscription fee, you can create a new transaction in which you remove the period of time that should no longer be part of the subscription fee interval.</span></span>

## <a name="reduce-the-days-on-a-subscription-fee"></a><span data-ttu-id="c0631-105">Omezení počtu dní pro poplatek předplatného</span><span class="sxs-lookup"><span data-stu-id="c0631-105">Reduce the days on a subscription fee</span></span>

1.  <span data-ttu-id="c0631-106">Klikněte na uzel **Řízení služeb** \> **Společné** \> **Servisní zakázky** \> **Všechny servisní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="c0631-106">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span> <span data-ttu-id="c0631-107">Vyberte předplatné služby a v podokně akcí klepněte na možnost **Poplatky za předplatné**</span><span class="sxs-lookup"><span data-stu-id="c0631-107">Select the service subscription, and on the Action Pane, click **Subscription fees**</span></span>

2.  <span data-ttu-id="c0631-108">V poli **Typ předplatného** vyberte **Dny omezení**.</span><span class="sxs-lookup"><span data-stu-id="c0631-108">In the **Subscription type** field, select **Reduction days**.</span></span>

3.  <span data-ttu-id="c0631-109">V poli **Od data** a **Do data** definujte interval kalendářních dat pro poplatek předplatného, který chcete z období pro poplatek předplatného odebrat, a poté klepněte na volbu **OK**.</span><span class="sxs-lookup"><span data-stu-id="c0631-109">Use the **From date** field and the **To date** fields to define the date interval of the subscription fee that you want to remove from the subscription fee period, and then click **OK**.</span></span>

<span data-ttu-id="c0631-110">Chcete-li zobrazit vytvořenou transakci, klepněte ve formuláři **Předplatné** na volbu **Poplatky za předplatné**.</span><span class="sxs-lookup"><span data-stu-id="c0631-110">To view the transaction that was created, in the **Subscription** form, click **Fee transactions**.</span></span>

## <a name="example"></a><span data-ttu-id="c0631-111">Příklad</span><span class="sxs-lookup"><span data-stu-id="c0631-111">Example</span></span>

<span data-ttu-id="c0631-112">Předpokládejme, že pro transakci předplatného je zadáno období 1. ledna až 31. ledna a že toto období má být omezeno o 10 dní. Vytvořte novou transakci s obdobím omezení 1. ledna až 10. ledna.</span><span class="sxs-lookup"><span data-stu-id="c0631-112">If a subscription transaction period runs from January 1 to January 31, and you want to reduce the period by 10 days, create a new transaction in which the reduction period is January 1 to January 10.</span></span> <span data-ttu-id="c0631-113">(Období omezení může mít rozsah například také 5. ledna až 15. ledna).</span><span class="sxs-lookup"><span data-stu-id="c0631-113">(The reduction period could also be January 5 to January 15, or any other ten day period).</span></span>

<span data-ttu-id="c0631-114">Pokud tedy proměnná **Od data** pro období omezení bude mít hodnotu 21. ledna (31 mínus 10), můžete pro proměnnou **Do data** nastavit libovolné datum po datu 31. ledna a z období transakce poplatku bude stále odebráno 10 dní.</span><span class="sxs-lookup"><span data-stu-id="c0631-114">Also, if the **From date** on the reduction period is January 21 (31 minus 10), you could set the **To date** to any date after January 31, and 10 days will still be removed from the fee transaction period.</span></span>

## <a name="see-also"></a><span data-ttu-id="c0631-115">Viz také</span><span class="sxs-lookup"><span data-stu-id="c0631-115">See also</span></span>

[<span data-ttu-id="c0631-116">Příklad dnů snížení</span><span class="sxs-lookup"><span data-stu-id="c0631-116">Reduction days example</span></span>](reduction-days-example.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]