---
title: Řízení a účetnictví projektů
description: Funkci řízení projektu a účetnictví lze použít v několika odvětvích k poskytování služeb, výrobě produktů nebo dosažení výsledků.
author: KimANelson
manager: AnnBe
ms.date: 01/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable; ProjProjectManagementWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c21587499a68143d403760ad32bea65948d7fbc9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "311328"
---
# <a name="project-management-and-accounting"></a>Řízení a účetnictví projektů

[!include [banner](../includes/banner.md)]

Funkci řízení projektu a účetnictví lze použít v několika odvětvích k poskytování služeb, výrobě produktů nebo dosažení výsledků.  

Projektu je skupina aktivit sloužící k poskytování služby, produkci produktu nebo dosažení výsledků. Projekty spotřebovávají prostředky a generují finanční výsledky v podobě příjmů nebo majetku.

## <a name="projects-across-industries"></a>Projekty napříč odvětvími
Řízení projektu a funkce účetnictví lze použít v několika průmyslových odvětvích, jak je zachyceno v následujícím obrázku.

[![Projekty napříč odvětvími](./media/projects-accross-industries.jpg)](./media/projects-accross-industries.jpg) 

V kontaktnímu středisku lze příkaz použít k popisu sady akcí, které jsou nutné při řešení volání. Konzultační společnosti, jako jsou například organizace pro management nebo technické konzultace nebo reklamní agentury, odkazují na svou činnost jako projekty. V marketingu kampaň představuje sadu práce, která musí být dodána. V projektové výrobě se výrobní zakázka týká různých prací, které je třeba provést, aby bylo možné vyrábět hotové zboží. Bez ohledu na označení tyto projekty zahrnují prostředky, kalendáře a náklady a funkce řízení projektu a účetnictví v aplikaci Microsoft Dynamics 365 for Finance and Operations vám mohou pomoci s plánováním, prováděním a analýzou těchto projektů.

## <a name="project-phases"></a>Fáze projektu
Ačkoli je následující postup určen pro externí projekty nebo projekty dokončené pro jednoho či více zákazníků, funkce platí i pro interní nákladové projekty. 

![3 fáze projektu](./media/3-stages-of-a-project.png) 

Jak je zobrazeno na předchozím obrázku, řízení projektu a účetnictví může být rozděleno do tří fází:

1.  Počáteční
2.  Spustit
3.  Analyzovat

## <a name="initiate-the-project"></a>Zahájení projektu
Při zahájení projektu nastává několik klíčových procesů. Pomocí nabídky projektu můžete zákazníkovi sdělit odkazovanou práci, výdaje a materiály. Můžete zaznamenat fakturační podmínky, omezení a dohody v projektové smlouvě. Strukturu rozpisu práce (WBS) můžete použít k plánování a odhadu práce. Můžete nastavit spuštění projektu k vedení realizace projektu. Následující ilustrace znázorňuje strukturu projektu.[![struktura projektu](./media/project-structure1.jpg)](./media/project-structure1.jpg)  

### <a name="create-project-quotations"></a>Vytvořit nabídky projektu

V počáteční prodejní fázi projektu vám projektová nabídka umožní poskytnout zákazníkovi nezávazné nabídky. Nabídka může zahrnovat prvky, jako jsou nabízené položky a služby, základní kontaktní údaje, zvláštní obchodní ujednání a slevy, případně daně a příplatky.

Pro transakci nabídky projektu můžete také vydat záruční listinu mezi vaší organizací a odběratelem. Po vytvoření nabídky projektu můžete vytvořit žádost o záruční listinu pro odběratele a odeslat ji do banky. Když banka žádost schválí, záruční listina je vydána odběrateli. 

Další informace naleznete v tématu [Nabídky projektu](project-quotations.md).

### <a name="create-project-contracts"></a>Vytvořit projektové smlouvy

Když vstoupíte do smlouvy s odběratelem nebo jiným zdrojem financování pro dokončení projektu, je nutné nejprve vytvořit projektovou smlouvu. Jakmile poté vytvoříte projekt, je nutné přiřadit ho do odpovídajících smlouvy. Typ projektu, který vytvoříte pro smlouvu projektu, určuje metodu použitou při fakturaci odběratelům projektu. Můžete upravit projektovou smlouvu a související projekt, ale nelze změnit typ projektu. Další informace o typech projektů naleznete v části „Vytvoření projektů”.

Další informace o projektových smlouvách naleznete v tématu [Projektové smlouvy](project-contracts.md).

### <a name="create-work-breakdown-structures"></a>Vytvoření strukturovaného rozpisu prací

Úroveň podrobností ve WBS závisí na přesnosti, která je nutná v odhadech, a úrovni sledování, které je nutné pro tyto odhady. Projekty, které mají velmi nízkou toleranci pro zaostávání za plánem nebo náklady, obvykle vyžadují podrobnější WBS a také důkladné sledování průběhu práce a nákladů vzhledem k WBS. 

Další informace naleznete v tématu [Strukturované rozpisy prací](work-breakdown-structures.md).

### <a name="create-project-forecasts-and-budgets"></a>Vytvoření projektových prognóz a rozpočtů

Prognózu můžete použít, má-li vaše organizace operační perspektivu a zaměřuje se na výnosy a náklady, které jsou odvozeny od specifických transakcí. Pokud se však vaše organizace více zaměřuje na finanční částky, můžete použít rozpočtování. Každá metoda má své výhody. Další informace naleznete v tématu [Prognózy a rozpočty projektu](project-forecasts-budgets.md).

### <a name="create-projects"></a>Vytvořit projekty

