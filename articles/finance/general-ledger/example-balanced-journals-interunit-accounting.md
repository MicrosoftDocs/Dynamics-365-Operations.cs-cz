---
title: Vyrovnávací deníky pro mezijednotkové účetnictví
description: Tento článek ukazuje, jak je deník automaticky vyrovnán pro výběru možnosti vyrovnávací finanční dimenzi na stránce hlavní knihy.
author: kweekley
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38a7d88602dcd0121eb331dab8bf35a815287f8c
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712307"
---
# <a name="balanced-journals-for-interunit-accounting"></a>Vyrovnávací deníky pro mezijednotkové účetnictví

[!include [banner](../includes/banner.md)]

Tento článek ukazuje, jak je deník automaticky vyrovnán pro výběru možnosti vyrovnávací finanční dimenzi na stránce hlavní knihy. 

Pokud účetní zápisy nejsou vyrovnány na úrovni hodnot finančních dimenzí, jsou automaticky vytvořeny další položky účtu za účelem vyrovnání deníku. Použijte tyto účetní položky v typech zaúčtování **Mezijednotkové účetnictví – má dáti** a **Mezijednotkové účetnictví – dal** na stránce **Účty pro automatické transakce**. Například Obchodní jednotka, tj. druhý segment účtu hlavní knihy, bude vybrána jako vyrovnávací finanční dimenze, a budou vytvořeny následující účetní položky.

| &nbsp;               | &nbsp;    |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100.00 OŘ |
| 6100 – NY – OU\_249  | 100.00 OŘ |
| 2100 – MSP – OU\_256 | 200.00 CR |

V tomto případě dojde k určení následujících zůstatků:

-   Pro obchodní jednotku MSP = 100.00 CR
-   Pro obchodní jednotku NY = 100.00 DR

Následující účetní položky jsou proto vytvořeny automaticky tak, aby vyrovnaly deník na úrovni hodnot finančních dimenzí.

| &nbsp;                            | &nbsp;    |
|-----------------------------------|-----------|
| (Mezijednotkový debit) – MSP – OU\_256 | 100.00 OŘ |
| (Interunit Credit) – NY – OU\_249 | 100.00 CR |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
