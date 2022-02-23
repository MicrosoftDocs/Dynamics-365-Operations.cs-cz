---
title: Součásti finančních sestav
description: Tento článek popisuje způsob použití komponent nebo stavebních bloků z definic sestavy ve finančních sestavách. Tyto stavební bloky zahrnují definice řádku, definice sloupce a definice stromu výkaznictví. Tento článek vysvětluje způsob uspořádání a uzamčení stavebních bloků a způsob, jak pracovat se skupinami stavebních bloků.
author: aprilolson
manager: AnnBe
ms.date: 10/27/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 97468be0bdea679ca7a52c5cef9c1e10950736e8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682714"
---
# <a name="financial-report-components"></a>Součásti finančních sestav

[!include [banner](../includes/banner.md)]

Tento článek popisuje způsob použití komponent nebo stavebních bloků z definic sestavy ve finančních sestavách. Tyto stavební bloky zahrnují definice řádku, definice sloupce a definice stromu výkaznictví. Článek vysvětluje, jak uspořádat a uzamknout stavební bloky.

Konstrukční filozofie za návrhářem finančních sestav je rozdělit informace na nejmenší součásti nebo stavební bloky a potom zkombinovat a spárovat součásti podle potřeby. Proto je formátování sestavy odděleno od finančních dat, a návrh sestavy můžete změnit bez úpravy finančních dat v systému Microsoft Dynamics ERP. Pomocí tohoto přístupu stavebních bloků můžete kombinovat text, částky a výpočty a vytvářet tak sestavy, jaké potřebujete. Navíc tato flexibilita podporuje tvořivost, protože usnadňuje zobrazování operací různými způsoby. Jednotlivé stavební bloky definice sestavy jsou podobné trojrozměrné tabulce, ale s ještě lepší využitelností. Definice sestavy určuje definici řádku, definici sloupce a volitelně definici stromu výkaznictví pro použití v sestavě. Také obsahuje informace o umístění pro uložení vygenerovaných sestav a o jejich formátování.

## <a name="building-blocks-of-a-report"></a>Stavební bloky sestavy

| Stavební blok            | popis | Získání dalších informací |
|---------------------------|-------------|----------------------|
| Definice řádku            | Definice řádku definuje v sestavě popisné řádky, například pro platy nebo prodeje. Také uvádí hodnoty segmentů nebo dimenze, které obsahují hodnoty pro každou položku řádku, a obsahuje formátování a výpočty řádků. | [Definice řádku](row-definitions-financial-reporting.md) |
| Definice sloupce         | Definice sloupce určuje období, které má být použito k extrahování dat z finančních dimenzí. Dále zahrnuje formátování a výpočty sloupců. | [Definice sloupce](column-definitions-financial-reports.md) |
| Definice organizačního stromu | Definice organizačního stromu se podobá organizačnímu grafu. Obsahuje jednotlivé jednotky výkaznictví, které reprezentují jednotlivá políčka v diagramu. Jednotky mohou být buď individuální oddělení z finančních dat, nebo jednotky na vyšší úrovni, které sumarizují data z jiných organizačních jednotek. | [Definice stromu výkaznictví](financial-reporting-tree-definitions.md) |
| Definice sestavy         | Definice sestavy využívá definici řádku, definici sloupce a volitelně definici stromu výkaznictví pro vytvoření sestavy. Také nabízí další možnosti a nastavení pro přizpůsobení sestavy. | [Definice sestavy](design-financial-report-definitions.md) |

Pokud začínáte s navrhováním sestav, je vhodné použít průvodce sestavou k rychlému vytvoření definice sestavy, kterou lze později upravit. Pokud máte zkušenosti s návrhem sestav a potřebujete větší flexibilitu pro návrh sestavy, můžete kombinovat nové a existující stavební bloky k vytvoření nové definice sestavy. Nemusíte plně rozumět všem dostupným možnostem definice sestavy k tvorbě kvalitních sestav. Jakmile se seznámíte s návrhem sestav, můžete své definice sestavy rozšířit a využít pokročilejší funkce. Po vytvoření základní zprávy můžete přizpůsobit definici sestavy a také všechny stavební bloky v definici sestavy.

