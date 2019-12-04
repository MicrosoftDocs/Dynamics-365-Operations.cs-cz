---
title: Co je nového nebo změněného v aplikaci Dynamics 365 for Operations verze 1611 (listopad 2016)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 for Operations verze 1611.
author: sericks007
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: 221294
ms.assetid: 357931ed-f843-4bf5-bc85-0da3de0619ec
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 03e7fcc2041363f9ddee8fdda9c4ea30bf89a9cb
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812467"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-operations-version-1611-november-2016"></a>Co je nového nebo změněného v aplikaci Dynamics 365 for Operations verze 1611 (listopad 2016)

[!include [banner](../includes/banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 for Operations verze 1611.

## <a name="cost-accounting"></a>Nákladové účetnictví

<table>
<thead>
<tr>
<th>Co můžete dělat</th>
<th>Proč je to důležité</th>
</tr>
</thead>
<tbody>
<tr>
<td>Definovat dimenze prvku nákladů a importovat členy dimenze prvku nákladů.</td>
<td>Prvky nákladů se používají v nákladovém účetnictví pro kategorizování nákladů a dokumentaci toku nákladů. Primární prvky nákladů jsou importovány prostřednictvím datového konektoru Microsoft Dynamics 365 for Operations, který umožňuje vstoupit k hlavním účtům přímo z Operations, nebo pomocí konektoru obecné údaje, díky němuž získáte přístup k hlavním účtům prostřednictvím aplikace Microsoft Excel z jiného typu zdrojového systému. Po importu hlavních účtů do nákladového účetnictví jsou používány jako členy dimenze prvku nákladů. Prvky sekundárních nákladů jsou definovány uživatelem a využívají se při přidělování, aby dokumentovaly toky nákladů.</td>
</tr>
<tr>
<td>Mapa dimenzí prvků nákladů.</td>
<td>Pokud nelze sdílet hlavní účty mezi právními subjekty kvůli zákonným požadavkům na účetnictví, můžete je mapovat po jejich importu do nákladového účetnictví za účelem komplexního zobrazení v organizaci.</td>
</tr>
<tr>
<td>Definovat dimenze objektu nákladů a importovat členy dimenze objektu nákladů.</td>
<td>Objekty nákladů jsou všechny objekty, k nimž jsou přiřazeny náklady. Typické objekty nákladů zahrnují produkty, projekty, prostředky, oddělení, nákladová střediska a geografické oblasti. Můžete použít datový konektor Microsoft Dynamics 365 for Operations a získávat finanční dimenze a hodnoty z Operations nebo použít konektor pro obecná data, kde lze získat dimenze a hodnoty prostřednictvím aplikace Excel z jiných typů zdrojového systému. Používáte-li například jako objekt dimenze finanční dimenzi nákladového střediska, jsou všechna importovaná nákladová střediska členy dimenze objektů nákladů.</td>
</tr>
<tr>
<td>Definování nebo import statistických dimenzí.</td>
<td>Členy statistických dimenzí se měří neměnovými jednotkami, jako je například počet strojohodin, počet zaměstnanců a plocha. Používají se ve výkazech a jako základ pro přidělení a rozdělení.</td>
</tr>
<tr>
<td>Tvorba šablon poskytovatelů statistického měření.</td>
<td>Šablona poskytovatele statistických měření slouží k převedení dat z Dynamics 365 for Operations s do statistických měření. Šablona je poté přidružená k danému členu statistické dimenze. Šablony jsou předfiltrovány tak, aby zobrazovaly pouze tabulky, které jsou přidruženy finančním dimenzím.</td>
</tr>
<tr>
<td>Tvorba hlavní knihy nákladového účetnictví</td>
<td>Hlavní kniha nákladového účetnictví je komplexní hlavní kniha používající své vlastní kalendáře a měny. Hraje důležitou úlohu při zpracování všech nákladových transakcí. Hlavní kniha nákladového účetnictví například klasifikuje náklady založené na vlastních nákladových prvcích a spojuje náklady založené na svých vlastních dimenzích objektu. Můžete vytvořit libovolný počet hlavních knih nákladového účetnictví, kolik potřebujete, abyste mohli podávat správní sestavy z různých pohledů.</td>
</tr>
<tr>
<td>Tvorba jednotek řízení nákladů.</td>
<td>Jednotky řízení nákladů tvoří strukturu nákladů a definují tok nákladů do hlavní knihy nákladového účetnictví. Musí být přidruženy k dimenzím objektů nákladů, aby mohly představovat dimenzi objektu nákladů v hlavní knize.</td>
</tr>
<tr>
<td>Zpracování položek hlavní knihy.</td>
<td>Pro změření skutečného výkonu, musíte mít data. Ta se importují pomocí konektorů, které definujete pro hlavní knihu nákladového účetnictví. Při zpracovávání položek hlavní knihy se data importují postupně.</td>
</tr>
<tr>
<td>Zpracovat položky rozpočtu</td>
<td>Pro změření rozpočtovaného výkonu musíte mít data. Ta se importují pomocí konektorů, které definujete pro hlavní knihu nákladového účetnictví. Při zpracovávání položek rozpočtu se data importují postupně.</td>
</tr>
<tr>
<td>Vytvořit a použít zásady chování nákladů.</td>
<td>Zásady chování nákladů slouží ke klasifikaci pevných, proměnných nebo částečně proměnných nákladů. Zásady jsou založené na pravidlech a datu platnosti. Standardně jsou všechny náklady označené jako Neklasifikované, dokud nepoužijte zásady chování nákladů a nespočítáte účinky tohoto pravidla. Po výpočtu dojde ke klasifikaci nákladů.</td>
</tr>
<tr>
<td>Sledování nákladů.</td>
<td>Abyste lépe pochopili dopad zásad nákladů, nákladové účetnictví vám umožňuje sledovat náklady ke zdrojovým hodnotám a původu používaných pravidel. Tato funkce umožňuje úplné sledování toho, kdy náklady proběhly, jaké typy nákladů proběhly a jaká pravidla nákladů byla použita.</td>
</tr>
<tr>
<td>Definování hierarchií dimenzí.</td>
<td>Můžete vytvořit hierarchii dimenzí pro účely kategorizace nebo klasifikace. Můžete například definovat kategorizaci hierarchie, která bude založená na dimenzi prvku nákladů a jejích členů. Můžete také definovat klasifikaci hierarchie, která bude založená na dimenzi objektu nákladů a jejích členů. Vykazovací struktury se používají v následujících situacích:
<ul>
<li>Můžete definovat přidělení, nákladové sazby a pravidla shrnutí nákladů.</li>
<li>Výkazy zobrazujete pomocí pracovního prostoru.</li>
<li>Přístup definujete tak, abyste mohli zobrazovat souhrnné údaje.</li>
<li>Data zobrazujete v aplikaci Excel.</li>
</ul></td>
</tr>
<tr>
<td>Vytváříte výkazy, které lze zobrazit v pracovním prostoru.</td>
<td>Pracovní prostor můžete používat pro rychlý přehled skutečných a rozpočtovaných nákladů i odchylek. Můžete filtrovat data podle období nebo nákladové úrovně. Pracovní prostor je určen pro vedoucí pracovníky, kteří zodpovídají za řízení nákladů. Řídí se pravidly přístupu, která jsou definována pro hierarchie dimenzí.</td>
</tr>
<tr>
<td>Vytvořte sestavy pomocí aplikace Excel.
<blockquote>[!NOTE] Je nutné spustit Microsoft Excel 2016.</blockquote>
</td>
<td>Data nákladového účetnictví můžete exportovat přímo do aplikace Excel prostřednictvím entit dat a používat Microsoft PivotTable pro vytváření sestav.</td>
</tr>
</tbody>
</table>

## <a name="expense-management"></a>Správa výdajů

| Co můžete dělat | Proč je to důležité |
|-----------------|-----------------------|
| Opětovně přiřadit transakce platební karty propuštěných zaměstnanců. | Je-li zaměstnance propuštěn, je v určitých případech jeho účet Active Directory Domain Services (AD DS) blokován při importu transakcí aktivní platební karty, které musí být zaneseny do výdajů. Předtím jste nemohli přiřadit zástupce pro vyúčtování výdajů nebo připojit transakce kreditních karet k vyúčtování výdajů. Nyní můžete použít stránku **transakce kreditních karet** k opětovnému přiřazení zaměstnance k libovolné transakci platební karty, pokud byl související zaměstnanec propuštěn. Poté, co přiřadíte transakce platební karty, můžete vybrat transakci pro sestavu výdajů a zaplatit běžným procesem pro hrazení sestavy výdajů. |
| Změňte informace o výdajích na platební kartě u budoucích a bývalých zaměstnanců. | Můžete změnit informace o správě výdajů kreditní karty budoucích a bývalých zaměstnanců. Předtím jste mohli změnit informace o správě výdajů kreditní karty pouze v případě, že je zaměstnanec aktivní. |
| Kopírovat sestavu výdajů. | Nyní můžete zkopírovat existující výdaje při vytváření nových výdajů ve stejné sestavě výdajů. Můžete kopírovat sestavu výdajů a všechny související bezkreditní výdaje do nové sestavy výdajů. Musíte stále provádět všechny požadované rozpisy a připojovat požadované příjmy dle definovaných zásad pro výdaje a kategorie. Můžete přidat transakce platební karty do sestavy výdajů, a to výběrem možnosti přidat neodsouhlasené výdaje. |
| Hromadně upravit výdaje. | Některé transakce platební karty nemusejí být mapovány do kategorie výdajů, nebo mohly být nesprávně zmapovány při importu. V takovém případě zaměstnanci musejí ručně změnit přidružené kategorie výdajů. Při správě neodsouhlasených výdajů, můžete nyní hromadně upravovat kategorie výdajů pro vybrané náklady. Kromě toho při správě vybraných výdajů pro určité sestavy nákladů můžete hromadně upravovat projekt i dodatečné informace. |
| Změnit směnný kurz pro transakce z platební karty. | Aktuální směnný kurz použitý pro transakci platební karty se může lišit od směnného kurzu nastaveného v systému. Dříve zaměstnanci nemohli měnit směnný kurz pro žádné transakce platební karty, které byly importovány do správy výdajů. Nyní můžete nastavit parametry na stránce **parametry správy výdajů** a umožnit tak změnu směnného kurzu pro transakce kreditní karty. |
| Nastavení protikorupčního potvrzení pro výdaje. | Někteří zaměstnanci organizace mohou mít obchodní vztah se státními úředníky a některé výdaje prováděné jako součást obchodu mohou být považovány za podplácení. V modulu Správa výdajů lze nyní nastavit protikorupční potvrzení, které se zobrazuje pro zvolené kategorie výdajů, například jídlo a dary. Zaměstnanci musejí vybírat, zda výdaje, které jsou nastaveny pro protikorupční potvrzení splňují kritéria, která jsou definována podle zásad vaší organizace. |
| Zabránit manuálnímu zadávání výdajů pro specifické kategorie výdajů. | Kategorie výdajů lze nastavit tak, aby zastupovaly transakce platební karty, jejichž kategorii nelze změnit. Jde například o poplatek za zpožděnou platbu kreditní karty. Nyní můžete nastavit kategorii výdajů umožňující tvorbu výdajů pouze pomocí importu. Tato funkce zabraňuje tomu, aby zaměstnanci ručně tvořili výdaje pro kategorie. Nepovoluje ani kategorie, které chcete změnit u transakcí, které byly importovány, a které používají tuto kategorii. |
| Připojit příjem k vícenásobným výdajům. | Příjem, který byl odeslán do modulu Správa výdajů, můžete spojit s vícenásobnými náklady. Příjem, který byl přiřazen k vícenásobným výdajům, se v předchozích verzích musel nahrát pro jednotlivé položky výdajů zvlášť. Nyní můžete spojit příjem s výdaji, které již byla odeslány a připojeny k jinému výdaji ve stejné sestavě výdajů. Dále, pokud odešlete potvrzení do záhlaví sestavy výdajů, můžete vybrat jeden nebo více řádků, k nimž chcete připojit příjmy. |
| Vytvořte budoucí náklady. | Kopírujete-li sestavu výdajů, můžete například uvést budoucí datum transakce pro výdaje. Předchozí verze neumožňují budoucí výdaje. Nyní můžete vytvořit a uložit výdaje s budoucím datem. Budoucí výdaje však nelze odeslat. |
| Konfigurovat daně výdajů pro stát/oblast. | V některých zemích nebo oblastech mohou výdaje, které jsou vynakládány v různých zemích nebo regionech podléhat sazbě DPH. Konfiguraci daní výdajů lze nyní nastavit na úrovni státu/oblasti, nikoli pouze na úrovni země/regionu. Ponecháte-li pole **Stát/oblast** prázdné na stránce **konfigurace daně**, skupina DPH se bude vztahovat na všechny regiony uvedené země/oblasti. |
| Nastavení typů nákladů kreditních karet. | V předchozích verzích nebyla žádná stránka, kde byste mohli vytvořit nové typy platebních karet, např. Visa, MasterCard nebo AMEX, které byste mohli použít pro správu výdajů. Nyní můžete vytvořit typy platebních karet, které budete používat s modulem Správa výdajů. Stránka se nachází v oblasti **nastavení** v oddílu **výpočty a kódy**. |
| Určení víceúrovňového schvalovacího workflowu pro sestavy výdajů. | Nový workflow pro sestavy výdajů podporuje víceúrovňový schvalovací proces. Zaměstnanci zadají prozatímní schvalovatele a konečného schvalovatele při tvorbě sestavy výdajů. Workflow přesměruje sestavu výdajů nejdříve k dočasnému schvalovateli. Po schválení sestavy výdajů na této úrovni, workflow ji přesměruje ke konečnému schvalovateli, který vydá konečný souhlas. |
| Vytvoření a Správa výdajů, které nejsou přiřazeny k sestavě výdajů. | Uživatel nyní může vytvořit výdaje a spravovat je (například pomocí připojení konkrétních příjmů nebo přiřazování hostů), aniž by nejdříve musel vytvořit sestavy výdajů. Lze vybrat jeden nebo více výdajů a přidat je do nové sestavy výdajů, aby mohly být odeslány ke schválení. Nová stránka pro správu výdajů je k dispozici na **Správa výdajů** &gt; **Moje výdaje** &gt; **Výdaje**. |

## <a name="financial-management"></a>Správa financí

<table>
<thead>
<tr>
<th>Co můžete dělat</th>
<th>Proč je to důležité</th>
</tr>
</thead>
<tbody>
<tr>
<td>Sledovat hodnocení dlouhodobého majetku pomocí konceptu "kniha" .</td>
<td>V předchozích verzích byly použity dvou odlišných typy sledování hodnoty dlouhodobého majetku: oceňovací modely a knihy odpisů. V této verzi byly tyto dva pojmy sloučeny do jednoho konceptu hodnocení, který se nazývá knihy. Knihy obsahují všechny funkce oceňovacích modelů a knih odpisů. Například můžete vypnout zaúčtování do hlavní knihy. Knihy, které se účtují do hlavní knihy, se obvykle používají pro korporátní vykazování financí. Knihy, které se neúčtují do hlavní knihy, se mohou používat pro účely vykazování daně.</td>
</tr>
<tr>
<td>Proces roční uzávěrky hlavní knihy pro více právnických osob.</td>
<td>Pro urychlení procesů roční uzávěrky nyní můžete spustit roční uzávěrku pro více právnických osob ze sdílené stránky roční uzávěrky. Lze definovat skupiny právnických osob spolu s nastavením, které byste uchovávat od jednoho roku do dalšího. Byla rovněž provedena další rozšíření použitelnosti pro proces roční uzávěrky.</td>
</tr>
<tr>
<td>Můžete využít vylepšení a vyzkoušet přecenění cizí měny hlavní knihy.</td>
<td>V procesu přecenění cizí měny hlavní knihy byla provedena tato vylepšení:
<ul>
<li>Typ směnného kurzu byl přidán do hlavního účtu. Tento typ směnného kurzu nyní slouží k určení směnného kurzu při přecenění měny. Pokud není definován žádný typ směnného kurzu, bude při procesu nadále využíván typ směnného kurzu, který je definován v hlavní knize.</li>
<li>Nyní je jednodušší vybrat rozsah hlavních účtů a měny, pokud chcete spustit proces přecenění.</li>
<li>Přecenění lze spustit pro více právnických osob.</li>
<li>Systém nyní uchovává historii všech provedených procesů přecenění, stejně jako v případě procesu přecenění pohledávek (Pohledávky) a závazků (Závazky).</li>
<li>Při spuštění procesu můžete nyní zobrazit výsledky přecenění. Náhled zobrazuje výsledky pro všechny právnické osoby, u nichž byl proces proveden. Poté lze z náhledu zaúčtovat všechny právnické osoby, nebo jen jejich část. Výsledky z náhledu také můžete exportovat do aplikace Excel.</li>
</ul></td>
</tr>
<tr>
<td>Zobrazit transakce pro dodatečné účtovací vrstvy.</td>
<td>Na stránce seznamu <strong>Předvaha</strong> a v sestavě <strong>Výpis dimenze</strong> nyní můžete vybrat další účtovací vrstvy, které byly přidány do hlavní knihy. Vyberete-li dodatečné účtovací vrstvy, jsou úpravy těchto účtovacích vrstev zahrnuty do zůstatků na stránce se seznamem.</td>
</tr>
<tr>
<td>Připojte návody k šabloně pro období finanční uzávěrky.</td>
<td>Dříve jste mohli připojit dokumentaci až po dokončení úlohy. Například jste mohli připojit sestavu, která byla generována. Nyní můžete připojit dokument s postupy už do šablony. Tento dokument s postupy se pak zkopíruje do každého úkolu v plánu pro finanční období, tak aby si vlastník úkolu mohl zobrazovat informace o tom jak dokončit úkol.</td>
</tr>
<tr>
<td>Definujte nastavení mezipodnikového účetnictví ze sdílené stránky.</td>
<td><strong>Stránku nastavení mezipodnikového účetnictví</strong> lze nyní sdílet, takže společnost může definovat dvojice právnických osob, které mohou navzájem provádět transakce. Navíc lze nyní zadat transakci pro původní právnickou osobu, ale ne z cílové právnické osoby. Pokud jedna z právnických osob může iniciovat mezipodnikovou transakci, pár musí být definován oboustranně. Z toho vyplývá, že cílová právnická osoba je také nastavena jako původní právnická osoba.</td>
</tr>
<tr>
<td>Přijmout dokumenty odůvodnění pro plán rozpočtu.</td>
<td>Můžete vytvořit šablonu odůvodnění jako doplňkovou dokumentaci pro jakoukoliv požadovanou rozpočtovou částku. Uživatelé mohou zadávat podrobnosti šablony a připojovat šablonu k plánu rozpočtu, aby ji pak mohli použít v průběhu procesu schvalování.</td>
</tr>
<tr>
<td>Povolte rozšířená pravidla pro položky registru rozpočtu.</td>
<td>Pokud jsou rozšířená pravidla konfigurována v hlavní knize, lze je použít pro nové položky a pro převody v registru rozpočtu.</td>
</tr>
<tr>
<td>Využijte rozšířené zobrazení aktivit v zálohové fakturaci.</td>
<td>Nová stránka se seznamem <strong>Otevřené zálohy</strong> nabízí snímek stavu aktivity zálohové fakturace. Na stránce najdete oddíl závazků s informacemi o nákupních objednávkách, které mají zbývající zálohové hodnoty, které musí být fakturovány, dále pak fakturované hodnoty, které musí být zaplaceny, a hodnoty zaplacených faktur, které je třeba použít na standardní faktury. Dále jde o vylepšení automatického používání zaplacených zálohových faktur a standardních faktur, což účetním pomůže zadávat data efektivněji.</td>
</tr>
<tr>
<td>Použijte pracovní prostor <strong>Fakturaci dodavatelské spolupráce</strong>.</td>
<td>Nový pracovní prostor <strong>Fakturace</strong> v oddíle <strong>Dodavatelská spolupráce</strong> přináší externím dodavatelům zabezpečený přístup k informacím o vlastních fakturách. Dodavatel si například může zobrazit, zda byla faktura zaplacena, nebo odesílat vlastní faktury. Tato změna podporuje účinnější a rychlejší komunikaci s externími dodavateli. Účetní tudíž mají méně přerušení při práci.</td>
</tr>
<tr>
<td>Přepínání právnických osob při zadání faktury.</td>
<td>Vylepšení umožňují účetním, kteří musejí zadávat faktury pro více právnických osob rychle měnit právnické osoby přímo na stránkách fakturace. Tato funkce šetří účetním hodně času, protože už nemusejí odhlašovat aktuální právnické osoby a přihlašovat se k jiným právnickým osobám. Jak stránka <strong>Globální deník faktur</strong> tak <strong>Dodavatelské faktury</strong> uživatelům umožňuje měnit právnickou osobu při zadávání dat.</td>
</tr>
<tr>
<td>Podpora elektronických souborů pro program amerického daňového úřadu Internal Revenue Service (IRS) 1099 Combined Federal/State</td>
<td>Pokud je povolen <strong>americký</strong> konfigurační klíč, proces elektronického vykazování 1099 poskytne další funkce, které jsou v souladu s předpisy amerického finančního úřadu pro vykazovací program Combined Federal/State. Finanční úřad vytvořil tento program tak, aby mohl elektronicky předávat informace účastnickým státům.</td>
</tr>
<tr>
<td>Vylepšení vyrovnání</td>
<td>Vylepšení pomáhají účetním provádět vyrovnání efektivněji, protože jim umožňují zahrnout více nezaúčtovaných plateb do stejné faktury.</td>
</tr>
<tr>
<td>Zobrazení napříč společnostmi</td>
<td>Účetní pro centralizované platby si nyní mohou zobrazovat faktury napříč společnostmi. Pracovní prostory <strong>Platby dodavatele</strong> a <strong>Platby odběratele</strong> nyní poskytují lepší přehled a snadnější správu prošlých faktur, jelikož umožňují zobrazení a filtrování napříč společnostmi, které jsou součástí organizační hierarchie centralizovaných plateb.</td>
</tr>
<tr>
<td>Používání pracovního prostoru <strong>Správa banky</strong>.</td>
<td>Nový pracovní prostor <strong>Správa banky</strong> pomáhá sledovat bankovní účty a zůstatky vašich právnických osob. Aktuální a nezaúčtované zůstatky jsou ihned k dispozici pro všechny účty a můžete přecházet zpět ze zůstatků do podrobných detailů transakce. Zobrazí se také data historie zůstatků pro každý bankovní účet nebo pro všechny bankovní účty ve společnosti, a to jak v krátkodobém tak v dlouhodobém souhrnném zobrazení . Vzhledem k tomu, že data posledního odsouhlasení se generují pro každý bankovní účet, a že je k dispozici také označení pro odsouhlasení, která budou teprve probíhat, lze získat lepší přehled o odsouhlasení bankovního účtu.</td>
</tr>
<tr>
<td>Importovat elektronický výpis pro všechny právnické osoby v jediném kroku.</td>
<td>Nyní můžete importovat elektronický výpis pro všechny právnické osoby v jediném kroku. Soubory bankovních výpisů mohou obsahovat příkazy z více bankovních účtů a právnických osob, komprimované zip soubory zase mohou obsahovat více souborů bankovních výpisů. Odsouhlasení pro všechny bankovní účty pro všechny právnické osoby můžete spustit pomocí jednoho importu. Tato funkce vám pomůže ušetřit čas, protože nemusíte přepínat mezi společnostmi a několika importy výkazů. Lze rovněž automaticky spustit příslušná pravidla pro všechny importované výkazy v každé společnosti.</td>
</tr>
<tr>
<td>Sledování ocenění</td>
<td>Jediný dlouhodobý majetek může mít několik ocenění pro různé účetní normy a může dle libosti účtovat přidružené transakce do hlavní knihy. V předchozích verzích byla tato ocenění sledována pomocí oceňovacích modelů nebo knih odpisů. Nyní můžete sledovat ocenění, která se nyní nazývají knihy, pomocí sady deníků, dotazů a sestav. Sjednocená zkušenost zjednodušuje implementaci a snižuje počet rozhraní, která jsou vyžadována periodickými procesy.</td>
</tr>
<tr>
<td>Využijte vylepšení pro spuštění odpisů mezi více společnostmi.</td>
<td>Nyní můžete začít s odepisováním majetku v rámci všech právnických osob na jedné stránce. Deníky lze rovněž automaticky zaúčtovat až po jejich vytvoření. Vytvoření a zaúčtování deníků můžete odeslat do procesu dávkového zpracování tak, že odpisy spustíte na pozadí. Tato zlepšení sníží nedostatky v efektivitě, protože není nutné samostatné spuštění kalkulace jednotlivých odpisů pro každou společnost. Zlepšení také umožňuje lepší centrální správu vašich dlouhodobých majetků.</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>Správa lidského kapitálu

<table>
<thead>
<tr>
<th>Co můžete dělat</th>
<th>Proč je to důležité</th>
</tr>
</thead>
<tbody>
<tr>
<td>Vytvoření deníku výkonnosti.</td>
<td>Často před provedením svého přezkoumání hledáte informace o aktivitách nebo událostech, které přispěly k vašemu úspěchu coby zaměstnance v období přezkoumání. Do deníku výkonnosti můžete vkládat položky, které budou tyto aktivity a události dokumentovat. Tyto činnosti a události můžete také připojit k cíli nebo přehledu výkonů a poskytnout tak kontrolorovi více informací.</td>
</tr>
<tr>
<td>Vytvořte podrobnější cíle.</td>
<td>Budete mít větší kontrolu nad obsahem cílů, které si stanovíte. Můžete vytvořit měření pro cíle, propojovat položky v deníku výkonosti s měřeními a připojovat a zobrazovat dokumenty. Cíle můžete uložit jako šablony a znovu je použít pro rychlé nastavení.</td>
</tr>
<tr>
<td>Vytvořte podrobnější hodnocení výkonu.</td>
<td>Hodnocení výkonu, která se oficiálně nazývají diskuse, jsou nyní dostatečně flexibilní, aby podporovaly jak průběžnou zpětnou vazbu tak formálnější přezkoumání. Můžete směřovat k aktivním cílům, zveřejňovat komentáře o nich a přidávat oddíly pro revizi vašich kompetencí. K dispozici jsou další oddíly, kde lze přidávat nebo zobrazovat měření, deníky výkonu, přílohy a schválení, která souvisejí s příslušnou kontrolu.</td>
</tr>
<tr>
<td>Přidružte další hierarchie pozic k workflowům.</td>
<td>Workflow je možné přiřadit k hierarchii pozic. Můžete také upravit kroky workflowu pro optimalizaci procesu schválení, tak aby odpovídal požadavkům společnosti. Proto můžete definovat efektivní strukturu schvalování, která bude vyhovovat různým vztahům vykazování, který vaše organizace používá.</td>
</tr>
<tr>
<td>Podpora workflowu pro zadávání osobních identifikačních kódů PIN na samoobslužných stránkách zaměstnanců.</td>
<td>Schopnost workflowu pro lidské zdroje (HR) se rozšířila a nyní podporuje kódy PIN. Zaměstnanci mohou přidávat a upravovat své PIN a zvyšovat tak efektivitu. Zaměstnanci HR však mohou zkontrolovat přesnost a úplnost těchto informací, než je přidají k záznamu zaměstnance.</td>
</tr>
<tr>
<td>Vytvořte šablony pro stanovování cílů a použijte je pro přidání nového cíle.</td>
<td>Můžete vytvořit šablony cílů pro cíle, které může sdílet mnoho zaměstnancům v dané společnosti. Zaměstnanci mohou přidávat své vlastní cíle ze šablon, manažeři mohou přidat cíle pro své týmy ze šablony a členové HR týmů mohou přidávat cíle pro zaměstnance napříč společnostmi.</td>
</tr>
<tr>
<td>Vytvořte skupiny cílů a použijte je pro přidání nových cílů.</td>
<td>Můžete přidat šablony cílů do skupiny a s její pomocí vytvořit jeden nebo více cílů pro zaměstnance, tým, pozici, oddělení nebo společnosti.</td>
</tr>
<tr>
<td>Mějte větší kontrolu nad procesem kontroly.</td>
<td>Workflow slouží i k řízení procesu kontroly. Můžete vytvořit šablony revize a použít je k vytvoření hodnocení. Můžete také přidat hodnocení pro revize.</td>
</tr>
<tr>
<td>Období revizí můžete využít k definování časového období pro kontrolu.</td>
<td>Můžete definovat časové období pro provedení kontroly výkonu, přičemž počáteční a koncové datum revize jsou zadány automaticky. Výchozí data můžete podle potřeby měnit.</td>
</tr>
<tr>
<td>Přístup k pěti novým sadám obsahu Power BI pro lidské zdroje</td>
<td>Nové sady obsahu umožňují personálním organizacím a personálním manažerům analyzovat následující:
<p>Metriky zaměstnanců</p>
<ul>
<li>Demografické rozúčtováními podle stáří, pohlaví nebo rodinného stavu</li>
<li>orovnání míry ztrácení podle roků a zobrazení seznamu důvodů odchodu zaměstnanců z organizace</li>
<li>Zobrazení seznamu volných pozic, také porovnání kompenzací a výhod volných a obsazených pozic</li>
</ul>
<p>Kompenzace a zaměstnanecké výhody</p>
<ul>
<li>orovnání zaměstnanců placených hodinově a se stálým platem</li>
<li>Zobrazení počtu zaměstnanců s registrovanými dostupnými zaměstnaneckými výhodami</li>
<li>Zobrazení zaměstnanců podle typu zaměstnání</li>
</ul>
<p>Nábor</p>
<ul>
<li>Analýza žadatelů podle počtu žadatelů, toho, odkud přicházejí a o jaké pozice žádající</li>
</ul>
<p>Školení organizace</p>
<ul>
<li>Registrace kurzu podle umístění </li>
<li>Docházka v rámci kurzu podle stavu</li>
<li>Seznam zaměstnanců registrovaných do kurzů</li>
</ul>
<p>Kompetence a rozvoj zaměstnance</p>
<ul>
<li>Seznam dovedností zaměstnanců</li>
<li>Rozdělení typů dovedností podle členů týmu</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="localizations"></a>Lokalizace

<table>
<thead>
<tr>
<th>Co můžete dělat</th>
<th>Proč je to důležité</th>
</tr>
</thead>
<tbody>
<tr>
<td>Lokalizace jsou k dispozici pro 18 dalších zemí:
<ul>
<li>Rakousko</li>
<li>Belgie</li>
<li>Brazílie</li>
<li>Čína</li>
<li>Česká republika</li>
<li>Estonsko</li>
<li>Finsko</li>
<li>Maďarsko</li>
<li>Itálie</li>
<li>Lotyšsko</li>
<li>Litva</li>
<li>Norsko</li>
<li>Polsko</li>
<li>Saúdská Arábie</li>
<li>Španělsko</li>
<li>Švédsko</li>
<li>Švýcarsko</li>
<li>Thajsko</li>
</ul>
<p>Následující země také vyžadují lokalizaci maloobchodu. Lokalizace maloobchodu pro tyto země nebyla dokončena a je plánována pouze pro H1 CY2017:</p>
<ul>
<li>Brazílie</li>
<li>Česká republika</li>
<li>Estonsko</li>
<li>Maďarsko</li>
<li>Lotyšsko</li>
<li>Litva</li>
<li>Malajsie</li>
<li>Polsko</li>
<li>Švédsko</li>
</ul>
</td>
<td>Dynamics 365 for Operations je k dispozici v 18 další zemích. V rámci našeho úsilí zjednodušit lokalizaci a učinit ji více konfigurovatelnou, konvertovali jsme regulační funkce elektronického vykazování na konfigurace elektronického vykazování (ER) a určité zákonem předepsané výkazy Microsoft SQL Server Reporting Services (SSRS) byly převedeny na ER konfigurace, které využívají šablony aplikace Excel. Tyto převedené funkce konkrétně zmiňované později v této tabulce.</td>
</tr>
<tr>
<td>Japonsko – Spojení dlouhodobého majetku při tisku formuláře 26 a dalších připojených tabulek.</td>
<td>Formulář 26 musí být odeslán do každého města, které společnost působí. Pro usnadnění práce při tisku formuláře 26, mohou být dlouhodobé majetky automaticky seskupeny a seřazena podle umístění.</td>
</tr>
<tr>
<td>Japonsko – Zobrazit částky pro zrychlené a dodatečné odpisy v profilu.</td>
<td>Profil může nabídnout přesný odhad částky pro zrychlený a dodatečný odpis.</td>
</tr>
<tr>
<td>Japonsko – postupně vypočítat srážkovou daň.</td>
<td>Japonská vláda vyžaduje vypočítat srážkovou daň postupně, a to na základě výše platby.</td>
</tr>
<tr>
<td>Japonsko – Import souboru poštovního směrovacího čísla pro určité velké budovy společnosti.</td>
<td>Soubor poštovního směrovacího čísla, který příslušní úředníci vydávají pro určité velké budovy společnosti, lze importovat do systému. Adresu lze poté odvodit z poštovních směrovacích čísel.</td>
</tr>
<tr>
<td>Japonsko – konfigurace období nečinnosti pro dlouhodobý majetek.</td>
<td>V období nečinnosti mohou uživatelé pozastavit odpisy dlouhodobého majetku ve stanoveném období. Tato funkce je vyžadována nařízením.</td>
</tr>
<tr>
<td>Evropa – Konfiguruje registrační číslo daně z přidané hodnoty (DPH) pro adresu stranu pomocí systému ID registrace.</td>
<td>Můžete konfigurovat DIČ pro adresu smluvní strany pomocí systému ID registrace a nové kategorie registrace <strong>DIČ</strong>.</td>
</tr>
<tr>
<td>Finsko – konfigurovat celní číslo odběratele pro adresu smluvní strany pomocí systému ID registrace.</td>
<td>Můžete konfigurovat celní číslo odběratele pro adresu smluvní strany pomocí systému ID registrace a nové kategorie registrace <strong>celního čísla odběratele</strong>.</td>
</tr>
<tr>
<td>Francie – tisknout více faktur odběratele v rozvržení, které je specifické pro Francii.</td>
<td>Výtisk faktury odběratele se upraví podle požadavků specifických pro Francii.</td>
</tr>
<tr>
<td>France – Podpora chronologického číslování dokladů podle fiskálního období.</td>
<td>Ve snaze splnit požadavky na číslování faktur odběratele, které jsou specifické pro Francii, můžete nastavovat číselné řady pro faktury odběratelů za jednotlivá fiskální období.</td>
</tr>
<tr>
<td>Rakouská lokalizace – konfigurace elektronických plateb</td>
<td>
<ul>
<li>Souhrnné hlášení (EU) ve formátu XML pro Rakousko</li>
<li>Formát Intrastat pro Rakousko</li>
<li>Specificky rakouský formát platby peněžního převodu ISO20022.</li>
<li>Specificky rakouský formát inkasní platby ISO20022.</li>
<li>Rakouský formát EDIFACT-PAYMUL</li>
<li>Přiznání k DPH pro Rakousko</li>
</ul>
</td>
</tr>
<tr>
<td>Belgická lokalizace – konfigurace elektronických plateb</td>
<td>
<ul>
<li>Formát BLWI pro Belgii</li>
<li>Souhrnné hlášení (EU) ve formátu XML pro Belgii</li>
<li>Sestava dlouhodobého majetku pro Belgii</li>
<li>Formát Intervat pro Belgii</li>
<li>Formát Intrastat pro Belgii</li>
<li>Sestava fakturovaného obratu pro Belgii</li>
<li>Formát pro export transakcí v hlavní knize pro Belgii</li>
<li>SWIFT formát platby dodavatelům pro Belgii</li>
<li>Formát importu CODA pro bankovní výpisy v Belgii</li>
<li>Specificky belgický formát platby peněžního převodu ISO20022.</li>
<li>Specificky belgický formát inkasní platby ISO20022.</li>
</ul>
</td>
</tr>
<tr>
<td>Brazilská lokalizace – konfigurace elektronických plateb</td>
<td>
<ul>
<li>GIA SP pro Brazílii</li>
<li>GIA-SP pro Brazílii</li>
</ul>
</td>
</tr>
<tr>
<td>Česká republika lokalizace – konfigurace elektronických plateb</td>
<td>
<ul>
<li>Souhrnné hlášení (EU) ve formátu XML pro Českou republiku</li>
<li>Formát Intrastat pro Českou republiku</li>
<li>Přiznání k DPH pro Českou republiku</li>
</ul>
</td>
</tr>
<tr>
<td>Čínská lokalizace – konfigurace elektronických plateb</td>
<td>
<ul>
<li>Formát sestavy sledování splatnosti klienta pro Čínu</li>
<li>formát sestavy analýzy splatných částek zákazníka pro Čínu</li>
<li>Formát sestavy sledování splatnosti dodavatele pro Čínu</li>
<li>formát sestavy analýzy splatných částek dodavatele pro Čínu</li>
<li>Analýza formátu sestavy plateb pohledávek pro Čínu</li>
<li>Formát sestavy sledování zůstatku klienta pro Čínu</li>
<li>Formát sestavy sledování zůstatku účtu v hlavní knize pro Čínu</li>
<li>Formát sestavy sledování zůstatku dodavatele pro Čínu</li>
<li>GBT soubor pro Čínu</li>
<li>Formátu exportu souboru golden daně</li>
<li>Formát sestavy odchylky výrobní spotřeby pro Čínu</li>
</ul>
</td>
</tr>
<tr>
<td>Estonská lokalizace – konfigurace elektronických plateb</td>
<td>
<ul>
<li>Souhrnné hlášení (EU) ve formátu XML pro Estonsko</li>
<li>Formát Intrastat pro Estonsko</li>
<li>Výkaz reklasifikace inventáře pro Estonsko</li>
<li>Specificky estonský formát platby peněžního převodu ISO20022.</li>
<li>Sestava oznámení o zůstatku odběratele dodavatele pro Estonsko</li>
<li>Přiznání k DPH pro Estonsko</li>
</ul>
</td>
</tr>
<tr>
<td>Finská lokalizace – konfigurace elektronických plateb</td>
<td>
<ul>
<li>Formát souhrnného hlášení (EU) pro Finsko</li>
<li>Formát Intrastat pro Finsko</li>
<li>Finský formát platby peněžního převodu ISO20022.</li>
</ul>
</td>
</tr>
<tr>
<td>Maďarská lokalizace – konfigurace elektronických plateb</td>
<td>
<ul>
<li>Souhrnné hlášení (EU) ve formátu XML pro Maďarsko</li>
<li>Formát Intrastat pro Maďarsko</li>
<li>Zjednodušený formát Intrastat pro Maďarsko</li>
<li>Exportní formát pro seznam faktur pro Maďarsko</li>
<li>DAŇOVÉ přiznání pro Maďarsko</li>
<li>Položkové DPH přiznání pro Maďarsko</li>
<li>Výkaz zásob pro Maďarsko</li>
<li>Formát multiCash platby pro Maďarsko</li>
</ul>
</td>
</tr>
<tr>
<td>Italská lokalizace – konfigurace elektronických plateb</td>
<td>
<ul>
<li>Formát Intrastat pro Itálii</li>
<li>Formát faktury projektu pro Itálii</li>
<li>Formát faktury prodeje pro Itálii</li>
<li>Italský formát platby peněžního převodu ISO20022.</li>
<li>Specificky italský formát inkasní platby ISO20022.</li>
<li>Formát vymáhání úhrady RIBA pro Itálii</li>
<li>Sestava transakcí domácí daně pro Itálii</li>
<li>Sestavy černé listiny pro Itálii</li>
<li>Sestava Modello770 pro Itálii</li>
<li>Roční daňový komunikační výkaz pro Itálii</li>
</ul>
</td>
</tr>
<tr>
<td>Lotyšská lokalizace – konfigurace elektronických plateb</td>
<td>
<ul>
<li>Sestava využití příjmů v hotovosti (LV)</li>
<li>Formát souhrnného hlášení prodejů (EU) pro Lotyšsko</li>
<li>Formát souhrnného hlášení korekcí (EU) pro Lotyšsko</li>
<li>Formát Intrastat pro Lotyšsko</li>
<li>Formát Intrastat (B) pro Lotyšsko</li>
<li>Seznam zásob inventáře pro Lotyšsko</li>
<li>Výkaz zásob inventáře pro Lotyšsko</li>
<li>Přesun zásob pro Lotyšsko</li>
<li>Poznámka k internímu převodu pro Lotyšsko</li>
<li>Dokument reklasifikace zásob pro Lotyšsko</li>
<li>Specificky lotyšský formát platby peněžního převodu ISO20022.</li>
<li>Přiznání k DPH pro Lotyšsko</li>
</ul>
</td>
</tr>
<tr>
<td>Litevská lokalizace – konfigurace elektronických plateb</td>
<td>
<ul>
<li>Souhrnné hlášení (EU) ve formátu XML pro Litvu</li>
<li>Formát Intrastat pro Litvu</li>
<li>Výkaz zásob pro Litvu</li>
<li>Litevský formát platby peněžního převodu ISO20022.</li>
<li>Sestava odsouhlasení mezi odběrateli dodavatele pro Litvu</li>
<li>Přiznání k DPH pro Litvu</li>
</ul>
</td>
</tr>
<tr>
<td>Norská lokalizace – konfigurace elektronických plateb</td>
<td>
<ul>
<li>Formát upomínky pro Norsko</li>
<li>Formát plateb AutoGiro pro Norsko</li>
<li>Formát platby odběratele AvtaleGiro pro Norsko</li>
<li>Formát platby odběratele eFaktura pro Norsko</li>
<li>Specificky norský formát platby peněžního převodu ISO20022.</li>
<li>Formát plateb NETS pro Norsko</li>
</ul>
</td>
</tr>
<tr>
<td>Polská lokalizace – konfigurace elektronických plateb</td>
<td>
<ul>
<li>Formát Intrastat pro Polsko</li>
<li>Skladové dokumenty pro Polsko</li>
<li>Dokument reklasifikace zásob pro Polsko</li>
<li>Formát multiCash platby pro Polsko</li>
<li>Formát multiCash zahraničních plateb pro Polsko</li>
<li>Sestava potvrzení o zůstatku odběratele dodavatele pro Polsko</li>
</ul>
</td>
</tr>
<tr>
<td>Saudskoarabská lokalizace – konfigurace elektronických plateb</td>
<td>Formát přidělení bankovního akreditivu vedlejších nákladů pro Saúdskou Arábii</td>
</tr>
<tr>
<td>Španělská lokalizace – konfigurace elektronických plateb</td>
<td>
<ul>
<li>Formát souhrnného hlášení (EU) pro Španělsko</li>
<li>Formát Intrastat pro Španělsko</li>
<li>Formát faktury projektu pro Španělsko</li>
<li>Formát faktury prodeje pro Španělsko</li>
<li>Španělský formát platby peněžního převodu ISO20022.</li>
<li>Specificky španělský formát inkasní platby ISO20022.</li>
<li>Formát evidenční kniha DPH pro Španělsko</li>
<li>Formát souhrnu Evidenční knihy DPH pro Španělsko</li>
<li>Export prohlášení 347 do ASCII pro Španělsko</li>
<li>Sestava prohlášení 347 pro Španělsko</li>
</ul>
</td>
</tr>
<tr>
<td>Švédská lokalizace – konfigurace elektronických plateb</td>
<td>
<ul>
<li>Formát Intrastat pro Švédsko</li>
<li>Formát platby odběratele Bankgirot Autogiro pro Švédsko</li>
<li>Formát platby dodavatele Bankgirot pro Švédsko</li>
<li>SWIFT formát platby dodavatelům pro Švédsko</li>
<li>Formát SIE export pro Švédsko</li>
<li>Specificky švédský formát platby peněžního převodu ISO20022.</li>
</ul>
</td>
</tr>
<tr>
<td>Švýcarská lokalizace – konfigurace elektronických plateb</td>
<td>
<ul>
<li>Formát platby DebitDirect pro Švýcarsko</li>
<li>Formát přímé inkasní platby LSV pro Švýcarsko</li>
<li>Švýcarský formát platby peněžního převodu ISO20022.</li>
<li>Specificky švýcarský formát inkasní platby ISO20022.</li>
<li>Importní formát bankovního výpisu ESR pro Švýcarsko.</li>
</ul>
</td>
</tr>
<tr>
<td>Německo – Export plateb dodavatelů ve formátu DTAZV</td>
<td>Německo vyžaduje DTAZV se specifikací cizí formátu představující zprávu o převodu kreditu (platbu dodavatele) podle specifikace pro platby zahraničí platby z Německa na účet v zahraniční bance nebo do domácí banku v cizí měně.</td>
</tr>
</tbody>
</table>

### <a name="electronic-reporting"></a>Elektronická sestava

| Co můžete dělat | Proč je to důležité |
|-----------------|-----------------------|
| Konfigurujte sestavy ER pro vložení údajů v různých formátech, z prostoru správy dokumentů do generovaných elektronických zpráv. | Sestavy ER mohou vkládat údaje v různých formátech, které se generují z prostoru správy dokumentů. Proto lze přílohy obchodního dokumentu přidat k elektronickým zprávám, které jsou generovány pro daný dokument podle právních předpisů. V současné době tyto přílohy můžete přidávat ve formátu MIME ke generované zprávě ve formátu XML. Přílohy lze případně přikládat ve formátu Base64 do generované binární zprávy. |
| Konfigurujte sestavy ER a generujte elektronické dokumenty do formátu aplikace Excel, Microsoft Word nebo PDF. | Jediná konfigurace umožňuje ER sestavám generovat elektronické dokumenty ve třech různých formátech: OpenXML list (aplikace Excel), Word a formuláře dat formátu XML (XFDF) (PDF). Uživatelé mohou vybrat formát přidáním šablony formátu k sestavě ER ve formě dokumentu aplikace Excel, aplikace Word a PDF. |
| Konfigurujte sestavy ER pro vložení dat do záhlaví a zápatí elektronických dokumentů, které jsou generovány ve formátu listu OpenXML. Můžete tak také určovat zalomení stránky. | Sestavy ER mohou zadávat obchodní data do záhlaví a zápatí a také určit, kde bude zalomení stránky. Sestavy proto mohou podporovat statické horní a dolní části stránek generovaných elektronických dokumentů. Mohou také podporovat specifické stránkování těchto dokumentů tak, aby splňovaly právní předpisy. |
| Konfigurujte cíle sestavy ER tak, aby se výstup posílal jako e-mail a aby obchodní data i ER logika (výrazy) sloužily k průběžnému určení použité e-mailové adresy. | Když jste v předchozích verzích konfigurovali cíle ER, mohla být e-mailová adresa příjemce definována už v době návrhu. Nyní můžete nakonfigurovat výrazy ve formátu ER. Tento výraz lze vybrat v cíli jako zdroj e-mailové adresy pro každou konfiguraci formátu a každý výstupní komponent (složku nebo soubor) samostatně. Proto pokud je spuštěn výkaz ER, každý generovaný soubor může být odeslán různým příjemcům a e-mailovou adresu lze definovat podle logiky ER a obchodních dat. |
| Konfigurujte cíl sestavy ER tak, aby se výstup odesílal do složky aplikace Microsoft SharePoint jako buď nový pojmenovaný soubor nebo jako nová verze existujícího souboru, a aby se obchodní data dala použít v rámci Microsoft Power BI jako sada dat nebo jako sestava. | Při konfiguraci sestav ER můžete nyní snadno (bez kódování) připravit požadovaná obchodní data, tak aby je šlo snadno použít v rozhraní Power BI. Při spuštění těchto sestav ER můžete pro rozhraní Power BI zajistit odpovídající obchodní data a/nebo Excelové sestavy, které jsou již k dispozici. Při plánování v režimu opakované spuštění sestavy, můžete vytvořit plánované vypuštění obchodních dat z Dynamics 365 for Operations do Power BI a podpořit tak plán aktualizace sestav na základě Power BI. |
| Konfigurujte sestavy ER pomocí části elektronického dokumentu, který již byl generován jako zdroj dat pro generování zbytku onoho dokumentu. | Můžete konfigurovat ER sestavy, které tvoří výstup v textovém formátu, a připravit řádek inventáře. Tyto údaje pak lze použít v jiných oddílech dokumentu a vytvořit řádky, které zahrnují podrobnosti souhrnu. Souhrnné informace (součty a čísla) můžete vypočítat a vytisknout do generovaných elektronických dokumentů, aniž by bylo nutné dodatečné transformování dat. Tato funkce tedy zlepšuje výkon při spuštění sestavy a usnadňuje budoucí údržbu konfigurovaného formátu ER. |
| Konfigurujte sestavy ER a určujte příponu názvu souboru pro elektronické dokumenty, které jsou generovány v textovém formátu. | Můžete konfigurovat sestavy ER a vytvořit výstup v textovém formátu, aby šel uložit jako soubor se specifickou příponou. Kromě výchozí .txt přípony můžete konfigurovat rozšíření např. csv a .prn v souladu se specifikací formátu. |
| Tvořte nové sestavy ER, které jsou založeny na konkrétní verzi modelu ER. | Když jste dříve tvořili nový formát ER, mohli jste jako umístění dat zdroje formátu použít pouze nejnovější verzi vybraného modelu ER. Nyní můžete vybrat jakoukoli dostupnou verzi vybraného modelu ER. Tato funkce vám umožní spravovat ER sestavy pro aktuální rok a současně navrhovat novou verzi modelu ER pro příští rok. |
| Vyhledávejte zdroje dat a formáty/modely podle textu nebo vybraných aspektů jediným kliknutím. Aktivně řešte konflikty přeskládání a řešte konflikty mezi konfiguracemi. Konfigurujte sestavy ER a tvořte tak více zprávy ověřování chyb, které se objevují, dokud nedojde k zastavení průběhu sestavy. | Několik zlepšení uživatelských zkušeností (UX)v rámci rozhraní ER uživatelům pomáhá pracovat s ER efektivněji a rychleji. |
| Zobrazit pracovní prostor **ER** v sestavách Power BI. | Uživatelé mohou konfigurovat stránku **pracovního prostoru ER** tak, aby zahrnovala nové položky nabídky a aktivní dlaždice založené na sestavách Power BI. |

## <a name="payroll"></a>Mzdy

<table>
<thead>
<tr>
<th>Co můžete dělat</th>
<th>Proč je to důležité</th>
</tr>
</thead>
<tbody>
<tr>
<td>Konfigurace mzdových záznamů a zpracování mezd pomocí funkce, která odpovídá funkci modulu <strong>Payroll</strong> v aplikaci Microsoft Dynamics AX 2012 R3.</td>
<td>Nyní můžete konfigurovat a zpracovávat mzdy v USA s použitím sady funkcí, která odpovídá sadě funkcí v aplikaci AX 2012 R3.
<ul>
<li>Můžete konfigurovat cykly plateb a platební období, pracovní cykly a pracovní doby, kódy příjmů a skupiny příjmových kódů, plány, typy odchodů a plány zaměstnaneckých výhod.</li>
<li>Můžete nastavit povinné odpočty pro benefity a daně a zaznamenávat mzdové informace pro pozice a zaměstnance pro účely vytváření sestav a analýz.</li>
<li>Můžete také nastavit a spravovat srážky pro obstavení a daň dávek a všechny přidružené administrativní poplatky.</li>
</ul>
</td>
</tr>
<tr>
<td>Sledování a zpracování procesu mzdového období s použitím nového pracovního prostoru <strong>správy mezd </strong>.</td>
<td>Nyní můžete snadno sledovat vaše zpracování mezd. Správci mezd mohou ihned vidět příjmy a platební příkazy, které vyžadují jejich pozornost tak, aby tok plateb byl úplný a přesný. Pracovní prostor <strong>správy mezd </strong>umožňuje uživatelům sledovat a spouštět procesy od začátku do konce, a to z jednoho pracovního prostoru.</td>
</tr>
<tr>
<td>Generujte kladné platební výměry pro kontrolu mezd.</td>
<td>Existuje nová přípona k pozitivní funkci řízení hotovostních a bankovních pohybů pro platby mezd. Přidali jsme samostatné položky v rámci základního procesu, které umožňují izolovanou konfiguraci, která je pro mzdy typická. Funkce je stejná jako základní funkce kladných plateb, která se objevila v aplikaci Microsoft Dynamics AX verze 7.0.1 (květen 2016). Z důvodu tohoto rozšíření jsou mzdová data plně oddělena od ostatních kladných platebních transakcí. Tato izolace pomáhá zajistit, aby pouze příjemci mezd mohli vstoupit a zobrazit si data, která souvisí se mzdou.</td>
</tr>
<tr>
<td>Importujte řádky výkazu zisků z externího zdroje s použitím nových dat entity řádku výkazu příjmů .</td>
<td>Nová důležitá datová entita umožňuje integraci s externími systémy výpočtu času a příjmů. Entita dat importuje řádky výkazu zisků a řídí se stejnou výchozí logikou, kterou uživatel zadal přímo ve výkazu příjmů. Po importu jsou řádky automaticky přiřazeny k odpovídajícímu dokumentu výkazu příjmů. Pokud neexistuje vhodný dokument s výkazy příjmů, je vytvořen automaticky.</td>
</tr>
</tbody>
</table>

## <a name="planning-and-scheduling"></a>Plánování a rozvrhy

| Co můžete dělat | Proč je to důležité |
|-----------------|-----------------------|
| Nastavte výchozí nastavení objednávek pro nákup i prodej podle všech aktivních dimenzi základního produktu. Můžete tedy definovat výchozích nastavení objednávek pro skladové jednotky zásob (SKU) nebo částečné SKU. | Můžete specifikovat výchozí nastavení objednávek, které se vztahují k dimenzi produktu nebo kombinaci dimenzí produktu.<p>**Příklad**</p><p>Prodáváte produkt s názvem Polo tričko. Tento produkt je k dispozici ve dvou barvách: zelená a modrá. Je také dostupná ve dvou velikostech: malá a střední. Barva a velikost jsou aktivní dimenze produktu Polo tričko. Je možné blokovat nákupy všechn zelených Polo triček, bez ohledu na jejich velikost.</p> |

## <a name="product-master-data"></a>Data základního produktu

<table>
<thead>
<tr>
<th>Co můžete dělat</th>
<th>Proč je to důležité</th>
</tr>
</thead>
<tbody>
<tr>
<td>Nastavte všechna výchozí nastavení objednávek a nastavení specifická pro pracoviště současně, a to z jedné stránky.</td>
<td>Tato funkce nabízí lepší přehled o nastavení položky.</td>
</tr>
<tr>
<td>Vytvořte názvosloví pro varianty produktu.</td>
<td>Do čísla varianty produktu můžete zahrnout celou řadu prvků, například dimenze produktu, atributy a znaky. Když tvoříte prodejní objednávku nebo nákupní objednávku, můžete rychle vyhledat varianty produktu.</td>
</tr>
<tr>
<td>Vyhledávání produktů a variant produktů pro prodejní a nákupní scénáře.</td>
<td>Při vytváření řádku prodeje nebo řádku nákupu, můžete vyhledávat produkty pomocí dimenze produktu a libovolného čísla produktu kromě čísla položek globálního obchodu (GTIN) a čárových kódů. Vyhledávání je fulltextové a nahrazuje stávající hledání na bázi "Začíná...", které je použito v seznamu prodejního a nákupního vyhledávání. Tato funkce umožňuje vyhledat skupiny produktů, které mají podobné vlastnosti, nebo jeden produkt, který má jedinečné vlastnosti. Chcete-li tuto funkci spustit, vyberte parametr <strong>povolit vyhledávání při hledání produktu</strong> na stránce <strong>parametry vyhledávání</strong>.</td>
</tr>
<tr>
<td>Když vytvoříte prodejní nebo nákupní transakci, specifikujte varianty produktu. Případně můžete vybrat v seznamu platných kombinací dimenzí.</td>
<td>Tato funkce slouží ke zvýšení produktivity.
<p><strong>Příklad</strong></p>
<p>Prodáváte produkt s názvem Polo tričko. Tento produkt je k dispozici ve dvou barvách: zelená a modrá. Je také dostupná ve dvou velikostech: malá a střední. Barva a velikost jsou aktivní dimenze produktu Polo tričko. Po zadání řádku prodeje Polo tričko v zelené barvě a malé velikosti, nemusíte zadávat data do polí <strong>č. položky</strong>, <strong>barva</strong>, a <strong>velikost</strong>. Řádek lze vytvořit jedním z následujících kroků:</p>
<ul>
<li>V <strong>č. položky</strong> zadejte číslo varianty produktu, barvu, velikost nebo velikost. Ve vyhledávacím poli hledejte konkrétní variantu, kterou chcete prodat, a vytvořte řádek prodeje.</li>
<li>Do pole <strong>Číslo položky</strong> zadejte hledané číslo položky. Přejděte na libovolné pole dimenze produktu. Ve vyhledávání <strong>dimenze produktu</strong> uvidíte všechny nalezené kombinace dimenzí, které se týkají položky Polo tričko. V jednom kroku tak můžete vybrat varianty produktu, který chcete prodat.</li>
</ul>
</td>
</tr>
<tr>
<td>Určete, zda se čísla produktů zobrazí na stránkách transakcí.</td>
<td>Stránky transakcí, například prodejní a nákupní objednávky, se zobrazí pouze v polích <strong>číslo položky</strong> a <strong>název produktu</strong>. Pro zobrazení <strong>čísla produktu</strong> vyberte parametr <strong>zobrazit na formulářích čísla produktů</strong> pod <strong>parametry modulu řízení informací o produktu</strong>.</td>
</tr>
</tbody>
</table>

## <a name="project-management-and-accounting"></a>Řízení a účetnictví projektů

| Co můžete dělat | Proč je to důležité |
|-----------------|-----------------------|
| Používejte pozdější výběr při zaúčtování návrhů faktury v dávce. | Účetní projektu může nastavit dávkovou úlohu na automatické vyzvedávání návrhů faktur pro zaúčtování, pokud tyto návrhy splňují kritéria, která jsou zadány v dávkové úloze. Tato funkce zlepšuje automatizace zaúčtování faktur, protože dávkovou úlohu lze spustit opakovaně. Navíc automaticky přebírá návrhy pro zaúčtování. |
| Vytvoření analýzy na ploše Power BI. | Obsah obchodní logiky (BI) pro s projektem související a prostředků se týkající data lze snadno vytvořit na ploše Power BI. |
| Používejte zálohy nákupních objednávek a správně je zahrnujte do procesu odhadu projektu. | Pro nákupní objednávky na projekt se musejí zpracovat zálohy předtím, než může být uvolněna některá platba dodavatelům. Tyto zálohové faktury se nyní zobrazí v procesu odhadu/uznání projektu pro projekty typu **S pevnou cenu**. |
| Přistupujte a spravujte odhady nákladů a výnosů i požadavky na položky přímo ze strukturovaného rozpisu prací. | Můžete spravovat odhad nákladů, odhady výnosů a požadavky na položku pro specifickou úlohu WBS v dialogovém okně pro tento úkol v plánovacím náhledu WBS. |
| Vyberte zdroj financování pro deníky poplatků. | Jestliže smlouva na projekt obsahuje více zdrojů financování, můžete vybrat jeden konkrétní zdroj financování, pokud jsou zaúčtovány poplatky. Pokud nevyberete konkrétní zdroj financování, pravidla financování zpřesněná ve smlouvě se používají pro přidělení poplatku. |
| Otevřete výkazy projektu v aplikaci Excel. | Nové datové entity pro aktualizace hlavní knihy a aktualizace rozpočtu vám umožňují otevřít data v Excelu a vytvářet analýzu pomocí funkce aplikace Excel. |
| Použijte pouze jeden konfigurační klíč, pokud chcete povolit funkci správy a účetnictví projektu (PMA). | Konfigurační klíče související s projektem byly nahrazeny jedním konfiguračním klíčem projektu, který spouští funkci PMA. |

## <a name="retail-and-commerce"></a>Maloobchodní a velkoobchodní prodej

### <a name="advanced-warehouse-management-in-a-retail-store"></a>Rozšíření správy skladu v obchodu

Maloobchodní prodejci mohou využít rozšíření řešení správy skladu (WHS) ve svých obchodech a provádět požadované úpravy funkcí prodejních míst (POS), které je budou podporovat. Procesy ručních řešení by měly fungovat v obchodě i v jakémkoliv jiném skladu. Všechny aktuální Maloobchodní skladové zásoby a procesy POS, které tvoří nebo aktualizují skladové transakce, jsou aktualizovány tak, aby mohly používat zvláštní požadavky pro sklady s podporou WHS.

| Co můžete dělat | Proč je to důležité |
|-----------------|-----------------------|
| Využijte POS pro vyhledávání dostupných zásob v obchodech s podporou WHS. | Při vyhledávání zásob by měl být pracovní proces stejný, jaký byl i předtím. Vyhledávání by mělo ukázat dostupné množství na úrovni skladu a neměl by brát do úvahy dimenze umístění, stavu zásob nebo licenční značky. |
| Využít POS pro zpracování příjmu produktu pro převodní příkaz v obchodě s podporou WHS. | Můžete přijímat převodní příkazy na POS pro obchody a položky s podporou WHS. Uživatel by měly být schopný vybrat umístění pro příjem a měl být schopný zadat ID licenčních značek pro automatické vyplnění řádků příjmu. |
| Využijte POS pro zpracování příjmu produktu pro nákupní příkaz v obchodě s podporou WHS. | Můžete přijímat nákupní příkazy na POS pro obchody a položky s podporou WHS. Uživatel by měly být schopný vybrat umístění pro příjem a měl být schopný zadat ID licenčních značek pro automatické vyplnění řádků příjmu. |
| POS slouží ke zpracování dodávky produktů z obchodu s podporou WHS. | Můžete registrovat přesuny z POS pro obchody a položky s podporou WHS. Uživatel by měl být schopný vybrat místa, z nichž se bude odesílat. Stav zásob bude automaticky generován a licenční značek by měly být ignorovány. |

### <a name="enable-seamless-omni-channel-commerce"></a>Povolte perfektní obchodní omni-channel

Perfektní obchodní omni-channel odkazuje ke správě a zpracovávání objednávek v kamenných obchodech, on-line obchodech, call centrech a mobilních obchodních platformách. V této verzi produktu byly provedeny následující investice v této oblasti:

- Vylepšení při zveřejňování úvodních poutačů e-shopů
- Nová mobilní aplikace orientující se na klienta umožňuje vyhledání produktu, správu účtů a nákupy online

| Co můžete dělat | Proč je to důležité |
|-----------------|-----------------------|
| Klient: Aktuální verze aplikace orientující se na klienta umožňuje následující funkce: Vyhledávání produktu, procházení kategorií, přidávání do nákupního košíku a nákup bez registrace. Maloobchodní prodejci mohou k aplikaci připojit vlastní značku a nabídnout ji v obchodech Android a iOS. | Maloobchodní prodejci mohou snadno vytvořit aplikaci orientující se na klienta, která svým zákazníkům umožňuje prohlížet a objednávat produkty a z mobilního přístroje bez registrace. |
| Seznamy požadovaných položek klientů on-line poutače e-shopů | Nezávislí výrobci softwaru (ISV) mohou využívat seznam požadovaných položek, aby klienti mohli vytvářet a spravovat více seznamů v on-line poutačích a zobrazovat/používat tyto seznamy na POS. |
| Vytvořit asynchronní objednávky odběratelů pomocí on-line poutače e-shopu | ISV nyní může vytvořit účty odběratelů, i když Commerce Data Exchange: Real-time Service není k dispozici. |
| Publikujte kanál produktů ze serveru pro maloobchod na poutače třetí strany. | Server maloobchodu nyní podporuje ověřování mezi službami. ISV využívá publikační kanály prezentace produktů z maloobchodního server na poutače třetí strany. |

### <a name="extensibility"></a>Rozšiřitelnost

- Spuštěné obchodní projekty jsou nyní zapečetěny před doplňkem Retail SDK.
- Snadnější nasazení a údržba prostřednictvím komponentizovaných balíčků komponent Microsoft a ISV POS, server maloobchodu, databáze, platby a hardwarové stanice.

| Co můžete dělat | Proč je to důležité |
|-----------------|-----------------------|
| CRT/ Server maloobchodu: Maloobchodní sítě nebo ISV mohou rozšířit CRT prostřednictvím rozšiřovacích vzorků. Vložené změny kódů již nejsou nepodporovány. | Chcete-li povolit souvislou integraci a souvislé nasazení, měli byste se zcela vyhnout vloženým změnám kódů. Také pro usnadnění příjmu opravy hotfix bez jakýchkoli kódů sloučení a nasazení pro CRT komponenty. |

### <a name="personalized-product-recommendations"></a>Doporučení přizpůsobeného produktu

| Co můžete dělat | Proč je to důležité |
|-----------------|-----------------------|
| Zobrazte přizpůsobená doporučení produktu ve více stykových místech pokladního místa (POS), chcete-li zjistit, jaký zákazník může mít zájem na základě jejich historie nákupů, položek v seznamu jejich přání a položek, které ostatní zákazníci zakoupili online a v kamenných obchodech | Co se týká maloobchodních prodejců s velkým katalogy, přizpůsobená doporučení pomáhají zákazníkům objevit produkty a poskytují zaměstnancům obchodů inteligentní clienteling. Vystavením produktů zaměřených na zájmy a nákupní zvyklosti zákazníka mohou doporučení produktu pomáhat maloobchodníkům navýšit prodeje a zlepšit udržení si zákazníka. V aplikaci Retail využívají doporučení produktu kognitivní služby a strojové učení Microsoft Azure. |

### <a name="pos-task-recorder"></a>Záznamník úkolů POS

| Co můžete dělat | Proč je to důležité |
|-----------------|-----------------------|
| Maloobchodní prodejci mohou použít Záznamník úkolů POS k výrobě výukových materiálů, modelování diagramů podnikových procesů (BPM) a generování obsahu nápovědy, díky čemuž zvýší produktivitu a zlepší analýzy i vzhled aplikací. | Chcete-li povolit souvislou integraci a souvislé nasazení, měli byste se zcela vyhnout vloženým změnám. Také pro usnadnění příjmu opravy hotfix bez jakýchkoli kódů sloučení a nasazení pro CRT komponenty. |
| Pomoc v reálném čase na POS. | Pokladník/manažer může získat pomoc v reálném čase z POS ohledně obchodního procesu, a to bez přepínání kontextu. |

### <a name="store-system-providing-a-seamless-on-premises-store-experience"></a>Uložit systém: poskytnout bezproblémové zkušenosti místního obchodu

Systém obchodu je možnost nasazení pro maloobchodní prodejce, který umožňuje vést sadu operací v obchodě, a to jak v místním úložišti, veřejném cloudu společnosti Microsoft nebo na vlastním soukromém cloudu klienta. V této verzi produktu je rozsah pouze v obchodě. Pro zvýšení podpory prostředí, která mají pomalé a nespolehlivé připojení k síti, musíme poskytovat možnost pro maloobchodní prodejce nasadit maloobchodní Server v obchodě a databázi kanálů. Pak mohou i nadále spouštět základní obchodní scénáře i v případě, že neexistuje žádná připojení k centrále (HQ). Na základě různých datových bodů, které zahrnovaly diskuse týmu analytiků, výsledky zákaznických průzkumů a analýzu konkurence, doporučujeme jako ideální řešení pro své zákazníky následující rozsah řešení:

- Samoobslužný balíček je dostupný pro systém obchodu.
- Výchozí instalace je nasazení jednoho přístroje, ale je povoleno vlastní nasazení.
- Umožňuje snadné nasazení/samoobsluhu.
- Maloobchodní Server a databáze obchodů jsou v obchodě, spolu s službu Async Client.
- Maloobchodní Server v obchodě komunikuje přímo s aplikačním objektovým serverem (AOS) v centrále systému obchodu.
- Podpora scénářů mezi terminály v případě bez připojení k centrále.
- Retail Modern POS a Cloud POS vždy komunikují s Retail Server v obchodě.
- Podpora Retail Modern POS a cloudových POS, kde není připojení k centrále.
- Podpora off-line databáze specifické pro Retail Modern POS (izolovaný vůči jednotlivým instancím Retail Modern POS), kde není žádné připojení k centrále.
- Ověření je založeno výměně služeb pouze pro obchod systému.
- Volání Real-time Service nejsou podporovány bez připojení k Internetu.
- Přímé připojení k databázi Retail Modern POS k databázi kanálů není podporováno.
- Umožňuje telemetrii/sledování.

| Co můžete dělat | Proč je to důležité |
|-----------------|-----------------------|
| Maloobchodní prodejce stahuje samoobslužnou instalaci systému obchodu z databáze kanálů v Dynamics AX HQ a stahuje i konfigurační soubor. | Prodejce může snadno stáhnout samoobslužný balíček. |
| Prodejce nainstaluje systém obchodu pomocí samoobslužného instalačního programu. | Prodejce může nainstalovat systém obchodu pomocí samoobslužného instalačního balíčku. |
| Správce IT konfiguruje systému obchodu v Dynamics 365 for Operations (databáze kanálů, profil kanálu, obchod a nasazovací balíček). | Správce IT může nakonfigurovat systém obchodu snadno a efektivně. |
| Maloobchodní prodejce spravuje Retail Modern POS v místně obchodu a může provést operace v reálném čase, například výdeje dárkových poukazů, pokud je připojení k dispozici. | Prodejce může provádět kroky v reálném čase ze systému obchodu, pokud má k dispozici připojení k síti. |
| Prodejce může synchronizace data ze systému v místě obchodu do centrály, pokud existuje připojení. | Prodejce může synchronizovat do a ze systému obchodu, pokud má k dispozici připojení k síti. |
| Prodejce může mít zabezpečenou komunikaci mezi systémem v místě obchodu a centrálou. | Prodejce může bezpečně komunikovat ze systému obchodu, pokud má k dispozici připojení k síti. |
| Správce IT a Microsoft Operations může sledovat a podávat hlášení do systému v místě obchodu (diagnostika a vykazování změn). | Správce IT a Microsoft Operations může bezpečně sledovat systém úložiště a hledat efektivní řešení problémů. |

### <a name="universal-windows-platform-app-for-retail-modern-pos"></a>Aplikace Univerzální platforma Windows pro Retail Modern POS

V současné době je Retail Modern POS k dispozici pouze jako aplikace systému Windows 8.1 pro stolní počítače a tablety, a jako POS v cloudu pro prohlížeče stolních počítačů nebo tabletů. V této verzi se Retail Moderns POS převádí do aplikace Universal Windows Platform (UWP). Tato změna umožní spuštění Retail Modern POS na jakémkoli zařízení s Windows 10 (stolní počítače, tablety a telefon) a také přepínat mezi různými zobrazeními na zařízeních povolujících Continuum.

| Co můžete dělat | Proč je to důležité |
|-----------------|-----------------------|
| Povoluje důležité funkce POS pro malá zařízení. | Funkce Retail POS je dostupná pro telefony a další malá zařízení se systémem Windows 10. |

## <a name="supply-chain-management"></a>Správa dodavatelsko-odběratelského řetězce

### <a name="consignment-inventory"></a>Zásoby dodávky

| Co můžete dělat | Proč je to důležité |
|-----------------|-----------------------|
| Jako dodavatel můžete ukládat suroviny ve skladu odběratele. Jako odběratel můžete odložit aktuální nákupy, dokud nebudou potřeba suroviny, které jsou nutné pro výrobu. | Udržování surovin skladu může zahrnovat značné náklady. Pomocí zásob dodávek, mohou dodavatelé skladovat suroviny na skladě odběratele. Odběratel pak může odložit aktuální nákupy, dokud nebudou potřeba suroviny, které jsou nutné pro výrobu. Suroviny se objednávají a získávají pomocí zakázek na doplnění stavu zásob dodávky. Tato zakázka na doplnění zaznamenává fyzické transakce, ale nemá žádný vliv na hlavní knihy. Pro rozlišení mezi skladovými položkami odběratele a dodavatele, můžete používat dimenzi Vlastníka zásob. Změna vlastnictví zásob se zpracovává v deníku procesů, který zaznamenává převod vlastnictví surovin ze zásob dodavatele do zásob odběratele. Tento proces spouští vytvoření nákupní objednávky a příjem produktu.<blockquote>[!NOTE] Tato funkce se omezuje na dodávku příchozích surovin pro výrobu. Není integrována s řízením skladu (WHS) ani správou přepravy (TMS).</blockquote> |
| Jako dodavatel můžete získat informace o množství zasílaných zásob, které se převádějí k odběrateli. | Pro možnost účtovat odběrateli dodavatel vyžaduje údaje o surovinách zakoupených ze zásilky dodávky a datum zakoupení. Dodavatel může také monitorovat zásoby na skladě u zákazníka pomocí rozhraní dodavatelské spolupráce. |
| Přesunujte zásoby vlastněné dodavatelem pomocí deníku převodu. | Chcete-li sledovat fyzickou pozici zásob vlastněných dodavatelem, musíte být schopní zaznamenat umístění v systému. Pomocí deníku převodu můžete zaznamenat fyzické přesunutí zásob, jako je například pohyb z jednoho místa ve skladu do jiného místa v dotyčném skladu. |
| Upravte zásoby vlastněné dodavatelem pomocí deníku inventur. | Je důležité, abyste zásoby na skladě systému synchronizovali se skutečnými fyzickými zásobami. Zásoby vlastněné dodavatelem lze upravit pomocí procesů inventury, například úpravou množství a procesů deníku inventury. |
| Další informace o podpoře pro dodávku v Dynamics 365 for Operations | Chcete-li zobrazit další informace týkající se podpory pro procesy dodávek, otevřete [Zásilka](../../../supply-chain/inventory/consignment.md), [Nastavení zásilky](../../../supply-chain/inventory/set-up-consignment.md), [Vytvoření nové zakázky na doplnění stavu zásob dodávky (Průvodce záznamem úloh)](../../../supply-chain/inventory/tasks/create-consignment-replenishment-order.md) a [Změna vlastnictví zásilky zásob na základě výrobní poptávky (Průvodce záznamem úloh)](../../../supply-chain/inventory/tasks/change-ownership-consignment.md). |

### <a name="vendor-collaboration-previously-known-as-the-vendor-portal"></a>Dodavatelská spolupráce (dříve označovaná jako portál pro dodavatele)

| Co můžete dělat | Proč je to důležité |
|-----------------|-----------------------|
| Povolte dodavatelům odpovídat na každý řádek nákupní objednávky a navrhovat změny. | V některých případech chce dodavatel přijímat některé řádky nákupní objednávky a jiné odmítat. Dodavatelé nyní mohou jednotlivě spravovat řádky nákupní objednávky. Každý řádek může být odmítnut, potvrzen nebo přijat se změnami. Dodavatele například může změnit datum dodání, rozdělit doručení a množství, nebo navrhnout alternativní položku. |
| Povolte dodavatelům spravovat informace o kontaktní osobě. | Dodavatelé mohou spravovat informace o kontaktní osobě pro svou společnost. Tyto informace zahrnují jména, e-mailové adresy a telefonní čísla. Přístup k této funkci je udělován prostřednictvím vyhrazené zabezpečené úlohy. |
| Sdílejte dokumenty, které souvisejí s nákupními objednávkami dodavatelů. | Jestliže musíte sdílet s dodavateli dokument, například dokumenty o požadavcích, je vhodné spojit dokument s příslušnou nákupní objednávkou. Dodavatel může sdílet poznámky a přílohy s odběratelem pomocí propojení dokumentu ke své reakci na nákupní objednávku. Správa dokumentů je podkladovou podpůrnou soustavou a pouze poznámky a přílohy, které jsou klasifikovány jako "externí", lze sdílet s dodavatelem. |
| Založit nového dodavatelského uživatele. | Pokud vaši dodavatelé používají rozhraní dodavatelské spolupráce, mají bezproblémový způsob, jak požadovat nové účty, pokud nové kontakty vyžadují přístup k dodavatelské spolupráci. Odborníci v oblasti zásobování mohou odeslat požadavek na účet pro kontaktní osoby u dodavatelské společnosti. Kontaktní osoba dodavatele, která je již uživatelem dodavatelské spolupráce, může tento typ požadavku také odeslat. Tento požadavek nakonec vytvoří nového uživatele v Dynamics 365 for Operations, který bude mít bezpečnostní role specifické pro dodavatele. Usnadňuje také požadavek na portál Microsoft Azure B2B k poskytnutí nového účtu Azure Active Directory (Azure AD) uživateli. Dodavatel také může požádat o deaktivaci nebo změnu zabezpečení úlohy účtu specifického dodavatelského uživatele. |
| Další informace o dodavatelské spolupráci v Dynamics 365 for Operations. | Další informace o dodavatelské spolupráci najdete na [Dodavatelská spolupráce s externími dodavateli](../../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md), [Dodavatelská spolupráce s odběrateli](../../../supply-chain/procurement/vendor-collaboration-work-customers-dynamics-365-operations.md), [Správa uživatelů dodavatelské spolupráce](../../../supply-chain/procurement/manage-vendor-collaboration-users.md), [Nastavení konfigurace a správa dodavatelské spolupráce](../../../supply-chain/procurement/set-up-maintain-vendor-collaboration.md) a [Pracovní prostor pro fakturaci dodavatelské spolupráce](../../../finance/accounts-payable/vendor-portal-invoicing-workspace.md). |

### <a name="intercompany-order-processing"></a>Mezipodnikové zpracovávání objednávek

<table>
<thead>
<tr>
<th>Co můžete dělat</th>
<th>Proč je to důležité</th>
</tr>
</thead>
<tbody>
<tr>
<td>Definujte přímo na řádcích prodejní objednávky, odkud a jak mají poptávky čerpat své zdroje.
<p><strong>Příklad</strong></p>
<p>Vytvořte řádek prodejní objednávky a určete přímou dodávku jakožto typ dodání. Primární dodavatel je přidán do řádku prodejní objednávky jako zdrojový bod.</p>
</td>
<td>Tok pro příjem objednávek byl výrazně vylepšen. Definujte nyní přímo na řádcích prodejní objednávky, odkud a jak mají poptávky čerpat své zdroje. Už nemusíte čekat, až budou všechny řádky přidány do prodejní objednávky. Nové možnosti na řádcích prodejní objednávky umožňují určit typ dodávky, pokud specifikujete dodavatele. Když spojíte dodavatele s řádky prodejní objednávky, vytvoří se řetězce objednávky pro dodání od dodavatele.
<ul>
<li>Dodavatelem může být mezipodnikový dodavatel, který využívá interní nákupní objednávky a prodejní objednávky, nebo to může být externí dodavatel používající externí nákupní objednávky.</li>
<li>Typem dodávky mohou být <strong>Přímá dodávka</strong> nebo <strong>Zásoby</strong>. Typ dodávky <strong>Zásoby</strong> označuje, že dodavatel má dodat zboží do místních zásob, než bude odesláno odběrateli.</li>
</ul>
</td>
</tr>
<tr>
<td>Vytvořte příslib objednávky přímo z řádků prodejní objednávky.
<p><strong>Příklad</strong></p>
<p>Vytvořte řádek prodejní objednávky, která čerpá zdroje u vnitropodnikového dodavatele. Opusťte řádek. Data doručení se vypočítávají podle dostupnosti ve zdrojové společnosti.</p>
</td>
<td>Při vytváření nových řádků prodejní objednávky využívajících nové zdrojové informace, data dodání se počítají podle prvku <strong>Data dodání</strong>. Například: pokud je vybrán mezipodnikový dodavatel, počítá se dostupnost ve zdrojové společnosti. Tímto způsobem jsou automaticky vytvořeny řetězce objednávky spolu s řádky prodejní objednávky. Tato funkce pomáhá zajistit, že data dodání budou zobrazena ve zdrojové společnosti, takže profily dostupné pro slíbení (ATP) budou moci zpracovat předpokládané požadavky přímo, jakmile budou vytvořeny prodejní objednávky.</td>
</tr>
<tr>
<td>Zkontrolujte dostupnost produktu ve všech zdrojových místech a vyberte nejlepší možnost zdrojů.</td>
<td>Stránka <strong>Alternativní dodání</strong> byla upravena a nyní poskytuje cenné informace o všech schválených interních i externích dodavatelích. Tyto informace zahrnují možnosti zdrojů pro zásoby poskytnuté dodavatelem. Pokud vyberete způsob dodání, systém vypočítá proveditelné datum dodání. Můžete snadno vybrat nejlepší možnost pro odběratele a aplikovat ji na každý řádek prodejní objednávky</td>
</tr>
</tbody>
</table>

### <a name="warehouse-enhancements-for-high-volume-distribution-centers"></a>Vylepšení skladu u velkoobjemových distribučních center

| Co můžete dělat | Proč je to důležité |
|-----------------|-----------------------|
| Vytvořte práci poté, co bylo zboží zabaleno v balírně zboží. | Tato funkce je užitečná, pokud existují dodatečné procesy po ručním balení (například paletizace, kontrola kvality, konsolidace dodávky nebo změny při nakládání na překladištích). Nový typ práce **Výdej zabaleného kontejneru** umožňuje upravovat tyto úlohy s použitím samostatné pracovní řádky. Nyní můžete modelovat balírny a generovat práci po balení. Tato práce slouží k organizování pohybů zabaleného zboží. |
| Skupiny kontejnerů balírně. | Tato funkce umožňuje seskupovat více balení do jednoho kontejneru nebo licenční značky v balírně. Například: Operátor e-shopu/velkoobchodu může seskupit 100 jednotlivých balíčků do jednoho kontejneru (například na paletu nebo do klece). Tento kontejner je poté přesunout, rozfázovat nebo naložen pomocí jediného pracovního příkazu, který pracovník generuje naskenováním jediného čárového kódu (licenční značky) pro celý seskupený kontejner. Tato funkce minimalizuje pracovní úkony pro přemístění spousty menších zabalených balíčků. Další informace najdete ve [Vytvoření položky v menu mobilního zařízení pro konsolidaci registračních značek vozidel (Průvodce záznamem úloh)](../../../supply-chain/warehousing/tasks/create-mobile-device-license-plate-consolidation.md). |
| Vytvořte zásady uvolnění pro zabalené kontejnery. | Práci, kterou spouští uvolnění kontejnerů, lze vytvořit automaticky nebo ručně. Když je automatická, práce je generována při uzavření kontejneru za použití směrnic umístění a pracovní šablony. Pokud uvolnění probíhá ručně, balírna může rozhodnout, zda má být práce vygenerována pro jeden kontejner nebo pro skupinu kontejnerů. Tato funkce snižuje riziko, že uzavřené kontejnery budou vyzvednuty a přesunuty před tím, než budou připravené k přesunutí z balírny. Umožňuje také nesystémově řízené seskupené uvolňování. |
| Krátkodobé opakované přidělení | Přidali jsme podporu pro krátkodobé procesy vyskladnění, které pomáhají zaměstnanci, který nemůže vyskladnit zboží ale chce splnit objednávku, pokud je požadované zboží k dispozici v jiném skladovém místě. Můžete použít automatický proces opětovného přidělení, který používá směrnice pro umístění k získání zboží, pokud je k dispozici na jiném místě. Případně, pokud se opětovné přidělení provádí ručně, mobilní zařízení ukáže seznam umístění spolu s dostupným množstvím. Pracovník skladu může vybrat, ze kterého skladového místa zásoby vyzvednout. Tyto dvě metody můžete nastavit jednotlivě nebo v kombinaci jako jeden příkaz v nabídce Pracovník skladu. Při ručním opětovném přidělování může pracovník skladu převzít množství krátkodobě vyskladněné položky z různých míst. Další informace najdete na [Nastavení změny opakovaného přidělení položky (Průvodce záznamem úloh)](../../../supply-chain/warehousing/tasks/set-up-short-picking-item-reallocation.md). |
| Přesunutí zásob s přidruženou prací | nyní můžete přesouvat zásoby s přidruženou prací. Tato funkce může být užitečná, například pokud chce pracovník zrušit místo vstupního překladiště a přesunout registrované palety, které čekají na přesunutí do jiného vstupního místa. Překladiště je volné a může přijmout další zboží. Zásoby, které byly přesunuty, mají novou informací o přesunutí na jiné místo. Tato funkce dokáže také uvolnit místo na výdejních skladových místech, a to přesunutím zásob s přidruženou prací, které vytvářejí místo pro doplnění. Také ji můžete využít pro přesunutí nákladu z jednoho přechodného skladového místa do jiného, aniž by došlo ke ztrátě nakládací prací, která byla vygenerována. Tímto způsobem vám funkce může pomoci optimalizovat čas potřebný pro naložení kamionů, když přijedou. Můžete přesunout zásoby, které byla rezervovány pro prodejní objednávky, problémy s převodními příkazy, příjmy převodních příkazů a nákupní objednávky. Pohybu je zabráněno, pokud hrozí rozdělení řádků. Pokud například máte řádek s prací pro 100 kusů položky, nemůžete přesouvat pouze 30 kusů položky do jiného místa. |
| Sloučení licenčních značek s přidruženou prací. | Můžete sloučit licenční značky s přidruženou odchozí prací. Například pokud zásilka byla rozdělena do několika prací, může být užitečné povolit sloučení licenčních značek, až dorazí na přechodné skladové místo. Licenční značky lze sjednocovat pouze v případě, že jsou na stejném skladovém místě, jsou součástí stejného nákladu a nesou stejné informace o dodávce. |
| Zmrazení práce výdeje související s doplňováním na úrovni řádku. | Nyní můžete zmrazit práci na úrovni řádku (a ne na úrovni záhlaví), aby zaměstnanci mohli plnit řádky výdeje, které nejsou zmrazeny pomocí doplňování poptávky. Proto velkoobchodník s velkými prodejními objednávkami, nebo prodejce, který má velké prodejní objednávky nebo převodní příkazy na doplnění, může povolit práci výdeje, která začne na všech řádcích, na které se nevztahují doplňovací práce. Práce výdeje a doplnění pak lze plnit současně. Tuto funkci lze nastavit tak, abyste si mohli vybrat, zda práci zmrazíte na úrovni záhlaví nebo řádku. Můžete také používat obě metody a vytvořit šablonu práce pro každou metodu zvlášť. Konfigurace záhlaví/řádku je převedena na šablony práce, ale můžete ji měnit přímo během generování práce. |
| Stornovat práci pomocí mobilního zařízení. | Nyní můžete zrušit práci pomocí mobilního zařízení, a to s i bez poptávky na doplnění. V předchozích verzích bylo nutné použít plně funkčního klienta. Chcete-li tuto funkci povolit, vytvořte položku nabídky na mobilním zařízení, která bude nastavena na režim **Nepřímý** a nastavte kód aktivity na **Zrušit práci**. |

### <a name="warehouse-operation-enhancements"></a>Vylepšení operací skladu

| Co můžete dělat | Proč je to důležité |
|-----------------|-----------------------|
| Modelujte různé typy kontejnerů. | Můžete použít různé typy kontejnerů ve skladu a optimalizovat tak úložiště. Rozhodnout se ale pro to můžete i z jiných důvodů. Nová entita typ kontejneru má fyzické vlastnosti typů kontejneru. Nyní můžete přidružit k určitému typu kontejneru licenční značky a použít limity pro místo uskladnění. Tuto funkci můžete například využít k určování, kolik palet (nebo jiných typů kontejnerů) povolíte na určitém místě. Typy kontejneru také byly přidány do skupiny klasifikace jednotek, aby přidaly výchozí typ kontejneru pro proces příjmu. Typy kontejneru lze použít u směrnic pro skladová místa pro příchozí a odchozí zboží. Můžete je také používat při zobrazení zásob na skladě, jelikož pomáhají určit, kolik typů kontejnerů máte aktuálně uloženo na skladě. Další informace hledejte v článku [Použití registračních značek přidružených k typu kontejneru pro procesy řízení skladu](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/06/20/use-of-license-plates-associated-with-a-container-type-to-drive-warehouse-management-processes/). I když tento článek popisuje aktualizaci aplikace Microsoft Dynamics AX 2012, stejnou podporu jsme nyní přidali i do Dynamics 365 for Operations. |
| Storno dopravy. | Ve skladu musíte být schopni zpracovat poslední změny. Například u některého zboží může dojít k poškození, takže je nelze odeslat. Případně může odběratel vydat opožděný požadavek na zrušení nebo změnu objednávky. Dynamics 365 for Operations nyní umožňuje stornovat dodávky. Proto můžete zrušit dodací list a později ho doplnit o správná množství. Stejně tak můžete zrušit příjmy produktů v příchozím toku a vytvořit aktualizovanou verzi. |
| Použijte palety se smíšeným zbožím. | Nyní můžete přijímat a registrovat „smíšené" palety. Smíšená paleta se skládá z různých položek, které jsou poskládány na jednu paletu, a to na jednu nebo několik nákupních objednávek nebo řádků. Všechny registrace lze shrnout do jedné cílové licenční značky. Tento proces se povoluje prostřednictvím mobilního zařízení skladu. Například: Když do skladu dorazí paleta se smíšenými položkami, úředník na příjmu položky a jejich množství identifikuje, potom paleta putuje do vyhrazeného místa určení. Tato skladová místa jsou určena šablonami práce a směrnicemi skladového místa. Pokud jsou skladová místa rozdělena pro několik položek, které mají pevná skladová místa, tato funkce vytvoří tolik řádků práce, kolik různých položek se na smíšené paletě nachází. Tato funkce registruje a ukládá přijaté palety se smíšenými položkami rychleji a pružněji. Další informace naleznete v článku [příjem a zaznamenávání palet s různými zdroji řádků dokumentu pomocí jedné licenční značky](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/13/receive-and-register-a-pallet-with-mixed-source-document-lines-using-1-license-plate-purchase-order-matching/) a informace o smíšených paletách na [Oznámení o naší poslední kumulativní aktualizaci](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/06/30/whats-new-in-cu11-for-wms-and-tms/). I když tento článek popisuje aktualizaci aplikace AX 2012, stejnou podporu jsme nyní přidali i do Dynamics 365 for Operations. |

### <a name="minor-feature-enhancements-in-supply-chain-management"></a>Méně výrazné změny funkcí v řízení řetězce dodávek

<table>
<thead>
<tr>
<th>Co můžete dělat</th>
<th>Proč je to důležité</th>
</tr>
</thead>
<tbody>
<tr>
<td>K importu a exportu dat použijte nové datové entity.</td>
<td>Můžete importovat a exportovat data pomocí těchto datových entit:
<ul>
<li>Faktura za přepravu</li>
<li>Sdružené zásoby na skladě podle skladu a stavu zásob</li>
<li>Změny zásob</li>
<li>Nabídka</li>
</ul>
</td>
</tr>
<tr>
<td>Použijte vylepšený Ganttův diagram k vývoji interaktivních scénářů plánování.</td>
<td>Rozšířený Ganttův diagram vám umožňuje vyvíjet nové interaktivní scénáře plánování a dodat rozšířené rozhraní API, které umožňuje přizpůsobovat vzhled aktivit. Zde jsou uvedena některá nová API:
<ul>
<li>Svislé funkce uchopení a přetažení aktivit</li>
<li>Přidat/odstranit aktivity</li>
<li>Náhled rezervovaných období v souhrnném pruhu</li>
<li>Změna barvy a stylu ohraničení aktivity</li>
<li>Změna barvy, stylu a pozadí nebo textu v mřížce</li>
</ul>
</td>
</tr>
<tr>
<td>Zvládejte lépe plánování materiálu a zdrojů.</td>
<td>Provedli jsme několik vylepšení pro plánování materiálu a zdrojů:
<ul>
<li>Rezerva výdeje se nyní využívá, když je položka na skladě.</li>
<li>Přepsání data dodání při potvrzení plánovaných objednávek.</li>
<li>Určete prioritu plnění objednávek prostřednictvím rezervních zásob.</li>
<li>Zabraňte plánování chystaných objednávek v minulosti.</li>
</ul>
</td>
</tr>
<tr>
<td>Vykázání aktuální spotřeby pro výrobu a zobrazení stavu zásob.</td>
<td>Můžete si zobrazit skutečnou spotřebu pro výrobu. Přidali jsme navíc nové zaškrtávací pole <strong>Zobrazit stav zásob</strong> do <strong>Pohyb</strong> v menu <strong>Vytvoření práce</strong>, které vám umožňuje zobrazit stav zásob.</td>
</tr>
<tr>
<td>Vypočtěte volumetrickou hmotnost, pokud se sazby pro vašeho dopravce opírají o volumetrickou hmotnost.</td>
<td>Byl přidán nový modul sazeb TMS, který se opírá o volumetrickou hmotnost, takže můžete vypočítat volumetrickou hmotnost.</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Další zdroje

[Domovská stránka Co je nového a co se změnilo v aplikaci Finance and Operations](whats-new-changed.md)
