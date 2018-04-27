---
title: "Návrhář receptur"
description: "Toto téma vysvětluje, jak pomocí návrháře receptur analyzovat a udržovat receptury ve stromovém zobrazení."
author: cvocph
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a4cfd017fe10bbda6eda0e3a9a045e0832b08753
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="formula-designer"></a>Návrhář receptur

[!INCLUDE [banner](../includes/banner.md)]

Toto téma vysvětluje, jak pomocí návrháře receptur analyzovat a udržovat receptury ve stromovém zobrazení.

Při otevření stránky **Návrhář receptur** ze stránky **Uvolněné produkty** se ve stromové struktuře v levém podokně zobrazuje seznam vedlejších produktů a hierarchie látek pro uvolněný produkt. Struktura je odvozena z hierarchie receptur, které jsou aktivní a schválené pro vybranou položku a její látky, výchozího objednacího místa položky a skutečného data.

Po kliknutí na možnost **Nastavení** můžete vybrat různé konfigurace a určit, které informace mají být zobrazeny ve stromu.

Kliknutím na tlačítko **Filtr** změňte počáteční výběr v zobrazení. Nastavením principu zobrazení na možnost **Vybrané/Aktivní** nebo **Vybrané** můžete vybrat jednotlivé verze receptury nebo postupu pro použití v zobrazení. Můžete vybrat neschválené a neaktivní verze receptury pro účely zobrazení či správy v návrháři receptur.  

> [!NOTE]
> Otevřete-li **Návrhář receptur** ze stránky seznamu **Kusovníky**, nezobrazí se informace o postupu. Výběr verze postupu nebo receptury se v současnosti vztahuje na všechny instance návrháře receptur.  

V následujících částech najdete popis funkcí, které jsou k dispozici na různých kartách návrháře.

## <a name="analyze-a-formula-structure-by-using-the-formula-designer"></a>Analýza struktury receptury pomocí modulu Návrhář receptur
Návrhář receptur má dvě části:

-   Stromové zobrazení struktury receptury.
-   Oddíl podrobností zobrazující podrobnosti o vybraných datech. Při výběru uzlu ve stromovém zobrazení se pevné záložky v části Podrobnosti aktualizují na základě daného uzlu:
    -   **Podrobnosti řádku receptury** – zobrazí podrobnosti o řádku receptury, který je vybrán ve stromovém zobrazení.
    -   **Data položky** – zobrazí podrobnosti hlavní položky nebo položky, která se používá ve vybraném uzlu. Můžete kliknout na **Upravit uvolněný produkt** a upravit vybranou položku.
    -   **Receptura** – zobrazí záhlaví receptury, která souvisí s vybraným uzlem.
    -   **Postup** – zobrazí záhlaví postupu, který souvisí s vybraným uzlem.
    -   **Operace postupu** – zobrazuje přehled operací daného postupu. Pokud je vybrán řádek kusovníku, který je přiřazen k určité operaci, operace je označena jako **Komponenta potřebná v operacích**.

## <a name="select-a-formula-and-route"></a>Výběr receptury a postupu
Filtr, který je použit pro recepturu a postup, se zobrazí v záhlaví návrháře receptury. Filtr lze změnit pomocí dialogového okna **Filtr**. Pole tohoto dialogového pole jsou popsána v následující tabulce.

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
<td>Pokud je vybraný hotový produkt základním produktem, můžete u hlavního výběru definovat aktivní dimenze produktu. Pokud otevřete návrhář receptury pro produkt, který není základní, v dialogovém okně <strong>Filtr</strong> nebude možné vybrat žádné dimenze produktu.</p></td>
</tr>
<tr class="even">
<td>Pracoviště</td>
<td>Změní pracoviště, pro které se zobrazuje strom látek. Výchozí pracoviště je výchozím skladovým pracovištěm dokončené položky.</td>
</tr>
<tr class="odd">
<td>Pravidlo zobrazení</td>
<td><p>Vybere princip zobrazení verze, který se vztahuje na aktuální strukturu receptury a na aktuální postup:</p>
<ul>
<li>Je-li pro princip nastavena hodnota <strong>Aktivní</strong> nebo <strong>Vybrané/Aktivní</strong>, zobrazí se verze receptury nebo postupu pro toto datum.</li>
<li>Je-li pro princip nastavena hodnota <strong>Vybrané/Aktivní</strong> nebo <strong>Vybrané</strong>, můžete vybrat verzi receptury nebo verzi postupu kliknutím na položky <strong>Receptura</strong> &gt; <strong>Verze receptury</strong> nebo <strong>Postup</strong> &gt; <strong>Verze postupu</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Datum verze</td>
<td>Zadejte datum verze pro recepturu a postup. Pomocí verze lze určit verzi receptury, která má být použita pro určité datum, a to podle dat verze v nastavení verze receptury.</td>
</tr>
<tr class="odd">
<td>Od množství</td>
<td>Filtrovat verze můžete výběrem konkrétního množství &quot;od&quot;. Pokud nastavíte nějakou hodnotu, může dojít k výběru jiné verze postupu a receptury.</td>
</tr>
<tr class="even">
<td>Zobrazit pouze platné</td>
<td>Pokud zaškrtnete toto políčko, budou ve struktuře stromu zobrazeny pouze řádky receptury s platnými daty. Dvojitým kliknutím nebo kliknutím pravým tlačítkem myši na řádek receptury můžete otevřít stránku <strong>Upravit řádek receptury</strong>, kde můžete vidět data platnosti pro daný řádek receptury.</td>
</tr>
</tbody>
</table>

