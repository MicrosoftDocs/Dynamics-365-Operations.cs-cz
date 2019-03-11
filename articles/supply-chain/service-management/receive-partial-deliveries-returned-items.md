---
title: Příjem částečných dodávek vrácených položek
description: Částečné dodávky jsou definovány v souvislosti se řádky vratek, nikoli s odesláním vratky.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2b7bfad1e0d80675848353d4118960d44f2dc01
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "363906"
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




