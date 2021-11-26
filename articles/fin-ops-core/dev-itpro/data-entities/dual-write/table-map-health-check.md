---
title: Kódy chyb pro kontrolu stavu mapy tabulky
description: Toto téma popisuje kódy chyb pro kontrolu stavu mapy tabulky.
author: nhelgren
ms.date: 10/04/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: nhelgren
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: c2d1f1e39a5ddccddf6fbbf524ff7eb0945b3c32
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782229"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Kódy chyb pro kontrolu stavu mapy tabulky

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma popisuje kódy chyb pro kontrolu stavu mapy tabulky.

## <a name="error-100"></a>Chyba 100

Chybová zpráva zní: „Požadována minimální verze platformy Finance and Operations je PU 43 ke spuštění doporučení Finance and Operations.“

Tato funkce vyžaduje aktualizace platformy pro verzi aplikace Finance and Operations 10.0.19 nebo novější.

## <a name="error-400"></a>Chyba 400

Chybová zpráva zní: „Pro entitu \{Finance and Operations UniqueEntityName\} nebyla nalezena žádná registrační data obchodních událostí, což znamená, že buď mapa neběží, nebo jsou všechna mapování polí jednosměrná.“

## <a name="error-500"></a>Chyba 500

Chybová zpráva je „Pro projekt nebyly nalezeny žádné konfigurace projektu \{název projektu\}. Může to být buď, že projekt není povolen, nebo všechna mapování polí jsou jednosměrná z Customer Engagement do Finance and Operations.“

Zkontrolujte mapování pro mapu tabulky. Pokud jsou jednosměrná z aplikací Customer Engagement do aplikací Finance and Operations, není generován žádný provoz pro živou synchronizaci z aplikací Finance and Operations do Dataverse.

## <a name="error-900"></a>Chyba 900

Chybová zpráva je „Neplatný formát zdrojového filtru \{sourceFilter\} pro entitu \{Finance and Operations UniqueEntityName\}.“

Zdrojový filtr, který je zadán na mapě tabulky pro aplikace Finance and Operations, není syntakticky správný. Chcete-li ověřit kritéria filtru, viz [Odstraňování problémů se synchronizací v reálném čase](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Chyba 1000

Chybová zpráva je „Dotaz entity \{Finance and Operations UniqueEntityName\} používaný pro živou synchronizaci s duálním zápisem je \{Finance and Operations EntityFilterQueryString\}. Záznamy, které splňují kritéria dotazu, budou vybrány pro živou synchronizaci.“

Dotaz entity, který byl vrácen, je podpůrným dotazem SQL pro entitu. Zkontrolujte vnitřní spojení nebo filtry v dotazu, které určují obchodní data, která se sbírají pro živou synchronizaci. Vnitřní spojení a filtry jsou povinné podmínky, které musí být splněny pro každý záznam, který je sbírán pro živou synchronizaci s duálním zápisem.

## <a name="error-1300"></a>Chyba 1300

Chybová zpráva je „Virtuální pole \{s.EntityFieldName\} pro entitu \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} nemusí být sledováno pro duální zápis.“

Virtuální pole z tabulek Finance and Operations nejsou povolena pro sledování. Živá synchronizace může synchronizovat data, ale nebude schopna zachytit změny provedené ve sloupcích.

## <a name="error-1500"></a>Chyba 1500

Chybová zpráva zní: „Mělo by být alespoň jedno pole namapované na nevyhledávací pole v Customer Engagement, aby bylo možné sledovat zdroj dat \{datasource.DataSourceName\}.“

Zdroj dat z entity nemá žádné pole mapované pro duální zápis. Změny v podkladové tabulce nebudou sledovány pro duální zápis.

## <a name="error-1600"></a>Chyba 1600

Chybová zpráva zní: „Zdroj dat: \{datasource.DataSourceName\} pro entitu \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} má rozsah. Pro odchozí komunikaci jsou vyzvednuty pouze záznamy, které splňují podmínku rozsahu.“

Entity v aplikacích Finance and Operations mohou mít zdroje dat, kde jsou povoleny rozsahy filtrů. Tyto rozsahy definují záznamy, které jsou sbírány jako součást živé synchronizace. Pokud jsou některé záznamy přeskočeny z aplikací Finance and Operations do Dataverse, zkontrolujte, zda záznamy splňují kritéria rozsahu na entitě. Jednoduchý způsob, jak provést tuto kontrolu, je spustit dotaz SQL, který se podobá následujícímu příkladu.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Chyba 1700

Chybová zpráva zní: „Tabulka: \{datasourceTable.Key.subscribedTableName\} pro entitu \{datasourceTable.Key.entityName\} je sledována pro entitu \{origTableToEntityMaps.EntityName\}. Stejné tabulky sledované pro více entit mohou ovlivnit výkon systému pro transakce živé synchronizace.“

Pokud je stejná tabulka sledována více entitami, jakákoli změna tabulky spustí vyhodnocení duálního zápisu pro propojené entity. Přestože klauzule filtru pošlou pouze platné záznamy, hodnocení může způsobit problém s výkonem, pokud existují dlouhotrvající dotazy nebo neoptimalizované plány dotazů. Tento problém nemusí být z obchodního hlediska nevyhnutelný. Pokud však existuje mnoho protínajících se tabulek ve více entitách, měli byste zvážit zjednodušení entity nebo kontrolu optimalizací pro dotazy na entity.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
