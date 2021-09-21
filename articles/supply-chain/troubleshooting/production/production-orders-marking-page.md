---
title: Výrobní zakázky se nezobrazují na stránce Označení
description: Některé výrobní zakázky se nezobrazují na stránce Označení. Toto téma vysvětluje tři konfigurace produktu, které nejsou k dispozici pro značení.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 87507e91d3feb2557e7ba771b8e34ff7ca105749
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475742"
---
# <a name="production-orders-arent-shown-on-the-marking-page"></a>Výrobní zakázky se nezobrazují na stránce Označení

## <a name="symptoms"></a>Příznaky

Při práci s diskrétní výrobou se některé výrobní zakázky nezobrazují na stránce **Označení**.

## <a name="resolution"></a>Řešení

Produkty, které mají následující konfiguraci, nejsou k dispozici pro označení. Proto nebudou zobrazeny na stránce **Označení**:

- Produkty jsou definovány jako produkty typu *skutečná hmotnost*.
- Jsou povoleny pro pokročilé skladové procesy.
- Jsou nakonfigurovány tak, aby byly řízeny zásadou *Standardní cena*.
