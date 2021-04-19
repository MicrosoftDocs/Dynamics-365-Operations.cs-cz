---
title: Řešení potíží s procesní výrobou
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s procesní výrobou.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 938820b6cd2bb470b440fea7b70124efc0faf7f8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824983"
---
# <a name="troubleshoot-process-manufacturing"></a>Řešení potíží s procesní výrobou

Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s procesní výrobou.

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a>Když použiji zařízení úkolového lístku k nahlášení částečného množství na posledním úkolu ve výrobní zakázce, automaticky se ukončí všechny předchozí úkoly na této zakázce, které mají stav Probíhá.

Toto chování je záměrné. Na stránce **Výchozí hodnoty výrobní zakázky** na kartě **Nahlásit jako dokončené** je možnost s názvem **Ukončení tech. postupu**. Pokud je toto téma nastaveno na *Ano*, deník karet postupů se zaúčtuje, když pracovník použije zařízení úkolového lístku nebo terminál úkolového lístku k nahlášení poslední operace. Tento deník označuje všechny operace jako dokončené a ukončí všechny produkční úlohy. Když je možnost **Ukončení tech. postupu** nastavena na *Ano*, systém nezohledňuje stav úlohy, který pracovník vybral, když ohlásil poslední operaci. Systém také nezvažuje, zda pracovník hlásí úplné nebo částečné množství.

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a>Když se pokusím o uzavření skladu, zobrazí se následující varovná zpráva: „Žádné provedení výpočtu zpětného účtování nákladů s datem konce odpovídajícího období %1 nebylo zaregistrováno."

Ve verzích před vydáním 10.0.13, pokud nepoužíváte tok výpočtu nákladů štíhlé výroby, zobrazí se během uzávěrky skladu následující chybová varovná zpráva:

> Chystáte se provést uzávěrku skladu s datem %1. Žádné provedení výpočtu zpětného účtování nákladů s datem konce odpovídajícího období %1 nebylo zaregistrováno. Nezapomeňte spustit výpočet zpětného účtování nákladů s datem konce odpovídajícího období %1. Ocenění zásob, náklady prodaného zboží a odchylky nemusí být správné v dílčí knize nebo hlavní knize, dokud to nebude provedeno.

Tento problém byl opraven ve verzi 10.0.13 a novější. Další informace naleznete v [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]