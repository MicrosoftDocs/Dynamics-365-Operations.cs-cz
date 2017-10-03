--- 
title: "Nastavení jednotlivých číselných řad"
description: "Číselné řady slouží ke generování čitelných, jedinečných identifikátorů pro záznamy hlavních dat a záznamy transakcí, které je požadují."
author: sericks007
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5c63022586f24cc1a50f7734910f15b237d35216
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-number-sequences-on-an-individual-basis"></a>Nastavení jednotlivých číselných řad

[!include[task guide banner](../../includes/task-guide-banner.md)]

Číselné řady slouží ke generování čitelných, jedinečných identifikátorů pro záznamy hlavních dat a záznamy transakcí, které je požadují. Hlavní záznam dat nebo transakce, která vyžaduje identifikátor, je označován jako odkaz. Než bude možné vytvořit nové záznamy pro odkaz, musíte nastavit číselné řady a spojit je s odkazem. Můžete nastavit všechny požadované číselné řady současně pomocí průvodce Nastavení číselných řad, nebo můžete vytvořit nebo upravit jednotlivé číselné řady na stránce Číselné řady.

1. Přejděte na Správa organizace > Číselné řady > Číselné řady.
2. Klikněte na Číselná řada.
3. Zadejte hodnotu do pole Kód číselné řady.
4. Zadejte hodnotu do pole Název.
5. Rozbalte sekci Parametry rozsahu.
    * Na pevné záložce Parametry rozsahu vyberte rozsah pro číselnou řadu a vyberte obor hodnot.     Rozsah určuje, které organizace používají číselnou řadu. Kromě toho číselné řady, které mají rozsah jiný než Sdílený, mohou mít segmenty, které odpovídají jejich rozsahu. Například číselná řada s rozsahem Právnická osoba může obsahovat segment právnické osoby. Další informace o oborech naleznete v tématu nápovědy "Přehled číselné řady".  
6. Rozbalte sekci Segmenty.
    * Na pevné záložce Segmenty přidáním, odebráním a změnou uspořádání segmentů určete formát pro číselné řady.  
    * Číselné řady všech oborů mohou obsahovat konstantní segmenty a alfanumerické segmenty. Konstantní segmenty obsahují sadu alfanumerických znaků, které se nemění. Pomocí tohoto typu segmentu můžete přidat pomlčky nebo jiné oddělovače mezi segmenty číselných řad. Alfanumerické segmenty obsahují kombinaci symbolů čísel (#) a ampersandy (&). Tyto znaky představují písmena a čísla, která se zvýší pokaždé, když se použije číslo z řady. Použijte znak čísla (#) k označení rostoucích čísel a znak ampersand (&) k označení rostoucích písmen. Formát #####_2014 například vytvoří řadu 00001_2014, 00002_2014 atd.     Musí obsahovat alespoň jeden alfanumerický segment. Segmenty oboru, například společnost nebo právnická osoba, nejsou povinné. Nicméně v případě, že formát neobsahuje segmenty oboru, čísla pro vybraný odkaz jsou stále generována pro obor.  
7. Rozbalte sekci Odkazy.
    * Na pevné záložce Odkazy vyberte typ dokumentu nebo záznamu, ke kterému chcete přiřadit číselnou řadu.     Tento krok je volitelný pro sekvence, které jsou definovány pro vzorce využití speciálních aplikací. V těchto scénářích je generováno nové číslo pomocí hodnoty kódu číselné řady nebo ID, bez použití odkazu. Příkladem vzorce použití speciální aplikace je řada dokladů použitá pro specifické názvy deníků. Nedoporučuje se však používat tyto vzory.  
8. Rozbalte sekci Obecné.
    * Na pevné záložce Obecné určete, zda je číselná řada manuální a souvislá nebo nesouvislá. Navíc zadejte nejnižší a nejvyšší čísla, která lze použít v číselné řadě.     Nedoporučujeme nesouvislou číselnou řadu změnit na souvislou číselnou řadu. Číselná řada nebude skutečně souvislá. Tato změna může způsobit narušení duplicitního klíče v databáze. Navíc souvislé číselné řady mají větší vliv na výkon.   
9. Klikněte na položku Uložit.


