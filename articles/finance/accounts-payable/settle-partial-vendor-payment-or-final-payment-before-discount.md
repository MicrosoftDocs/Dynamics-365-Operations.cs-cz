---
title: Vyrovnání částečné platby dodavatele a plné vyrovnání konečné platby před datem slevy
description: Tento článek vás provede scénářem, kdy jsou částečné platby provedeny pro fakturu dodavatele a je využita platební sleva.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14431
ms.assetid: 6b8e3420-b4c9-4e02-9588-598fe6d3df0d
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 202d6e8b0933522c2faf5fb49291f11200e4754f
ms.sourcegitcommit: b40d6ce45aeb07724fc41d1a41923970b007fbcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/14/2020
ms.locfileid: "4441319"
---
# <a name="settle-a-partial-vendor-payment-and-the-final-payment-in-full-before-the-discount-date"></a>Vyrovnání částečné platby dodavatele a plné vyrovnání konečné platby před datem slevy

[!include [banner](../includes/banner.md)]

Tento článek vás provede scénářem, kdy jsou částečné platby provedeny pro fakturu dodavatele a je využita platební sleva.

Tato společnost nakupuje zboží od dodavatele 3064. Dodavatel umožňuje společnosti Fabrikam přijmout platební slevu 1 %, pokud je faktura splacena do 14 dní. Faktury je nutné zaplatit do 30 dnů. Dodavatel dá společnosti Fabrikam také platební slevy pro částečné platby. Parametry vyrovnání se nacházejí na stránce **Parametry závazkůs**. Dne 25. dubna je zadána faktura na 1 000,00 pro dodavatele 3064.

## <a name="vendor-invoice-on-june-25"></a>Faktura dodavatele dne 25. června
25. června Anežka zadá a zaúčtuje fakturu na 1 000,00 pro dodavatele 3064. Na stránce **Transakce dodavatele** si může Anežka transakci prohlédnout.

| Doklad   | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek   | Měna |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Fakt-10010 | 25. 6. 2015 | 10010   |                                      | 1 000,00                              | -1 000,00 | USD      |

Ze stránky **Dodavatelé** otevře April stránku **Vyrovnat transakce**. April může použít stránku **Vyrovnat transakce** k zobrazení dat a částek platební slevy. Datum splatnosti je 25. července a platební sleva ve výši -10,00 je k dispozici, je-li faktura zaplacena do 9. července.

| Označit | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normální            | Fakt-10010 | 3064    | 25. 6. 2015 | 25. 7. 2015 | 10010   | 1 000,00                       | USD      | 990,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**.

|       &nbsp;                 | &nbsp;    |
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
| 25. 7. 2015          | 0,00                 | 1 000,00                       |

## <a name="partial-payment-on-july-1-by-using-the-settle-transactions-page"></a>Částečná platba 1. července pomocí stránky Transakce vyrovnání
April můžete vytvořit deník plateb pro tuto platbu otevřením stránky **Deník plateb** na závazcích. Vytvoří nový deník a zadá řádek pro dodavatele 3064. Otevře stránku **Vyrovnat transakce**, aby mohla označit fakturu k vyrovnání. April označí fakturu a změní hodnotu v poli **Částka k vyrovnání** na **-500,00**. Znovu uvidí, že hodnota v poli **Částka platební slevy** je **-10,00** pro případ úplné fakturace, a že hodnota v poli **Částka platební slevy k přijetí** se změnila na **-5,05**. Proto April vyrovnává u této faktury částku -505,05.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané | Normální            | FTI-10010 | 4028    | 25. 6. 2015 | 25. 7. 2015 | 10010   | 1 000,00                       | USD      | -500,00          |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**.

|  &nbsp;                      |  &nbsp;   |
|------------------------------|-----------|
| Datum platební slevy           | 7/09/2015 |
| Částka platební slevy         | -10,00    |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 0,00      |
| Částka platební slevy k přijetí | -5,05     |

April chce vyrovnat přesně polovinu faktury. Proto April změní hodnotu v poli **Částka k vyrovnání** na **-495,00**. Celková částka, která je vyrovnána, je nyní 500,00. Tato částka zahrnuje platební slevu -5,00.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané | Normální            | FTI-10010 | 4028    | 25. 6. 2015 | 25. 7. 2015 | 10010   | 1 000,00                       | USD      | -495,00          |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**.

|  &nbsp;                      |  &nbsp;   |
|------------------------------|-----------|
| Datum platební slevy           | 7/09/2015 |
| Částka platební slevy         | -10,00    |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 0,00      |
| Částka platební slevy k přijetí | -5,00     |

April zavře stránku **Vyrovnat transakce**. Řádky plateb pro 495,00 se vytvoří v deníku a April pak zaúčtuje deník. Na stránce **Transakce dodavatele** může Anežka transakce dodavatele překontrolovat. Na této stránce vidí, že faktura má zůstatek -500,00. Rovněž uvidí platbu ve výši 495,00 a platební slevu 5,00.

| Doklad    | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek | Měna |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fakt-10010  | Faktura          | 25. 6. 2015 | 10010   |                                      | 1 000,00                              | -500,00 | USD      |
| APP-10010  | Platba          | 7/1/2015  |         | 495,00                               |                                       | 0,00    | USD      |
| SLEV-10010 | Platební sleva    | 7/1/2015  |         | 5,00                                 |                                       | 0,00    | USD      |

## <a name="remaining-amount-paid-on-july-8"></a>Zbývající částka zaplacená dne 8. července
April zaplatí zbývající část faktury pro dodavatele 3064 8. července, tj. v období platební slevy. April vytvoří deník plateb 8. července a označí transakci pro vyrovnání. Zjistí, že je částka, kterou je nutné vyrovnat, je 495,00. Hodnota v poli **Odhadovaná platební sleva** je **-5,00**, protože sleva 5,00 nebyla dříve využita.

|  &nbsp;                 |  &nbsp; |
|-------------------------|--------|
| Celkem označeno            | 495,00 |
| Odhadovaná platební sleva | -5,00  |

Informace o označených transakcích se zobrazí v mřížce na stránce **Vyrovnání otevřených transakcí**.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané | Normální            | FTI-10010 | 4028    | 25. 6. 2015 | 25. 7. 2015 | 10010   | 1 000,00                       | USD      | 495,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**.

|  &nbsp;                      | &nbsp;    |
|------------------------------|-----------|
| Datum platební slevy           | 7/09/2015 |
| Částka platební slevy         | 10,00     |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 5,00      |
| Částka platební slevy k přijetí | 5,00      |

April zaúčtuje deník plateb a zkontroluje transakce dodavatele na stránce **Transakce dodavatele**. Zůstatek faktury je nyní 0,00 a April uvidí dvě platby a dvě platební slevy.

| Doklad    | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek | Měna |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fakt-10010  | Faktura          | 25. 6. 2015 | 10010   |                                      | 1 000,00                              | 0,00    | USD      |
| APP-10010  |  Platba         | 7/1/2015  |         | 495,00                               |                                       | 0,00    | USD      |
| SLEV-10010 | Platební sleva    | 7/1/2015  |         | 5,00                                 |                                       | 0,00    | USD      |
| APP-10011  | Platba          | 7/8/2015  |         | 495,00                               |                                       | 0,00    | USD      |
| SLEV-10011 | Platební sleva    | 7/8/2015  |         | 5,00                                 |                                       | 0,00    | USD      |





