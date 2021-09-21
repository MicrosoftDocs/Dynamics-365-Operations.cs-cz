---
title: Nelze nastavit množství servisní položky na řádku nabídky prodeje
description: Při práci s prodejními cenovými nabídkami nemůžete nastavit prodejní množství u produktů, které jsou položkami služeb, protože zde nelze počítat žádné fyzické položky.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea0f8f246e95f90b6ac5e78ee63950c9ca836a0e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475837"
---
# <a name="cant-change-the-sales-quantity-of-a-service-item-on-a-sales-quotation-line"></a>Nelze změnit prodejní množství servisní položky na řádku nabídky prodeje

## <a name="symptoms"></a>Příznaky

Pokud se pokusíte nastavit prodejní množství (pole **SalesQty**) pro položku typu *Služba* na řádku prodejní nabídky, zobrazí se následující zpráva:

> Aktualizace není povolena pro pole Množství.

## <a name="cause"></a>Příčina

To je záměrné. U produktů, které jsou položkami služby, nemůžete nastavit prodejní množství. Například pokud nabídnete službu pro instalaci položky, nemá smysl zaznamenávat množství, protože neexistuje žádná fyzická položka k započítání. Existuje pouze služba.
