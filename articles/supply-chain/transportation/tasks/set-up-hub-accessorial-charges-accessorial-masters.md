---
title: Nastavení nákladů na dodatečnou službu centra a hlavních dodatečných služeb
description: Tento postup popisuje vytvoření hlavní dodatečnou služby pro centrum a použití této hlavní položky k vytvoření poplatků za dodatečnou službu centra.
author: ShylaThompson
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSCarrierAccessorial,TMSAccessorialMaster, TMSHubAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e67992c9e744b6337cf4921e06cc7886dead8021102d263022f67940c3e7669b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720125"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a>Nastavení nákladů na dodatečnou službu centra a hlavních dodatečných služeb

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]