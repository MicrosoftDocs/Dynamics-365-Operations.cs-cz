---
title: Zákaz pravidel v kontrole konzistence maloobchodních transakcí
description: Toto téma popisuje funkci pro zákaz pravidel kontroly konzistence transakcí v aplikaci Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: abd97819d44963d22269efc9536f746c3c0b3812
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230583"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>Zákaz pravidel v kontrole konzistence maloobchodních transakcí 

[!include [banner](../includes/banner.md)]

Maloobchodní prodejci mohou mít obchodní scénáře a procesy, které jsou pro ně jedinečné. Proto ne všechna pravidla, která jsou zahrnuta ve výchozím nastavení v kontrole konzistence obchodních transakcí, platí pro všechny maloobchodní prodejce. Pro přizpůsobení rozdílů poskytuje aplikace Microsoft Dynamics 365 Commerce funkci, kterou lze použít k zakázání pravidel, která nelze použít.

Chcete-li zobrazit seznam pravidel, která jsou k dispozici v kontrole konzistence transakcí maloobchodu ve vašem prostředí, a zobrazit stav jednotlivých pravidel, přejděte na **Retail a Commerce \> Nastavení centrály \> Parametry \> Parametry Commerce** a pak zvolte kartu **Ověření transakce**

Ve výchozím nastavení je stav každého pravidla nastaven na **Povoleno**. Proto se všechna pravidla používají k ověření transakcí předtím, než jsou načtena do obchodních výkazů. Chcete-li pravidlo zakázat, změňte jeho stav na **Zakázáno**. Zakázaná pravidla nejsou zvažována při ověřování transakcí během procesu výpočtu výkazu.

Chcete-li obejít celý proces ověření bez ohledu na povolená pravidla, přejděte na **Retail a Commerce \> Nastavení centrály \> Parametry \> Parametry Commerce** a pak na kartě **Ověření transakcí** nastavte možnost **Zakázat kontrolu konzistence pro obchodní transakce** na **Ano**. Po nastavení této možnosti na **Ne** ji nelze z uživatelského rozhraní nastavit zpět na možnost **Ano**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]