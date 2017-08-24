--- 
title: "Návrh datového modelu pro určitou doménu pro elektronické výkaznictví (ER)"
description: "Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit novou konfiguraci pro elektronické výkaznictví, která obsahuje model dat pro elektronické platební doklady."
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: bf727b63ed86e7cc26d4fca630d97af88abb1804
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="design-a-domain-specific-data-model-for-electronic-reporting-er"></a>Návrh datového modelu pro určitou doménu pro elektronické výkaznictví (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit novou konfiguraci pro elektronické výkaznictví, která obsahuje model dat pro elektronické platební doklady. Tento datový model se použije později jako zdroj dat při vytvoření formátu pro platební doklady.



V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace ER se sdílí mezi společnostmi. K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".

1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
    * Vyberte poskytovatele konfigurace pro vzorovou společnost Litware, Inc. Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".  
2. Klikněte na Konfigurace výkaznictví.
    * Vytvoříte konfiguraci, která obsahuje model dat pro elektronické platební doklady. Tento datový model se použije později jako zdroj dat při vytvoření formátu pro platební doklady.  

## <a name="create-a-new-data-model-configuration"></a>Vytvoření nové konfigurace datového modelu
1. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
2. V poli Název zadejte Platby (zjednodušený model).
    * Platby (zjednodušený model)  
3. V poli Popis zadejte „Konfigurace modelu platby“.
    * Konfigurace modelu platby  
    * Aktivní poskytovatel konfigurace se zadá automaticky v tomto poli. Tento zprostředkovatel bude moci udržovat tuto konfiguraci. Jiní poskytovatelé mohou použít tuto konfiguraci, ale nebudou moci ji spravovat.  
4. Klepnutím na tlačítko Dokončit konfiguraci dokončíte vytvoření konfigurace

## <a name="create-a-data-model"></a>Vytvoření datového modelu
    * Vytváříte nový datový model pro vybranou konfiguraci. Tato verze konfigurace bude mít stav Koncept.  
1. Klikněte na možnost Návrhář.

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a>Definování struktury strany účastnící se v platebním procesu
1. Kliknutím na možnost Nový otevřete dialogové okno.
2. Do pole Název zadejte 'Strana'.
    * Strana  
3. Klepněte na možnost Přidat.
4. Kliknutím na možnost Nový otevřete dialogové okno.
5. Do pole Název zadejte název.
    * Jméno  
6. V poli Typ položky vyberte Řetězec.
7. Klepněte na možnost Přidat.
8. Do pole Najít zadejte 'Strana'.
    * Strana  
9. Klikněte na Vyhledat předchozí.

## <a name="define-the-bank-structure-for-this-model"></a>Definování struktury banky pro tento model
1. Kliknutím na možnost Nový otevřete dialogové okno.
2. Do pole Název zadejte hodnotu Agent.
    * Zástupce  
3. V poli Typ položky vyberte Záznam.
4. Klepněte na možnost Přidat.
5. V poli Popis zadejte 'Finanční instituce (například banka) obsluhující účet pro stranu (dlužník/věřitel).'.
    * Finanční instituce (například banka) obsluhující účet pro stranu (dlužníka/věřitele).  
6. Kliknutím na možnost Nový otevřete dialogové okno.
7. Do pole Název zadejte název.
    * Jméno  
8. V poli Typ položky vyberte Řetězec.
9. Klepněte na možnost Přidat.
10. Kliknutím na možnost Nový otevřete dialogové okno.
11. Do pole Název zadejte SWIFT.
    * SWIFT  
12. Klepněte na možnost Přidat.
13. Do pole Popis zadejte Identifikační kód banky.
    * Identifikační kód banky  
14. Kliknutím na možnost Nový otevřete dialogové okno.
15. Do pole Název zadejte „RoutingNumber“.
    * Směrový kód  
16. Klepněte na možnost Přidat.
17. Do pole Popis zadejte 'Směrový kód'.
    * Směrový kód banky  
18. Klikněte na Vyhledat předchozí.

## <a name="define-the-bank-account-structure-for-this-model"></a>Definování struktury bankovního účtu pro tento model
1. Kliknutím na možnost Nový otevřete dialogové okno.
2. Do pole Název zadejte Účet.
    * Účet  
3. V poli Typ položky vyberte Záznam.
4. Klepněte na možnost Přidat.
5. Do pole Popis zadejte 'Identifikace účtu strany ve finanční instituci (například bance).'.
    * Identifikace účtu strany ve finanční instituci (například bance).  
6. Kliknutím na možnost Nový otevřete dialogové okno.
7. Do pole Název zadejte Měna.
    * Měna  
8. V poli Typ položky vyberte Řetězec.
9. Klepněte na možnost Přidat.
10. Do pole Popis zadejte Kód měny.
    * Kód měny  
11. Kliknutím na možnost Nový otevřete dialogové okno.
12. Do pole Název zadejte Číslo.
    * Počet  
13. Klepněte na možnost Přidat.
14. Kliknutím na možnost Nový otevřete dialogové okno.
15. Do pole Název zadejte IBAN.
    * KÓD IBAN  
16. Klepněte na možnost Přidat.
17. Do pole Popis zadejte 'Číslo IBAN (International Bank Account Number)'.
    * Číslo IBAN (International Bank Account Number)  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a>Definování struktury platební zprávy pro platby typu převod kreditu
1. Kliknutím na možnost Nový otevřete dialogové okno.
2. Do pole Nový uzel zadejte Kořen modelu.
3. Zadejte hodnotu CustomerCreditTransferInitiation do pole Název.
    * CustomerCreditTransferInitiation  
4. Klepněte na možnost Přidat.
5. Do pole Najít zadejte hodnotu 'CustomerCreditTransferInitiation'.
    * CustomerCreditTransferInitiation  
6. Klikněte na Vyhledat předchozí.
7. Kliknutím na možnost Nový otevřete dialogové okno.
8. Do pole Název zadejte „MessageIdentification“.
    * MessageIdentification  
9. Klepněte na možnost Přidat.
10. V poli Popis zadejte Odkaz Point to Point tak, jak byl přiřazen přikazující straně a odeslán další straně k identifikaci zprávy.
    * Odkaz Point to Point tak, jak byl přiřazen přikazující straně a odeslán další straně k identifikaci zprávy.  
11. Kliknutím na možnost Nový otevřete dialogové okno.
12. Do pole Název zadejte „ProcessingDateTime“.
    * ProcessingDateTime  
13. V poli Typ položky vyberte Datum a čas.
14. Klepněte na možnost Přidat.
15. Do pole Popis zadejte 'Datum a čas, kdy byla platební zpráva vytvořena.'.
    * Datum a čas, kdy byla platební zpráva vytvořena.  
16. Kliknutím na možnost Nový otevřete dialogové okno.
    * Definování struktury platební transakce pro tento model.  
17. Do pole Název zadejte Platby.
    * Platby  
18. V poli Typ položky vyberte Seznam záznamů.
19. Klepněte na možnost Přidat.
20. Do pole Popis zadejte Řádky platby pro aktuální zprávu.
    * Řádky platby pro aktuální zprávu  
21. Kliknutím na možnost Nový otevřete dialogové okno.
22. Do pole Název zadejte Věřitel.
    * Věřitel  
23. V poli Typ položky vyberte Záznam.
24. Klepněte na možnost Přidat.
25. V poli Popis zadejte Strana, pro kterou je peněžní částka splatná.
    * Strana, pro kterou je peněžní částka splatná.  
26. Klikněte na možnost Přepnout odkaz položky.
27. Do pole Najít zadejte 'Strana'.
    * Strana  
28. Klikněte na Najít další.
29. Klikněte na tlačítko OK.
30. Do pole Najít zadejte 'Platby'.
    * Platby  
31. Klikněte na Najít další.
32. Kliknutím na možnost Nový otevřete dialogové okno.
33. Do pole Název zadejte Dlužník.
    * Dlužník  
34. Klepněte na možnost Přidat.
35. V poli Popis zadejte Strana vlastnící finanční částku pro (konečného) věřitele.
    * Strana vlastnící finanční částku pro (konečného) věřitele.  
36. Klikněte na možnost Přepnout odkaz položky.
37. Do pole Najít zadejte 'Strana'.
    * Strana  
38. Klikněte na Najít další.
39. Klikněte na tlačítko OK.
40. Klikněte na Najít další.
41. Kliknutím na možnost Nový otevřete dialogové okno.
42. Do pole Název zadejte Popis.
    * popis  
43. V poli Typ položky vyberte Řetězec.
44. Klepněte na možnost Přidat.
45. Kliknutím na možnost Nový otevřete dialogové okno.
46. Do pole Název zadejte Měna.
    * Měna  
47. Klepněte na možnost Přidat.
48. Do pole Popis zadejte Kód měny.
    * Kód měny  
49. Kliknutím na možnost Nový otevřete dialogové okno.
50. Do pole Název zadejte Datum transakce.
    * Datum transakce  
51. V poli Typ položky vyberte Datum.
52. Klepněte na možnost Přidat.
53. Do pole Popis zadejte 'Datum transakce'.
    * Datum transakce  
54. Kliknutím na možnost Nový otevřete dialogové okno.
55. Do pole Název zadejte Požadovaná částka.
    * Požadovaná částka  
56. V poli Typ položky vyberte Reálný.
57. Klepněte na možnost Přidat.
58. V poli Popis uveďte Peněžní částka, která má být přesunuta mezi dlužníkem a věřitelem před odečtením poplatků. Částka by měla být vyjádřená v měně podle objednávky strany příkazce.
    * Peněžní částka, která má být přesunuta mezi dlužníkem a věřitelem před odečtením poplatků. Částka by měla být vyjádřená v měně podle objednávky strany příkazce.  
59. Kliknutím na možnost Nový otevřete dialogové okno.
60. Zadejte text „End2EndID“ do pole Název.
    * End2EndID  
61. V poli Typ položky vyberte Řetězec.
62. Klepněte na možnost Přidat.
63. Do pole Popis zadejte hodnotu 'Jedinečná identifikace přiřazena stranou příkazce'. Tato identifikace se přenáší beze změny v průběhu celého řetězce od začátku do konce.
    * Jedinečná identifikace přiřazena stranou příkazce. Tato identifikace se přenáší beze změny v průběhu celého řetězce od začátku do konce.  
64. Zadejte PaymentModel do pole Název.
    * Název PaymentModel vychází z předdefinovaných rozhraní formulářů plateb.  
65. Klikněte na položku Uložit.
66. Zavřete stránku.


