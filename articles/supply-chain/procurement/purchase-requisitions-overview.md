---
title: "Přehled nákupních žádanek"
description: "Toto téma popisuje workflow nákupní žádanky a různé možné stavy nákupních žádanek."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqConsolidation, PurchReqCreate, PurchReqCreatePurchDetails, PurchReqCreatePurchListPage, PurchReqTable, PurchReqTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 2174
ms.assetid: 77d07119-4d9f-4c0e-acbe-d319203571ab
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 942693ed3d2d54c6e973e5d3f86454b195f0fdee
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="purchase-requisition-overview"></a>Přehled nákupních žádanek

[!include [banner](../includes/banner.md)]

Toto téma popisuje workflow nákupní žádanky a různé možné stavy nákupních žádanek.

V závislosti na nastavení vaší organizace můžete vytvářet a odesílat nákupní požadavky pro produkty, které vaše organizace používá. Nákupní požadavek je interní dokument, který opravňuje nákupní oddělení k nákupu položek nebo služeb.  

Po schválení nákupní žádanky ho lze použít k vytvoření nákupní objednávky. Nákupní objednávky jsou externí dokumenty, které nákupní oddělení odesílá dodavatelům.

## <a name="creating-purchase-requisitions"></a>Vytvoření nákupních žádanek
Můžete vytvořit nákupní požadavek na stránce **Mé nákupní žádanky** a vybrat položky a služby, které požadujete. Můžete vybrat položky ze zásobovacího katalogu, který vytvořila vaše organizace, nebo si můžete vyžádat položky, které nejsou k dispozici v katalogu, výběrem kategorie zásobování a zadáním podrobností o produktu.  

Před tím, než bude možné odeslat nákupní žádanku ke kontrole, musí být v klientovi Microsoft Dynamics 365 for Finance and Operations nakonfigurován workflow. Workflow se používá k přesouvání nákupní žádanky v procesu kontroly od počátečního stavu **Koncept** do konečného stavu **Schváleno**.

### <a name="purchase-requisition-statuses"></a>Stavy nákupních požadavků

Když vytváříte nákupní požadavek, je mu přiřazen stav. Stav je přiřazen také všem řádkům, které přidáte do nákupního požadavku. Po odeslání nákupního požadavku do workflowu pro revizi se stav nákupního požadavku a stav každého řádku aktualizuje v reakci na pohyb řádků v rámci procesu workflowu.  

Můžete nastavit proces pracovního postupu pro nákupní žádanku a směrovat tak nákupní žádanku procesem kontroly jako jeden dokument. Případně lze řádky nákupní žádanky směrovat jednotlivě ke vhodným revidujícím uživatelům. Pokud jsou řádky nákupního požadavku zkontrolovány jednotlivě, stav každého řádku nákupního požadavku lze aktualizovat, jak se řádek pohybuje skrze proces kontroly. Po dokončení kontroly u všech řádků a dokončení všech kroků kontroly pro nákupní žádanku bude stav celé nákupní žádanky aktualizován.

### <a name="purchase-requisition-workflow"></a>Workflow nákupního požadavku

Následující diagram znázorňuje stavy, které jsou přiřazeny nákupnímu požadavku a řádku nákupní žádanky při procházení skrze proces workflowu.  

[![Záhlaví nákupní žádanky a stavy řádku](./media/purchasereq_headerline_statuses.jpg)](./media/purchasereq_headerline_statuses.jpg)

### <a name="purchase-requisition-header-and-line-status-relationships"></a>Záhlaví nákupního požadavku vztahy stavů řádku

Celkový stav nákupní žádanky se řídí stavem řádků nákupní žádanky. Je proto třeba před dokončením revize celé nákupní žádanky dokončit proces přezkoumání všech řádků nákupní žádanky. Následující tabulka znázorňuje stavy, které jsou přiřazeny záhlaví nákupního požadavku a řádkům při procházení nákupní žádanky skrze proces workflowu.

