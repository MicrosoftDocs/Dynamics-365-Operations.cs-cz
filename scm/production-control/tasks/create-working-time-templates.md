--- 
title: "Vytvoření šablon pracovní doby"
description: "Šablony pracovní doby definují pracovní dobu v týdnu a slouží ke generování pracovní doby pro časový úsek."
author: sorenva
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: ff1978f127a014e75619a4bbbb9b6ff3a3ad7c7a
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="create-working-time-templates"></a>Vytvoření šablon pracovní doby

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


