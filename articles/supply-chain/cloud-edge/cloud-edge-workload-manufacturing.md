---
title: Pracovní zátěže spuštění výroby pro cloudové a hraniční jednotky škálování
description: Toto téma popisuje, jak pracovní zátěže spuštění výroby fungují s cloudovými a hraničními jednotkami škálování.
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 799c479c750fcaf296f3e2787fa38416af51963c
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516746"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a>Pracovní zátěže spuštění výroby pro cloudové a hraniční jednotky škálování

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Některé obchodní funkce nejsou ve veřejném náhledu plně podporovány, když se používají jednotky škálování pracovní zátěže.

Při provádění výroby poskytují cloudové a okrajové jednotky škálování následující funkce, i když hraniční jednotky nejsou připojeny k centru:

- Obsluha strojů a vedoucí výroby mají přístup k operačnímu výrobnímu plánu.
- Operátoři strojů mohou udržovat aktuální plán spuštěním samostatných a procesních výrobních úloh.
- Vedoucí dílny může upravit operační plán.
- Pracovníci mají přístup k času a docházce pro označení příchodu a odchodu v hraničním pásmu, aby zajistili správný výpočet platu pracovníka.

Toto téma popisuje, jak pracovní zátěže spuštění výroby fungují s cloudovými a hraničními jednotkami škálování.

## <a name="the-manufacturing-lifecycle"></a>Životní cyklus výroby

Jak ukazuje následující obrázek, životní cyklus výroby je rozdělen do tří fází: *Plánování*, *Provedení* a *Dokončení*.

[![Fáze provedení výroby při použití jediného prostředí](media/mes-phases.png "Fáze provedení výroby při použití jediného prostředí")](media/mes-phases-large.png)

Fáze _Plánování_ zahrnuje definici produktu, plánování, vytváření a plánování objednávek a vydání. Krok uvolnění označuje přechod z fáze _Plánování_ do fáze _Provedení_. Po uvolnění výrobní zakázky budou úlohy výrobní zakázky viditelné na produkční ploše a připraveny k provedení.

Když je úloha produkce označena jako dokončená, přesune se z fáze _Provedení_ do fáze _Dokončení_. Ve fázi _Dokončení_ projdou registrace z fáze *Provedení* schvalovacím pracovním procesem, kde jsou vypočítány, schváleny a přeneseny. V tomto okamžiku je výrobní zakázka dokončena. Tím je generován základ pro plat pracovníka.

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a>Rozdělení fáze Provedení na samostatnou úlohu

Jak ukazuje následující obrázek, při použití jednotek měřítka je fáze _Provedení_ rozdělena jako samostatná úloha.

[![Fáze provedení výroby při použití jednotek škálování](media/mes-phases-workloads.png "Fáze provedení výroby při použití jednotek škálování")](media/mes-phases-workloads-large.png)

Model nyní přechází z instalace s jednou instancí na model, který je založen na jednotkách centra a škálování. Fáze _Plánování_ a _Dokončení_ běží jako operace back-office v centru a pracovní zátěž provedení výroby probíhá na jednotkách škálování. Data se přenášejí asynchronně mezi centrem a jednotkami měřítka.

Když je v centru uvolněna výrobní zakázka, všechna data potřebná ke zpracování produkčních úloh se přenesou do jednotky škálování. Tato data zahrnují výrobní zakázky, výrobní trasy, kusovníky a produkty. Data, která nesouvisí s výrobní zakázkou (například nepřímé aktivity, kódy nepřítomnosti a parametry výroby), se také přenesou z centra do jednotky škálování. Data, která pocházejí z centra a která se přenášejí do jednotky škálování, lze zpravidla vytvářet nebo aktualizovat pouze v centru. Například na stupnici nelze vytvořit nový kód absence nebo nepřímou aktivitu&mdash;lze je použít pouze pro registraci. Registrace provedené na jednotce škálování během provádění se poté přenesou do centra, kde se zpracovávají schválení času a docházky, inventář a finanční aktualizace.

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a>Výroba prováděcích úloh, které lze spouštět na úlohách

Následující úlohy provádění výroby lze aktuálně spouštět na úlohách, když se používají jednotky škálování:

