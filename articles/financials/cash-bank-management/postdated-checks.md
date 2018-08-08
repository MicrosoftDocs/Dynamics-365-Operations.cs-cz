---
title: "Postdatované šeky"
description: "Tento článek obsahuje informace o podpoře pro postdatované šeky v aplikaci Microsoft Dynamics 365 for Finance and Operations. Postdatované šeky jsou šeky, které jsou vydány za účelem provedení a přijetí platby v budoucí datu. Takže lze šek proplatit až od určeného data."
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPostDatedChecks, CustPostDatedChecks
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 7ea1cd9926f3ea55d82f9030372a15b3545ed824
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---

# <a name="postdated-checks"></a><span data-ttu-id="f396c-105">Postdatované šeky</span><span class="sxs-lookup"><span data-stu-id="f396c-105">Postdated checks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f396c-106">Tento článek obsahuje informace o podpoře pro postdatované šeky v aplikaci Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f396c-106">This article provides information about support for postdated checks in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="f396c-107">Postdatované šeky jsou šeky, které jsou vydány za účelem provedení a přijetí platby v budoucí datu.</span><span class="sxs-lookup"><span data-stu-id="f396c-107">Postdated checks are checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="f396c-108">Takže lze šek proplatit až od určeného data.</span><span class="sxs-lookup"><span data-stu-id="f396c-108">Therefore, the check can't be cashed until the specified date.</span></span>

<span data-ttu-id="f396c-109">Microsoft Dynamics 365 for Finance and Operations podporuje úplné řízení cyklu postdatovaných šeků v pohledávkách i závazcích, jak znázorňuje následující tabulka.</span><span class="sxs-lookup"><span data-stu-id="f396c-109">Microsoft Dynamics 365 for Finance and Operations supports the full management cycle for postdated checks in both Accounts receivable and Accounts payable, as shown in the following table.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f396c-110">Scénář</span><span class="sxs-lookup"><span data-stu-id="f396c-110">Scenario</span></span></th>
<th><span data-ttu-id="f396c-111">Podrobnosti</span><span class="sxs-lookup"><span data-stu-id="f396c-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f396c-112">Nastavení postdatovaných šeků</span><span class="sxs-lookup"><span data-stu-id="f396c-112">Set up postdated checks</span></span></td>
<td><span data-ttu-id="f396c-113">Musíte nastavit novou metodu platby a zadat platební postup pro clearingové účty pro vydané šeky, přijaté šeky a srážkovou daň.</span><span class="sxs-lookup"><span data-stu-id="f396c-113">You must set up a new payment method, and specify the payment routine for clearing accounts for issued checks, received checks, and withholding tax.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f396c-114">Registrace a účtování postdatovaného šeku pro dodavatele</span><span class="sxs-lookup"><span data-stu-id="f396c-114">Register and post a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="f396c-115">Zaregistrujte podrobnosti postdatovaného šeku, který vydáte dodavateli.</span><span class="sxs-lookup"><span data-stu-id="f396c-115">Register the details of a postdated check that you issue to a vendor.</span></span> <span data-ttu-id="f396c-116">Při zaúčtování platby je uznán pasiv dodavatele, avšak bankovní účet není dosud Dal.</span><span class="sxs-lookup"><span data-stu-id="f396c-116">When the payment is posted, the vendor liability is recognized, but the bank account isn’t yet credit.</span></span> <span data-ttu-id="f396c-117">Místo toho se pro tento účel používá clearingový účet.</span><span class="sxs-lookup"><span data-stu-id="f396c-117">Instead, a clearing account is used for this purpose.</span></span> </td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f396c-118">Registrace a zaúčtování postdatovaného šeku pro odběratele</span><span class="sxs-lookup"><span data-stu-id="f396c-118">Register and post a postdated check for a customer</span></span></td>
<td><span data-ttu-id="f396c-119">Zaregistruje podrobnosti postdatovaného šeku přijatého od odběratele.</span><span class="sxs-lookup"><span data-stu-id="f396c-119">Register the details of a postdated check that you receive from a customer.</span></span> <span data-ttu-id="f396c-120">Při zaúčtování platby je pohledávka odběratele Dal, avšak bankovní účet není ještě Má dáti.</span><span class="sxs-lookup"><span data-stu-id="f396c-120">When the payment is posted, the customer receivable is credit, but the bank account isn’t yet debit.</span></span> <span data-ttu-id="f396c-121">Místo toho se pro tento účel používá clearingový účet.</span><span class="sxs-lookup"><span data-stu-id="f396c-121">Instead, a clearing account is used for this purpose.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f396c-122">Zaregistruje a zaúčtujte náhradní postdatovaný šek pro odběratele nebo dodavatele.</span><span class="sxs-lookup"><span data-stu-id="f396c-122">Register and post a replacement postdated check for a customer or a vendor</span></span></td>
<td>
<span data-ttu-id="f396c-123">V případě ztráty nebo poškození původního šeku pro dodavatele nebo od odběratele můžete vydat náhradní postdatovaný šek.</span><span class="sxs-lookup"><span data-stu-id="f396c-123">If your original check to a vendor or from a customer is lost or damaged, you can issue a replacement postdated check.</span></span> <span data-ttu-id="f396c-124">Při registraci detailů šeku zadejte odkaz na původní šek a označte, že nový šek je náhrada za původní.</span><span class="sxs-lookup"><span data-stu-id="f396c-124">When you register the check details, provide a reference to the original check, and indicate that the new check is a replacement for the original.</span></span> <span data-ttu-id="f396c-125">Náhradní šek můžete také zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="f396c-125">You can also post the replacement check.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f396c-126">Přenos postdatovaného šeku odběratele na dodavatele</span><span class="sxs-lookup"><span data-stu-id="f396c-126">Transfer a customer postdated check to a vendor</span></span></td>
<td><span data-ttu-id="f396c-127">Když od odběratele obdržíte postdatovaný šek, můžete přenést tento šek na dodavatele jako platbu.</span><span class="sxs-lookup"><span data-stu-id="f396c-127">When you receive a postdated check from a customer, you can transfer that check to a vendor as a payment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f396c-128">Vyrovnání postdatovaných šeků pro odběratele nebo dodavatele</span><span class="sxs-lookup"><span data-stu-id="f396c-128">Settle a postdated check for a customer or a vendor</span></span></td>
<td><span data-ttu-id="f396c-129">Vyrovnejte postdatovaný šek, který je zaúčtován na překlenovací účet odběratele nebo dodavatele, když je šek již splatný.</span><span class="sxs-lookup"><span data-stu-id="f396c-129">Settle a postdated check that is posted to a bridging account for a customer or a vendor when the check finally matures.</span></span> <span data-ttu-id="f396c-130">Při vyrovnání šeku je banka již Má dáti nebo Dal s ohledem na clearingový účet, který byl použit dříve.</span><span class="sxs-lookup"><span data-stu-id="f396c-130">When the check is settled, the bank is finally debit or credit against the clearing account that was used earlier.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f396c-131">Zrušení postdatovaného šeku pro dodavatele</span><span class="sxs-lookup"><span data-stu-id="f396c-131">Cancel a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="f396c-132">Zaúčtovaný postdatovaný šek v těchto situacích můžete zrušit - šek je vrácen bankou.</span><span class="sxs-lookup"><span data-stu-id="f396c-132">You can cancel a posted postdated check in these situations: - The check is returned by the bank.</span></span>
<span data-ttu-id="f396c-133">- Šek je použit k nesprávné faktuře.</span><span class="sxs-lookup"><span data-stu-id="f396c-133">- The check is applied to an incorrect invoice.</span></span>
<span data-ttu-id="f396c-134">- Proti šeku je provedena hotovostní platba.</span><span class="sxs-lookup"><span data-stu-id="f396c-134">- A cash payment is made against the check.</span></span>
  </td>
  </tr>
  <tr class="even">
  <td><span data-ttu-id="f396c-135">Zastavte platbu postdatovaného šeku.</span><span class="sxs-lookup"><span data-stu-id="f396c-135">Stop payment for a postdated check</span></span></td>
  <td><span data-ttu-id="f396c-136">Můžete zastavit platbu na postdatovaném šeku vystaveném dodavateli z důvodů, jako je nedostatek finančních prostředků, změna podmínek smlouvy s dodavatelem, vadné zboží u dodavatele, dodání nebo vrácení zboží dodavateli.</span><span class="sxs-lookup"><span data-stu-id="f396c-136">You can stop payment on a postdated check that was issued to a vendor, for reasons such as not sufficient funds, changes in the terms of the agreement with the vendor, supply of defective goods by the vendor, or return of goods to the vendor.</span></span> <span data-ttu-id="f396c-137">Můžete zastavit platbu pouze u šeků, které nebyly proplaceny.</span><span class="sxs-lookup"><span data-stu-id="f396c-137">You can stop payment only on checks that haven’t cleared.</span></span></td>
  </tr>
  </tbody>
  </table>



