---
title: "Šablony se plánování rozpočtu pro Excel"
description: "Toto téma popisuje, jak vytvořit šablony aplikace Microsoft Excel, které lze použít pro plány rozpočtu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 0e2eb6e7c130f03edbf60a185d397d94b5d61d7d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-templates-for-excel"></a>Šablony se plánování rozpočtu pro Excel

[!include[banner](../includes/banner.md)]


Toto téma popisuje, jak vytvořit šablony aplikace Microsoft Excel, které lze použít pro plány rozpočtu.

Toto téma ukazuje, jak vytvořit šablony aplikace Excel, které budou použity s plány rozpočtu pomocí standardní Ukázková sada dat a přihlašovací jméno uživatele Admin. Další informace o plánování rozpočtu naleznete v tématu [přehled plánování rozpočtu.](budget-planning-overview-configuration.md) Můžete také sledovat [rozpočtové plánování 101](budget-plan.md) kurz naučit základní modul zásad konfigurace a použití.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Generovat listu pomocí rozvržení dokumentu plánu rozpočtu
Dokumenty plánu rozpočtu lze zobrazit a upravit pomocí jednoho nebo více rozložení. Každé zobrazení může mít šablonu dokumentu přidružené rozpočtu plánu můžete zobrazit a upravit data plánu rozpočtu v listu aplikace Excel. V tomto tématu budou generovány šablonu dokumentu plánu rozpočtu pomocí stávající konfigurace rozložení. Otevřít **seznam plánů rozpočtu** (**rozpočtování**&gt;**plány rozpočtu**). Klepněte na tlačítko **nové** Chcete-li vytvořit nový dokument plánu rozpočtu. [![bpt1](./media/bpt11-1024x552.png)](./media/bpt11.png) 

Použití **přidat** řádku možnost přidávat řádky. Klepněte na tlačítko **rozložení** Chcete-li zobrazit konfiguraci rozvržení dokumentu plánu rozpočtu. 
[![bpt2](./media/bpt2-1024x274.png)](./media/bpt2.png) 

Můžete zkontrolovat konfiguraci rozvržení a podle potřeby upravit. Přejít na **šablony**&gt;**generovat** k vytvoření souboru aplikace Excel pro toto rozložení. Po šablona je vytvořena, přejděte k **šablony**&gt;**zobrazení** otevřít a zobrazit dokument šablony plánu rozpočtu. Ukládáte soubor aplikace Excel na místní jednotku. [![bpt3](./media/bpt3-1024x545.png)](./media/bpt3.png) 

> [!NOTE] 
> Poté, co je s ním související šablonu aplikace Excel nelze upravovat rozložení dokumentu plánu rozpočtu. Chcete-li změnit rozložení, odstranit přidružený soubor šablony aplikace Excel a obnovit ji. To je nutné, aby pole v rozložení a synchronizovat listu. 

Šablona aplikace Excel bude obsahovat všechny prvky z rozložení dokumentu plánu rozpočtu, kde **k dispozici v listu** sloupce je nastavena na hodnotu True. Překrývající se prvky nejsou povoleny v šabloně aplikace Excel. Například pokud rozvržení obsahuje žádost Q1, Q2 žádost, žádost Q3 a Q4 žádost sloupce a sloupec celkový požadavek, který představuje součet všech sloupců 4 čtvrtletní, čtvrtletní sloupce nebo sloupec celkem je k dispozici pro použití v šabloně aplikace Excel. Soubor aplikace Excel nelze aktualizovat sloupce překrývající se během aktualizace, protože data v tabulce může být zastaralé a nepřesné.

[![bpt4](./media/bpt4-1024x615.png)](./media/bpt4.png)

> [!NOTE] 
> Chcete-li předejít problémům s zobrazení a úpravy dat plánu rozpočtu pomocí aplikace Excel, stejný uživatel protokolovány do obou 365 Dynamics pro operace a datový konektor Microsoft Dynamics Office Add-in.

## <a name="add-a-header-to-budget-plan-document-template"></a>Přidat záhlaví dokumentu šablony plánu rozpočtu
Chcete-li přidat informace záhlaví, vyberte horní řádek v souboru aplikace Excel a vložit prázdné řádky. Klepněte na tlačítko **návrh** v **datový konektor** Chcete-li přidat pole záhlaví souboru.

[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png) 

V **návrh** kartu, ** ** klepněte na **přidat** pole a pak vyberte **tabulek BudgetPlanHeader** jako zdroj dat entity.

[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)

