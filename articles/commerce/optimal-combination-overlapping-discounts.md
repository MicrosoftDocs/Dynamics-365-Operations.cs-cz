---
title: Určení optimální kombinace překrývajících se slev
description: Při překrytí slev je třeba určit kombinaci překrývající se slev, které budou tvořit nejnižší celkové částky transakce nebo nejvyšší celkovou slevu. Pokud se částka slevy liší podle ceny produktů, které jsou zakoupeny, například u běžné maloobchodní slevy typu Při nákupu 1 sleva X procent (BOGO), tento proces bude problémem pro kombinatorní optimalizaci.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 89643
ms.assetid: 09843c9a-3e19-4e4a-a8ce-80650f2095f9
ms.search.industry: Retail
ms.search.form: RetailParameters, RetailPeriodicDiscount,
ms.openlocfilehash: 64137b877ff1250770ec0794167ba494970bc10e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269101"
---
# <a name="determine-the-optimal-combination-of-overlapping-discounts"></a>Určení optimální kombinace překrývajících se slev

[!include [banner](includes/banner.md)]

Při překrytí slev je třeba určit kombinaci překrývající se slev, které budou tvořit nejnižší celkové částky transakce nebo nejvyšší celkovou slevu. Pokud se částka slevy liší podle ceny produktů, které jsou zakoupeny, například u běžné maloobchodní slevy typu "Při nákupu 1 sleva X procent" (BOGO), tento proces bude problémem pro kombinatorní optimalizaci.

Tento článek platí pro Microsoft Dynamics AX 2012 R3 s KB 3105973 (vydáno 2 listopadu 2015) nebo novější, a na Dynamics 365 Commerce. Abyste mohli určit překrývající se kombinované slevy pro včasné použití, zavedli jme metodu použití překrývajících se slev. Nazýváme tuto novou metodu **mezní hodnota pořadí**. Mezní hodnota pořadí se používá, když doba potřebná k vyhodnocení možných kombinací překrývajících se slev překročí prahovou hodnotu, kterou je možné konfigurovat na stránce **Parametry velkoobchodu**. V metodě mezní hodnoty pořadí se vypočítá hodnota pro každou překrývající se slevu pomocí hodnoty slevy ve sdílených produktech. Překrývající se slevy jsou pak použity od nejvyšší relativní hodnoty po nejnižší relativní hodnotu. Další informace o nové metodě naleznete v části "Mezní hodnota" dále v tomto článku. Mezní hodnota pořadí nebude použita, pokud částky slev produktu nejsou ovlivněny jiným produktem v transakci. Například se tato metoda nepoužívá pro dvě jednoduché slevy nebo jednoduchou slevu a množstevní slevu pro jeden produkt.

## <a name="discount-examples"></a>Příklady slev

Můžete vytvořit neomezený počet slev na společnou sadu produktů. Nicméně vzhledem k tomu, že neexistuje žádné omezení, problémy s výkonem mohou nastat při výpočtu slev, které je třeba použít na různé produkty. Následující příklady ilustrují tento problém podrobněji. V příkladu 1 můžeme začít se dvěma produkty a dvěma překrývajícími se slevami. Potom v příkladu 2 můžeme zobrazit, jak se problém vyvíjí, když budou přidávány další produkty.

### <a name="example-1-two-products-and-two-discounts"></a>Příklad 1: Dva produkty a dvě slevy

V tomto příkladu jsou požadovány dva produkty ke kvalifikaci k získání každé slevy a slevy nelze kombinovat. Slevy v tomto příkladu jsou slevy za **nejlepší cenu**. Oba produkty jsou způsobilé pro obě slevy. Zde jsou dvě slevy.

![Příklad dvou nejlepších cenových slev.](./media/overlapping-discount-combo-01.jpg)

Pro libovolné dva výrobky lepší z obou slev závisí na cenách těchto dvou výrobků. Pokud je cena obou produktů stejná nebo téměř stejná, sleva 1 je lepší. Pokud je cena produktu významně nižší než ceny ostatních produktů, je lepší sleva 2. V tomto poli je matematické pravidlo pro vyhodnocení těchto dvou slev proti sobě.

