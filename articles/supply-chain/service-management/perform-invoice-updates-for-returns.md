---
title: Provádění aktualizací faktur pro vrácení
description: Tato funkce aplikace  dále podporuje obchodní procesy organizací, které se rozhodly fakturovat vratky a prodejní objednávky najednou a stejnou osobou.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d60e29aec1ebdec939aaafc978ee4de04b96136
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983836"
---
# <a name="perform-invoice-updates-for-returns"></a><span data-ttu-id="a855c-103">Provádění aktualizací faktur pro vrácení</span><span class="sxs-lookup"><span data-stu-id="a855c-103">Perform invoice updates for returns</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a855c-104">Vratka je typem prodejní objednávky označeným jako Vrácená položka.</span><span class="sxs-lookup"><span data-stu-id="a855c-104">A return order is a type of sales order that is marked as a returned order.</span></span> <span data-ttu-id="a855c-105">Proto se stránka se seznamem **Všechny prodejní objednávky** používá ke generování faktur vratek namísto formuláře **Vratky** .</span><span class="sxs-lookup"><span data-stu-id="a855c-105">Therefore, the **All sales orders** list page is used to generate invoices for return orders instead of the **Return orders** form.</span></span> <span data-ttu-id="a855c-106">Tato funkce aplikace  dále podporuje obchodní procesy organizací, které se rozhodly fakturovat vratky a prodejní objednávky najednou a stejnou osobou.</span><span class="sxs-lookup"><span data-stu-id="a855c-106">This functionality supports the business processes of organizations that choose to have return orders and sales orders invoiced at the same time and by the same person.</span></span>

<span data-ttu-id="a855c-107">Vzhledem k tomu, že pro vrácenou položku obsahuje zápornou částku, jedná se o dobropis.</span><span class="sxs-lookup"><span data-stu-id="a855c-107">Because the invoice for a returned item is for a negative amount, it is called a credit note.</span></span>

<span data-ttu-id="a855c-108">Při nastavení aktualizace faktury pro dávkové zpracování musí prodejní objednávka typu **Vrácená položka** obsahovat stav řádku vrácenky **Přijato** , který indikuje, že byl aktualizován dodací list objednávky.</span><span class="sxs-lookup"><span data-stu-id="a855c-108">When you set up the invoice update for batch processing, the sales order of type **Returned order** must have a return line status of **Received** , which indicates that the order's packing slip has been updated.</span></span>

## <a name="post-an-invoice-for-a-return-order"></a><span data-ttu-id="a855c-109">Zaúčtujte fakturu pro objednávku vratky</span><span class="sxs-lookup"><span data-stu-id="a855c-109">Post an invoice for a return order</span></span>

1.  <span data-ttu-id="a855c-110">Klikněte na **Pohledávky** \> **Společné** \> **Prodejní objednávky** \> **všechny prodejní objednávky** .</span><span class="sxs-lookup"><span data-stu-id="a855c-110">Click **Accounts receivable** \> **Common** \> **Sales orders** \> **All sales orders** .</span></span>

2.  <span data-ttu-id="a855c-111">Vyberte prodejní objednávku, pro kterou se v poli **Typ objednávky** zobrazí **Vratka** .</span><span class="sxs-lookup"><span data-stu-id="a855c-111">Select a sales order for which **Returned order** is displayed in the **Order type** field.</span></span>

3.  <span data-ttu-id="a855c-112">V podokně akcí na kartě **Faktura** ve skupině **Generovat** klikněte na **Faktura** .</span><span class="sxs-lookup"><span data-stu-id="a855c-112">On the Action Pane, on the **Invoice** tab, in the **Generate** group, click **Invoice** .</span></span>

4.  <span data-ttu-id="a855c-113">Na kartě **Parametry** zaškrtněte políčko **Zaúčtování** .</span><span class="sxs-lookup"><span data-stu-id="a855c-113">On the **Parameters** tab, select the **Posting** check box.</span></span>

5.  <span data-ttu-id="a855c-114">Zkontrolujte informace ve formuláři a proveďte potřebné změny.</span><span class="sxs-lookup"><span data-stu-id="a855c-114">Review information in the form and make any changes that are needed.</span></span>

6.  <span data-ttu-id="a855c-115">Klikněte na tlačítko **OK** .</span><span class="sxs-lookup"><span data-stu-id="a855c-115">Click **OK** .</span></span> <span data-ttu-id="a855c-116">Zaúčtuje se dobropis.</span><span class="sxs-lookup"><span data-stu-id="a855c-116">The credit note is posted.</span></span>

## <a name="see-also"></a><span data-ttu-id="a855c-117">Viz také</span><span class="sxs-lookup"><span data-stu-id="a855c-117">See also</span></span>

[<span data-ttu-id="a855c-118">Aktualizace dodacího listu pro vrácení</span><span class="sxs-lookup"><span data-stu-id="a855c-118">Packing slip updates for returns</span></span>](packing-slip-updates-returns.md)

  


