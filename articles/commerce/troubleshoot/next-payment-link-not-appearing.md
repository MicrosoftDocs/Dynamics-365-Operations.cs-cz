---
title: Možnost Uložit pro mou další platbu se nezobrazí
description: Tento článek poskytuje pokyny pro řešení potíží, které vám mohou pomoci, když se políčko Uložit pro moji další platbu nezobrazí v části Platební metoda na stránce pokladny webu elektronického obchodování.
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
ms.openlocfilehash: efa04c87f78c376fd00da1b26aedb9e8b428dfa5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871548"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>Možnost „Uložit pro mou další platbu“ se nezobrazí

[!include [banner](../../includes/banner.md)]

Tento článek poskytuje pokyny pro řešení potíží, které vám mohou pomoci, když se políčko **Uložit pro moji další platbu** nezobrazí v části **Platební metoda** na stránce pokladny webu elektronického obchodování.

## <a name="description"></a>popis

Zaškrtávací políčko **Uložit na mou další platbu** políčko se nezobrazí v části **Způsob platby** na stránce pokladny webu elektronického obchodování.

Následující obrázek ukazuje příklad stránky pokladny, která obsahuje zaškrtávacího políčka **Uložit pro mou další platbu**.

![Zaškrtávací políčko Uložit pro mou další platbu v modulu Platba.](media/payment-module-save-payment.jpg)

## <a name="resolution"></a>Řešení

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a>Ověřte, zda je Konektor platby Dynamics 365 pro Adyen správně nakonfigurován v centrále Commerce

K ověření, zda je Konektor platby Dynamics 365 pro Adyen správně nakonfigurován v centrále Commerce, postupujte následovně.

1. Přejděte na **Retail a Commerce \> Kanály \> Online obchody**.
1. Vyberte online obchod.
1. Na kartě s náhledem **Platební účty** zkontrolujte, že pole **Povolit ukládání platebních údajů v elektronickém obchodování** je nastaveno na **True**.

![Povolení ukládání platebních údajů v poli elektronického obchodu v centrále Commerce.](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a>Další prostředky

[Platební modul](../payment-module.md)

[Úspora nástrojů online plateb s konektorem Adyen](../dev-itpro/adyen-connector-listPI.md)
