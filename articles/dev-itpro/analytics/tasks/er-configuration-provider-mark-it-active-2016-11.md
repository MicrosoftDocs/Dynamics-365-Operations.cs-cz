--- 
title: "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního pro elektronické výkaznictví (ER)"
description: "Následující procedura vysvětluje, jak uživatel přiřazený k roli Správce systému nebo Návrhář elektronického výkaznictví může vytvořit poskytovatele konfigurace pro elektronické výkaznictví."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bdb3a3857a7293828a7766b6988c123a43e0673c
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-configuration-providand-mark-it-as-active-for-electronic-reporting-er"></a>Vytvoření poskytovatele konfigurace a jeho označení jako aktivního pro elektronické výkaznictví (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Následující procedura vysvětluje, jak uživatel přiřazený k roli Správce systému nebo Návrhář elektronického výkaznictví může vytvořit poskytovatele konfigurace pro elektronické výkaznictví. Každá konfigurace ER bude odkazovat na zprostředkovatele jako na autora konfigurace. V tomto příkladu vytvoříte konfiguraci poskytovatele pro vzorovou společnost Litware, Inc. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace poskytovatele ER se sdílí mezi všemi společnostmi.


## <a name="create-a-provider"></a>Vytvoření poskytovatele
1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
2. Klikněte na Poskytovatelé konfigurace.
3. Klikněte na položku Nová.
    * Záznam poskytovatele má jedinečný název a adresu URL. Pokud záznam pro společnosti Litware, Inc. (http://www.litware.com) již existuje, zkontrolujte obsah této stránky a přeskočte tento postup.  
4. Zadejte Litware, Inc. do pole Název.
    * Litware, Inc.  
5. V poli internetové adresy zadejte "http://www.litware.com".
    * http://www.litware.com  
6. Klikněte na položku Uložit.
7. Zavřete stránku.

## <a name="select-as-an-active-provider"></a>Výběr ve formě aktivního poskytovatele
1. Vyberte poskytovatele Litware, Inc.
2. Klikněte na možnost Nastavit jako aktivní.


