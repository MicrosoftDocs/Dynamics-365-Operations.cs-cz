---
title: Zpoždění
description: Toto téma obsahuje informace o zpožděných datech v hlavním plánování. Zpožděné datum je realistické datum splatnosti přidělené transakci, pokud je nejbližší datum plnění vypočítané hlavním plánováním pozdější než požadované datum.
author: roxanadiaconu
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da09d670fd952d885f013693b6362cf9002343ff
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424058"
---
# <a name="delays"></a>Zpoždění

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace o zpožděných datech v hlavním plánování. Zpožděné datum je realistické datum splatnosti přidělené transakci, pokud je nejbližší datum plnění vypočítané hlavním plánováním pozdější než požadované datum.

Hlavní plánování dokáže vypočítat nejbližší datum plnění transakce na základě doby realizace, dostupnosti materiálu, dostupné kapacity a různých parametrů plánování. 

Pokud hlavní plánování vypočítá datum objednávky, které předchází dnešnímu datu, objednávku nelze splnit včas. Objednávka je proto zpožděná. V takovém případě hlavní plánování objednávku naplánuje dopředně od dnešního data a zahrne doby realizace. Tyto realizace časy zahájení kteroukoliv položkou součásti na nižší úrovni. Objednávce se pak přiřadí datum zpoždění. Datum zpoždění je realistické datum dodání stanovené podle aktuálního data. Hlavní plánování vypočte také počet dnů zpoždění. 

V některých situacích může být vhodnější zpoždění nevypočítávat, například pokud uživatelé vědí, že lze dobu realizace urychlit výběrem alternativních způsobů dodání. 

Způsob výpočtu zpoždění pro skupinu disponibility lze upravit. Skupinu disponibility můžete k položce přiřadit později. 

Na stránce **Parametry hlavního plánování** můžete nastavit čas zahájení výpočtu zpoždění. Pokud je objednávka splněna po tomto termínu, k datu zpoždění objednávky se přičte jeden den. 

> [!NOTE]
> V předchozích verzích se vypočtená zpoždění nazývala *termínové zprávy*, datum zpoždění se nazývalo *datum termínu* a zpožděná transakce se označovala jako *transakce nastavená na budoucí datum*.

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a>Omezené zpoždění při nastavení výroby s více úrovněmi kusovníku
Pokud pracujete se zpožděními v nastavení výroby, které má více úrovní kusovníku, je důležité poznamenat, že pouze položky, které způsobují zpoždění, přímo nad položkou (ve struktuře kusovníku), budou při spuštění hlavního plánování aktualizovány s prodlením. Ostatní položky ve struktuře kusovníku nebudou při schválení nebo potvrzení plánované objednávky pro nejvyšší úroveň použity zpoždění použité do prvního hlavního plánování. 

Chcete-li toto známé omezení obejít, je možné schválit výrobní zakázky na vrcholu struktury kusovníku se zpožděními (nebo pevně) před dalším spuštěním hlavního plánování. Tímto způsobem se zachovají zpoždění z opožděné schválené plánované výrobní zakázky a všechny podřízené komponenty budou odpovídajícím způsobem aktualizovány.
Zprávy akce lze rovněž použít k identifikaci plánovaných objednávek, které lze přesunout do pozdějšího data z důvodu jiných zpoždění ve struktuře kusovníku.

## <a name="desired-date"></a>Požadované datum

Na stránce **Plánovaná objednávka** na kartě **Zpoždění** je uvedeno **požadované datum** plánované objednávky. Požadované datum plánované objednávky je základní datum zpoždění, což je vypočítané datum, které se rovná **požadovanému datu** počítáno od **čistého požadavku**. Pokud je plánovaná objednávka řádka kusovníku, výroby nebo řádka kamban, je požadované datum založeno na **datu požadavku** a nebude uvedeno na stránce **Plánovaná objednávka**.

<a name="additional-resources"></a>Další zdroje
--------

[Nastavení distponibility](coverage-settings.md)
