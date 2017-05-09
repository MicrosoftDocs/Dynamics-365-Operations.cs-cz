---
title: "Upgrade týkající se jednoho dokladu a přecenění měny pro aplikaci Microsoft Dynamics 365 for Operations verze 1611"
description: "Některé organizace zadávají deníky obsahující jeden doklad, který má více než jednoho odběratele nebo dodavatele, a rovněž spouští proces přecenění cizí měny pohledávek a závazků. Toto téma popisuje kroky, podle kterých by tyto organizace měly postupovat při upgradu na aplikaci Microsoft Dynamics 365 for Operations verze 1611."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-28 16 - 04 - 17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d42c753d0dc8b8efc2a0d2a26da32a4951d85503
ms.lasthandoff: 03/31/2017


---

# <a name="single-voucher-and-currency-revaluation-upgrade-for-microsoft-dynamics-365-for-operations-version-1611"></a>Upgrade týkající se jednoho dokladu a přecenění měny pro aplikaci Microsoft Dynamics 365 for Operations verze 1611

Některé organizace zadávají deníky obsahující jeden doklad, který má více než jednoho odběratele nebo dodavatele, a rovněž spouští proces přecenění cizí měny pohledávek a závazků. Toto téma popisuje kroky, podle kterých by tyto organizace měly postupovat při upgradu na aplikaci Microsoft Dynamics 365 for Operations verze 1611.

Při upgradu na Microsoft Dynamics 365 for Operations verzi 1611 postupujte následujícím způsobem.

1.  Před upgradem na aplikaci Dynamics 365 for Operations spusťte procesy přecenění cizí měny pro pohledávky a závazky. Pole **Metoda** nastavte na **Datum faktury**. Transakce přecenění je vytvořena, aby vrátila zpět poslední přecenění cizí měny. Proto se otevřené transakce oceňují v jejich původní zúčtovací měně.
2.  Upgrade na Dynamics 365 for Operations verze 1611.
3.  Spusťte znovu procesy přecenění cizí měny pohledávek a závazků Tentokrát nastavte pole **Metoda** na **Standardní**. Vytvoří se nová transakce přecenění, která je založena na aktuálních směnných kurzech. Tato transakce zaznamená nerealizovaný zisk/ztrátu a správný součtový účet hlavní knihy.



