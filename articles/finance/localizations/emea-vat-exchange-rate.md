---
title: Přehled směnného kurzu DPH
description: Toto téma obsahuje informace o směnných kurzech pro výpočet DPH. Směnný kurz, který se používá k výpočtu DPH, může být odlišný od směnného kurzu, který organizace používá pro funkce účetnictví. Při zaúčtování dokumentu v cizí měně jsou zaúčtovány všechny vzniklé kurzové rozdíly do konkrétních účtů hlavní knihy.
author: ShylaThompson
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ExchangeRateCurrencyPairCalculationRules, LedgerParameters, SalesTaxExchangeRateType, TaxTmpWorkTrans
audience: Application User
ms.reviewer: kfend
ms.custom: 272703
ms.assetid: 2d1fad67-8234-49cc-b009-0f3cc29f5886
ms.search.region: Czech Republic, Hungary, Poland
ms.author: mrolecki
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 8a3f02d0a86ddf54e6f1a5a11a795561a7ec01af
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832668"
---
# <a name="vat-exchange-rate-overview"></a>Přehled směnného kurzu DPH

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace o směnných kurzech pro výpočet DPH. Směnný kurz, který se používá k výpočtu DPH, může být odlišný od směnného kurzu, který organizace používá pro funkce účetnictví. Při zaúčtování dokumentu v cizí měně jsou zaúčtovány všechny vzniklé kurzové rozdíly do konkrétních účtů hlavní knihy.

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