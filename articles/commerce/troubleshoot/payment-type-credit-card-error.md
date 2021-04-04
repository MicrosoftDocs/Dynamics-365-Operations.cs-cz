---
title: Chyba Typ platby musí být kreditní karta na stránce prodejní objednávky
description: Toto téma poskytuje pokyny pro řešení potíží, které vám mohou pomoci, když se po synchronizaci objednávky zobrazí chybová zpráva na stránce prodejní objednávky.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 20f18507dee330fd1affedeee092b3dfa7cc10bc
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585232"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>Chyba „Typ platby musí být kreditní karta“ na stránce prodejní objednávky

[!include [banner](../../includes/banner.md)]

Toto téma poskytuje pokyny pro řešení potíží, které vám mohou pomoci, když se po synchronizaci objednávky zobrazí chybová zpráva na stránce prodejní objednávky.

## <a name="description"></a>popis

Když otevřete stránku prodejní objednávky po synchronizaci objednávky, zobrazí se následující chybová zpráva: „Typ platby musí být kreditní karta, protože bylo zadáno číslo kreditní karty“.

![Chyba typ platby musí být kreditní karta](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>Rozlišení

### <a name="set-the-payment-type-in-commerce-headquarters"></a>Nastavení typu platby v centrále Commerce

1. Přejděte do nabídky **Pohledávky \> Nastavení platby \> Platební podmínky**.
1. Na levém navigačním panelu vyberte platební podmínky.
1. V poli **Způsob platby** zkontrolujte, že je vybráno **Kreditní karta**.

## <a name="additional-resources"></a>Další prostředky

[Zaúčtování online prodeje a plateb](../tasks/posting-online-sales-payments.md)
