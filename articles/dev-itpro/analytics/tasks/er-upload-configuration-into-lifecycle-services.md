---
title: Odeslání konfigurace ER do služby Lifecycle Services
description: Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit novou konfiguraci formátu pro elektronické výkaznictví a odeslat ji do služby Microsoft Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19ae8820e5d4a798a5789e9632edb431fe9fede4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551106"
---
# <a name="er-upload-a-configuration-into-lifecycle-services"></a>Odeslání konfigurace ER do služby Lifecycle Services

[!include [task guide banner](../../includes/task-guide-banner.md)]

Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit novou konfiguraci formátu pro elektronické výkaznictví a odeslat ji do služby Microsoft Lifecycle Services (LCS).

V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc a odešlete ji do LCS. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace ER se sdílí mezi společnostmi. K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního". K dokončení tohoto postupu je nutný také přístup k LCS.

1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
2. Vyberte Litware, Inc. a nastavte ji jako aktivní.
3. Klikněte na Konfigurace.

## <a name="create-a-new-data-model-configuration"></a>Vytvoření nové konfigurace datového modelu
1. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
    * Vytvoříte konfiguraci, která obsahuje vzorový model dat pro elektronické doklady. Tato konfigurace modelu dat bude odeslána do LCS později.  
2. V poli Název zadejte Vzorová konfigurace modelu.
    * Vzorová konfigurace modelu  
3. V poli Popis zadejte „Vzorová konfigurace modelu“.
    * Vzorová konfigurace modelu  
4. Klepněte na možnost Vytvořit konfiguraci.
5. Klikněte na Návrhář modelů.
6. Klikněte na položku Nová.
7. Do pole Název zadejte Vstupní bod.
    * Vstupní bod  
8. Klepněte na možnost Přidat.
9. Klikněte na položku Uložit.
10. Zavřete stránku.
11. Klikněte na položku Změnit stav.
12. Klikněte na tlačítko Dokončit.
13. Klikněte na tlačítko OK.

## <a name="register-a-new--repository"></a>Registrace nového úložiště
1. Zavřete stránku.
2. Klikněte na možnost Úložiště.
    * To umožňuje otevřít seznam úložišť pro poskytovatele konfigurace Litware, Inc.  
3. Klepnutím na možnost Přidat otevřete dialogové okno.
    * Tímto způsobem můžete přidat nové úložiště.  
4. V poli Typ úložiště konfigurace vyberte LCS.
5. Klikněte na Vytvořit úložiště.
6. V poli Projekt zadejte nebo vyberte hodnotu.
    * Vyberte příslušný projekt LCS. Musíte mít přístup k tomuto projektu.  
7. Klikněte na tlačítko OK.
    * Vytvořte nový záznam v úložišti.  
8. Označte v seznamu vybraný řádek.
    * Vybrat záznam úložiště LCS.  
    * Všimněte si, registrované úložiště je označeno aktuálním poskytovatelem, tj. pouze konfigurace ve vlastnictví daného poskytovatele mohou být umístěny do tohoto úložiště a následně odeslány do vybraného projektu LCS.  
9. Klikněte na možnost Otevřít.
    * Otevřete úložiště a prohlédněte si seznam konfigurací ER. Bude prázdný, pokud tento projekt nebyl dosud použit pro sdílení konfigurací ER.  
10. Zavřete stránku.
11. Zavřete stránku.

## <a name="upload-configuration-into-lcs"></a>Odeslání konfigurace do LCS
1. Klikněte na Konfigurace.
2. Ve stromovém zobrazení vyberte možnost Vzorová konfigurace modelu.
    * Vyberte vytvořenou konfiguraci, která již byla dokončena.  
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte verzi vybrané konfigurace se stavem "Dokončeno".  
4. Klikněte na položku Změnit stav.
5. Klepněte na Sdílet.
    * Stav konfigurace se změní z "Dokončeno" na 'Sdíleno' během publikování v LCS.  
6. Klikněte na tlačítko OK.
7. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte verzi konfigurace se stavem „Sdílena“.  
    * Všimněte si, že stav vybrané verze se změnil z "Dokončeno" na 'Sdíleno'.  
8. Zavřete stránku.
9. Klikněte na možnost Úložiště.
    * To umožňuje otevřít seznam úložišť pro poskytovatele konfigurace Litware, Inc.  
10. Klikněte na možnost Otevřít.
    * Vyberte úložiště LCS a otevřete je.  
    * Všimněte si, že vybraná konfigurace je uvedena jako aktiva vybraného projektu LCS.  
    * Otevřete LCS pomocí https://lcs.dynamics.com. Otevřete projekt, který byl použit dříve pro registraci úložiště, otevřete Knihovnu majetku pro tento projekt a rozbalte obsah s typem majetku Konfigurace GER – odeslané konfigurace ER budou nyní k dispozici. Všimněte si, že odeslané konfigurace LCS je možné importovat do jiné instance aplikace Microsoft Dynamics 365 for Finance and Operations Enterprise edition, pokud poskytovatelé mají přístupová práva k tomuto projektu LCS.  

