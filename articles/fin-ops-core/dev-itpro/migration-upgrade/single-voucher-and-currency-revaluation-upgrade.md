---
title: Upgrade deníků jednoho dokladu a přecenění měny
description: Toto téma popisuje, jak postupovat při upgradu deníků jednoho dokladu a přecenění měny.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: feafcd5c309360467344618f7cec15235ddbe77df807f75873ac82c941073500
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735487"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a>Upgrade deníků jednoho dokladu a přecenění měny

[!include [banner](../includes/banner.md)]

Některé organizace zadávají deníky obsahující jeden doklad, který má více než jednoho odběratele nebo dodavatele, a rovněž spouští proces přecenění cizí měny pohledávek a závazků. Toto téma popisuje kroky, podle kterých by tyto organizace měly postupovat při upgradu na aplikaci Microsoft Dynamics 365 for Operations verze 1611.

Tyto kroky použijte při upgradu na Microsoft Dynamics 365 for Operations verze 1611.

1.  Před upgradem na aplikaci Finance and Operations spusťte procesy přecenění cizí měny pro pohledávky a závazky. Pole **Metoda** nastavte na **Datum faktury**. Transakce přecenění je vytvořena, aby vrátila zpět poslední přecenění cizí měny. Proto se otevřené transakce oceňují v jejich původní zúčtovací měně.
2.  Upgrade na verzi 1611.
3.  Spusťte znovu procesy přecenění cizí měny pohledávek a závazků Tentokrát nastavte pole **Metoda** na **Standardní**. Vytvoří se nová transakce přecenění, která je založena na aktuálních směnných kurzech. Tato transakce zaznamená nerealizovaný zisk/ztrátu a správný součtový účet hlavní knihy.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]