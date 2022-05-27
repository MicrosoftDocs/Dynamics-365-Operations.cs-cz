---
title: Mezipodnikové parametry
description: Toto téma vysvětluje mezipodnikové parametry
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder, InterCompanyTradingRelationSetupCustomer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 78186d466d88f876629ceb81ec99b94c8818c560
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678596"
---
# <a name="intercompany-parameters"></a>Mezipodnikové parametry

[!include [banner](../../includes/banner.md)]

V mezipodnikové organizaci lze nastavit parametry definující způsob obchodování mezi různými právnickými osobami. Tyto parametry jsou určeny vybranými poli. Můžete vybrat různé kombinace tak, aby odrážely různé obchodní scénáře.

Následující dva příklady popisují scénáře mezipodnikových organizací, jeden se dvěma úrovněmi a jeden se třemi úrovněmi.

## <a name="example-1-two-level-intercompany-chain"></a>Příklad 1: Dvouúrovňový mezipodnikový řetězec

Mezipodniková organizace zahrnuje následující právnické osoby:

- Právnická osoba A - Prodává externím odběratelům, ale nemá žádné zásoby. Tato právnická osoba nakupuje od právnické osoby B.
- Právnická osoba B - Prodává pouze právnické osobě A.

Obě právnické osoby si mohou navzájem prodávat a nakupovat zboží.

V tomto příkladu je cenová kalkulace u původní prodejní objednávky, která je směrována na externího odběratele, vždy založena na prodejní ceně. Cenová kalkulace u mezipodnikové prodejní či nákupní objednávky se řídí cenovou kalkulací interního prodeje nebo převodu u mezipodnikové prodejní objednávky právnické osoby B.

Informace v záhlaví objednávky se řídí z původní prodejní objednávky pro externího odběratele. Případné změny v mezipodnikové prodejní objednávce NEJSOU synchronizovány s původní prodejní objednávkou.

V právnické osobě A na stránce **Mezipodnikové** pro dodavatele vyberte **Zásady nákupních objednávek**. Vyberte následující pole ve skupině polí **Původní prodejní objednávka (přímá dodávka)**:

- **Tisknout dodací list automaticky**
- **Zaúčtovat fakturu automaticky**
- **Tisknout fakturu automaticky**

Ve skupině polí **Mezipodniková nákupní objednávka (přímá dodávka)** vyberte následující pole:

- **Zaúčtovat fakturu automaticky**

Ve skupině **Původní prodejní objednávka <-> Mezipodniková nákupní objednávka** vyberte následující pole:

- **Informace o odběrateli**
- **Číslo RMA**

Ve skupině **Mezipodniková nákupní objednávka <-> Mezipodniková prodejní objednávka** vyberte následující pole:

- **Informace o odběrateli**
- **Číslo RMA**
- **Číslo dávky**
- **Sériové číslo**

V právnické osobě B na stránce **Mezipodniková** pro odběratele vyberte **Zásady prodejních objednávek**. Vyberte následující pole ve skupině polí **Vytvoření mezipodnikové prodejní objednávky**:

- **Číslování prodejních objednávek** : **Společnost + původní číslo**
- **Povolit souhrnnou aktualizaci dokumentů pro původního odběratele**

Ve skupině polí **Ceny mezipodnikové prodejní objednávky** vyberte následující pole:

- **Vyhledávání ceny a slevy**
- **Povolit úpravu ceny**
- **Povolit úpravu slevy**

Ve skupině polí **Mezipodniková prodejní objednávka \> Mezipodniková nákupní objednávka** vyberte následující pole:

- **Číslo dávky**
- **Sériové číslo**

## <a name="example-2-three-level-intercompany-chain"></a>Příklad 2: tříúrovňový mezipodnikový řetězec

Mezipodniková organizace zahrnuje následující právnické osoby:

- Právnická osoba A - Prodejní právnická osoba, která prodává externím odběratelům a nakupuje od právnické osoby B.
- Právnická osoba B - Produkční nebo distribuční právnická osoba, která nemůže dodávat produkty a nakupuje od Právnické osoby C.
- Právnická osoba C - Produkční nebo distribuční právnická osoba, která dodává produkty právnické osobě B.

Interní ceny převodů mezi právnickými osobami B a C jsou nákladové ceny od prodávající právnické osoby na začátku řetězce. Je také nákladovou cenou pro právnickou osobu A, která prodává externím odběratelům. Avšak cenová kalkulace původní prodejní objednávky pro externího odběratele je vždy založena na prodejní ceně.

