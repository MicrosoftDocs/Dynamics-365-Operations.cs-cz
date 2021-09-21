---
title: Hlavní plánování plánuje větší množství, než je dostupná kapacita
description: Nezdá se, že by hlavní plánování respektovalo omezení kapacity a plánuje více, než je dostupná kapacita
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 48b3d179bb923ff6f6cc5b6be291408b3eb34d98
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475810"
---
# <a name="master-planning-is-scheduling-more-than-the-available-capacity"></a>Hlavní plánování plánuje větší množství, než je dostupná kapacita

## <a name="symptoms"></a>Příznaky

Nezdá se, že by hlavní plánování respektovalo omezení kapacity a plánuje více, než je dostupná kapacita.

Když používáte plánování operací, kde je konečná kapacita a kde postup určuje kombinaci požadavků jak pro skupinu zdrojů, tak pro jednotlivé zdroje, existuje malá šance na nadměrnou rezervaci kvůli způsobu, jakým algoritmus ověřuje konflikty kapacity. K této nadměrné rezervaci může dojít, když ke spuštění hlavního plánování použijete pomocníky. S největší pravděpodobností k tomu dojde, pokud existuje mnoho úloh, které mají relativně krátkou dobu běhu.

## <a name="resolution"></a>Řešení

Pokud je pro plánování operací zásadní, aby nedocházelo k nadměrné rezervaci, můžete naplánovanou část hlavního plánování nastavit na jedno vlákno zapnutím možnosti **Přesná konečná kapacita pro plánování operací** na stránce **Parametry hlavního plánování**. Tato možnost není k dispozici ve výchozím nastavení. Musíte ji ručně přidat na stránku pomocí funkcí přizpůsobení. Když použijete tuto možnost, bude plánování probíhat pomaleji z důvodu nedostatku paralelního zpracování.
