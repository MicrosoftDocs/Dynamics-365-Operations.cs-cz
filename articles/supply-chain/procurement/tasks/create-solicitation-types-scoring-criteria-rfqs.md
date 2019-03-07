---
title: Vytvoření typů oslovení a kritérií hodnocení pro požadavky na nabídku
description: Tato příručka popisuje způsob vytvoření typu oslovení a jeho přiřazení k metodě hodnocení.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14fd7d0bfa17427883f97c5e0a72044016d4965e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "344609"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a>Vytvoření typů oslovení a kritérií hodnocení pro požadavky na nabídku

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato příručka popisuje způsob vytvoření typu oslovení a jeho přiřazení k metodě hodnocení. Rovněž zobrazuje způsob použití typu oslovení pro požadavek na nabídku, který stanoví výchozí metodu hodnocení. Tyto úkoly obvykle provádějí vedoucí nákupu. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat. Před zahájením je nutné mít k dispozici metodu hodnocení.


## <a name="create-a-solicitation-type"></a>Vytvořit nový typ oslovení
1. Přejděte na Zásobování a zdroje > Nastavení > Požadavek na nabídku > Typ oslovení.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Název.
4. Zadejte nějakou hodnotu do pole Popis.
5. V poli Metoda hodnocení vyberte metodu hodnocení, kterou chcete pro tento typ oslovení použít.
6. Klikněte na položku Uložit.
7. Zavřete stránku.

## <a name="use-the-solicitation-type"></a>Použití typu oslovení
1. Přejděte na Zásobování a zdroje > Požadavky na nabídky > Všechny požadavky na nabídky.
2. Klikněte na položku Nová.
3. V poli Typ oslovení vyberte typ oslovení, který jste právě vytvořili. 
    *   
4. Klikněte na tlačítko OK.
5. Klikněte na Kritéria hodnocení.
    * Zobrazená kritéria hodnocení jsou ta z metody hodnocení, která je přidružena k typu oslovení. Na této stránce je možné přidat nebo odstranit kritérií. Dále je možné přidat nová kritéria kopírováním z jiné metody hodnocení.  
6. Klikněte na Kopírovat kritéria.
7. V poli Metoda hodnocení zadejte nebo vyberte hodnotu.
8. Klikněte na tlačítko OK.
9. Zavřete stránku.

