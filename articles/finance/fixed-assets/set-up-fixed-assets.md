---
title: Nastavení dlouhodobého majetku
description: Toto téma poskytuje přehled nastavení modulu Dlouhodobý majetek.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c42522f69ecf2eb25d8d9384737115826ff4cda
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978504"
---
# <a name="set-up-fixed-assets"></a>Nastavení dlouhodobého majetku

[!include [banner](../includes/banner.md)]

Toto téma poskytuje přehled nastavení modulu **Dlouhodobý majetek**.

## <a name="overview"></a>Přehled

Parametry řídí obecné chování v modulu Dlouhodobý majetek.

Skupiny dlouhodobého majetku umožňují seskupování majetku a zadat výchozí atributy pro každý jednotlivý majetek, který je přiřazen ke skupině. Knihy jsou přiřazeny skupinám dlouhodobého majetku Knihy sledují finanční hodnotu dlouhodobého majetku v čase pomocí konfigurace odpisů definované profilu odpisů.

Dlouhodobý majetek je při vytvoření zařazen do určité skupiny položek. Ve výchozím nastavení jsou knihy, které jsou přiřazeny ke skupině dlouhodobého majetku, následně přiřazeny dlouhodobému majetku. Knihy, které jsou konfigurovány pro zaúčtování do hlavní knihy, souvisejí s účetním profilem. Účty hlavní knihy jsou definovány pro každou knihu v účetním profilu a jsou použity při zaúčtování transakcí dlouhodobého majetku.

