---
title: Chyba synchronizace objednávky související s výchozí platební službou
description: Toto téma obsahuje pokyny pro řešení potíží, které vám pomohou opravit chybu, která může nastat při synchronizaci online objednávky.
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
ms.openlocfilehash: fa174bbb257379f6ce906dd21180bbcb19f8bc3f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021120"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>Chyba synchronizace objednávky související s výchozí platební službou

[!include [banner](../../includes/banner.md)]

Toto téma obsahuje pokyny pro řešení potíží, které vám pomohou opravit chybu, která může nastat při synchronizaci online objednávky.

## <a name="description"></a>popis

Při synchronizaci online objednávky se zobrazí následující chybová zpráva: „Ke zpracování transakcí kreditní kartou musí existovat výchozí platební služba.“

![Chybí výchozí chyba platební služby](media/default-payment-method-error.jpg)

## <a name="resolution"></a>Rozlišení

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>Potvrzení nebo nastavení výchozí platební služby v centrále Commerce

K potvrzení nebo nastavení výchozí platební služby v centrále Commerce postupujte následovně.

1. Přejděte do nabídky **Pohledávky \> Nastavení platby \> Služby pro platby**.
1. Ujistěte se, že je možnost **Výchozí zpracovatel pro nové kreditní karty** je nastavena na **Ano** pro jednu platební službu.

## <a name="additional-resources"></a>Další prostředky

[Nastavení platební karty, autorizace a záznam](../../finance/accounts-receivable/credit-card-authorizations.md)