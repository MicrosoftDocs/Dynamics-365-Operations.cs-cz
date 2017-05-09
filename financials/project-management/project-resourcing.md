---
title: "Prostředky pro projekt"
description: "V tomto tématu jsou informace o přidělování prostředků k projektu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: cmercado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: c29c95fc6abd13e668c44d3ccf437bb0e879e46b
ms.lasthandoff: 03/31/2017


---

# <a name="project-resourcing"></a>Prostředky pro projekt

[!include[banner](../includes/banner.md)]


V tomto tématu jsou informace o přidělování prostředků k projektu.

Jednou z výzev pro správce projektu a prostředků ve fázi plánování projektu je přiřazení zdrojů, kdy musí určit a rezervovat správné zdroje pro práci na projektu. V aplikaci Microsoft Dynamics 365 for Operations umožňuje přidělení prostředků pro projekty definovat role, které jsou považovány za dočasné zdroje, které mohou být vyhrazeny pro konkrétní pracovní balíček nebo součásti zapojení. Tento typ přidělování prostředků umožňuje manažerům projektů a prostředků provádět následující úkony:

-   Definovat roli, která má požadované kompetence pro snadné spárování zdrojů.
-   Používat role k definování původního schématu zapojení založeného na rezervovaných prostředcích.
-   Odhadovat náklady a určovat původní rozpočet na základě přiřazených rolí a zdrojů pro projekt.
-   Používat role pro odhad počtu rezervací prostředků, které jsou nutné pro každé zapojení.
-   Odhadovat počet prostředků, které jsou požadovány pro celý životní cyklus projektu.
-   Vytvářet koncept strukturovaného rozpisu prací pomocí prvotního přiřazení prostředků.

