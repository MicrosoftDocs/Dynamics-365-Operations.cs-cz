---
title: Úpravy ceny a slevy
description: Tento článek obsahuje informace o úpravách cen a slev v aplikaci Dynamics 365 Commerce.
author: scott-tucker
ms.date: 06/11/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 96a695df250cda514b7bd8b9716c0f03fb2bfd28d3af4daedaf1335c3099fbb6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748491"
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

> [!NOTE]
> Kombinační sleva a mezní sleva mají vlastnosti s názvem „Započítat produkty bez slevy“ a „Započítat produkty bez slevy do mezní hodnoty“. Pokud jsou tyto vlastnosti povoleny, položka, která nemá nárok na žádnou slevu, může stále pomoci kvalifikovat transakci k udělení slevy, ale nezpůsobilá položka slevu nezíská. 
> 
> Například pokud vytvoříte kombinační slevu se dvěma řádky A a B, kde by měl zákazník získat slevu 10% na obě položky, ale položka A má zaškrtnutou konfiguraci „Zabránit všem slevám“, pak by obvykle položka A do slevy zahrnuta nebyla. Pokud je však povolena vlastnost „Započítat produkty bez slevy“, lze položku A použít k získání kombinační slevy, ale 10% sleva se použije pouze na položku B. Podobná logika platí i pro mezní slevu. 
>
> Vlastnost „Započítat produkty bez slevy do mezní hodnoty“ má však ve srovnání s vlastností „Započítat produkty bez slevy“ kombinační slevy další schopnost. Pokud je povolena mezní sleva a pokud existuje položka, která má existující slevu, která by bránila položce v jakýchkoli jiných slevách, pak by cena zaplacená za tuto položku způsobila splnění mezní hodnoty, ale tato položka nedostane další slevu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
