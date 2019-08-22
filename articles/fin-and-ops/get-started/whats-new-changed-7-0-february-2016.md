---
title: Co je nového nebo změněného v aplikaci Dynamics AX 7.0 (únor 2016)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics AX 7.0. Tato verze obsahuje funkce pro obě platformy a byla vydána v únoru 2016.
author: sericks007
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: 91243
ms.assetid: 515bc6e7-a85d-4995-95c6-6cab6c8aa0f9
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f11d27da288ba69511f4159aad2155abe3467ff
ms.sourcegitcommit: 299e20b59ebefa584ed46a13da3f1a7ff709e43c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863520"
---
# <a name="whats-new-or-changed-in-dynamics-ax-70-february-2016"></a>Co je nového nebo změněného v aplikaci Dynamics AX 7.0 (únor 2016)

[!include [banner](../includes/banner.md)]

Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics AX 7.0. Tato verze obsahuje funkce pro obě platformy a byla vydána v únoru 2016.

## <a name="cost-management"></a>Správa nákladů

<table>
<thead>
<tr>
<th>Co můžete udělat?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Proč je to důležité?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Získejte rychlý přehled o zůstatku na skladě, zůstatku na skladě pro nedokončenou výrobu (NV) a o přírůstku a úbytku na skladě za vybraný fiskální rok.</td>
<td>Nelze použít</td>
<td>Pracovní prostor <strong>Správa nákladů</strong> obsahuje oddíl, ve kterém je uveden výkaz zásob nebo výkaz zásob NV za vybrané fiskální období. Výkaz vychází z mezipaměti sady dat, která se standardně aktualizuje každých 24 hodin. Mezipaměť sady dat lze nakonfigurovat tak, aby ji uživatelé mohli ručně aktualizovat pro hlášení v reálném čase. Na kartě <strong>Stav aktualizace dat</strong> v pracovním prostoru <strong>Správa nákladů</strong> se zobrazuje čas poslední aktualizace mezipaměti.</td>
<td>Kontroloři nákladů se zajímají o to, zda se zůstatek na skladě nebo zůstatek na skladě NV v čase zvyšuje nebo snižuje. Klasifikací provozních událostí ve výkazu může kontrolor nákladů získat přehled o proudění zásob. Jsou-li zásoby nebo zásoby NV vyhodnoceny podle standardních nákladů, lze zobrazit také celkové zaregistrované odchylky.</td>
</tr>
<tr>
<td>Použití modulu<strong> Správa nákladů</strong>.</td>
<td>Nelze použít</td>
<td>Řízení nákladů má podobu domény. Konfigurace a analytika související s náklady byly rozděleny do modulů Řízení zásob, Řízení výroby a Závazky.</td>
<td>Vzhledem k tomu, že všechny úlohy vztahující se k řízení nákladů jsou centralizovány do jednoho modulu, bude se kontrolorům nákladů snáze spravovat systém.</td>
</tr>
<tr>
<td>Typy zaúčtování, které se vztahují k účtování zásob a výroby, byly aktualizovány.</td>
<td>Popisky ve formulářích <strong>InventPosting</strong>, <strong>Prostředek</strong>, <strong>ResourceGroup</strong> a <strong>ProductionGroup</strong> vždy neodpovídají skutečně použitým popiskům <strong>LedgerPostingType</strong>. Porozumět terminologii použité v popiscích není snadné.</td>
<td>Popisky byly upraveny tak, aby popisky ve formulářích <strong>InventPosting</strong>, <strong>Prostředek</strong>, <strong>ResourceGroup</strong> a <strong>ProductionGroup</strong> odpovídaly skutečně použitým popiskům <strong>LedgerPostingType</strong>. Všechny popisky byly také přejmenovány tak, aby odpovídaly provozním událostem. Vlastní logika zaúčtování se však nezměnila.</td>
<td>Konfigurace systému je snazší, protože nové popisky se vztahují k provozním událostem, které používají tento typ zaúčtování.</td>
</tr>
<tr>
<td>Import/export nákupní ceny, nákladů nebo prodejní ceny z aplikace Microsoft Excel do/z verze výpočtu nákladů.</td>
<td>Nelze správně importovat ceny nebo náklady do verze výpočtu nákladů, protože datový model vyžaduje identifikátor InventDim.</td>
<td>Díky zavedení datových entit lze implementovat funkci importu/exportu. Tato funkce slouží k importu/exportu cen nebo nákladů do verze výpočtu nákladů.
<ul>
<li>Importujte úplný seznam nákupních cen pro příští rok, který jste obdrželi od nákupního oddělení.</li>
<li>Předejte náklady a standardní prodejní ceny z centrály jedné nebo více prodejním společnostem najednou.</li>
</ul></td>
<td>Kontrolorům nákladů tím můžete při údržbě systému (zejména při správě předem definovaných nákladů pro příští fiskální rok) ušetřit velké množství času.</td>
</tr>
<tr>
<td>Získáte rychlý přehled o zůstatku na skladě průměrné jednotkové náklady objektu nákladů.</td>
<td>Uživatel musí otevřít skladový formulář a vybrat dimenze zásob, které odpovídají objektu nákladů. Z tohoto důvodu je nutné, aby uživatel věděl, které dimenze zásob byly označeny pro finanční zásoby určitého výrobku.</td>
<td>Byla zavedena nová stránka <strong>Objekt nákladů</strong>. Ve výchozím nastavení se na této stránce zobrazují všechny objekty nákladů, které se vztahují k produktu. Na stránce se zobrazuje aktuální množství zásob, hodnota a průměrné jednotkové náklady na objekt nákladů.</td>
<td>Systém tím byl zjednodušen a kontroloři nákladů mají snadnější práci.</td>
</tr>
<tr>
<td>Použití nové stránky <strong>Položky nákladů</strong> během řízení zásob.</td>
<td>Řízení zásob na zaregistrovaných skladových transakcích a souvisejících vyrovnáních může být někdy složité, protože stejné transakce mohou být fyzické nebo finanční.</td>
<td>Stránka <strong>Položky nákladů</strong> nabízí nový způsob, jak zobrazovat skladové transakce.
<ul>
<li>Transakce se zobrazují v chronologickém pořadí.</li>
<li>Zahrnuty jsou pouze transakce, které přispívají k nákladům.</li>
<li>Nezáleží na tom, zda jsou náklady fyzické nebo finanční.</li>
<li>Nezáleží na fyzickém ani finančním množství.</li>
<li>Náklady jsou přidávány přírůstkově.</li>
</ul></td>
<td>Kontrolorům nákladů to může při provádění kontroly zásob na transakční úrovni ušetřit značné množství času.</td>
</tr>
<tr>
<td>Použití nového dialogového okna <strong>Výrobní výkaz NV</strong>, které nabízí souhrnné zobrazení kumulovaných nákladů pro daný produkt.</td>
<td>Nelze použít</td>
<td>Výkaz nedokončené výroby obsahuje souhrnný zůstatek NV konkrétní výrobní zakázky, který je seskupen do příslušných klasifikací nákladů. Graf znázorňuje chronologické pořadí, v jakém provozní zaúčtování ovlivnila zůstatek NV.</td>
<td>Kontrolorům nákladů to může ušetřit značné množství času, protože musí znát, jaký je aktuální zůstatek NV u konkrétní výrobní zakázky a jaký materiál byl v zakázce spotřebován.</td>
</tr>
<tr>
<td>Použijte funkci Zobrazit porovnání nákladů, která byla zavedena u výrobních zakázek. Tato funkce usnadňuje porovnání nákladů souvisejících s výrobní zakázkou.</td>
<td>Uživatel může porovnávat pouze odhadované náklady a realizované náklady. Porovnání lze provádět na nejnižší úrovni.</td>
<td>Funkce porovnání nákladů dává kontrolorům nákladů možnost porovnat tyto údaje:
<ul>
<li>Aktivní náklady vůči odhadovaným nákladům = odchylka plánování</li>
<li>Odhadované náklady vůči realizovaným nákladům = výrobní odchylka</li>
<li>Odchylka plánování + výrobní odchylka = celková odchylka</li>
</ul>
Tato funkce pracuje nezávisle na metodě výpočtu nákladů, která je přiřazena vyráběné položce. Ve výchozím nastavení zobrazuje graf porovnání nákladů podle typu nákladové skupiny. Uživatel může uživatel na podrobnější úroveň grafu.</td>
<td>Kontrolorům nákladů a vedoucím výroby slouží k analýze původu a příčin výrobních odchylek.</td>
</tr>
</tbody>
</table>

## <a name="developer"></a>Vývojář

| Co můžete udělat? | Dynamics AX 2012 | Dynamics AX 7.0 | Proč je to důležité? |
|------------------|------------------|-----------------|------------------------|
| Vytvořte webové řešení v cloudu, které bude přístupné z mnoha zařízení. | Není k dispozici. | Aktuální verzi aplikace Dynamics AX je založena na novém webovém klientovi a klientském rozhraní. | Svým koncovým uživatelům můžete poskytovat řešení nové generace. |
| K vývoji svých řešení použijte aplikaci Microsoft Visual Studio. | Microsoft MorphX je hlavní vývojové prostředí, ale některé části vývoje probíhají v aplikaci Visual Studio. | Visual Studio je jediné vývojové prostředí. | Dodržuje známé koncepty Dynamics AX 2012 a bez problémů je adaptuje prostředí a modelům aplikace Visual Studio. Zajišťuje standardní interakci s jinými jazyky a projekty v prostředí .NET. |
| Kompilovat jazyk Common Intermediate Language (CIL) pro všechny funkce. | X++ je kompilován na p-kód. | Zcela nový kompilátor jazyka X ++ generuje jazyk CIL pro všechny funkce. Jazyk CIL je stejný převodní jazyk, který je použit i jinými jazyky vycházejícími z prostředí .NET. | Jazyk CIL je rychlejší, může efektivněji odkazovat na třídy ve spravované dynamické knihovně (DLL) a lze jej spustit na velkém množství nástrojů v prostředí .NET. |
| Vestavěné sestavy a vizualizace analytických nástrojů v klientovi aplikace Microsoft Dynamics AX. | Není k dispozici. | Vytváření mimořádně intuitivních a plynulých vizualizací. | Poskytuje podklady k rozhodnutím, které vychází z analytických nástrojů. |
| Integrujte s aplikací Microsoft Office. | Není k dispozici. | Mezi nové funkce patří aplikace Excel Data Connector, stránka **Návrhář sešitu**, rozhraní API exportu a správa dokumentů. | Můžete vytvořit řešení produktivity pro své koncové uživatele. |
| Automatizace sestavování, testování a nasazení. | Částečně k dispozici | Nasazení topologie pro vývojáře pomocí nástrojů Vývojář a Build VM. Automatická konfigurace nástroje Build VM, sestavování modulů z aplikace Visual Studio Online (VSO) a spouštění testů. Je podporována kompilace a odkazy jazyka C\# a X++. | Snížením nákladů a nutného úsilí při testování a ověřování se zvýší produktivita vývojářů. |
| Úprava překrývání vrstev a rozšíření. | Rozšíření nejsou k dispozici. | Aktuální verze aplikace Dynamics AX má nový model přizpůsobení. | Můžete upravit zdrojový kód a metadata prvků modelu, které jsou odeslány společnosti Microsoft nebo partnerské třetí straně společnosti Microsoft. |
| Sestavování nových ovladačů a prvků uživatelského rozhraní pomocí jazyka X++ a moderního webového rozhraní. | Vlastní ovládací prvky jsou založeny na externích architekturách, jako je například Microsoft ActiveX nebo Windows Presentation Foundation (WPF). | Vytvoření ovládacích prvků je v aktuální verzi snadnější. Architekturu X++ lze použít pro chování aplikace a obchodní logiku; klient založený na jazyku HTML/JavaScript umožňuje moderní vizualizace. | Ovládací prvky lze navrhnout tak, aby vypadaly a chovaly se stejně jako předpřipravené (OOB) ovládací prvky Dynamics AX. |
| Vyhodnocení a vyladění výkonu pomocí nových nástrojů. | PerfSDK, Data Expansion Toolkit, aplikace Trace Parser WEb a PerfTimer nejsou k dispozici. | PerfSDK, Data Expansion Toolkit, aplikace Trace Parser Web a PerfTimer jsou nové. | Sada Software Development Kit (SDK) slouží k testování a ověření všech kritických obchodních procesů z hlediska výkonu v jednouživatelském nebo (je-li k dispozici) také víceuživatelském režimu. Sada Data Expansion Toolkit umožňuje správné rozbalení všech testů výkonu, které musí mít hlavní data a data transakcí správně rozbalena. Analyzátor trasování umožňuje ověření výkonu při testu v jednouživatelském nebo víceuživatelském režimu. Díky nástroji PerfTimer uvidíte, zda dotaz nebo některý konkrétní způsob volání způsobuje potíže s výkonem. Z tohoto důvodu nemusíte trasovat a analyzovat všechno dopodrobna. |
| Zveřejnění aktualizovatelných pohledů pomocí služby OData. | Není k dispozici. | Novinkou v aktuální verzi aplikace Dynamics AX je veřejný koncový bod služby OData umožňující přístup k datům aplikace Dynamics AX jednotným způsobem mezi širokou škálou klientů. | Vaše řešení mohou spolupracovat se službami RESTful, sdílet data zjistitelným způsobem a umožnit širokou integraci pomocí zásobníkového protokolu HTTP. |
| Využijte výhod programu Business Connector v oblasti autorizace obchodní logiky a podpory scénářů integrace. | Je k dispozici program Business Connector pro volání kódu X++ ze spravovaného kódu. Doporučujeme, abyste pomocí programu Business Connector vytvářeli pouze obchodní logiku v C\#, nepoužívejte jej pro scénáře integrace. | Program Business Connector již není podporován. Požadavky na autorizaci jsou dány skutečností, že kód jazyka X++ je zkompilován do spravovaného kódu. Zprostředkování komunikace je tedy snadnější. Scénáře integrace jsou splněny pomocí služby OData. | Program Business Connector nelze do budoucna používat. |
| Vyberte škálu (tzn. počet desetinných míst) na skutečných databázových polích a rozšířených datových typech (EDT). | Výchozí škála je 16 a vývojář ji nemůže změnit. | Rozšířené datové typy a pole mají nyní vlastnost škály, kterou lze použít pro jednotlivá pole a rozšířené datové typy. Výchozí hodnota je 6, nikoliv 16. | Je-li použita nižší škála, výkon s tabulkami NCCI (podpora SQL v paměti) se podle hodnoty zvyšuje. Změna škálu podle požadavků jednotlivých polí. |

