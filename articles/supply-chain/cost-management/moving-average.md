---
title: Klouzavý průměr
description: Klouzavý průměr je trvalá metoda nákladů založená na principu průměru, kde se náklady na skladový výdej nemění, když se mění nákupní ceny. Rozdíl je kapitalizován a je založen na proporcionálním výpočtu. Zbývající částka je zanesena do výdajů.
author: AndersGirke
manager: tfehr
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 65531
ms.assetid: dfd10099-8f7f-44b1-917e-df37c2fe8773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb0472a0d2ac9b552cd16e4d6bf516a876ea4a0e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981504"
---
# <a name="moving-average"></a>Klouzavý průměr

[!include [banner](../includes/banner.md)]

Klouzavý průměr je trvalá metoda nákladů založená na principu průměru, kde se náklady na skladový výdej nemění, když se mění nákupní ceny. Rozdíl je kapitalizován a je založen na proporcionálním výpočtu. Zbývající částka je zanesena do výdajů.

Při použití klouzavého průměru nejsou podporována vyrovnání a označení zásob. Uzávěrka skladu nemá vliv na produkty, které mají klouzavý průměr jako skupinu skladových modelů, a negeneruje žádná vyrovnání mezi transakcemi.

Následují předpoklady pro použití klouzavého průměru nákladů jako nákladové metody.

1. Na stránce **Skupiny modelů položek** nastavte skupinu modelů položky, u kterých je vybrán **Klouzavý průměr** v poli **Skladový model** .

    > [!NOTE]
    > Ve výchozím nastavení po výběru **Klouzavý průměr** jsou vybrána také pole **Zaúčtovat fyzické zásoby** a **Zaúčtovat finanční zásoby** .

1. Na stránce **Zaúčtování** přiřaďte účty k **Cenová odchylka pro klouzavý průměr** . Můžete použít účet **Cenová odchylka pro klouzavý průměr** , když mají náklady být proporcionálně zaneseny. K tomu dochází v následujících dvou scénářích:
    - Existuje rozdíl nákladů mezi nákupním příjmem a nákupní fakturou kvůli rozdílu mezi původním množstvím zásob a aktuálním množstvím na skladě.
    - Transakce přinášejí zásoby ze záporných hodnot na nulu a existuje rozdíl mezi transakčními náklady a aktuálními klouzavými průměrnými náklady.

1. Na stránce **Zaúčtování** přiřaďte účty k účtům **Přecenění nákladů pro klouzavý průměr** na kartě **Zásoby** . Účet **Přecenění nákladů pro klouzavý průměr** použijte, pokud chcete upravit klouzavý průměr nákladů pro produkt na novou cenu jednotky.

1. Na stránce **Uvolněné produkty** přiřaďte skupinu modelu položky klouzavého průměru k produktu.

    > [!NOTE]
    > Proces uzávěrky skladu pouze uzavírá účetní období. Neovlivňuje produkty, které mají přiřazený klouzavý průměr jako skupinu modelů zboží.

## <a name="convert-to-the-moving-average-costing-method"></a>Převedení na metodu klouzavého průměru nákladů

Produkty je možné převést tak, aby používaly metodu klouzavého průměru pro ocenění skladu. Tento druh převodu je obvykle prováděn na konci roku po uzavření posledního měsíce aktuálního roku. To se provádí pomocí aktuálního nákladového modelu výrobku. Nákladovou metodu pro sklad můžete změnit z nákladové metody průměrných nákladů nebo standardních nákladů na metodu , která je založena na klouzavém průměru.

Chcete-li změnit metodu výpočtu nákladů ze standardní nákladové metody na metodu klouzavého průměru, je nutné provést následující úkoly:

1. Upravte množství zásob a hodnoty na 0 (nula).
1. Po nastavení skladové hodnoty a množství na 0 (nula) změňte skupinu modelu zboží na klouzavý průměr.
1. Úpravou nastavte množství a hodnotu zpět na sklad.

Nelze změnit metodu ocenění skladu z metody klouzavého průměru na metodu FIFO, LIFO nebo metodu váženého průměru.

> [!NOTE]
> Převod ze standardních nákladů na klouzavý vážený průměr je ruční proces.

V následujících příkladech je znázorněn dopad použití metody klouzavého průměru nákladů. Existují čtyři konfigurace:

