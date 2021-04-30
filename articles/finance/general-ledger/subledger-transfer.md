---
title: Převod dílčí hlavní knihy do hlavní knihy
description: Toto téma popisuje funkce Microsoft Dynamics 365 Finance související s procesem převodu dílčí hlavní knihy do hlavní knihy.
author: roschlom
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1efdf095e379b73d553ca3525abbeee8ca35bcbb
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897497"
---
# <a name="subledger-transfer-to-the-general-ledger"></a><span data-ttu-id="0110a-103">Převod dílčí hlavní knihy do hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="0110a-103">Subledger transfer to the General ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0110a-104">V tomto tématu jsou popsány funkce Microsoft Dynamics 365 Finance, které se vztahují k pravidlům převodu dávek položek dílčí hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="0110a-104">This topic describes capabilities in Microsoft Dynamics 365 Finance that are related to the rules for transferring batches of subledger journal entries.</span></span>

<span data-ttu-id="0110a-105">Ve verzi 8.1 byly provedeny změny za účelem umožnění přenosu pravidel, na jejichž základě je **synchronní** možnost odepsána.</span><span class="sxs-lookup"><span data-stu-id="0110a-105">In version 8.1, changes were made to allow the transfer of rules, which deprecated the **Synchronous** option.</span></span> <span data-ttu-id="0110a-106">Další informace naleznete v části [Odstraněné nebo zastaralé funkce pro Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).</span><span class="sxs-lookup"><span data-stu-id="0110a-106">For more information, see [Removed or deprecated features for Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).</span></span>

<span data-ttu-id="0110a-107">Pro převod dávek dílčí hlavní knihy jsou k dispozici následující možnosti.</span><span class="sxs-lookup"><span data-stu-id="0110a-107">The following options are available for transferring subledger batches.</span></span> 

 - <span data-ttu-id="0110a-108">Asynchronní – Tato možnost okamžitě naplánuje převod účetních položek dílčí hlavní knihy do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="0110a-108">Asynchronous – This option will immediately schedule the transfer of the subledger accounting entries to the general ledger.</span></span> <span data-ttu-id="0110a-109">Doklad hlavní knihy bude zaznamenán, jakmile zdroje budou moci zpracovat tento požadavek na serveru.</span><span class="sxs-lookup"><span data-stu-id="0110a-109">The general ledger voucher will be recorded as soon as resources are free to process this request on the server.</span></span> 

- <span data-ttu-id="0110a-110">Plánovaná dávka – Tato možnost přidá do hlavní knihy položky modulu zaúčtování dílčí hlavní knihy, které jsou přeneseny do fronty zpracování, kde budou položky zpracovány v přijatém pořadí.</span><span class="sxs-lookup"><span data-stu-id="0110a-110">Scheduled batch – This option will add the subledger accounting entries that are being transferred to the processing queue in the general ledger, where the entries will be processed in order received.</span></span> <span data-ttu-id="0110a-111">Doklad hlavní knihy bude v naplánovaném čase zaznamenán, jakmile zdroje budou moci zpracovat tuto dávkovou úlohu na serveru.</span><span class="sxs-lookup"><span data-stu-id="0110a-111">The general ledger voucher will be recorded at the scheduled time if resources are free to process this batch job on the server.</span></span> 
 
<span data-ttu-id="0110a-112">Ve verzi 10.0.8 byla provedena vylepšení pro zvýšení výkonu možnosti Asynchrnonní.</span><span class="sxs-lookup"><span data-stu-id="0110a-112">In version 10.0.8, improvements were made to enhance the performance of the Asynchronous option.</span></span> <span data-ttu-id="0110a-113">Tato funkce je povolena pod názvem funkce **Optimalizace výkonu převodu z dílčí knihy do hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="0110a-113">This feature is enabled under the feature name **Subledger transfer to General Ledger performance optimization**.</span></span> 
 
<span data-ttu-id="0110a-114">Tato funkce zlepšuje přenos dat z dílčí hlavní knihy do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="0110a-114">This functionality improves the transfer of data from the subledger to the general ledger.</span></span> <span data-ttu-id="0110a-115">Umožňuje efektivnější proces a seskupuje sady menších transakcí pro převod.</span><span class="sxs-lookup"><span data-stu-id="0110a-115">It allows the process to be more efficient, and it groups together sets of smaller transactions to transfer.</span></span> <span data-ttu-id="0110a-116">To umožňuje efektivnější využití dávkového serveru.</span><span class="sxs-lookup"><span data-stu-id="0110a-116">This allows for a more efficient use of the batch server.</span></span> <span data-ttu-id="0110a-117">Tato funkce vyžaduje, aby byl dávkový server nastaven, online a funkční, aby bylo možné použít možnost asynchronního převodu.</span><span class="sxs-lookup"><span data-stu-id="0110a-117">This functionality requires that the batch server be set up, online, and functioning in order for the Asynchronous transfer option to work.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]