---
title: " Vytváření balení produktů pro nákupní objednávky"
description: Tato procedura vás provede vytvářením balíčku výrobku a jeho použití v nákupní objednávce.
author: josaw1
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb10164be8d7a0828169cf3865f884afaa2e8408472edebe4cb0c7d4db059d8c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723230"
---
# <a name="create-product-packages-for-purchase-orders"></a> Vytváření balení produktů pro nákupní objednávky

[!include [banner](../includes/banner.md)]

Tato procedura vás provede vytvářením balíčku výrobku a jeho použití v nákupní objednávce. Nákupní objednávka se použije k vytvoření objednávky na předdefinování sady produktů. Tato procedura používá data ukázkové společnosti USRT.


## <a name="create-a-product-package"></a>Vytvoření balení produktů
1. Přejděte na Retail and Commerce > Řízení zásob > Doplnění > Balení produktů.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Číslo balíku.
4. Zadejte nějakou hodnotu do pole Popis.
5. V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Klikněte na odkaz na vybraném řádku v seznamu.
7. Klepněte na možnost Přidat.
8. Do pole Číslo zboží zadejte „0160“.
9. V poli Velikost kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
10. Klikněte na odkaz na vybraném řádku v seznamu.
11. Zadejte číslo do pole Množství.
12. Klepněte na možnost Přidat.
13. Do pole Číslo zboží zadejte „0160“.
14. V poli Číslo varianty kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
15. Klikněte na odkaz na vybraném řádku v seznamu.
16. Zadejte číslo do pole Množství.
17. Klepněte na možnost Přidat.
18. Do pole Číslo zboží zadejte „0175“.
19. Zadejte číslo do pole Množství.
20. Klikněte na položku Uložit.
21. Zavřete stránku.

## <a name="add-package-to-purchase-order"></a>Přidání balíku k nákupní objednávce
1. Přejděte na Závazky > Nákupní objednávky > Všechny nákupní objednávky.
2. Klikněte na položku Nová.
3. V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Na seznamu vyberte stejného dodavatele, pro kterého byl balíček dříve vytvořený, pokud byl vybrán dodavatel.
5. Přepněte rozšíření oddílu Obecné.
6. V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
9. Klikněte na odkaz na vybraném řádku v seznamu.
10. Klepněte na tlačítko OK.
11. Přepněte rozšíření oddílu Podrobnosti řádku.
12. Klepněte na kartu Balení produktů.
13. Klikněte na Řádek nákupní objednávky.
14. Klikněte na Vytvořit řádky z balíků.
15. V rozevíracím seznamu vyhledejte a vyberte balíček produktu vytvořený v předchozím kroku.
16. Zadejte číslo do pole Množství.
17. Klikněte na položku Vytvořit.
18. Klikněte na položku Uložit.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]