- Nákupní objednávka a proporcionální rozdíl nákladů zanesený do výdajů
- Úpravy klouzavého průměru pro produkt a zásoby
- Klouzavý průměr pro výrobu
- Klouzavý průměr s datovanou transakcí

## <a name="purchase-order-and-proportionally-expensed-cost-difference"></a>Nákupní objednávka a proporcionální rozdíl nákladů zanesený do výdajů

S klouzavým průměrem jsou ceny produktu určeny nákupní příjemkou. Při zaúčtování nákupní objednávky, pokud existuje rozdíl v nákladech mezi nákupní příjemkou a nákupní fakturou, je rozdíl proporcionálně upraven pro aktuální produkty na skladě a zbývající částka je zanesena do výdajů.

V tomto příkladu je vytvořena nákupní objednávka a přijata s jednou cenou a nákupní faktura je zaúčtována s jinou cenou.

1. Vytvořte nákupní objednávku pro množství 2 a jednotkovou cenu ve výši 10,00.
1. Vytvořte nákupní příjemku pro produkt.
1. Vytvořte prodejní objednávku pro množství 1 a jednotkovou cenu ve výši 10,00.
1. Vytvořte nákupní fakturu pro množství 2 a jednotkovou cenu ve výši 12,00.

Rozdíl jednotkové ceny 2,00 bude zaúčtován do cenové odchylky pro účet klouzavého průměru při zaúčtování nákupní faktury. Důvodem je, že byly zakoupeny dva produkty v ceně 20,00. Jeden nebo více produktů byly prodány za jednotkovou cenu ve výši 10,00. Nákupní faktura byla zaúčtována za pořizovací cenu 12,00 s množstvím 2. Jednotková cena produktu nemůže být zaúčtována ve 14.00.

## <a name="moving-average-product-and-inventory-adjustment"></a>Úpravy klouzavého průměru pro produkt a zásoby

Pokud je nutné upravit klouzavý průměr nákladů produktu, jsou povoleny úpravy zásob k dnešnímu datu. Nelze zpětně datovat úpravy zásob pro korekci klouzavého průměru nákladů produktu. Nemůže mít tok nákladů skrze následné transakce.

V tomto příkladu se upraví klouzavý průměr nákladů pro produkt.

1. Vyberte produkt, pro který chcete upravit klouzavý průměr nákladů. 

 > [!NOTE]
 > Stránka **Přecenění pro klouzavý průměr** ověřuje dostupné zásoby pro produkt. Vybraný produkt má zaúčtované množství 1, zaúčtovanou hodnotu 12,00, zaúčtované jednotkové náklady 12,00 a jednotkové náklady 12,00.
    
1. Aktualizujte pole **Jednotková cena** na 16,00. Systém vypočítá zbývající pole.
1. Úpravy jsou zaúčtovány.

> [!NOTE]
> Lze upravit pouze klouzavý průměr nákladů k dnešnímu datu.

Na stránce **Vyrovnání pro doklad** se zobrazí úpravy 4,00 zaúčtované do účtu Přecenění nákladů pro klouzavý průměr.

## <a name="moving-average-with-production"></a>Klouzavý průměr pro výrobu

Klouzavý průměr podporuje vyrobené položky. Pokud chcete použít klouzavý průměr v provozním prostředím, vyberte **Použít odhadovanou nákladovou cenu** na stránce **Parametry modulu Řízení výroby** . To znamená, že nákladová cena, která se vypočítá během odhadu, bude použita místo skutečné nákladové ceny z výpočtu v kusovníku.

## <a name="moving-average-with-a-backdated-transaction"></a>Klouzavý průměr s datovanou transakcí

Zpětně datované transakce jsou přiřazeny k aktuálnímu klouzavému průměru nákladů a aktualizuje se fyzické množství produktu, ale neovlivní se klouzavý průměr nákladů produktu. V tomto příkladu klouzavého průměru je zaúčtována zpětně datovaná transakce pro klouzavý průměr produktu.

1. Vytvořte úpravy zásob pro klouzavý průměr produktu na množství 1 a cenu 20,00.
1. Historie transakcí zásob produktu bude vypadat takto:
    - Skladová transakce 1 s náklady 16,00, datem zaúčtování 15. ledna a datem transakce 15. ledna.
    - Skladová úprava 1 s náklady 20,00, datem zaúčtování 1. ledna a datem transakce 15. ledna.
