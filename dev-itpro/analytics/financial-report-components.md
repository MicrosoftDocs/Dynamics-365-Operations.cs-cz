---
title: "Součásti finančních sestav"
description: "Tento článek popisuje způsob použití komponent nebo stavebních bloků z definic sestavy ve finančních sestavách. Tyto stavební bloky zahrnují definice řádku, definice sloupce a definice stromu výkaznictví. Tento článek vysvětluje způsob uspořádání a uzamčení stavebních bloků a způsob, jak pracovat se skupinami stavebních bloků."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 057c338c11518b3a1081223e432cbfd109d5e679
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="financial-report-components"></a>Součásti finančních sestav

[!include[banner](../includes/banner.md)]


Tento článek popisuje způsob použití komponent nebo stavebních bloků z definic sestavy ve finančních sestavách. Tyto stavební bloky zahrnují definice řádku, definice sloupce a definice stromu výkaznictví. Tento článek vysvětluje způsob uspořádání a uzamčení stavebních bloků a způsob, jak pracovat se skupinami stavebních bloků. 

Konstrukční filozofie za návrhářem finančních sestav je rozdělit informace na nejmenší součásti nebo stavební bloky a potom zkombinovat a spárovat součásti podle potřeby. Proto je formátování sestavy odděleno od finančních dat, a návrh sestavy můžete změnit bez úpravy finančních dat v systému Microsoft Dynamics ERP. Pomocí tohoto přístupu stavebních bloků můžete kombinovat text, částky a výpočty a vytvářet tak sestavy, jaké potřebujete. Navíc tato flexibilita podporuje tvořivost, protože usnadňuje zobrazování operací různými způsoby. Jednotlivé stavební bloky definice sestavy jsou podobné trojrozměrné tabulce, ale s ještě lepší využitelností. Definice sestavy určuje definici řádku, definici sloupce a volitelně definici stromu výkaznictví pro použití v sestavě. Také obsahuje informace o umístění pro uložení vygenerovaných sestav a o jejich formátování. Kvůli lepším možnostem opakovaného používání a sdílení můžete vytvořit skupinu stavebních bloků, což je kolekce existujících definic sestavy, definic řádku definic sloupce, definic stromu výkaznictví a sad dimenzí, které jsou přidruženy ke společnosti.

## <a name="building-blocks-of-a-report"></a> Stavební bloky sestavy
| Stavební blok            | Popis                                                                                                                                                                                                                                                                              | Získání dalších informací                                                                                                 |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Definice řádku            | Definice řádku definuje v sestavě popisné řádky, například pro platy nebo prodeje. Také uvádí hodnoty segmentů nebo dimenze, které obsahují hodnoty pro každou položku řádku, a obsahuje formátování a výpočty řádků.                                                    | [Definice řádku](row-definitions-financial-reporting.md)                       |
| Definice sloupce         | Definice sloupce určuje období, které má být použito k extrahování dat z finančních dimenzí. Dále zahrnuje formátování a výpočty sloupců.                                                                                                                                 | [Definice sloupce](column-definitions-financial-reports.md)         |
| Definice stromu výkaznictví | Definice stromu výkaznictví se podobá organizačnímu grafu. Obsahuje jednotlivé jednotky výkaznictví, které reprezentují jednotlivá políčka v diagramu. Jednotky mohou být buď samostatná oddělení z finančních dat nebo jednotky vyšší úrovně, které shrnují data z jiných jednotek výkaznictví. | [Definice stromu výkaznictví](financial-reporting-tree-definitions.md) |
| Definice sestavy         | Definice sestavy využívá definici řádku, definici sloupce a volitelně definici stromu výkaznictví pro vytvoření sestavy. Také nabízí další možnosti a nastavení pro přizpůsobení sestavy.                                                                    | [Definice sestavy](design-financial-report-definitions.md)                  |

