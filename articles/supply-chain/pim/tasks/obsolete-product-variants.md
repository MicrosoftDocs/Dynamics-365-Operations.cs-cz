---
title: Nalezení zastaralých variant produktů
description: Tato procedura ukazuje, jak nalézt zastaralé uvolněné produkty nebo varianty produktu a jak přiřadit stav životního cyklu produktu k zastaralým produktům.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 212e2a3a4ea38e60af16b8a50fdfe6f038666fdc241e3bb28ad5c57d6149ccd7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765923"
---
# <a name="find-obsolete-product-variants"></a>Nalezení zastaralých variant produktů 

[!include [banner](../../includes/banner.md)]

Tato procedura ukazuje, jak nalézt zastaralé uvolněné produkty nebo varianty produktu a jak přiřadit stav životního cyklu produktu k zastaralým produktům. Předpoklad: Je nutné definovat nejméně jeden stav životního cyklu produktu, který není aktivní pro plánování, ještě před přehráním tohoto Průvodce záznamem úloh.


## <a name="run-a-simulation"></a>Spuštění simulace ceny
1. Přejděte na Správa informací o produktech > Pravidelné úlohy > Změnit stav životního cyklu zastaralé produktů.
2. V poli Stav cyklu životnosti nového produktu zadejte nebo vyberte hodnotu.
3. V datovém poli Spustit simulaci bez aktualizace dat produktu vyberte Ano.
4. V poli Vyloučit produkty vytvořené za tento počet dní zadejte číslici.
5. V poli Vyloučit produkty používané v transakcích (za tento počet) dní zadejte číslici.
6. Rozbalte oddíl Záznamy k zahrnutí.
7. Klepněte na tlačítko Filtr.
8. Označte v seznamu vybraný řádek.
9. Zadejte hodnotu do pole Kritéria.
10. Klikněte na tlačítko OK.
11. Klikněte na tlačítko OK.

> [!NOTE]
> Doporučujeme spustit simulaci v dávce, pokud plánujete vyhledávat velký počet produktů. Ujistěte se také, že simulace není spuštěna během nejaktivnější pracovní doby společnosti.  

## <a name="review-the-simulation-results"></a>Projděte si výsledky simulace.
1. Přejděte na možnost Správa informací o produktech > Dotazy a sestavy > Historie údržby stavu životního cyklu produktu.
   
> [!NOTE]
> Na této stránce můžete zkontrolovat výsledky simulace a vyhodnotit počet produktů a variant produktů, který bude přidružen k novému stavu životního cyklu produktu při spuštění aktualizace bez simulace.  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a>Spuštění aktualizace stavu životního cyklu produktu pro zastaralé produkty
1. Zavřete stránku.
2. Přejděte na Správa informací o produktech > Pravidelné úlohy > Změnit stav životního cyklu zastaralé produktů.
3. Rozbalte oddíl Záznamy k zahrnutí.

> [!NOTE]
> Všimněte si, že byl uložen poslední výběr.  

4. V datovém poli Spustit simulaci bez aktualizace dat produktu vyberte Ne.
5. Rozbalte sekci Spustit na pozadí.

> [!NOTE]
> V závislosti na počtu ovlivněných produktů a variant produktů zvažte tuto úlohu spustit jako dávku. Nespouštějte velkou úlohu aktualizace během nejvíce aktivní pracovní doby ve společnosti.  

6. Klikněte na tlačítko OK.
7. Přejděte na možnost Správa informací o produktech > Dotazy a sestavy > Historie údržby stavu životního cyklu produktu.

> [!NOTE]
> Zkontrolujte změněné uvolněné produkty a varianty produktu.  

8. Vyhledejte na seznamu požadovaný záznam a vyberte ho.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]