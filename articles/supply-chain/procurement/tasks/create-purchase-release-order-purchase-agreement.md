--- 
title: "Vytvoření dílčí nákupní objednávky z nákupní smlouvy"
description: "Tento postup popisuje použití nákupní smlouvy při vytváření nákupní objednávky."
author: mkirknel
manager: AnnBe
ms.date: 12/04/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cecda03dd4d224d4319f2b0b196560389bb54195
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a>Vytvoření dílčí nákupní objednávky z nákupní smlouvy

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje použití nákupní smlouvy při vytváření nákupní objednávky. Nákupní smlouva musí být použita při vytvoření nákupní objednávky, protože jsou v ní obecné podmínky, které musí být zkopírovány do záhlaví nákupní objednávky. Tento úkol obvykle provádí nákupčí. Nezbytným předpokladem pro tohoto průvodce je platná nákupní smlouva se závazkem na množství produktu pro dodavatele a položky. Stejný postup lze použít, máte-li nákupní smlouvou s jinými typy závazků. Tohoto průvodce můžete použít s ukázkových dat společnosti USMF. Pokud používáte data USMF, můžete nejprve použít průvodce „Vytvoření nákupní smlouvy“ k nastavení nutných předpokladů pro tohoto průvodce.


## <a name="create-a-purchase-order"></a>Vytvoření nákupní objednávky
1. Otevřete pracovní prostor pro přípravu nákupní objednávky.
2. Klikněte na možnost Nová nákupní objednávka.
3. V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Přepněte rozšíření oddílu Obecné.
7. V poli Nákupní smlouva kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Zde jsou uvedeny všechny dostupné smlouvy pro daného dodavatele. Najděte platnou smlouvu, kterou chcete použít.  
8. Klikněte na odkaz na vybraném řádku v seznamu.
9. Klepněte na tlačítko Ano.
10. Klikněte na tlačítko OK.

## <a name="add-a-line"></a>Přidání řádku
1. Zadejte hodnotu do pole Číslo zboží.
    * Pokud jsou u závazku konkrétní dimenze zásob nebo místa, je nutné zadat stejné hodnoty na řádku nákupní objednávky, aby bylo možné smlouvu použít.  
2. V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Site již může být vyplněn výchozí hodnotou z objednávky a od dodavatele. Pokud je vyplněn, tento krok vynechejte.  
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. Zadejte číslo do pole Množství.
    * Ověřte, že se cena zkopírovala ze závazku.  

## <a name="look-up-the-commitment"></a>Vyhledání závazku
1. Klikněte na položku Aktualizovat řádek.
2. Klikněte na položku Připojeno.
    * Zde můžete zjistit podrobnosti nákupní smlouvy. Například zde je cena a údaj, zda jsou cena a sleva pevné, což znamená, že při změně ceny nebo slevy na nákupní objednávce na jinou hodnotu, než která je v závazku, systém propojení odebere, aby řádek nákupní objednávky nesplňoval závazek. Můžete také vidět, zda je vybrána možnost Max je vynuceno, což znamená, že množství v závazku nelze překročit v součtu všech nákupů, které splňují daný závazek.  
3. Zavřete stránku.

## <a name="look-up-the-purchase-agreement"></a>Vyhledání nákupní smlouvy
1. V podokně akcí klikněte na položku Obecné.
2. Klikněte na možnost Nákupní smlouva.
3. Zavřete stránku.
4. Zavřete stránku.


