--- 
title: "Příprava datového modelu k použití souborů pro správu dokumentů ve formátech výstupu"
description: "Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9f99259056fab2d56d1ccf7487681c183551c64f
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="prepare-data-model-to-use-document-management-files-in-format-outputs"></a>Příprava datového modelu k použití souborů pro správu dokumentů ve formátech výstupu

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví. Tyto kroky lze provést v rámci libovolné společnosti.

K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".

Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Získání přístupu k seznamu konfigurací poskytovaných společností Microsoft
1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
    * Ujistěte se, že poskytovatel 'Litware, Inc.' je k dispozici a označen jako aktivní.  
2. Vyberte Litware, Inc. Poskytovatel
3. Klikněte na možnost Úložiště.
    * Pokud již existuje úložiště typu Zdroje operace, přeskočte zbývající kroky aktuální dílčí úlohy.  
4. Klepnutím na možnost Přidat otevřete dialogové okno.
5. V poli Typ úložiště konfigurace zadejte "Provozní prostředky".
6. Klikněte na Vytvořit úložiště.
7. Klikněte na tlačítko OK.

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a>Získání konfigurace modelu odběratele poskytnuté společností Microsoft
1. Klepněte na tlačítko Zobrazit filtry.
2. Použijte následující filtry: Zadejte hodnotu filtru Provozní prostředky do pole Název pomocí operátoru filtru "začíná na". Jako hodnotu filtru do pole popis zadejte "" pomocí operátoru filtru "začíná na".
3. Klepněte na tlačítko Zobrazit filtry.
4. Klikněte na možnost Otevřít.
5. Ve stromovém zobrazení vyberte možnost CustomerCreditTransferInitiation.
    * Vyberte konfiguraci modelu "Model faktury odběratele" k importu.  
6. Klepněte na tlačítko Importovat.
    * Klikněte na Import pro verzi 1 vybrané konfigurace.  
7. Klepněte na tlačítko Ano.
8. Zavřete stránku.
9. Zavřete stránku.
10. Klikněte na Konfigurace výkaznictví.
11. Ve stromovém zobrazení vyberte možnost CustomerCreditTransferInitiation.

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a>Vytvořte odvozený model na podporu přístupu k souborům správy dokumentů.
    * Vytvoříte vlastní konfiguraci modelu faktury odběratele vyplývající z konfigurace dodávané společností Microsoft. Pomocí této konfigurace budete implementovat přístup k souborům Správy dokumentů a zpřístupníte je pro elektronické dokumenty, které vytvoříte na základě tohoto modelu.  
1. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
2. V poli Nový zadejte „Odvodit z názvu: Model faktury zákazníka, Microsoft“.
3. Zadejte hodnotu Model faktury odběratele (vlastní) do pole Název.
    * Model faktury odběratele (vlastní)  
4. Klepněte na možnost Vytvořit konfiguraci.