V aplikaci Microsoft Finance and Operations můžete vytvořit šest typů projektů. Každý typ projektu je nastaven jinak pro rozpoznávání výnosů a nákladů. Vybraný typ projektu závisí na jeho účelu. V následující tabulce je popsán typický příklad použití všech typů projektů.
                                                                                                            
<table>
  <tr>
    <td>Typ projektu</th>
    <td>Popis</th>
  </tr>
  <tr>
    <td>Čas a materiál</td>
    <td>V časových a materiálových projektech jsou odběrateli účtovány všechny náklady, které na projektu vzniknou. Tyto náklady zahrnují náklady za hodiny, výdaje, položky a poplatky.</td>
  </tr>
  <tr>
    <td>Fixní cena</td>
    <td>Faktury v projektech s pevnou cenou se skládají z transakcí na účet. Projekt s pevnou cenou se fakturuje podle plánu účtování založeného na projektové smlouvě. Výnosy projektu s pevnou cenou je možné vypočítávat a zaúčtovávat v průběhu projektu použitím metody procentuální hodnoty dokončení. Alternativně výnosy je možné vypočítat a zaúčtovat po dokončení projektu použitím metody dokončené smlouvy. Společnosti často těží z používání hodnoty nedokončené výroby (NV) pro výpočet stupně dokončení projektu či skupiny projektů.</td>
  </tr>
  <tr>
    <td>Investiční</td>
    <td>Investiční projekty jsou projekty, které nereprodukují okamžitý výdělek. Obvykle se používají pro dlouhodobé interní projekty, kde náklady musejí být kapitalizovány. Pro investiční projekt je možné zaznamenat pouze náklady položek, hodin a výdajů. Náklady u investičního projektu jsou sledovány a řízeny pomocí oceňovací funkce. Investiční projekty lze nastavit s volitelnou maximální kapitalizací. Během investičního projektu zaznamenáte jeho náklady na účtech NV, kde jsou uložené do dokončení projektu. Pokud je projekt vyřazen, převedete hodnotu NV přenesena do dlouhodobého majetku, účtu hlavní knihy nebo do nového projektu. <br></br> <strong>POZNÁMKA:</strong> Transakce investičních projektů nejsou zobrazeny na stránce <strong>Zaúčtování nákladů<strong>, <strong>Časově rozlišené výnosy</strong>, nebo <strong>Vytvořit návrhy faktur</strong>.</td>
  </tr>
  <tr>
    <td>Nákladový projekt</td>
    <td>Stejně jako v případě investičních projektů se nákladové projekty obvykle používají ke sledování interních projektů a lze pro ně zaznamenat pouze hodiny, výdaje a položky. Nákladové projekty ovšem obvykle trvají kratší dobu než investiční projekty. Navíc narozdíl od investiční projektů nelze nákladové projekty kapitalizovat do rozvahových účtů. Místo toho jejich transakce jsou zaúčtovány pouze na účty zisků a ztrát. <br></br> <strong>POZNÁMKA:</strong> Transakce v nákladových projektech se neprojeví na stránce <strong>Zaúčtování nákladů</strong>, <strong>Časově rozlišené výnosy</strong> nebo <strong>Vytvořit návrhy faktur</strong>. Vzhledem k tomu, že nákladové projekty jsou obvykle používány ke sledování interních projektů, nemusí být obvykle přidruženy k účtu odběratele. Jestliže nastavení vyžaduje vytvoření požadavků na zboží pro nákupní objednávky, musíte přidružit nákladový projekt k odběrateli. Toto přidružení je vyžadováno proto, že požadavky na položku jsou spravovány jako řádky prodejní objednávky a systém vyžaduje zadání odběratele. Toto nastavení však nebude vést k automatické tvorbě žádosti o zboží z nákupní objednávky. U nákladových projektů se nastavení <strong>Vytvořit požadavky na položky</strong> ignoruje. Pokud potřebujete požadavek na zboží u nákladového projektu, můžete ho vytvořit ručně za předpokladu, že odběratel je stále přidružen k projektu.</td>
  </tr>
  <tr>
    <td>Interní</td>
    <td>Interní projekty slouží ke sledování nákladů na projekt, který je interní pro vaši organizaci. Tento typ projektu může poskytnout nástroj plánování pro správu spotřeby prostředků. <br></br><strong>POZNÁMKA:<strong> Transakce investičních projektů nejsou zobrazeny na stránce <strong>Zaúčtování nákladů</strong> nebo <strong>Vytvořit návrhy faktur</strong>.</td>
  </tr>
  <tr>
    <td>Čas</td>
    <td>Časové projekty se používají ke sledování času, který je přidružen s nefakturovatelnými a neproduktivními aktivitami, jako je například projekt pro zaznamenání nemocí pracovníků. Transakce v časových projektech nejsou zaúčtovány do hlavní knihy. Místo toho jsou zahrnuty do sestavy využití pracovníka. Do časových projektů lze zaznamenat pouze hodinové transakce. K registraci těchto hodin na projektu použijete deník hodin nebo časový rozvrh. Po zaregistrování hodin se zobrazí jako transakce projektu, ale bez odpovídajícího dokladu transakce. <br></br><strong>POZNÁMKA:</strong> Transakce v časových projektech se neprojeví na stránce <strong>Zaúčtování nákladů</strong>, <strong>Časově rozlišené výnosy</strong>, nebo <strong>Vytvořit návrhy faktur</strong>.</td>
  </tr>
</table>


### <a name="assign-workers-categories-and-resources"></a>Přiřazení zaměstnanců, kategorií a prostředků

