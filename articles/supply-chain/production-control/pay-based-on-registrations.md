---
title: "Plat na základě registrace"
description: "Toto téma popisuje způsob výpočtu mzdy na základě registrací pracovníka."
author: johanhoffmann
manager: AnnBe
ms.date: 03/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgCalcApproveWeekView
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-03-20
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1ae0f142ebd2252b1df414998c153d32127bc1b7
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="pay-based-on-registrations"></a>Plat na základě registrace

[!include [banner](../includes/banner.md)]

Toto téma podrobně popisuje způsob výpočtu mzdy na základě registrací pracovníka. Obsahuje příklady ukazující, jak různé kombinace možností nastavení, které jsou k dispozici pro výpočet, ovlivní výsledek. Zde jsou uvedeny některé z oblastí, které budou pokryty:

- Pružná doba
- Přesčas
- Přestávky
- Přepínací kódy
- Položky mzdy
- Platební smlouvy
- Parametry výpočtu času a docházky
- Nepřítomnost

## <a name="the-use-of-flex-time"></a>Použití pružné pracovní doby

Období pružného času jsou nastavena v časových profilech, které se používají v modulu Čas a docházka. Existují dva typy profilů pružné pracovní doby: **Flex+** a **Flex-**. Když pracovník registruje čas v době Flex+, pružný zůstatek pracovníka se zvyšuje podle odpracovaných hodin. Pracovník nedostane žádnou kompenzaci za hodiny, které byly odpracovány během pružné pracovní doby Flex+. Pracovník si však může vzít volno v obdobích Flex- a být kompenzován za hodiny od svého zůstatku pružné pracovní doby. Proto volno během pružné pracovní doby považuje systém za absenci.

## <a name="scenarios-based-on-flex-periods"></a>Scénáře na základě pružné pracovní doby

Dva následující scénáře vycházejí z profilu pružné pracovní doby, která předtavuje pracovní den. V obou případech je mzda vypočítávána podle období pružné pracovní doby, kdy pracovník označí příchod a odchod.

### <a name="flex-profile-for-one-workday"></a>Profil pružné pracovní doby pro jeden pracovní den

| Typ profilu  | Spuštění    | Konec      | Den     |
|---------------|----------|----------|---------|
| Přesčas     | 00:00 dop. | 06:00 dop. | Pondělí  |
| Flexibilita+         | 06:00 dop. | 07:00 dop. | Pondělí  |
| Registrace příchodu      | 07:00 dop. | 07:00 dop. | Pondělí  |
| Standardní čas | 07:00 dop. | 02:30 odp. | Pondělí  |
| Flexibilita-         | 02:30 odp. | 03:30 odp. | Pondělí  |
| Registrace odchodu     | 03:30 odp. | 03:30 odp. | Pondělí  |
| Přesčas     | 03:30 odp. | 06:00 dop. | Úterý |

### <a name="scenario-1-a-worker-registers-clock-in-during-a-flex-period-and-clock-out-during-a-flex--period"></a>Scénář 1: Pracovník označí příchod během pružné pracovní doby (Flex+) a odchod během pružné pracovní doby (Flex-).

Registrace pracovníka za daný den vypadají takto.

| Typ registrace deníku | Spuštění    | Konec      |
|---------------------------|----------|----------|
| Registrace příchodu                  | 06:30 dop. | 06:30 dop. |
| Výrobní úloha            | 06:30 dop. | 02:45 odp. |
| Registrace odchodu                 | 02:45 odp. | 02:45 odp. |

Registrace pracovníka pro den jsou vypočítány a přenesena do mzdy na stránce **schválit** (**Čas a docházka** &gt; **Zkontrolovat a schválit** &gt; **Schválit**). Poté, co byly registrace vypočteny, výsledek výpočtu může být zobrazen na kartě **Časy**. 

Abyste pochopili tento scénář, podívejte se na následující pole.

| Flex + | Flex - | Čas | Placený čas |
|--------|--------|------|----------|
| 0,50   | 0.75   | 8.25 | 8.50     |

#### <a name="calculation-of-flex"></a>Výpočet Flex+

Podle profilu pružné pracovní doby je doba mezi 06:00 do 07:00 dopoledne období Flex+. Proto pokud pracovník označí příchod v 06:30, získá 0,5 hodiny. Toto množství času je přidáno na účet pružné pracovní doby zaměstnance.

#### <a name="calculation-of-flex-"></a>Výpočet Flex-

Podle profilu pružné pracovní doby, období pružné doby začíná v 02:30 odp. a končí v 03:30 odp. Pokud pracovníka označí odchod v 14:45, 45 minut (0,75 hodiny) zbývajích v pružné pracovní době Flex- se zaregistruje jako placený čas, a stejná doba bude odečtena od účtu pružné pracovní doby pracovníka. 45 minut je zahrnuto v placeném čase, protože pracovník má nárok na zaplacení zbývajících 45 minut v pružné pracovní době Flex-. Pokud pracovník není k dispozici během doby Flex-, bude od jeho účtu pružné pracovní doby odečteno 45 minut.

#### <a name="calculation-of-time"></a>Výpočet času

Čas se vypočítá jako časový interval mezi příchodem a odchodem, to je 06:30 až 14:45, což se rovná 8,25 hodin.

#### <a name="calculation-of-pay-time"></a>Výpočet placeného času

Placený čas je čas, za který má pracovník zaručenu výplatu. V tomto případě je pracovník v práci 8,25 hodiny (**čas**). Avšak **placený čas** se vypočítá jako počet hodin 8,50, protože pracovník má zaručený plat během období Flex- poté, co zaregistruje odchod. Placený čas rovná se plánované pracovní hodiny pružné pracovní doby, protože doba Flex+ je přidána k účtu pružné pracovní doby pracovníka, ne pro placený čas. Čas absence v období pružné pracovní doby Flex- je kompenzován placeným časem a odečten z účtu pracovní doby pracovníka.