## <a name="financial-management"></a>Správa financí

<table>
<thead>
<tr>
<th>Co můžete udělat?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Proč je to důležité?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Exportujte účetní struktury do Microsoft Excel.</td>
<td>Není k dispozici.</td>
<td>Nyní můžete vybrat účetní strukturu a exportovat ji do aplikace Excel.</td>
<td>Mnozí zákazníci žádali o možnost exportu účetních struktur do aplikace Excel za účelem snazšího filtrování.</td>
</tr>
<tr>
<td>Zobrazení hlavních knih a struktur rozšířených pravidel, které jsou přidruženy k účetní struktuře na jedné stránce.</td>
<td> Uživatel musí přejít několika formulářů, aby si mohl prohlédnout použité hlavní knihy a účetní strukturu.</td>
<td>Na stránku účetní struktury byla přidána okna s fakty.</td>
<td>Když jsou účetní struktury definovány a upraveny, je přístup k důležitým informacím snazší.</td>
</tr>
<tr>
<td>Zobrazení hlavních knih, které jsou přidruženy k účtové osnově, na jedné stránce.</td>
<td>Uživatel musí přejít na každou společnost a otevřít formulář hlavní knihy, aby si mohl prohlédnout graf účtu, který je přiřazen k hlavní knize.</td>
<td>Na stránku <strong>Účtová osnova</strong> byla přidána okna s fakty.</td>
<td> Když jsou účtové osnovy definovány a přiřazeny, je přístup k důležitým informacím snazší.</td>
</tr>
<tr>
<td>Zobrazení úprav uzávěrek a uzávěrkových transakcí v samostatných sloupcích na stránce <strong>Předvaha</strong>.</td>
<td>Uživatel vidí oba typy transakcí v jednom sloupci.</td>
<td>Na stránku se seznamem <strong>Předvaha</strong> byly přidán další parametr.</td>
<td>Umožňuje přesnější analýzu dat a také je v některých zemích/oblastech vyžadován předpisy pro sestavy.</td>
</tr>
<tr>
<td>Použití nové stránky <strong>Globální hlavní deník</strong>.</td>
<td>Není k dispozici</td>
<td>Nová stránka <strong>Globální hlavní deník</strong> umožňuje zadání hlavních deníků. Oprávnění pro tuto stránku jsou přidány k roli <strong>Účetní</strong>.</td>
<td>Umožňuje u sdílených účetních služeb zadávat hlavní deníky ve všech společnostech bez nutnosti opustit formulář nebo přepnout kontext společnosti.</td>
</tr> 
<tr>
<td>Použití nové stránky <strong>Průzkumník zdroje účetnictví</strong>.</td>
<td>K dispozici v Dynamics AX 2012 R3 CU10.</td>
<td>Nová stránka <strong>Průzkumník zdroje účetnictví</strong> a akce umožňují navigaci ze stránky se seznamem <strong>Předvaha</strong> a <strong>Transakce dokladu</strong>.</td>
<td>Umožňuje zobrazit podrobné informace o zdroji předvahy nebo účetní položky v hlavní knize, nebo použití ad-hoc analýzy.</td>
</tr>
<tr>
<td>Přidání dalších účtovacích vrstev.</td>
<td>Přidání dalších účtovacích vrstev byla práce pro vývojáře.</td>
<td>Nyní je k dispozici deset účtovacích vrstev.</td>
<td>Většina zákazníků přidává další účtovací vrstvy.</td>
</tr>
<tr>
<td>Použití možnosti Související doklad.</td>
<td>Není k dispozici</td>
<td>Možnost Související doklad je k dispozici pro uživatele, kteří chtějí vidět doklad ve společnosti pro vyrovnání při zaúčtování mezipodnikové transakce. Ze souvisejících dokladů mohou uživatelé kliknout na podrobnosti a rychle přejít na doklad společnosti pro vyrovnání.</td>
<td>Při zaúčtování mezipodnikové transakce nemají uživatelé přehled ani stopu k dokladu, který byl zaúčtován ve společnosti pro vyrovnání.</td>
</tr>
<tr>
<td>Hromadné uzavření finančního období</td>
<td>Není k dispozici</td>
<td>Uživatelé mohou aktualizovat přístup k modulu a měnit stav období pro více společností současně.</td>
<td>Před zavedením této funkce museli uživatelé měnit, ke které společnosti jsou přihlášeni, přejít na formulář s kalendářem hlavní knihy a ručně aktualizovat přístup modulu a stav období.</td>
</tr>
<tr>
<td>Nastavení směnných kurzů využívajících modul Oanda.</td>
<td>Konfigurace poskytovatele směnného kurzu pro import sazby Oanda byla práce pro vývojáře.</td>
<td>Pokud mají uživatelé klíč ke službě Oanda, mohou jej zadat při konfiguraci poskytovatele směnného kurzu.</td>
<td>Uživatelé mohou využít výhod okamžitě dostupné funkce tím, že směnné kurzy budou využívat modul Oanda importovaný v plánovaných intervalech.</td>
</tr>
<tr>
<td>Filtrování finančních sestav (Management Reporter) podle dimenzí, atributů, dat a scénářů.</td>
<td> Všechno filtrování sestav aplikace Management Reporter se provádí prostřednictvím návrhu sestavy. Pokud si chce uživatel s oprávněním k zobrazení zobrazit například sestavu pro jiné datum, musí návrhář sestav provést změny.</td>
<td>Byly přidány možnosti sestavy, takže různé filtry lze použít, když si uživatel prohlíží sestavu. Potom je vygenerována nová sestava na základně těchto filtrů.</td>
<td>Spotřebitelé finančních sestav mohou použít různé filtry pro dimenze, data, atributy a scénáře, aniž by bylo nutné aktualizovat návrhy sestav.</td>
</tr>
<tr>
<td>Zobrazení finančních sestav (Management Reporter) v klientovi aplikace Microsoft Dynamics AX.</td>
<td>K zobrazování sestav aplikace Management Reporter se používal samostatný webový klient.</td>
<td>Ke všem finančním sestavám lze přistoupit z klienta aplikace Dynamics AX. Uživatel vybere sestavu, kterou si chce zobrazit, a sestava se zobrazí v klientovi.</td>
<td>Nyní lze zobrazit finanční sestavy, aniž by bylo nutné přistupovat k jinému klientovi/aplikaci.</td>
</tr>
<tr>
<td>Tisk finančních sestav (Management Reporter) z klienta aplikace Microsoft Dynamics AX.</td>
<td>Tisk sestavy může využívat možnosti tisku v prohlížeči, a může tisknout pouze to, co se nachází na obrazovce uživatelů.</td>
<td>Uživatel může vybrat úroveň podrobností a nastavení stránky se sestavou pomocí možnosti Tisk ve finanční sestavě v klientovi Dynamics AX.</td>
<td>Tištěné sestavy se tisknou tak, jak to uživatelé očekávají, namísto tisku webové stránky.</td>
</tr><tr>
<td>Analýza finančních dat pomocí obsahu Power BI Sledování finanční výkonnosti.</td>
<td>Není k dispozici.</td>
<td>Na stránce PowerBI.com vyberte možnost <strong>Načíst data</strong> a poté vyberte balíček obsahu <strong>Dynamics AX – Finanční výkonnost</strong>. Zadejte adresu URL koncového bodu Dynamics AX, aby se data zobrazovala na řídicím panelu.</td>
<td>Třemi až čtyřmi kliknutími mohou organizace nasadit do provozu řídicí panel Power BI obsahující důležitá finanční data. Obsah lze přizpůsobit podle požadavků organizace.</td>
</tr>
<tr>
<td>Sledování procesů uzávěrek finančního období.</td>
<td>Není k dispozici.</td>
<td>Šablony a plány uzávěrek lze vytvářet pomocí konfigurace uzávěrky finančního období. Ke sledování průběhu plánů uzávěrky mezi více společnostmi použijte pracovní prostor <strong>Uzavření finančního období</strong> .</td>
<td>Tento pracovní prostor eliminuje použití ručních systémů k definování, plánování a komunikaci ohledně činností spojených s uzávěrkou. Počet dní do uzávěrky se tím sníží.</td>
</tr>
<tr>
<td>Sledování rozpočtu vůči skutečným údajům a vytvoření prognóz hlavní knihy pomocí pracovního prostoru <strong>Rozpočty a prognózy hlavní knihy</strong> a dalších formulářů.</td>
<td>Není k dispozici.</td>
<td> K pracovnímu prostoru lze přistupovat prostřednictvím řídicího panelu aplikace Dynamics AX. Obsahuje odkazy na několik nových stránek s dotazy: <strong>Souhrn skutečných a rozpočtových hodnot</strong>, <strong>Statistický souhrn kontroly rozpočtu</strong>, <strong>Položky registru rozpočtu</strong> a <strong>Plány rozpočtu</strong>.</td>
<td>Nové stránky s dorazy umožňují snadný přístup k informacím o rozpočtu. Pracovní prostor kombinuje všechny úkoly správy a sledování rozpočtu na jednom místě a vedoucím rozpočtu a vedoucím účetním se snadno používá.</td>
</tr>
<tr>
<td>Vytvoření rozložení pro plány a prognózy rozpočtu.</td>
<td>Dokument <strong>Plán rozpočtu</strong> se zobrazuje jako seznam řádků, které mají efektivní data a částky pro kombinace finančních dimenzí. Uživatel musí vytvořit a použít šablonu pro aplikaci Excel k zobrazení dat plánu rozpočtu v kontingenční tabulce.</td>
<td>Pro plány a prognózy rozpočtu je k dispozici neomezený počet rozvržení. V rozvržení lze kombinovat vybrané finanční dimenze, uživatelem definované sloupce a další atributy řádku (například komentáře, projekty nebo majetek). Uživatelé mohou průběžně přepínat rozvržení dokumentu plánu rozpočtu a upravovat data pomocí jakéhokoliv vybraného rozvržení. Konfigurace plánování rozpočtu je zjednodušena eliminací omezení scénáře a použitím rozvržení k definici dat, která mohou zobrazena a upravena v jednotlivých fázích dokumentu plánu rozpočtu.</td>
<td>To dává možnost pružně vytvářet a upravovat plány rozpočtu pomocí aplikace Excel i klienta aplikace Dynamics AX. Šablony pro sešity aplikace Excel lze generovat pomocí nastavení rozvržení plánu rozpočtu.</td>
</tr>
<tr>
<td>Tisk sestavy <strong>Transakce faktur dodavatele</strong> pomocí informací ze sestavy <strong>Detailní výpis dne splatnosti</strong>, která zahrnuje dny po splatnosti.</td>
<td>Je nutné vytisknout dvě různé sestavy: <strong>Detailní výpis dne splatnosti</strong> a <strong>Transakce faktur dodavatele</strong>.</td>
<td>Informace na dvou sestavách byly konsolidovány do sestavy <strong>Transakce faktur dodavatele</strong>. Sestava <strong>Detailní výpis dne splatnosti</strong> byla zrušena.</td>
<td>To eliminuje nutnost tisku dvou samostatných, avšak souvisejících sestav.</td>
</tr>
<tr>
<td>Generování zákonem předepsaných sestav přímo ve formátu PDF.</td>
<td>Nejprve je nutné vygenerovat zákonem předepsanou sestavu v jednom formátu a poté ji exportovat do formátu PDF.</td>
<td>Formát PDF je výchozím formátem pro zákonem předepsané sestavy.</td>
<td>Zajišťuje jednotné zobrazení na obrazovce počítače i ve vytištěné podobě.</td>
</tr>
<tr>
<td>Spuštění procesu vyrovnání DPH v podobě dávkového zpracování.</td>
<td>Není k dispozici.</td>
<td>Na stránce <strong>Období vyrovnání DPH</strong> můžete určit, zda má být proces vyrovnání spuštěn v dávkovém režimu.</td>
<td>U období s mnoha daňovými transakcemi může být proces vyrovnání časově náročný, takže bude pravděpodobně výhodnější spustit proces na pozadí v podobě dávkového zpracování.</td>
</tr>
</tbody>
</table>

