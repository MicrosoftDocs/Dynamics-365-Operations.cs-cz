---
title: Chyba Typ platby musí být kreditní karta na stránce prodejní objednávky
description: Tento článek poskytuje pokyny pro řešení potíží, které vám mohou pomoci, když se po synchronizaci objednávky zobrazí chybová zpráva na stránce prodejní objednávky.
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
ms.openlocfilehash: 71c5cbaf574866c74e222f4d67132004327db8fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285625"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>Chyba „Typ platby musí být kreditní karta“ na stránce prodejní objednávky

[!include [banner](../../includes/banner.md)]

Tento článek poskytuje pokyny pro řešení potíží, které vám mohou pomoci, když se po synchronizaci objednávky zobrazí chybová zpráva na stránce prodejní objednávky.

## <a name="description"></a>popis

Když otevřete stránku prodejní objednávky po synchronizaci objednávky, zobrazí se následující chybová zpráva: „Typ platby musí být kreditní karta, protože bylo zadáno číslo kreditní karty“.

![Chyba typ platby musí být kreditní karta.](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>Řešení

### <a name="set-the-payment-type-in-commerce-headquarters"></a>Nastavení typu platby v centrále Commerce

1. Přejděte do nabídky **Pohledávky \> Nastavení platby \> Platební podmínky**.
1. Na levém navigačním panelu vyberte platební podmínky.
1. V poli **Způsob platby** zkontrolujte, že je vybráno **Kreditní karta**.

## <a name="additional-resources"></a>Další prostředky

[Zaúčtování online prodeje a plateb](../tasks/posting-online-sales-payments.md)
