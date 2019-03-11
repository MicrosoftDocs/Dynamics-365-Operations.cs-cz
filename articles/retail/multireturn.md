---
title: Vrácení položek napříč vícero objednávkami odběratele a fakturami
description: Toto téma popisuje funkci, která umožňuje vrácení napříč vícero objednávkami odběratele a fakturami v Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 1/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: d2cf6f92e90ef196827abb599c65c732615ec7bb
ms.sourcegitcommit: e72eae546d48d41d4b07ff78cfc0242c32b793e7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2019
ms.locfileid: "373061"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Vrácení položek napříč vícero objednávkami odběratele a fakturami

[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

V aplikaci Dynamics 365 for Finance and Operations verze 10.0 lze provést vrácení napříč vícero objednávkami a fakturami, zatímco ve verzích předcházejících verzi 10.0 mohla být vrácení zpracovávána pouze pomocí jedné faktury současně. 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a>Konfigurace aplikace Retail pro podporu vrácení napříč vícero objednávkami a fakturami

1. Přejděte na **Parametry maloobchodu \> Objednávky odběratele**.
1. Zapněte parametr **Povolit vrácení pro více objednávek**. 

## <a name="process-returns"></a>Zpracování vracení

Poté, co je zapnut tento parametr a změny se synchronizují do obchodů, pokladník v obchodě může zvolit více prodejních objednávek pro odběratele k vrácení.

Když jsou zvoleny objednávky, zobrazí se seznam všech vratných produktů napříč všemi fakturami pro objednávky. Pokladník může poté zvolit produkty, které mají být vráceny. Pro všechny zvolené produkty bude vytvořena jediná vratka.