![Pravidlo pro vyhodnocení slev.](./media/overlapping-discount-combo-02.jpg)

> [!NOTE]
> Když se cena produktu 1 rovná dvěma třetinám ceny produktu 2, slevy se rovnají. V tomto příkladu se procento účinnosti slevy 1 liší o několik procent (jsou-li ceny těchto dvou výrobků daleko od sebe) na maximálně 25procent (pokud dva produkty mají stejnou cenu). Procento účinnosti slevy 2 je pevné. Jedná se vždy o 20 procent. Protože procento účinnosti slevy 1 má rozsah, který může být větší než nebo menší než sleva 2, nejlepší sleva závisí na ceně těchto dvou výrobků, které musí být odečtena. V tomto příkladu je výpočet dokončen rychleji, protože jsou použity pouze dvě slevy na pouze dva výrobky. Existují pouze dvě možné kombinace: jedna aplikace slevy 1 nebo jedna aplikace slevy 2. Není k dispozici pořadí pro výpočet. Hodnota každé slevy se vypočítá pomocí obou produktů a použije se nejlepší sleva.

### <a name="example-2-four-products-and-two-discounts"></a>Příklad 2: Čtyři produkty a dvě slevy

Dále použijeme čtyři produkty a stejné dvě slevy. Všechny čtyři produkty jsou způsobilé pro obě slevy. Existuje dvanáct možných kombinací. Nakonec budou použity dvě slevy pro transakci v jedné ze tří kombinací: dvě uplatnění slevy 1, dvě uplatnění slevy 2 nebo jeden uplatnění slevy 1 a jedno uplatnění slevy 2. Pro ilustraci možných kombinací se podíváme na dvě sady čtyř produktů, které mají různé ceny:

- Všechny čtyři produkty mají stejnou cenu 15,00 USD. V tomto případě je optimální kombinace slev dvě uplatnění slevy 1. Dva produkty budou mít plnou cenu a dva 50procentní slevu. Celková částka se slevou pro transakci je $45 (15 + 15 + 7.50 + 7,50), což je sleva $15 (25 procent) z nezlevněného celku$60. Sleva 2 je pouze $12 (20 %).
- Dva výrobky každý stojí $20, jeden $15 a jeden $5. V tomto případě je optimální kombinace slev jedno uplatnění slevy 2 a jedno uplatnění slevy 1. Následující tabulka ukazuje slevy.

Pokud chcete tabulky číst, použijte jeden produkt z řádku a jeden produkt ze sloupce. Například v tabulce pro slevu 1, pokud zkombinujete dva výrobky za $20, získáte $10. V tabulce pro slevu 2, pokud zkombinujete dva výrobky za $15 a jeden za $5, získáte slevu $4.

![Příklad, který používá čtyři produkty pro stejné dvě slevy.](./media/overlapping-discount-combo-03.jpg)

Nejprve najdeme největší slevu dostupnou z libovolných dvou produktů pomocí některé ze slev. Dvě tabulky zobrazují částku slevy pro všechny kombinace těchto dvou výrobků. Vystínované části tabulky představují buď případy, kde je produkt spárovaný se sebou sama, což nemůžeme udělat, nebo reverzní párování dvou výrobků, které vytváří stejnou částku slevy, která může být ignorována. Pohledem na tabulky uvidíte, že sleva 1 pro dvě položky po 20 USD je největší sleva, která je k dispozici pro jakoukoli slevu na všechny čtyři výrobky. (Tato sleva je zvýrazněna zeleně v první tabulce). To znamená pouze produkt za $15 a za $5. Dalším pohledem na dvě tabulky uvidíte, že u těchto dvou produktů znamená sleva 1 $2,50, zatímco sleva 2 $4. Proto vybereme slevu 2. Celková sleva činí $14. Abychom tuto diskusi snadno vizualizovali, této diskusi, zde jsou dva další tabulky zobrazující efektivní procento slevy pro všechny možné kombinace dvou produktů se slevou 1 i 2. Je zahrnuta pouze polovina seznamu kombinací, protože pro tyto dvě slevy není důležité pořadí, ve kterém jsou dva výrobky zlevněny. Nejvyšší efektivní sleva (25 procent) je zvýrazněna zeleně a nejnižší efektivní sleva (10 procent) červeně.

