---
title: Rozšířené možnosti formátování ve finančním výkaznictví
description: Toto téma popisuje pokročilé funkce formátování, včetně filtrů, omezení, netištěných řádků a podmíněných příkazů ve výpočtech.
author: panolte
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 106571
ms.assetid: 895b5127-01d6-4495-b127-343387b743aa
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e15869fdd598aeec7ef616f6d54593c7551cb906ab53763a64f4202473bcd926
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760119"
---
# <a name="advanced-formatting-options-in-financial-reporting"></a>Rozšířené možnosti formátování ve finančním výkaznictví

[!include [banner](../includes/banner.md)]

Vytvoříte-li zprávu ve finančním vykazování, budou k dispozici další funkce formátování, včetně filtrů pro dimenze, omezení pro sloupce a jednotky vykazování, řádky neurčené pro tisk a výrazy IF/THEN/ELSE ve výpočtech.

Následující tabulka vysvětluje rozšířené funkce formátování, které jsou k dispozici při návrhu sestav.

| Funkce                   | Popis |
|----------------------------|-------------|
| Filtr dimenze           | Pro přístup k určitým sadám dat můžete použít dimenze v definici řádku a definici sloupce. Mnoho sestav používá pouze přirozené segmenty ve formátu řádku. Řádky lze však upravit, aby zahrnovaly hodnoty dimenzí. Filtry dimenzí v definici sloupce jsou používané pro přístup ke konkrétním hodnotám dimenzí. |
| Omezení jednotky výkaznictví | Řádek sestavy lze nastavit tak, aby zobrazil pouze informace, které jsou propojeny s určitou jednotkou výkaznictví. |
| Netisknuté (NP) řádky     | Netisknuté řádky jsou užitečné v mnoha sestavách. Pokud je vyžadováno několik výpočtů za účelem získání hodnoty, lze tyto výpočty skrýt v tištěné sestavě. Netisknuté řádky jsou také užitečné při řešení problémů při návrhu sestav a pro přesné umísťování buněk. |
| Omezení sloupce         | Omezení sloupce v definici řádku je užitečné ke skrývání hodnot, které jsou relevantní pouze pro některé řádky sestavy. Při provádění výpočtu procent na řádku zabrání omezení sloupce sloupcům součtů nebo jiným sloupcům ve vytištění, pokud daná čísla neplatí. |
| Zalomení sloupce               | Můžete přidat zalomení sloupce do definice řádku a zobrazit tak informace sestavy vedle sebe. Můžete přidat více zalomení sloupce do jedné definice řádku a záhlaví sloupce bude opakováno nad každým sloupcem po zalomení sloupce. Komentáře pro sestavu se zobrazují mezi zalomeními sloupců. |
| Výraz IF/THEN/ELSE     | Výpočty v definici řádku nebo definici sloupce lze upravit. |
| Pro hodnoty dimenze používejte jednoduché uvozovky (' ') a znak ampersand (&). | Můžete použít hodnoty dimenze, včetně znaku ampersandu pro návrh sestavy. |

## <a name="advanced-cell-placement"></a>Přesné umísťování buněk

Přesné umísťování buněk (jinak *vynucení*) zahrnuje umístění konkrétních hodnot do konkrétních buněk. Například vynucení často slouží k přesunutí správného zůstatku ve výkazu cashflow. Vynucení můžete použít pro následující účely:

- Přesunutí hodnot z aplikace Microsoft Excel do konkrétních buněk
- pevné zakódování konkrétních hodnot do sestavy;
- změna znamének zkopírováním hodnoty z předchozí buňky a vynásobení hodnoty -1.

> [!NOTE]
> V mnoha případech je nutné konfigurovat definici sestavy tak, aby se prováděly výpočty sloupců před výpočty řádků. Abyste dokončili tuto konfiguraci, postupujte takto.
>
> 1. V Návrháři sestav otevřete definici sestavy.
> 2. Na kartě **Nastavení** v části **Priorita výpočtu** vyberte možnost **Nejprve provést výpočet sloupce a pak řádku**.

