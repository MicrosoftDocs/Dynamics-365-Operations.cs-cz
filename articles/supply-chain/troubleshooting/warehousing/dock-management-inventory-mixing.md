---
title: Smíšené typy zásob při používání profilu pro správu dokování
description: Aby profil správy doku mohl efektivně spravovat míchání zásob, musí být nejdříve nastaveno zalomení pracovní hlavičky. Tato stránka vysvětluje, jak to udělat.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cc660a2f9839e886240c97a7f60d2e264653074a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475780"
---
# <a name="inventory-types-are-being-mixed-when-using-a-dock-management-profile"></a>Při používání profilu pro správu dokování se míchají typy zásob

## <a name="symptoms"></a>Příznaky

Používáte *zásady konsolidace dodávky*. Nastavili jste *profil správy doku* pro *profil umístění*, ale když je práce vytvořena, typy zásob se v konečném umístění smíchají.

## <a name="resolution"></a>Řešení

Profily správy doků vyžadují, aby byla práce předem rozdělena. Jinými slovy, profil správy doku očekává, že pracovní záhlaví nebude mít více umístění pro vložení.

Aby profil správy doku mohl efektivně spravovat míchání zásob, musí být nastaveno zalomení pracovní hlavičky.

V tomto příkladu je náš profil správy doku nakonfigurován tak, že hodnota **Typy zásob, které by se neměly kombinovat** je nastavena na *ID zásilky* a nastavíme pro ni zalomení pracovní hlavičky:

1. Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.
1. Vyberte **Typ pracovního příkazu** pro úpravu (například *Nákupní objednávky*).
1. Vyberte pracovní šablonu, kterou chcete upravit.
1. V podokně akcí vyberte **Upravit dotaz**.
1. Otevřete kartu **Řazení** a přidejte řádek s následujícím nastavením:
    - **Tabulka** - *Dočasné pracovní transakce*
    - **Odvozená tabulka** - *Dočasné pracovní transakce*
    - **Pole** - *ID dodávky*
1. Vyberte **OK**.
1. Vrátíte se na stránku **Pracovní šablony**. V podokně akcí vyberte **Zalomení pracovních hlaviček**.
1. V podokně akcí vyberte **Upravit**.
1. Zaškrtněte políčko spojené s **Název pole** *ID zásilky*.
1. V podokně akcí vyberte **Uložit**.
