---
title: "Definice stromu výkaznictví ve finančních sestavách"
description: "Tento článek obsahuje informace o definicích stromu výkaznictví. Definice stromu výkaznictví je součástí sestavy nebo stavební blok, který pomáhá definovat strukturu a hierarchii vaší organizace."
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 57592
ms.assetid: 747faa47-9a23-4277-bc11-8d0a1267c3a4
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 00219f21076af60f8e2f16ca365b1138bb279400
ms.contentlocale: cs-cz
ms.lasthandoff: 08/13/2018

---

# <a name="reporting-tree-definitions-in-financial-reports"></a>Definice stromu výkaznictví ve finančních sestavách

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o definicích stromu výkaznictví. Definice stromu výkaznictví je součástí sestavy nebo stavební blok, který pomáhá definovat strukturu a hierarchii vaší organizace.

Finanční sestavy podporují flexibilní vykazování, takže lze snadno provádět změny podle změn struktury vaší firmy. Sestavy jsou sestaveny z různých komponent nebo stavebních bloků. Jedním z těchto stavebních bloků je definice stromu výkaznictví. Definice stromu výkaznictví pomáhá definovat strukturu a hierarchii organizace. Jedná se o strukturu hierarchie s více dimenzemi na základě vztahů mezi dimenzemi ve finančních datech. Poskytuje informace na úrovni výkazové jednotky a na souhrnné úrovni pro všechny jednotky ve stromu. Definice stromu výkaznictví lze kombinovat s definicemi sloupců a definicemi sestav a vytvořit skupinu stavebních bloků, které může používat více společností. Jednotka výkaznictví se používá pro každé pole v organizačním grafu. Organizačními jednotkami mohou být jednotlivá oddělení z finančních dat, nebo se může jednat o souhrnné jednotky na vyšší úrovni, ve kterých jsou sloučeny informace z jiných organizačních jednotek. Pro definici sestavy obsahující strom výkaznictví je vytvořena jedna sestava pro každou jednotku výkaznictví a pro úroveň souhrnu. Všechny tyto sestavy používají definice řádků a sloupců, které jsou určené v definici sestavy, pokud definice sestavy nespecifikuje použití stromu výkaznictví z definice řádku. Definice řádků a sloupců jsou důležité součásti pro plánování a fungování finančních sestav. Stromy výkaznictví rozšiřují možnosti komponent a podporují flexibilní vykazování při změnách firemní struktury. Finanční sestavy, které nejsou založeny na stromu výkaznictví, používají pouze některé možnosti finančního výkaznictví. Více definic stromu výkaznictví se stejnými definicemi řádků a sloupců můžete použít k zobrazení dat organizace různými způsoby.

## <a name="reporting-tree-best-practices"></a>Doporučené postupy stromu výkaznictví
Před vytvořením stromu výkaznictví zvažte následující doporučené postupy:

- Určete nejdříve, které dimenze výkaznictví vaše právnická osoba nebo společnost vyžaduje.
- Zvažte, jak je nastavena vaše struktura, a potom vytvořte organizační graf vaší společnosti. Organizační diagram vám pomůže si představit, jak organizační jednotky seskupit do jednoho nebo několika organizačních stromů.
- Začněte nejnižší dostupnou úrovní podrobností, jako jsou například oddělení a projekty definované ve finančních datech. Přidáním požadovaného počtu polí do úrovně podrobností můžete zobrazit divize nebo oblasti vyšší úrovně. Každé pole představuje potenciální jednotku výkaznictví ve stromu výkaznictví, který vytvoříte.
- Rovněž je třeba zvážit nejlepší způsob, jak budovat stromy. Můžete použít automatizovaný proces sestavení k vytvoření stromu výkaznictví, nebo ho můžete vytvořit ručně. Je důležité rozumět oběma způsobům dříve, než budete vytvářet stromové struktury.
- Můžete použít jednotky výkaznictví, které jsou definovány ve vašem systému finančních dat, k přidání jednotek výkaznictví k definici sestavy stromu výkaznictví.

