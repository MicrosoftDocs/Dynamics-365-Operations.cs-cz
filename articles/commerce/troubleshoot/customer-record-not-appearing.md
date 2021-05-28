---
title: Záznamy zákazníků se nezobrazují v centrále Commerce
description: Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když se záznamy zákazníků okamžitě nezobrazí v centrále Commerce.
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
ms.openlocfilehash: b8d065dd104df616ba8f10f7813e74c900fdcf77
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018475"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a>Záznamy zákazníků se nezobrazují v centrále Commerce

[!include [banner](../../includes/banner.md)]

Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když se záznamy zákazníků okamžitě nezobrazí v centrále Commerce.

## <a name="description"></a>popis

Když vytvoříte nový záznam zákazníka pomocí toku přihlášení na webu elektronického obchodu, odpovídající záznam zákazníka se okamžitě nezobrazí v centrále Commerce.

## <a name="resolution"></a>Rozlišení

### <a name="disable-customer-creation-in-async-mode"></a>Zakázání vytváření zákazníků v asynchronním režimu

> [!IMPORTANT]
> Pokud zakážete asynchronní vytváření zákazníků, může to ovlivnit výkon systému, protože vytvoření každého záznamu vytvoří požadavek v reálném čase na centrálu Commerce. Kromě toho, pokud je sídlo společnosti Commerce nefunkční (například během servisních toků), jakékoli nové toky vytváření zákazníků způsobí chyby.

Chcete-li zakázat vytváření zákazníků v asynchronním režimu v centrále Commerce, postupujte takto.

1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Nastavení online obchodu \> Funkční profily**.
1. Pokud pro svůj online kanál ještě nepoužíváte funkční profil, vytvořte si ho.
1. Ujistěte se, že možnost **Vytvořit zákazníka v asynchronním režimu** je nastavena na **Ne**.
1. Přejděte na **Retail a Commerce \> Kanály \> Online obchody**.
1. Vyberte online obchod, pro který zakážete asynchronní vytváření zákazníků.
1. Na kartě **Všeobecné** zkontrolujte se, že pole **Funkční profil** je nastaveno na funkční profil, který používáte pro svůj online kanál.

## <a name="additional-resources"></a>Další prostředky

[Nastavení klienta B2C v Commerce](../set-up-b2c-tenant.md)
