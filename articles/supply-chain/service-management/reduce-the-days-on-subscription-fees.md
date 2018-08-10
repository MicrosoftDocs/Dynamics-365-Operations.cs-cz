---
title: "Snížení počtu dnů u poplatků za odběr"
description: "Chcete-li omezit počet dní pro některý existující poplatek předplatného, můžete vytvořit novou transakci, v níž odeberete dobu, která již nadále nemá být součástí intervalu pro poplatek předplatného."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c70e393c125eecef85e8711d1635250f5ff408d9
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---


# <a name="reduce-the-days-on-subscription-fees"></a>Snížení počtu dnů u poplatků za odběr 

[!include [banner](../includes/banner.md)]


Chcete-li omezit počet dní pro některý existující poplatek předplatného, můžete vytvořit novou transakci, v níž odeberete dobu, která již nadále nemá být součástí intervalu pro poplatek předplatného.

## <a name="reduce-the-days-on-a-subscription-fee"></a>Omezení počtu dní pro poplatek předplatného

1.  Klikněte na uzel **Řízení služeb** \> **Společné** \> **Servisní zakázky** \> **Všechny servisní zakázky**. Vyberte předplatné služby a v podokně akcí klepněte na možnost **Poplatky za předplatné**

2.  V poli **Typ předplatného** vyberte **Dny omezení**.

3.  V poli **Od data** a **Do data** definujte interval kalendářních dat pro poplatek předplatného, který chcete z období pro poplatek předplatného odebrat, a poté klepněte na volbu **OK**.

Chcete-li zobrazit vytvořenou transakci, klepněte ve formuláři **Předplatné** na volbu **Poplatky za předplatné**.

## <a name="example"></a>Příklad

Předpokládejme, že pro transakci předplatného je zadáno období 1. ledna až 31. ledna a že toto období má být omezeno o 10 dní. Vytvořte novou transakci s obdobím omezení 1. ledna až 10. ledna. (Období omezení může mít rozsah například také 5. ledna až 15. ledna).

Pokud tedy proměnná **Od data** pro období omezení bude mít hodnotu 21. ledna (31 mínus 10), můžete pro proměnnou **Do data** nastavit libovolné datum po datu 31. ledna a z období transakce poplatku bude stále odebráno 10 dní.

## <a name="see-also"></a>Viz také

[Příklad dnů snížení](reduction-days-example.md)

  