## <a name="organize-the-building-blocks"></a>Uspořádání stavebních bloků
Použijte složky k organizaci svých stavebních bloků v Návrháři sestav. Všechny složky jsou specifické pro typ stavebních bloků, které obsahují. Například všechny složek, které obsahují definice řádku, se nacházejí v podokně **Definice řádku** v Návrháři sestav.

### <a name="create-a-folder"></a>Vytvoření složky

1. V Návrháři sestav vyberte typ stavebního bloku k uspořádání v navigačním podokně. Chcete-li například seřadit definici řádku, klikněte na položku **Definice řádku**.
2. V navigačním podokně vyberte existující složku, ve které bude vytvořena nová složka, a potom proveďte některé z následujících akcí:

    - Klikněte pravým tlačítkem myši na nadřazenou složku a klikněte na **Nová složka**.
    - Vyberte nadřazenou složku, klikněte na možnost **Soubor** a vyberte možnost **Nová složka**.

3. Když se objeví nová složka, zadejte název nové složky a stiskněte klávesu Enter.

## <a name="lock-a-building-block"></a> Uzamknutí stavebního bloku
Můžete vytvořit heslo pro ochranu a uzamknutí stavebního bloku. Takový krok přidá úroveň zabezpečení pro součást sestavy bez zabezpečení celého systému. Heslo může ochránit informace ve stavebním bloku, které jsou důležité pro proces vykazování na konci měsíce. Uživatel v jakékoli roli může zamknout stavební blok. Chráněná součást je však vždy k dispozici ostatním uživatelům ve formě pouze ke čtení. Uživatelé mohou uzamčenou součást otevřít, upravit a uložit pod novým názvem. Uživatel s rolí správce má vždy přístup k zobrazení a změně uzamčeného stavebního bloku.

1. V Návrháři sestav otevřete součást sestavy, kterou chcete uzamknout, například definici řádku, definici sloupce, definici sestavy nebo definici stromu výkaznictví.
2. V nabídce **Nástroje** klepněte na tlačítko **Zamknout/Odemknout**. Můžete také kliknout na ikonu **Zamknout/Odemknout** (ikona zámku) na panelu nástrojů.
3. V dialogovém okně **Zamknout** zadejte a potvrďte heslo a potom klepněte na tlačítko **OK**. Ikona zámku na panelu nástrojů se zvýrazní, když je otevřený stavební blok uzamčen.

Abyste odemkli uzamčený stavební blok, otevřete stavební blok a poté klikněte na **Zamknout/Odemknout** na panelu nástrojů. Případně v nabídce **Nástroje** klepněte na tlačítko **Odemknout**.

## <a name="building-block-groups"></a>Skupiny stavebních bloků

Stavební bloky jsou definice řádků, definice sloupců, definice stromu výkaznictví a definice sestav, které vytvoříte pro sestavy. Skupiny stavebních bloků jsou kolekce definicí a sad dimenzí.

### <a name="view-a-building-block-group"></a>Zobrazení skupiny stavebních bloků

Můžete zobrazit všechny stavební bloky, které jsou přiřazeny ke skupině stavebních bloků. Můžete také exportovat nebo importovat skupinu stavebních bloků.

1. V Návrháři sestav klikněte v nabídce **Společnost** na položku **Skupiny stavebních bloků**.
2. V dialogovém okně **Skupiny stavebních bloků** vyberte stavební blok k zobrazení.
3. Kliknutím na tlačítko **Zobrazení** otevřete dialogové okno **Zobrazení skupiny stavebních bloků** a zobrazíte obsah skupiny stavebních bloků.
4. Kliknutím na tlačítko **Zavřít** zavřete dialogová okna.

### <a name="export-a-building-block-group"></a>Export skupiny stavebních bloků

Můžete vyexportovat celou skupinu stavebních bloků nebo jen určité stavební bloky sestavy ze skupiny stavebních bloků. Skupinu exportovaných stavebních bloků můžete použít jako zálohu. Exportovaná data také můžete kopírovat mezi instalacemi. Návrhář sestav zahrnuje odkazované styly písem a sady dimenzí společně se skupinou stavebních bloků.

