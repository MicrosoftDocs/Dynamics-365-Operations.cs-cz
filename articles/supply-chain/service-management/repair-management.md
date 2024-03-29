---
title: Správa oprav
description: Systematicky seskupujte problémy s cílem usnadnit nalezení návrhů řešení, která byla úspěšná v minulosti.
author: sorenva
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32372a6a54e2adfbf511e2247be4a9baa28b4b53
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015194"
---
# <a name="repair-management"></a>Správa oprav       

[!include [banner](../includes/banner.md)]


Při správě oprav můžete systematicky seskupovat problémy. Cílem je usnadnit nalezení návrhů řešení, která byla úspěšná v minulosti.

Můžete nastavit příznaky, diagnózu a řešení. Všechny můžete později použít v případě, obdržíte obdobné položky k opravě. Můžete také nastavit fáze oprav, které mohou sledovat postup opravy určité položky.

## <a name="setting-up-repair-management"></a>Nastavení správy oprav

Formuláře pro nastavení slouží k zadávání informací, které budou použity k zadání symptomů, diagnózy a rozhodnutí opravy.

- **Správa servisu** \> **Nastavení** \> **Opravy** \> **Podmínky**.
- **Správa servisu** \> **nastavení** \> **opravy** \> **Oblasti příznaků**.
-  **Správa servisu** \> **nastavení** \> **opravy** \> **Oblasti diagnózy**.
- **Správa servisu** \> **nastavení** \> **opravy** \> **Řešení**.
- **Správa servisu** \> **nastavení** \> **opravy** \> **Fáze oprav**.

## <a name="symptoms-and-conditions"></a>Příznaky a podmínky

Příznaky definují, jak odběratel charakterizuje problém. Mezi příznaky patří postřehy odběratele, kterými oznamuje nutnost opravy.

Můžete definovat oblasti symptomů, kódy symptomů a stavy. Oblast symptomů odpovídá oblasti, v níž se projevují příznaky nefunkčnosti, a kód symptomu popisuje symptom nefunkčnosti. Podmínka popisuje stav nebo prostředí, které je k dispozici v případě, že dochází k potížím.

**Příklad**

Počítač je předán do opravy vzhledem k tomu, že po delším používání selhává pevný disk. Chyba pevného disku způsobí chybu modré obrazovky. Technik, který obdrží počítač, zadá následující příznaky a podmínky:

1.  Oblast symptomů je pevný disk

2.  Kód symptomu je chyba modré obrazovky

3.  Podmínkou je, že pevný disk po delším použití selhává

## <a name="diagnosis-and-resolutions"></a>Diagnóza a řešení

Pole diagnózy a řešení obsahují příkazy z hlediska oprav. Jedná se o kroky, které servisní technik provedl při prověřování daného problému.

Oblast diagnózy popisuje operace, které je třeba podniknout s cílem vyřešení problému. Kód diagnózy popisuje postup při zpracování problému a řešením je například oprava či výměna položky nebo zrušení objednávky odběratelem. Pokud je počítač opraven, může být oblastí diagnózy například "vadný díl," kódem opravy může být "nainstalovaná nová videokarta" a řešením bude "výměna".

## <a name="repair-stages"></a>Fáze opravy

Fáze opravy popisují průběh procesu opravy. Fáze opravy obsahuje parametr **Dokončeno**, který udává, že zpracování řádku opravy bylo dokončeno a datum a čas dokončení byl zaznamenán.

## <a name="applying-repair-management"></a>Použití správy oprav

Chcete-li pro určitou položku použít správu oprav, musí být tato položka konfigurována prostřednictvím relace předmětu servisu v servisní zakázce. Ze servisní zakázky můžete poté vytvořit řádek opravy s údaji o aktuálním problému. Na řádku opravy definujete předmět servisu, který je předmětem opravy a také informace o symptomech, diagnóze a zpracování. Pro řádek opravy můžete též vytvořit poznámku.

Řádky oprav lze vytvořit pro všechny kroky v procesu opravy.

## <a name="create-a-repair-line-on-a-service-order"></a>Vytvoření řádku opravy pro servisní zakázku

1.  Přejděte na **Správa servisu** \> **Servisní zakázky** \> **Servisní zakázky**.

2.  Vyberte servisní zakázku s předmětem servisu, který vyžaduje opravu.

3.  Vyberte formulář **Oprava** \> **Řádky opravy** k otevření formuláře **řádky oprav**.

4.  Zvolte **Nový** pro vytvoření nového řádku.

5.  Vyberte předmět servisu. Můžete vybrat libovolný předmět servisu, který byl konfigurován prostřednictvím relace předmětu v servisní zakázce.

6.  Vyberte libovolné přednastavené symptomy, diagnózy či hodnoty zpracování, které jsou relevantní pro daný řádek opravy, a v případě potřeby vyberte **Poznámka** a vytvořte na řádku opravy poznámku.

7.  Kliknutím na tlačítko **Uložit** uložte nový řádek opravy. Pole **Vytvořené datum a čas** na kartě **hlavní** ve formuláři **řádky oprav** se aktualizuje s použitím času uložení.

## <a name="tracking-progress-and-resolving-a-repair-issue"></a>Sledování průběhu a vyřešení opravy problému

Chcete-li sledovat průběh opravy problému, můžete pro řádek opravy definovat fáze opravy.

Po vyřešení problému s opravou můžete řádek opravy zavřít. Nastavte fázi opravy na fázi s aktivovanou vlastností **dokončeno**. Jako čas dokončení zpracování řádku bude zaregistrováno aktuální datum a čas.

## <a name="close-a-repair-line-for-a-resolved-issue"></a>Zavřete řádek opravy pro vyřešený problém

1.  Otevřete formulář **Řádky opravy**. Pomocí postupu popsaného dříve v tomto článku vytvořte řádek opravy.

2.  Vyberte řádek opravy s položkou opravy, kterou chcete uzavřít.

3.  V poli **Fáze opravy** vyberte fázi s aktivovanou vlastností **Dokončeno**.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]