## <a name="designing-the-report"></a>Návrh sestavy

Při návrhu sestavy musíte nejprve vytvořit všechny řádky s podrobnostmi, abyste se ujistili, že hodnoty jsou získávány podle očekávání. Poté přidejte přepsání formátu **NP** (Netisknout) k potlačení podrobností, které zahrnují výsledné hodnoty.

> [!IMPORTANT]
> Pokud v definici řádků použijete kód formátu **CAL**, nelze přejít k podrobnostem transakce.

K vynucení používají vzorce následující formát: &lt;cílový sloupec&gt;=&lt;původní sloupec&gt;.&lt;kód řádku&gt; Oddělte jakékoli další umístění pro řádek čárkou a mezerou. Příklad: D=C.190,E=C.100

## <a name="examples-of-advanced-formatting-options"></a>Příklady rozšířených možností formátování

V následujících příkladech je ukázáno formátování definice řádku a definice sloupce pro vynucení základní sestavy cashflow (příklad 1) a statistické sestavy (příklad 2).

### <a name="example-1-basic-forcing"></a>Příklad 1: Základní vynucení

Následující tabulka znázorňuje příklad definice řádku používající základní vynucení.

| Kód řádku |           popis            | Kód formátu | Související vzorce/řádky/jednotky |        Modifikátor řádku        | Odkaz na finanční dimenze |
|----------|----------------------------------|-------------|-----------------------------|----------------------------|------------------------------|
| 100      | Hotovost na začátku období (NP) |             |                             | Modifikátor účtu = \[/BB\] | +Segment2 = \[1100\]         |
| 1.3.0      | Hotovost na začátku období      | CAL         | C=C.100,F=D.100             |                            |                              |
| 160      |                                  |             |                             |                            |                              |
| 190      |                                  |             |                             |                            |                              |

> [!NOTE]
> Prázdné sloupce byly odebrány z předchozí tabulky pro účely prezentace: nezobrazují se sloupce Přepsání formátu, Normální zůstatek, Řízení tisku a Omezení sloupce.

Následující tabulka znázorňuje příklad definice sloupce používající základní vynucení v řádku.

|           Formát             | A   | mld.    | K        | D      | E      | F    |
|------------------------------|-----|------|----------|--------|--------|------|
| Záhlaví 1                     |     |      |          |        |        |      |
| Záhlaví 2                     | A   | mld.    | K        | D      | E      | F    |
| Záhlaví 3                     |     |      |          |        |        |      |
| Typ sloupce                  | ROW | POPIS | FD       | FD     | FD     | VÝPOČET |
| Kód knihy / Kategorie atributů |     |      | SKUTEČNÝ   | SKUTEČNÝ | SKUTEČNÝ |      |
| Fiskální rok                  |     |      | ZÁKLAD     | ZÁKLAD   | ZÁKLAD   |      |
| Období                       |     |      | ZÁKLAD     | ZÁKLAD   | ZÁKLAD   |      |
| Pokrytá období              |     |      | PERIODICKÝ | OD POČÁTKU ROKU/BB | Od začátku roku    |      |
| Vzorec                      |     |      |          |        |        | E-D  |
| Šířka sloupce                 | 5   | 30   | 14       | 14     | 14     | 14   |

### <a name="example-2-statistical-reports"></a>Příklad 2: Statistické sestavy

Následující tabulka znázorňuje příklad definice řádku používající vynucení pro statistickou sestavu.

