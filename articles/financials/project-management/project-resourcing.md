---
title: "Prostředky pro projekt"
description: "V tomto tématu jsou informace o přidělování zdrojů k projektu."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8139134ed230cc1525c698fadb20309afee0a68f
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="project-resourcing"></a>Prostředky pro projekt

[!include[banner](../includes/banner.md)]

V tomto tématu jsou informace o přidělování zdrojů k projektu.

Jednou z výzev pro správce projektu a prostředků ve fázi plánování projektu je přiřazení zdrojů, kdy musí určit a rezervovat správné zdroje pro práci na projektu. V aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition umožňuje přidělení zdrojů pro projekty definovat role, které jsou považovány za dočasné zdroje, které mohou být vyhrazeny pro konkrétní pracovní balíček nebo součásti zapojení. Tento typ přidělování zdrojů umožňuje manažerům projektů a zdrojů provádět následující úkony:

- Definovat roli, která má požadované kompetence pro snadné spárování zdrojů.
- Používat role k definování původního schématu zapojení založeného na rezervovaných zdrojích.
- Odhadovat náklady a určovat původní rozpočet na základě přiřazených rolí a zdrojů pro projekt.
- Používat role pro odhad počtu rezervací zdrojů, které jsou nutné pro každé zapojení.
- Odhadovat počet prostředků, které jsou požadovány pro celý životní cyklus projektu.
- Vytvářet koncept strukturovaného rozpisu prací pomocí prvotního přiřazení zdrojů.

