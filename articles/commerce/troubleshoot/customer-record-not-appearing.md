---
title: Záznamy zákazníků se nezobrazují v centrále Commerce
description: Tento článek poskytuje pokyny pro řešení potíží, které mohou pomoci, když se záznamy zákazníků okamžitě nezobrazí v Commerce headquarters.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: f1ad1f45abbc95cbf6d41b3c8681db781c6c9d23
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268831"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a>Záznamy zákazníků se nezobrazují v centrále Commerce

[!include [banner](../../includes/banner.md)]

Tento článek poskytuje pokyny pro řešení potíží, které mohou pomoci, když se záznamy zákazníků okamžitě nezobrazí v Commerce headquarters.

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