| Kód řádku | Popis               | Kód formátu | Související vzorce/řádky/jednotky     | Přepsání formátu      | Normální rozvaha | Odkaz na finanční dimenze               |
|----------|---------------------------|-------------|---------------------------------|----------------------|----------------|--------------------------------------------|
| 50       | Statistické informace   | REM         |                                 |                      |                |                                            |
| 100      | Počet zaměstnanců – USA            | CAL         | 4                               | \#\#\#0.;($\#\#\#0.) |                |                                            |
| 115      | Počet zaměstnanců - mezinárodní | CAL         | 11                              | \#\#\#0.;($\#\#\#0.) |                |                                            |
| 1.3.0      |                           |             |                                 |                      |                |                                            |
| 190      | Prodej USA                  |             |                                 |                      | K              | +Segment2 = \[41\*\], Segment3 = \[00\]    |
| 220      | Mezinárodní prodej       |             |                                 |                      | K              | +Segment2 = \[41\*\], Segment3 = \[01:99\] |
| 250      |                           |             |                                 |                      |                |                                            |
| 280      |                           |             |                                 |                      |                |                                            |
| 310      | Prodej USA                  | CAL         | D=C.190,E=C.100,F=(C.100/C.190) |                      |                |                                            |
| 340      | Mezinárodní prodeje       | CAL         | D=C.220,E=C115,F=(C.220/C.115)  |                      |                |                                            |

> [!NOTE]
> Prázdné sloupce byly odebrány z předchozí tabulky pro účely prezentace: nezobrazují se sloupce Řízení tisku, Omezení sloupce a Modifikátor řádku.

Následující tabulka znázorňuje příklad definice sloupce používající vynucení pro statistickou sestavu.

|    Formát                    | A   | mld.    | K      | D            | E     | F            |
|------------------------------|-----|------|--------|--------------|-------|--------------|
| Záhlaví 1                     | A   | mld.    | K      | D            | E     | F            |
| Záhlaví 2                     | -   | -    | Od začátku roku    | Roční prodeje | Zaměstnanec | Kč na osobu |
| Záhlaví 3                     |     |      |        |              |       |              |
| Typ sloupce                  | ŘÁDEK | POPIS | FD     | VÝPOČET         | VÝPOČET  | VÝPOČET         |
| Kód knihy / Kategorie atributů |     |      | SKUTEČNÝ |              |       |              |
| Fiskální rok                  |     |      | ZÁKLAD   |              |       |              |
| Období                       |     |      | ZÁKLAD   |              |       |              |
| Pokrytá období              |     |      | Od začátku roku    |              |       |              |
| Receptura                      |     |      |        |              |       | E-D          |
| Šířka sloupce                 | 5   | 30   | 14     | 14           | 14    | 14           |

## <a name="restricting-a-row-to-a-specific-reporting-unit"></a>Omezení řádku na určitou jednotku výkaznictví

Když je řádek sestavy omezen na určitou jednotku výkaznictví, daný řádek zobrazí propojená data pouze pro určenou jednotku výkaznictví a ignoruje data pro jiné jednotky výkaznictví ve stromu výkaznictví. Můžete například vytvořit řádek, který obsahuje podrobnosti o celkových provozních výdajích pro konkrétní oddělení. Sestava může obsahovat zdvojená data, obsahuje-li sestava strom výkaznictví i definici řádku s více než daným přirozeným účtem. Například máte strom výkaznictví uvádějící šest oddělení ve vaší organizaci a máte také definici řádku uvádějící specifickou kombinaci účtu a oddělení v řádku. Při vygenerování sestavy bude konkrétní kombinace účtu a oddělení vytištěna na každé úrovni stromu výkaznictví i v případě, že se dané oddělení neshoduje s obsahem stromu. K této situaci dochází, protože řádek přepíše to, co je obvykle odfiltrováno definicí sestavy. Jedním způsobem, jak se vyhnout duplikaci dat, je omezením řádku na určitou jednotku výkaznictví.

> [!NOTE]
> Pokud řádek obsahuje dimenze a omezíte tento řádek na podřízenou jednotku výkaznictví, částka řádku je zahrnuta pro danou podřízenou jednotku a pro její nadřazené jednotky, nedojde však ke zdvojení.

### <a name="restrict-a-row-to-a-reporting-unit"></a>Omezení řádku na jednotku výkaznictví

