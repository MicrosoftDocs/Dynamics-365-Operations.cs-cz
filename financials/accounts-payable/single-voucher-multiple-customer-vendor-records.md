---
title: "Jeden doklad se záznamy několika odběratelů nebo dodavatelů"
description: "Toto téma poskytuje přehled o to, co se stane, když zaúčtujete jeden doklad s více záznamy odběratele nebo dodavatele. Tato funkce nebude podporována v budoucích verzích aplikace Microsoft Dynamics 365 for Operations, proto nedoporučujeme využívat tuto metodu účtování z důvodu dopadu účetnictví na zpracování vyrovnání."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 222534
ms.assetid: d4df11ce-4d36-4c66-8230-f5fc58e021bc
ms.search.region: global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b1038ea950141f0e7d4678cac9edd3b0bd5beb6f
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="single-voucher-with-multiple-customer-or-vendor-records"></a>Jeden doklad se záznamy několika odběratelů nebo dodavatelů

[!include[banner](../includes/banner.md)]


Toto téma poskytuje přehled o to, co se stane, když zaúčtujete jeden doklad s více záznamy odběratele nebo dodavatele. Tato funkce nebude podporována v budoucích verzích aplikace Microsoft Dynamics 365 for Operations, proto nedoporučujeme využívat tuto metodu účtování z důvodu dopadu účetnictví na zpracování vyrovnání. 

Běžné příklady, kdy se jeden doklad se záznamy používá pro několika odběratelů nebo dodavatelů, zahrnují převody zůstatku mezi odběrateli a vzájemných zůstatků mezi odběrateli a dodavateli v rámci stejné organizace. 

Doklad obsahující více než jednoho odběratele nebo dodavatele lze zadat pomocí některé z následujících metod:

-   Pomocí deníku, který má vybranou možnost **Pouze jedno číslo dokladu**, takže každý přidaný řádek do deníku je zahrnut na stejném dokladu.
-   Používání dokladu s více řádky, kde neexistuje žádný protiúčet hlavní knihy, s více než jedním odběratelem nebo dodavatelem.
-   Zadání dokladu s účtem a protiúčtem, ať jde o dodavatele/dodavatele, odběratele/odběratele, odběratele/dodavatele nebo odběratele/dodavatele.

Toto téma popisuje, jak se zpracovává vyrovnání při zaúčtování jednoho dokladu několika odběratelů nebo dodavatelů. Toto téma dále obsahuje postupy, které vám pomohou pochopit, jak se vyhnout používání jednoho dokladu se záznamy několika odběratelů nebo dodavatelů. Zejména uvádíme příklady, které ilustrují dva běžné scénáře vyrovnání ovlivněné použitím jednoho dokladu se záznamy několika odběratelů nebo dodavatelů:

-   Účtování platební slevy
-   Účtování přecenění

## <a name="how-does-settlement-impact-single-voucher-usage"></a>Jak vyrovnání ovlivňuje využití jednoho dokladu
Při zaúčtování jednoho dokladu se záznamy několika odběratelů nebo dodavatelů, vytvoří se jeden účetní doklad obsahující více pohledávek nebo závazků zůstatků. Během procesu vyrovnání slouží původní účetní položky k vytvoření účetní položky pro platební slevu, nerealizované zisky a ztráty, realizované zisky a ztráty a úlevu od souhrnného účtu z původního dokumentu. Například pokud dojde k platební slevě při vyrovnání platby faktury dodavatele, musí účetní platební slevy zaúčtovat do hlavní knihy splatných účty slevu z původní faktury. V případě, že původní faktura byla zaúčtována v dokladu se záznamy několika odběratelů nebo dodavatelů, bude shrnuta v původním účetnictví. V takovém případě (protože neexistuje žádný způsob, jak se dostat k podrobné účetní položce pro jednotlivé transakce dodavatele v jednom dokladu) není možné zjistit, jak uživatel zamýšlel, aby se platební sleva zaúčtovala.

### <a name="one-voucher-with-multiple-vendors-and-the-impact-on-cash-discount-accounting"></a>Jeden doklad se záznamy několika dodavatelů a vliv na účtování platební slevy

