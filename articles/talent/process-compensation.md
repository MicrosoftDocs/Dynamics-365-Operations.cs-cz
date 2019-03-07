---
title: Proces kompenzace
description: Zpracování kompenzace umožňuje vypočítat částky nové základní kompenzace pro zaměstnance na základě úpravy jmění, cílů zvýšení zásluh a výkonnosti.
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 3ecadaf20ea82cd1328b266907d2ba43515d76c6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "303598"
---
# <a name="process-compensation"></a>Proces kompenzace

[!include [banner](includes/banner.md)]

Zpracování kompenzace umožňuje vypočítat částky nové základní kompenzace pro zaměstnance na základě úpravy jmění, cílů zvýšení zásluh a výkonnosti. Teoto téma se věnuje základnímu zpracování toku kompenzace pro plány fixní kompenzace bez faktoringu ve výkonu zaměstnance.

## <a name="plan-the-new-compensation-amounts-and-budgets"></a>Naplánování nových částek kompenzace a rozpočtů
Abyste zaměstnancům mohli zvýšit nastavení zásluh, je nutné nastavit pevný přírůstkový rozpočet pro každé oddělení: Správa kompenzací > Odkazy > Zvýšení cílů zásluh. (Případně můžete otevřít tento formulář prostřednictvím voleb Oddělení: organizace > oddělení). Zde můžete dále specifikovat, zda zaměstnanci v určitém odboru nebo skladovém místě mají získat jiné procentuální zvýšení. Pole **Rozpočet** a **Měna** mají informativní charakter a umožňují zaznamenat peněžní částku rozpočtu.

## <a name="set-up-the-compensation-process"></a>Nastavení procesu kompenzace
Procesní událost slouží k určení parametrů pro zpracování kompenzace. Patří sem období vyhodnocení k určení částek kompenzace a data, kdy by měly nové částky kompenzace vstoupit v platnost.

Případně můžete zahrnout fixní poměrně rozdělené datum náboru, pokud některý z vašich fixních plánů kompenzace používá pravidlo zařazení podle procent. Pro tyto plány platí, že kdokoli, kdo byl přijat po datu zahájení cyklu a před poměrným rozložením fixní mzdy po datu zařazení, obdrží 100 % svých vypočtených zásluh nebo obecné zvýšení. Každý uživatel, který byl přijat po datu poměrného rozložení pevné mzdy a před koncovým datem cyklu, obdrží část vypočítaného zvýšení na základě počtu dní z celkového počtu dnů cyklu, po které byli zaměstnáni. Například pokud náš cyklus běží od 1. ledna do 31. prosince a máme k dispozici datum poměrného rozložení pevné mzdy 1. dubna, zaměstnanec, který je přijat v březnu, obdrží úplné vypočítané zvýšení, zatímco zaměstnanec přijatý 1. července obdrží přibližně polovinu vypočteného navýšení.

Datum procesní události **Bod v čase** se používá pouze pro zpracování určitých variabilních plánů kompenzace, nebudou v tomto blogovém příspěvku uvedena. **Konečný termín kontroly** je konečný termín provedení všech doporučení tak, aby nové částky kompenzace mohly být načteny do záznamu zaměstnance. Datum revize je pouze informativní.

Po uložení parametrů procesní události můžete klepnutím na tlačítko **Nastavení** označit spuštění plánů, které mají být zahrnuty do daného procesu a které fixní kompenzace akce mají být provedeny pro jednotlivé plány.

Klepněte na tlačítko **Přidat** na kartě **Plány** pro přidání plánu kompenzace do procesní události. Sloupce **Použít jiný účinek**, **Koeficient účinku** a **Popis účinku** slouží pouze pro variabilní plány kompenzace a nejsou uvedené v tomto tématu.

Uložte záznam a klepněte na tlačítko **Přidat** na kartě **Akce** pro přidání akcí fixní kompenzace pro vybraný plán. Použijte volbu **Povolit doporučení**, pokud chcete zadat jiné množství než vypočtené zvýšení směrnice pro akci. Pokud chcete vypočítat akci, která je založena na výsledku předchozí akce, která má propojit více akcí kompenzace, označte možnost **Použít předchozí výsledek**, akce fixní kompenzace jsou typy kompenzační logiky, které můžete přidělit popisné názvy. Pro plány Platová třída a Pásmo můžete přidat pouze akce fixní kompenzace následujících typů:

| Typ fixní kompenzace | Funkce                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jmění                        | Akce jmění porovnají mzdovou sazbu zaměstnance mezd ke koncovému datu cyklu s nejnižším referenčním bodem pro úroveň určenou v úloze zaměstnance. Pokud je mzdová sazba zaměstnance menší než minimální referenční bod, bude vypočítáno zvýšení potřebné k získání zaměstnance na minimální bod v rozsahu.                                                                                |
| Zásluha                         | Akce zásluh vypočítá zvýšení založen na mzdové sazbě zaměstnance ke koncovému datu cyklu a procento zvýšení uvedené v rozpočtu fixního navýšení pro oddělení, odbor a umístění zaměstnance.                                                                                                                                                                                         |
| Obecné                       | Hlavní akce vypočítají navýšení na základě procenta nebo přidělí zaměstnanci paušální částku. To závisí na nastavení **fixní kompenzace** na kartě **Obecné**.                                                                                                                                                                                                                        |
| Povýšení                     | Propagační akce obsahují pojmenované místo, kde můžete zadat zvýšení, proto je nutné vybrat volbu **Povolit doporučení** abyste mohli zadat doporučení pro zaměstnance, kteří obdrží promoakce.  Zaměstnanci bez doporučeného zvýšení nebudou mít **promoakce** přidané ke svým záznamům fixních kompenzací.                                                                       |
| Změna jiné úrovně            | V předcházejícím příkladu označuje pojem **snížení** název akce **fixní kompenzace** typu **Změna na jinou úroveň**. Tím se vygeneruje nárůst 0 (nulová změna) zvýšení, takže lze zadat doporučenou částku pro účely úpravy mzdové sazby zaměstnance. (Je třeba označit možnost **povolit doporučení**.) Zaměstnanci bez doporučení nemají tuto akci přidanou ve svých záznamech fixní kompenzace. |

