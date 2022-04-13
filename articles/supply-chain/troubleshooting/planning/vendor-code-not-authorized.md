---
title: Kód dodavatele není autorizován pro konkrétní produkt a datum
description: Při pokusu o potvrzení plánované objednávky nebo přidání řádku k nákupní objednávce se zobrazí chybová zpráva s oznámením, že kód dodavatele není pro produkt a datum autorizován.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 917526dfcefb36ce6e59af6f1f5bebc23ee6e53f
ms.sourcegitcommit: ab690bc897699ff8a4c489e749251fe0367050ca
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/26/2022
ms.locfileid: "8489049"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a>Kód dodavatele není autorizován pro konkrétní produkt a datum

Kód chyby: SYP4881415

## <a name="symptoms"></a>Příznaky

Když se pokusíte potvrdit plánovanou objednávku nebo přidat řádek k nákupní objednávce, zobrazí se následující chybová zpráva:

> Kód dodavatele %1 není autorizován pro %2 v %3.

## <a name="cause"></a>Příčina

Došlo k chybě, protože je pole **Metoda kontroly schváleného dodavatele** je nastaveno na *Pouze varování* nebo *Nepovoleno* pro zadaný produkt a dodavatel není aktuálně oprávněn dodat tento produkt.

## <a name="resolution"></a>Řešení

Chcete-li tento problém vyřešit, deaktivujte kontrolu dodavatele u příslušného produktu nebo schvalte dodavatele.

Chcete-li zakázat kontrolu dodavatele produktu, postupujte takto.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Otevřete relevantní produkt.
1. Na pevné záložce **Nákup** nastavte pole **Metoda kontroly schváleného dodavatele** na jinou hodnotu než *Pouze varování* nebo *Nepovoleno*.

Chcete-li schválit dodavatele produktu, postupujte takto.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Otevřete relevantní položku.
1. V podokně Akce na kartě **Nákup** ve skupině **Schválený dodavatel** vyberte **Nastavení**.
1. Na stránce seznamu **Schválený dodavatel** přidejte řádek do mřížky a pak pro ni nastavte následující hodnoty:

    - **Dodavatel** - Vyberte dodavatele ke schválení pro aktuální produkt.
    - **Datum účinnosti** - Vyberte první datum, pro které je dodavatel schválen.
    - **Datum vypršení platnosti** - Vyberte poslední datum, pro které je dodavatel schválen.

Pro další informace viz [Schválení dodavatelů pro konkrétní produkty](../../procurement/tasks/approve-vendors-specific-products.md).
