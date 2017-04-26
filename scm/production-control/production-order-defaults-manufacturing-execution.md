---
title: "Výchozí pořadí výroby při výrobě spuštění"
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70073
ms.assetid: 620944ae-3e20-444a-807e-65495f160904
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: b310e799c1ef0756291c5f7ab886531e4caf1945
ms.lasthandoff: 03/31/2017


---

# <a name="production-order-defaults-in-manufacturing-execution"></a>Výchozí pořadí výroby při výrobě spuštění

[!include[banner](../includes/banner.md)]




Měli byste pečlivě zvážit všechna nastavení na **výchozí pořadí výroby** stránky nejprve zaměstnanci provést registrací o výrobních úlohách. Pokud vaše společnost používá funkce více pracovišť, můžete nastavit různé výchozí hodnoty pro výrobní zakázky pro každý web. Výchozí nastavení pro integraci s řízením výroby se nastavují na následujících kartách na stránce **Výchozí hodnoty pro výrobní objednávku**:

-   **Hlavní** – hlavní zakázky vychází z výrobních prací v modulu Provádění výroby.
-   **Spustit** – výchozí hodnoty objednávky jsou použity při zahájení výrobní práce nebo operace.
-   **Operace** – výchozí hodnoty objednávky používané pro výrobní úlohy nebo operace, a zpětná vazba pro operace během výrobního procesu.
-   **Vykázat jako dokončené** – výchozí hodnoty objednávky používané při hlášení dokončených položek u poslední operace výrobní zakázky.
-   **Ověření množství** – výchozí hodnoty objednávky pro ověřování počátečního množství a množství zpětné vazby pro výrobní zakázky.

## <a name="types-of-production-jobs"></a>Typy výrobních prací
Na kartě **Operace** vyberte typy výrobních prací, které vyžadují registraci na stránce **Registrace práce**. Obvykle zaměstnanci provádí registrace pro nastavení a procesy. Jestliže používáte plánování práce, můžete vybrat jiné typy prací, například přepravu, které zaměstnanci rovněž musí registrovat při zpracování výrobní zakázky. **Upozornění:** zkontrolujte, zda jsou vybrány všechny důležité typy prací. V opačném případě úlohy nemusí být k dispozici pro registraci na stránce **Registrace práce**. Sjednoťte váš výběr s výběry, které jsou provedeny ve sloupci **Správa práce** na stránce **Skupiny směrování**. Pokud je vybrána **Správa práce** ve skupině směrování, typ úlohy bude ohlášen jako dokončený ve výrobní zakázce. Toto oznámení proběhne v případě, že úloha hlášena jako dokončená v modulu Provádění výroby. Když všechny úlohy typy, pro které je vybrána možnost **Správa práce**, byly ohlášeny jako dokončené v operaci, modul Provádění výroby ohlásí také operaci jako dokončenou. **Poznámka:** U některých typů prací lze hlášení provést ručně ve výrobních denících. V tomto případě vyberte **Správa práce** pro typ úlohy, ale nevybírejte typ práce k registraci na kartě **Operace** na stránce **Výchozí hodnoty pro výrobní objednávku**.

## <a name="bom-consumption-and-picking-list-journals"></a>Spotřeba kusovníku a deníky výdejek
Materiály lze nastavit tak, že se při výrobě spotřebovávají automaticky nebo ručně. Automatická spotřeba je řízena podle principu vyprazdňování, který je nastaven na řádcích kusovníku, a podle nastavení v poli **Automatická spotřeba kusovníku** ve výchozích hodnotách výrobní zakázky. Automatickou spotřebu lze nastavit tak, aby proběhla při hlášení výrobní zakázky jako zahájené nebo dokončené. Případně k tomu může dojít na úrovni úlohy při zahájení nebo dokončení úlohy.

### <a name="controlling-material-consumption-when-a-production-order-is-started"></a>Řízení spotřeby materiálu při zahájení výrobní zakázky

Spotřeba materiálu při zahájení výrobní zakázky je řízena v poli **Automatická spotřeba kusovníku** na kartě **Počáteční**. K dispozici jsou následující hodnoty:

-   **Princip vyprazdňování** – při zahájení výrobní zakázky bude množství materiálu spotřebováno podle principu vyprazdňování, který je nastaven na řádcích kusovníku výroby. Pouze řádky s materiálem, kde je princip vyprazdňování nastaven na **Počáteční**, bude spotřebován při zahájení výroby.
-   **Vždy** – množství materiálu, které je úměrné zahájenému množství, bude vždy spotřebováno.
-   **Nikdy** – množství materiálu nebude nikdy spotřebováno.

### <a name="controlling-material-consumption-when-a-production-job-is-started-or-completed"></a>Řízení spotřeby materiálu při zahájení nebo dokončení výrobní úlohy

Spotřeba materiálu při zahájení nebo dokončení výrobní úlohy je řízena v poli **Automatická spotřeba kusovníku** na kartě **Operace**. K dispozici jsou následující hodnoty:

-   **Princip vyprazdňování** – při zahájení nebo dokončení množství ve výrobní úloze bude množství materiálu spotřebováno podle principu vyprazdňování, který je nastaven na řádcích kusovníku výroby. Pouze řádky s materiálem, kde je princip vyprazdňování nastaven na **Počáteční** nebo **Dokončené** budou spotřebovány.
-   **Vždy** – množství materiálu, které je úměrné zahájenému množství v úloze, bude vždy spotřebováno.
-   **Nikdy** – množství materiálu nebude nikdy spotřebováno.

### <a name="controlling-material-consumption-when-a-production-order-is-reported-as-finished"></a>Řízení spotřeby materiálu při nahlášení výrobní zakázky jako dokončené

Spotřeba materiálu během procesu Ohlásit jako dokončené u výrobní zakázky je řízena v poli **Automatická spotřeba kusovníku** na kartě **Ohlásit jako dokončené**. K dispozici jsou následující hodnoty:

-   **Princip vyprazdňování** – když výrobní zakázka bude hlášena jako dokončená, množství materiálu spotřebováno podle principu vyprazdňování, který je nastaven na řádcích kusovníku výroby. Pouze řádky s materiálem, kde je princip vyprazdňování nastaven na **Dokončeno**, budou spotřebovány.
-   **Vždy** – množství materiálu, které je úměrné množství, které je hlášeno jako dokončené, bude vždy spotřebováno.
-   **Nikdy** – množství materiálu nebude nikdy spotřebováno.