[![Životní cyklus projektu](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg) 

Jak probíhá plánování projektu, plánované prostředky je možné nahradit personálními zdroji. Manažer projektu se může také vrátit zpět a aktualizovat rezervace prostředků v libovolné fázi projektu

## <a name="set-up-project-resources"></a>Nastavení prostředků projektu
Musíte nastavit kalendář a přidružit jej se zaměstnancem nebo pracovníkem. Kalendář lze použít pro naplánování projektu a pracovní doby prostředků, které jsou na projekt rezervovány. Během nastavení kalendáře může projektoví manažer provádět vyrovnání prostředků v rámci optimalizace prostředku. Na základě plánu kalendáře lze pro prostředky uvalit omezení. Můžete nastavit kalendář na stránce **Kalendáře**. 

Při nastavení pracovníka jako projektového prostředku můžete vybírat z pracovníků, kteří pracují ve firmě, pro kterou nastavujete prostředky, nebo můžete vybrat pracovníky z jiných firem ve vaší organizaci. Jedná se o mezipodnikové prostředky. Následující postupy vysvětlují, jak nastavit pracovníka jako zdroj projektu v rámci společnosti a jak nastavit prostředek mezipodnikové projektu.

### <a name="set-up-a-worker-as-a-project-resource"></a>Nastavení pracovníka jako prostředek projektu

1.  Na stránce **Pracovníci** v seznamu **Pracovníci** vyberte pracovníka, kterého chcete přidat jako prostředek projektu, a otevřete záznam pracovníka.
2.  V podokně akcí klepněte na **Projekt** &gt; **Nastavení** &gt; **Nastavení projektu**.
3.  Vyberte kalendář a zavřete stránku.

Můžete také určit výchozí projekty pro prostředky jako typ předběžného přiřazení. Předběžné přiřazení lze použít, pokud manažer prostředků nebo projektu dopředu ví, na kterých projektech budou prostředky pracovat. Předběžné přiřazení může být založeno také na žádosti investora projektu nebo odběratele. Pokud chcete předběžně přiřadit projekt, na stránce **Přiřadit projekty** na kartě **Projekty** v seznamu **Zbývající projekty** vyberte příslušný projekt.

### <a name="set-up-an-intercompany-resource"></a>Nastavení mezipodnikového zdroje

Při nastavování pracovníka jako mezipodnikového zdroje je nutné dokončit nastavení ve společnosti poskytující půjčku a společnosti, která zažádala o půjčku. 

**Společnost poskytující půjčku:**

1.  V aplikaci Dynamics 365 for Operations ověřte, zda je vybrána společnost poskytující půjčku, a pak dokončete výše uvedený postup Nastavení pracovníka jako prostředku projektu.
2.  Přejděte na **Hlavní kniha **&gt; **Nastavení účetnictví **&gt; **Mezipodnikové účetnictví**. Klepněte na možnost **Nový**.
3.  V poli **ID právnické osoby ** vyberte společnost poskytující půjčku. Podle potřeby vyplňte zbývající pole a potom klepněte na tlačítko **Uložit**.
4.  Přejděte na **Řízení a účetnictví projektu **&gt; **Nastavení **&gt; **Ceny ** &gt; **Převést cenu**.** **
5.  Ve formuláři **Převést cenu ** klepněte na tlačítko **Nový** a v poli ** Právnická osoba, která si půjčuje ** vyberte příslušnou společnost.
6.  Pokud chcete si od společnosti poskytující půjčku chcete pouze vypůjčit prostředek, který jste vytvořili na začátku této části, v poli **Zdroje**, vyberte název zdroje, který jste vytvořili. Pokud chcete zpřístupnit všechny prostředky ve firmě půjčující si společnosti, ponechejte pole **Zdroj **prázdné.
7.  Přejděte na položky **Řízení a účetnictví projektu **&gt; **Nastavení **&gt; **Parametry správy projektu a účetnictví** a na kartě **Mezipodnikové **nastavte hodnotu v poli **Povolit mezipodnikové plánování prostředků a časové rozvrhy**na **Ano**.

**Společnost, která zažádala o půjčku:**

1.  Přejděte na **Řízení a účetnictví projektů** &gt; **Prostředky projektu** &gt; **Seznam prostředků**.
2.  Ve filtru vyhledávání zadejte název prostředku, který jste vytvořili v předchozím postupu pro společnost poskytující půjčku, ověřte, že název je zahrnut v seznamu zdrojů pro společnost, která žádá o půjčku.

## <a name="manage-resource-competencies"></a>Správa kompetencí prostředků
Kompetence prostředků jsou důležitou částí správy prostředku. Kompetence slouží jako základ pro určení zdroje, který má správný poměr dovedností, vzdělání, kvalifikace a zkušeností s projektem. Doporučujeme nastavit tento údaj pro každý zdroj a aktualizovat jej v pravidelných intervalech. Tímto způsobem můžete maximalizovat možnosti v případě, že jsou porovnány konkrétní kompetence prostředků při přiřazení prostředků k projektu. [![Příklady dovedností, certifikátů, vzdělání a zkušeností z projektu](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg) 

Následující postupy vysvětlují, jak nastavit některé kompetence prostředku. 

Pro nastavení kompetencí pracovníka slouží buď stránka se seznamem **Pracovníci** v rámci lidských zdrojů, nebo stránka se seznamem **Prostředky** v rámci Řízení a účetnictví projektů. Pro následující procesy bude použita stránka se seznamem **Pracovníci** v rámci lidských zdrojů.

### <a name="set-up-competencies-certificates"></a>Nastavení kompetencí: certifikáty

1.  Na stránce se seznamem **Pracovníci** vyberte řádek zaměstnance, pro kterého přidáváte informace o certifikátu.
2.  Na panelu akcí na kartě **Pracovník** ve skupině **Kompetence** klikněte na možnost **Certifikáty**.
3.  Klepněte na možnost **Nový**.
4.  V poli **Typ certifikátu** vyberte **PMP**.
5.  V poli **Počáteční datum** vyberte **10/1/2015**.
6.  Klikněte na tlačítko **Uložit** a pak zavřete stránku.

### <a name="set-up-competencies-skills"></a>Nastavení kompetencí: dovednosti

1.  Na stránce se seznamem **Pracovníci** vyberte pracovníka, kterého jste použili v předchozím postupu. Poté v podokně akcí na kartě **Pracovník** ve skupině **Kompetence** klikněte na **Dovednosti**.
2.  Klepněte na možnost **Nový**.
3.  V poli **Dovednost** vyberte **Správa projektu**.
4.  V poli **Úroveň** vyberte **5 Odborník**.
5.  V poli **Datum úrovně** vyberte **1-/14/2014**.
6.  V poli **Roky praxe** zadejte **10**.
7.  Klikněte na tlačítko **Uložit** a pak zavřete stránku.

## <a name="create-a-new-project"></a>Vytvořit nový projekt
1.  Klikněte na **Řízení a účetnictví projektů** &gt; **Pracovní prostory** &gt; **Řízení projektu**.
2.  Klepněte na **Nový projekt** a zadejte následující hodnoty:
    -   **Typ projektu:** - Čas a materiál
    -   **Název projektu:** - Upgrade XYZ fáze 2
    -   **Skupina projektu** - TM\_WIP
    -   **ID projektové smlouvy:** - 00000002
3.  Klikněte na **Vytvoření projektu**.

### <a name="assign-a-resource-to-a-project"></a>Přiřazení prostředku k projektu

1.  Klikněte na **Lidské zdroje** &gt; **Pracovníci** &gt; **Pracovníci**.
2.  V seznamu **Pracovníci** vyberte záznam o zaměstnanci, pro kterého jste dříve nastavili kompetence, a otevřete záznam pracovníka.
3.  V podokně akcí na kartě **Projekt** ve skupině **Nastavení** klikněte na **Přiřadit projekty**.
4.  Na stránce **Přiřazení projektů ověření prostředku** klikněte na kartu **Projekty**.
5.  V části **Přidat projekt do vybraných projektů** vyfiltrujte projekt, Upgrade XYZ fáze 2
6.  V podokně **Zbývající projekty** vyberte projekt a kliknutím na šipku jej přidejte do podokna **Vybrané projekty**.
7.  Zavřete stránku.

V případě potřeby můžete také přiřadit kategorie ke zdroji. Typ kategorie jsou Náklady nebo Výnosy. Ten je určen vaší organizací. Pokud neexistují žádné přiřazené kategorie pro prostředek, aplikace Dynamics 365 for Operations vyhledá výchozí kategorii pro hodinové ceny pro náklady a výnosy.

### <a name="set-up-project-resource-and-role-characteristics"></a>Nastavení vlastností prostředků a role projektu

Manažer projektu může použít funkci přidělení prostředků k projektu pro vytvoření rolí potřebných pro daný projekt. Role lze použít, pokud potvrzené prostředky jsou během rezervace prostředku zatím neznámé. Role lze použít pro dočasné rezervování jako plánovaných zdrojů, abyste mohli pokračovat ve fázi plánování projektu. 

[![Příklad role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scénář:** Společnost Contoso byla najata na dokončení projektu Čas a materiál, který má schválené stanovy projektu. Nižší manažer projektu stále dokončuje rozsah projektu. Manažer prostředků aktuálně identifikuje konkrétní zdroje, které budou rezervovány k práci na novém projektu. Jedna z rolí, kterou investor projektu požaduje s ohledem na kritickou povahu projektu, je Vrchní vedoucí projektu. Správce zdrojů musí získat nový prostředek a rozhodne se, že určí roli v systému pro případ, že nižší manažer projektu bude potřebovat informace o prostředku během plánování projektu. 

Následující pokyny popisují, jak může manažer prostředků nastavit roli Vrchní vedoucí projektu a přidružit k ní vlastnosti prostředků. Později slouží role k vyhledání dostupných zdrojů, které odpovídají požadovaným kompetencím prostředku.

1.  Klepněte na tlačítko **Řízení a účetnictví projektu** &gt; **Nastavení** &gt; **Zdroje** &gt; **Nastavení rolí**.
2.  Klepněte na **Nový** a zadejte následující hodnoty:
    -   **ID role:** - vrchní manažer projektu
    -   **Popis:** - vrchní manažer projektu
3.  Klepněte na volbu **Nový**.
4.  Vyberte roli **Vrchní manažer projektu** a klepněte na tlačítko **Konfigurace vlastností**.
5.  V poli **Typ charakteristik** vyberte **Dovednost**.
6.  V poli **Dostupné charakteristiky** zadejte dovednost, kterou hledáte.
7.  V poli **Typ charakteristiky** vyberte **Certifikát**.
8.  V poli **Dostupné charakteristiky** zadejte hledaný typ certifikátu.
9.  Klikněte na tlačítko **OK** a pak zavřete stránku.

### <a name="assign-a-project-resource-to-a-project"></a>Přiřazení prostředku projektu k projektu

1.  Klikněte na **Řízení a účetnictví projektů** &gt; **Obecné** &gt; **Projekty** &gt; **Všechny projekty**a otevřete projekt **Upgrade XYZ fáze 2**.
2.  Na kartě **Projektový tým a plánování** klikněte na možnost **Přidat**.
3.  V poli **Role** vyberte **Člen týmu**.
4.  Klikněte na **Rezervovat z kalendáře**.
5.  Na stránce **Dostupnost prostředku** klepněte na **Zobrazit nastavení**.
6.  Na stránce **Upravit nastavení zobrazení** zadejte následující hodnoty:
    -   **Formát pro zobrazení rozsahu dat:** - den
    -   **Zobrazit popisy dostupnosti:** - Ano
    -   **Zobrazit zbývající kapacitu** - Ano
7.  V seznamu zdrojů vyberte prostředek.
8.  Klepněte na tlačítko **Závazně rezervovat** &gt; **Plná kapacita**.
9.  Zavřete stránku.

### <a name="assign-a-resource-to-a-default-role"></a>Přiřazení prostředku k jiné roli

Pokud chcete usnadnit práci manažerům projektu nebo prostředků, můžete přejít hlouběji do podrobností, které lze pro projekt rezervovat. Můžete přiřadit výchozí roli k existujícímu prostředku nebo nově získanému prostředku. Například když byl přijat Daniel, měl zkušenosti a schopnosti plnit roli obchodního analytika. Správce prostředků přiřadil tuto roli Danielovi jako výchozí. Proto správce prostředků přidal Daniela do fondu obchodních analytiků, kteří jsou k dispozici pro práci na projektech. 

Během rezervování zdrojů mohou projektoví manažeři filtrovat zdroje v roli, které jsou k dispozici pro práci na projektech. Tyto údaje lze použít jako jednu z kritérií při provádění analýzy rozhodnutí s více kritérii během plnění prostředků. Mohou také přidat další charakteristiky prostředků do filtru a vyhledat zdroje, které mají určité dovednosti, vzdělání a zkušenosti s daným projektem. 

**Situace:** začal schválený projekt a role Hlavní manažer projektu byla během fáze plánování projektu rezervována jako plánovaný zdroj. Manažer prostředků získá prostředek pro naplnění role Hlavní manažer projektu.

1.  Klepněte na tlačítko **Řízení a účetnictví projektů** &gt; **Zdroje projektu** &gt; **Seznam zdrojů**.
2.  V seznamu **Prostředky** vyberte položku **Daniel Goldschmidt**.
3.  Klepněte na tlačítko **Prostředek projektu** &gt; **Udržovat** &gt; **Role prostředku**.
4.  Klepněte na **Nový** a zadejte následující hodnoty:
    -   **Platnost:** - (aktuální datum)
    -   **Vypršení platnosti:** - nikdy
    -   **Role:** - hlavní manažer projektu
5.  Klikněte na tlačítko **Uložit** a pak zavřete stránku.
6.  Na kartě **Kompetence** přidejte dovednost **ProjectMgmt** a certifikát **PMP**.

## <a name="set-up-role-based-pricing"></a>Nastavení cen na základě role
Pro role lze nastavit všechny náklady, prodeje, a převodní ceny.

1.  Klepněte na tlačítko **Řízení a účetnictví projektu >** &gt; **Nastavení** &gt; **Ceny** &gt; **Prodejní cena (hodinová)**.
2.  Klepněte na možnost **Nový**.
3.  Zadejte datum platnosti.
4.  Ve sloupci **Role** vyberte roli.
5.  Ve sloupci **Ocenění** zadejte cenu pro vybranou roli prostředku.

## <a name="form-a-project-team"></a>Formování projektového týmu
Pokud chcete použít role, které byly dříve nastaveny, v projektu, projektový manažer musí přiřadit role k projektu. Pro projekt lze přiřadit více rolí a aplikace Dynamics 365 for Operations tyto role automaticky při rezervaci označí, aby se zabránilo nejasnostem. Například pokud manažer projektu požaduje tři softwarové techniky, automaticky se vygenerují tři role Softwarový technik, které jsou pojmenovány jako Softwarový technik 1, Softwarový technik 2 a Softwarový technik 3. Pokud byly dříve pro roli nastaveny charakteristiky role, jsou použity jako filtr při hledání zdroje. Pro další upřesnění hledání lze volitelně přidat další charakteristiky. 

Možnost Zobrazit nastavení lze také upravit tak, aby poskytovala lepší pohled na dostupnost prostředků. K dispozici je možnost zobrazit dostupnost hodinově, denně, týdně, měsíčně, čtvrtletně a ročně. Existuje také možnost zobrazit dostupnou a zbývající kapacitu prostředků. Tato možnost je užitečná pro časovou správu, pokud odhadujete dostupný čas pro aktivity nebo dostupnost prostředku. 

Manažer projektu může vybrat roli na stránce a poté, je-li dostupný prostředek, který odpovídá požadavkům, může vybrat a rezervovat prostředek pro obsazení role. Mějte na paměti, že prostředky nemusí být v této fázi plánování rezervovány. Při vytváření struktury WBS můžete nahradit role skutečnými personálními prostředky pro daný projekt. Pokud role budou nahrazeny skutečnými zaměstnanci ve struktuře WBS, nastavení prostředků automaticky aktualizuje výpis a plánování projektového týmu. 

[![Seznam týmů projektu, který obsahuje role a skutečné zdroje](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Vedoucí projektu má řadu možností pro rezervaci zdroje na projekt, například **Zbývající kapacita**, **Plná kapacita**, **Procento kapacity** a **Zadání hodin**. Tyto možnosti rezervace lze kdykoli zrušit v případě, že se změní přiřazení prostředků. Podporovány jsou dva typy rezervace:

-   **Závazná rezervace** – Rezervace prostředku byla schválena a práce na projektu byla po určenou dobu trvání potvrzena.
-   **Předběžná rezervace** – rezervace prostředku a účast na projektu po určenou dobu trvání je nezávazně schválena.

Při vytváření projektového týmu postupujte následujícím způsobem.

### <a name="create-a-project-team"></a>Vytvoření projektového týmu

1.  Na stránce se seznamem **Všechny projekty** vyberte projekt a klepněte na **Upravit**.
2.  Na kartě **Projektový tým a plánování** v poli **Naplánovat koncové datum** zadejte datum zahájení plánu posunuté o jeden měsíc. Je-li datum zahájení plánu například 24. června 2017 (24/06/2017), zadejte **24/07/2017**.
3.  Klikněte na tlačítko **Přidat**.
4.  V podokně **Přidat role do projektu** v poli **Role **vyberte **Vrchní manažer projektu**.
5.  Klikněte na **Požadované kompetence**.
6.  Na stránce **Vybrat charakteristiky** jsou standardně zvoleny charakteristiky, které jste dříve nastavili pro roli Vrchní manažer projektu. Klepněte na tlačítko **OK**.
7.  Na stránce **Přidat role do projektu** v poli **Počet prostředků** zadejte **1**.
8.  V poli **Prostředek** vyhledávání zobrazí všechny zdroje, které mají požadované kompetence. Vyberte **Daniel Goldschmidt**a klepněte na tlačítko **Vytvořit**.
9.  Na stránce **Projekt** klikněte na **Přidat**.
10. V podokně **Přidat role do projektu** v poli **Role** vyberte **Člen týmu**. V poli **Počet prostředků** zadejte hodnotu **5**.
11. Klepněte na volbu **Nový**.
12. Na stránce **Projekty** klepněte na **Splnit prostředek**.

## <a name="resource-capacity-synchronization"></a>Synchronizace kapacity prostředku
Procesy pro synchronizaci prostředků pomáhají zajistit, aby kalendář a základní informace o kalendáři přešly dále do plánování prostředků pro projekt. Pokud dojde ke změně kalendáře, procesy provedou požadované aktualizace v plánování zdrojů pro projekt. Procesy také pomáhají zvýšit efektivitu, protože informace o prostředcích v kalendáři jsou synchronizovány v předstihu tak, aby se informace o plánování prostředků předávaly rychleji. Doporučujeme naplánovat procesy jako dávku namísto postupného zpracování. V opačném případě je riziko, že někdo zapomene inkluzivní datum, kdy byly informace naposled synchronizovány. Pokud inkluzivní data nejsou použity, mohou vzniknout mezery v synchronizaci dat.

### <a name="calendar-synchronizationmediaprojectresourcing04-1024x471jpg"></a>![Synchronizace kalendáře](./media/projectresourcing04-1024x471.jpg)

**Synchronizace shrnutí kapacity pro prostředek**

Proces synchronizace umožňuje synchronizovat všechny informace v kalendáři prostředku. Tyto informace zahrnují základní informace z kalendáře o všech změnách v tabulce kapacity kalendáře prostředků projektu. Pokud jsou do projektu přidány nové prostředky, synchronizace pomáhá zajistit, že jsou aktualizované informace k dispozici. Tuto synchronizaci lze provádět kdykoliv. 

Doporučujeme používat dávky. Možnosti jsou dostupné při synchronizaci rezervací kapacity.

-   Klikněte na **Řízení a účetnictví projektů** &gt; **Periodicky** &gt; **Synchronizace kapacity** &gt; **Synchronizace shrnutí kapacity pro prostředek**.

| Parametr | popis                                                                                                                                                                                          |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ano    | Synchronizujte všechna data prostředků s kalendářem a základními informacemi o kalendáři a nahraďte všechny informace v kalendáři kapacity prostředku projektu.                                                  |
| Č.     | Synchronizujte data prostředků na základě kódu intervalu dat a zadaném počátečním a koncovým datem. Tato možnost neodstraní existující data, a aktualizuje údaje pouze pro nově přidané prostředky. |

[![Proces synchronizace](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Nastavení rolí v šablonách WBS
Vedoucí projektu může nastavit šablony WBS, které později použijí při vytváření struktury WBS pro nové projekty. Vedoucí projektu nyní může při vytváření šablony přidat role. Pomocí následujícího postupu se přiřadí role k šabloně WBS.** **

1.  Klikněte na **Řízení a účetnictví projektů** &gt; **Nastavení** &gt; **Projekty** &gt; **Šablony strukturovaného rozpisu prací**.
2.  Klepněte na tlačítko **Podrobnosti** u vybrané šablony WBS.
3.  Vyberte úkol v seznamu a pak v poli **Role** vyberte roli pro přiřazení k úloze.

### <a name="work-with-a-wbs"></a>Práce se strukturou WBS

Můžete vytvořit novou strukturu WBS, nebo můžete zkopírovat strukturu WBS z existující šablony WBS. Manažer projektu může snadno spravovat prostředky přiřazením rolí k novým úkolům v rámci WBS. Role lze nahradit po pořízení prostředku, nebo po určení prostředku, který potvrdil práci na úkolu. Tato možnost umožňuje vedoucím projektu provádět následující úkoly:

-   Určit počet prostředků, které jsou požadovány pro balíky práce WBS.
-   Odhadovat náklady na projekt.
-   Určovat předběžný rozpočet.
-   Odhadovat dobu trvání aktivity na základě rolí a zdrojů.
-   Vyvíjet některé plány pro vedení projektu, které jsou založené na informacích o projektu.

Další možnosti byly přidány do struktury WBS a umožňují lepší využití přidělování prostředků.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Možnost</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Přiřazení prostředků</td>
<td>Úlohy spojené se strukturou WBS viz přidělené prostředky, data, počty hodin a typ rezervace.</td>
</tr>
<tr class="even">
<td>Automaticky generovat tým</td>
<td>Automaticky přidělíte plánované prostředky pomocí rolí, které jsou přidruženy k úkolu. Aplikace Dynamics 365 for Operations automaticky navrhuje plánované prostředky použitím analýzy kritérií s více rozhodnutími založené na rolích. Po nastavení rolí a úsilí (hodiny) pro úkoly ve struktuře WBS a vydání struktury klepněte na tlačítko <strong>Automaticky generovat tým</strong>. Požadovaný počet plánovaných prostředků je přidán do struktury WBS a na kartu <strong>Plánování projektu a týmu</strong>.</td>
</tr>
<tr class="odd">
<td>Prostředek (rozevírací seznam)</td>
<td>Na stránce <strong>Spuštění přiřazení zdrojů </strong>můžete vybrat prostředky, které chcete závazně nebo nezávazně rezervovat podle zadaného trvání. Můžete upravit nastavení zobrazení a prohlédnout si trvání aktivit prostředku. Pomocí následujících možností můžete vybrat a přiřadit prostředky na úrovni balíčku práce:
<ul>
<li><strong>Přijmout</strong> – potvrdit změny u prostředku, který je přiřazen k úkolu.</li>
<li><strong>Storno</strong> – zrušit změny u prostředku, který je přiřazen k úkolu.</li>
<li><strong>Automaticky přiřadit</strong> – tato možnost vybere dostupný personální prostředek s odpovídající rolí pro vybraný úkol.</li>
</ul></td>
</tr>
</tbody>
</table>

1.  Klikněte na **Řízení projektu a účetnictví** &gt; **Projekty** &gt; **Všechny projekty**.
2.  V seznamu vyberte projekt **Upgrade XYZ fáze 2**.
3.  Klikněte na možnosti **Plán** &gt; **Aktivity** &gt; **Strukturovaný rozpis prací**.
4.  Klepněte na tlačítko **Nový** a přidejte tak následující činnosti první úrovně do struktury WBS:
    -   Inicializace
    -   Plánování
    -   Zpracování
    -   Sledování a řízení
    -   Zavřít

5.  Nastavte data a úsilí (v hodinách), jak je uvedeno na následujícím snímku obrazovky.[![Nastavení dat a úsilí](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)
6.  Vyberte řádek úlohy **Inicializace** a v poli **Role** vyberte **Vyšší manažer projektu**.
7.  Klikněte na tlačítko **Publikovat**.
8.  Na stejném řádku v poli **Prostředky** vyberte **Daniel Goldschmidt**.
9.  Klepněte na možnost **Přijmout**.
10. Vyberte řádek úlohy **Plánování** a v poli **Role** vyberte **Obchodní analytik**.
11. Klepněte na tlačítko **Publikovat** a poté na tlačítko **Automaticky generovat tým**.
12. V nově otevřeném dialogovém okně klepněte na tlačítko **Ano**.
13. V poli **Prostředek** zkontrolujte, zda je hodnota **Obchodní analytik 1**.
14. U prostředku **Obchodní analytik 1** spusťte vyhledávání a klepněte na **Spustit formulář přiřazení prostředku**.
15. Vyberte pracovníka pro úlohu.
16. Klepněte na tlačítko **Předběžně přiřadit** &gt; **Plná kapacita**.
17. Klikněte na tlačítko **Uložit** a pak zavřete stránku. 

> [!NOTE] 
> Neobdržíte upozornění, že vybraný prostředek je nyní „2“, protože počet prostředků zůstává „1“.
18. Na stránce **Strukturovaný rozpis prací **ověřte přiřazení prostředku ve struktuře WBS a klepněte na tlačítko **Uložit**.

## <a name="resource-fulfillment-for-planned-resources"></a>Plnění prostředků pro plánované prostředky
Manažer projektu může naplánovat požadované role prostředku pro projekt. Správce prostředků uvidí tyto plánované prostředky jako požadavky na stránce **Plnění prostředků** a má možnost přiřadit skutečné prostředky.

1.  Klikněte na **Řízení projektu a účetnictví** &gt; **Projekty** &gt; **Všechny projekty**.
2.  V seznamu vyberte projekt **Upgrade XYZ fáze 2**.
3.  Klikněte na **Projekt**.
4.  Klikněte na možnost **Upravit**.
5.  Na kartě **Projektový tým a plánování** klikněte na možnost **Přidat**.
6.  V dialogovém okně **Přidat role** vyberte roli **Softwarový vývojář**.
7.  Klepněte na volbu **Nový**.
8.  Zavřete stránku s projektem.
9.  Klepněte na tlačítko **Řízení a účetnictví projektů** &gt; **Zdroje projektu** &gt; **Plnění prostředků**.
10. Vyberte **Vývojář softwaru 1** pro projekt **Upgrade XYZ fáze 2**.
11. Vyberte pracovníka a klikněte na možnost **Přiřadit**.
12. Ověřte, že byl odstraněn řádek **Vývojář softwaru 1** z projektu **Upgrade XYZ fáze 2**.
13. Na kartě **Projektový tým a plánování** u projektu **Upgrade XYZ fáze 2** ověřte, zda byl přidán pracovník, kterého jste vybrali v kroku 11, jako **Vývojář softwaru**.

## <a name="requests-for-project-resources"></a>Požadavky na prostředky projektu
Funkce plánování zdrojů podporuje pouze správce prostředků k distribuci personálních prostředků k distribuci personálních prostředků nebo projektů. Chcete-li povolit tuto funkci, proveďte následující úlohy nebo ověřte, že byly dokončeny.

-   Nastavte číselné řady.
-   Nastavte workflowy pro řízení a účetnictví projektu.
-   Povolte workflow žádosti o prostředek.

Poté, co jste ověřili nebo dokončili výše uvedené úkoly, můžete provést následující úkoly podle potřeby.

-   Vytvořte požadavek na prostředek z předběžně definovaných personálních prostředků.
-   Monitorujte požadavky na prostředky.
-   Naplňte požadavky na prostředky
-   Požádejte o personální prostředek z WBS.
-   Zarezervujte si zdroje na projektu bez požadavku na personální prostředek.

## <a name="monitor-project-teams"></a>Monitorování projektových týmů
1.  Klikněte na **Řízení projektu a účetnictví** &gt; **Projekty** &gt; **Všechny projekty**.
2.  V seznamu projektů klepněte na odkaz **ID projektu** u projektu **Upgrade XYZ fáze 2**.
3.  Na pevné záložce **Projektový tým a plánování** ověřte správnost uvedených prostředků.