V následujícím příkladu byl nahrán větší počet dodavatelských faktur do hlavní knihy do jednoho dokladu stránky **Hlavního deníku**. Tyto faktury jsou distribuovány napříč několika dimenzemi účtů.

|             |                  |              |                 |           |            |
|-------------|------------------|--------------|-----------------|-----------|------------|
| **Doklad** | **Typ účtu** | **Účet**  | **Popis** | **Má Dáti** | **Kreditní** |
| GNJL001     | Dodavatel           | 1 001         | INV1            |           | 100,00     |
| GNJL001     | Dodavatel           | 1 001         | INV2            |           | 200,00     |
| GNJL001     | Dodavatel           | 1 001         | INV3            |           | 300,00     |
| GNJL001     | Hlavní kniha           | 606300-001-- | INV1            |   50,00   |            |
| GNJL001     | Hlavní kniha           | 606300-002-- | INV1            |   50,00   |            |
| GNJL001     | Hlavní kniha           | 606300-003-- | INV2            | 200,00    |            |
| GNJL001     | Hlavní kniha           | 606300-004-- | INV3            | 300,00    |            |

Po zaúčtování byl vytvořen jeden doklad.

|             |              |                  |                                    |
|-------------|--------------|------------------|------------------------------------|
| **Doklad** | **Účet**  | **Typ zaúčtování** | **Částka v měně transakce** |
| GNJL001     | 606300-001-- | Deník hlavní knihy   | 50,00                              |
| GNJL001     | 606300-002-- | Deník hlavní knihy   | 50,00                              |
| GNJL001     | 606300-003-- | Deník hlavní knihy   | 200,00                             |
| GNJL001     | 606300-004-- | Deník hlavní knihy   | 300,00                             |
| GNJL001     | 200110-001-  | Zůstatek dodavatele   | -100,00                            |
| GNJL001     | 200110-001-  | Zůstatek dodavatele   | -200,00                            |
| GNJL001     | 200110-001-  | Zůstatek dodavatele   | -300.00                            |

Všimněte si, že doklad obsahuje tři položky pro zaúčtování typu zůstatku dodavatele do jednoho dokladu. Neexistuje žádný způsob, jak označit, že debet 50.00 pro 606300 001 a debet 50.00 pro 606300 002 jsou zamýšleny jako protiúčet pro položku 200110 001 zůstatku dodavatele. Důvodem je skutečnost, že uživatel zadal více záznamů dodavatele do jednoho dokladu.

Pomocí tohoto příkladu můžeme analyzovat dopad, jaký má používání jednoho dokladu na podřízené vyúčtování vyrovnání. Při předpokladu, že zaplatíte 197.00 z faktury 200,00, takže 3,00 činí platební sleva. Všimněte si, že účetní hodnota platební slevy je přidělena napříč všemi dimenzemi z účtů výdajů dokladu faktury. Důvodem je skutečnost, že jeden doklad byl použit k zaúčtování výše uvedené faktury bez údaje o způsobu, jakým uživatel zamýšlí, aby distribuce výdajů byla v korelaci se zůstatkem dodavatele v jednom dokladu.

|             |              |                      |           |            |
|-------------|--------------|----------------------|-----------|------------|
| **Doklad** | **Účet**  | **Typ zaúčtování**     | **Má Dáti** | **Kreditní** |
| APPAYM001   | 200110-001-  | Zůstatek dodavatele       | 197.00    |            |
| APPAYM001   | 110110-001-  | Banka                 |           | 197.00     |
| 14000056    | 520200-001-- | Platební sleva dodavatele |           | 0.25       |
| 14000056    | 520200-002-- | Platební sleva dodavatele |           | 0.25       |
| 14000056    | 520200-003-- | Platební sleva dodavatele |           | 1,00       |
| 14000056    | 520200-004-- | Platební sleva dodavatele |           | 1.50       |
| 14000056    | 200110-001-  | Zůstatek dodavatele       | 3,00      |            |

Pokud uživatel není spokojen, že se platební sleva přiděluje napříč všemi distribucemi výdajů z původní faktury, namísto jednoho dokladu, mělo by se pro záznam faktur použít několika dokladů. Zde je uveden příklad, jak mohlo být zadáno několik dokladů v hlavní knize, namísto jednoho dokladu, jak je uvedeno na začátku tohoto příkladu.

