---
title: Šablony plánování rozpočtu pro Excel
description: Toto téma popisuje, jak vytvořit šablony aplikace Microsoft Excel, které lze použít pro plány rozpočtu.
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanSetLayout
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4deba271912d3495ac08cd6a65c2b2f9c6a04850
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188572"
---
# <a name="budget-planning-templates-for-excel"></a>Šablony plánování rozpočtu pro Excel

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vytvořit šablony aplikace Microsoft Excel, které lze použít pro plány rozpočtu.

Toto téma ukazuje, jak vytvořit šablony aplikace Excel, které budou použity s plány rozpočtu pomocí standardní sady ukázkových dat a přihlášení uživatele admin. Další informace o plánování rozpočtu naleznete v tématu [Přehled plánování rozpočtu.](budget-planning-overview-configuration.md) Můžete také postupovat podle kurzu [Plánování rozpočtu 101](budget-plan.md) a naučit se konfiguraci základního modulu a zásady a použití.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Vygenerování listu pomocí rozvržení dokumentu plánu rozpočtu

Dokumenty plánu rozpočtu lze zobrazit a upravit pomocí jednoho nebo více rozvržení. Každé rozvržení může mít přidruženou šablonu dokumentu rozpočtu plánu pro zobrazení a úpravy dat plánu rozpočtu v listu aplikace Excel. V tomto tématu budou generovány šablonu dokumentu plánu rozpočtu pomocí stávající konfigurace rozvržení. 

1. Otevřete **Seznam plánů rozpočtu** (**Rozpočtování** &gt; **Plány rozpočtu**). 
2. Kliknutím na možnost **Nový** vytvořte nový dokument plánu rozpočtu. 

   [![Seznam plánů rozpočtu](./media/bpt11-1024x552.png)](./media/bpt11.png) 

3. Použijte možnost řádku **Přidat** k přidání řádků. Klikněte na možnost **Rozvržení**, abyste zobrazili konfiguraci rozvržení dokumentu plánu rozpočtu. 

   [![Přidání plánů rozpočtu](./media/bpt2-1024x274.png)](./media/bpt2.png) 

Můžete zkontrolovat konfiguraci rozvržení a podle potřeby ji upravit. 
1. Přejděte na možnosti **Šablona**&gt;**Generovat** k vytvoření souboru aplikace Excel pro toto rozvržení. 
2. Po vytvoření šablony přejděte na položky **Šablona**&gt;**Zobrazit** a otevřete a zkontrolujte šablonu dokumentu plánu rozpočtu. Soubor aplikace Excel můžete uložit na místní disk. 

[![Uložit jako](./media/bpt3-1024x545.png)](./media/bpt3.png)

> [!NOTE] 
> Poté, co přidružíte k rozvržení dokumentu plánu rozpočtu šablonu aplikace Excel, nemůžete už rozvržení upravovat. Chcete-li změnit rozvržení, odstraňte přidružený soubor šablony aplikace Excel a vygenerujte ho znovu. Tato možnost je vyžadována pro zachování polí v rozvržení a synchronizaci listů. 

Šablona aplikace Excel bude obsahovat všechny prvky z rozložení dokumentu plánu rozpočtu, kde sloupec **Dostupné v listu** je nastaven na hodnotu True. Překrývající se prvky nejsou v šabloně aplikace Excel povoleny. Například pokud rozvržení obsahuje sloupce Žádost na 1. čtvrtletí, Žádost na 2. čtvrtletí, Žádost na 3. čtvrtletí a Žádost na 4. čtvrtletí a sloupec celkového požadavku, který představuje součet všech čtyřech sloupců čtvrtletí, lze v šabloně aplikace Excel použít pouze čtvrtletní sloupce nebo sloupec součtu. Soubor aplikace Excel nemůže aktualizovat překrývající se sloupce se během aktualizace, protože data v tabulce by se mohla stát zastaralá a nepřesná.

[![Příklad](./media/bpt4-1024x615.png)](./media/bpt4.png)

> [!NOTE] 
> Chcete-li předejít možným problémům se zobrazením a úpravami dat plánu rozpočtu při použití aplikace Excel, měl by být přihlášen do aplikace Microsoft Dynamics 365 Finance a datového konektoru doplňku Microsoft Dynamics pro Office stejný uživatel.

## <a name="add-a-header-to-budget-plan-document-template"></a>Přidání záhlaví do šablony dokumentu plánu rozpočtu
Chcete-li přidat informace záhlaví, vyberte horní řádek v souboru aplikace Excel a vložte prázdné řádky. Klikněte na tlačítko **Návrh** v **datovém konektoru**, pokud chcete přidat pole záhlaví do souboru aplikace Excel.

[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png) 

Na kartě **Návrh** klikněte na pole **Přidat** a pak vyberte **BudgetPlanHeader** jako zdroj dat entity.

[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)

