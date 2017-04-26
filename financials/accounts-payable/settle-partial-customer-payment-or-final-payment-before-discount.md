---
title: "Vyrovnání platby částečné odběratele a konečné platby plně před datum skonta"
description: "Tento článek popisuje scénáře, které zobrazují způsob záznamu částečných plateb pro odběratele a využití platebních slev v rámci období platební slevy."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14491
ms.assetid: 0f07d3ce-a439-43ed-a22e-957ccd36a37b
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: ac2c569666b97bc430d3d677366a88446ab76091
ms.lasthandoff: 03/31/2017


---

# <a name="settle-a-partial-customer-payment-and-the-final-payment-in-full-before-the-discount-date"></a>Vyrovnání platby částečné odběratele a konečné platby plně před datum skonta

[!include[banner](../includes/banner.md)]


Tento článek popisuje scénáře, které zobrazují způsob záznamu částečných plateb pro odběratele a využití platebních slev v rámci období platební slevy.

Tato společnost prodává zboží zákazníkovi 4028. Tato společnost nabízí platební sleva 1 % Pokud je faktura zaplacena do 14 dnů. Faktury je nutné zaplatit do 30 dnů. Společnost Fabrikam nabízí také platební slevy pro částečné platby. Vyrovnání parametry jsou umístěny na **parametry pohledávek** stránky.

## <a name="customer-invoice"></a>Faktura odběratele
25. června Arnold zadá a účtuje faktury pro částku 1 000,00 4028 zákazníka. Arnold tyto transakce můžete zobrazit na stránce** Transakce odběratele**.

| Doklad   | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek  | Měna |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10010 | Faktura          | 6/25/2015 | 10010   | 1 000,00                             |                                       | 1 000,00 | USD      |

Na stránce **Odběratel** nebo **Transakce odběratele** Arnie může otevřít stránku **Vyrovnat transakce** a zobrazit tak data a částky platebních slev, které jsou k dispozici pro fakturu. Datum splatnosti je 25. července a platební sleva ve výši 10,00 je k dispozici, je-li faktura zaplacena do 9. července.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané | Normální            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1 000,00                       | USD      | 990,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce** pro označenou fakturu.

|                              |           |
|------------------------------|-----------|
| Datum platební slevy           | 7/09/2015 |
| Částka platební slevy         | 10,00     |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 0,00      |
| Částka platební slevy k přijetí | 10,00     |

Arnie klepne na kartu **Platební sleva** a zobrazí tak částku slevy.

| Datum platební slevy | Částka platební slevy | Částka v měně transakce |
|--------------------|----------------------|--------------------------------|
| 7/9/2015           | 10,00                | 990,00                         |
| 7/25/2015          | 0,00                 | 1 000,00                       |

## <a name="partial-payment-by-using-the-enter-customer-payments-page"></a>Částečná platba za použití stránky Zadat platby odběratele
Zákazník 4028 odešle platbu za 500,00 dne 1. Zadejte tuto platbu, Arnold není klepnutím na **řádky**. Místo toho zaznamená platbu vytvořením nového deníku plateb a opětovným otevřením stránky **Zadat platby odběratele**. Zadá informace o platbě a označí fakturu, kterou zadal. Poté Arnie zadá **500,00** jako částku a zadá také **500,00** v poli **Částka k úhradě** v mřížce. Vzhledem k tomu, že společnost Fabrikam umožňuje platební slevy pro částečné platby, zjistí, že bude využita také částečná platební sleva 5,05. Výpočet pro tuto slevu je 500,00 ÷ 0,99 × 0,01 = 5,05. (V tomto výpočtu je 500,00 vyděleno číslem 0,99, protože existuje 1% sleva. Z toho vyplývá, že odběratel zaplatí 99 % faktury. Výsledek je vynásoben procentem slevy, což je 1 procento, neboli 0,01. Pokud zákazník přebírá plnou sleva 10,00, částku, která musí být vyrovnána bude 990.00.) V mřížce v dolní části se zobrazí slevy informace **zadat platby odběratele** stránky.

