---
title: Vrácení položek napříč vícero objednávkami odběratele a fakturami
description: Toto téma popisuje funkci, která umožňuje vrácení napříč vícero objednávkami odběratele a fakturami v Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
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
ms.openlocfilehash: 25a1081e5f903076e23089c41dda7437f8a70124
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017982"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Vrácení položek napříč vícero objednávkami odběratele a fakturami

[!include [banner](includes/banner.md)]


Vrácení lze provést napříč vícero objednávkami a fakturami. 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a>Konfigurace aplikace Retail pro podporu vrácení napříč vícero objednávkami a fakturami

1. Přejděte na **Parametry maloobchodu \> Objednávky odběratele**.
1. Zapněte parametr **Povolit vrácení pro více objednávek**. 

## <a name="process-returns"></a>Zpracování vracení

Poté, co je zapnut tento parametr a změny se synchronizují do obchodů, pokladník v obchodě může zvolit více prodejních objednávek pro odběratele k vrácení.

Když jsou zvoleny objednávky, zobrazí se seznam všech vratných produktů napříč všemi fakturami pro objednávky. Pokladník může poté zvolit produkty, které mají být vráceny. Pro všechny zvolené produkty bude vytvořena jediná vratka.
