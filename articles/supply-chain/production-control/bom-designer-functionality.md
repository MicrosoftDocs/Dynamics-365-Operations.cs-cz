---
title: "Funkce návrháře kusovníku"
description: "Toto téma popisuje, jak můžete na stránce Návrhář kusovníku navrhnout a používat stromové struktury pro kusovníky (BOM)."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMDesigner
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 20981
ms.assetid: 2b92eec1-d28c-4965-9086-939c77b3c62b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 41f629401731920a9cb6443ada8b1a34a70e8da9
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="bom-designer-functionality"></a>Funkce návrháře kusovníku

[!include[banner](../includes/banner.md)]


Toto téma popisuje, jak můžete na stránce Návrhář kusovníku navrhnout a používat stromové struktury pro kusovníky (BOM). Kliknutím na možnost Nastavení můžete vybrat různé konfigurace a určit, které informace mají být zobrazeny v rámci jednotlivých liniích stromu.

Otevřete-li stránku **Návrhář Kusovníku** ze stránky **Uvolněné produkty**, zobrazí se na ní hierarchie kusovníků (BOM), které jsou aktivní a schválené pro vybranou položku, výchozí objednací web položky a skutečné datum.  

Kliknutím na tlačítko **Filtr** změňte počáteční výběr v zobrazení. Nastavením principu zobrazení na možnost **Vybrané/Aktivní nebo Vybrané** můžete vybrat jednotlivé verze kusovníku nebo postupu pro použití v zobrazení. Můžete vybrat neschválené a neaktivní verze kusovníku pro zobrazení či správu v návrháři kusovníku.  

**Poznámka:** Otevřete-li návrhář kusovníku ze stránky seznamu **Kusovníky**, nezobrazí se informace o postupu. V současné době je výběr verze kusovníku nebo postupu vlastností verze kusovníku a postupu a platí pro všechny instance návrháře kusovníku.  

V následujících částech naleznete popis funkcí, které jsou k dispozici na různých kartách návrháře kusovníku.

## <a name="analyzing-a-bom-structure-by-using-the-bom-designer"></a>Analýza struktury kusovníku pomocí návrháře kusovníku
Návrhář kusovníku má dvě části:

-   Stromové zobrazení struktury kusovníku.
-   Oddíl podrobností zobrazující podrobnosti o vybraných datech. Při výběru uzlu ve stromovém zobrazení se pevné záložky v části Podrobnosti aktualizují na základě daného uzlu:
    -   **Podrobnosti řádku kusovníku** – zobrazí podrobnosti o řádku kusovníku, který je vybrán ve stromovém zobrazení.
    -   **Data položky** – zobrazí podrobnosti hlavní položky nebo položky, která se používá ve vybraném uzlu. Můžete kliknout na **Upravit uvolněný produkt** a upravit vybranou položku.
    -   **Kusovník** – zobrazí záhlaví kusovníku, který souvisí s vybraným uzlem.
    -   **Postup** – zobrazí záhlaví postupu, který souvisí s vybraným uzlem.
    -   **Operace postupu** – zobrazuje přehled operací daného postupu. Pokud je vybrán řádek kusovníku, který je přiřazen k určité operaci, operace je označena jako **Komponenta potřebná v operacích**.

## <a name="selecting-a-bom-and-route"></a>Výběr kusovníku a postupu
Filtr, který je použit pro kusovník a postup se zobrazí v záhlaví návrháře kusovníku. Filtr lze změnit pomocí dialogového okna **Filtr**. Pole tohoto dialogového pole jsou popsána v následující tabulce.

<table>
<thead>
<tr class="header">
<th>Pole</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Dimenze produktu</td>
<td>Pokud je vybraný hotový produkt základním produktem, můžete u hlavního výběru definovat aktivní dimenze produktu. <strong>Poznámka:</strong> Pokud otevřete návrhář kusovníku pro produkt, který není základní, v dialogovém okně <strong>Filtr</strong> nebude možné vybrat žádné dimenze produktu.</td>
</tr>
<tr class="even">
<td>Lokalita</td>
<td>Změňte pracoviště pro které je zobrazen strom kusovníku. Výchozí pracoviště je výchozím skladovým pracovištěm dokončené položky.</td>
</tr>
<tr class="odd">
<td>Pravidlo zobrazení</td>
<td>Vyberte princip zobrazení verze, který se vztahuje na aktuální strukturu kusovníku a na aktuální postup:
<ul>
<li>Je-li pro princip nastavena hodnota <strong>Aktivní nebo Vybrané/Aktivní</strong>, je nalezena verze postupu nebo kusovníku pro toto datum.</li>
<li>Je-li pro princip nastavena hodnota <strong>Vybrané/Aktivní nebo Vybrané</strong>, můžete vybrat verzi kusovníku nebo verzi postupu kliknutím na položky <strong>Kusovník</strong>&gt; <strong>Verze kusovníku</strong> nebo <strong>Postup</strong> &gt; <strong>Verze postupu</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Datum verze</td>
<td>Zadejte datum verze pro kusovník a postup. Pomocí dané verze lze identifikovat verzi kusovníku, která má být použita pro určité datum, jak je určeno daty verze v nastavení verze kusovníku.</td>
</tr>
<tr class="odd">
<td>Od množství</td>
<td>Filtrovat verze můžete výběrem specifika z množství. Nastavíte-li hodnotu, lze vybrat jiné verze kusovníku a postupu.</td>
</tr>
<tr class="even">
<td>Zobrazit pouze platné</td>
<td>Pokud zaškrtnete toto políčko, budou ve struktuře stromu zobrazeny pouze řádky kusovníku s platnými daty. Dvojitým kliknutím nebo kliknutím pravým tlačítkem myši na řádek kusovníku můžete otevřít stránku <strong>Upravit řádek kusovníku</strong>, kde můžete vidět data platnosti pro daný řádek kusovníku.</td>
</tr>
</tbody>
</table>

