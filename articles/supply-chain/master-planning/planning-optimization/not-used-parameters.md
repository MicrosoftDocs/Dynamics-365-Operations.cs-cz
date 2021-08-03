---
title: Parametry, které optimalizace plánování nepoužívá
description: V tomto tématu jsou uvedeny parametry, které optimalizace plánování aktuálně během provozu nezvažuje.
author: crytt
ms.date: 6/29/2021
ms.topic: article
ms.search.form: ReqParameters, ReqGroup, ReqItemTable, ReqPlanSched, EcoResProductDetailsExtended, InventItemOrderSetup, WorkCalendarTable, PdsDispositionMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-29
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4d459f4de67f26f36aabcbde015988132e957601
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361326"
---
# <a name="parameters-not-used-by-planning-optimization"></a>Parametry, které optimalizace plánování nepoužívá

[!include [banner](../../includes/banner.md)]

V tomto tématu jsou uvedeny parametry, které optimalizace plánování aktuálně během provozu nezvažuje. Služba plánování může přeskočit parametr, protože například související funkce ještě nejsou podporovány. Alternativně může být parametr zastaralý kvůli funkčním změnám.

V následujících částech je uveden seznam parametrů, které optimalizace plánování nepoužívá na konkrétních stránkách. Vysvětlují také, proč se každý parametr nepoužívá.

## <a name="master-planning-parameters-page"></a>Stránka s parametry hlavního plánování

Optimalizace plánování nepoužívá následující parametry nebo možnosti na stránce **Hlavní plánovací parametry**:

- Karta **Obecné**:

    - **Aktuální plán předpovědi** – Čekající podpora *Předpověď*.
    - **Aktuální statický hlavní plán** – Čekající podpora *Zkopírovat statický do dynamického plánu*.
    - **Aktuální dynamický hlavní plán** – Čekající podpora *Zkopírovat statický do dynamického plánu*.
    - **Kopírovat kompletní a aktualizovaný statický hlavní plán do dynamického hlavního plánu** – Čekající podpora *Zkopírujte statický do dynamického plánu*.
    - **Počáteční čas pro vypočítané zpoždění** – Čekající podpora *Vypočítané zpoždění*.
    - **Použít dynamické negativní dny** – Optimalizace plánování vždy používá přístup *Dynamické negativní dny*.
    - **Dnešní kalendář** – Čekající podpora *Plánování*.
    - **Použití mezipaměti** – Konfigurace předplatného Microsoft Azure zpracovává body výkonu.
    - **Počet úkolů ve svazku pomocných úkolů** – Konfigurace předplatného Azure zpracovává body výkonu.
    - **Předběžné zpracování: Automatické filtrování podle položek s přímým požadavkem** – Konfigurace předplatného Azure zpracovává body výkonu.
    - **Následné zpracování: Automatické filtrování podle položek s přímým požadavkem** – Konfigurace předplatného Azure zpracovává body výkonu.
    - **Počet objednávek ve svazku potvrzení** – Konfigurace předplatného Azure zpracovává body výkonu.
    - **Počet vláken** – Konfigurace předplatného Azure zpracovává body výkonu.
    - **Vypršení časového limitu procesu plánování v minutách** – Konfigurace předplatného Azure zpracovává body výkonu.
    - **Čas zahájení plánování** - Čekající podpora *Plánování*.

- Karta **Plánované objednávky**:

    - **Čas přijetí** – Čekající podpora *Plánování*.
    - **Produkce** – Čekající podpora *Plánování*.
    - Pole v části **Projekt** – čekající podpora *Plánování*.

- Karta **Standardní aktualizace**:

    - **Aktualizovat označení** – Čekající podpora *Potvrzení*.
    - **Pokud dojde k chybě, zastavit potvrzování** – Čekající podpora *Potvrzování*.
    - **Seskupit podle dodavatele** – Čekající podpora *Potvrzování*.
    - **Seskupit podle skupiny kupujícího** – Čekající podpora *Potvrzování*.
    - **Seskupit podle nákupní smlouvy** – Čekající podpora *Potvrzování*.
    - **Seskupit podle období** – Čekající podpora *Potvrzování*.
    - **Vyhledat nákupní smlouvu** – Čekající podpora *Potvrzování*.
    - **Seskupit podle priority plánování** – Čekající podpora *Potvrzování*.
    - **Seskupit podle období** – Čekající podpora *Potvrzování*.

## <a name="coverage-groups-page"></a>Stránka skupin disponibility

