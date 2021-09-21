---
title: Chyba celkového množství výrobků při pokusu o ukončení zakázky
description: Při pokusu o ukončení výrobní zakázky a hlášení jako dokončené se může zobrazit chyba celkem dobrého množství. Tato stránka vysvětluje, proč a jak tento problém opravit.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5f0c2c2ca64ada9d72c0ebd04e7de561aaa52039
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475786"
---
# <a name="total-good-quantity-error-when-trying-to-end-a-production-order"></a>Chyba celkového množství výrobků při pokusu o ukončení výrobní zakázky

## <a name="symptoms"></a>Příznaky

Při pokusu o zaúčtování deníku sestavy jako dokončené na výrobní zakázce se zobrazí následující chybová zpráva:

> Celkové množství zboží hlášené jako dokončené pro výrobu bude %1. Zpětná vazba pro poslední operaci je 0.00 celkem.

## <a name="cause"></a>Příčina

K tomuto problému dochází, pokud množství, která byla zaúčtována v posledních operacích, byla nesprávná. Například pokud je zahájena výroba, ale množství, které musí být zahájeno, není přiděleno, bude deníku karet postupů zaúčtován bez řádků. Chcete-li potvrdit situaci, otevřete výrobní zakázku a poté v podokně akcí na kartě **Zobrazení** vyberte **Karta postupu**.

## <a name="resolution"></a>Řešení

Tento problém můžete vyřešit zaúčtováním dalších deníků pro operace, pro které deníky nebyly správně zaúčtovány. Restartujte výrobní zakázku a výběrem odešlete další deníky. Tato akce nespustí výrobní zakázku, ale zaúčtuje deníky. Karta postupu by pak měla zobrazit množství, která byla zaúčtována, a měli byste být schopni úspěšně ukončit výrobní zakázky.
