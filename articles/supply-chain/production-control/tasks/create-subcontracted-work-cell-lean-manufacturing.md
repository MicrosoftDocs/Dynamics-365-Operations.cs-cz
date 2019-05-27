---
title: Vytvoření subdodavatelské pracovní buňky pro lean manufacturing
description: K modelování práce subdodávky pro lean manufacturing je nutné vytvořit pracovní buňku přidruženou k dodavateli, který zajišťuje práci.
author: cvocph
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58b725af456f1a5c7f158f01ffe48a2d8cdf056b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550530"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a>Vytvoření subdodavatelské pracovní buňky pro lean manufacturing

[!include [task guide banner](../../includes/task-guide-banner.md)]

K modelování práce subdodávky pro lean manufacturing je nutné vytvořit pracovní buňku přidruženou k dodavateli, který zajišťuje práci. Pracovní buňka subdodavatele je připojena k dodavateli prostřednictvím přidružení prostředků typu Dodavatel. Pokud použijete tento záznam v ukázkové společnosti USMF, můžete vybrat účet dodavatele ID 1002 a pracoviště 1.


## <a name="create-a-vendor-resource"></a>Vytvoření prostředků dodavatele
1. Přejděte na Prostředky.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Prostředek.
4. Zadejte nějakou hodnotu do pole Popis.
5. V poli Typ vyberte možnost Dodavatel.
6. V poli Dodavatel kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.

## <a name="create-the-resource-group"></a>Vytvoření skupiny prostředků
1. Přejděte do Skupiny prostředků.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Skupina prostředků.
4. Zadejte nějakou hodnotu do pole Popis.
5. V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Vyberte pracoviště, do kterého má být přidělena pracovní buňka. Teoreticky pracoviště může představovat jedno pracoviště, které je ovládáno dodavatelem. Ale ve většině případů jsou prostředky subdodavatele pouze přidělovány k pracovišti, které si objednalo subdodavatelskou práci. Všimněte si, že vstupní a výstupní sklady pracovních buněk subdodavatele musí být na stejném pracovišti.  
6. Zadejte hodnotu do pole Pracoviště.
7. @SysTaskRecorder:_RequestClose
8. Zaškrtněte políčko Pracovní buňka nebo jeho zaškrtnutí zrušte.
9. V poli Vstupní sklad klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Vyberte sklad a umístění, které se používají k fázování materiálu pro dodavatelem řízenou pracovní buňku. V mnoha případech jsou sklad a umístění modelovány s použitím samostatného skladu pro dodavatele a jednoho místa na každou pracovní buňku.  
10. V poli Vstupní umístění klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
11. V poli Výstupní sklad klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Definujte sklad a umístění, kde se materiál zaúčtuje při zaúčtování subdodavatelských aktivit pracovní buňky. Sklad a umístění mohou být v místě dodavatele, pokud dodavatel vykáže kanbanové úlohy. Případně sklad a umístění mohou být skladovým místem příjmu, které je přidruženo k dalšímu kroku výrobního toku.  
12. V poli Výstupní umístění klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
13. Rozbalte nebo sbalte oddíl Kalendáře.
14. Klepněte na možnost Přidat.
15. V poli Kalendář kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Přidružte kalendář pracovní doby pracovní buňky ke skupině prostředků. Pro kritické zdroje doporučujeme definovat určité kalendáře, které představují přesné pracovní doby a související kapacity pracovní buňky nebo pracoviště dodavatele.  
16. Rozbalte nebo sbalte oddíl Prostředky.
17. Klepněte na možnost Přidat.
    * Skupina prostředků subdodavatelské musí mít přidružené prostředky typu Dodavatel, které odkazují skupinu prostředků k účtu dodavatele.  
18. V poli Prostředky kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Vyberte nebo zadejte zdroje dodavatele vytvořené v předchozím podúkolu.  
19. Rozbalte nebo sbalte část Kapacita pracovní buňky.
20. Klepněte na možnost Přidat.
    * Pracovní buňka musí mít určenou kapacitu. V tomto příkladu vytvoříme kapacitu prostupnosti 100 kusů pro každý standardní pracovní den.  
21. V poli Model výrobního toku klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
22. V poli Období kapacity vyberte možnost.
23. V poli Průměrné množství propustnosti zadejte číslo.
24. V poli Jednotka klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
25. Vyřešit změny jednotky.

