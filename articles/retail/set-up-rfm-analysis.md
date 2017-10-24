---
title: "Nastavení analýzy RFM"
description: "Toto téma vysvětluje, jak nastavit analýzu RFM (Recency, Frequency, and Monetary) odběratelů."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e11ec02d7392601b22e17384a4dbf620b79df035
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-rfm-analysis"></a>Nastavení analýzy RFM

[!include[banner](includes/banner.md)]


Toto téma vysvětluje, jak nastavit analýzu RFM (Recency, Frequency, and Monetary) odběratelů.

Analýza RFM je marketingový nástroj, který vaše organizace může používat k vyhodnocení dat, která je vygenerována nákupy odběratelů. Po nastavení analýzy RFM je odběratelů přiřazeno hodnocení RFM, jak nakupují. Hodnocení RFM může být trojmístné hodnocení nebo celkové číslo v závislosti na konfiguraci analýzy RFM ve vaší organizaci. Pokud vaše organizace používá pro výsledek trojmístné hodnocení, první číslice hodnocení je hodnocení aktuálnosti odběratele (před jakou dobou zákazník provedl nákup z vaší organizace). Druhá číslice je hodnocení frekvence zákazníka (jak často odběratel provádí nákupy od vaší organizace). Třetí číslice je ohodnocení peněžní částky zákazníka (kolik odběratel utratí při nákupech od vaší organizace). Například vaše organizace má nastavená hodnocení v rozsahu 1 až 5, kde 5 je nejvyšší hodnocení. V tomto případě hodnocení 535 odběratelů informuje následujících informace o zákazníkovi:

-   **Skóre aktuálnosti 5** – zákazník nedávno provedl nákup.
-   **Hodnocení četnosti 3** – odběratel středně často nakupuje produkty od vaší organizace.
-   **Peněžní hodnocení 5** – když zákazník nakoupí, utratí velké množství peněz.

Pokud vaše organizace používá agregaci těchto čísel, individuální hodnocení se sečtou. Například má zákazník ohodnocení 13 (5 + 3 + 5).




