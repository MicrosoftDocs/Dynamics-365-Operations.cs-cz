---
title: "Určit optimální kombinací překrývajících se slevy"
description: "Při překrytí slev, je třeba určit kombinaci překrývající se slev, které budou tvořit nejnižší celkové částky transakce nebo nejvyšší Celková sleva. Pokud částka slevy se liší podle ceny produktů, které jsou zakoupeny, například společné &quot;koupit 1, získat 1 X procent&quot; maloobchodní slevy (BOGO), tento proces bude problematická combinatorial optimalizace."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 89643
ms.assetid: 09843c9a-3e19-4e4a-a8ce-80650f2095f9
ms.search.region: global
ms.search.industry: Retail
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 31e5104045ed5b8fbfa3677a7f5702d551de4231
ms.lasthandoff: 03/31/2017


---

# <a name="determine-the-optimal-combination-of-overlapping-discounts"></a>Určit optimální kombinací překrývajících se slevy

[!include[banner](includes/banner.md)]


Při překrytí slev, je třeba určit kombinaci překrývající se slev, které budou tvořit nejnižší celkové částky transakce nebo nejvyšší Celková sleva. Pokud částka slevy se liší podle ceny produktů, které jsou zakoupeny, například společné "koupit 1, získat 1 X procent" maloobchodní slevy (BOGO), tento proces bude problematická combinatorial optimalizace.

Tento článek se týká aplikace Microsoft Dynamics AX 2012 R3 s KB 3105973 (vydáno 2. listopadu 2015) nebo vyšší a v únoru 2016 vydání aplikace Microsoft Dynamics AX. K určení kombinace překrývající se slevy platí včas a nadále poskytuje bohatou nabídku funkcí užívána, která je k dispozici v aplikaci Microsoft Dynamics AX for Retail, jsme zavedli metodu pro použití překrývajících se slevy. Nazýváme tuto novou metodu **mezní hodnota pořadí**. Mezní hodnota pořadí se používá při doba potřebná k vyhodnocení možných kombinací slev překrývající se překročí prahovou hodnotu, kterou je možné konfigurovat na **parametry programu Retail** stránky v aplikaci Dynamics AX. Mezní hodnoty metody hodnocení se vypočítá hodnotu každý překrývající se slevou pomocí hodnoty je sleva na sdílené produkty. Překrytí slev platí od nejvyšší relativní hodnoty nejnižší relativní hodnotu. Další informace o nové metody naleznete v části "Mezní hodnotou" dále v tomto článku. Mezní hodnota pořadí nebude použito, pokud částky slev produktu nejsou ovlivněny další produkt v transakci. Například tato metoda nepoužívá pro dvě jednoduché slevy nebo jednoduché slevy a množstevní slevy pro jeden produkt.

## <a name="discount-examples"></a>Příklady slev
V aplikaci Dynamics AX můžete vytvořit neomezený počet maloobchodních slev na společnou sadu produktů. Nicméně vzhledem k tomu, že neexistuje žádné omezení, problémy s výkonem může dojít při výpočtu slev, které je třeba použít na různé produkty. Následující příklady ilustrují tento problém podrobněji. V příkladu 1 můžeme začít s dva produkty a dvě překrývající se slevy. Potom v příkladu 2, můžeme zobrazit řídíte problém budou přidávány další produkty.

### <a name="example-1-two-products-and-two-discounts"></a>Příklad 1: Dva produkty a dvě slevy