Pracovní zdroje můžete plánovat na základě požadavků a plánu projektu nebo podle kvalifikace a dostupnosti pracovníků. Pomocí možností plánování zdrojů můžete efektivně využívat lidské zdroje v organizaci. Můžete rychle vyhledat nejlépe kvalifikované pracovníky, kteří jsou pro práci na projektu k dispozici. Můžete také snadno zobrazit zaměstnance, které je v průběhu projektu možné využít efektivněji. 

Zde jsou některé možnosti, které můžete použít ve funkci plánování prostředků:

-   Používat informace o atributech pracovníka, jako je například vzdělání, dovednosti, certifikáty a zkušenosti z projektu k přiřazení pracovníka podle požadavků projektu.
-   Použití informací o kalendáři a dostupnosti pracovníka k porovnání plánu pracovníka s kalendářem projektu.
-   Kontrola kapacity jednotlivých pracovních a určení způsobu, jak se tato kapacita využívá. Pokud je například pracovník nedostatečně využíván, může být přiřazen k projektu, který odpovídá jeho dostupnosti a vlastnostem.
-   Zobrazení dostupnost pracovníka, abyste se ujistili, že neexistují žádné konflikty kalendáře s jeho přiřazeními.
-   Zkontrolujte informace o využití pracovníka buď v souhrnném zobrazení (například podle oddělení nebo pracovníka), nebo v podrobném zobrazení (například podle pracovníků v oddělení nebo podle týdenních podrobností pro každého pracovníka).
-   Úprava přiřazení zdrojů pro různé časové jednotky, jako je den, týden nebo měsíc k optimalizaci způsobu použití pracovníků.

## <a name="execute-the-project"></a>Spuštění projektu
Během provádění projektu členové týmu nebo manažeři zaznamenávají práci a vzniklé výdaje pomocí časových rozvrhů, sestav výdajů a jiných obchodních dokumentů. Manažeři projektu mají nástroje, které umožňují sledovat spotřebu rozpočtových částek pro projekt. Manažeři projektu mohou také objednávat, vyzvedávat a pořizovat materiály pro projekty pomocí nákupních objednávek a jiných obchodních dokumentů. Faktury jsou připraveny a schváleny, takže odběratelům lze probíhající práci účtovat. Výnos je uznán v průběhu tohoto procesu, aby ovlivnil finance organizace.

### <a name="manage-work-breakdown-structures"></a>Správa strukturovaného rozpisu prací

WBS je popis práce, která bude dokončena pro projekt. WBS je hierarchie úkolů. Představuje nejen práci na každém úkolu, ale také velikost, náklady a dobu trvání úkolu. 

Další informace naleznete v tématu [Strukturované rozpisy prací](work-breakdown-structures.md).

### <a name="manage-project-forecasts-and-budgets"></a>Správa projektových prognóz a rozpočtů

Existují dva způsoby, jak spravovat a řídit projekty: prognózy projektu a rozpočty projektu. Prognózu můžete použít, má-li vaše organizace operační perspektivu a zaměřuje se na výnosy a náklady, které jsou odvozeny od specifických transakcí. Pokud se však vaše organizace více zaměřuje na finanční částky, můžete použít rozpočtování.

Další informace naleznete v tématu [Prognózy a rozpočty projektu](project-forecasts-budgets.md).

### <a name="create-production-orders"></a>Vytvoření výrobní zakázky

Projekt související s výrobní zakázkou lze propojit s prodejní objednávkou nebo požadavkem na položku buď použitím metody dokončené položky, nebo metodou spotřebované položky. Pokud navíc byla výrobní zakázka vytvořena ručně, není mezi výrobní zakázkou a prodejní objednávkou nebo požadavkem na položku žádné propojení (žádné propojení k objednávce). Když však byla výrobní zakázka vytvořena automaticky ke splnění prodejní objednávky nebo s požadavku na položku, existuje propojení mezi výrobní zakázkou a prodejní objednávkou nebo požadavkem na položku (propojení k objednávce). 

V závislosti na kombinací uvedených činitelů použijte jednu z následujících metod:

- **Dokončená položka/propojení k objednávce** – Propojte projekt s nákupní objednávkou nebo s požadavkem na položku. Když použijete tuto metodu, skutečné náklady projektu se zaúčtují při vystavení faktury prodejní objednávky nebo při aktualizaci dodacího listu požadavku na položku. Tyto náklady se zaúčtují jako dokončená položka.
- **Dokončená položka/bez propojení k objednávce** – skutečné náklady nelze zaúčtovat, dokud výrobní cyklus položky není ve stavu **Ukončeno**. Náklady na dokončenou položku se zaúčtují jako jedna transakce.
- **Spotřebovaná položka/propojení k objednávce** – Propojte projekt s požadavkem na položku. Při použití této metody budete moci zobrazit skutečné náklady projektu v případě, že se výroba nachází ve stavu **Zahájeno** nebo je označena za dokončenou. Náklady jsou zaúčtovány jako několik transakcí položek projektu pro suroviny a hodiny spotřebované pro výrobu. Při aktualizaci dodacího listu pro požadavek na položku nedojde k zaúčtování žádných nákladů na projekt. Můžete také definovat úroveň hierarchie kusovníku, po kterou se projekty ve výrobě sledují.
- *<strong><em>Spotřebovaná položka/bez propojení k objednávce</em></strong>* – Propojte projekt s požadavkem na položku. Při použití této metody budete moci zobrazit skutečné náklady projektu v případě, že se výroba nachází ve stavu <strong>Zahájeno</strong> nebo je označena za dokončenou. Náklady se zaúčtují jako několik transakcí položek projektu pro suroviny a hodiny spotřebované pro výrobu. Můžete také definovat úroveň hierarchie kusovníku, po kterou se projekty ve výrobě sledují.

