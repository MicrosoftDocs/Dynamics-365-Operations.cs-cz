---
title: Výstupní místo výroby
description: Toto téma popisuje hierarchii, která se používá k identifikaci výstupního místa výroby.
author: johanhoffmann
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 48b68c36718fa42b7f80e3ffe1f54b7efbbee8bd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814625"
---
# <a name="production-output-location"></a>Výstupní místo výroby

[!include [banner](../includes/banner.md)]

Toto téma popisuje hierarchii, která se používá k identifikaci výstupního místa výroby.

Výstupní místo výroby je místo, kam se nejprve uloží hotové zboží poté, co je vyrobeno. Tohoto skladové místo je obvykle blízko výrobního procesu, který vytváří dokončené zboží. Výstupní místo výroby se používá jako dočasné úložiště pro materiál před jeho přesunutím do oblasti expedice, skladovacího místa, vstupního místa výroby pro proces výroby směrem dolů, atd. 

Výchozí výstupní místo výroby je nastaveno, když je dokončené vykázáno ve výrobním příkazu nebo dávkové objednávce. Následující hierarchie se používá k identifikaci tohoto výstupního místa:

1. Použijte výstupní místo definované v záhlaví výrobní zakázky nebo dávkové objednávky.
2. Pokud zde není nalezeno žádné místo, použijte výstupní místo, které je definováno ve zdroji, který byl použit v poslední operaci definované ve výrobním postupu.
3. Pokud zde není nalezeno žádné místo, použijte výstupní místo, které je definováno ve skupině zdrojů používané zdrojem, který byl použit v poslední operaci definované ve výrobním postupu.
4. Pokud zde není nalezeno žádné místo, použijte výstupní místo, které je definováno pro sklad, který je definován pro výrobní zakázku.

Výchozí výstupní místo výroby je nastaveno pouze pro produkty, které se nastavují pomocí rozšířených skladových procesů. Když je tento typ zboží nahlášen jako dokončený, vytvoří se skladová práce typu **Odložení hotového zboží** nebo **Odložení společných a vedlejších produktů**. Tento typ práce používá výstupní místo výroby jako místo pro výdej. Místo pro odložení je určeno směrnicemi místa.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]