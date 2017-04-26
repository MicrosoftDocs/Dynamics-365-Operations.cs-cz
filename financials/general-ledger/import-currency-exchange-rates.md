---
title: "Importovat směnné kurzy měn"
description: "Jestliže právnická osoba obdržela faktury v cizí měně, je nutné převést cizí měny do místní měny. To znamená, že jsou potřebné aktuální směnné kurzy pro různé měny. Toto téma obsahuje přehled požadovaných nastavení a zpracování pro import směnné kurzy odkaz zveřejněn prostřednictvím Internetu poskytovatele směnných kurzů, jako je Evropská centrální banka a centrální banky Ruska."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf66a1b1c9314b454223274810a21913d54b702d
ms.lasthandoff: 03/31/2017


---

# <a name="import-currency-exchange-rates"></a>Importovat směnné kurzy měn

[!include[banner](../includes/banner.md)]


Jestliže právnická osoba obdržela faktury v cizí měně, je nutné převést cizí měny do místní měny. To znamená, že jsou potřebné aktuální směnné kurzy pro různé měny. Toto téma obsahuje přehled požadovaných nastavení a zpracování pro import směnné kurzy odkaz zveřejněn prostřednictvím Internetu poskytovatele směnných kurzů, jako je Evropská centrální banka a centrální banky Ruska.

Následující oddíly popisují tok informací, které slouží pro nastavení a zpracování importu směnných kurzů.

## <a name="configure-an-exchange-rate-provider"></a>Konfigurace poskytovatele směnného kurzu
Lze importovat směnné kurzy, musíte nastavit informace vyžadované zprostředkovatelů, kteří nabízejí směnných kurzů. Použití **konfigurace zprostředkovatelů směnného kurzu** stránku pro výběr poskytovatele směnných kurzů. Některé poskytovatele směnných kurzů jsou zahrnuty v demo datech v 365 Microsoft Dynamics pro operace. V následující tabulce je uveden popis ovládacích prvků na této stránce.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field** | **Description**                                                                                                                                                                                                             |
| **Name**  | Název poskytovatele směnného kurzu.                                                                                                                                                                                     |
| **Klíč**   | Jedinečný identifikátor součásti všech konfiguračních informací požadovaný poskytovatelem. Tyto informace je automaticky přidán pro každého poskytovatele směnného kurzu přidáte klepnutím **přidat** tlačítko. |
| **Value** | Informace pro každý klíč. Tyto informace přidány pro každého poskytovatele směnného kurzu přidáte klepnutím **přidat** tlačítko.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Importovat směnné kurzy měn
Import směnných kurzů ze zdroje zprostředkovatelů směnného kurzu a jejich nastavení **směnné kurzy** stránky. Použití **importovat směnné kurzy** stránky, chcete-li importovat směnné kurzy. Následující tabulka obsahuje popis polí, které jsou nutné k dokončení procesu importu.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field**                              | **Description**                                                                                                                                                                                                                                                                                                                                                             |
| **Exchange rate type**                 | Typ směnného kurzu.                                                                                                                                                                                                                                                                                                                                                      |
| **Exchange rate provider**             | Poskytovatele směnného kurzu.                                                                                                                                                                                                                                                                                                                                                  |
| **Import as of**                       | Tento parametr řídí, zda mají být importovány, k dnešnímu datu nebo období. Pokud chcete použít časové období, zadejte nebo vyberte počáteční a koncové datum.                                                                                                                                                                                                                |
| **Create necessary currency pairs**    | Toto zaškrtávací políčko řídí automatické vytváření dvojic měn Pokud neexistuje páry měn, které jsou importovány. Tato možnost nemusí být k dispozici pro některé poskytovatele.                                                                                                                                                                                               |
| **Override existing exchange rates**   | Toto zaškrtávací políčko spravuje aktualizace stávající směnný kurz pro měnu pár směnný kurz k určitému datu již existuje. Pokud toto políčko není zaškrtnuté, směnný kurz pro konkrétní data importována, pokud již existuje jiný směnný kurz.                                                                                       |
| **Prevent import on national holiday** | Toto zaškrtávací políčko řídí import směnného kurzu k datu, který je státní svátek. Například pokud vyberte toto zaškrtávací políčko a používat jako poskytovatele směnného kurzu Evropské centrální banky, systém nebude aktualizace směnný kurz svátek vztahující se k aktuální právnické osobě. Tato možnost nemusí být k dispozici pro některé poskytovatele. |