### <a name="procure-products-and-services"></a>Zajišťování produktů a služeb

Nákup a prodej položek jsou běžnými aktivitami v mnoha firmách zaměřených na projekty.

#### <a name="purchase-orders-for-projects"></a>Nákupní objednávky pro projekty

Účel nákupní objednávky určuje, kdy je nákupní objednávka spotřebována a tedy kdy lze na projektu účtovat poplatky za položky.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metoda</th>
<th>Účel</th>
<th>Spotřeba položek</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Přímé vytvoření nákupní objednávky</td>
<td>Nakupte položky od externího dodavatele pro účely spotřeby na projektu. Nákupní objednávky lze vytvořit následujícími způsoby:
<ul>
<li>Ze samotného projektu. V tomto případě je projekt pro nákupní objednávku již definován.</li>
<li>Přechodem k nákupní objednávce projektu. Je nezbytné vybrat jak dodavatele, tak projekt, pro který se má nákupní objednávka vytvořit.</li>
</ul></td>
<td>Položky jsou spotřebovány při aktualizaci faktury dodavatele.</td>
</tr>
<tr class="even">
<td>Vytvořte nákupní objednávku z prodejní objednávky.</td>
<td>Nakupte položky při vytváření prodejní objednávky z projektu.</td>
<td>Položky jsou spotřebovány, když se prodejní objednávka fakturuje odběrateli.</td>
</tr>
<tr class="odd">
<td>Vytvořte nákupní objednávku z požadavku na položku.</td>
<td>Nakupte položky, když vytváříte požadavek na položku z projektu.</td>
<td>Položky jsou spotřebovány, když se aktualizuje dodací list požadavku na položku.</td>
</tr>
</tbody>
</table>

#### <a name="sales-orders-for-projects"></a>Prodejní objednávky pro projekty

V části Řízení a účetnictví projektů můžete zaregistrovat spotřebu položek několika způsoby. Můžete prodávat položky z projektu nebo do něj nakupovat, případně vyhradit položky pro projekt. 

Můžete objednat položky ze skladu společnosti pro spotřebu na projektu. Nebo můžete nakoupit položky od externího dodavatele. Položky lze spotřebovávat ve všech typech projektů s výjimkou časových projektů. 

Způsob objednání zboží závisí na tom, odkud objednáváte:

-   Chcete-li objednat položky ze skladu společnosti, je nutné objednávku zadat jako požadavek na položku. Při použití stránky **Požadavky na položku** je možné požadavek nastavit tak, abyste položky přijímali jako součást dodávek.To znamená, že spotřebu množství položek můžete posunout, dokud tyto položky nebudou vyžadovány.
-   Pro objednání položky od externího dodavatele je nutné tuto objednávku vytvořit jako nákupní objednávku na stránce **Nákupní objednávka**.

> [!NOTE] 
> Dodací list pro prodejní objednávky související s projektech nelze zrušit, pokud již položky byly označeny k balení. 

V následující tabulce jsou uvedeny metody objednávání položek a popis, jak jsou položky spotřebovány.

| Metoda            | Účel                                                                                                                                                        | Spotřeba nových transakcí                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Prodejní objednávka       | Zadejte transakci přímo do projektu určeného časem a materiálem.                                                                                                   | Transakce položek jsou spotřebovány při zaúčtování faktury odběratele.                                                                               |
| Deník inventáře | Rychle zadejte a spravujte záznamy položek. Chcete-li například zadat požadavek na položku založený na vytištěném seznamu, bude použit skladový deník. | Transakce položek jsou spotřebovány při zaúčtování deníku.                                                                                        |
| Požadavek na položku  | Zadejte položky, které nebudou okamžitě spotřebovány. Tato metoda vám umožňuje sledovat počet spotřebovaných položek v jednom záznamu požadavků na položku.    | Transakce položek jsou spotřebovány při aktualizaci dodacího listu. Požadavek na položku je tedy jinými slovy vytvořen při zaúčtování dodacího listu. |
| Nákupní objednávky   | Zadejte transakce do jednoho ze tří různých umístění v závislosti na metodě nákupu.                                                                              | Transakce položek jsou spotřebovány při aktualizaci dodacího listu nebo při fakturaci odběratele nebo dodavatele.                                      |

### <a name="process-project-invoices"></a>Zpracování faktur projektu

Typ projektu stanoví, který fakturační postup by měl být použit. Fakturovat lze pouze dva typy externích projektů (časový a materiálový projekt nebo projekt s fixní cenou). Časové a materiálové projekty a projekty s pevnou cenou jsou vždy připojeny k projektové smlouvě. 

Před vytvořením faktury odběratele pro projekt můžete vytvořit předběžnou fakturu nebo návrh faktury. Do návrhu faktury můžete vybrat projektové transakce, které mají být zahrnuty do faktury projektu. Poté můžete zobrazit podrobnosti faktury před zaúčtováním faktury projektu a jejím odesláním odběrateli nebo jinému zdroji financování. 


Další informace o zpracování faktur projektu naleznete v tématu [Fakturace projektu](../accounts-payable/project-invoicing.md).


### <a name="calculate-the-cost-to-complete-a-project"></a>Výpočet nákladů na dokončení projektu

Při vytváření odhadu můžete zvolit metodu, která se použije k výpočtu nákladů na dokončení projektu. Vyberte metodu v poli **Metoda nákladů na dokončení** na stránce **Vytvořit odhad**. Vybraná metoda se použije samostatné v každém řádku nákladů v odhadu nákladů. Když je řádek ve stavu **Vytvořeno**, můžete změnit metodu, která se použije na stránce **Odhad nákladů**. 

