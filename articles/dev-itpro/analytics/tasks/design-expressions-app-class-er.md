---
title: Návrh výrazů elektronického výkaznictví pro volání metod třídy aplikace
description: Tento průvodce obsahuje informace o tom, jak opakovaně použít existující aplikační logiku v konfiguracích elektronického výkaznictví (ER) voláním požadovaných metod aplikačních tříd ve výrazech ER.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fdacd852eeed33b443a3c79b96fc4c4af04bb6b2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544879"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>Návrh výrazů elektronického výkaznictví pro volání metod třídy aplikace

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento průvodce obsahuje informace o tom, jak opakovaně použít existující aplikační logiku v konfiguracích elektronického výkaznictví (ER) voláním požadovaných metod aplikačních tříd ve výrazech ER. Argumenty pro volání třídy hodnoty lze definovat dynamicky při spuštění: například na základě informací v dokumentu určeném k ověření jejich správnosti. V této příručce vytvoříte požadované konfigurace elektronického výkaznictví pro vzorovou společnost Litware, Inc. Tento postup je vytvořen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického výkaznictví. 

Tyto kroky lze dokončit za použití libovolné datové sady. Je nutné stáhnout a lokálně uložit následující soubor: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.

K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v proceduře "ER Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".

1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
    * Ověřte, zda poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako aktivní. Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu „Vytvoření poskytovatele konfigurace a jeho označení jako aktivního“.   
    * Předpokládejme, že navrhujete proces pro analýzu příchozích bankovních výpisů pro aktualizaci dat aplikace. Obdržíte příchozí bankovní výpisy jako TXT soubory, které obsahují kód IBAN kódy. V rámci procesu importu bankovního výpisu je nutné ověřit správnost těchto kódů IBAN na základě logiky, která je již k dispozici v aplikaci Dynamics 365 for Finance and Operations.   

## <a name="import-a-new-er-model-configuration"></a>Import nové konfigurace ER modelu
1. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte dlaždici poskytovatele společnosti Microsoft.  
2. Klikněte na možnost Úložiště.
3. Klepněte na tlačítko Zobrazit filtry.
4. Přidejte pole filtru ‘Type name’. Do pole Název typu zadejte hodnotu filtru “zdroje”, vyberte operaci filtru "obsahuje" a klikněte na Použít.
5. Klikněte na možnost Otevřít.
6. Ve stromovém zobrazení vyberte „Model platby“.
    * Pokud není aktivní tlačítko Import na pevné záložce Verze, již jste importovali verzi 1 konfigurace ER Platební model. Zbývající kroky tohoto dílčího úkolu můžete vynechat.   
7. Klepněte na tlačítko Importovat.
8. Klepněte na tlačítko Ano.
9. Zavřete stránku.
10. Zavřete stránku.

## <a name="add-a-new-er-format-configuration"></a>Přidání nové konfigurace formátu ER
1. Klikněte na Konfigurace výkaznictví.
    * Přidejte nový formát ER pro účely analýzy příchozích bankovních výpisů ve formátu TXT.  
2. Ve stromovém zobrazení vyberte „Model platby“.
3. Kliknutím na možnost Vytvořit konfiguraci otevřete nabídku dialogového okna.
4. V poli Nový zadejte "Formát založený na datovém modelu PaymentModel".
5. Do pole Název zadejte "Formát importu bankovního výpisu (ukázka)".
    * Formát importu bankovního výpisu (ukázka)  
6. Vyberte možnost Ano v poli Podporuje import dat.
7. Klepněte na možnost Vytvořit konfiguraci.

## <a name="design-the-er-format-configuration---format"></a>Návrh konfigurace formátu ER - formát
1. Klikněte na možnost Návrhář.
    * Navržený formát představuje očekávanou strukturu externího souboru ve formátu TXT.  
2. Klepnutím na možnost Přidat kořen otevřete nabídku dialogového okna.
3. Ve stromovém zobrazení vyberte 'Text\Pořadí'.
4. Do pole Název zadejte Kořen.
    * Kořen  
5. V poli speciální znaky vyberte "Nový řádek – Windows (CR LF)".
    * V poli ‘Speciální znaky’ je vybraná možnost ‘Nový řádek - Windows (CR LF)’. Na základě tohoto nastavení je každý řádek analýzy souboru považována za samostatný záznam.  
6. Klikněte na tlačítko OK.
7. Klepnutím na možnost Přidat otevřete dialogové okno.
8. Ve stromovém zobrazení vyberte 'Text\Pořadí'.
9. Do pole název zadejte text Řádky.
    * Řádky  
10. V poli Násobnost vyberte Jeden-n.
    * V poli "Násobnost" je vybraná možnost Jeden k mnoha. Na základě tohoto nastavení se očekává, že v souboru analýzy bude prezentován alespoň jeden řádek.  
11. Klikněte na tlačítko OK.
12. Ve stromu vyberte možnost 'Root\Rows'.
13. Klikněte na položku Přidat pořadí.
14. Do pole Název zadejte text Pole.
    * Pole  
