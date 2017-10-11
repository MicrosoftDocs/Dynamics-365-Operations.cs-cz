---
title: "Úpravy ceny a slevy"
description: "Tento článek obsahuje informace o úpravě ceny a slevách v aplikaci Microsoft Dynamics 365 for Retail."
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: caa701dfcbffe045d701442b1a39b88ea5f43125
ms.contentlocale: cs-cz
ms.lasthandoff: 06/20/2017

---

# <a name="price-adjustments-and-discounts"></a>Úpravy ceny a slevy

[!include[banner](includes/banner.md)]


Tento článek obsahuje informace o úpravě ceny a slevách v aplikaci Microsoft Dynamics 365 for Retail.

V aplikaci Microsoft Dynamics 365 for Retail můžete provádět úpravy ceny produktů a můžete také nastavit slevy, které budou použity pro položky řádku nebo transakce v pokladních místech (POS), a to v prodejní objednávce kontaktního střediska nebo online objednávce. Úpravy ceny i slevy lze propojit s cenovými skupinami. Pro úpravy ceny a slevy můžete určit jedno počáteční a koncové datum nebo opakované období, kód slevy a další atributy. Úpravy ceny a slevy lze použít pro produkty, varianty nebo kategorie. Pokud je pro produkt platná více než jedna sleva, odběratel může obdržet buď jednu ze slev nebo kombinovanou slevu, a to v závislosti na konfiguraci slevy. Aplikace Dynamics 365 for Retail automaticky použije slevu nebo kombinaci slevy, jež nabízí nejlepší cenu pro odběratele. Při nastavení úpravy ceny nebo slevy je nutné zkontrolovat, zda jsou cenové skupiny přiřazeny pro správné kanály, katalogy, umístění nebo věrnostní programy, u kterých mají být použity slevy. Dále, pokud potřebujete automaticky vygenerovat ID slevy, můžete před definováním nové slevy nebo úpravy ceny nastavit číselné řady na stránce **Parametry maloobchodu**. **Poznámka:** Úpravu ceny nebo slevu můžete odstranit. Dojde však ke ztrátě statistických údajů.

### <a name="types-of-discounts"></a>Typy slev

Existují čtyři typy maloobchodních slev:

-   **Jednoduchá sleva** – jedno procento nebo částka.
-   **Množstevní sleva** – sleva, která se použije při zakoupení dvou nebo více produktů.
-   **Kombinační sleva** – sleva je uplatněna v případě, že se zakoupí určitá kombinace položek.
-   **Mezní sleva** – sleva, která se použije, když celková částka transakce je větší než zadaná částka.

Úpravy ceny i slevy lze propojit s cenovými skupinami. Skupiny cen lze pak přidružit s kanály, katalogy, umístěním a věrnostními programy.



