---
title: Přeřazení krátkodobé části leasingového závazku
description: Toto téma vysvětluje, jak vytvořit měsíční zápis do deníku k reklasifikaci části závazku z leasingu jako krátkodobého.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 46bcd396c93bc1d2944241165d438f8ccc013e20
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441350"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a><span data-ttu-id="a685c-103">Přeřazení krátkodobé části leasingového závazku</span><span class="sxs-lookup"><span data-stu-id="a685c-103">Reclassify the short-term portion of lease liability</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a685c-104">Toto téma vysvětluje, jak vytvořit měsíční zápis do deníku k reklasifikaci části závazku z leasingu jako krátkodobého.</span><span class="sxs-lookup"><span data-stu-id="a685c-104">This topic explains how to create a monthly journal entry to reclassify a portion of the lease liability as short-term.</span></span> <span data-ttu-id="a685c-105">Když je plán, který je vybrán v dávkovém procesu, **Přeřazení závazků z krátkodobého pronájmu**, je vytvořena položka deníku.</span><span class="sxs-lookup"><span data-stu-id="a685c-105">When the schedule that is selected in the batch process is **Short-term lease liability reclass**, a journal entry is created.</span></span> <span data-ttu-id="a685c-106">Tato položka se používá k zaúčtování aktuální části závazku z leasingu k poslednímu dni měsíce.</span><span class="sxs-lookup"><span data-stu-id="a685c-106">This entry is used to post the current portion of the lease liability on the last day of the month.</span></span> <span data-ttu-id="a685c-107">Současně je zaúčtována položka storna od prvního dne následujícího měsíce.</span><span class="sxs-lookup"><span data-stu-id="a685c-107">At the same time, a reversal entry is posted as of the first day of the next month.</span></span>

<span data-ttu-id="a685c-108">Krátkodobá část závazku z leasingu je uvedena v plánu amortizace závazků.</span><span class="sxs-lookup"><span data-stu-id="a685c-108">The short-term portion of the lease liability is shown on the liability amortization schedule.</span></span> <span data-ttu-id="a685c-109">Když je zaúčtována položka deníku, bude k dispozici sloupec **Vytvořen deník reklasifikace odpovědnosti** a v plánu se vyplní také ID deníku.</span><span class="sxs-lookup"><span data-stu-id="a685c-109">When the journal entry is posted, the **Liability reclass journal created** column becomes available, and the journal ID is also filled in on the schedule.</span></span>

<span data-ttu-id="a685c-110">Chcete-li vytvořit a zaúčtovat záznam deníku reklasifikace krátkodobých závazků, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="a685c-110">To create and post the short-term liability reclassification journal entry, follow these steps.</span></span>

1. <span data-ttu-id="a685c-111">Jděte na **Leasing majetku \> Periodicky \> Vytvoření dávkového deníku**.</span><span class="sxs-lookup"><span data-stu-id="a685c-111">Go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span>
2. <span data-ttu-id="a685c-112">V dialogovém okně **Dávkové vytvoření deníku** v poli **Vybrat plán** vyberte **Přeřazení závazků z krátkodobého pronájmu**.</span><span class="sxs-lookup"><span data-stu-id="a685c-112">In the **Batch journal creation** dialog box, in the **Select schedule** field, select **Short-term lease liability reclass**.</span></span>
3. <span data-ttu-id="a685c-113">V poli **Leasingová skupina** vyberte leasingovou skupinu.</span><span class="sxs-lookup"><span data-stu-id="a685c-113">In the **Lease group** field, select a lease group.</span></span> <span data-ttu-id="a685c-114">Případně v poli **ID knihy** vyberte ID knihy.</span><span class="sxs-lookup"><span data-stu-id="a685c-114">Alternatively, in the **Book ID** field, select the book ID.</span></span>
4. <span data-ttu-id="a685c-115">Zapněte parametr **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="a685c-115">Turn on the **Post** parameter.</span></span> <span data-ttu-id="a685c-116">Případně, pokud by měl být záznam vytvořen, ale ne zaúčtován, ponechte tento parametr vypnutý.</span><span class="sxs-lookup"><span data-stu-id="a685c-116">Alternatively, if the entry should be created but not posted, leave this parameter turned off.</span></span>
5. <span data-ttu-id="a685c-117">Zapněte parametr **Náhled před zveřejněním** k zobrazení záznamu před jeho zaúčtováním.</span><span class="sxs-lookup"><span data-stu-id="a685c-117">Turn on the **Preview before posting** parameter to view the entry before it's posted.</span></span>
6. <span data-ttu-id="a685c-118">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="a685c-118">Select **OK**.</span></span>