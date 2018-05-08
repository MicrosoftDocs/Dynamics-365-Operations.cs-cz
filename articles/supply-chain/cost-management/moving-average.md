---
title: "Klouzavý průměr"
description: "Klouzavý průměr je trvalá metoda nákladů založená na principu průměru, kde se náklady na skladový výdej nemění, když se mění nákupní ceny. Rozdíl je kapitalizován a je založen na proporcionálním výpočtu. Zbývající částka je zanesena do výdajů."
author: AndersGirke
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 65531
ms.assetid: dfd10099-8f7f-44b1-917e-df37c2fe8773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c1f8a8cf4a58177d423709f245760a5ba9ca7e4e
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="moving-average"></a>Klouzavý průměr

[!include [banner](../includes/banner.md)]

Klouzavý průměr je trvalá metoda nákladů založená na principu průměru, kde se náklady na skladový výdej nemění, když se mění nákupní ceny. Rozdíl je kapitalizován a je založen na proporcionálním výpočtu. Zbývající částka je zanesena do výdajů. 

Při použití klouzavého průměru nejsou podporována vyrovnání a označení zásob. Uzávěrka skladu nemá vliv na produkty, které mají klouzavý průměr jako skupinu skladových modelů, a negeneruje žádná vyrovnání mezi transakcemi.

Následují předpoklady pro použití klouzavého průměru nákladů jako nákladové metody.

1.  V poli **Skupiny modelů položek** nastavte skupinu modelů položky, u kterých je vybrán Klouzavý průměr v poli **Skladový model**. **Poznámka:** Ve výchozím nastavení po výběru klouzavého průměru jsou vybrána také pole **Zaúčtovat fyzické zásoby** a **Zaúčtovat finanční zásoby**. 

2.  Na stránce **Zaúčtování** přiřaďte účty do účtů **Cenová odchylka pro klouzavý průměr** a **Přecenění nákladů pro klouzavý průměr** na kartě **Zásoby**. Použijte účet **Cenová odchylka pro klouzavý průměr**, pokud musí být náklady proporcionálně zanesené do výdajů. K tomu dochází v důsledku rozdílů nákladů mezi nákupním příjmem a nákupní fakturou, a kvůli rozdílu mezi původním množstvím zásob a aktuálním množstvím na skladě. Účet **Přecenění nákladů pro klouzavý průměr** můžete použít, pokud chcete upravit klouzavý průměr nákladů na produkt pro novou jednotkovou cenu.
3.  Na stránce **Uvolněné produkty** přiřaďte skupinu modelu položky klouzavého průměru k produktu. **Poznámka:** Proces uzávěrky skladu pouze uzavírá účetní období. Neovlivňuje produkty, které mají přiřazený klouzavý průměr jako skupinu modelů zboží.

## <a name="convert-to-the-moving-average-costing-method"></a>Převedení na metodu klouzavého průměru nákladů
Produkty je možné převést tak, aby používaly metodu klouzavého průměru pro ocenění skladu. Tento druh převodu je obvykle prováděn na konci roku po uzavření posledního měsíce aktuálního roku. To se provádí pomocí aktuálního nákladového modelu výrobku. Nákladovou metodu pro sklad můžete změnit z nákladové metody průměrných nákladů nebo standardních nákladů na metodu , která je založena na klouzavém průměru. 

Chcete-li změnit metodu výpočtu nákladů ze standardní nákladové metody na metodu klouzavého průměru, je nutné provést následující úkoly:

1.  Upravte množství zásob a hodnoty na 0 (nula).
2.  Po nastavení skladové hodnoty a množství na 0 (nula) změňte skupinu modelu zboží na klouzavý průměr.
3.  Úpravou nastavte množství a hodnotu zpět na sklad.

Nelze změnit metodu ocenění skladu z metody klouzavého průměru na metodu FIFO, LIFO nebo metodu váženého průměru.

**Poznámka:** Převod ze standardních nákladů na klouzavý vážený průměr je ruční proces.

V následujících příkladech je znázorněn dopad použití metody klouzavého průměru nákladů. Existují čtyři konfigurace:
-   Nákupní objednávka a proporcionální rozdíl nákladů zanesený do výdajů
-   Úpravy klouzavého průměru pro produkt a zásoby
-   Klouzavý průměr pro výrobu
-   Klouzavý průměr s datovanou transakcí

## <a name="purchase-order-and-proportionally-expensed-cost-difference"></a>Nákupní objednávka a proporcionální rozdíl nákladů zanesený do výdajů
S klouzavým průměrem jsou ceny produktu určeny nákupní příjemkou. Při zaúčtování nákupní objednávky, pokud existuje rozdíl v nákladech mezi nákupní příjemkou a nákupní fakturou, je rozdíl proporcionálně upraven pro aktuální produkty na skladě a zbývající částka je zanesena do výdajů. 

V tomto příkladu je vytvořena nákupní objednávka a přijata s jednou cenou a nákupní faktura je zaúčtována s jinou cenou.

1.  Vytvořte nákupní objednávku pro množství 2 a jednotkovou cenu ve výši 10,00.
2.  Vytvořte nákupní příjemku pro produkt.
3.  Vytvořte prodejní objednávku pro množství 1 a jednotkovou cenu ve výši 10,00.
4.  Vytvořte nákupní fakturu pro množství 2 a jednotkovou cenu ve výši 12,00.

