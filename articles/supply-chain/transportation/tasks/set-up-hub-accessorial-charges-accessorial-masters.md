--- 
title: "Nastavení nákladů na dodatečnou službu centra a hlavních dodatečných služeb"
description: "Tento postup popisuje vytvoření hlavní dodatečnou služby pro centrum a použití této hlavní položky k vytvoření poplatků za dodatečnou službu centra."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6381416640ffacf0a9d96d7da96bc33612ca7137
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a>Nastavení nákladů na dodatečnou službu centra a hlavních dodatečných služeb

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje vytvoření hlavní dodatečnou služby pro centrum a použití této hlavní položky k vytvoření poplatků za dodatečnou službu centra. Procedura používá soubor dat USMF. Toto nastavení obvykle provádí koordinátor přepravy.


## <a name="set-up-a-hub-master"></a>Nastavení hlavního centra
1. Přejděte do nabídky Správa přepravy > Nastavení > Ohodnocení > Hlavní dodatečné služby.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Hlavní dodatečná služba.
4. Zadejte hodnotu do pole Název.
5. Vyberte možnost Centrum v poli Typ dodatečné služby.
6. Klikněte na položku Uložit.
7. Zavřete stránku.

## <a name="set-up-a-hub-accessorial-charge"></a>Nastavení poplatků za dodatečnou službu centra
1. Přejděte do nabídky Správa přepravy > Nastavení > Ohodnocení > Poplatky za dodatečnou službu centra.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole ID dodatečné služby centra.
4. V poli Centrum kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
6. Vyberte možnost v poli Pozice centra.
    * Můžete vytvořit náklady za vyzvednutí nebo za předání. V závislosti na výběru se náklady použijí na odpovídající segment přepravy na trase.  
7. V poli Hlavní dodatečná služba kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
8. Klikněte na odkaz na vybraném řádku v seznamu.
    * Vyberte hlavní položku, kterou jste právě vytvořili.  
9. Klikněte na položku Uložit.
10. Zavřete stránku.