| Čas              | Typ registrace | Placený čas (hodiny)      |
|-------------------|-------------------|-----------------------|
| 6:30:00 - 7:00:00 dop | Flexibilita+             | 0                     |
| 7:00 dop. – 2:45 odp. | Standardní čas     | 7.75                  |
| 2:45 odp. – 3:30 odp. | Flexibilita-             | 0,75 (období absence) |
|                   | Celkem             | 8.50                  |

### <a name="scenario-2-a-worker-works-during-the-whole-flex--period-and-also-works-overtime"></a>Scénář 2: Pracovník pracuje během celé pružné pracovní doby (Flex-) a také pracuje přesčas

Registrace pracovníka za daný den vypadají takto.

| Typ registrace deníku | Spuštění    | Konec      |
|---------------------------|----------|----------|
| Registrace příchodu                  | 06:30 dop. | 06:30 dop. |
| Výrobní úloha            | 06:30 dop. | 05:00 odp. |
| Registrace odchodu                 | 05:00 odp. | 05:00 odp. |

Poté, co jste vypočítali registrace deníku na stránce **Schválit** můžete zobrazit výsledek výpočtu na kartě **časy**. Pro pochopení tohoto scénáře viz následující pole.

| Flex + | Flex - | Čas  | Placený čas | Placený přesčas |
|--------|--------|-------|----------|--------------|
| 0,50   | 0,00   | 10,50 USD | 10.00    | 1.50         |

#### <a name="calculation-of-flex"></a>Výpočet Flex+

Podle profilu pružné pracovní doby je doba mezi 06:00 do 07:00 dopoledne období Flex+. Proto pokud pracovník označí příchod v 06:30, získá 0,5 hodiny pružné pracovní doby Flex+ na svém zůstatku pružné pracovní doby.

#### <a name="calculation-of-flex-"></a>Výpočet Flex-

Vzhledem k tomu, že pracovník pracuje v období Flex-, Flex. se nevypočítává. Flex- se vypočítává, pouze pokud je pracovník nepřítomen během Flex-. Z pohledu platby platí, že pokud pracovník pracuje během období Flex-, má přidělenou platební sazbu definovanou pro standardní čas. Pokud pracovník není k dispozici během doby Flex+, bude od jeho účtu pružné pracovní doby odečteno 45 minut.

#### <a name="calculation-of-time"></a>Výpočet času

Čas se vypočítá jako časový interval mezi příchodem ve 06:30 a odchodem v 17:00, což se rovná 10,50 hodiny.

#### <a name="calculation-of-pay-time"></a>Výpočet placeného času

V tomto případě pracovník pracuje 10,50 hodiny (**čas**). Platí však, že **placený čas** se počítá jako 10,00 hodin, protože pracovník nemá zaručenu platbu během období Flex+.

#### <a name="calculation-of-pay-overtime"></a>Výpočet placeného přesčasu

| Čas               | Typ registrace | Placený čas (hodiny) |
|--------------------|-------------------|------------------|
| 6:30:00 - 7:00:00 dop  | Flexibilita+             | 0                |
| 7:00:00-14:30:00 odp.  | Standardní čas     | 7.50             |
| 2:30 odp. – 3:30 odp.  | Flexibilita-             | 1.00             |
| 3:30 odp. – 05:00 odp. | Přesčas          | 1.50             |
|                    | Celkem             | 10.00            |

### <a name="generation-of-pay-items"></a>Generování položek mzdy

Registrace pracovníka pro daný den lze převést ze stránky **Schválit**. V průběhu převodu jsou generovány položky mzdy a přenesené registrace. Placené položky představují rozúčtování placeného času do standardního času, přesčasů, placené přestávky a tak dále.

Chcete-li otevřít seznam mzdových položek, vyberte **Časa a docházka** &gt; **Zkontrolovat a schválit** &gt; **Schválit**. Poté vyberte **Dotaz** &gt; **Převedené registrace**.

Položky mzdy slouží jako základ pro mzdu zaměstnance. Můžete vygenerovat soubor, který obsahuje informace z položek mzdy, a převést ho do mzdového systému.

V rámci procesu převodu jsou čas a náklady z aktivit výroby a projektu převedeny do výrobních a projektových deníků pro zaúčtování investovaného času a nákladů. Převedené registrace slouží jako základ pro čas a nákladové ceny za hodinu pro výrobní zakázky a projekty. Převedené registrace lze otevřít pomocí nabídky **Dotaz** na stránce **Schválit**.

Například ve scénáři 2 jsou generovány následující položky mzdy.

| Typ mzdy     | Typ mzdy | Mzdové jednotky | Kurz  | Celkové náklady |
|---------------|----------|-----------|-------|------------|
| Standardní čas | 1201     | 10.0      | 10    | 100        |
| Přesčas      | 1301     | 1.50      | 5     | 7.50       |
|               |          |           | Celkem | 107.50     |

Položka mzdy pro standardní čas má mzdovou jednotku 10 hodin, což pokrývá standardní pracovní dobu, pružnou pracovní dobu Flex- a přesčas. Standardní čas, pružný pracovní doba (Flex-) a přesčas jsou konsolidovány do jedné mzdové položky, protože všechny typy se počítají jako standardní čas, na základě výchozí nastavení parametru na stránce **Parametry výpočtu** (**Čas a docházka** &gt; **Nastavení** &gt; **Parametry výpočtu**). Přesčas je počítán navíc ke standardnímu času pomocí dodatečné sazby 5.

Aby bylo možné zřetelně rozlišit standardní čas a přesčas, tak, aby mzdové jednotky pro typy mzdy pokrývaly pouze skutečný strávený čas a standardní čas a přesčas, mzdové jednotky pro standardní čas musí být vypočítány jako 8,50 a mzdových jednotky pro přesčas musí být vypočítány jako 1,50.

Chcete-li nakonfigurovat systém tak, aby jasně rozlišoval standardní pracovní dobu a přesčas, musíte vyloučit přesčas ze standardního času. Je nutné také změnit nastavení typu mzdy pro přesčasy tak, aby mzdová sazba za práci přesčas pokrývala všechny platby za přesčasové hodiny.

### <a name="exclude-overtime-from-the-standard-time"></a>Vyloučit přesčas ze standardního času

