---
title: Zpracování fakturace
description: Toto téma obsahuje informace o zpracování faktur pro východní Evropu.
author: v-kikozl
manager: AnnBe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, VendParameters
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia, Italy
ms.author: v-kikozl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 87a06e1b17e9c0bdb4147f49b2dacb74236360fa
ms.sourcegitcommit: f860ac2b18f6bbbfc4a46b497baec2477105b116
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/19/2020
ms.locfileid: "4407630"
---
# <a name="invoice-processing"></a>Zpracování fakturace

[!include [banner](../includes/banner.md)]

Toto téma stručně popisuje některé scénáře specifické pro určité země či oblasti, jako je například intrakomunitární daň z přidané hodnoty (DPH) a odložená daň. Právní požadavky pro některé evropské země mají vliv na proces fakturace. Toto téma poskytuje také informace o zpracování faktur odběratelů a dodavatelů pro tyto země. 
<table>
<thead>
<tr>
<th>Scénář</th>
<th>Země</th>
<th>Popis změn funkcí</th>
</tr>
</thead>
<tbody>
<tr>
<td> Data pohledávek a závazků pro DPH</td>
<td>Česká republika, Polsko</td>
<td>
<p>Při nákupu zboží ze zemí Evropské unie (EU) existuje povinnost vlastního vyměření DPH:</p>
<ul>
<li>DPH na výstupu musí být zaplacena v období DPH, kdy byla vystavena faktura (datum dokumentu).</li>
<li>DPH na vstupu nemůže být odečtena před přijetím dokumentu (datum registrace DPH).</li>
</ul>
<p>Pro podporu tohoto scénáře musí být nakonfigurována následující nastavení:</p>
<ul>
<li>Na stránce <strong>Parametry závazků</strong> povolte parametry <strong>DPH intrakomunitárního plnění</strong> a <strong>Datum dokumentu pro intrakomunitární DPH</strong>.</li>
<li>Nastavte dva kódy daně z přidané hodnoty: jeden, který má kladné procento daně z přidané hodnoty, a druhý, který má záporné procento daně z přidané hodnoty.</li>
<li>Nastavte skupinu daně z přidané hodnoty obsahující kladné i záporné kódy daně z přidané hodnoty. Pro záporný kód daně z přidané hodnoty nastavte parametr <strong>DPH intrakomunitárního plnění</strong> na <strong>Ano</strong>.</li>
</ul>
<p>Po úspěšném nastavení budou mít nákupy dvě zaúčtované transakce DPH:</p>
<ul>
<li>Pozitivní transakci, která má charakter <strong>pohledávky DPH</strong>, a datum registrace DPH, které je shodné s datem stránky zaúčtování faktury.</li>
<li>Negativní transakci, která má charakter <strong>závazku DPH</strong>, a datum registrace DPH, které je shodné s datem dokumentu.</li>
</ul>
</td>
</tr>
<tr>
<td>Změňte datum prodejního dokladu.</td>
<td>Všechny východoevropské země</td>
<td><p>Můžete změnit pole <strong>Datum dokladu</strong> na projektové faktuře. Toto datum se zobrazuje na vytištěné faktuře.</p>
<p>Na stránkách <strong>Zaúčtování faktury</strong> a <strong>Volná faktura</strong> existuje pole <strong>Datum dokumentu</strong>. Po zaúčtování faktury se datum dokumentu zobrazí v záhlaví faktury.</p>
</td>
</tr>
<tr>
<td>Datum dokumentu pro směnné kurzy</td>
<td>Polsko, Maďarsko, Česká republika, Itálie</td>
<td>
<p>Legislativa obsahuje různá pravidla pro výběr platných směnných kurzů pro obchodní transakce. V poli <strong>Datum směnného kurzu</strong> na stránkách <strong>Parametry pohledávek</strong> a <strong>Parametry závazků</strong> můžete vybrat datum, které má být použito pro částky ve výpočtu zúčtovací měny na nákupních a prodejních dokumentech. Při zadávání dat systém načte směnný kurz pro transakci na základě tohoto parametru.</p>
<blockquote>[!NOTE]<br>V Itálii je tato funkce použitelná pouze v modulu Závazky. V parametrech Závazků může uživatel vybrat <strong>Datum zaúčtování</strong> nebo <strong>Datum dokumentu</strong> v poli <strong>Datum směnného kurzu</strong>.   </blockquote>
<blockquote>[!NOTE]<br>Když nastavíte pole <strong>Datum směnného kurzu</strong> na <strong>Datum dokumentu (pouze pro obchod EU)</strong>, systém použije skupinu DPH. Pro skupinu DPH existuje parametr <strong>Obchod EU</strong> na kartě <strong>Hlavní</strong>. Pokud je možnost <strong>Obchod EU</strong> nastavena na <strong>Ano</strong> pro skupinu DPH a pokud je tato skupina DPH v záhlaví dokumentu, systém načte směnný kurz, který je založený na datu dokumentu. Pokud je možnost <strong>Obchod EU</strong> nastavena na <strong>Ne</strong> pro tuto skupinu DPH, systém načte směnný kurz podle data zaúčtování dokladu.</blockquote>
</td>
</tr>
<tr>
<td>Data obchodů, data registrace DPH a dokument a kontrol dat DPH</td>
<td>Polsko, Maďarsko, Česká republika,</td>
<td>
<p>Datum prodeje a datum příjmu dokumentu jsou povinné pro vykazování DPH:</p>
<ul>
<li>Datum prodeje je datum plnění transakce v pohledávkách.</li>
<li>Datum příjmu dokumentů je datum dokazující práva nárokovat odpočet DPH v závazcích. Každý dokument, který je přijat, obsahuje datum pro účely auditu.</li>
</ul>
<p>Maďarská funkce pro termíny dat, česká funkce pro data plnění a polská funkce pro datum registrace DPH obsahují požadavek na vykazování informace o dani, která je založena na datu lišícím se od data zaúčtování.</p>
<p>Pole <strong>Datum registrace DPH</strong> podporuje tento požadavek a zobrazuje se na více než 20 stránkách. Tyto stránky obsahují deníky, prodejní objednávky, nákupní objednávky, volné faktury, deníky faktur dodavatele a projektové faktury. Když aktualizujete nebo zaúčtujete dokumenty, všechny daně se zaúčtují pomocí příslušného data registrace DPH a toto datum bude obsaženo na stránkách, jako jsou například stránky deníků faktur odběratele a dodavatele.</p>
<p>Konkrétně pro Českou republiku pole <strong>Datum registrace DPH</strong> může být ponecháno při zaúčtování prázdné, v případě zaúčtování odložené DPH. V opačném případě je toto pole povinné a musí být vyplněno.</p>
<p>Lze nastavit parametry ověření data na stránce <strong>Skupiny DPH</strong>:</p>
<ul>
<li>Parametry <strong>Datum vyplnění registrace DPH</strong> a <strong>Vyplnění data prodeje</strong> se používají jako výchozí metoda pro vyplnění příslušných dat. K dispozici je rovněž ruční zadání a několik metod automatizovaného zadání.</li>
<li>Pole <strong>Povinné datum prodeje</strong> udává, zda je nutné zadat datum prodeje před zaúčtování prodejní faktury.</li>
</ul>
<p>Na stránce <strong>Transakce registru DPH</strong> můžete vyplnit prázdná data pro registr DPH pro zaúčtované daňové transakce.</p>
</td>
</tr>
<tr>
<td>Data registrace DPH, která zahrnují odloženou daň</td>
<td>Maďarsko</td>
<td>
<p>Maďarské daňové předpisy vyžadují, aby faktury byly vytvářeny buď v okamžiku plnění nebo ne později než 15 dnů po plnění.</p>
<p>Datum plnění je buď datum, kdy byly poskytnuty objednané služby, nebo datum, kdy byly dodány objednané položky. Při aktualizaci nebo zaúčtování dokladů se zaúčtují všechny daně s použitím odpovídajícího data registrace DPH a toto datum se zobrazí na příslušných stránkách. Dále právní předpisy vyžadují, aby DPH při souvislých dodávkách služeb, jako je například pronájem, leasing, konzultace a topení, splňovalo následující kritéria:</p>
<ul>
<li>DPH musí být zaúčtováno na vyhrazený účet hlavní knihy v datum fakturace.</li>
<li>DPH je nutné převést ze speciálních účtů na účet pohledávek DPH nebo na účet závazků a musí být zahrnuto do sestavy DPH v den splatnosti.</li>
</ul>
<p>Abyste splnili tyto požadavky, můžete převést zaúčtování do hlavní knihy na účet odložené příchozí daně a účet odchozí odložené daně. Musíte však nejprve dokončit následující předpoklady:</p>
<ul>
<li>Nastavte účty hlavní knihy pro odložené DPH závazky a pohledávky ve skupinách zaúčtování hlavní knihy.</li>
<li>Povolte parametr <strong>Odložená DPH</strong> pro skupiny DPH položky.</li>
</ul>
</td>
</tr>
<tr>
<td> Povinné datum DPH</td>
<td>Polsko</td>
<td>
<p>Můžete vyžadovat, aby datum registrace DPH bylo zahrnuto do záznamů transakcí nákupu a prodeje. Datum registrace DPH lze tedy zaznamenat před zaúčtováním transakce. Tato funkce umožňuje, že nemusíte pracovat s více transakcemi na konci období.</p>
<p>Můžete nastavit pole <strong>Datum registrace DPH</strong> jako povinné při zaúčtování transakcí odběratele nebo dodavatele. Chcete-li tak učinit, povolte možnost <strong>Datum DPH je požadováno</strong> pro související účet odběratele nebo dodavatele.</p>
</td>
</tr>
</tbody>
</table>
