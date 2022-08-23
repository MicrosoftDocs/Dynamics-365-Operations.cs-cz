---
title: Úplné vyrovnání částečných a konečných plateb před datem slevy
description: Tento článek popisuje scénáře, které zobrazují způsob záznamu částečných plateb pro odběratele a využití platebních slev v rámci období platební slevy.
author: abruer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 14491
ms.assetid: 0f07d3ce-a439-43ed-a22e-957ccd36a37b
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
ms.openlocfilehash: 7acc4655be35eff73dc5f2cad1fd0f511a0a7fc3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281318"
---
# <a name="settle-partial-and-final-payments-in-full-before-the-discount-date"></a>Úplné vyrovnání částečných a konečných plateb před datem slevy

[!include [banner](../includes/banner.md)]

Tento článek popisuje scénáře, které zobrazují způsob záznamu částečných plateb pro odběratele a využití platebních slev v rámci období platební slevy.

Fabrikam prodává zboží zákazníkovi 4028. Fabrikam nabízí platební slevu 1 %, pokud je faktura splacena do 14 dní. Faktury je nutné zaplatit do 30 dnů. Společnost Fabrikam nabízí také platební slevy pro částečné platby. Parametry vyrovnání se nacházejí na stránce **Parametry pohledávek**.

## <a name="customer-invoice"></a>Faktura odběratele
25. června Arnold zadá a zaúčtuje fakturu na 1 000,00 pro zákazníka 4028. Arnold tyto transakce můžete zobrazit na stránce **Transakce odběratele**.

| Doklad   | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek  | Měna |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10010 | Faktura          | 25. 6. 2015 | 10010   | 1 000,00                             |                                       | 1 000,00 | USD      |

Na stránce **Odběratel** nebo **Transakce odběratele** Arnie může otevřít stránku **Vyrovnat transakce** a zobrazit tak data a částky platebních slev, které jsou k dispozici pro fakturu. Datum splatnosti je 25. července a platební sleva ve výši 10,00 je k dispozici, je-li faktura zaplacena do 9. července.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané | Normální            | FTI-10010 | 4028    | 25. 6. 2015 | 25. 7. 2015 | 10010   | 1 000,00                       | USD      | 990,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce** pro označenou fakturu.

|    &nbsp;                    |  &nbsp;   |
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
| 25. 7. 2015          | 0,00                 | 1 000,00                       |

## <a name="partial-payment-by-using-the-enter-customer-payments-page"></a>Částečná platba za použití stránky Zadat platby odběratele
Zákazník 4028 odešle platbu za 500,00 1. června. Při zadávání této platby Arnold neklikne na **Řádky**. Místo toho zaznamená platbu vytvořením nového deníku plateb a opětovným otevřením stránky **Zadat platby odběratele**. Arnie zadá informace o platbě a označí fakturu, kterou zadal. Když Arnie zadá **500,00** jako částku, zadá také **500,00** v poli **Částka k úhradě** v mřížce. Vzhledem k tomu, že společnost Fabrikam umožňuje platební slevy pro částečné platby, Arnie zjistí, že bude využita také částečná platební sleva 5,05. Výpočet pro tuto slevu je 500,00 ÷ 0,99 × 0,01 = 5,05. (V tomto výpočtu je 500,00 vyděleno číslem 0,99, protože existuje 1% sleva. Z toho vyplývá, že odběratel zaplatí 99 % faktury. Výsledek je vynásoben procentem slevy, což je 1 procento, neboli 0,01. Pokud zákazník přebírá plnou slevu ve výši 10,00, částka, která musí být vyrovnána, bude 990,00.) V mřížce v dolní části stránky **Zadat platby odběratele** se zobrazí informace o slevě.

| Částka platební slevy k přijetí | Přijatá platební sleva | Částka k vyplacení |
|------------------------------|---------------------|---------------|
| 5,05                         | 0,00                | 500,00        |