Pokud začínáte s navrhováním sestav, je vhodné použít průvodce sestavou k rychlému vytvoření definice sestavy, kterou lze později upravit. Pokud máte zkušenosti s návrhem sestav a potřebujete větší flexibilitu pro návrh sestavy, můžete kombinovat nové a existující stavební bloky k vytvoření nové definice sestavy. Nemusíte plně rozumět všem dostupným možnostem definice sestavy k tvorbě kvalitních sestav. Jakmile se seznámíte s návrhem sestav, můžete své definice sestavy rozšířit a využít pokročilejší funkce. Po vytvoření základní zprávy můžete přizpůsobit definici sestavy a také všechny stavební bloky v definici sestavy.

## <a name="organize-the-building-blocks"></a>Uspořádání stavebních bloků
Použijte složky k organizaci svých stavebních bloků v Návrháři sestav. Všechny složky jsou specifické pro typ stavebních bloků, které obsahují. Například všechny složek, které obsahují definice řádku, se nacházejí v podokně **Definice řádku** v Návrháři sestav.

### <a name="create-a-folder"></a>Vytvoření složky

1.  V Návrháři sestav vyberte typ stavebního bloku k uspořádání v navigačním podokně. Chcete-li například seřadit definici řádku, klikněte na položku **Definice řádku**.
2.  V navigačním podokně vyberte existující složku, ve které bude vytvořena nová složka, a potom proveďte některé z následujících akcí:
    -   Klikněte pravým tlačítkem myši na nadřazenou složku a klikněte na **Nová složka**.
    -   Vyberte nadřazenou složku, klikněte na možnost **Soubor** a vyberte možnost **Nová složka**.

3.  Když se objeví nová složka, zadejte název nové složky a stiskněte klávesu Enter.

## <a name="lock-a-building-block"></a> Uzamknutí stavebního bloku
Můžete vytvořit heslo pro ochranu a uzamknutí stavebního bloku. Takový krok přidá úroveň zabezpečení pro součást sestavy bez zabezpečení celého systému. Heslo může ochránit informace ve stavebním bloku, které jsou důležité pro proces vykazování na konci měsíce. Uživatel v jakékoli roli může ochránit stavební blok. Chráněná součást je však vždy k dispozici uživatelům ve formě pouze pro čtení. Uživatelé mohou uzamčenou součást otevřít, upravit a uložit pod novým názvem. Uživatel s rolí správce má vždy přístup k zobrazení a změně uzamčeného stavebního bloku.
1.  V Návrháři sestav otevřete součást sestavy, kterou chcete uzamknout, například definici řádku, definici sloupce, definici sestavy nebo definici stromu výkaznictví.
2.  V nabídce **Nástroje** klepněte na tlačítko **Zamknout/Odemknout**. Můžete také kliknout na ikonu **Zamknout/Odemknout** (ikona zámku) na panelu nástrojů.
3.  V dialogovém okně **Zamknout** zadejte a potvrďte heslo a potom klepněte na tlačítko **OK**. Ikona zámku na panelu nástrojů se zvýrazní, když je otevřený stavební blok uzamčen.

Abyste odemkli uzamčený stavební blok, otevřete stavební blok a poté klikněte na **Zamknout/Odemknout** na panelu nástrojů. Případně v nabídce **Nástroje** klepněte na tlačítko **Odemknout**.

## <a name="building-block-groups"></a>Skupiny stavebních bloků

Stavební bloky jsou definice řádků, definice sloupců, definice stromu výkaznictví a definice sestav, které vytvoříte pro sestavy. Stavební bloky jsou kolekce definic a sad dimenzí, které jsou přidruženy ke společnosti. Skupiny stavebních bloků mohou být specifické pro společnost, nebo může více společností sdílet stejnou sadu stavebních bloků. Pokud máte některé společnosti, které mají různé účtové osnovy, zvažte použití jiné skupiny stavebních bloků pro každou společnost. Můžete také zvážit pojmenování všech svých jednotlivých stavebních bloků podle společnosti, se kterou jsou kompatibilní.
### <a name="create-a-building-block-group"></a>Vytvoření skupiny stavebních bloků