1. V Návrháři sestav klikněte na tlačítko **Definice řádku** a potom vyberte definici řádku ke změně.
2. Dvakrát klikněte na příslušnou buňku **Související vzorce/řádky/jednotky**.
3. V poli **Organizační strom** v dialogovém okně **Výběr organizační jednotky** vyberte strom, který je přiřazen v definici sestavy.
4. Vyberte jednotku výkaznictví a klikněte na tlačítko **OK**. Omezení se zobrazí v buňce definice řádku.
5. Klikněte dvakrát na buňku ve sloupci **Odkaz na finanční dimenze** omezeného řádku a pak zadejte odkaz na systém finančních dat.

## <a name="selecting-print-control-in-a-row-definition"></a>Výběr řízení tisku v definici řádku

Můžete určit kódy řízení tisku pro jednotlivé sloupce použitím buňky **Řízení tisku**.

### <a name="add-print-control-codes-to-a-report-row"></a>Přidání kontrolních kódů tisku do řádku sestavy

1. V Návrháři sestav otevřete definici řádků, kterou chcete změnit.
2. Klikněte dvakrát na buňku **Řízení tisku**.
3. V dialogovém okně **Řízení tisku** vyberte kontrolní kód tisku nebo stiskněte a podržte klávesu Ctrl a vyberte více kódů. Lze také zadat kontrolní kódy tisku přímo do buňky **Řízení tisku**. Více kontrolních kódů tisku oddělte čárkou.
4. Vyberte jakékoli podmíněné možnosti tisku.
5. Klepněte na tlačítko **OK**.

### <a name="regular-print-control-codes"></a>Normální kontrolní kódy tisku

V následující tabulce jsou popsány běžné kontrolní kódy tisku pro definici řádku.

| Kontrolní kód tisku | Interpretace kontrolního kódu tisku         | Popis |
|--------------------|--------------------------------------------------|-------------|
| NP                 | Netisknutý řádek                                 | Zabrání částkám v řádku ve vytištění na sestavě a vyloučí částky z výpočtů. Chcete-li do výpočtu zahrnout netisknutý sloupec, odkazujte na sloupec přímo ve vzorci výpočtu. Například netisknutý řádek 240 je součástí následujícího výpočtu: **230+240+250**. Netisknutý řádek 240 však nebude součástí následujícího výpočtu: **230:250**. |
| CS                 | Symbol měny; v tomto řádku se použije formát měny | Zahrne symbol měny do všech částek kromě procent. Hodnoty v procentech nikdy nejsou opatřeny symbolem měny. |
| XD                 | Potlačení řádku v sestavě podrobností účtu            | Potlačí zobrazení účtů na sestavách podrobností účtů a sestavách podrobností transakcí. Tento kontrolní prvek tisku je užitečný, pokud řádek obsahuje více účtů, které by neměly být uvedeny v sestavě podrobností účtu nebo sestavě podrobností transakce. |
| X0                 | Potlačení řádku v případě samých nul                        | Vyloučí řádek ze sestavy, pokud jsou všechny buňky v řádku prázdné nebo obsahují nuly. Tento ovládací prvek tisku má význam pouze v případě, že není vybrána možnost potlačení nulového zůstatku v definici sestavy. |
| B0                 | Ponechání sloupců s nulou prázdnými                         | Ponechá sloupce prázdné v řádku, který obsahuje nulové částky. |
| XR                 | Potlačit shrnutí                                  | Potlačí shrnutí. Pokud sestava používá strom výkaznictví, částky v tomto řádku nebudou shrnuty do následných nadřazených uzlů. |
| SR                 | Potlačit zaokrouhlení                                | Zabrání zaokrouhlení částek v tomto řádku. |
| XT                 | Potlačení řádku v sestavě podrobností transakce        | Potlačí zobrazení transakcí v sestavách podrobností transakcí. Tento kontrolní prvek tisku je užitečný, pokud řádek obsahuje více účtů, které by neměly být uvedeny v sestavě podrobností transakce. |

### <a name="conditional-print-control-codes"></a>Podmíněné kontrolní kódy tisku

