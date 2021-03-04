---
title: Řešení potíží s hlavním plánováním
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s hlavním plánováním.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
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
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1492854b7d2da480942800e378be9d2bb60bb1f
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645058"
---
# <a name="troubleshoot-master-planning"></a>Řešení potíží s hlavním plánováním

Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s hlavním plánováním.

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a>Rozpad kusovníku se chová odlišně pro potvrzené výrobní zakázky a pro odhadované výrobní zakázky pro ručně vytvořenou práci.

### <a name="issue-description"></a>Popis problému

Když je výrobní zakázka potvrzena, položky nebudou rozpadnuty, když rozpadnete kusovník (BOM). Když však ručně vytvoříte pracovní příkaz a poté odhadnete výrobní zakázku, položky se rozpadnou.

### <a name="issue-resolution"></a>Řešení problému

Systém funguje podle očekávání. Rozpad, ke kterému dojde, když je výrobní zakázka potvrzena, bude ukazovat na plánovanou zakázku, ale nezdá se, že by v tomto případě byla plánovaná objednávka aktuálně potvrzena. Pokud však byla výrobní zakázka odhadnuta, rozpad se spustí z uvolněné výrobní zakázky, kde neexistuje žádná plánovaná objednávka.

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a>Hodnota zpoždění se neaktualizuje, když přeplánuji plánovanou objednávku.

Chcete-li aktualizovat zpoždění u plánovaných zakázek, otevřete dialogové okno **Přeplánování** pro plánovanou objednávku. Na záložce s náhledem **Rozpad** se ujistěte, že je možnost **Provést rozpad po přeplánování** nastavená na *Ano*.

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a>Plánování výroby nezohledňuje bezpečnostní rezervy, které jsou nastaveny na pokrytí položky pro doloženou dodávku.

### <a name="issue-description"></a>Popis problému

Hlavní plánování zohledňuje bezpečnostní rezervy. Při plánování plánovaných výrobních zakázek jsou však bezpečnostní rezervy ignorovány.

### <a name="issue-resolution"></a>Řešení problému

Rezervy se berou v úvahu pouze během hlavního plánování, nikoli během manuálního plánování. Rezervy jsou navrženy tak, aby fungovaly jako nárazník během fáze plánování a aby poskytly určitou „rezervu“ pro skutečný proces.

Chcete-li dosáhnout požadovaného výsledku, můžete odstranit rezervu. Postup musí být poté aktualizován tak, aby obsahoval požadovaný čas (například jako čas fronty). Hlavní plánování i manuální plánování by pak mělo přinést stejný výsledek.

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a>Plánované objednávky se generují, i když máme položky na skladě a výrobní zakázky pro ně již existují.

Tento problém můžete vyřešit zvýšením hodnoty **Pozitivní dny** pro příslušné skupiny na stránce **Skupina pokrytí**. Tato změna způsobí, že systém určí, zda lze pro poptávku použít zásoby na skladě. Pak nebude vygenerována nová plánovaná objednávka pro položky, které jsou na skladě.

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a>Nezdá se, že by hlavní plánování respektovalo omezení kapacity a plánuje více, než je dostupná kapacita.

### <a name="issue-description"></a>Popis problému

Když používáte plánování operací, kde je konečná kapacita a kde postup určuje kombinaci požadavků jak pro skupinu zdrojů, tak pro jednotlivé zdroje, existuje malá šance na nadměrnou rezervaci kvůli způsobu, jakým algoritmus ověřuje konflikty kapacity. K této nadměrné rezervaci může dojít, když ke spuštění hlavního plánování použijete pomocníky. S největší pravděpodobností k tomu dojde, pokud existuje mnoho úloh, které mají relativně krátkou dobu běhu.

### <a name="issue-resolution"></a>Řešení problému

Pokud je pro plánování operací zásadní, aby nedocházelo k nadměrné rezervaci, můžete naplánovanou část hlavního plánování nastavit na jedno vlákno zapnutím možnosti **Přesná konečná kapacita pro plánování operací** na stránce **Parametry hlavního plánování**. Tato možnost není k dispozici ve výchozím nastavení. Musíte ji ručně přidat na stránku pomocí funkcí přizpůsobení. Když použijete tuto možnost, bude plánování probíhat pomaleji z důvodu nedostatku paralelního zpracování.

## <a name="planned-orders-take-a-long-time-to-update"></a>Aktualizace plánovaných objednávek trvá dlouho.

### <a name="issue-description"></a>Popis problému

Při aktualizaci požadovaného množství anebo data dodání u plánované objednávky uložení aktualizace obvykle trvá alespoň 30 sekund na objednávku.

### <a name="issue-resolution"></a>Řešení problému

Toto je známý problém s integrovaným modulem hlavního plánování. Je to způsobeno podkladovým automatickým rozpadem skrz strukturu kusovníku během úprav. Tomuto problému se věnuje optimalizace plánování, kde plánovač může aktualizovat a schválit příslušné objednávky a v případě potřeby spustit plánovací běh k aktualizaci plánovaných objednávek pro podkladovou strukturu kusovníku.

Jedním ze způsobů, jak zlepšit výkon pomocí integrovaného modulu hlavního plánování, je provést následující:

1. Přejděte na **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**.
1. Vyberte plán.
1. Rozbalte záložku s náhledem **Ochranné doby ve dnech**.
1. Nastavte **Rozpad** na *Ano* a nastavte pole pod tímto nastavením na 0 (nula).

> [!NOTE]
> Tím se omezí doba rozpadů provedených pro tento hlavní plán na jeden den.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]