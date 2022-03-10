---
title: Zakázat pravidla používaná v procesu ověřování transakcí
description: Toto téma popisuje funkci pro zákaz pravidel ověřování transakcí v aplikaci Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 12/11/2021
ms.topic: index-page
ms.prod: ''
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
ms.openlocfilehash: cdaea51b4c84e6a62f0eb9412315ae77b4c11503
ms.sourcegitcommit: 9c2bc045eafc05b39ed1a6b601ccef48bd62ec55
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/14/2021
ms.locfileid: "7919518"
---
# <a name="disable-rules-used-in-the-transaction-validation-process"></a>Zakázat pravidla používaná v procesu ověřování transakcí

[!include [banner](../includes/banner.md)]

Maloobchodní prodejci mohou mít obchodní scénáře a procesy, které jsou pro ně jedinečné. Proto ne všechna pravidla, která jsou zahrnuta v nastavení procesu ověřování transakcí, platí pro všechny maloobchodní prodejce. Pro přizpůsobení rozdílů poskytuje aplikace Microsoft Dynamics 365 Commerce funkci, kterou lze použít k zakázání pravidel, která není třeba použít.

Chcete-li zobrazit seznam pravidel, která jsou k dispozici v procesu ověřování transakcí ve vašem prostředí, a zobrazit stav každého pravidla, přejděte na **Retail a Commerce \> Nastavení centrály \> Parametry \> Parametry Commerce** a vyberte kartu **Ověření transakce**. Všechna povolená pravidla se používají k ověření transakcí během procesu **Ověřit transakce obchodu** a musí proběhnout, aby se transakce mohly shromáždit a zaúčtovat na výkazu transakcí.

Ve výchozím nastavení je stav každého pravidla nastaven na **Povoleno**. Proto se všechna pravidla používají k ověření transakcí předtím, než je lze načíst do výkazu transakcí. Chcete-li pravidlo zakázat, změňte jeho stav na **Zakázáno**. Zakázaná pravidla nejsou zvažována při ověřování transakcí během procesu **Ověřit transakce obchodu**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
