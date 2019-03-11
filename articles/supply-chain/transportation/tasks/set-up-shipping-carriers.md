---
title: Nastavení dopravců
description: Tento postup popisuje, jak nastavit dopravce a definujte podrobnosti například pro službu, způsob dodávky, úhradu přepravy, omezení přepravy nebo sazbu expedice.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c5ac13d17c97f20ee79e7faf57c570f02158424
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "314479"
---
# <a name="set-up-shipping-carriers"></a>Nastavení dopravců

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje, jak nastavit dopravce a definujte podrobnosti například pro službu, způsob dodávky, úhradu přepravy, omezení přepravy nebo sazbu expedice. Koordinátor přepravy potom může přiřadit dopravce k příchozímu nebo odchozímu vytížení.


## <a name="create-a-new-shipping-carrier"></a>Vytvoření nového dopravce
1. Přejděte do nabídky Správa přepravy > Nastavení > Dopravci > Dopravci.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Dopravce dodávky .
4. Zadejte hodnotu do pole Název.
5. V poli Režim kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
7. Klikněte na odkaz na vybraném řádku v seznamu.

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>Zadání obecných informací pro dopravce
1. Přepněte rozšíření oddílu Přehled.
2. Zaškrtněte nebo zrušte zaškrtnutí políčka Aktivovat dopravce.
3. V poli Dodavatel kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Vyberte účet dodavatele, ke kterému chcete přiřadit dopravce.  
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. V poli Typ úhrady přepravy vyberte požadovanou možnost.
    * Vyberte Ručně, pokud chcete použít stránku Úhrada přepravy, nebo vyberte EDI a nechte aktualizovat úhrady pomocí služby Electronic Data Interchange (EDI).  
7. Zaškrtněte nebo zrušte zaškrtnutí políčka Aktivovat hodnocení dopravce.

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>Vytvoření nezbytných služeb pro dopravce
1. Přepněte rozšíření oddílu Služby.
2. Klikněte na položku Nová.
3. Označte v seznamu vybraný řádek.
4. Zadejte hodnotu do pole Služba dopravce.
5. Zadejte hodnotu do pole Název.
6. V poli Metoda přepravy kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
7. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
8. Klikněte na odkaz na vybraném řádku v seznamu.

## <a name="set-up-the-address-for-the-carrier-optional"></a>Nastavení adresy pro dopravce (volitelné)
1. Přepněte rozšíření oddílu Adresy.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Název nebo popis.
4. V poli Země / oblast kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. V poli PSČ kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
7. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
8. Klikněte na odkaz na vybraném řádku v seznamu.
9. Zadejte hodnotu do pole Ulice.
10. Klikněte na tlačítko OK.

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>Nastavení profilu hodnocení pro dopravce
1. Rozbalte oddíl Profily sazeb.
2. Klikněte na položku Nová.
3. Označte na seznamu vybraný řádek.
4. Zadejte hodnotu do pole Profil sazeb.
5. Zadejte hodnotu do pole Název.
6. V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
7. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
8. Klikněte na odkaz na vybraném řádku v seznamu.
9. V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
10. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
11. Klikněte na odkaz na vybraném řádku v seznamu.
12. V poli Výpočet přepravních sazeb kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Vyberte modul sazeb, který je v souladu se smlouvou, které máte s dopravcem.  
13. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
14. Klikněte na odkaz na vybraném řádku v seznamu.
15. V poli Hlavní sazba kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
16. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
17. Klikněte na odkaz na vybraném řádku v seznamu.
18. V poli Modul mezioperačního času kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
19. Klikněte na odkaz na vybraném řádku v seznamu.
20. Klikněte na položku Uložit.

