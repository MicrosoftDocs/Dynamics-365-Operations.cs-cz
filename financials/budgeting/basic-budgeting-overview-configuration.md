---
title: "Přehled rozpočtování"
description: "Téměř všechny společnosti, které používají funkci Finance v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition budou mít možnost vytvářet sestavy rozpočtu a skutečných hodnot. Tento článek popisuje minimální konfiguraci, která je nezbytná pro vytváření rozpočtů v aplikaci Finance and Operations, Enterprise edition nebo pro jejich načítání z programu třetích stran."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 60113
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: sigitac
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: f35db274a6b14f6bae185b69348d3829c77801b5
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017

---

# <a name="budgeting-overview"></a>Přehled rozpočtování 

[!include[banner](../includes/banner.md)]


Téměř všechny společnosti, které používají funkci Finance v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition budou mít možnost vytvářet sestavy rozpočtu a skutečných hodnot. Tento článek popisuje minimální konfiguraci, která je nezbytná pro vytváření rozpočtů v aplikaci Finance and Operations nebo pro jejich načítání z programu třetích stran.

<a name="overview"></a>Přehled
--------

Schválený rozpočet pro právnickou osobu je udržován v dokumentu, který je označován jako *položka registru rozpočtu*. Řádky v dokumentu položek registru rozpočtu se označují jako položky *rozpočtového účtu* a obsahují informace o finančních dimenzích, datech a částkách schváleného rozpočtu. Dokument s položkami registru rozpočtu je integrován se základními finančními sestavami a stránkami s dotazy, kde se skutečné částky hlavní knihy porovnávají s částkami rozpočtu. 

Vytvoření položek registru rozpočtu v aplikaci Finance and Operations lze několika způsoby:

-   Ručně zadat informace o dokumentu na stránce **položky registru rozpočtu**.
-   Použít šablonu aplikace Microsoft Excel, kterou lze otevřít klepnutím na tlačítko **Otevřít v aplikaci Excel** na stránce **položky registru rozpočtu**.
-   Použití datovou entitu **účetní položky rozpočtu** v modulu Správa dat pro import položek registru rozpočtu. Zvažte použití této metody a zapnutí **zpracování parametru **Založeno na sadě** **, když musíte importovat velký počet účetních položek rozpočtu do systému.
-   Pokud společnost používá funkci plánování rozpočtu pro přípravu dat rozpočtu, můžete použít periodické zpracování **Generovat položku registru rozpočtu**.

Položka registru rozpočtu je považována za dokončenou po aktualizaci rozpočtového zůstatku. Na stránce **Položky registru rozpočtu** klikněte na **Aktualizovat rozpočtové zůstatky** pro výběr položky registru rozpočtu nebo více položek. Po provedení aktualizace zůstatků rozpočtu se stav položky rozpočtu registru změní na **Dokončeno**. Dokončená položka registru rozpočtu nemůže být znovu otevřena pro úpravy. Proto, chcete-li upravit data rozpočtu, musíte vytvořit novou položku registru rozpočtu namísto opravy dat v dokončené položce registru rozpočtu.

## <a name="configuration"></a>Konfigurace
Při konfiguraci rozpočtování začněte na stránce **Parametry rozpočtování**. Na této stránce je nutné definovat deník rozpočtu, číselnou řadu pro položky registru rozpočtu a výchozí nastavení v pracovních prostorách.

Dále pokud existují zásady, které řídí schválení položek registru rozpočtu v závislosti na typu rozpočtu (například převody nebo revize), je nutné vytvořit workflow položek registru rozpočtu na stránce **Workflowy rozpočtování**. Pokud jsou scénáře, kde mohou být převody povoleny bez schválení workflow, můžete definovat pravidla převodu rozpočtu pro podporu těchto scénářů. 

Na stránce **Dimenze rozpočtování**, je nutné vybrat finanční dimenze, které se používají pro rozpočtování na základě dimenzí použitých v účtové osnově. Můžete vybrat všechny finanční dimenze nebo pouze jejich podsadu pro rozpočtování.

