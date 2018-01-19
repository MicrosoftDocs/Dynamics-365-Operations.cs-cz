---
title: "Registrace spotřeby materiálu pomocí mobilního zařízení"
description: "Toto téma popisuje workflow, který umožňuje registraci spotřeby surovin ve výrobě pomocí ručního zařízení."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 525b5a21047f0f39b9cd15448c4096d17c0e2dbd
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="register-material-consumption-using-a-mobile-device"></a>Registrace spotřeby materiálu pomocí mobilního zařízení
Toto téma popisuje workflow, který umožňuje registraci spotřeby surovin ve výrobě pomocí ručního zařízení.

<a name="introduction"></a>Úvod
------------

Tento workflow platí v případě, že existují přísné požadavky na sledování materiálu. V těchto případech musí být vykázán přesný stav spotřeby pro účely zachování sledovatelnosti materiálů. Na tento proces lze nazírat jako na opačný proces, než jsou operace vyprázdnění předem nebo následně, kdy existuje posun mezi časem registrace a časem, kdy proběhne skutečná spotřeba. To vysvětluje, proč nelze pro některé materiály použít strategii sledování automatické spotřeby. Podívejme se na jednoduchý scénář, který vysvětluje postup při nastavování workflowu s povolením registrace spotřeby surovin ve výrobě pomocí ručního zařízení. [![nastavení workflowu pro povolení registrace spotřeby suroviny s použitím ručního zařízení](./media/scenario3.png)](./media/scenario3.png)

### <a name="scenario-details"></a>Podrobnosti scénáře

Proces souvislé výroby (5) spotřebovává surovinu RM-100 řízenou dávkou. Materiál je k dispozici v umístění Bulk-001 (1) pro registrační značku vozidla PL-1 se dvěma dávkami, B1 a B2, z nichž obě mají množství 100 kg. Práce ve skladu (2) je uvolněna a zpracována pro RM-100 a materiál je vyzvednut ze skladu Bulk-001 do vstupního místa výroby PIL-01 (3), které je definováno jako místo neřízené registrační značkou. Obsluha stroje zváží materiál ze vstupního místa výroby (3) a registruje hmotnost a číslo dávky jako spotřebované (4). Ze vstupního místa výroby je část materiálu ručně vložena do výrobního procesu v definovaných časových intervalech. Když obsluha stroje přidá materiál, je zvážen na váze a zaregistruje se číslo dávky.

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a>Nastavení workflowu při registraci spotřeby pomocí ručního zařízení
Vytvořte produkt dokončené výroby FG-100 s kusovníkem, kde je surovina řízenou dávkou RM-100. Přidejte dvě dávky B1 a B2 RM-100 v množství 100 do umístění: Bulk-001 s registrační značkou: PL-1. Princip vyprazdňování na řádku kusovníku pro RM-100 kusovníku je nastaven na **ruční**. Nastavte výchozí umístění výrobního vstupu na PIL-01. To můžete provést výběrem tohoto skladového místa jako vstupního místa výroby ve skladu 51.

1.  Vytvoření nové položky nabídky mobilních zařízení: 

-    **Název položky nabídky** – zaregistrujte spotřebu materiálu. 
-    **Název** - Zaregistrovat spotřebu materiálu 
-    **Režim** – nepřímé. 
-    **Kód činnosti** - Zaregistrovat spotřebu materiálu

2.  Přidejte položku nabídky do nabídky zařízení **Mobilní výroba**.
3.  Vytvořte výrobní zakázku dokončeného produktu: 

-    **Číslo položky** - FG-100 
-    **Lokalita** - 5 
-    **Sklad** - 51 
-    **Množství** - 150

Výrobní zakázka je **odhad** a **Uvolněno** a je vytvořena práce ve skladu.

4.  Dokončete práci pomocí workflowu pro vyzvednutí surovin pro přenosná zařízení pro výdej.

To přenese materiál z velkoskladu do vstupního místa výroby PIL 01. Po dokončení práce má materiál stav **vydáno na vstupní místo výroby**. Stav poté, co byla práce zpracována, může být buď **vyskladněno** nebo **Rezervované – fyzicky**. To je nakonfigurováno s parametrem **stav výdeje po vložení ve formuláři skladu**.

5.  Spusťte výrobní zakázku z klienta nebo v ručního zařízení spuštění pomocí položky nabídky **zahájení výroby**.

Po spuštění výrobní zakázky můžete zaregistrovat spotřeby materiálu s workflowem pro ručním zařízení. Začněme registrací spotřeby 25 kg dávky B1.

6.  Vyberte položku nabídky **Zaregistrovat materiál** **spotřeba** pro ruční zařízení a zadejte následující informace: 

-    Číslo výrobní zakázky  
-    Skladové místo, ve kterém se bude materiál spotřebovávat, je v tomto případě PIL-01. 
-    Číslo položky RM-100. 
-    Číslo dávky B1. 
-    Množství 25.

7.  Vyberte **OK**.

Všimněte si, že se na displeji zobrazí zpráva "Vytvoření řádku deníku". Ve výrobní zakázce se vytvoří otevřený deník typu **výrobní výdejka** pro číslo položky RM-100 a číslo dávky B1. 

Nyní můžete pokračovat v registraci, například v čísle dávky B2 a pokaždé, když vyberete **OK**, se do otevřeného deníku přidá nový řádek deníku. 

Po dokončení registrace vyberte možnost **Hotovo** k zaúčtování deníku a ukončení workflowu.

### <a name="additional-comments"></a>Další komentáře 

-   Pokud uživatel zruší workflow po vytvoření řádku deníku, tento deník je ve stavu nezaúčtované, ale jestli uživatel později použije workflow pro stejnou výrobní zakázku, budou řádky přidány do otevřeného deníku, nikoli do nového deníku.
-   Nový workflow podporuje také registrace sériového čísla.
-   Je možné registrovat číslo položky, která je definováno v kusovníku nebo v receptuře pro vybranou výrobní zakázku nebo dávkovou objednávku.
-   Může dojít k vyčerpání materiálu. Například pokud má být spotřebováno množství 100 kg materiálu, poté ji může být vyčerpán, pokud je množství například 105 kg.



