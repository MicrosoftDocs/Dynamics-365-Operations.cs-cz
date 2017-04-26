---
title: "Plány kompenzace"
description: "Manažeři kompenzací a výhod mohou pomocí správy kompenzací udržovat a zpracovávat fixní i variabilní plány kompenzací pro zaměstnance organizace."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6f4429202efd0506378d681188035c5cc69f56a1
ms.openlocfilehash: 1809a6679685e483694a53b7742d80f02ade2cd5
ms.lasthandoff: 03/31/2017


---

# <a name="compensation-plans"></a>Plány kompenzace

[!include[banner](includes/banner.md)]


Manažeři kompenzací a výhod mohou pomocí správy kompenzací udržovat a zpracovávat fixní i variabilní plány kompenzací pro zaměstnance organizace.

### <a name="introduction"></a>Úvod

Správa vyrovnání slouží k řízení dodávky základní platby a ocenění. Pro zaměstnance stanovena základní platby a zvýšení zásluh jsou řízena plány fixní kompenzace. Pobídkové platby, jako například výplaty bonusů, výkonnostních odměn, opcí na nákup akcií nebo grantů, a také jednorázové odměny jsou řízeny prostřednictvím plánů variabilní kompenzace. 

Zaměstnance lze zaregistrovat k jednomu i několika plánům obou typů. Aby byl zaměstnanec způsobilý k registraci v plánu kompenzace, musí splňovat tyto předpoklady:
-   Zaměstnanec musí mít přiřazenu aktivní pozici.
-   Zaměstnanec musí splňovat kritéria, která jsou definována pravidly způsobilosti pro plán kompenzace.

## <a name="compensation-setup"></a> Nastavení kompenzace
V následující tabulce jsou uvedeny komponenty procesu kompenzace, které mohou nedílnou součástí nastavování plánů kompenzace ve vaší společnosti.

