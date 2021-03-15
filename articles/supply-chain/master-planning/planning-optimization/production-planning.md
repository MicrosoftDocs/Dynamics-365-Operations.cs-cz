---
title: Plánování výroby
description: Toto téma popisuje plánování výroby a vysvětluje, jak upravit plánované výrobní zakázky pomocí optimalizace plánování.
author: ChristianRytt
manager: tfehr
ms.date: 12/15/2020
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
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: eda22aa6f1e8d665d8ef390f24b247a76d4c2956
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992388"
---
# <a name="production-planning"></a>Plánování výroby

Optimalizace plánování podporuje několik produkčních scénářů. Pokud migrujete ze stávajícího integrovaného hlavního plánovacího modulu, je důležité si uvědomit nějaké změněné chování.

<!-- The following video gives a short introduction to some of the current capabilities. 
KFM: Link to video for production functionality, coming soon... -->

## <a name="planned-production-orders"></a>Plánované výrobní zakázky

Když hlavní plánování vytvoří plánované objednávky pro splnění požadavků, je typ objednávky určen hodnotou pole **Typ plánované objednávky**. Pokud je pole **Plánovaný typ objednávky** nastaveno na *Výroba*, jsou vytvořeny plánované výrobní zakázky. Tyto plánované výrobní zakázky obsahují informace o aktivním kusovníku (BOM) a ID trasy ze souvisejícího výrobního nastavení.

## <a name="requirements-from-boms"></a>Požadavky na kusovníky

Informace o kusovníku se zadávají během hlavního plánování. Výstup plánu zahrnuje dodávku materiálu k pokrytí související materiálové poptávky po výrobě.

Během hlavního plánování se k určení materiálů potřebných pro výrobu použije aktuální aktivní kusovník. Tento krok se provádí na všech úrovních struktury kusovníku, která souvisí s požadovanou výrobní zakázkou. Požadavek na materiál je splněn využitím dostupných zásob na skladě, existujícího dodání na objednávku a schválených plánovaných objednávek. Pokud je kdekoli potřeba další materiál, vytvoří se plánovaná objednávka k pokrytí poptávky.

## <a name="scheduling-during-firming"></a>Plánování během potvrzení

Plánované výrobní zakázky zahrnují ID trasy, které je požadováno pro plánování výroby. Podpora plánování během běhu plánování pro plánované objednávky však čeká na vyřízení. ID trasy se používá k plánování plánovaných výrobních zakázek během zpevňování. Dodací lhůta u plánovaných výrobních zakázek se proto může lišit od dodací lhůty u souvisejících naplánovaných, zpevněných výrobních zakázek, které se z nich generují, jak je popsáno zde:

- **Plánovaná výrobní zakázka** - Dodací lhůta je založena na statické dodací době z uvolněného produktu.
- **Pevná výrobní zakázka** - Dodací lhůta je založena na plánování, které využívá informace o trase a související omezení zdrojů.

Další informace o očekávané dostupnosti funkcí najdete v části [Analýza přizpůsobení optimalizace plánování](planning-optimization-fit-analysis.md).

Pokud jste závislí na produkčních funkcích, které pro optimalizaci plánování ještě nejsou k dispozici, můžete nadále používat integrovaný hlavní plánovací stroj. Není nutná žádná výjimka.

## <a name="delays"></a>Zpoždění

Pokud je dodací lhůta pro požadovaný materiál delší než období mezi dnešním datem a datem požadavku na materiál, plánovaná objednávka požadovaného materiálu a související výrobní zakázka se zpozdí. U plánovaných objednávek se zpoždění (ve dnech) počítá na základě doby realizace vydaného produktu. Informace o zpoždění se poté šíří všemi úrovněmi struktury kusovníku. Proto můžete sledovat dopad zpožděné suroviny až k zákaznické prodejní objednávce.

## <a name="modifying-planned-orders"></a>Změna plánovaných objednávek

Když změníte informace o plánované objednávce, zobrazí se následující zpráva: „Dopad manuálních změn na plánované objednávky se neprojeví ve zbytku plánu až do příštího hlavního plánování.“

Pokud chcete změnit informace o plánované objednávce a zjistit dopad na související požadavky na materiál, postupujte podle těchto kroků.

1. Aktualizujte plánovanou objednávku.
2. Schvalte plánovanou objednávku.
3. Spusťte hlavní plánování.

Při spuštění hlavního plánování byste neměli používat filtry, pokud jsou zahrnuty plánované výrobní zakázky. Více informací naleznete v části [Filtry](#filters) v dále v tomto tématu.

> [!NOTE]
> Pokud se datum dodání plánované objednávky změní na pozdější datum, může být požadavek navázán na novou plánovanou objednávku. K tomuto chování dochází, když nové datum dodávky způsobí zpoždění pro vázanou poptávku, ale podle nastavení doby předstihu lze zpoždění zabránit.

## <a name="explosion-page"></a>Stránka exploze

Stránku **Exploze** můžete použít pro analýzu poptávky, která je požadována pro konkrétní výrobní zakázku nebo plánovanou výrobní zakázku, související pokrytím a informacemi o fixaci. Informace na stránce **Exploze** se během hlavního plánování aktualizuje. Informace nemůžete aktualizovat přímo ze stránky **Exploze**.

## <a name="filters"></a><a name="filters"></a>Filtry

Pro scénáře plánování, které zahrnují produkci, doporučujeme vyhnout se filtrovaným běhům hlavního plánování. Abyste zajistili, že optimalizace plánování obsahuje informace, které jsou požadovány k výpočtu správného výsledku, musíte zahrnout všechny produkty, které mají jakýkoli vztah k produktům, do celé struktury kusovníku plánované objednávky.

I když jsou závislé podřízené položky automaticky detekovány a zahrnuty do hlavních běhů plánování, když je použit integrovaný hlavní plánovací stroj, Optimalizace plánování tuto akci neprovede.

Například pokud se k výrobě produktu B použije také jeden šroub ze struktury kusovníku produktu A, musí být do filtru zahrnuty všechny produkty ve struktuře kusovníku produktů A a B. Protože to může být velmi složité, aby bylo zajištěno, že všechny produkty jsou součástí filtru, doporučujeme, abyste se vyhnuli filtrovaným hlavním plánovacím běhům, když jsou zahrnuty výrobní zakázky.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]