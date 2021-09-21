---
title: Nelze zrušit rezervaci zásob na řádku prodejní objednávky
description: Pokud existuje otevřená práce proti prodejní linii a pokusíte se zrušit rezervaci zásob na řádku, zobrazí se chyba. Dokončete nebo odstraňte práci a uvolněte rezervaci.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1a042065dc4cd637aff58e55cf16179b7022f6ca
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475805"
---
# <a name="cant-unreserve-inventory-on-a-sales-order-line"></a>Nelze zrušit rezervaci zásob na řádku prodejní objednávky

## <a name="symptoms"></a>Příznaky

Pokud existuje otevřená práce proti řádku prodejní objednávky a pokusíte se zrušit rezervaci zásob na tomto řádku, zobrazí se následující chybová zpráva:

> Rezervace nelze odebrat, protože je vytvořena práce, která je na rezervacích závislá.

## <a name="resolution"></a>Řešení

Prozkoumejte, zda existuje práce skupiny balení, která přepravuje položku z balicí stanice na jiné místo (např *Nákladová brána*). Zkontrolujte záznamy na stránkách **Protokol historie vytvoření práce** a **Podrobnosti o práci**, abyste zjistili, co fyzicky rezervuje zásoby, a poté dokončete nebo odstraňte práci, abyste rezervaci uvolnili.
