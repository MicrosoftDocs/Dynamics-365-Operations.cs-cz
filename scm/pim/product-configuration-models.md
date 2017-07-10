---
title: "Přehled modelů konfigurace produktu"
description: "Tento článek definuje termíny a pojmy, které jsou relevantní pro modely konfigurace produktu. Modely konfigurace produktu umožňují vytvořit obecnou strukturu produktu, kterou lze použít ke konfiguraci mnoha variant produktu pro jeden produkt."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 4031
ms.assetid: 70b968e8-e550-4731-823d-d713b8910f7b
ms.search.region: Global
ms.author: yuyus
ms.dyn365.intro: Feb-16
ms.dyn365.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 1270c35bc7dbe4c85a1aa991a0387b33e1cb6990
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017


---

# <a name="product-configuration-models-overview"></a>Přehled modelů konfigurace produktu

[!include[banner](../includes/banner.md)]


Tento článek definuje termíny a pojmy, které jsou relevantní pro modely konfigurace produktu. Modely konfigurace produktu umožňují vytvořit obecnou strukturu produktu, kterou lze použít ke konfiguraci mnoha variant produktu pro jeden produkt.

Modely konfigurace produktu slouží pro reprezentaci obecné struktury produktů. Po nastavení modelu konfigurace produktu můžete nakonfigurovat jedinečnou variantu produktu s jedinečným kusovníkem (BOM) a jedinečným postupem. Modely konfigurace produktu využívají ke zpracování vztahů a omezení mezi různými variantami produktu jak deklarativní omezení, tak i příkazové výpočty . Je možné konfigurovat položky na prodejních objednávkách, prodejních nabídkách, nákupních objednávkách a výrobních zakázkách. V následující tabulce jsou termíny a koncepty popsány na základě omezení.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Součásti</td>
<td>Komponenty jsou hlavní stavební bloky modelu konfigurace produktu. Komponenty se zobrazují ve stromové struktuře na stránce <strong>Podrobnosti modelu produktu s konfigurací založenou na omezeních</strong>. Komponenty mohou obsahovat následující prvky:
<ul>
<li>Atributy</li>
<li>Omezení</li>
<li>Výpočty</li>
<li>Dílčí komponenty</li>
<li>Požadavky uživatele</li>
<li>Řádky kusovníku</li>
<li>Operace postupu</li>
</ul></td>
</tr>
<tr class="even">
<td>Atributy</td>
<td>Atributy popisují všechny funkce modelu konfigurace produktu. Atributy můžete použít k určení funkcí, které mohou být vybrány při konfiguraci jedinečného produktu. Atributy jsou používány pro omezení a podmínky. Při vytváření a přidávání atributů do modelu konfigurace produktu jsou vytvářeny odkazy na související typy atributů. Pro atribut lze nastavit výchozí hodnotu. Výchozí hodnota je použita při konfiguraci uživatelského rozhraní (UI), když je konfigurován model konfigurace produktu. Můžete určit, zda je atribut povinný, jen pro čtení nebo skrytý.
<ul>
<li><strong>Povinný</strong> – při konfiguraci produktu musí být pro atribut nastavena hodnota.</li>
<li><strong>Jen pro čtení</strong> – během relace konfigurace se hodnota atributu zobrazuje, nicméně nelze ji změnit.</li>
<li><strong>Skrytý</strong> – hodnota atributu je součástí omezení a podmínek, avšak během relace konfigurace se nezobrazuje.</li>
</ul>
Můžete také určit podmínky pro atributy. Pokud je podmínka splněna, musí být zadána hodnota pro povinný atribut. Podmínky jsou výrazy, které musí být splněny, aby byly atributy, řádky kusovníku a operace postupu zahrnuty v modelu konfigurace produktu. Všechny atributy, které jsou v podmínce zahrnuty, budou povinné. Doporučujeme, abyste povinné atributy vybírali na kartě <strong>Atributy</strong>. To usnadní identifikaci povinných atributů. Hodnoty atributů hrají důležitou roli při opakovaném použití konfigurací. Systém použije hodnoty atributů k určení, zda existuje konfigurace odpovídající volbám, které uživatel provedl během relace konfigurace.</td>
</tr>
<tr class="odd">
<td>Typy atributů</td>
<td>Typy atributu určují sadu datových typů atributů, které jsou použity v modelu konfigurace výrobku. Používány jsou následující typy atributů:
<ul>
<li><strong>Celé číslo</strong> s rozsahem nebo bez něj</li>
<li><strong>Des. místo</strong></li>
<li><strong>Text</strong> s pevným seznamem možností nebo bez něj</li>
<li><strong>Logická hodnota</strong></li>
</ul>
Pokud je typ atributu <strong>Logická hodnota</strong>, <strong>Celé číslo</strong> s rozsahem nebo <strong>Text</strong> s pevným seznamem, bude při nastavování konfigurace modelu produktu k dispozici množina hodnot. <strong>Poznámka:</strong> Řešitel konfigurace produktu rozpoznává pouze tyto typy atributů: <strong>Logická hodnota</strong>, <strong>Text</strong> s pevným seznamem a <strong>Celé číslo</strong> s rozsahem. Proto lze v omezeních a podmínkách výrazů použít pouze tyto typy atributů.</td>
</tr>
<tr class="even">
<td>Omezení</td>
<td>Omezení popisují limity konfigurace modelu produktu. Omezení slouží k zajištění toho, aby byly při konfiguraci produktu vybrány pouze platné hodnoty. Omezení může být omezení výrazů nebo omezení tabulek:
<ul>
<li>Omezení výrazů mohou být použita pouze pro komponentu, se kterou jsou svázány. Omezení výrazů pro komponentu se může odkazovat na atributy dílčích komponent dané komponenty. Řešitel konfigurace produktu slouží k vyřešení omezení. Při psaní omezení je třeba dodržovat syntaxi tohoto řešitele. Další informace naleznete v odkazu na téma věnované omezením výrazu a omezením tabulky.</li>
<li>Omezení tabulky musí být definována předtím, než je možné použít pro komponentu v modelu konfigurace produktu. Omezení tabulek mohou být definovaná uživatelem nebo systémem. Uživatelem definované omezení tabulky je typ matice, kterou lze použít k popisu sady kombinací hodnot atributů, které jsou definovány pomocí typů atributů. Například v případě výroby reproduktorů může matice pro uživatelem definované omezení tabulky obsahovat sloupce pro povrch a mřížku reproduktorů.</li>
</ul>
<strong>Příklad:</strong> Reproduktory jsou k dispozici se čtyřmi různými povrchy: černý, dub, palisandr nebo bílý. Reproduktory mohou mít jednu ze tří předních mřížek: černá, kov nebo bílá. Černé provedení je k dispozici pro všechny mřížky, ale ostatní materiály povrchové úpravy jsou omezeny na konkrétní mřížky. V následující tabulce je ukázka informace, které se zobrazí na kartě <strong>Povolené kombinace</strong> na stránce <strong>Upravit omezení tabulky</strong>.
<table>
<thead>
<tr class="header">
<th>Povrch skříňky</th>
<th>Přední mřížka</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Černá</td>
<td>Černá</td>
</tr>
<tr class="even">
<td>Černá</td>
<td>Kov</td>
</tr>
<tr class="odd">
<td>Černá</td>
<td>Bílá</td>
</tr>
<tr class="even">
<td>Dub</td>
<td>Černá</td>
</tr>
<tr class="odd">
<td>Palisandr</td>
<td>Bílá</td>
</tr>
<tr class="even">
<td>Bílá</td>
<td>Černá</td>
</tr>
<tr class="odd">
<td>Bílá</td>
<td>Bílá</td>
</tr>
</tbody>
</table>
Systémem definované omezení tabulek představuje mapování mezi typem atributu a polem v tabulce aplikace Finance and Operations. Omezení tabulky definované systémem dynamicky propojuje typ atributu s polem. Propojení umožňuje, aby atribut v modelu konfigurace produktu odrážel data v poli pro tabulku Finance and Operations.</td>
</tr>
<tr class="odd">
<td>Výpočty</td>
<td>Výpočty představují doplněk k omezením. Výpočet můžete použít k provedení aritmetické operace na atributech typu <strong>Desetinné číslo</strong> a <strong>Celé číslo</strong>nebo logických operací zahrnujících atributy typu <strong>Text</strong> s pevným seznamem a <strong>Logická hodnota</strong>. Výpočet má cílový atribut, do kterého bude zapsán výsledek výpočetního výrazu. Výpočetní výraz se vytváří pomocí editoru výrazu.</td>
</tr>
<tr class="even">
<td>Dílčí komponenty</td>
<td>Dílčí komponenty odrážejí stromovou strukturu modelu konfigurace produktu. Dílčí komponenty můžete použít k vybudování struktury modelu konfigurace produktu. Dílčí komponenty se odkazují na existující komponenty. Proto používání dílčích komponent podporuje opakované používání komponent ve více modelech konfigurace produktů. Na stránce <strong>Podrobnosti řádku kusovníku</strong> pro dílčí komponentu můžete vybrat různé hodnoty pro danou dílčí komponentu. Můžete také vybrat atribut, u kterého se hodnota vybírá při nastavování modelu konfigurace produktu. Abyste mohli jako komponentu nebo dílčí komponentu zahrnout produkt, je nutné při vytváření produktu na stránce <strong>Vytvořit produkt</strong> zadat tyto informace:
<ul>
<li>V poli <strong>Typ produktu</strong> vyberte možnost<strong>Zboží</strong>.</li>
<li>V poli <strong>Podtyp produktu</strong> vyberte možnost <strong>Základní produkt</strong>.</li>
<li>V poli <strong>Technologie konfigurace</strong> vyberte možnost <strong>Konfigurace založená na omezeních</strong>.</li>
</ul>
Informaci o tom, zda lze uvolněný produkt použít jako komponentu nebo dílčí komponentu, najdete na kartě <strong>Obecné</strong> na stránce <strong>Podrobnosti o uvolněném produktu</strong>. Pokud je v poli <strong>Technologie konfigurace</strong> zvolena možnost <strong>Konfigurace založená na omezeních</strong>, lze produkt použít jako komponentu nebo dílčí komponentu. Dílčí komponenty můžete skrýt tak, aby se během relace konfigurace uživateli nezobrazovaly. Atributy, dílčí komponenty a požadavky uživatelů související s dílčí komponentou budou rovněž skryty.</td>
</tr>
<tr class="odd">
<td>Požadavky uživatele</td>
<td>Požadavky uživatelů představují abstrakci mezi požadavky uživatelů a určitými komponentami a atributy. Požadavek uživatele nelze mapovat na položku. Zákazník chce například koupit systém domácího kina. Prodejní zástupce se může zeptat na velikost místnosti, do které chce zákazník systém instalovat, aby mohl určit potřebný výkon. V tomto příkladu může velikost místnosti být požadavek uživatele, který pomáhá určit hodnotu atributu odpovídající určité komponentě. Požadavky uživatele můžete skrýt, takže se uživateli nebudou během relace konfigurace zobrazovat. Atributy, dílčí komponenty a požadavky uživatelů související s požadavkem uživatele budou rovněž skryty. Můžete vytvořit podmínku určující, zda může být požadavek uživatele skrytý. Podmínku musíte napsat podle syntaxe jazyka OML (Optimization Modeling Language).</td>
</tr>
<tr class="even">
<td>Řádky kusovníku</td>
<td>Řádky kusovníku představují jednotlivé materiály komponent v modelu konfigurace produktu. Na stránce <strong>Podrobnosti řádku kusovníku</strong> lze vybírat všechny položky. Pro řádek kusovníku lze přidat podmínku, aby se mohly řádky kusovníku vybrané pro jedinečnou variantu produktu lišit v závislosti na uživatelském výběru při nastavování modelu konfigurace produktu. Podmínky jsou výrazy, které musí být splněny, aby byly atributy, řádky kusovníku a operace postupu zahrnuty v modelu konfigurace produktu. Na stránce <strong>Podrobnosti řádku kusovníku</strong> lze vybrat jedinečnou hodnotu. Můžete také provést mapování na atribut, pro který je hodnota vybírána při nastavování modelu konfigurace produktu.</td>
</tr>
<tr class="odd">
<td>Operace postupu</td>
<td>Na stránce <strong>Podrobnosti operace postupu</strong> lze vybrat jedinečnou hodnotu. Můžete také provést mapování na atribut, pro který je hodnota vybírána při nastavování modelu konfigurace produktu. Podmínky jsou psány jako omezení výrazů. Podmínky jsou výrazy, které musí být splněny, aby byly atributy, řádky kusovníku a operace postupu zahrnuty v modelu konfigurace produktu.</td>
</tr>
</tbody>
</table>






