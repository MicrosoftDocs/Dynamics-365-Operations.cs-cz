---
title: "Aktualizovat zobrazení částek v sestavách a dokumenty"
description: "Toto téma obsahuje informace o tom, jak aktualizovat zobrazení částek v sestavách a jiné dokumenty, Estonska, Lotyšska, Litvy, Polska, České republiky, Maďarska a Ruska."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264254
ms.assetid: 70b32d8d-6fa7-4617-ba74-a74bc6568d6e
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 870341b81e49c9fc677052e9ef87a580892f486f
ms.lasthandoff: 03/31/2017


---

# <a name="update-how-amounts-are-displayed-on-reports-and-documents"></a>Aktualizovat zobrazení částek v sestavách a dokumenty

[!include[banner](../includes/banner.md)]


Toto téma obsahuje informace o tom, jak aktualizovat zobrazení částek v sestavách a jiné dokumenty, Estonska, Lotyšska, Litvy, Polska, České republiky, Maďarska a Ruska.

Pro právnické osoby do Estonska, Lotyšska, Litvy, Polska, Maďarska, České republiky a Ruska můžete nastavit úplné názvy nebo zkrácené názvy pro měnové jednotky a podjednotky. Tyto názvy slouží k transformaci zastoupení částky na dokladech a sestavách. Příklad: částka **LTL 100.20** mohou být zobrazeny jako **100 Litas 20 Centas**.

## <a name="set-up-full-and-short-names-for-currency-units-and-subunits"></a>Nastavit úplný a krátké názvy pro měnové jednotky a podjednotky
Nastavit úplný a krátké názvy pro měnové jednotky a podjednotky jazyka, proveďte následující kroky:

1.  Otevřít **měny** stránky.
2.  Vyberte měnu.
3.  V podokně akcí klepněte na tlačítko **Skloňování**.
4.  Celé jméno a krátký název jazyka klepnutím na tlačítko **nové** a vyplňte následující pole.
    |                                                           |                                                                                                                                                                                                                    |
    |-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **Field**                                                 | **Description**                                                                                                                                                                                                    |
    | **Language**                                              | Vyberte jazyk pro aktuální text.                                                                                                                                                                          |
    | **Singulární nominative (název skupiny polí jednotek)**       | Zadejte měny jednotném čísle. Například jednotném čísle Litas je Litas.                                                                                                                         |
    | **Množném čísle nominative (název skupiny polí jednotek)**         | Zadejte měny množném čísle. Například zadejte Litai. **Poznámka:**: **singulární genitive** a **genitive množném čísle** pole jsou k dispozici na základě jazyka, který jste vybrali v **jazyka** pole. |
    | **Singulární nominative pole (název pole skupiny částí)** | Zadejte jednotném čísle podjednotce měny.                                                                                                                                                            |
    | **Množném čísle nominative (název skupiny polí částí)**         | Zadejte množné číslo bylo měny.                                                                                                                                                              |
    | **Zkrácený název jednotek (krátký název skupiny polí)**       | Zadejte kód ISO k identifikaci měny. Například zadejte LTL k identifikaci Litas.                                                                                                                             |
    | **Zkrácený název částí (krátký název skupiny polí)**      | Zadejte název měny podjednotce. Například zadejte Centas.                                                                                                                                         |
    | **Conjunction 'and' between units and parts**             | Vyberte pro tisk ve spojení "a" mezi jednotkami měny a částí celku. Například na fakturách nebo sestavy částka pro LTL 100.20 se zobrazí jako 100 Litas a 20 Centas.                      |

5.  Click **Save**.





