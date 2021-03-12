---
title: Pracovní prostor řízení nákladů
description: Toto téma obsahuje informace o pracovním prostoru řízení nákladů. Tento pracovní prostor je centrálním místem, kde vedoucí pracovníci, kteří jsou zodpovědní za kontrolu objektu nákladů nebo sady objektů nákladů v rámci dimenze nebo napříč dimenzemi, mohou přistupovat k sestavám.
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostControlWorkspaceConfiguration, CAMCostControlWorkspace, CAMCostControlWorkspaceConfigurationPerUser
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3163975a8cc99c4b07fdbe03fa57ea6cfef53cd9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995208"
---
# <a name="cost-control-workspace"></a>Pracovní prostor řízení nákladů 

[!include [banner](../includes/banner.md)]

Pracovní prostor **Řízení nákladů** je centrálním místem, kde vedoucí pracovníci, kteří jsou zodpovědní za kontrolu objektu nákladů nebo sady objektů nákladů v rámci dimenze nebo napříč dimenzemi (například nákladovými středisky nebo skupinami produktů), mohou přistupovat k sestavám. Sestavy v pracovním prostoru jsou plně spravovány nákladovými účetními, aby rozvržení a data, která se používají k vykazování, byla konzistentní napříč celou organizací.

## <a name="cost-control-workspace-configuration"></a>Konfigurace pracovního prostoru řízení nákladů

Nákladoví účetní mohou definovat tolik konfigurací sestav, kolik potřebují pro požadované složení nebo rozvržení dat. Konfigurace sestav obsahuje šest částí, z nichž každá přispívá k výběru složení cílových dat a rozvržení.

Chcete-li nakonfigurovat pracovní prostor řízení nákladů, klikněte na **Nákladové účetnictví** \> **Nastavení** \> **Konfigurace pracovního prostoru řízení nákladů**.

### <a name="general"></a>Obecné

Na pevné záložce **Obecné** můžete vytvořit jedinečné rozvržení sestavy. Název sestavy bude jedinečný identifikátor, který uživatelé budou moci rozpoznat v pracovním prostoru **Řízení nákladů**. Můžete také určit, zda sestava bude sdílená nebo ponechána jako interní pro nákladové účetní.

| Pole       | popis |
|-------------|-------------|
| Jméno        | Zadejte jedinečný název rozvržení. |
| popis | Zadejte podrobný popis. |
| Publikováno   | Pokud nastavíte toto pole na **Ano**, uživatel, kterému je přiřazena jedna z následujících rolí, může zobrazit sestavu v pracovním prostoru **Řízení nákladů**:<ul><li>Správce nákladového účetnictví</li><li>Nákladový účetní</li><li>Úředník na pozici nákladového účetního</li><li>Kontrolor objektu nákladů</li></ul>Pokud nastavíte toto pole na **No**, pouze uživatelé, kterým je přiřazena jedna z následujících rolí, může zobrazit sestavu v pracovním prostoru **Řízení nákladů**:<ul><li>Správce nákladového účetnictví</li><li>Nákladový účetní</li><li>Úředník na pozici nákladového účetního</li></ul> |

### <a name="data-filtering"></a>Filtrování dat

Na pevné záložce **Filtrování dat** určete základ dat pro sestavu. Uživatelé této sestavy uvidí hodnoty na sestavě po zpracování zdrojových dat.

| Pole                                                             | popis |
|-------------------------------------------------------------------|-------------|
| Hlavní kniha nákladového účetnictví                                            | **Hlavní kniha nákladového účetnictví**, na které je sestava založena. Hodnota je odvozena od pole **Jednotka řízení nákladů**. |
| Jednotka řízení nákladů                                                 | Hodnota, kterou jste vybrali, určuje hlavní knihu nákladového účetnictví a objekty nákladů, na kterých je tato sestava založena. |
| Hierarchie statistické dimenze, Hierarchie dimenze prvku nákladů | Záznam konfigurace pracovního prostoru **Řízení nákladů** může vykázat buď nepeněžní nebo peněžní hodnoty, nikoliv však ve stejném rozvržení. Vyberte hodnotu v poli **Hierarchie dimenze prvku nákladů** pro vykázání peněžních hodnot. Vyberte hodnotu v poli **Hierarchie statistické dimenze** pro vykázání nepeněžních hodnot. Zvolený záznam hierarchie dimenze určuje strukturu úrovně vykazování a agregace.<blockquote>[!NOTE]<br>Chcete-li zobrazit nefinanční a finanční hodnoty vedle sebe, můžete exportovat data do aplikace Microsoft Excel pro balíček obsahu Microsoft Power BI.</blockquote> |
| Hierarchie dimenze objektu nákladů                                   | Vyberte hierarchii dimenze z dimenze objektu nákladů, který vyhovuje účelu vykazování, které definujete. |
| Původní verze rozpočtu                                           | Vyberte ID verze rozpočtu, která se chová jako původní rozpočet v rámci této sestavy. |
| Revidovaná verze rozpočtu                                            | Vyberte ID verze rozpočtu, která se chová jako revidovaný rozpočet v rámci této sestavy. |

