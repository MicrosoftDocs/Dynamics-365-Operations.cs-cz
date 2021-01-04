---
title: Položky deníku úprav po přechodu v leasingu majetku
description: Toto téma popisuje funkce, které vám umožní přechod portfolia leasingu na nové účetní standardy leasingu, téma Kodifikace účetních standardů 842 (ASC 842) a mezinárodní standard pro finanční výkaznictví 16 (IFRS 16).
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
ms.openlocfilehash: 4af7b9dc7a03a6d17ff34ffc726eb87e848dd785
ms.sourcegitcommit: f0f5545a8ff99583e0131f435d91c64bb68a1c38
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/30/2020
ms.locfileid: "4441372"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a><span data-ttu-id="8f815-103">Položky deníku úprav po přechodu v leasingu majetku</span><span class="sxs-lookup"><span data-stu-id="8f815-103">Post transition adjustment journal entries in Asset leasing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f815-104">Toto téma popisuje funkce, které vám umožňují přechod portfolia leasingu na nové účetní standardy leasingu: téma Kodifikace účetních standardů 842 (ASC 842), což je standard v Obecně přijímaných účetních zásadách v USA (US GAAP) a Mezinárodní finanční výkaznictví Standard 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="8f815-104">This topic describes the functionality that lets you transition a lease portfolio to the new lease accounting standards: Accounting Standards Codification Topic 842 (ASC 842), which is the standard in Generally Accepted Accounting Principles in the US (US GAAP), and International Financial Reporting Standard 16 (IFRS 16).</span></span>

<span data-ttu-id="8f815-105">Informace o tom, jak nastavit knihu pro přechod na nové standardy, viz [Nastavit knihy leasingu](set-up-lease-books.md).</span><span class="sxs-lookup"><span data-stu-id="8f815-105">For information about how to set up a book for the transition to the new standards, see [Set up lease books](set-up-lease-books.md).</span></span>

<span data-ttu-id="8f815-106">Když vytvoříte položku deníku úpravy přechodu, vygeneruje se položka deníku.</span><span class="sxs-lookup"><span data-stu-id="8f815-106">When you create a transition adjustment journal entry, a journal entry is generated.</span></span> <span data-ttu-id="8f815-107">Tato položka odráží dopad rozvahy na záznam leasingu podle nových standardů k uvedenému datu.</span><span class="sxs-lookup"><span data-stu-id="8f815-107">This entry reflects the balance sheet impact of recording the lease under the new standards on that date.</span></span> <span data-ttu-id="8f815-108">Příslušný účet aktiv je debetován zůstatkovou hodnotou k danému dni a účet pasiv je kreditován.</span><span class="sxs-lookup"><span data-stu-id="8f815-108">The appropriate asset account is debited for the carrying amount on that date, and the liability account is credited.</span></span> <span data-ttu-id="8f815-109">Rozdíl se odečte nebo připíše k pozdrženým příjmům.</span><span class="sxs-lookup"><span data-stu-id="8f815-109">The difference is either debited or credited to retained earnings.</span></span>

<span data-ttu-id="8f815-110">Chcete-li zaúčtovat vyrovnání přechodu v souladu s novými účetními standardy, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="8f815-110">To post a transition adjustment in compliance with the new accounting standards, follow these steps.</span></span>

1. <span data-ttu-id="8f815-111">Na stránce **Shrnutí leasingu** vyberte leasing a poté vyberte **Knihy**.</span><span class="sxs-lookup"><span data-stu-id="8f815-111">On the **Lease summary** page, select the lease, and then select **Books**.</span></span>
2. <span data-ttu-id="8f815-112">V knize vyberte **Splátkový kalendář**.</span><span class="sxs-lookup"><span data-stu-id="8f815-112">In the book, select **Payment schedule**.</span></span>
3. <span data-ttu-id="8f815-113">V dialogovém okně **Splátkový kalendář** vyberte **Potvrdit**.</span><span class="sxs-lookup"><span data-stu-id="8f815-113">In the **Payment schedule** dialog box, select **Confirm**.</span></span> <span data-ttu-id="8f815-114">Pak zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="8f815-114">Then close the dialog box.</span></span>
4. <span data-ttu-id="8f815-115">Vyberte **Vyrovnání přechodu**.</span><span class="sxs-lookup"><span data-stu-id="8f815-115">Select **Transition adjustment**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8f815-116">Vyrovnání přechodu lze vytvořit pouze pro knihy leasingu, které jsou přiřazeny ke knize, kde je pole **Kniha přechodů** k dispozici.</span><span class="sxs-lookup"><span data-stu-id="8f815-116">A transition adjustment can be created only for lease books that are assigned to a book where the **Transition book** field is available.</span></span> <span data-ttu-id="8f815-117">Pokud je hodnota v poli **Zahájení leasingu** pozdější než datum přechodu, hodnota v poli **Vyrovnání přechodu** nebude aktualizována.</span><span class="sxs-lookup"><span data-stu-id="8f815-117">If the value in the **Lease commencement** field is later than the transition date, the value in the **Transition adjustment** field won't be updated.</span></span>

5. <span data-ttu-id="8f815-118">Chcete-li zobrazit položku deníku, vyberte **Deníky leasingu majetku**.</span><span class="sxs-lookup"><span data-stu-id="8f815-118">To view the journal entry, select **Asset leasing journals**.</span></span>
6. <span data-ttu-id="8f815-119">Vyberte nový deník a pak vyberte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="8f815-119">Select the new journal, and then select **Post**.</span></span>
