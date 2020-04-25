---
title: Definování procesů inventur zásob
description: Toto téma popisuje konfiguraci základního inventurního procesu vytvořením inventurní skupiny a deníku inventur.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountGroup, InventJournalName, InventParameters, EcoResProductDetailsExtended, InventItemLocation, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9df5db0e71f550e82820e15b1597d9e287071f83
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213991"
---
# <a name="define-inventory-counting-processes"></a>Definování procesů inventur zásob

[!include [banner](../../includes/banner.md)]

Toto téma popisuje konfiguraci základního inventurního procesu vytvořením inventurní skupiny a deníku inventur. Je zde také uveden postup povolení zásady inventury na úrovni skladu a položky. Tyto úkoly obvykle provádějí vedoucí skladu. Jedná se o předpoklad, aby bylo možné použít stávající uvolněné produkty a sklady. Používáte-li ukázková data společnosti, můžete tento postup provést se společností USMF a s každou naskladněnou položkou.


## <a name="create-a-counting-group"></a>Vytvoření inventurní skupiny
1. V navigačním podokně přejděte na **Moduly > Řízení zásob > Nastavení > Zásoby > Inventurní skupiny**.
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **Inventurní skupina** nového řádku.
4. Zadejte hodnotu do pole **Název**.
5. Vyberte možnost v poli **Kód inventur**.

    - **Ruční** - Zahrne řádky pokaždé, když spustíte úkol. Jinak řečeno, rozhodujete o intervalu načítání pro skupinu načítání.  
    - **Období** - Zahrne řádky pro období v deníku načítání po vypršení intervalu období.  
    - **Nula na skladě** - Pokud množství na skladě dosáhne hodnoty nula (0), budou se řádky generovat v deníku načítání během spuštění úkolu. Pokud po načtení dosáhne hodnota množství na skladě nuly, budou se řádky generovat při následujícím spuštění načítání.  
    - **Minimum** - Vloží řádky do deníku načítání, pokud je množství na skladě rovno nebo menší než minimální stanovené množství.  
    - Volitelně: Pokud bylo v poli **Kód inventur** zvoleno **Období**, je třeba do pole **Období inventury** zadat časový interval. Jednotkou pro intervaly jsou dny.  
    - Pokud spustíte úlohu pro vytvoření nových řádků v deníku inventur, nové řádky se vytvoří v intervalu zadaném pro toto pole bez ohledu na četnost spouštění stejné úlohy. Pokud je **Období inventury** nastaveno na 7 a řádky deníku byly naposled generovány pro inventuru 1. ledna a jiná úloha je spuštěna 5. ledna, ještě neuplynulo sedm dní a tedy v deníku pro tento interval období nebudou generovány žádné řádky. Pokud se s úkolem opět začne 8. ledna, budou řádky v deníku inventury generovány za toto období, protože již uplynulo 7 dní.  

6. Zvolte **Uložit**.

## <a name="create-a-counting-journal-name"></a>Vytvoření názvu deníku inventury
1. V navigačním podokně přejděte na **Moduly > Řízení zásob > Nastavení > Názvy deníků > Zásoby**.
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **Název**.
4. Zadejte hodnotu do pole **Popis**.
5. V poli **Typ deníku** vyberte **Inventura**. Volitelné: můžete vybrat jiné ID číselné řady dokladů, pokud chcete určitou číselnou řadu pro ID dokladů generované při vytvoření deníků inventur. Číselná řada dokladů vytvoříte na stránce **Číselné řady**.  
6. Vyberte volbu v poli **Úroveň podrobností**.  

    - Toto je úroveň podrobností, která se použije při zaúčtování deníku.  
    - Volitelně: hodnotu můžete změnit v poli Rezervace. Toto je způsob pro rezervaci položek během inventury.   
    - **Ruční** – položky jsou rezervovány ručně ve formuláři rezervace.  
    - **Automaticky** - množství objednávky se zarezervuje z dostupného množství položky na skladě.   
    - **Rozpad** – rezervace je součástí hlavního plánování transakce.  

7. Zvolte **Uložit**.

## <a name="set-standard-counting-journal-name"></a>Nastavení standardního názvu deníku inventury
1. V navigačním podokně přejděte na **Moduly > Řízení zásob > Nastavení > Parametry řízení zásob a skladu**.
2. Vyberte kartu **Deníky**.
3. V rozevírací nabídce pole **Inventura** vyberte dříve vytvořený deník. Tento deník bude výchozí název deníku pro deníky zásob typu **Inventura**.  
4. Zvolte kartu **Obecné**. Volitelně: Tuto možnost vyberte, pokud chcete uzamknout položku během procesu inventury, aby nedošlo k aktualizaci například dodacích listů, výdejek nebo registrací výdejek.  

## <a name="set-the-counting-policy-for-an-item"></a>Nastavení zásady inventury pro položku
1. V navigačním podokně přejděte na **Moduly > Řízení informací o produktech > Produkty > Vydané produkty**.
2. V seznamu zvolte odkaz pro číslo položky produktu, pro který chcete nastavit zásady inventury. Je nutné vybrat položku, u které jsou sledovány zásoby. Nenaskladněný produkt nelze započítat. Používáte-li ukázková data USMF a vyberte položku A0001.  
3. Vyberte možnost **Upravit**.
4. Rozbalte oddíl **Spravovat sklad**.
5. V rozevírací nabídce pole **Skupina inventury** vyberte dříve vytvořenou skupinu inventury. Tento produkt nyní bude zahrnut při vytvoření řádků deníku inventur zásob pomocí této inventurní skupiny.  
6. Zvolte **Uložit**.

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a>Nastavení zásady inventury pro položku v určitém skladu
1. V podokně akcí klikněte na možnost **Spravovat sklad**.
2. Vyberte **Skladové položky**.
3. Zvolte **Nové**.
4. V rozevírací nabídce pole **Sklad** vyberte sklad, pro který chcete nastavit specifické zásady inventury.
5. V rozevírací nabídce pole **Skupina inventury** vyberte skupinu inventury. Můžete vybrat konkrétní inventurní skupinu, která má být použita pro položku v určitém skladu, který jste vybrali. Při provádění inventury skladu tato zásada inventury přepíše hlavní zásady inventury pro položku.  
6. Zvolte **Uložit**.