1.  V Návrháři sestav v nabídce **Společnost** klikněte na položku **Skupiny stavebních bloků**.
2.  V dialogovém okně **Skupiny stavebních bloků** klikněte na možnost **Nová**.
3.  Zadejte jedinečný název a popis skupiny stavebních bloků. Každé pole může obsahovat maximálně 256 znaků. (Toto číslo zahrnuje mezery).
4.  Kliknutím na tlačítko **OK** vytvořte novou skupinu stavebních bloků.

### <a name="assign-a-building-block-group"></a>Přiřaďte skupinu stavebních bloků

Po vytvoření skupiny bloků je nutné přiřadit ji alespoň k jedné společnosti. Můžete poté vytvořit definice sestavy, řádku, sloupce a stromu výkaznictví a uložit je do skupiny stavebních bloků. Před zahájením následujícího postupu je nutné zavřít všechny stavební bloky.
1.  V Návrháři sestav v nabídce **Společnost** klikněte na položku **Společnosti**.
2.  V dialogovém okně **Společnosti** vyberte společnost, ke které chcete přiřadit skupinu stavebních bloků.
3.  Klikněte na příkaz **Upravit**.
4.  V dialogovém okně **Upravit společnost** v poli **Skupina stavebních bloků** vyberte skupinu stavebních bloků, kterou chcete přiřadit ke společnosti, nebo kliknutím na položku **Nová** vytvořte novou skupinu stavebních bloků.
5.  Kliknutím na tlačítko **OK** přiřaďte skupinu stavebních bloků.
6.  Klepnutím na tlačítko **Zavřít** zavřete dialogové okno **Společnosti**. Společnosti bude nyní přidělena skupina stavebních bloků, kterou jste vybrali. Nyní budou všechny nové definice řádku, definice sloupce atd. součástí skupiny stavebních bloků přiřazené k dané společnosti. Můžete také importovat soubor TDBX nebo sestavu z jiného systému.

### <a name="view-a-building-block-group"></a> Zobrazení skupiny stavebních bloků

Po vytvoření a použití skupiny stavebních bloků, lze zobrazit všechny stavební bloky přiřazené k ní. Můžete také exportovat nebo importovat skupinu stavebních bloků a provádět další údržbu skupin stavebních bloků.
1.  V Návrháři sestav v nabídce **Společnost** klikněte na položku **Skupiny stavebních bloků**.
2.  V dialogovém okně **Skupiny stavebních bloků** vyberte stavební blok k zobrazení.
3.  Kliknutím na tlačítko **Zobrazení** otevřete dialogové okno **Zobrazení skupiny stavebních bloků** a zobrazíte obsah skupiny stavebních bloků.
4.  Kliknutím na tlačítko **Zavřít** zavřete dialogová okna.

### <a name="save-a-building-block-group-under-a-new-name"></a>Uložení skupiny stavebních bloků pod novým názvem

Existující skupinu stavebních bloků je možné uložit pod novým názvem. Poté můžete novou skupinu stavebních bloků upravovat beze změny původní skupiny stavebních bloků.
1.  V Návrháři sestav v nabídce **Společnost** klikněte na položku **Skupiny stavebních bloků**.
2.  V dialogovém okně **Skupiny stavebních bloků** vyberte skupinu stavebních bloků k uložení pod novým názvem.
3.  Klikněte na možnost **Uložit jako**.
4.  Zadejte nový název a popis skupiny stavebních bloků.
5.  Klepněte na tlačítko **OK**. Nová skupina stavebních bloků se zobrazí v dialogovém okně **Skupiny stavebních bloků**.

### <a name="export-a-building-block-group"></a> Export skupiny stavebních bloků

