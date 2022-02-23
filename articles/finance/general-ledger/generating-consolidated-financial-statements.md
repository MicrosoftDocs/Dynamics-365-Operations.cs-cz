---
title: Vytváření konsolidovaných finančních výkazů
description: Toto téma popisuje různé scénáře, jak můžete vygenerovat konsolidované finanční výkazy.
author: aprilolson
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: a32fb8cce4353f57155fc7a723aa90e3c17178e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441208"
---
# <a name="generate-consolidated-financial-statements"></a>Vytváření konsolidovaných finančních výkazů

[!include [banner](../includes/banner.md)]

Toto téma popisuje různé scénáře, jak můžete vygenerovat konsolidované finanční výkazy.

## <a name="single-level-and-multilevel-consolidations-across-legal-entities"></a>Jednoúrovňové a mnohoúrovňové konsolidace mezi právnickými osobami
Nejjednodušší metodou konsolidace prostřednictvím finančního výkaznictví je použít organizační stromy k agregaci dat ve všech společnostech, které mají stejné účtové osnovy a fiskální období. Zde jsou hlavní kroky konsolidace pomocí organizačního stromu.

1. Vytvořte definici řádku a ujistěte se, že řádky obsahují všechny příslušné účty ve všech společnostech.
2. Vytvořte definici sloupců, která zahrnuje všechny sloupce, které jsou požadovány pro sestavu, kterou vytváříte.
3. Vytvořte organizační strom, který obsahuje uzel výkaznictví pro každou společnost, kterou používáte v konsolidovaných sestavách.

> [!TIP]
> Další informace o postupu při vytváření a správě definic řádků, definic sloupců a organizačního stromu naleznete v tématu [Součásti finančních sestav](../../dev-itpro/analytics/financial-report-components.md).

Následující obrázek znázorňuje použití definice organizačního stromu ve finančními výkaznictví k identifikaci jednotlivých společností, které budete konsolidovat.

![Definice organizačního stromu](./media/reporting-tree-definition.png "Definice organizačního stromu")

Konsolidovaná sestava na následujícím obrázku znázorňuje, že když použijete organizační strom spolu definicí sestavy, každou společnost můžete zobrazit zvlášť. Konsolidované částky jsou zobrazeny na souhrnné úrovni.

![Úroveň souhrnu konsolidované částky](./media/consolidate-amount-summary-level.png "Úroveň souhrnu konsolidované částky")

Můžete také vytvořit víceúrovňový organizační strom s tolika úrovněmi, kolik potřebujete. Následující obrázek znázorňuje víceúrovňový organizační strom, který obsahuje shrnutí podle celosvětové oblasti.

![Definice stromu víceúrovňového vykazování se zahrnutím podle oblasti](./media/multilevel-reporting-tree-definition-roll-ups-worldwide-region.png "Definice stromu víceúrovňového vykazování se zahrnutím podle oblasti")

Následující obrázek znázorňuje víceúrovňový organizační strom, který obsahuje shrnutí podle funkce.

![Definice stromu víceúrovňového vykazování se zahrnutím podle funkce](./media/multilevel-reporting-tree-definition-roll-ups-by-function.png "Definice stromu víceúrovňového vykazování se zahrnutím podle funkce")

### <a name="viewing-companies-side-by-side"></a>Zobrazení společností vedle sebe
Mnozí zákazníci preferují sestavy, ve kterých se společnosti zobrazují vedle sebe a kde sloupce zobrazují celkové konsolidované součty. Tento formát lze jednoduše použít po vytvoření organizačního stromu. Zde jsou hlavní kroky, jak zobrazit společnosti vedle sebe na konsolidovaných finančních výkazech.

1. Pro každou společnost vytvořte definici sloupce, která obsahuje sloupec **Finanční dimenze**.
2. Pomocí pole **Organizační jednotka** vyberte pro každý sloupec strom a organizační jednotku.
3. Volitelné: Přidejte záhlaví a sloupce součtů.

Následující obrázek znázorňuje definici sloupce ve formátu vedle sebe.