<table>
<thead>
<tr class="header">
<th>Stav nákupní žádanky</th>
<th>Stav řádku nákupní žádanky</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Koncept</td>
<td>Koncept</td>
<td>Nákupní požadavek a řádek nákupní žádanky byly vytvořeny, ale nebyly odeslány ke kontrole. Nákupní žádanky a řádky nákupní žádanky, které mají stav <strong>Koncept</strong>, lze upravit. Nákupní žádanka nebo řádek nákupní žádanky mají také stav <strong>Koncept</strong>, pokud byly stornovány, ale nebyly odeslány na kontrolu. <strong>Poznámka:</strong> Můžete odeslat nebo stornovat nákupní žádanku na úrovni dokumentů. Nelze však odeslat nebo odvolat jeden řádek nákupní žádanky.</td>
</tr>
<tr class="even">
<td>Probíhá kontrola</td>
<td><ul>
<li>Probíhá kontrola</li>
<li>Odmítnuto</li>
</ul></td>
<td>Je-li workflow konfigurován pro směrování řádků nákupního požadavku jednotlivým kontrolorům, každý řádek může mít stav <strong>Kontrolované</strong> nebo <strong>Odmítnuto</strong>. Stav nákupního požadavku se aktualizuje po dokončení procesu kontroly pro všechny řádky nákupního požadavku, a pokud nezbývají žádné kroky kontroly pro nákupní žádanku.
<ul>
<li><strong>Probíhá kontrola</strong> – řádky nákupního požadavku byly odeslány ke kontrole. Po dokončení procesu workflowu pro řádek nákupního požadavku zůstane stav daného řádku <strong>Kontrolované</strong>, dokud všechny zbývající řádky nákupního požadavku nebudou zkontrolovány.</li>
<li><strong>Odmítnuto</strong> – řádek nákupní žádanky byl odmítnut. Nákupní žádanka a řádky nákupní žádanky, které jsou odmítnuty, je možné upravit a znovu odeslat.</li>
</ul>
Pokud znovu odešlete řádek nákupní žádanky, který byl zamítnut, proces kontroly začne znovu pro všechny řádky nákupního požadavku, u kterých stále probíhá kontrola. <strong>Poznámka:</strong> můžete odvolat nákupní požadavek, který již byl odeslán. Když odvoláte nákupní požadavek, jsou odvolány také ostatní řádky nákupního požadavku. Lze odstranit řádky nákupního požadavku, které byly odvolány.</td>
</tr>
<tr class="odd">
<td>Odmítnuto</td>
<td>Odmítnuto</td>
<td>Nákupní žádanka a všechny její řádky byly odmítnuty. Nákupní žádanka a řádky nákupní žádanky, které byly odmítnuty, je možné znovu odeslat.</td>
</tr>
<tr class="even">
<td>Schváleno</td>
<td><ul>
<li>Schváleno</li>
<li>Stornováno</li>
<li>Uzavřené</li>
</ul></td>
<td>U všech řádků nákupního požadavku byl dokončen proces kontroly a nezbývají žádné další kroky kontroly pro daný nákupní požadavek.
<ul>
<li><strong>Schváleno</strong> – proces kontroly pro řádek nákupní žádanky byl dokončen a řádek byl schválen.</li>
<li><strong>Zrušeno</strong> – řádek nákupního požadavku byl schválen, ale byl zrušen vzhledem k tomu, že již nebyl vyžadován. Zrušit lze pouze řádky nákupního požadavku, které byly schváleny.</li>
<li><strong>Uzavřeno</strong> – řádek nákupní žádanky byl schválen a byly generovány dokumenty v závislosti na účelu žádanky.
<ul>
<li>Pokud je účelem žádanky spotřeba, nákupní objednávka byla vygenerována pro řádek nákupního požadavku.</li>
<li>Pokud je účelem žádanky doplnění, dojde k vygenerování jednoho nebo více dokumentů plnění.</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>Stornováno</td>
<td>Stornováno</td>
<td>Nákupní žádanka a všechny řádky nákupní žádanky byly zrušeny. <strong>Poznámka:</strong> Pokud již položku, která je na řádku nákupní žádanky, nepotřebujete, je nutné zrušit řádek nákupní žádanky, pokud byl již schválen. Zrušit lze pouze řádky nákupního požadavku, které byly schváleny. Pokud všechny řádky nákupního požadavku jsou vystaveny kontrole, nákupní požadavek se bude nacházet ve stavu <strong>Kontrolované</strong>. V takovém případě lze odvolat nákupní požadavek a odstranit odpovídající řádek nákupní žádanky.</td>
</tr>
<tr class="even">
<td>Uzavřené</td>
<td><ul>
<li>Uzavřené</li>
<li>Stornováno</li>
</ul></td>
<td>Nákupní žádanka je uzavřena a dojde k vygenerování jednoho nebo více dokumentů plnění.
<ul>
<li><strong>Uzavřeno</strong> – řádek nákupní žádanky byl schválen a byly generovány dokumenty v závislosti na účelu žádanky.
<ul>
<li>Pokud je účelem žádanky spotřeba, nákupní objednávka byla vygenerována pro řádek nákupního požadavku.</li>
<li>Pokud je účelem žádanky doplnění, dojde k vygenerování jednoho nebo více dokumentů plnění.</li>
</ul></li>
<li><strong>Zrušeno</strong> – řádek nákupního požadavku byl schválen, ale byl zrušen vzhledem k tomu, že již nebyl vyžadován. Zrušit lze pouze řádky nákupního požadavku, které byly schváleny.</li>
</ul>
<strong>Poznámka:</strong> Pokud již nepotřebujete položku na řádku nákupní žádanky, která již byla uzavřena, je nutné zrušit řádek v dokumentu pro plnění, který byl vygenerován pro řádek nákupního požadavku.</td>
</tr>
</tbody>
</table>