Ve skupině stavebního bloku můžete exportovat skupinu stavebního bloku nebo stavební bloky konkrétní sestavy. Exportovanou skupinu stavebního bloku můžete použít jako zálohu. Můžete také kopírovat exportovaná data mezi skupinami stavebních bloků nebo instalacemi aplikace Dynamics 365 for Operations. Návrhář sestav zahrnuje odkazované styly písem a sady dimenzí společně se skupinou stavebních bloků.
1.  V Návrháři sestav v nabídce **Společnost** klikněte na položku **Skupiny stavebních bloků**.
2.  V dialogovém okně **Skupiny stavebních bloků** vyberte skupinu stavebních bloků k exportu a klikněte na tlačítko **Exportovat**.
3.  V dialogovém okně **Export** vyberte definice sestavy k exportu:
    -   Pokud chcete exportovat všechny definice sestavy a přidružené stavební bloky, klikněte na tlačítko **Vybrat vše**.
    -   Pokud chcete exportovat konkrétní sestavy, řádky, sloupce, stromy či sady dimenzí, klikněte na příslušnou kartu a vyberte položky k exportu. Když stisknete a podržíte klávesu Ctrl, můžete vybrat na kartě více položek. **Poznámka:** Při výběru sestav k exportu jsou zvoleny přidružené řádky, sloupce, stromy a sady dimenzí.

4.  Po dokončení výběru položek pro export klikněte na tlačítko **Exportovat**.
5.  V dialogovém okně **Uložit jako** vyberte umístění pro export skupiny stavebních bloků.
6.  Do pole **Název souboru** zadejte název souboru. Návrhář sestav automaticky přidá příponu souboru .tdbx.
7.  Klepněte na tlačítko **Uložit**. Skupina stavebních bloků bude uložena do umístění určeného v kroku 5.

### <a name="import-a-building-block-group"></a> Import skupiny stavebních bloků

Skupinu stavebních bloků můžete importovat do stávající skupiny stavebních bloků nebo můžete vytvořit novou skupinu stavebních bloků pro data. Všechny importované skupiny stavebních bloků si zachovají původní styly písem a odkazy na společnost a budou zahrnovat odpovídající sady dimenzí.
1.  V Návrháři sestav v nabídce **Společnost** klikněte na položku **Skupiny stavebních bloků**.
2.  V dialogovém okně **Skupiny stavebních bloků** vyberte stavební blok, do kterého chcete skupinu stavebních bloků importovat, a klikněte na tlačítko **Importovat**.
3.  V dialogovém okně **Otevřít** vyberte skupinu stavebních bloků k importu a klikněte na tlačítko **Otevřít**.
4.  V dialogovém okně **Import** vyberte definice sestavy k importu:
    -   Pokud chcete importovat všechny definice sestavy a podpůrné stavební bloky, klikněte na tlačítko **Vybrat vše**.
    -   Chcete-li importovat konkrétní sestavy, řádky, sloupce, stromy či sady dimenzí, vyberte sestavy, řádky, sloupce, stromy a sady dimenzí k importu.

5.  Po dokončení výběru položek pro import klikněte na tlačítko **Importovat**.

### <a name="undo-a-checkout-of-a-building-block"></a>Zrušení rezervace stavebního bloku

Při otevření stavebního bloku mají k tomuto stavebnímu bloku ostatní uživatelé přístup pouze pro čtení. V některých případech uživatel zapomene zavřít stavební blok nebo vypnout svůj systém bez zavření stavebního bloku. V důsledku toho je stavební blok rezervován a ostatní uživatelé ho nemohou otevřít. V takových situacích může správce finančních sestav použít dialogové okno **Rezervované položky** ke zrušení rezervace stavebních bloků, které uživatelé ponechali rezervované. **Poznámka:** Abyste mohli v dialogovém okně **Rezervované položky** rušit rezervace stavebních bloků, musíte mít roli správce.
1.  V Návrháři sestav v nabídce **Nástroje** klikněte na tlačítko **Rezervované položky**.
2.  V dialogovém okně **Rezervované položky** vyberte možnost **Zobrazit položky všech uživatelů**. Seznam se aktualizuje a zobrazí všechny stavební bloky, které jsou rezervovány, a uživatele, kteří je mají rezervovány.
3.  Vyberte stavební blok a klikněte na tlačítko **Zrušit rezervaci**.
4.  Kliknutím na tlačítko **Ano** zrušíte rezervaci stavebního bloku.

# <a name="see-also"></a>Viz také

[Finanční výkaznictví](financial-reporting-intro.md)