Na stránce **Parametry výpočtu** vyberte **Přesčas** jako typ specifikace profilu a nastavte možnost **Placený čas**na **Ne**, jak je uvedeno v tomto poli.

| Reg. určení | Typ specifikace profilu | Výpočet   |     | Placeno         |     |
|--------------------|----------------------------|---------------|-----|--------------|-----|
| Prac. doba       | Přesčas                   | Standardní čas | Ano | Placený čas     | Žádný  |
|                    |                            | Placený čas      | Ano | Placený přesčas | Ano |

Po úpravě parametrů výpočtu jsou generovány následující položky mzdy.

| Typ mzdy     | Typ mzdy | Mzdové jednotky | Kurz  | Celkové náklady |
|---------------|----------|-----------|-------|------------|
| Standardní čas | 1201     | 8.50      | 10    | 85.0       |
| Přesčas      | 1301     | 1.50      | 15    | 22.50      |
|               |          |           | Celkem | 107.50     |

> [!NOTE]
> Parametry výpočtu mají doporučené standardní nastavení. Obecně platí, že byste při změně těchto parametrů měli být opatrní. Chcete-li obnovit doporučené standardní nastavení, na stránce **Parametry výpočtu** vyberte **Obnovit hodnoty**.

### <a name="allow-a-deviation-from-the-standard-pay-profiles"></a>Povolit odchylky od standardních platebních profilů

Na stránce **Profily** (**čas a docházka** &gt; **Nastavení** &gt; **Časové profily** &gt; **Profily**) můžete nastavit typy profilů zahrnující přepínací kódy a přestávky.

### <a name="switch-codes"></a>Přepínací kódy

Přepínací kódy můžete povolit pracovníkům, aby se mohli odchýlit od svého typu profilu změnou na odlišný typ profilu. Lze například povolit pracovníka ke změně z doby Flex+ na přesčas. Pracovník může přidat přepínací kód během registrace nebo může přiřadit úkol přidání přepínacího kódu schvalujícímu registrací.

Aby bylo možné použít přepínací kód, je nutné definovat ho jako typ nepřímé činnosti. Potom je nutné přidat přepínací kód do časového profilu za období, ve kterém chcete povolit změnu typu profilu. Například podle následujícího postupu vytvořte přepínací kód, který umožňuje kladný pružný zůstatek pro období od 06:00 do 07:00 na přesčas.

1. Vytvořte přepínací kód s názvem **OTBCI (Převést pružné pracovní doby na přesčas před příchodem)**. Vyberte **Čas a docházka** &gt; **Spravovat nepřímé aktivity** &gt; **Nepřímé aktivity**.
2. Ve sloupci **Přepínací kód** přidejte OTBCI do řádku Flex+ v časovém profilu.
3. Ve sloupci **sekundární** přidejte typ profilu **Přesčas**.

Zvažte následující profil pružné pracovní doby představující pracovní den.

| Typ profilu  | Spuštění    | Konec      | Den     |
|---------------|----------|----------|---------|
| Přesčas     | 00:00 dop. | 06:00 dop. | Pondělí  |
| Flexibilita+         | 06:00 dop. | 07:00 dop. | Pondělí  |
| Registrace příchodu      | 07:00 dop. | 07:00 dop. | Pondělí  |
| Standardní čas | 07:00 dop. | 02:30 odp. | Pondělí  |
| Flexibilita-         | 02:30 odp. | 03:30 odp. | Pondělí  |
| Registrace odchodu     | 03:30 odp. | 03:30 odp. | Pondělí  |
| Přesčas     | 03:30 odp. | 06:00 dop. | Úterý |

V tomto poli jsou registrace pracovníka za daný den.

| Typ registrace deníku | Spuštění    | Konec      |
|---------------------------|----------|----------|
| Registrace příchodu                  | 06:30 dop. | 06:30 dop. |
| Výrobní úloha            | 06:30 dop. | 02:45 odp. |
| Registrace odchodu                 | 05:00 odp. | 05:00 odp. |

Po převodu jsou generovány následující položky mzdy.

| Typ mzdy     | Typ mzdy | Mzdové jednotky | Kurz  | Celkové náklady |
|---------------|----------|-----------|-------|------------|
| Standardní čas | 1201     | 8.50      | 10    | 85.0       |
| Přesčas      | 1305     | 1.50      | 15    | 22.50      |
|               |          |           | Celkem | 107.50     |

Na stránce **Schválit** zrušte převod a poté pomocí nabídky **Přepínací kód** aplikujte přepínací kód **OTBCI**. Při druhém převodu registrací jsou vygenerovány následující položky mzdy.

| Typ mzdy     | Typ mzdy | Mzdové jednotky | Kurz  | Celkové náklady |
|---------------|----------|-----------|-------|------------|
| Standardní čas | 1201     | 8.50      | 10    | 80.0       |
| Přesčas      | 1305     | 2,00      | 15    | 30.0       |
|               |          |           | Celkem | 107.50     |

> [!NOTE]
> Při použití přepínacího kódu se přesčas zvýší o 0,5 hodiny, z 1,5 na 2. 0,5 hodiny je konverze registrované pružné pracovní doby, od 6:30 do 07:00, do přesčasu.

### <a name="breaks"></a>Přestávky

Přestávky v práci mají vliv na výpočet mezd pracovníků. Přestávky jsou definované jako typ nepřímé aktivity. Lze je definovat jako **Zaplacené**, aby bylo možné přestávku přidat k mzdě pracovníka, nebo **Nezaplacené**, aby přestávka nebyla přidána do mzdy pracovníka. Přestávky lze také definovat jako **plánované** nebo **registrované**.

#### <a name="planned-breaks"></a>Plánované přestávky

Pokud má společnost pevně daný seznam přestávek, jako je například pevná přestávka na oběd, můžete být přestávka v profilu doby předddefinována. V takovém případě pracovník nemusí registrovat přestávku na stránkách karty úlohy. Místo toho je přestávka automaticky zaúčtována při výpočtu registrací pracovníka na stránce **Schválit**.

#### <a name="registered-breaks"></a>Registrované přestávky

