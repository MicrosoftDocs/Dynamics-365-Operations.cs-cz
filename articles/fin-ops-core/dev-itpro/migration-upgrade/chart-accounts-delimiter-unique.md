---
title: Jak vytvořit jedinečný oddělovač účtové osnovy
description: Toto téma vysvětluje, proč nemůžete mít stejný oddělovač pro účtovou osnovu a hodnoty dimenze. Po upgradu je třeba změnit hodnoty oddělovače.
author: panolte
ms.date: 04/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 6081a62077f1fc6b6920991ed6faae667c25a47c
ms.sourcegitcommit: e8a2a1e34fa48a42afac9724828f4ec72b6d7085
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2022
ms.locfileid: "8573611"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Jak vytvořit jedinečný oddělovač účtové osnovy

[!include [banner](../includes/banner.md)]

V aplikaci Microsoft Dynamics AX 2012 můžete použít stejný oddělovač pro hodnoty účtové osnovy a dimenze. V aktuálních verzích finančních a provozních aplikací nemůžete mít stejný oddělovač pro účtovou osnovu a názvy či hodnoty dimenze. Pokud je duplicitní oddělovač, můžete ho změnit po upgradu. 

## <a name="update-delimiter"></a>Aktualizovat oddělovač
Pokud je v konfliktu s účtovou osnovu, lze změnit formát oddělovače účetní osnovy a formát ID projektu/dílčího projektu. Žádné další oddělovače dimenze nelze změnit. 
- Můžete změnit oddělovač účtové osnovy po upgradu v poli **parametry hlavní knihy** > **účtová osnova a dimenze** > **změnit oddělovač**. 
- Jestliže pouze konflikt s formát ID dílčího projektu/projektu, můžete změnit hodnotu do **projektu a parametrech účetnictví Správa** > **hlavní** > **změnit dílčí projekt formát**. 

### <a name="other-considerations"></a>Ostatní úvahy
Podobně jako ID projektu/dílčího projektu by žádné další záznamy hlavních dat používané jako finanční dimenze, jako jsou dodavatelé nebo zákazníci, neměly mít hodnoty ID účtu, které používají stejný znak jako oddělovač účtové osnovy. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Určení, zda prostředí vyžaduje aktualizaci oddělovače 
Pokud jsou oddělovače ve vašem upgradovaném prostředí konfliktní, může dojít k nestabilitě při zadávání hodnot v ovládacím prvku segmentované položky nebo položky řízení dimenzí. To znamená, že je třeba vždy použít vyhledávací kódy nebo plovoucí nabídku při zadávání kombinací účtů a dimenzí.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
