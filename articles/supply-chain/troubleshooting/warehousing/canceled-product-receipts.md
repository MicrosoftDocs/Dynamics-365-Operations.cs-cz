---
title: Zrušené příjmy produktů neaktualizují stav transakce na Registrovaný
description: Po zrušení příjmu produktu při příchozím načtení systém automaticky aktualizuje stav transakce inventáře z Přijato na Objednané.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294027"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a><span data-ttu-id="a2a26-103">Zrušené příjmy produktů neaktualizují stav transakce na Registrovaný</span><span class="sxs-lookup"><span data-stu-id="a2a26-103">Canceled product receipts don't update transaction status to Registered</span></span>

## <a name="symptoms"></a><span data-ttu-id="a2a26-104">Příznaky</span><span class="sxs-lookup"><span data-stu-id="a2a26-104">Symptoms</span></span>

<span data-ttu-id="a2a26-105">Po spuštění akce **Zrušení příjmu produktu** při příchozím načtení systém automaticky aktualizuje stav transakce inventáře z *Přijato* na *Objednané*.</span><span class="sxs-lookup"><span data-stu-id="a2a26-105">After you run the **Cancel product receipts** action on an inbound load, the system automatically updates the status of inventory transactions from *Received* to *Ordered*.</span></span>

## <a name="resolution"></a><span data-ttu-id="a2a26-106">Řešení</span><span class="sxs-lookup"><span data-stu-id="a2a26-106">Resolution</span></span>

<span data-ttu-id="a2a26-107">Když jsou dodací listy zrušeny pro odchozí zatížení, stav transakcí zásob zůstane *Vydáno*.</span><span class="sxs-lookup"><span data-stu-id="a2a26-107">When packing slips are canceled for outbound loads, the status of inventory transactions remains *Picked*.</span></span> <span data-ttu-id="a2a26-108">Když se však zruší příjmy produktu z příchozího zatížení, stav inventárních transakcí se neobnoví na *Registrováno*.</span><span class="sxs-lookup"><span data-stu-id="a2a26-108">However, when product receipts from an inbound load are canceled, the status of inventory transactions isn't restored to *Registered*.</span></span> <span data-ttu-id="a2a26-109">Proto po zrušení příjmu produktu z příchozího nákladu musí pracovník skladu znovu zaregistrovat množství položek pro zatížení.</span><span class="sxs-lookup"><span data-stu-id="a2a26-109">Therefore, after a product receipt from an inbound load is canceled, the warehouse worker must re-register item quantities for the loads.</span></span>

<span data-ttu-id="a2a26-110">Další informace viz [Zaregistrujte množství zboží, které dorazí v příchozím nákladu](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span><span class="sxs-lookup"><span data-stu-id="a2a26-110">For more information, see [Register item quantities that arrive on an inbound load](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span></span>