Pokud společnost nepoužívá plánované přestávky, zaměstnanci mohou registrovat přestávky během pracovního dne. Registrované přestávky lze použít například tehdy, pokud pracovník pracuje podle profilu pružné pracovní doby, která nemá žádný definovaný čas příchodu a odchodu. Registrované přestávky jsou typem nepřímé aktivity. Pracovník zaregistruje přestávku na stránce terminálu **Úkolový lístek** nebo na stránce zařízení **Úkolový lístek**. Na obou těchto stránkách uživatel může vybrat typ konce v seznamu předdefinovaných aktivit přestávky.

#### <a name="paid-and-unpaid-breaks"></a>Placené a neplacené přestávky

Konec aktivity lze nastavit jako **zaplacené** nebo **nezaplacené**. Placená přestávka je zahrnuta do výpočtu placeného času a systém použije typ mzdy, který je definován v platební dohodě pro typ registrace **přestávka**.

### <a name="example-of-a-planned-break"></a>Příklad plánované přestávky

Zvažte následující časový profil, který obsahuje neplacenou přestávku na oběd.

| Typ profilu  | Spuštění    | Konec      | Den     |
|---------------|----------|----------|---------|
| Přesčas     | 00:00 dop. | 06:00 dop. | Pondělí  |
| Flexibilita+         | 06:00 dop. | 07:00 dop. | Pondělí  |
| Registrace příchodu      | 07:00 dop. | 07:00 dop. | Pondělí  |
| Standardní čas | 07:00 dop. | 12:00 odp. | Pondělí  |
| Přerušení         | 12:00 odp. | 12:30 odp. | Pondělí  |
| Standardní čas | 12:30 odp. | 02:30 odp. | Pondělí  |
| Flexibilita-         | 02:30 odp. | 03:30 odp. | Pondělí  |
| Registrace odchodu     | 03:30 odp. | 03:30 odp. | Pondělí  |
| Přesčas     | 03:30 odp. | 06:00 dop. | Úterý |

V tomto poli jsou registrace pracovníka za daný den.

| Typ registrace deníku | Spuštění    | Konec      |
|---------------------------|----------|----------|
| Registrace příchodu                  | 06:30 dop. | 06:30 dop. |
| Výrobní úloha            | 06:30 dop. | 02:45 odp. |
| Registrace odchodu                 | 05:00 odp. | 05:00 odp. |

Poté, co jste vypočítali registrace deníku na stránce **Schválit** můžete zobrazit výsledek výpočtu na kartě **časy**. Pro pochopení tohoto scénáře viz následující pole.

| Flex + | Flex - | Čas  | Placený čas | Neplacená přestávka | Placený přesčas |
|--------|--------|-------|----------|---------------------|--------------|
| 0,50   | 0,00   | 10,50 USD | 9.50     | 0.5                 | 1.50         |

> [!NOTE] 
> Systém vypočítá 0,5 hodiny nezaplacené přestávka a tento čas není součástí placeného času.

### <a name="example-of-a-registered-break"></a>Příklad registrované přestávky

Zvažte následující časový profil, který neobsahuje plánované přestávky.

| Typ profilu  | Spuštění    | Konec      | Den     |
|---------------|----------|----------|---------|
| Přesčas     | 00:00 dop. | 06:00 dop. | Pondělí  |
| Flexibilita+         | 06:00 dop. | 07:00 dop. | Pondělí  |
| Registrace příchodu      | 07:00 dop. | 07:00 dop. | Pondělí  |
| Standardní čas | 07:00 dop. | 02:30 odp. | Pondělí  |
| Flexibilita-         | 02:30 odp. | 03:30 odp. | Pondělí  |
| Registrace odchodu     | 03:30 odp. | 03:30 odp. | Pondělí  |
| Přesčas     | 03:30 odp. | 06:00 dop. | Úterý |

V tomto poli jsou registrace pracovníka za daný den.

| Typ registrace deníku | Spuštění    | Konec      |
|---------------------------|----------|----------|
| Registrace příchodu                  | 06:30 dop. | 06:30 dop. |
| Výrobní úloha            | 06:30 dop. | 05:00 odp. |
| Přerušení                     | 12:03 odp. | 12:32 odp. |
| Registrace odchodu                 | 05:00 odp. | 05:00 odp. |

Při výpočtu registrací se vypočítá čas aktivit.

| Typ registrace deníku | Spuštění    | Konec      | Čas  |
|---------------------------|----------|----------|-------|
| Registrace příchodu                  | 06:30 dop. | 06:30 dop. |       |
| Výrobní úloha            | 06:30 dop. | 05:00 odp. | 10.00 |
| Přerušení                     | 12:03 odp. | 12:32 odp. | 0,50  |
| Registrace odchodu                 | 05:00 odp. | 05:00 odp. |       |

> [!NOTE]
> Čas přestávky běží současně s časem aktivity (v tomto příkladu je to výrobní úloha). Toto chování se používá vždy pro aktivity přestávky. Při výpočtu registrací se doba přestávky odečte od času aktivity. V takovém případě má výrobní úloha dobu trvání 10,50 hodin, ale čas se vypočítá jako 10, protože 0,5 hodin přestávka je odečtena od času aktivity.

Poté, co jste vypočítali registrace deníku na stránce **Schválit** můžete zobrazit výsledek výpočtu na kartě **časy**. Pro pochopení tohoto scénáře viz následující pole.

| Flex + | Flex - | Čas  | Placený čas | Neplacená přestávka | Placený přesčas |
|--------|--------|-------|----------|---------------------|--------------|
| 0,50   | 0,00   | 10,50 USD | 9.50     | 0.5                 | 1.50         |

Pokud byla plánovaná přestávka zaplacena a ne nezaplacena, výsledek výpočtu by vypadal takto.

| Flex + | Flex - | Čas  | Placený čas | Placená přestávka | Placený přesčas |
|--------|--------|-------|----------|-----------------|--------------|
| 0,50   | 0,00   | 10,50 USD | 10.00    | 0.5             | 1.50         |

### <a name="pay-items-and-paid-breaks"></a>Placené položky a placené přestávky