| Částka platební slevy k přijetí | Přijatá platební sleva | Částka k vyplacení |
|------------------------------|---------------------|---------------|
| 5,05                         | 0,00                | 500,00        |

## <a name="partial-payment-by-using-the-journal-lines"></a>Částečná platba pomocí řádků deníku
Místo otevření stránky **Zadat platby odběratele** v deníku plateb Arnie může kliknout na **Řádky** a zadat platbu. Zobrazí deník plateb kde Arnold zadat řádek pro zákazníka 4028. Arnold otevře stránku **Vyrovnat transakce**, aby mohl označit fakturu k vyrovnání. Arnie označí fakturu a změní hodnotu v poli **Částka k vyrovnání** na **500,00**. Znovu uvidí, že hodnota v poli **Částka platební slevy** je **10,00** pro případ úplné fakturace, a že hodnota v poli **Částka platební slevy k přijetí** se změnila na **5,05**. Proto Arnie vyrovnává u této faktury částku 505,05.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané | Normální            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1 000,00                       | USD      | 500,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**.

|                              |           |
|------------------------------|-----------|
| Datum platební slevy           | 7/09/2015 |
| Částka platební slevy         | 10,00     |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 0,00      |
| Částka platební slevy k přijetí | 5,05      |

Pokud si zákazník přeje vyrovnat přesně polovinu faktury, odešle platbu na 495,00. V takovém případě Arnie zadá **495,00** do pole **Částka k vyrovnání**. Platební sleva ve výši 5,00 bude využita a celková vyrovnaná částka je tedy 500,00.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané | Normální            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1 000,00                       | USD      | 495,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**.

|                              |           |
|------------------------------|-----------|
| Datum platební slevy           | 7/09/2015 |
| Částka platební slevy         | 10,00     |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 0,00      |
| Částka platební slevy k přijetí | 5,00      |

Arnie zavře stránku **Vyrovnat transakce**. Řádky plateb pro 495,00 se vytvoří v deníku a Arnie pak zaúčtuje deník. Transakce odběratele může zkontrolovat na stránce **Transakce odběratele**. Na této stránce Arnie vidí, že faktura má zůstatek 500,00. Rovněž uvidí platbu ve výši 495,00 a slevu 5,00.

| Doklad    | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek | Měna |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10010  | Faktura          | 6/25/2015 | 10010   | 1 000,00                             |                                       | 500,00  | USD      |
| ARP-10010  |  Platba         | 7/1/2015  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10010 |  Platební sleva   | 7/1/2015  |         |                                      | 5,00                                  | 0,00    | USD      |

## <a name="payment-for-the-remaining-amount"></a>Platba zbývající částky
Odběratel 4028 zaplatí zbývající částku 495,00 dne 8. července, tedy v rámci období platební slevy. Arnie vytvoří deník plateb 8. července a označí transakci pro vyrovnání. Zjistí, že je částka, kterou je nutné vyrovnat, je 495,00. Hodnota v poli **Odhadovaná platební sleva** je **5,00**, protože sleva 5,00 nebyla dříve využita.

|                         |        |
|-------------------------|--------|
| Celkem označeno            | 495,00 |
| Odhadovaná platební sleva | 5,00   |

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

Arnie zaúčtuje deník a zkontroluje transakce odběratele na stránce **Transakce odběratele**. Zůstatek faktury je nyní 0,00 a Arnie uvidí dvě platby a dvě platební slevy.

| Doklad    | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek | Měna |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10010  | Faktura          | 6/25/2015 | 10010   | 1 000,00                             |                                       | 0,00    | USD      |
| ARP-10010  | Platba          | 7/1/2015  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10010 | Platební sleva    | 7/1/2015  |         |                                      | 5,00                                  | 0,00    | USD      |
| ARP-10011  | Platba          | 7/8/2015  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10011 | Platební sleva    | 7/8/2015  |         |                                      | 5,00                                  | 0,00    | USD      |






