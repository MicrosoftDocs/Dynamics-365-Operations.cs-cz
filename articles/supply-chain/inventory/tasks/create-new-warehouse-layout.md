---
title: "Vytvoření nového rozvržení skladu"
description: "Tento postup popisuje způsob nastavení informací o umístění ve skladu."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 253440d81edd6f71b52ae349398e3c6a895bf05c
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-new-warehouse-layout"></a>Vytvoření nového rozvržení skladu

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje způsob nastavení informací o umístění ve skladu. To platí pouze pro sklady vytvořené pomocí "základních funkcí skladu" v modulu Řízení zásob, ne pro sklady, které jsou vytvořeny v modulu Řízení skladu. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.


## <a name="set-the-default-location-capacity"></a>Nastavte výchozí kapacitu skladového místa
1. Přejděte do nabídky Řízení zásob > Nastavení > Parametry řízení zásob a skladu.
2. Klikněte na kartu Umístění.
3. V poli Standardní šířka zadejte číslo.
4. V poli Standardní hloubka zadejte číslo.
5. V poli Standardní výška zadejte číslo.
6. Klikněte na položku Uložit.
7. Zavřete stránku.

## <a name="define-the-location-name-format"></a>Definujte formát názvu skladového místa
1. Přejděte do části Řízení zásob > Nastavení > Rozdělení zásob > Sklady.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Sklad.
4. Zadejte hodnotu do pole Název.
5. V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
7. Přepněte rozšíření oddílu Názvy lokalit.
    * Možnosti v tomto oddílu definují výchozí formát pro názvy umístění. V našem příkladu použijeme čísla uličky, stojanu a police.  
8. Nastavte možnost Včetně uličky na Ano.
9. Nastavte možnost Včetně stojanu na Ano.
10. V poli Formát zadejte pro stojan hodnotu.
    * Například: -##  
11. Nastavte možnost Včetně police na Ano.
12. V poli Formát zadejte pro polici hodnotu.
    * Například: -##  

## <a name="define-warehouse-locations"></a>Definujte umístění ve skladu
1. V podokně akcí klikněte na možnost Sklad.
2. Klikněte na Průvodce skladovým místem.
3. Klepněte na tlačítko Další.
4. Zrušte výběr možnosti Výstupní překladiště
5. Zrušte výběr možnosti Hromadné umístění
6. Klepněte na tlačítko Další.
7. Klepněte na tlačítko Další.
8. Klepněte na tlačítko Další.
9. Klepněte na tlačítko Další.
10. Klepněte na tlačítko Další.
11. Klepněte na tlačítko Další.
12. Klepněte na tlačítko Další.
    * Všimněte si, že zobrazené fyzické dimenze na této stránce jsou ty, které jste nastavili na začátku tohoto postupu.  
13. Klepněte na tlačítko Další.
14. Klepněte na tlačítko Dokončit.
15. Zavřete stránku.
16. Aktualizujte stránku.

