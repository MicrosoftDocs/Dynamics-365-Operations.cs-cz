---
title: "Přehled správy kvality"
description: "Tento článek popisuje, jak lze použít správu kvality v aplikaci Microsoft Dynamics 365 for Finance and Operations ke zlepšení kvality produktů v rámci dodavatelsko-odběratelského řetězce."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: c2c7a9c82809bd989eb362995dfe8e6d7829e89d
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---

# <a name="quality-management-overview"></a>Přehled správy kvality

[!include[banner](../includes/banner.md)]


Tento článek popisuje, jak lze použít správu kvality v aplikaci Microsoft Dynamics 365 for Finance and Operations ke zlepšení kvality produktů v rámci dodavatelsko-odběratelského řetězce.

Správa kvality pomáhá se správou doby oběhu objednávky při zpracování nevyhovujících produktů bez ohledu na místo jejich původu. Vzhledem k tomu, že typy diagnostiky jsou propojeny s hlášením oprav, aplikace Microsoft Dynamics 365 for Finance and Operations může naplánovat úlohy k nápravě problémů a zabránění jejich opakování.

Kromě funkcí pro správu neshod obsahuje moduly správy kvality také funkce pro sledování problémů podle jejich typu (včetně interních potíží) a pro určování krátkodobých a dlouhodobých řešení. Statistické údaje o klíčových ukazatelů výkonnosti (KPI) nabízí náhled na historii předchozích potíží s neshodami a řešení, která byla použita k jejich nápravě. Historická data můžete použít ke kontrole účinnosti předchozích opatření pro zajištění kvality a k rozhodnutí o tom, zda tato opatření použít i v budoucnu.

Při nastavování přidružení kvality může aplikace Finance and Operations vygenerovat objednávky kvality pro různé obchodní procesy, události a podmínky. Přiřazení kvality může zahrnovat určitou položku, určitou skupinu položek nebo všechny položky.

## <a name="examples-of-the-use-of-quality-management"></a>Příklady použití správy kvality
Správa kvality je flexibilní a lze ji implementovat různými způsoby, aby byly splněny požadavky konkrétních úrovní operací dodavatelsko-odběratelského řetězce. V následujících příkladech jsou znázorněna možná použití těchto funkcí:

-   Automatické spuštění procesu řízení kvality na základě předem definovaných kritérií (při registraci nákupní objednávky od konkrétního dodavatele ve skladu).
-   Blokování zásob při inventuře zabraňuje použití neschválených zásob (úplné blokování množství nákupní objednávky).
-   Použití vzorkování jako součásti přidružení k definici množství aktuálních fyzických zásob, které je nutné zkontrolovat. Vzorkování může být založeno na pevném množství nebo na procentuální hodnotě. 
-   Vytvořte objednávky kvality pro částečné příjmy. Abyste mohli vytvořit objednávku kvality, která je založena na množství fyzicky přijatém s objednávkou, je nutné zaškrtnout políčko **Na aktualizované množství** ve formuláři **Vzorkování položky**. 
-   Vytvoření typů testu, které zahrnují minimální, maximální a cílové hodnoty testu, a vykonání testu kvality vůči množství s předdefinovanými ověřovacími výsledky.
-   Určení přijatelné úrovně kvality (AQL) pro řízení odchylek měření kvality.
-   Určení zdrojů vyžadovaných operací kontroly, jako je například prostor testu nebo testovací přístroje.

## <a name="working-with-quality-associations"></a>Práce s přidruženími kvality
Obchodní proces, který používá přidružení kvality, může být přiřazen k různým zdrojovým dokumentům, jako například k nákupním objednávkám, prodejním objednávkám nebo výrobním zakázkám. 

Každý záznam o přidružení kvality určuje sadu testů, přijatelnou úroveň kvality a plán vzorkování, které platí pro vygenerované objednávky kvality. Je nutné definovat záznam o přidružení kvality pro každou variantu v obchodním procesu. Můžete například nastavit přidružení kvality, které vygeneruje objednávku kvality při aktualizaci příjemky produktu nákupní objednávky. V závislosti na nastavení plánu provedení může být samotný spouštěcí proces blokován, dokud existuje otevřená objednávka kvality, nebo mohou být blokovány další procesy, jako například fakturování nákupní objednávky. 