<span data-ttu-id="f396c-138">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="f396c-138">For more information, see the following topics:</span></span>

[<span data-ttu-id="f396c-139">Nastavení postdatovaných šeků</span><span class="sxs-lookup"><span data-stu-id="f396c-139">Set up postdated checks</span></span>](tasks/set-up-postdated-checks.md)

[<span data-ttu-id="f396c-140">Registrace a zaúčtování postdatovaného šeku pro odběratele</span><span class="sxs-lookup"><span data-stu-id="f396c-140">Register and post a postdated check for a customer</span></span>](tasks/register-post-postdated-check-customer.md)

[<span data-ttu-id="f396c-141">Vyrovnání postdatovaného šeku od odběratele</span><span class="sxs-lookup"><span data-stu-id="f396c-141">Settle a postdated check from a customer</span></span>](tasks/settle-postdated-check-customer.md)

[<span data-ttu-id="f396c-142">Registrace a zaúčtování postdatovaného šeku pro dodavatele</span><span class="sxs-lookup"><span data-stu-id="f396c-142">Register and post a postdated check for a vendor</span></span>](tasks/register-post-postdated-check-vendor.md) 

[<span data-ttu-id="f396c-143">Vyrovnání postdatovaného šeku pro dodavatele</span><span class="sxs-lookup"><span data-stu-id="f396c-143">Settle a postdated check for a vendor</span></span>](tasks/settle-postdated-check-vendor.md)




