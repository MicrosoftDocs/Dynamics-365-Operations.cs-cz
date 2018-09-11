---
title: "Jak udělat oddělovač účtové osnovy jedinečným"
description: "V aplikaci Dynamics 365 for Finance and Operations nemůžete mít stejný oddělovač pro účtovou osnovu a hodnoty dimenze. Po upgradu je třeba změnit hodnoty oddělovače."
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e197a1b44e038a97b8bf6db692dcc2eef2bc5f7b
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---

# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Jak udělat oddělovač účtové osnovy jedinečným

[!include [banner](../includes/banner.md)]

V aplikaci Microsoft Dynamics AX 2012 můžete použít stejný oddělovač pro hodnoty účtové osnovy a dimenze. V aplikaci Dynamics 365 for Finance and Operations nemůžete mít stejný oddělovač pro účtovou osnovu a hodnoty dimenze. Pokud je duplicitní oddělovač, můžete ho změnit po upgradu. 

Tato funkce je k dispozici v:
- Dynamics 365 for Finance and Operations verze 8.0
- Dynamics 365 for Finance and Operations 7.1 KB 4094701 Nelze zadat finanční dimenze, když hodnoty dimenze obsahují oddělovač účtové osnovy
- Dynamics 365 for Finance and Operations verze 7.2 KB 4092967 Nelze zvolit dílčí projekt jako dimenzi, když formát pro dílčí projekt obsahuje oddělovač dimenzí

## <a name="update-delimiter"></a>Aktualizovat oddělovač
Pokud je v konfliktu s účtovou osnovu, lze změnit formát oddělovače účetní osnovy a formát ID projektu/dílčího projektu. Žádné další oddělovače dimenze nelze změnit. 
- Můžete změnit oddělovač účtové osnovy po upgradu na Finance and Operations v poli **parametry hlavní knihy** > **účtová osnova a dimenze** > **změnit oddělovač**. 
- Jestliže pouze konflikt s formát ID dílčího projektu/projektu, můžete změnit hodnotu do **projektu a parametrech účetnictví Správa** > **hlavní** > **změnit dílčí projekt formát**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Určení, zda prostředí vyžaduje aktualizaci oddělovače 
Pokud jsou oddělovače ve vašem upgradovaném prostředí konfliktní, může dojít k nestabilitě při zadávání hodnot v ovládacím prvku segmentované položky nebo položky řízení dimenzí. To znamená, že je třeba vždy použít vyhledávací kódy nebo plovoucí nabídku při zadávání kombinací účtů a dimenzí.