Při převodu registrací na stránce **Schválit** jsou vygenerovány položky mzdy. Samostatná mzdová položka je generována pro placené přestávky.

Mzdová sazba pro placenou přestávku je určena typem mzdy, který se nastavuje v mzdové smlouvě pro přestávky. Místo použití typu mzdy můžete nastavit nákladovou cenu na hodinu na přestávku pro definovaný časový interval.

Představte si následující časový profil:

| Typ profilu  | Spuštění    | Konec      | Den     |
|---------------|----------|----------|---------|
| Přesčas     | 00:00 dop. | 06:00 dop. | Pondělí  |
| Flexibilita+         | 06:00 dop. | 07:00 dop. | Pondělí  |
| Registrace příchodu      | 07:00 dop. | 07:00 dop. | Pondělí  |
| Standardní čas | 07:00 dop. | 02:30 odp. | Pondělí  |
| Flexibilita-         | 02:30 odp. | 03:30 odp. | Pondělí  |
| Registrace odchodu     | 03:30 odp. | 03:30 odp. | Pondělí  |
| Přesčas     | 03:30 odp. | 06:00 dop. | Úterý |

V tomto poli jsou registrace pracovníka za daný den.

| Typ registrace deníku | Spuštění    | Konec      | Čas |
|---------------------------|----------|----------|------|
| Registrace příchodu                  | 07:00 dop. | 07:00 dop. |      |
| Výrobní úloha            | 07:00 dop. | 03:00 odp. | 7.5  |
| Přestávka (placená)              | 12:00 odp. | 12:30 odp. | 0.5  |
| Registrace odchodu                 | 03:00 odp. | 03:00 odp. |      |

V tomto příkladu je typ mzdy pro běžný čas nastaven na hodnotu **1201**a mzdová sazba **10** ve smlouvě o platbě. Placená přestávka má typ mzdy **1301** a mzdovou sazbu **8**. Po převodu registrací se vygenerují následující položky platby.

| Typ mzdy     | Typ mzdy | Mzdové jednotky | Kurz |
|---------------|----------|-----------|------|
| Standardní čas | 1201     | 7.50      | 10   |
| Flexibilita-         | 1201     | 0,50      | 10   |
| Přestávka (placená)  | 1301     | 0,50      | 8    |

## <a name="how-the-cost-of-paid-breaks-is-allocated-to-projects-and-production-orders"></a>Jak jsou náklady na placené přestávky přiřazeny k projektům a výrobním objednávkám

Hodinové náklady na aktivity projektu a výrobní úlohy lze nastavit tak, aby byly určeny buď podle mzdových sazeb, které jsou vypočteny v modulu Čas a docházka, nebo podle kategorií nákladů, které jsou definovány pro aktivity.

Chcete-li nastavit nákladovou kategorii, vyberte **Řízení výroby** &gt; **Nastavení** &gt; **Provádění výroby** &gt; **Výchozí nastavení výrobní zakázky**a nastavte pole **Nákladová kategorie** buď na **Ano** nebo **Ne**.

- **Ne** – náklady se vypočítávají na základě mzdových sazeb, které jsou definovány pro typy registrace času a docházky.
- **Ano** – náklady se vypočítávají na základě kategorií nákladů pro aktivity výroby a projektu.

### <a name="cost-calculation-based-on-pay-rates-that-are-calculated-in-time-and-attendance"></a>Výpočet nákladů podle mzdových sazeb, které jsou vypočteny v modulu Čas a docházka

Následující příklad ukazuje výpočet hodinových nákladů za hodinu při nastavení nákladů tak, aby se vypočítaly na základě mzdové sazby.

Hodinová sazba nákladů, používaná pro výrobní zakázky a projekty, se vypočítá během procesu převodu. Chcete-li zobrazit hodinovou sazbu podle aktivity, otevřete stránku **Schválit** v modulu Čas a docházka a poté vyberte **Dotaz** &gt; **Převedené registrace**. Hodinovou nákladovou sazbu podle registrace lze najít na kartě **Nákladové ceny**.

Zvažte následující registrace využívající stejný časový profil jako v předchozím příkladu.

| Typ registrace deníku | Spuštění    | Konec      | Čas |
|---------------------------|----------|----------|------|
| Registrace příchodu                  | 07:00 dop. | 07:00 dop. |      |
| Proces (objednávka: 4711)     | 07:00 dop. | 11:00 dop. | 4    |
| Proces (objednávka: 4712)     | 11:00 dop. | 03:00 odp. | 3.50 |
| Přestávka (placená)              | 12:00 odp. | 12:30 odp. | 0,50 |
| Registrace odchodu                 | 03:00 odp. | 03:00 odp. |      |

Po převodu registrací, dojde ke generování následujících přenesených registrací.

| Typ registrace     | Čas | Nákladová cena za hodinu |
|-----------------------|------|---------------------|
| Označení příchodu              | 0,00 | 0,00                |
| Proces (objednávka: 4711) | 4,00 | 10.00               |
| Proces (objednávka: 4712) | 3.50 | 11.14               |
| Přestávka (placená)          | 0,50 | 0,00                |
| Registrace odchodu             | 0,00 | 0,00                |

Výpočet nákladové ceny za hodinu pro placenou přestávku závisí na nastavení pro přímé mzdové náklady. Vyberte **Čas a docházka** &gt; **Nastavení** &gt; **Parametry času a docházky**. Na kartě **nákladová cena** v části **přímé mzdové náklady**v poli **standardní čas** můžete vybrat **Ano**, **ne** nebo **přidělení**.

- **Ano** – tato hodnota se používá pro předchozí příklad. Náklady jsou přiděleny na výrobu nebo aktivitu projektu, která běží současně s aktivitou placené přestávky. V tomto příkladu je tato aktivita výrobní zakázka pro objednávku 4712. Jak vidíte, nákladová cena za hodinu placené přestávky je 0 (nula) a je přidělena úloze, která se spouští současně s přestávkou.

    Placená přestávka má dobu trvání 0,5 hodiny a mzdová sazba je 8. Celkové náklady placené přestávky jsou tedy 4. Celkové náklady jsou potom přiřazeny k úloze procesu o trvání 3,5 hodiny. Placená přestávka tedy přispívá 1,14 za hodinu k nákladům (4 ÷ 3.5 = 1,14).

