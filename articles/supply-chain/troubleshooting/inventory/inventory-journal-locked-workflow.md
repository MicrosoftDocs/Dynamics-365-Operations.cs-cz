---
title: Deník zásob je uzamčen a dávková úloha workflow nefunguje
description: Jeden z vašich deníků zásob je uzamčen nějakou operací a není uvolněn
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b21ec2e2b3b8546dcb138422c5540053392c179
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475769"
---
# <a name="your-inventory-journal-is-locked-and-the-workflow-batch-job-doesnt-work"></a>Deník zásob je uzamčen a dávková úloha workflow nefunguje

## <a name="symptoms"></a>Příznaky

Jeden z vašich deníků zásob je uzamčen nějakou operací a není uvolněn. Například pokud během zaúčtování dojde k neznámé chybě (což je operace uzamčení systému), deník může zůstat ve stavu uzamčeného systému. V tomto případě obslužná rutina pracovní položky pracovního postupu vyvolá chybu, zatímco provede ověření zámku.

## <a name="resolution"></a>Řešení

Přihlaste se k instanci serveru SQL Server pro Supply Chain Management a zkontrolujte, zda je **InventJournalTable.SystemBlocked** nastaven na *1*. Pokud ano, ujistěte se, že deník by neměl být v uzamčeném stavu, a poté resetujte **InventJournalTable.SystemBlocked** na *0*.
