---
title: Vytvoření šablon pracovní doby
description: Šablony pracovní doby definují pracovní dobu v týdnu a slouží ke generování pracovní doby pro časový úsek.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f41ae891625fea77eed6650a5bc1fb800a08ee8f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210702"
---
# <a name="create-working-time-templates"></a>Vytvoření šablon pracovní doby

[!include [banner](../../includes/banner.md)]

Šablony pracovní doby definují pracovní dobu v týdnu a slouží ke generování pracovní doby pro časový úsek. Tento postup popisuje, jak definovat šablony pracovní doby pomocí vlastností plánování pracovní doby pro zařazení časových intervalů práce. Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.

1. Přejít na Všechny pracovní prostory > Správa životního cyklu prostředků.
2. Klepněte na Šablony pracovních dob.

## <a name="create-working-time-template"></a>Vytvoření šablony pracovní doby
1. Klikněte na položku Nová.
2. Zadejte hodnotu do pole Pracovní doba.
3. Zadejte hodnotu do pole Název.
4. Rozbalte sekci Pondělí.
5. Klepněte na možnost Přidat.
6. Do pole Od zadejte čas.
    * Určete čas při zahájení práce ráno.  
7. Do pole Do zadejte čas.
    * Zadejte čas, kdy zaměstnanci mají přestávku na oběd.  
8. Klepněte na možnost Přidat.
9. Do pole Od zadejte čas.
    * Zadejte čas, kdy práci obnoví po obědě.  
10. Do pole Do zadejte čas.
    * Určete konec pracovního dne.  

## <a name="replicate-working-times-to-all-week-days"></a>Replikace pracovní doby pro všechny dny v týdnu
1. Klepněte na Kopírovat den.
    * Zkopírujte definice pracovní doby od pondělí do úterý.  
2. Klikněte na tlačítko OK.
3. Klepněte na Kopírovat den.
    * Zkopírujte definice pracovní doby od pondělí do středa.  
4. Vyberte volbu v poli Do pracovního dne.
5. Klikněte na tlačítko OK.
6. Klepněte na Kopírovat den.
    * Zkopírujte definice pracovní doby od pondělí do čtvrtka.  
7. Vyberte volbu v poli Do pracovního dne.
8. Klikněte na tlačítko OK.
9. Klepněte na Kopírovat den.
    * Zkopírujte definice pracovní doby od pondělí do pátku.  
10. Vyberte volbu v poli Do pracovního dne.
11. Klikněte na tlačítko OK.

## <a name="define-time-slots-for-special-operations"></a>Definování časových úseků pro zvláštní operace
1. Rozbalte sekci Pátek.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. V poli Vlastnosti zadejte nebo vyberte hodnotu.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. V poli Vlastnosti zadejte nebo vyberte hodnotu.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Označení víkendových dnů jako uzavřených pro výdej
1. Rozbalte sekci Sobota.
2. Vyberte možnost Ano v poli Uzavřeno pro výdej.
3. Rozbalte sekci Neděle.
4. Vyberte možnost Ano v poli Uzavřeno pro výdej.

