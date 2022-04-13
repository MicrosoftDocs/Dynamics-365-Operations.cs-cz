---
title: Parametry data a času, které používá optimalizace plánování
description: Toto téma poskytuje informace o parametrech data a času, které optimalizace plánování používá během své činnosti.
author: t-benebo
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0708404f286253449e0400fc65680e903f6d1e9b
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468825"
---
# <a name="date-and-time-parameters-used-by-planning-optimization"></a>Parametry data a času, které používá optimalizace plánování

[!include [banner](../../includes/banner.md)]

Toto téma poskytuje informace o parametrech data a času, které optimalizace plánování používá během své činnosti.

Zatímco vestavěný modul hlavního plánování používá data transakcí ve všech výpočtech, optimalizace plánování pracuje s hodnotami data a času, které jsou převedeny na data. Tento rozdíl v chování může vést k situacím, kdy například prognózované transakce, které jsou vytvořeny o půlnoci dne, kdy je spuštěno hlavní plánování, nejsou zahrnuty, protože optimalizace plánování se domnívá, že byly vytvořeny před aktuálním datem.

## <a name="parameters-for-issue-and-demand-transactions"></a>Parametry pro výdejní a poptávkové transakce

V následující tabulce jsou uvedeny parametry, které nástroj optimalizace plánování používá při zpracování transakcí výdeje a poptávky.

| Parametr | Název parametru v optimalizaci plánování | Popis | Ekvivalentní pole v Microsoft Dynamics 365 Supply Chain Management (v tabulce ReqTrans) |
|---|---|---|---|
| Plánovaný čas vydání | `PlannedIssueTime` | Datum, na které má být vydání aktuálně plánováno. | **K datu** (`FuturesDate`) a **Zpožděno na čas** (`FuturesTime`) |
| Požadovaný čas vydání | `RequestedIssueTime` | Datum vydání požadovaný uživatelem a nastavený v Supply Chain Management. Tento parametr je použitelný pouze pro uvolněné nebo schválené plánované objednávky. U plánovaných objednávek je ve výchozím nastavení prázdné. | **Požadované datum** (`ReqDateDlvOrig`) |
| Požadovaný čas vydání | `RequiredIssueTime` | Požadované datum vydání, které je upraveno optimalizací plánování. Pokud je požadovaný čas vydání při spuštění optimalizace plánování v minulosti, bude požadovaný čas vydání upraven na první den otevření, který není dřívější než dnešní datum. Pokud je požadovaný čas vydání označen v kalendáři jako blokovaný, bude požadovaný čas vydání upraven na první den otevření před tímto datem. | **Datum požadavku** (`ReqDate`) a **Doba požadavku** (`ReqTime`) |
| Časová prodleva vydání | `IssueTimeDelay` | Časový rozdíl mezi plánovaným časem vystavení a buď požadovaným časem vystavení pro schválené a uvolněné objednávky, nebo požadovaným časem vystavení. | **Zpoždění (ve dnech)** (`FuturesDays`) |

## <a name="parameters-for-receipt-and-supply-transactions"></a>Parametry pro transakce příjmu a dodávek

V následující tabulce jsou uvedeny parametry, které nástroj optimalizace plánování používá při zpracování transakcí příjmu a dodání.

| Parametr | Název parametru v optimalizaci plánování | Popis | Ekvivalentní pole v Supply Chain Management (v tabulce ReqTrans nebo ReqPO) |
|---|---|---|---|
| Plánovaná doba dostupnosti | `PlannedAvailabilityTime` | Plánované datum dostupnosti příjmu. | **Datum požadavku** (`ReqDate`) a **Doba požadavku** (`ReqTime`) |
| Plánovaný čas příjmu | `PlannedReceiptTime` | Datum, kdy příjem dorazí na místo. | **K datu** (`FuturesDate`), **Zpožděno k času** (`FuturesTime`) a **Datum doručení** (`ReqDateDlv`) nebo **Požadované datum** (`ReqDateDlvOrig`), pokud objednávka ještě není uvolněna. |
| Požadovaný čas dostupnosti | `RequiredAvailabilityTime` | Požadované datum dostupnosti, které je upraveno optimalizací plánování. | **Datum požadavku** (`ReqDate`) a **Doba požadavku** (`ReqTime`) |
| Očekávaný čas příjmu | `ExpectedReceiptTime` | Očekávané datum příjmu pro uvolněný příjem. Hodnotu nastavuje uživatel v Supply Chain Management a neupravuje ji optimalizace plánování. Tento parametr platí pouze pro uvolněné příjmy. | **Požadované datum** (`ReqDateDlvOrig`) |
| Požadovaný čas příjmu | `RequiredReceiptTime` | Požadované datum příjmu, které je upraveno optimalizací plánování. | **Datum požadavku** (`ReqDate`) a **Doba požadavku** (`ReqTime`) |
| Plánovaný čas objednání | `PlannedOrderingTime` | Datum objednání, které je vypočítáno optimalizací plánování. | **Datum objednávky** (`ReqDateOrder`) a **Čas objednávky** (`ReqTimeOrder`) |
| Plánovaný čas zahájení aktivity | `PlannedActivityStartTime` | Datum, kdy má začít činnost pro tuto účtenku. | **Počáteční datum** (`SchedFromDate`) |
| Časové zpoždění příjmu | `ReceiptTimeDelay` | Časový rozdíl mezi plánovaným časem příjmu a požadovaným časem příjmu. | **Zpoždění (dny)** (`FuturesDays`) a **Zpožděno do času** (`FuturesTime`) |

