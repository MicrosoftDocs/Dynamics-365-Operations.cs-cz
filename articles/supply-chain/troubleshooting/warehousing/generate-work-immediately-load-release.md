---
title: Generování práce vyzvedávání okamžitě po uvolnění odchozího vytížení
description: Pokud musí být práce generována okamžitě po uvolnění nákladu, musíte odpovídajícím způsobem nakonfigurovat šablonu vln. Tato stránka vás provede jednotlivými kroky.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fdeb0b27f4d2c1a2cc9f8e0c4ba537cdce604bd2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475814"
---
# <a name="picking-work-isnt-generated-immediately-when-outbound-load-is-released"></a>Práce vyzvedávání se nevygeneruje okamžitě po uvolnění odchozího vytížení

## <a name="symptoms"></a>Příznaky

Odchozí zatížení vytvoříte pomocí prodejní nebo převodní objednávky a uvolníte náklad do skladu. Všimnete si však, že zatím není žádná práce výdeje k vygenerování.

## <a name="resolution"></a>Řešení

Pokud musí být práce generována okamžitě po uvolnění nákladu, musíte odpovídajícím způsobem nakonfigurovat šablonu vln. Na šabloně vlny nastavte následující možnosti na *Ano*:

- Automatizovat vytvoření vlny
- Zpracovat vlnu při uvolnění do skladu
- Automatizovat uvolnění vlny
