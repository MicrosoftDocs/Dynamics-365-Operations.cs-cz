--- 
title: "Rozdělení dlouhodobého majetku"
description: "Tento průvodce záznamem úloh rozdělí procento jedné knihy majetku na novou knihu majetku."
author: saraschi2
manager: AnnBe
ms.date: 10/19/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5aea1aab9f6b084bd0c5bd2119639bff3555bb8a
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="split-a-fixed-asset"></a>Rozdělení dlouhodobého majetku

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento průvodce záznamem úloh rozdělí procento jedné knihy majetku na novou knihu majetku.  Používá účetní roli a vzorová data USMF.


## <a name="create-a-new-fixed-asset"></a>Vytvořit nový dlouhodobý majetek
1. Přejděte do části Dlouhodobý majetek > Dlouhodobý majetek > Dlouhodobý majetek.
2. Klikněte na položku Nová.
3. Zadejte nebo vyberte hodnotu v poli Skupina dlouhodobého majetku.
4. Poznamenejte si číslo dlouhodobého majetku pro pozdější použití v procesu rozdělení.
5. Zadejte hodnotu do pole Název.
6. Zavřete formulář.

## <a name="split-a-fixed-asset"></a>Rozdělení dlouhodobého majetku
1. V seznamu najděte a vyberte dlouhodobý majetek, který chcete rozdělit.
2. Klikněte na odkaz na vybraném řádku v seznamu.
3. Klepněte na Knihy.
    * Vyberte knihu určenou pro rozdělení na nový majetek.  
4. Klepněte na možnost Funkce.
5. Klikněte na Rozdělit dlouhodobý majetek.
6. Zadejte nebo vyberte hodnotu v poli Do dlouhodobého majetku.
7. V poli Do knihy kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
8. Zadejte datum do pole Datum transakce.
9. Zadejte číslo do pole Procento.
10. V poli Název deníku zadejte nebo vyberte hodnotu.
11. Klikněte na tlačítko OK.

## <a name="post-the-journal-transaction"></a>Zaúčtování transakce deníku
1. Přejděte na Dlouhodobý majetek > Položky deníku > Deník dlouhodobého majetku.
2. V seznamu vyberte deník vytvořený pomocí procesu rozdělení.
3. Klikněte na položku Řádky.
    * Ověřte, že byly vytvořeny řádky deníku.  Transakce Oprava pořizovací ceny byla vytvořena pro původní majetek s cílem snížit hodnotu o procento uvedené během procesu rozdělení.  Je vytvořena transakce pořízení pro nový majetek na stejnou částku.  
4. Klikněte na položku Zaúčtovat.


