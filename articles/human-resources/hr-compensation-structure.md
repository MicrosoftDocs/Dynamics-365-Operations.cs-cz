---
title: Vývoj struktury kompenzace
description: Tento článek vás provede procesem vytváření plánu fixní kompenzace a přihlašování zaměstnanců do plánu pomocí pravidel způsobilosti.
author: andreabichsel
manager: tfehr
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a5e7ef2021e41c13b82523f2dc6a1b09bd1ba9f
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115889"
---
# <a name="develop-a-compensation-structure"></a>Vývoj struktury kompenzace

Tento článek vás provede procesem vytváření plánu fixní kompenzace a přihlašování zaměstnanců do plánu pomocí pravidel způsobilosti. Tento článek používá ukázková data USMF a je určen pro manažery kompenzace a výhod.

## <a name="create-a-fixed-compensation-plan"></a>Vytvoření plánu fixní kompenzace

1. Vyberte **Správa kompenzací**.

2. Vyberte **Plány fixní kompenzace**.

3. Zvolte **Nové**.

4. Zadejte hodnotu do pole **Plán**.

5. V poli **Popis** zadejte hodnotu.

6. Zadejte datum do pole **Datum platnosti**.

7. V poli **Typ** určete, zda je plánem fixní kompenzace **Pásmo**, **Stupeň** nebo **Krok**.

8. Pole **Doporučení povoleno** se chová jako výchozí hodnota pro všechny akce přidané do tohoto plánu v události zpracování. Povolením doporučení lze při zpracování kompenzace přepsat vypočítanou částku směrnice.

9. Pole **Tolerance mimo rozsah** umožňuje určit, jakým způsobem chcete zpracovat částky kompenzace, které se nacházejí mimo určený rozsah struktury kompenzace na dané úrovni. Nastavení pole **Tolerance mimo rozsah** na **Žádný** umožňuje použít jakoukoli částku kompenzace. **Předběžná tolerance** upozorní uživatele, pokud je kompenzace menší než minimální nebo větší než maximální výše referenčního bodu této úrovně. Uživatelé mohou výstrahu ignorovat a pokračovat. **Pevná tolerance** vytvoří chybu, pokud je kompenzace zaměstnance nastavena mimo minimální a maximální referenční body pro úroveň, a automaticky upraví kompenzaci zaměstnance tak, aby spadala do rozsahu.

10. Pole **Pravidlo zařazení** vypočítává kompenzaci zaměstnance během procesní události. **Pravidlo zařazení** s hodnotou **Procento** vypočítá zvýšení, které je poměrné délce času, kdy byl pracovník zaměstnán během daného cyklu.

11. Zadejte hodnotu do pole **Měna**.

12. V poli **Převod mzdové sazby** zadejte nebo vyberte hodnotu.

13. Rozbalte oddíl **Matice využití rozsahu**. Volitelně můžete přidat záznamy využití a dostat tak zaměstnance rychleji do jejich středového bodu a zpomalit jejich dosažení maxima rozsahu.

14. Zvolte **Uložit**. Tím se aktivuje tlačítko **Nastavit kompenzaci** a budete pokračovat ve definování struktury kompenzací pro daný plán.

15. Vyberte **Nastavení kompenzace**. Můžete vytvořit strukturu kompenzace pomocí jedné z následujících třech metod:

    - Vytvořte zcela novou strukturu výběrem sady referenčních bodů a přidáním úrovní pro vytvoření vlastní struktury.
    - Zkopírujte strukturu kompenzací z existujícího plánu jako výchozí bod a upravte jej na nový plán.
    - Vyberte existující mřížku kompenzace. Je-li kompenzační mřížka již používaná jiným plánem, změny provedené v mřížce budou také zahrnuty do jiného plánu.

16. Vyberte **Vytvořit novou ze stávající matice kompenzace**.

17. V poli **Kopírovat z mřížky** zadejte nebo vyberte hodnotu. Volitelně můžete změnit název nové mřížky kompenzací, která bude vytvořena jako kopie vybrané mřížky.

18. Vyberte **OK**.

19. Vyberte **Hromadnou změnu**. **Hromadná změna** vám umožní spravovat částky matice kompenzace použitím procenta nebo jednotného nárůstu pro jednu nebo více úrovní a/nebo referenčních bodů.

20. Zadejte číslo do pole **Částka úpravy**.

21. V seznamu označte všechny řádky nebo jejich označení zrušte.

22. Klikněte na **Použít na mřížku**.

23. Zavřete stránku. Jakmile struktura kompenzace bude vytvořena nebo vybrána, lze vybrat, který referenční bod by měl být použit jako kontrolní bod pro plán fixní kompenzace. Kontrolní bod se používá k výpočtu srovnávacího poměru zaměstnance.

24. V poli **Kontrolní bod** zadejte nebo vyberte hodnotu.

25. Zavřete stránku.

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a>Vytvoření pravidla kompenzace pro plán fixní kompenzace

Nový plán fixní kompenzace nelze přiřadit zaměstnanci, dokud nebudou definována pravidla způsobilosti pro plán.  

1. Vyberte **Pravidla nároků**.

2. Zvolte **Nové**.

3. V poli **Nárok** zadejte hodnotu.

4. V poli **Popis** zadejte hodnotu.

5. Zadejte datum do pole **Datum platnosti**. Pravidla způsobilosti se používají pro plány fixní i variabilní kompenzace. V poli **Typ** vyberte typ plánování.

6. V poli **Plán** zadejte nebo vyberte hodnotu. Vyberte kritéria, která zaměstnanec musí splňovat, aby splňoval požadavky pro plán kompenzace. Kritéria mohou zahrnovat:

    - **Oddělení**
    - **Odbor**
    - **Umístění** (**Umístění kompenzace**)
    - **Práce**
    - **Funkce**
    - **Typ úlohy**
    - **Úroveň kompenzace**
    
    Zaměstnanec musí splňovat všechna uvedená kritéria, aby splňoval požadavky pro plán kompenzace. Pokud neuvedete žádná kritéria, všichni zaměstnanci splňují požadavky pro plán kompenzace. Pokud zaměstnanec nesplňuje kritéria určená v pravidlu způsobilosti, nebo nebylo zadáno pravidlo způsobilosti pro plán kompenzace, plán kompenzace se nezobrazí ve vyhledávání při vytváření záznamu fixní kompenzace pro určitého zaměstnance.

7. Zavřete stránku.

8. Zavřete stránku.

