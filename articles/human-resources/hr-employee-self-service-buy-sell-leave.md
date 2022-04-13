---
title: Koupit a prodat pracovní volno
description: Toto téma popisuje, jak odeslat žádosti o nákup a prodej dovolené v Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 80b7125df93d9bdfb866b37abebbdc412d7e5b95
ms.sourcegitcommit: 67c4ed957e43d4d60bb609d93921a0be9619e675
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2022
ms.locfileid: "8509381"
---
# <a name="buy-and-sell-leave"></a>Koupě a prodej pracovního volna


>[!Important]
>Funkce uvedené v tomto tématu jsou aktuálně dostupné pro zákazníky používající samostatnou verzi aplikace Dynamics 365 Human Resources. Některé nebo všechny funkce budou dostupné jako součást budoucího vydání na infrastruktury Finance po vydání Finance 10.0.26.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

V aplikaci Dynamics 365 Human Resources můžete odesílat žádosti o nákup a prodej pracovního volna na základě zásad nákupu a prodeje pracovního volna stanovených vaší společností.  

## <a name="request-to-buy-leave"></a>Žádost o koupi volna

1. V pracovním prostoru **Samoobsluha pro zaměstnance** vyberte **Žádost o koupi volna** v dlaždici **Zůstatky volna**. 

2. Přejte **Typ volna** a zadejte **Množství** volna, které chcete koupit. 

3. Jakmile budete připravení žádost odeslat, vyberte **Odeslat**. 

Vaše zůstatky se před aktualizací buď automaticky aktualizují, nebo projdou schvalovacím procesem. To záleží na tom, jak byla nakonfigurována zásada nákupu.

## <a name="request-to-sell-leave"></a>Žádost o prodej pracovního volna

1. V pracovním prostoru **Samoobsluha pro zaměstnance** vyberte **Žádost o prodej pracovního volna** v dlaždici **Zůstatky volna**. 

2. Přejte **Typ pracovního volna** a zadejte **Množství** pracovního volna, které chcete prodat. 

3. Jakmile budete připravení žádost odeslat, vyberte **Odeslat**.

Vaše zůstatky se před aktualizací buď automaticky aktualizují, nebo projdou schvalovacím procesem. To záleží na tom, jak byla nakonfigurována zásada nákupu.


## <a name="troubleshooting"></a>Řešení potíží 

Pokud pracovní postup požadavku na nákup nebo prodej volna selže, uživatelé s oprávněním **EssLeaveBuySellRequestApprover** mohou zkontrolovat protokol zpráv o všech požadavcích na nákup a prodej. Chcete-li to provést, přejděte na **Pracovní volno a nepřítomnost > Odkazy > Žádosti o nákup a prodej volna > Protokol zpráv** (vlevo nahoře). **Protokol zpráv** ukazuje uživatelům, jak byly transakce zpracovány, a související historii pracovního postupu.


## <a name="see-also"></a>Viz také

[Přehled pracovního volna a absencí](hr-leave-and-absence-overview.md)</br>
[Správa zásad nákupu a prodeje pracovního volna](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
