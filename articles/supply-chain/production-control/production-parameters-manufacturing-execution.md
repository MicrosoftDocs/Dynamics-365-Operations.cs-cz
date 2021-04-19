---
title: Parametry výroby v modulu Provádění výroby
description: Toto téma obsahuje informace o nastavení parametrů výroby v modulu Provádění výroby.
author: johanhoffmann
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 30bbcd0365fada4554dc2f7d12b40abc9b22ac63
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814601"
---
# <a name="production-parameters-in-manufacturing-execution"></a>Parametry výroby v modulu Provádění výroby

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace o nastavení parametrů výroby v modulu Provádění výroby.

Modul **Provádění výroby** je určen především pro výrobní společnosti. Lze ho použít k registraci času a spotřeby zboží ve výrobních úlohách nebo projektech. Dříve než začnete používat modul Provádění výroby pro registrace úlohy, musíte nastavit různé parametry výroby, které definují, jak a kdy jsou zaúčtovány registrace během výrobního procesu. Nastavení parametrů výroby ovlivňuje správu skladů, řízení výroby a výpočet nákladů.

Měli byste pečlivě zvážit všechna nastavení na stránce **Parametry výrobní zakázky** předtím, než začnou zaměstnanci provádět registraci výrobních úloh. Klikněte na **Řízení výroby** &gt; **Nastavení** &gt; **Provádění výroby** &gt; **Výchozí hodnoty výrobní zakázky**. Pokud vaše společnost používá funkci více pracovišť, můžete nastavit různé parametry pro výrobní zakázky pro každé pracoviště. Parametry k integraci s modulem **Production** se nastavují na následujících kartách stránky **Parametry výroby**:

- **Obecné** – Obecné nastavení parametrů pro výrobní úlohy v modulu Provádění výroby.
- **Spustit** – parametry používané při zahájení operací výroby.
- **Operace** – parametry používané pro výrobní úlohy nebo operace, a zpětná vazba pro operace během výrobního procesu.
- **Oznámit jako dokončené** – parametry používané při hlášení dokončených položek u poslední operace výrobní zakázky.
- **Ověření množství** – parametry, které se používají k ověřování počátečního množství a množství zpětné vazby pro výrobní zakázky.

## <a name="types-of-production-jobs"></a>Typy výrobních prací
Na kartě **Operace** vyberte , které typy výrobních prací vyžadují registraci na stránce **Registrace práce**.

Obvykle zaměstnanci provádí registrace pro nastavení a procesy. Jestliže používáte plánování práce, můžete vybrat jiné typy prací, například přepravu, které zaměstnanci rovněž musí registrovat při zpracování výrobních zakázek. Můžete například požadovat registrace u přepravních úloh.

> [!IMPORTANT]
> Ujistěte se, zda jsou vybrány všechny důležité typy prací. V opačném případě úlohy nemusí být k dispozici pro registraci na stránce **Registrace práce**. Výběr by měl odpovídat výběru ve sloupci **Správa úloh** na kartě **Nastavení** stránky **Skupiny postupů** (**Řízení výroby** &gt; **Nastavení** &gt; **Postupy** &gt; **Skupiny postupů**).

Pokud je ve skupině postupů vybraná možnost **Správa úlohy**, bude tento typ práce na výrobní zakázce hlášen jako dokončený, když je úloha v modulu Provádění výroby označena jako dokončená. Když jsou všechny typy úloh, pro které je vybrána možnost **Správa práce** ohlášeny jako dokončené v operaci, modul Provádění výroby ohlásí také operaci jako dokončenou.

> [!NOTE]
> U některých typů prací je možné hlášení provést ručně ve výrobních denících. V tomto případě vyberte **Správa práce** pro typ úlohy, ale nevybírejte typ práce k registraci na kartě **Operace** na stránce **Parametry výroby** v modulu Provádění výroby.

## <a name="bom-consumption-and-picking-list-journals"></a>Spotřeba kusovníku a deníky výdejek
Konzistentní nastavení spotřebou kusovníku (BOM) je důležité, protože pomáhá zajistit, že je řízení zásob efektivní. Pokud například nejsou správně nastaveny parametry spotřeby kusovníku v modulu Provádění výroby, mohou být materiály odpočítány ze zásob dvakrát nebo vůbec.