![Definice sloupce ve formátu vedle sebe](./media/column-definition-side-by-side-format.png "Definice sloupce ve formátu vedle sebe")

## <a name="consolidations-that-use-organization-structures-that-are-created-from-legal-entities"></a>Konsolidace, které používají organizační struktury vytvořené právnických osob
Organizační hierarchie, které obsahují dimenze nebo právnické osoby, dynamicky vytváří definice organizačního stromu v rámci finančního výkaznictví. Snadným způsobem, jak zefektivnit konsolidace, je přidat organizační hierarchii do vaší sestavy v rámci finančního výkaznictví. Podle data sestavy pak finanční výkaznictví vybere organizační hierarchii k datu účinnosti nebo před datem účinnosti, jak je znázorněno na následujícím obrázku.

![Dynamické vytváření definice stromu výkaznictví](./media/dynamically-create-reporting-tree-definitions.png "Dynamické vytváření definice stromu výkaznictví")

## <a name="consolidations-that-involve-eliminations"></a>Konsolidace zahrnující eliminace
Transakce eliminací jsou běžnou součástí procesu konsolidace. V tomto příkladu je během konsolidace eliminováno pět účtů: 142600 211400, 401420, 401180 a 510820. Společnosti mohou mít mezi vnitropodnikové účty nastaveny různě. Některé společnosti například používají jako poslední číslici 9, pokud je účet používán pro vnitropodnikové transakce. Bez ohledu na metodu – pokud znáte vnitropodnikové účty, na svých konsolidovaných finančních výkazech můžete zobrazovat eliminace.

Následující obrázek znázorňuje definici sloupce pro konsolidovanou výsledovku. Tři vnitropodnikové účty zisků a ztrát jsou definovány pro každou společnost s použitím filtru dimenze. Sloupec D obsahuje eliminace účtů pouze pro společnost USMF a sloupec E obsahuje eliminace pouze pro společnost DEMF. Sloupce E i D jsou nastaveny tak, aby **nebyly** vytištěny ve finančním výkazu.

![Definice sloupce - konsolidovaný výpis příjmů](./media/column-definition-consolidated-income-statement.png "Definice sloupce - konsolidovaný výpis příjmů")

Ve vygenerované sestavě jsou eliminované částky vypočteny ve sloupcích F, G a H a jejich součet je uveden ve sloupci I. Sloupec J zobrazuje konsolidované částky. Tyto konsolidované částky vylučují eliminace pro společnosti USMF, USRT a DEMF.

> [!TIP]
> Vytvořte druhou sestavu, která zobrazí pouze položky eliminace, použijte ji ve skupině sestavy, která obsahuje konsolidovanou sestavu. Tímto způsobem máte všechny potřebné informace pro vytvoření libovolných položek, které jsou vyžadovány.

Následující obrázek znázorňuje konsolidovanou sestavu.

![Konsolidovaná sestava výpisu příjmů](./media/consolidated-report-income-statement.png "Konsolidovaná sestava výpisu příjmů")

Zda používáte účty, dimenze nebo obojí, finanční výkaznictví vám umožňuje filtrovat položky eliminace pomocí funkce filtrování dimenzí.

## <a name="minority-interest"></a>Minoritní podíl
Společnost může vlastnit pouze procento jiné společnosti. V takovém případě při tvorbě konsolidované sestavy je důležité zaúčtovat pouze procento, které společnost vlastní. Finanční výkaznictví nabízí několik způsobů, jak zobrazovat minoritní podíl v závislosti na předvolbě uživatele. Jeden způsob je použít souhrnné procento v definici organizačního stromu. Další možností je v sestavě zobrazit menšinové vlastnictví jako samostatný řádek.

### <a name="using-the-reporting-tree-definition"></a>Použití definice organizačního stromu
V definici organizačního stromu zadejte do sloupce **Zahrnutí (%)** (sloupec H) procento vlastnictví, jak je ukázáno na následujícím obrázku. Na vygenerované sestavě se tohle procento použije k výpočtu konsolidované částky. V tomto případě vlastní společnost Contoso pouze 80 procent společnosti Contoso Germany. Ve sloupci **Zahrnutí (%)** můžete zadat buď **80** nebo **.8** a na úrovni konsolidace bude zahrnuto 80 procent.

