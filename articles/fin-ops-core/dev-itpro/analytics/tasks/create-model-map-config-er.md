---
title: Vytvoření konfigurací mapování modelu elektronického výkaznictví
description: Tento postup slouží k navržení nové konfigurace mapování modelu elektronického výkaznictví a použití integrovaných funkcí ER k efektivním agregovaným výpočtům.
author: NickSelin
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
ms.openlocfilehash: 9a614ce0f055691e36c1aab5d84d4fc3355026f1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752549"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a>Vytvoření konfigurací mapování modelu elektronického výkaznictví

[!include [banner](../../includes/banner.md)]

Tento postup slouží k navržení nové konfigurace mapování modelu elektronického výkaznictví a použití integrovaných funkcí ER k efektivním agregovaným výpočtům. V tomto postupu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc. 

Tento postup je vytvořen pro použití s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování.

Tyto kroky lze dokončit za použití libovolné datové sady. K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v proceduře "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".

1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
    * Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako Aktivní. Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu „Vytvoření poskytovatele konfigurace a jeho označení jako aktivního“.  
2. Klikněte na Konfigurace výkaznictví.
3. Klepněte na tlačítko Zobrazit filtry.
4. Do pole Název zadejte hodnotu filtru Intrastat a použijte operaci filtru "začíná na".
    * Tento filtr použijte k vyhledání konfigurace datového modelu ‘Intrastat’. Tento model již může existovat ve stromu konfigurace. Pokud ano, vynechejte další dílčí úkol.   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a>Získání modelové konfigurace Intrastat dodané společností Microsoft
1. Zavřete stránku.
2. Zavřete stránku.
3. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte dlaždici poskytovatele společnosti Microsoft.  
5. Klikněte na možnost Úložiště.
    * V dlaždici poskytovatele Microsoft klikněte na Úložiště.  
6. Klepněte na tlačítko Zobrazit filtry.
7. Do pole Název typu zadejte hodnotu filtru “zdroje” a použijte operaci filtru "obsahuje". 
8. Klikněte na možnost Otevřít.
9. Ve stromovém zobrazení vyberte 'Intrastat model'.
10. Klepněte na tlačítko Importovat.
11. Klepněte na tlačítko Ano.
    * Importovali jste konfiguraci modelu ER, která obsahuje datový model, který použijete k zjištění, jak bude možné používat novou funkci ER.  
12. Zavřete stránku.
13. Zavřete stránku.
14. Klikněte na Konfigurace výkaznictví.

## <a name="add-a-new-model-mapping-configuration"></a>Přidání nové konfigurace mapování modelu
1. Ve stromovém zobrazení vyberte 'Intrastat model'.
2. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
3. V poli Nový zadejte 'Mapování modelu založené na datovém modelu Intrastat'.
4. V poli Název zadejte Mapování ukázky Intrastat.
    * Mapování ukázky Intrastat  
5. Klepněte na možnost Vytvořit konfiguraci.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]