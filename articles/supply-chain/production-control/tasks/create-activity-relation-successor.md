--- 
title: "Vytvoření relace aktivity - následník"
description: "Tok aktivit ve štíhlém výrobním toku je zaznamenán prostřednictvím vztahů aktivity."
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 75a76252cc3cb6f3e7516309a7d9a6f2d1934ccd
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-activity-relation-successor"></a>Vytvoření relace aktivity: následník

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tok aktivit ve štíhlém výrobním toku je zaznamenán prostřednictvím vztahů aktivity. Tento záznam ukazuje, jak vytvořit relaci aktivity.

Požadavky:

- Výrobní tok a verze v režimu konceptu. 

- Dvě aktivity, které po sobě navzájem následují ve výrobním toku, jsou vytvořeny, ale nesouvisí.


## <a name="find-the-production-flow-version"></a>Najděte verzi výrobního toku 
1. Přejděte na Řízení výroby > Nastavení > Tok štíhlé výroby > Výrobního toky.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Označte v seznamu vybraný řádek.
5. V seznamu vyberte verzi konceptu.
    * Vztahy aktivit lze přidat do konceptu nebo aktivních verzí výrobního toku.  

## <a name="open-the-activity-overview"></a>Otevřete přehled aktivit
1. Klepněte na aktivity.
    * Nezapomeňte, že ve formuláři se zobrazují všechny aktivity výrobního toku přidělené k verzi výrobního toku, ve kterém pracujete.  

## <a name="add-a-successor"></a>Přidejte následníka
1. Klepněte na Přidat následníka.
2. V poli Aktivita klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. Zaškrtněte políčko Omezení.
6. V poli Hodnota omezení zadejte číslo.
    * Omezení času je čas naplánovaný mezi naplánovaným koncem předchůdce (datum splatnosti a čas) a plánovaným začátkem nástupce.  
7. Zadejte hodnotu do pole Jednotky.
8. Do pole Poměr času cyklu zadejte číslo.
    * Pokud obě aktivity běží ve stejném taktu, poměr času cyklu musí být 1. Pokud předchůdce běží dvojnásobnou rychlostí následníka, poměr musí být 2.   Poměry času cyklu se používají pro výpočet jednotlivých časů cyklu aktivit výrobního toku.  
9. Klikněte na tlačítko OK.
10. Zavřete stránku.
11. Klepněte na kartu panel mřížky.
12. Zavřete stránku.
13. Aktualizujte stránku.

