---
title: "Přehled rozpočtování"
description: "Téměř všechny společnosti, která používá funkci Finance v Microsoft Dynamics 365 pro operace budou mít možnost vytvářet sestavy Rozpočtové vs. skutečné hodnoty. Tento článek popisuje minimální konfiguraci, která je nezbytná pro vytváření rozpočtů v 365 Dynamics pro operace nebo je můžete načíst z jiného programu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 60113
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a639e509cf6a3d2f1b850f27481d7b95546522b8
ms.openlocfilehash: b62e14f7c91692ae97bb332b38b0deeb328cc1bd
ms.lasthandoff: 03/31/2017


---

# <a name="budgeting-overview"></a>Přehled rozpočtování

[!include[banner](../includes/banner.md)]


Téměř všechny společnosti, která používá funkci Finance v Microsoft Dynamics 365 pro operace budou mít možnost vytvářet sestavy Rozpočtové vs. skutečné hodnoty. Tento článek popisuje minimální konfiguraci, která je nezbytná pro vytváření rozpočtů v 365 Dynamics pro operace nebo je můžete načíst z jiného programu.

<a name="overview"></a>Přehled
--------

Schválený rozpočet pro právnickou osobu je udržován v dokumentu, který je označován jako *položka registru rozpočtu*. Řádky v dokumentu položky rejstříku rozpočtu jsou známé jako *účet rozpočtu* položky a obsahují informace o finanční dimenzi, data a výše schváleného rozpočtu. Dokument položky rejstříku rozpočtu je integrována do základní finanční výkazy a dotaz na stránky, kde jsou knihy skutečné částky ve srovnání s částkami rozpočtu. 

Existuje několik metod pro vytvoření položky registru rozpočtu v 365 Dynamics pro operace:

-   Ručně zadat informace o dokumentu na stránce **položky registru rozpočtu**.
-   Použít šablonu aplikace Microsoft Excel, kterou lze otevřít klepnutím na tlačítko **Otevřít v aplikaci Excel**na stránce **položky registru rozpočtu**.
-   Použití datovou entitu **účetní položky rozpočtu** v modulu Správa dat pro import položek registru rozpočtu. Měli byste zvážit použití této metody a zapnutí **nastaveny na základě** ** zpracování ** parametr, když je nutné importovat mnoho položek účtu rozpočtu do systému.
-   Pokud společnost používá funkci plánování rozpočtu pro přípravu dat rozpočtu, můžete použít periodické zpracování **Generovat položku registru rozpočtu**.

Položka registru rozpočtu, je považován za dokončený, po aktualizaci zůstatků rozpočtu. Na **položky registru rozpočtu** klepněte na tlačítko **aktualizovat zůstatky rozpočtu** pro vybraný rozpočtový registrovat položku nebo více položek. Po provedení aktualizace zůstatků rozpočtu se stav položky rozpočtu registru změní na **Dokončeno**. Dokončená položka registru rozpočtu nemůže být znovu otevřena pro úpravy. Proto, chcete-li upravit data rozpočtu, musíte vytvořit novou položku registru rozpočtu namísto opravy dat v dokončené položce registru rozpočtu.

## <a name="configuration"></a>Konfigurace
Při konfiguraci rozpočtování začněte na stránce **Parametry rozpočtování**. Na této stránce je nutné definovat deník rozpočtu, číselnou řadu pro položky registru rozpočtu a výchozí nastavení v pracovních prostorách.

Dále pokud existují zásady, které řídí schválení položek registru rozpočtu v závislosti na typu rozpočtu (například převody nebo revize), je nutné vytvořit workflow položek registru rozpočtu na stránce **Workflowy rozpočtování**. Pokud jsou scénáře, kde mohou být převody povoleny bez schválení workflow, můžete definovat pravidla převodu rozpočtu pro podporu těchto scénářů. 

Na stránce **Dimenze rozpočtování**, je nutné vybrat finanční dimenze, které se používají pro rozpočtování na základě dimenzí použitých v účtové osnově. Můžete vybrat všechny finanční dimenze nebo pouze jejich podsadu pro rozpočtování.