Do plánu Krok je možné přidat pouze akce **Fixní kompenzace** typu Krok.

| Typ akce fixní kompenzace | Funkce                                                                                                                                                                                           |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Krok                           | Na této kartě určete, zda má tato akce kroku převést zaměstnance dopředu o 0 kroků, 1 krok nebo dva kroky.                                                                                  |
|                                | **0 kroků** – zaměstnanec obdrží dojde mzdovou sazbu pro aktuální krok, na kterém jsou.                                                                                                                      |
|                                | **1 krok** – systém nejprve zkontroluje, zda zaměstnanec již je na posledním referenční bodě pro svou úroveň.                                                                                             |
|                                | **2 kroky** -systém přesune zaměstnance o dva kroky na jejich aktuální úrovni. Systém může přesouvat zaměstnance pouze o jeden nebo nula kroků, pokud dosáhnou posledního referenčního bodu pro svou úroveň. |

## <a name="run-the-compensation-process"></a>Spustit proces kompenzace
Po nastavení procesní události s nezbytnými datovými poli, plány a akcemi můžete klepnout na **Spustit proces** na stránce **Událost procesu**. Tím se otevře dialogové okno **Spustit události procesu kompenzace**. V rámci tohoto dialogového okna můžete klepnout na možnost **Zobrazit výsledky zpracování** a podívat se, jak velké částky kompenzace byly vypočteny pro jednotlivé zaměstnance. Klepnutím na tlačítko **OK** se spustí proces kompenzace pro všechny zaměstnance, kteří jsou ve vybraných plánech kompenzací ke koncovému datu.

## <a name="view-the-process-results"></a>Zobrazení výsledků procesu
Chcete-li zobrazit výsledky procesu, otevřete stránku **výsledky procesu**. Při každém spuštění procesní události se vytvoří událost kompenzace. Tímto způsobem proveďte zkušební spuštění, proveďte úpravy a spusťte události kompenzace několikrát, abyste viděli dopad různých změn na kompenzace zaměstnance.

Na stránce **Výsledky procesu** jsou uvedeny informace o běhu procesu včetně toho, kdy k němu došlo, který uživatel spustil proces a zda při spuštění procesu nedošlo k chybám. Můžete také označit volbu **uzamčeno** pro zakázání tlačítka **Načíst kompenzaci** a zabránění jakémukoli uživateli načítat události kompenzace do záznamů zaměstnance. Kliknutím na tlačítko **Výsledky zaměstnanců** zobrazíte seznam zaměstnanců zahrnutých v spuštění.

Možnost **Výsledky zaměstnance** zobrazuje informace o procesu jako takovém a jakékoli akce kompenzace prováděné v procesu. Oddíl **Fixní kompenzace** bude obsahovat záznam pro každou akci, zahrnutou do události procesu pro plán kompenzace. Sloupce **Aktuální pokyny** a **Doporučení** budou zobrazovat více informací pro akci vybranou v oddílu **Fixní kompenzace**. Pokud byla pro akci označena možnost **Povolit doporučení**, budou pole Doporučení upravitelná. To umožňuje ručně upravit částky podle zaměstnance. Pokud byla označena možnost **Použít předchozí výsledek** pro akci v procesní události, je nutné ručně aktualizovat částky pro všechny závislé akce.

Po zkontrolování částek kompenzace pro zaměstnance a provedení úprav doporučených hodnot můžete změnit **stav** na řádku **událost zaměstnance** a označit tak, zda byla událost schválena nebo by měla být ignorována. V případě potřeby můžete vymazat jakékoli změny provedené na doporučení zaměstnance klepnutím na tlačítko **přepočítat**. Tím se existující událost zaměstnance označí stavem Ignorovat a vytvoří nová událost zaměstnance s přepočítanými hodnotami.

## <a name="loading-approved-compensation-changes"></a>Načítání schválených změn kompenzace
Jakmile má jedna nebo více událostí zaměstnance aktualizován stav na Schváleno, mohou být události nahrány do záznamů fixní kompenzace zaměstnance. To lze provést postupným výběrem jednotlivých událostí zaměstnance a klepnutím na tlačítko **Nahrát kompenzaci zaměstnance** na stránce **Výsledky zaměstnance** nebo klepnutím na tlačítko **Načíst kompenzaci** na stránce **Výsledky procesu** k načtení stránky všech schválených událostí zaměstnance najednou.

Klepnutím na tlačítko **OK** v dialogovém okně **Načíst kompenzaci** přidáte řádky akce kompenzace na stránku **Fixní kompenzace zaměstnance**.
