---
title: Přehled směnného kurzu DPH
description: Tento článek poskytuje informace o směnných kurzech pro výpočet DPH, který je k dispozici pro Česko, Maďarsko a Polsko.
author: mrolecki
ms.date: 07/08/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Czech Republic, Hungary, Poland
ms.author: mrolecki
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 272703,  ""intro-internal
ms.assetid: 2d1fad67-8234-49cc-b009-0f3cc29f5886
ms.search.form: ExchangeRateCurrencyPairCalculationRules, LedgerParameters, SalesTaxExchangeRateType, TaxTmpWorkTrans
ms.openlocfilehash: b132eb08bbdba8c940d2e359c9f01beb1f4a376a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269340"
---
# <a name="vat-exchange-rate-overview"></a>Přehled směnného kurzu DPH

[!include [banner](../includes/banner.md)]

Tento článek poskytuje informace o směnných kurzech pro výpočet DPH, který je k dispozici pro Česko, Maďarsko a Polsko. Směnný kurz, který se používá k výpočtu DPH, může být odlišný od směnného kurzu, který organizace používá pro funkce účetnictví. Při zaúčtování dokumentu v cizí měně jsou zaúčtovány všechny vzniklé kurzové rozdíly do konkrétních účtů hlavní knihy.

Vaše organizace může vybrat směnný kurz, který používá, pro výpočet daně z přidané hodnoty (DPH) pro výkazy DPH. Tento směnný kurz může být odlišný od směnného kurzu, který organizace používá pro funkce účetnictví společnosti. Funkce účetnictví zahrnují přípravu následujících dokumentů souvisejících s daněmi:

-   Faktury
-   Volné faktury
-   Nákupní objednávky
-   Faktury projektu
-   Dobropisy
-   Opravné faktury

Při zaúčtování dokumentu, který používá cizí měnu, jsou zaúčtovány všechny vzniklé kurzové rozdíly do konkrétních účtů hlavní knihy.

## <a name="prerequisites"></a>Požadavky

Než budete moci použít tuto funkci, musíte nakonfigurovat systém.

1.  Vytvořte typy směnných kurzů a nastavte směnné kurzy pro DPH pomocí možností **Hlavní kniha** &gt; **Měny** &gt; **Typy směnných kurzů**. Můžete definovat tolik typů směnných kurzů a tolik směnných kurzů pro páry měn, kolik potřebujete.
2.  Povolte výpočet směnných kurzů DPH zapnutím parametru **Bankovní směnný kurz** a definováním typů směnných kurzů pohledávek DPH a závazků DPH v parametrech **Hlavní kniha** &gt; **Nastavení hlavní knihy** &gt; **Parametry hlavní knihy**.
3.  Nastavte typy směnných kurzů měny pro určité prodejní a nákupní typy transakcí v možnostech **Hlavní kniha** &gt; **Měny** &gt;**Typy směnného kurzu pro prodejní daň**.
4.  Nastavte rozdíl mezi závazky DPH a pohledávkami DPH a rozdíl protiúčtů ve skupinách zaúčtování hlavní knihy v možnostech **Daň** &gt; **Nastavení** &gt; **DPH** &gt; **Skupiny zaúčtování hlavní knihy**.
5.  Volitelné: Nastavte pravidlo výpočtu směnného kurzu pro pár měny v možnostech **Hlavní kniha** &gt; **Měny** &gt; **Pravidla výpočtu směnného kurzu pro páry měn**. Pravidla výpočtu směnného kurzu se používají k převodu částek DPH pro prodejní faktury v cizí měně na částky DPH v cílové měně.

## <a name="overview"></a>Přehled

Po dokončení konfigurace systému pro použití směnných kurzů DPH, pokud je nutné zadat dokument nebo vytvořit objednávku používající cizí měnu, lze použít stránku **Transakce DPH** pro nastavení hodnoty **Datum rejstříku DPH** k vyzvednutí a nastavení výchozí hodnoty **Směnný kurz DPH**. Obě pole lze upravovat. Můžete také použít pole **Původ opravené částky (směnný kurz DPH)** nebo **Opravená částka DPH (směnný kurz DPH)** pro zadání skutečných částek DPH v místní měně, která je uvedena v externím dokumentu. Při kontrole účetnictví můžete zobrazit částky rozdílu DPH na stránce **Dílčí hlavní kniha**. Při zaúčtování dokumentu můžete zobrazit jakékoliv rozdíly v částkách DPH způsobené rozdílem mezi směnným kurzem měny DPH a směnným kurzem účetnictví vaší organizace, které jsou zaúčtovány do účtů hlavní knihy, které jste nakonfigurovali.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
