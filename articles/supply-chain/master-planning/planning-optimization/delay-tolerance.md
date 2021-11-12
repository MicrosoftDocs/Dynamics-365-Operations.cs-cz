---
title: Tolerance zpoždění (záporné dny)
description: Toto téma poskytuje informace o výpočtu tolerance zpoždění a o tom, jak ovlivňuje plánované vytváření objednávek v Optimalizaci plánování.
author: ChristianRytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: ccf827983694eab2037c73aa3251846b051e66f1
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678560"
---
# <a name="delay-tolerance-negative-days"></a>Tolerance zpoždění (záporné dny)

[!include [banner](../../includes/banner.md)]

Funkce tolerance zpoždění umožňuje Optimalizaci plánování zohlednit hodnotu **Negativní dny**, která je nastavena pro skupiny pokrytí. Používá se k prodloužení doby tolerance zpoždění, která se použije během hlavního plánování. Tímto způsobem se můžete vyhnout vytváření nových objednávek dodávek, pokud stávající nabídka bude schopna pokrýt poptávku po krátké prodlevě. Účelem této funkce je určit, zda má smysl vytvořit novou objednávku dodávky pro danou poptávku.

## <a name="turn-on-the-feature-in-your-system"></a>Zapnutí funkce ve vašem systému

Chcete-li funkci tolerance zpoždění ve svém systému zpřístupnit, přejděte na [Správu funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte funkci *Záporné dny pro optimalizaci plánování*.

## <a name="delay-tolerance-in-planning-optimization"></a>Tolerance zpoždění v Optimalizaci plánování

Tolerance zpoždění představuje počet dní po dodací lhůtě, kterou jste ochotni počkat, než si objednáte nové doplnění, když je již plánovaná stávající dodávka. Tolerance zpoždění je definována pomocí kalendářních dnů, nikoli pracovních dnů.

Když systém v době hlavního plánování vypočítá toleranci zpoždění, vezme v úvahu nastavení **Záporné dny**. Hodnotu **Záporné dny** lze zadat na stránce **Skupiny disponibility** nebo **Disponibilita položky**.

Systém spojuje výpočet tolerance zpoždění s *nejbližším datem doplnění*, což se rovná dnešnímu datu plus dodací lhůta. Tolerance zpoždění se vypočítá pomocí následujícího vzorce, kde *max()* najde větší ze dvou hodnot:

*max(nejbližší datum doplnění, termín splnění doplnění)* – *termín splnění doplnění* + *záporné dny*

Tento vzorec zajišťuje, že hlavní plánování nevytváří nové objednávky dodávek, pokud existuje dostatečná zásoba během doby realizace produktu.

> [!NOTE]
> Výpočet tolerance zpoždění v Optimalizaci plánování vždy používá výpočet dynamických záporných dnů z integrovaného hlavního plánování. Nastavení **Použít dynamické záporné dny** na stránce **Parametry hlavního plánování** nemá na toto chování žádný vliv.

Pokud stávající nabídka implikuje zpoždění poptávky, které je menší nebo rovné vypočítané toleranci zpoždění, Optimalizace plánování spojí stávající nabídku s poptávkou. V některých případech je lepší odložit poptávku, než skončit s nadměrnou dodávkou.

Následující podsekce poskytují příklady, které ukazují, jak tolerance zpoždění ovlivňuje vytváření plánovaných objednávek v Optimalizaci plánování.

### <a name="example-1"></a>Příklad 1

Produkt má následující konfiguraci:

- **Doba realizace:** *10*
- **Záporné dny:** *2*

Po produktu existuje následující nabídka a poptávka:

- **Poptávka pro dnešek:** Prodejní objednávka na množství 10
- **Dodávka za 12 dnů:** Nákupní objednávka na množství 10

Stávající nabídka může pokrýt poptávku do 12 dnů a toto období se rovná toleranci zpoždění. Proto při spuštění hlavního plánování nejsou vytvářeny žádné plánované objednávky.

### <a name="example-2"></a>Příklad 2

Produkt má následující konfiguraci:

- **Doba realizace:** *10*
- **Záporné dny:** *0*

Po produktu existuje následující nabídka a poptávka:

- **Poptávka pro dnešek:** Prodejní objednávka na množství 10
- **Dodávka za 12 dnů:** Nákupní objednávka na množství 10

Stávající nabídka může pokrýt poptávku až po 12 dnech. Tolerance zpoždění je však 10 dní. Při spuštění hlavního plánování se proto vytvoří plánovaná objednávka pro množství 10.

### <a name="example-3"></a>Příklad 3

Produkt má následující konfiguraci:

- **Doba realizace:** *10*
- **Záporné dny:** *2*

Po produktu existuje následující nabídka a poptávka:

- **Poptávka za 11 dnů:** Prodejní objednávka na množství 10
- **Dodávka za 14 dnů:** Nákupní objednávka na množství 10

Stávající nabídka může pokrýt poptávku až po třech dnech. Tolerance zpoždění jsou však 2 dny. (V tomto případě tolerance zpoždění zahrnuje pouze dva záporné dny. Datum poptávky není zahrnuto, protože je po dodací lhůtě produktu.) Proto se při spuštění hlavního plánování vytvoří plánovaná objednávka na množství 10.
