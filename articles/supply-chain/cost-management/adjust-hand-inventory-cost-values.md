---
title: "Úprava nákladové ceny množství na skladě"
description: "Stránku Úprava zásob na skladě použijte pro úpravu hodnoty nákladů na množství zásob na skladě po spuštění procesu uzávěrky skladu."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: AndersGirke
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 21942f7aa57d21f70e3014051c42328164b750a3
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="adjust-on-hand-inventory-cost-values"></a><span data-ttu-id="520ed-103">Úprava nákladové ceny množství na skladě</span><span class="sxs-lookup"><span data-stu-id="520ed-103">Adjust on-hand inventory cost values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="520ed-104">Stránku Úprava zásob na skladě použijte pro úpravu hodnoty nákladů na množství zásob na skladě po spuštění procesu uzávěrky skladu.</span><span class="sxs-lookup"><span data-stu-id="520ed-104">Use the Adjustment of on-hand inventory page to adjust the cost value of the on-hand inventory quantities after an inventory close process is run.</span></span>

<span data-ttu-id="520ed-105">Stránku **Úprava zásob na skladě** můžete použít pro úpravu hodnoty nákladů na množství zásob na skladě po spuštění procesu uzávěrky skladu.</span><span class="sxs-lookup"><span data-stu-id="520ed-105">You can use the **Adjustment of on-hand inventory** page to adjust the cost value of on-hand inventory quantities after an inventory close process is run.</span></span> <span data-ttu-id="520ed-106">**Poznámka:** Stránku **Úprava zásob na skladě** otevřete tak, že na stránce **Závěrka a oprava** vyberete záznam dokončeného procesu uzávěrky skladu a zvolíte možnost **Úprava** &gt; **Na skladě**.</span><span class="sxs-lookup"><span data-stu-id="520ed-106">**Note:** To open the **Adjustment of on-hand inventory** page, on the **Closing and adjustment** page, select the record of a completed inventory close process, and then click **Adjustment** &gt; **On-hand**.</span></span> <span data-ttu-id="520ed-107">**Příklad:** V únoru dojde k následujícím transakcím:</span><span class="sxs-lookup"><span data-stu-id="520ed-107">**Example:** You have the following transactions in February:</span></span>

-   <span data-ttu-id="520ed-108">1. únor: Finanční příjem zásob v množství 2 kusů v hodnotě 10,00 USD.</span><span class="sxs-lookup"><span data-stu-id="520ed-108">February 1: An inventory financial receipt for a quantity of 2 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="520ed-109">5. únor: Finanční příjem zásob v množství 1 kus v hodnotě 13,00 USD.</span><span class="sxs-lookup"><span data-stu-id="520ed-109">February 5: An inventory financial receipt for a quantity of 1 at a cost of USD 13.00</span></span>
-   <span data-ttu-id="520ed-110">19. únor: Finanční výdej zásob v množství 1 kus a s průběžnou průměrnou cenou 11,00 USD.</span><span class="sxs-lookup"><span data-stu-id="520ed-110">February 19: An inventory financial issue for a quantity of 1 at a running average cost of USD 11.00</span></span>

<span data-ttu-id="520ed-111">Pro tuto položku byl nastaven skladový model podle metody FIFO a uzávěrka skladu byla provedena k 28. únoru.</span><span class="sxs-lookup"><span data-stu-id="520ed-111">This item was set up with the first in, first out (FIFO) inventory model, and inventory close was performed as of February 28.</span></span> <span data-ttu-id="520ed-112">Finanční transakce výdeje v hodnotě 11,00 USD bude vyrovnána s finančním příjmem datovaným k 1. únoru a dále bude provedena úprava v hodnotě 1,00 USD.</span><span class="sxs-lookup"><span data-stu-id="520ed-112">The financial issue transaction of USD 11.00 will be settled against the financial receipt that is dated February 1, and an adjustment of USD 1.00 will be made.</span></span> <span data-ttu-id="520ed-113">Následující skladové příjmy pak budou obsahovat otevřená skladová množství:</span><span class="sxs-lookup"><span data-stu-id="520ed-113">The following inventory receipts will then contain open inventory quantities:</span></span>

-   <span data-ttu-id="520ed-114">1. února: Množství 1 s náklady 10,00 USD</span><span class="sxs-lookup"><span data-stu-id="520ed-114">February 1: A quantity of 1 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="520ed-115">5. února: Množství 1 s náklady 13,00 USD</span><span class="sxs-lookup"><span data-stu-id="520ed-115">February 5: A quantity of 1 at a cost of USD 13.00</span></span>

<span data-ttu-id="520ed-116">Chcete-li nastavit náklady těchto dvou položek na 15,00 USD, upravte pomocí možnosti úpravy množství na skladě k poslední uzávěrce skladu otevřené množství na skladě.</span><span class="sxs-lookup"><span data-stu-id="520ed-116">To set the cost of these two items to USD 15.00, use the on-hand adjustment option to adjust the open on-hand quantities as of the last inventory close period.</span></span> <span data-ttu-id="520ed-117">**Poznámka:** Datem zaúčtování transakce úpravy množství na skladě bude datum poslední uzávěrky skladu.</span><span class="sxs-lookup"><span data-stu-id="520ed-117">**Note:** The posting date of the on-hand adjustment transaction will be the date of the last inventory close.</span></span> <span data-ttu-id="520ed-118">Toto datum nelze změnit.</span><span class="sxs-lookup"><span data-stu-id="520ed-118">This date can't be modified.</span></span>

