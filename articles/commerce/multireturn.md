---
title: Vrácení položek napříč vícero objednávkami odběratele a fakturami
description: Tento článek popisuje funkci, která umožňuje vrácení napříč vícero objednávkami odběratele a fakturami v Dynamics 365 Commerce.
author: josaw1
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 65ef700db5a81c49a962fd388af54e7811c088d2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890314"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Vrácení položek napříč vícero objednávkami odběratele a fakturami

[!include [banner](includes/banner.md)]


Vrácení lze provést napříč vícero objednávkami a fakturami. 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a>Konfigurace aplikace Commerce pro podporu vrácení napříč vícero objednávkami a fakturami

1. Přejděte na **Parametry obchodu \> Objednávky odběratele**.
1. Zapněte parametr **Povolit vrácení pro více objednávek**. 

## <a name="process-returns"></a>Zpracování vracení

Poté, co je zapnut tento parametr a změny se synchronizují do obchodů, pokladník v obchodě může zvolit více prodejních objednávek pro odběratele k vrácení.

Když jsou zvoleny objednávky, zobrazí se seznam všech vratných produktů napříč všemi fakturami pro objednávky. Pokladník může poté zvolit produkty, které mají být vráceny. Pro všechny zvolené produkty bude vytvořena jediná vratka.