Kurzor přejděte do požadovaného umístění v souboru aplikace Excel. Klepněte na tlačítko **přidat popisek** Chcete-li přidat popisek daného pole do vybraného umístění. Vyberte **přidat hodnotu** Chcete-li přidat pole hodnota na vybrané místo. Klepněte na **v** zavřete návrháře.

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[![bpt7](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Přidat vypočítaný sloupec do tabulky Šablona dokumentu plánu rozpočtu
--------------------------------------------------------------

Další, vypočítané sloupce bude přidán do šablony dokumentu generovaného rozpočtu plánu. A **celkový požadavek** sloupec, který obsahuje souhrn požadavku Q1: Q4 požadavku sloupce a **úprava** sloupec, který přepočítá **celkový požadavek** sloupec faktorem předdefinovaného.

Klepněte na tlačítko **návrh** v **datový konektor** Chcete-li přidat sloupce do tabulky. Klepněte na tlačítko **úprava** u **BudgetPlanWorksheet** zdroj dat ke spuštění, přidání sloupců.

[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png) 

Vybranou skupinu polí zobrazí sloupce, které jsou k dispozici v šabloně. Klepněte na tlačítko **vzorec** Chcete-li přidat nový sloupec. Zadejte název nového sloupce a poté vložit do vzorce **vzorec** pole. Klepněte na tlačítko **aktualizace** Chcete-li vložit sloupec.

[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> Definovat vzorec, vytvořte vzorec v tabulce a zkopírujte jej **návrh** okna. Dynamics 365 pro operace vázané tabulky se obvykle nazývá "AXTable1". Například sumarizovat požadovat Q1: požadovat Q4 sloupce v tabulce vzorec = AxTable1\[požadovat Q1\]+ AxTable1\[požadovat Q2\]+ AxTable1\[Q3 požádat o\]+ AxTable1\[požadovat Q4\].

Opakujte tyto kroky pro vložení **úprava** sloupec. Pomocí vzorce = AxTable1\[celkový požadavek\]\*$I$ 1 v tomto sloupci. To bude trvat hodnotu v buňce I1 a násobení hodnot v **celkový požadavek** sloupec pro výpočet částek úprav.

Uložte a zavřete soubor aplikace Excel. Vrátit do Dynamics 365 pro operace a v **rozložení**, klepněte na tlačítko **šablony &gt;odeslat** odešlete uloženou šablonu aplikace Excel má být použit pro plán rozpočtu. 

[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Zavřít **rozložení** jezdce. V **plán rozpočtu** dokumentu, klepněte na tlačítko **listu** Chcete-li zobrazit a upravit dokument v aplikaci Excel. Všimněte si, že upravené šablony aplikace Excel byla použita k vytvoření tohoto listu plánu rozpočtu a výpočtových sloupcích jsou aktualizovány pomocí vzorců, které byly definovány v předchozích krocích. 

[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Tipy a triky pro vytvoření šablony plánu rozpočtu
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Můžete přidávat a používat další zdroje dat pro šablony plánu rozpočtu?

Ano, lze použít **návrh** nabídky Chcete-li přidat další subjekty na stejné nebo jiné listy v šabloně aplikace Excel. Například můžete přidat **BudgetPlanProposedProject** zdroj dat, vytvořit a udržovat seznam navrhovaných projektů současně při práci s rozpočtu plán data v aplikaci Excel. Poznámka: včetně zdroje velkých objemů dat může ovlivnit výkon aplikace Excel sešitu. 

Lze použít **filtr** možnost **datový konektor** doplnit další datové zdroje požadované filtry.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Skrýt možnosti návrhu v datový konektor pro ostatní uživatele

Ano, otevřete **datový konektor** možnosti skrýt **návrh** možnost od jiných uživatelů.

[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)

Rozbalte položku **možnosti spojnice Data** a zrušte **povolení návrhu** políčko. To bude skrýt **návrh** možnost z **datový konektor**.

[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Můžete zabránit uživatelům v náhodou zavřením datový konektor při práci s daty?

Doporučujeme zamykání šablonu, kterou chcete uživatelům zabránit v jeho zavření. Zámek zapnout, klepněte na tlačítko **datový konektor**, v pravém horním rohu se zobrazí šipka. 

[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Klepněte na šipku pro další nabídky. Vyberte **Zámek**.

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Můžete použít jiné funkce aplikace Excel, například formátování buněk, barvy, podmíněné formátování a grafy s šablony plánu rozpočtu

Ano, většinu standardních funkcí aplikace Excel bude pracovat v šablony plánu rozpočtu. Doporučujeme používat barevné označení pro uživatele k rozlišení mezi sloupce jen pro čtení a upravitelné. Podmíněné formátování umožňuje zvýraznit problematické oblasti rozpočtu. Součty sloupců lze snadno předložit pomocí standardního vzorce aplikace Excel nad tabulkou.

Můžete také vytvořit a použít kontingenční tabulky a grafy pro další seskupení a vizualizace dat rozpočtu. Na **dat** karta v **připojení** skupinu, klepněte na tlačítko **Aktualizovat vše**a potom klepněte na tlačítko **vlastnosti připojení**. Klepněte **využití** kartu. Podle **aktualizace**, vyberte **aktualizovat data při otevření souboru** políčko. 

[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)