## <a name="create-multiple-reporting-trees"></a> Tvorba více stromů výkaznictví
Můžete vytvořit neomezený počet stromů výkaznictví k zobrazování dat vaší organizace různými způsoby. Každý organizační strom může obsahovat libovolnou kombinaci oddělení a souhrnných jednotek. Definice sestavy může obsahovat odkaz vždy na pouze jeden strom výkaznictví. Změnou uspořádání struktury jednotek výkaznictví můžete vytvořit různé stromy výkaznictví. Potom můžete použít stejné definice řádku a sloupce pro každý strom výkaznictví. Tímto způsobem lze rychle vytvořit různé rozložení finančního výkaznictví. Pokud vytváříte několik různých stromů výkaznictví, můžete vytisknout řadu finančních výkazů každý měsíc, které analyzují a prezentují provoz vaší společnosti různými způsoby. Další informace viz příklady struktury jednotek výkaznictví na konci tohoto článku.

## <a name="create-a-reporting-tree-definition"></a> Vytvoření definice stromu výkaznictví
Definice stromu výkaznictví obsahuje sloupce popsané v následující tabulce.

| Sloupec sestavy výkaznictví | popis |
|-----------------------|-------------|
| Společnost               | Název společnosti pro jednotku výkaznictví. Hodnota **@ANY**, která je obvykle přiřazena pouze na úrovni souhrnu, umožňuje strom výkaznictví používat pro všechny společnosti. Všechny větve podřízených jednotek mají přiřazenu společnost. |
| Název jednotky             | Kód identifikující tuto jednotku výkaznictví v grafickém stromu výkaznictví. Nezapomeňte vytvořit jedinečný systém kódování, který je konzistentní, a které bude snadno pochopitelný pro uživatele. |
| Popis jednotky      | Název jednotky výkaznictví se zobrazí v záhlaví nebo zápatí sestavy, když zadáte hodnotu **UnitDesc** jako kód na kartě **Záhlaví a zápatí** v definici sestavy. Nadpis se zobrazí v sestavě v řádku popisu, pokud zadáte hodnotu **UnitDesc** do buňky **Popis** v definici řádku. |
| Dimenze            | Jednotka výkaznictví, která získává informace přímo z finančních dat. Definuje logické umístění a délky pro účet a související segmenty. Každý řádek sestavy musí mít uveden rozměr v tomto sloupci. Dimenzi můžete vložit také do řádku Souhrn jednotky (například pro výdaje, které přímo souvisejí s touto jednotkou). Zadáte-li dimenzi v řádku jednotky souhrnu, účty, které se používají v nadřazených jednotkách nepoužívejte v podřízených jednotkách. Jinak může docházet ke zdvojování částek. |
| Definice řádku       | Název definice řádku pro jednotku výkaznictví. Stejná definice řádků se používá pro všechny jednotky organizačního stromu. Při generování sestavy se tato definice řádků použije pro jednotlivé organizační jednotky. Definice řádků může obsahovat více odkazů na finanční dimenze. Pokud je v organizačním stromu zadána definice řádků, zaškrtněte políčko **Používat definici řádků z organizačního stromu** na kartě **Sestava** definice sestavy. |
| Odkaz na řádek              | Odkaz na řádek, který chcete použít pro organizační jednotku. Odkazy na řádky definované pro definici řádků umožňují identifikovat finanční dimenze, se kterými se mají propojit. |
| Externí odkaz         | Odkaz na řádek, který chcete použít pro tuto organizační jednotku. Odkazy řádků jsou definovány pro definici řádku k identifikaci sestavy k propojení. |
| Externí soubor         | Cesta k souboru na listu finančního vykazování, ze kterého se budou získávat data. |
| Možnosti stránky          | Tento sloupec určuje, zda jsou potlačeny informace zpravodajské jednotky při zobrazení nebo tisku sestavy. |
| % shrnutí              | Procento jednotky výkaznictví, které má být přiděleno nadřazené jednotce. Procento, které zadáte v tomto sloupci, se vztahuje na každý řádek definice řádku před přidáním hodnoty řádku do nadřazené sestavy. Například pokud má být podřízená jednotka rozdělena rovnoměrně mezi dvě oddělení, částky na každém řádku budou vynásobeny 50 procenty před přidáním hodnoty do sestavy oddělení. Jedna jednotka výkaznictví nemůže mít dvě nadřazené jednotky. Přidělit částky z jednotky výkaznictví do dvou nadřazených jednotek můžete vytvořením jiné jednotky výkaznictví se stejnou dimenzí k zahrnutí dalších 50 procent. Zadejte celá procenta bez desetinného místa. Například **25** představuje 25procentní přidělení k nadřazené jednotce. Pokud přidáte desetinnou čárku (**.25**), k nadřazené jednotce je přiděleno 0,25 %. K použití hodnoty menší než jedno procento použijte možnost **Povolit shrnutí &lt;1%** v definici sestavy. Tato možnost se nachází na kartě **Další možnosti** v dialogovém okně **Nastavení sestavy**. Přístup k tomuto dialogovému oknu nabízí tlačítko **Jiné** na kartě **Nastavení** v definici sestavy. |
| Zabezpečení jednotky         | Omezuje přístup uživatelů a skupin k informacím pro jednotku výkaznictví. |
| Doplňkový text       | Text, který je zahrnutý do sestavy. |

