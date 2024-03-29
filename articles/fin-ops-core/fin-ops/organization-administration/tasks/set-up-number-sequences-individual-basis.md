---
title: Nastavení číselných řad na jednotlivém základě
description: Tento článek vysvětluje nastavení číselných řad na jednotlivém základě.
author: SunilGarg
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceDetails
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7be72d348957c5c6494958276b2baa9c67d63c58
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904981"
---
# <a name="set-up-number-sequences-on-an-individual-basis"></a>Nastavení číselných řad na jednotlivém základě

[!include [banner](../../includes/banner.md)]

Tento článek vysvětluje nastavení číselných řad na jednotlivém základě. Číselné řady slouží ke generování čitelných, jedinečných identifikátorů pro záznamy hlavních dat a záznamy transakcí, které je požadují. Hlavní záznam dat nebo transakce, která vyžaduje identifikátor, je označován jako odkaz. Než bude možné vytvořit nové záznamy pro odkaz, musíte nastavit číselné řady a spojit je s odkazem. Můžete nastavit všechny požadované číselné řady současně pomocí průvodce **Nastavení číselných řad**, nebo můžete vytvořit nebo upravit jednotlivé číselné řady na stránce **Číselné řady**.

1. Přejděte na **Navigační podokno > Moduly > Správa organizace > Číselné řady > Číselné řady**.
2. Vyberte **Číselnou řadu**.
3. Zadejte hodnotu do pole **Kód číselné řady**.
4. Zadejte hodnotu do pole **Název**.
5. Na pevné záložce **Parametry rozsahu** vyberte rozsah pro číselnou řadu a vyberte obor hodnot z rozvíracího seznamu. Rozsah určuje, které organizace používají číselnou řadu. Kromě toho číselné řady, které mají rozsah jiný než **Sdílený**, mohou mít segmenty, které odpovídají jejich rozsahu. Například číselná řada s rozsahem **Právnická osoba** může obsahovat segment právnické osoby. Další informace o oborech naleznete v tématu nápovědy [Přehled číselné řady](../number-sequence-overview.md). 
6. Rozbalte sekci **Segmenty**.
    - Určete formát pro číselné řady přidáním, odebráním a změnou uspořádání segmentů.  
    - Číselné řady všech oborů mohou obsahovat *Konstantní segmenty* a *Alfanumerické segmenty*. Konstantní segmenty obsahují sadu alfanumerických znaků, které se nemění. Pomocí tohoto typu segmentu můžete přidat pomlčky nebo jiné oddělovače mezi segmenty číselných řad. Alfanumerické segmenty obsahují kombinaci symbolů čísel (#) a ampersandy (&). Tyto znaky představují písmena a čísla, která se zvýší pokaždé, když se použije číslo z řady. Použijte znak čísla (#) k označení rostoucích čísel a znak ampersand (&) k označení rostoucích písmen. Formát `#####_2014` například vytvoří řadu `00001_2014`, `00002_2014` atd. Musí obsahovat alespoň jeden alfanumerický segment. Segmenty oboru, například společnost nebo právnická osoba, nejsou povinné. Nicméně v případě, že formát neobsahuje segmenty oboru, čísla pro vybraný odkaz jsou stále generována pro obor.  
7. Rozbalte sekci **Odkazy**. Vyberte typ dokumentu nebo záznamu, ke kterému chcete přiřadit číselnou řadu. Tento krok je volitelný pro sekvence, které jsou definovány pro vzorce využití speciálních aplikací. V těchto scénářích je generováno nové číslo pomocí hodnoty kódu číselné řady nebo ID, bez použití odkazu. Příkladem vzorce použití speciální aplikace je řada dokladů použitá pro specifické názvy deníků. Nedoporučuje se však používat tyto vzory.  
8. Rozbalte sekci **Obecné**. Na pevné záložce Obecné určete, zda je číselná řada manuální a souvislá nebo nesouvislá. Navíc zadejte nejnižší a nejvyšší čísla, která lze použít v číselné řadě. Nedoporučujeme nesouvislou číselnou řadu změnit na souvislou číselnou řadu. Číselná řada nebude skutečně souvislá. Tato změna může způsobit narušení duplicitního klíče v databáze. Navíc souvislé číselné řady mají větší vliv na výkon.   
9. Klikněte na možnost **Uložit**.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
