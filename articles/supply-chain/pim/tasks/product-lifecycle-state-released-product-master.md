---
title: Přiřazení stavu životního cyklu produktu k uvolněnému hlavnímu produktu
description: Tento postup ukazuje, jak přiřadit k uvolněnému produktu a jeho variantám stav životního cyklu produktu.
author: t-benebo
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 217bab38544c2794d2e57410f8c2a979605106b0
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567000"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a>Přiřazení stavu životního cyklu produktu k uvolněnému hlavnímu produktu

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]