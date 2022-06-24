---
title: Mezipodnikové objednávky a vratky
description: Tento článek vysvětluje mezipodnikové objednávky a vratky
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 65d0dc6049969ff7d8f84ca4eb3baf486ddad660
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859020"
---
# <a name="intercompany-orders-and-return-orders"></a>Mezipodnikové objednávky a vratky

[!include [banner](../../includes/banner.md)]

Tento článek popisuje, jak vytvořit a aktualizovat mezipodnikové nákupní objednávky, prodejní objednávky, vratky, nákupní smlouvy a prodejní smlouvy.

## <a name="about-intercompany-orders"></a>O mezipodnikových objednávkách

Při vytvoření mezipodnikové prodejní objednávky aplikace Microsoft Dynamics 365 Supply Chain Management automaticky vytvoří odpovídající nákupní objednávku. Obdobně vytvoření mezipodnikové nákupní objednávky vyvolá automatické vytvoření odpovídající mezipodnikové prodejní objednávky.

Tento postup se uplatní u dvoustranných objednávek (transakcí mezi dvěma souvisejícími společnostmi) i u většiny třístranných objednávek (kdy mezipodniková transakce vychází z prodejní objednávky vystavené pro externího odběratele).

## <a name="intercompany-order-example"></a>Příklad mezipodnikové objednávky

Mějme dvě související společnosti. Společnost A je prodejní dceřiná společnost, společnost B je distribuční jednotka. Mezipodnikové prodejní a nákupní objednávky budou automaticky vytvořeny v následujících situacích:

- Když společnost A vytvoří nákupní objednávku, u níž je dodavatelem společnost B, bude ve společnosti B automaticky vytvořena mezipodniková prodejní objednávka. Dvoustranný objednávkový řetězec se skládá z nákupní objednávky ve společnosti A a z mezipodnikové prodejní objednávky ve společnosti B.
- Když společnost B vytvoří prodejní objednávku, u níž je odběratelem společnost A, bude ve společnosti A automaticky vytvořena mezipodniková nákupní objednávka. Dvoustranný objednávkový řetězec se skládá z prodejní objednávky ve společnosti B a z mezipodnikové nákupní objednávky ve společnosti A.
- Když společnost A na počátku vytvoří prodejní objednávku pro externího odběratele, může být ve společnosti A automaticky vytvořena nákupní objednávka, což dále povede k automatickému vytvoření mezipodnikové prodejní objednávky ve společnosti B. Třístranný objednávkový řetězec se skládá z prodejní a nákupní objednávky ve společnosti A a z mezipodnikové prodejní objednávky ve společnosti B.

## <a name="about-intercompany-return-orders"></a>O mezipodnikových vratkách

Mezipodnikové položky lze vracet v podstatě stejně jako u běžných případů vracení. U mezipodnikových položek však vratka od externího odběratele vytvoří mezipodnikovou nákupní objednávku. To následně vede k automatickému vytvoření mezipodnikové prodejní vratky. Mezipodnikovou položku lze ovšem vrátit i bez vratky od externího odběratele.

Mezipodnikové vratky se podobně jako běžné vratky vytvářejí ve stránce **Vytvořit vratku**.

V aplikaci Microsoft Dynamics 365 Supply Chain Management jsou mezipodnikové prodejní a nákupní smlouvy automaticky aktualizovány podle vrácené položky. Závazky prodejní nebo nákupní smlouvy pro danou položku budou automaticky upraveny tak, aby odrážely změnu množství nebo částky při vrácení položky.

## <a name="intercompany-return-order-example"></a>Příklad mezipodnikové vratky

Společnost A vytvoří nákupní objednávku, která je propojena s nákupní smlouvou pro mezipodnikovou položku. Ve společnosti B bude automaticky vytvořena mezipodniková prodejní objednávka propojená s odpovídající prodejní smlouvou. Nákupní smlouva a prodejní smlouva jsou provázány jako mezipodnikové smlouvy.

Společnost A vrátí mezipodnikovou položku společnosti B. Společnost B vytvoří vratku pro danou položku a ve společnosti A bude automaticky vytvořena nákupní vratka. Závazky v nákupní smlouvě a prodejní smlouvě propojené s původními objednávkami budou automaticky upraveny tak, aby odrážely změny v množství nebo částce.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