> [!NOTE]
> Tohle procento vlastnictví můžete použít na libovolnou organizační jednotku a nikoli pouze na úrovni společnosti. 

![Procento použití definice organizačního stromu](./media/Using-reporting-tree-definition-percentage.png "Procento použití definice organizačního stromu")

Ve vygenerované sestavě bude sestava společnosti Contoso Germany zobrazovat 100 procent prodejní částky a 80 procent částky bude přiděleno a zahrnuto na konsolidované úrovni pro prodej.

Vlastníte-li méně než 1 procento společnosti, můžete zaškrtnout políčko **Povolit zahrnutí nižší než 1 %** na kartě **Další možnosti** stránky **Nastavení sestav**, jak je uvedeno na následujícím obrázku. V tomto případě budou hodnoty **Zahrnutí (%)** v organizačním stromu považovány za menší než 1 procento. Zadáte-li například **.8**, 0,8 procenta bude zahrnuto na konsolidované úrovni, nikoli 80 procent. Případně lze dosáhnout stejného výsledku ponecháním zaškrtávacího políčka **Povolit zahrnutí nižší než 1 %** jako prázdné a zadáním hodnoty **.008** ve sloupci **Zahrnutí (%)**.

![Možnosti nastavení výkaznictví](./media/reporting-setting-options.png "Možnosti nastavení výkaznictví")

### <a name="showing-ownership-as-a-separate-row-on-the-consolidated-report"></a>Zobrazení vlastnictví jako samostatného řádku v konsolidované sestavě
Jinou možností pro minoritní podíl je zobrazit 100 procent dceřiné společnosti pro každý řádek v sestavě, ale odečíst nekontrolní podíl od čistého příjmu.

Následující obrázek znázorňuje, že v definici řádku lze použít příkaz **IF THEN ELSE** a omezení sloupce pro výpočet minoritního podílu ve finančních výkazech.

![Zobrazení vlastnictví jako samostatného řádku v konsolidované sestavě](./media/Showing-ownership-separate-row-consolidated-report.png "Zobrazení vlastnictví jako samostatného řádku v konsolidované sestavě")

## <a name="multiple-charts-of-accounts-across-legal-entities"></a>Více účtových osnov mezi právnickými osobami
Různé právnické osoby mají často různé účtové osnovy, ale i tak chtějí vytvářet konsolidované finanční výkazy. V takovém případě lze finanční výkaznictví použít ke konsolidaci dat, takže je možné vygenerovat konsolidované finanční výkazy. Zde jsou hlavní korky při konsolidaci, pokud mezi právnickými osobami existují různé účtové osnovy.

1. Vytvořte definici řádku, která obsahuje více odkazů na finanční dimenze. Měl by existovat jeden odkaz pro každou účtovou osnovu.
2. Použijte omezení organizační jednotky v definici sloupce pro přiřazení každé společnosti k příslušnému sloupci.


Do každého řádku v definici řádku lze pro každou jedinečnou účtovou osnovu společnosti přidat více odkazů na finanční dimenze. Na následujícím obrázku používá společnost USMF sadu účtů v prvním sloupci **Odkaz na finanční dimenze** (sloupec J) a společnost DEMF používá účty ve druhém sloupci **Odkaz na finanční dimenze** (sloupec K).

> [!TIP]
> Další informace o buňce **Odkaz na finanční dimenze** najdete v tématu Zadání buňky Odkaz na finanční dimenze.

![Nastavení prvního odkazu účtů na finanční dimenze](./media/set-accounts-first-Link-to-Financial-Dimensions.png "Nastavení prvního odkazu účtů na finanční dimenze")

Organizační strom můžete použít k definování, který odkaz na finanční dimenze z definice řádku se použije na jednotlivé společnosti. Ve sloupci E vyberte definici řádku a poté vyberte příslušný odkaz na řádek ve sloupci F, jak je ukázáno na následujícím obrázku.