V následující tabulce jsou popsány podmíněné kontrolní kódy tisku pro definici řádku.

| Kontrolní kód tisku | Popis                                  |
|--------------------|----------------------------------------------|
| (žádný)             | Zruší výběr podmíněného tisku.       |
| OŘ                 | Vytiskne pouze zůstatky na straně Má dáti pro tento řádek.  |
| CR                 | Vytiskne pouze zůstatky na straně Dal pro tento řádek. |

## <a name="column-restriction-cell-in-a-row-definition"></a>Buňka Omezení sloupce v definici řádku

Buňka **Omezení sloupce** v definici řádku slouží více účelům. V závislosti na typu řádku můžete použít buňku **Omezení sloupce** k určení jedné z následujících funkcí:

- Buňka může omezit tisk částek řádků na konkrétní sloupec. Tato funkce je užitečná, pokud vytváříte tabulkovou rozvahu.
- Buňka může určit sloupec částek k seřazení.

## <a name="using-a-calculation-formula-in-a-row-definition"></a>Použití vzorce výpočtu v definici řádku

Výpočetní vzorec v definici řádku může zahrnovat operátory **+**, **-**, **\**_ a _*/**, a také příkazy **IF/THEN/ELSE**. Výpočet může navíc zahrnovat jednotlivé buňky a absolutní hodnoty (skutečná čísla, která jsou zahrnuta ve vzorci). Vzorec může obsahovat až 1 024 znaků. Výpočty nelze použít pro řádky obsahující buňky typu **Odkaz na finanční dimenze** (FD). Můžete však zahrnout výpočty v rámci po sobě jdoucích řádků, potlačit tisk těchto řádků a poté sečíst řádky výpočtů.

### <a name="operators-in-a-calculation-formula"></a>Operátory ve výpočetním vzorci

Výpočetní vzorec používá složitější operátory než vzorec součtu řádku. Lze však použít operátory **\**_ a _*/** spolu s dalšími operátory k násobení (\*) a dělení (/) částek. Pokud chcete použít ve vzorci pro výpočet rozsah nebo součet, je nutné použít zavináč (@) před jakýmkoli kódem řádku, pokud nepoužíváte sloupec v definici řádku. Například pro přičtení částky v řádku 100 k částce v řádku 330 lze použít vzorec součtu řádku **100+330** nebo výpočetní vzorec **@100+@330**.

> [!NOTE]
> Je třeba použít zavináč (@) před každým kódem řádku, který využíváte ve výpočetním vzorci. Jinak bude číslo přečteno jako absolutní hodnota. Například vzorec **@100+330** přidá k částce na řádku 100 částku ve výši 330 USD. Při odkazování na sloupec ve vzorci pro výpočet není znak (@) zapotřebí.

### <a name="create-a-calculation-formula"></a>Vytvoření výpočetního vzorce

1. V Návrháři sestav klikněte na tlačítko **Definice řádku** a potom otevřete definici řádku ke změně.
2. Dvakrát klikněte na buňku **Kód formátu** a vyberte kód **CAL**.
3. V buňce **Související vzorce/řádky/jednotky** zadejte výpočetní vzorec.

### <a name="example-of-a-calculation-formula-for-specific-rows"></a>Příklad vzorce výpočtu pro určité řádky

V tomto příkladu vzorec výpočtu **@100+@330** znamená, že částka v řádku 100 se přidá k částce řádku 330. Vzorec součtu řádku **340+370** přidá částku v řádku 340 k částce v řádku 370. (Částku v řádku 370 je částka z vzorce výpočtu).

| Kód řádku | Popis                 | Kód formátu | Související vzorce/řádky/jednotky | Řízení tisku | Modifikátor řádku | Odkaz na finanční dimenze |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Hotovost na začátku období |             |                            | NP            | BB           | +Účet=\[1100:1110\]       |
| 370      | Hotovost na začátku roku   | CAL         | @100+@330                  | NP            |              |                              |
| 400      | Hotovost na začátku období | TOT         | 340+370                    |               |              |                              |