Použijete-li návrhář kusovníku ke kontrole nebo úpravě kusovníků, které se skládají z jedné nebo více úrovní fiktivních kusovníků, pak postup, který je přidružen k nejvyšší položce, obvykle zahrnuje celou hierarchii kusovníku. Pro zjednodušení přehledu můžete uzamknout postup nejvyšší úrovně v zobrazení kliknutím na tlačítko **Zobrazení** &gt; **Uzamknout postup**. Postup můžete odemknout kliknutím na položky **Zobrazení** &gt; **Odemknout postup**.

## <a name="adding-and-editing-boms-and-bom-lines"></a>Přidávání a úprava kusovníků a řádků kusovníku
Použijte funkce **Řádky kusovníku**nebo **Kusovník** k úpravě kusovníku nebo řádků kusovníku. Když vyberete uzel ze stromu, typ uzlu určí, které z funkcí budou k dispozici.

| Funkce                            | popis                                                                                               | Typ a podmínky uzlu                                                                                                                                                                                                                                                                       |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Řádky kusovníku &gt; Upravit                 | Otevřete dialogové okno, ve kterém můžete upravit atributy řádku kusovníku.                                             | Tato funkce je k dispozici, pokud je vybrán uzel řádku kusovníku.                                                                                                                                                                                                                                   |
| Řádky kusovníku &gt; Odstranit               | Odstraní řádek kusovníku z vybraného kusovníku.                                                                  | Tato funkce je dostupná, když je vybrán uzel řádku kusovníku a kusovník není uzamčen pro úpravy.                                                                                                                                                                                             |
| Řádky kusovníku &gt; Přidat před řádek      | Otevře dialogové okno, ve kterém můžete vybrat variantu produktu k zahrnutí před vybraným řádkem kusovníku.         | Tato funkce je k dispozici, pokud je vybrán uzel řádku kusovníku.                                                                                                                                                                                                                                   |
| Řádky kusovníku &gt; Přidat do kusovníku komponent | Otevře dialogové okno, ve kterém můžete vybrat variantu produktu k zahrnutí na konci vybraného kusovníku.       | Tato funkce je k dispozici, pokud má vybraný uzel zvolený kusovník. Pokud tato funkce není dostupná, verze kusovníku možná chybí pro vybranou variantu položky. V takovém případě lze kliknutím na položky **Kusovník** &gt; **Vytvořit verzi** vytvořit chybějící verzi pro vybraný uzel. |
| Řádky kusovníku &gt; Přidat za řádek       | Otevře dialogové okno, ve kterém můžete vybrat variantu produktu k zahrnutí za vybraným řádkem kusovníku.          | Tato funkce je k dispozici, pokud je vybrán uzel řádku kusovníku.                                                                                                                                                                                                                                   |
| Kusovník &gt; Vytvořit verzi             | Vytvoří nový kusovník nebo verzi kusovníku pro variantu produktu vybraného uzlu.                             | Tato funkce je k dispozici, pokud je vybraný uzel řádku kusovníku spojen s položkou, která má typ výroby **Kusovník** nebo **Receptura**.                                                                                                                                                  |
| Kusovník &gt; Výpočet                | Otevře dialogové okno, ve kterém můžete provést výpočet nákladů nebo prodejní ceny pro vybranou variantu produktu. | Tato funkce je k dispozici, pokud vybraný uzel souvisí s verzí kusovníku.                                                                                                                                                                                                         |
| Kusovník &gt; Zkontrolovat                      | Ověří a zkontroluje vybraný kusovník.                                                                      | Tato funkce je k dispozici, pokud vybraný uzel souvisí s verzí kusovníku.                                                                                                                                                                                                         |

## <a name="configuring-the-tree-view"></a>Konfigurace stromového zobrazení
Kliknutím na tlačítko **Nastavení** můžete upravit informace zobrazené ve stromovém zobrazení návrháře kusovníku.

| Skupina polí | Popis                                                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kusovník         | Pomocí zaškrtávacích políček vyberte kritéria, která se zobrazí ve stromové struktuře. V návrháři kusovníku jsou vybraná kritéria zobrazena v dolní části obou tabulek. |
| Trasa       | Pomocí zaškrtávacích políček vyberte kritéria, která se zobrazí pro postupy.                                                                                    |






