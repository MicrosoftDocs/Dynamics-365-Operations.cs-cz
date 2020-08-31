---
title: Správa měrných jednotek
description: Tento postup popisuje definování měrné jednotky, poskytnutí překladů pro jednotky a jejich popisu a definování pravidel pro převod souvisejících jednotek.
author: sorenva
manager: tfehr
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b8b432e1ec8a26b54574c417e618ded694b19556
ms.sourcegitcommit: 59a9e840989bc9f2c7004efa3499b69c09a91b06
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677864"
---
# <a name="manage-unit-of-measure"></a>Správa měrných jednotek

[!include [banner](../../includes/banner.md)]

Tento postup popisuje definování měrné jednotky, poskytnutí překladů pro jednotky a jejich popisu a definování pravidel pro převod souvisejících jednotek. Tento postup můžete projít pomocí ukázkových dat společnosti nebo pomocí vlastních dat.

1. Přejděte na **Navigační podokno > Moduly > Řízení informací o produktech > Produkty > Údržba uvolněného produktu**.
2. Klikněte na možnost **Jednotky**.

## <a name="create-a-unit-of-measure"></a>Vytvoření měrné jednotky
1. Klepněte na možnost **Nový**.
2. Do pole **Jednotka** zadejte hodnotu. Zadejte ID nebo symbol pro použití při odkazování na měrnou jednotku.  
3. Zadejte hodnotu do pole **Popis**. Zadejte popisný název měrné jednotky v systémovém jazyce.  
4. V poli **Třída jednotek** vyberte možnost. Třída jednotek určuje, do jakého logického seskupení, například do oblasti, hmotnosti nebo množství, měrná jednotka patří.  
5. V poli **Desetinná přesnost** zadejte číslo. Určete počet desetinných míst, na který má být převedená měrná jednotka zaokrouhlena při dokončení výpočtu pro měrnou jednotku.  
6. Klikněte na možnost **Uložit**.

## <a name="define-unit-translations"></a>Definování překladů jednotek
1. V **podokně akcí** klikněte na možnost **Texty jednotek**.
2. Klepněte na možnost **Nový**. Text jednotky použijte k vytvoření překladu ID nebo symbolu představujícího měrnou jednotku pro použití u externích dokumentů v jazycích odběratele nebo dodavatele.  
3. V poli **Jazyk** zadejte nebo vyberte hodnotu.
4. Zadejte hodnotu do pole **Text**.
5. Klikněte na možnost **Uložit**.
6. Zavřete stránku.
7. V **podokně akcí** klikněte na možnost **Popisy přeložené jednotky**.
8. Klepněte na možnost **Nový**. Definujte popisy měrné jednotky pro daný jazyk.  
9. V poli **Jazyk** zadejte nebo vyberte hodnotu.
10. Zadejte hodnotu do pole **Popis**.
11. Klikněte na možnost **Uložit**.
12. Zavřete stránku.

## <a name="define-unit-conversion-rules"></a>Definování pravidel pro převod jednotek
1. V **podokně akcí** klikněte na možnost **Převody jednotek**. Definujte pravidla pro převod měrné jednotky do a z jiných měrných jednotek ve vybrané třídě jednotky.  
2. Kliknutím na možnost **Nový** otevřete dialogové okno.
3. Do pole **Koeficient** zadejte číslo. Koeficient převodu mezi hodnotou Z jednotky a Do jednotky. Například koeficient převodu centimetrů na metry je 100, protože v jednom metru je 100 centimetrů.  
4. V poli **Do jednotky** zadejte nebo vyberte hodnotu.
5. Vyberte možnost v poli **Zaokrouhlení**. Definujte, jak má být převedená hodnota zaokrouhlena.  
6. Klikněte na tlačítko **OK**.
7. Zavřete stránku.