Definovat * rozpočtový model *, který odpovídá všechny nebo některé rozpočty. Jediný rozpočtový model můžete použít pro všechny položky registru rozpočtu. Alternativně můžete vytvořit samostatné modely, které jsou založeny na typu rozpočtu, geografickém umístění nebo nějakém jiném způsobu, jak je možné rozpočet klasifikovat. 

> [!NOTE] 
> Pokud je použít kontrolu rozpočtu, můžete přidružit pouze jeden model rozpočtu rozpočet cyklu časové rozpětí. 

Vytvořte *kódy rozpočtu*, které určují typ transakcí rozpočtu pro záznam a všechny související workflow. Kódy rozpočtu mohou podporovat následující typy rozpočtu:

-   Původní rozpočet
-   Převést
-   Revize
-   Břemeno
-   Předběžné břemeno
-   Přenesený rozpočet

Kódy rozpočtu umožňují mít záznam auditu schválených úprav rozpočtu v průběhu kurzu rozpočtového cyklu. Pokud pracovní postup je spojen s kód rozpočtu, pracovní postup bude povoleno pro všechny položky registru rozpočtu, které používají tento kód rozpočtu a kroky pracovního postupu musí být vyplněna před položky registru rozpočtu lze kontaktovat **dokončeno** fáze.  

Volitelně také můžete nastavit *pravidla převodu rozpočtu*. Chcete-li použít pravidla převodu rozpočtu, vyberte **použít pravidla pro rozpočtové převody** na **parametry rozpočtu** stránky. Když jsou používány pravidla převodu rozpočtu, když uživatel vytvoří dokument za použití kód rozpočtu typu **Převod**, zůstatky rozpočtu nebudou aktualizovány, pokud budou narušena pravidla převodu rozpočtu. Například můžete povolit dokumenty převodu rozpočtu, kde je převeden rozpočet výdajů mezi hlavní účty pro oddělení prodeje a marketingu, ale lze zabránit přenášení rozpočtu z nebo do daného oddělení, pokud nebylo uděleno schválení workflowu pro daný typ účetní položku rozpočtu.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Použití pracovní plochy a stránek s dotazy ke sledování rozpočtu a skutečných hodnot
Správce rozpočtu může kontrolovat aktuální stav rozpočtu v pracovním prostoru**Rozpočty hlavní knihy a prognózy**. Karty **Výdaje nad rozpočet** a **Výnosy pod rozpočtem** poskytují rychlý přehled o kombinacích finančních dimenzí, kde cíle rozpočtu nedosáhly nebo se blížily prahové hodnotě. Prahovou procentuální hodnotu rozpočtu a sady finančních dimenzí, které se používají na těchto kartách, můžete přizpůsobit klepnutím na možnost **Konfigurovat můj pracovní prostor**. Můžete klepnout na možnost **Manažeři jednotky** a zobrazíte pracovníky, kteří odpovídají za kombinace specifických finančních dimenzí, které jsou na těchto kartách vybrány. Například pokud vidíte, že rozpočet výdajů oddělení Operace překročí rozpočtový práh, lze snadno najít a kontaktovat správce oddělení operací a problém probrat. 

> [!NOTE] 
> **Vedoucí oddělení** v **organizační jednotky** stránky určuje vedoucí, které podporují kombinace určitých finančních dimenzí. Klepněte na tlačítko **Zobrazit více** v dolní části karty a otevřete stránku s dotazy **Rozpočet a skutečné hodnoty** s dalšími podrobnostmi o částkách rozpočtu versus skutečných částkách. 

Ze stránky s dotazy **Rozpočet a skutečné hodnoty** můžete přejít na podrobné informace o rozpočtu versus skutečných částkách. Vyberte řádek stránky s dotazy a pak klepněte na možnost **Zůstatky za období** a zobrazíte rozpočet a skutečné částky rozdělené do fiskálních období. Stránka **Účetní položky rozpočtu** poskytují přecházení k podrobnostem o rozpočtových částkách v položkách registru rozpočtu. Stránka **Položky hlavního deníku **otevře transakce hlavní knihy, které jsou zahrnuty do vypočítané částky **skutečné hodnoty**. 

Společnost, která používá funkci plánování rozpočtu může vytvořit a použít *prognózy rozpočtu *v pracovním prostoru **Rozpočty hlavní knihy a prognózy**.




