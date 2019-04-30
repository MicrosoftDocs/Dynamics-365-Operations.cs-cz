---
title: Vývoj struktury platu/kompenzace a plánu
description: Tento průvodce úkolem vás provede procesem vytváření plánu fixní kompenzace a umožňuje zaměstnancům přihlášení do plánu pomocí pravidel způsobilosti.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichsea
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e3b71e679539441b90f399a84ad8ef8d3decf19
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "859406"
---
# <a name="develop-salarycompensation-structure-and-plan"></a>Vývoj struktury platu/kompenzace a plánu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento průvodce úkolem vás provede procesem vytváření plánu fixní kompenzace a umožňuje zaměstnancům přihlášení do plánu pomocí pravidel způsobilosti. Společnost s ukázkovými daty používaná k tvorbě tohoto úkolu je USMF a tento úkol je určen pro manažera kompenzace a výhod.


## <a name="create-fixed-compensation-plan"></a>Vytvoření plánu fixní kompenzace
1. Klikněte na Správa kompenzací.
2. Klikněte na Plány fixních kompenzací.
3. Klikněte na položku Nová.
4. Zadejte hodnotu do pole Plán.
5. Zadejte nějakou hodnotu do pole Popis.
6. Zadejte datum do pole Datum platnosti.
7. V poli Typ určete, zda je plánem fixní kompenzace Pásmo, Stupeň nebo Krok.
8. Pole Doporučení povoleno se chová jako výchozí hodnota pro všechny akce přidané do tohoto plánu v události zpracování.  Povolením doporučení lze při zpracování kompenzace přepsat vypočítanou částku směrnice.
9. Pole Tolerance mimo rozsah umožňuje určit, jakým způsobem chcete zpracovat částky kompenzace, které se nacházejí mimo určený rozsah struktury kompenzace na dané úrovni.  Tolerance mimo rozsah s hodnotou Žádná umožní použít libovolné částky kompenzace.  Předběžná tolerance upozorní uživatele, pokud je kompenzace menší než minimální výše referenčního bodu této úrovně, nebo větší než maximální částka pro danou úroveň. Uživatel může výstrahu ignorovat a pokračovat.  Pevná tolerance vytvoří chybu, pokud je kompenzace zaměstnance nastavena mimo minimální a maximální referenční body pro úroveň, a automaticky upraví kompenzaci zaměstnance tak, aby spadala do rozsahu.
10. Pole Pravidlo zařazení se používá při spuštění události procesu kompenzace pro výpočet kompenzace zaměstnance.  Pravidlo zařazení s hodnotou procento vypočítá zvýšení, které je poměrné délce času, kdy byl pracovník zaměstnán během daného cyklu.
11. Zadejte hodnotu do pole Měna.
12. V poli Převod mzdové sazby zadejte nebo vyberte hodnotu.
13. Rozbalte oddíl Matice využití rozsahu.
    * Volitelně můžete přidat záznamy využití a dostat tak zaměstnance rychleji do jejich středového bodu a zpomalit jejich dosažení maxima rozsahu.  
14. Nyní musíte uložit plán fixní kompenzace a zpřístupnit tak tlačítko Nastavit kompenzace a pokračovat tak v určení struktury kompenzací pro daný plán.  Klikněte na položku Uložit.
15. Klikněte na Nastavit kompenzaci.
    * Existují tři způsoby, jak vytvoříte strukturu kompenzace. 1: Vytvořte zcela novou strukturu výběrem sady referenčních bodů a přidáním úrovní pro vytvoření vlastní struktury. 2: Zkopírujte strukturu kompenzací z existujícího plánu jako výchozí bod a upravte jej na nový plán. 3: Vyberte existující mřížku kompenzace. Je-li kompenzační mřížka již používaná jiným plánem, změny provedené v mřížce budou také zahrnuty do jiného plánu.  
16. Vyberte možnost Vytvořit nové pro stávající matici kompenzace.
17. V poli Kopírovat z mřížky zadejte nebo vyberte hodnotu.
    * Volitelně můžete změnit název nové mřížky kompenzací, která bude vytvořena jako kopie vybrané mřížky.  
18. Klikněte na tlačítko OK.
19. Klikněte na Hromadná změna.
    * Hromadná změna vám umožní spravovat částky matice kompenzace použitím procenta nebo jednotného nárůstu pro jednu nebo více úrovní nebo referenčních bodů.  
20. Zadejte číslo do pole Částka úpravy.
21. V seznamu označte všechny řádky nebo jejich označení zrušte.
22. Klikněte na Použít na mřížku.
23. Zavřete stránku.
    * Jakmile struktura kompenzace bude vytvořena nebo vybrána, lze vybrat, který referenční bod by měl být použit jako kontrolní bod pro plán fixní kompenzace.  Kontrolní bod se používá k výpočtu srovnávacího poměru zaměstnance.  
24. V poli Kontrolní bod zadejte nebo vyberte hodnotu.
25. Zavřete stránku.

## <a name="create-an-eligibility-rule-for-the-new-fixed-compensation-plan"></a>Vytvoření pravidla kompenzace pro nový plán fixní kompenzace
    * Nový plán fixní kompenzace nelze přiřadit zaměstnanci, dokud nebudou definována pravidla způsobilosti pro plán.  
1. Klikněte na tlačítko Pravidla způsobilosti.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Způsobilost.
4. Zadejte nějakou hodnotu do pole Popis.
5. Zadejte datum do pole Datum platnosti.
    * Pravidla způsobilosti se používají pro plány fixní i variabilní kompenzace.  V poli Typ vyberte typ plánu, pro který je tato sada pravidel způsobilosti určena.  
6. V poli Plán zadejte nebo vyberte hodnotu.
    * Vyberte kritéria, která zaměstnanec musí splňovat, aby splňoval požadavky pro plán kompenzace. Kritéria mohou zahrnovat oddělení, odbory, skladové místo (oblastí kompenzace), úlohu, funkci, typ úlohy nebo úroveň kompenzace. Zaměstnanec musí splňovat všechna uvedená kritéria, aby splňoval požadavky pro plán kompenzace. Pokud nejsou uvedena žádná kritéria, všichni zaměstnanci splňují požadavky pro plán kompenzace. Pokud zaměstnanec nesplňuje kritéria určená v pravidlu způsobilosti, nebo nebylo zadáno pravidlo způsobilosti pro plán kompenzace, plán kompenzace se nezobrazí ve vyhledávání při vytváření záznamu fixní kompenzace pro určitého zaměstnance.  
7. Zavřete stránku.
8. Zavřete stránku.