## <a name="partial-payment-by-using-the-journal-lines"></a>Částečná platba pomocí řádků deníku
Místo otevření stránky **Zadat platby odběratele** v deníku plateb Arnie může kliknout na **Řádky** a zadat platbu. Zobrazí se platební deník, kam může Arnold zadat řádek pro zákazníka 4028. Arnold otevře stránku **Vyrovnat transakce**, aby mohl označit fakturu k vyrovnání. Arnie označí fakturu a změní hodnotu v poli **Částka k vyrovnání** na **500,00**. Znovu uvidí, že hodnota v poli **Částka platební slevy** je **10,00** pro případ úplné fakturace, a že hodnota v poli **Částka platební slevy k přijetí** se změnila na **5,05**. Proto Arnie vyrovnává u této faktury částku 505,05.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané | Normální            | FTI-10010 | 4028    | 25. 6. 2015 | 25. 7. 2015 | 10010   | 1 000,00                       | USD      | 500,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**.

|        &nbsp;                | &nbsp;    |
|------------------------------|-----------|
| Datum platební slevy           | 7/09/2015 |
| Částka platební slevy         | 10,00     |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 0,00      |
| Částka platební slevy k přijetí | 5,05      |

Pokud si zákazník přeje vyrovnat přesně polovinu faktury, odešle platbu na 495,00. V takovém případě Arnie zadá **495,00** do pole **Částka k vyrovnání**. Platební sleva ve výši 5,00 bude využita a celková vyrovnaná částka je tedy 500,00.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané | Normální            | FTI-10010 | 4028    | 25. 6. 2015 | 25. 7. 2015 | 10010   | 1 000,00                       | USD      | 495,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**.

|     &nbsp;                   | &nbsp;    |
|------------------------------|-----------|
| Datum platební slevy           | 7/09/2015 |
| Částka platební slevy         | 10,00     |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 0,00      |
| Částka platební slevy k přijetí | 5,00      |

Arnie zavře stránku **Vyrovnat transakce**. Řádky plateb pro 495,00 se vytvoří v deníku a Arnie pak zaúčtuje deník. Transakce odběratele může zkontrolovat na stránce **Transakce odběratele**. Na této stránce Arnie vidí, že faktura má zůstatek 500,00. Rovněž uvidí platbu ve výši 495,00 a slevu 5,00.

| Doklad    | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek | Měna |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10010  | Faktura          | 25. 6. 2015 | 10010   | 1 000,00                             |                                       | 500,00  | USD      |
| ARP-10010  |  Platba         | 7/1/2015  |         |                                      | 495,00                                | 0,00    | USD      |
| SLEV-10010 |  Platební sleva   | 7/1/2015  |         |                                      | 5,00                                  | 0,00    | USD      |

## <a name="payment-for-the-remaining-amount"></a>Platba zbývající částky
Odběratel 4028 zaplatí zbývající částku 495,00 dne 8. července, tedy v rámci období platební slevy. Arnie vytvoří deník plateb 8. července a označí transakci pro vyrovnání. Zjistí, že je částka, kterou je nutné vyrovnat, je 495,00. Hodnota v poli **Odhadovaná platební sleva** je **5,00**, protože sleva 5,00 nebyla dříve využita.

|   &nbsp;                | &nbsp; |
|-------------------------|--------|
| Celkem označeno            | 495,00 |
| Odhadovaná platební sleva | 5,00   |

Informace o označených transakcích se zobrazí v mřížce na stránce **Vyrovnání otevřených transakcí**.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané | Normální            | FTI-10010 | 4028    | 25. 6. 2015 | 25. 7. 2015 | 10010   | 1 000,00                       | USD      | 495,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**.

|  &nbsp;                      |  &nbsp;   |
|------------------------------|-----------|
| Datum platební slevy           | 7/09/2015 |
| Částka platební slevy         | 10,00     |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 5,00      |
| Částka platební slevy k přijetí | 5,00      |

Arnie zaúčtuje deník a zkontroluje transakce odběratele na stránce **Transakce odběratele**. Zůstatek faktury je nyní 0,00 a Arnie uvidí dvě platby a dvě platební slevy.

| Doklad    | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek | Měna |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10010  | Faktura          | 25. 6. 2015 | 10010   | 1 000,00                             |                                       | 0,00    | USD      |
| ARP-10010  | Platba          | 7/1/2015  |         |                                      | 495,00                                | 0,00    | USD      |
| SLEV-10010 | Platební sleva    | 7/1/2015  |         |                                      | 5,00                                  | 0,00    | USD      |
| ARP-10011  | Platba          | 7/8/2015  |         |                                      | 495,00                                | 0,00    | USD      |
| SLEV-10011 | Platební sleva    | 7/8/2015  |         |                                      | 5,00                                  | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