V následující tabulce jsou popsány metody pro výpočet nákladů na dokončení projektu.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Metoda</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Celkové náklady – skutečné</td>
<td>Odhadované náklady je nutné zadat ručně. Po vyplnění sloupce <strong>Celkové náklady</strong> nebo <strong>Celkové množství</strong> na stránce <strong>Odhad nákladů </strong>se skutečné náklady odečtou od součtů zadaných uživatelem. Výsledek představuje náklady na dokončení projektu. Průběh nákladů se obvykle nesleduje na základě například počtu hotelových pobytů a nákladů na stravování zaznamenaných v každém období. Namísto. Sledování je obvykle založeno na porovnání s celkovou částkou odhadovaných hodin. Tato metoda nevyžaduje model prognózy a celkové náklady nebo celkové množství lze změnit ručně. Když se zadá hodnota ve sloupci <strong>Celkové náklady</strong> nebo <strong>Celkové množství</strong>, aplikace Finance and Operations porovnává tuto hodnotu se skutečnými transakcemi, které jsou zaúčtovány v období, a potom snižuje hodnotu ve sloupci <strong>Množství k dokončení</strong> nebo <strong>Náklady na dokončení</strong>.</td>
</tr>
<tr class="even">
<td>Celkový rozpočet – skutečný</td>
<td>Skutečné náklady se porovnávají s modelem prognózy, který jste vybrali k určení nákladů. Tato metoda používá model celkového rozpočtu, který obsahuje prognózy transakcí. Pro získání přesnějšího přehledu o projektu můžete upravit rozpočtový model, zatímco projekt probíhá. Pokud je nutné upravit prognózu, toto je obecný postup:
<ol>
<li>Zkopírujte transakce prognózy do jiného modelu prognózy.</li>
<li>Porovnejte transakce prognózy se skutečnými transakcemi.</li>
<li>Zachovejte, snižte nebo zvyšte odhady pro další období.</li>
</ol>
Finance and Operations nesnižuje automaticky prognózované odhady. Je proto vhodné zachovat původní model prognózy projektu s pevnou cenou, aby se vytvořila základna pro srovnání při dokončení projektu. 
<br></br> <strong>POZNÁMKA:</strong> Vyberete-li tuto metodu, použijte nejméně dva modely prognóz. Jeden model by měl obsahovat původní prognózy. Pro další model je třeba z jiného modelu zkopírovat transakce prognózy. Tato metoda je platná pouze pro projekty s pevnou cenou a pro investiční projekty.</td>
</tr>
<tr class="odd">
<td>Zbývající rozpočet</td>
<td>Tato metoda používá zbývající rozpočtový model pro výpočet nákladů na dokončení projektu. Pokud použijete tuto metodu, skutečné náklady a prognózy částek ve zbývajícím rozpočtovém modelu se sečtou. Výsledkem jsou celkové náklady. Než použijete tuto metodu, zbývající rozpočtový model se musí nastavit k odečítání transakcí podle skutečných transakcí, které jsou zaznamenány v systému. Na stránce <strong>Modely prognóz</strong> se ujistěte, že pole ve skupině <strong>Automatické snížení prognózy</strong> jsou označena. Zbývající rozpočet se obvykle zkopíruje z původního rozpočtu. Při zadávání transakcí se sníží transakce ve zbývajícím rozpočtu. Pokud v průběhu projektu zjistíte, že se musí upravit zbývající rozpočet, změňte transakce prognózy do zbývajícího rozpočtu. <br></br> <strong>POZNÁMKA:</strong> Tuto metodu je možné použít pouze v případě, že je model prognózy přiřazen k odhadu.</td>
</tr>
<tr class="even">
<td>Jako předchozí odhad</td>
<td>Použije se stejná metoda odhadu, která byla použita v předchozím období. Tato metoda vyžaduje model prognózy, pokud předchozí období vyžadovalo model prognózy.</td>
</tr>
<tr class="odd">
<td>Nastavit náklady dokončení na nulu</td>
<td>Tato metoda se obvykle používá předtím, než se eliminuje projekt odhadu. Tato metoda přiřadí celkové odhady skutečným transakcím, které byly zaúčtovány, a vymaže sloupec <strong>Náklady na dokončení</strong>. Výsledná procentuální hodnota dokončení je vždy 100 procent. Pole <strong>Prognózování</strong> není vybráno pro každý řádek nákladů, který vytvoříte, a celkový odhad se zkopíruje z předchozího odhadu nákladů. Aktuální spotřeba pro období odhadu je odvozena z nákladů na dokončení projektu. Tato metoda nevyžaduje model prognózy.</td>
</tr>
<tr class="even">
<td>Z šablony nákladů</td>
<td>Použijí se náklady na dokončení metody, která je nastavená ve šabloně nákladů přidružené k vybranému projektu odhadu.</td>
</tr>
</tbody>
</table>

## <a name="analyze-the-project"></a>Analýza projektu
Na nejzákladnější úrovni projekt slouží k seskupení transakcí, které zaznamenávají náklady, a poté k zaúčtování těchto nákladů do hlavní knihy. 

Obecně platí, že tyto transakce jsou výsledkem obchodních dokumentů, například časových rozvrhů, vyúčtování výdajů, faktur dodavatele nebo skladových transakcí. Životní cyklus projektu obvykle začíná u odhadů, prognóz a rozpočtů, které pomáhají plánovat a odhadnout pracovní a finanční dopady projektu. Při analýze projektu můžete vyhodnotit nejen transakce, ke kterým došlo během projektu, ale také přesnost prognóz a odhadů, úrovně využití členů týmu a celkový úspěch projektu.

