---
title: Zakázat pravidla používaná v procesu ověřování transakcí
description: Tento článek popisuje funkci pro zákaz pravidel ověřování transakcí v aplikaci Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 7d566aa3b829dad281528925a341382f9637fdba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884869"
---
# <a name="disable-rules-used-in-the-transaction-validation-process"></a>Zakázat pravidla používaná v procesu ověřování transakcí

[!include [banner](../includes/banner.md)]

Maloobchodní prodejci mohou mít obchodní scénáře a procesy, které jsou pro ně jedinečné. Proto ne všechna pravidla, která jsou zahrnuta v nastavení procesu ověřování transakcí, platí pro všechny maloobchodní prodejce. Pro přizpůsobení rozdílů poskytuje aplikace Microsoft Dynamics 365 Commerce funkci, kterou lze použít k zakázání pravidel, která není třeba použít.

Chcete-li zobrazit seznam pravidel, která jsou k dispozici v procesu ověřování transakcí ve vašem prostředí, a zobrazit stav každého pravidla, přejděte na **Retail a Commerce \> Nastavení centrály \> Parametry \> Parametry Commerce** a vyberte kartu **Ověření transakce**. Všechna povolená pravidla se používají k ověření transakcí během procesu **Ověřit transakce obchodu** a musí proběhnout, aby se transakce mohly shromáždit a zaúčtovat na výkazu transakcí.

Ve výchozím nastavení je stav každého pravidla nastaven na **Povoleno**. Proto se všechna pravidla používají k ověření transakcí předtím, než je lze načíst do výkazu transakcí. Chcete-li pravidlo zakázat, změňte jeho stav na **Zakázáno**. Zakázaná pravidla nejsou zvažována při ověřování transakcí během procesu **Ověřit transakce obchodu**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