## <a name="foundation"></a>Nadace

<table>
<thead>
<tr>
<th>Co můžete udělat?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Proč je to důležité?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Přístup ke klientovi kdykoliv a odkudkoliv.</td>
<td>Klient aplikace AX 2012 pro stolní počítače nabízí kompletní sadu formulářů, avšak lze jej spustit pouze v počítačích se systémem Microsoft Windows a je nutné jej nainstalovat. V kombinaci s klientem pro stolní počítače se často používá terminálový server, který umožňuje přístup prostřednictvím sítě WAN. Webový klient podnikového portálu disponuje omezenou sadou formulářů.</td>
<td>Dva klienti AX 2012 byli nahrazeni jedním standardizovaným webovým klientem, který poskytuje kompletní sadu funkcí klienta pro stolní počítače i dosah klienta podnikového portálu.</td>
<td>Tím je zabráněno tomu, aby vývojáři museli rozdělovat své úsilí mezi dvě platformy uživatelského rozhraní. Použití standardních webových rozhraní eliminuje nutnost terminálového serveru.</td>
</tr>
<tr>
<td>Produktivita pomocí nového záznamníku úkolů.</td>
<td>Záznamník úkolů AX 2012 vyžaduje přímý přístup k počítači se serverem aplikačního objektového serveru (AOS) a vyšší oprávnění a neposkytuje žádné možnosti úpravy.</td>
<td>Nový záznamník úkolů lze použít přímo z webové klienta. Přístup k záznamníku úkolů nevyžaduje oprávnění správce. Zaznamenané kroky lze zobrazit přímo při záznamu, byly zavedeny nové možnosti úprav a záznamník úkolů podporuje kromě stávajících scénářů modelování podnikových procesů (BPM) i další scénáře.</td>
<td>Nový záznamník úkolů nabízí jednodušší a efektivnější nové funkce v aplikaci Dynamics AX. Některé z těchto funkcí jsou k dispozici už nyní a další budou následovat v budoucnosti.</td>
</tr>
<tr>
<td>Pomoc uživatelům lépe porozumět jejich nadcházející práci s pracovními prostory.</td>
<td>Pracovní plocha rolí poskytuje přehled informací souvisejících s pracovní funkci uživatele ve vašem podniku nebo organizaci.</td>
<td>Pracovní prostory jsou nový koncept v aplikaci Dynamics AX, které jsou určeny k nahrazení center rolí jako hlavního způsobu navigace úkoly a určitými stránkami. Poskytují jednostránkový přehled o obchodní činnosti a pomoc uživatelům lépe pochopit aktuální stav, nadcházející pracovní zatížení a výkon uživatele nebo procesu. Pracovní prostory jsou přesnější, než pracovní plochy rolí v AX 2012, a uživatel může mít přístup k více pracovním prostorům.</td>
<td>Pracovní prostory jsou určeny pro zvýšení produktivity uživatelů. Vývojáři musí vytvářet pracovní prostor pro každou významnou "aktivitu" podporovanou v produktu. Původní pracovní plocha role z AX 2012 bude standardně nahrazena více pracovními prostory v aktuální verzi aplikace Dynamics AX.</td>
</tr>
<tr>
<td>Vytváření formulářů reagujících na velikost zobrazení v prohlížeči nebo zařízení.</td>
<td>V aplikaci AX 2012 byl obsah formuláře pevně stanoven pomocí sloupců, a celková výška a šířka formuláře do značné míry závisela na ovládacích prvcích ve formuláři.</td>
<td>S přesunem na web v nejnovějším produktu Dynamics AX nyní rozměry formuláře vychází z velikosti zobrazení v prohlížeči nebo zařízení. Ovládací prvky a parametry pro rozložení byly změněny nebo přidány, aby lépe reagovaly na změny velikosti zobrazení.</td>
<td>Obsah formuláře musí být lépe reagující pro optimální využívání dostupné výšky a šířky prohlížeče nebo zařízení. Dosažení responzivního návrhu může požadovat změny ve způsobu, jakým je formulář modelován.</td>
</tr>
<tr>
<td>Použití vzorků pro efektivnější rozvoj formuláře.</td>
<td>Šablony formulářů byly na začátku vývoje formulářů v aplikaci AX 2012 k dispozici na základě stylu formuláře. Kontrola stylu formuláře (volitelný doplněk) poskytoval informace o tom, jak se formulář odkláněl od jeho odpovídající šablony.</td>
<td>V aktuální verzi aplikace Dynamics AX byly zavedeny vzory formulářů. Vzory formulářů představují kombinace šablon formulářů a kontrolu stylu formuláře, a jsou úzce integrovány do vývojového prostředí. Vzory byly definovány na úrovni formuláře (například AX 2012) s dalšími dílčími vzory k dispozici na úrovni skupiny a karty.</td>
<td>Formuláře, které jsou v souladu se vzory, mají mnoho výhod, včetně více konzistentního uživatelského rozhraní, jednoduššího vývoje, jednodušších postupů při upgradu formuláře, a posílení důvěry v responzivnosti rozložení formuláře.</td>
</tr>
</tbody>
</table>

## <a name="help"></a>Nápověda

<table>
<thead>
<tr>
<th>Co můžete udělat?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Proč je to důležité?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Přístup k procesní nápovědě (průvodce úkolem) a rámcovým tématům kliknutím na tlačítko <strong>Nápověda</strong>.</td>
<td>Systém nápovědy aplikace AX 2012 odkazuje na témata ve formátu HTML, která jsou uložena na místním webovém serveru. Zákazníci a partneři si mohou vytvářet svou vlastní nápovědu.</td>
<td>Systém nápovědy v aktuální verzi aplikace Dynamics AX zobrazuje průvodce úkolem, kteří jsou uloženi v BPM služby Microsoft Dynamics Lifecycle Services (LCS). Systém nápovědy také zobrazuje témata z webu dokumentů společnosti Microsoft. Další infirmace uvádí nápověda pro <a href="help-overview.md" data-raw-source="[Dynamics AX Help - Getting Started](help-overview.md)">Dynamics AX Help – začínáme</a> a <a href="new-task-guides-available-february-2016.md" data-raw-source="[New task guides available (February 2016)](new-task-guides-available-february-2016.md)">Dostupní nový průvodci záznamem úloh (únor 2016)</a>.</td>
<td>Průvodci úkolem vás interaktivním způsobem provedou kroky daného úkolu nebo obchodního procesu. Můžete stahovat a upravovat průvodce úkoly, které společnost Microsoft poskytuje. Téma nabízí rychlejší a pružnější způsob vytváření, dodávání a aktualizace dokumentace k produktu. Díky tomu pomáhá zajistit, že budete mít přístup k aktuálním technickým informacím.</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>Správa lidského kapitálu

