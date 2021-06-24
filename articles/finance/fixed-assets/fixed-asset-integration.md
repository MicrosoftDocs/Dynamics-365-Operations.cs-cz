---
title: Integrace dlouhodobého majetku
description: Modulu Dlouhodobý majetek lze integrovat s moduly Hlavní kniha, Řízení zásob, Pohledávky a Závazky. U dlouhodobého majetku lze rovněž nastavit integraci s nákupními objednávkami.
author: ShylaThompson
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3501
ms.assetid: f0639053-d99c-432a-8ead-5c26e0d4eaec
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e6be2aeb263c339f4e733b98ea4e01194973a9f
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189777"
---
# <a name="fixed-assets-integration"></a>Integrace dlouhodobého majetku

[!include [banner](../includes/banner.md)]

Modulu Dlouhodobý majetek lze integrovat s moduly Hlavní kniha, Řízení zásob, Pohledávky a Závazky. U dlouhodobého majetku lze rovněž nastavit integraci s nákupními objednávkami.

## <a name="general-ledger"></a>Hlavní kniha

V hlavní knize je obvykle hodnota veškerého dlouhodobého majetku shrnuta do několika hlavních účtů, které jsou nutné pro finanční vykazování. Avšak na stránce **Dlouhodobý majetek** můžete vytvořit mnoho záznamů dlouhodobého majetku. Tyto záznamy mohou zahrnovat informace, jako je například pořizovací cena, odpisy a oceněni. Při každém zaúčtování transakce s dlouhodobým majetkem se aktualizují příslušné hlavní účty. Hlavní účty vždy ukazují aktualizovanou hodnotu dlouhodobého majetku.

Na stránce **Účetní profily dlouhodobého majetku** můžete definovat hlavní účty pro zaúčtování transakcí knihy dlouhodobého majetku. Můžete zadat také typy transakcí dlouhodobého majetku zaúčtovaných na jednotlivé hlavní účty. Můžete vytvářet různé kombinace hlavních účtů dlouhodobého majetku, v závislosti na úrovni podrobností, které pro dlouhodobý majetek v hlavní knize chcete mít. Hlavní účty mohou být založeny na typech transakce, knihách a dalších hlavních účtech.

## <a name="inventory-management"></a>Řízení zásob
Ve skladovém deníku dlouhodobého majetku můžete zadat pořízení dlouhodobého majetku, který právnická osoba vyrobila nebo sestavila pro sebe. Pak můžete předat skladové položky do dlouhodobého majetku ve formě pořízení nebo částečného pořízení. 

Majetek můžete rovněž pořídit pomocí nákupních objednávek. Pokud nákupní objednávky obsahují skladové položky, které patří do dlouhodobého majetku, nastavení pole Povolit pořízení majetku v části **Nakupování** na stránce **Parametry dlouhodobého majetku** určuje, zda při zaúčtování faktury bude zároveň zaúčtováno pořízení dlouhodobého majetku. Jeden řádek nákupu vytvoří pouze jeden dlouhodobý majetek bez ohledu na množství. Vliv pořízení dlouhodobého majetku vliv na zásoby závisí na nastavení právnické osoby. 

Když se ve skladovém deníku, nákupní objednávce nebo v návrhu pořízení ze skladové položky stane pořízení dlouhodobého majetku, je vytvořena transakce knihy pořízení dlouhodobého majetku. Pokud kniha pořízení zahrnuje odvozenou knihu odpisů, bude transakce pořízení rovněž vytvořena v odvozené knize. 

Úbytek zásob způsobený zaúčtováním pořízení majetku se řídí účetními pravidly nastavenými na stránce **Zaúčtování** v modulu Řízení zásob. Při účtování faktur na dlouhodobý majetek nemusí vždy docházet k úbytku zásob. V některých případech může být dlouhodobý majetek nakoupen pro interní použití. Příkladem je laptop, který se nakupuje pro prodejní oddělení. Když pracujete s nákupními objednávkami, můžete používat položky, které jsou nastavené jak pro další prodej, tak k internímu použití. 

Jestliže u skupin položek používáte zvláštní účty pro příjem a výdej majetku, můžete stejnou skladovou položku použít jak pro interní nákupy tak pro zásobu určenou k prodeji. 

Dlouhodobý majetek pro interní použití lze nastavit tak, že bude mít typ účtu **Příjem dlouhodobého majetku**. Tento typ účtu umožňuje sledovat příjem dlouhodobého majetku. Při zaúčtování faktury dodavatele použijte účet příjmu dlouhodobého majetku, pokud platí některá z následujících podmínek:

-   Řádek faktury obsahuje stávající dlouhodobý majetek pro interní účely.
-   Políčko **Nový dlouhodobý majetek?** je zaškrtnuto pro řádek příjemky produktu, který je zaúčtován.
-   Pole **Vytvořit nový dlouhodobý majetek** je vybráno na řádku faktury dodavatele.

Obvykle se jedná o nákladový účet. Můžete nastavit typ účtu **Příjem dlouhodobého majetku** pro skupinu položek nebo jednotlivé položky pomocí karty **Nákupní objednávka** na stránce **Skupina položek** nebo **Zaúčtování**.

Podobně také dlouhodobý majetek pro interní použití lze nastavit tak, že bude mít typ účtu **Výdej dlouhodobého majetku**. Tento typ účtu umožňuje sledovat výdej dlouhodobého majetku příjemci. Účet pro výdej dlouhodobého majetku slouží jako protiúčet k debetnímu účtu majetku použitému při pořízení prostřednictvím nákupní objednávky. Pořízení majetku lze účtovat se zaúčtováním faktury dodavatele nebo účetním zápisem pořízení majetku do deníku dlouhodobého majetku, například prostřednictvím návrhu na pořízení. Můžete nastavit typ účtu **Výdej dlouhodobého majetku** pro skupinu položek nebo jednotlivé položky pomocí karty **Zásoby** na stránce **Skupina položek** nebo **Zaúčtování zboží**. 