## <a name="distributing-costs-to-multiple-financial-accounts"></a>Rozdělení nákladů do několika finančních výkazů
Můžete distribuovat náklady na produktu, které jsou zahrnuty do nákupní žádanky, do několika finančních výkazů. Pokud vaše organizace používá dimenze, například nákladová střediska a oddělení, můžete distribuovat náklady na produkt do dimenzí pro finanční účty.

## <a name="requisition-purposes"></a>Účely žádanky
Účely žádanky umožňují flexibilnější proces plnění poptávky žádanek. Při vytvoření žádanky k ní můžete přiřadit jeden nebo dva účely: spotřeba nebo doplnění. V závislosti na účelu žádanky a způsobu nastavení vaší organizace lze poptávku žádanky naplnit pomocí nákupní objednávky, objednávky přenosu, výrobní zakázky nebo kanbanové úlohy.  

V rámci zásad zásobování můžete určit účely žádanky, které budou dostupné při vytvoření žádanky pro vaši organizaci.

### <a name="requisitions-that-have-a-purpose-of-consumption"></a>Žádanky, které mají účel spotřeby

Žádanka, kterou má účel spotřeby představuje poptávku po zboží nebo službách, které bude interně používat vaše organizace. Poptávka, která je vytvořena tímto typem žádanky, je vždy splněna prostřednictvím nákupní objednávky. Pokud je aplikace Microsoft Dynamics 365 for Finance and Operations nastavena na automatické vytváření nákupních objednávek, budou nákupní objednávky vytvořeny po schválení nákupní žádanky.

### <a name="requisitions-that-have-a-purpose-of-replenishment"></a>Požadavky, které mají účel doplnění

Žádanka za účelem doplnění představuje požadavek na doplnění zásob. Například můžete vytvořit žádanku na doplnění zboží, které chcete prodat v určitém obchodě v určitou dobu. Poptávku vytvořenou tímto druhem žádanky lze naplnit pomocí nákupní objednávky, převodního příkazu, výrobní zakázky nebo kanbanu.  

Pokud je účelem požadavku doplnění, poptávka je namísto peněžní částky vyjádřena jako množství. Proto nejsou platná pravidla pro účtování břemen, rozpočtové řízení, obchodní pravidla pro stanovení dlouhodobého majetku (BRAD), projektové účetnictví a ostatní související pravidla. Poptávku žádanky dokáží naplnit pouze produkty, které jsou skladovány a vydány pro uvedené právnické osoby. Produkty, které jsou k dispozici, pokud je účelem žádanky doplnění, můžete zadat na stránce **Pravidlo zásad přístupu ke kategorii doplnění**.  

Jestliže chcete použít nákupní žádanky s účelem doplnění, hlavní plánování je třeba nastavit tak, aby zahrnovalo účel žádanek. Způsob plnění pro poptávku, který se vytvoří z tohoto druhu požadavku je poté automaticky určen podle zásad dodávky, které byly nastaveny pro položky v rámci organizace a naplánovány s použitím hlavního plánování.