**Poznámka:** Pokud existují otevřené objednávky kvality, skladová množství jsou automaticky blokována před vydáním. V závislosti na nastavení **Úplné blokování** na stránce **Vzorkování položky** se množství rovná buď množství na objednávce kvality, nebo množství na řádku zdrojového dokumentu. 

Pro určitý obchodní proces určuje záznam o přidružení kvality událost a podmínky, pro které je objednávka kvality generována. Podmínky mohou být specifické buď pro pracoviště, nebo pro právnickou osobu. Objednávku kvality, která zahrnuje destrukční testy, je možné generovat, jen když pro tuto událost existují zásoby. 

Následující příklady ilustrují způsob definování záznamu o přidružení kvality pro varianty každého obchodního procesu. Pro každý příklad jsou v následující tabulce shrnuty události a podmínky, kterou jsou definovány v záznamu o přidružení kvality.

<table>
<tbody>
<tr>
<th>Typ odkazu</th>
<th>Typ události</th>
<th>Spuštění</th>
<th>Blokování události</th>
<th>Odkaz na dokument</th>
</tr>
<tr>
<td>Zásoby</td>
<td>Nelze použít</td>
<td>Nelze použít</td>
<td>Žádné</td>
<td>Vše</td>
</tr>
<tr>
<td rowspan="7">Prodeje</td>
<td rowspan="4">Proces vyskladnění je naplánován.</td>
<td rowspan="4">Před</td>
<td>Žádné</td>
<td rowspan="22">Specifické ID, Skupina nebo Vše</td>
</tr>
<tr>
<td>Proces vyskladnění</td>
</tr>
<tr>
<td>Dodací list</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="3">Dodací list</td>
<td rowspan="3">Před</td>
<td>Žádné</td>
</tr>
<tr>
<td>Dodací list</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="15">Nákup</td>
<td rowspan="7">Příjemka</td>
<td rowspan="4">Před</td>
<td>Žádné</td>
</tr>
<tr>
<td>Příjemka</td>
</tr>
<tr>
<td>Příjemka produktu</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="3">Po</td>
<td>Žádné</td>
</tr>
<tr>
<td>Příjemka produktu</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="3">Registrace</td>
<td rowspan="3">Nelze použít</td>
<td>Žádné</td>
</tr>
<tr>
<td>Příjemka produktu</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="5">Příjemka produktu</td>
<td rowspan="3">Před</td>
<td>Žádné</td>
</tr>
<tr>
<td>Příjemka produktu</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="2">Po</td>
<td>Žádné</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="8">Výroba</td>
<td rowspan="3">Registrace</td>
<td rowspan="3">Nelze použít</td>
<td>Žádné</td>
<td rowspan="12">Vše</td>
</tr>
<tr>
<td>Ohlásit jako dokončené</td>
</tr>
<tr>
<td>Konec</td>
</tr>
<tr>
<td rowspan="5">Ohlásit jako dokončené</td>
<td rowspan="3">Před</td>
<td>Žádné</td>
</tr>
<tr>
<td>Ohlásit jako dokončené</td>
</tr>
<tr>
<td>Konec</td>
</tr>
<tr>
<td rowspan="2">Po</td>
<td>Žádné</td>
</tr>
<tr>
<td>Konec</td>
</tr>
<tr>
<td rowspan="4">Karanténa</td>
<td rowspan="3">Ohlásit jako dokončené</td>
<td rowspan="2">Před</td>
<td>Ohlásit jako dokončené</td>
</tr>
<tr>
<td>Konec</td>
</tr>
<tr>
<td>Po</td>
<td>Konec</td>
</tr>
<tr>
<td>Konec</td>
<td>Před</td>
<td>Konec</td>
</tr>
<tr>
<td rowspan="3">Operace postupu</td>
<td rowspan="3">Ohlásit jako dokončené</td>
<td rowspan="2">Před</td>
<td>Žádné</td>
<td rowspan="3">Specifické ID, Skupina nebo Vše a Podle prostředku, Skupina nebo Vše</td>
</tr>
<tr>
<td>Ohlásit jako dokončené</td>
</tr>
<tr>
<td>Po</td>
<td>Žádné</td>
</tr>
<tr>
<td rowspan="3">Výroba vedlejších produktů</td>
<td>Registrace</td>
<td>Nelze použít</td>
<td rowspan="3">Žádné</td>
<td rowspan="3">Vše</td>
</tr>
<tr>
<td rowspan="2">Ohlásit jako dokončené</td>
<td>Před</td>
</tr>
<tr>
<td>Po</td>
</tr>
</tbody>
</table>

