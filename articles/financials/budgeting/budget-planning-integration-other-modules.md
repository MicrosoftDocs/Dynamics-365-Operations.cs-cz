---
title: "Integrace plánování rozpočtu s jinými moduly"
description: "Plány rozpočtu lze vytvořit z několika různých zdrojů. Základní prvky periodického zpracování jsou stejné pro všechny zdroje."
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanGenerate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 64443
ms.assetid: f9a94db5-906c-404a-9ca5-91528d67c490
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4a18190152b6e5ea520a81f1db2cf67ded652bbe
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="budget-planning-integration-with-other-modules"></a>Integrace plánování rozpočtu s jinými moduly

[!include [banner](../includes/banner.md)]

 Plány rozpočtu lze vytvořit z několika různých zdrojů. Základní prvky periodického zpracování jsou stejné pro všechny zdroje. 



<a name="periodic-processes-for-generating-budget-plans"></a>Periodické procesy pro generování plánů rozpočtu
----------------------------------------------

Plány rozpočtu lze vytvořit z následujících zdrojů:

-   Transakce hlavní knihy
-   Dlouhodobý majetek
-   Pozice prognóz
-   Prognózy projektu
-   Prognózy dodávek
-   Prognózy poptávky
-   Položky registru rozpočtu
-   Jiné plány rozpočtu

Základní prvky periodického zpracování jsou stejné u všech procesů. Karty umožňují definovat zdroj dat, cílové atributy (plán rozpočtu) a možnosti spuštění procesu na pozadí jako dávkový proces. Dále v tomto článku jsou popsány položky, které nemusí být viditelné v jednotlivých procesech.

### <a name="actions"></a>Akce

Pro každý proces generování jsou k dispozici tři akce:

-   **Vytvořit nový plán rozpočtu** – vytvoření nového plánu s atributy, které jsou vybrány v části **Cíl**. Tyto atributy nemusí být jedinečné. Dva plány mohou tudíž být se stejným názvem a jinými hodnotami.
-   **Nahradit existující scénář plánu rozpočtu** – odstranění všech dat v cílovém plánu rozpočtu ve vybraném scénáři plánu rozpočtu a vytvoření nových řádků, které používají vybraná zdrojová data.
-   **Aktualizovat existující scénář plánu rozpočtu a připojit nová data** – aktualizace existujících řádků v cílovém plánu, které odpovídají původním řádkům, a také přidání nových řádků pro nová data. Párování vychází z účtu hlavní knihy, data, třídy rozpočtu a různých ostatních polí. Například při vytvoření plánů rozpočtu z pozic prognózy je číslo pozice důležité pole. Všechny řádky, které mají číslo pozice odpovídající číslu zdrojové pozice, budou nahrazeny novými řádky ze zdroje.

### <a name="source"></a>Zdroj

Karta **Zdroj** umožňuje filtrovat data pomocí tlačítka **filtr** pro všechny procesy. Určitá pole jsou ve výchozím nastavení přidána do filtru pro každý proces. Například pro proces **Generovat plán rozpočtu z hlavní knihy** jsou k dispozici kategorie **Účet hlavní knihy** a **Hlavní účet** a jsou k dispozici na stránce generování. Všechna pole, která přidáte do filtru, jsou přidány také na stránku společně s kritérii, která můžete přidávat.

### <a name="target"></a>Cíl

Možnost **Historie** na kartě **Cíl** umožňuje použití dat ze zdrojových dat, jako počáteční datum v plánu rozpočtu. Datum platnosti obvykle musí být v rozpočtovém cyklu plánu. Při nastavení možnosti **Historie** na **Ano** se použije datum (i rok) ze zdroje, takže můžete použít minulá data jako základ pro srovnání. Historická data nemůžete měnit v plánu rozpočtu a plán je nastaven na stav Schválený workflow. Můžete však podle potřeby vynulovat stav, pokud ostatní scénáře v plánu vyžadují změny.

Pole **Agregovat součet podle** v horní části stránky také určuje datum, které je použito. Toto pole je součet částek a volitelně nastaví datum platnosti na první den fiskálního období nebo fiskálního roku. 

Mnoho polí na kartě <strong>Cíl</strong> lze upravit nebo je jen pro čtení – v závislosti na akci, kterou jste vybrali. Při změně z vytváření nového plánu rozpočtu na aktualizaci existujícího plánu pole **Název plánu rozpočtu** nebude k dispozici a pole, která se vztahují k výběru existujícího plánu, bude k dispozici. Na obou kartách **Cíl** i **Zdroj** je pole **Hlavní kniha** vždy k dispozici, protože hodnota vychází z vybraného procesu plánování rozpočtu. 

Pole **Třída rozpočtu** umožňuje nastavit řádky plánu rozpočtu jako výdajové transakce nebo transakce výnosů. Transakce výnosů se obvykle připíší na účet hlavní knihy a jsou tedy uloženy jako záporné. Obvykle se tyto transakce také zobrazí jako záporné částky v plánu rozpočtu. Přidáním třídy rozpočtu jako pole v rozvržení pro plán však můžete povolit výnosy, aby se zobrazily jako kladné množství.

