---
title: Potvrzení platebních kalendářů leasingu majetku v dávce
description: Toto téma vysvětluje, jak potvrdit více platebních kalendářů v dávce.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymConfirmationDetails
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: eaff604b92c412cd35c5c2aeadb2d9ed8dc77706
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881245"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a><span data-ttu-id="cf575-103">Potvrzení platebních kalendářů leasingu majetku v dávce</span><span class="sxs-lookup"><span data-stu-id="cf575-103">Confirm Asset leasing payment schedules in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf575-104">Toto téma vysvětluje, jak potvrdit více platebních kalendářů v dávce.</span><span class="sxs-lookup"><span data-stu-id="cf575-104">This topic explains how to confirm multiple payment schedules in a batch.</span></span> <span data-ttu-id="cf575-105">Platební kalendáře se potvrzují buď pro jednotlivé leasingy, nebo prostřednictvím dávkového zpracování.</span><span class="sxs-lookup"><span data-stu-id="cf575-105">Payment schedules are confirmed either on a lease-to-lease basis or through the confirmation batch process.</span></span> <span data-ttu-id="cf575-106">Položku deníku lze zaúčtovat pouze pro leasing, který má potvrzený platební kalendář.</span><span class="sxs-lookup"><span data-stu-id="cf575-106">A journal entry can be posted only against a lease that has a confirmed payment schedule.</span></span> <span data-ttu-id="cf575-107">Potvrzení platebního kalendáře slouží jako konečné schválení finančních informací o leasingu.</span><span class="sxs-lookup"><span data-stu-id="cf575-107">Confirmation of the payment schedule serves as a final approval of the financial information for the lease.</span></span> <span data-ttu-id="cf575-108">Všechny budoucí změny finančních informací o leasingu, jako jsou platby a doba leasingu, představují úpravu leasingu a měly by být zpracovány tímto způsobem.</span><span class="sxs-lookup"><span data-stu-id="cf575-108">All future changes to the financial information for the lease, such as payments and the lease term, constitute a lease adjustment and should be processed in that way.</span></span>

<span data-ttu-id="cf575-109">Chcete-li potvrdit více platebních kalendářů, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="cf575-109">To confirm multiple payment schedules, follow these steps.</span></span>

1. <span data-ttu-id="cf575-110">Jděte na **Leasing majetku \> Periodicky \> Potvrzení dávky**.</span><span class="sxs-lookup"><span data-stu-id="cf575-110">Go to **Asset leasing \> Periodic \> Confirmation batch**.</span></span>
2. <span data-ttu-id="cf575-111">Na stránce **Potvrzení dávky** vyberte **Potvrzení dávky**.</span><span class="sxs-lookup"><span data-stu-id="cf575-111">On the **Confirmation batch** page, select **Confirmation batch**.</span></span>
3. <span data-ttu-id="cf575-112">V zobrazeném dialogovém okně vyfiltrujte knihy, které chcete potvrdit.</span><span class="sxs-lookup"><span data-stu-id="cf575-112">In the dialog box that appears, filter for the books that you want to confirm.</span></span>

    - <span data-ttu-id="cf575-113">Chcete-li potvrdit všechny knihy v konkrétní skupině leasingu, vyberte skupinu v poli **Skupina leasingu**.</span><span class="sxs-lookup"><span data-stu-id="cf575-113">To confirm all the books in a specific lease group, select the group in the **Lease group** field.</span></span>
    - <span data-ttu-id="cf575-114">Chcete-li potvrdit konkrétní knihy, vyberte knihy v poli **ID knihy**.</span><span class="sxs-lookup"><span data-stu-id="cf575-114">To confirm specific books, select the books in the **Book ID** field.</span></span>
    - <span data-ttu-id="cf575-115">Chcete-li potvrdit všechny knihy, zapněte parametr **Pro všechny knihy**.</span><span class="sxs-lookup"><span data-stu-id="cf575-115">To confirm all books, turn on the **For all books** parameter.</span></span>

<span data-ttu-id="cf575-116">Informace o nově potvrzených knihách jsou uvedeny na stránce **Potvrzené knihy**.</span><span class="sxs-lookup"><span data-stu-id="cf575-116">Information for the newly confirmed books is shown on the **Confirmed books** page.</span></span> <span data-ttu-id="cf575-117">Po potvrzení platebních kalendářů je možné zaúčtovat položky deníku počátečního uznání pro leasingy.</span><span class="sxs-lookup"><span data-stu-id="cf575-117">After the payment schedules are confirmed, the initial recognition journal entries can be posted against the leases.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
