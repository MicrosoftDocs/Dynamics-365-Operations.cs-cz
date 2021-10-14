---
title: Nastavení parametrů pro účtování mezipodnikové objednávky
description: Toto téma vysvětluje, jak nastavit parametry pro účtování mezipodnikové objednávky
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c728f2f491948ae1c8550396ba4d72f76f46fe85
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548146"
---
# <a name="set-up-parameters-to-post-an-intercompany-order"></a>Nastavení parametrů pro účtování mezipodnikové objednávky

[!include [banner](../../includes/banner.md)]

Při zaúčtování faktury mezipodnikové faktury odběratele ji můžete nastavit tak, aby se automaticky zaúčtovala mezipodniková nákupní objednávka i původní faktura odběratele.

> [!NOTE]
> Než provedete tento postup, nastavte ve své organizaci správu tisku tak, aby ukazovala na správnou tiskárnu faktur. Tím zajistíte, že faktura za původní prodejní objednávku bude vytištěna na správné tiskárně.

Je nutné nastavit následující parametry:

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**. Vyberte prodejní objednávku, se kterou chcete pracovat.
1. U prodejní objednávky v podokně akcí vyberte **Zobrazení záhlaví** a poté vyberte záložku **Mezipodniková nastavení** a otevřete ji.
1. Přejděte do podokna akcí a na kartě **Prodejní objednávka** zvolte **Upravit**.
1. Vraťte se do záložky **Mezipodniková nastavení** a vyberte **Přímá dodávka**, aby byla povolena přímá dodávka v rámci mezipodnikového řetězce (všechny objednávky).
1. Výběrem **Uložit** uložíte prodejní objednávky s novým nastavením. Poté vyberte **Zavřít** a zavřete prodejní objednávku.
1. Přejděte na **Zásobování a zdroje \> Dodavatelé \> Všichni dodavatelé**. Na kartě **Obecné** vyberte **Mezipodnikové**.
1. Na stránce **Mezipodnikové** vyberte odkaz **Zásady nákupních objednávek**. Ve skupině polí **Mezipodniková nákupní objednávka (přímá dodávka)** vyberte možnost **Zaúčtovat fakturu automaticky** a vypněte zaškrtávací políčko u pole **Vytisknout fakturu automaticky**.
1. Ve skupině polí **Původní prodejní objednávka (přímá dodávka)** vyberte pole **Zaúčtovat fakturu automaticky** a pole **Vytisknout fakturu automaticky**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
