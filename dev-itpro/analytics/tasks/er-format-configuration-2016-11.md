--- 
title: "Vytvoření konfigurace formátu pro elektronické výkaznictví (ER)"
description: "Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit konfiguraci formátu pro elektronické výkaznictví."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: c46b222cb12d0432609c47f89afc522e02c41ab6
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-format-configuration-for-electronic-reporting-er"></a>Vytvoření konfigurace formátu pro elektronické výkaznictví (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit konfiguraci formátu pro elektronické výkaznictví. Tato konfigurace formátu definuje formát elektronických dokumentů, které jsou použity pro zpracování plateb. V tomto příkladu budete vytvářet konfiguraci formátu pro vzorovou společnost Litware, Inc. K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu Mapování modelu na vybrané zdroje dat.


## <a name="create-a-new-format-configuration"></a>Vytvoření nové konfigurace formátu
1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
2. Klikněte na Konfigurace výkaznictví.
3. Ve stromovém zobrazení vyberte možnost „Platby (zjednodušený model)“.
4. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
5. V poli Nový zadejte "Formát založený na datovém modelu PaymentModel".
6. Do pole Název zadejte „BACS (Velká Británie – fiktivní)“.
    * BACS (Velká Británie – fiktivní)  
7. Do pole Popis zadejte "Formát plateb dodavatele BACS (Velká Británie – fiktivní)".
    * Formát plateb dodavatele BACS (Velká Británie – fiktivní)  
    * Aktivní poskytovatel konfigurace se zadá automaticky v tomto poli. Tento zprostředkovatel bude moci udržovat tuto konfiguraci. Jiní poskytovatelé mohou použít tuto konfiguraci, ale nebudou moci ji spravovat.  
    * Lze definovat určitý formát elektronického dokumentu. Ponechejte toto pole prázdné, pokud chcete vybrat formát při spuštění.  
8. V poli Definice datového modelu zadejte nebo vyberte hodnotu.
9. Klepněte na možnost Vytvořit konfiguraci.
    * Byla vytvořena nová konfigurace. Verzi konceptu lze použít k ukládání formát návrhu pro správu elektronických dokumentů.  

## <a name="design-format-of-electronic-document"></a>Návrh formátu elektronického dokumentu
1. Klikněte na možnost Návrhář.
2. Klepnutím na možnost Přidat kořen otevřete dialogové okno.
3. Ve stromovém zobrazení vyberte „Společné\Soubor“.
4. Do pole Název zadejte „Xml“.
    * XML  
5. Zadejte hodnotu UTF-8 do pole Kódování.
    * UTF-8  
6. Klikněte na tlačítko OK.
7. Klepnutím na možnost Přidat otevřete dialogové okno.
8. Ve stromovém zobrazení vyberte „XML\Prvek“.
9. Do pole Název zadejte „Zpráva“.
    * Zpráva  
10. Klikněte na tlačítko OK.
11. Ve stromovém zobrazení vyberte 'Xml\Zpráva'.
12. Klepněte na Přidat prvek.
13. Do pole Název zadejte „ProcessingDate“.
    * ProcessingDate  
14. Klikněte na tlačítko OK.
15. Klepněte na Přidat prvek.
16. Do pole Název zadejte „MessageId“.
    * MessageId  
17. Klikněte na tlačítko OK.
18. Klepněte na Přidat prvek.
19. Do pole Název zadejte Platby.
    * Platby  
20. Klikněte na tlačítko OK.
21. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby'.
22. Klepněte na Přidat prvek.
23. Do pole Název zadejte „Položka“.
    * Zboží  
24. Klikněte na tlačítko OK.
25. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka'.
26. Klepnutím na možnost Přidat otevřete dialogové okno.
27. Ve stromovém zobrazení vyberte „XML\Atribut“.
28. Do pole Název zadejte „Id“.
    * ID  
