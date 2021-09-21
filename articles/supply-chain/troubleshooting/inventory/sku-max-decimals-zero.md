---
title: Maximální počet desetinných míst pro skladovou jednotku je 0
description: 'Při pokusu o zaúčtování transakce zásob nebo rezervace zásob se zobrazí chyba: "Maximální počet desetinných míst pro jednotku udržování zásob je 0."'
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9dec198e2d77efd2253c80e14d15791cc37f88e1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475835"
---
# <a name="maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Maximální počet desetinných míst pro skladovou jednotku je 0


## <a name="symptoms"></a>Příznaky

Při pokusu o zaúčtování skladové transakce nebo rezervace zásob se zobrazí následující chybová zpráva:

> Maximální počet desetinných míst pro skladovou jednotku je 0.

K tomuto problému dochází, když je množství transakce zásob zadáno jako desetinná hodnota, která je pod úrovní přesnosti, kterou pole podporuje. Například množství *0,5* bylo zadán pro transakci inventáře, ale jsou podporována pouze celočíselná množství. Hodnota by proto měla být *1* namísto *0,5*.

## <a name="resolution"></a>Řešení

1. Spusťte následující skript na instanci serveru SQL Server a zaokrouhlete množství v transakcích zásob. Tento skript opraví hodnoty v tabulce **inventTrans**.

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. Spusťte kontrolu konzistence na skladě, kde je možnost **opravit chybu** zapnutá. Tato kontrola opraví hodnoty v tabulce **inventSum**.

> [!IMPORTANT]
> Důrazně doporučujeme, abyste skript pečlivě upravili podle potřeby pro své prostředí, otestovali jej v testovacím prostředí a poté zkontrolovali výsledná data před spuštěním skriptu v provozním prostředí.
