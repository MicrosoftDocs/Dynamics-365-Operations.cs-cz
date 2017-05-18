---
title: "Nastavení dlouhodobého majetku"
description: "Toto téma poskytuje přehled nastavení modulu Dlouhodobý majetek."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: c239fd31e8ea865b0378cf0d6feb1dd920e396d0
ms.contentlocale: cs-cz
ms.lasthandoff: 04/25/2017


---

# <a name="set-up-fixed-assets"></a>Nastavení dlouhodobého majetku

[!include[banner](../includes/banner.md)]


Toto téma poskytuje přehled nastavení modulu Dlouhodobý majetek.

<a name="overview"></a>Přehled
--------
Parametry řídí obecné chování v modulu Dlouhodobý majetek.

Skupiny dlouhodobého majetku umožňují seskupování majetku a zadat výchozí atributy pro každý jednotlivý majetek, který je přiřazen ke skupině. Knihy jsou přiřazeny skupinám dlouhodobého majetku Knihy sledují finanční hodnotu dlouhodobého majetku v čase pomocí konfigurace odpisů definované profilu odpisů.

Dlouhodobý majetek je při vytvoření zařazen do určité skupiny položek. Ve výchozím nastavení jsou knihy, které jsou přiřazeny ke skupině dlouhodobého majetku, následně přiřazeny dlouhodobému majetku. Knihy, které jsou konfigurovány pro zaúčtování do hlavní knihy, souvisejí s účetním profilem. Účty hlavní knihy jsou definovány podle knihy v účetním profilu a jsou použity při zaúčtování transakcí dlouhodobého majetku. 