Na stránce **Parametry výroby** je automatická spotřeba kusovníku nastavena ve třech fázích:

- Při zahájení výroby. Nastavte tuto fázi na kartě **Spustit**.
- Během výrobního procesu po dokončení operace. Nastavte tuto fázi na kartě **Operace**.
- Po ohlášení výrobní zakázky jako dokončené. Nastavte tuto fázi na kartě **Vykázat jako dokončené**.

Pro každou fázi můžete v poli **Automatická spotřeba kusovníku** vybrat jednu ze tří metod výběru položek pro výrobní zakázku:

- **Princip vyprazdňování** – tato možnost se používá v kombinaci s možností definované v kusovníku v modulu **Výroba**. Klikněte na **Řízení výroby** &gt; **Společné** &gt; **výrobní zakázky** &gt; **Všechny výrobní zakázky**. Na stránce **Všechny výrobní zakázky** vyberte v seznamu výrobní zakázku a v podokně akcí klikněte na tlačítko **Kusovník**. Na stránce **Kusovník** na kartě **Nastavení** v poli **Princip vyprazdňování** vyberte některou z následujících možností:

  - **Spustit**
  - **Dokončit**
  - **Ruční**
  - Prázdné (žádná možnost není vybrána.)
  - **K dispozici na skladě**

    V modulu Provádění výroby, pokud je vybraný **Princip vyprazdňování** v poli **Automatická spotřeba Kusovníku** na kartě **Spustit**, jsou všechny materiály, které jsou nastaveny na kartě **Spustit** v kusovníku, odečteny ze skladu při zahájení operace. Možnost **K dispozici ve skladovém místě** se používá pro produkty, které jsou povoleny pro pokročilé skladové procesy. Pokud vyberete tento princip vyprazdňování, je materiál vyprázdněn po dokončení skladové práce pro vyskladnění surovin. Materiál je vyprázdněn také v případě, kdy je řádka kusovníku, která používá tento princip vyskladnění, uvolněn do skladu a materiál je dostupný ve vstupním místě výroby.

    > [!NOTE]
    > Pokud je **Princip vyprazdňování** nastaven na kartě **Počáteční** v Provádění výroby, je nutné vybrat stejný princip buď na kartě **Operace** nebo na kartě **Ohlásit jako dokončené**. Tento požadavek umožňuje zajistit, že se odečtou materiály ze zásob u kusovníků, které používají **Dokončit** jako princip vyprazdňování na výrobní zakázce. Pokud není vybraný stejný princip vyprazdňování na kartě **Operace** nebo **Vykázat jako dokončené**, mohou být materiály odpočteny ze zásob dvakrát.

- **Vždy** – Pokud vyberete tuto možnost pro fázi, materiály jsou vždy odečteny ze zásob v této fázi. Například materiály pro výrobu jsou odečteny při zahájení výrobní zakázky. Toto nastavení vyžaduje, aby byla vybraná možnost **Nikdy** na kartě **Operace** a **Vykázat jako dokončené**. Tento požadavek umožňuje zabránit odečtení položky ze skladu dvakrát.
- **Nikdy** – Pokud vyberete tuto možnost pro fázi, neproběhne v této fázi žádná spotřeba Kusovníku. Pokud například vyberete **Nikdy** na všech třech kartách (**Spustit**, **Operace** a **Vykázat jako dokončené**), musí být materiál ručně odečten ze skladu.

> [!IMPORTANT]
> Pečlivě zvažte nastavení parametrů výroby a ujistěte se, že parametry, které jsou vybrány na různých kartách stránky **Parametry výroby** se navzájem nevylučují.

Následující příklady ilustrují nastavení parametrů, které podporuje různé principy spotřeby Kusovníku. Parametry jsou nastaveny na stránce **Parametry výroby** stránky v modulu Provádění výroby.

### <a name="example-1-backflushing-on-operations"></a>Příklad č. 1: zpětný odpočet v operacích

Následující nastavení použijte, pokud deníky výdejek a spotřeba položky kusovníku musejí být generovány při ohlášení dokončených položek na operaci.

