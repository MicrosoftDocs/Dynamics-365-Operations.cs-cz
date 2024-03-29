---
title: Základní nastavení uvolněného základního produktu
description: Tento článek popisuje, jak dokončit minimální požadované nastavení před použitím základního produktu ve verzích kusovníku.
author: t-benebo
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a403600bfdc257587441b5b5a907981d5eebaf58
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844845"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a>Základní nastavení uvolněného základního produktu

[!include [banner](../../includes/banner.md)]

Tento článek popisuje, jak dokončit minimální požadované nastavení před použitím základního produktu ve verzích kusovníku.

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