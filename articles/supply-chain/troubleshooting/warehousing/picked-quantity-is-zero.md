---
title: Zásilku nemůžete potvrdit, protože je prázdná
description: Zásilku nemůžete potvrdit, protože je prázdná
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938433"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a>Zásilku nemůžete potvrdit, protože je prázdná

Kód chyby: LoadLineWarningUpdatedToZero

## <a name="symptoms"></a>Příznaky

Když se pokusíte potvrdit dodávku, systém zobrazí následující chybovou zprávu:

> Řádek nákladu pro položku %1 a dodávka %2 byly aktualizovány tak, aby měly nulové množství kvůli nastavení nedostatečné dodávky, které neumožňuje odeslat jakékoliv množství pro tuto položku.

Proto nemůžete potvrdit dodání pro zásilku.

## <a name="cause"></a>Příčina

Systém vyhodnotí, zda je vybrané množství v očekávaných mezích, na základě vybraného množství, množství načtené linky a procenta nedostatečného doručení. Pokud systém zjistí, že vybrané množství na řádku nákladu je 0 (nula), nemůžete dodávku potvrdit. Například k tomuto problému může dojít, pokud byla práce zrušena a procento nedoručení na řádku nákladu je 100 procent.

## <a name="resolution"></a>Rozlišení

Zkontrolujte řádky nákladu a ujistěte se, že procento a množství podlimitního doručení je v souladu s vybranou prací.

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. Vyberte dodávku, pro kterou nelze potvrdit odeslání.
1. Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu, který přesahuje procento pro snížení dodávky.
1. Upravte hodnotu pole **Nedostatečné doručení** nebo **Množství** podle potřeby.

> [!TIP]
> Pokud problém stále není vyřešen, možná budete muset dokončit další vychystávací práce pro související prodejní objednávky nebo objednávky přenosu, dokud nebude dostupné množství v souladu s nákladem nebo zásilkou.