Hlavní účty, které se používají pro zaúčtování, jsou rovněž ovlivněny možnostmi integrace hlavní knihy, zadanými pro skupinu modelů zboží. Kromě toho hlavní účty, které jsou použity, se liší v závislosti na tom, zda je majetek přiřazen k řádku nákupní objednávky. Účty jsou odvozeny od účetního profilu každé skupiny položek. 
**Poznámka:** Jestliže při zaúčtování příjemek produktu existuje rezervace zásob, nemůžete na řádku přiřadit a ani z takového řádku vytvořit dlouhodobý majetek. 

Účty, do kterých jsou transakce dlouhodobého majetku zaúčtovány, závisí dvou faktorech: zda je majetek zakoupen nebo vytvořen právnickou osobou a rovněž na typu transakce majetku. 

Typ transakce spojuje skladovou transakci s účetním profilem modulu Dlouhodobý majetek. Protože účetní profil u dlouhodobého majetku definuje, které účty budou aktualizovány, výběr typu transakce dlouhodobého majetku představuje nepřímo také výběr hlavních účtů, na které bude transakce zaúčtována. U vyrobeného a zakoupeného dlouhodobého majetku je obvykle typ transakce **Pořízení** nebo **Oprava pořizovací ceny**.

## <a name="accounts-receivable"></a>Pohledávky
Integrace modulu Dlouhodobý majetek s modulem Pohledávky používá účetní profily nastavené v modulu Dlouhodobý majetek. Tyto účetní profily se aktivují, když je dlouhodobý majetek, kniha a typ transakce dlouhodobého majetku vybrán pro fakturu odběratele před zaúčtováním faktury odběratele. Vzhledem k tomu že dlouhodobý majetek není součástí modulu **Řízení zásob**, musíte při prodeji majetku použít stránku Volná faktura. 

Pokud kniha zahrnuje odvozenou knihu, bude vytvořena odvozená transakce knihy odpisů v okamžiku zaúčtování faktury odběratele.

## <a name="accounts-payable"></a>Závazky
Obvykle dlouhodobý majetek pořizujete od externích dodavatelů. Na stránce **Parametry dlouhodobého majetku** můžete upřesnit, zda při zaúčtování dodavatelských faktur týkajících se majetku má pokaždé dojít k zaúčtování pořízení majetku, nebo zda se pořízení majetku účtuje pouze v modulu Dlouhodobý majetek. Jestliže povolíte účtování pořizování majetku z modulu Pohledávky, budou účty dlouhodobého majetku aktualizovány při každém zaúčtování faktury dodavatele za pořízený majetek. 

Jestliže je systém nastaven tak, že pořízení majetku se účtuje při zaúčtování faktury, bude transakce zaúčtována podle účetních profilů nastavených v modulu Dlouhodobý majetek pro různé typy majetkových transakcí. Zaúčtování se řídí dlouhodobým majetkem, knihou a typem majetkové transakce, které jsou vybrané na stránce **Nákupní objednávka** před zaúčtováním faktury dodavatele. 

Pokud kniha zahrnuje odvozenou knihu, bude vytvořena odvozená transakce knihy odpisů v okamžiku zaúčtování faktury dodavatele.

Pro každý řádek objednávky je integrace aktivována na kartě **Dlouhodobý majetek** na pevné záložce **Podrobnosti řádku** na stránce **Nákupní objednávka**. Nákupní objednávku pro dlouhodobý majetek můžete odeslat dodavateli. Dlouhodobý majetek a hlavní účty však budou aktualizovány pouze při zaúčtování faktur dodavatele po přijetí dlouhodobého majetku. Vzhledem k tomu, že nákupní objednávky mohou obsahovat pouze skladové položky, závisí vliv pořízení dlouhodobého majetku na sklad na nastavení právnické osoby.

## <a name="project-management-and-accounting"></a>Řízení a účetnictví projektů
Můžete spojit projekt s majetkem, který projekt ovlivňuje. Můžete také spojit každou fázi, úkol nebo dílčí projekt s různým majetkem. Jeden majetek lze přidružit k záznamu jednotlivých projektů. Spojení vytváříte zadáním čísla majetku do pole **Číslo dlouhodobého majetku** na stránce **Projekty**. Typ projektu musí být **interní** nebo **nákladový projekt**. 

Stránku **Projekty** lze rovněž použít k zobrazení podrobných informací o majetku, který je přidružený k projektům. Pokud chcete zobrazit záznam o dlouhodobém majetku, klepnutím na odkaz na majetek na pevné záložce **Nastavení** otevřete stránku **Dlouhodobý majetek**. Poté klepnutím na možnost **Projekty** &gt; **Všechny projekty** zobrazíte projekty, které jsou s tímto dlouhodobým majetkem spojené. 

Obvykle přidružíte dlouhodobý majetek k projektům, když se projekt týká práce, údržby nebo zlepšení majetku. Po dokončení projektu nebude navýšení hodnoty majetku vytvořeno automaticky. Proto je nutné vytvořit navýšení hodnoty ručně, je-li navýšením vyžadováno. 

Jestliže chcete odstranit propojení mezi projektem a majetkem, vymažte pole **Číslo dlouhodobého majetku** na stránce **Projekty**. 

Vytvářený nebo vyráběný dlouhodobý majetek lze rovněž identifikovat v rámci projektu odhadu. Na konci projektu odhadu můžete automaticky zaúčtovat transakci pořízení majetku.

Další informace naleznete v tématu [Pořízení majetku pomocí zásobování](acquire-assets-procurement.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]