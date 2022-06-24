---
title: Metody doplnění a modifikace množství
description: Tento článek obsahuje informace o metodách doplnění v Optimalizaci plánování Vysvětluje také, jak vícenásobné množství objednávky pro produkt ovlivňuje výsledek.
author: t-benebo
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d3e8ef3d38f1b9bacd89304aaf3f0350050232bd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873688"
---
# <a name="replenishment-methods-and-quantity-modification"></a>Metody doplnění a modifikace množství

[!include [banner](../../includes/banner.md)]

Tento článek obsahuje informace o metodách doplnění v Optimalizaci plánování Vysvětluje také, jak vícenásobné množství objednávky pro produkt ovlivňuje výsledek.

Metody doplňování jsou také známé jako metody pokrytí a metody stanovení velikosti šarže.

## <a name="coverage-codes"></a>Kódy pokrytí

Optimalizaci plánování lze nakonfigurovat tak, aby používalo různé metody doplnění. Metody doplňování jsou techniky, které systém používá k výpočtu požadavků na produkt. Metody doplňování jsou definovány kódy pokrytí, které můžete nastavit buď pro skupinu pokrytí, nebo pro produkt.

V optimalizaci plánování lze použít následující kódy pokrytí:

- **Období** - metoda doplnění kombinuje všechny požadavky na období do jedné objednávky pro daný produkt. Zakázka bude naplánována pro první den období a její množství bude plnit čisté požadavky během stanoveného období. Toto období začíná první poptávkou produktu a pokrývá určenou délku v čase. Další období bude začínat následujícími požadavky produktu. Kód pokrytí *Období* se často používá pro nepředvídatelné čerpání zásob, produkty ovlivněné sezónou nebo produkty s vysokou cenou. Následující obrázek znázorňuje příklad.

    ![Příklad použití kódu pokrytí období.](./media/coverage-code-period.png "Příklad použití kódu pokrytí období")

- **Požadavek** – v metodě doplňování systém vytváří plánovaný nákup, převod nebo výrobní zakázku podle požadavků na produkt. Tato metoda se používá pro drahé výrobky, které mají nestálou poptávku. Kód pokrytí *Požadavek* se často používá pro konfigurovatelné produkty nebo scénáře na objednávku. Následující obrázek znázorňuje příklad.

    ![Příklad použití kódu pokrytí požadavku.](./media/coverage-code-requirement.png "Příklad použití kódu pokrytí požadavku")

- **Min./Max.** - Metoda doplňování je založena na úrovni zásob. Definuje doplnění zásob až na určitou úroveň, když je předpokládaná úroveň po ruce pod určitou prahovou hodnotou. Množství doplnění bude rozdíl mezi maximální úrovní a předpokládanou úrovní zásob na skladě. *Min./Max.* kód pokrytí se často používá k předvídatelnému čerpání zásob, nejprodávanějším produktům nebo levnějším výrobkům. Následující obrázek znázorňuje příklad.

    ![Příklad použití kódu pokrytí Min./Max.](./media/coverage-code-min-max.png "Příklad použití kódu pokrytí Min./Max.")

- **Ruční** - v metodě doplňování systém nenavrhuje nákup, převod nebo výrobní objednávky pro daný produkt. Místo toho je plánovač produktu zodpovědný za vytvoření požadovaných objednávek pro doplnění produktu. *Ruční* kód pokrytí se často používá u produktů, pro které nejsou plánované objednávky generované systémem požadovány.

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a>Dopad množství objednávky na výchozí nastavení objednávky

Na stránce **Výchozí nastavení objednávky** s vydaným produktem můžete na stránce zadat každé z následujících nastavení množstv na pevných záložkách **Nákupní objednávka**, **Zásoby** a **Prodejní objednávka**. (Pevná záložka **Zásoby** se používá pro převodní příkazy a výrobní zakázky.)