1. V Návrháři sestav v nabídce **Společnost** klikněte na položku **Skupiny stavebních bloků**.
2. V dialogovém okně **Skupiny stavebních bloků** vyberte skupinu stavebních bloků, kterou chcete vyexportovat, a pak klikněte na položku **Export**.
3. V dialogovém okně **Export** vyberte definice sestavy k exportu:

    - Pokud chcete exportovat všechny definice sestavy a přidružené stavební bloky, klikněte na tlačítko **Vybrat vše**.
    - Pokud chcete exportovat konkrétní sestavy, řádky, sloupce, stromy či sady dimenzí, klikněte na příslušnou kartu a vyberte položky k exportu. Když stisknete a podržíte klávesu Ctrl, můžete vybrat na kartě více položek.

    > [!NOTE]
    > Když pro export vyberete sestavy, vyberou se také přidružené řádky, sloupce, stromy a sady dimenzí.

4. Po dokončení výběru položek pro export klikněte na tlačítko **Exportovat**.
5. V dialogovém okně **Uložit jako** vyberte umístění pro export skupiny stavebních bloků.
6. Do pole **Název souboru** zadejte název souboru. Návrhář sestav automaticky přidá příponu souboru .tdbx.
7. Klepněte na tlačítko **Uložit**. Skupina stavebních bloků bude uložena do umístění určeného v kroku 5.

### <a name="import-a-building-block-group"></a> Import skupiny stavebních bloků

Skupinu stavebních bloků můžete importovat do existující skupiny stavebních bloků. Všechny importované skupiny stavebních bloků si zachovají původní styly písem a odkazy na společnost a budou zahrnovat odpovídající sady dimenzí.

1. V Návrháři sestav v nabídce **Společnost** klikněte na položku **Skupiny stavebních bloků**.
2. V dialogovém okně **Skupiny stavebních bloků** vyberte stavební blok, do kterého chcete skupinu stavebních bloků naimportovat, a pak klikněte na položku **Import**.
3. V dialogovém okně **Otevřít** vyberte skupinu stavebních bloků, kterou chcete naimportovat, a pak klikněte na položku **Otevřít**.
4. V dialogovém okně **Import** vyberte definice sestavy k importu:

    - Pokud chcete importovat všechny definice sestavy a podpůrné stavební bloky, klikněte na tlačítko **Vybrat vše**.
    - Chcete-li importovat konkrétní sestavy, řádky, sloupce, stromy či sady dimenzí, vyberte sestavy, řádky, sloupce, stromy a sady dimenzí k importu.

5. Po dokončení výběru položek pro import klikněte na tlačítko **Importovat**.

### <a name="undo-a-checkout-of-a-building-block"></a>Zrušení rezervace stavebního bloku

Při otevření stavebního bloku mají k tomuto stavebnímu bloku ostatní uživatelé přístup pouze pro čtení. V některých případech uživatel zapomene zavřít stavební blok nebo vypnout svůj systém bez zavření stavebního bloku. V důsledku toho je stavební blok rezervován a ostatní uživatelé ho nemohou otevřít. V takových situacích může správce finančních sestav použít dialogové okno **Rezervované položky** ke zrušení rezervace stavebních bloků, které uživatelé ponechali rezervované.

> [!NOTE]
> Pro vrácení stavebních bloků se změnami pomocí dialogového okna **Rezervované položky** je zapotřebí role správce.

1. V Návrháři sestav v nabídce **Nástroje** klikněte na tlačítko **Rezervované položky**.
2. V dialogovém okně **Rezervované položky** vyberte možnost **Zobrazit položky od všech uživatelů**. Seznam se aktualizuje a zobrazí se v něm všechny rezervované stavební bloky spolu s informacemi o uživatelích, kteří je rezervovali.
3. Vyberte stavební blok a klikněte na položku **Zrušit rezervaci**.
4. Kliknutím na tlačítko **Ano** potvrďte, že se má stavební blok vrátit se změnami.

## <a name="additional-resources"></a>Další zdroje

[Finanční výkaznictví](financial-reporting-intro.md)