### <a name="analyze-cash-flow"></a>Analýza cashflow

Použijte monitorování cashflow ke sledování prognóz cashflow i aktuálního cashflow projektu. Kontrolovat cashflow můžete v průběhu zpracování projektu nebo můžete zobrazit cashflow dokončeného projektu. 

Pomocí monitorování cashflow můžete vyhodnocovat jednotlivé projekty, zobrazit více projektů pomocí sestav nebo převést cashflow projektu do prognóz cashflow v hlavní knize.

#### <a name="cash-inflow-forecasting"></a>Prognóza cashflow

Na základě vašeho nastavení můžete vytvořit prognózu cashflow pro vybraný projekt. Pokud je například datem projektu 5. březen 2012 a fakturujete 31. března 2012, následujícím způsobem můžete vytvořit prognózu data splatnosti a očekávaného data platby prodeje:

-   **Datum projektu:** 5. březen 2012.
-   **Datum faktury:** 31. březen 2012. Toto datum závisí na četnosti faktur. V tomto příkladu nastavujete četnost faktur na aktuální měsíci. Z toho vyplývá, že všechny transakce, které jsou zaúčtované v měsíci březnu, budou fakturovány v poslední den v měsíci.
-   **Datum splatnosti:** 14. duben 2012. Toto datum je stanoveno podle platebních podmínek nastavených pro projekt. V tomto příkladu jste vybrali platební podmínky o délce 14 dní. 14 dní se tedy přidá k datu faktury, aby se dosáhlo data splatnosti 14. dubna 2012.
-   **Očekávané datum platby prodeje:** 27. duben 2012. Toto datum se vypočítává přičtením počtu dnů v poli **Obecné pojistné dny** na stránce **Parametry modulu Řízení a účetnictví projektu**  k počtu dnů v poli **Jednotlivé pojistné dny** na stránce **Projektové smlouvy**, a poté přičtením součtu k celkovému počtu dnů v poli **Datum splatnosti**. V tomto příkladu jste zadali hodnotu **3** do pole **Obecné pojistné dny** a hodnotu **10** do pole **Jednotlivé pojistné dny**. 13 dní se tedy přičte k datu splatnosti, aby se dosáhlo předpokládaného data platby prodeje 27. dubna 2012.

Obecné pojistné dny mohou buď nahradit jednotlivé pojistné dny, nebo je lze přičíst k jednotlivým pojistným dnům:

-   Chcete-li použít obecné pojistné dny jako náhradu za jednotlivé pojistné dny, zadejte průměrný počet dnů mezi datem splatnosti a skutečným datem platby pro odběratele.
-   Chcete-li přidat obecné pojistné dny k jednotlivým pojistným dnům, v poli **Obecné pojistné dny** zadejte odhadovaný počet dní mezi dnem, kdy zákazník odešle platbu, a dnem, kdy organizace platbu přijme.

Nastavte jednotlivé pojistné dny v projektové smlouvě. Počet dnů se vypočte na základě dne splatnosti prodejní faktury a na základě zkušeností, které má vaše společnost se vzorci chování odběratelů při platbě.

#### <a name="actual-cash-inflow"></a>Skutečný přírůstek hotovosti

Skutečný přírůstek hotovosti se podobá prognóze, ale výpočty můžete zahájit od prvního data faktury. Zde je příklad:

-   **Datum faktury:** 2. březen 2012.
-   **Datum splatnosti:** 16. březen 2012. Platební podmínky jsou nastavené na 14 dní.
-   **Očekávané datum platby prodeje:** 29. březen 2012. Výpočet zahrnuje tři obecné pojistné dny a 10 jednotlivých pojistných dnů.

#### <a name="cost-forecasting"></a>Prognóza nákladů

V závislosti na definovaném počtu dní se bude datum platby nákladů může lišit od data projektu. V takovém případě bude datum platby nákladů vypočítáno přičtením počtu dnů od data projektu k počtu dnů v platebních podmínkách. 

Například datum transakce projektu je 5. březen 2012 a jsou nastaveny následující platební podmínky:

-   **Hodiny:** Aktuální měsíc (**M**)
-   **Výdaje:** 14 dnů (**D14**)
-   **Položky:** 30 dnů (**D30**)

Na základě tohoto nastavení je datum platby nákladů pro každý typ transakce zde:

-   **Počet hodin:** 31. březen 2012, což je poslední den vybraného měsíce.
-   **Výdaje:** 19. březen 2012, což je 14 dní po datu transakce.
-   **Položky:** 4. duben 2012, což je 30 dní po datu transakce.

> [!NOTE] 
> Datum splatnosti nákupní objednávky je založeno na transakci dodavatele v době vytvoření nákupní objednávky projektu. Datum splatnosti se neurčuje podle žádného výchozího nastavení. 

Datum platby nákladů se nepočítá v pojistných dnech. Až je projekt dokončen a veškeré náklady a fakturace jsou úplné, náklady a prodeje se zaúčtují na účty výnosů a ztrát. 

Až jsou všechny faktury dodavatele a prodeje dokončeny, můžete zobrazit vztah mezi poli na stránce **Cashflow** a poli na stránce **Výkazy projektu**.

:::row:::
    :::column:::
        #### Cash flow page
        - Cash inflows 
        - Cash outflows
        - Net cash flows
    :::column-end:::
    :::column:::
        #### Project statements page
        - Revenue
        - Total cost
        - Gross margin
    :::column-end:::