![Propojení použité definice řádku finančních dimenzí](./media/link-financial-dimensions-row-definition-used.png "Propojení použité definice řádku finančních dimenzí")

> [!TIP]
> Při vytváření odkazů na finanční dimenze použijte popisy k identifikaci společností, na které se vztahují jednotlivé odkazy. Tímto způsobem můžete snadněji vybrat správnou společnost při vytváření organizačního stromu. Ve definici sloupce vám pole **Organizační jednotka** umožňuje omezit každý sloupec na jednotku organizačního stromu, takže můžete zobrazit data vedle sebe. Pokud pro sloupec neoznačíte konkrétní společnost, budou zobrazeny konsolidovaná data pro všechny společnosti.

## <a name="different-fiscal-calendars-across-multiple-legal-entities"></a>Různé fiskální kalendáře mezi více právnickými osobami
Různé právnické osoby mohou mít různé fiskální kalendáře, ale i tak jsou potřeba pro vytváření konsolidovaných finančních výkazů. Existují dva způsoby konsolidace, pokud mezi právnickými osobami existují různá fiskální období:

- Vytvořte definici sloupce a pomocí období a roku namapujte příslušná období na jednotlivé společnosti.
- V **Nastavení** \> **Další** \> **Další možnosti** vyberte, zda chcete konsolidovat pomocí koncového data období nebo čísla období.

Při vytváření definice sloupce pro několik společností, které mají různé fiskálních období, je důležité zvážit, která společnost bude přiřazena k poli **Název společnosti** v definici sestavy. Fiskální kalendář takové společnosti se použije jako základní fiskální kalendář pro definici sestavy. Následující tabulka například zobrazuje nastavení fiskálního období pro společnosti USMF a INMF. Pro konsolidované sestavy chcete použít fiskální kalendář, který používá společnost USMF. Sloupec „Mapování“ zobrazuje ekvivalentní období a rok pro každou společnost, je-li sestava vytvořena pro 30. června 2018.

| Společnost   | Fiskální rok                                  | Mapování                     |
|-----------|----------------------------------------------|-----------------------------|
| USMF      | Fiskální rok, 1. červenec až 30. červen          | Období 12, fiskální rok 2018 | 
| INMF      | Kalendářní rok, 1. leden až 31. prosinec | Období 6, fiskální rok 2018  |

Na následujícím obrázku je v definici sestavy v poli **Název společnosti** zadána společnost USMF. Proto se fiskální kalendář společnosti USMF použije jako základní fiskální kalendář. V tomto příkladu při generování sestavy k 30. červnu 2018 použije společnost USMF ZÁKLADNÍ období, které je v definici sestavy definováno jako období 12. Společnost INMF použije ZÁKLAD-6, tj. období 6. Oba sloupce budou obsahovat data pro červen 2018.

![Základní období sestavy](./media/report-base-period.png "Základní období sestavy")

Následující obrázek znázorňuje možnosti v definici sestavy, která vám umožňuje vybrat, zda se pro konsolidaci použije číslo období nebo koncové datum období.

![Možnosti čísla období definice sestavy](./media/options-report-definition-period-number.png "Možnosti čísla období definice sestavy")

## <a name="business-unit-consolidations"></a>Konsolidace obchodní jednotky
Toto téma se zaměřuje na používání definicí organizačního stromu a organizační hierarchie ve finančním výkaznictví pro účely konsolidace. Pro vytváření sestav konsolidace obchodní jednotky, jako jsou například sestavy týkající se celosvětových prodejů nebo operací, můžete použít také organizační strom. Tyto sestavy jsou běžné požadavky. Chcete-li je vytvořit, pro každou jednotku, kterou chcete konsolidovat, vyberte společnost a dimenzi. Například na následujícím obrázku je souhrnu organizační jednotky dosaženo opakováním jednotlivých společností ve sloupci **Společnost** (sloupec A) a identifikací skupiny hodnot dimenze Oddělení na společnost ve sloupci **Dimenze** (sloupec D).