[![Životní cyklus projektu](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Jak probíhá plánování projektu, plánované zdroje je možné nahradit personálními zdroji. Manažer projektu se může také vrátit zpět a aktualizovat rezervace zdrojů v libovolné fázi projektu.

## <a name="set-up-project-resources"></a>Nastavení prostředků projektu
Musíte nastavit kalendář a přidružit jej se zaměstnancem nebo pracovníkem. Kalendář lze použít pro naplánování projektu a pracovní doby zdrojů, které jsou na projekt rezervovány. Během nastavení kalendáře může projektový manažer provádět vyrovnání zdrojů v rámci optimalizace zdrojů. Na základě plánu kalendáře lze na zdroje uvalit omezení. Můžete nastavit kalendář na stránce **Kalendáře**.

Pokud nastavíte pracovníka jako projektový zdroj, můžete se vybrat z pracovníků, kteří pracují ve společnosti, pro kterou nastavujete zdroje. Případně můžete vybrat pracovníky z ostatních společností ve vaší organizaci. Tito pracovníci se označují jako mezipodnikové zdroje.

Následující postupy vysvětlují, jak nastavit pracovníka jako zdroj projektu v rámci společnosti a jak nastavit mezipodnikový zdroj projektu.

### <a name="set-up-a-worker-as-a-project-resource"></a>Nastavení pracovníka jako prostředek projektu

1. Na stránce **Pracovníci** v seznamu **Pracovníci** vyberte pracovníka, kterého chcete přidat jako prostředek projektu, a otevřete záznam pracovníka.
2. V podokně akcí zvolte na **Projekt** &gt; **Nastavení** &gt; **Nastavení projektu**.
3. Vyberte kalendář a zavřete stránku.

Můžete také určit výchozí projekty pro prostředky jako typ předběžného přiřazení. Předběžné přiřazení lze použít, pokud manažer prostředků nebo projektu dopředu ví, na kterých projektech budou prostředky pracovat. Předběžné přiřazení může být založeno také na žádosti investora projektu nebo odběratele. Pokud chcete předběžně přiřadit projekt, na stránce **Přiřadit projekty** na kartě **Projekty** v seznamu **Zbývající projekty** vyberte příslušný projekt.

### <a name="set-up-an-intercompany-resource"></a>Nastavení mezipodnikového zdroje

Při nastavování pracovníka jako mezipodnikového zdroje je nutné dokončit nastavení ve společnosti poskytující půjčku a společnosti, která zažádala o půjčku.

**Ve společnosti poskytující půjčku**

1. V aplikaci Finance and Operations ověřte, zda je vybrána společnost poskytující půjčku, a pak dokončete postup uvedený v předchozí části s názvem Nastavení pracovníka jako zdroje projektu.
2. Na stránce **Mezipodnikového účetnictví** vyberte **Nová**.
3. V poli **ID právnické osoby** vyberte společnost poskytující půjčku. Podle potřeby vyplňte zbývající pole a potom zvolte **Uložit**.
4. Na stránce **Mezipodniková cena** vyberte **Nová**.
5. V poli **Právnická osoba, která si půjčuje** vyberte příslušnou společnost.
6. Pokud si chcete od společnosti poskytující půjčku pouze vypůjčit zdroj, který jste vytvořili na začátku této části, v poli **Zdroj**, vyberte název zdroje, který jste vytvořili. Pokud chcete zpřístupnit všechny zdroje společnosti poskytující půjčku společnosti, která si půjčuje, ponechte pole **Zdroj** prázdné.
7. Na stránce **Parametry modulu Řízení a účetnictví projektu** na kartě **Mezipodnikové** nastavte možnost **Povolit mezipodnikové plánování prostředků a časové rozvrhy** na **Ano**.

**Ve společnosti, která zažádala o půjčku** 

- Na stránce **Seznam zdrojů** ve filtru vyhledávání zadejte název zdroje, který jste vytvořili v předchozím postupu pro společnost poskytující půjčku, a ověřte, že název je zahrnut v seznamu zdrojů pro společnost, která žádá o půjčku.

## <a name="manage-resource-competencies"></a>Správa kompetencí prostředků
Kompetence prostředků jsou důležitou částí správy prostředku. Kompetence slouží jako základ pro určení zdroje, který má správný poměr dovedností, vzdělání, kvalifikace a zkušeností s projektem. Doporučujeme nastavit tento údaj pro každý zdroj a aktualizovat jej v pravidelných intervalech. Tímto způsobem můžete maximalizovat možnosti v případě, že jsou porovnány konkrétní kompetence prostředků při přiřazení prostředků k projektu.

[![Příklady dovedností, certifikátů, vzdělání a zkušeností z projektu](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Následující postupy vysvětlují, jak nastavit některé kompetence prostředku.

Pro nastavení kompetencí pracovníka slouží buď stránka se seznamem **Pracovníci** v rámci lidských zdrojů, nebo stránka se seznamem **Prostředky** v rámci Řízení a účetnictví projektů. Pro následující procesy bude použita stránka se seznamem **Pracovníci** v rámci lidských zdrojů.

### <a name="set-up-competencies-certificates"></a>Nastavení kompetencí: certifikáty

1. Na stránce se seznamem **Pracovníci** vyberte řádek zaměstnance, pro kterého přidáváte informace o certifikátu.
2. Na panelu akcí na kartě **Pracovník** ve skupině **Kompetence** zvolte **Certifikáty**.
3. Vyberte **Nový**a poté v poli **Typ certifikátu** vyberte **PMP**.
4. V poli **Počáteční datum** vyberte **10/1/2015**a vyberte **Uložit**.

### <a name="set-up-competencies-skills"></a>Nastavení kompetencí: dovednosti

1. Na stránce se seznamem **Pracovníci** vyberte pracovníka, kterého jste použili v předchozím postupu. Poté v podokně akcí na kartě **Pracovník** ve skupině **Kompetence** zvolte **Dovednosti**.
2. Vyberte možnost **Nový**.
3. V poli **Dovednost** vyberte **Správa projektu**.
4. V poli **Úroveň** vyberte **5 Odborník**.
5. V poli **Datum úrovně** vyberte **1-/14/2014**.
6. V poli **Roky praxe** zadejte **10**.
7. Zvolte **Uložit** a pak zavřete stránku.

## <a name="create-a-new-project"></a>Vytvořit nový projekt
1. Na stránce **Správa projektu** vyberte **Nový projekt** a zadejte následující hodnoty:

    - **Typ projektu:** Čas a materiál
    - **Název projektu:** Upgrade XYZ fáze 2
    - **Skupina projektu:** TM\_WIP
    - **ID projektové smlouvy:** 00000002

2. Zvolte **Vytvořit projekt**.

### <a name="assign-a-resource-to-a-project"></a>Přiřazení prostředku k projektu

1. Na stránce **Pracovníci** v seznamu **Pracovníci** vyberte záznam o zaměstnanci, pro kterého jste dříve nastavili kompetence, a otevřete záznam pracovníka.
2. V podokně akcí na kartě **Projekt** ve skupině **Nastavení** zvolte **Přiřadit projekty**.
3. Na stránce **Přiřazení projektů ověření prostředku** na kartě **Projekty** v poli **Přidat projekt do vybraných projektů** pole filtrujte na projektu **Upgrade XYZ fáze 2**.
4. V podokně **Zbývající projekty** vyberte projekt, zvolte tlačítko šipky a přidejte ho do podokna **Vybrané projekty**.

Podle potřeby můžete také přiřadit kategorie ke zdroji. Typ kategorie jsou buď **Náklady** nebo **Výnosy**. Typ kategorie je určen vaší organizací. Pokud neexistují žádné přiřazené kategorie pro zdroj, aplikace Finance and Operations vyhledává výchozí kategorii pro hodinové ceny pro náklady a výnosy.

### <a name="set-up-project-resource-and-role-characteristics"></a>Nastavení vlastností prostředků a role projektu

Manažer projektu může použít funkci přidělení prostředků k projektu pro vytvoření rolí potřebných pro daný projekt. Role lze použít, pokud potvrzené zdroje jsou během rezervace zdroje zatím neznámé. Role lze použít pro dočasné rezervování jako plánovaných zdrojů, abyste mohli pokračovat ve fázi plánování projektu.

[![Příklad role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scénář:** Společnost Contoso byla najata na dokončení projektu Čas a materiál, který má schválené stanovy projektu. Nižší manažer projektu stále dokončuje rozsah projektu. Manažer prostředků aktuálně identifikuje konkrétní zdroje, které budou rezervovány k práci na novém projektu. S ohledem na kritickou povahu projektu investor projektu požaduje, aby jedna z rolí byla vrchní vedoucí projektu. Správce zdrojů musí získat nový zdroj a rozhodne se, že určí roli v systému pro případ, že nižší manažer projektu bude potřebovat informace o zdroji během plánování projektu.

Následující pokyny popisují, jak může manažer prostředků nastavit roli Vrchní vedoucí projektu a přidružit k ní vlastnosti prostředků. Později slouží role k vyhledání dostupných zdrojů, které odpovídají požadovaným kompetencím prostředku.

1. Na stránce **Nastavení role** vyberte **Nová** a zadejte následující hodnoty:

    - **ID role:** vrchní manažer projektu
    - **Popis:** vrchní manažer projektu

2. Vyberte **Vytvořit**.
3. Vyberte roli **Vrchní manažer projektu** a zvolte **Konfigurace vlastností**.
4. V poli **Typ charakteristik** vyberte **Dovednost**.
5. V poli **Dostupné charakteristiky** zadejte hledanou dovednost.
6. V poli **Typ charakteristiky** vyberte **Certifikát**.
7. V poli **Dostupné charakteristiky** zadejte hledaný typ certifikátu.

### <a name="assign-a-project-resource-to-a-project"></a>Přiřazení prostředku projektu k projektu

1. Na stránce **Všechny projekty** vyberte projekt **Upgrade XYZ fáze 2**.
2. Na kartě **Projektový tým a plánování** zvolte **Přidat**.
3. V poli **Role** vyberte **Člen týmu**.
4. Zvolte **Rezervovat z kalendáře**.
5. Na stránce **Dostupnost prostředku** zvolte **Zobrazit nastavení**.
6. Na stránce **Upravit nastavení zobrazení** zadejte následující hodnoty:

    - **Formát pro zobrazení rozsahu dat:** den
    - **Zobrazit popisy dostupnosti:** ano
    - **Zobrazit zbývající kapacitu:** ano

7. V seznamu zdrojů vyberte prostředek.
8. Vyberte **Závazná rezervace** a **Plná kapacita**.


### <a name="assign-a-resource-to-a-default-role"></a>Přiřazení prostředku k jiné roli

Pokud chcete usnadnit práci manažerům projektu nebo zdrojů, můžete přejít hlouběji do podrobností zdrojů, které lze pro projekt rezervovat. Můžete přiřadit výchozí roli k existujícímu prostředku nebo nově získanému prostředku. Například když byl přijat Daniel, měl zkušenosti a schopnosti plnit roli obchodního analytika. Správce prostředků přiřadil tuto roli Danielovi jako výchozí. Proto správce prostředků přidal Daniela do fondu obchodních analytiků, kteří jsou k dispozici pro práci na projektech.

Během rezervování zdrojů mohou projektoví manažeři filtrovat zdroje v roli, které jsou k dispozici pro práci na projektech. Tyto údaje lze použít jako jednu z kritérií při provádění analýzy rozhodnutí s více kritérii během plnění prostředků. Mohou také přidat další charakteristiky prostředků do filtru a vyhledat zdroje, které mají určité dovednosti, vzdělání a zkušenosti s daným projektem.

**Situace:** začal schválený projekt a role Hlavní manažer projektu byla během fáze plánování projektu rezervována jako plánovaný zdroj. Manažer prostředků získá prostředek pro naplnění role Hlavní manažer projektu.

1. Na stránce **Seznam prostředků** vyberte **Daniel Goldschmidt**.
2. Na stránce **Role prostředku** vyberte **Nový** a zadejte následující hodnoty:

    - **Platnost:** Zadejte aktuální datum.
    - **Vypršení platnosti:** Zadejte **Nikdy**.
    - **Role:** Zadejte **Vrchní manažer projektu**.

3. Zvolte **Uložit** a pak zavřete stránku.
4. Na kartě **Kompetence** přidejte dovednost **ProjectMgmt** a certifikát **PMP**.

## <a name="set-up-role-based-pricing"></a>Nastavení cen na základě role
Pro role lze nastavit všechny náklady, prodeje, a převodní ceny.

1. Na stránce **Prodejní cena (hodina)** vyberte **Nové**a zadejte datum účinnosti.
2. Ve sloupci **Role** vyberte roli.
3. Ve sloupci **Ocenění** zadejte cenu pro vybranou roli prostředku.

## <a name="form-a-project-team"></a>Formování projektového týmu
Pokud chcete použít role, které byly dříve nastaveny, v projektu, projektový manažer musí přiřadit role k projektu. Projektu může být přiřazeno více rolí. Aby se zabránilo nejasnostem, aplikace Finance and Operations automaticky označuje tyto role během rezervace. Například pokud manažer projektu požaduje tři softwarové techniky, automaticky se vygenerují tři role softwarový technik, které jsou pojmenovány jako **Softwarový technik 1**, **Softwarový technik 2** a **Softwarový technik 3**. Pokud byly dříve pro roli nastaveny charakteristiky role, jsou použity jako filtr při hledání zdroje. Pro další upřesnění hledání lze volitelně přidat další charakteristiky.

Možnost Zobrazit nastavení lze také upravit tak, aby poskytovala lepší pohled na dostupnost prostředků. K dispozici je možnost zobrazit dostupnost hodinově, denně, týdně, měsíčně, čtvrtletně a ročně. Existuje také možnost zobrazit dostupnou a zbývající kapacitu prostředků. Tato možnost je užitečná pro časovou správu, pokud odhadujete dostupný čas pro aktivity nebo dostupnost prostředku.

Manažer projektu může vybrat roli na stránce a poté, je-li dostupný prostředek, který odpovídá požadavkům, může vybrat a rezervovat prostředek pro obsazení role. Mějte na paměti, že zdroje nemusí být v této fázi plánování rezervovány. Při vytváření struktury WBS můžete nahradit role skutečnými personálními prostředky pro daný projekt. Pokud role budou nahrazeny skutečnými zaměstnanci ve struktuře WBS, nastavení prostředků automaticky aktualizuje výpis a plánování projektového týmu.

[![Seznam týmů projektu, který obsahuje role a skutečné zdroje](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Vedoucí projektu má řadu možností pro rezervaci zdroje na projekt, například **Zbývající kapacita**, **Plná kapacita**, **Procento kapacity** a **Zadání hodin**. Tyto možnosti rezervace lze kdykoli zrušit v případě, že se změní přiřazení prostředků. Podporovány jsou dva typy rezervace:

- **Závazná rezervace** – Rezervace prostředku byla schválena a práce na projektu byla po určenou dobu trvání potvrzena.
- **Předběžná rezervace** – rezervace prostředku a účast na projektu po určenou dobu trvání je nezávazně schválena.

Při vytváření projektového týmu postupujte následujícím způsobem.

### <a name="create-a-project-team"></a>Vytvoření projektového týmu

1. Na stránce se seznamem **Všechny projekty** vyberte projekt a pak vyberte **Upravit**.
2. Na kartě **Projektový tým a plánování** v poli **Naplánovat koncové datum** zadejte datum zahájení plánu posunuté o jeden měsíc. Je-li datum zahájení plánu například 24. června 2017 (24/06/2017), zadejte **24/07/2017**.
3. Vyberte **přidat**.
4. V podokně **Přidat role do projektu** v poli **Role** vyberte **Vrchní manažer projektu**.
5. Vyberte **Požadované kompetence**.
6. Na stránce **Vybrat charakteristiky** jsou standardně zvoleny charakteristiky, které jste dříve nastavili pro roli Vrchní manažer projektu. Vyberte **OK**.
7. Na stránce **Přidat role do projektu** v poli **Počet prostředků** zadejte **1**.
8. V poli **Prostředek** vyhledávání zobrazí všechny zdroje, které mají požadované kompetence. Vyberte **Daniel Goldschmidt** a vyberte **Vytvořit**.
9. Na stránce **Projekt** vyberte **Přidat**.
10. V podokně **Přidat role do projektu** v poli **Role** vyberte **Člen týmu**. V poli **Počet prostředků** zadejte hodnotu **5**.
11. Vyberte **Vytvořit**.
12. Na stránce **Projekty** vyberte **Splnit prostředek**.

## <a name="resource-capacity-synchronization"></a>Synchronizace kapacity prostředku
Procesy pro synchronizaci prostředků pomáhají zajistit, aby informace pro kalendář a základní kalendář přešly dále do plánování prostředků pro projekt. Pokud dojde ke změně kalendáře, procesy provedou požadované aktualizace v plánování zdrojů pro projekt. Procesy také pomáhají zvýšit výkonnost, protože informace o zdrojích kalendáře jsou synchronizovány v předstihu. Aktualizace informací o plánování zdrojů se děje tudíž rychleji. Doporučujeme naplánovat procesy jako dávku namísto postupného zpracování. V opačném případě je riziko, že někdo zapomene inkluzivní datum, kdy byly informace naposled synchronizovány. Pokud inkluzivní data nejsou použity, mohou vzniknout mezery v synchronizaci dat.

![Synchronizace kalendáře](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Synchronizace shrnutí kapacity pro prostředek

Proces synchronizace umožňuje synchronizovat všechny informace v kalendáři prostředku. Tyto informace zahrnují základní informace z kalendáře o všech změnách v tabulce kapacity kalendáře prostředků projektu. Pokud jsou do projektu přidány nové prostředky, synchronizace pomáhá zajistit, že jsou aktualizované informace k dispozici. Tuto synchronizaci lze provádět kdykoliv.

Doporučujeme používat dávky. Možnosti jsou dostupné při synchronizaci rezervací kapacity.

1. Zvolte **Řízení a účetnictví projektů** &gt; **Periodicky** &gt; **Synchronizace kapacity** &gt; **Synchronizace shrnutí kapacity pro prostředek**.
2. Nastavte možnosti v následující tabulce.

    | Parametr      | popis |
    |-------------|-------------|
    | Kód období | Volitelně vyberte kód datového intervalu hlavní knihy k nastavení počátečního a koncového data pro synchronizaci procesu pro shrnutí kapacity zdrojů. |
    | Počáteční datum  | Zadejte počáteční datum pro proces synchronizace pro shrnutí kapacity zdrojů. |
    | Koncové datum    | Zadejte koncové datum pro proces synchronizace pro shrnutí kapacity zdrojů. |

[![Proces synchronizace](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Nastavení rolí v šablonách WBS
Vedoucí projektu může nastavit šablony WBS, které později použijí při vytváření struktury WBS pro nové projekty. Vedoucí projektu nyní může při vytváření šablony přidat role. Pomocí následujícího postupu se přiřadí role k šabloně WBS. 

1. Vyberte **Řízení a účetnictví projektů** &gt; **Nastavení** &gt; **Projekty** &gt; **Šablony strukturovaného rozpisu prací**.
2. Vyberte **Podrobnosti** u vybrané šablony WBS.
3. Vyberte úkol v seznamu a pak v poli **Role** vyberte roli pro přiřazení k úloze.

### <a name="work-with-a-wbs"></a>Práce se strukturou WBS

Můžete vytvořit novou strukturu WBS, nebo můžete zkopírovat strukturu WBS z existující šablony WBS. Manažer projektu může snadno spravovat prostředky přiřazením rolí k novým úkolům v rámci WBS. Role lze nahradit buď po pořízení zdroje, nebo po určení zdroje, který potvrdil práci na úkolu. Tato možnost umožňuje vedoucím projektu provádět následující úkoly:

- Určit počet prostředků, které jsou požadovány pro balíky práce WBS.
- Odhadovat náklady na projekt.
- Určovat předběžný rozpočet.
- Odhadovat dobu trvání aktivity na základě rolí a zdrojů.
- Vyvíjet některé plány pro vedení projektu, které jsou založené na informacích o projektu.

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
<td>Automaticky přidělíte plánované prostředky pomocí rolí, které jsou přidruženy k úkolu. Aplikace Finance and Operations automaticky navrhuje plánované prostředky použitím analýzy kritérií s více rozhodnutími založené na rolích. Po nastavení rolí a úsilí (hodiny) pro úkoly ve struktuře WBS a po vydání struktury vyberte <strong>Automaticky generovat tým</strong>. Požadovaný počet plánovaných prostředků je přidán do struktury WBS a na kartu <strong>Plánování projektu a týmu</strong>.</td>
</tr>
<tr class="odd">
<td>Prostředek (rozevírací seznam)</td>
<td>Na stránce <strong>Spuštění přiřazení zdrojů </strong>můžete vybrat prostředky, které chcete závazně nebo nezávazně rezervovat podle zadaného trvání. Můžete upravit nastavení zobrazení a prohlédnout si trvání aktivit prostředku. Pomocí následujících možností můžete vybrat a přiřadit prostředky na úrovni balíčku práce:
<ul>
<li><strong>Přijmout</strong> – potvrdit změny u prostředku, který je přiřazen k úkolu.</li>
<li><strong>Storno</strong> – zrušit změny u prostředku, který je přiřazen k úkolu.</li>
<li><strong>Automaticky přiřadit</strong> – Dostupný personální zdroj s odpovídající rolí je automaticky vybrán a přiřazen ke zvolenému úkolu.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Na stránce **Všechny projekty** vyberte projekt **Upgrade XYZ fáze 2**.
2. Vyberte **Plán** &gt; **Aktivity** &gt; **Strukturovaný rozpis prací**.
3. Vyberte **Nový** a přidejte tak následující činnosti první úrovně do struktury WBS:

    - Inicializace
    - Plánování
    - Zpracování
    - Sledování a řízení
    - Zavřít

4. Nastavte data a úsilí (v hodinách), jak je uvedeno na následujícím obrázku.

    [![Nastavení dat a úsilí](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Vyberte řádek úlohy **Inicializace** a v poli **Role** vyberte **Vyšší manažer projektu**.
6. Zvolte **Publikovat**.
7. Na stejném řádku v poli **Zdroj** vyberte **Daniel Goldschmidt** a potom vyberte **Přijmout**.
8. Vyberte řádek úlohy **Plánování** a v poli **Role** vyberte **Obchodní analytik**.
9. Vyberte **Publikovat** a poté vyberte **Automaticky generovat tým**.
10. V otevřeném okně se zprávou vyberte **Ano**.
11. V poli **Prostředek** zkontrolujte, zda je hodnota **Obchodní analytik 1**.
12. U prostředku **Obchodní analytik 1** spusťte vyhledávání a vyberte **Spustit formulář přiřazení prostředku**. Pak vyberte pracovníka pro úlohu.
13. Vyberte**Předběžně přiřadit** &gt; **Plná kapacita**.

    > [!NOTE] 
    > Neobdržíte upozornění, že vybraný prostředek je nyní „2“, protože počet prostředků zůstává „1“.

14. Na stránce **Strukturovaný rozpis prací** ověřte přiřazení prostředku ve struktuře WBS a vyberte **Uložit**.

## <a name="resource-fulfillment-for-planned-resources"></a>Plnění prostředků pro plánované prostředky
Manažer projektu může naplánovat požadované role prostředku pro projekt. Správce prostředků uvidí tyto plánované prostředky jako požadavky na stránce **Plnění prostředků** a má možnost přiřadit skutečné prostředky.

1. Na stránce **Všechny projekty** vyberte projekt **Upgrade XYZ fáze 2**.
2. Vyberte **Projekt** a poté upravit **Upravit**.
3. Na kartě **Projektový tým a plánování** zvolte **Přidat**.
4. V dialogovém okně **Přidat role** vyberte roli **Softwarový vývojář**.
5. Zvolte **Vytvořit** a pak zavřete stránku projektu.
6. Na stránce **Plnění prostředku** vyberte **Vývojář softwaru 1** pro projekt **Upgrade XYZ fáze 2**.
7. Vyberte pracovníka a vyberte **Přiřadit**.
8. Ověřte, že byl odstraněn řádek **Vývojář softwaru 1** z projektu **Upgrade XYZ fáze 2**.
9. Na kartě **Projektový tým a plánování** u projektu **Upgrade XYZ fáze 2** ověřte, zda byl přidán pracovník, kterého jste vybrali v předchozím kroku, jako **Vývojář softwaru**.

## <a name="requests-for-project-resources"></a>Požadavky na prostředky projektu
Funkce pro plánování projektových zdrojů umožní pouze správcům zdrojů distribuovat personální zdroje na aktivity nebo projekty. Chcete-li povolit tuto funkci, proveďte následující úlohy nebo ověřte, že byly dokončeny:

- Nastavte číselné řady.
- Nastavte workflowy pro řízení a účetnictví projektu.
- Povolit workflowy žádosti o prostředek.

Po dokončení předcházejících úkolů můžete provést následující úkoly podle potřeby.

- Vytvořte požadavek na prostředek z předběžně definovaných personálních prostředků.
- Monitorujte požadavky na prostředky.
- Naplňte požadavky na prostředky
- Požádejte o personální prostředek z WBS.
- Zarezervujte si zdroje na projektu bez požadavku na personální prostředek.

## <a name="monitor-project-teams"></a>Monitorování projektových týmů
1. Na stránce **Všechny projekty** vyberte odkaz **ID projektu** pro projekt **Upgrade XYZ fáze 2**.
2. Na pevné záložce **Projektový tým a plánování** ověřte správnost uvedených prostředků.

