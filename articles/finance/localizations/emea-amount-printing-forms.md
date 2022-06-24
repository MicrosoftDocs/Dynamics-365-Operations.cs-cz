---
title: Aktualizovat zobrazení částek v sestavách a dokumentech
description: Tento článek obsahuje informace o tom, jak aktualizovat zobrazení částek v sestavách a jiných dokumentech pro Estonsko, Lotyšsko, Litvu, Polsko, Českou republiku, Maďarsko a Rusko.
author: anasyash
ms.date: 01/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Currency
audience: Application User
ms.reviewer: kfend
ms.custom: 264254
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e985ffc156caa86da3a3e8c36122e4f73278ca7f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907708"
---
# <a name="update-how-amounts-are-displayed-on-reports-and-documents"></a>Aktualizovat zobrazení částek v sestavách a dokumentech

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o tom, jak aktualizovat zobrazení částek v sestavách a jiných dokumentech pro Estonsko, Lotyšsko, Litvu, Polsko, Českou republiku, Maďarsko a Rusko.

Pro právnické osoby v Estonsku, Lotyšsku, Litvě, Polsku, Maďarsku, České republice a Rusku můžete nastavit úplné názvy nebo zkrácené názvy pro měnové jednotky a podjednotky. Tyto názvy slouží k transformaci zastoupení částky na dokladech a sestavách. Například částka **LTL 100,20** může být zobrazena jako **100 Litas 20 Centas**.

## <a name="set-up-full-and-short-names-for-currency-units-and-subunits"></a>Nastavení úplného a krátkého názvu pro měnové jednotky a podjednotky
Pro nastavení úplného a krátkého názvu měnových jednotek a podjednotek pro daný jazyk proveďte následující kroky:

1. Otevřete stránku **Měny**.
2. Vyberte měnu.
3. V podokně akcí zvolte **Skloňování**.
4. Úplný název a krátký název pro jazyk přidáte volbou **Nový** a zadáním informací do následujících polí.

   |             Pole                                                           |                        popis                                                                                                                                                                                                                                                |
   |------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |                       <strong>Jazyk</strong>                        |                                                                                                               Vyberte jazyk pro aktuální text.                                                                                                                |
   |    <strong>1. pád jednotného čísla (název skupiny polí jednotek)</strong>    |                                                                                       Zadejte jednotné číslo názvu měny. Například jednotné číslo slova Litas je Litas.                                                                                       |
   |     <strong>1. pád množného čísla (název skupiny polí jednotek)</strong>     | Zadejte množné číslo názvu měny. Například zadejte Litai. <strong>Poznámka:</strong>: pole <strong>2. pád jednotného čísla</strong> a <strong>2. pád množného čísla</strong> jsou k dispozici na základě jazyka, který jste vybrali v poli <strong>Jazyk</strong>. |
   | <strong>Pole 1. pád jednotného čísla (název skupiny polí podjednotek)</strong> |                                                                                                        Zadejte jednotné číslo podjednotky měny.                                                                                                         |
   |     <strong>1. pád množného čísla (název skupiny polí podjednotek)</strong>     |                                                                                                         Zadejte množné číslo podjednotky měny.                                                                                                          |
   |    <strong>Krátký název jednotek (krátký název skupiny polí)</strong>    |                                                                                         Zadejte ISO kód pro identifikaci měny. Například zadejte LTL k identifikaci Litas.                                                                                         |
   |   <strong>Krátký název podjednotek (skupina polí krátkého názvu)</strong>    |                                                                                               Zadejte název podjednotky měny. Například zadejte Centas.                                                                                               |
   |       <strong>Spojka 'a' mezi jednotkami a podjednotkami</strong>       |                                     Zvolte tuto možnost, chcete-li vytisknout spojku „a“ mezi jednotkami a podjednotkami. Například částka LTL 100,20 se zobrazí na fakturách nebo v sestavách jako 100 litas and 20 centas.                                      |
   |       <strong>Rod</strong>       |  Vyberte **Mužský**, **Ženský** nebo **Střední**. Tento parametr může ovlivnit text skloňování částky, který se zobrazuje v textu místního jazyka na pokladním dokladu. Pokud například nastavíte **Rod** pro měnu EUR jako **Střední**, bude částka 1,01 EUR zapsána v českém jazyce na pokladním dokladu jako *Jedno euro 01 cent*.  |

5. Zvolte možnost **Uložit**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
