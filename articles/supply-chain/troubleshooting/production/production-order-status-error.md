---
title: Chyba při změně stavu z Vykázáno jako dokončeno na Konec
description: Můžete obdržet chybu při změně stavu výrobní zakázky z Vykázáno jako dokončeno na Konec Tato stránka vysvětluje, jak tento problém zmírnit.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 744637f5cccffe44b85f77c1a9df2034012fac40
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475802"
---
# <a name="error-when-changing-status-of-production-order-from-reported-as-finished-to-end"></a>Chyba při změně stavu výrobní zakázky z Vykázáno jako dokončeno na Konec

## <a name="symptoms"></a>Příznaky

Když se stav výrobní zakázky změní z Ohlášeno jako dokončené na Konec, zobrazí se následující některá z následujících chybových zpráv:

> Konflikt aktualizace. Standardní náklady neodpovídají finanční hodnotě zásob po aktualizaci.

> Ve funkci InventCostMovement.checkVariance došlo k kritické chybě.

## <a name="cause"></a>Příčina

K tomuto problému dochází, protože podkladová data byla změněna jiným procesem. Proces se pokusí aktualizovat data až pětkrát. Pokud konflikt přetrvává i po pěti pokusech, obdržíte jednu z výše uvedených zpráv.

## <a name="resolution"></a>Řešení

Toto chování je záměrné. Chcete-li problém zmírnit, obnovte dávkovou úlohu. Mělo by to nakonec běžet.

Pokud dávková úloha po jejím obnovení nadále selhává, ověřte, zda přesnost zaokrouhlování výchozí měny hlavní knihy odpovídá zaokrouhlování použitému na hodnoty v tabulce InventSum. Pokud byla přesnost zaokrouhlení změněna na nevyhovující hodnotu, pravděpodobně ji musíte změnit zpět na vyhovující hodnotu. Vyhledejte **ModifiedDateTime**. V tomto případě hodnota obvykle ukazuje, že přesnost zaokrouhlování byla nedávno změněna.
