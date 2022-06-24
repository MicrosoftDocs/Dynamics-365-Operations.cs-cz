---
title: Změna základu ve výpočtech daně ICMS-DIF pro produkty od dodavatelů z jiných států
description: Tento článek popisuje konfiguraci pro výpočty typu daně ICMS-DIF při obdržení fiskálního dokladu v brazilském státě Rio Grande do Sul (RS) nebo São Paulo (SP).
author: Kai-Cloud
ms.date: 1/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 1fde18c79f375db4db6bc52cdb5c40a61625ae63
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868255"
---
# <a name="basis-change-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Změna základu ve výpočtech daně ICMS-DIF pro produkty od dodavatelů z jiných států

Tento článek popisuje konfiguraci pro výpočty typu daně **ICMS-DIF** při obdržení fiskálního dokladu v brazilském státě Rio Grande do Sul (RS) nebo São Paulo (SP).

Podle definice ve státním zákoně se vybíraný Imposto sobre Circulação de Mercadorias e Serviços (ICMS) musí řídit tímto pravidlem:

*ICMS k výběru* = ([(*Operační částka* − *ICMS ze zdroje*) ÷ (1 − *ICMS % interní*)] × *ICMS % interní*) − *Částka ICMS ze zdroje*

## <a name="example"></a>Příklad

Brazilská společnost ve státě RS obdrží fiskální doklad o nákupu od prodejce ve státě SP. Společnost musí inkasovat procentuální rozdíl ICMS mezi státem RS (18 %) a státem SP (12 %). Základ však musí být vypočten podle předchozího pravidla.

- **Operační částka:** 1000,00 brazilských realů (1000,00 R$)
- **Mezistátní ICMS:** 120,00 R$
- **Procento ICMS ve státě RS:** 18 %
- **ICMS k výběr ve státě RS:** (\[(1000 − 120) ÷ (1 – 0,18)\] × 0,18) – 120 = 73,17 R$ 

## <a name="resolution"></a>Řešení

Chcete-li vypočítat rozdílové ICMS (ICMS-DIF) podle pravidel státu RS, musíte nastavit kódy daně z prodeje a skupinu daně z prodeje následujícím způsobem:

1. Vytvořte kód daně z prodeje pro příjem 12% ICMS (pro druhý stát). Tento kód se používá k registraci částky daňové pohledávky od dodavatele.
2. Vytvořte kód daně z prodeje pro výběr ICMS-DIF. Tento kód daně z prodeje by měl mít procentuální částku 18 % (pro váš vlastní stát), aby se definoval rozdíl mezi 18 % a 12 %. Nastavte typ daně na **ICMS-DIF**. Tento kód daně z prodeje musí být v parametrech výpočtu definován následujícím způsobem:

    - V poli **Původ** vyberte **Procento hrubé částky**.
    - V poli **Základ marže** vyberte **Čistá částka na řádek** nebo **Čistá částka součtu faktury**.
    - Definujte daňový kód tak, aby měl fiskální hodnotu **3**. Tímto způsobem bude opravná transakce automaticky vytvořena, když je aktivní modul **Fiskální knihy**.
    - V konfiguraci skupiny daně z prodeje vyberte možnost **Použít daň** pro kód daně z prodeje **ICMS-DIF**.
