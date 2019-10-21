---
title: Import konfigurace ER ze služby Lifecycle Services
description: Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může importovat novou verzi konfigurace formátu pro elektronické výkaznictví ze služby Microsoft Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0830707885e8ed52581aa789df0279d78e3a9c10
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184823"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a>Import konfigurace ER ze služby Lifecycle Services

[!include [task guide banner](../../includes/task-guide-banner.md)]

Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může importovat novou verzi konfigurace formátu pro elektronické výkaznictví ze služby Microsoft Lifecycle Services (LCS).

V tomto příkladu zvolíte požadovanou verzi konfiguraci ER a importujete ji pro vzorovou společnost Litware, Inc a odešlete ji do LCS. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace ER se sdílí mezi společnostmi. K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Odeslání konfigurace ER do služby Lifecycle Services". K dokončení tohoto postupu je nutný také přístup k LCS.

1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
2. Klikněte na Konfigurace.

## <a name="delete-a-shared-version-of-data-model-configuration"></a>Odstranění sdílené verze konfigurace modelu dat
1. Ve stromovém zobrazení vyberte možnost Vzorová konfigurace modelu.
    * První verze vzorové konfigurace modelu dat byla vytvořena a publikována do LCS během procesu "Odeslání konfigurace ER do služby Lifecycle Services". V tomto postupu tuto verzi konfigurace ER odstraníte. Tato verze vzorové konfigurace datového modelu bude importována ze LCS později.  
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte verzi této konfigurace se stavem „Sdíleno“. Tento stav označuje, že byla konfigurace publikována do LCS.  
3. Klikněte na položku Změnit stav.
4. Klikněte na Ukončit.
    * Změňte stav vybrané verze ze "Sdíleno" na „Ukončeno“ a umožněte tak její odstranění.  
5. Klikněte na tlačítko OK.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte verzi této konfigurace se stavem „Ukončeno“.  
7. Klepněte na tlačítko Odstranit.
8. Klepněte na tlačítko Ano.
    * Všimněte si, že pouze 2. verze návrhu vybrané konfigurace modelu dat je k dispozici.  
9. Zavřete stránku.

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a>Import sdílené verze konfigurace modelu dat z LCS
1. Označte v seznamu vybraný řádek.
    * Otevřete seznam úložišť pro poskytovatele konfigurace Litware, Inc.    
2. Klikněte na možnost Úložiště.
3. Klikněte na možnost Otevřít.
    * Vyberte úložiště LCS a otevřete je.  
4. Označte v seznamu vybraný řádek.
    * Vyberte první verzi vzorové konfigurace modelu v seznamu verzí.  
5. Klepněte na tlačítko Importovat.
6. Klepněte na tlačítko Ano.
    * Potvrďte import vybrané verze z LCS.  
    * Všimněte si, že informační zpráva (nad formulářem) potvrzuje úspěšné dokončení importu vybrané verze.  
7. Zavřete stránku.
8. Zavřete stránku.
9. Klikněte na Konfigurace.
10. Ve stromovém zobrazení vyberte možnost Vzorová konfigurace modelu.
11. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte verzi této konfigurace se stavem „Sdíleno“.  
    * Všimněte si, že nově je také sdílená 1. verze vybrané konfigurace modelu dat k dispozici.  