15. V poli Násobnost vyberte Přesně jeden.
16. Klikněte na tlačítko OK.
17. Ve stromu vyberte možnost 'Root\Rows\Fields'.
18. Klepnutím na možnost Přidat otevřete dialogové okno.
19. Ve stromovém zobrazení vyberte „Text\Řetězec“.
20. Do pole Název zadejte IBAN.
    * KÓD IBAN  
21. Klikněte na tlačítko OK.
    * Konfigurace je taková, že každý řádek v souboru analýzy obsahuje pouze kód IBAN.  
22. Klikněte na položku Uložit.

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a>Návrh konfigurace formátu ER – mapování na datový model
1. Klikněte na Mapovat formát na model.
2. Klikněte na položku Nová.
3. V poli Definice zadejte hodnotu BankToCustomerDebitCreditNotificationInitiation.
    * BankToCustomerDebitCreditNotificationInitiation  
4. ResolveChanges Definice.
5. Do pole Název zadejte Mapování na model dat.
    * Mapování na datový model  
6. Klikněte na položku Uložit.
7. Klikněte na možnost Návrhář.
8. Ve stromu vyberte'Dynamics 365 for Operations\Class'.
9. Klikněte na možnost Přidat kořen.
    * Přidejte nový zdroj dat pro volání existující aplikační logiky pro ověření kódů IBAN.  
10. Do pole Název zadejte 'check_codes'.
    * check_codes  
11. Do pole Třída napište 'ISO7064'.
    * ISO7064  
12. Klikněte na tlačítko OK.
13. Ve stromové struktuře rozbalte Formát.
14. Ve stromovém zobrazení rozbalte 'format\Root: Sequence(Root)'.
15. Ve stromovém zobrazení vyberte 'format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)'.
16. Klikněte na možnost Vazba.
17. Ve stromovém zobrazení rozbalte 'format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)'.
18. Ve stromovém zobrazení rozbalte 'format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)\Fields: Sequence 1..1 (Fields)'.
19. Ve stromovém zobrazení vyberte 'format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.
20. Ve stromovém zobrazení rozbalte 'Payments = format.Root.Rows'.
21. Ve stromovém zobrazení rozbalte 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)'.
22. Ve stromovém zobrazení rozbalte 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification'.
23. Ve stromovém zobrazení vyberte 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN'.
24. Klikněte na možnost Vazba.
25. Klikněte na kartu Ověření.
26. Klikněte na položku Nová.
    * Přidejte nové pravidlo ověření pro chybovou zprávu u všech řádků v souboru analýzy, který obsahuje neplatný kód IBAN.  
27. Klikněte na Upravit podmínku.
28. Ve stromovém zobrazení rozbalte 'check_codes'.
29. Ve stromovém zobrazení vyberte 'check_codes\verifyMOD1271_36'.
30. Klikněte na možnost Přidat datový zdroj.
31. V poli Vzorec zadejte 'check_codes.verifyMOD1271_36('.
    * check_codes.verifyMOD1271_36(  
32. Ve stromové struktuře rozbalte Formát.
33. Ve stromovém zobrazení rozbalte 'format\Root: Sequence(Root)'.
34. Ve stromovém zobrazení rozbalte 'format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)'.
35. Ve stromovém zobrazení rozbalte 'format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)\Fields: Sequence 1..1 (Fields)'.
36. Ve stromovém zobrazení vyberte 'format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.
37. Klikněte na možnost Přidat datový zdroj.
38. V poli Vzorec zadejte 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)'.
    * check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)  
39. Klikněte na položku Uložit.
40. Zavřete stránku.
    * Stav ověření je nakonfigurován tak, že vrátí hodnotu FALSE u každého neplatného kódu IBAN voláním stávající metody ‘verifyMOD1271_36’ aplikační třídy ‘ISO7064’. Všimněte si, že hodnota kódu IBAN je definována dynamicky při spuštění jako argumentem metody volání založený na obsahu souboru TXT analýzy.   
41. Klikněte na Upravit zprávu.
42. V poli Vzorec zadejte 'CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)'.
    * CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)  
43. Klikněte na položku Uložit.
44. Zavřete stránku.
45. Klikněte na položku Uložit.
46. Zavřete stránku.

## <a name="run-the-format-mapping"></a>Spuštění mapování formátu
Pro účely testování proveďte mapování formátu pomocí souboru SampleIncomingMessage.txt, který jste stáhli. Generovaný výstup zahrnuje data, která budou importována z vybraného souboru TXT a načtena do vlastního datového modelu při reálném importu.   
1. Klikněte na položku Spustit.
    * Klikněte na tlačítko Procházet a vyhledejte soubor SampleIncomingMessage.txt, který jste předtím stáhli.  
2. Klikněte na tlačítko OK.
    * Zkontrolujte výstup ve formátu XML, který představuje data importovaná z vybraného souboru a přenesená do datového modelu. Všimněte si, že byly zpracovány pouze řádky 3 importovaného souboru TXT. Kód IBAN na řádku 4, který není platný, byl vynechán a v informačním protokolu je uvedena chybová zpráva.  