![Sestavy konsolidace obchodní jednotky](./media/business-unit-consolidation-reports.png "Sestavy konsolidace obchodní jednotky")

## <a name="consolidations-that-involve-multiple-reporting-currencies"></a>Konsolidace, které obsahují více měn vykazování
Finanční výkaznictví nabízí větší flexibilitu při zobrazení skutečných dat, rozpočtových dat, dat kontroly rozpočtu a dat plánování rozpočtu v různých měnách. Přenesením klíčových dat nastavení nemusíte provádět žádné další nastavení finančního výkaznictví kvůli zobrazení jakékoli sestavy v libovolné měně kdykoli pro libovolného uživatele.

### <a name="prerequisites"></a>Požadavky
Pro správný výpočet přeložených zůstatků vyžaduje finanční výkaznictví, aby byla kategorie **Účet nerozděleného zisku** přidělena k účtu nerozděleného zisku v seznamu **Hlavní účet**. Finanční výkaznictví nepodporuje zaúčtování na účet nerozděleného zisku. Jsou-li transakce zaúčtovány na účet nerozděleného zisku, přeložené zůstatky nebudou správně vypočteny. Doporučujeme, aby uživatelé nastavili další účet nerozděleného zisku kvůli zaúčtování úprav na účet nerozděleného zisku.

V hlavním účtu musejí být pro každý účet nastavena pole **Typ směnného kurzu finančního výkaznictví** a **Typ převodu měny** pole na pevné záložce **Finanční výkaznictví**, jak je ukázáno na následujícím obrázku. Tento úkol můžete dokončit účet po účtu, nebo můžete použít šablony účtů, kterými můžete změny snadno prosadit.

- V poli **Typ směnného kurzu finančního výkaznictví** vyberte typ směnného kurzu, který obsahuje měny a směnné kurzy, které mají být použity pro účet. Tato tabulka měn a směnné kurzy se použijí pro skutečná data v rámci finančního výkaznictví.
- V poli **Typ převodu měny** vyberte metodu pro výpočet směnného kurzu pro účet. Tato metoda měny se používá pro skutečná a rozpočtová data v rámci finančního výkaznictví.

![Hlavní účty finančního výkaznictví](./media/Financial-reporting-main-accounts.png "Hlavní účty finančního výkaznictví")

Pro data rozpočtu, data kontroly rozpočtu a data plánování rozpočtu je definován typ směnného kurzu na stránce **Hlavní kniha**. Tato tabulka se použije pro vytáhnutí směnných kurzů a dále se použije typ převodu měny přiřazený k účtu.

### <a name="currency-translation-methods"></a>Metody převodu měny
Existují čtyři možnosti pro výpočet směnných kurzů v rámci finančního výkaznictví:

- **Vážený průměr** – tato metoda se nejčastěji používá pro účty zisků a ztrát. Používá se následující vzorec:

    (Směnný kurz x počet dnů platnosti) ÷ počet dnů za období

- **Průměr** – tato metoda je alternativní metoda pro účty zisků a ztrát. Používá se následující vzorec:

    Součet směnných kurzů ÷ počet směnných kurzů

- **Aktuální** – tato metoda se používá nejčastěji pro rozvahové účty. Použitý směnný kurz je sazba k datu nebo před datem sestavu nebo sloupce v rámci finančního výkaznictví.
- **Datum transakce** – tato metoda se používá pro účty dlouhodobého majetku. Použitý směnný kurz je sazba ke dni, kdy byl majetek získán. Pokud není pro dané datum zadána sazba, použije se předchozí kurz, který byl zadán k nejbližšímu datu pořízení majetku.

### <a name="report-designer-options-for-currency-translation"></a>Možnosti návrháře sestav pro převod měn
V rámci finančního výkaznictví lze zobrazit libovolná sestava v libovolném počtu měn. Následující pole v definici sestavy podporují tuto funkci:

