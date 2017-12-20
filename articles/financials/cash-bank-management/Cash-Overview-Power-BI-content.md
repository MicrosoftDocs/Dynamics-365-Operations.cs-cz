---
title: "Obsah přehledu hotovosti v Power BI"
description: "Toto téma popisuje obsah přehledu hotovosti v Microsoft Power BI. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření obsahu."
author: saraschi2
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 8a3d12b3b0f71ea8b84b1618d9bb6bbc416e3b1d
ms.contentlocale: cs-cz
ms.lasthandoff: 12/01/2017

---

# <a name="cash-overview-power-bi-content"></a>Obsah přehledu hotovosti v Power BI

[!include[banner](../includes/banner.md)]

Toto téma popisuje obsah **Přehled hotovosti** v Microsoft Power BI. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření obsahu.

## <a name="overview"></a>Přehled

Obsah **Přehled hotovosti** v Power BI byl vytvořen pro jednotlivce, kteří zodpovídají za hotovost ve své organizaci. Obsah **Přehled hotovosti** v Power BI vizibilitu vašeho cashflow. Rovněž poskytuje prognózy, které vám mohou pomoci lépe rozhodovat a tím vylepšovat stav vašeho cashflow. Můžete analyzovat hotovost podle právnické osoby, měny a bankovního účtu, abyste získali lepší pochopení k lepšímu pochopení přebytků a nedostatků.

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI

Sestavy z obsahu Power BI **Přehled hotovosti** se zobrazí v pracovních prostorech **Přehled hotovosti** a **Správa banky**.

Aby bylo možné zobrazit sestavy hotovostního toku s datem, je nutné nejprve spustit proces výpočtu prognózy pomocí funkce **Vypočítat prognózy hotovostního toku** v oblasti správy hotovosti a banky.  To je třeba dokončit pro každou společnost zahrnutou do prognózy.  Potom je nutné aktualizovat souhrnné měření LedgerCovLiquidityMeasurement na stránce **Úložiště entit**.  

Pro účely ukázky můžete přidat ukázková data prognózy hotovostního toku pomocí stránky **Generovat data** z modulu Ukázková data.  Tento skript data vloží do tabulek prognózy hotovostního toku, aby bylo možné rychle zadat informace nezbytné pro sestavy.  Tento modul je dostupný, pouze pokud máte v prostředí nasazený model sady ukázkových dat. 

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Sestavy, které jsou součástí obsahu Power BI
Následující tabulka obsahuje podrobnosti o metrikách, které jsou k dispozici na každé stránce sestavy obsahu Power BI **Přehled hotovosti**.

| Sestava                                | Obsah |
|---------------------------------------|----------|
| Přehled hotovosti – všechny společnosti         | <ul><li>Přírůstky a úbytky v systémové měně</li><li>Předpokládané zůstatky měny</li><li>Celkový bankovní zůstatek v měně systému</li><li>Zůstatek podle právnické osoby</li><li>Dnešní skutečný a předpokládaný zůstatek v měně bankovního účtu</li></ul> |
| Přehled hotovosti – aktuální společnost       | <ul><li>Přírůstky a úbytky v zúčtovací měně</li><li>Předpokládané zůstatky měny</li><li>Celkový bankovní zůstatek v zúčtovací měně</li><li>Dnešní skutečný a předpokládaný zůstatek v měně bankovního účtu</li></ul> |
| Prognóza cashflow – všechny společnosti    | <ul><li>Přírůstky a úbytky v systémové měně</li><li>Denní souhrn prognóz</li><li>Podrobnosti o prognóze</li></ul> |
| Prognóza cashflow – aktuální společnost | <ul><li>Přírůstky a úbytky v zúčtovací měně</li><li>Denní souhrn prognóz</li><li>Podrobnosti o prognóze</li></ul> |
| Prognóza měny                     | <ul><li>Předpokládané zůstatky měny</li><li>Denní souhrn měny</li><li>Podrobnosti o prognóze</li></ul> |
| Bankovní zůstatky                         | <ul><li>Celkový bankovní zůstatek v měně systému</li><li>Zůstatek podle právnické osoby</li><li>Dnešní skutečný a předpokládaný zůstatek v měně bankovního účtu</li><li>Zůstatek podle bankovního účtu</li><li>Zůstatek podle měny</li></ul> |

## <a name="extending-the-power-bi-content"></a>Rozšíření obsahu v Power BI
Můžete poskytovat skvělé analýzy těm, kteří nejsou přihlášeni do aplikace Dynamics 365, pomocí balíčku obsahu balen dostupného ve službě Lifecycle Services. Tyto balíčky obsahu můžete upravit tak, aby zahrnovaly jiné sestavy nebo vizuály, a potom publikovat balíčky obsahu na svého klienta Power BI.com pro analýzu. 

Obsah **Přehled hotovosti** v Power BI naleznete v knihovně sdíleného majetku ve službě LCS. Další informace o stažení obsahu a jeho implementaci ve vaší organizaci naleznete v tématu [Obsah Power BI v LCS od společnosti Microsoft a vašich partnerů](../../dev-itpro/analytics/power-bi-content-microsoft-partners.md). Pokud se chcete podívat na ukázku, jak implementovat obsah Power BI, najdete informace v tématu [Obsah Power BI od společnosti Microsoft a partnerů ve službě Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) pro Office Mix.

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách

Následující tabulka zobrazuje entity, na kterých je obsah **Přehled hotovosti** v Power BI založen.

| Celek                                                                          | Obsah |
|---------------------------------------------------------------------------------|----------|
| LedgerCovLiquidityMeasurement\_Společnost                                          | Společnosti, podle kterých se filtrují sestavy |
| LedgerCovLiquidityMeasurement\_Datum                                             | Data, podle kterých se filtrují sestavy |
| LedgerCovLiquidityMeasurement\_LedgerCovForecastActual                          | Aktuální bankovní zůstatek a poslední předpokládaný bankovní zůstatek |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidity                               | Podrobnosti o předpokládaných transakcích |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany    | Souhrnné přírůstky, úbytky a zůstatek hotovosti s použitím zúčtovací měny každé společnosti |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise | Souhrnné přírůstky, úbytky a zůstatek hotovosti s použitím systémové měny pro všechny společnosti |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency            | Souhrnná čistá částka transakce a zůstatek měn pomocí měny transakce |

Tyto entity byly použity k vytvoření vypočítaných hodnot v datovém modelu. Tyto vypočtené hodnoty se poté použijí pro výpočet grafů a sestav, které se používají v obsahu **Přehled hotovosti** Power BI. Pokud chcete zahrnout další výpočty do sestav a řídicího panelu, můžete stáhnout a upravit soubor Power BI z LCS. Tento soubor představuje výchozí datový model, který byl použit k vytvoření obsahu. Po provedení změn můžete vytvořit organizační obsah a řídicí panely, které budou obsahovat vámi přidané informace.