<table>
<thead>
<tr>
<th>Co můžete udělat?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Proč je to důležité?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Přenos dovedností a certifikátů k účastníkům třídy po dokončení kurzu.</td>
<td>Jedná se o ruční proces.</td>
<td>Po dokončení kurzu je k dispozici nová možnost pro aktualizaci záznamů účastníka nové o nové dovednosti a certifikáty.</td>
<td>Jedná se o nový a efektivní způsob, jak aktualizovat záznamy zaměstnanců.</td>
</tr>
<tr>
<td>Rychlé ověření zaměstnání.</td>
<td>Jedná se o ruční proces.</td>
<td>Oddělení lidských zdrojů může pomocí pracovního prostoru nebo stránky zaměstnance rychle ověřit zaměstnání.</td>
<td>Oddělení lidských zdrojů již nemá přístup k několika stránkám, na kterých bylo možné ověřit počáteční datum, manažera, počet měsíců na dané pozici a údaje o kompenzaci.</td>
</tr>
<tr>
<td>Možnost prohlížení, aktualizace a odstraňování informací v systému ze strany zaměstnanců.</td>
<td>K dispozici, avšak s omezenými možnostmi zobrazení a aktualizace.</td>
<td>Tato funkce je povolena a zaměstnanci a dodavatelé si díky ní mohou zobrazit celou řadu osobních údajů. Volitelně lze workflow použít při vytvoření, aktualizaci nebo odstranění informací.</td>
<td>Dává zaměstnancům kontrolu nad jejich informacemi. Mezi dostupné funkce patří aktualizace adresy nebo kontaktních informací, podávání žádosti o zaměstnání, vyplňování dotazníku nebo aktualizace obrázku. Pokud je workflow povolen, může informace zkontrolovat schvalující nebo mohou být schváleny automaticky (záleží na vašich obchodních procesech).</td>
</tr>
<tr>
<td>Možnost zobrazení nebo úpravy informací i zaměstnancích ze strany manažerů</td>
<td>K dispozici, avšak s omezenými možnostmi zobrazení a aktualizace.</td>
<td>V závislosti na konfiguraci a zabezpečení si mohou manažeři prohlížet nebo upravovat informace o zaměstnancích.</td>
<td>Manažeři mají díky tomu přístup k důležitým datům o zaměstnancích, takže se mohou lépe rozhodovat o volbě zdrojů, výkonnosti a rozvoje zaměstnance.</td>
</tr>
<tr>
<td>Využijte výhod funkcí samoobsluhy pro manažery.</td>
<td>Není k dispozici</td>
<td>Manažeři mohou nyní odesílat požadavky na nové zaměstnance (zaměstnance a dodavatele), převody a ukončení spolupráce (ukončení zaměstnání). Manažeři mohou také požádat o novou pozici, prodloužit dobu trvání pozice nebo požadovat změnu pozice.</td>
<td>Tyto scénáře byly dříve přístupné pouze pro oddělení lidských zdrojů. Povolení těchto scénářů poskytuje výkonné nástroje pro správce v organizaci. Lze povolit volitelné pracovní postupy, které poskytují odpovídající úroveň kontroly a schválení.</td>
</tr>
<tr>
<td>Zobrazení výsledků zpracování kompenzací.</td>
<td>Výsledky jsou k dispozici pouze v době zpracování.</td>
<td>Výsledky zpracování kompenzací je nyní možné zobrazit kdykoli po spuštění procesu.</td>
<td>To nabízí skvělé možnosti auditu procesu a výsledků procesu. Také je tím zajištěn komplexní náhled na data před aktualizací záznamů o zaměstnancích.</td>
</tr>
<tr>
<td>Zobrazení výsledků zpracování zaměstnaneckých výhod.</td>
<td>Výsledky jsou k dispozici pouze v době zpracování.</td>
<td>Výsledky zpracování zaměstnaneckých výhod je nyní možné zobrazit kdykoli po spuštění procesu.</td>
<td>Tím je zajištěn kompletní náhled na data, která byla aktualizována při přihlášení k zaměstnaneckým výhodám a změnách nákladů.</td>
</tr>
<tr>
<td>Zobrazení změn na časové ose „Datum platnosti“.</td>
<td>Není k dispozici.</td>
<td>Tento nástroj k porovnání je k dispozici pro zaměstnance, pozice a úlohy. Nabízí kompletní náhled na změny mezi jednotlivými verzemi záznamu.</td>
<td>Při zobrazování změn provedených v čase u záznamů o zaměstnancích, pozicích a úlohách vám ušetří čas. Díky tomu můžete rychleji porovnat dvě verze záznamu anebo všechny záznamy v čase.</td>
</tr>
<tr>
<td>Zobrazení zaměstnanců ze strany společnosti</td>
<td>Jedná se o ruční proces, který se provádí filtrováním.</td>
<td>Seznamy zaměstnanců a dodavatelů jsou automaticky filtrovány podle společnosti, ke které jste se přihlásili.</td>
<td>Nabízí filtrované zobrazení zaměstnanců, kteří jsou zaměstnáni v přihlášené společnosti. I nadále je k dispozici seznam pracovníků pro účely nefiltrovaného zobrazení všech zaměstnanců a dodavatelů. V aktuální verzi aplikace Dynamics AX systém nezmění společnost podle zaměstnance, který je vybrán v seznamu.</td>
</tr>
<tr>
<td>Aktualizace seznamu účastníků kurzu.</td>
<td>Není k dispozici.</td>
<td>Účastníci kurzu mohou být odstraněni ze seznamu účastníků.</td>
<td>Snadno lze aktualizovat seznam účastníků kurzu a odstranit tak ty, kteří se zaregistrovali omylem.</td>
</tr>
<tr>
<td>Správa událostí kompenzace ve skupině.</td>
<td>Není k dispozici.</td>
<td>Tato funkce zefektivňuje zpracování změn kompenzací pro zaměstnance.</td>
<td>Usnadnění a zefektivnění procesu aktualizace záznamů o zaměstnancích prostřednictvím pracovního prostoru kompenzace a souvisejících stránek.</td>
</tr>
</tbody>
</table>

## <a name="inventory-management"></a>Řízení zásob

Nebyly přidány následující nové funkce.

## <a name="localization"></a>Lokalizace

