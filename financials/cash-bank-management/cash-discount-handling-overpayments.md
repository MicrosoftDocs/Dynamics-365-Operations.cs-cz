---
title: "Zpracování platební slevy u přeplatků"
description: "Tento článek popisuje scénáře, které znázorňují způsob zpracování platby, když zákazník využije platební slevu, ale má také přeplatek."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14171
ms.assetid: a94d0fd0-57ba-4054-93c8-519d01d50e19
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 451273a8ee98f7033795182e754f76aca3788f47
ms.lasthandoff: 03/31/2017


---

# <a name="handling-cash-discounts-for-overpayments"></a>Zpracování platební slevy u přeplatků

[!include[banner](../includes/banner.md)]


Tento článek popisuje scénáře, které znázorňují způsob zpracování platby, když zákazník využije platební slevu, ale má také přeplatek. 

Faktura je považována za přeplacenou, pokud je částka platby větší než částka faktury bez platební slevy. K určení dostupného rozdílu platební slevy je zpracováno, když je faktura přeplacená, použijte pole **Správa platební slevy** a **Maximální přeplatek nebo nedoplatek** na stránce **Parametry pohledávek**. V následujícím příkladu odběratel přeplatil fakturu o 0,50.

| Faktura celkem | Dostupná platební sleva | Částka k úhradě obsahující platební slevu | Částka skutečně uhrazená odběratelem |
|---------------|-------------------------|-----------------------------------------------------|-----------------------------------|
| 105,00 USD        | 10,50 USD                   | 94,50 USD                                               | 95,00 USD                             |

## <a name="cash-discount-administration--specific"></a>Správa platební slevy = specifická
Při výběru možnosti **Specifické** v poli **Správa platební slevy** na stránce **Účty pro automatické transakce** je převzata úplná platební sleva. Částka přeplatku buď je zaúčtována na účet hlavní knihy s rozdílem platební slevy, nebo zůstane zůstatek na účtu odběratele. Chování závisí na tom, zda je částka přeplatku mezi 0,00 a částkou zadanou v poli **Maximální přeplatek či nedoplatek**, nebo zda je částka přeplatku větší než částka **Maximální přeplatek či nedoplatek**.

### <a name="scenario-1"></a>Scénář 1

V tomto scénáři se částka přeplatku nachází mezi hodnotami 0,00 a maximálním přeplatkem nebo nedoplatkem. Pokud je faktura zaplacena v rámci sedmi dní, faktura bude zadána na částku 105,00 s dostupnou platební slevou.

| Faktura celkem | Dostupná platební sleva | Částka k úhradě obsahující platební slevu |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00 USD        | 10,50 USD                   | 94,50 USD                                               |

Odběratel odešle platbu za 95,00 v rámci období platební slevy. Platba je poté vyrovnána podle faktury ve výši 105,00. Po vyrovnání faktury a platby se u pohledávky odběratele vytvoří následující transakce.

| Transakce   | Částka | Zůstatek |
|---------------|--------|---------|
| Faktura       | 105,00 USD | 0,00    |
| Platba       | -95,00 | 0,00    |
| Platební sleva | -10,50 | 0,00    |

Pro platby a vyrovnání jsou generovány následující účetní položky. **Platba**

| Účet             | Částka Má dáti | Částka kreditu |
|---------------------|--------------|---------------|
| Hotovost                | 95,00 USD        |               |
| Pohledávky |              | 95,00 USD         |

**Vyrovnání**

| Účet                                                                                                          | Částka Má dáti | Částka kreditu |
|------------------------------------------------------------------------------------------------------------------|--------------|---------------|
| Pole Platební sleva (**Hlavní účet pro slevy odběratele** na stránce **Platební slevy**).                 | 10,50 USD        |               |
| Pohledávky                                                                                              |              | 10,50 USD         |
| Platební slevy pro odběratele (pole **Platební slevy pro odběratele** na stránce **Účty pro automatické transakce**. |              | 0,50          |
| Pohledávky                                                                                              | 0,50         |               |

### <a name="scenario-2"></a>Scénář 2

V tomto scénáři částka přeplatku přesahuje maximální přeplatek nebo nedoplatek. Pokud je faktura zaplacena v rámci sedmi dní, faktura bude zadána na částku 105,00 s dostupnou platební slevou.

| Faktura celkem | Dostupná platební sleva | Částka k úhradě obsahující platební slevu |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00 USD        | 10,50 USD                   | 94,50 USD                                               |

Odběratel odešle platbu za 95,00 v rámci období platební slevy. Platba je poté vyrovnána podle faktury ve výši 105,00. Po vyrovnání faktury a platby se u pohledávky odběratele vytvoří následující transakce.

| Transakce   | Částka | Zůstatek |
|---------------|--------|---------|
| Faktura       | 105,00 USD | 0,00    |
| Platba       | -95,00 | -0,50   |
| Platební sleva | -10,50 | 0,00    |

Částka přeplatku ve výši 0,50 zůstane jako otevřený zůstatek platby a lze ji vyrovnat podle další faktury. Pro platby a vyrovnání jsou generovány následující účetní položky. **Platba**

| Účet             | Částka Má dáti | Částka kreditu |
|---------------------|--------------|---------------|
| Hotovost                | 95,00 USD        |               |
| Pohledávky |              | 95,00 USD         |

**Vyrovnání**

| Účet                                                                                          | Částka Má dáti | Částka kreditu |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Pole Platební sleva (**Hlavní účet pro slevy odběratele** na stránce** Platební slevy**). | 10,50 USD        |               |
| Pohledávky                                                                              |              | 10,50 USD         |

## <a name="cash-discount-administration--unspecific"></a>Správa platební slevy = nespecifická
Při výběru možnosti **Nespecifické** v poli **Správa platební slevy** na stránce **Účty pro automatické transakce** je částka platební slevy snížena částkou přeplatku. Toto chování se vždy používá bez ohledu na to, zda je částka přeplatku větší nebo menší než částka zadaná v poli **Maximální přeplatek či nedoplatek**.

### <a name="scenario-3"></a>Scénář 3

V tomto scénáři je faktura zaplacena v rámci sedmi dní, faktura bude zadána na částku 105,00 s dostupnou platební slevou.

| Faktura celkem | Dostupná platební sleva | Částka k úhradě obsahující platební slevu |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00 USD        | 10,50 USD                   | 94,50 USD                                               |

Odběratel odešle platbu za 95,00 v rámci data platební slevy. Platba je poté vyrovnána podle faktury ve výši 105,00. Po vyrovnání faktury a platby se u pohledávky odběratele vytvoří následující transakce.

| Transakce   | Částka | Zůstatek |
|---------------|--------|---------|
| Faktura       | 105,00 USD | 0,00    |
| Platba       | -95,00 | -0,00   |
| Platební sleva | -10,00 | 0,00    |

Částka platební slevy se sníží z 10,50 na 10,00. Platba a faktura je považována za vyrovnanou. **Platba**

| Účet             | Částka Má dáti | Částka kreditu |
|---------------------|--------------|---------------|
| Hotovost                | 95,00 USD        |               |
| Pohledávky |              | 95,00 USD         |

**Vyrovnání**

| Účet                                                                                          | Částka Má dáti | Částka kreditu |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Pole Platební sleva (**Hlavní účet pro slevy odběratele** na stránce **Platební slevy**). | 10,50 USD        |               |
| Pohledávky                                                                              |              | 10,50 USD         |






