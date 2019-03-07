---
title: Jak vytvořit jedinečný oddělovač účtové osnovy
description: V aplikaci Dynamics 365 for Finance and Operations nemůžete mít stejný oddělovač pro účtovou osnovu a hodnoty dimenze. Po upgradu je třeba změnit hodnoty oddělovače.
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e197a1b44e038a97b8bf6db692dcc2eef2bc5f7b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "335846"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Jak vytvořit jedinečný oddělovač účtové osnovy

[!include [banner](../includes/banner.md)]

V aplikaci Microsoft Dynamics AX 2012 můžete použít stejný oddělovač pro hodnoty účtové osnovy a dimenze. V aplikaci Dynamics 365 for Finance and Operations nemůžete mít stejný oddělovač pro účtovou osnovu a hodnoty dimenze. Pokud je duplicitní oddělovač, můžete ho změnit po upgradu. 

Tato funkce je k dispozici v:
- Dynamics 365 for Finance and Operations verze 8.0
- Dynamics 365 for Finance and Operations verze 7.1, KB 4094701 Nelze zadat finanční dimenze, když hodnoty dimenze obsahují oddělovač účtové osnovy
- Dynamics 365 for Finance and Operations verze 7.2 KB 4092967, Nelze zvolit dílčí projekt jako dimenzi, když formát pro dílčí projekt obsahuje oddělovač dimenzí

## <a name="update-delimiter"></a>Aktualizovat oddělovač
Pokud je v konfliktu s účtovou osnovu, lze změnit formát oddělovače účetní osnovy a formát ID projektu/dílčího projektu. Žádné další oddělovače dimenze nelze změnit. 
- Můžete změnit oddělovač účtové osnovy po upgradu na Finance and Operations v poli **parametry hlavní knihy** > **účtová osnova a dimenze** > **změnit oddělovač**. 
- Jestliže pouze konflikt s formát ID dílčího projektu/projektu, můžete změnit hodnotu do **projektu a parametrech účetnictví Správa** > **hlavní** > **změnit dílčí projekt formát**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Určení, zda prostředí vyžaduje aktualizaci oddělovače 
Pokud jsou oddělovače ve vašem upgradovaném prostředí konfliktní, může dojít k nestabilitě při zadávání hodnot v ovládacím prvku segmentované položky nebo položky řízení dimenzí. To znamená, že je třeba vždy použít vyhledávací kódy nebo plovoucí nabídku při zadávání kombinací účtů a dimenzí.
