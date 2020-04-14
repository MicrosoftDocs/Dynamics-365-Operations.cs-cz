---
title: Zpracování rabatu pro platbu
description: Tento postup ukazuje převod schválených a zpracovaných rabatů odběratele na dobropisy.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 412e7df299a419642018a62e6e8febd5d59c65e1
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148436"
---
# <a name="process-rebates-for-payment"></a>Zpracování rabatu pro platbu

[!include [banner](../../includes/banner.md)]

Tento postup ukazuje převod schválených a zpracovaných rabatů odběratele na dobropisy. Tohoto průvodce můžete použít s ukázkovou společností USMF. Předpokladem pro tohoto průvodce je existence jednoho nebo více nároků na rabat ve stavu Označit. Pokud používáte USMF, před použitím tohoto průvodce použijte průvodce „Generování a zpracování rabatů odběratele“.


## <a name="convert-rebate-claims-to-credit-note"></a>Převedení nároků na rabat na dobropis
1. Přejděte do nabídky Všichni odběratelé.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. V podokně akcí klikněte na možnost Kolekce.
5. Klikněte na možnost Vyrovnat transakce.
6. Klepněte na možnost Funkce.
7. Klikněte na možnost Rabatový program.
    * Stránka Rabat uvádí nároky na rabat, které jste zpracovali na pracovní ploše pro rabat odběratele a které jsou ve stavu Označit.    
8. Klikněte na položku Upravit.
    * Zaškrtněte políčka v poli Označit u nároků, které chcete zahrnout do dobropisu.   
9. Klepněte na možnost Funkce.
10. Klikněte na možnost Vytvořit dobropis.
    * Zobrazí se zpráva informující o tom, že byl zaúčtován deník (je to ten deník spotřeby pohledávek zadaný na stránce Parametry pohledávek). To způsobí, že se skutečná částka závazku (Dal) přesune do zůstatku odběratele. To znamená, že na účtu odběratele bylo provedeno připsání a na účtu časového rozlišení rabatu bylo provedeno odepsání.  
11. Zavřete stránku.
12. Klikněte na možnost Zrušit.
    * Aktualizuje stránku, aby se zobrazily aktualizace.  
13. V podokně akcí klikněte na možnost Kolekce.
14. Klikněte na možnost Vyrovnat transakce.
    * Všimněte si, že transakce pro zápornou částku představující celkovou částku rabatu bez referenčního čísla faktury byla přidána k zůstatku odběratele.   
15. Klikněte na možnost Zrušit.

