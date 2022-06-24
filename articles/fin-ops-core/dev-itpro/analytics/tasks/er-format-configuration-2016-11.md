---
title: Elektronické vykazování – Vytvoření konfigurace formátu (listopad 2016)
description: Tento článek vysvětluje, jak vytvořit konfiguraci formátu pro elektronické výkaznictví (ER).
author: NickSelin
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2617f33293c38b7f1aaa61fda7d8de06711c6727
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902647"
---
# <a name="er-create-a-format-configuration-november-2016"></a>Elektronické vykazování – Vytvoření konfigurace formátu (listopad 2016)

[!include [banner](../../includes/banner.md)]

Tento článek popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit konfiguraci formátu pro elektronické výkaznictví. Tato konfigurace formátu definuje formát elektronických dokumentů, které jsou použity pro zpracování plateb. V tomto příkladu budete vytvářet konfiguraci formátu pro vzorovou společnost Litware, Inc. K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Mapování modelu na vybrané zdroje dat".


## <a name="create-a-new-format-configuration"></a>Vytvoření nové konfigurace formátu
1. Přejděte do části **Správa organizace > Pracovní prostory > Elektronické výkaznictví**.
2. Klikněte na **Konfigurace výkaznictví**.
3. Ve stromovém zobrazení vyberte možnost **Platby (zjednodušený model)**.
4. Kliknutím na možnost **Vytvořit konfiguraci** otevřete dialogové okno.

 > [!NOTE]
 > Pokud se možnost **Vytvořit konfiguraci** nezobrazuje, musíte povolit režim návrhu na stránce **Parametry elektronického výkaznictví**. 
 
5. V poli **Nový** zadejte **Formát založený na datovém modelu PaymentModel**.
6. Do pole **Název** zadejte **BACS (Velká Británie – fiktivní)**.
7. Do pole **Popis** zadejte **Formát plateb dodavatele BACS (Velká Británie – fiktivní)**.
    * Aktivní poskytovatel konfigurace se zadá automaticky v tomto poli. Tento zprostředkovatel bude moci udržovat tuto konfiguraci. Jiní poskytovatelé mohou použít tuto konfiguraci, ale nebudou moci ji spravovat.  
    * Lze definovat určitý formát elektronického dokumentu. Ponechejte toto pole prázdné, pokud chcete vybrat formát při spuštění.  
8. V poli **Definice datového modelu** zadejte nebo vyberte hodnotu.
9. Klepněte na možnost **Vytvořit konfiguraci**. Byla vytvořena nová konfigurace. Verzi konceptu lze použít k ukládání formát návrhu pro správu elektronických dokumentů.  

