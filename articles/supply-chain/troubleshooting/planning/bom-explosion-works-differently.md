---
title: U pevných a odhadovaných výrobních zakázek se rozpad kusovníku chová odlišně
description: Rozpad kusovníku se chová odlišně pro potvrzené výrobní zakázky a pro odhadované výrobní zakázky pro ručně vytvořenou práci
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
ms.openlocfilehash: 94d4b00ea30396923a61b2748cf1aaeedc0af8af
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475793"
---
# <a name="bom-explosion-behaves-differently-for-firmed-and-estimated-production-orders"></a>U pevných a odhadovaných výrobních zakázek se rozpad kusovníku chová odlišně

## <a name="symptoms"></a>Příznaky

Když je výrobní zakázka potvrzena, položky nebudou rozpadnuty, když rozpadnete kusovník (BOM). Když však ručně vytvoříte pracovní příkaz a poté odhadnete výrobní zakázku, položky se rozpadnou.

### <a name="resolution"></a>Řešení

Rozpad, ke kterému dojde, když je výrobní zakázka potvrzena, bude ukazovat na plánovanou zakázku, ale nezdá se, že by v tomto případě byla plánovaná objednávka aktuálně potvrzena. Pokud však byla výrobní zakázka odhadnuta, rozpad se spustí z uvolněné výrobní zakázky, kde neexistuje žádná plánovaná objednávka.