|             |                  |              |                 |           |            |                 |                    |
|-------------|------------------|--------------|-----------------|-----------|------------|-----------------|--------------------|
| **Doklad** | **Typ účtu** | **Účet**  | **Popis** | **Má Dáti** | **Kreditní** | **Typ odsazení** | **Protiúčet** |
| GNJL001     | Dodavatel           | 1 001         | INV1            |           | 100,00     | Hlavní kniha          | &lt;Nevyplněné&gt;:      |
| GNJL001     | Hlavní kniha           | 606300-001-- | INV1            |   50,00   |            | Hlavní kniha          | &lt;Nevyplněné&gt;:      |
| GNJL001     | Hlavní kniha           | 606300-002-- | INV1            |   50,00   |            | Hlavní kniha          | &lt;nevyplněné&gt;:      |
| GNJL002     | Dodavatel           | 1 001         | INV2            |           | 200,00     | Hlavní kniha          | 606300-003--       |
| GNJL003     | Dodavatel           | 1 001         | INV3            |           | 300,00     | Hlavní kniha          | 606300-004--       |

Nyní po zaplacení INV2 vznikne následující položka. Všimněte si, že platební sleva finanční dimenze se řídí finančními dimenzemi přidružených výdajů.

|             |              |                      |           |            |
|-------------|--------------|----------------------|-----------|------------|
| **Doklad** | **Účet**  | **Typ zaúčtování**     | **Má Dáti** | **Kreditní** |
| APPAYM001   | 200110-001-  | Zůstatek dodavatele       | 197.00    |            |
| APPAYM001   | 110110-001-  | Banka                 |           | 197.00     |
| 14000056    | 520200-003-- | Platební sleva dodavatele |           | 3,00       |
| 14000056    | 200110-001-  | Zůstatek dodavatele       | 3,00      |            |

### <a name="one-voucher-with-multiple-vendors-and-the-impact-on-realized-gainloss-accounting"></a>Jeden doklad se záznamy několika dodavatelů a vliv na účtování provedených zisků/ztrát

|             |                  |             |                 |           |            |                  |              |
|-------------|------------------|-------------|-----------------|-----------|------------|------------------|--------------|
| **Doklad** | **Typ účtu** | **Účet** | **Popis** | **Má Dáti** | **Kreditní** | **Typ účtu** | **Účet**  |
| GNJL001     | Dodavatel           | 1 001        | INV1            |           | 100,00     | Hlavní kniha           | 606300-001-- |
| GNJL001     | Dodavatel           | 1 001        | INV2            |           | 200,00     | Hlavní kniha           | 606300-002-- |

V následujícím příkladu byl nahrán větší počet dodavatelských faktur do hlavní knihy do jednoho dokladu stránky **Hlavního deníku**. Tyto faktury jsou distribuovány napříč několika dimenzemi účtů. Po zaúčtování byl vytvořen jeden doklad.

|             |              |                  |                                          |                                         |
|-------------|--------------|------------------|------------------------------------------|-----------------------------------------|
| **Doklad** | **Účet**  | **Typ zaúčtování** | **Částka v měně transakce (EUR)** | **Částka v zúčtovací měně (USD)** |
| GNJL001     | 606300-001-- | Deník hlavní knihy   | 100,00                                   | 114.00                                  |
| GNJL001     | 606300-002-- | Deník hlavní knihy   | 200,00                                   | 228.00                                  |
| GNJL001     | 200110-001-  | Zůstatek dodavatele   | -100,00                                  | -114.00                                 |
| GNJL001     | 200110-001-  | Zůstatek dodavatele   | -200,00                                  | -228.00                                 |

Všimněte si, že doklad obsahuje dvě položky pro zaúčtování typu zůstatku dodavatele do jednoho dokladu. Neexistuje žádný způsob, jak označit, že debet pro 606300-001 jsou zamýšleny jako protiúčet pro položku 100.00 to 200110-001 zůstatku dodavatele. Důvodem je skutečnost, že uživatel zadal více záznamů dodavatele do jednoho dokladu. 

