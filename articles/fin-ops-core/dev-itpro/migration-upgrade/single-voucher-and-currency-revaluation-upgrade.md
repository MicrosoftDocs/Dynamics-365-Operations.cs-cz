---
title: Upgrade deníků jednoho dokladu a přecenění měny
description: Toto téma popisuje, jak postupovat při upgradu deníků jednoho dokladu a přecenění měny.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6b66b969d13cff7f1f39fb644f459aa92bea198f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743914"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="f0c77-103">Upgrade deníků jednoho dokladu a přecenění měny</span><span class="sxs-lookup"><span data-stu-id="f0c77-103">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0c77-104">Některé organizace zadávají deníky obsahující jeden doklad, který má více než jednoho odběratele nebo dodavatele, a rovněž spouští proces přecenění cizí měny pohledávek a závazků.</span><span class="sxs-lookup"><span data-stu-id="f0c77-104">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="f0c77-105">Toto téma popisuje kroky, podle kterých by tyto organizace měly postupovat při upgradu na aplikaci Microsoft Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="f0c77-105">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="f0c77-106">Tyto kroky použijte při upgradu na Microsoft Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="f0c77-106">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="f0c77-107">Před upgradem na aplikaci Finance and Operations spusťte procesy přecenění cizí měny pro pohledávky a závazky.</span><span class="sxs-lookup"><span data-stu-id="f0c77-107">Before you upgrade to Finance and Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="f0c77-108">Pole **Metoda** nastavte na **Datum faktury**.</span><span class="sxs-lookup"><span data-stu-id="f0c77-108">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="f0c77-109">Transakce přecenění je vytvořena, aby vrátila zpět poslední přecenění cizí měny.</span><span class="sxs-lookup"><span data-stu-id="f0c77-109">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="f0c77-110">Proto se otevřené transakce oceňují v jejich původní zúčtovací měně.</span><span class="sxs-lookup"><span data-stu-id="f0c77-110">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="f0c77-111">Upgrade na verzi 1611.</span><span class="sxs-lookup"><span data-stu-id="f0c77-111">Upgrade to version 1611.</span></span>
3.  <span data-ttu-id="f0c77-112">Spusťte znovu procesy přecenění cizí měny pohledávek a závazků</span><span class="sxs-lookup"><span data-stu-id="f0c77-112">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="f0c77-113">Tentokrát nastavte pole **Metoda** na **Standardní**.</span><span class="sxs-lookup"><span data-stu-id="f0c77-113">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="f0c77-114">Vytvoří se nová transakce přecenění, která je založena na aktuálních směnných kurzech.</span><span class="sxs-lookup"><span data-stu-id="f0c77-114">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="f0c77-115">Tato transakce zaznamená nerealizovaný zisk/ztrátu a správný součtový účet hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="f0c77-115">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]