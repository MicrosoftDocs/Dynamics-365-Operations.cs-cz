---
title: Chyba Typ platby musí být kreditní karta na stránce prodejní objednávky
description: Toto téma poskytuje pokyny pro řešení potíží, které vám mohou pomoci, když se po synchronizaci objednávky zobrazí chybová zpráva na stránce prodejní objednávky.
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
ms.openlocfilehash: 1d6813a642aefa59e20a7c77ddcf53ce7d3625eb
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347337"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>Chyba „Typ platby musí být kreditní karta“ na stránce prodejní objednávky

[!include [banner](../../includes/banner.md)]

Toto téma poskytuje pokyny pro řešení potíží, které vám mohou pomoci, když se po synchronizaci objednávky zobrazí chybová zpráva na stránce prodejní objednávky.

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
