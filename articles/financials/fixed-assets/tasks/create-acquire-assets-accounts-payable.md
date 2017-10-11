--- 
title: "Vytvoření a získání majetku z modulu Závazky"
description: "Tento průvodce úkolem vás provede vytvořením a pořízením dlouhodobého majetku s procesem nákupu."
author: saraschi2
manager: AnnBe
ms.date: 11/10/2016
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
ms.openlocfilehash: f814d20bc16bb3334ae4bc449cc0d45843487023
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Vytvoření a získání majetku z modulu Závazky

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento průvodce úkolem vás provede vytvořením a pořízením dlouhodobého majetku s procesem nákupu.  Používá účetní a úředníky závazků a vzorovou společnost USMF.


## <a name="set-fixed-assets-parameters"></a>Nastavení parametrů dlouhodobého majetku
1. Přejděte na Dlouhodobý majetek > Nastavení > Parametry dlouhodobého majetku.
2. Rozbalte nebo sbalte oddíl Nákupní objednávky.
3. Označte pole Povolit pořízení majetku v části Nakupování.
4. Označte pole Vytvořit majetek při zaúčtování příjemky produktu nebo faktury.

## <a name="create-a-new-vendor-invoice"></a>Vytvoření nové faktury dodavatele
1. Přejděte na Závazky > Pracovní prostory > Záznam faktury dodavatele.
2. Klikněte na Nová faktura dodavatele.
3. V poli Účet faktury kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. Zadejte hodnotu do pole Číslo.
6. V poli Datum zaúčtování zadejte datum.
7. Klikněte na položku Přidat řádek.
8. V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Pro pořízení dlouhodobého majetku lze použít neskladované zboží nebo kategorie zásobování.  
9. Klikněte na odkaz na vybraném řádku v seznamu.
10. Zadejte číslo do pole Množství.
    * Jeden řádek faktury vytvoří pouze jeden dlouhodobý majetek bez ohledu na množství.  Hodnota pole Množství na faktuře se přesune do množství dlouhodobého majetku.  
11. Zadejte číslo do pole Jednotková cena.
12. Rozbalte nebo sbalte oddíl Podrobnosti řádku.
13. Klikněte na kartu Dlouhodobý majetek.
14. Označte pole Vytvořit nový dlouhodobý majetek.
15. V poli Skupina dlouhodobého majetku kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
16. V seznamu vyberte skupinu dlouhodobého majetku, kterou chcete použít pro vytvoření nového dlouhodobého majetku.
17. Klikněte na odkaz na vybraném řádku v seznamu.
18. Klikněte na položku Zaúčtovat.
    * Dlouhodobý majetek se vytvoří a pořídí při zaúčtování faktury.  