Rozdíl jednotkové ceny 2,00 bude zaúčtován do cenové odchylky pro účet klouzavého průměru při zaúčtování nákupní faktury. Důvodem je, že byly zakoupeny dva produkty v ceně 20,00. Jeden nebo více produktů byly prodány za jednotkovou cenu ve výši 10,00. Nákupní faktura byla zaúčtována za pořizovací cenu 12,00 s množstvím 2. Jednotková cena produktu nemůže být zaúčtována ve 14.00.

## <a name="moving-average-product-and-inventory-adjustment"></a>Úpravy klouzavého průměru pro produkt a zásoby
Pokud je nutné upravit klouzavý průměr nákladů produktu, jsou povoleny úpravy zásob k dnešnímu datu. Nelze zpětně datovat úpravy zásob pro korekci klouzavého průměru nákladů produktu. Nemůže mít tok nákladů skrze následné transakce. 

V tomto příkladu se upraví klouzavý průměr nákladů pro produkt.

1.  Vyberte produkt, pro který chcete upravit klouzavý průměr nákladů. **Poznámka:** Stránka **Přecenění pro klouzavý průměr** ověřuje dostupné zásoby pro produkt. Vybraný produkt má zaúčtované množství 1, zaúčtovanou hodnotu 12,00, zaúčtované jednotkové náklady 12,00 a jednotkové náklady 12,00.
2.  Aktualizujte pole **Jednotková cena** na 16,00. Systém vypočítá zbývající pole.
3.  Úpravy jsou zaúčtovány.

**Poznámka:** Lze upravit pouze klouzavý průměr nákladů k dnešnímu datu.

Na stránce **Vyrovnání pro doklad** se zobrazí úpravy 4,00 zaúčtované do účtu Přecenění nákladů pro klouzavý průměr.

## <a name="moving-average-with-production"></a>Klouzavý průměr pro výrobu
Klouzavý průměr podporuje vyrobené položky. Pokud chcete použít klouzavý průměr v provozním prostředím, vyberte posuvník **Použít odhadovanou nákladovou cenu** na stránce **Parametry modulu Řízení výroby**. To znamená, že nákladová cena, která se vypočítá během odhadu, bude použita místo skutečné nákladové ceny z výpočtu v kusovníku.

## <a name="moving-average-with-a-backdated-transaction"></a>Klouzavý průměr s datovanou transakcí
Zpětně datované transakce jsou přiřazeny k aktuálnímu klouzavému průměru nákladů a aktualizuje se fyzické množství produktu, ale neovlivní se klouzavý průměr nákladů produktu. V tomto příkladu klouzavého průměru je zaúčtována zpětně datovaná transakce pro klouzavý průměr produktu.

1.  Vytvořte úpravy zásob pro klouzavý průměr produktu na množství 1 a cenu 20,00.
2.  Historie transakcí zásob produktu bude vypadat takto:
    -   Skladová transakce 1 s náklady 16,00, datem zaúčtování 15. ledna a datem transakce 15. ledna.
    -   Skladová úprava 1 s náklady 20,00, datem zaúčtování 1. ledna a datem transakce 15. ledna.
3.  Zaúčtujte úpravu.

Na stránce **Skladové transakce** vidíte, že 4,00 je zaneseno do výdajů, protože aktuální klouzavý průměr produktu je 16,00. Lze zaúčtovat v minulosti, ale rozdíl v nákladech se zanese do výdajů, takže klouzavý průměr nákladů se nezmění.

## <a name="inventory-value-report"></a>Sestava hodnoty zásob
V tomto příkladu klouzavého průměru je sestava hodnoty skladu vytištěna pro podporu výpočtu aktuálního klouzavého průměru pro produkt. Sestava hodnoty zásob může vytisknout transakce v chronologickém pořadí společně s náklady pro podporu výpočtu klouzavého průměru nákladů pro produkt. Sestava obsahuje klouzavý průměr nákladů pro produkt. V dialogovém okně **Sestavy hodnot zásob** umožňuje pole Intervalu dat vybrat **Čas transakce** nebo **Datum zaúčtování** pro seřazení sestavy. Možnost **Datum zaúčtování** určuje, jak je obvykle sestava vytištěna. Možnost **Čas transakce** je aktuální datum vytvoření sestavy transakce a aktualizace klouzavého průměru nákladů pro produkt. Můžete vytisknout sestavu hodnot zásob pomocí možnosti**Řazení času transakce** v případě, že chcete vidět výpočet klouzavého průměru nákladů v čase. Následující tabulka zobrazuje transakce pro produkt, pro který je sestava vytištěna, když použijete možnost **Řazení času transakce**.

| Čas transakce | Datum         | Typ transakce           | Množství | Částka | Průměrné náklady na jednotku |
|------------------|--------------|----------------------------|----------|--------|-------------------|
|                  | 1. říjen    | Počáteční zůstatek          | 0        | 0,00   | 0,00              |
| 8. říjen        | 28. září | Zpětně datovaný příjem          | 1        | 16,00  | 16,00             |
| 3. říjen        | 3. říjen    | Nákupní příjemka           | 2        | 20,00  | 12,00             |
| 5. říjen        | 5. říjen    | Prodejní objednávka                | -1       | -10,00 | 13,00             |
| 7. říjen        | 7. říjen    | Nákupní faktura           |          | 2,00   | 14,00             |
| 8. říjen        | 8. říjen    | Přecenění klouzavého průměru |          | 4,00   | 16.00             |
|                  | 31. říjen   | Celkem                      | 2        | 32.00  | 16.00             |

 **Poznámka:** Odsouhlasení hlavní knihy se zásobami pomocí možnosti **Řazení času transakce** není možné. Sestava musí být vytištěna pomocí možnosti **Datum zaúčtování**.