## <a name="design-the-format-of-an-electronic-document"></a>Návrh formátu elektronického dokumentu
1. Klikněte na možnost **Návrhář**.
2. Klepnutím na možnost **Přidat kořen** otevřete dialogové okno.
3. Ve stromovém zobrazení vyberte **Společné\Soubor**.
4. Do pole **Název** zadejte **Xml**.
5. Zadejte hodnotu **UTF-8** do pole **Kódování**.
6. Klikněte na tlačítko **OK**.
7. Klikněte na položku **Přidat**.
8. Ve stromovém zobrazení vyberte **XML\Element**.
9. Do pole **Název** zadejte **Zpráva**.
10. Klikněte na tlačítko **OK**.
11. Ve stromovém zobrazení vyberte **Xml\Message**.
12. Klepněte na **Přidat element**.
13. Do pole **Název** napište **ProcessingDate**.
14. Klikněte na tlačítko **OK**.
15. Klepněte na **Přidat element**.
16. Do pole Název napište **MessageId**.
17. Klikněte na tlačítko **OK**.
18. Klepněte na **Přidat element**.
19. Do pole **Název** napište **Payments**.
20. Klikněte na tlačítko **OK**.
21. Ve stromové struktuře vyberte **Xml\Message\Payments**.
22. Klepněte na **Přidat element**.
23. Do pole **Název** napište **Item**.
24. Klikněte na tlačítko **OK**.
25. Ve stromové struktuře vyberte **Xml\Message\Payments\Item**.
26. Klikněte na položku **Přidat**.
27. Ve stromovém zobrazení vyberte **XML\Attribute**.
28. Do pole Název zadejte **Id**.
29. Klikněte na tlačítko **OK**.
30. Klikněte na položku **Přidat**.
31. Ve stromovém zobrazení vyberte **XML\Element**.
32. Do pole Název zadejte **Vendor**.
33. Klikněte na tlačítko **OK**.
34. Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor**.
35. Klepněte na **Přidat element**.
36. Do pole Název zadejte **Name**.
37. Klikněte na tlačítko **OK**.
38. Klepněte na **Přidat element**.
39. Do pole **Název** zadejte **Bank**.
40. Klikněte na tlačítko **OK**.
41. Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor\Bank**.
42. Klepněte na **Přidat element**.
43. Do pole **Název** zadejte **RoutingNumber**.
44. Klikněte na tlačítko **OK**.
45. Klepněte na **Přidat element**.
46. Do pole **Název** zadejte **AccountNumber**.
47. Klikněte na tlačítko **OK**.
48. Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor**.
49. Klepněte na tlačítko **Kopírovat**.
50. Ve stromové struktuře vyberte **Xml\Message\Payments\Item**.
51. Klepněte na tlačítko **Vložit**.
52. Do pole **Název** zadejte **Payer**.
53. Ve stromové struktuře vyberte **Xml\Message\Payments\Item**.
54. Klepněte na **Přidat element**.
55. Do pole **Název** zadejte **Currency**.
56. Klikněte na tlačítko **OK**.
57. Klepněte na **Přidat element**.
58. Do pole **Název** zadejte **Description**.
59. Klikněte na tlačítko **OK**.
60. Klepněte na **Přidat element**.
61. Do pole Název zadejte **TransDate**.
62. Klikněte na tlačítko **OK**.
63. Klepněte na **Přidat element**.
64. Do pole Název zadejte **Amount**.
65. Klikněte na tlačítko **OK**.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>Příprava součástí formátu pro mapování na prvky datového modelu
1. Ve stromové struktuře vyberte **Xml\Message\ProcessingDate**.
2. Kliknutím na **Přidat** otevřete dialogové okno pro přetažení.
3. Ve stromové struktuře vyberte **Text\DateTime**.
4. Do pole **Formát** zadejte **yyyy-MM-dd**.
5. Klikněte na tlačítko **OK**.
6. Ve stromové struktuře vyberte **Xml\Message\Payments\Item\TransDate**.
7. Klikněte na možnost **Přidat DateTime**.
8. Do pole **Formát** zadejte **yyyy-MM-dd**.
9. V poli **DateTime** vyberte **Date**.
10. Klikněte na tlačítko **OK**.
11. Ve stromové struktuře vyberte **Xml\Message\MessageId**.
12. Kliknutím na **Přidat** otevřete dialogové okno pro přetažení.
13. Ve stromovém zobrazení vyberte **Text\String**.
14. Klikněte na tlačítko **OK**.
15. Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor\Name**.
16. Klikněte na **Přidat řetězec**.
17. Klikněte na tlačítko **OK**.
18. Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.
19. Klikněte na **Přidat řetězec**.
20. Klikněte na tlačítko **OK**.
21. Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.
22. Klikněte na **Přidat řetězec**.
23. Klikněte na tlačítko **OK**.
24. Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Payer\Name**.
25. Klikněte na **Přidat řetězec**.
26. Klikněte na tlačítko **OK**.
27. Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.
28. Klikněte na **Přidat řetězec**.
29. Klikněte na tlačítko **OK**.
30. Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.
31. Klikněte na **Přidat řetězec**.
32. Klikněte na tlačítko **OK**.
33. Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Currency**.
34. Klikněte na **Přidat řetězec**.
35. Klikněte na tlačítko **OK**.
36. Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Description**.
37. Klikněte na **Přidat řetězec**.
38. Klikněte na tlačítko **OK**.
39. Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Amount**.
40. Klikněte na **Přidat řetězec**.
41. Klikněte na tlačítko **OK**.
42. Klikněte na tlačítko **Uložit**.
43. Zavřete stránku.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]