- Píchnutí příchodu, přihlášení, odpíchnutí příchodu a nepřítomnost
- Zahájit práci
- Seskupení úloh
- Průběh sestavy
- Vykázat odpad
- Nepřímá aktivita
- Přerušení

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a>Práce s výrobními úlohami spuštění v centru

Obvykle se procesy, které jsou vyžadovány ke spouštění pracovních úloh spuštění výroby, spouštějí automaticky, aby se podle potřeby synchronizovalo centrum a všechny jednotky škálování. Pokud však máte potíže, můžete ručně spustit zpracování nezpracovaných registrací, které jsou přijímány z úloh, nebo zkontrolovat protokol zpracování registrace.

### <a name="manually-process-raw-registrations"></a>Ruční zpracování nezpracovaných registrací

Dávková úloha v Supply Chain Management se spouští automaticky a zpracovává všechny registrace, které byly přijaty z úloh. Tato úloha vytvoří požadované produkční deníky a položky deníku při zpracování registrace dokončené úlohy na úloze.

I když se úloha obvykle spouští automaticky, můžete ji kdykoli spustit ručně po přihlášení do centra a přejít na **Kontrola výroby \> Pravidelné úkoly \> Správa zátěže backoffice \> Zpracovat nezpracované registrace**.

### <a name="check-the-raw-registration-processing-log"></a>Kontrola nezpracovaného protokolu zpracování registrace

Chcete-li zkontrolovat protokol zpracování registrace, přihlaste se do centra a přejděte na **Kontrola výroby \> Pravidelné úkoly \> Správa zátěže backoffice \> Nezpracovaný protokol zpracování registrace**. Stránka **Protokol zpracování nezpracované registrace** zobrazuje seznam zpracovaných nezpracovaných registrací a stav každé registrace.

![Kontrola stránky protokolu nezpracované registrace](media/mes-processing-log.png "Kontrola stránky protokolu nezpracované registrace")

Na jakékoli registraci v seznamu můžete pracovat tak, že ji vyberete a poté vyberete jedno z následujících tlačítek v podokně akcí:

- **Proces** - Ruční zpracování vybrané registrace. Tato akce může být užitečná, pokud úloha _Zpracovat nezpracované registrace_ neproběhla nebo selhala.
- **Zrušit** - Zruší vybranou registraci.

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a>Práce s výrobními úlohami spuštění na jednotce škálování

Obvykle se procesy, které jsou vyžadovány ke spouštění pracovních úloh spuštění výroby, spouštějí automaticky, aby se podle potřeby synchronizovalo centrum a všechny jednotky škálování. Pokud však máte potíže, můžete zkontrolovat historii objednávek, které byly zpracovány v jednotce škálování, nebo ručně spustit úlohu _Výrobní centrum procesoru zpráv jednotky škálování_.

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a>Zobrazte historii výrobních úloh, které byly zpracovány na jednotce škálování

Chcete-li zkontrolovat historii výrobních úloh, které byly zpracovány na jednotce škálování, přihlaste se do stroje jednotky škálování a přejděte na **Kontrola výroby \> Pravidelné úkoly \> Správa úloh backoffice \> Historie zpracování výrobních úloh**. Stránka **Historie zpracování výrobních úloh** zobrazuje historii zpracování výrobních zakázek na jednotce škálování. Na každé výrobní zakázce v seznamu můžete pracovat tak, že ji vyberete a poté vyberete jedno z následujících tlačítek v podokně akcí:

- **Proces** - Ruční zpracování vybrané výrobní zakázky.
- **Zrušit** - Zrušte vybranou výrobní zakázku.

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a>Výrobní centrum pro úlohu procesoru zprávy jednotky škálování

Úloha _Výrobní centrum pro procesor zpráv jednotky škálování_ zpracovává data z centra do jednotky škálování. Tato úloha se automaticky spustí, když je nasazena úloha provedení. Můžete jej však kdykoli spustit ručně tak, že přejdete na **Kontrola výroby \> Pravidelné úkoly \> Správa úlohy backoffice \> Výrobní centrum pro škálování procesorů zpráv jednotky**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]