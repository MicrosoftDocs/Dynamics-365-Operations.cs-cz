---
title: "Jediný doklad a přecenění měny aktualizace pro Microsoft Dynamics 365 pro verzi operace 1611"
description: "Některé organizace zadejte deníků, které obsahují jeden doklad, který má více než jednoho odběratele nebo dodavatele a také spustit pohledávky nebo procesu přecenění cizí měny platí účty. Toto téma popisuje kroky, které tyto organizace by měla provést při upgradu na Microsoft Dynamics 365 pro verzi operace 1611."
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

# <a name="single-voucher-and-currency-revaluation-upgrade-for-microsoft-dynamics-365-for-operations-version-1611"></a>Jediný doklad a přecenění měny aktualizace pro Microsoft Dynamics 365 pro verzi operace 1611

Některé organizace zadejte deníků, které obsahují jeden doklad, který má více než jednoho odběratele nebo dodavatele a také spustit pohledávky nebo procesu přecenění cizí měny platí účty. Toto téma popisuje kroky, které tyto organizace by měla provést při upgradu na Microsoft Dynamics 365 pro verzi operace 1611.

Při upgradu na Microsoft Dynamics 365 pro verzi operace 1611, postupujte následujícím způsobem.

1.  Před inovací na 365 Dynamics pro operace spuštění procesů přecenění cizí měny pro účty pohledávek a závazků. Nastavit **metoda** na **datum faktury**. Transakce přecenění je vytvořen, který vrátí zpět poslední přecenění cizí měny. Proto se oceňují v jejich původní zúčtovací měnu otevřené transakce.
2.  Upgrade verze operace 1611 Dynamics 365.
3.  Pohledávek a účty závazků cizí měny přecenění procesy spusťte znovu. Tentokrát nastavte **metoda** na **standardní**. Nové transakce přecenění je vytvořen, který je založen na aktuálních směnných kurzů. Tato transakce zaznamená nerealizovaný zisk/ztráta a správné součtový účet hlavní knihy.



