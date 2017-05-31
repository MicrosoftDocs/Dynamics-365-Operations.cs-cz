---
title: "Zpoždění"
description: "Tento článek obsahuje informace o zpožděných datech v hlavním plánování. Zpožděné datum je realistické datum splatnosti přidělené transakci, pokud je nejbližší datum plnění vypočítané hlavním plánováním pozdější než požadované datum."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 84682e08da6da8928004c7971cd2c2a3725446c0
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="delays"></a>Zpoždění

[!include[banner](../includes/banner.md)]


Tento článek obsahuje informace o zpožděných datech v hlavním plánování. Zpožděné datum je realistické datum splatnosti přidělené transakci, pokud je nejbližší datum plnění vypočítané hlavním plánováním pozdější než požadované datum.

Hlavní plánování dokáže vypočítat nejbližší datum plnění transakce na základě doby realizace, dostupnosti materiálu, dostupné kapacity a různých parametrů plánování. 

Pokud hlavní plánování vypočítá datum objednávky, které předchází dnešnímu datu, objednávku nelze splnit včas. Objednávka je proto zpožděná. V takovém případě hlavní plánování objednávku naplánuje dopředně od dnešního data a zahrne doby realizace. Tyto realizace časy zahájení kteroukoliv položkou součásti na nižší úrovni. Objednávce se pak přiřadí datum zpoždění. Datum zpoždění je realistické datum dodání stanovené podle aktuálního data. Hlavní plánování vypočte také počet dnů zpoždění. 

V některých situacích může být vhodnější zpoždění nevypočítávat, například pokud uživatelé vědí, že lze dobu realizace urychlit výběrem alternativních způsobů dodání. 

Způsob výpočtu zpoždění pro skupinu disponibility lze upravit. Skupinu disponibility můžete k položce přiřadit později. 

Na stránce **Parametry hlavního plánování** můžete nastavit čas zahájení výpočtu zpoždění. Pokud je objednávka splněna po tomto termínu, k datu zpoždění objednávky se přičte jeden den. 

**Poznámka:** V předchozích verzích se vypočtená zpoždění nazývala *termínové zprávy*, datum zpoždění se nazývalo *datum termínu* a zpožděná transakce se označovala jako *transakce nastavená na budoucí datum*.

<a name="see-also"></a>Viz také
--------

[Nastavení pokrytí](coverage-settings.md)




