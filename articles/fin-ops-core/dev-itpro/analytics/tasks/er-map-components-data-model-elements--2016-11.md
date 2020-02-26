---
title: Elektronické vykazování – Mapování komponent vytvořeného formátu na prvky datového modelu (listopad 2016)
description: Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může mapovat prvky datového modelu na komponenty vytvořené konfigurace elektronického výkaznictví, která určuje formát elektronického dokumentu obchodní doménu pro platby.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 548f16034ebdf7e0f29e8e89d85aac880f6323a1
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026233"
---
# <a name="er-map-components-of-the-created-format-to-data-model-elements-november-2016"></a>Elektronické vykazování – Mapování komponent vytvořeného formátu na prvky datového modelu (listopad 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může mapovat prvky datového modelu na komponenty vytvořené konfigurace elektronického výkaznictví, která určuje formát elektronického dokumentu obchodní doménu pro platby. Tento formát bude využit později s cílem vygenerovat elektronické dokumenty pro zpracování plateb. V tomto příkladu vytvoříte konfiguraci formátu pro vzorovou společnost ‘Litware, Inc.’. Tyto kroky lze provést v každé společnosti, protože konfigurace ER jsou sdíleny všemi společnostmi. K provedení těchto kroků musíte nejprve dokončit kroky Průvodce záznamem úloh „Vytvoření konfigurace formátu“.


## <a name="select-a-format-configuration"></a>Zvolte konfiguraci formátu
1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
2. Klikněte na Konfigurace výkaznictví.
3. Ve stromovém zobrazení rozbalte možnost „Platby (zjednodušený model)“.
4. Ve stromovém zobrazení vyberte možnost „Platby (zjednodušený model)\BACS (Velká Británie – fiktivní)“.
5. Klikněte na možnost Návrhář.

## <a name="map-format-components-to-data-model-elements"></a>Mapování součástí formátu na prvky datového modelu
1. Klikněte na Rozbalit/sbalit.
2. Klikněte na kartu Mapování.
3. Ve stromovém zobrazení rozbalte „model“.
4. Ve stromové struktuře vyberte 'Xml\Zpráva\ProcessingDate\DateTime'.
5. Ve stromové struktuře zvolte 'model\ProcessingDateTime'.
6. Klikněte na možnost Vazba.
7. Ve stromové struktuře vyberte 'Xml\Zpráva\MessageId\Řetězec'.
8. Ve stromové struktuře vyberte 'model\MessageIdentification'.
9. Klikněte na možnost Vazba.
10. Ve stromovém zobrazení rozbalte „model\Platby“.
11. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Částka\Řetězec'.
12. Ve stromové struktuře zvolte 'model\Platby\InstructedAmount'.
13. Klikněte na možnost Vazba.
14. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\TransDate\DateTime'.
15. Ve stromové struktuře vyberte 'model\Platby\TransactionDate'.
16. Klikněte na možnost Vazba.
17. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Popis\Řetězec'
18. Ve stromovém zobrazení vyberte „model\Platby\Popis“.
19. Klikněte na možnost Vazba.
20. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Měna\Řetězec'
21. Ve stromovém zobrazení vyberte „model\Platby\Měna“.
22. Klikněte na možnost Vazba.
23. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Id'
24. Ve stromové struktuře vyberte 'model\Platby\End2EndID'.
25. Klikněte na možnost Vazba.
26. Ve stromovém zobrazení rozbalte „model\Platby\Věřitel“.
27. Ve stromovém zobrazení rozbalte „model\Platby\Věřitel\Účet“.
28. Ve stromovém zobrazení rozbalte „model\Platby\Věřitel\Zástupce“.
29. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Název\Řetězec'.
30. Ve stromovém zobrazení vyberte „model\Platby\Věřitel\Název“.
31. Klikněte na možnost Vazba.
32. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Banka\RoutingNumber\Řetězec'
33. Ve stromové struktuře vyberte 'model\Platby\Věřitel\Agent\RoutingNumber'.
34. Klikněte na možnost Vazba.
35. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Banka\AccountNumber\Řetězec':
36. Ve stromovém zobrazení vyberte „model\Platby\Věřitel\Účet\Číslo“.
37. Klikněte na možnost Vazba.
38. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Plátce\Název\Řetězec'
39. Ve stromovém zobrazení rozbalte „model\Platby\Dlužník“.
40. Ve stromovém zobrazení rozbalte „model\Platby\Dlužník\Účet“.
41. Ve stromovém zobrazení rozbalte „model\Platby\Dlužník\Zástupce“.
42. Ve stromovém zobrazení vyberte „model\Platby\Dlužník\Název“.
43. Klikněte na možnost Vazba.
44. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Plátce\Banka\RoutingNumber\Řetězec'
45. Ve stromové struktuře vyberte 'model\Plátce\Dlužník\Agent\RoutingNumber'.
46. Klikněte na možnost Vazba.
47. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Plátce\Banka\AccountNumber\Řetězec'
48. Ve stromovém zobrazení vyberte „model\Platby\Dlužník\Účet\Číslo“.
49. Klikněte na možnost Vazba.
50. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka'.
51. Ve stromovém zobrazení vyberte „model\Platby“.
52. Klikněte na možnost Vazba.
53. Klikněte na položku Uložit.

## <a name="validate-format-mapping"></a>Ověření mapování formátu
1. Klikněte na tlačítko Ověřit.
    * Ověřte nové mapování, abyste se ujistili, že všechny vazby jsou v pořádku.  
2. Zavřete stránku.

## <a name="change-status-of-the-current-version-of-format-configuration"></a>Změna stavu aktuální verze konfigurace formátu
V dalších krocích změníte stav konfigurace formátu ze stavu Návrh na stav Dokončeno, aby byla dostupná pro generování platebních dokumentů.  
1. Klikněte na položku Změnit stav.
2. Klikněte na tlačítko Dokončit.
3. Zadejte nějakou hodnotu do pole Popis.
    * Například 'verze 1'.  
4. Klikněte na tlačítko OK.
5. Vyberte dokončenou verzi aktuální konfigurace.
    * Všimněte si, že je konfigurace uložena jako dokončená verze 1.1: verze 1 formátu založeného na verzi 1 datového modelu.  

## <a name="define-effective-date-for-completed-version-of-format"></a>Definování data účinnosti dokončené verze formátu
Každou verzi formátu lze konfigurovat jako dostupnou pro použití od určitého data. Je-li více než jedna verze formátu aktivní ke konkrétnímu datu, k použití bude vybrán nejnovější formát (na základě čísla verze). Pro výběr správné verze se používá hodnota data relace.  

## <a name="restrict-access-to-created-format-from-companies"></a>Omezení přístupu k vytvořenému formátu ze společností
1. Rozbalte oddíl Kódy ISO zemí/oblastí.
    * Označením konkrétní země/oblasti, ve které lze formát použít, lze omezit přístup ke každému formátu. Pokud je seznam zemí/oblastí pro určitý formát prázdný, lze použít tento formát v jakékoli společnosti. Pokud jsou do tohoto seznamu zemí/oblastí vloženy některé kódy země/oblasti ISO, lze použít tento formát pouze ve společnostech, které mají primární adresu v této zemi/regionu.  

