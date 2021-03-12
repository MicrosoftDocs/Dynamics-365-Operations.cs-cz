---
title: Úpravy ceny a slevy
description: Tento článek obsahuje informace o úpravách cen a slev v aplikaci Dynamics 365 Commerce.
author: scott-tucker
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f29e90e1c61792c70d4d6eaeee7758676bf193b2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972473"
---
# <a name="price-adjustments-and-discounts"></a>Úpravy ceny a slevy

[!include [banner](includes/banner.md)]

Tento článek obsahuje informace o úpravách cen a slev v aplikaci Dynamics 365 Commerce.

V aplikaci Commerce můžete provést úpravy cen produktů a také nastavit slevy, které jsou použity pro položku řádku nebo transakci na pokladním místě (POS), v prodejní objednávce kontaktního střediska nebo v online objednávce. Úpravy ceny i slevy lze propojit s cenovými skupinami. Pro úpravy ceny a slevy můžete určit jedno počáteční a koncové datum nebo opakované období, kód slevy a další atributy. 

Úpravy ceny a slevy lze použít pro produkty, varianty nebo kategorie. Pokud je pro produkt platná více než jedna sleva, odběratel může obdržet buď jednu ze slev nebo kombinovanou slevu, a to v závislosti na konfiguraci slevy. Commerce automaticky použije slevu nebo kombinaci slevy, jež nabízí nejlepší cenu pro odběratele. Při nastavení úpravy ceny nebo slevy je nutné zkontrolovat, zda jsou cenové skupiny přiřazeny pro správné kanály, katalogy, umístění nebo věrnostní programy, u kterých mají být použity slevy. Dále, pokud potřebujete automaticky vygenerovat ID slevy, můžete před definováním nové slevy nebo úpravy ceny nastavit číselné řady na stránce **Parametry obchodu**.

> [!NOTE]
> Úpravu ceny nebo slevu můžete odstranit. Dojde však ke ztrátě statistických údajů.

## <a name="types-of-discounts"></a>Typy slev

Existují mnoho typů slev:

- **Jednoduchá sleva** – jedno procento nebo částka.
- **Množstevní sleva** – sleva, která se použije při zakoupení dvou nebo více produktů.
- **Kombinační sleva** – sleva je uplatněna v případě, že se zakoupí určitá kombinace položek.
- **Mezní sleva** – sleva, která se použije, když celková částka transakce je větší než zadaná částka.
- **Slevy založené na úhradě** – Sleva, která se použije, když celková částka transakce přesáhne stanovenou částku a pro platbu se použije určitý typ platby (například hotovost, kreditní nebo debetní karta).
- **Přepravní sleva** – Sleva, která se použije, když celková částka transakce přesáhne zadanou částku a na objednávku se použije určitý způsob doručení (například dvoudenní nebo noční přeprava).

Úpravy ceny i slevy lze propojit s cenovými skupinami. Skupiny cen lze pak přidružit s kanály, katalogy, umístěním a věrnostními programy.
