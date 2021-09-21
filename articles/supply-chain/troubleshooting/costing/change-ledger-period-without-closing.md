---
title: Varování nebo chyby při změně stavu období hlavní knihy bez uzávěrky zásob
description: Varování nebo chyby při změně stavu období hlavní knihy bez uzávěrky zásob
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 05851753e29da75f014d2cc77e2b8df259620eee
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475782"
---
# <a name="warnings-or-errors-on-changing-ledger-period-status-without-closing-inventory"></a>Varování nebo chyby při změně stavu období hlavní knihy bez uzávěrky zásob

Společnost Microsoft zavedla následující ověření, aby zabránila problémům způsobeným nesprávným procesem na konci období kolem výpočtu nákladů. Pokud narazíte na některou z následujících chybových zpráv, podívejte se na [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3) ohledně informací o řešení těchto problémů.

- Chystáte se provést přepočet s datem %1 (10-02-2019). Poslední registrovaný přepočet byl proveden v předchozím období s datem %2 (20-01-2019). Žádné provedení uzávěrky skladu s datem konce odpovídajícího období %3 (31-01-2019) nebylo zaregistrováno. Nezapomeňte provést uzávěrku skladu k datu konce odpovídajícího období %3 (31-01-2019). Ocenění zásob, náklady prodaného zboží a odchylky nemusí být správné v dílčí knize nebo hlavní knize, dokud to nebude provedeno.

- Chystáte se změnit stav období hlavní knihy %1 na %2. Žádné provedení uzávěrky skladu s datem konce odpovídajícího období %3 nebylo zaregistrováno. Proveďte prosím uzávěrku skladu k datu konce odpovídajícího období %3 před změnou stavu. Ocenění zásob, náklady prodaného zboží a odchylky nemusí být správné v dílčí knize nebo hlavní knize, dokud to nebude provedeno. Hlášeno z právnické osoby %4. Prozatím je to informační, ale v budoucnu budete muset provést takovou akci.

- Účetní struktura %1 byla změněna. Jeden nebo více hlavních účtů %2 již neexistuje. Tyto hlavní účty jsou vyžadovány %3 s datem %4. Přidejte tyto hlavní účty do účetní struktury %1, než budete moci obnovit úlohu %3. Prozatím je to informační, ale v budoucnu budete muset provést takovou akci.

- Chystáte se provést uzávěrku skladu s datem %1 (31-01-2019). Žádné provedení výpočtu zpětného účtování nákladů s datem konce odpovídajícího období %2 (31-01-2019) nebylo zaregistrováno. Nezapomeňte spustit výpočet zpětného účtování nákladů s datem konce odpovídajícího období %3 (31-01-2019). Ocenění zásob, náklady prodaného zboží a odchylky nemusí být správné v dílčí knize nebo hlavní knize, dokud to nebude provedeno.

- Chystáte se provést výpočet zpětného účtování nákladů s datem %1 (28-02-2019). Poslední registrovaný výpočet zpětného účtování nákladů byl proveden v předchozím období s datem %2 (31-01-2019). Žádné provedení uzávěrky skladu s datem konce odpovídajícího období %3 (31-01-2019) nebylo zaregistrováno.

Nezapomeňte provést uzávěrku skladu k datu konce odpovídajícího období %3 (31-01-2019). Ocenění zásob, náklady prodaného zboží a odchylky nemusí být správné v dílčí knize nebo hlavní knize, dokud nebude uzávěrka skladu provedena.