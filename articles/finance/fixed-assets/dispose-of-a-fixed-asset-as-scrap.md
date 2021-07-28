---
title: Zlikvidovat dlouhodobý majetek jako odpad
description: V tématu je popsán postup při odstranění transakcí dlouhodobého majetku, který byl odstraněn jako odpad.
author: moaamer
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 0e465594968ac860a9cb8f6f5d679084e5594457
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355597"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a>Zlikvidovat dlouhodobý majetek jako odpad

[!include [banner](../includes/banner.md)]

V tématu je popsán postup při odstranění transakcí dlouhodobého majetku, který byl odstraněn jako odpad. Typy transakcí, které lze eliminovat, zahrnují pořízení majetku a kumulované transakce odpisů a další transakce dlouhodobého majetku. Eliminace těchto transakcí má vliv na rozvahové účty, jako je například množství úpravy pořizovací ceny, množství úpravy odpisů, přecenění, navýšení a odpisy.

| Transakce                                         | Má dáti (MD) | Dal (D) |
|-----------------------------------------------------|-------------|--------------|
| MD akumulovaný odpis                        | X           |              |
| D zisk/ztráta z dlouhodobého majetku                          |             | X            |
| MD zisk/ztráta z dlouhodobého majetku                          | X           |              |
| D Účet pořízení dlouhodobého majetku                 |             | X            |
| MD dlouhodobý majetek – zisk/ztráta (zůstatková účetní hodnota \[hodnota NBV\]) | X           |              |
| D zisk/ztráta z dlouhodobého majetku (zůstatková účetní hodnota)                    |             | X            |

> [!NOTE]
> Doporučujeme, abyste úzce spolupracovali s vedoucím finančního oddělení nebo s kontrolorem, který bude identifikovat správné účty, které by měly být použity pro každý typ transakce, a také ověření, zda proces vyřazení a jím generované transakce aktualizují tyto účty správně.

Před vyřazením dlouhodobého majetku jako odpadu je nutné vytvořit účty hlavní knihy, které jsou spojeny s pořizovací hodnotou majetku, odpisy pro aktuální rok, odpisy za předchozí roky a zůstatkovou účetní hodnotou majetku. Typy transakcí dlouhodobého majetku jsou uvedeny na stránce **Účetní profil dlouhodobého majetku**. Přejděte na **Dlouhodobý majetek \> Nastavení \> Účetní profily dlouhodobého majetku** a pak na pevné záložce **Vyřazení** vyberte **Odpad** v poli nad mřížkou. Následující ilustrace znázorňuje seznam typů transakcí dlouhodobého majetku na stránce **Účetní profily dlouhodobého majetku**.


[![Likvidace majetku jako odpad, obr. 1.](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)

Pro následující příklad byl dlouhodobý majetek pořízen 1. ledna 2018 a bude zlikvidován 31. března 2019.

- **Pořizovací cena:** 24 000,00 USD
- **Životnost:** dva roky
- **Metoda odpisování:** Lineární doba životnosti
- **Částka odpisu**: 1 000,00 USD za měsíc

Zůstatková účetní hodnota dlouhodobého majetku se vypočte podle následujícího vzorce:

Zůstatková účetní hodnota = Pořizovací cena – odpisy

V tomto příkladu byl dlouhodobý majetek pořízen a odepisován po dobu 15 měsíců od ledna 2018 do března 2019. Z toho vyplývá, že zůstatková účetní hodnota majetku je 9 000,00 USD (24 000,00 USD – 15 000,00 USD).

[![Příklad odpisu dlouhodobého majetku.](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)


Chcete-li vytvořit deník likvidace, přejděte na **Dlouhodobý majetek \> Položky deníku \> Deník dlouhodobého majetku** a poté v podokně akcí vyberte možnost **Řádky**. Vyberte **Vyřazení – likvidace** a poté vyberte ID dlouhodobého majetku. Chcete-li majetek úplně vyřadit, nezadávejte hodnotu do pole **Má dáti** nebo **Dal**.

[![Deník dlouhodobého majetku.](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)

Transakce likvidace dlouhodobého majetku mění hodnoty polí pro knihu dlouhodobého majetku následujícími způsoby:

- V části **Zůstatek** je pole **Stav** aktualizováno na **Zlikvidovaný**.
- V oddílu **Výdej** je pole **Datum vyřazení** nastaveno na datum, kdy byl majetek zlikvidován.

[![Podrobnosti deníku dlouhodobého majetku.](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)

Zůstatek dlouhodobého majetku je zobrazen na následujícím obrázku.

[![Zůstatek dlouhodobého majetku.](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)

Na následující ilustraci je zobrazen zaúčtovaný doklad.

[![Zůstatková účetní hodnota.](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]