:::row-end:::

### <a name="review-costs"></a>Kontrola nákladů

Náklady, které vaše organizace vynaloží v průběhu projektu, lze sledovat na stránce **Řízení nákladů**. Porovnáním původních rozpočtových nákladů pro projekt s aktuálními skutečnými náklady a potvrzenými náklady lze zjistit, zda projekt běží podle plánu, překračuje rozpočet nebo rozpočet nevyužívá naplno. 

> [!NOTE] 
> Poznámka: používáte-li stránku **Řízení nákladů** k zobrazení stavu aktuálních nákladů projektu, použijte modely prognózy, které byly vybrány pro původní i zbývající rozpočet. Pokud při výpočtu nákladů zaškrtnete jiné modely prognóz, výsledky výpočtu nebudou přesné.

#### <a name="viewing-the-remaining-budgeted-amounts"></a>Zobrazení zbývajících rozpočtových částek

Je-li vybrána možnost **Zbývající rozpočet** jako metoda řízení nákladů na stránce **Parametry modulu Řízení a účetnictví projektu**, stránka **Řízení nákladů** vypočte náklady, které nebyly zaúčtovány jako skutečné nebo označeny jako potvrzené. Konkrétně částky na kartě **Hlavní** v dolním podokně stránky **Řízení nákladů** se počítají následujícím způsobem:

-   **Skutečné náklady** – celková částka, která se utratila za projekt pro vybraný řádek nákladů. Částka skutečných nákladů se vypočítává na stránce **Aktualizace hlavní knihy**.
-   **Potvrzené náklady** – další částky výdajů, které se právnická osoba zavázala platit. Konkrétní potvrzené nákladové částky se vypočítávají na stránce **Potvrzené náklady**.
-   **Zbývající rozpočet** – částka z původní částky rozpočtu, která je stále k dispozici pro vybraný řádek nákladů. Zbývající částka rozpočtu se vypočítává na stránce **Náhled hlavní knihy**.
-   **Celkové náklady** – součet skutečných nákladů, potvrzených nákladů a zbývající částek rozpočtu.

Na stránce **Řízení nákladů** na kartě **Odchylka** lze zobrazit porovnání celkových očekávaných nákladů s původním rozpočtem. Toto porovnání ukazuje rozdíly mezi částkami. Poté se zobrazí, kde se data neshodují. Částky odchylky jsou vypočteny následujícím způsobem:

-   **Původní rozpočet** – částka, která byla původně rozpočtovaná pro vybraný řádek nákladů. Původní částka rozpočtu se vypočítává na stránce **Náhled hlavní knihy**.
-   **Celkové náklady**– součet skutečných nákladů, potvrzených nákladů a zbývající částky rozpočtu, jak je uvedeno na kartě **Obecné**.
-   **Odchylka** – rozdíl mezi celkovými náklady a původním rozpočtem.
-   **Odchylka založená na množství** – celkový rozdíl mezi původní prognózou a celkovou prognózou. Tento rozdíl lze vyjádřit matematicky jako (celková cena z prognózy) × (původní průměrná cena – celková průměrná cena). Tato kalkulace se vztahuje pouze k hodinám projektu.
-   **Odchylka založená na ceně** – celkový rozdíl mezi původní prognózou a celkovou prognózou. Tento rozdíl lze vyjádřit matematicky jako (celková cena z prognózy) × (původní množství z prognózy – celkové množství z prognózy). Tato kalkulace se vztahuje pouze k hodinám projektu.

#### <a name="viewing-the-total-budgeted-amounts"></a>Zobrazení celkových rozpočtových částek

Pokud je vybrána možnost **Celkový rozpočet** jako řídicí metoda nákladů na stránce **Parametry modulu Řízení a účetnictví projektu**, stránka **Řízení nákladů** vypočítává skutečné a celkové náklady projektu, aby pomohla určit jakýkoliv rozdíl mezi těmito dvěma hodnotami. Konkrétně částky na kartě **Hlavní** ve sloupcích v dolním podokně stránky **Řízení nákladů** se počítají následujícím způsobem:

-   **Celkové náklady rozpočtu** – celková částka pro vybraný řádek nákladů rozpočtu.
-   **Skutečné náklady** – celková částka, která se dosud vydala za projekt pro vybraný řádek nákladů.
-   **Potvrzené náklady** – celková částka, která se potvrdila za projekt pro vybraný řádek nákladů.
-   **Odchylka** – rozdíl mezi součtem skutečných a potvrzených nákladů a celkových nákladů. Odchylka ukáže, zda je k celkovému rozpočtu nutné určit vedlejší náklady.

Na stránce **Řízení nákladů** na kartě **Odchylky** si můžete prohlédnout rozdíl mezi celkovým rozpočtem a původním rozpočtem v následujících polích:

-   **Původní rozpočet** – částka, která byla původně rozpočtovaná pro řádek nákladů. Původní rozpočet se vypočítává na stránce **Náhled hlavní knihy**.
-   **Celkové náklady rozpočtu** – celkové náklady, která se původně rozpočtovaly pro řádek nákladů. Celkové náklady rozpočtu se vypočítávají na stránce **Náhled hlavní knihy**.
-   **Odchylka** – odchylka řádku nákladů. Tuto částku lze vypočítat odečtením celkových nákladů od původního rozpočtu.
-   **Odchylka založená na množství** – celkový rozdíl mezi původním rozpočtem a celkovým rozpočtem. Tato částka se vypočte odečtením celkového počtu hodin rozpočtu od původního počtu hodin rozpočtu a následným vynásobením tohoto rozdílu původní cenou rozpočtových nákladů. Rozdíl lze vyjádřit matematicky jako (původní cena rozpočtových nákladů) × (původní počet hodin rozpočtu – celkový počet hodin rozpočtu). Tato kalkulace se vztahuje pouze k hodinám projektu.
-   **Odchylka založená na ceně** – tato částka se vypočte odečtením celkového počtu hodin rozpočtu od původního počtu hodin rozpočtu a následným vynásobením tohoto rozdílu celkovým počtem spotřebovaných hodin. Rozdíl lze vyjádřit matematicky jako (celkový počet spotřebovaných hodin) × (původní počet hodin rozpočtu – celkový počet hodin rozpočtu). Tato kalkulace se vztahuje pouze k hodinám projektu.

