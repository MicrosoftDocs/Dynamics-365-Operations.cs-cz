---
title: "Sladění dovedností zaměstnanců s potřebami společnosti"
description: "Můžete sledovat dovednosti, které zaměstnanci, uchazeči nebo kontaktní osoby mají (nebo které by měli mít) k účinnému plnění svých rolí. Můžete také určit dovednosti, které jsou požadovány pro určitou práci."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 720a1f272948eb310dc3cd02588aeec40b556d20
ms.openlocfilehash: 31dda85ff2e4a4e5380401b031b2dd74acff394b
ms.lasthandoff: 03/31/2017


---

# <a name="align-workforce-skills-with-business-needs"></a>Sladění dovedností zaměstnanců s potřebami společnosti

Můžete sledovat dovednosti, které zaměstnanci, uchazeči nebo kontaktní osoby mají (nebo které by měli mít) k účinnému plnění svých rolí. Můžete také určit dovednosti, které jsou požadovány pro určitou práci.

Zde jsou příklady dovedností, které lze sledovat:
-   Dozorčí - schopnost dohlížet na práci ostatních.
-   Vůdčí - schopnost vést zaměstnance a obchodní domény.
-   Plánování - schopnost dívat se dopředu, formulovat vize a schopnost tyto vize definovat.
-   HTML – schopnost psát v kódu HTML.

Před přiřazením dovednosti k osobě nebo pracovní pozici, vytvořením vyhledávání s mapováním dovedností nebo vytvořením profilu dovedností je nutné zadat informace o dovednostech na stránce **Dovednosti**. Pro každou dovednost můžete vybrat typ dovednosti a model hodnocení.

## <a name="rating-models"></a>Modely hodnocení
Modely hodnocení pomáhají ve vyhodnocení skutečné úrovně dovedností osoby, úrovně, které mají dosáhnout, nebo úrovně dovednosti, která je požadována pro úlohu. Můžete zadat až 10 úrovní pro model hodnocení.  Každé úrovni v modelu hodnocení je přiřazen koeficient.  Hodnota koeficientu se použije k normalizaci výsledků dovedností, které používají různé modely hodnocení.  Koeficient musí být číslo mezi 0 a 9 a každá úroveň musí mít jedinečný koeficient.  Úrovně s vyšší hodnotou koeficientu nesou v modelu hodnocení větší váhu.

## <a name="specify-job-skills"></a>Určení dovedností pro úlohu
Při zadání informací o pracovní pozici můžete zadat dovednosti, které má daná osoba mít k provedení práce v rámci pracovní pozice.  Dále je možné určit požadovanou úroveň pro každou dovednost a také úroveň důležitosti dané dovednosti. Různé pracovní pozice mohou vyžadovat různé úrovně důležitosti pro stejné dovednosti.

## <a name="enter-skills-for-workers-applicants-or-contacts"></a>Zadejte dovedností zaměstnanců, uchazečů nebo kontaktů
Můžete zadat cílové dovednosti, nebo skutečné dovedností zaměstnanců, uchazečů nebo kontaktů. Cílové dovednosti jsou dovednosti, kterých se osoba chystá dosáhnout. Skutečná dovednost je dovednost, kterou pracovník aktuálně disponuje.

## <a name="skill-mapping-and-skill-mapping-profiles"></a> Mapování dovedností a profily mapování dovedností
Lze vytvořit hledání v rámci mapování dovedností k vyhledání pracovníka, uchazeče nebo kontaktní osoby, která je kvalifikována k provádění určitého úkolu. Při hledání v rámci mapování dovedností se prohledávají dovednosti, certifikáty vzdělání, pozice důvěry a zkušenosti s projektem a jsou vráceny výsledky, které odpovídají zadaným kritériím.  Například může být užitečné vědět, kteří pracovníci ve vaší organizaci získali CPA.

Profily mapování dovedností umožňují vyhledání aktuálního zaměstnance nebo kandidáta s kvalifikací, která přímo odpovídá obchodním potřebám.  Můžete například vytvořit profil mapování dovedností pro otevřenou pozici ve vaší organizaci. Vytvořením profilu pro určitou pozici a zkopírováním dovedností, vzdělání a certifikátů z této pracovní pozice do profilu lze rychle vyhledat pracovníky, uchazeče a kontaktní osoby, které odpovídají jednomu nebo více kritériím zadaným v profilu, a zobrazit seznam uchazečů, jejichž dovednosti nejlépe odpovídají požadovaným dovednostem pro pracovní pozici.

<table>
<thead>
<tr class="header">
<th><strong>Poznámka </strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>V seznamu s výsledky mapování dovednosti mohou být zobrazeni nebo zahrnuti v profilu dovedností pouze zaměstnanci, uchazeči a kontaktní osoby, které jsou vybrány k zahrnutí do hledání v rámci mapování dovedností. Chcete-li zahrnout pracovníka, uchazeče nebo kontaktní osobu do vyhledávání v rámci mapování dovedností, nastavte možnost <strong>Zahrnout do mapování dovedností</strong> na hodnotu Ano na následujících stránkách:
<ul>
<li>Pracovní podproces</li>
<li>Zaměstnanec</li>
<li>Uchazeč</li>
<li>Kontakty</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a>Analýza mezer v dovednostech a analýza profilu dovedností
Můžete vytvořit analýzu profilu dovedností, a zobrazit tak seznam kompetencí pro pracovníka, uchazeče nebo kontaktní osobu k určitému datu. Můžete vytvořit analýzu dovednostních mezer k porovnání dovedností dané osoby s dovednostmi požadovanými pro určitou úlohu.  



<a name="see-also"></a>Viz také
--------

[Lidské zdroje](index.md)


