---
title: Synchronizace mezipodnikových cen a slev
description: Tento článek vysvětluje synchronizaci cen a slev u mezipodnikových prodejních objednávek a nákupních objednávek
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 64130c400212a819f931cc36459667e4d7c83f32
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905682"
---
# <a name="synchronize-intercompany-prices-and-discounts"></a>Synchronizace mezipodnikových cen a slev

[!include [banner](../../includes/banner.md)]

Slevy a ceny lze vždy synchronizovat mezi mezipodnikovou prodejní objednávkou a mezipodnikovou nákupní objednávkou. Lze rovněž synchronizovat ceny a slevy do a z původní prodejní objednávky, aby měly všechny objednávky stejné ceny a slevy. To uděláte na stránce **Mezipodnikové**, na kterou se přistupuje z karty **Obecné** na stránce se seznamem **Všichni odběratelé** – buď z **Prodeje a marketingu** nebo ze **Zásobování a zdrojů**.

Pole **Cena a sleva** se synchronizuje s řádkem mezipodnikové prodejní objednávky. To znamená, že výběrem polí **Povolit úpravu ceny** a **Povolit úpravu slevy** se povolí změna mezi mezipodnikovou prodejní a nákupní objednávkou. Změna jednotkové ceny, cenové jednotky a nákladů prodeje u mezipodnikové prodejní objednávky určuje cenu v řádku mezipodnikové nákupní objednávky.

Pokud jsou pole **Povolit úpravu ceny** a **Povolit úpravy slevy** povolena v mezipodnikové prodejní objednávce nebo v mezipodnikové nákupní objednávce, u každé objednávky můžete cenu nebo slevu změnit ručně. V opačném případě tak učinit nemůžete.

Pokud pole **Povolit úpravu ceny** a **Povolit úpravy slevy** nejsou povolena v mezipodnikové prodejní objednávce, nemůžete cenu (nebo náklady) či slevu v mezipodnikové prodejní objednávce změnit ručně.

Pokud pole **Povolit úpravu ceny** a **Povolit úpravy slevy** nejsou povolena v mezipodnikové nákupní objednávce, nemůžete cenu (nebo náklady) či slevu v mezipodnikové nákupní objednávce změnit ručně.

Pokud jsou pole **Povolit úpravu ceny** a **Povolit úpravy slevy** povolena současně v mezipodnikové prodejní objednávce i v mezipodnikové nákupní objednávce, můžete v obou objednávkách cenu nebo slevu změnit ručně. To však může způsobit situaci, kdy aktualizace provedené jednou osobou budou přepsány aktualizacemi provedenými jinou osobou v jiné společnosti na stejné objednávce.

> [!NOTE]
> Pokud je povoleno pole **Cena a sleva** v mezipodnikové prodejní i nákupní objednávce, nemáte kontrolu nad oceňováním.

Nejlepším způsobem, jak se vyhnout tomuto typu konfliktů, je povolit změny cen a slev pouze v mezipodnikové prodejní objednávce. Toho dosáhnete povolením polí **Povolit úpravu ceny** a **Povolit úpravy slevy** pouze u jednoho typu objednávky.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