Pomocí následujících kroků vytvořte definici stromu výkaznictví.

1. Otevřete Návrhář sestav.
2. Klikněte na **Soubor** &gt; **Nový** &gt; **Definice stromu výkaznictví**.
3. Klikněte na **Upravit** &gt; **Vložit jednotky výkaznictví z dimenzí**.
4. V dialogovém okně **Vložit jednotky výkaznictví z dimenzí** zaškrtněte políčka všech dimenzí, které mají být zahrnuty ve stromu výkaznictví. Dialogové okno **Vložit jednotky výkaznictví z dimenzí** obsahuje následující oddíly.

    | Oddíl                          | Popis |
    |----------------------------------|-------------|
    | Segmentace dimenze vykazování | Pomocí tlačítek **Rozdělit segmenty** a **Sloučit segmenty** můžete změnit počet a délku segmentů.<blockquote>[!NOTE] Sloučit lze pouze segmenty, které jste rozdělili. Sloučit více dimenzí můžete použitím zástupných znaků ve vašich hodnotách dimenzí.</blockquote> |
    | Zahrnout / pozice znaku       | Tato sekce obsahuje seznam dimenzí definovaných ve finančních datech a uvádí počet znaků v nejdelší definované hodnotě pro každou dimenzi. Zaškrtněte políčko pro dimenzi k zahrnutí dané dimenze do hierarchie stromu výkaznictví. |
    | Hierarchie a rozsahy segmentů     | Tento oddíl ukazuje hierarchii dimenze. Dimenze lze přesunout v seznamu a změnit jejich pořadí vykazování. V polích **Od dimenze** a **Do dimenze** stanovte rozmezí hodnot v rámci jednotlivých dimenzích. Pokud neurčíte rozsah, všechny hodnoty dimenzí budou vloženy do stromu výkaznictví.<blockquote>[!NOTE] Používáte-li více než jednu dimenzi, budou ve výsledcích vráceny pouze kombinace dimenzí, které byly zaúčtovány.</blockquote> |

    Pokud vás zajímá snímek obrazovky, který ukazuje příklad pole **Vložit jednotky výkaznictví z dimenzí**, přejděte k části „Příklad vložení jednotky výkaznictví z dialogového okna Dimenze“ dále v tomto článku.

5. Chcete-li vytvořit další segmenty, například rozdělením jednoho segmentu na dva kratší segmenty, klikněte na odpovídající místo v poli **Pozice znaku** a poté klikněte na tlačítko **Rozdělit segmenty**.
6. Pro sloučení dvou segmentů v jeden segment klikněte do pole některého ze segmentů ke sloučení a klikněte na tlačítko **Sloučit segmenty**.
7. Hierarchie definuje, jak jsou dimenze vykazovány mezi sebou, a určuje rozsah pro každou dimenzi. Chcete-li změnit hierarchii dimenzí v oblasti **Hierarchie a rozsahy segmentů**, vyberte dimenzi, kterou chcete přesunout, a poté klikněte na tlačítko **Přesunout nahoru** nebo **Přesunout dolů**.
8. Chcete-li definovat rozsah hodnot dimenze k přidání do nového stromu výkaznictví, v oblasti **Hierarchie a rozsahy segmentů**, postupujte následujícím způsobem:

    1. V poli **Od dimenze** pro tuto dimenzi zadejte první hodnotu v rozsahu.
    2. V poli **Do dimenze** zadejte poslední hodnotu v rozsahu.

9. Pro každou dimenzi v oblasti **Hierarchie a rozsahy segmentů** zopakujte krok 7 a 8.
10. Po dokončení definování způsobu zanášení jednotek výkaznictví do nového stromu výkaznictví klikněte na tlačítko **OK**.
11. Chcete-li uložit strom výkaznictví, klikněte na **Soubor** &gt; **Uložit**. Zadejte jedinečný název a popis stromu výkaznictví a klikněte na tlačítko **OK**.

### <a name="open-an-existing-reporting-tree-definition"></a>Otevření existující definice stromu výkaznictví

