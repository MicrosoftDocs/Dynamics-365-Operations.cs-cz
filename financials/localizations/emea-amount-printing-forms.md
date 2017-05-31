---
title: "Aktualizovat zobrazení částek v sestavách a dokumentech"
description: "Toto téma obsahuje informace o tom, jak aktualizovat zobrazení částek v sestavách a jiných dokumentech pro Estonsko, Lotyšsko, Litvu, Polsko, Českou republiku, Maďarsko a Rusko."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264254
ms.assetid: 70b32d8d-6fa7-4617-ba74-a74bc6568d6e
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 3aa3d3e6cff9f3a6ebdbdbab63392dd1ef2cc192
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="update-how-amounts-are-displayed-on-reports-and-documents"></a>Aktualizovat zobrazení částek v sestavách a dokumentech

[!include[banner](../includes/banner.md)]


Toto téma obsahuje informace o tom, jak aktualizovat zobrazení částek v sestavách a jiných dokumentech pro Estonsko, Lotyšsko, Litvu, Polsko, Českou republiku, Maďarsko a Rusko.

Pro právnické osoby v Estonsku, Lotyšsku, Litvě, Polsku, Maďarsku, České republice a Rusku můžete nastavit úplné názvy nebo zkrácené názvy pro měnové jednotky a podjednotky. Tyto názvy slouží k transformaci zastoupení částky na dokladech a sestavách. Příklad: částka **LTL 100,20** může být zobrazena jako **100 Litas 20 Centas**.

## <a name="set-up-full-and-short-names-for-currency-units-and-subunits"></a>Nastavení úplného a krátkého názvu pro měnové jednotky a podjednotky
Pro nastavení úplného a krátkého názvu měnových jednotek a podjednotek pro daný jazyk proveďte následující kroky:

1.  Otevřete stránku **Měny**.
2.  Vyberte měnu.
3.  V podokně akcí klikněte na možnost **Kolísání**.
4.  Úplný název a krátký název pro jazyk přidáte kliknutím na tlačítko **Nová** a vyplněním následujících polí.
    |                                                           |                                                                                                                                                                                                                    |
    |-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **Pole**                                                 | **Popis**                                                                                                                                                                                                    |
    | **Jazyk**                                              | Vyberte jazyk pro aktuální text.                                                                                                                                                                          |
    | **1. pád jednotného čísla (název skupiny polí jednotek)**       | Zadejte jednotné číslo názvu měny. Například jednotné číslo slova Litas je Litas.                                                                                                                         |
    | **1. pád množného čísla (název skupiny polí jednotek)**         | Zadejte množné číslo názvu měny. Například zadejte Litai. **Poznámka:**: pole **2. pád jednotného čísla** a **2. pád množného čísla** jsou k dispozici na základě jazyka, který jste vybrali v poli **Jazyk**. |
    | **Pole 1. pád jednotného čísla (název skupiny polí podjednotek)** | Zadejte jednotné číslo podjednotky měny.                                                                                                                                                            |
    | **1. pád množného čísla (název skupiny polí podjednotek)**         | Zadejte množné číslo podjednotky měny.                                                                                                                                                              |
    | **Krátký název jednotek (krátký název skupiny polí)**       | Zadejte ISO kód pro identifikaci měny. Například zadejte LTL k identifikaci Litas.                                                                                                                             |
    | **Krátký název podjednotek (skupina polí krátkého názvu)**      | Zadejte název podjednotky měny. Například zadejte Centas.                                                                                                                                         |
    | **Spojka 'a' mezi jednotkami a podjednotkami**             | Zvolte tuto možnost, chcete-li vytisknout spojku „a“ mezi jednotkami a podjednotkami. Například částka LTL 100,20 se zobrazí na fakturách nebo v sestavách jako 100 litas and 20 centas.                      |

5.  Klikněte na možnost **Uložit**.





