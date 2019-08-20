---
title: Kontrola kvality zboží
description: Toto téma vysvětluje, jak zpracovat objednávku kvality.
author: perlynne
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10acb9aadfeb11ede1d66dd525ace7b70db3bd1c
ms.sourcegitcommit: fbaccf72df82e6b6927f0c9f0d35af0ca3ecbc2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/02/2019
ms.locfileid: "1855679"
---
# <a name="inspect-the-quality-of-goods"></a>Kontrola kvality zboží

[!include [task guide banner](../../includes/task-guide-banner.md)]

Toto téma vysvětluje, jak zpracovat objednávku kvality. Tohoto průvodce můžete použít s ukázkových dat společnosti USMF. Před zahájením tohoto vzorového postupu je nutné potvrdit nákupní objednávku "000016" a zaúčtovat příjemku produktu. To způsobí automatické vytvoření objednávky kvality. Kontroly kvality obvykle provádějí pracovníci pro kontrolu kvality.


## <a name="select-a-quality-order"></a>Vyberte objednávku kvality
1. V podokně navigace přejděte na **Moduly > Řízení zásob > Periodické úlohy > Správa kvality > Objednávky kvality**.
2. Vyberte objednávku kvality, která byla vytvořena před zahájením tohoto postupu.  

## <a name="record-test-results"></a>Záznam výsledků testu
1. Vyberte **Výsledky**
2. Vyberte možnost **Upravit**.
3. V poli **Výsledné množství** zadejte číslo.
4. V poli **Výsledek** vyberte požadovaný záznam v rozevírací nabídce.  
- V tomto příkladu vychází výsledek z předem definovaného výsledku. Běžně byste vytvořili záznam s mnohem přesnějšími výsledky, jako například s velikostí nebo jinou dimenzí.  
5. Zvolte **Uložit**.
6. Zavřete stránku.

## <a name="validate-the-quality-order"></a>Ověřit objednávku kvality
1. Vyberte **Ověřit**.
2. V poli **Ověřil/a** vyberte uživatele provádějícího kontrolu z rozevírací nabídky.  
3. Klepněte na tlačítko **Vybrat**.
4. Vyberte **OK**.
5. Zavřete stránku.