1. V Návrháři sestav v navigačním podokně klikněte na tlačítko **Definice stromu výkaznictví**.
2. Otevřete strom výkaznictví kliknutím dvakrát na název v seznamu.
3. Chcete-li zobrazit jakékoli stavební bloky, které jsou přidruženy ke stromu výkaznictví, klikněte pravým tlačítkem myši na definici stromu výkaznictví a poté vyberte možnost **Přidružení**.

### <a name="roll-up-data-in-a-reporting-tree"></a>Shrnutí dat ve stromu výkaznictví

Díky použití stromu výkaznictví můžete agregovat částky z podřízených jednotek výkaznictví na úrovni nadřazené jednotky výkaznictví. Tato agregace je označována jako shrnutí dat. Pro shrnutí částek do nadřazených jednotek ve stromu výkaznictví se používají následující pravidla:

- V rámci stromu sestav musí podřízené jednotky obsahovat dimenze, pokud se nejedná o strom výkaznictví s jednou úrovní. Nadřazené jednotky obvykle neobsahují dimenze ve stromu výkaznictví.

    > [!NOTE]
    > Určení dimenzí pro podřízené jednotky i nadřazené jednotky může způsobit duplikaci dat v sestavě.

- Jednotky výkaznictví, které obsahují dimenze ve stromu výkaznictví, odpovídají dimenzím, které se používají v definicích řádků a sloupců. Kombinace dimenzí určuje částky vrácené pro danou jednotku. Například u příkladu č. 2 dále v tomto článku se na řádku 6 a 7 vrátí hodnoty pouze pro oddělení 00 a 01.
- Částky nadřazených jednotek výkaznictví, které neobsahují žádné dimenze ve stromu výkaznictví, se určují na základě sestavy podřízené jednotky a zahrnují částku do určené nadřazené jednotky. Například pokud má nadřazená jednotka (viz Contoso USA v příkladu 2 Shrnutí dat) dvě podřízené jednotky (022 a 023) a neobsahuje dimenze, sestava bude vygenerována pro každou podřízenou a nadřazenou položku. Nadřazený součet je součtem částek dvou podřízených položek.

### <a name="manage-reporting-units"></a>Správa jednotek výkaznictví

Každá definice stromu vykazování se zobrazí v jedinečném zobrazení. K dispozici je grafické zobrazení pro vizualizaci hierarchie nadřízených a podřízených položek a zobrazení listu uvádějící konkrétní informace pro každou jednotku výkaznictví. Grafické zobrazení a zobrazení listu jsou připojena. Když vyberete jednotku výkaznictví v jednom zobrazení, vybere se také ve druhém zobrazení. Je možné vytvářet hierarchie s více dimenzemi na základě vztahů mezi dimenzemi ve finančních datech. Při vytváření definice stromu výkaznictví můžete použít stejné definice řádku opakovaně, ať už generujete výkaz příjmů oddělení nebo konsolidovaný souhrnný výkaz příjmů. Dimenze, které jsou definovány v definici řádku, lze kombinovat s dimenzemi v definici stromu výkaznictví za účelem získání řady přehledů výsledků vaší organizace.

### <a name="reporting-unit-structure"></a> Struktura jednotky výkaznictví

Ve finančním výkaznictví se používají následující typy jednotek výkaznictví:

- Jednotka podrobností získává informace přímo z finančních dat, z tabulky aplikace Excel nebo z jiného listu pro finanční výkaznictví.
- Jednotka souhrnu obsahuje souhrn dat z jednotek nižší úrovně.

Nadřazená jednotka výkaznictví je jednotka souhrnu, která agreguje souhrnné informace z jednotky podrobností. Jednotka souhrnu může být zároveň jednotkou podrobností i jednotkou souhrnu. To znamená, že jednotka souhrnu může získávat informace z jednotky nižší úrovně, finančních dat nebo tabulky aplikace Excel. Nadřazená jednotka může být podřízenou jednotkou vyšší nadřazené jednotky. Podřízená jednotka výkaznictví může být jednotkou podrobností, která získává informace přímo z finančních dat nebo tabulky aplikace Excel. Podřízená jednotka vykazování může být také zprostředkující jednotkou souhrnu. Jinými slovy může být nadřazená jednotka jednotky nižší úrovně, ale také podřízená jednotka souhrnné jednotky na vyšší úrovni. Nejběžnější scénář pro jednotky výkaznictví je použití nadřazených jednotek s prázdnou buňkou ve sloupci **Dimenze** a podřízených jednotek s odkazy na konkrétní nebo zástupné kombinace dimenzí.