Definujte *rozpočtový model*, který odpovídá všem nebo některým rozpočtům. Jediný rozpočtový model můžete použít pro všechny položky registru rozpočtu. Alternativně můžete vytvořit samostatné modely, které jsou založeny na typu rozpočtu, geografickém umístění nebo nějakém jiném způsobu, jak je možné rozpočet klasifikovat. 

> [!NOTE] 
> Pokud je používána kontrola rozpočtu, je možné přiřadit pouze jeden rozpočtový model konkrétnímu časovému intervalu rozpočtového cyklu. 

Vytvořte *kódy rozpočtu*, které určují typ transakcí rozpočtu pro záznam a všechny související workflow. Kódy rozpočtu mohou podporovat následující typy rozpočtu:

-   Původní rozpočet
-   Převést
-   Revize
-   Břemeno
-   Předběžné břemeno
-   Přenesený rozpočet

Kódy rozpočtu umožňují mít záznam auditu schválených úprav rozpočtu v průběhu kurzu rozpočtového cyklu. Pokud je workflow spojeno s kódem rozpočtu, bude k dispozici pro všechny položky registru rozpočtu, které používají tento kód rozpočtu, a kroky workflow musí být dokončeny dříve, než položka registru rozpočtu dosáhne fáze **Dokončeno**.  

Můžete také libovolně nastavit *pravidla převodu rozpočtu*. Pro použití pravidel převodu rozpočtu, vyberte možnost **Použít pravidla pro rozpočtové převody** na stránce **Parametry rozpočtu**. Když jsou používány pravidla převodu rozpočtu, když uživatel vytvoří dokument za použití kód rozpočtu typu **Převod**, zůstatky rozpočtu nebudou aktualizovány, pokud budou narušena pravidla převodu rozpočtu. Například můžete povolit dokumenty převodu rozpočtu, kde je převeden rozpočet výdajů mezi hlavní účty pro oddělení prodeje a marketingu, ale lze zabránit přenášení rozpočtu z nebo do daného oddělení, pokud nebylo uděleno schválení workflowu pro daný typ účetní položku rozpočtu.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Použití pracovní plochy a stránek s dotazy ke sledování rozpočtu a skutečných hodnot
Správce rozpočtu může kontrolovat aktuální stav rozpočtu v pracovním prostoru **Rozpočty hlavní knihy a prognózy**. Karty **Výdaje nad rozpočet** a **Výnosy pod rozpočtem** poskytují rychlý přehled o kombinacích finančních dimenzí, kde cíle rozpočtu nedosáhly nebo se blížily prahové hodnotě. Prahovou procentuální hodnotu rozpočtu a sady finančních dimenzí, které se používají na těchto kartách, můžete přizpůsobit klepnutím na možnost **Konfigurovat můj pracovní prostor**. Můžete klepnout na možnost **Manažeři jednotky** a zobrazíte pracovníky, kteří odpovídají za kombinace specifických finančních dimenzí, které jsou na těchto kartách vybrány. Například pokud vidíte, že rozpočet výdajů oddělení Operace překročí rozpočtový práh, lze snadno najít a kontaktovat správce oddělení operací a problém probrat. 

> [!NOTE] 
> Pole **Správce oddělenír** na stránce **Organizační jednotky** určuje, kteří manažeři podporují kombinace specifických finančních dimenzí. Klepněte na tlačítko **Zobrazit více** v dolní části karty a otevřete stránku s dotazy **Rozpočet a skutečné hodnoty** s dalšími podrobnostmi o částkách rozpočtu versus skutečných částkách. 

Ze stránky s dotazy **Rozpočet a skutečné hodnoty** můžete přejít na podrobné informace o rozpočtu versus skutečných částkách. Vyberte řádek stránky s dotazy a pak klepněte na možnost **Zůstatky za období** a zobrazíte rozpočet a skutečné částky rozdělené do fiskálních období. Stránka **Účetní položky rozpočtu** poskytují přecházení k podrobnostem o rozpočtových částkách v položkách registru rozpočtu. Stránka **Položky hlavního deníku** otevře transakce hlavní knihy, které jsou zahrnuty do vypočítané částky **skutečné hodnoty**. 

Společnost, která používá funkci plánování rozpočtu může vytvořit a použít *prognózy rozpočtu *v pracovním prostoru **Rozpočty hlavní knihy a prognózy**.




