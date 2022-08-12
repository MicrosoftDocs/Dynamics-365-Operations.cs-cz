---
title: Obchodní dokumenty podporované globálním účtováním zásob
description: V tomto článku je uveden seznam obchodních dokumentů, které jsou podporovány globálních účtováním zásob. Poskytuje také podrobný příklad pro dokumenty nákupní objednávky.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0dee558de2defa7baae4bc4097c750e974c12a14
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135682"
---
# <a name="business-documents-supported-by-global-inventory-accounting"></a>Obchodní dokumenty podporované globálním účtováním zásob

[!include [banner](../includes/banner.md)]

Poté, co je doplněk globálního účtování zásob plně nastaven, je připraven zpracovat dokumenty související se zásobami, které jsou zadány v Microsoft Dynamics 365 Supply Chain Management.

## <a name="supported-business-documents"></a>Podporované obchodní dokumenty

Existují dva typy obchodních dokumentů:

- **Dokumenty, které mají deník** - Mezi tyto dokumenty patří doklad o přijetí produktu, nákupní faktura, dodací list a prodejní faktura.
- **Dokumenty, které nemají deník** - Mezi tyto dokumenty patří dokumenty o počítání, pohybu a úpravách zásob.

Později v tomto článku budou nákupní objednávky použity jako příklad pro ilustraci procesu.

V následující tabulce jsou uvedeny dokumenty, které aktuální vydaná verze podporuje.

| Typ dokumentu       | Doklad        |
|--------------------|-----------------|
| Nákupní objednávka     | Příjem produktu |
| Nákupní objednávka     | Faktura         |
| Prodejní objednávka        | Dodací list    |
| Prodejní objednávka        | Faktura         |
| Skladové deníky | Přesun        |
| Skladové deníky | Úprava      |
| Skladové deníky | Inventura        |
| Skladové deníky | Převod        |
| Objednávka převozu     | Dodávka        |
| Objednávka převozu     | Přijmout         |

> [!IMPORTANT]
> Globální účetnictví zásob asynchronně zpracovává dokumenty, které jsou zadávány do Supply Chain Management. U problémových dokumentů se nebudou zobrazovat žádné chybové zprávy.

## <a name="example-purchase-order"></a>Příklad: nákupní objednávka

### <a name="product-receipt"></a>Příjemka produktu

Zaúčtujte příjmy z produktu obvyklým způsobem. Na stránce **Všechny nákupní objednávky** vyberte nákupní objednávku a poté v podokně akcí na kartě **Příjem** vyberte **Příjemka produktu** a otevřete stránku **Deník příjmu produktu**. Pro každý řádek se vygeneruje událost operace a událost Global Invntroy Accounting. Proto vyberte kartu **Řádky** a poté vyberte **Zásoby \> Události a měření** pro otevření stránky **Události a měření**.

Global Inventory Accounting je účetní systém založený na událostech a měřeních. Mřížka měřicího řádku na stránce **Události a měření** zobrazuje seznam měření. Každé měření má seznam rozměrů.

Pro každou událost operace existují dva typy měření:

- **Provozní měření** - Tato měření obecně popisují obchodní dokumenty. Jedno měření je množství produktu pomocí měrné jednotky použité v dokumentu. K dispozici jsou také měření, která ovlivňují hodnotu zásob, jako je rozšířená cena, sleva, procentuální částka slevy a řádkový poplatek.
- **Měření účtování zdrojů** - Tato měření jsou z pohledu inventárního registru. Popisují dopad dokumentu na zásoby v měrné jednotce zásob. Pokud existuje více registrací inventáře, existuje několik řádků měření účtování prostředků.

Dimenze jsou uspořádány následujícím způsobem:

- **Dualita** - Dualita popisuje agenty, kteří se účastní ekonomických událostí. U externích obchodních dokumentů popisuje primární dimenze právní subjekt, do kterého je dokument zadán, zatímco duální dimenze popisuje dodavatele, zákazníka atd. U interních obchodních dokumentů (například převodních objednávek) popisují duální dimenze protipoložkový sklad.
- **Typ dimenzí** - Typy dimenzí kategorizují dimenze.
- **Dimenze** - Název dimenze.
- **Hodnota dimenze** - Hodnota dimenze.

### <a name="global-inventory-accounting-event"></a>Událost globálního účetnictví zásob

Globální účetnictví zásob bere provozní události a měření jako vstup. Poté provede příslušné účtování pro každou související účetní knihu na základě připojené měny a konvence. Můžete vybrat **Událosdti globálního účetnictví zásob a měření** pro zobrazení události Globálního účetnictví zísob. Událost Globálního účetnictví zásob se řídí stejnou metodikou jako provozní události, ale používá různá měření. Existují tři hlavní typy měření: množství nákladů na produkt, cena produktu a odchylka.

Účty podřízené knihy se používají k další klasifikaci měření. Mohlo by existovat více účetních knih. Tyto účetní knihy jsou propojeny s právnickou osobou, kde je dokument zadán. Můžete zobrazit události a měření pro každou knihu změnou hodnoty pole **účetní kniha**.

### <a name="cost-element"></a>Prvek nákladů

Na základě zásady nákladových prvků, která je připojena k účetní knize, systém přiřadí nákladový prvek každému měření účtované provozní události, které ovlivňuje náklady na zásoby. Tato měření zahrnují rozšířenou cenu, slevu, procento slevy a poplatek za linku.

### <a name="measurement-line-details"></a>Podrobnosti řádku měření

Karta **Přehled** uvádí podrobnosti připojených zásad. Dimenze nákladového objektu ukazují nákladový objekt na základě zásady nákladového objektu. Specifické identifikační rozměry ukazují číslo šarže, pokud je předpoklad toku nákladů *Specifické - dávka*.

### <a name="purchase-invoice"></a>Nákupní faktura

Zaúčtujte fakturu obvyklým způsobem. Poté v podokně akcí na kartě **Faktura** ve skupině **Deníky** vyberte **Fakturu** a otevřete deník faktur. Pro každý řádek se vygeneruje událost operace a událost Globálního účetnictví zásob. Proto vyberte kartu **Řádky** a poté vyberte **Zásoby \> Události a měření** pro otevření stránky **Události a měření**. Stránka **Události a měření** zobrazuje stejný typ měření. Protože však stránka zobrazuje jinou roli měření a modifikátor měření, dopad na agenta (právnickou osobu) se liší.

Vyberte **Události globálního účetnictví zásob a měření** pro zobrazení události Globálního účetnictví zísob. Množství a náklady na zásoby nyní plynou z účtu podřízené knihy *Zboží přijato, nevyfakturovaný inventář* a do účtu podřízené knihy *Náklady na zakoupené zboží*.