Optimalizace plánování nepoužívá následující parametry nebo možnosti na stránce **Skupiny disponibility**:

- Pevná záložka **Obecné**:

    - **Pozitivní dny** – Čekající podpora *Pozitivní dny*.
    - **Spotřebovat zásob na skladě** – Čekající podpora *Spotřeba zásob na skladě*.
    - **Použijte zadaný kusovník nebo verzi vzorce** – Čekající podpora *Verze receptury s vedlejším/souběžným produktem*.
    - **Použijte zadanou verzi trasy** – Čekající podpora *Poptávka se specifickými požadavky na kusovník nebo trasu*.

- Pevná záložka **Akce**:

    - **Akční zpráva** – Čekající podpora *Akce*.
    - **Ochranná doba akce** – Čekající podpora *Akce*.
    - **Odložit marži** – Čekající podpora *Akce*.
    - **Marže předem** – Čekající podpora *Akce*.
    - **Základní datum** – Čekající podpora *Akce*.
    - **Předem** – Čekající podpora *Akce*.
    - **Odložit** – Čekající podpora *Akce*.
    - **Snížit** – Čekající podpora *Akce*.
    - **Zvýšit** – Čekající podpora *Akce*.
    - **Odvozené akce** – Čekající podpora *Akce*.

- Pevná záložka **Jiný**:

    - **Ochranná doba zablokování (dny)** – Podpora *Ochranná doba zablokování* není plánována v optimalizaci plánování.
    - **Ochranná doba rozbalení kusovníku (dny)** - Čekající podpora *Plánování*.
    - **Ochranná doba plánování kapacity (dny)** - Čekající podpora *Plánování*.
    - **Ochranná doba schváleného nákupu (dny)** – Čekající podpora *Požadavek*.
    - **Ochranná doba plánování předpovědi** – Čekající podpora *Předpověď*.

- Pevná záložka **Zpoždění**:

    - **Vypočítaná zpoždění** – Čekající podpora *Vypočítané zpoždění*.
    - **Ochranná doba vypočítaného zpoždění (dny)** – Čekající podpora *Vypočítané zpoždění*.

## <a name="item-coverage-page"></a>Stránka Disponibilita položky

Optimalizace plánování nepoužívá následující parametry nebo možnosti na stránce **Disponibilita položky**:

- Karta **Obecné**:

    - **Plánovaný typ objednávky** – Optimalizace plánování nepodporuje možnost *Kanban*, čekající podpora *Kanban*.
    - **Ochranná doba zablokování (dny)** – Podpora *Ochranná doba zablokování* není plánována v optimalizaci plánování.
    - **Ochranná doba rozbalení kusovníku (dny)** - Čekající podpora *Plánování*.
    - **Ochranná doba plánování kapacity (dny)** - Čekající podpora *Plánování*.
    - **Ochranná doba schváleného nákupu (dny)** – Čekající podpora *Požadavek*.
    - **Minimum plnění** – Optimalizace plánování nepodporuje možnosti *Dnešní datum*, *První vydání* a *Ochranná doba disponibility*. Vždy používá možnost *Dnešní datum a čas pořízení*.
    - **Minimální období** – Čekající podpora *Minimální úroveň zásob*.
    - **Plánovací receptura** – Čekající podpora *Verze receptury se souběžnými/vedlejšími produkty*.
    - **Výchozí priorita** – Čekající podpora *Verze receptury se souběžnými/vedlejšími produkty*.
    - **Aktuální priorita** – Čekající podpora *Verze receptury se souběžnými/vedlejšími produkty*.
    - **Datum změněno** – Čekající podpora *Verze receptury se souběžnými/vedlejšími produkty*.
    - **Spotřebovat zásob na skladě** – Čekající podpora *Spotřeba zásob na skladě*.

## <a name="master-plans-page"></a>Stránka Hlavní plány

Optimalizace plánování nepoužívá následující parametry nebo možnosti na stránce **Hlavní plány**:

- Pevná záložka **Obecné**:

    - **Zahrnout zásoby na skladě** – Čekající podpora *Spotřeba zásob na skladě*.
    - **Přepsat na skladě** – Čekající podpora *Spotřeba zásob na skladě*.
    - **Spotřebovat zásob na skladě** – Čekající podpora *Spotřeba zásob na skladě*.
    - **Zahrnout transakce zásob** – Čekající podpora *Spotřeba zásob na skladě*.
    - **Zahrnout prodejní nabídky** – Čekající podpora *Prodejní nabídky*.
    - **Zahrnout požadavky na nabídku** – Čekající podpora *Požadavky na nabídku*.
    - **Použít data trvanlivosti** – Čekající podpora *Skladovatelnost*.
    - **Zahrnout plán kontinuity** – Čekající podpora *Plánování kontinuity*.
    - **Metoda plánování** – Čekající podpora *Plánování*.
    - **Konečná vlastnost** – Čekající podpora *Plánování*.
    - **Ochranná doba zpětného plánování kapacity** – Čekající podpora *Plánování*.
    - **Konečná kapacita** – Čekající podpora *Plánování*.
    - **Ochrann doba konečné kapacity** – Čekající podpora *Plánování*.
    - **Konečná kapacita pro úzká místa zdrojů** – Čekající podpora *Plánování*.
    - **Ochranná doba kapacity pro úzká místa zdrojů** – Čekající podpora *Plánování*.
    - **Plánované objednávky** – Optimalizace plánování používá pevné číselné řady.
    - **Relace** – Optimalizace plánování používá pevné číselné řady.
    - **Plán kontinuity** – Optimalizace plánování používá pevné číselné řady.

- Pevná záložka **Ochranné doby ve dnech**:

    - **Ochranná doba** – Podpora *Ochranná doba zablokování* není plánována v optimalizaci plánování.
    - **Rozbalení** – Čekající podpora *Plánování*.
    - **Plán předpovědi** – Čekající další podpora *Předpověď*.
    - **Kapacita** – Čekající podpora *Plánování*.
    - **Plán kontinuity** – Čekající podpora *Plánování kontinuity*.
    - **Akční zpráva** – Čekající podpora *Akce*.
    - **Vypočítaná zpoždění** – Čekající další podpora *Vypočítané zpoždění*.
    - **Pořadí** – Čekající podpora *Produkce*.

- Pevná záložka **Vypočítaná zpoždění**:

    - **Zajistit, aby plánované objednávky nebyly vytvořeny před datem spuštění hlavního plánování** – Čekající podpora *Vypočítané zpoždění*.
    - **Přidat vypočítané zpoždění k datu požadavku** (v části **Plánované nákupní objednávky**) – čekající podpora *Vypočítané zpoždění*.
    - **Přidat vypočítané zpoždění k datu požadavku** (v části **Plánované výrobní zakázky**) – čekající podpora *Vypočítané zpoždění*.
    - **Přidat vypočítané zpoždění k datu požadavku** (v části **Plánovaný převod**) – čekající podpora *Vypočítané zpoždění*.
    - **Přidat vypočítané zpoždění k datu požadavku** (v části **Plánovaný kanban**) – čekající podpora *Vypočítané zpoždění*.

- Pevná záložka **Pořadí**:

    - **Pořadí plánovaných objednávek po hlavním plánování** – Čekající podpora *Pořadí*.
    - **Typ kontejneru** – Čekající podpora *Pořadí*.
    - **Typ období** – Čekající podpora *Pořadí*.
    - **Počet kontejnerů v cyklu kampaně** – Čekající podpora *Pořadí*.

## <a name="released-product-details-page"></a>Stránka podrobností o uvolněném produktu

Optimalizace plánování nepoužívá následující možnost parametru na stránce **Údaje o vydaném produktu**:

- Pevná záložka **Technik**:

    - **Typ výroby** – Optimalizace plánování nepodporuje možnost *Položka plánování*, čekající podpora *Položky plánování*.

## <a name="default-order-settings-page"></a>Stránka Výchozí nastavení objednávky

Optimalizace plánování nepoužívá následující možnost parametru na stránce **Nastavení výchozího pořadí**:

- Pevná záložka **Zásoby**:

    - **Řízení data dodání** – Optimalizace plánování nepodporuje možnost *CTP*, čekající podpora *CTP*.

## <a name="working-time-calendars-page"></a>Stránka Kalendáře pracovní doby

Optimalizace plánování nepoužívá následující parametr na stránce **Kalendáře pracovní doby**:

- **Základní kalendář** – Čekající podpora *Základní kalendáře*.

## <a name="batch-disposition-master-page"></a>Stránka Vzor dispozice dávky

Optimalizace plánování nepoužívá následující parametr na stránce **Vzor dispozice dávky**:

- Pevná záložka **Nastavení**:

    - **Možnost čisté hodnoty** – Čekající podpora *Dávkové dispoziční kódy*.