V tomto příkladu dva výrobky jsou nutné k získání každé slevy a slevy nelze kombinovat. Slevy v tomto příkladu se **nejlepší cenu** slevy. Oba produkty způsobilé pro obě slevy. Zde jsou dvě slevy. [![Překrývající se slevy combo 01](./media/overlapping-discount-combo-01.jpg)](./media/overlapping-discount-combo-01.jpg) pro dva výrobky, tím lepší tyto dvě slevy závisí na ceny těchto dvou výrobků. Pokud je cena obou produktů stejným nebo téměř stejným, sleva 1 je lepší. Pokud je cena výrobku významně nižší než ceny ostatních produktů, je lepší slevy 2. Zde je matematická pravidla za vaše rozhodnutí vyzkoušet tyto dvě slevy proti sobě: [![combo slev Overlapping 02](./media/overlapping-discount-combo-02.jpg)](./media/overlapping-discount-combo-02.jpg) při ceně produktu 1 se rovná dvě třetiny ceny produktu 2, dvě slevy jsou stejné. V tomto příkladu procento účinnosti slevy slevy 1 se liší od několika procent (jsou-li ceny těchto dvou výrobků daleko od sebe) na maximálně 25procent $2 (je-li dva produkty mají stejnou cenu). Procento účinnosti slevy slevy 2 je pevná. Jedná se vždy o 20procent $2. Protože procento účinnosti slevy slevy 1 má rozsah, který může být větší než nebo menší než 2 slevy, nejlepší slevy závisí na ceny těchto dvou výrobků, které musí být odečtena. V tomto příkladu je výpočet dokončen rychleji, protože jsou použity pouze dvě slevy na pouze dva výrobky. Existují pouze dvě možné kombinace: jednu aplikaci slevy 1 nebo jeden uplatnění slevy 2. Neexistují žádné permutací pro výpočet. Hodnota každého sleva se vypočítá pomocí oba produkty a nejlepší slevy slouží.

### <a name="example-2-four-products-and-two-discounts"></a>Příklad 2: Čtyři produkty a dvě slevy

Dále použijeme čtyři produkty a stejné dvě slevy. Všechny čtyři produkty způsobilé pro obě slevy. Existuje dvanáct možných kombinací. Nakonec budou použity dvě slevy do transakce v jednom ze tří kombinací: dvě aplikace slevy 1, dvě žádosti slevy 2 nebo jeden uplatnění slevy 1 a jedno uplatnění slevy 2. Pro ilustraci možných kombinací, se podíváme na dvě sady čtyř produktů, které mají různé ceny:

-   Všechny čtyři produkty mají stejnou cenu $15.00. V tomto případě je optimální kombinaci slev dvě aplikace slevy 1. Dva produkty budou plnou cenu a dva 50procent $2 bude vypnuto. Celková částka se slevou pro transakci je vypnuto undiscounted celkem $60 $45 (15 + 15 + 7.50 + 7.50), což je $15 (25procent $2). Sleva 2 je pouze $12 (20 %).
-   Dva výrobky jsou $20 každý $15 je jeden produkt a jeden výrobek je $5. V tomto případě je optimální kombinaci slev jednu aplikaci slevy 2 a jeden uplatnění slevy 1. Následující tabulka ukazuje slevy.

Čtení tabulky, použijte jeden produkt z řádku a jeden produkt ze sloupce. Například v tabulce Sleva 1, pokud zkombinujete dva výrobky $20 získáte $10. V tabulce slevy 2 při kombinaci produktů $15 a $5 produktu získáte $4. [![Překrývající se seznamem 03 slevy](./media/overlapping-discount-combo-03.jpg)](./media/overlapping-discount-combo-03.jpg) nejprve můžeme najít největší slevy, která je dostupná z libovolné dva produkty pomocí buď slevu. Dvě tabulky zobrazí částku slevy pro všechny kombinace těchto dvou výrobků. Vystínovanými částmi tabulky představují buď případy, kde je spárováno produktu se sama, které nelze provádíme nebo reverzní párování dva výrobky, které vytváří stejný částka slevy a může být ignorována. Pohledem na tabulkách uvidíte dvě položky $20 této slevy 1 je největší slevy, která je k dispozici buď slevu na všechny čtyři výrobky. (Tato sleva je zvýrazněno zeleně v první tabulce). Který opustí pouze produkt $15 a $5 produktu. Pohledem na dvě tabulky znovu, uvidíte, že u těchto dvou produktů poskytuje slevy 1 $2.50 sleva, že slevy 2 nabízí $4 slevy. Proto jsme vyberte slevu 2. Celková sleva je $14. Usnadňují vizualizaci této diskusi, zde jsou dva další tabulky zobrazit procento slevy účinné pro všechny možné kombinace dvou produktů obou sleva 1 a 2 slevy. Pouze polovina seznam kombinací je zahrnut, protože pro tyto dvě slevy není důležité pořadí, ve kterém jsou dva výrobky propuštěny do slevy. Nejvyšší účinnosti sleva (25procent $2) se zvýrazní zeleně a nejnižší účinné slevy (10procent $2) se zobrazí červeně. [![Překrývající se slevy se seznamem 04](./media/overlapping-discount-combo-04.jpg)](./media/overlapping-discount-combo-04.jpg)**Poznámka:** ceny se liší a soutěžit dva nebo více slev, je jediný způsob jak zaručit optimální kombinaci slev k vyhodnocení obou slev a jejich porovnání.

