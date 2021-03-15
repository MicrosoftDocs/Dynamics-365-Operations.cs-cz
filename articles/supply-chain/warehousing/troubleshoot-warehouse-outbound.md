---
title: Řešení potíží s odchozími skladovými operacemi
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s odchozími skladovými operacemi v Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 165ac8145ad75c2c6619764b9abe855b9d32eb46
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993971"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a>Řešení potíží s odchozími skladovými operacemi

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s odchozími skladovými operacemi v Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a>Zobrazí se následující chybová zpráva: „Prodejní objednávku nelze uvolnit.“

### <a name="issue-description"></a>Popis problému

K tomuto problému může dojít z několika důvodů. Například je objednávka blokována správou kreditů a není možné vytvářet žádné zásilky, dokud nezadáte platnou poštovní adresu pro všechny prodejní řádky spojené s prodejní objednávkou. Alternativně existuje blokování objednávky, které musí být vyřešeno, než bude možné objednávku uvolnit do skladu. Toto pozastavení může být specifické pro objednávku nebo může být na zákaznickém účtu.

### <a name="issue-resolution"></a>Řešení problému

Přidejte nebo aktualizujte adresu na řádcích prodejní objednávky a objednávky a poté objednávku uvolněte do skladu. Objednávky lze do skladu uvolnit, pouze pokud mají platnou dodací adresu (podle nastavení formátu adresy v modulu **Správa organizace**).

Prozkoumejte pozastavení objednávky a vyřešte problémy. Poté odeberte blokování objednávky nebo zákazníka a uvolněte objednávku do skladu.

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a>Zobrazuje se následující zpráva: „Zásilka s nákladem 1% byla potvrzena.“ Žádné řádky však nejsou vystaveny.

### <a name="issue-description"></a>Popis problému

Zásilka s nákladem byla potvrzena, ale k dalšímu odeslání nedošlo.

### <a name="issue-resolution"></a>Řešení problému

Potvrzení zásilky nemá vliv na odeslání. Pouze aktualizuje stav zásilky a nákladu. Vystavení musí proběhnout v samostatném procesu.

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a>Zobrazuje se následující chybová zpráva: „Přímé doručení není možné zpracovat pro sklad 1%, protože má povolenou správu skladu. Zadejte prosím jiný sklad, který nemá povolenou správu skladu. “

### <a name="issue-description"></a>Popis problému

Položka je přidána na prodejní řádek pro přímé dodání ze skladu, který je povolen pro správu skladu (WMS). Tato chybová zpráva se zobrazí při aktualizaci řádku prodeje. 

### <a name="issue-resolution"></a>Řešení problému

Společnost Microsoft vyhodnotila tento problém a zjistila, že jde o omezení funkcí. V současné době WMS nepodporuje přímé doručování. Chcete-li tedy použít přímé doručení, musíte vybrat položku a sklad, který nespadá do WMS.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]