29. Klikněte na tlačítko OK.
30. Klepnutím na možnost Přidat otevřete dialogové okno.
31. Ve stromovém zobrazení vyberte „XML\Prvek“.
32. Do pole Název zadejte „Dodavatel“.
    * Dodavatel  
33. Klikněte na tlačítko OK.
34. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel'.
35. Klepněte na Přidat prvek.
36. Do pole Název zadejte název.
    * Jméno  
37. Klikněte na tlačítko OK.
38. Klepněte na Přidat prvek.
39. Do pole Název zadejte „Banka“.
    * Banka  
40. Klikněte na tlačítko OK.
41. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Banka'.
42. Klepněte na Přidat prvek.
43. Do pole Název zadejte „RoutingNumber“.
    * Směrový kód  
44. Klikněte na tlačítko OK.
45. Klepněte na Přidat prvek.
46. Do pole Název zadejte „AccountNumber“.
    * AccountNumber  
47. Klikněte na tlačítko OK.
48. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel'.
49. Klepněte na tlačítko Kopírovat.
50. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka'.
51. Klepněte na tlačítko Vložit.
52. Do pole Název zadejte „Plátce“.
    * Plátce  
53. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka'.
54. Klepněte na Přidat prvek.
55. Do pole Název zadejte Měna.
    * Měna  
56. Klikněte na tlačítko OK.
57. Klepněte na Přidat prvek.
58. Do pole Název zadejte Popis.
    * popis  
59. Klikněte na tlačítko OK.
60. Klepněte na Přidat prvek.
61. Do pole Název zadejte „TransDate“.
    * TransDate  
62. Klikněte na tlačítko OK.
63. Klepněte na Přidat prvek.
64. Do pole Název zadejte „Částka“.
    * Množství  
65. Klikněte na tlačítko OK.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>Příprava součástí formátu pro mapování na prvky datového modelu
1. Ve stromové struktuře vyberte 'Xml\Zpráva\ProcessingDate'.
2. Klepnutím na možnost Přidat otevřete dialogové okno.
3. Ve stromové struktuře vyberte 'Text\DateTime'.
4. V poli Formát zadejte „rrrr-MM-dd“.
    * yyyy-MM-dd  
5. Klikněte na tlačítko OK.
6. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\TransDate'.
7. Klikněte na možnost Přidat datum a čas.
8. V poli Formát zadejte „rrrr-MM-dd“.
    * yyyy-MM-dd  
9. V poli Typ data a času vyberte 'Datum'.
10. Klikněte na tlačítko OK.
11. Ve stromové struktuře vyberte 'Xml\Zpráva\MessageId'.
12. Klepnutím na možnost Přidat otevřete dialogové okno.
13. Ve stromovém zobrazení vyberte „Text\Řetězec“.
14. Klepněte na tlačítko OK.
15. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Název'.
16. Klepněte na tlačítko Přidat řetězec.
17. Klepněte na tlačítko OK.
18. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Banka\RoutingNumber'.
19. Klepněte na tlačítko Přidat řetězec.
20. Klepněte na tlačítko OK.
21. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Banka\AccountNumber'.
22. Klepněte na tlačítko Přidat řetězec.
23. Klepněte na tlačítko OK.
24. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Plátce\Název'.
25. Klepněte na tlačítko Přidat řetězec.
26. Klepněte na tlačítko OK.
27. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Plátce\Banka\RoutingNumber'.
28. Klepněte na tlačítko Přidat řetězec.
29. Klepněte na tlačítko OK.
30. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Plátce\Banka\AccountNumber'.
31. Klepněte na tlačítko Přidat řetězec.
32. Klepněte na tlačítko OK.
33. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Měna'.
34. Klepněte na tlačítko Přidat řetězec.
35. Klepněte na tlačítko OK.
36. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Popis'.
37. Klepněte na tlačítko Přidat řetězec.
38. Klepněte na tlačítko OK.
39. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Částka'.
40. Klepněte na tlačítko Přidat řetězec.
41. Klepněte na tlačítko OK.
42. Klikněte na položku Uložit.
43. Zavřete stránku.