<table>
<thead>
<tr>
<th>Co můžete udělat?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Proč je to důležité?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Konfigurace a generování elektronických dokumentů pro splnění právních předpisů v různých zemích či oblastech.</td>
<td>Elektronické dokumenty jsou pevně začleněny v kódu v jazyce X ++ nebo Extensible Stylesheet Language Transformations (XSLT). Jakékoliv úpravy formátu vyžadují práci vývojového týmu. Nelze samostatně přistupovat k datům a formátování. Nasazení upraveného formátu vyžaduje nový balíček s opravou hotfix pro aplikaci Microsoft Dynamics AX, kterým se přepíše stávající formát. Vlastní úpravy každého formátu je nutné ručně přenést do zdrojového kódu nového balíčku s opravou hotfix pro aplikaci Microsoft Dynamics AX.</td>
<td>Elektronické výkaznictví (EV) je nový nástroj pro konfiguraci a generování elektronických dokumentů, který je namísto vývojářů určen pro podnikové uživatele. S EV můžete vytvářet modely dat, které budou specifické pro domény a nezávislé na databázi aplikace Microsoft Dynamics AX, jež je zdrojem dat pro formáty dokumentu. Podnikový uživatel můře nakonfigurovat formáty, které jsou založené na těchto datových modelech specifických pro domény (například platby, sestavy Intrastat nebo daňové sestavy). Uživatel konfiguruje formáty pomocí jednoduchého vizuálního nástroje podobného aplikaci Excel. Nástroj EV aktuálně podporuje generování elektronických dokumentů v textovém formátu, ve formátu XML a ve formátu pro aplikaci Excel. Tyto dokumenty lze vygenerovat současně a zabalit je do souborů ZIP. Modely dat a formáty podporují správu verzí. Verze formátu mohou mít období platnosti. Každá verze modelu dat nebo formátu je uložena v samostatné konfiguraci a distribuována partnerům a zákazníkům pomocí LCS. Partneři a odběratelé si mohou přizpůsobovat modely dat a formáty společnosti Microsoft nebo si vytvořit vlastní. Nástroj EV ukládá změny partnerů a odběratelů v podobě přírůstků ke konfiguracím společnosti Microsoft, což zjednodušuje upgrade na nové verze konfigurací společnosti Microsoft. Pomocí LCS mohou partneři sdílet také své konfigurace modelů dat a formátů s ostatními partnery a odběrateli, kteří si je mohou upravovat a sdílet. Přírůstkové úpravy a snadné upgrady jsou podporovány v celém řetězci přizpůsobování.</td>
<td>Nástroj EV usnadňuje vytváření, údržbu a upgrade formátů elektronických dokumentů pro splnění právních předpisů v různých zemích či oblastech. Nástroj EV zrychluje a usnadňuje proces vytváření nebo změny formátů elektronických dokumentů. Tyto změny mohou být provedeny podnikovými uživateli a nemusí je dělat vývojáři. Nástroj EV zrychluje a usnadňuje partnerům a odběratelům upgrade svých úprav formátů na nové verze zveřejněné společností Microsoft nebo jinými partnery. Nástroj EV poskytuje (prostřednictvím LCS) společnosti Microsoft a partnerům jednotný způsob, jak distribuovat konfigurace elektronických dokumentů jiným partnerům a odběratelům. Nástroj EV partnerům a odběratelům rovněž usnadňuje přizpůsobení, upgrade a distribuci formátů elektronických dokumentů pro své konkrétní podnikové potřeby.</td>
</tr>
<tr>
<td>(MEX) Generování zákonem předepsaných sestav mexické daně z přidané hodnoty (DPH).</td>
<td>Je nutné vygenerovat sestavy <strong>prodejní a nákupní DPH</strong> pomocí funkce neuplatněné DPH, aby uživatelé mohli podle stavu identifikovat transakce, které patří do oddílů uplatněných a neuplatněných.</td>
<td>Sestavy <strong>Prodejní a nákupní DPH</strong> byly změněny – nyní zohledňují podmínkovou funkci DPH pouze při použití konkrétních období vyrovnání pro definici kódů uplatněné a neuplatněné DPH.</td>
<td>Změny v konfiguraci kódů DPH jsou požadovány předtím, než mohou uživatelé vygenerovat tyto sestavy správně. Funkce podmíněné DPH je vyžadována a uživatel musí nakonfigurovat samostatná období vyrovnání (neuplatněné a uplatněné), aby mohl v příslušných oblastech identifikovat transakce.</td>
</tr>
<tr>
<td>(JPN) Správa dokumentu s prohlášením zrychleného odpisu japonského dlouhodobého majetku.</td>
<td>Není k dispozici.</td>
<td>Informace o důležitém prohlášení jsou uloženy centrálně v jednom dokumentu kvůli zjednodušení údržby.</td>
<td>Soulad dokumentu a snadná správa pomáhají předcházet potížím při auditech a ostatních hodnoceních.</td>
</tr>
<tr>
<td>(JPN) Ověření znaků JBA v bankovním účtu.</td>
<td>Není k dispozici.</td>
<td>Můžete ověřit, že pole pro jméno kana obsahuje pouze znaky, které jsou povoleny v bankovním formátu JBA.</td>
<td>Tímto se eliminuje riziko přerušení při generování souboru plateb z důvodu neplatných znaků.</td>
</tr>
<tr>
<td>(JPN) Zachycení haléřového rozdílu v japonském dlouhodobém majetku na konci fiskálního roku.</td>
<td>Není k dispozici.</td>
<td>Na stránce <strong>Parametry dlouhodobého majetku</strong> můžete zvolit, zda má být zachycován na konci fiskálního období nebo fiskálního roku.</td>
<td>Poskytnutí větší flexibility kvůli souladu s místními postupy.</td>
</tr>
<tr>
<td>(JPN) Vytvoření řady tabulek 16 pro japonské podnikové daňové přiznání pro souhrnnou částku podle hlavního typu dlouhodobého majetku.</td>
<td>Není k dispozici.</td>
<td>U oceňovacích modelů dlouhodobého majetku je možné provést shrnutí podle hlavního typu. Ve výchozím nastavení se tato funkce používá pro nově vytvořený dlouhodobý majetek.</td>
<td>U velkých společností s tisíci dlouhodobými majetky přispívají souhrnné sestavy k výraznému zmenšení vygenerované sestavy.</td>
</tr>
<tr>
<td>(JPN) Zahájení přidělování rezervy na zvláštní odpisy z dalšího fiskálního roku pro japonský dlouhodobý majetek.</td>
<td>Není k dispozici.</td>
<td>U oceňovacích modelů dlouhodobého majetku, které mají příslušný mimořádný odpisový plán, můžete zahájit přidělování z dalšího fiskálního období nebo dalšího fiskálního roku.</td>
<td>Poskytnutí větší flexibility kvůli souladu s místními postupy.</td>
</tr>
<tr>
<td>(JPN) Generování sestavy japonské spotřební daně obsahující revidované daňové sazby.</td>
<td>Sestava spotřební daně je dostupná pro daňovou sazbu 5 procent.</td>
<td>Sestava spotřební daně obsahuje oddíl pro revidovanou daňovou sazbu (například 8 procent).</td>
<td>Rozvržení bylo nově oznámeno vládou.</td>
</tr>
<tr>
<td>(EU) Konfigurace nastavení zaokrouhlení pro souhrnné hlášení EU.</td>
<td>Nastavení zaokrouhlení pro souhrnné hlášení EU pro různé země a oblasti jsou pevnou součástí jazyka X++ nebo Extensible Stylesheet Language Transformations (XSLT).</td>
<td>Nastavení zaokrouhlení jsou přidána do parametrů zahraničního obchodu. Můžete konfigurovat přesnost zaokrouhlení, metodu zaokrouhlení, přesnost výstupu a chování pro menší číslo, než na jaké se vztahuje přesnost zaokrouhlení.</td>
<td>Tím se sjednocuje a zjednodušuje konfigurace souhrnného hlášení EU. Úprava nastavení zaokrouhlení již nevyžaduje další vývoj.</td>
</tr>
<tr>
<td>(EU) Konfigurace pravidel použitelnosti stornovacího poplatku.</td>
<td>Pravidla použitelnosti stornovacího poplatku jsou pevnou součástí scénáře domácího stornovacího poplatku. Lze nastavit mezní hodnotu použitelnosti pro každou skupinu položek. Funkce je k dispozici pouze pro Velkou Británii.</td>
<td>Pravidla použitelnosti stornovacího poplatku můžete nakonfigurovat dle typu dokladu (nákupní/prodejní objednávky, faktury dodavatele, volné faktury atd.) a skupiny stornovacího poplatku, které jsou kombinací položek, skupin položek a kategorie nákupu/prodeje. Pravidla použitelnosti jsou vázána na datum platnosti. Jednotlivé kódy DPH ve skupinách DPH můžete také označit jako platné pro stornovací poplatek. Sestava prodejní faktury bude upravena tak, aby představovala detaily použitého stornovacího poplatku. Funkce je k dispozici ve všech evropských zemích.</td>
<td>Tato změna sjednocuje konfiguraci pravidel použitelnosti stornovacího poplatku a podporuje přijetí předpisů pro domácí stornovací poplatky v evropských zemích a oblastech.</td>
</tr>
<tr>
<td>(DE) Generování souboru auditu pro Německo - GDPdUGoBD</td>
<td>Uživatelé mohou vytvořit definice tabulek, které obsahují finanční data určená k exportu ve formátu přijímaného německými auditory a orgány.</td>
<td>Tato funkce byla implementována jako konfigurace elektronického vykazování. Funkce je k dispozici pro Německo a Rakousko.</td>
<td>Tato změna poskytuje uživateli mnohem více možností při formátování dat a transformaci, ale také poskytuje všechny výhody spojené se správou životního cyklu konfigurace elektronického vykazování, jako je snadná výměna konfigurace, správa verzí, atd.</td>
</tr>
<tr>
<td>(FR) Sestava seznamu zůstatků se součty skupiny účtů.</td>
<td>Seznam zůstatků se součty skupiny účtů je implementován jako sestava SSRS (LedgerAccountSum_FR).</td>
<td>Seznam zůstatků se součty skupiny účtů je implementován jako sestava Management Reporter, a je k dispozici ve složce s lokalizovanými finančními sestavami pro knihovnu datových zdrojů LCS.</td>
<td>To umožňuje uživatelům získat všechny výhody a volnost nastavení pomocí finančních sestav v nástroji Management Reporter.</td>
</tr>
<tr>
<td>(EU) Avízo platby, průvodka a kontrolní sestavy pro platby.</td>
<td>Všechny tyto zprávy jsou implementované sestavy/sestavy SSRS.</td>
<td>Tyto zprávy byly implementovány jako šablony Open XML pro použití v aplikaci Microsoft Excel.</td>
<td>Konfigurace elektronické platby obsahují nástroj pro nastavení formátu souboru plateb a jejich šablony. To umožňuje uživatelům získat všechny výhody a volnost přizpůsobení sestav pomocí nástroje Elektronické výkaznictví.</td>
</tr>
<tr>
<td>(EU) Konfigurace nastavení zaokrouhlení pro Intrastat.</td>
<td>Nastavení zaokrouhlení pro Intrastat pro různé země a oblasti jsou pevnou součástí jazyka X++ nebo Extensible Stylesheet Language Transformations (XSLT).</td>
<td>Nastavení zaokrouhlení jsou přidána do parametrů zahraničního obchodu. Můžete konfigurovat přesnost zaokrouhlení, metodu zaokrouhlení, přesnost výstupu a chování pro menší číslo, než na jaké se vztahuje přesnost zaokrouhlení.</td>
<td>Tím se sjednocuje a zjednodušuje konfigurace hlášení Intrastat. Úprava nastavení zaokrouhlení již nevyžaduje další vývoj.</td>
</tr>
<tr>
<td>(EU) Nastavení kódů komodit systému Intrastat v hierarchiích kategorie.</td>
<td>Kódy komodit systému Intrastat představují samostatný seznam. Zatímco existuje hierarchie kategorií typu „Kód komodity“, tyto kódy komodity je možné nastavit s výchozími hodnotami v rámci nástroje Retail HQent a prodejních kategorií.</td>
<td>Samostatné seznamy kódů komodit systému Intrastat jsou sloučeny s hierarchií produktu typu „Kód komodity“.</td>
<td>To sjednocuje přístup pro přiřazování kódů komodit k uvolněným produktům a kategoriím v prodejních a nákupních dokladech.</td>
</tr>
<tr>
<td>(EU) Hlášení množství v dalších jednotkách pro systém Intrastat pomocí nastavení převodu jednotky.</td>
<td>Kód komodit v systému Intrastat obsahuje textové pole pro identifikaci dalších jednotek a na kartě<strong> Výrobek</strong> se nachází pole identifikující další jednotky v kilogramech.</td>
<td>Další jednotky pro kód komodit systému Intrastat je vybrán ze seznamu jednotek. Množství dodatečných jednotek se počítá z nastavení převodu jednotky.</td>
<td>To sjednocuje postup pro přepočet z jednotek transakce na dodatečné jednotky.</td>
</tr>
<tr>
<td>(EU) Přiřazení výchozí metody přepravy ke způsobu dodání.</td>
<td>Není k dispozici</td>
<td>Pole pro výchozí metodu přepravy je přidáno ke způsobu dodání.</td>
<td>To zjednodušuje přípravu vykazování v systému Intrastat.</td>
</tr>
<tr>
<td>(EU) Označení vydaného produktu, který se nebude hlásit v systému Intrastat.</td>
<td>Není k dispozici</td>
<td>K uvolněnému produktu je přidána možnost vyloučit položku z hlášení Intrastat.</td>
<td>To zjednodušuje přípravu vykazování v systému Intrastat.</td>
</tr>
</tbody>
</table>

## <a name="manufacturing"></a>Výroba

| Co můžete udělat? | Dynamics AX 2012 |
|------------------|------------------|
| Provedení kontroly dostupnosti materiálu pro výrobní zakázky na samostatné stránce, která se otevírá z pracovního prostoru **Správa výrobního provozu**. | Není k dispozici |
| Spuštění a hlášení průběhu u výrobních úloh pomocí nové stránky **Zařízení úkolového lístku**. | Formulář **Registrace úlohy** je určen především pro velké terminálové obrazovky a uživatelské rozhraní se obvykle ovládá pomocí myši. |

## <a name="master-planning-and-forecasting"></a>Hlavní plánování a prognóza

| Co můžete udělat? | Dynamics AX 2012 | Dynamics AX 7.0 | Proč je to důležité? |
|------------------|------------------|-----------------|------------------------|
| Může uživatele upozornit na to, že prodejní objednávka nebo výrobní zakázka nejsou připraveny k dodání k naplánovanému datu. | Upozornění, které jsou vytvořena na základě hlavního plánování, se nazývají *termínové zprávy*. *Termíny* jsou smlouvy mezi dvěma stranami nákupu nebo prodeje majetku za cenu, která je sjednána dnes (*termínová cena*), i když k dodání a platbě může dojít v budoucnu (*datum dodání*). | *Termínové zprávy* a *data termínů* byly přejmenovány na *vypočtená zpoždění* a *zpožděná data*. | Pojmy používané v aplikaci AX 2012 byly nepřesné a vedly k nesprávným překladům. |
| Získání rychlého přehledu o stavu průběhu hlavního plánování, naléhavých plánovaných objednávkách a plánovaných objednávkách, které mají za následek zpoždění. | Informace jsou k dispozici, ale jsou roztříštěny v několika formulářích. | Pracovní prostor **Hlavní plánování** nabízí přehledné informace o dokončení posledního průběhu hlavního plánování a o tom, zda došlo k chybám, jaké jsou naléhavé plánované objednávky a které objednávky způsobují zpoždění. | Výhodou pracovního prostoru je přehlednost. Relevantní informace jsou shromážděny a mohou pomoct s hlavním plánováním a zvýšením produktivity. |
| Použití aplikace Excel k aktualizace prognóz poptávky. | Není k dispozici. | Při zadávání, aktualizaci a odstraňování prognóz poptávky můžete využít výhod bezproblémové integrace s aplikací Excel. | Je tím zvýšena efektivita a produktivita. |
| Umožňuje odhadovat budoucí poptávku a vytvářet prognózy poptávky na základě historických dat transakcí. | V Microsoft Dynamics AX 2012 R3 modely prognózy v Microsoft SQL Server Analysis Service slouží k vytváření prognózy předpovědi poptávky. | Odhadování budoucí poptávky pomocí výkonu a rozšiřitelnosti cloudové služby Microsoft Azure Machine Learning. Snadno se používá a ve službě Machine Learning můžete modely prognóz rozšířit tak, aby splňovaly požadavky odběratelů. Služba provádí výběr nejlépe odpovídajícího modelu a nabízí klíčové indikátory výkonnosti (KPI), které lze použít k výpočtu přesnosti prognózy. | Generování přesnějších prognóz pomocí technik služby Machine Learning. |
| Optimalizace data objednávky a množství na základě grafického znázornění souvisejících akcí z průběhu hlavního plánování. | Přehledový graf akcí je k dispozici, ale obsahuje všechny související akce. Jakmile jsou akce použity, okamžitě zmizí ze zobrazení. | Graf akcí je přehlednější. Disponuje možnosti, kterými lze zobrazit pouze použité akce a přímo související akce. Jakmile jsou akce použity, sníží se jejich jas, avšak zůstanou i nadále zobrazeny. Tím je zaručena přehlednost. Do grafu akcí jsou přidány další informace, aby se data zobrazila na jedné stránce. | Budete se moci soustředit pouze na relevantní akce, což se projeví zvýšením produktivity. |

## <a name="procurement-and-sourcing"></a>Zásobování a zdroje

