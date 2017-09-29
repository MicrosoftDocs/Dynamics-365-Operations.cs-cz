---
title: "Upgrade týkající se jednoho dokladu a přecenění měny"
description: "Některé organizace zadávají deníky obsahující jeden doklad, který má více než jednoho odběratele nebo dodavatele, a rovněž spouští proces přecenění cizí měny pohledávek a závazků. Toto téma popisuje kroky, podle kterých by tyto organizace měly postupovat při upgradu na aplikaci Microsoft Dynamics 365 for Operations verze 1611."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 13ad43cc77731727525aae1edc4d405c166acbc1
ms.contentlocale: cs-cz
ms.lasthandoff: 07/18/2017

---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a><span data-ttu-id="9807f-104">Upgrade týkající se jednoho dokladu a přecenění měny</span><span class="sxs-lookup"><span data-stu-id="9807f-104">Single voucher and currency revaluation upgrade</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9807f-105">Některé organizace zadávají deníky obsahující jeden doklad, který má více než jednoho odběratele nebo dodavatele, a rovněž spouští proces přecenění cizí měny pohledávek a závazků.</span><span class="sxs-lookup"><span data-stu-id="9807f-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="9807f-106">Toto téma popisuje kroky, podle kterých by tyto organizace měly postupovat při upgradu na aplikaci Microsoft Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="9807f-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="9807f-107">Při upgradu na Microsoft Dynamics 365 for Operations verzi 1611 postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="9807f-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="9807f-108">Před upgradem na aplikaci Dynamics 365 for Operations spusťte procesy přecenění cizí měny pro pohledávky a závazky.</span><span class="sxs-lookup"><span data-stu-id="9807f-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="9807f-109">Pole **Metoda** nastavte na **Datum faktury**.</span><span class="sxs-lookup"><span data-stu-id="9807f-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="9807f-110">Transakce přecenění je vytvořena, aby vrátila zpět poslední přecenění cizí měny.</span><span class="sxs-lookup"><span data-stu-id="9807f-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="9807f-111">Proto se otevřené transakce oceňují v jejich původní zúčtovací měně.</span><span class="sxs-lookup"><span data-stu-id="9807f-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="9807f-112">Upgrade na Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="9807f-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="9807f-113">Spusťte znovu procesy přecenění cizí měny pohledávek a závazků</span><span class="sxs-lookup"><span data-stu-id="9807f-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="9807f-114">Tentokrát nastavte pole **Metoda** na **Standardní**.</span><span class="sxs-lookup"><span data-stu-id="9807f-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="9807f-115">Vytvoří se nová transakce přecenění, která je založena na aktuálních směnných kurzech.</span><span class="sxs-lookup"><span data-stu-id="9807f-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="9807f-116">Tato transakce zaznamená nerealizovaný zisk/ztrátu a správný součtový účet hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="9807f-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>