| Karta                | Pole                          | Nastavení                             |
|--------------------|--------------------------------|-------------------------------------|
| Spuštění              | Aktualizovat zahájení on-line           | **Stav** nebo **Stav + množství** |
| Spuštění              | Automatická spotřeba kusovníku      | **Nikdy**                           |
| Operations         | Automatická spotřeba kusovníku      | **Vždy**                          |
| Hlášení jako dokončené | Automatická spotřeba kusovníku      | **Nikdy**                           |
| Hlášení jako dokončené | Aktualizovat sestavu o dokončení on-line | **Stav + množství**               |

### <a name="example-2-backflushing-on-production"></a>Příklad č. 2: zpětný odpočet ve výrobě

Následující nastavení použijte, pokud deníky výdejek a spotřebované položky kusovníku musejí být generovány při ohlášení dokončených položek na výrobní zakázce.

| Karta                | Pole                          | Nastavení                             |
|--------------------|--------------------------------|-------------------------------------|
| Spuštění              | Aktualizovat zahájení on-line           | **Stav** nebo **Stav + množství** |
| Spuštění              | Automatická spotřeba kusovníku      | **Nikdy**                           |
| Operations         | Automatická spotřeba kusovníku      | **Nikdy**                           |
| Hlášení jako dokončené | Automatická spotřeba kusovníku      | **Vždy**                          |
| Hlášení jako dokončené | Aktualizovat sestavu o dokončení on-line | **Stav + množství**               |

### <a name="example-3-flushing-principle"></a>Příklad č. 3: Princip vyprazdňování

Následující nastavení použijte, pokud deníky výdejek a spotřebované položky kusovníku musejí být generovány podle nastaveného principu odhlašování položek kusovníku.

| Karta                | Pole                          | Nastavení                |
|--------------------|--------------------------------|------------------------|
| Spuštění              | Aktualizovat zahájení on-line           | **Stav + množství**  |
| Spuštění              | Automatická spotřeba kusovníku      | **Princip vyprazdňování** |
| Operations         | Automatická spotřeba kusovníku      | **Princip vyprazdňování** |
| Hlášení jako dokončené | Automatická spotřeba kusovníku      | **Nikdy**              |
| Hlášení jako dokončené | Aktualizovat sestavu o dokončení on-line | **Stav + množství**  |

### <a name="example-4-deduction-of-materials-during-startup-of-a-production-order"></a>Příklad 4: Odpočet materiálů při spuštění výrobní zakázky

Následující nastavení použijte, pokud deníky výdejek a spotřeba položky kusovníku musejí být generovány při zahájení výroby.

| Karta                | Pole                          | Nastavení                             |
|--------------------|--------------------------------|-------------------------------------|
| Spuštění              | Aktualizovat zahájení on-line           | **Stav + množství**               |
| Spuštění              | Automatická spotřeba kusovníku      | **Vždy**                          |
| Operations         | Automatická spotřeba kusovníku      | **Nikdy**                           |
| Hlášení jako dokončené | Automatická spotřeba kusovníku      | **Nikdy**                           |
| Hlášení jako dokončené | Aktualizovat sestavu o dokončení on-line | **Stav** nebo **Stav + množství** |

Na základě výběrů popsaných výše v této části jsou deníky výdejek zaúčtovány v různých fázích procesu výrobní zakázky:

- Při zahájení operace
- Při hlášení zpětné vazby o množství pro operaci
- Při hlášení dokončených položek výrobní zakázky

### <a name="example-5-manual-bom-consumption"></a>Příklad 5: Ruční spotřeba kusovníku

Když mají být materiály ručně odečteny ze skladu, můžete použít následující nastavení. V takovém případě se nezaúčtují deníky výdejek.


|        Karta         |             Pole              |         Nastavení         |
|--------------------|--------------------------------|-------------------------|
|       Spuštění        |      Aktualizovat zahájení on-line      | <strong>Stav</strong> |
|       Spuštění        |   Automatická spotřeba kusovníku    | <strong>Nikdy</strong>  |
|     Operations     |   Automatická spotřeba kusovníku    | <strong>Nikdy</strong>  |
| Hlášení jako dokončené |   Automatická spotřeba kusovníku    | <strong>Nikdy</strong>  |
| Hlášení jako dokončené | Aktualizovat sestavu o dokončení on-line | <strong>Stav</strong> |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]