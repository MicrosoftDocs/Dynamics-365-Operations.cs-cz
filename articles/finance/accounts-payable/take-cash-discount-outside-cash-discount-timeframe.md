---
title: Provedení platební slevy mimo období platební slevy
description: Tento článek obsahuje dva scénáře, které zobrazují způsob využití platební slevy i v případě, že bude platba provedena mimo období platební slevy.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14301
ms.assetid: bad10b7f-e550-4742-9261-8a094c9c624d
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 47acacf9b1e9667e86fcdd5ce1ed62e79d8afec3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810215"
---
# <a name="take-a-cash-discount-outside-the-cash-discount-period"></a>Provedení platební slevy mimo období platební slevy

[!include [banner](../includes/banner.md)]

Tento článek obsahuje dva scénáře, které zobrazují způsob využití platební slevy i v případě, že bude platba provedena mimo období platební slevy.

28. června Anežka vytvoří fakturu na 2 000,00 pro dodavatele 3052. Faktura obsahuje platební slevu 1 %, pokud je splacena do 14 dní.

## <a name="use-cash-discount-option--always"></a>Použití možnosti platební slevy = vždy
April vytvoří platbu k 1. červenci, které následuje po datu slevy. April otevře stránku **Vyrovnat transakce** pro zobrazení transakcí, které lze vyrovnat. 

April označí fakturu k platbě. Není možná žádná platební sleva, protože je platba provedena po ukončení datu slevy. Dodavatele však poskytl Anežce schválení přesto provést platební slevu. Proto změní hodnotu v poli **Použít platební slevu** na **vždy**.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum platební slevy | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané | Vždy            | Fakt-10030 | 3052    | 28. 6. 2015          | 12. 7. 2015 | 10030   | -2 000,00                      | USD      | -1 980,00        |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat transakce**.

| Pole                        | Hodnota     |
|------------------------------|-----------|
| Dat. plat. slevy           | 12. 7. 2015 |
| Částka platební slevy         | -20,00    |
| Použít platební slevu            | Vždy    |
| Přijatá platební sleva          | 0,00      |
| Částka platební slevy k přijetí | -20,00    |

## <a name="date-to-use-for-calculating-discounts--selected-date"></a>Použité datum pro výpočet slevy = vybrané datum
Pokud byla zaúčtována faktura a platba, platební sleva stále se stále může použít při vyrovnání transakcí na stránce **Vyrovnat transakce**. April změní hodnotu v poli **Datum pro výpočet slevy** na **Vybrané datum**. Uživatel poté zadá datum 28. června, tj. období platební slevy pro fakturu. Toto datum se používá k výpočtu platební slevy pro transakci. Na stránce **Vyrovnání otevřené transakce** April uvidí, že ve výchozím nastavení je úplné sleva 20,00. Řádek faktury zobrazuje, že částka k vyrovnání je 1 980,00.

| Označit                     | Použít platební slevu | Doklad   | Účet | Datum platební slevy | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|--------------------------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané a zvýrazněné | Normální            | Fakt-10030 | 3052    | 28. 6. 2015          | 12. 7. 2015 | 10030   | -2 000,00                      | USD      | -1 980,00        |
| Vybrané                 | Normální            | APP-10030 | 3052    | 7/15/2015          | 7/15/2015 |         | 500,00                         | USD      | 500,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**. Částka slevy, která je přijatá, je 20,00, protože částka k vyrovnání faktury je výchozí částka, 1 980,00.

| Pole                        | Hodnota     |
|------------------------------|-----------|
| Dat. plat. slevy           | 12. 7. 2015 |
| Částka platební slevy         | -20,00    |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 0,00      |
| Částka platební slevy k přijetí | -20,00    |

April aktualizuje hodnoty v poli **Částka k vyrovnání** na **500,00**. Hodnota v poli **Částka platební slevy k přijetí** je vypočtena jako **5,05**.

| Označit                     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané a zvýrazněné | Normální            | Fakt-10030 | 3052    | 28. 6. 2015 | 12. 7. 2015 | 10030   | 2 000,00                       | USD      | -500,00          |
| Vybrané                 | Normální            | APP-10030 | 3052    | 7/15/2015 | 7/15/2015 |         | 500,00                         | USD      | 500,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**. Hodnota v poli **Částka platební slevy k přijetí** je **5,05**, protože částka k vyrovnání faktury byla změněna na částku platby 500,00.

| Pole                        | Hodnota     |
|------------------------------|-----------|
| Dat. plat. slevy           | 12. 7. 2015 |
| Částka platební slevy         | -20,00    |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 0,00      |
| Částka platební slevy k přijetí | -5,05     |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]