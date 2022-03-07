---
title: Import konfigurace převodu kreditu ve formátu ISO20022
description: Tento postup ukazuje, jak importovat konfiguraci elektronického výkaznictví pro platby dodavatelů.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ffc86ba9dade0ae494ca4ace8d9f562da9c9527a4731493d892b60112293af3f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781129"
---
# <a name="import-iso20022-credit-transfer-configuration"></a>Import konfigurace převodu kreditu ve formátu ISO20022

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]