| Co můžete udělat? | Dynamics AX 2012 | Dynamics AX 7.0 | Proč je to důležité? |
|------------------|------------------|-----------------|------------------------|
| Pomocí pracovního prostoru **Příprava nákupní objednávky** získáte rychlý přehled o stavu připravovaných nákupních objednávek. | Nepodporováno | Pracovní prostor **Příprava nákupní objednávky** nabízí přehledné zobrazení objednávek od chvíle, kdy byly vytvořeny jako koncept a bylo zahájeno jejich sledování, přes různé stavy workflowu až po potvrzení. | Pracovníci nákupního oddělení již nemusí vyhledávat informace na několika stránkách, protože přehled nyní získají na jednom pracovním prostoru. |
| Pomocí pracovního prostoru **Příjemka a zpracování nákupní objednávky** získáte rychlý přehled o nákupních objednávkách s čekající příjemkou a usnadníte si zpracování. | Nepodporováno | Pracovní prostor **Příjemka a zpracování nákupní objednávky** nabízí přehled o potvrzených nákupních objednávkách, které čekají na příjemku nebo dodávku. Na pracovním prostoru se nachází seznam příjemek po splatnosti a čekajících příjemkách, což usnadní aktivní kontrolu a zpracování ze strany dodavatele. Kromě toho je na pracovním prostoru také seznam nákupních objednávek, u kterých proběhla registrace doručení pro sklad, aby bylo zaručeno, že bude příjem zaúčtován. Vratky nákupních objednávek, které dosud nebyly expedovány, jsou k dispozici ke kontrole. | Pracovníci oddělení nákupu budou těžit z přehlednosti informací na pracovním prostoru. Relevantní informace jsou shromážděny a mohou pomoct se zpracováním a zvýšením produktivity. |
| Odeslat nákupní objednávky za účelem potvrzení na portál dodavatele hostovaný v klientovi aplikace Dynamics AX. Nechat dodavatele potvrdit nebo zamítnout. | Nepodporováno | Rozhraní portálu dodavatele umožňuje dodavatelům přijímat nákupní objednávky za účelem potvrzení nebo zamítnutí. Také dává dodavateli přehled o všech potvrzených nákupních objednávkách na účtu. Nákupčí může odeslat žádost o potvrzení nákupní objednávky ze strany dodavatele. Dodavatel musí být registrovaný uživatel Microsoft Azure Active Directory (Azure AD) v Dynamics AX, být kontaktní osobou dodavatele a mít vyhrazenou roli zabezpečení. | Pracovníkům nákupního oddělení se omezí papírování a ruční sledování odpovědí na nákupní objednávky, protože tyto odpovědi se vloží rovnou do systému. Jeden zdroj informací navíc sníží riziko nedorozumění mezi odběratelem a dodavatelem. |

## <a name="projects"></a>Projekty

| Co můžete udělat? | Dynamics AX 2012 | Dynamics AX 7.0 | Proč je to důležité? |
|------------------|------------------|-----------------|------------------------|
| Rezervovat pracovníky jako prostředky pro projekty. | Pracovníci se – podobně jako prostředky – rezervují přímo k projektům. | Tabulka Pracovní středisko, v níž se ukládají prostředky pro výrobu, může být nyní použita k rezervaci pracovníků jako prostředků pro projekt. | Při rezervaci projektů stačí rezervovat pouze prostředky. |

## <a name="retail-sales-marketing-and-customer-service"></a>Maloobchodní prodej, marketing a služby pro odběratele

### <a name="retail-hq"></a>Centrála pro maloobchod

Centrála pro maloobchod hostovaná v Microsoft Azure nabízí centrální správu a komplexní náhled na všechny aspekty obchodních operací prostřednictvím webového klienta.

<table>
<thead>
<tr>
<th>Co můžete udělat?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Proč je to důležité?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Provádět obchodní operace.</td>
<td>Ke správě následujících dat musí uživatelé používat několik formulářů:
<ul>
<li>Správa kategorií</li>
<li>Řízení produktu</li>
<li>Atributy produktu kanálu</li>
<li>Sortimenty</li>
<li>Správa katalogu</li>
<li>Sady</li>
<li>Ceny a slevy</li>
</ul></td>
<td>Pracovní prostor <strong>Správa kategorií a produktů</strong> disponuje těmito funkcemi:
<ul>
<li>Správa sortimentu.</li>
<li>Sledování životního cyklu sortimentu.</li>
<li>Správa uvolněných produktů.</li>
</ul>
Pracovní prostor <strong>Správa cen a slev</strong> disponuje těmito funkcemi:
<ul>
<li>Správa cen a slev pro daný kanál a kategorii.</li>
<li>Správa cenových pravidel kategorií.</li>
<li>Priority cen a slev, díky nimž lze přiřadit priority cenovým skupinám a slevám, čímž stanovíte, v jakém pořadí se použijí.</li>
<li>Správa umístění a katalogových slev.</li>
</ul>
Pracovní prostor <strong>Správa katalogu</strong> disponuje těmito funkcemi:
<ul>
<li>Souhrn aktivních katalogů.</li>
<li>Sledování životního cyklu katalogů na jednom místě.</li>
</ul></td>
<td><ul>
<li>Pracovní prostory zvyšují efektivitu a produktivitu pracovníků tím, že jim dávají možnost centrální správy úloh a akcí, které souvisejí s obchodovací rolí.</li>
<li>Funkce priorit cen a slev poskytuje zákazníkům větší kontrolu nad způsobem, jakým jsou ceny a slevy používány. Tato funkce umožňuje také nové scénáře, u nichž mají vyšší obchodní ceny přednost před standardními cenami.</li>
</ul></td>
</tr>
<tr>
<td>Spravovat nasazení maloobchodního kanálu a operací.</td>
<td>Při provádění následujících úloh musel uživatel používat několik formulářů:
<ul>
<li>Vytvoření a konfigurace nových kanálů a souvisejících entit.</li>
<li>Správa denních aktivit obchodu.</li>
<li>Zpracování maloobchodních transakcí v Microsoft Dynamics AX, generování výkazy maloobchodu a aktualizace zásob a finančních údajů Microsoft Dynamics AX.</li>
</ul>
</td>
<td>Na pracovním prostoru <strong>Nasazení kanálu</strong> můžete provádět tyto činnosti:
<ul>
<li>Vytvoření nových kanálů a souvisejících entit.</li>
<li>Sledování průběhu konfigurace maloobchodu.</li>
<li>Provádění kroků potřebných k dokončení úlohy nebo poskytnutí informací k dokončení úlohy.</li>
<li>Sledování stavu zařízení a přímé ověření a stažení instalace programu Retail Modern POS (MPOS) do obchodů.</li>
<li>Přístup ke všem souvisejícím stránkám.</li>
</ul>Na pracovním prostoru 
<strong>Maloobchod</strong> můžete provádět tyto činnosti:
<ul>
<li>Správa zaměstnanců a oprávnění k pokladním místům (POS) zaměstnanců.</li>
<li>Sledování stavu směny pro daný obchod nebo skupinu obchodů.</li>
<li>Přímé ověření a stažení instalačního programu MPOS v obchodech.</li>
<li>Tisk sestav a přístup k souvisejícím stránkám.</li>
</ul>Na pracovním prostoru 
<strong>Finance maloobchodu</strong> můžete provádět tyto činnosti:
<ul>
<li>Vytvoření, výpočet a zaúčtování výkazů pro daný kanál.</li>
<li>Plánování dávkových úloh pro aktualizaci zásob a výpočet a zaúčtování výkazů.</li>
<li>Sledování otevřených výkazů.</li>
<li>Sledování stavu směny pro daný obchod nebo skupinu obchodů.</li>
<li>Tisk sestav a rychlý přístup ke všem souvisejícím stránkám.</li>
</ul></td>
<td>Pracovní prostory zvyšují efektivitu a produktivitu pracovníků tím, že jim dávají možnost centrální správy většiny úloh a akcí, které souvisejí s nasazením kanálu, správou obchodu a financemi.</td>
</tr>
<tr>
<td>Správa IT operací pro maloobchod.</td>
<td>Uživatel musí použít několik formulářů.</td>
<td>V pracovním prostoru <strong>IT pro maloobchod</strong> lze na jednom místě pokládat dotazy Commerce Data Exchange pro daný kanál a provádět tak tyto úlohy:
<ul>
<li>Stahování relací.</li>
<li>Nahrávání relací.</li>
<li>Sledování relací, které selhaly, a jejich opětovně inicializování nebo spuštění.</li>
<li>Zobrazení nebo spuštění nadcházejících úloh.</li>
</ul></td>
<td>Pracovní prostory zvyšují efektivitu a produktivitu pracovníků tím, že jim dávají možnost centrální správy úloh a akcí, které souvisejí s IT operacemi pro maloobchod.</td>
</tr>
<tr>
<td>Importovat a exportovat data pomocí datových entit.</td>
<td>Aplikace AX 2012 podporuje migraci systému Microsoft Dynamics Retail Management System (RMS) prostřednictvím platformy importu a exportu dat.</td>
<td>K podpoře všech hlavních a referenčních dat souvisejících s maloobchodem byly rozšířeny datové entity maloobchodu. Také se zvýšila podpora pro datové entity napříč celým řešením Dynamics AX.</td>
<td>Datové entity umožňují odběratelům provádět import a export dat na základě metadat. Díky entitám OData mohou odběratelé také integrovat aplikaci Dynamics AX s aplikacemi třetích stran.</td>
</tr>
<tr>
<td>Provádět inteligentní analýzu pomocí sestav BI pro aplikaci Microsoft Dynamics AX a klienta POS.</td>
<td>K dispozici je více než 25 administrativních sestav a 5 sestav na straně kanálu.</td>
<td>K dispozici je více než 30 administrativních sestav a 10 sestav na straně kanálu.</td>
<td>S těmito sestavami budou mít odběratelé více BI k odhadnutí trendů, odhalení informací a udržení maximálního výkonu.</td>
</tr>
<tr>
<td>Analyzovat data prodeje přes maloobchodní kanály pomocí obsahu Power BI „Sledování výkonu maloobchodního kanálu“.</td>
<td>Není k dispozici.</td>
<td>Na stránce PowerBI.com vyberte možnost <strong>Načíst data</strong> a poté vyberte balíček obsahu <strong>Dynamics AX – výkonnost maloobchodního kanálu</strong>. Zadejte adresu URL koncového bodu Dynamics AX, aby se data zobrazovala na řídicím panelu.</td>
<td>Třemi až čtyřmi kliknutími mohou organizace nasadit do provozu řídicí panel Power BI obsahující důležitá finanční data. Obsah lze přizpůsobit podle požadavků organizace. Kromě toho mohou uživatelé vkládat dlaždice panelu Power BI na své vlastní pracovní prostory v aplikaci Dynamics AX, aby měli přehled o všech analytických informacích.</td>
</tr>
<tr>
<td>Konfigurovat oprávnění spotřebitelů.</td>
<td>Není k dispozici</td>
<td>Odběratelé mohou rozhodnout o tom, zda budou operace POS dostupné spotřebitelům. Server maloobchodu používá oprávnění pro volání aplikačního rozhraní (API).</td>
<td>Dává možnost konfigurace oprávnění na úrovni spotřebitele.</td>
</tr>
<tr>
<td>Spravovat a ověřovat konfigurace entit.</td>
<td>Není k dispozici.</td>
<td>Správce a validátor konfigurací umožňují tyto funkce:
<ul>
<li>Hromadné nahrání konfiguračních dat</li>
<li>Ověření obchodních entit</li>
</ul></td>
<td>Dává možnost spuštění konfigurace a ověření stavu a úplnosti konfigurace pro různé prvky konfigurace.</td>
</tr>
</tbody>
</table>

### <a name="retail-hardware-station"></a>Hardwarová stanice pro maloobchod

