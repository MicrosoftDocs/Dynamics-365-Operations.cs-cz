---
title: Upgrade deníků jednoho dokladu a přecenění měny
description: Některé organizace zadávají deníky obsahující jeden doklad, který má více než jednoho odběratele nebo dodavatele, a rovněž spouští proces přecenění cizí měny pohledávek a závazků. Toto téma popisuje kroky, podle kterých by tyto organizace měly postupovat při upgradu na aplikaci Microsoft Dynamics 365 for Operations verze 1611.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5fa955f4548acc48208d8b151d1eee1fa5e59225
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249042"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a>Upgrade deníků jednoho dokladu a přecenění měny

[!include [banner](../includes/banner.md)]

Některé organizace zadávají deníky obsahující jeden doklad, který má více než jednoho odběratele nebo dodavatele, a rovněž spouští proces přecenění cizí měny pohledávek a závazků. Toto téma popisuje kroky, podle kterých by tyto organizace měly postupovat při upgradu na aplikaci Microsoft Dynamics 365 for Operations verze 1611.

Tyto kroky použijte při upgradu na Microsoft Dynamics 365 for Operations verze 1611.

1.  Před upgradem na aplikaci Finance and Operations spusťte procesy přecenění cizí měny pro pohledávky a závazky. Pole **Metoda** nastavte na **Datum faktury**. Transakce přecenění je vytvořena, aby vrátila zpět poslední přecenění cizí měny. Proto se otevřené transakce oceňují v jejich původní zúčtovací měně.
2.  Upgrade na verzi 1611.
3.  Spusťte znovu procesy přecenění cizí měny pohledávek a závazků Tentokrát nastavte pole **Metoda** na **Standardní**. Vytvoří se nová transakce přecenění, která je založena na aktuálních směnných kurzech. Tato transakce zaznamená nerealizovaný zisk/ztrátu a správný součtový účet hlavní knihy.