- Část **Informace o měně** na straně **Definice sestavy**. Tato část zobrazuje měnu, ve které jsou při vygenerování sestavy zobrazeny hodnoty.
- Nové zaškrtávací políčko **Zahrnout všechny měny sestavy**. Jestliže je toto políčko zaškrtnuto, sestavu pro jednotlivé měny vykazování přidáte do fronty sestavy za vygenerovanou sestavu, která používá funkční měnu společnosti. Je-li toto políčko prázdné, měnu vykazování můžete stále vybrat ve webovém prohlížeči. V takovém případě se měna vykazování zpracuje pouze v případě, že ji vyberete.

Možnosti definice sestavy umožňují sestavu snadno převést na všechny měny vykazování. Proto je možné eliminovat definice duplicitní definice sestav, které se liší pouze použitými měnami. Chcete-li sestavu zobrazující více měn vedle sebe, můžete dále použít pole **Zobrazení měny** na stránce **Definice sloupce**, čímž převedete pouze tento sloupec sestavy na alternativní měnu vykazování.

### <a name="currency-translation-adjustment"></a>Úprava převodu měny
Úprava převodu měny (CTA) je rozdíl mezi sazbami, které se používají k výpočtu rozvahové účty, a sazbou, která je použita pro účty výsledovky. Rozdíl způsobí, rozvaha je mimo zůstatek. Pomocí finančního výkaznictví můžete vypočítat CTA dvěma způsoby:

- Použijte stránku **Vyrovnání rozdílů po zaokrouhlení** v definici řádku, jak je ukazuje následující obrázek.

    ![Úpravy zaokrouhlení úprav měny](./media/Currency-translation-adjustment-rounding-adjustments.png "Úpravy zaokrouhlení úprav měny")

    Když zadáte řádek, který má zobrazovat vyrovnání rozdílů po zaokrouhlení (CTA), řádek celkového majetku, řádek celkových závazků a akciového jmění a prahovou hodnotu, která vám vyhovuje, finanční výkaznictví vypočítá daný rozdíl a umístí jej na požadovaný řádek. Vytvoří se řádek s názvem **Vyrovnání rozdílů po zaokrouhlení** a zobrazí po rozbalení, jak je ukázáno na následujícím obrázku.

    ![Procházení úprav zaokrouhlení](./media/rounding-adjustment-drill-down.png "Procházení úprav zaokrouhlení")

- Všechny účty umístí do rozsahu, od majetku po výdaje. Jak je uvedeno v následujícím obrázku, rozdíl bude stejná částka jako vyrovnání rozdílů po zaokrouhlení (CTA). Z toho vyplývá, že jej můžete použít jako kontrolní součet a máte jistotu, že na stránce pro vyrovnání rozdílů po zaokrouhlení nebudou chybět žádné zůstatky na účtu.

    ![Kontrola formuláře – úprava zaokrouhlení](./media/rounding-adjustment-form-check.png "Kontrola formuláře – úprava zaokrouhlení")

### <a name="balance-calculation-approach"></a>Přístup k výpočtu zůstatku
Chcete-li získat správně převedené částky při použití měn, finanční výkaznictví používá následující metody výpočtu zůstatků:

- **Vážený průměr a průměr** – každé období je vypočteno ve svém váženém průměru a sečteno pro sloupce, například čtvrtletně a od začátku roku.
- **Historické** – kterýkoli účet, který používá metodu historického převodu, přejde zpět k datu transakce. Pokud je datum pořízení přidružené k transakci, toto datum se použije k získání směnného kurzu. Každé období je poté sečteno a uloženo za účelem zlepšení času výpočtu.
- **Aktuální** – vypočtené sloupce a sloupce součtů, například sloupce s hodnotami čtvrtletně a od začátku roku, se vypočtou podle místní sazby, která je určena ve sloupci nebo v sestavě. Například sloupec **Čtvrtletí 1** použije sazbu 31. března, pokud je použitý kalendářní rok.

## <a name="additional-resources"></a>Další zdroje

Další informace o konsolidaci a převodech měn naleznete v nadřazeném tématu [Přehled finanční konsolidace a převodu měny](./financial-consolidations-currency-translation.md).

Další informace o zadání podrobností online konsolidace získáte v části [Online finanční konsolidace](./consolidate-online.md).