Pomocí tohoto příkladu můžeme analyzovat dopad, jaký má používání jednoho dokladu na podřízené vyúčtování vyrovnání. Předpokládejme, že je vaší zúčtovací měnou USD a že výše uvedené transakce byly zaúčtovány v měně transakce EUR. Předpokládejme, že plně uhradíte fakturu na 200,00 EUR, ale narazíte na realizovanou ztrátu vzniklou kvůli rozdílu směnného kurzu mezi dobami zaúčtování faktury a platby. Všimněte si, že účetní hodnota realizované ztráty je přidělena napříč všemi dimenzemi z účtů výdajů dokladu faktury. V takovém případě byly přiděleny obě dimenze (001 i 002), i když to uživatel může vnímat tak, že pouze 002 patří do účtu výdajů z faktury, u které je prováděno vyrovnání. Důvodem je skutečnost, že jeden doklad byl použit k zaúčtování výše uvedené faktury a neexistuje způsob, jak prozradit, jakým uživatel zamýšlí, aby distribuce výdajů byla v korelaci se zůstatkem dodavatele v jednom dokladu.

|             |             |                    |                                          |                                         |
|-------------|-------------|--------------------|------------------------------------------|-----------------------------------------|
| **Doklad** | **Účet** | **Typ zaúčtování**   | **Částka v měně transakce (EUR)** | **Částka v zúčtovací měně (USD)** |
| APPAYM001   | 200110-001- | Zůstatek dodavatele     | 200,00                                   | 230.00                                  |
| APPAYM001   | 110110-001- | Banka               | -200,00                                  | -230.00                                 |
| 14000056    | 801300-001- | Ztráta směnného kurzu | 0,00                                     | 0.67                                    |
| 14000056    | 801300-002- | Ztráta směnného kurzu | 0,00                                     | 1.33                                    |
| 14000056    | 200110-001- | Zůstatek dodavatele     |                                          | -2.00                                   |

Pokud uživatel není spokojen, že se ztráta směnného kurzu přiděluje napříč všemi distribucemi výdajů z původní faktury, namísto jednoho dokladu, mělo by se pro záznam faktur použít několika dokladů. Zde je uveden příklad, jak mohlo být zadáno několik dokladů v hlavní knize, namísto jednoho dokladu, jak je uvedeno na začátku tohoto příkladu.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Doklad** | **Typ účtu** | **Účet** | **Popis** | **Má Dáti** | **Kreditní** | **Typ protiúčtu** | **Protiúčet** |
| GNJL002     | Dodavatel           | 1 001        | INV1            |           | 100,00     | Hlavní kniha          | 606300-001--       |
| GNJL003     | Dodavatel           | 1 001        | INV2            |           | 200,00     | Hlavní kniha          | 606300-002--       |

Nyní po zaplacení INV2 vznikne následující položka. Všimněte si, že platební sleva finanční dimenze se řídí finančními dimenzemi přidružených výdajů.

|             |             |                    |                                          |                                         |
|-------------|-------------|--------------------|------------------------------------------|-----------------------------------------|
| **Doklad** | **Účet** | **Typ zaúčtování**   | **Částka v měně transakce (EUR)** | **Částka v zúčtovací měně (USD)** |
| APPAYM001   | 200110-001- | Zůstatek dodavatele     | 200,00                                   | 230.00                                  |
| APPAYM001   | 110110-001- | Banka               | -200,00                                  | -230.00                                 |
| 14000056    | 801300-002- | Ztráta směnného kurzu | 0,00                                     | 2,00                                    |
| 14000056    | 200110-001- | Zůstatek dodavatele     |                                          | -2.00                                   |

## <a name="one-voucher-for-balance-transfers-and-netting-scenarios"></a>Jedno číslo dokladu pro převody zůstatků a vzájemné scénáře
Dva běžně používané scénáře, které používají jeden doklad obsahující více zákazníků nebo dodavatelů zahrnují zůstatky převodů od jednoho odběratele nebo dodavatele na jiného odběratele nebo dodavatele, a vzájemné vztahy odběratele a dodavatele, kteří jsou ze stejné organizace. Následující dva příklady ilustrují upřednostňovanou metodu zadávání scénářů v Dynamics 365 for Operations jako alternativu k zadávání do jednoho dokladu. 

