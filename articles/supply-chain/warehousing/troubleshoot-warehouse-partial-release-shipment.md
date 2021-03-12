---
title: Odstraňování potíží s částečným uvolněním a částečnou dodávkou
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s příchozími s částečným uvolněním a částečnými dodávkami v Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 33323a8aed44cf19db6c2c937abcb09f7e05b6c1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993932"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a><span data-ttu-id="63bcc-103">Odstraňování potíží s částečným uvolněním a částečnou dodávkou</span><span class="sxs-lookup"><span data-stu-id="63bcc-103">Troubleshoot partial releases and partial shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63bcc-104">Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s příchozími s částečným uvolněním a částečnými dodávkami v Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="63bcc-104">This topic describes how to fix common issues that you might encounter while you work with partial releases and partial shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a><span data-ttu-id="63bcc-105">Stav uvolnění prodejní objednávky zůstává Částečně uvolněn i po fakturaci prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="63bcc-105">The release status of a sales order remains Partially released even after the sales order is invoiced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="63bcc-106">Popis problému</span><span class="sxs-lookup"><span data-stu-id="63bcc-106">Issue description</span></span>

<span data-ttu-id="63bcc-107">Prodejní objednávka je objednávka dodání, ale jedna nebo více položek v ní má jiný způsob dodání.</span><span class="sxs-lookup"><span data-stu-id="63bcc-107">A sales order is a delivery order, but one or more items on it have a different mode of delivery.</span></span> <span data-ttu-id="63bcc-108">Po fakturaci objednávky má stále stav uvolnění *Částečně uvolněn*.</span><span class="sxs-lookup"><span data-stu-id="63bcc-108">After the order is invoiced, it still has a release status of *Partially released*.</span></span>

<span data-ttu-id="63bcc-109">Například prodejní objednávka má dvě položky: jednu pro doručení a druhou pro vyzvednutí.</span><span class="sxs-lookup"><span data-stu-id="63bcc-109">For example, a sales order has two items: one for delivery and one for pickup.</span></span> <span data-ttu-id="63bcc-110">Dodání i vyzvednutí byly provedeny.</span><span class="sxs-lookup"><span data-stu-id="63bcc-110">Both the delivery and the pickup have been done.</span></span> <span data-ttu-id="63bcc-111">Proto byly oba řádky fakturovány.</span><span class="sxs-lookup"><span data-stu-id="63bcc-111">Therefore, both lines have been invoiced.</span></span> <span data-ttu-id="63bcc-112">Stav uvolnění se však stále zobrazuje jako *Částečně uvolněno*, což je zavádějící.</span><span class="sxs-lookup"><span data-stu-id="63bcc-112">However, the release status is still shown as *Partially released*, which is misleading.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="63bcc-113">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="63bcc-113">Issue resolution</span></span>

<span data-ttu-id="63bcc-114">Stav uvolnění se vztahuje pouze na řádky objednávky, kde jsou položky povoleny pro správu skladu.</span><span class="sxs-lookup"><span data-stu-id="63bcc-114">The release status applies only to order lines where the items are enabled for warehouse management.</span></span> <span data-ttu-id="63bcc-115">Stav uvolnění proto zůstává *Částečně uvolněno* v tomto scénáři.</span><span class="sxs-lookup"><span data-stu-id="63bcc-115">Therefore, the release status remains *Partially released* in this scenario.</span></span> <span data-ttu-id="63bcc-116">Společnost Microsoft vyhodnotila tento problém a zjistila, že jde o omezení funkcí.</span><span class="sxs-lookup"><span data-stu-id="63bcc-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="63bcc-117">Jako součást procesu dodacího listu a procesu fakturace bylo možné přidat rozšíření pro aktualizaci stavu uvolnění.</span><span class="sxs-lookup"><span data-stu-id="63bcc-117">An extension could be added as part of the packing slip and invoicing process to update the release status.</span></span>
