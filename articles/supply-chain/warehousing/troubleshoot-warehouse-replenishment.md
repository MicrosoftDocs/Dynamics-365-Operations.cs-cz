---
title: Odstraňování problémů s doplňováním skladu
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s doplňováním skladu v Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8dfb58c9156df106f58dfdc0ee2e0ef8defb9d9f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263197"
---
# <a name="troubleshoot-warehouse-replenishment"></a>Odstraňování problémů s doplňováním skladu

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s doplňováním skladu v Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a>Zobrazuje se mi následující chybová zpráva: „Pác %1 nelze odblokovat, protože má nedokončené doplňování.“

### <a name="issue-description"></a>Popis problému

Výběr práce je blokován z důvodu práce se závislým doplňováním.

### <a name="issue-resolution"></a>Řešení problému

Při použití doplňování požadavků vlny, pokud je nutné místo pro výdej doplnit, aby byla splněna zdrojový požadavek na objednávku, vytvoří systém práci s doplňováním i výdejem. Blokuje však výdej práci, dokud není dokončena doplňovací práce. Toto chování je záměrné, protože místo výdeje nebude mít dostatek zásob, dokud nebude dokončeno doplňování. Dokončete doplňovací práci a poté zpracujte výdej.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]