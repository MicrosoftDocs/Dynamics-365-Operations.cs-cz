---
title: Obsah přehledu hotovosti v Power BI
description: Toto téma popisuje obsah přehledu hotovosti v Microsoft Power BI. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření obsahu.
author: saraschi2
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 5dccb5c5c6c336607603dfc7a935c039e5ac4aa5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568910"
---
# <a name="cash-overview-power-bi-content"></a>Obsah přehledu hotovosti v Power BI

[!include [banner](../includes/banner.md)]

Toto téma popisuje obsah **Přehled hotovosti** v Microsoft Power BI. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření obsahu.

## <a name="overview"></a>Přehled

Obsah **Přehled hotovosti** v Power BI byl vytvořen pro jednotlivce, kteří zodpovídají za hotovost ve své organizaci. Obsah **Přehled hotovosti** v Power BI poskytuje vizibilitu vašeho cashflow. Rovněž poskytuje prognózy, které vám mohou pomoci lépe rozhodovat a tím vylepšovat stav vašeho cashflow. Můžete analyzovat hotovost podle právnické osoby, měny a bankovního účtu, abyste získali lepší pochopení k lepšímu pochopení přebytků a nedostatků.

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI

Sestavy z obsahu **Přehled hotovosti** Power BI se zobrazí v pracovních prostorech **Přehled hotovosti** a **Správa banky**.

Aby bylo možné zobrazit sestavy hotovostního toku s datem, je nutné nejprve spustit proces výpočtu prognózy pomocí funkce **Vypočítat prognózy hotovostního toku** v oblasti správy hotovosti a banky.  To je třeba dokončit pro každou společnost zahrnutou do prognózy.  Potom je nutné aktualizovat souhrnné měření LedgerCovLiquidityMeasurement na stránce **Úložiště entit**.  

Pro účely ukázky můžete přidat ukázková data prognózy hotovostního toku pomocí stránky **Generovat data** z modulu Ukázková data.  Tento skript data vloží do tabulek prognózy hotovostního toku, aby bylo možné rychle zadat informace nezbytné pro sestavy.  Tento modul je dostupný, pouze pokud máte v prostředí nasazený model sady ukázkových dat. 

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Sestavy, které jsou součástí obsahu Power BI
Následující tabulka obsahuje podrobnosti o metrikách, které jsou k dispozici na každé stránce sestavy obsahu **Přehled hotovosti** v Power BI.

| Sestava                                | Obsah |
|---------------------------------------|----------|
| Přehled hotovosti – všechny společnosti         | <ul><li>Přírůstky a úbytky v systémové měně</li><li>Předpokládané zůstatky měny</li><li>Celkový bankovní zůstatek v měně systému</li><li>Zůstatek podle právnické osoby</li><li>Dnešní skutečný a předpokládaný zůstatek v měně bankovního účtu</li></ul> |
| Přehled hotovosti – aktuální společnost       | <ul><li>Přírůstky a úbytky v zúčtovací měně</li><li>Předpokládané zůstatky měny</li><li>Celkový bankovní zůstatek v zúčtovací měně</li><li>Dnešní skutečný a předpokládaný zůstatek v měně bankovního účtu</li></ul> |
| Prognóza cashflow – všechny společnosti    | <ul><li>Přírůstky a úbytky v systémové měně</li><li>Denní souhrn prognóz</li><li>Podrobnosti o prognóze</li></ul> |
| Prognóza cashflow – aktuální společnost | <ul><li>Přírůstky a úbytky v zúčtovací měně</li><li>Denní souhrn prognóz</li><li>Podrobnosti o prognóze</li></ul> |
| Prognóza měny                     | <ul><li>Předpokládané zůstatky měny</li><li>Denní souhrn měny</li><li>Podrobnosti o prognóze</li></ul> |
| Bankovní zůstatky                         | <ul><li>Celkový bankovní zůstatek v měně systému</li><li>Zůstatek podle právnické osoby</li><li>Dnešní skutečný a předpokládaný zůstatek v měně bankovního účtu</li><li>Zůstatek podle bankovního účtu</li><li>Zůstatek podle měny</li></ul> |


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


