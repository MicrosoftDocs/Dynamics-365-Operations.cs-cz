--- 
title: "Přiřazení stavu životního cyklu produktu k uvolněnému hlavnímu produktu"
description: "Tento postup ukazuje, jak přiřadit k uvolněnému produktu a jeho variantám stav životního cyklu produktu."
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d445ea2f2362f146a1e3e7bcf747898dc2cc89ba
ms.openlocfilehash: f476c1b2585ce0b5b67cd0d91684c86f7d3bda36
ms.contentlocale: cs-cz
ms.lasthandoff: 02/08/2018

---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a>Přiřazení stavu životního cyklu produktu k uvolněnému hlavnímu produktu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup ukazuje, jak přiřadit k uvolněnému produktu a jeho variantám stav životního cyklu produktu. Předpoklad: Nejprve je nutné přehrát Průvodce záznamem úloh Vytvoření nového stavu cyklu životnosti produktu pro zajištění, že je vytvořen nejméně jeden stav životního cyklu produktu před přehráním tohoto průvodce záznamem úloh.


## <a name="find-a-released-product-master"></a>Najděte uvolněný základní produkt.
1. Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.

> [!NOTE]
> Základní produkt má podtyp produktu Základní produkt.  

## <a name="update-the-lifecycle-state"></a>Aktualizace stavu životního cyklu
1. Klikněte na položku Upravit.
2. V poli Stav cyklu životnosti produktu zadejte nebo vyberte hodnotu.
3. Klikněte na položku Uložit.
4. Klepněte na tlačítko Ano.

> [!NOTE]
> Pokud je vybrána možnost Ano, budou mít všechny související varianty uvolněného produktu, které mají stejný původní stav jako vydaný hlavní produkt, také aktualizovány na nový stav životního cyklu produktu. Pokud je vybraná možnost Ne, budou mít všechny varianty svůj stávající stav. Varianty, které mají jiný stav životního cyklu než vydaný základní produkt, aktualizovány nejsou.  

## <a name="verify-the-lifecycle-state-of-the-variants"></a>Ověření stavu životního cyklu variant
1. Klikněte na možnost Uvolněné varianty produktu.

> [!NOTE]
> Všimněte si, že všechny varianty zdědily vybraný stav životního cyklu z uvolněného hlavního uvolněného produktu.  

2. Označte v seznamu vybraný řádek.
3. V poli Stav cyklu životnosti produktu zadejte nebo vyberte hodnotu.