### <a name="generation-rules"></a>Pravidla generování

Tři pole zajišťují dodatečné funkce: **Koeficient**, **Minimální** a **Zaokrouhlení** (**pravidlo**). 

Hodnota v poli **Koeficient** je vynásobena zdrojovou částkou za účelem nastavení částky v plánu rozpočtu. Úpravy lze provádět při vytvoření řádků plánu rozpočtu. Můžete například zadat **1,03** pro zvýšení o 3 %. Koeficient musí být kladné číslo. 

Pole **Minimální** umožňuje nastavit prahovou částku pro vytváření řádku plánu rozpočtu. Pokud je zdrojová částka nižší než tato hodnota, nedojde k vytvoření řádku plánu rozpočtu. Hodnota **0,00** umožňuje použít všechny částky, ale neomezuje řádky na kladné částky. (Žádná hodnota neomezuje řádky na kladné částky. Záporné částky jsou vždy zahrnuty a obvykle představují kreditní položky.)

Pole **Pravidlo zaokrouhlení** umožňuje nastavení přesnosti řádků plánu rozpočtu, které jsou vytvořeny. Můžete zaokrouhlit množství na nejbližší násobek měny 1,00, 10,00, 100,00 a tak dále.

## <a name="notes-for-specific-processes"></a>Poznámky k specifickým procesům
### <a name="generate-budget-plan-from-general-ledger"></a>Generovat plán rozpočtu z hlavní knihy

Pokud vytváříte plán rozpočtu z dat hlavní knihy, je nutné nastavit pole **Agregovat součet podle** na **Fiskální rok**, pokud je možnost **Historie** nastavena na **Ne**. Období a data ve zdroji se nemusí shodovat s obdobím a daty v cíli. Vzhledem k tomu, že proces nemá spolehlivý způsob mapování těchto hodnot, musíte omezit proces na první rok. 

V cíli je pole **Třída rozpočtu** nastaveno na hodnotu **Výdaje** nebo **Výnosy**. Toto nastavení se používá k výběru atributu **Typ rozpočtu** pro vytvořené řádky, pokud není hlavní účet na řádku typu **Výnosy** nebo **Výdaje**.

### <a name="generate-budget-plan-from-fixed-assets"></a>Generovat plán rozpočtu z dlouhodobého majetku

Proces **Generovat plán rozpočtu z dlouhodobého majetku** nemá možnost agregace podle období nebo dne. Zároveň neexistuje možnost nastavení plánu jako historického. Tento periodický proces můžete použít pro zahrnutí očekávané transakce pro dlouhodobý majetek v plánování rozpočtu.

### <a name="generate-budget-plan-from-forecast-positions"></a>Generovat plán rozpočtu z pozic prognóz

Proces **Generovat plán rozpočtu z pozic prognóz** přiřadí zdrojové pozice prognózy k řádku plánu rozpočtu. Pokud chcete zobrazit pozici, můžete přidat pozici prognózy jako řádek v rozvržení pro plán rozpočtu, nebo použít dotaz **Řádky plánu rozpočtu**. Pokud nechcete, aby se pozice prognózy přiřadila k řádkům plánu rozpočtu, nastavte možnost **Zahrnout pozici v řádku plánu rozpočtu** na **Ne**.

Řádky v plánu rozpočtu se agregují podle účtu hlavní knihy a pozice. Číslo pozice je však možné vyloučit tak, aby řádky byly seskupeny pouze podle účtu hlavní knihy. Na kartě **Cíl** nastavte možnost **Zahrnout pozici v plánu rozpočtu** na **Ne**.

V poli **Scénář FTE plánu rozpočtu** můžete vybrat scénář a zahrnout počet ekvivalentu plného pracovního úvazku do plánu rozpočtu. Toto pole je omezeno na scénáře typu množství, které jsou zahrnuty v rozvržení cílového plánu rozpočtu. Když vyberete scénář FTE, je také nutné určit hlavní účet FTE. Tento účet se používá k vytvoření řádků plánu rozpočtu množství. 

Proces plánování rozpočtu a scénář plánu rozpočtu, které jsou vybrané ve zdroji, určují proces plánování rozpočtu cílového scénáře a scénář. Vzhledem k tomu, že tyto atributy jsou přiřazeny k pozicím prognózy, musí být srovnány s plánem rozpočtu. Atributy proto nemohou být upraveny v cíli.

### <a name="generate-budget-plan-from-project-forecasts"></a>Generovat plán rozpočtu z prognóz projektů

Proces **Generovat plán rozpočtu z prognóz projektu**, stejně jako proces **Generovat plán rozpočtu z pozic prognóz**, umožňuje zahrnout množství projektu (hodiny, výdaje a položky) do scénáře množství. Dva procesy mají také podobné filtry pro sloupce v rozvržení pro plán rozpočtu. 

