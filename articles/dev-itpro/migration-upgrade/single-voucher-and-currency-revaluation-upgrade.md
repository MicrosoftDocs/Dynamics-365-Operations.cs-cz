---
title: "Upgrade deníků jednoho dokladu a přecenění měny"
description: "Některé organizace zadávají deníky obsahující jeden doklad, který má více než jednoho odběratele nebo dodavatele, a rovněž spouští proces přecenění cizí měny pohledávek a závazků. Toto téma popisuje kroky, podle kterých by tyto organizace měly postupovat při upgradu na aplikaci Microsoft Dynamics 365 for Operations verze 1611."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 343fa226e1cf9072696082e9ebf0a1629e553ae9
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---

# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a>Upgrade deníků jednoho dokladu a přecenění měny

[!include [banner](../includes/banner.md)]

Některé organizace zadávají deníky obsahující jeden doklad, který má více než jednoho odběratele nebo dodavatele, a rovněž spouští proces přecenění cizí měny pohledávek a závazků. Toto téma popisuje kroky, podle kterých by tyto organizace měly postupovat při upgradu na aplikaci Microsoft Dynamics 365 for Operations verze 1611.

Při upgradu na Microsoft Dynamics 365 for Operations verzi 1611 postupujte následujícím způsobem.

1.  Před upgradem na aplikaci Dynamics 365 for Operations spusťte procesy přecenění cizí měny pro pohledávky a závazky. Pole **Metoda** nastavte na **Datum faktury**. Transakce přecenění je vytvořena, aby vrátila zpět poslední přecenění cizí měny. Proto se otevřené transakce oceňují v jejich původní zúčtovací měně.
2.  Upgrade na Dynamics 365 for Operations verze 1611.
3.  Spusťte znovu procesy přecenění cizí měny pohledávek a závazků Tentokrát nastavte pole **Metoda** na **Standardní**. Vytvoří se nová transakce přecenění, která je založena na aktuálních směnných kurzech. Tato transakce zaznamená nerealizovaný zisk/ztrátu a správný součtový účet hlavní knihy.