### <a name="analyze-utilization"></a>Analýza využití

Míra využití je procento času, ve kterém pracovník provádí fakturovatelnou nebo výrobní práci v určitém období pracovní doby. Fakturovatelné hodiny jsou hodiny pracovníka, které lze účtovat konkrétnímu odběrateli. 

Míra využití zaměstnance se vypočítá vydělením počtu fakturovatelných hodin počtem pracovních hodin v určitém období. Například pokud má pracovník 30 fakturovatelných hodin za období a počet pracovních hodin ve stejném období je 40, míra využití pracovníka je 75 procent. 

Když vypočítáváte míru využití pracovníka, můžete vypočítat buď fakturovatelnou sazbu, nebo míru účinnosti:

-   **Fakturovatelná sazba** – rozdíl mezi fakturovatelnými hodinami a nefakturovatelnými hodinami nebo normovanými hodinami.
-   **Míra účinnosti** – rozdíl mezi produktivními hodinami a neproduktivními hodinami nebo normovanými hodinami. Produktivní hodiny jsou hodiny, které pracovník stráví přispíváním ke specifickému projektu. Produktivní hodiny se obvykle účtují odběratelům, s výjimkou interních projektů. Neproduktivní hodiny se nikdy neúčtují odběrateli.

Míry využití počítáte na stránce **Využití hodin**. Výpočty jsou založeny na výchozích předvolbách. Tyto předvolby také určují, jak hodiny se vypočítávají, přiřazením **Využití** nebo **Režie** k jednotlivým typům projektu. To se vztahuje na výpočty fakturovatelné sazby a výpočty míry účinnosti.

-   **Využití** – hodiny, které jsou nahlášeny pro vybraný typ projektu, se vždy zahrnou do fakturovatelných nebo využití účinnosti.
-   **Režie** – hodiny, které jsou nahlášeny pro vybraný typ projektu, se vždy zahrnou do nefakturovatelných nebo využití neúčinnosti.
-   **Podle vlastnosti řádku** – vlastnosti řádku konkrétní hodinové transakce určují, zda se hodiny zahrnou do fakturovatelného nebo využití účinnosti.
-   **Nezahrnuto** – hodiny se nezahrnou do výpočtu fakturovatelných nebo využití účinnosti.

Na stránce **Využití hodin** můžete kromě celkové procentuální míry využití pro pracovníka nebo projekt zobrazit počet hodin, které byly použity při výpočtu míry využití pro každý z následujících typů hodin:

-   **Nezahrnuté hodiny** – tyto hodiny nejsou zahrnuty do míry využití hodin.
-   **Zahrnuté hodiny** – tyto hodiny se počítají sečtením hodin využití a hodin režie. Tyto hodiny se zahrnují do míry využití.
-   **Režijní čas** – pokud počítáte fakturovatelnou sazbu, tyto hodiny jsou stejné jako nefakturovatelné hodiny. Jestliže počítáte míru účinnosti, tyto hodiny jsou stejné jako neproduktivní hodiny.
-   **Využitý čas** – pokud počítáte fakturovatelnou sazbu, tyto hodiny jsou stejné jako fakturovatelné hodiny. Jestliže počítáte míru účinnosti, tyto hodiny jsou stejné jako produktivní hodiny.

Při výpočtu míry využití pro pracovníka můžete použít normované hodiny nebo zahrnuté hodiny. Používáte-li zahrnuté hodiny, je nutné zajistit, aby pracovníci zaznamenali veškerý pracovní čas pro období časového rozvrhu, protože výpočet je vyjádřený jako procento hodin, které jsou zadány. Při výpočtu míry využití hodin pro projekt, projektovou smlouvu, záznam odběratele nebo kategorii je nutné použít zahrnuté hodiny při výpočtu.

### <a name="review-project-statements"></a>Zobrazení výkazů projektu

Můžete vytvořit výkaz projektu, abyste zobrazili rychlý náhled vývoje projektu. Při spuštění výkazu projektu můžete zadat kritéria, která se používají pro výpočet výkazu, výběrem na kartě **Hlavní** na stránce **Příkazy projektu**. Můžete vybrat zahrnutí nebo vynechání následujících informací:

-   Typy projektů
-   Typy transakcí
-   Datum projektu / datum hlavní knihy
-   Údaje

Po výpočtu výkazu můžete zobrazit následující informace na různých kartách na stránce **Výkazy projektu**:

-   **Hlavní** – obecné informace o základních strukturách zisku a ztráty projektu.
-   **Zisky a ztráty** – informace o časově rozlišených výnosech.
-   **VN** – informace o zůstatcích účtů NV.
-   **Spotřeba** – informace o spotřebě hodin, výdajů, položek a mzdových transakcí.
-   **Faktura** – informace o fakturách a fakturaci na účet.
-   **Hodinová sazba** – hodinové sazby za hodiny zaúčtované na účty výnosů a nákladů.