### <a name="assign-calculation-records"></a>Přiřazení záznamů výpočtů

Výpočet režijních nákladů provádí několik kroků výpočtů na zdrojových datech, jako je například klasifikace chování nákladů, distribuce nákladů a přidělení nákladů. V případě, že byla objevena chybějící zdrojová data nebo je třeba aktualizovat pravidla, lze provést pro stejné fiskální období více výpočtů režijních nákladů. Každý výpočet režijních nákladů je uložen s jedinečným ID. Nákladový účetní může vybrat konkrétní ID výpočtu režijních nákladů. Uživatelé sestavy, jako je například vedoucí pracovníci, zobrazí výsledky výpočtu režijních nákladů v pracovním prostoru **Řízení nákladů**.

| Pole                  | popis |
|------------------------|-------------|
| Fiskální kalendářní období | Vyberte období fiskálního kalendáře, ke kterému přiřadíte ID výpočtu režijních nákladů.<blockquote>[!NOTE]<br>Fiskální období, která jsou uvedena v poli, pocházejí z fiskálního kalendáře, který je přidružen k hlavní knize nákladového účetnictví.</blockquote> |
| Aktuální verze         | Vyberte odpovídající ID výpočtu režijních nákladů. |
| Rozpočtová verze         | Vyberte odpovídající ID výpočtu režijních nákladů. |
| Verze revidovaného rozpočtu | Vyberte odpovídající ID výpočtu režijních nákladů. |

### <a name="fiscal-periods-per-column"></a>Fiskální období dle sloupce

Na pevné záložce **Fiskální období dle sloupce** se nákladový účetní rozhodne, které fiskálních období má být zobrazeno v rozvržení sestavy.

Hodnoty ve vybraných sloupcích budou vynásobeny vybranými hodnotami na pevné záložce **Fiskální období dle sloupce**.

| Pole                | popis |
|----------------------|-------------|
| Aktuální období       | Je zobrazen zůstatek aktuálního fiskálního období.<blockquote>[!NOTE]<br>Ve výchozím nastavení je aktuální období určeno datem relace. V pracovním prostoru **Řízení nákladů** lze vybrat konkrétní fiskální období. Vybraná hodnota pak představuje aktuální období.</blockquote> |
| Předchozí období      | Je zobrazen zůstatek předchozího fiskálního období. Použije se následující vzorec:<br>Aktuální fiskální období - 1<blockquote>[!NOTE]<br>Ve výchozím nastavení je předchozí období odvozeno od data relace. V pracovním prostoru **Řízení nákladů** lze vybrat konkrétní fiskální období jako aktuální období. **Předchozí období** se pak přepočítá odpovídajícím způsobem.</blockquote> |
| Rok do data         | Zobrazí se hodnota od začátku roku. Použije se následující vzorec:<br>YearToDate (Aktuální fiskální období)<blockquote>[!NOTE]<br>Ve výchozím nastavení je aktuální období určeno datem relace. V pracovním prostoru **Řízení nákladů** lze vybrat konkrétní fiskální období. Vybraná hodnota pak představuje aktuální období a hodnota **Od začátku roku** bude aktualizována odpovídajícím způsobem.</blockquote> |
| Průměr od začátku roku | Zobrazí se průměr od začátku roku. Použije se následující vzorec:<br>(Od začátku roku [aktuální fiskální období]) ÷ (počet [aktuální fiskální období])<p><strong>Příklad</strong></p><ul><li>**Člen statistické dimenze:** Zaměstnanci na plný úvazek</li><li>**Aktuální datum:** 21. 3. 2017</li><li>**Období:** Fiskální období 1, Fiskální období 2, Fiskální období 3</li><li>**Hodnota:** 10, 10, 12</li></ul>V takovém případě **Průměr od začátku roku** = (10 + 10 + 12) ÷ 3 = 10,67<p>Hodnota **Průměr od začátku roku** může být vypočítána pro členy dimenze prvku nákladů a členy statistické dimenze.</p><blockquote>[!NOTE]<br>Ve výchozím nastavení je aktuální období určeno datem relace. V pracovním prostoru **Řízení nákladů** lze vybrat konkrétní fiskální období. Vybraná hodnota pak představuje aktuální období a hodnoty **Od začátku roku** a **Průměr od začátku roku** budou aktualizovány odpovídajícím způsobem.</blockquote> |

