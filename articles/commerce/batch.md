---
title: Vylepšené zpracování položek sledovaných dávkou
description: Toto téma popisuje vylepšení provedená u zpracování dávek pro položky sledované dávkou během procesu zaúčtování výkazu.
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: ecff18f0a34d22ef359f473fa6aaaff16c811bb6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458602"
---
# <a name="improved-handling-of-batch-tracked-items"></a><span data-ttu-id="7f7e2-103">Vylepšené zpracování položek sledovaných dávkou</span><span class="sxs-lookup"><span data-stu-id="7f7e2-103">Improved handling of batch-tracked items</span></span>


[!include [banner](includes/banner.md)]


<span data-ttu-id="7f7e2-104">V Point of Sale (POS) nelze zaznamenat čísla dávek pro položky sledované dávkou v okamžiku prodeje.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-104">In Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</span></span> <span data-ttu-id="7f7e2-105">Nicméně pro konkrétní konfigurace při zaúčtování prodejů v centrále prostřednictvím objednávek zákazníků nebo zaúčtování výkazů očekává systém Microsoft Dynamics, že platná čísla dávky pro položky sledované dávkou existují a že budou použity během procesu fakturace.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-105">However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</span></span>

<span data-ttu-id="7f7e2-106">Pokud jsou pro produkty k dispozici platná čísla dávek, použije je proces fakturace objednávky zákazníka a proces fakturace prodejní objednávky ze zaúčtování výkazu.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-106">If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</span></span> <span data-ttu-id="7f7e2-107">V opačném případě proces fakturace objednávky zákazníka nemůže provést zaúčtování a uživatel POS obdrží chybovou zprávu.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-107">Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</span></span> <span data-ttu-id="7f7e2-108">Zaúčtování výkazu se pak dostane do chybového stavu.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-108">Statement posting then goes into an error state.</span></span> <span data-ttu-id="7f7e2-109">K tomuto chybovému stavu dojde tehdy, když byly pro produkty zapnuty záporné zásoby.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-109">This error state occurs even when negative inventory has been turned on for the products.</span></span>

<span data-ttu-id="7f7e2-110">Vylepšení, která byla provedena v aplikaci Retail verze 10.0.4 a novějších, pomáhají zaručit, že při zapnutých záporných zásobách pro položky sledované dávkou nebudou pro tyto položky blokovány fakturace objednávek zákazníků a fakturace prodejních objednávek prostřednictvím zaúčtování výkazu, pokud jsou zásoby 0 (nula) nebo není k dispozici číslo dávky.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-110">Improvements that have been made in Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</span></span> <span data-ttu-id="7f7e2-111">Nová funkcionalita používá výchozí ID dávky pro prodejní řádky, když nejsou čísla dávek k dispozici.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-111">The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</span></span>

<span data-ttu-id="7f7e2-112">Chcete-li definovat výchozí ID dávky, které se používá pro objednávky zákazníka, na stránce **Parametry obchodu** na kartě **Objednávky zákazníka** na záložce s náhledem **Objednávka** nastavte pole **Výchozí ID dávky**.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-112">To define the default batch ID that is used for customer orders, on the **Commerce parameters** page, on the **Customer orders** tab, on the **Order** FastTab, set the **Default batch id** field.</span></span>

<span data-ttu-id="7f7e2-113">Chcete-li definovat výchozí ID dávky, které se používá pro fakturaci prodejní objednávky prostřednictvím zaúčtování výkazu, na stránce **Parametry obchodu** na kartě **Zaúčtování** na záložce s náhledem **Aktualizace zásob** nastavte pole **Výchozí ID dávky**.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-113">To define the default batch ID that is used for sales order invoicing through statement posting, on the **Commerce parameters** page, on the **Posting** tab, on the **Inventory update** FastTab, set the **Default batch id** field.</span></span>

> [!NOTE]
> <span data-ttu-id="7f7e2-114">Tato funkce je k dispozici pouze tehdy, když je zapnuta rozšířená správa skladu pro konkrétní sklad obchodu a položky.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-114">This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</span></span> <span data-ttu-id="7f7e2-115">V novější verzi bude tato funkcionalita podporována též pro scénáře, kde se rozšířená správa skladu nepoužívá.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-115">In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</span></span>

> [!NOTE]
> <span data-ttu-id="7f7e2-116">Podpora pro zlepšené zpracování položek sledovaných dávkou při zaúčtování výkazů pro nerozšířené scénáře správy skladu byla představena v aplikaci Retail verze 10.0.5.</span><span class="sxs-lookup"><span data-stu-id="7f7e2-116">Support for improved handling of batch-tracked items during statement posting for non-advanced warehouse management scenarios was introduced in Retail version 10.0.5.</span></span>