Kurzor přejděte do požadovaného umístění v souboru aplikace Excel. Chcete-li přidat popisek pole do vybraného umístění, klikněte na tlačítko **Přidat popisek**. Chcete-li přidat pole hodnoty na vybrané místo, zvolte možnost **Přidat hodnotu**. Kliknutím na tlačítko **Hotovo** ukončíte návrháře.

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[![bpt7](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Přidání vypočteného sloupce do tabulky šablony dokumentu plánu rozpočtu
--------------------------------------------------------------

Poté se přidají vypočtené sloupce do vygenerované šablony dokumentu rozpočtu plánu. Sloupec **Celkový požadavek**, který obsahuje souhrn sloupců požadavků na první až čtvrté čtvrtletí, a sloupec **Úprava**, který přepočítá sloupec **Celkový požadavek** předdefinovaným koeficientem.

Klikněte na tlačítko **Návrh** v **datovém konektoru**, pokud chcete přidat sloupce do tabulky. Klikněte na tlačítko **Upravit** vedle zdroje dat **BudgetPlanWorksheet** a začněte přidávat sloupce.

[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png) 

Vybraná skupina polí zobrazuje sloupce, které jsou k dispozici v šabloně. Kliknutím na **Vzorec** přidejte nový sloupec. Zadejte název nového sloupce a poté vložte vzorec do pole **Vzorec**. Kliknutím na položku **Aktualizovat** vložte sloupec.

[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> Abyste definovali vzorec, vytvořte vzorec v tabulce a zkopírujte ho do okna **Návrh**. Tabulka vázaná na aplikaci Finance and Operations se obvykle nazývá "AXTable1". Například k sumarizaci sloupců požadavků na první až čtvrté čtvrtletí v tabulce je vzorec = AxTable1\[Požadavek na 1. čtvrtletí\]+ AxTable1\[Požadavek na 2. čtvrtletí\]+ AxTable1\[Požadavek na 3. čtvrtletí\]+ AxTable1\[Požadavek na 4. čtvrtletí\].

Opakujte tyto kroky pro vložení sloupce **Úprava**. Použijte vzorec = AxTable1\[Celkový požadavek\]\*$I$ 1 pro tento sloupec. Vezme se hodnota v buňce I1 a vynásobí se hodnoty ve sloupci **Celkový požadavek** pro výpočet částek úprav.

Uložte a zavřete soubor aplikace Excel. V **Rozvržení** klikněte na **Šablona &gt; Odeslat** k odeslání uložené šablony aplikace Excel, která se použije pro plán rozpočtu. 

[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Zavřete posuvník **Rozvržení**. Chcete-li zobrazit a upravit dokument v aplikaci Excel, v dokumentu **Plán rozpočtu** klikněte na tlačítko **List**. Všimněte si, že upravená šablona aplikace Excel byla použita k vytvoření tohoto listu plánu rozpočtu a vypočtené sloupce jsou aktualizovány pomocí vzorců, které byly definovány v předchozích krocích. 

[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Tipy a triky pro vytvoření šablon plánu rozpočtu
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Mohu přidávat a používat další zdroje dat pro šablonu plánu rozpočtu?

Ano. Chcete-li přidat další entity do stejného nebo jiných listů šablony aplikace Excel, můžete použít nabídku **Návrh**. Můžete například přidat zdroj dat **BudgetPlanProposedProject** a vytvořit a udržovat tak seznam navrhovaných projektů současně při práci s daty plánu rozpočtu v aplikaci Excel. Pamatujte, že pokud zahrnete zdroje dat s velkým objemem, může to ovlivnit výkon sešitu aplikace Excel. 

Můžete použít možnost **Filtr** v **datovém konektoru**, abyste přidali požadované filtry k dalším zdrojům dat.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Můžu skrýt možnost návrhu v datovém konektoru pro ostatní uživatele?

Ano. Otevřete možnosti **datového konektoru** a skryjte možnost **Návrh** před jinými uživateli.

[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)

Rozbalte **Možnosti datového konektoru** a zrušte zaškrtávací políčko **Povolit návrh**. Tato akce skryje možnost **Návrh** z **datového konektoru**.

[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Můžu zabránit uživatelům v náhodném uzavření datového konektoru během práce s daty?

Doporučujeme šablonu uzamknout, abyste zabránili uživatelům v jejím uzavření. Zámek zapnete kliknutím na **Datový konektor**. V pravém horním rohu se zobrazí šipka. 

[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Klikněte na šipku pro další nabídku. Vyberte **Uzamknout**.

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Můžu použít jiné funkce aplikace Excel, jako například formátování buněk, barvy, podmíněné formátování a grafy pro moje šablony plánu rozpočtu?

Ano, většina standardních funkcí aplikace Excel bude fungovat i v šablonách plánu rozpočtu. Doporučujeme používat barevné kódy pro uživatele k rozlišení mezi sloupci jen pro čtení a sloupci, které lze upravit. Podmíněné formátování lze použít ke zvýraznění problematických oblastí rozpočtu. Součty sloupců lze snadno získat pomocí standardních vzorců aplikace Excel nad tabulkou.

Můžete také vytvořit a použít kontingenční tabulky a grafy pro další seskupení a vizualizace dat rozpočtu. Na kartě **Data** ve skupině **Připojení** klikněte na tlačítko **Aktualizovat vše** a potom klikněte na tlačítko **Vlastnosti připojení**. Klikněte na kartu **Použití**. Pod možností **Aktualizovat** zvolte zaškrtávací políčko **Aktualizovat data při otevření souboru**. 

[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)



