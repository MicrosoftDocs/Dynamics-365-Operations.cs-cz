---
title: Počet knih na deník
description: Toto téma popisuje vztah mezi deníky a knihami majetku, když vytvoříte návrh na pořízení nebo odpis dlouhodobého majetku prostřednictvím dávkové úlohy. Můžete definovat maximální počet knih, které jsou zahrnuty pro každou akvizici a pro odpisy.
author: moaamer
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e948b4353d0216f1e09019a98319e343bd535861
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822026"
---
# <a name="number-of-books-per-journal"></a>Počet knih na deník

[!include [banner](../includes/banner.md)]

Toto téma popisuje vztah mezi deníky a knihami majetku, když vytvoříte návrh na pořízení nebo odpis dlouhodobého majetku prostřednictvím dávkové úlohy. Můžete definovat maximální počet knih, které jsou zahrnuty pro každou akvizici a pro odpisy pomocí polí v části **Počet knih na deník** na kartě **Obecné** na stránce **Parametry dlouhodobého majetku** (**Dlouhodobý majetek \> Nastavení \> Parametry dlouhodobého majetku**). Tato pole vám umožňují rozdělit počet knih majetku do deníku pořízení a deníku odpisů.

U akvizičního návrhu je výchozí hodnota alespoň 10 000 knih. U návrhu odpisů je výchozí hodnota alespoň 2 000 knih.

Například pokud existuje 4 000 položek dlouhodobého majetku a ke každému majetku jsou přidruženy dvě knihy, jedna kniha bude zaúčtována do aktuální vrstvy a druhá kniha bude zaúčtována do daňové vrstvy. Pokud získáte 4 000 položek dlouhodobého majetku prostřednictvím dávkového zpracování, bude dávková úloha, která vytvoří jeden deník pořízení dlouhodobého majetku, obsahovat 4 000 knih majetku.

> [!NOTE]
> Vytvořený deník se bude používat až do dokončení dávkové úlohy.
>
> Odvozené knihy nejsou zahrnuty do maximálního počtu knih v deníku.

Dávkové zpracování můžete použít ke spuštění odpisů pro stejnou sadu pořízeného majetku. Například dávková úloha vytvoří dva odpisové deníky, z nichž každý obsahuje 2 000 knih majetku. První deník bude obsahovat knihy spojené s dlouhodobým majetkem, které jsou očíslovány od 1 do 2 000. Druhý deník bude pak obsahovat knihy spojené s dlouhodobým majetkem, které jsou očíslovány od 2 001 do 4 000.

Úloha dávkového zpracování vylučuje uzavřené knihy. Například v dávkové úloze pro odpisy je uzavřeno 10 z prvních 2 000 knih. V tomto případě bude první deník obsahovat knihy spojené s dlouhodobým majetkem, které jsou očíslovány od 1 do 2 011. Druhý deník bude pak obsahovat knihy spojené s dlouhodobým majetkem, které jsou očíslovány od 2 012 do 4 000.

> [!NOTE]
> Pokud máte identifikátory dlouhodobého majetku s různými oddělovači (například - nebo /) a vytváříte transakce dlouhodobého majetku v dávkových úlohách, musíte pro každý typ oddělovače spustit samostatnou dávkovou úlohu. Systém nemůže zpracovat různé oddělovače v rámci stejné dávkové úlohy.

Omezení počtu knih se použije, pokud ve stejném deníku neexistují duplicitní ID majetku. Pokud je však ID majetku stejné jako ID knihy, lze počet knih v deníku překročit, aby bylo ID majetku ve stejném deníku.

Například existuje 5 001 ID dlouhodobého majetku, ke každému ID dlouhodobého majetku jsou přidruženy tři knihy a každá kniha majetku je zaúčtována do stejné účtovací vrstvy. Spustíte odpisy po tři po sobě jdoucí měsíce bez shrnutí.  Odpisový deník bude vytvořen pomocí dávkové úlohy a systém vytvoří sedm deníků, které mají 667 ID dlouhodobého majetku a tři knihy pro každé ID dlouhodobého majetku. Výsledkem bude 2 001 knih. Proto za tři měsíce bude existovat 6 003 řádků deníku, které udržují stejná ID majetku ve stejném deníku. Systém také vytvoří jeden deník, který má 332 ID dlouhodobého majetku a tři knihy pro každé ID dlouhodobého majetku. Za tři měsíce to bude 2 988 řádků.

> [!NOTE] 
> Pokud je zapnutý parametr **Shrnout odpisy** když vytváříte návrh odpisování, pak hodnota v poli **Počet knih v deníku - návrh odpisování** nemá žádný účinek. V tomto případě je počet knih v deníku 6000, což je interně definovaný limit.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