| Co můžete udělat? | Dynamics AX 2012 | Dynamics AX 7.0 | Proč je to důležité? |
|------------------|------------------|-----------------|------------------------|
| Povolit zařízením POS, aby se připojila k periferním zařízením, jako jsou tiskárny, pokladní zásuvky nebo platební zařízení. | K určení používaných zařízení je použit profil hardwaru MPOS. | Přidaný profil hardwaru podporuje více různých typů hardwaru mezi jednotlivými stanicemi. Nový profil Hardwarová stanice podporuje jedinečné ID terminálu pro každou hardwarovou stanici při zpracování transakcí elektronického převodu peněžních prostředků (EFT). Podpora EFT byla sloučena do hardwarové stanice, aby se omezilo zapojení MPOS do zpracování plateb EFT. | Tím je dána větší flexibilita pro implementace. Také je tím zajištěno lepší zabezpečení a omezeno vystavování údajů o kreditní kartě. |

### <a name="retail-server-and-data-management"></a>Server maloobchodu a správa dat

Se serverem maloobchodu a správou dat mohou spotřebitelé a podniků vytvářet společné nákupní prostředí pro všechny kanály (online, obchody a kontaktní střediska).

<table>
<thead>
<tr>
<th>Co můžete udělat?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Proč je to důležité?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Připojit se k databázi služby Commerce Runtime (CRT), ve které jsou prostřednictvím služeb CRT ukládána obchodní data pro kanál.</td>
<td>Podporován standard OData V3.</td>
<td>Podporován standard OData V4.</td>
<td>Odběratelé si udrží krok se současnými standardy OData. Integrací mezi obchodními, mobilními a online kanály se také vytvoří robustní jednotné prostředí pro všechny kanály.</td>
</tr>
<tr>
<td>Podporovat Maloobchodní služby jako sadu služeb s možnostmi hostitele.</td>
<td>Aplikační rozhraní E-commerce není serverem maloobchodu podporováno.</td>
<td>Aplikační rozhraní E-commerce je nyní k dispozici prostřednictvím serveru maloobchodu a podporuje online scénáře.</td>
<td>K dispozici jsou hostované a škálovatelné služby e-commerce, které lze použít s online obchody třetích stran.</td>
</tr>
<tr>
<td>Přesun dat mezi záložní kanceláří Microsoft Dynamics AX a kanály pomocí Commerce Data Exchange.</td>
<td>Commerce Data Exchange je systém, který přenáší data mezi aplikací Microsoft Dynamics AX a maloobchodními kanály, jako jsou například online obchody nebo kamenné obchody. Další informace naleznete v tématu <a href="https://technet.microsoft.com/library/dn741440.aspx">Commerce Data Exchange [AX 2012]</a>.</td>
<td>Funkční parita s Microsoft Dynamics AX 2012 CU8. Upozorňujeme však na tyto skutečnosti:
<ul>
<li>Služba Commerce Data Exchange byla přepracována pro cloud.</li>
<li>Asynchronní služba používá přímý přístup k databázi kanálu.</li>
<li>Commerce Data Exchange: služba v reálném čase je hostovaná jako vlastní služba Microsoft Dynamics AX.</li>
<li>MPOS spravuje synchronizaci mezi offline databázemi a serverem maloobchodu.</li>
</ul></td>
<td>Služba Commerce Data Exchange byla přepracována pro cloudovou platformu. I nadále spravuje přenos dat mezi aplikací Microsoft Dynamics AX a maloobchodními kanály, jako jsou například online obchody nebo kamenné obchody.</td>
</tr>
<tr>
<td>Podporovat připojitelné polointegrované zpracování plateb mezi kanály pomocí plateb SDK.</td>
<td>AX 2012 nabízí tyto funkce:
<ul>
<li>Podpora pro všechny kanály: POS, e-commerce a kontaktní střediska.</li>
<li>Podpora transakcí s kartou i bez karty.</li>
<li>Stránka pro přijetí plateb.</li>
<li>Podpora periférií pro LS5300 a MX925 jako vzorový kód v doplňku Retail SDK.</li>
</ul></td>
<td>Aktuální verze aplikace Dynamics AX podporuje všechny stávající funkce kreditních/debetních karet v aplikaci Microsoft Dynamics AX pro Retail 2012 a čtyři nová rozšíření.</td>
<td>Odběratelé mohou díky tomu zpracovávat transakce kreditní nebo debetní karty pro platby.</td>
</tr>
<tr>
<td>Aktivovat zařízení pomocí účtu Microsoft (Microsoft Azure Active Directory (Azure AD)).</td>
<td>Není k dispozici.</td>
<td>K dispozici jsou tyto funkce:
<ul>
<li>Zdokonalené zabezpečení prostřednictvím aktivace na základě Azure AD pro cloud</li>
<li>Zdokonalené zabezpečení pro správu tokenů.</li>
<li>Vylepšení spolehlivosti, řešení potíží a chybových zpráv při aktivaci</li>
<li>Zjednodušené IT administrativní úlohy vztahující se k aktivaci.</li>
<li>Přepracovaný model hrozeb a vyřešené problémy se zabezpečením.</li>
</ul></td>
<td>Přináší to tyto výhody:
<ul>
<li>Zdokonalené zabezpečení díky Azure AD a tokenu/ID zařízení (volání RS používají token, úložiště aplikace specifické pro uživatele).</li>
<li>Zastavení neoprávněného vzdáleného použití MPOS (zařízení brick).</li>
<li>Sledování zařízení MPOS pro účely kompatibility PCI.</li>
<li>Mapování fyzických zařízení s podnikovou entitou (registrací) pomocí tokenu zařízení.</li>
<li>Inicializace nastavení pro plynulý průběh funkcí MPOS (číselné řady a profily hardwaru) jako prvního kontaktu MPOS.</li>
<li>Hlášení informací o zařízení z centrály.</li>
</ul></td>
</tr>
<tr>
<td>Správa bohatého mediálního obsahu pro vytváření a obsluhování pomocí galerie médií.</td>
<td>Není k dispozici.</td>
<td><ul>
<li>Podpora nahrávání, zobrazování, správy a odstraňování obrázků v Galerii médií pro externě hostované obrázky i obrázky hostované v maloobchodu.</li>
<li>Podpora nahrávání obrázků a jejich prohlížení na stránce entit (<strong>Produkty</strong>, <strong>Katalogy</strong> atd.) propojením obrázku z galerie a jeho nahráním z počítače.</li>
<li>Optimalizace obrázků pro miniatury, vlastní velikosti a původní velikosti.</li>
<li>Hromadné entity odkazů pomocí šablony a úloh na pozadí pro hromadné přiřazování.</li>
<li>Integrace s aplikací Microsoft Excel přepisuje omezení skupin atributů konvencí pojmenovávání a předdefinovaných cest.</li>
<li>Podpora offline obrázků a zabezpečených obrázků pro obsah s osobními údaji (PII), jako například obrázky zaměstnanců a odběratelů hostovaných v maloobchodu.</li>
</ul></td>
<td><ul>
<li>Reaguje na slabiny v oblasti externě hostovaných obrázků, takže se vyhnete přechodům tam a zpět a můžete místo toho spravovat vše na jednom místě.</li>
<li>Zajišťuje výkonnou správu obsahu prostřednictvím Galerie médií pro nahrané a externě hostované obrázky a také nabízí funkci filtrování, pomocí níž lze vyhledávat obrázky.</li>
<li>Můžete snadno vytvářet hromadná přidružení mezi externě hostovanými obrázky a entitami, jako jsou produkty a katalogy.</li>
<li>Podporuje úložiště pro obrázky hostované maloobchodem a integraci s aplikací Excel pro snadné aktualizace.</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="rich-clientele-experience"></a>Bohaté zkušenosti zákazníků

Maloobchod nabízí dokonalý mobilní zážitek kdekoliv, kdykoliv a na jakémkoliv zařízení. Tato funkce rozšiřuje možnosti nákupů a zlepšuje zkušenost s obchodem ve všech kanálech.

<table>
<thead>
<tr>
<th>Co můžete udělat?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Proč je to důležité?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prohledávat, procházet, vyhledávat nebo skenovat produkty, přidávat produkty do košíku, přijímat platby a kontrolovat pomocí intuitivního a bohatého uživatelského rozhraní na MPOS s podporou dotykového ovládání.</td>
<td>Aplikace AX 2012 disponuje těmito funkcemi:
<ul>
<li>Provádění prodeje, vratek a anulování.</li>
<li>Vytváření, úprava a výdej objednávek odběratele.</li>
<li>Provádění operací se směnou a zásuvkou.</li>
<li>Výdej a příjem objednávek a provádění inventury.</li>
<li>Zobrazení obchodních sestav.</li>
</ul></td>
<td>K dispozici je funkční parita s AX 2012 MPOS. Ta zahrnuje tyto funkce:
<ul>
<li>Vyhledávání odběratelů mezi obchody a kanály.</li>
<li>Možnost vytvoření objednávky odběratele bez nutnosti využití služby v reálném čase.</li>
<li>Zdokonalené workflowy aktivace zařízení, stavy a chybové zprávy.</li>
<li>Vylepšení rozšiřitelnosti, jako například aktivátory předběžného zaúčtování nebo podpora aktivit pro zvýšení možností přizpůsobení.</li>
</ul></td>
<td>Prodavači mohou zpracovávat prodejní transakce a objednávky odběratelů a provádět každodenní operace a řízení zásob pomocí mobilního zařízení kdekoliv v obchodě.</td>
</tr>
<tr>
<td>Spuštění POS jako webové aplikace prostřednictvím cloudu POS.</td>
<td>Není k dispozici.</td>
<td>K dispozici je funkční parita s MPOS. Ta zahrnuje tyto funkce:
<ul>
<li>Aktivace zařízení pomocí AAD</li>
<li>Interaktivní rozvržení</li>
<li>Podpora prohlížečů Edge, Internet Explorer a Chrome.</li>
</ul></td>
<td>Poskytuje webovou aplikaci POS s funkcemi, které jsou kompatibilní s MPOS a které lze použít v různých platformách a prohlížečích s nulovými náklady na nasazení.</td>
</tr>
<tr>
<td>Integrace se systémem správy obsahu pro vytvoření internetových stránek e-commerce pro všechny kanály.</td>
<td>Jsou podporovány obchodní poutače aplikace Microsoft SharePoint a třetích stran.</td>
<td>Je k dispozici platforma e-commerce, která podporuje obchodní poutače třetích stran. Platforma zahrnuje tyto funkce:
<ul>
<li>Bohaté aplikační rozhraní pro spotřebitele.</li>
<li>Integrace ověřování do jakéhokoliv otevřeného ID řešení poskytovatele třetích stran.</li>
<li>Integrace plateb.</li>
</ul></td>
<td>Odběratelé mají nyní možnost použít libovolný systém správy obsahu.</td>
</tr>
<tr>
<td>Oslovit odběratele prostřednictvím katalogů poštovních objednávek a zefektivnit operace prostřednictvím rychlého zadání objednávky, asistovaného prodeje a plnění pomocí kontaktního střediska.</td>
<td><ul>
<li>Kanál kontaktního střediska</li>
<li>Katalogy poštovních objednávek</li>
<li>Rychlé zadání objednávky a asistovaný prodej</li>
<li>Zdokonalené plnění objednávky</li>
<li>Služby odběratele</li>
<li>Integrované oceňování a propagační akce / slevy</li>
</ul></td>
<td>K dispozici je funkční parita s řešením kontaktního střediska AX 2012 s výjimkou přepisů cen.</td>
<td>Kontaktní střediska jsou typem maloobchodního kanálu, ve kterém pracovníci mohou přijímat objednávky od odběratelů telefonicky a vytvářet prodejní objednávky.</td>
</tr>
</tbody>
</table>

### <a name="commerce-essentials"></a>Základy obchodování

Možnost konfigurace zaměřená na maloobchod a e-commerce zjednodušuje nasazení specifická pro maloobchod.