Použijete-li návrhář receptur ke kontrole nebo úpravě receptur, které se skládají z jedné nebo více úrovní fiktivních položek, pak postup, který je přidružen k nejvyšší položce, obvykle zahrnuje celou hierarchii receptur. Pro zjednodušení přehledu můžete uzamknout postup nejvyšší úrovně v zobrazení kliknutím na tlačítko **Zobrazení** &gt; **Uzamknout postup**. Postup můžete odemknout kliknutím na položky **Zobrazení** &gt; **Odemknout postup**.

## <a name="add-and-edit-formulas-and-formula-lines"></a>Přidání a úprava receptur a řádků receptur
Pomocí funkcí **Řádky receptury** nebo **Receptura** můžete upravit řádky receptur nebo receptury samotné. Když vyberete uzel ze stromu, typ uzlu určí, které z funkcí budou k dispozici.

| Funkce                            | popis                                                                                               | Typ a podmínky uzlu |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|--------------------------|
| Řádky kusovníku &gt; Upravit                 | Zobrazí dialogové okno, ve kterém můžete upravit atributy řádku receptury.                                         | Tato funkce je k dispozici, pokud je vybrán uzel řádku receptury. |
| Řádky kusovníku &gt; Odstranit               | Odstraní z vybrané receptury řádek receptury.                                                          | Tato funkce je dostupná, když je vybrán uzel řádku receptury a receptura není uzamčena pro úpravy. |
| Řádky kusovníku &gt; Přidat před řádek      | Zobrazí dialogové okno, ve kterém můžete vybrat variantu produktu k zahrnutí před vybraným řádkem receptury.     | Tato funkce je k dispozici, pokud je vybrán uzel řádku receptury. |
| Řádky kusovníku &gt; Přidat do kusovníku komponent | Zobrazí dialogové okno, ve kterém můžete vybrat variantu produktu k zahrnutí na konci vybrané receptury.   | Tato funkce je k dispozici, pokud má vybraný uzel zvolenou recepturu. Pokud tato funkce není dostupná, pro vybranou variantu položky možná chybí verze receptury. V takovém případě lze kliknutím na položky **Receptura** &gt; **Vytvořit verzi** vytvořit chybějící verzi pro vybraný uzel. |
| Řádky kusovníku &gt; Přidat za řádek       | Zobrazí dialogové okno, ve kterém můžete vybrat variantu produktu k zahrnutí za vybraným řádkem receptury.      | Tato funkce je k dispozici, pokud je vybrán uzel řádku receptury. |
| Receptura &gt; Vytvořit verzi         | Vytvoří novou recepturu nebo verzi receptury pro variantu produktu vybraného uzlu.                     | Tato funkce je k dispozici, pokud je vybraný uzel řádku receptury spojen s položkou, která má typ výroby **Kusovník** nebo **Receptura**. |
| Receptura &gt; Výpočet            | Otevře dialogové okno, ve kterém můžete provést výpočet nákladů nebo prodejní ceny pro vybranou variantu produktu. | Tato funkce je k dispozici, pokud vybraný uzel souvisí s verzí receptury. |
| Receptura &gt; Zkontrolovat                  | Ověří a zkontroluje vybranou recepturu.                                                                  | Tato funkce je k dispozici, pokud vybraný uzel souvisí s verzí receptury. |

## <a name="configuring-the-tree-view"></a>Konfigurace stromového zobrazení
Kliknutím na tlačítko **Nastavení** můžete upravit informace zobrazené ve stromovém zobrazení návrháře receptur.


| Skupina polí |                                                                          popis                                                                          |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     Kusovník     | Pomocí zaškrtávacích políček vyberte kritéria, která se zobrazí ve stromové struktuře. V modulu Návrhář receptur jsou vybraná kritéria zobrazena v dolní části obou tabulek. |
|    Postup    |                                           Pomocí zaškrtávacích políček vyberte kritéria, která se zobrazí pro postupy.                                           |