*Zůstatek převodu* je jeden doklad s více zákazníky, který je zadaný pro účely převodu zůstatku od jednoho odběratele k jinému odběrateli (totéž platí pro dodavatele). Tento scénář může nastat, pokud zodpovědnost za platbu faktury přechází na jinou stranu, jako je například dceřiná společnost, která přesouvá zodpovědnost k mateřské společnosti. 

Tento příklad předpokládá prodej, kde má odběratel nárok na platební slevu, pokud bude platba uskutečněna do 10 dní. V tomto případě odběratel využívá pojišťovací společnost, která bude odpovědná za zaplacení. Pojišťovací společnost je nastavena v systému jako druhý odběratel. Původní zůstatek odběratele se převede na pojišťovací společnost, která zaplatí, přičemž získá platební slevu 2 %, jelikož platbu provedla během období slevy. 

Například předpokládejme, že následující prodej je proveden odběrateli ACME. Následující účetní položky představují prodej.

|                    |                  |           |            |
|--------------------|------------------|-----------|------------|
| **Účet hlavní knihy** | **Typ zaúčtování** | **Má Dáti** | **Kreditní** |
| 401100-002-023-    | Výnosy          |           | 100        |
| 130100-002-        | Zůstatek odběratele | 100       |            |

Za další, uživatel přesune splatný zůstatek z ACME pojišťovací společnosti, a to do jednoho dokladu v Deníku plateb pohledávek. V aplikaci Dynamics 365 for Operations je pojišťovací společnost nastavena jako odběratel pojištění.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Doklad** | **Typ účtu** | **Účet** | **Popis** | **Má Dáti** | **Kreditní** | **Typ protiúčtu** | **Protiúčet** |
| ARPAYM001   | Zákazník         | ACME        | Převod        |           | 100,00     | Zákazník        | Pojištění          |

Všimněte si, výše uvedená položka je součástí jedno čísla dokladu. Tento doklad obsahuje dva záznamy odběratelů. Následující doklad byl vytvořen, když byla zaúčtována výše uvedená položka hlavní knihy.

|             |             |                  |                                    |
|-------------|-------------|------------------|------------------------------------|
| **Doklad** | **Účet** | **Typ zaúčtování** | **Částka v měně transakce** |
| ARPAYM001   | 130100-002- | Zůstatek odběratele | 100,00                             |
| ARPAYM001   | 130100-002- | Zůstatek odběratele | -100,00                            |

Dále předpokládejme, že obdržíte platbu od odběratele pojištění pro 98,00 a rozhodnete se vyrovnat platbu fakturou, která byla vytvořena převodem zůstatku. Výsledkem bude zaúčtování následujícího dokladu. Může dojít k očekávání, že vyrovnání využívá finanční dimenze z původní faktury, ale to není možné vzhledem k tomu, že není k dispozici dokument faktury pro odběratele pojištění. Všimněte si, že v původním nastavení přicházejí dimenze distribuce na platební slevu z transakce odběratele vytvořené z převodu, nikoli z původní faktury účtu výnosů. Výchozí hodnota je výsledkem použití jednoho dokladu pro převod zůstatků.

|             |             |                  |           |            |
|-------------|-------------|------------------|-----------|------------|
| **Doklad** | **Účet** | **Typ zaúčtování** | **Má Dáti** | **Kreditní** |
| ARPAYM002   | 110110-002- | Banka             | 98.00     |            |
| ARPAYM002   | 130100-002- | Zůstatek odběratele |           | 98.00      |

V souvisejícím dokladu pro platební slevu vychází výchozí hodnota pro finanční dimenzi z transakce odběratele vytvořené z převodu, protože převod má více než jednoho odběratele.

|             |             |                        |           |            |
|-------------|-------------|------------------------|-----------|------------|
| **Doklad** | **Účet** | **Typ zaúčtování**       | **Má Dáti** | **Kreditní** |
| ARP-00001   | 403300-002- | Platební sleva odběratele | 2,00      |            |
| ARP-00001   | 130100-002- | Zůstatek odběratele       |           | 2,00       |