![Komponenty dlouhodobého majetku](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Odpisové plány

Nejprve byste měli nastavit odpisové plány. V odpisovém plánu konfigurujete způsob odepisování hodnoty majetku v čase. Je nutné definovat způsob odpisu, rok pro odpisy (kalendářní rok nebo fiskální rok) a četnost odpisů. Další informace naleznete v tématu [Nastavení a vytvoření odpisových profilů](tasks/set-up-depreciation-profiles.md).

## <a name="books"></a>Knihy

Po nastavení odpisových plánů je nutné vytvořit požadované knihy majetku. Každá kniha sleduje nezávislý finanční životní cyklu majetku. Lze konfigurovat knihy pro zaúčtování souvisejících transakcí do hlavní knihy. Tato konfigurace je výchozí nastavení, protože je běžně používána pro podnikové finanční vykazování. Knihy, které se nezaúčtovávají do hlavní knihy, se zaúčtovávají pouze do hlavní knihy dlouhodobého majetku a obvykle se používají pro účely vykázání daně.

Každá kniha má přiřazen primární odpisový plán. Knihy také mají alternativní nebo náhradní odpisový plán, pokud tento typ profilu je možné použít. Pokud chcete automaticky zahrnout knihu dlouhodobého majetku do spuštění odpisů, musíte povolit možnost **Vypočítat odpis**. Pokud tato možnost není povolena pro majetek, bude majetek při návrhu odpisu vynechán.

Lze také nastavit odvozené knihy. Určené odvozené transakce jsou zaúčtovány oproti odvozeným knihám jako přesná kopie primární transakce. Z toho vyplývá, že odvozené transakce jsou obvykle nastaveny pro pořízení a likvidace, ne pro transakce odpisů. Další informace naleznete v tématu [Nastavení modelů ocenění](tasks/set-up-value-models.md).

## <a name="fixed-asset-posting-profiles"></a>Účetní profily dlouhodobého majetku

Po nastavení knih můžete vytvořit účetní profil. Účetní profil musí být definován v knize, ale lze ho také definovat na podrobnější úrovni. Lze například definovat účetní profil pro kombinaci knihy a skupiny dlouhodobého majetku nebo dokonce pro jednotlivou knihu dlouhodobého majetku. Standardně se používají účty hlavní knihy, které jsou definovány pro transakce dlouhodobého majetku.

Je nutné definovat účty hlavní knihy použité během procesu vyřazení prodeje a odstraňování odpadu. V čase vyřazení jsou transaakce dlouhodobého majetku, které byly dříve zaúčtovány, vystornovány z původních účtů. Čisté částky jsou pak přesunuty na příslušný účet pro zisk a ztrátu pro vyřazení majetku. K zajištění, že jsou transakce stornovány správně, je nutné nastavit účty pro jednotlivé typy transakcí, které používáte při vašich obchodních činnostech. Hlavní účet by měl být původním hlavním účtem, který nastavíte pro tento typ transakce v účtovacím profilu, zatímco protiúčet by měl být účet pro zisky a ztráty pro dispoziční účet. Výjimku tvoří zůstatkové účetní hodnoty. V tomto případě by měl být hlavní účet i protiúčet nastaven na zisky a ztráty pro dispoziční účet. Další informace naleznete v tématu [Nastavení účetních profilů dlouhodobého majetku](tasks/set-up-fixed-asset-posting-profiles.md).

## <a name="fixed-asset-groups"></a>Skupiny dlouhodobého majetku

Pole **Skupina dlouhodobého majetku** je jediné povinné pole při vytváření dlouhodobého majetku. Hodnota tohoto pole určuje výchozí hodnotu několika informační polí majetku. Knihy jsou nastaveny tak, aby výchozí kniha byla přiřazen ke každému majetku ve skupině. Tímto způsobem mohou být atributy, které jste nastavili pro knihy, specifické pro skupinu majetku. Tyto atributy zahrnují životnost a způsob odpisu.

Můžete také definovat náhrady za zvláštní odpisy nebo počáteční mimořádný odpis pro určité kombinace skupiny dlouhodobého majetku a knihy. Je nutné přiřadit prioritu náhradě za zvláštní odpisy k určení pořadí výpočtu náhrad, když je knize přiřazeno více náhrad. Další informace naleznete v tématu [Nastavení skupiny dlouhodobého majetku](tasks/set-up-fixed-asset-groups.md).

## <a name="journal-names"></a>Názvy deníků

Na stránce **Názvy deníků** je nutné vytvořit názvy deníků, které musí být použity s deníkem dlouhodobého majetku. Je nutné nastavit pole **Typ deníku** na **Zaúčtovat dlouhodobý majetek**. Nastavte pole **Číselná řada dokladů** tak, aby se názvy deníku použily pro deník dlouhodobého majetku. Deníky dlouhodobého majetku by neměly používat nastavení **Pouze jedno číslo dokladu**, protože jedinečné číslo dokladu je požadováno pro několik automatizovaných procesů, jako jsou například převody a rozdělení.

## <a name="fixed-asset-parameters"></a>Parametry dlouhodobého majetku

Posledním krokem je aktualizace parametrů dlouhodobého majetku.

Pole **Prahová hodnota kapitalizace** určuje majetek, který je odepsán. Jestliže je řádek nákupu vybrán jako dlouhodobý majetek, ale neodpovídá prahové hodnotě kapitalizace, která je zadána, dlouhodobý majetek je stále vytvořen nebo aktualizován, ale možnost **Výpočtu odpisů** je nastavena na **Ne**. Proto nebude majetek odepsán automaticky v rámci návrhů odpisů.

Jedna z důležitých možností se nazývá **Automaticky vytvořit částky úprav odpisů s vyřazením**. Pokud tuto možnost nastavíte na **Ano**, odpis majetku je automaticky upraven na základě nastavení odpisů při likvidaci aktiva. Další možnost umožńuje odečíst slevy z částky pořízení při pořízení dlouhodobého majetku pomocí faktury dodavatele.

Na pevné záložce **Nákupní objednávky** můžete nakonfigurovat způsob, jakým bude majetek vytvářen jako součást procesu nakupování. První možnost se nazývá **Povolit pořízení majetku v části Nakupování**. Pokud tuto možnost nastavíte na **Ano**, při zaúčtování faktury dojde k pořízení majetku. Pokud tuto možnost nastavíte na hodnotu **Ne**, i nadále můžete vkládat dlouhodobý majetek na nákupní objednávky a faktury, ale nezaúčtují se pořízení. Zaúčtování je nutné provést jako samostatný krok v deníku dlouhodobého majetku. Možnost **Vytvořit majetek při zaúčtování příjemky produktu nebo faktury** umožňuje vytvořit nový majetek "průběžně" během zaúčtování. Majetek tedy nemusí být nastaven jako dlouhodobý majetek před transakcí. Poslední možnost **Kontrola vytvoření dlouhodobého majetku při zadání řádku** platí pouze pro nákupní požadavky.

Je možné nakonfigurovat kódy důvodu tak, aby byly vyžadovány pro změny dlouhodobého majetku nebo pro konkrétní transakce dlouhodobého majetku.

Nakonec na kartě **Číselné řady** můžete definovat číselné řady pro dlouhodobý majetek. Číselná řada **Dlouhodobého majetku** může být přepsána číselnou řadou číslo **skupiny dlouhodobého majetku**, pokud byla zadána.

Další informace naleznete v tématu [Vytvoření dlouhodobého majetku](tasks/create-fixed-asset.md).
