---
title: "Definice řádku v návrháři finanční sestavy"
description: "Definice řádku je součástí sestavy nebo stavebního bloku, který určuje obsah jednotlivých řádků ve finanční sestavě. Definici řádku lze kombinovat s definicemi sloupců, definicemi stromu výkaznictví a definicemi sestav a vytvořit tak skupinu stavebních bloků, které může používat více společností."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 770a1681e4fa9974b081d0c63a10eb1961f13014
ms.openlocfilehash: 6d4697af6f7467f25a461fae4e9320402f83b0e3
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017

---

# <a name="row-definitions-in-financial-report-designer"></a>Definice řádku v návrháři finanční sestavy

[!include[banner](../includes/banner.md)]


Definice řádku je součástí sestavy nebo stavebního bloku, který určuje obsah jednotlivých řádků ve finanční sestavě. Definici řádku lze kombinovat s definicemi sloupců, definicemi stromu výkaznictví a definicemi sestav a vytvořit tak skupinu stavebních bloků, které může používat více společností.

<a name="create-a-row-definition"></a>vytvoření definice řádku,
-----------------------

1.  V Návrháři sestav v navigačním podokně klikněte na tlačítko **Definice řádku**.
2.  V nabídce **Soubor** klikněte na tlačítko **Nový** a klikněte na možnost **Definice řádku**. Další informace o obsahu každé buňky naleznete v tématu [Úprava buněk definice řádku](modify-row-definition-cells-financial-reporting.md).

## <a name="open-a-row-definition"></a>Otevření definice řádku
1.  V Návrháři sestav v navigačním podokně klikněte na tlačítko **Definice řádku**.
2.  Definici řádku otevřete kliknutím dvakrát na její název.
3.  Chcete-li zobrazit stavební bloky, které jsou přidruženy k definici řádku, klikněte pravým tlačítkem myši na definici řádku a poté vyberte možnost **Přidružení**.

## <a name="contents-of-a-row-definition"></a> Obsah definice řádku
Definice řádku může obsahovat až 20 000 řádků finančních dimenzí a obsahovat následující informace:

-   popisný text, který přidává do sestavy přehlednost vytvořením záhlaví, řádků a mezer pro oddíly, například **Hotovost** nebo **Celkové výnosy**
-   Odkazy na finanční data, která mohou zahrnovat hodnoty dimenze v aplikaci Microsoft Dynamics 365 for Finance and Operations **Poznámka:** Můžete nastavit definici řádku na stahování dat ze systému finančních dimenzí vždy při vygenerování sestavy.
-   Součty a vzorce řádků, které jsou založeny na propojených finančních datech

Obvykle každý řádek v definici řádku obsahuje jeden z následujících typů informací:

-   Odkazy na systém finančních dimenzí
-   Součty nebo výpočty založené na údajích
-   Formátování

Existují dvě metody pro zadávání informací do definice řádku:

-   Ručně zadejte informace řádku do nové definice řádku. Další informace naleznete v tématu [Úprava buněk definice řádku](modify-row-definition-cells-financial-reporting.md).
-   Použijte návrháře sestav k získání informací řádku přímo z finančních dimenzí. Další informace naleznete v části „Související vzorce/řádky/jednotky“ v části [Úprava buněk definice řádku](modify-row-definition-cells-financial-reporting.md).

## <a name="add-dimensions-in-a-row-definition"></a> Přidání dimenzí do definice řádku
Dimenze je protnutím dat a hodnot. Můžete seskupit data a hodnoty v návrháři sestav. Potom můžete klasifikovat a analyzovat transakce podrobněji. Můžete použít dialogové okno **Vložit řádky z dimenzí** k přidání více řádků současně do definice řádku. Dialogové okno zobrazí pro každou dimenzi jeden sloupec. Následující tabulka popisuje informace, které můžete zadat do každé z dimenzí.