### <a name="organize-reporting-units"></a> Uspořádání jednotek výkaznictví

Organizační strukturu definice organizačního stromu můžete uspořádat přesunutím organizačních jednotek v grafickém zobrazení. Můžete také povyšovat jednotky výkaznictví na vyšší úrovně ve stromu výkaznictví a přesunovat je na nižší úrovně.

1. V Návrháři sestav otevřete definici stromu výkaznictví k úpravě.
2. V grafickém zobrazení definice stromu výkaznictví vyberte jednotku výkaznictví.
3. Přetáhněte jednotku na nové místo. Případně klikněte pravým tlačítkem na jednotku a vyberte možnost **Zvýšit úroveň jednotky výkaznictví** nebo **Snížit úroveň jednotky výkaznictví**.
4. Klepnutím na **Soubor** &gt; **Uložit** uložte změny.

### <a name="add-text-about-a-reporting-unit"></a> Přidání textu o jednotce výkaznictví

Záznam dodatečného textu je statický textový řetězec o nejvýše 255 znacích, který přidá informace do definice stromu výkaznictví. Příkladem dodatečného textu je například stručný popis společnosti. Můžete vytvořit maximálně deset položek doplňkového textu pro každou jednotku výkaznictví v definici stromu výkaznictví. Doplňkový text se zobrazí v sestavě pro jednotku výkaznictví, k níž je přiřazen. Můžete přidat textové položky ze sloupce **Popis** v definici řádku a z karty **Záhlaví a zápatí** v definici sestavy.

1. V Návrháři sestav otevřete definici stromu výkaznictví k úpravě.
2. Klikněte dvakrát na buňku **Doplňkový text** pro řádek jednotky výkaznictví.
3. V dialogovém okně **Doplňkový text** na prvním prázdném řádku zadejte text. První řádek, který obsahuje text, je odkazován jako UnitText1, bez ohledu na pozici v dialogovém okně **Doplňkový text**.
4. Přidat další položky textu pro tuto jednotku výkaznictví můžete zadáním textu do prázdného řádku.
5. Klepněte na tlačítko **OK**.

### <a name="remove-additional-text-from-a-reporting-unit"></a>Odebrání doplňkového textu z jednotky výkaznictví

1. V Návrháři sestav otevřete definici organizačního stromu, kterou chcete změnit.
2. Dvakrát klikněte na buňku **Doplňkový text** pro řádek organizační jednotky.
3. V dialogovém okně **Doplňkový text** vyberte položku k odstranění a klikněte na položku **Vymazat**. Případně klikněte pravým tlačítkem myši a vyberte možnost **Vyjmout**.
4. Klepněte na tlačítko **OK**.

### <a name="restrict-access-to-a-reporting-unit"></a>Omezení přístupu k jednotce výkaznictví

Můžete zabránit určitým uživatelům a skupinám v přístupu k jednotkám výkaznictví. Můžete také definovat omezení, aby se vztahovaly na podřízené jednotky vykazování v jednotce vykazování.

1. V Návrháři sestav otevřete definici stromu výkaznictví k úpravě.
2. Dvakrát klikněte na buňku **Zabezpečení jednotky** v řádku organizační jednotky, k níž chcete omezit přístup.
3. V dialogovém okně **Zabezpečení jednotky** klikněte na tlačítko **Uživatelé a skupiny**.
4. Vyberte uživatele nebo skupiny, které budou mít přístup k jednotce výkaznictví a klikněte na tlačítko **OK**.
5. Chcete-li omezit přístup k podřízeným jednotkám výkaznictví, zaškrtněte políčko **Přidat zabezpečení k podřízeným jednotkám výkaznictví**.
6. Klepněte na tlačítko **OK**.

### <a name="remove-access-to-a-reporting-unit"></a>Odebrání přístupu k jednotce výkaznictví

1. V Návrháři sestav otevřete definici stromu výkaznictví k úpravě.
2. Klikněte dvakrát na buňku **Zabezpečení jednotky** pro řádek jednotky výkaznictví, jejíž přístup chcete odebrat.
3. V dialogovém okně **Zabezpečení jednotky** zvolte název a klikněte na tlačítko **Odebrat**.
4. Klepněte na tlačítko **OK**.

### <a name="link-to-reports"></a>Odkaz na sestavy

