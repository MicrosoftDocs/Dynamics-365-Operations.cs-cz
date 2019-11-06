---
title: Zákaz pravidel v kontrole konzistence maloobchodních transakcí
description: Toto téma popisuje funkci pro zákaz pravidel kontroly konzistence maloobchodních transakcí v aplikaci Microsoft Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586290"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>Zákaz pravidel v kontrole konzistence maloobchodních transakcí 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Maloobchodní prodejci mohou mít obchodní scénáře a procesy, které jsou pro ně jedinečné. Proto ne všechna pravidla, která jsou zahrnuta ve výchozím nastavení v kontrole konzistence transakcí maloobchodu, platí pro všechny maloobchodní prodejce. Pro přizpůsobení rozdílů poskytuje aplikace Microsoft Dynamics 365 Retail funkci, kterou lze použít k zakázání pravidel, která nelze použít.

Chcete-li zobrazit seznam pravidel, která jsou k dispozici v kontrole konzistence transakcí maloobchodu ve vašem prostředí, a zobrazit stav jednotlivých pravidel, přejděte na **Maloobchod \> Nastavení centrály \> Parametry \> Parametry maloobchodu** a pak zvolte kartu **Ověření transakce**

Ve výchozím nastavení je stav každého pravidla nastaven na **Povoleno**. Proto se všechna pravidla používají k ověření maloobchodních transakcí předtím, než jsou načtena do maloobchodních výkazů. Chcete-li pravidlo zakázat, změňte jeho stav na **Zakázáno**. Zakázaná pravidla nejsou zvažována při ověřování maloobchodních transakcí během procesu výpočtu výkazu.

Chcete-li obejít celý proces ověření bez ohledu na povolená pravidla, přejděte na **Maloobchod \> Nastavení centrály \> Parametry \> Parametry maloobchodu** a pak na kartě **Ověření transakcí** nastavte možnost **Zakázat kontrolu konzistence pro maloobchodní transakce** na **Ano**. Po nastavení této možnosti na **Ne** ji nelze z uživatelského rozhraní nastavit zpět na možnost **Ano**.