Pokud má řádek v definici řádku kód formátu **CAL** a zadáte matematický výpočet do buňky **Související vzorce/řádky/jednotky**, musíte také zadat písmeno přidruženého sloupce a řádku v sestavě. Například zadejte **A.120** pro znázornění sloupce A, řádku 120. Případně můžete použít zavináč (@) k označení všech sloupců. Například zadejte **@120** pro znázornění všech sloupců v řádku 120. Matematický výpočet, který neobsahuje písmeno sloupce nebo znak zavináče (@), se považuje za reálné číslo.

> [!NOTE]
> Když použijete kód řádku popisku pro referenci řádku, musíte použít tečku (.) jako oddělovač mezi písmenem sloupce a popiskem (například **A.GROSS\_MARGIN/A.SALES**). Pokud používáte zavináč (@), oddělovač není požadován (například **\@GROSS\_MARGIN/@SALES**).

### <a name="example-of-a-calculation-formula-for-a-specific-column"></a>Příklad výpočetního vzorce pro konkrétní sloupec

V tomto příkladu značí výpočetní vzorec **E=C.340**, že výpočet v buňce ve sloupci C na řádku 340 je proveden pouze u sloupce E.

> [!NOTE]
> Při odkazování na sloupec ve vzorci pro výpočet není znak (@) zapotřebí.

| Kód řádku | Popis                 | Kód formátu | Související vzorce/řádky/jednotky | Řízení tisku | Modifikátor řádku | Odkaz na finanční dimenze |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Hotovost na začátku období |             |                            | NP            | BB           | +Účet=\[1100:1110\]       |
| 370      | Hotovost na začátku roku   | CAL         | E=C.340                    | NP            |              |                              |
| 400      | Hotovost na začátku období | TOT         | 340+370                    |               |              |                              |

### <a name="modifying-a-number-in-selected-columns"></a>Úprava čísla ve vybraných sloupcích

Pokud upravíte číslo nebo výpočet v jednom sloupci konkrétního řádku, ale nechcete ovlivnit jiné sloupce v sestavě, můžete určit sloupec **CAL** (Výpočet) ve sloupci **Kód formátu** v definici řádku.

- Chcete-li provést výpočet všech sloupců sestavy (**FD**), nezadávejte přiřazení sloupce.
- Chcete-li omezit vzorec na konkrétní sloupce, zadejte písmeno sloupce, znaménko rovnosti (**=**) a potom vzorec.
- Můžete určit více sloupců. Pokud použijete zavináč (@) při konkrétním umístění sloupce, zavináč (@) se vztahuje k řádku.
- V jednom řádku můžete zadat více výpočetních vzorců sloupců. Vzorce oddělte čárkami.

### <a name="calculation-examples"></a>Příklady výpočtů

| Výpočet            | Akce, která je vytvořena                                                                                                   |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| @130\*.75              | Pro každý sloupec je hodnota v řádku 130 vynásobena hodnotou 0,75. Výsledek je pak uložen do aktuálního řádku každého sloupce. |
| B=@130\*.75            | Stejný výpočet se provádí pouze pro sloupec B.                                                                      |
| A,B,C=(@100/@130)\*.75 | A=(A.100/A.130)\*,75 B=(B.100/B.130)\*.75 C=(C.100/C.130)\*,75                                                           |

### <a name="ifthenelse-statements-in-a-row-definition"></a>Výrazy IF/THEN/ELSE v definici řádku

Výrazy **IF/THEN/ELSE** lze přidat k jakémukoli platnému výpočtu a použít s formátem **CAL**. Výpočetní vzorce **IF/THEN/ELSE** zadávejte do buňky ve sloupci **Související vzorce/řádky/jednotky**. Výpočetní vzorce **IF/THEN/ELSE** používají následující formát: IF &lt;výrok pravda/nepravda&gt; THEN &lt;vzorec&gt; ELSE &lt;vzorec&gt; Část **ELSE &lt;vzorec&gt;** výrazu není povinná.

