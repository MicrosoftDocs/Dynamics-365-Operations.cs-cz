---
title: Nesrovnalosti v datech řádků nákupní objednávky
description: Na řádcích nákupní objednávky vidíte nesrovnalosti nebo poškozená data.
author: SmithaNataraj
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: PurchLineManualCorrection, PurchTable, PurchLine, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: ee2cb9a07c8a00a92c71e3e99d8ec20aa27fb20e
ms.sourcegitcommit: b9799a58d6ec221df86788bc37c4fbd28b435e89
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/08/2022
ms.locfileid: "8100797"
---
# <a name="purchase-order-line-data-discrepancies"></a>Nesrovnalosti v datech řádků nákupní objednávky

## <a name="symptoms"></a>Příznaky

Při kontrole řádků nákupní objednávky si všimnete jednoho nebo více z následujících problémů:

- Ve zbytcích řádku nákupní objednávky (dodávka nebo faktura) existuje nesrovnalost nebo poškozená data.
- Řádek nákupní objednávky nebo stav záhlaví je poškozen.
- Nemůžete fakturovat nákupní objednávku, protože například obdržíte jednu nebo více z následujících chybových zpráv:

    - „Zastaveno (chyba): Transakce již byla zaúčtována.“
    - „Množství nelze vyfakturovat, protože skladové transakce se stavem Přijato nejsou dostatečné.“
    - „Nedostatečné transakce zásob se stavem "Zakoupeno" pro položku %0Množství%1 .“

- Objednávku nemůžete dokončit nebo uzavřít například kvůli jednomu z následujících problémů:

    - Tlačítko **Dokončit** není k dispozici.
    - Nemůžete zrušit objednané množství řádku nákupní objednávky pro nákupní objednávku, která je ve stavu potvrzeno a přijato.

## <a name="cause"></a>Příčina

Tyto problémy jsou obvykle způsobeny poškozením dat nebo nesrovnalostí ve zbývajících množstvích v jednom nebo více řádcích nákupní objednávky.

## <a name="resolution"></a>Řešení

Tyto problémy můžete obvykle vyřešit aktualizací stavu nákupu, zbytků dodávky a/nebo fakturačních zbytků v příslušných řádcích nákupní objednávky, jak je popsáno v následujícím postupu.

1. Přejděte do nabídky **Zásobování a zdroje \> Periodické úlohy \> Vyčištění \> Ruční oprava řádků nákupní objednávky**.
1. V poli **Nákupní objednávka** vyhledejte a vyberte nákupní objednávku, která vám způsobuje potíže.
1. V sekci **Řádky nákupní objednávky** vyberte řádek, kde jste našli nesrovnalost.
1. V sekci **Skladové transakce** zkontrolujte data, která jsou zobrazena. Pokud si všimnete jakýchkoli nesrovnalostí mezi řádkem nákupní objednávky a jeho skladovými transakcemi, vyberte v podokně akcí jeden z následujících příkazů v závislosti na tom, kde tyto nesrovnalosti vidíte:

    - **Přepočítat \> Přepočítat zbytek dodávky** – Automaticky aktualizovat stavy řádku nákupní objednávky a záhlaví. Tato funkce funguje pouze pro skladové řádky nákupní objednávky (tj. řádky, kde je položka skladovou položkou). Položky, které nejsou na skladě, a položky se skutečnou hmotností nejsou v současné době podporovány.
    - **Přepočítat \> Přepočítat zbytek faktury** – Automaticky aktualizovat stavy řádku nákupní objednávky a záhlaví. Tato funkce funguje pouze pro skladové řádky nákupní objednávky (tj. řádky, kde je položka skladovou položkou). Položky, které nejsou na skladě, a položky se skutečnou hmotností nejsou v současné době podporovány.
    - **Přepočítat \> Přepočítat stav** – Přepočítat stav vybraného řádku. Tento výpočet je založen na stávající logice. Proto bude stav záhlaví nákupní objednávky aktualizován podle potřeby na základě nového stavu řádku nákupní objednávky.

1. Pokud stále vidíte nesrovnalosti ve zbývajících množstvích, můžete je pomocí následujících polí upravit přímo podle potřeby:

    - Zbývá dodat
    - Zbývající část zásob k dodání
    - Zůstatek faktury
    - Zůstatek skladové faktury