Po vytvoření sloupce **Sestava** v definici řádku a určení sestavy k zahrnutí v sestavě musíte aktualizovat stromu výkaznictví pomocí propojeného sloupce a informací o sestavě. Sestavu lze importovat do jakékoli jednotky ve stromu výkaznictví.

### <a name="identify-the-report-in-a-reporting-tree"></a>Identifikace sestavy ve stromu výkaznictví

1. V Návrháři sestav otevřete definici stromu výkaznictví k úpravě.
2. Buňky ve sloupci **Definice řádku** zobrazují informace na základě informací vybraného řádku, protože stejná definice řádku musí být použita ve všech jednotkách stromu výkaznictví. Klikněte dvakrát na buňku **Definice řádku** a poté vyberte definici řádku, která obsahuje informace o sestavě.
3. V buňce **Odkaz listu** pro jednotku výkaznictví, vyberte název odkazu, který odpovídá sestavě.
4. V buňce **Cesta sešitu nebo sestavy** pro jednotku výkaznictví zadejte název sestavy nebo vyhledejte a vyberte sestavu.
5. Chcete-li určit list v sestavě, zadejte název listu do buňky **Název listu**.
6. Zopakujte kroky 3 až 5 pro každou jednotku výkaznictví, která má získat data ze sestavy. Abyste zabránili zobrazení nesprávných dat v sestavě, ujistěte se, že se správné názvy sestav zobrazují v odpovídající jednotce stromu výkaznictví.

## <a name="examples"></a>Příklad
### <a name="reporting-unit-structure--example-1"></a>Struktura jednotky výkaznictví – příklad 1

V následujícím stromu výkaznictví je uvedena struktura jednotek výkaznictví:

- Jednotka výkaznictví Japonska Contoso je nadřazená jednotka podřízené jednotky Prodej Contoso Japonsko a Konzultace Contoso Japonsko.
- Jednotka divize Prodej Contoso Japonsko je zároveň podřízená jednotce Contoso Japonsko a nadřazená jednotkám Domácí prodej a Automatický prodej.
- Jednotky výkaznictví podrobností na nejnižší úrovni (Domovní prodej, Automatický prodej, Klientské služby a Provoz) představují oddělení ve finančních datech. Tyto jednotky výkaznictví jsou v šedé oblasti diagramu.
- Jednotky souhrnu na vyšší úrovni shrnují informace z jednotek podrobností.

[![ContosoEntertainmentSummaryReportStructure](./media/contosoentertainmentsummaryreportstructure.png)](./media/contosoentertainmentsummaryreportstructure.png)

### <a name="reporting-unit-structure--example-2"></a>Struktura jednotky výkaznictví – příklad 2

Následující diagram znázorňuje strom výkaznictví zobrazující organizační strukturu, která je rozdělena podle firemní funkce.

[![summaryofallunitscontoso](./media/summaryofallunitscontoso.png)](./media/summaryofallunitscontoso.png)

### <a name="example-of-the-insert-reporting-units-from-dimensions-dialog-box"></a>Příklad dialogového okna Vložit jednotky výkaznictví z dimenzí

V následujícím příkladu dialogové okno **Vložit jednotky výkaznictví z dimenzí** obsahuje následující informace. V tomto příkladu vrátí výsledky kombinaci obchodních jednotek, nákladových středisek a oddělení.

[![InsertReportingUnits](./media/insertreportingunits.png)](./media/insertreportingunits.png)

Výsledná definice stromu výkaznictví je řazena podle organizační jednotky, potom podle nákladového střediska a nakonec podle oddělení. Dimenze páté jednotky výkaznictví je **Obchodní jednotka = \[001\], Nákladové středisko =\[\], Oddělení = \[022\]**, a identifikuje jednotky výkaznictví pro účty, které jsou specifické pro obchodní jednotku 001 a oddělení 022.

[![Strom výkaznictví](./media/reportingtree-1024x646.png)](./media/reportingtree.png)

### <a name="examples-of-data-roll-up"></a>Příklady shrnutí dat

Následující příklady ukazují možné informace, které jsou použity v definici stromu výkaznictví pro shrnutá data.

#### <a name="example-1"></a>Příklad 1

[![MutliCompanyRollUp](./media/mutlicompanyrollup.png)](./media/mutlicompanyrollup.png)

#### <a name="example-2"></a>Příklad 2

[![CrossCompanyDepartmentRollUp](./media/crosscompanydepartmentrollup.png)](./media/crosscompanydepartmentrollup.png)

## <a name="additional-resources"></a>Další zdroje

[Finanční výkaznictví](financial-reporting-intro.md)

