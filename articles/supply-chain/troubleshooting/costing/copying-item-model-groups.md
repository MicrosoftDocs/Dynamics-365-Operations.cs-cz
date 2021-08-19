---
title: Chybí nastavení pole při kopírování skupin modelů položek do jiné právnické osoby
description: Chybí nastavení pole při kopírování skupin modelů položek do jiné právnické osoby.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 128caead04cf467c65a50bc6cd2f9e76e318f536b7eafa7972ffc1b5da5bceba
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738836"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a>Chybí nastavení pole při kopírování skupin modelů položek do jiné právnické osoby

Číslo článku znalostní báze: 4612800

## <a name="symptoms"></a>Příznaky

Když kopírujete skupiny modelů položek do jiné právnické osoby (společnosti) pomocí entity *Zásady skupinových zásob modelu položky*, některá nastavení pole (například model a popis zásob) chybí v nové skupině modelů v cílové právnické osobě.

## <a name="resolution"></a>Rozlišení

Chcete-li vytvořit úplnou kopii skupiny modelů položek do jiné právnické osoby, musíte také vybrat obě zásady zásob skupiny modelů položek (`InventInventoryPolicyEntity`) a zásady převzetí toků nákladů (`InventCostFlowAssumptionPolicyEntity`), které jsou přidruženy ke skupině modelů položek.