## <a name="examples-of-date-parameter-use-by-planning-optimization"></a>Příklady použití parametru data optimalizací plánování

Plány na následujících ilustracích jsou na úrovni dne, ale optimalizace plánování je spuštěna na podrobnější úrovni. Například protože marže mohou být v hodinách, plánovací čas objednání může být 22. ledna 2021, v 11.35 a tak dále.

### <a name="example-1-simple-scenario"></a>Příklad 1: Jednoduchý scénář

Jedna prodejní objednávka, která má požadovaný čas vystavení 22. ledna, je pokryta jednou nákupní objednávkou. Požijí se následující nastavení:

- Žádná doba realizace
- Žádné kalendáře (všechny dny jsou otevřené.)
- Žádné marže

Následující obrázek znázorňuje tento scénář. (Výběrem obrázku otevřete větší verzi.)

[![Jednoduchý scénář.](media/planning-service-dates-1-small.png)](media/planning-service-dates-1.png)

### <a name="example-2-lead-time-scenario"></a>Příklad 2: Scénář doby realizace

Jedna prodejní objednávka, která má požadovaný čas vystavení 22. ledna, je pokryta jednou nákupní objednávkou. Požijí se následující nastavení:

- Tři dny doby realizace
- Žádné kalendáře (všechny dny jsou otevřené.)
- Žádné marže

Následující obrázek znázorňuje tento scénář. (Výběrem obrázku otevřete větší verzi.)

[![Scénář doby realizace.](media/planning-service-dates-2-small.png)](media/planning-service-dates-2.png)

### <a name="example-3-margin-scenario"></a>Příklad 3: Scénář marže

Jedna prodejní objednávka, která má požadovaný čas vystavení 22. ledna, je pokryta jednou nákupní objednávkou. Požijí se následující nastavení:

- Tři dny doby realizace
- Čtyřdenní objednávková marže
- Pětidenní marže dostupnosti
- Žádné kalendáře (všechny dny jsou otevřené.)

Následující obrázek znázorňuje tento scénář. (Výběrem obrázku otevřete větší verzi.)

[![Maržový scénář.](media/planning-service-dates-3-small.png)](media/planning-service-dates-3.png)

### <a name="example-4-delay-scenario"></a>Příklad 4: Scénář zpoždění

Jedna prodejní objednávka, která má požadovaný čas vystavení 22. ledna, je pokryta jednou nákupní objednávkou. Tento příklad používá stejné nastavení jako příklad 3, ale datum plánování bylo přesunuto na 15. ledna. Zpětné plánování (červené značky) se nezdaří, protože plánovaný čas objednávky by musel být před dnešním datem. Proto musí hlavní plánování naplánovat do budoucna a dochází ke zpožděním.

Následující obrázek znázorňuje tento scénář. (Výběrem obrázku otevřete větší verzi.)

[![Scénář zpoždění.](media/planning-service-dates-4-small.png)](media/planning-service-dates-4.png)

### <a name="example-5-transfer-scenario"></a>Příklad 5: Scénář převodu

Jedna prodejní objednávka ze skladu 1, která má požadovaný čas vydání 22. ledna, je pokryta jednou převodní objednávkou ze skladu 2, která je pokryta plánovanou nákupní objednávkou. Požijí se následující nastavení:

- Tři dny doby realizace převodu (sklad 1)
- Dva dny doby realizace nákupu (sklad 2)
- Žádné kalendáře (všechny dny jsou otevřené.)

Následující obrázek znázorňuje tento scénář. (Výběrem obrázku otevřete větší verzi.)

[![Scénář převodu.](media/planning-service-dates-5-small.png)](media/planning-service-dates-5.png)

### <a name="example-6-lead-time-with-calendars-scenario"></a>Příklad 6: Scénář doby realizace s kalendáři

Jedna prodejní objednávka, která má požadovaný čas vystavení 22. ledna, je pokryta jednou nákupní objednávkou. Požijí se následující nastavení:

- Tři dny doby realizace
- Kalendář vydávání (v pátek zavřeno)
- Kalendář dostupnosti (ve čtvrtek a pátek zavřeno)
- Kalendář příjmu (v úterý, středu a neděli zavřeno)
- Kalendář doby realizace (ve čtvrtek a pátek zavřeno)
- Objednávkový kalendář (otevřeno v pondělí a sobotu)

Následující obrázek znázorňuje tento scénář. (Výběrem obrázku otevřete větší verzi.)

[![Scénář doby realizace s kalendáři.](media/planning-service-dates-6-small.png)](media/planning-service-dates-6.png)

### <a name="example-7-delay-with-calendars-scenario"></a>Příklad 7: Scénář zpoždění s kalendáři

Jedna prodejní objednávka, která má požadovaný čas vystavení 22. ledna, je pokryta jednou nákupní objednávkou. Tento příklad používá stejné nastavení jako příklad 6, ale datum plánování bylo přesunuto na 13. ledna. Zpětné plánování (červené značky) se nezdaří, protože plánovaný čas objednávky by musel být před dnešním datem. Proto musí hlavní plánování naplánovat do budoucna a dochází ke zpožděním.

Následující obrázek znázorňuje tento scénář. (Výběrem obrázku otevřete větší verzi.)

[![Scénář zpoždění s kalendáři.](media/planning-service-dates-7-small.png)](media/planning-service-dates-7.png)
