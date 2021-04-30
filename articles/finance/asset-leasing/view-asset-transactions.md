---
title: Zobrazení transakcí závazků, majetku a nákladů
description: Toto téma vysvětluje, jak zobrazit transakce s pronajatým majetkem. Tyto transakce zahrnují transakce odpovědnosti za leasing a transakce prováděcích výdajů, které byly zaúčtovány.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 55b8019db6abdb3bd5ecdb6eadc4f7443f2bf071
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881631"
---
# <a name="view-liability-asset-and-expense-transactions"></a><span data-ttu-id="1ccdb-104">Zobrazení transakcí závazků, majetku a nákladů</span><span class="sxs-lookup"><span data-stu-id="1ccdb-104">View liability, asset, and expense transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ccdb-105">Toto téma vysvětluje, jak zobrazit transakce s pronajatým majetkem.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-105">This topic explains how to view transactions for a leased asset.</span></span> <span data-ttu-id="1ccdb-106">Tyto transakce zahrnují transakce odpovědnosti za leasing a transakce prováděcích výdajů, které byly zaúčtovány.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-106">These transactions include lease liability transactions and executory expense transactions that have been posted.</span></span> <span data-ttu-id="1ccdb-107">Účetní hodnoty závazku a používaného majetku jsou použity v několika zprávách.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-107">The carrying values of the liability and right-of-use (ROU) asset are used on several reports.</span></span> <span data-ttu-id="1ccdb-108">Používají se také k výpočtu hodnot vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-108">They are also used to calculate adjustment values.</span></span>

## <a name="liability-transactions"></a><span data-ttu-id="1ccdb-109">Transakce pasiv</span><span class="sxs-lookup"><span data-stu-id="1ccdb-109">Liability transactions</span></span>

<span data-ttu-id="1ccdb-110">Chcete-li zobrazit transakce odpovědnosti za leasing, vyberte leasing na stránce **Souhrn pronájmu** a poté vyberte **Knihy** k otevření knih, které jsou připojeny k záznamu o leasingu.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-110">To view the lease liability transactions, select a lease on the **Lease summary** page, and then select **Books** to open the books that are attached to the lease record.</span></span> <span data-ttu-id="1ccdb-111">Po počátečním uznání byla zaúčtována faktura nebo deník úroků, vyberte **Transakce závazku**.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-111">After an initial recognition, an invoice, or an interest journal has been posted, select **Liability transactions**.</span></span>

<span data-ttu-id="1ccdb-112">Stránka **Odpovědnost za transakce** zobrazuje transakce, které zvyšují nebo snižují odpovědnost za leasing.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-112">The **Liability transactions** page shows the transactions that either increase or decrease the lease liability.</span></span> <span data-ttu-id="1ccdb-113">Záporné částky na této stránce představují kreditní transakce ve standardní aplikaci.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-113">Negative amounts on this page represent credit transactions in the standard application.</span></span> <span data-ttu-id="1ccdb-114">Případné úroky se zobrazují jako záporné hodnoty a zvyšují celkový závazek z leasingu.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-114">Any interest accruals are shown as negative values and increase the total lease liability.</span></span> <span data-ttu-id="1ccdb-115">Jakékoli úpravy leasingu se zobrazují jako kladné nebo záporné hodnoty v závislosti na povaze a dopadu knihy leasingu.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-115">Any lease adjustments are shown as positive or negative values, depending on the nature and impact of the lease book.</span></span> <span data-ttu-id="1ccdb-116">Aktuální čistý celkový zůstatek leasingového závazku pro vybraný leasing je uveden v levé dolní části stránky.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-116">The current net total balance of the lease liability for the selected lease is shown at the bottom left of the page.</span></span>

## <a name="asset-transactions"></a><span data-ttu-id="1ccdb-117">Transakce majetku</span><span class="sxs-lookup"><span data-stu-id="1ccdb-117">Asset transactions</span></span>

<span data-ttu-id="1ccdb-118">Chcete-li zobrazit majetkové leasingové transakce, vyberte leasing na stránce **Souhrn pronájmu** a poté vyberte **Knihy** k otevření leasingových knih, které jsou připojeny k záznamu o leasingu.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-118">To view the lease asset transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="1ccdb-119">Pak vyberte **Majetkové transakce**.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-119">Then select **Asset transactions**.</span></span>

<span data-ttu-id="1ccdb-120">Na stránce **Majetkové transakce** se zobrazují transakce, které buď zvyšují nebo snižují majetek na leasing a účty akumulovaných odpisů.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-120">The **Asset transaction** page shows the transactions that either increase or decrease the lease asset and accumulated depreciation accounts.</span></span> <span data-ttu-id="1ccdb-121">Debety se zobrazují jako kladné hodnoty a kredity se zobrazují jako záporné hodnoty, jako na stránce **Odpovědnost za transakce**.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-121">Debits are shown as positive values, and credits are shown as negative values, as on the **Liability transactions** page.</span></span> <span data-ttu-id="1ccdb-122">Zaúčtované počáteční uznání a další akumulované odpisy jsou zobrazeny v levém dolním rohu stránky jako zůstatek aktiv.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-122">The posted initial recognition and the next of accumulated depreciation are shown at the bottom left of the page as the asset balance.</span></span> 

## <a name="expenses-transactions"></a><span data-ttu-id="1ccdb-123">Výdajové transakce</span><span class="sxs-lookup"><span data-stu-id="1ccdb-123">Expenses transactions</span></span>

<span data-ttu-id="1ccdb-124">Chcete-li zobrazit výdajové leasingové transakce, vyberte leasing na stránce **Souhrn pronájmu** a poté vyberte **Knihy** k otevření leasingových knih, které jsou připojeny k záznamu o leasingu.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-124">To view the lease expense transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="1ccdb-125">Pak vyberte **Výdajové transakce**.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-125">Then select **Expense transactions**.</span></span>

<span data-ttu-id="1ccdb-126">Na stránce **Výdajové transakce** se zobrazují všechny výdaje, které byly zaúčtovány oproti leasingu, jako jsou úrokové náklady, výdaje na odpisy a jakékoli zachraňovací náklady.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-126">The **Expense transactions** page shows all the expenses that have been posted against the lease, such as interest expenses, depreciation expenses, and any executory costs.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
