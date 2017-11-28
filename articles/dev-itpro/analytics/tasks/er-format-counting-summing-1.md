--- 
title: "Vytvoření formátu pro počítání a sčítání pro elektronické výkaznictví (ER)"
description: "Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: 5d4f57ae2a309d9e15c1afe60c3e91d7d7eb3870
ms.openlocfilehash: 3c4ae958a03d4681a85f5b83d81fe64b9ac99cf5
ms.contentlocale: cs-cz
ms.lasthandoff: 11/02/2017

---
# <a name="create-format-for-counting-and-summing-for-electronic-reporting-er"></a>Vytvoření formátu pro počítání a sčítání pro elektronické výkaznictví (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu. Tyto kroky lze provést v rámci libovolné společnosti.

K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".

Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Získání přístupu k seznamu konfigurací poskytovaných společností Microsoft
1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
    * Ujistěte se, že poskytovatel 'Litware, Inc.' je k dispozici a označen jako aktivní.  
2. Vyberte poskytovatele Litware, Inc.  
3. Klikněte na možnost Úložiště.
    * Pokud již existuje úložiště typu Zdroje operace, přeskočte zbývající kroky aktuální dílčí úlohy.  
4. Klepnutím na možnost Přidat otevřete dialogové okno.
5. V poli Typ úložiště konfigurace zadejte "Provozní prostředky".
6. Klikněte na Vytvořit úložiště.
7. Klikněte na tlačítko OK.

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a>Získání konfigurací Intrastat dodaných společností Microsoft
1. Klikněte na možnost Otevřít.
2. Ve stromové struktuře vyberte Modul Intrastat\Intrastat (DE).
3. Klepněte na tlačítko Importovat.
    * Klikněte na Import pro verzi 1.1 vybrané konfigurace.  
4. Klepněte na tlačítko Ano.
5. Zavřete stránku.
6. Zavřete stránku.
7. Klikněte na Konfigurace výkaznictví.
8. Ve stromovém zobrazení rozbalte „Modul Intrastat“.
9. Ve stromové struktuře vyberte Modul Intrastat\Intrastat (DE).