#### <a name="if-statements"></a>Výrazy IF

Výraz následující výraz **IF** může být libovolný příkaz, který lze vyhodnotit jako pravdu nebo nepravdu. Výraz následující výraz **IF** může zahrnovat jednoduché vyhodnocení nebo může představovat složitý příkaz, který může obsahovat více výrazů. Několik příkladů:

- **IF A.200&gt;0** (Jednoduché vyhodnocení)
- **IF A.200&gt;0 AND A.200&lt;10,000** (Složitý výraz)
- **IF A.200&gt;10000 OR ((A.340/B.1200)\*2 &lt;1200)** (Složitý výraz, který obsahuje více výrazů)

Termín **Období** ve výrazu **IF** reprezentuje počet období pro sestavu. Tento termín se obvykle používá pro výpočet průměru od začátku roku. Pokud například spustíte sestavu pro období 7 YTD, výraz **B.150/Období** bude znamenat, že hodnota v řádku 150 sloupce B bude vydělena 7.

#### <a name="then-and-else-formulas"></a>Vzorce THEN a ELSE

Vzorce **THEN** a **ELSE** mohou představovat jakýkoli platný výpočet od velmi jednoduchého přiřazení hodnoty po složité vzorce. Například výraz **IF A.200&gt;0 THEN A=B.200** znamená „Je-li hodnota v buňce ve sloupci A v řádku 200 větší než 0 (nula), vložit hodnotu z buňky ve sloupci B v řádku 200 do buňky ve sloupci A aktuálního řádku“. Předchozí výraz **IF/THEN** vloží hodnotu do jednoho sloupce aktuálního řádku. Lze však také použít zavináč (@) ve vyhodnocování pravdy a nepravdy nebo vzorec představující všechny sloupce. Zde je několik dalších příkladů, které jsou popsány v následujících oddílech:

- **IF A.200 &gt;0 THEN B.200**: Pokud je hodnota v buňce A.200 kladná, hodnota z buňky B.200 bude vložena do každého sloupce aktuálního řádku.
- **IF A.200 &gt;0 THEN @200**: Pokud je hodnota v buňce A.200 kladná, hodnota z každého sloupce v řádku 200 bude vložena do odpovídajícího sloupce aktuálního řádku.
- **IF @200 &gt;0 THEN @200**: Je-li hodnota v řádku 200 aktuálního sloupce kladná, hodnota z řádku 200 bude vložena do stejného sloupce v aktuálním řádku.

### <a name="restricting-a-calculation-to-a-reporting-unit-in-a-row-definition"></a>Omezení výpočtu na jednotku výkaznictví v definici řádku

Omezit výpočet na jednu jednotku výkaznictví ve stromu výkaznictví tak, aby výsledná částka nebyla shrnuta do jednotky vyšší úrovně, můžete použít kód **\@Unit** v buňce **Související vzorce/řádky/jednotky** v definici řádku. Kód **\@Unit** je uveden ve sloupci B stromu výkaznictví, část **Název jednotky**. Používáte-li kód **\@Unit**, hodnoty nejsou shrnuty, ale výpočet bude vyhodnocen na všech úrovních stromu výkaznictví.

> [!NOTE]
> Abyste mohli tuto funkci použít, je nutné přiřadit k definici řádku strom výkaznictví.

Řádek výpočtu může odkazovat na řádek výpočtu nebo řádek finančních dat. Výpočet se zaznamenává do buňky **Související vzorce/řádky/jednotky** v definici řádku a do omezení typu finančních dat. Výpočet musí použít podmíněný výpočet, který začíná konstrukcí **IF \@Unit**. Příklad: IF @Unit(SALES) THEN @100 ELSE 0 Tento výpočet obsahuje částku z řádku 100 každého sloupce sestavy, ale pouze pro jednotku SALES. Pokud je více jednotek nazváno SALES, částka se zobrazí v každé z těchto jednotek. Řádek 100 může být navíc řádek finančních dat a lze ho definovat jako netisknutý. Částka se v tomto případě nemůže zobrazit u všech jednotek ve stromu. Můžete také omezit částku na jeden sloupec sestavy, například sloupec H pomocí omezení sloupce k tisku hodnoty pouze v daném sloupci sestavy. Můžete zahrnout kombinace **OR** ve výrazu **IF**. Zde je příklad: **IF @Unit(SALES) OR @Unit(SALESWEST) THEN 5 ELSE @100**. Jednotku pro omezení podle typu výpočtu můžete zadat jedním z následujících způsobů:

