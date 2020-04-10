---
title: Vytváření a export plateb dodavatelů s použitím formátu platby ISO20022
description: Tento postup ukazuje, jak vytvořit platební řádky pro platbu dodavateli v deníku, a generovat soubor pro platbu dodavateli pomocí příkladu převodu kreditu ISO2022.
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff8a2858bfa96eb1d4b0afa1e48ebd1b578a4431
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143117"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="a149f-103">Vytváření a export plateb dodavatelů s použitím formátu platby ISO20022</span><span class="sxs-lookup"><span data-stu-id="a149f-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a149f-104">Toto téma vysvětluje, jak vytvořit platební řádky pro platbu dodavateli v deníku, a generovat soubor pro platbu dodavateli pomocí příkladu převodu kreditu ISO2022.</span><span class="sxs-lookup"><span data-stu-id="a149f-104">This topic explains how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span>

<span data-ttu-id="a149f-105">Toto je pátý z pěti úkolů, které společně popisují proces platby dodavatele pomocí konfigurací elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="a149f-105">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="a149f-106">K dokončení tohoto příkladu použijte ukázková data DEMF.</span><span class="sxs-lookup"><span data-stu-id="a149f-106">Use the DEMF demo data to complete this example.</span></span>

## <a name="example"></a><span data-ttu-id="a149f-107">Příklad</span><span class="sxs-lookup"><span data-stu-id="a149f-107">Example</span></span>

1.    <span data-ttu-id="a149f-108">Přejděte na **Závazky > Platby > Deník plateb**.</span><span class="sxs-lookup"><span data-stu-id="a149f-108">Go to **Accounts payable > Payments > Payment journal**.</span></span>
2.    <span data-ttu-id="a149f-109">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="a149f-109">Click **New**.</span></span>
3.    <span data-ttu-id="a149f-110">V poli **Název** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a149f-110">In the **Name** field, enter or select a value.</span></span>
4.    <span data-ttu-id="a149f-111">Klikněte na **Řádky > Návrh platby -> Vytvořit návrh platby**.</span><span class="sxs-lookup"><span data-stu-id="a149f-111">Click **Lines > Payment proposal > Create payment proposal**.</span></span>
5.    <span data-ttu-id="a149f-112">Rozbalte oddíl **Záznamy k zahrnutí**.</span><span class="sxs-lookup"><span data-stu-id="a149f-112">Expand the **Records to include** section.</span></span>
6.    <span data-ttu-id="a149f-113">Klikněte na tlačítko **Filtr**.</span><span class="sxs-lookup"><span data-stu-id="a149f-113">Click **Filter**.</span></span>
7.    <span data-ttu-id="a149f-114">V seznamu vyberte řádek pro **tabulku dodavatelů** a pole **Účet dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="a149f-114">In the list, select the row for **Vendors table** and **Vendor account field**.</span></span>
8.    <span data-ttu-id="a149f-115">V poli **Kritéria** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a149f-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="a149f-116">Můžete použít všechna kritéria pro výběr transakcí dodavatele k zaplacení. Pro tento příklad použijte DE-001 jako účet dodavatele.</span><span class="sxs-lookup"><span data-stu-id="a149f-116">You can apply any criteria for selecting vendor transactions to pay, for this example, use DE-001 as a vendor account.</span></span>
12.    <span data-ttu-id="a149f-117">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="a149f-117">Click **OK**.</span></span>
13.    <span data-ttu-id="a149f-118">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="a149f-118">Click **OK**.</span></span>
14.    <span data-ttu-id="a149f-119">Klikněte na **Vytvořit platby**.</span><span class="sxs-lookup"><span data-stu-id="a149f-119">Click **Create payments**.</span></span>
15. <span data-ttu-id="a149f-120">Vygenerujte soubor platby ISO20022.</span><span class="sxs-lookup"><span data-stu-id="a149f-120">Generate an ISO20022 payment file.</span></span>
    1.    <span data-ttu-id="a149f-121">Klikněte na **Generovat platby**.</span><span class="sxs-lookup"><span data-stu-id="a149f-121">Click **Generate payments**.</span></span>
    2.    <span data-ttu-id="a149f-122">V poli **Metody platby** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a149f-122">In the **Method of payment** field, enter or select a value.</span></span>
    3.    <span data-ttu-id="a149f-123">Zadejte hodnotu do pole **Název souboru**.</span><span class="sxs-lookup"><span data-stu-id="a149f-123">In the **File name** field, type a value.</span></span> <span data-ttu-id="a149f-124">Z důvodu platby v EUR bude v tomto příkladu vygenerovaný soubor kompatibilní se SEPA.</span><span class="sxs-lookup"><span data-stu-id="a149f-124">For this example, because of the EUR payment, the generated file will be SEPA compliant.</span></span> <span data-ttu-id="a149f-125">Převod kreditu ISO20022, jakož i jiné formáty plateb dodavatelů, lze také použít k vytváření plateb v jiných měnách.</span><span class="sxs-lookup"><span data-stu-id="a149f-125">ISO20022 credit transfer as well as other vendor payment formats can also be used for generating payments in other currencies.</span></span>
    4.    <span data-ttu-id="a149f-126">V poli **Bankovní účet** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a149f-126">In the **Bank account** field, enter or select a value.</span></span>

