---
title: Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 1 - Příprava datového modelu)
description: Tento článek popisuje, jak nakonfigurovat formát elektronického výkaznictví (ER) na použití souborů (příloh) správy dokumentů ve výstupu ER. (část 1)
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form:
- ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
- ERSolutionTable, ERSolutionCreateDropDialog
ms.openlocfilehash: f407555eca4c4bd08d09047e9d8f8512cb99d254
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291017"
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