## <a name="total-possible-combinations"></a>Celkový počet možných kombinací.
Tato část pokračuje v příkladu z předchozího oddílu. Můžeme přidat další výrobky a jiné slevy a viz, kolik kombinací musí být vypočtena a porovnání. Následující tabulka zobrazuje počet možných kombinací slev jako zvýšení množství produktu. Tabulka uvádí, co se stane, dva překrývající se slevy, jako v předchozím příkladu jsou i při existují tři překrývající se slevy. Brzy překročí počet možných kombinací slev, které musí být vyhodnocena co rychlý počítač můžete vypočítat a porovnávat dostatečně rychle jako přijatelné pro maloobchodní transakce. [![Překrývající se seznamem 05 slevy](./media/overlapping-discount-combo-05.jpg)](./media/overlapping-discount-combo-05.jpg) i při větším množství nebo více překrývajících se uplatnění slev, celkový počet možných kombinací slev rychle přejde do milionů a čas, který je nutný pro zhodnotí a vybere nejlepší možné kombinace rychle se pozná. V modulu Maloobchodní ceny snížit celkový počet kombinací, které musí být vyhodnoceny byly provedeny některé optimalizace. Však protože čísel překrývající se slevy a množství v transakci nejsou omezeny, velký počet kombinací budou mít vždy vyhodnocen pokaždé, když jsou překrývající se slevy. Tento problém je problém, který řeší mezní hodnota metoda hodnocení.

## <a name="marginal-value-method"></a>Metoda mezní hodnoty
Chcete-li vyřešit problém exponenciálně rostoucí počet kombinací, které musí být vyhodnocena, optimalizace existuje, která vypočítá hodnotu každý sdílený produkt každý slevu na sadu produktů, které lze použít dvě nebo více slev. Odkazujeme na tuto hodnotu jako **mezní hodnota** slevy pro sdílené produkty. Mezní hodnota je průměr za produkt zvýšit celkovou částku slevy při sdílené produkty jsou součástí každého slevy. Mezní hodnota se vypočte celkovou částku slevy (DTotal) odečtením částky slevy bez sdílených produktů s využitím (DMinus\\ Shared) a tento rozdíl se vydělí počet sdílených produktů (ProductsShared). [![Překrývající se slevy se seznamem 06](./media/overlapping-discount-combo-06.jpg)](./media/overlapping-discount-combo-06.jpg) po každé slevy na sdílené sadě produktů mezní hodnota se vypočítá, slevy platí pro sdílené výrobků v pořadí, vyčerpávajícím způsobem, z nejvyšší mezní hodnota nejnižší mezní hodnotu. Pro tuto metodu nejsou porovnány všechny zbývající možnosti slev vždy po jedné instanci slevu. Místo toho překrývající se slevy jsou porovnány jednou a poté použity v pořadí. Jsou prováděny žádné další porovnání. Můžete nakonfigurovat prahové hodnoty přepnout na metodu mezní hodnoty **sleva** karta **parametry programu Retail** stránky. Přijatelné doby při výpočtu celkové slevy se liší v rámci odvětví maloobchodu. Tentokrát však obecně spadá do rozsahu desítky milisekund na jednu sekundu.




