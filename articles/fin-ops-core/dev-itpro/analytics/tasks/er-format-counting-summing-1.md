---
title: Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 1 - Vytvoření formátu)
description: Tento článek popisuje, jak nakonfigurovat formát elektronického výkaznictví tak, aby počítal a sčítal na základě dat již vygenerovaného textového výstupu. (část 1)
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
- ERSolutionTable
ms.openlocfilehash: b9e0128e55ba6ab356d6942020a34e5e74d6b7e2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290687"
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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
