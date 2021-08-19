---
title: Nastavení zásad proplachování na řádcích kusovníku není respektováno
description: Nastavení zásad proplachování na řádcích kusovníků není respektováno.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ee40eff53efd920ebe43a7b2dd28129f01e6ebb5e75bd480a91f758529f77fc5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716949"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a>Nastavení zásad proplachování na řádcích kusovníku není respektováno

Číslo článku znalostní báze: 4612725

## <a name="symptoms"></a>Příznaky

K tomuto problému dochází, když je pole **Automatická spotřeba kusovníku** na kartě **Automatická aktualizace** stránky **Parametry řízení výroby** nastaveno na *Princip vyprazdňování*. Toto nastavení označuje, že všechny řádky kusovníku (BOM) by měly být automaticky spotřebovány, když je přijata nákupní objednávka. Pokud je pole **Princip vyprazdňování** na řádcích kusovníku výslovně nastaveno na *Ruční*, můžete očekávat, že řádky kusovníku nebudou automaticky spotřebovány. Když však nastane tento problém, řádky kusovníku, kde je pole **Princip vyprazdňování** nastaveno na *Ruční* jsou přesto automaticky spotřebovány.

## <a name="resolution"></a>Rozlišení

Pokud dochází k tomuto problému, mohou být nastaveny parametry řízení výroby tak, aby přepsaly nastavení **Princip vyprazdňování** na řádcích kusovníku. Na stránce **Parametry řízení výroby** na kartě **Automatická aktualizace** zkontrolujte hodnotu pole **Automatická spotřeba kusovníku**. Pokud je nastavena na *Vždy*, bude systém ignorovat nastavení **Princip vyprazdňování** na všech řádcích kusovníku a vždy tyto řádky vyprázdní. Aby systém respektoval nastavení **Princip vyprazdňování** na řádcích kusovníku, změňte hodnotu **Automatická spotřeba kusovníku** na *Princip vyprazdňování*.