- **Přidělení** – placená přestávka rovnoměrně distribuovaná do projektů, které jsou registrovány pro daný den. Pokud se tato hodnota používá pro předchozí příklad, jsou generovány následující přenesené registrace.

    | Typ registrace     | Čas | Nákladová cena za hodinu |
    |-----------------------|------|---------------------|
    | Označení příchodu              | 0,00 | 0,00                |
    | Proces (objednávka: 4711) | 4,00 | 10.53               |
    | Proces (objednávka: 4712) | 3.50 | 10.53               |
    | Přestávka (placená)          | 0,50 | 0,00                |
    | Registrace odchodu             | 0,00 | 0,00                |

    Celkový čas zpracování pro dvě výrobní úlohy je 7,5 hodiny a celkové náklady placené přestávky jsou 4. Proto se náklady přestávky vypočítají jako 0,53 (= 4 ÷ 7,5).

- **Ne** – náklady placené přestávky nezvyšují hodinové náklady aktivit zpracování.

    | Typ registrace     | Čas | Nákladová cena za hodinu |
    |-----------------------|------|---------------------|
    | Označení příchodu              | 0,00 | 0,00                |
    | Proces (objednávka: 4711) | 4,00 | 10.00               |
    | Proces (objednávka: 4712) | 3.50 | 10.00               |
    | Přestávka (placená)          | 0,50 | 0,00                |
    | Registrace odchodu             | 0,00 | 0,00                |

## <a name="absence"></a>Nepřítomnost

Kód absence se používá k registraci období absence pracovníka. Stejné jako přestávky a přepínací kódy je kód absence typ nepřímých aktivit. Čas absence může být plánovaný nebo registrovaný a absence může být legální nebo nelegální. K příkladům legální absence patří návštěva lékaře, semináře nebo plnění soudní povinnosti. Neplatná absence je absence, která nemá žádný důvod, například když pracovník přijde pozdě do práce. Zákonná absence obvykle nezpůsobí srážky ze mzdy pracovníka, zatímco neplatná absence bude mít za následek srážku.

### <a name="planned-absence"></a>Plánovaná absence

Můžete vytvořit plánovanou absenci pro pracovníky na stránce **Vytvořit plánovanou absenci** (**Čas a docházka** &gt; **Vytvořit plánovanou absenci**). Tam se zaregistruje plánovaná absence jako práce absence pro zadané datum a čas intervalu.

Úloha je založena na dotazu. Můžete tedy vytvořit plánovanou absenci u více pracovníků, jako jsou například pracovníci, kteří patří do stejné skupiny výpočtu. Pokud je plánovaná absence pro jednoho zaměstnance, lze zadat registrace ze stránky **Docházka** nebo **Pracovníci s registrací času**.

- Chcete-li zadat registrace absencí ze stránky **Docházka**, vyberte **Čas a docházka** &gt; **Dotazy a sestavy** &gt; **Docházka** &gt; **Docházka**a poté vyberte **Registrace absencí**.
- Chcete-li zadat registrace absencí ze stránky *<strong><em>Pracovníci registrace času</em></strong>*, vyberte <strong>Čas a docházka</strong> &gt; <strong>Nastavení</strong> &gt; <strong>Pracovníci registrace času</strong> a poté na kartě <strong>Čas</strong> pod položkou <strong>Přiřazení času</strong> vyberte <strong>Registrace absencí</strong>.

Můžete použít sestavu **Plánované absence** pro získání přehledu o plánovaných absencích pracovníků. Chcete-li otevřít tuto sestavu, vyberte **Čas a docházka** &gt; **Dotazy a sestavy** &gt; **Sestavy absencí** &gt; **Plánované absence**.

### <a name="registered-absence"></a>Registrovaná absence

Obecně platí, že zaměstnanci jsou považováni za nepřítomné, pokud nejsou v práci pro jakékoli období mezi jejich plánovaným časem příchodu a jejich plánovaným časem odchodu. Pokud se pracovníci přihlásí do práce později, než je plánovaný příchodu nebo odhlásí dříve, než je plánovaný odchod, jsou vyzváni, aby vybrali kód absence k označení důvodu absence. Kód absence můžete nastavit tak, že je platný pro registraci. Pouze platné kódy jsou k dispozici pro výběr v seznamu.

## <a name="scenarios-based-on-various-combinations-of-work-hour-registrations"></a>Scénáře založené na různých kombinacích registrací pracovních hodin

Následující scénáře zobrazují položky mzdy a položky ke schválení, které jsou generovány pro pracovníky podle jejich registrace. Všechny tyto scénáře jsou založeny na následujícím časovém profilu:

| Typ profilu  | Spuštění    | Konec      | Den     |
|---------------|----------|----------|---------|
| Přesčas     | 00:00 dop. | 06:00 dop. | Pondělí  |
| Flexibilita+         | 06:00 dop. | 07:00 dop. | Pondělí  |
| Registrace příchodu      | 07:00 dop. | 07:00 dop. | Pondělí  |
| Standardní čas | 07:00 dop. | 02:30 odp. | Pondělí  |
| Flexibilita-         | 02:30 odp. | 03:30 odp. | Pondělí  |
| Registrace odchodu     | 03:30 odp. | 03:30 odp. | Pondělí  |
| Přesčas     | 03:30 odp. | 06:00 dop. | Úterý |

### <a name="scenario-1-the-worker-clocks-in-later-than-planned"></a>Scénář 1: Pracovník označí příchod později, než bylo plánováno

Pracovník označí příchod v 08:30. Vzhledem k tomu, že jeho plánovaný čas příchodu je 07:00 dopoledne, má 1,50 hodin zpoždění. Vzhledem k tomu, že je 1,50 hodin považováno za čas absence, je pracovník vyzván k výběru kódu absence. Pracovník zanechá práce v 15:30, což je plánovaný čas odchodu. Když jsou registrace pracovníka vypočítány a schváleny, zobrazí se pro čas mezi 07:00 a 08:30 registrace absence, spolu s kódem absence, který pracovník vybral při příchodu.