## <a name="purchase-requisitions-and-requests-for-quotation"></a>Nákupní žádanky a požadavky na nabídku
V některých případech je nutné spustit zpracování požadavku na nabídku pro identifikaci dodavatele a ceny produktů, které jsou vyžadovány v nákupní žádance. Požadavek na nabídku lze generovat, když je nákupní požadavek v kontrole. Při přijetí nabídky se informace týkající se dodavatele, ceny a tak dále převedou do požadavku.  

Nákupní žádanku můžete zablokovat vložit výběrem políčka **Blokování** na stránce **Podrobnosti nákupní žádanky**. Zpracování nákupní žádanky můžete pokračovat až poté, co blokování odstraníte zrušením zaškrtnutí políčka.  

**Poznámka:** v e-zásobování mohou požadavky na nabídku pro vaši nákupní žádanku povolit dodavatelům přidávat řádky alternativy. V tomto případě nákupní požadavek bude odpovídat schváleným alternativám.

## <a name="demand-consolidation"></a>Konsolidace poptávky
Konsolidací řádků nákupní žádanky z více nákupních žádanek můžete posílit svoji vyjednávací pozici s dodavateli a dosáhnout lepších cen, levnějšího dopravného a poplatků za balné a snížení režijních nákladů.  

Řádky nákupní žádanky je možné použít v konsolidaci poptávky pouze je-li splněno následující:

-   Nákupní žádanka byla schválena.
-   Nákupní žádanka splňuje kritéria pravidel zásad nákupu pro ruční zpracování a konsolidaci poptávky.

Schválené řádky nákupních požadavků, které splňují kritéria pro ruční zpracování, jsou uvedeny na stránce **Uvolnit schválené nákupní žádanky**. Pokud-li řádek nákupní žádanky také splňuje kritéria pro konsolidaci poptávky, řádek lze přidat do konsolidační příležitosti.  

Konsolidační příležitost je sada řádků nákupní žádanky, které jsou seskupeny tak, aby nákupní odborník mohl vyjednat nejlepší dohodu s dodavateli. Řádky nákupní žádanky, které vyberete pro konsolidační příležitost se zobrazí na stránce **Konsolidace nákupní žádanky**. Řádky na této stránce lze změnit, pokud je to zapotřebí. Můžete také přidat nové řádky nebo odebrat stávající řádky z konsolidační příležitosti.  

Po přidání řádků žádanky do konsolidační příležitosti a provedení potřebných změn můžete vytvořit nákupní objednávku pro řádky konsolidované nákupní žádanky.  

**Poznámka:** Změny provedené u řádku nákupní žádanky na stránce **Konsolidace nákupní žádanky** se odrazí v nákupní objednávce, kterou vytvoříte. V nákupním požadavku se však řádek nezmění, aby jeho historie zůstala zachována.  

Pro řádky nákupní žádanky, které nejsou určeny pro konsolidaci poptávky nebo nebyly vybrány pro konsolidační příležitost, musí být řádky zpracovány ručně.

### <a name="consolidating-purchase-requisition-lines"></a>Konsolidace řádků nákupní žádanky

Jestliže je pro vaši organizaci nastavena kontrola rozpočtu, proces konsolidace poptávky se spustí v okamžiku schválení nákupní žádanky ve workflowu a zaznamenání rezervace rozpočtu a předběžných břemen. Následující diagram znázorňuje průběh zpracování konsolidace poptávky.  

[![Tok procesu pro konsolidaci poptávky](./media/demand-consolidation.gif)](./media/demand-consolidation.gif)  

Pokud chcete konsolidovat schválené řádky nákupní žádanky, postupujte takto:

1.  Ověřte schválené řádky žádanky vyhrazené pro ruční zpracování a způsobilé pro konsolidaci poptávky.
2.  Vyberte řádky pro přidání ke konsolidační příležitosti.
3.  Vytvořte novou konsolidační příležitost nebo přidejte řádky požadavku k existující konsolidační příležitosti.
4.  Použijte změny, které chcete provést na řádcích požadavku a odeberte položky z řádku požadavku, které již nechcete zahrnout do konsolidační příležitosti.
5.  Vytvořte nákupní objednávky pro řádky konsolidované žádanky nebo řádky nákupní žádanky v konsolidační příležitosti.


<a name="additional-resources"></a>Další zdroje
--------

[Vytvořeni požadavku na využití (Průvodce záznamem úloh)](tasks/create-requisition-consumption.md)

[Workflow nákupního požadavku](purchase-requisitions-workflow.md)