<table>
<thead>
<tr class="header">
<th>Součást</th>
<th>Více informací…</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Akce fixní kompenzace</td>
<td>Akce fixních kompenzací mají dva účely:
<ul>
<li>Akce může určit druh informací, které musí být zaznamenány při změně kompenzace zaměstnance. Můžete například požadovat, aby byl zaznamenán důvody změny, jako třeba povýšení nebo naopak degradace.</li>
<li>Akce můžete zajistit, že výpočet se použije, když jsou zpracovány plány fixní kompenzace.  Například akce typu jmění porovná mzdy zaměstnance na minimální referenční bod pro úroveň na zaměstnance a zajistit, aby že zaměstnanec získávání platí alespoň minimální.</li>
</ul></td>
</tr>
<tr class="even">
<td>Úrovně</td>
<td>Úrovně jsou přiřazeny k úlohám a všem pozicím souvisejícím s odkazy na úlohy. Můžete vytvořit diskrétní úrovně pro tři typy plánů kompenzace: Třída, Pásmo a Krok.</td>
</tr>
<tr class="odd">
<td>Matice využití rozsahu</td>
<td>Matice využití rozsahu pomáhá s přenosem zaměstnanců do kontrolního bodu pro jejich úlohu. Díky využití rozsahu lze také řídit sazbu jmění ve společnosti bez ohledu na výkon jednotlivých zaměstnanců a celkový výkon společnosti. Například zaměstnanci, kteří jsou ve svém rozsahu placeni méně, získají vyšší procentuální navýšení než zaměstnanci, kteří jsou ve svém rozsahu placeni více. Tímto způsobem lze systematicky posunovat rozdíly ve jmění. Výpočet využití rozsahu se provádí takto: (pevná mzdová sazba – minimum rozsahu) ÷ (maximum rozsahu – minimum rozsahu).</td>
</tr>
<tr class="even">
<td>Nastavení referenčních bodů</td>
<td>Nastavení referenčních bodů zahrnuje sadu referenčních bodů představující rozsahy v matici. Každý rozsah lze přidružit k mzdové sazbě. Stupňové plány například často obsahují referenční body Minimum, Střední bod a Maximum.</td>
</tr>
<tr class="odd">
<td>Matice kompenzace</td>
<td>Matice kompenzace je sada referenčních bodů a úrovní, které slouží k vytváření struktury kompenzací.</td>
</tr>
<tr class="even">
<td>Struktura kompenzací</td>
<td>Struktura kompenzace je matice kompenzace s mzdovými sazbami přidruženými k referenčním bodům pro každou úroveň.</td>
</tr>
<tr class="odd">
<td>Pravidla způsobilosti</td>
<td>Pravidla způsobilosti slouží k určení pracovníků s určitými úlohami, pracovními funkcemi, typy úloh, odbory nebo oblastmi kompenzace, které jsou kryty danými plány kompenzace. Chcete-li zařadit zaměstnance do plánu, je nutné vytvořit pravidla způsobilosti pro plány variabilní i fixní kompenzace. Po určení pravidel způsobilosti pro plán kompenzace můžete definovat úrovně, které mají být použity pro úlohy kryté plánem.</td>
</tr>
<tr class="even">
<td>Interval plateb</td>
<td>Plateb se používají k definování časové období, pro které je určena vyrovnání.  Například mzdy frekvence usnadňuje pochopení, pokud částka kompenzace je určena jako ročního platu oproti hodinové mzdy. Plateb jsou také použity k nastavení koeficientů převodu pro převod částek odškodnění měsíčně, týdně, biweekly a hodinové plateb každoroční mzdy.</td>
</tr>
<tr class="odd">
<td>Oblasti kompenzací</td>
<td>Oblasti kompenzace slouží k určení kompenzace zaměstnance na základě umístění pracovního prostředí.</td>
</tr>
<tr class="even">
<td>Kontrolní bod</td>
<td>Kontrolní bod určuje to, co považujete za ideální sazbu pro všechny zaměstnance na úrovni kompenzace. U struktur plánů tříd jsou kontrolní body obvykle středním bodem rozsahu. Struktury pásma kontrolní body používají jen zřídka. Kontrolní bod pro plán fixní kompenzace můžete určit ve formuláři Plány fixní kompenzace.</td>
</tr>
<tr class="odd">
<td>Pracovní funkce</td>
<td>Pracovní funkce se používají ke klasifikaci a k filtrování plánů kompenzací pro určité úlohy.</td>
</tr>
<tr class="even">
<td>Typ úloh</td>
<td>Typy úloh se používají ke klasifikaci a k filtrování plánů kompenzací pro určité úlohy.</td>
</tr>
<tr class="odd">
<td>Typy variabilních kompenzací</td>
<td>Typy variabilní kompenzace (například odměny v akciích nebo finanční bonusy) se nastavují v plánu variabilní kompenzace.</td>
</tr>
<tr class="even">
<td>Kompenzační mřížky</td>
<td>Kompenzační mřížky obsahovat strukturu kompenzace.  Kompenzační mřížky slouží jednomu nebo více plánům kompenzace.</td>
</tr>
<tr class="odd">
<td>Plány výkonnosti</td>
<td>Plány výkonnosti slouží k přidružení výkonu k matici přidělení, aby bylo možné plán použít ve strategii výkonnostní složky.</td>
</tr>
<tr class="even">
<td>Hodnocení výkonnosti</td>
<td>Hodnocení výkonnosti se používá v plánech výkonnosti k určení částky odměny za zásluhy nebo odměny za výkonnost.</td>
</tr>
</tbody>
</table>

## <a name="process-events"></a>Procesní události
Procesní události vypočítá informace o kompenzaci za dané časové období pro všechny zaměstnance, kteří jsou přihlášeni v jednom nebo několika plánech fixní nebo variabilní kompenzace. Procesní událost lze spouštět opakovaně a tím otestovat nebo aktualizovat vypočítané výsledky kompenzace.

<a name="compensation-events"></a>Události kompenzace
-------------------

Každém spuštění procesní události kompenzace událostí je vytvořen.  Události kompenzace obsahovat výsledky procesu kompenzace pro každého zaměstnance součástí této události procesu.  Pokud jsou správné výpočty, můžete načíst události aktualizovat záznamy kompenzace pro zaměstnance, kteří jsou ovlivněny procesní události kompenzace.

## <a name="recommendations"></a> Doporučení
Po spuštění procesní události můžete doporučit úpravy nárůstu zásluh zaměstnance nebo částku odměny na základě vypočtených směrnic procesní události. Aby bylo možné dívat doporučení pro zaměstnance, je nutné povolit doporučení při nastavování plánů kompenzace nebo při vytváření procesní události.