- **Násobek** - Plánované objednávky budou násobkem tohoto množství.

    Například pokud je pole **Násobek** nastaveno na *5*, objednávka může být na množství 5, 10, 15, 20 atd.

- **Min. objednané množství** - Plánované objednávky nebudou menší než zadaná hodnota.

    Například pokud je pole **Min. objednané množství** nastaveno na *10*, bude vytvořena plánovaná objednávka na množství 10, i když k uspokojení poptávky jsou zapotřebí pouze čtyři.

- **Max. objednané množství** - Plánované objednávky nebudou překračovat zadanou hodnotu. Pokud je poptávka větší než hodnota **Max. objednané množství**, bude vytvořeno několik plánovaných objednávek, které ji pokryjí.

    Například pokud je pole **Max. objednané množství** nastaveno na *100* a poptávka je 450, budou vytvořeny čtyři plánované objednávky pro množství 100 a jedna plánovaná objednávka pro množství 50.

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a>Příklady doplňování, které používají min./max. kód pokrytí

Pokud nezadáte hodnotu v poli **Násobek** pro produkt na stránce **Výchozí nastavení objednávky**  a pokud používáte *Min./Max.* metodu doplnění, Optimalizace plánování doplní zásoby až na určitou úroveň, když je předpokládaná úroveň po ruce pod určitou prahovou hodnotou.

Pokud pro produkt definujete více množství, zobrazí se *Min./Max.* metoda doplňování mění své chování a bere v úvahu hodnotu **Násobek**.

Jinými slovy, Optimalizace plánování bude i nadále doplňovat inventář až na definovanou maximální úroveň, pokud je předpokládaná úroveň po ruce menší než definovaná minimální úroveň. Množství doplňování však musí být násobkem hodnoty **Násobek**.

Pokud množství doplňování (rozdíl mezi maximální úrovní a předpokládanou úrovní po ruce) není násobkem definovaného vícenásobného množství, Optimalizace plánování použije první možnou hodnotu, která spolu s předpokládanou úrovní na straně bude pod maximální úroveň. Pokud je součet nižší než minimální úroveň, použije optimalizace plánování první hodnotu, která bude spolu s předpovězenou hodnotou vyšší než maximální úroveň.

Následující podkapitoly poskytují několik příkladů, které ukazují, jak množství vícenásobné objednávky produktu ovlivňuje výsledek *Min./Max.* metodu doplnění.

### <a name="example-1"></a>Příklad 1

Produkt má následující konfiguraci:

- **Kód pokrytí:** *Min./Max.*
- **Minimum:** *15*
- **Maximum:** *22*
- **Násobek:** *0*

K dispozici je 10 kusů zásob na skladě a neexistuje žádná jiná poptávka nebo nabídka.

Když běží hlavní plánování, vytvoří se plánovaná objednávka na 12 kusů, aby se doplnily zásoby na maximální množství.

### <a name="example-2"></a>Příklad 2

Produkt má následující konfiguraci:

- **Kód pokrytí:** *Min./Max.*
- **Minimum:** *15*
- **Maximum:** *22*
- **Násobek:** *5*

K dispozici je 10 kusů zásob na skladě a neexistuje žádná jiná poptávka nebo nabídka.

Když běží hlavní plánování, vytvoří se plánovaná objednávka na 10 kusů (protože 15 kusů doplňování plus 10 kusů inventáře na skladě překročí maximální množství).

### <a name="example-3"></a>Příklad 3

Produkt má následující konfiguraci:

- **Kód pokrytí:** *Min./Max.*
- **Minimum:** *21*
- **Maximum:** *24*
- **Násobek:** *5*

K dispozici je 10 kusů zásob na skladě a neexistuje žádná jiná poptávka nebo nabídka.

Když běží hlavní plánování, vytvoří se plánovaná objednávka na 15 kusů (protože 10 kusů doplňování plus 10 kusů inventáře na skladě bude méně než minimální množství).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
