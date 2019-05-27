---
title: Základní nastavení uvolněného základního produktu
description: Tento postup popisuje, jak dokončit minimální požadované nastavení před použitím základního produktu ve verzích kusovníku.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d3a91977c38c0ce0f9fe114bec943c7cb32a5d4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568757"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a>Základní nastavení uvolněného základního produktu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje, jak dokončit minimální požadované nastavení před použitím základního produktu ve verzích kusovníku.

Jedná se o třetí postup z osmi, který vysvětluje vytvoření kombinací konfigurace založené na dimenzích. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.

1. Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte základní produkt, který jste uvolnili v druhém postupu. Tento základní produkt je vytvořen s technologií konfigurace založené na dimenzích.  
3. V podokně akcí klikněte na možnost Produkt.
4. Kliknutím na možnost Skupiny dimenzí otevřete dialog Zanechat.
5. V poli Skupina dimenze úložiště kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Skupina dimenze úložiště určuje, které dimenze úložiště jsou použity pro transakci produktu. Pro tento postup vyberte Lokalita.  
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. V poli Skupina sledovací dimenze kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
9. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Skupina sledovacích dimenzí určuje, které sledovací dimenze jsou použity pro transakci produktu. Pro tento postup vyberte Žádné.  
10. Klikněte na odkaz na vybraném řádku v seznamu.
11. Klikněte na tlačítko OK.
12. Klikněte na odkaz na vybraném řádku v seznamu.
13. Klikněte na položku Upravit.
    * Otevřete formulář Podrobnosti o uvolněném produktu a pokračujte v nastavování.  
14. V poli Skupina modelů položek kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
15. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Skupiny modelů položek obsahují nastavení určující, jak jsou položky kontrolovány a zpracovávány při příjmu a výdeji položek. Také určují způsob výpočtu spotřeby položek. Pro tento postup vyberte FIFO.  
16. Klikněte na odkaz na vybraném řádku v seznamu.
17. Rozbalte nebo sbalte oddíl Správa nákladů.
18. V poli Skupina položek kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
19. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Skupiny zboží se používají ke správě skladových zásob tak, že se skladové položky rozdělí na skupiny. Pro tento postup vyberte CarAudio.  
20. Klikněte na odkaz na vybraném řádku v seznamu.
21. V podokně akcí klikněte na položku Plán.
22. Klikněte na Výchozí nastavení objednávky.
23. V poli Výchozí typ objednávky vyberte možnost.
    * Zvolením možnosti Výroba zadejte, že výchozí možností zásob pro tento základní produkt je jeho výroba.  
24. Zavřete stránku.
25. Zavřete formulář Podrobnosti o uvolněném produktu.