Pokud uživatel není spokojen s výchozím nastavením finanční dimenze pro platební slevu, může namísto jednoho dokladu použít několik dokladů pro záznam převodu zůstatku. Tohoto scénáře by mělo být dosaženo, pokud vytvoříte dobropis pro odběratele, že zůstatek je přesunut Z, a že byl vytvořen dobropis nebo faktura pro odběratele, kterému je zůstatek přesunut DO. Následující příklad ukazuje, jak může být několik dokladů zadáno v Deníku plateb pohledávek pro převod zůstatku, namísto jednoho dokladu, jak bylo uvedeno výše v tomto příkladu.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Doklad** | **Typ účtu** | **Účet** | **Popis** | **Má Dáti** | **Kreditní** | **Typ protiúčtu** | **Protiúčet** |
| ARPAYM001   | Zákazník         | ACME        |                 |           | 100,00     | Hlavní kniha          | 401100-002-023-    |
| ARPAYM002   | Zákazník         | Pojištění   |                 | 100,00    |            | Hlavní kniha          | 401100-002-023-    |

To znamená, že když odběratel pojištění zaplatí 98,00 s dokladem ARPAYM02, bude použita správná finanční dimenze z dokladu ARPAYM002 účtu hlavní knihy.

|             |             |                  |           |            |
|-------------|-------------|------------------|-----------|------------|
| **Doklad** | **Účet** | **Typ zaúčtování** | **Má Dáti** | **Kreditní** |
| ARPAYM003   | 110110-002- | Banka             | 98.00     |            |
| ARPAYM003   | 130100-002  | Zůstatek odběratele |           | 98.00      |

V souvisejícím dokladu pro platební slevu budou použity finanční dimenze z vyrovnání účtu výnosů zobrazeném na dokladu ARPAYM002.

|             |                 |                        |           |            |
|-------------|-----------------|------------------------|-----------|------------|
| **Doklad** | **Účet**     | **Typ zaúčtování**       | **Má Dáti** | **Kreditní** |
| ARP-00001   | 403300-002-023- | Platební sleva odběratele | 2,00      |            |
| ARP-00001   | 130100-002-     | Zůstatek odběratele       |           | 2,00       |

### 

## <a name="one-voucher-with-a-netting-for-multiple-customers-and-vendors"></a>Jedno číslo dokladu s vypořádáním pro více odběratelů a dodavatelů
Vypořádání může být užitečné při organizaci nákupů nebo prodejů v rámci stejné společnosti. Namísto úhrady faktur dodavatelů a čekáním na přijetí platby pro faktury odběratelů jsou vyrovnány faktury dodavatelů a odběratelů. Transakce vyrovnání se počítá proti neuhrazeným zůstatkům. 

Předpokládejme například, že dodavatel 1001 a zákazník US-008 jsou stejnými osobami, takže chce vaše organizace chce vypořádat zůstatky závazků a pohledávek před přijetím/zaplacením zbývajících zůstatků. Předpokládejme, že záznam odběratele dluží 75.00 EUR a záznam dodavatele má pohledávku 100,00 EUR, což znamená, že chcete raději vypořádat zůstatky a zaplatit dodavateli jen 25,00 EUR Dále předpokládejme, že zúčtovací měnou je USD. V takovém případě se zadává transakce vypořádání do jednoho dokladu v deníku plateb závazků.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Doklad** | **Typ účtu** | **Účet** | **Popis** | **Má Dáti** | **Kreditní** | **Typ protiúčtu** | **Protiúčet** |
| APPAYM001   | Dodavatel           | 1 001        | Určování čistých částek         |  75,00    |            | Zákazník        | US-008             |

Chcete-li se vyhnout nežádoucím problémům s budoucím vyrovnání pro tuto transakci. měli byste namísto jednoho dokladu zadat několik dokladů v deníku, aby došlo k zápisu transakce vyrovnání. Všimněte si, že zůstatky odběratele a dodavatele jsou vyrovnány jedním clearingovým účtem. Díky tomu se můžete vyhnout použití jednoho dokladu, který obsahuje několik zůstatků odběratele a dodavatele.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Doklad** | **Typ účtu** | **Účet** | **Popis** | **Má Dáti** | **Kreditní** | **Typ protiúčtu** | **Protiúčet** |
| 001         | Zákazník         | US-008      |                 |           |  75,00     | Hlavní kniha          | 999999---          |
| 002         | Dodavatel           | 1 001        |                 |  75,00    |            | Hlavní kniha          | 999999---          |

 