V časovém profilu lze konfigurovat typ registrace **Příchod** tak, aby existovala tolerance při pozdním příchodu zaměstnanců do práce. Například pokud nastavíte toleranci 5, bude pracovník vyzván k zadání kódu absence pouze v případě, že se přihlásí později než v 07:05 dop.

V takovém případě vzhledem k tomu, že pracovník nemá správný důvod pro pozdní příchod do práce, vybere kód absence, definovaný pro nelegální absenci. Kód absence je považován za platný pro nelegální absenci, pokud nastavení pro srážku přesčasu je povoleno pro skupinu absencí, do níž náleží kód absence. Pro toto nastavení vyberte **Čas a docházka** &gt; **Nastavení** &gt; **Skupiny** &gt; **Skupiny absencí**a vyberte zaškrtávací políčko **Odečíst přesčas**.

V tomto poli se zobrazují registrace pracovníka pro daný den na stránce **Schválit** po výpočtu.

| Typ registrace deníku         | Spuštění    | Konec      | Čas |
|-----------------------------------|----------|----------|------|
| Absence (nelegální - pozdě v práci) | 07:00 dop. | 08:30 dop. | 1.5  |
| Registrace příchodu                          | 08:30 dop. | 08:30 dop. |      |
| Výrobní úloha                    | 07:30 dop. | 03:30 odp. | 7.0  |
| Registrace odchodu                         | 03:30 odp. | 03:30 odp. |      |

V tomto poli je výsledná položka mzdy po převodu registrací.

| Typ mzdy     | Typ mzdy | Mzdové jednotky | Kurz |
|---------------|----------|-----------|------|
| Standardní čas | 1201     | 7:00      | 10   |

### <a name="scenario-2-the-worker-clocks-out-before-the-planned-clock-out-time-during-a-standard-time-period"></a>Scénář 2: Pracovník označí odchod před plánovaným časem odchodu během standardní pracovní doby

Pracovník označí čas příchodu v 7:00 a čas odchodu předčasně v 13:00. Vzhledem k tomu, že 01:00 odpoledne předchází plánovanému odchodu ve 3:00 odp. a 01:00 dop. je standardní časové období, je pracovník vyzván k výběru kódu absence. Pracovník vybere kód absence pro návštěvu lékaře, což je definováno jako platná absence. Mzdová sazba pro oprávněnou basenci je definována v mzdových smlouvách pro typ registrace **Absence** (**Čas a docházka** &gt; **Nastavení** &gt; **Mzda** &gt; **Mzdové smlouvy**).

V tomto poli se zobrazují registrace pracovníka pro daný den na stránce **Schválit** po výpočtu.

| Typ registrace deníku              | Spuštění    | Konec      | Čas |
|----------------------------------------|----------|----------|------|
| Registrace příchodu                               | 07:00 dop. | 07:00 dop. |      |
| Výrobní úloha                         | 07:00 dop. | 01:00 odp. | 4.0  |
| Registrace odchodu                              | 01:00 odp. | 01:00 odp. |      |
| Absence (právní – návštěva lékaře) | 01:00 odp. | 03:30 odp. | 3.5  |

V tomto poli je výsledná položka mzdy po převodu registrací.

| Typ mzdy     | Typ mzdy | Mzdové jednotky | Kurz |
|---------------|----------|-----------|------|
| Standardní čas | 1201     | 7.50      | 10   |

### <a name="scenario-3-the-worker-clocks-out-before-the-planned-clock-out-time-during-a-flex--period"></a>Scénář 3: Pracovník označí odchod před plánovaným časem odchodu během pružné pracovní doby (Flex-)

Pracovník označí příchod v 07:00 a odchod v 14:15, což je plánovaná pružná pracovní doba Flex-. Čas mezi skutečným časem odchodu a plánovaným časem odchodu není považován za absenci, a pracovník není vyzván k volbě kódu absence. Částka se odečte z účtu pružné pracovní doby pracovníka a pracovník má nárok na mzdu během zbývající části pružné pracovní doby Flex- od 14:15 do 15:30.

V tomto poli se zobrazují registrace pracovníka pro daný den na stránce **Schválit** po výpočtu.

| Typ registrace deníku | Spuštění    | Konec      | Čas |
|---------------------------|----------|----------|------|
| Registrace příchodu                  | 07:00 dop. | 07:00 dop. |      |
| Výrobní úloha            | 07:00 dop. | 02:15 odp. | 7.25 |
| Registrace odchodu                 | 02:15 odp. | 02:15 odp. |      |

V tomto poli je výsledná položka mzdy po převodu registrací.

| Typ mzdy     | Typ mzdy | Mzdové jednotky | Kurz |
|---------------|----------|-----------|------|
| Standardní čas | 1201     | 8.50      | 10   |

### <a name="scenario-4-the-worker-clocks-in-late-and-clocks-out-after-the-planned-clock-out-time-during-an-overtime-period"></a>Scénář 4: Pracovník označí přichod pozdě a odchod po plánovaném čase odchodu během přesčasové doby

Pracovník označí pozdní příchod v 09:30 a pak, aby vykompenzoval svůj pozdní příchod, pracuje přesčas a označí odchod v 17:00. Vzhledem k tomu, že pracovník přišel pozdě a dostal zaplaceno za delší práci, společnost nechce udělit pracovníkovi platbu za přesčas pro hodiny, které odpracoval mezi plánovaným odchodem v 03:30 odp. a jeho skutečným odepsáním odchodu v 05:00 odpoledne, i v případě, že toto období je definováno jako přesčas v časovém profilu.

Chcete-li zpracovat tento scénář, lze nastavit kód absence pro snížení přesčasovéých hodin o hodiny neplatné absence, které má pracovník tentýž den. Vyberte **Čas a docházka** &gt; **Nastavení** &gt; **Skupiny** &gt; **Skupiny absencí**a vyberte zaškrtávací políčko **Odečíst přesčas** pro odečtení přesčasu od hodin neplatné absence.

V tomto poli se zobrazují registrace pracovníka pro daný den na stránce **Schválit** po výpočtu.

