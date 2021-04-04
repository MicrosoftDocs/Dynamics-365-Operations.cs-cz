---
title: Návrh konfigurací elektronického výkaznictví pro analýzu příchozích dokumentů
description: Kroky v tomto postupu popisují postup návrhu konfigurace elektronického vykazování k analýze příchozího elektronického dokumentu.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7235d75aee3b8fdf39492cfbc1760bf6eae4b82e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562849"
---
# <a name="design-er-configurations-to-parse-incoming-documents"></a>Návrh konfigurací elektronického výkaznictví pro analýzu příchozích dokumentů

[!include [banner](../../includes/banner.md)]

Kroky v tomto postupu popisují postup návrhu konfigurace elektronického vykazování k analýze příchozího elektronického dokumentu. V tomto postupu naimportujete požadované konfigurace elektronického výkaznictví, které byly vytvořeny pro vzorovou společnost Litware, Inc., a poté je použijete k analýze příchozích elektronických dokumentů. K provedení kroků v tomto postupu musíte nejprve dokončit postup "ER Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".

Tento postup je vytvořen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování.

Tyto kroky lze dokončit za použití libovolné datové sady. Než začnete, stáhněte a uložte soubory uvedené v tématu "Analýza příchozích dokumentů pro aktualizaci dat aplikace" ([Analýza příchozích dokumentů](../parse-incoming-electronic-documents.md)). Soubory jsou: EFSTA model.xml, EFSTA format.xml Response1.xml Response2.xml, Response3.xml, Response4.xml.

1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
    * Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako Aktivní. Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu „Vytvoření poskytovatele konfigurace a jeho označení jako aktivního“.
