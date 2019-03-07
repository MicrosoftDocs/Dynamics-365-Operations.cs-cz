---
title: Upgrade deníků jednoho dokladu a přecenění měny
description: Některé organizace zadávají deníky obsahující jeden doklad, který má více než jednoho odběratele nebo dodavatele, a rovněž spouští proces přecenění cizí měny pohledávek a závazků. Toto téma popisuje kroky, podle kterých by tyto organizace měly postupovat při upgradu na aplikaci Microsoft Dynamics 365 for Operations verze 1611.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 343fa226e1cf9072696082e9ebf0a1629e553ae9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "328141"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="317bf-104">Upgrade deníků jednoho dokladu a přecenění měny</span><span class="sxs-lookup"><span data-stu-id="317bf-104">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="317bf-105">Některé organizace zadávají deníky obsahující jeden doklad, který má více než jednoho odběratele nebo dodavatele, a rovněž spouští proces přecenění cizí měny pohledávek a závazků.</span><span class="sxs-lookup"><span data-stu-id="317bf-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="317bf-106">Toto téma popisuje kroky, podle kterých by tyto organizace měly postupovat při upgradu na aplikaci Microsoft Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="317bf-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="317bf-107">Tyto kroky použijte při upgradu na Microsoft Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="317bf-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="317bf-108">Před upgradem na aplikaci Dynamics 365 for Operations spusťte procesy přecenění cizí měny pro pohledávky a závazky.</span><span class="sxs-lookup"><span data-stu-id="317bf-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="317bf-109">Pole **Metoda** nastavte na **Datum faktury**.</span><span class="sxs-lookup"><span data-stu-id="317bf-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="317bf-110">Transakce přecenění je vytvořena, aby vrátila zpět poslední přecenění cizí měny.</span><span class="sxs-lookup"><span data-stu-id="317bf-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="317bf-111">Proto se otevřené transakce oceňují v jejich původní zúčtovací měně.</span><span class="sxs-lookup"><span data-stu-id="317bf-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="317bf-112">Upgradujte na Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="317bf-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="317bf-113">Spusťte znovu procesy přecenění cizí měny pohledávek a závazků</span><span class="sxs-lookup"><span data-stu-id="317bf-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="317bf-114">Tentokrát nastavte pole **Metoda** na **Standardní**.</span><span class="sxs-lookup"><span data-stu-id="317bf-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="317bf-115">Vytvoří se nová transakce přecenění, která je založena na aktuálních směnných kurzech.</span><span class="sxs-lookup"><span data-stu-id="317bf-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="317bf-116">Tato transakce zaznamená nerealizovaný zisk/ztrátu a správný součtový účet hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="317bf-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>