Na kartě **Zdroj** jsou tři možnosti v části **Zahrnout výkaz**, které určují, jaké řádky plánu rozpočtu jsou vytvořeny. Tyto volby jsou stejné jako možnosti, které jsou k dispozici při vytváření položek registru rozpočtu z prognóz projektu. Nastavte možnost **Zisk a ztráta** na **Ano** a vytvořte tak řádky pro náklady a výnosy. Nastavte možnost **NV** na **Ano** pro vytvoření položek typu "nedokončená výroba". Nastavte možnost **Přidělení mezd** na **Ano** a vytvořte tak řádky pro protiúčty mezd pro hodinové transakce. 

Neexistuje žádné pole **Třída rozpočtu**, protože třída rozpočtu (**Výdajů** nebo **Výnosy**) je určena zdrojem. 

Můžete použít rozpočty projektu jako zdroj výběrem modelu prognózy, který obsahuje částky projektového rozpočtu. Mějte na paměti, že projektové rozpočty vytvoří položky prognózy projektu při jejich schválení.

Pokud chcete vybrat pouze náklady nebo výnosy pro řádky plánu rozpočtu, použijte filtr a vyberte tak <strong>Aktualizace rozpočtu: typ částky = náklady</strong>. Pokud chcete vybrat pouze jeden typ prognózy, použijte filtr a vyberte <strong>Aktualizace rozpočtu: typ transakce = *xxx</strong>*. 

Pouze jeden model prognózy lze použít pro generování scénáře plánu rozpočtu. Pokud je spuštěn proces jednoho modelu prognózy a následně provedete aktualizaci a pokusíte se určit jiný model, první model bude přepsán v případě, že použijete stejný projekt a účet hlavní knihy. Pokud chcete generovat scénář plánu rozpočtu z více než jednoho modelu prognózy, generujte do jiných scénářů plánu rozpočtu a použijte možnosti přidělení pro jejich přidání do jiného scénáře. 

Proces **Generovat plán rozpočtu z prognóz projektů** přiřadí také zdrojový projekt k řádku plánu rozpočtu.

### <a name="generate-budget-plan-from-supply-forecast"></a>Generovat plán rozpočtu z prognózy dodávek

Možnosti filtru pro zdroj v procesu **Generovat plán rozpočtu z prognózy dodávek** byly modelovány podle možností ve funkci **Převod rozpočtu nákupu do hlavní knihy** z důvodu podobnosti mezi procesem a funkcí.

### <a name="generate-budget-plan-from-demand-forecast"></a>Generovat plán rozpočtu z prognózy poptávky

Pro proces **Generovat plán rozpočtu z prognózy poptávky** můžete nastavit možnost **Prodejní objednávka** na **Ano** a generovat tak řádky výnosu do plánu rozpočtu, nastavit **Spotřeba** na **Ano** a vytvořit tak řádky výdajů, nebo nastavit obě možnosti na **Ano**.

### <a name="generate-budget-plan-from-budget-register-entries"></a>Generovat plán rozpočtu z položek registru rozpočtu

Pro proces **Generovat plán rozpočtu z položek registru rozpočtu** musí zdroj určit jeden dílčí model, jeden kód rozpočtu a jedno číslo položky. Jinak řečeno můžete najednou vytvořit řádky plánu rozpočtu pro pouze jednu položku registru rozpočtu. Můžete použít další záznamy ve stejném plánu rozpočtu spuštěním procesu vždy pro každou položku zdroje.

### <a name="generate-budget-plan-from-budget-plan"></a>Generovat plán rozpočtu z plánu rozpočtu

Pro proces **Generovat plán rozpočtu z plánu rozpočtu** vám další sada možností na kartě **Cíl** umožní přiřadit nové finanční dimenze. Pokud je vybraná finanční dimenze, tato hodnota se použije pro všechny řádky plánu rozpočtu. Z toho vyplývá, že můžete použít jeden plán rozpočtu jako základ pro jiné plány rozpočtu, ale lze přiřadit například různá oddělení nebo nákladová střediska k novým plánům rozpočtu.

## <a name="looking-back-from-the-budget-plan"></a>Zpětné hledání z plánu rozpočtu
### <a name="budget-plans-by-dimension-set-inquiry"></a>Dotaz Plány rozpočtu podle sad dimenzí

Dotaz **Plány rozpočtu podle sad dimenzí** obsahuje několik možností, které umožňují spuštění dotazu pro lepší určení zdroje dat plánu rozpočtu. 

Vyberte řádek a klepnutím na tlačítko **Řádky plánu rozpočtu** spusťte dotaz **Řádky plánu rozpočtu**. Výsledky jsou filtrovány pro hodnoty dimenze vybraného řádku. Poté můžete použít další parametry. 

Ke spuštění těchto dotazů můžete použít tlačítka **Prognóza dodávky** a **Prognóza poptávky**. V obou případech dotaz hledá řádky prognózy, které by mohly vytvořit řádky plánu rozpočtu. 

Další sestavy, které jsou k dispozici, zahrnují sestavu **Pozice prognózy podle plánu rozpočtu**. Tato sestava je užitečná, pokud chcete určit, zda byla pozice správně přiřazena k plánům rozpočtu.