Ceny všech mezipodnikových prodejních objednávek a mezipodnikových nákupních objednávek se řídí na mezipodnikové prodejní objednávce. Jsou řízeny na začátku řetězce. Cenu tedy řídí právnická osoba C, která prodává právnické osobě B. Cenová kalkulace u mezipodnikových prodejních objednávek je založena na cenové kalkulaci interního prodeje/převodu nastavené v právnické osobě C.

Informace v záhlaví objednávky se řídí z původní prodejní objednávky pro externího odběratele. Případné změny v mezipodnikových objednávkách NEJSOU synchronizovány s původní prodejní objednávkou.

Je vhodné zvolit následující parametry:

V právnické osobě A na stránce **Mezipodnikové** pro dodavatele vyberte **Zásady nákupních objednávek**. Vyberte následující pole ve skupině polí **Původní prodejní objednávka (přímá dodávka)**:

- **Tisknout dodací list automaticky**
- **Zaúčtovat fakturu automaticky**
- **Tisknout fakturu automaticky**

Ve skupině polí **Mezipodniková nákupní objednávka (přímá dodávka)** vyberte následující pole:

- **Zaúčtovat fakturu automaticky**

Ve skupině polí **Původní prodejní objednávka <-> Mezipodniková nákupní objednávka** vyberte následující pole:

- **Informace o odběrateli**
- **Číslo RMA**

Ve skupině **Mezipodniková nákupní objednávka <-> Mezipodniková prodejní objednávka** vyberte následující pole:

- **Informace o odběrateli**
- **Číslo RMA**
- **Číslo dávky**
- **Sériové číslo**

V právnické osobě B na stránce **Mezipodniková** pro odběratele vyberte **Zásady prodejních objednávek**. Vyberte následující pole ve skupině polí **Vytvoření mezipodnikové prodejní objednávky**:

- **Číslování prodejních objednávek** : **Společnost + původní číslo**
- **Povolit souhrnnou aktualizaci dokumentů pro původního odběratele**

Ve skupině polí **Mezipodniková prodejní objednávka \> Mezipodniková nákupní objednávka** vyberte následující pole:

- **Číslo dávky**
- **Sériové číslo**

Ve skupině polí **Zaúčtování mezipodnikové faktury odběratele** vyberte následující pole:

- **Jednotková cena shodná s nákladovou cenou**
- **Spustit zaúčtování původní faktury odběratele**

V právnické osobě B na stránce **Mezipodnikové** pro dodavatele vyberte **Zásady nákupních objednávek**. Vyberte následující pole ve skupině polí **Původní prodejní objednávka (přímá dodávka)**:

- **Tisknout dodací list automaticky**
- **Zaúčtovat fakturu automaticky**
- **Tisknout fakturu automaticky**

Ve skupině polí **Mezipodniková nákupní objednávka (přímá dodávka)** vyberte následující pole:

- **Zaúčtovat fakturu automaticky**

Ve skupině polí **Původní prodejní objednávka <-> Mezipodniková nákupní objednávka** vyberte následující pole:

- **Informace o odběrateli**
- **Číslo RMA**
- **Cena a sleva**

Ve skupině **Mezipodniková nákupní objednávka <-> Mezipodniková prodejní objednávka** vyberte následující pole:

- **Informace o odběrateli**
- **Číslo RMA**
- **Číslo dávky**
- **Sériové číslo**

V právnické osobě C na stránce **Mezipodnikové** pro odběratele vyberte **Zásady prodejních objednávek**. Vyberte následující pole ve skupině polí **Vytvoření mezipodnikové prodejní objednávky**:

- **Číslování prodejních objednávek** : **Číselný pořadový kód**
- **Povolit souhrnnou aktualizaci dokumentů pro původního odběratele**

Ve skupině polí **Ceny mezipodnikové prodejní objednávky** vyberte následující pole:

- **Vyhledávání ceny a slevy**

Ve skupině polí **Zaúčtování mezipodnikové faktury odběratele** vyberte následující pole:

- **Jednotková cena shodná s nákladovou cenou**
- **Spustit zaúčtování původní faktury odběratele**

Ve skupině **Mezipodniková prodejní objednávka <-> Mezipodniková nákupní objednávka** vyberte následující pole:

- **Číslo dávky**
- **Sériové číslo**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
