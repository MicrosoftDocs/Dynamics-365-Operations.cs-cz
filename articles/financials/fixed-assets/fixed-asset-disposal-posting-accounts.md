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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8e00c00b0cb7058858fde3774941911ce20fb6f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "367172"
---
# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="f62d1-103">Účty zaúčtování dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="f62d1-103">Fixed asset disposal posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f62d1-104">Toto téma vysvětluje nastavení účtů pro zaúčtování do hlavní knihy pro účely vyřazení majetku.</span><span class="sxs-lookup"><span data-stu-id="f62d1-104">This topic explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="f62d1-105">Na stránce Účetní profily dlouhodobého majetku na pevné záložce Účty hlavní knihy výběrem Vyřazení – prodej a Vyřazení – likvidace nastavte zaúčtování do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="f62d1-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="f62d1-106">U obou typů transakcí je účet hlavní knihy pro hodnotu vyřazení dlouhodobého majetku zaúčtován na stranu Dal.</span><span class="sxs-lookup"><span data-stu-id="f62d1-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="f62d1-107">Částka MD je zaúčtována na protiúčet, který může být například bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="f62d1-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="f62d1-108">Byl-li dlouhodobý majetek prodán zákazníkovi, použije se místo protiúčtu účet zákazníka.</span><span class="sxs-lookup"><span data-stu-id="f62d1-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="f62d1-109">Klepněte na tlačítko Vyřazení a poté klepněte na Prodej nebo Likvidace a poté nastavte podrobné účty pro vrácení zůstatkové účetní hodnoty dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="f62d1-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="f62d1-110">Také můžete zadat informace v polích Zaúčtovat hodnotu a Hodnota prodeje na stránce Parametry vyřazení.</span><span class="sxs-lookup"><span data-stu-id="f62d1-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="f62d1-111">Transakce vyřazení pro položku dlouhodobého majetku ve fondu majetku s nízkou hodnotou snižuje čistou účetní hodnotu fondu majetku s nízkou hodnotou pouze o vyřazenou částku.</span><span class="sxs-lookup"><span data-stu-id="f62d1-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="f62d1-112">Pokud je však hodnota prodeje položky majetku vyšší než čistá účetní hodnota fondu majetku s nízkou hodnotou, je hodnota fondu majetku s nízkou hodnotou snížena na nulovou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="f62d1-112">However, when the sale of an asset exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>





