---
title: Automatické vyrovnání a stanovení priorit
description: Tento článek popisuje způsob vyrovnání transakcí, pokud vyberete možnost Automatické vyrovnání na straně Parametry pohledávek. Vysvětluje také, jak lze automatické vyrovnání použít v kombinaci s prioritou platby.
author: ShivamPandey-msft
ms.date: 01/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: kfend
ms.custom: 14531
ms.assetid: e7837cf6-ec69-44b4-8d47-eba38d5c7b1f
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd5b894c82beb1b5d69ad6bf485161ab9c91a806
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855513"
---
# <a name="automatic-settlement-and-prioritization"></a>Automatické vyrovnání a stanovení priorit

[!include [banner](../includes/banner.md)]

Tento článek popisuje způsob vyrovnání transakcí, pokud vyberete možnost Automatické vyrovnání na straně Parametry pohledávek. Vysvětluje také, jak lze automatické vyrovnání použít v kombinaci s prioritou platby.

Při vyrovnání plateb pomocí faktur a ostatních transakcí, máte k dispozici dvě možnosti. Transakce pro vyrovnání je možné vybrat ručně, nebo systém tyto transakce vybere automaticky pomocí funkce automatického vyrovnání. Můžete také upravit, jak je automatické vyrovnání zpracováno, pomocí možnosti **Určit prioritu vyrovnání**. Všechny z těchto možností jsou součástí parametrů vyrovnání , které jsou definovány na stránce **Parametry pohledávek**. Způsob automatického vyrovnání transakcí se může lišit v závislosti na metodě, kterou používáte pro automatické vyrovnání. K dispozici jsou následující metody:

-   Priorita vyrovnání definovaná uživatelem
-   Výchozí automatické vyrovnání

Následuje části popisují způsob vyrovnání transakcí pro každou z metod.

## <a name="example-transactions"></a>Příklady transakcí
Příklady vyrovnání dále v tomto článku jsou založeny na následujících transakcích. Všechny transakce jsou pro odběratele 2050.

| Transakce   | Datum        | Částka | Podmínky platební slevy | Dat. plat. slevy | Poznámky                                                                                                                                                                                      |
|---------------|-------------|--------|---------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Faktura 1     | 15. srpna   | 100,00 | 2%14, čisté 30        | 29. srpna          |                                                                                                                                                                                               |
| Faktura 2     | 1. září | 250.00 | 2%14, čisté 30        | 15. září       |                                                                                                                                                                                               |
| Faktura 3     | 15. říjen  | 500.00 | 2% 14/netto 30        | 29. října         |                                                                                                                                                                                               |
| Oznámení úroků | 15. října  | 7:00   |                     |                    | Toto oznámení úroků je pro fakturu 1 a fakturu 2. Částka se počítá jako 2% úrok z částek, které jsou 30 nebo více dnů po splatnosti. Například 0,02 × (100,00 + 250,00) = 7,00. |

## <a name="user-defined-settlement-priority"></a>Priorita vyrovnání definovaná uživatelem
Nastavíte-li **Použít prioritu pro automatické vyrovnání** na **Ano** na stránce **Parametry pohledávek**, priorita vyrovnání, která je definována na stránce **Priorita vyrovnání**, se použije při výběru transakcí pro automatické vyrovnání. V tomto příkladu je definována následující priorita vyrovnání:

1.  Typ transakce
    -   Platební poplatky
    -   Upomínky
    -   Oznámení úroků
    -   Faktury

2.  Datum transakce, Vzestupně
3.  Doklad

Pokud zaúčtujete platbu ve výši 700,00 ke dni 25. října, platba se vyrovná pro transakce v následujícím pořadí.

| Doklad       | Datum       | Faktura | Částka v měně transakce | Částka k vyrovnání | Zůstatek | Měna |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Oznámení úroků | 15. 10. 2015 |         | 7:00                           | 7:00             | 0,00    | USD      |
| Faktura 1     | 15. 8. 2015  | 10001   | 100,00                         | 100,00           | 0,00    | USD      |
| Faktura 2     | 1. 9. 2015   | 10002   | 250,00                         | 250,00           | 0,00    | USD      |
| Faktura 3     | 15. 10. 2015 |         | 500,00                         | 343,00           | 157,00  | USD      |

## <a name="default-automatic-settlement"></a>Výchozí automatické vyrovnání
Pokud nejsou uvedeny žádné uživatelem definované priority vyrovnání, transakce jsou automaticky vybrány k vyrovnání na základě data splatnosti. Vyrovnané transakce musí mít stejnou měnu jako transakce, se kterou je vyrovnána. Pokud zaúčtujete platbu ve výši 700,00 ke dni 25. října, následující transakce budou vybrány pro k vyrovnání.

| Doklad       | Datum       | Faktura | Částka v měně transakce | Částka k vyrovnání | Zůstatek | Měna |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Faktura 1     | 15. 8. 2015  | 10001   | 100,00                         | 100,00           | 0,00    | USD      |
| Faktura 2     | 1. 9. 2015   | 10002   | 250,00                         | 250,00           | 0,00    | USD      |
| Faktura 3     | 15. 10. 2015 |         | 500.00                         | 350.00           | 150.00  | USD      |
| Oznámení úroků | 15. 10. 2015 |         | 7.00                           | 0,00             | 7.00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
