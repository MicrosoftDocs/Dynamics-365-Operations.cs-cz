---
title: Vyrovnání částečné platby dodavatele před datem slevy s konečnou platbou po datu slevy
description: Tento článek vás provede scénářem, kde je provedeno více částečných plateb, některé v rámci období platební slevy a jiné mimo období platební slevy.
author: abruer
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14411
ms.assetid: 302ad6ae-28ee-4899-9f6b-f74424a5f50c
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b44d3d561b5d7fdccf34d2220d5ade0d3974ea8b
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/25/2019
ms.locfileid: "896964"
---
# <a name="settle-a-partial-vendor-payment-before-the-discount-date-with-a-final-payment-after-the-discount-date"></a>Vyrovnání částečné platby dodavatele před datem slevy s konečnou platbou po datu slevy

[!include [banner](../includes/banner.md)]

Tento článek vás provede scénářem, kde je provedeno více částečných plateb, některé v rámci období platební slevy a jiné mimo období platební slevy.

Tato společnost nakupuje zboží od dodavatele 3057. Fabrikam přijme platební slevu 1 %, pokud je faktura splacena do 14 dní. Faktury je nutné zaplatit do 30 dnů. Dodavatel dá společnosti Fabrikam také platební slevy pro částečné platby. Parametry vyrovnání se nacházejí na stránce **Parametry závazkůs**.

## <a name="invoice-on-june-25"></a>Faktura ze dne 25. června
25. června Anežka zadá a zaúčtuje fakturu na 1 000,00 pro dodavatele 3057. Na stránce **Transakce dodavatele** si může Anežka transakci prohlédnout.

| Doklad   | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek   | Měna |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Fakt-10020 | Faktura          | 25. 6. 2015 | 10020   |                                      | 1 000,00                              | −1 000,00 | USD      |

## <a name="partial-payment-on-july-2"></a>Částečná platba dne 2. července
2. července chce Anežka vyrovnat 300,00 z této faktury. Platba má nárok na slevu, protože společnost Fabrikam dostává slevy na částečné platby. Anežka tedy zaplatí 297,00 a dostane slevu 3,00. Vytvoří platební deník a zadá řádek pro dodavatele 3057. Otevře stránku **Vyrovnat transakce**, aby mohla označit fakturu k vyrovnání.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané | Normální            | Fakt-10020 | 3057    | 25. 6. 2015 | 25. 7. 2015 | 10020   | −1 000,00                      | USD      | –297,00          |

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
| Fakt-10020  | Faktura          | 25. 6. 2015 | 10020   |                                      | 1 000,00                              | -700,00 | USD      |
| APP-10020  | Platba          | 7/1/2015  |         | 297,00                               |                                       | 0,00    | USD      |
| SLEV-10020 | Platební sleva    | 7/1/2015  |         | 3,00                                 |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--normal"></a>Zbývající platba 15. července, použití platební slevy = normální
15. července Anežka zaplatí zbytek faktury, což je až po období slevy. Na stránce **Vyrovnat otevřené transakce** se v poli **Odhadovaná platební sleva** částka slevy nezobrazí a hodnota v poli **Částka platební slevy** bude **0,00**. Když Anežka zaplatí zbývajících 700,00, není získána žádná další sleva.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané | Normální            | Fakt-10020 | 3057    | 25. 6. 2015 | 25. 7. 2015 | 10020   | -700,00                        | USD      | -700,00          |

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
| Fakt-10020  | Faktura          | 25. 6. 2015 | 10020   |                                      | 1 000,00                              | 0,00    | USD      |
| APP-10020  | Platba          | 7/1/2015  |         | 297,00                               |                                       | 0,00    | USD      |
| SLEV-10020 | Platební sleva    | 7/1/2015  |         | 3,00                                 |                                       | 0,00    | USD      |
| APP-10021  | Platba          | 7/15/2015 |         | 700,00                               |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--always"></a>Zbývající platba 15. července, použití platební slevy = vždy
Pokud dodavatel Anežce umožní uplatnit slevu, i když splácí po datu slevy, může změnit hodnotu v poli **Použít hotovostní slevu** na **Vždy**. Nastavení **Vypočítat platební slevy pro částečné platby** se přepíše a je uplatněna sleva. Částka platby se změní na 693,00 a sleva je zbývajících 7,00.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Vybrané | Vždy            | Fakt-10020 | 3057    | 25. 6. 2015 | 25. 7. 2015 | 10020   | 700,00                               |                                       | USD      | –693,00          |

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
| Fakt-10020  | Faktura          | 25. 6. 2015 | 10020   |                                      | 1 000,00                              | 0,00    | USD      |
| APP-10020  | Platba          | 7/1/2015  |         | 297,00                               |                                       | 0,00    | USD      |
| SLEV-10020 | Platební sleva    | 7/1/2015  |         | 3,00                                 |                                       | 0,00    | USD      |
| APP-10021  | Platba          | 7/15/2015 |         | 693,00                               |                                       | 0,00    | USD      |
| SLEV-10021 | Platební sleva    | 7/15/2015 |         | 7:00                                 |                                       | 0,00    | USD      |





