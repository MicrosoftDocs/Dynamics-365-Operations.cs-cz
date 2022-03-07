---
title: Řešení potíží s optimalizací plánování
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete při práci s optimalizací plánování setkat.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 39583c244f09f54551d560e8b1dd9f1a5a1590cc
ms.sourcegitcommit: 72f70c81176e86cda714a4712525f73514c895b7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/16/2021
ms.locfileid: "5457322"
---
# <a name="troubleshoot-planning-optimization"></a>Řešení potíží s optimalizací plánování 

[!include [banner](../../includes/banner.md)]

Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete při práci s optimalizací plánování setkat.

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a>Instalace doplňku Optimalizace plánování se nedokončuje

Optimalizace plánování vyžaduje povolenou službu Lifecycle Services (LCS), prostředí s vysokou dostupností, vrstvy 2 nebo vyšší (ne prostředí OneBox) s Dynamics 365 Supply Chain Management verze 10.0.7 a novější. Pokud se pokusíte nainstalovat doplněk v prostředí OneBox, instalace nebude dokončena.

**Oprava**: Zrušte instalaci a použijte prostředí s vysokou dostupností, stupeň 2 nebo vyšší (nikoli prostředí OneBox).

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a>Když je povolena optimalizace plánování, plánování dávkových úloh se nezdaří

Pokud povolíte optimalizaci plánování, vestavěný modul hlavního plánování se automaticky deaktivuje. Dávkové úlohy hlavního plánování, které byly vytvořeny pro vestavěný plánovací modul Supply Chain Management, selžou, pokud jsou spuštěny při povolené optimalizaci plánování. Může se zobrazit chybová zpráva, například *Tato operace spustila hlavní plánování, které není podporováno, když je povolena optimalizace plánování*.

**Oprava**: Zrušte všechny dávkové úlohy hlavního plánování, které byly vytvořeny pro vestavěný plánovací modul Supply Chain Management.

## <a name="planning-optimization-results-are-different-from-earlier-results"></a>Výsledky optimalizace plánování se liší od předchozích výsledků

Optimalizace plánování se v některých oblastech liší od vestavěného hlavního plánování. To může být také způsobeno chystanými funkcemi.

**Oprava**: Spusťte analýzu přizpůsobení optimalizace plánování a poté analyzujte výsledky a porozumění dopadu s odkazem na související dokumentaci. Další informace naleznete v tématu [Analýza shody optimalizace plánování](planning-optimization-fit-analysis.md)

## <a name="cant-enable-planning-optimization"></a>Nelze povolit optimalizaci plánování

**Stav připojení** musí být **Připojeno** před nastavením možnosti **Použít optimalizaci plánování** na **Ano**. Další informace naleznete v tématu [Začínáme s optimalizací plánování](get-started.md)

**Oprava**: Zkontrolujte, zda byl doplněk optimalizace plánování úspěšně nainstalován.

## <a name="error-message-is-shown-during-ctp"></a>Během CTP se zobrazí chybová zpráva

Pokud se pokusíte spustit příslib na základě ověření dostupné kapacity (CTP) z prodejní objednávky, když je aktivována optimalizace plánování, zobrazí se následující chybová zpráva: *Tato operace spustila hlavní plánování, které není podporováno, když je aktivována optimalizace plánování*.

Souvisí to s čekající funkcí, která je plánována jako součást podpory výrobních zakázek.

**Oprava:** Pokud je aktivována optimalizace plánování, vyhněte se výpočtům CTP, dokud nebude dostupná podpora CTP.

## <a name="additional-resources"></a>Další prostředky

[Začínáme s optimalizací plánování](get-started.md)

[Analýza přizpůsobení pro optimalizaci plánování](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]