| Typ registrace deníku         | Spuštění    | Konec      | Čas |
|-----------------------------------|----------|----------|------|
| Absence (nelegální - pozdě v práci) | 07:00 dop. | 09:30 dop. | 1.5  |
| Registrace příchodu                          | 09:30 dop. | 09:30 dop. |      |
| Výrobní úloha                    | 09:30 dop. | 05:00 odp. | 7.5  |
| Registrace odchodu                         | 05:30 odp. | 05:30 odp. |      |

Pokud je zaškrtnuto políčko **Odečíst přesčas** pro vybraný kód absence, je platba za přesčas odečtena podle hodin, kdy měl pracovník nelegálně přesčas. V tomto případě jsou po generování platebních položek převedeny následující položky platby.

| Typ mzdy     | Typ mzdy | Mzdové jednotky | Kurz |
|---------------|----------|-----------|------|
| Standardní čas | 1201     | 9:00      | 10   |
| Přesčas      | 1301     | 0.5       | 15   |

Od 1,5 hodin nelegální absence v době z 07:00 do 09:30 hodin ráno se odečte 2,0 hodin přesčasu z 03:30 odpoledne do 05:30 hodin odpoledne. Výsledek registrace je 1,5 hodiny standardního času a 0,5 hodiny přesčasu.

Naopak pokud není zaškrtnuto zaškrtávací políčko **Odečíst přesčas** pro vybraný kód absence, proplácení přesčasů je uděleno pracovníkovi, i když přišel pozdě a měl nelegální absenci. V tomto případě jsou po generování platebních položek převedeny následující položky platby.

| Typ mzdy     | Typ mzdy | Mzdové jednotky | Kurz |
|---------------|----------|-----------|------|
| Standardní čas | 1201     | 7.50      | 10   |
| Přesčas      | 1301     | 2.0       | 15   |

### <a name="scenario-5-the-worker-clocks-out-before-the-planned-clock-out-time-and-can-convert-the-absence-period-to-a-flex--period"></a>Scénář 5: Pracovník označí odchod před plánovaný časem odchodu a může převést dobu absence do pružné pracovní doby (Flex-)

Následující příklad ukazuje, jak lze snížit účet pružné pracovní doby pracovníka převodem doby absence na dobu Flex-.

Pracovník označí čas příchodu v 7:00 a čas odchodu v 13:00. Dohodla se se svým vedoucím, že může jít domů na víkend, pokud odečte tyto hodiny ze svého účtu pružné pracovní doby. Když pracovník označí odchod v 13:00, bude vyzván k výběru kódu absence, protože doba absence pro zbývající část pracovního dne, která je ovlivněna, není plánovanou pružnou pracovní dobou Flex-. Pokud chcete převést zbývající část pracovního dne na pružnou pracovní dobu Flex-, pracovník může vybrat kód absence, nastavený ke snížení účtu pružné pracovní doby.

Chcete-li snížit zůstatek pružné pracovní doby pro pracovníky, kteří budou registrovat absenci v pracovní den, vyberte **Čas a docházka** &gt; **Nastavení** &gt; **Skupiny** &gt; **Skupiny absencí** a zvolte zaškrtávací políčko **Snížit pružnou pracovní dobu**.

V tomto poli se zobrazují registrace pracovníka pro daný den na stránce **Schválit** před výpočtem.

| Typ registrace deníku | Spuštění    | Konec      | Čas |
|---------------------------|----------|----------|------|
| Registrace příchodu                  | 07:00 dop. | 07:00 dop. |      |
| Výrobní úloha            | 07:00 dop. | 01:00 odp. | 6.0  |
| Registrace odchodu                 | 01:00 odp. | 01:00 odp. |      |

Pracovník vybere kód absence neplatné absence. Tady je, jak bude vypadat výsledná položka mzdy po převodu registrace.

| Typ mzdy     | Typ mzdy | Mzdové jednotky | Kurz |
|---------------|----------|-----------|------|
| Standardní čas | 1201     | 6,00      | 10   |

Jestli pracovník vybere kód absence pro zákonnou absenci a kód absence je nastaven na redukci účtu pružné pracovní doby, bude výsledná položka mzdy po převodu registrací vypadat následovně.

| Typ mzdy     | Typ mzdy | Mzdové jednotky | Kurz |
|---------------|----------|-----------|------|
| Standardní čas | 1201     | 8.50      | 10   |

V takovém případě je pružný zůstatek snížen o počet hodin mezi skutečným časem odchodu a plánovaným časem odchodu (to znamená 2,5 hodiny od 01:00 odpoledne do 03:30 odp.).

> [!NOTE]
> Nedoporučujeme vybrat obě zaškrtávací políčka **Odečíst pružnou pracovní dobu** a **Odečíst přesčas** pro kód absence, vzhledem k tomu, že toto nastavení bude odečítat neplatné hodiny z přesčasu pracovníka a současně sníží účet pružné pracovní doby zaměstnance.

### <a name="scenario-6-there-is-no-planned-absence-for-the-day-and-no-worker-attendance-for-the-day"></a>Scénář 6: Není žádná plánovaná absence pro daný den a žádná docházka pracovníka pro tento den

Pokud se pracovník nedostaví na práci v pracovní den a nemá na ten den plánovanou absenci, použije se výchozí kód absence pro výpočet registrací pracovníka. Chceteli definovat výchozí kódy absencí, zvolte **Čas a docházky** &gt; **Parametry času a docházky**. Lze pak vybrat kód absence v následujících polích:

- Automaticky vložit flex-
- Automaticky vložit absenci

Při výpočtu denních registrací pro pracovníka, který má oprávnění k pružné pracovní době, se použije jako kód absence kód, který je určený v poli **Automaticky vložit flex-**. Pokud pracovník není aktivován pro pružnou pracovní dobu, bude použit kód absence zadaný v poli **Automaticky vložit absenci**. Pokud má společnost kombinaci pracovníků, kteří mají povolenu pružnou pracovní dobu, a pracovníky, kteří nemají povolenu pružnou pracovní dobu, musíte nastavit oba parametry.

