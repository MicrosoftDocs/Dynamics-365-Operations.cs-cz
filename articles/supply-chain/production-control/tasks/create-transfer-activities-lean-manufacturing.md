---
title: Vytváření aktivit převodu pro lean manufacturing
description: Vytvořte aktivitu převodu pro lean manufacturing.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 629acdebd321154873feddcdfd8555d33e931f4f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996819"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a>Vytváření aktivit převodu pro lean manufacturing

[!include [banner](../../includes/banner.md)]

Vytvořte aktivitu převodu pro lean manufacturing. 

Požadavky: 

1. Je nutné vytvořit výrobní tok a verzi, která není aktivní.

2. Je nutné pro sklad a umístění vytvořit časový rozsah od a do. V případě potřeby by měla být vytvořeno doplňování nebo doplněná pracovní buňka.


## <a name="find-the-production-flow-version"></a>Najděte verzi výrobního toku
1. Přejděte na Řízení výroby > Nastavení > Tok štíhlé výroby > Výrobního toky.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Nezapomeňte, že výrobní tok musí mít verzi ve stavu konceptu.  
3. Klikněte na odkaz na vybraném řádku v seznamu.

## <a name="create-a-new-activity"></a>Vytvořte novou aktivitu
1. Klepněte na aktivity.
    * Ujistěte se, že vybraný výrobní tok má verzi v konceptu a tuto verzi vyberte.  
2. Klepněte na Vytvořit novou aktivitu plánu.
3. Klepněte na tlačítko Další.
4. Zadejte hodnotu do pole Název.
5. V poli Aktivita vyberte položku „Převod“.
6. V poli Množství procesu zadejte číslo.
7. Klepněte na tlačítko Další.

## <a name="select-the-work-cells"></a>Vyberte pracovní buňky
1. V poli Doplňování klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Chcete-li používat výstupní místo pracovní buňky jako z umístění v aktivitě převodu, vyberte pracovní buňku. Totéž lze provést s doplněnou pracovní buňkou, která nastavuje cílové umístění aktivit převodu.  
2. Klikněte na odkaz na vybraném řádku v seznamu.

## <a name="define-the-inventory-updates"></a>Definujte aktualizace zásob
1. Vyberte možnost v poli Typ produktu.
    * Nezapomeňte, že převod nemění typ produktu. Můžete převést hotové výrobky nebo polotovary (převod mezi dvěma aktivitami výrobního toku a případně kanbanového toku).     Při převodu hotových výrobků můžete vybrat výdej nebo příjem výsledků ve skladové transakci.  

## <a name="define-the-transfer-locations"></a>Definujte umístění převodu
1. Klepněte na tlačítko Další.
2. V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. V poli Umístění kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Klikněte na odkaz na vybraném řádku v seznamu.
7. V poli Dopravce vyberte hodnotu „Přepravce“.
    * Možnosti zahrnují: Přepravce – organizace provozující expediční sklad, příjemce – organizace provozující příjem ze skladu, dopravce – dodavatel třetí strany. Pokud pracující organizace je dodavatelem, vyžaduje aktivita převodu smlouvu o subdodavatelství.  
8. Klepněte na tlačítko Další.

## <a name="define-the-activity-times"></a>Definujte čas aktivity
1. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Je požadována definice modulu Runtime. Modul Runtime se používá k výpočtu nákladů a doby propustnosti kanbanových úloh. Moduly Runtime nejsou používány k výpočtu vytížení kapacity a spotřeby, což je počítáno podle času cyklu, odvozeného z úlohy verze výrobního toku.  
2. Do pole Čas zadejte číslo.
3. Zadejte hodnotu do pole Jednotka.
4. Vyberte jednotku času.
5. V poli Podle množství zadejte číslo.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Časy čekání jsou volitelné.  
7. Do pole Čas zadejte číslo.
8. Zadejte hodnotu do pole Jednotka.
9. Vyberte jednotku času.
10. V poli Podle množství zadejte číslo.
11. Klepněte na tlačítko Další.
12. Klepněte na tlačítko Dokončit.
13. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]