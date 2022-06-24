---
title: Formát importu pro konsolidaci
description: Tento článek poskytuje podrobné informace o formátu importu, který se používá při konsolidaci finančních údajů od více právnických osob.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 0aee830f8fbfa384c86dc16465b202be36f07b73
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871297"
---
# <a name="import-format-for-consolidation"></a>Formát importu pro konsolidaci

[!include [banner](../includes/banner.md)]

Tento článek poskytuje podrobné informace o formátu importu, který se používá při konsolidaci finančních údajů od více právnických osob. Formát importu musí být uložen jako textový soubor (.txt).

## <a name="import-format"></a>Formát importu

V následující tabulce je uveden formát importu, který byste měli použít při konsolidaci během importu.

| Tabulka záznamů | Formát | Poznámky |
|--------------|---------|-------|
| 1            | 170150, Goodwill, 4 | <ul><li>Tabulka záznamů</li><li>ID hlavního účtu zdroje</li><li>Řádek hlavního účtu</li><li>Typ hlavního účtu</li></ul> |
| 2            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>ID hlavního účtu</li><li>Datum transakce</li><li>Typ fiskálního období (**0** = Zahájení, **1** = Provozní a **2** = Uzávěrka)</li><li>Měna transakce</li><li>Debet nebo kredit (**0** = Debet a **1** = Kredit)</li><li>Účtovací vrstva</li><li>Částky transakce</li><li>Množství</li><li>Místní RecID (nejednoznačná, jedinečná hodnota int64 pro transakci)</li></ul> |
| 3            | USMF0000009, 2017/01/01, FY2017, 1, 2017,01,01, 602200, USD, 6053.6.0 | <ul><li>Číslo záznamu (číslo transakce záhlaví rozpočtu)</li><li>Výchozí datum hlavičky rozpočtu</li><li>ID rozpočtového modelu</li><li>Typ rozpočtu (**1** - původní rozpočet, **2** - převod, **3** - revize, **4** - břemeno, **5** - předběžné břemeno, **6** - přenesený rozpočet, **7** - projekt, **8** - dlouhodobý majetek, **9** - prognóza poptávky, **10** - prognóza nabídky, **11** - rozdělení, **12** - předběžný rozpočet.)</li><li>Datum řádku.</li><li>ID hlavního účtu pro řádek</li><li>Kód měny pro řádek</li><li>Částka řádku v měně transakce</li><li>Hodnota celočíselného výčtu pro typ rozpočtu pro řádek (výdaj nebo výnos)</li></ul> |
| 4            | DEMF | RecordCompany je zdrojová právnická osoba. |
| 5            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>ID hlavního účtu</li><li>Datum transakce</li><li>Typ fiskálního období (0 Zahájení, 1 Provozní a 2 Uzávěrka)</li><li>Měna transakce</li><li>Debet nebo kredit (0 Debet a 1 Kredit)</li><li>Účtovací vrstva</li><li>Částka transakce</li><li>Množství</li><li>Místní RecID (nejednoznačná, jedinečná hodnota int64 pro transakci)</li></ul>  |
| 6            | BusinessUnit, 1 oddělení, 2 | Atributy finanční dimenze, které jsou definovány v pořadí segmentů.<p>Můžete použít stránku **Export** k ověření, jak jsou definovány atributy.</p> |
| 7            | 002,1,658 | <ul><li>Hodnota finanční dimenze</li><li>Finanční dimenze jako index poskytovaný v RecordDimensions</li><li>Nejednoznačné, jedinečné ID záznamu, které je přidruženo k jedinečnému ID záznamu z RecordTrans nebo RecordTrans2</li></ul> |
| 8            | 002,1,1 | <ul><li>Hodnoty dimenze, které jsou přidruženy k transakci z RecordBudget</li><li>Finanční dimenze jako index poskytovaný v RecordDimensions</li><li>Nejednoznačné ID záznamu řádku, které je zarovnáno s řádkem transakčních řádků v souboru</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
