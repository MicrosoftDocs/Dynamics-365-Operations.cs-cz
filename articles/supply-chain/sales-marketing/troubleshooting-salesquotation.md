---
title: Řešení problémů s prodejními nabídkami
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s prodejními nabídkami.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 67610a833be132399b2d47ae8c6b27119be9ce95
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834325"
---
# <a name="troubleshoot-sales-quotations"></a>Řešení problémů s prodejními nabídkami

Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s prodejními nabídkami.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>Nemohu změnit prodejní množství prodejní nabídky pro položku služby.

### <a name="issue-description"></a>Popis problému

Pokud se pokusíte nastavit prodejní množství (pole **SalesQty**) pro položku typu *Služba* na řádku prodejní nabídky, zobrazí se následující zpráva: „Aktualizace není povolena pro pole Množství.“

### <a name="issue-resolution"></a>Řešení problému

U produktů, které jsou položkami služby, nemůžete nastavit prodejní množství. Například pokud nabídnete službu pro instalaci položky, nemá smysl zaznamenávat množství, protože neexistuje žádná fyzická položka. Existuje pouze služba.

