---
title: "Vyrovnávací deníky pro mezijednotkové účetnictví"
description: "Tento článek ukazuje, jak je deník automaticky vyrovnán pro výběru možnosti vyrovnávací finanční dimenzi na stránce hlavní knihy."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0909b64a77024d551af0dad2de985887cf6ff06d
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="balanced-journals-for-interunit-accounting"></a>Vyrovnávací deníky pro mezijednotkové účetnictví

[!include[banner](../includes/banner.md)]


Tento článek ukazuje, jak je deník automaticky vyrovnán pro výběru možnosti vyrovnávací finanční dimenzi na stránce hlavní knihy. 

Pokud účetní zápisy nejsou vyrovnány na úrovni hodnot finančních dimenzí, jsou automaticky vytvořeny další položky účtu za účelem vyrovnání deníku. Použijte tyto účetní položky v typech zaúčtování **Mezijednotkové účetnictví – má dáti** a**Mezijednotkové účetnictví – dal** na stránce **Účty pro automatické transakce**. Například pobočka, tj. druhý segment účtu hlavní knihy, bude vybrána jako vyrovnávací finanční dimenze, a budou vytvořeny následující účetní položky.

|                      |           |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100.00 OŘ |
| 6100 – NY – OU\_249  | 100.00 OŘ |
| 2100 – MSP – OU\_256 | 200.00 CR |

V tomto případě dojde k určení následujících zůstatků:

-   Pro pobočku MSP = 100,00 CR
-   Pro pobočku NY = 100,00 DR

Následující účetní položky jsou proto vytvořeny automaticky tak, aby vyrovnaly deník na úrovni hodnot finančních dimenzí.

|                                   |           |
|-----------------------------------|-----------|
| (Mezijednotkový debit) – MSP – OU\_256 | 100.00 OŘ |
| (Interunit Credit) – NY – OU\_249 | 100.00 CR |






