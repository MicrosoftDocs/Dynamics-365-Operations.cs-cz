---
title: Import konfigurace převodu kreditu ve formátu ISO20022
description: Tento postup ukazuje, jak importovat konfiguraci elektronického výkaznictví pro platby dodavatelů.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee7e69611d31d2577ebafdfc059b0936aef0520b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174791"
---
# <a name="import-iso20022-credit-transfer-configuration"></a>Import konfigurace převodu kreditu ve formátu ISO20022

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup ukazuje, jak importovat konfiguraci elektronického výkaznictví pro platby dodavatelů. Formát pro peněžní převod podle německé normy ISO 20022 slouží jako příklad. Tento postup lze použít pro jiný dostupný formát elektronického výkaznictví. 

Tento úkol byl vytvořen pomocí ukázkových dat společnosti DEMF, ale k jeho dokončení můžete použít ukázková data libovolné společnosti.

Toto je první z pěti úkolů, které společně popisují proces platby dodavatele pomocí konfigurací elektronického výkaznictví. Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.

1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
2. V seznamu dostupných poskytovatelů konfigurace vyberte Microsoft.
3. Klikněte na možnost Nastavit jako aktivní.
4. Klikněte na možnost Úložiště.
5. Klikněte na možnost Otevřít.
6. Klepněte na tlačítko Zobrazit filtry.
7. Použijte následující filtry: Do pole Název konfigurace zadejte hodnotu filtru ISO20022 Credit transfer (DE) a použijte operátor filtru začíná na
    * Případně vyhledejte konfiguraci v seznamu, vyberte ji a převeďte na úlohu importu.  
8. Klepněte na tlačítko Importovat.
    * Pokud tlačítko Importovat není k dispozici, znamená to, že tato konfigurace je již po importu.  
9. Klepněte na tlačítko Ano.
