---
title: Možnost Uložit pro mou další platbu se nezobrazí
description: Toto téma poskytuje pokyny pro řešení potíží, které vám mohou pomoci, když se políčko Uložit pro moji další platbu nezobrazí v části Platební metoda na stránce pokladny webu elektronického obchodování.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: af19a3abd78d543d82f7a8d017e2dc413115a6d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018427"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>Možnost „Uložit pro mou další platbu“ se nezobrazí

[!include [banner](../../includes/banner.md)]

Toto téma poskytuje pokyny pro řešení potíží, které vám mohou pomoci, když se políčko **Uložit pro moji další platbu** nezobrazí v části **Platební metoda** na stránce pokladny webu elektronického obchodování.

## <a name="description"></a>popis

Zaškrtávací políčko **Uložit na mou další platbu** políčko se nezobrazí v části **Způsob platby** na stránce pokladny webu elektronického obchodování.

Následující obrázek ukazuje příklad stránky pokladny, která obsahuje zaškrtávacího políčka **Uložit pro mou další platbu**.

![Zaškrtávací políčko Uložit pro mou další platbu v modulu Platba](media/payment-module-save-payment.jpg)

## <a name="resolution"></a>Rozlišení

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a>Ověřte, zda je Konektor platby Dynamics 365 pro Adyen správně nakonfigurován v centrále Commerce

K ověření, zda je Konektor platby Dynamics 365 pro Adyen správně nakonfigurován v centrále Commerce, postupujte následovně.

1. Přejděte na **Retail a Commerce \> Kanály \> Online obchody**.
1. Vyberte online obchod.
1. Na kartě s náhledem **Platební účty** zkontrolujte, že pole **Povolit ukládání platebních údajů v elektronickém obchodování** je nastaveno na **True**.

![Povolení ukládání platebních údajů v poli elektronického obchodu v centrále Commerce](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a>Další prostředky

[Platební modul](../payment-module.md)

[Úspora nástrojů online plateb s konektorem Adyen](../dev-itpro/adyen-connector-listPI.md)
