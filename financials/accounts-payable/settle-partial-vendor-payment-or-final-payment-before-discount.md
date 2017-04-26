---
title: "Vyrovnání platby částečné dodavatele a konečné platby plně před datum skonta"
description: "Tento článek vás provede scénářem, kdy jsou částečné platby provedeny pro fakturu dodavatele a je využita platební sleva."
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
ms.custom: 14431
ms.assetid: 6b8e3420-b4c9-4e02-9588-598fe6d3df0d
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 6cd87dc1b34d1d689d5417359e1ec3a34d53afb4
ms.lasthandoff: 03/31/2017


---

# <a name="settle-a-partial-vendor-payment-and-the-final-payment-in-full-before-the-discount-date"></a>Vyrovnání platby částečné dodavatele a konečné platby plně před datum skonta

[!include[banner](../includes/banner.md)]


Tento článek vás provede scénářem, kdy jsou částečné platby provedeny pro fakturu dodavatele a je využita platební sleva.

Tato společnost nakupuje zboží od dodavatele 3064. Dodavatel poskytuje Fabrikam platební sleva 1 % Pokud je faktura zaplacena do 14 dnů. Faktury je nutné zaplatit do 30 dnů. Dodavatel dá společnosti Fabrikam také platební slevy pro částečné platby. Vyrovnání parametry jsou umístěny na **parametry závazků** stránky. Dne 25. dubna je zadána faktura na 1 000,00 pro dodavatele 3064.

## <a name="vendor-invoice-on-june-25"></a>Faktura dodavatele dne 25. června
Dne 25. dubna zadá a účtuje faktury pro částku 1 000,00 pro dodavatele 3064. Na stránce **Transakce dodavatele** si může Anežka transakci prohlédnout.

| Doklad   | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek   | Měna |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Fakt-10010 | 6/25/2015 | 10010   |                                      | 1 000,00                              | -1 000,00 | USD      |

Ze stránky **Dodavatelé** otevře April stránku **Vyrovnat transakce**. April může použít stránku **Vyrovnat transakce** k zobrazení dat a částek platební slevy. Datum splatnosti je 25. července a platební sleva ve výši -10,00 je k dispozici, je-li faktura zaplacena do 9. července.

| Označit | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normální            | Fakt-10010 | 3064    | 6/25/2015 | 7/25/2015 | 10010   | 1 000,00                       | USD      | 990,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**.

|                              |           |
|------------------------------|-----------|
| Datum platební slevy           | 7/09/2015 |
| Částka platební slevy         | -10,00    |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 0,00      |
| Částka platební slevy k přijetí | -10,00    |

April klepne na kartu **Platební sleva** a zobrazí tak částku slevy.

| Datum platební slevy | Částka platební slevy | Částka v měně transakce |
|--------------------|----------------------|--------------------------------|
| 7/9/2015           | 10,00                | 990,00                         |
| 7/25/2015          | 0,00                 | 1 000,00                       |

## <a name="partial-payment-on-july-1-by-using-the-settle-transactions-page"></a>Částečná platba 1. července pomocí stránky Transakce vyrovnání
April můžete vytvořit deník plateb pro tuto platbu otevřením stránky **Deník plateb** na závazcích. Si vytvořte nový deník a zadá řádek pro dodavatele 3064. Uživatel otevře **vyrovnat transakce** stránky, takže si můžete označit faktury pro vyrovnání. April označí fakturu a změní hodnotu v poli **Částka k vyrovnání** na **-500,00**. Znovu uvidí, že hodnota v poli **Částka platební slevy** je **-10,00** pro případ úplné fakturace, a že hodnota v poli **Částka platební slevy k přijetí** se změnila na **-5,05**. Proto April vyrovnává u této faktury částku -505,05.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané | Normální            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1 000,00                       | USD      | -500,00          |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**.

|                              |           |
|------------------------------|-----------|
| Datum platební slevy           | 7/09/2015 |
| Částka platební slevy         | -10,00    |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 0,00      |
| Částka platební slevy k přijetí | -5,05     |

April chce vyrovnat přesně polovinu faktury. Proto April změní hodnotu v poli **Částka k vyrovnání** na **-495,00**. Celková částka, která je vyrovnána, je nyní 500,00. Tato částka zahrnuje platební slevu -5,00.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané | Normální            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1 000,00                       | USD      | -495,00          |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**.

|                              |           |
|------------------------------|-----------|
| Datum platební slevy           | 7/09/2015 |
| Částka platební slevy         | -10,00    |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 0,00      |
| Částka platební slevy k přijetí | -5,00     |

April zavře stránku **Vyrovnat transakce**. Řádky plateb pro 495,00 se vytvoří v deníku a April pak zaúčtuje deník. Dubna můžete zkontrolovat transakce dodavatele na **transakce dodavatele** stránky. Zjistí, že má faktura zůstatek-500.00. Rovněž uvidí platbu ve výši 495,00 a platební slevu 5,00.

| Doklad    | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek | Měna |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fakt-10010  | Faktura          | 6/25/2015 | 10010   |                                      | 1 000,00                              | -500,00 | USD      |
| APP-10010  | Platba          | 7/1/2015  |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10010 | Platební sleva    | 7/1/2015  |         | 5,00                                 |                                       | 0,00    | USD      |

## <a name="remaining-amount-paid-on-july-8"></a>Zbývající částka zaplacená dne 8. července
April zaplatí zbývající část faktury pro dodavatele 3064 8. července, tj. v období platební slevy. April vytvoří deník plateb 8. července a označí transakci pro vyrovnání. Zjistí, že je částka, kterou je nutné vyrovnat, je 495,00. Hodnota v poli **Odhadovaná platební sleva** je **-5,00**, protože sleva 5,00 nebyla dříve využita.

|                         |        |
|-------------------------|--------|
| Celkem označeno            | 495,00 |
| Odhadovaná platební sleva | -5,00  |

Informace o označených transakcích se zobrazí v mřížce na stránce **Vyrovnání otevřených transakcí**.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané | Normální            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1 000,00                       | USD      | 495,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**.

|                              |           |
|------------------------------|-----------|
| Datum platební slevy           | 7/09/2015 |
| Částka platební slevy         | 10,00     |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 5,00      |
| Částka platební slevy k přijetí | 5,00      |

April zaúčtuje deník plateb a zkontroluje transakce dodavatele na stránce **Transakce dodavatele**. Zůstatek faktury je nyní 0,00 a April uvidí dvě platby a dvě platební slevy.

| Doklad    | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek | Měna |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fakt-10010  | Faktura          | 6/25/2015 | 10010   |                                      | 1 000,00                              | 0,00    | USD      |
| APP-10010  |  Platba         | 7/1/2015  |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10010 | Platební sleva    | 7/1/2015  |         | 5,00                                 |                                       | 0,00    | USD      |
| APP-10011  | Platba          | 7/8/2015  |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10011 | Platební sleva    | 7/8/2015  |         | 5,00                                 |                                       | 0,00    | USD      |






