---
title: Přidání typu částky platby
description: Tento článek vysvětluje, jak nastavit typy částky platby v leasingu majetku.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRevaluation
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 03fc903e6cfe78ef2fed7e3a0744a8f809f6892d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891602"
---
# <a name="add-payment-amount-types"></a>Přidání typu částky platby

[!include [banner](../includes/banner.md)]

Tento článek popis, jak nastavit typy částky platby v leasingu majetku. Tímto způsobem můžete rozepsat částku leasingové splátky namísto přidávání jednorázové částky do řádků splátkového kalendáře.

Chcete-li přidat typy částky platby, postupujte takto:

1. Přejděte na **Leasing majetku \> Nastavení \> Typy částek platby**.
2. Zvolte **Nové**.
3. Zadejte nový typ platby a popis.

> [!NOTE]
> Pro přecenění indexu podle IFRS 16 musíte vytvořit jeden typ částky platby a označit jej jako **Používá se pro přecenění indexu IRFS 16**. Tento typ částky platby se použije, když je proces přecenění indexu spuštěn podle knihy IFRS 16, a vezme v úvahu změny, ke kterým došlo v důsledku procesu přecenění indexu.
>
> Když je možnost **Rozpis plateb** možnost v leasingu nastavena na **Ano**, pokud je provedeno přecenění indexu pro IFRS 16, ale neexistuje žádný typ platby pro IFRS 16, proces nebude dokončen.

Jako lze označit pouze jeden záznam **Používá se pro přecenění indexu IFRS 16**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