![FixedAssetsComponentsImage](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Odpisové plány
Nejprve byste měli nastavit odpisové plány. V odpisovém plánu konfigurujete způsob odepisování hodnoty majetku v čase. Je nutné definovat způsob odpisu, rok pro odpisy (kalendářní rok nebo fiskální rok) a četnost odpisů.

## <a name="books"></a>Knihy
Po nastavení odpisových plánů je nutné vytvořit požadované knihy majetku. Každá kniha sleduje nezávislý finanční životní cyklu majetku. Lze konfigurovat knihy pro zaúčtování souvisejících transakcí do hlavní knihy. Tato konfigurace je výchozí nastavení, protože je běžně používána pro podnikové finanční vykazování. Knihy, které se nezaúčtovávají do hlavní knihy, se zaúčtovávají pouze do hlavní knihy dlouhodobého majetku a obvykle se používají pro účely vykázání daně.

Každá kniha má přiřazen primární odpisový plán. Knihy také mají alternativní nebo náhradní odpisový plán, pokud tento typ profilu je možné použít. Pokud chcete automaticky zahrnout knihu dlouhodobého majetku do spuštění odpisů, musíte povolit možnost Vypočítat odpis. Pokud tato možnost není vybraná pro majetek, bude majetek při návrhu odpisu vynechán.

Lze také nastavit odvozené knihy. Určené odvozené transakce jsou zaúčtovány jako přesná kopie primární transakce oproti odvozeným knihám. Z toho vyplývá, že odvozené transakce jsou obvykle nastaveny pro pořízení a likvidace, ne pro transakce odpisů.

## <a name="fixed-asset-posting-profiles"></a>Účetní profily dlouhodobého majetku
Po nastavení knih můžete vytvořit účetní profil. Účetní profil musí být definován v knize, ale lze ho také definovat na podrobnější úrovni. Lze například definovat účetní profil pro kombinaci knihy a skupiny dlouhodobého majetku nebo dokonce pro jednotlivou knihu dlouhodobého majetku. Standardně se používají účty hlavní knihy, které jsou definovány pro transakce dlouhodobého majetku.

Je nutné definovat účty hlavní knihy použité během procesu vyřazení prodeje a odstraňování odpadu. V době vyřazení jsou stornovány transakce dlouhodobého majetku, které byly dříve zaúčtovány z původních účtů a čisté částky jsou přesunuty na příslušný účet zisků a ztrát pro vyřazení majetku. K zajištění, že jsou transakce stornovány správně, je nutné nastavit účty pro jednotlivé typy transakcí, které používáte při vašich obchodních činnostech. Hlavní účet by měl být původním hlavním účtem, který nastavíte pro tento typ transakce v účtovacím profilu, zatímco protiúčet by měl být účet pro zisky a ztráty pro dispoziční účet. Výjimku tvoří zůstatkové účetní hodnoty. V tomto případě by měl být hlavní účet i protiúčet nastaven na zisky a ztráty pro dispoziční účet.

## <a name="fixed-asset-groups"></a>Skupiny dlouhodobého majetku
Skupina dlouhodobého majetku je jediné povinné pole při vytváření dlouhodobého majetku. Hodnota tohoto pole určuje výchozí hodnotu několika informační polí majetku. Knihy jsou nastaveny tak, aby výchozí kniha byla přiřazen ke každému majetku ve skupině. Pak můžete nastavit atributy knihy, které jsou specifické pro skupinu majetku, jako je například Životnost a Konvence odpisu.

Můžete také definovat náhrady za zvláštní odpisy nebo počáteční mimořádný odpis pro určité kombinace skupiny dlouhodobého majetku a knihy. Je nutné přiřadit prioritu náhradě za zvláštní odpisy k určení pořadí výpočtu náhrad, když je knize přiřazeno více náhrad.

## <a name="fixed-asset-parameters"></a>Parametry dlouhodobého majetku
Posledním krokem je aktualizace parametrů dlouhodobého majetku.

Pole Prahová hodnota kapitalizace určuje majetek, který je odepsán. Jestliže je řádek nákupu vybrán jako dlouhodobý majetek, ale neodpovídá prahové hodnotě kapitalizace, která je zadána, dlouhodobý majetek je stále vytvořen nebo aktualizován, ale možnost výpočtu odpisů je nastavena na Ne. Proto nebude majetek odepsán automaticky v rámci návrhů odpisů.

Jednou z důležitých možností je Automaticky vytvořit částky úprav odpisů s vyřazením. Pokud tuto možnost nastavíte na Ano, odpis majetku je automaticky upraven na základě nastavení odpisů při likvidaci aktiva. Další možnost umožńuje odečíst slevy z částky pořízení při pořízení dlouhodobého majetku pomocí faktury dodavatele.

Na pevné záložce Nákupní objednávky můžete nakonfigurovat způsob, jakým bude majetek vytvářen jako součást procesu nakupování. První možnost je Povolit pořízení majetku v části Nakupování. Pokud tuto možnost nastavíte na Ano, při zaúčtování faktury dojde k pořízení majetku. Pokud tuto možnost nastavíte na hodnotu Ne, i nadále můžete vkládat dlouhodobý majetek na nákupní objednávky a faktury, ale nezaúčtují se pořízení. Zaúčtování je nutné provést jako samostatný krok v deníku dlouhodobého majetku. Možnost Vytvořit majetek při zaúčtování příjemky produktu nebo faktury umožňuje vytvořit nový majetek "průběžně" při zaúčtování tak, aby nemusel být nastaven jako dlouhodobý majetek před transakcí. Poslední možnost Kontrola vytvoření dlouhodobého majetku při zadání řádku platí pouze pro nákupní požadavky.

Je možné nakonfigurovat kódy důvodu tak, aby byly vyžadovány pro změny dlouhodobého majetku nebo pro konkrétní transakce dlouhodobého majetku.

Nakonec na kartě Číselné řady můžete definovat číselné řady pro dlouhodobý majetek. Číselná řada dlouhodobého majetku může být přepsána číselnou řadou Číslo skupiny dlouhodobého majetku, pokud byla zadána.




