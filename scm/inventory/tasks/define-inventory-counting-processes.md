--- 
title: "Definování procesů inventur zásob"
description: "Tento postup vás provede konfigurací základního inventurního procesu vytvořením inventurní skupiny a deníku inventur."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 62c60faafd9ad96ce636a08102bc8652f9fff870
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="define-inventory-counting-processes"></a>Definování procesů inventur zásob

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup vás provede konfigurací základního inventurního procesu vytvořením inventurní skupiny a deníku inventur. Je zde také uveden postup povolení zásady inventury na úrovni skladu a položky. Tyto úkoly obvykle provádějí vedoucí skladu. Jedná se o předpoklad, aby bylo možné použít stávající uvolněné produkty a sklady. Používáte-li ukázková data společnosti, můžete tento postup provést se společností USMF a s každou naskladněnou položkou.


## <a name="create-a-counting-group"></a>Vytvoření inventurní skupiny
1. Přejděte do možnosti Řízení zásob > Nastavení > Sklady > Inventurní skupiny.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Inventurní skupina.
4. Zadejte hodnotu do pole Název.
5. Vyberte možnost v poli Kód inventur.
    * Ručně - Zahrne řádky pokaždé, když spustíte úkol. Jinak řečeno, rozhodujete o intervalu načítání pro skupinu načítání.  Období - Zahrne řádky pro období v deníku načítání po vypršení intervalu období.   Nula na skladě - Pokud množství na skladě dosáhne hodnoty nula (0), budou se řádky generovat v deníku načítání během spuštění úkolu. Pokud po načtení dosáhne hodnota množství na skladě nuly, budou se řádky generovat při následujícím spuštění načítání.   Minimum - Vloží řádky do deníku načítání, pokud je množství na skladě rovno nebo menší než minimální stanovené množství.  
    * Volitelně: Pokud bylo v poli Kód inventur zvoleno období, je třeba do tohoto pole zadat časový interval období inventury. Jednotkou pro intervaly jsou dny.  
    * Pokud spustíte úlohu pro vytvoření nových řádků v deníku inventur, nové řádky se vytvoří v intervalu zadaném pro toto pole bez ohledu na četnost spouštění stejné úlohy. Pokud období inventury je nastaveno na 7 a řádky deníku byly naposled generovány pro inventuru 1. ledna a jiná úloha je spuštěna 5. ledna, ještě neuplynulo sedm dní a tedy v deníku pro tento interval období nebudou generovány žádné řádky. Pokud se s úkolem opět začne 8. ledna, budou řádky v deníku inventury generovány za toto období, protože již uplynulo 7 dní.  
6. Klikněte na položku Uložit.

## <a name="create-a-counting-journal-name"></a>Vytvoření názvu deníku inventury
1. Přejděte do možnosti Řízení zásob > Nastavení > Názvy deníků > Zásoby.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Název.
4. Zadejte nějakou hodnotu do pole Popis.
5. V poli Typ deníku vyberte Inventura.
    * Volitelné: můžete vybrat jiné ID číselné řady dokladů, pokud chcete určitou číselnou řadu pro ID dokladů generované při vytvoření deníků inventur. Číselná řada dokladů vytvoříte na stránce Číselné řady.  
6. Vyberte volbu v poli Úroveň podrobností.
    * Toto je úroveň podrobností, která se použije při zaúčtování deníku.  
    * Volitelně: hodnotu můžete změnit v poli Rezervace. Toto je způsob pro rezervaci položek během inventury.   
    * Ručně – položky jsou rezervovány ručně ve formuláři rezervace.   Automaticky - množství objednávky se zarezervuje z dostupného množství položky na skladě.   Rozpad – rezervace je součástí hlavního plánování transakce.  
7. Klikněte na položku Uložit.

## <a name="set-standard-counting-journal-name"></a>Nastavení standardního názvu deníku inventury
1. Přejděte do nabídky Řízení zásob > Nastavení > Parametry řízení zásob a skladu.
2. Klikněte na kartu Deníky.
3. V poli Inventura kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Vyberte dříve vytvořený deník.
    * Tento deník bude výchozí název pro skladové deníky typu Inventura.  
5. Klikněte na záložku Obecné.
    * Volitelně: Tuto možnost vyberte, pokud chcete uzamknout položku během procesu inventury, aby nedošlo k aktualizaci například dodacích listů, výdejek nebo registrací dodacího listu.  

## <a name="set-the-counting-policy-for-an-item"></a>Nastavení zásady inventury pro položku
1. Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.
2. V seznamu klepněte na odkaz pro číslo položky produktu, pro který chcete nastavit zásady inventury.
    * Všimněte si, že je nutné vybrat položku, u které jsou sledovány zásoby. Nenaskladněný produkt nelze započítat. Používáte-li ukázková data USMF a vyberte položku A0001.  
3. Klikněte na položku Upravit.
4. Rozbalte oddíl Spravovat sklad.
5. V poli Inventurní skupina kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. V seznamu klepněte na dříve vytvořenou inventurní skupinu.
    * Tento produkt nyní bude zahrnut při vytvoření řádků deníku inventur zásob pomocí této inventurní skupiny.  
7. Klikněte na položku Uložit.

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a>Nastavení zásady inventury pro položku v určitém skladu
1. V podokně akcí klikněte na možnost Spravovat sklad.
2. Klikněte na Skladové položky.
3. Klepněte na možnost Nový.
4. V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. V seznamu vyberte sklad, pro který chcete nastavit konkrétní zásady inventury.
6. V poli Inventurní skupina kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
7. V seznamu vyberte skupinu inventury
    * Můžete zde vybrat konkrétní inventurní skupinu, která má být použita pro položku v určitém skladu, který jste vybrali. Při provádění inventury skladu tato zásada inventury přepíše hlavní zásady inventury pro položku.  
8. Klikněte na položku Uložit.


