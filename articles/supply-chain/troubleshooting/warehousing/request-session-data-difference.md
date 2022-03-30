---
title: Neočekávaný rozdíl mezi daty žádosti a relace během testování
description: Ve výsledcích ověření úlohy aplikace skladu dojde k neočekávanému rozdílu mezi daty žádosti a relace.
author: mamuszal
ms.date: 03/11/2022
ms.topic: troubleshooting
ms.search.form: WHSValidatorRunInstance_executeRun
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mamuszal
ms.search.validFrom: 2022-03-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: da8f0506a76b0d0cc02bfc2e1bff01b4ddccb578
ms.sourcegitcommit: 941119133be1765f653d5d5270dfdf58466e1d07
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/17/2022
ms.locfileid: "8456933"
---
# <a name="unexpected-difference-between-request-and-session-data-during-testing"></a>Neočekávaný rozdíl mezi daty žádosti a relace během testování

Kód chyby: WarehouseMobileDeviceRequestInputValidationError

## <a name="symptoms"></a>Příznaky

Když používáte [architekturu pro ověřování úloh aplikace skladu](/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/warehouse-app-task-validation-rsat), validátor vrátí následující chybovou zprávu:

> Neočekávaný rozdíl mezi daty žádosti a relace. Porušen protokol XML skladu pro mobilní zařízení.REQUEST_XML_TAMPERING

## <a name="cause"></a>Příčina

K chybě dojde, když výstup posledního kroku, který byl úspěšně spuštěn v testovacím běhu, neodpovídá zaznamenanému vstupu pro další krok. Tato situace může nastat, protože validátor úlohy nepoužívá výstup předchozího kroku jako vstup pro krok následující. Místo toho používá zaznamenané XML jako vstup pro každý krok.

Ve většině případů k chybě dojde při opětovném spuštění úlohy, ale test vyžaduje některé záznamy, které byly změněny nebo odstraněny předchozím spuštěním stejné úlohy.

## <a name="resolution"></a>Řešení

Testovací běh úlohy ověření aplikace skladu není idempotentní operací, ale mění podkladová data. Proto než znovu spustíte úlohu, budete možná muset resetovat příslušná data.

1. Prohlédněte si výstupní XML posledního úspěšného testovacího kroku a určete, kde byl test ukončen.
1. Zkontrolujte svůj test a ujistěte se, že všechny požadované prodejní objednávky, převodní příkazy, pracovní záhlaví a další záznamy jsou stále přítomné a v očekávaném stavu.
1. Znovu vytvořte nebo upravte chybějící nebo upravené záznamy. Případně vytvořte nové nastavení testu a navrhněte test tak, aby používal platné existující záznamy.