2. Vyberte Konfigurace vykazování.
    * Následující scénář bude použit pro zobrazení možností analyzování příchozích elektronických dokumentů ve formátu XML: aplikace ERP požaduje data z webové služby (například daňové služby [efsta](http://efsta.org/)) a analyzuje příchozí odpovědi, aby odpovídajícím způsobem aktualizovala data aplikace. Pro nejefektivnější způsob analýzy je použit jeden ER formát navzdory odlišné struktuře očekávaných příchozích dokumentů ve formátu XML.

## <a name="import-and-review-er-configurations"></a>Import a kontrola konfigurací ER

Importujte model konfigurace ER, který obsahuje vzorový datový model určený k uložení podrobností vstupního souboru.

1. Vyberte Exchange.
2. Vyberte Načíst ze souboru XML.
    * Vyberte tlačítko Procházet a vyberte soubor EFSTA model.xml.
3. Vyberte OK.
4. Ve stromovém zobrazení vyberte „Model EFSTA“.
5. Vyberte možnost Návrhář.
    * Zkontrolujte strukturu importovaného modelu dat. Výčet enumType je definován tak, aby rozlišil následující typy odpovědi odpovědí služby: získání potvrzení o odeslání transakce, získání informací o poslední odeslané transakci, rozpoznání nepodporovaných typů odpovědi.
6. Ve stromu rozbalte 'Response'.
    * Kořenová položka 'Odpověď' je definována pro určení, jaký typ dat musí být pořízen z podporované odpovědi služby na aktualizaci dat aplikace.
7. Zavřete stránku.
    * Budete importovat konfiguraci formátu ER, která určuje způsob analýzy příchozích dokumentů pro uložení dat v datovém modelu ER.
8. Vyberte Exchange.
9. Vyberte Načíst ze souboru XML.
    * Vyberte tlačítko Procházet a vyberte soubor EFSTA format.xml.
10. Vyberte OK.
11. Ve stromovém zobrazení rozbalte „Model EFSTA“.
12. Ve stromovém zobrazení vyberte 'EFSTA model\EFSTA format'.
13. Vyberte možnost Návrhář.
14. Vyberte příkaz Rozbalit/sbalit.
    * Prvek formátu CASE se používá v kořeni a obsahuje tři vnořené prvky FILE. To znamená, že je tento formát určen k analýze příchozích souborů několika formátů.
15. Ve stromovém zobrazení vyberte 'Responses\Transaction completion\TraC'.
    * Odpověď na odeslanou transakci začíná kořenovým prvkem 'TraC'.
16. Ve stromovém zobrazení vyberte 'Responses\Last transaction request\Tra'.
    * Odpověď na poslední odeslanou transakci začíná kořenovým prvkem 'Era'.
17. Ve stromovém zobrazení vyberte 'Responses\Unexpected response\Text'.
    * Třetí element FILE s vnořeným elementem TEXT byl přidán pro účely rozpoznání jakýchkoli dalších typů odpovědí, které se liší od výše uvedených.
18. Vyberte příkaz Mapovat formát na model.
    * Tento model mapování obsahuje definice toku dat pro uložení podrobností analyzovaného příchozího dokumentu s použitím položek modelu dat.
19. Vyberte možnost Návrhář.
20. Ve stromové struktuře rozbalte Formát.
21. Ve stromovém zobrazení rozbalte 'format\Responses: Case(Responses)'.
    * Zkontrolujte strukturu zdroje dat 'formát'. Všechny tři typy odpovědí jsou k dispozici samostatně.
22. Ve stromovém zobrazení vyberte 'format\Responses: Case(Responses)\aType'.
    * Položka zdroje dat 'aType' byla přidána, aby označovala typ odpovědi a je vázaná na položku datového modelu 'Type'.
23. Vyberte kartu Ověření.
24. Ve stromovém zobrazení vyberte 'Type = format.Responses.aType'.
    * Ověření ER, které bylo konfigurováno s cílem informovat uživatele o situaci, kdy struktura odpovědi neodpovídá potvrzení o odeslání transakce nebo informacím o poslední odeslané transakci (nepodporovaný případ odezvy).
25. Zavřete stránku.

## <a name="run-model-mapping-of-er-format-configured-for-parsing-incoming-files"></a>Spuštění mapování modelu formátu ER nakonfigurovaného pro zpracování příchozí souborů

Spuštěním mapování vytvářeném modelu pro testovací účely zobrazíte, jak bude konfigurovaný formát ER analyzovat odpovědi na příchozí služby. Tento krok používá různé soubory XML k simulaci jiného typu odpovědí webové služby.

1. Otevřete soubor Response1.xml v čtečce xml například ve webovém prohlížeči. Tento soubor obsahuje podrobnosti o potvrzení o dokončené transakci (kořenový prvek je 'TraC').
2. Vyberte Spustit.
    * Vyberte tlačítko Procházet a vyberte soubor Response1.xml.
3. Vyberte OK.
    * Prohlédněte si generovaný výstup. Typ odpovědi byl správně rozpoznán a analyzován (`ERModelEnumDataSourceHandler#EFSTA model#enumType#C` znamená případ dokončení transakce).
    * Otevřete soubor Response2.xml v čtečce XML. Tento soubor obsahuje informace o poslední provedené transakci (kořenový prvek je `Tra`).
4. Vyberte Spustit.
    * Vyberte tlačítko Procházet a vyberte soubor Response2.xml.
5. Vyberte OK.
    * Prohlédněte si generovaný výstup. Typ odpovědi byl správně rozpoznán a analyzován (`ERModelEnumDataSourceHandler#EFSTA model#enumType#R` znamená případ restartování systému).
    * Otevřete soubor Response3.xml v čtečce XML. Tento soubor začíná kořenovou položkou TraZ a struktura není konfigurovaná pomocí formátu ER.
6. Vyberte Spustit.
    * Vyberte tlačítko Procházet a vyberte soubor Response3.xml.
7. Vyberte OK.
    * Prohlédněte si generovaný výstup. Typ odpovědi byl správně rozpoznán jako nepodporovaný (`ERModelEnumDataSourceHandler#EFSTA model#enumType#U`). Do informačního protokolu byla zadána příslušná zpráva (podle nastavení ověření ER) a většina datového modelu nebyla vyplněna.
    * Otevřete soubor Response4.xml v čtečce XML. Struktura tohoto souboru je skoro stejná jako u úspěšně analyzovaného souboru Response1.xml kromě sekvence vnořených elementů kořenového elementu ‘TraC’.
8. Vyberte Spustit.
    * Vyberte tlačítko Procházet a vyberte soubor Response4.xml.
9. Vyberte OK.
    * Prohlédněte si generovaný výstup. Typ odpovědi byl správně rozpoznán jako nepodporovaný (`ERModelEnumDataSourceHandler#EFSTA model#enumType#U`). Do informačního protokolu byla zadána příslušná zpráva a většina datového modelu nebyla vyplněna. Důvodem tohoto chování je skutečnost, že aktuální nastavení tohoto formátu ER předpokládá posloupnost vnořených elementů položky kořenové příchozí souboru.
10. Zavřete stránku.
11. Ve stromovém zobrazení vyberte 'Responses\Transaction completion\TraC'.
12. V pořadí analýzy pole vnořených prvků pole vyberte 'Libovolný.
    * V poli 'Analýza pořadí vnořených prvků' vyberte Libovolné, aby byla povolena libovolná sekvence vnořených prvků pro tuto kořenovou položku XML.
13. Zvolte Uložit.
14. Vyberte příkaz Mapovat formát na model.
15. Vyberte Spustit.
    * Vyberte tlačítko Procházet a vyberte soubor Response4.xml.
16. Vyberte OK.
    * Prohlédněte si generovaný výstup. Typ odezvy nyní byl správně rozpoznán jako rovnající se souboru Response1.xml.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]