| Možnost                | Popis                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dimenze             | Vzor, který identifikuje dimenzi pro přidání definice řádku. Tento vzor obsahuje jeden znak ampersand (&) nebo znak křížku (\#) pro každou pozici v dimenzích. Obecně byste měli používat všechny ampersandy pro dimenzi hlavního účtu a všechny křížky pro jiné dimenze. |
| Počátek rozsahu dimenzí | První hodnota pro tuto dimenzi k přidání do definice řádku.                                                                                                                                                                                                                 |
| Konec rozsahu dimenzí   | Poslední hodnota pro tuto dimenzi k přidání do definice řádku.                                                                                                                                                                                                                  |

Chcete-li přidat dimenze do definice řádku, proveďte následující kroky.

1.  V Návrháři sestav klikněte na tlačítko **Definice řádku** a potom otevřete definici řádku ke změně.
2.  V nabídce **Upravit** klikněte na tlačítko **Vložit řádky z dimenzí**.
3.  V dialogovém okně **Vložit řádky z dimenzí** vyberte v řádku **Dimenze** buňku dimenze, která má být převedena do definice řádku, a klikněte na tlačítko **Všechny &&&**.
4.  Chcete-li omezit definici řádku na určitý rozsah hodnot dimenzí, zadejte počáteční hodnotu dimenze do buňky **Počátek rozsahu dimenzí** a poté zadejte konečnou hodnotu dimenze do buňky **Konec rozsahu dimenzí**. Chcete-li zahrnout všechny hodnoty pro vybranou dimenzi, nevyplňujte tyto buňky. **Poznámka:** Zástupné znaky (\* nebo ?) v rozsahu dimenze nemusí vrátit všechny požadované výsledky; záleží na tom, jak databáze ERP třídí data.
5.  V poli **Kód počátečního řádku** určete kód řádku pro první hodnotu dimenze, která má být přidána do definice řádku.
6.  V poli **Zvýšit každý řádek o** určete mezeru mezi po sobě jdoucími kódy řádků. Například pokud je kód prvního řádku 100 a přírůstek je 30, první nové řádky budou mít kódy 100, 130, 160, 190 a 220. Použijte hodnotu přírůstku, která zajistí dostatek prostoru pro vkládání nových řádků formátu a vzorců.
7.  Klepněte na tlačítko **OK**. Pro každý řádek vybrané hodnoty dimenze je přidán jeden řádek do definice řádku.

## <a name="adjust-rounding-in-a-row-definition"></a> Úprava zaokrouhlování v definici řádku
Pokud máte rozvahu, ve které jsou částky zaokrouhleny, součty mohou překračovat zůstatek. Tomuto problému může dojít, pokud například použijete možnost zaokrouhlení v sestavě rozvahy a definice sestavy také určuje zaokrouhlení. Můžete použít možnost **Vyrovnání rozdílů po zaokrouhlení** v definici řádku a vyrovnat tak částky v rozvaze. Zaokrouhlení se vypíná nebo upravuje na kartě **Nastavení** v rámci definice sestavy. Způsob zaokrouhlování částek je uveden v následující tabulce. V této tabulce se součty řádků 100 a 200 liší, když je zaokrouhlování zapnuto.

| Kód řádku | Částky bez zaokrouhlení | Částka se zaokrouhlením na celé tisíce |
|----------|--------------------------|-----------------------------------------|
| 100      | 3 600                    | 4                                       |
| 200      | 3 700                    | 4                                       |
| Celkem    | 7 300                    | 8                                       |

Chcete-li upravit zaokrouhlování v rozvaze, proveďte následující kroky.

1.  V Návrháři sestav klikněte na tlačítko **Definice řádku** a potom otevřete definici řádku ke změně.
2.  V nabídce **Upravit** klikněte na tlačítko **Úprava zaokrouhlení**.
3.  V dialogovém okně **Vyrovnání rozdílů po zaokrouhlení** zadejte následující hodnoty:
    -   **Řádek vyrovnání rozdílů po zaokrouhlení** – kód řádku, který bude upraven kvůli vyrovnání rozvahy.
    -   **Řádek součtu majetku** – kód řádku v rozvaze, který obsahuje součet majetku.
    -   **Řádek součtu závazků a jmění** – kód řádku v rozvaze, který obsahuje součet závazků a jmění.
    -   **Limit částky úpravy** – limit pro automatické úpravy vyjádřený jako kladné celé číslo. Tato částka se porovnává s absolutní hodnotou skutečného rozdílu zaokrouhlení.

    **Poznámka:** Tyto kódy řádků musejí být propojeny s finančními daty. Jinak řečeno, řádek musí mít hodnotu dimenze v buňce **Odkaz na finanční dimenze**. **Neodkazujte** na řádek popisu (**DESC**), výpočtu (**CALC**) nebo součtu (**TOT**).

Částky ve vaší rozvaze budou vyrovnávány rovnoměrně při zapnutém zaokrouhlování. **Poznámka:** Limit úpravy je použit na základě možnosti **Přesnost zaokrouhlování**, která je určena pro definici sestavy. Pokud například vyberete zaokrouhlení sestavy na tisíce a zadáte hodnotu **2** do pole **Limit částky úpravy**, zobrazí se upozornění, když se hodnota identifikovaná v poli **Řádek vyrovnání rozdílů po zaokrouhlení** zvýší nebo sníží o více než 2 000 Kč.

## <a name="format-row-and-column-text"></a>Formátování textu řádků a sloupců
Změnou písma a formátováním textu můžete přizpůsobit vzhled sestav. Následující části vysvětlují formátování vzhledu řádků a sloupců v sestavách.

### <a name="manage-font-styles"></a>Správa stylů písem

Můžete vytvořit a upravit styly písem pro sestavy. Můžete také použít tyto styly pro dokument nebo konkrétní řádek či sloupec v sestavě.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Vytvoření stylu písma</td>
<td><ol>
<li>V Návrháři sestav v nabídce <strong>Formát </strong>klikněte na tlačítko <strong>Styly a formátování</strong>.</li>
<li>Klikněte na tlačítko <strong>Nový</strong> v dialogovém okně <strong>Styly a formátování</strong> a pak zadejte jedinečný název nového stylu.</li>
<li>Proveďte výběr písem a klikněte na tlačítko <strong>OK</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Úprava stylu písma</td>
<td><ol>
<li>V Návrháři sestav v nabídce <strong>Formát </strong>klikněte na tlačítko <strong>Styly a formátování</strong>.</li>
<li>Vyberte styl k úpravě v dialogovém okně <strong>Styly a formátování</strong> a klikněte na tlačítko <strong>Upravit</strong>.</li>
<li>Proveďte výběr písem a klikněte na tlačítko <strong>OK</strong>.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Použití stylu písma</td>
<td><ol>
<li>V návrháři sestav v definici či definici sloupce nebo v záhlavích a zápatích vyberte jednu nebo více buněk.</li>
<li>V seznamu <strong>Styl</strong> na panelu nástrojů vyberte styl písma.</li>
</ol></td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a>Formátování textu řádků

Formátování určené v definici řádku přepíše formátování určené v definici sloupce a definici sestavy. Pomocí ovládacích prvků na panelu nástrojů formátování můžete upravit formát textu. Jedná se o standardní ovládací prvky systému Microsoft Windows.

1.  V Návrháři sestav otevřete definici řádku k úpravě.
2.  Vyberte buňky k formátování. Chcete-li vybrat více buněk, podržte klávesu Ctrl a vyberte buňky.
3.  Na panelu nástrojů klikněte na tlačítko formátu, který chcete použít. Chcete-li například odsadit řádek, vyberte ho a klikněte na tlačítko **Zvětšit odsazení** ![Zvětšit odsazení](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Zvětšit odsazení") na panelu nástrojů.

### <a name="adjust-columns-while-you-design-reports"></a>Úprava sloupců během návrhu sestav

K usnadnění zobrazování sloupců, se kterými pracujete v definici řádku, můžete upravit šířku sloupce a skrýt (minimalizovat) nebo zobrazit sloupce v podokně náhledu. Provedené úpravy mají vliv pouze na vzhled zobrazení ve sloupcích. Nemají vliv na formátování sloupců v sestavách.

### <a name="change-the-width-of-a-column-in-the-view-pane"></a>Změna šířky sloupce v podokně náhledu

1.  V Návrháři sestav otevřete definici řádku k úpravě.
2.  V nabídce **Formát** klikněte na příkaz **Šířka sloupce**.
3.  V dialogovém okně **Šířka sloupce** zadejte hodnotu a klikněte na tlačítko **OK**. Případně můžete také přetáhnout pravý okraj buňky záhlaví sloupce a změnit tak šířku sloupce.

### <a name="hide-columns-in-the-view-pane"></a>Skrytí sloupců v podokně náhledu

1.  V Návrháři sestav otevřete definici řádku k úpravě.
2.  Vyberte sloupec nebo sloupce, které chcete minimalizovat.
3.  Klikněte pravým tlačítkem myši a poté klikněte na položku **Skrýt**.

### <a name="show-all-hidden-columns-in-the-view-pane"></a>Zobrazení všech skrytých sloupců v podokně náhledu

1.  V Návrháři sestav otevřete definici řádku k úpravě.
2.  Klikněte pravým tlačítkem myši na minimalizovaný sloupec, který chcete zobrazit, a klikněte na tlačítko **Zobrazit**.


<a name="see-also"></a>Viz také
--------

[Finanční výkaznictví](financial-reporting-intro.md)



