---
title: "Účty pro zaúčtování likvidace dlouhodobého majetku"
description: "V tomto článku je vysvětleno nastavení účtů pro zaúčtování do hlavní knihy pro účely vyřazení majetku."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 0129eae177d44100b09c2b7bce553dd5bde5ce0c
ms.contentlocale: cs-cz
ms.lasthandoff: 06/29/2017


---

# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="2ec04-103">Účty pro zaúčtování likvidace dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="2ec04-103">Fixed asset disposal posting accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2ec04-104">V tomto článku je vysvětleno nastavení účtů pro zaúčtování do hlavní knihy pro účely vyřazení majetku.</span><span class="sxs-lookup"><span data-stu-id="2ec04-104">This article explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="2ec04-105">Na stránce Účetní profily dlouhodobého majetku na pevné záložce Účty hlavní knihy výběrem Vyřazení – prodej a Vyřazení – likvidace nastavte zaúčtování do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="2ec04-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="2ec04-106">U obou typů transakcí je účet hlavní knihy pro hodnotu vyřazení dlouhodobého majetku zaúčtován na stranu Dal.</span><span class="sxs-lookup"><span data-stu-id="2ec04-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="2ec04-107">Částka MD je zaúčtována na protiúčet, který může být například bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="2ec04-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="2ec04-108">Byl-li dlouhodobý majetek prodán zákazníkovi, použije se místo protiúčtu účet zákazníka.</span><span class="sxs-lookup"><span data-stu-id="2ec04-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="2ec04-109">Klepněte na tlačítko Vyřazení a poté klepněte na Prodej nebo Likvidace a poté nastavte podrobné účty pro vrácení zůstatkové účetní hodnoty dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="2ec04-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="2ec04-110">Také můžete zadat informace v polích Zaúčtovat hodnotu a Hodnota prodeje na stránce Parametry vyřazení.</span><span class="sxs-lookup"><span data-stu-id="2ec04-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="2ec04-111">Transakce vyřazení pro položku dlouhodobého majetku ve fondu majetku s nízkou hodnotou snižuje čistou účetní hodnotu fondu majetku s nízkou hodnotou pouze o vyřazenou částku.</span><span class="sxs-lookup"><span data-stu-id="2ec04-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="2ec04-112">Pokud je však hodnota prodeje položky majetku vyšší než čistá účetní hodnota fondu majetku s nízkou hodnotou, je hodnota fondu majetku s nízkou hodnotou snížena na nulovou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2ec04-112">However, when the sale of an asset is exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>






