---
title: Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 1 - Vytvoření formátu)
description: Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7a2559bdadbfc74a14bd0e7add9c2f794226e0b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141918"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a>Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 1 - Vytvoření formátu)

[!include [banner](../../includes/banner.md)]

Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu. Tyto kroky lze provést v rámci libovolné společnosti.

K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v proceduře "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".

Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Získání přístupu k seznamu konfigurací poskytovaných společností Microsoft
1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
    * Ujistěte se, že poskytovatel 'Litware, Inc.' je k dispozici a označen jako aktivní.  
2. Vyberte poskytovatele 'Litware, Inc'.  
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

