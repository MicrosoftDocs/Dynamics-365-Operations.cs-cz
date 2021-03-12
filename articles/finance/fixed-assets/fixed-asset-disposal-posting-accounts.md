---
title: Účty zaúčtování dlouhodobého majetku
description: Toto téma vysvětluje nastavení účtů pro zaúčtování do hlavní knihy pro účely vyřazení majetku.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d9c386b5da90918226e8b1a224bf628c65702b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988995"
---
# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="e9367-103">Účty zaúčtování dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="e9367-103">Fixed asset disposal posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9367-104">Toto téma vysvětluje nastavení účtů pro zaúčtování do hlavní knihy pro účely vyřazení majetku.</span><span class="sxs-lookup"><span data-stu-id="e9367-104">This topic explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="e9367-105">Na stránce Účetní profily dlouhodobého majetku na pevné záložce Účty hlavní knihy výběrem Vyřazení – prodej a Vyřazení – likvidace nastavte zaúčtování do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="e9367-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="e9367-106">U obou typů transakcí je účet hlavní knihy pro hodnotu vyřazení dlouhodobého majetku zaúčtován na stranu Dal.</span><span class="sxs-lookup"><span data-stu-id="e9367-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="e9367-107">Částka MD je zaúčtována na protiúčet, který může být například bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="e9367-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="e9367-108">Byl-li dlouhodobý majetek prodán zákazníkovi, použije se místo protiúčtu účet zákazníka.</span><span class="sxs-lookup"><span data-stu-id="e9367-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="e9367-109">Klepněte na tlačítko Vyřazení a poté klepněte na Prodej nebo Likvidace a poté nastavte podrobné účty pro vrácení zůstatkové účetní hodnoty dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="e9367-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="e9367-110">Také můžete zadat informace v polích Zaúčtovat hodnotu a Hodnota prodeje na stránce Parametry vyřazení.</span><span class="sxs-lookup"><span data-stu-id="e9367-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="e9367-111">Transakce vyřazení pro položku dlouhodobého majetku ve fondu majetku s nízkou hodnotou snižuje čistou účetní hodnotu fondu majetku s nízkou hodnotou pouze o vyřazenou částku.</span><span class="sxs-lookup"><span data-stu-id="e9367-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="e9367-112">Pokud je však hodnota prodeje položky majetku vyšší než čistá účetní hodnota fondu majetku s nízkou hodnotou, je hodnota fondu majetku s nízkou hodnotou snížena na nulovou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e9367-112">However, when the sale of an asset exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>





