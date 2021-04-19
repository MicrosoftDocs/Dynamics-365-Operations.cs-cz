---
title: Příjem částečných dodávek vrácených položek
description: Částečné dodávky jsou definovány v souvislosti se řádky vratek, nikoli s odesláním vratky.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 51213f8f46638b0cce10251e761d7f276c39d924
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836127"
---
# <a name="receive-partial-deliveries-of-returned-items"></a>Příjem částečných dodávek vrácených položek    

[!include [banner](../includes/banner.md)]


Částečné dodávky jsou definovány v souvislosti se řádky vratek, nikoli s odesláním vratky.

To znamená, že když obdržíte úplné množství určené na jednom řádku vratky, ale nic z jiných řádků vratky, tato dodávka není částečnou dodávkou. Pokud však řádek vratky vyžaduje vrácení například 10 jednotek konkrétní položky, ale obdržíte pouze čtyři, o částečnou dodávku se jedná.

Pokud vrácená dodávka obsahuje menší než úplné množství na řádku vratky, můžete dodávku odložit a vyčkat doručení zbylého množství nebo můžete zaznamenat a zaúčtovat částečné množství.

## <a name="register-and-post-a-partial-quantity"></a>Zaznamenání a zaúčtování částečného množství

1.  Po výběru objednávky vrácení pro příjezd ve formuláři **Přehled příjezdu – sklad: %1, Dok: %2, název deníku: %3** klikněte na **zahájit příjezd** k vytvoření deníku příjezdu a pak kliknutím na **Deníky** \> **Zobrazit příjezdy z příjmů** otevřete formulář **Deník místa**.

2.  Vyberte řádek deníku, se kterým chcete pracovat, a poté klepnutím na položku **Řádky** otevřete formulář **Řádky deníku, místa**.

3.  Vyberte řádek čísla položky, pro který bylo doručeno pouze částečné množství, a poté klepnutím na položky **Funkce** \> **Rozdělit** otevřete formulář **Rozdělit**.

4.  Do pole **Rozdělit množství** zadejte množství pro celkový počet přijatých položek a poté klepněte na tlačítko **OK**.

5.  Ve formuláři **Řádky deníku, skl. místa** vyberte řádek pro množství položek, které jste obdrželi, a poté klepněte na položku **Zaúčtovat**. Po převzetí položek můžete zaúčtovat řádek pro další množství.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]