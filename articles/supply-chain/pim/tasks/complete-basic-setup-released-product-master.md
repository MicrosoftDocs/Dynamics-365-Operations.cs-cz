---
title: Základní nastavení uvolněného základního produktu
description: Toto téma popisuje, jak dokončit minimální požadované nastavení před použitím základního produktu ve verzích kusovníku.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ac4ceeb3e21ab089eb16565bb6e38c7eb44be80
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423824"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a>Základní nastavení uvolněného základního produktu

[!include [banner](../../includes/banner.md)]

Toto téma popisuje, jak dokončit minimální požadované nastavení před použitím základního produktu ve verzích kusovníku.

Jedná se o třetí postup z osmi, který vysvětluje vytvoření kombinací konfigurace založené na dimenzích. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.

1. Klikněte na **Navigační podokno > Moduly > Řízení informací o produktech > Produkty > Vydané produkty**.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho. Vyberte základní produkt, který jste uvolnili v druhém postupu. Tento základní produkt je vytvořen s technologií konfigurace založené na dimenzích.  
3. V podokně akcí klikněte na možnost **Produkt**.
4. Kliknutím na možnost **Skupiny dimenzí** otevřete dialog Zanechat.
5. V poli **Skupina dimenze úložiště** výběrem tlačítka rozevíracího seznamu otevřete vyhledávání.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho. Skupina dimenze úložiště určuje, které dimenze úložiště jsou použity pro transakci produktu. Pro tento postup vyberte **Lokalita**.  
7. V poli **Skupina sledovací dimenze** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
8. Vyhledejte na seznamu požadovaný záznam a vyberte ho. Skupina sledovacích dimenzí určuje, které sledovací dimenze jsou použity pro transakci produktu. Pro tento postup vyberte **Žádné**.  
9. Klikněte na tlačítko **OK**.
10. Klikněte na možnost **Upravit**.
11. V poli **Skupina modelů položek** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
12. Vyhledejte na seznamu požadovaný záznam a vyberte ho. Skupiny modelů položek obsahují nastavení určující, jak jsou položky kontrolovány a zpracovávány při příjmu a výdeji položek. Také určují způsob výpočtu spotřeby položek. Pro tento postup vyberte **FIFO**.  
13. Rozbalte oblast **Správa nákladů**.
14. V poli **Skupina položek** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
15. Vyhledejte na seznamu požadovaný záznam a vyberte ho. Skupiny zboží se používají ke správě skladových zásob tak, že se skladové položky rozdělí na skupiny. Pro tento postup vyberte **CarAudio**.  
16. V podokně akcí zvolte **Plán**.
17. Vyberte **Výchozí nastavení pořadí produktů**.
18. V poli **Výchozí typ objednávky** vyberte možnost. Zvolením možnosti **Výroba** zadejte, že výchozí možností zásob pro tento základní produkt je jeho výroba.  
19. Zvolte **Uložit**.
20. Zavřete stránku.
21. Zavřete formulář **Podrobnosti o uvolněném produktu**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]