- Zadáním názvu jednotky zahrňte jednotky, které odpovídají. Například **IF \@Unit(SALES)** umožňuje výpočet pro jakoukoli jednotku názvem SALES, i když ve stromu výkaznictví existuje několik jednotek SALES.
- Zadejte název společnosti a jednotky pro omezení výpočtu na specifické jednotky v určité společnosti. Zadejte například hodnotu **IF @Unit (ACME:SALES)** k omezení výpočtu na jednotky SALES ve společnosti ACME.
- Zadejte úplný kód hierarchie ze stromu výkaznictví pro omezení výpočtu na určitou jednotku. Zadejte například výraz **IF @Unit(SUMMARY^ACME^WEST COAST^SALES)**.

> [!NOTE]
> Plně hierarchický kód zjistíte tak, že kliknete pravým tlačítkem v definici organizačního stromu a pak vyberete příkaz **Kopírovat identifikátor organizační jednotky (kód H)**.

#### <a name="restrict-a-calculation-to-a-reporting-unit"></a>Omezení výpočtu na organizační jednotku

1. V Návrháři sestav klikněte na položku **Definice řádků** a otevřete definici řádků, kterou chcete změnit.
2. Dvakrát klikněte na buňku **Kód formátu** a vyberte kód **CAL**.
3. Klikněte na buňku **Související vzorce/řádky/jednotky** a poté zadejte podmíněné výpočty, které začínají konstrukcí **IF \@Unit**.

### <a name="ifthenelse-statements-in-a-column-definition"></a>Výrazy IF/THEN/ELSE v definici sloupce

Výraz **IF/THEN/ELSE** umožňuje závislost jakéhokoli výpočtu na výsledcích z jiného sloupce. Můžete odkazovat na jiné sloupce, nemůžete však odkazovat na buňku sestavy ve vzorci **IF**. Všechny výpočtu musí být uplatněny pro celý sloupec. Například výraz **IF B&gt;100 THEN B ELSE C\*1.25** znamená „Je-li částka ve sloupci B vyšší než 100, vložit hodnotu ze sloupce B do sloupce **CALC**. Není-li částka ve sloupci B větší než 100, vynásobit hodnotu ve sloupci C hodnotou 1,25 a vložit výsledky do sloupce **CALC**“. Vždy následujte výrok **IF** logickým prohlášením, které lze vyhodnotit jako pravdu nebo nepravdu. Vzorce, které použijete pro oba výroky **THEN** a výraz **ELSE** mohou obsahovat odkazy na libovolný počet sloupců a tyto vzorce mohou být tak složité, jak budete potřebovat.

> [!NOTE]
> Nemůžete vložit výsledky výpočtu do žádného jiného sloupce. Výsledky musí být ve sloupci, který obsahuje vzorec.

#### <a name="use-single-quotes-and-an-ampersand-for-dimension-values-in-a-row-column-or-tree"></a>Použití jednoduchých uvozovek a znaku ampersand pro hodnoty dimenze v řádku, sloupci nebo stromu

Sestavy lze navrhovat pomocí hodnot dimenzí, které obsahují znak ampersand (&).

V rámci jakéhokoliv pole **Odkaz na finanční dimenze** můžete zadat hodnotu, například **P&L**. Zahrnutí jednoduchých uvozovek (' ') na obou stranách hodnoty dimenze označuje, že používáte hodnotu literálu, například zahrnutí znaku ampersandu (&).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