![Efektivní procento slevy pro všechny kombinace dvou produktů pro obě slevy.](./media/overlapping-discount-combo-04.jpg)

> [!NOTE]
> Když se ceny liší a dvě nebo více slev soupeří, je jediný způsob, jak zaručit optimální kombinaci slev k vyhodnocení obou slev, jejich porovnání.

## <a name="total-possible-combinations"></a>Celkem možných kombinací

Tato část pokračuje v příkladu z předchozího oddílu. Můžeme přidat další výrobky a jinou slevu a podívat se, kolik kombinací musí být vypočteno a porovnáno. Následující tabulka zobrazuje počet možných kombinací slev s tím, jak se zvyšuje množství produktu. Tabulka uvádí, co se stane, když existují dvě překrývající se slevy jako v předchozím příkladu, a když existují tři překrývající se slevy. Počet možných kombinací slev, které musí být vyhodnoceny, brzy překročí to, co nedokáže ani nejrychlejší počítač vypočítat porovnávat dostatečně rychle jako přijatelné pro maloobchodní transakce.

![Počet možných kombinací slev s tím, jak se zvyšuje množství produktu.](./media/overlapping-discount-combo-05.jpg)

Když jsou použita ještě větší množství nebo více překrývajících se slev, celkový počet možných kombinací slev rychle přejde do milionů a čas, který je nutný pro zhodnocení a výběru nejlepší možné kombinace se rychle. V modulu ceny byly provedeny určité optimalizace na snížení celkového počtu kombinací, které musí být vyhodnoceny. Protože ale počet překrývajících se slev a množství v transakci nejsou omezeny, bude vždy potřeba vyhodnotit velký počet kombinací tam, kde existují překrývající se slevy. Tento problém je problém, který řeší metoda mezního hodnocení.

## <a name="marginal-value-method"></a>Metoda mezní hodnoty

Chcete-li vyřešit problém exponenciálně rostoucího počtu kombinací, které musí být vyhodnoceny, existuje optimalizace, která vypočítá hodnotu pro každý sdílený produkt každé slevy v sadě produktů, u nichž lze použít dvě nebo více slev. Odkazujeme na tuto hodnotu jako na **Mezní hodnotu** slevy pro sdílené produkty. Mezní hodnota je průměr za zvýšení produktu v celkové částce slevy při zahrnutí sdílených produktů do každé slevy. Mezní hodnota se vypočte převzetím celkové částky slevy (DTotal) odečtením částky slevy bez sdílených produktů s využitím (DMinus\\ Shared) a tento rozdíl se vydělí počet sdílených produktů (ProductsShared).

![Vzorec pro výpočet mezní hodnoty.](./media/overlapping-discount-combo-06.jpg)

Po odečtení mezní hodnoty každé slevy ve sdílené sadě produktů se vypočte mezní hodnota, uplatní slevy na sdílené výrobky v pořadí, vyčerpávajícím způsobem, od nejvyšší mezní hodnoty k nejnižší mezní hodnotě. Pro tuto metodu nejsou porovnány všechny zbývající možnosti slev pokaždé, když je uplatněna jedna instance slevy. Místo toho jsou překrývající se slevy porovnány jednou a poté použity v pořadí. Nejsou prováděny žádné další porovnání. Můžete nakonfigurovat prahové hodnoty pro přepnutí na metodu mezní hodnoty na kartě **Sleva** stránky **Parametry velkoobchodu**. Přijatelná doba při výpočtu celkové slevy se v rámci odvětví maloobchodu liší. Tentokrát však obecně spadá do rozsahu desítky milisekund na jednu sekundu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