### <a name="columns-to-display-for-costs"></a>Sloupce k zobrazení nákladů

Na pevné záložce **Sloupce k zobrazení nákladů** se nákladový účetní rozhodne, které sloupce má rozvržení sestavy obsahovat. Existují tři kategorie: pevné náklady, variabilní náklady a neklasifikované náklady.

| Pole                 | popis |
|-----------------------|-------------|
| Pevné náklady            | Tento typ sloupce zobrazuje pevné náklady založené na zvoleném ID výpočtu režijních nákladů.<blockquote>[!NOTE]<br>Tento typ sloupce zobrazí zůstatek pouze v případě, kdy je pro fiskální období zvolené ID výpočtu režijních nákladů.</blockquote> |
| Variabilní náklady         | Tento typ sloupce zobrazuje variabilní náklady založené na zvoleném ID výpočtu režijních nákladů.<blockquote>[!NOTE]<br>Tento typ sloupce zobrazí zůstatek pouze v případě, kdy je pro fiskální období zvolené ID výpočtu režijních nákladů.</blockquote> |
| Fixní + variabilní náklady | Tento typ sloupce zobrazuje pevné a variabilní náklady založené na zvoleném ID výpočtu režijních nákladů.<blockquote>[!NOTE]<br>Tento typ sloupce zobrazí zůstatek pouze v případě, kdy je pro fiskální období zvolené ID výpočtu režijních nákladů.</blockquote> |
| Celkové náklady            | Tento typ sloupce zobrazuje celkové náklady (neklasifikované náklady, pevné náklady a variabilní náklady).<blockquote>[!NOTE]<br>Typ sloupce vždy zobrazí zůstatek.</blockquote> |
| Neklasifikované náklady     | Tento typ sloupce zobrazí neklasifikované náklady.<blockquote>[!NOTE]<br>Tento sloupec slouží k ověření, zda byly všechny náklady správně klasifikovány podle výpočtu režijních nákladů, nebo zda musí být upraveno pravidlo chování nákladů.</blockquote> |

### <a name="columns-to-display-for-budgeted-costs"></a>Sloupce k zobrazení rozpočtových nákladů

Na pevné záložce **Sloupce k zobrazení rozpočtových nákladů** se nákladový účetní rozhodne, které sloupce mají být zobrazeny pro zvolené verze rozpočtu. Jednotlivé volby lze provést pro původní a revidovaný rozpočet.

> [!NOTE]
> Protože následující pole se chovají stejným způsobem pro původní a revidovaný rozpočet, budou vysvětleny pouze jednou.

| Pole                     | popis |
|---------------------------|-------------|
| Rozpočet                    | Zůstatky rozpočtu budou zobrazeny podle zvolených sloupců.<blockquote>[!NOTE]<br>Zůstatky budou založeny na verzích rozpočtu, které jsou vybrané na pevné záložce **Filtrování dat**.</blockquote> |
| Odchylka rozpočtu           | Vypočítejte a zobrazte rozdíl mezi skutečným a rozpočtovým zůstatkem. Použije se následující vzorec:<br>Rozpočtový zůstatek – Skutečný zůstatek |
| Odchylka rozpočtu v %      | Vypočítejte a zobrazte rozdíl v procentech mezi skutečným a rozpočtovým zůstatkem. Použije se následující vzorec:<br>(Rozpočtový zůstatek – Skutečný zůstatek) ÷ Rozpočtový zůstatek |
| Práh období odchylky | Nastavte prahovou hodnotu pro odchylku peněžní částky za aktuální období. Při přesažení prahové hodnoty se řádek zvýrazní červeně v pracovním prostoru **Řízení nákladů**.<blockquote>[!NOTE]<br>Toto pole se vztahuje pouze na prvky nákladů, které představují výdaje.</blockquote> |
| Práh roku odchylky   | Nastavte prahovou hodnotu pro odchylku peněžní částky za rok. Při přesažení prahové hodnoty se řádek zvýrazní červeně v pracovním prostoru **Řízení nákladů**. |
| Práh odchylky v %      | Nastavte prahovou hodnotu pro odchylku v procentech. Při přesažení prahové hodnoty se řádek zvýrazní červeně v pracovním prostoru **Řízení nákladů**.<blockquote>[!NOTE]<br>Stejná procentuální prahová hodnota platí pro aktuální období a rok.</blockquote> |

