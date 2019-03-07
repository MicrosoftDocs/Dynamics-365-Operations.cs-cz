---
title: Účty pro zaúčtování pořízení dlouhodobého majetku
description: V tomto článku je vysvětleno nastavení účtů pro zaúčtování do hlavní knihy pro účely pořizování majetku.
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
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a3ac1580e33197c0cd8a82f34804d4639945d861
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "325358"
---
# <a name="fixed-asset-acquisition-posting-accounts"></a><span data-ttu-id="52214-103">Účty pro zaúčtování pořízení dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="52214-103">Fixed asset acquisition posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52214-104">V tomto článku je vysvětleno nastavení účtů pro zaúčtování do hlavní knihy pro účely pořizování majetku.</span><span class="sxs-lookup"><span data-stu-id="52214-104">This article explains how to set up general ledger posting accounts for acquiring assets.</span></span>

<span data-ttu-id="52214-105">Účty použité pro zaúčtování pořízení dlouhodobého majetku se mohou lišit v závislosti na způsobu pořízení majetku.</span><span class="sxs-lookup"><span data-stu-id="52214-105">Accounts used for posting fixed asset acquisitions may vary depending upon the method used to acquire the asset.</span></span> <span data-ttu-id="52214-106">Na stránce profilů zaúčtování dlouhodobého majetku na kartě Účty hlavní knihy vyberte možnost Pořízení a Oprava pořizovací ceny a nastavte účty dlouhodobého majetku pro zaúčtování do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="52214-106">On the Fixed asset posting profiles page, on the Ledger accounts tab, select Acquisition and Acquisition adjustment to set up fixed asset accounts to post to the ledger.</span></span> 

<span data-ttu-id="52214-107">V denících a nákupních objednávkách je účet hlavní knihy obvykle rozvahovým účtem, ve kterém je hodnota pořizovací ceny nového dlouhodobého majetku zaúčtována na stranu Má dáti.</span><span class="sxs-lookup"><span data-stu-id="52214-107">In journals and on purchase orders, Ledger account is typically the balance sheet account, where the acquisition value of the new fixed asset is debited.</span></span> <span data-ttu-id="52214-108">Tento účet není v deníku zobrazen a nelze jej nahradit ani v průběhu transakcí.</span><span class="sxs-lookup"><span data-stu-id="52214-108">This account is not displayed in the journal and cannot be replaced in transactions.</span></span> 

<span data-ttu-id="52214-109">Protiúčet je také rozvahovým účtem.</span><span class="sxs-lookup"><span data-stu-id="52214-109">Offset account is also a balance sheet account.</span></span> <span data-ttu-id="52214-110">V hlavním deníku a v deníku dlouhodobého majetku bude tento účet často sloužit jako bankovní účet používaný pro platby za pořízení majetku.</span><span class="sxs-lookup"><span data-stu-id="52214-110">In the general journal and in the fixed assets journal, this account often will be the bank account that is used to pay for the acquisition of the asset.</span></span> <span data-ttu-id="52214-111">Protiúčet je výchozím účtem nabízeným v denících.</span><span class="sxs-lookup"><span data-stu-id="52214-111">The offset account is a default account, which is suggested in the journals.</span></span> <span data-ttu-id="52214-112">Je možné jej změnit v deníku na jakýkoli jiný účet z účtové osnovy nebo na účet dodavatele, a to v případě, že byl dlouhodobý majetek zakoupen od dodavatele.</span><span class="sxs-lookup"><span data-stu-id="52214-112">It can be changed in the journal to any other account from the chart of accounts or to a vendor account, if the fixed asset was purchase from a vendor.</span></span> 

<span data-ttu-id="52214-113">Jsou-li položky Deník faktur nebo Nákupní objednávky v modulu Závazky určeny k pořízení dlouhodobého majetku, bude protiúčet pro transakci dlouhodobého majetku nahrazen účtem dodavatele vybraným pro tuto transakci.</span><span class="sxs-lookup"><span data-stu-id="52214-113">When Invoice journal or Purchase orders in Accounts payable are used for fixed asset acquisitions, the offset account for the fixed asset transaction is replaced by the vendor account that is selected for the transaction.</span></span>

<span data-ttu-id="52214-114">Pro nabytí zaúčtované pomocí Skladového deníku dlouhodobého majetku v modulu Hlavní kniha není dlouhodobý majetek zakoupen z externích zdrojů, ale převeden z vlastních zásob společnosti.</span><span class="sxs-lookup"><span data-stu-id="52214-114">For acquisitions posted using the Inventory to fixed assets journal in General ledger, the fixed asset is not bought from external sources, but transferred from the company's own inventory.</span></span> <span data-ttu-id="52214-115">Z toho důvodu je protiúčet účtem skladového výdeje pro skladové položky v modulu Správa zásob.</span><span class="sxs-lookup"><span data-stu-id="52214-115">Therefore, the offset account is an inventory issue account for the inventory item in Inventory management.</span></span>

<span data-ttu-id="52214-116">Další informace naleznete v tématu [Pořízení majetku pomocí zásobování](acquire-assets-procurement.md).</span><span class="sxs-lookup"><span data-stu-id="52214-116">For more information, see [Acquire assets through procurement](acquire-assets-procurement.md).</span></span>



