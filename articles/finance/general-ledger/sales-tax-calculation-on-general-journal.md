---
title: Výpočet DPH na řádcích hlavního deníku
description: V tomto tématu je vysvětleno, jak se počítá DPH pro různé typy účtů (dodavatel, odběratel, hlavní kniha a projekt) na řádcích hlavního deníku.
author: EricWang
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 93c9f2bebd038723d50e64bdaa0e0992c003f88d
ms.sourcegitcommit: cec5de2dcfc7210a86a220e308f80ab204f12383
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665835"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a>Výpočet DPH na řádcích hlavního deníku
[!include [banner](../includes/banner.md)]

V tomto tématu je vysvětleno, jak se počítá DPH pro různé typy účtů (dodavatel, odběratel, hlavní kniha a projekt) na řádcích hlavního deníku.

Tento proces lze rozdělit do tří kroků:

- Určete směr DPH.

- Určete částku DPH, která bude uložena jako dočasná tabulka DPH.

- Určete částku DPH a účet na dokladu.

## <a name="determine-the-sales-tax-direction"></a>Určení směru DPH

Způsob, jakým je určen směr DPH, závisí na typu účtu v dokladu. Směr DPH je určen kombinací typu účtu a kódu DPH. V následujících oddílech jsou uvedeny podrobnosti o možnostech. 

### <a name="account-type-is-project"></a>Typ účtu je Projekt.

Pokud má doklad řádek deníku, u kterého je typ účtu **Projekt**, budou všechny řádky deníku v dokladu používat stejný směr DPH. Následující obrázek znázorňuje pravidlo. Následující body znázorňují možné daňové pokyny pro účty projektu.

•   Pokud je kód DPH importní DPH, je směr DPH Importní DPH.

•   Pokud je kód DPH Osvobození od daně, je směr Nákup bez daně.

•   Pokud je kód DPH vnitřní DPH, je směr DPH Splatná DPH.

•   Pokud je kód DPH stornované účtování, je směr DPH Splatná DPH.

V opačném případě je směr DPH pohledávka DPH.

V následujícím diagramu je pravidlo znázorněno graficky.

![Možnosti daňových směrů pro účty projektu](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a>Typ účtu je Dodavatel

Pokud má doklad řádek deníku, u kterého je typ účtu **Dodavatel**, budou všechny řádky deníku v dokladu používat stejný směr DPH. Následující body znázorňují možné daňové pokyny pro účty dodavatele. 

•   Pokud je kód DPH importní DPH, je směr DPH Importní DPH.

•   Pokud je kód DPH Osvobození od daně, je směr Nákup bez daně.

•   Pokud je kód DPH vnitřní DPH, je směr DPH Splatná DPH.

•   Pokud je kód DPH stornované účtování, je směr DPH Splatná DPH.

V opačném případě je směr DPH pohledávka DPH.

V následujícím diagramu je pravidlo znázorněno graficky.

![Možnosti daňových směrů pro účty dodavatele](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a>Typ účtu je Zákazník.

Pokud má doklad řádek deníku, u kterého je typ účtu **Zákazník**, budou všechny řádky deníku v dokladu používat stejný směr DPH. Následující body znázorňují možné daňové pokyny pro účty zákazníka.

•   Pokud je kód DPH Osvobození od daně, je směr Nákup bez daně.

•   Pokud je kód DPH vnitřní DPH, je směr DPH Pohledávka DPH.

•   Pokud je kód DPH stornované účtování, je směr DPH Pohledávka DPH.

V opačném případě je směr DPH Splatná DPH.

V následujícím diagramu je pravidlo znázorněno graficky.

![Možnosti daňových směrů pro účty zákazníka](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a>Typ účtu je Hlavní kniha

Na následujícím obrázku je znázorněno pravidlo, které platí, pokud má doklad pouze řádky deníku, u nichž je typem účtu **Hlavní kniha**. Následující body znázorňují možné daňové pokyny pro účty hlavní knihy.

•   Pokud je kód DPH importní DPH, je směr DPH Importní DPH.

•   Pokud je kód DPH Osvobození od daně, je směr Nákup bez daně.

V opačném případě, je-li částka v deníku debetní (kladná), směr DPH je Pohledávka DPH; Pokud je částka deníku kreditní (záporná), směr DPH je Splatná DPH.

V následujícím diagramu je pravidlo znázorněno graficky.

![Možnosti daňových směrů pro účty hlavní knihy](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a>Přepis směru DPH

Směr DPH lze přepsat, pokud doklad obsahuje pouze řádky s typem účtu **hlavní kniha**.

Přejděte na **Hlavní kniha \> Účtová osnova \> Účty \> Hlavní účty** a vyberte pevnou záložku **Přepisy právnické osoby**.

## <a name="determine-the-sales-tax-amount"></a>Určení částky DPH

Tento oddíl popisuje, jak se vypočítává znak částky DPH.

![Stránka transakce DPH](media/sales-tax-amount-sign.jpg)

V následující tabulce je uvedeno obecné pravidlo pro určení znaménka částek DPH v dočasné tabulce DPH.

| Částka řádky deníku | Směr DPH  | Znak částky DPH |
|---------------------|----------------------|-----------------------|
| Kladné            | Pohledávky DPH | Kladné              |
| Kladné            | Splatná DPH    | Záporné              |
| Záporné            | Pohledávky DPH | Záporné              |
| Záporné            | Splatná DPH    | Kladné              |

Pro doklady, které mají pouze řádky **Projekt** nebo **Hlavní kniha**, existuje zvláštní pravidlo, když je na řádku **Hlavní kniha** vybrána skupina DPH nebo skupina DPH položky. Toto pravidlo je řízeno povolením funkce nezávislého výpočtu DPH pro hlavní deníky. Když je tato funkce vypnutá, částka daně na řádku **hlavní knihy** použije stranu má dáti/dal řádku **projektu**. Když je tato funkce zapnutá, částka daně na řádku **hlavní knihy** použije vlastní směr má dáti/dal. V následujících tabulkách jsou uvedena pravidla pro jednotlivé scénáře. 

**Pravidlo, když je funkce zapnutá**

| Částka řádky deníku projektu | Směr DPH  | Znak částky DPH |
|--------------------------------|----------------------|-----------------------|
| Kladné                       | Pohledávky DPH | Kladné              |
| Záporné                       | Pohledávky DPH | Záporné              |

**Pravidlo, když je funkce vypnutá**

| Částka řádky deníku hlavní knihy  | Směr DPH  | Znak částky DPH |
|--------------------------------|----------------------|-----------------------|
| Kladné                       | Pohledávky DPH | Kladné              |
| Záporné                       | Pohledávky DPH | Záporné              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a>Určete částku DPH a účet na dokladu

Při zaúčtování DPH se hlavní účet načte z profilu účetní skupiny hlavní knihy. Pokud jsou DPH pohledávky, systém použije účet pohledávek DPH, který je uveden v profilu. Pokud jsou DPH splatné, systém použije účet splatné DPH, který je uveden v profilu.

Následující tabulka zobrazuje obecné pravidlo.

| Směr DPH  | Znak částky DPH | Účet DPH      | Částka na dokladu |
|----------------------|-----------------------|------------------------|-------------------|
| Pohledávky DPH | Kladné              | Účet pohledávek | Kladný (debet)  |
| Pohledávky DPH | Záporné              | Účet pohledávek | Záporné (dal)  |
| Splatná DPH    | Kladné              | Účet závazků    | Záporné (dal)  |
| Splatná DPH    | Záporné              | Účet závazků    | Kladný (debet)  |
