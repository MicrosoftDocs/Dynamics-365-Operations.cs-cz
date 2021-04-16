---
title: Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 1 - Příprava datového modelu)
description: Toto téma popisuje, jak nakonfigurovat formát elektronického výkaznictví (ER) na použití souborů (příloh) správy dokumentů ve výstupu ER. (část 1)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6b265c9af0635e6c9fb6295f7e8e4e353b2a5ba5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754931"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a>Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 1 - Příprava datového modelu)

[!include [banner](../../includes/banner.md)]

Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví. Tyto kroky lze provést v rámci libovolné společnosti.

K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v proceduře "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".

Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Získání přístupu k seznamu konfigurací poskytovaných společností Microsoft
1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.

    Ujistěte se, že poskytovatel 'Litware, Inc.' je k dispozici a označen jako aktivní.  

2. Vyberte Litware, Inc. Poskytovatel
3. Klikněte na možnost Úložiště.

    Pokud již existuje úložiště typu Zdroje operace, přeskočte zbývající kroky aktuální dílčí úlohy.  

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

    Vyberte konfiguraci modelu "Model faktury odběratele" k importu.  

6. Klepněte na tlačítko Importovat.

    Klikněte na Import pro verzi 1 vybrané konfigurace.  

7. Klepněte na tlačítko Ano.
8. Zavřete stránku.
9. Zavřete stránku.
10. Klikněte na Konfigurace výkaznictví.
11. Ve stromovém zobrazení vyberte možnost CustomerCreditTransferInitiation.

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a>Vytvořte odvozený model na podporu přístupu k souborům správy dokumentů.
Vytvoříte vlastní konfiguraci modelu faktury odběratele vyplývající z konfigurace dodávané společností Microsoft. Pomocí této konfigurace budete implementovat přístup k souborům Správy dokumentů a zpřístupníte je pro elektronické dokumenty, které vytvoříte na základě tohoto modelu.  
1. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
2. V poli Nový zadejte „Odvodit z názvu: Model faktury zákazníka, Microsoft“.
3. Zadejte hodnotu Model faktury odběratele (vlastní) do pole Název.
4. Klepněte na možnost Vytvořit konfiguraci.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]