## <a name="cost-control-workspace"></a>Pracovní prostor kontroly nákladů

Pracovní prostor **Řízení nákladů** je navržen jako webová sestava. Proto všichni vedoucí pracovníci, kteří odpovídají za objekt nákladů, mohou získat přístup podle toho, jak je popsáno v [Definování přístupových práv pro kontrolory objektů nákladů](access-rights-cost-object-controller.md).

Seznam sestav, které jsou k dispozici pro uživatele, jako jsou například vedoucí pracovníci, je řízen nastavením možnosti **Publikováno** na stránce **Konfigurace pracovního prostoru řízení nákladů**.

![Sestava, kterou uživatelé mohou zobrazit v pracovním prostoru řízení nákladů](./media/report-cost-control.png)

Manažer může vybrat období fiskálního kalendáře, které chcete zobrazit. K určení výchozího aktuálního období se používá datum relace.

Hodnoty v období fiskálního kalendáře jsou určeny podle názvu sestavy a fiskálního kalendáře zvoleného pro hlavní knihu nákladového účetnictví, která je přidružená k názvu sestavy na stránce **Konfigurace pracovního prostoru řízení nákladů**.

V hierarchii dimenze objektu nákladů uživatelé mohou vybírat úroveň agregace, na které mají být zobrazeny zůstatky. Povolením zabezpečení na úrovni přístupu kontrolujete oprávnění, tak, aby uživatelé mohli zvolit pouze úrovně hierarchie, ke kterým jim byl udělen přístup. Proto mohou zobrazovat pouze agregované zůstatky, ke kterým jim byl udělen přístup.

### <a name="add-or-remove-columns"></a>Přidat nebo odebrat sloupce

Uživatelé mohou přizpůsobit sloupce v sestavě podle svých požadavků.

### <a name="view-details"></a>Zobrazit podrobnosti

Uživatelé mohou procházet podrobnosti za zůstatky, které jsou zobrazeny v pracovním prostoru. Pokud uživatelé zvolí uzel hierarchie dimenze prvku nákladů a poté kliknou na možnost **Zobrazit podrobnosti**, ukáže dialogové okno **Podrobnosti prvku nákladů** podrobné informace o uzlu.

Mřížka ukazuje každý prvek nákladů, který je přidružen k uzlu hierarchie dimenze prvku nákladů, a jeho hodnoty. Sloupce, které se zobrazí v mřížce, odpovídají nastavení pracovního prostoru.

Dva grafy zobrazují souhrn skutečných a rozpočtových hodnot a odchylku rozpočtu podle období.

![Grafy, které zobrazují souhrn skutečných a rozpočtových hodnot a odchylku rozpočtu podle období.](./media/cost-element-details-operations.png)

Uživatelé mohou kliknout na **Položky nákladů** a procházet podrobnosti položek podle potřeby.

![Položky nákladů](./media/cost-entries.png)

Například nájemné je výdaj rozdělený do nákladových středisek. Uživatel, který chce porozumět nákladům na nájemné, které musí nést jeho nákladové středisko, může procházet podrobnosti a vidět, jak bylo nájemné vypočítáno.

Pokud uživatelé kliknou na volbu **Základ přidělení** na stránce **Položky nákladů**, zobrazí se dialogové okno. Uživatele mohou poté přiřadit základ přidělení k pravidlu a zobrazit odpovídající statistická měření, která jsou registrována pro období.

V následujícím příkladu je základ přidělení typu **Základ přidělení vzorce** a je zobrazen vzorec. Jsou uvedeny koeficienty, které definují vzorec. Kromě toho mřížka zobrazí výpočet, který se provádí podle objektu nákladů.

![Výpočty podle objektu nákladů](./media/cost-entries-allocation-base.png)

Další zdroje 

[Definování přístupových práv pro kontrolory objektů nákladů](access-rights-cost-object-controller.md)


