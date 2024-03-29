---
title: Řešení potíží s optimalizací plánování
description: Tento článek popisuje, jak vyřešit problémy, s nimiž se můžete při práci s optimalizací plánování setkat.
author: t-benebo
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 37c38ab9cec8ae3c9d4decf8043b43ea2251083e
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739722"
---
# <a name="troubleshoot-planning-optimization"></a>Řešení potíží s optimalizací plánování 

[!include [banner](../../includes/banner.md)]

Tento článek popisuje, jak vyřešit běžné problémy, s nimiž se můžete při práci s optimalizací plánování setkat.

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a>Instalace doplňku Optimalizace plánování se nedokončuje

Optimalizace plánování vyžaduje povolenou službu Lifecycle Services (LCS), prostředí s vysokou dostupností, vrstvy 2 nebo vyšší (ne prostředí OneBox) s Dynamics 365 Supply Chain Management verze 10.0.7 a novější. Pokud se pokusíte nainstalovat doplněk v prostředí OneBox, instalace nebude dokončena.

**Oprava**: Zrušte instalaci a použijte prostředí s vysokou dostupností, stupeň 2 nebo vyšší (nikoli prostředí OneBox).

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a>Když je povolena optimalizace plánování, plánování dávkových úloh se nezdaří

Pokud povolíte optimalizaci plánování, zastaralý modul hlavního plánování se automaticky deaktivuje. Dávkové úlohy hlavního plánování, které byly vytvořeny pro zastaralý hlavní plánovací modul, selžou, pokud jsou spuštěny při povolené optimalizaci plánování. Může se zobrazit chybová zpráva, například *Tato operace spustila hlavní plánování, které není podporováno, když je povolena optimalizace plánování*.

**Oprava**: Zrušte všechny dávkové úlohy hlavního plánování, které byly vytvořeny pro zastaralý hlavní plánovací modul.

## <a name="planning-optimization-results-are-different-from-earlier-results"></a>Výsledky optimalizace plánování se liší od předchozích výsledků

Optimalizace plánování se v některých oblastech liší od zastaralého modulu hlavního plánování. To může být také způsobeno chystanými funkcemi.

**Oprava**: Spusťte analýzu přizpůsobení optimalizace plánování a poté analyzujte výsledky a porozumění dopadu s odkazem na související dokumentaci. Další informace naleznete v tématu [Analýza shody optimalizace plánování](planning-optimization-fit-analysis.md)

## <a name="cant-enable-planning-optimization"></a>Nelze povolit optimalizaci plánování

**Stav připojení** musí být **Připojeno** před nastavením možnosti **Použít optimalizaci plánování** na **Ano**. Další informace naleznete v tématu [Začínáme s optimalizací plánování](get-started.md)

**Oprava**: Zkontrolujte, zda byl doplněk optimalizace plánování úspěšně nainstalován.

## <a name="error-message-is-shown-during-ctp"></a>Během CTP se zobrazí chybová zpráva

Pokud se pokusíte spustit příslib na základě ověření dostupné kapacity (CTP) z prodejní objednávky, když je aktivována optimalizace plánování, zobrazí se následující chybová zpráva: *Tato operace spustila hlavní plánování, které není podporováno, když je aktivována optimalizace plánování*.

Souvisí to s čekající funkcí, která je plánována jako součást podpory výrobních zakázek.

**Oprava:** Pokud je aktivována optimalizace plánování, vyhněte se výpočtům CTP, dokud nebude dostupná podpora CTP.

## <a name="additional-resources"></a>Další prostředky

- [Začínáme s hlavním plánováním](get-started.md)
- [Analýza přizpůsobení pro optimalizaci plánování](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]