| Co můžete udělat? | Dynamics AX 2012 | Dynamics AX 7.0 | Proč je to důležité? |
|------------------|------------------|-----------------|------------------------|
| Použít řídicí panel Základy obchodování. | K dispozici je stránka s odkazy na položky nabídky. | Řídicí panel Základy obchodování obsahuje odkazy na často prováděné úkoly, včetně odkazů na pracovní prostory, webové ovládání Power BI, oblíbené položky, naposledy navštívené stránky a aktuální pracovní položky. | Zdokonalený řídicí panel pomáhá pracovníkům zvýšit efektivitu práce a nabízí jim flexibilní výchozí bod pro provádění jakéhokoliv úkolu v maloobchodu. |
| Použít datové entity k přístupu ke změnám v účtu. | Změny v účtu jsou exportovány do složky v systému souborů. | Změny v účtu jsou přístupné pomocí datových entit. | Tato funkce nabízí větší flexibilitu při přesunu dat mezi různými systémy. Tuto funkci lze vylepšit také prostřednictvím aplikací OData. |
| Použít cloudový POS a MPOS. | Okamžitou podporu má pouze podnikový POS (EPOS). | MPOS a cloudový POS nahrazují klienta EPOS. Ve výchozím nastavení byl do Základů obchodování přidán také kanál eCommerce. | Tato funkce umožňuje větší přímou podporu kanálu s možností rychlého nasazení klientů prodejních míst. |
| Implementovat a udržovat dvouvrstvou architekturu. | Platforma importu a exportu dat umožňuje přesun dat mezi aplikací AX 2012 a systémy třetích stran. | Jsou vytvářeny datové entity pro lepší podporu dvouvrstvé architektury. | Datové entity a aplikace OData zajišťují abstraktní vrstvu, která usnadňuje implementaci a udržování scénářů se dvěma vrstvami. |
| Zjednodušit formuláře. | Zjednodušení uživatelského rozhraní vyžaduje vlastní kód. | Rozšíření formulářů a nabídek zajišťují zjednodušení standardizovaného uživatelského rozhraní. | Tato funkce umožňuje rychlejší a snadnější optimalizaci formulářů podle potřeb daného prodejce. |

### <a name="pos-task-recorder"></a>Záznamník úkolů POS

<table>
<thead>
<tr>
<th>Co můžete udělat?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Proč je to důležité?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Vytvořit a sdílet průvodce úkolem a dokumenty pro moderní POS.</td>
<td>Není k dispozici.</td>
<td>Záznamník úkolů MPOS podporuje tyto funkce:
<ul>
<li>Vytvoření záznamů úkolů pro různé úkoly provádění v MPOS.</li>
<li>Generování dokumentu obsahujícího kroky a snímky obrazovky a jeho přidružení k uzlu v modelu obchodního procesu.</li>
</ul></td>
<td>Partneři a nezávislí dodavatelé softwaru (ISV) si mohou přizpůsobit MPOS a poskytnout podpůrné dokumenty pro zaškolení uživatelů.</td>
</tr>
</tbody>
</table>

### <a name="extensibility"></a>Rozšiřitelnost

<table>
<thead>
<tr>
<th>Co můžete udělat?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Proč je to důležité?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Podporovat rozšířitelné a snadno nasaditelné maloobchodní komponenty mezi ústřednou, kontaktním střediskem, e-commerce a POS.</td>
<td>Komponenty lze rozšířit pomocí doplňku Retail SDK. Nejsou podporovány žádné možnosti balení a nasazení.</td>
<td>Byla vylepšena připojitelnost rozšíření v různých komponentách, aby byla lépe podporována izolace a udržovatelnost kódu. Zde je přehled některých zahrnutých funkcí:
<ul>
<li>Workflow, aktivita a operace.</li>
<li>Předběžné a následné aktivační události, kterými lze snadno rozšířit workflow.</li>
<li>Aktivace a provozní aktivační události.</li>
</ul>
Kromě toho je k dispozici architektura, s níž můžete sestavovat a balit tyto součásti pomocí aplikace MSBuild a poté své přizpůsobení bez problémů nasadit prostřednictvím Microsoft Dynamics Lifecycle Services (LCS).</td>
<td>Maloobchodní prodejci mají velmi specifické požadavky založené na vertikálech a geografické oblasti činnosti. Poskytnutím snadno rozšířitelné platformy umožňujeme použití mezi různými vertikály a trhy. Vzhledem k tomu, že maloobchod má velmi distribuovanou architekturu, možnost snadného nasazení výrazně zvyšuje produktivitu.</td>
</tr>
</tbody>
</table>

### <a name="lifecycle-management"></a>Správa životního cyklu

Lifecycle Services (LCS) obsahuje sadu služeb, kterou mohou odběratelé a partneři použít ke správě životního cyklu systému od registrace až po každodenní operace.

<table>
<thead>
<tr>
<th>Co můžete udělat?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Proč je to důležité?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Spravovat program pomocí služeb pro nasazení cloudu.</td>
<td>Není k dispozici.</td>
<td>Do cloudu lze nasadit tyto topologie:
<ul>
<li>Zkušební topologie Retail 1-box.</li>
<li>Topologie s vysokou dostupností Retail multi-box.</li>
<li>Vývojářská topologie s doplňkem Retail SDK.</li>
</ul>
K dispozici je zlepšená instalace součásti zlepšení odlehčeného klienta prostřednictvím samoobslužné instalace:
<ul>
<li>Retail Modern POS.</li>
<li>Retail Hardware Station.</li>
<li>Podpora pro nahrávání a distribuci upravených balíčků prostřednictvím samoobslužné instalace.</li>
</ul></td>
<td>Služby nasazení cloudu nabízí tyto výhody:
<ul>
<li>Výrazně usnadnění nasazení a zjednodušení komponent Centrály pro maloobchod.</li>
<li>Nativní nasazení do veřejného cloudu Microsoft Azure.</li>
<li>Vylepšená samoobslužná instalace komponent v obchodě pro snazší a intuitivnější konfiguraci</li>
</ul></td>
</tr>
<tr>
<td>Sledovat stav systému a určit příčiny chyb a potíží.</td>
<td>Tato funkce vyžaduje balíček <a href="https://www.microsoft.com/download/details.aspx?id=42636">System Center 2012 Management Pack for Microsoft Dynamics AX 2012 R3 CU8 Retail</a>.</td>
<td>Sledování a diagnostika pro součásti maloobchodu jsou nyní dostupné prostřednictvím řídicího panelu <strong>Provozní analytika</strong>v LCS.</td>
<td>Řídicí panel <strong>Provozní analytika</strong> je cloudový sledovací portál, díky kterému není potřeba instalovat infrastrukturu System Center Operations Manager (SCOM).</td>
</tr>
<tr>
<td>Samoobslužně vytvořit, konfigurovat, stáhnout a nainstalovat hardwarovou stanici pro maloobchod a zařízení.</td>
<td>Pomocí instalačního balíčkovače a podnikového portálu může uživatel provádět automatickou instalaci a konfiguraci všech komponent, které jsou podle definované topologie potřeba v určitém počítači.</td>
<td>Vzhledem k tomu, že k dispozici jsou pouze dva instalace balíčky (jeden pro klienta MPOS a druhý pro komponentu hardwarové stanice pro maloobchod), omezila samoobslužná služba množství práce, kterou je nutné vykonat při instalaci těchto komponent klienta na všech úrovních.</td>
<td>Cílem samoobslužné služby je minimalizovat požadavky a usnadnit uživateli instalaci.</td>
</tr>
</tbody>
</table>

## <a name="sales"></a>Prodej.

<table>
<thead>
<tr>
<th>Co můžete udělat?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Proč je to důležité?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Získat rychlý přehled alternativ doručení, když odběratelům slíbíte objednávky.</td>
<td>Pokud existují omezení dostupnosti produktu a pro jeden nebo více produktů na objednávce nelze splnit odběratelem požadované datum dodání, může být slíbení objednávky obtížným úkolem. Pokud chce zpracovatel objednávky najít alternativní možnosti, jak vyřešit potíže s dostupností a časem dodání tak, aby byl splněn termín požadovaný odběratelem, anebo nabídnout odběrateli takové řešení dodání, na které bude moci odběratel přistoupit a spolehnout se na něj, musí tento zpracovatel otevřít několik formulářů, z nichž každý obsahuje část z potřebných informací. Přesněji řečeno: na jednom formuláři se zobrazuje množství na skladě na různých pracovištích, na druhém formuláři se zobrazuje množství na skladě v mezipodnikovém nastavení, na třetím formuláři se zobrazuje nejdřívější datum dostupnosti pro jedno pracoviště/variantu současně a na čtvrtém se zobrazují objednávky dodávky. Uživatel tedy nemá jistotu, že zvážil všechny relevantní možnosti a že jednoduše nezvolil jedno z prvních řešení, které ovšem nemusí být optimální. Uživatelé se rovněž necítí produktivně, protože při procesu přislíbení objednávky dochází k četným přerušením kvůli otevírání a zavírání mnoha stránek a kombinování analýz a možností.</td>
<td>Podle stávajících algoritmů pro výpočet data dodání mají uživatelé s přislíbením objednávky na stránce <strong>Alternativní dodání </strong>lepší zkušenosti:
<ul>
<li>Konsolidace relevantních informací z více formulářů na jedno místo.</li>
<li>Nabídka „předdefinovaných“ balíčků alternativního dodání, jako je například kombinace pracoviště/skladu/varianty/transportního režimu na základě kritéria nejrychlejšího doručení (nejbližší dostupné datum), ze kterých si může uživatel vybrat.</li>
<li>Uživatel si může vybrat možnosti z rozhraní simulace a přenést je do řádku prodejní objednávky.</li>
</ul></td>
<td>Společnosti, které chtějí poskytovat kvalitní služby odběratelům a zároveň dodržovat strategii optimalizace zásob, musí být schopné slibovat objednávky spolehlivě a konkurenceschopně. Koneckonců, odběratelská firma potřebuje mít produkty dostupné včas. Stránka úlohy <strong>Alternativní dodání</strong> zrychluje a usnadňuje úlohu slíbení objednávky a také ji činí systematičtější díky tomu, že na jednom místě určí a doporučí nejlepší alternativní datum dodání objednávky.</td>
</tr>
</tbody>
</table>

## <a name="service-management"></a>Správa servisu

Nebyly přidány následující nové funkce.

## <a name="transportation-management"></a>Správa přepravy

Nebyly přidány následující nové funkce.

## <a name="travel-and-expense"></a>Cestovné a výdaje

Nebyly přidány následující nové funkce.

## <a name="warehouse-management"></a>Řízení skladu

| Co můžete udělat? | Dynamics AX 2012 | Dynamics AX 7.0 | Proč je to důležité? |
|------------------|------------------|-----------------|------------------------|
| Stáhnout, nainstalovat a nakonfigurovat Portál skladu pro mobilní zařízení. | Portál můžete stáhnout, nainstalovat a nakonfigurovat při instalaci aplikace Microsoft Dynamics AX pomocí standardního nastavení. Je navržen pro místní nasazení a konfiguraci vlastními silami. | Prostřednictvím položky nabídky v modulu Řízení skladu si můžete stáhnout samostatný instalační program. Je navržen pro místní nasazení a konfiguraci vlastními silami. | Pokud nastavíte možnost použití funkce mobilního zařízení, je nutné Portál skladu pro mobilní zařízení nainstalovat a nakonfigurovat místně a připojit se k aplikaci Dynamics AX v cloudu. |

## <a name="additional-resources"></a>Další prostředky

[Co je nového a co se změnilo](whats-new-changed.md)

[Nový průvodce úkolem je k dispozici (únor 2016)](new-task-guides-available-february-2016.md)
