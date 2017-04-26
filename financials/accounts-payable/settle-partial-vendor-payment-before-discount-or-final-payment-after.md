---
title: "Vyrovnání platby částečné dodavatele před datum skonta s konečnou platbu po datu skonta"
description: "Tento článek vás provede scénářem, kde je provedeno více částečných plateb, některé v rámci období platební slevy a jiné mimo období platební slevy."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14411
ms.assetid: 302ad6ae-28ee-4899-9f6b-f74424a5f50c
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 33851ff7c9ee2c50544589ade0191798a13706e7
ms.lasthandoff: 03/31/2017


---

# <a name="settle-a-partial-vendor-payment-before-the-discount-date-with-a-final-payment-after-the-discount-date"></a>Vyrovnání platby částečné dodavatele před datum skonta s konečnou platbu po datu skonta

[!include[banner](../includes/banner.md)]


Tento článek vás provede scénářem, kde je provedeno více částečných plateb, některé v rámci období platební slevy a jiné mimo období platební slevy.

Tato společnost nakupuje zboží od dodavatele 3057. Společnost Fabrikam obdrží platební sleva 1 % Pokud je faktura zaplacena do 14 dnů. Faktury je nutné zaplatit do 30 dnů. Dodavatel dá společnosti Fabrikam také platební slevy pro částečné platby. Vyrovnání parametry jsou umístěny na **parametry závazků** stránky.

## <a name="invoice-on-june-25"></a>Faktura ze dne 25. června
Dne 25. dubna zadá a účtuje faktury pro částku 1 000,00 pro dodavatele 3057. Na stránce **Transakce dodavatele** si může Anežka transakci prohlédnout.

| Doklad   | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek   | Měna |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Fakt-10020 | Faktura          | 6/25/2015 | 10020   |                                      | 1 000,00                              | −1 000,00 | USD      |

## <a name="partial-payment-on-july-2"></a>Částečná platba dne 2. července
2. července chce Anežka vyrovnat 300,00 z této faktury. Platba má nárok na slevu, protože společnost Fabrikam dostává slevy na částečné platby. Anežka tedy zaplatí 297,00 a dostane slevu 3,00. Vytvoří deník plateb a zadá řádek pro dodavatele 3057. Uživatel otevře **vyrovnat transakce** stránky, takže si můžete označit faktury pro vyrovnání.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané | Normální            | Fakt-10020 | 3057    | 6/25/2015 | 7/25/2015 | 10020   | −1 000,00                      | USD      | –297,00          |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**.

|                              |           |
|------------------------------|-----------|
| Datum platební slevy           | 7/09/2015 |
| Částka platební slevy         | -10,00    |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 0,00      |
| Částka platební slevy k přijetí | –3,00     |

Potom Anežka zaúčtuje platbu. Faktura má nyní zůstatek 700,00. Na stránce **Transakce dodavatele** si může Anežka transakci prohlédnout.

| Doklad    | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek | Měna |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fakt-10020  | Faktura          | 6/25/2015 | 10020   |                                      | 1 000,00                              | -700,00 | USD      |
| APP-10020  | Platba          | 7/1/2015  |         | 297,00                               |                                       | 0,00    | USD      |
| SLEV-10020 | Platební sleva    | 7/1/2015  |         | 3,00                                 |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--normal"></a>Zbývající platba 15. července, použití platební slevy = normální
15. července Anežka zaplatí zbytek faktury, což je až po období slevy. Na stránce **Vyrovnat otevřené transakce** se v poli **Odhadovaná platební sleva** částka slevy nezobrazí a hodnota v poli **Částka platební slevy** bude **0,00**. Když Anežka zaplatí zbývajících 700,00, není získána žádná další sleva.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané | Normální            | Fakt-10020 | 3057    | 6/25/2015 | 7/25/2015 | 10020   | -700,00                        | USD      | -700,00          |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat transakce**. Anežka může vidět, že již dostala slevu 3,00.

|                              |           |
|------------------------------|-----------|
| Datum platební slevy           | 7/09/2015 |
| Částka platební slevy         | 0,00      |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | –3,00     |
| Částka platební slevy k přijetí | 0,00      |

Potom Anežka zaúčtuje platbu. Jakmile otevře stránku **Transakce dodavatele**, zjistí, že faktura má zůstatek 0,00. Také vidí, že jsou zde dvě platby. Jedna platba je na 297,00 s platební slevou 3,00 a druhá platba je na 700,00.

| Doklad    | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek | Měna |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fakt-10020  | Faktura          | 6/25/2015 | 10020   |                                      | 1 000,00                              | 0,00    | USD      |
| APP-10020  | Platba          | 7/1/2015  |         | 297,00                               |                                       | 0,00    | USD      |
| SLEV-10020 | Platební sleva    | 7/1/2015  |         | 3,00                                 |                                       | 0,00    | USD      |
| APP-10021  | Platba          | 7/15/2015 |         | 700,00                               |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--always"></a>Zbývající platba 15. července, použití platební slevy = vždy
Pokud dodavatel umožní dne přijmout slevu, i když si platí po datu skonta, si můžete změnit hodnotu v **použít platební slevu** na **vždy**. **Vypočítat platební slevy pro částečné platby** nastavení přepsáno a sleva uplatněna. Částka platby se změní na 693,00 a sleva je zbývajících 7,00.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Vybrané | Vždy            | Fakt-10020 | 3057    | 6/25/2015 | 7/25/2015 | 10020   | 700,00                               |                                       | USD      | –693,00          |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat transakce**.

|                              |           |
|------------------------------|-----------|
| Datum platební slevy           | 7/09/2015 |
| Částka platební slevy         | 7:00      |
| Použít platební slevu            | Vždy    |
| Přijatá platební sleva          | –3,00     |
| Částka platební slevy k přijetí | –7,00     |

Potom Anežka zaúčtuje platbu. Jakmile otevře stránku **Transakce dodavatele**, zjistí, že faktura má zůstatek 0,00. Také vidí, že jsou zde dvě platby. Jedna platba je na 297,00 s platební slevou 3,00 a druhá platba je na 693,00 s platební slevou 7,00.

| Doklad    | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek | Měna |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fakt-10020  | Faktura          | 6/25/2015 | 10020   |                                      | 1 000,00                              | 0,00    | USD      |
| APP-10020  | Platba          | 7/1/2015  |         | 297,00                               |                                       | 0,00    | USD      |
| SLEV-10020 | Platební sleva    | 7/1/2015  |         | 3,00                                 |                                       | 0,00    | USD      |
| APP-10021  | Platba          | 7/15/2015 |         | 693,00                               |                                       | 0,00    | USD      |
| SLEV-10021 | Platební sleva    | 7/15/2015 |         | 7:00                                 |                                       | 0,00    | USD      |






