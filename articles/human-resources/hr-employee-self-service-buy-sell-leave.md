---
title: Koupit a prodat pracovní volno
description: V aplikaci Dynamics 365 Human Resources můžete odesílat žádosti o nákup a prodej pracovního volna na základě zásad nákupu a prodeje pracovního volna stanovených vaší společností.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d32abacc1539cb930ad6f1ebcfe6fa9af4befcf
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271472"
---
# <a name="buy-and-sell-leave"></a><span data-ttu-id="ebefd-103">Koupit a prodat pracovní volno</span><span class="sxs-lookup"><span data-stu-id="ebefd-103">Buy and sell leave</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ebefd-104">V aplikaci Dynamics 365 Human Resources můžete odesílat žádosti o nákup a prodej pracovního volna na základě zásad nákupu a prodeje pracovního volna stanovených vaší společností.</span><span class="sxs-lookup"><span data-stu-id="ebefd-104">In Dynamics 365 Human Resources, you can submit requests to buy and sell leave based on the buy and sell leave policies set up by your company.</span></span>  

## <a name="request-to-buy-leave"></a><span data-ttu-id="ebefd-105">Žádost o koupi volna</span><span class="sxs-lookup"><span data-stu-id="ebefd-105">Request to buy leave</span></span>

1. <span data-ttu-id="ebefd-106">V pracovním prostoru **Samoobsluha pro zaměstnance** vyberte **Žádost o koupi volna** v dlaždici **Zůstatky volna**.</span><span class="sxs-lookup"><span data-stu-id="ebefd-106">In the **Employee self service** workspace, select **Buy leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="ebefd-107">Přejte **Typ volna** a zadejte **Množství** volna, které chcete koupit.</span><span class="sxs-lookup"><span data-stu-id="ebefd-107">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to buy.</span></span> 

3. <span data-ttu-id="ebefd-108">Jakmile budete připravení žádost odeslat, vyberte **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="ebefd-108">Select **Submit** when you're ready to submit your request.</span></span> 

<span data-ttu-id="ebefd-109">Vaše zůstatky se před aktualizací buď automaticky aktualizují, nebo projdou schvalovacím procesem.</span><span class="sxs-lookup"><span data-stu-id="ebefd-109">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="ebefd-110">To záleží na tom, jak byla nakonfigurována zásada nákupu.</span><span class="sxs-lookup"><span data-stu-id="ebefd-110">This depends on how the buy policy has been configured.</span></span>

## <a name="request-to-sell-leave"></a><span data-ttu-id="ebefd-111">Žádost o prodej pracovního volna</span><span class="sxs-lookup"><span data-stu-id="ebefd-111">Request to sell leave</span></span>

1. <span data-ttu-id="ebefd-112">V pracovním prostoru **Samoobsluha pro zaměstnance** vyberte **Žádost o prodej pracovního volna** v dlaždici **Zůstatky volna**.</span><span class="sxs-lookup"><span data-stu-id="ebefd-112">In the **Employee self service** workspace, select **Sell leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="ebefd-113">Přejte **Typ pracovního volna** a zadejte **Množství** pracovního volna, které chcete prodat.</span><span class="sxs-lookup"><span data-stu-id="ebefd-113">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to sell.</span></span> 

3. <span data-ttu-id="ebefd-114">Jakmile budete připravení žádost odeslat, vyberte **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="ebefd-114">Select **Submit** when you're ready to submit your request.</span></span>

<span data-ttu-id="ebefd-115">Vaše zůstatky se před aktualizací buď automaticky aktualizují, nebo projdou schvalovacím procesem.</span><span class="sxs-lookup"><span data-stu-id="ebefd-115">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="ebefd-116">To záleží na tom, jak byla nakonfigurována zásada nákupu.</span><span class="sxs-lookup"><span data-stu-id="ebefd-116">This depends on how the buy policy has been configured.</span></span>


## <a name="troubleshooting"></a><span data-ttu-id="ebefd-117">Řešení potíží</span><span class="sxs-lookup"><span data-stu-id="ebefd-117">Troubleshooting</span></span> 

<span data-ttu-id="ebefd-118">Pokud pracovní postup požadavku na nákup nebo prodej volna selže, uživatelé s oprávněním **EssLeaveBuySellRequestApprover** mohou zkontrolovat protokol zpráv o všech požadavcích na nákup a prodej.</span><span class="sxs-lookup"><span data-stu-id="ebefd-118">If a buy or sell leave request workflow fails, users with the **EssLeaveBuySellRequestApprover** privilege can review the message log for all leave buy and sell requests.</span></span> <span data-ttu-id="ebefd-119">Chcete-li to provést, přejděte na **Pracovní volno a nepřítomnost > Odkaz > Žádosti o nákup a prodej volna > Protokol zpráv** (vlevo nahoře).</span><span class="sxs-lookup"><span data-stu-id="ebefd-119">To do this, go to **Leave and absence > Link > Buy and sell leave requests > Message log** (on the upper left).</span></span> <span data-ttu-id="ebefd-120">**Protokol zpráv** ukazuje uživatelům, jak byly transakce zpracovány, a související historii pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="ebefd-120">The **Message log** shows users how the transactions were processed and the associated workflow history.</span></span>


## <a name="see-also"></a><span data-ttu-id="ebefd-121">Viz také</span><span class="sxs-lookup"><span data-stu-id="ebefd-121">See also</span></span>

[<span data-ttu-id="ebefd-122">Přehled pracovního volna a absencí</span><span class="sxs-lookup"><span data-stu-id="ebefd-122">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="ebefd-123">Správa zásad nákupu a prodeje pracovního volna</span><span class="sxs-lookup"><span data-stu-id="ebefd-123">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
