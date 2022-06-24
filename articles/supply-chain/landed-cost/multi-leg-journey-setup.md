---
title: Nastavení cesty s více úseky
description: Tento článek popisuje, jak nastavit cestu s více úseky pro modul nákladů za doručení.
author: Weijiesa
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMLegTable, ITMJourneyTable, ITMActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: dcb536c03d09d51b247d9060d87db64e2b80383b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905827"
---
# <a name="multi-leg-journey-setup"></a>Nastavení cesty s více úseky

[!include [banner](../../includes/banner.md)]

Tento článek popisuje, jak nastavit cestu s více úseky pro modul **nákladů za doručení**.

## <a name="legs"></a>Úseky

Úseky se používají k identifikaci samostatných částí cesty. Každý úsek je vybudován výběrem přepravních přístavů „do“ a „z“ a způsobu dopravy, který se pro tento úsek používá. S každým úsekem lze spojit doby realizace. Doby realizace mohou pomoci sledovat zásilku a lze je také použít k výpočtu předpokládaného data dodání zboží na cestě. Kromě toho lze po dokončení úseku cesty aktualizovat stav cesty, přepravního kontejneru a souvisejících řádků nákupní objednávky prostřednictvím nastavení řízení sledování. Úseky mohou být použity v jedné šabloně cesty nebo mohou být znovu použity v několika šablonách cesty. Nakládání kontejnerů, celní a místní přeprava se obvykle nastavují jako úseky a používá se pro ně nespecifický přepravní přístav.

Pokud chcete pracovat s úseky, přejděte na **Náklady za doručení \> Nastavení cesty s více úseky \> Úseky**. Zde můžete prohlížet, otevírat, vytvářet a mazat záznamy úseků. V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.

| Pole | popis |
|---|---|
| Úsek | Zadejte jedinečný identifikační název/číslo úseku cesty. |
| popis | Zadejte stručný popis úseku cesty. Tento popis obvykle označuje přístavy „do“ a „od“ nebo krok cesty. |
| Výchozí přístav | V úseku zadejte místo původu zboží. |
| Cílový přístav | Zadejte bod pro cíl zboží v úseku. |
| Způsob dodání | Zadejte způsob přepravy pro úsek. |

## <a name="journey-templates"></a>Šablony cesty

Šablona cesty definuje cestu s několika úseky mezi dvěma přístavy, mezi nimiž zboží cestuje během plavby. Úseky cesty jsou kombinovány, aby se určilo množství času, které bude vyžadováno, aby zboží mohlo cestovat z místa původu u dodavatele do konečného cílového skladu. Když jsou úseky umístěny na šabloně cesty v určitém pořadí, doby realizace určí datum každého úseku a stav řádku plavby, kontejneru a nákupu pro plavbu. Možnost [Sledovací kontrolní centrum](delivery-information-setup.md) se používá k nastavení dob realizace, které jsou spojeny s každým úsekem, který tvoří šablonu cesty. Šablona cesty se také používá, když jsou nastaveny automatické náklady na cestu. Když je cesta definována, náklady spojené s přepravou zboží lze definovat na stránce s automatickými náklady.

Pokud chcete pracovat s šablonami cesty, přejděte na **Náklady za doručení \> Nastavení cesty s více úseky \> Šablony cesty**. Zde můžete prohlížet, otevírat, vytvářet a mazat šablony cesty.

U každé šablony cesty nastavte v záhlaví následující pole.

| Pole | popis |
|---|---|
| Šablona cesty | Zadejte jedinečný identifikační název/číslo šablony cesty. Šablona cesty obvykle popisuje počáteční a cílový bod cesty. |
| popis | Zadejte popis šablony cesty. Popis obvykle označuje přístavy „do“ a „od“ a typ cesty. |

V části **Řádky** přidejte řádek pro každý úsek cesty a řádky uspořádejte. Pomocí šipky **Nahoru** a **Dolů** na panelu nástrojů změňte pořadí řádků. V následující tabulce jsou popsána pole, která jsou k dispozici pro každý řádek.

| Pole | popis |
|---|---|
| Úsek | Vyberte úsek, který chcete přidat k cestě. |
| popis | Popis úseku. |
| Výchozí přístav | Přístav, který je v místě původu zboží v úseku. Tento přístav je cílový přístav, který se používá k určení automatických nákladů na cestu. |
| Cílový přístav | Konečný cílový přístav zboží v úseku. |
| Způsob dodání | Režim dodání, který se používá pro úsek. |
| Cesta z přístavu | Jestliže se přístav, který je určen pro úsek, používá k určení automatických nákladů, zaškrtnutím tohoto políčka ho určete jako výchozí přístav cesty. Tento přístav se zobrazí v záhlaví cesty. |
| Cesta do přístavu | Jestliže se přístav, který je určen pro úsek, používá k určení automatických nákladů, zaškrtnutím tohoto políčka ho určete jako cílový přístav cesty. Tento přístav se zobrazí v záhlaví cesty. |
| Dopravní společnost | Vyberte přepravní společnost, která se používá pro úsek. |

## <a name="activities"></a>Aktivity

Nastavení na stránce **Aktivity** stanoví typy aktivit, které mohou nastat v cílovém přístavu úseku. Uživatelé, kteří pracují na stránce **Všechny přepravní kontejnery**, si mohou vybrat mezi těmito hodnotami, když odhadují trvání každé aktivity a zaznamenávají skutečné trvání pro účely srovnání.

Chcete-li nastavit své aktivity, přejděte na **Náklady za doručení \> Nastavení cesty s více úseky \> Aktivity**. Můžete zde přidávat, odebírat a upravovat aktivity pomocí tlačítek v podokně akcí.

V následující tabulce jsou popsána pole, která jsou k dispozici pro každou aktivitu v mřížce.

| Pole | popis |
|---|---|
| Aktivita | Název aktivity. |
| popis | Popis aktivity. |
| Dopravní společnost | Účet dodavatele přepravní společnosti, který je spojen s aktivitou. |
