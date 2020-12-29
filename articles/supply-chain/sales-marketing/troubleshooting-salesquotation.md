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
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423768"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="4a0aa-103">Řešení problémů s prodejními nabídkami</span><span class="sxs-lookup"><span data-stu-id="4a0aa-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="4a0aa-104">Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s prodejními nabídkami.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="4a0aa-105">Nemohu změnit prodejní množství prodejní nabídky pro položku služby.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="4a0aa-106">Popis problému</span><span class="sxs-lookup"><span data-stu-id="4a0aa-106">Issue description</span></span>

<span data-ttu-id="4a0aa-107">Pokud se pokusíte nastavit prodejní množství (pole **SalesQty**) pro položku typu *Služba* na řádku prodejní nabídky, zobrazí se následující zpráva: „Aktualizace není povolena pro pole Množství.“</span><span class="sxs-lookup"><span data-stu-id="4a0aa-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4a0aa-108">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="4a0aa-108">Issue resolution</span></span>

<span data-ttu-id="4a0aa-109">U produktů, které jsou položkami služby, nemůžete nastavit prodejní množství.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="4a0aa-110">Například pokud nabídnete službu pro instalaci položky, nemá smysl zaznamenávat množství, protože neexistuje žádná fyzická položka.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="4a0aa-111">Existuje pouze služba.</span><span class="sxs-lookup"><span data-stu-id="4a0aa-111">There is only a service.</span></span>