1. Zaúčtujte úpravu.

Na stránce **Skladové transakce** vidíte, že 4,00 je zaneseno do výdajů, protože aktuální klouzavý průměr produktu je 16,00. Lze zaúčtovat v minulosti, ale rozdíl v nákladech se zanese do výdajů, takže klouzavý průměr nákladů se nezmění.

## <a name="negative-inventory-balances"></a>Záporné zůstatky zásob

Transakce jsou zpracovávány odlišně v závislosti na tom, zda je nové množství na skladě po transakci záporné, nulové nebo kladné.

### <a name="new-balance-is-negative-or-zero"></a>Nový zůstatek je záporný nebo nulový

Pokud je nové množství na skladě záporné nebo nulové, náklady na transakci se vypočítají podle aktuálních průměrných nákladů. Pokud existuje rozdíl mezi kupní cenou a aktuálními průměrnými náklady, zaúčtuje se na účet **Cenová odchylka pro klouzavý průměr** .

### <a name="new-balance-is-positive"></a>Nový zůstatek je kladný

Pokud je nové množství na skladě po transakci kladné, transakce se rozdělí na dvě části a náklady se vypočítají odlišně, jak je shrnuto v následující tabulce.

| Součást | popis |
|---|---|
| Záporné až nulové množství | Zásoby použijí aktuální klouzavé průměrné náklady na položku namísto transakčních nákladů pro tu část množství příjmu, která zvyšuje zůstatek na skladě ze záporného na nulový. Rozdíl mezi transakčními náklady a aktuálními klouzavými průměrnými náklady se zaúčtuje na účet **Cenová odchylka pro klouzavý průměr** . |
| Nulové až kladné množství | Sklad používá transakční náklady pro tu část množství příjmu, která zvyšuje zůstatek na skladě z nuly na kladnou hodnotu.                                                  |

## <a name="inventory-value-report"></a>Sestava hodnoty zásob

V tomto příkladu klouzavého průměru je sestava hodnoty skladu vytištěna pro podporu výpočtu aktuálního klouzavého průměru pro produkt. Sestava hodnoty zásob může vytisknout transakce v chronologickém pořadí společně s náklady pro podporu výpočtu klouzavého průměru nákladů pro produkt. Sestava obsahuje klouzavý průměr nákladů pro produkt. V dialogovém okně **Sestavy hodnot zásob** umožňuje pole intervalu dat vybrat **Čas transakce** nebo **Datum zaúčtování** pro seřazení sestavy. Možnost **Datum zaúčtování** určuje, jak je obvykle sestava vytištěna. Možnost **Čas transakce** je aktuální datum vytvoření sestavy transakce a aktualizace klouzavého průměru nákladů pro produkt. Můžete vytisknout sestavu hodnot zásob pomocí možnosti **Řazení času transakce** v případě, že chcete vidět výpočet klouzavého průměru nákladů v čase. Následující tabulka zobrazuje transakce pro produkt, pro který je sestava vytištěna, když použijete možnost **Řazení času transakce** .

| Čas transakce | Datum         | Typ transakce           | Množství | Částka | Průměrné náklady na jednotku |
|------------------|--------------|----------------------------|----------|--------|-------------------|
|                  | 1. říjen    | Počáteční zůstatek          | 0        | 0,00   | 0,00              |
| 8. říjen        | 28. září | Zpětně datovaný příjem          | 1        | 16,00  | 16,00             |
| 3. říjen        | 3. říjen    | Nákupní příjemka           | 2        | 20,00  | 12,00             |
| 5. říjen        | 5. říjen    | Prodejní objednávka                | -1       | -10,00 | 13,00             |
| 7. říjen        | 7. říjen    | Nákupní faktura           |          | 2,00   | 14,00             |
| 8. říjen        | 8. říjen    | Přecenění klouzavého průměru |          | 4.00   | 16.00             |
|                  | 31. říjen   | Celkem                      | 2        | 32.00  | 16.00             |

> [!NOTE]
> Odsouhlasení hlavní knihy se zásobami pomocí možnosti **Řazení času transakce** není možné. Sestava musí být vytištěna pomocí možnosti **Datum zaúčtování** .