V následující tabulce jsou uvedeny další informace o způsobu, jak lze generovat objednávky kvality pro určité typy procesů.
<div class="tableSection">

<table>
<tbody>
<tr>
<th>Typ procesu</th>
<th>Kdy lze objednávku kvality generovat automaticky</th>
<th>Kdy lze objednávku kvality generovat v případě, že je vyžadován destrukční test</th>
<th>Informace o podmínkách</th>
<th>Informace o ručním generování</th>
</tr>
<tr>
<td>Nákupní objednávka</td>
<td>Před tím nebo po tom, co je příjemka produktu pro přijatý materiál zaúčtována</td>
<td>Po tom, co je příjemka produktu pro přijatý materiál zaúčtována, protože materiál musí být k dispozici pro destrukční testy</td>
<td>Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky, dodavatele nebo kombinace těchto podmínek.</td>
<td>Ručně vygenerovaná objednávka kvality, která odkazuje na nákupní objednávku, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</td>
</tr>
<tr>
<td>Karanténní příkaz</td>
<td>Před tím nebo po tom, co je karanténní příkaz vykázán jako dokončený nebo ukončený</td>
<td>Objednávky kvality, které vyžadují provedení destrukčních testů, nelze generovat. Předpokládá se, že funkce karanténního příkazu zpracovává likvidaci materiálu, který je zničen.</td>
<td>Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky, dodavatele nebo kombinace těchto podmínek.</td>
<td>Ručně vygenerovaná objednávka kvality, která odkazuje na karanténní příkaz, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</td>
</tr>
<tr>
<td>Prodejní objednávka</td>
<td>Před naplánovaným procesem vyskladnění nebo aktualizací dodacího listu pro položky, které byly právě dodány</td>
<td>Při jakémkoli kroku</td>
<td>Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky, odběratele nebo kombinace těchto podmínek.</td>
<td>Ručně vygenerovaná objednávka kvality, která odkazuje na prodejní objednávku, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</td>
</tr>
<tr>
<td>Výrobní zakázka</td>
<td>Před tím nebo po tom, co je vykázáno dokončené množství pro výrobní zakázku</td>
<td>Po tom, co je vykázáno dokončené množství pro výrobní zakázku</td>
<td>Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky nebo kombinace těchto podmínek.</td>
<td>Ručně vygenerovaná objednávka kvality, která odkazuje na výrobní zakázku, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</td>
</tr>
<tr>
<td>Výrobní zakázka s operací postupu</td>
<td>Před tím nebo po tom, co je dokončeno ohlášení pro operaci</td>
<td>Po tom, co je pro poslední operaci dokončeno ohlášení výrobní zakázky</td>
<td>Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky, provozního prostředku nebo kombinace těchto podmínek.</td>
<td>Ručně vygenerovaná objednávka kvality, která odkazuje na operaci postupu, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</td>
</tr>
<tr>
<td>Zásoby</td>
<td>Objednávku kvality nelze automaticky generovat pro transakci v deníku zásob ani pro transakce převodních příkazů.</td>
<td></td>
<td></td>
<td>Objednávku kvality je možné vytvořit ručně pro množství položky na skladě. Jsou vyžadovány fyzické zásoby na skladě.</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a>Stránky modulu Správa kvality
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Strana</th>
<th>Popis</th>
<th>Příklad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Přiřazení kvality</td>
<td>Přečtěte si předchozí část tohoto článku.</td>
<td>Přidružení kvality určuje pro vygenerovanou objednávku kvality tyto informace:
<ul>
<li>Událost transakce</li>
<li>Sada testů, které je nutné u položky vykonat</li>
<li>Přijatelná úroveň kvality</li>
<li>Plán vzorkování</li>
</ul>
Přiřazení kvality je nutné definovat pro každou variantu obchodního procesu, který vyžaduje automatické generování objednávky kvality. Objednávky kvality lze generovat například v obchodních procesech pro nákupní objednávky, karanténní příkazy, prodejní objednávky a výrobní zakázky.</td>
</tr>
<tr class="even">
<td>Testy</td>
<td>Tuto stránku použijte k definování a prohlížení individuálních testů, které zjišťují, zda vaše produkty splňují specifikace kvality. Ke skupině testů můžete přiřadit jeden nebo více individuálních testů. V tomto případě zadáte také informace specifické pro daný test, jako jsou například přijatelné hodnoty měření. Hodnoty měření se používají k testování množství a testovací proměnné slouží pro testy kvality.
<ul>
<li>Kvantitativní test má typ testu <strong>Celé číslo</strong> nebo <strong>Zlomek</strong> a také má určenou měrnou jednotku. Specifikace kvality a výsledky testu jsou vyjádřeny jako čísla.</li>
<li>V případě testu kvality se jedná o test typu <strong>Parametr</strong>. Testy kvality vyžadují další informace o měřených testovacích proměnných a o výčtu jejich hodnot. Specifikace kvality a výsledky testu jsou vyjádřeny v závislosti na výstupu.</li>
</ul></td>
<td>Výrobní společnost provádí dva testy na zakoupeném materiálu: kvantitativní test ohledně kvality materiálu a test kvality ohledně poškození balení. Tato společnost definuje další informace ohledně kvalitativního testu s cílem identifikovat testovací proměnnou (poškozené balení) a její výstupní hodnoty. Společnost používá stránku <strong>Testovací skupiny</strong> k přiřazení dvou testů do skupiny testů a k určení informací o daném testu. Testovací skupina je přiřazena k objednávce kvality, takže daná společnost může vytvořit sestavu pro dané dva testy.</td>
</tr>
<tr class="odd">
<td>Testovací skupiny</td>
<td>Tato stránka slouží k nastavení, úpravě a zobrazení testovacích skupin a jednotlivých testů přiřazených testovací skupině. V horním podokně jsou zobrazeny testovací skupiny a v dolním podokně jsou zobrazeny testy, které jsou přiřazené vybrané testovací skupině. Každé testovací skupině můžete přiřadit několik zásad, jako například plán vzorkování, přijatelnou úroveň kvality a požadavek na destrukční testy. Při přiřazení jednotlivého testu do skupiny testů definujete další informace, jako jsou například pořadí, dokumenty nebo data platnosti. Pro kvantitativní test definujete také informace o přijatelných hodnotách měření. Informace o testu kvality obsahují také testovací proměnné a výchozí výstup. Skupina testů přiřazená objednávce kvality určuje výchozí sadu testů, které je nutné na určených položkách vykonat. Testy však můžete přidat, odstranit nebo změnit na objednávce kvality. Výsledky testu jsou uvedeny pro všechny testy v objednávce kvality.</td>
<td>Výrobní společnost má definované testovací skupiny pro každou variantu pokynů týkajících se kvality. Různé testovací skupiny odrážejí rozdíly v plánech vzorkování, v sadách testů, které je nutné provádět dohromady, v přijatelné úrovni kvality i v dalších činitelích. Pro kvantitativní testy existují také rozdíly v přijatelných hodnotách měření. K uplatnění pokynů týkajících se kvality přiřadí společnost na stránce <strong>Přidružení kvality</strong> každé testovací skupině pravidlo automatického generování objednávek kvality a také přiřadí skupiny testů k objednávce kvality, který byla vytvořena ručně.</td>
</tr>
<tr class="even">
<td>Skupiny kvality položek</td>
<td>Tato stránka slouží k nastavení, úpravě a zobrazení položek zařazených do skupin kvality, které jsou přiřazeny položce. Skupina kvality představuje společné požadavky na testování položek. Po určení požadavků na testování na stránce <strong>Testovací skupiny</strong> můžete definovat pravidla pro automatické generování objednávek kvality. Proces můžete zjednodušit tak, že nebudete definovat pravidla pro jednotlivé položky. Namísto toho na stránce <strong>Přidružení kvality</strong> určíte pravidla pro skupinu kvality. Pro vybranou skupinu kvality můžete také použít stránku <strong>Skupiny kvality položek</strong> a přiřadit k této skupině příslušné položky. Pro vybranou položku můžete také použít stránku <strong>Skupiny kvality položek</strong> a přiřadit příslušnou skupiny kvality příslušné položce.</td>
<td>Výrobní společnost nakupuje různé suroviny, které při vstupní kontrole podléhají stejným požadavkům na testování. Společnost definuje skupinu kvality a přiřadí čísla položek, které jsou přidruženy k surovinám, do této skupiny. Později společnosti zakoupí nový typ suroviny, který má stejné požadavky na testování. Namísto vytvoření nových požadavků na testování pro nový materiál společnost přidá číslo položky pro nový materiál do stávající skupiny kvality. Stejná výrobní společnost vyrábí také položky, na které jsou kladeny stejné požadavky na testování, a expeduje položky, které před odesláním podléhají stejné kontrole. Společnost definuje další dvě skupiny kvality a do každé skupiny zařadí příslušné položky.</td>
</tr>
<tr class="odd">
<td>Testovací proměnné</td>
<td>Tato stránka slouží k určení a zobrazení proměnných spojených s testem kvality. Pro každou proměnnou určete výčet výstupních hodnot, které reprezentují možné volby. Na stránce <strong>Testy</strong> určete testy. U testů kvality je nutné nastavit typ testu na hodnotu <strong>Možnost</strong>. Na stránce <strong>Testovací skupiny</strong> přiřaďte testovací proměnnou k jednotlivému testu.</td>
<td>Společnost vyrábějící cukrovinky používá kontrolní test pro dokončené výrobky. Kontrolní test má několik proměnných. Jedna proměnná odpovídá chuti, přičemž možné výstupní hodnoty pro tuto proměnnou jsou „dobrá“ a „špatná“. Druhá proměnná odpovídá barvě, přičemž možní výstupní hodnoty jsou „příliš tmavá“, „příliš světlá“ a „správná“.</td>
</tr>
<tr class="even">
<td>Výsledky testovacích proměnných</td>
<td>Na této stránce lze nastavit, upravit nebo zobrazit možné výsledky testů pro testovací proměnnou, která je přidružena k testu kvality. Každé výstupní hodnotě přiřadíte stav <strong>úspěch</strong> nebo <strong>neúspěch</strong>. Pro každý test kvality definovaný na stránce <strong>Testy</strong> je nutné definovat proměnnou a její výstupní hodnoty. (U kvalitativních testů je typ testu nastaven na <strong>Volba</strong> na stránce <strong>Testy</strong>.) Pomocí stránky <strong>Skupiny testů</strong> přiřaďte proměnnou testu a výchozí výstup k samostatnému kvalitativnímu testu.</td>
<td>Společnost vyrábějící cukrovinky používá kontrolní test pro dokončené výrobky. Kontrolní test má několik proměnných. Jedna proměnná odpovídá chuti, přičemž možné výstupní hodnoty pro tuto proměnnou jsou „dobrá“ a „špatná“. Druhá proměnná odpovídá barvě, přičemž možní výstupní hodnoty jsou „příliš tmavá“, „příliš světlá“ a „správná“. Ke každé výstupní hodnotě je přiřazen stav <strong>úspěch</strong> nebo <strong>neúspěch</strong>. Během kontrolního testu pro každou proměnnou kontrolor ohlásí výsledky testu výběrem některé z výstupních hodnot.</td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Viz také
--------

[Procesy správy kvality](quality-management-processes.md)

[Povolení správy neshod](enable-nonconformance-management.md)




