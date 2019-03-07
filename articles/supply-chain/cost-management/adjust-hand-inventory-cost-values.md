---
title: Úprava nákladové ceny množství na skladě
description: Stránku Úprava zásob na skladě použijte pro úpravu hodnoty nákladů na množství zásob na skladě po spuštění procesu uzávěrky skladu.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2417a278e58f4309873ab4d33b0d1f1686081951
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "335156"
---
# <a name="adjust-on-hand-inventory-cost-values"></a><span data-ttu-id="113bb-103">Úprava nákladové ceny množství na skladě</span><span class="sxs-lookup"><span data-stu-id="113bb-103">Adjust on-hand inventory cost values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="113bb-104">Stránku Úprava zásob na skladě použijte pro úpravu hodnoty nákladů na množství zásob na skladě po spuštění procesu uzávěrky skladu.</span><span class="sxs-lookup"><span data-stu-id="113bb-104">Use the Adjustment of on-hand inventory page to adjust the cost value of the on-hand inventory quantities after an inventory close process is run.</span></span>

<span data-ttu-id="113bb-105">Stránku **Úprava zásob na skladě** můžete použít pro úpravu hodnoty nákladů na množství zásob na skladě po spuštění procesu uzávěrky skladu.</span><span class="sxs-lookup"><span data-stu-id="113bb-105">You can use the **Adjustment of on-hand inventory** page to adjust the cost value of on-hand inventory quantities after an inventory close process is run.</span></span> <span data-ttu-id="113bb-106">**Poznámka:** Stránku **Úprava zásob na skladě** otevřete tak, že na stránce **Závěrka a oprava** vyberete záznam dokončeného procesu uzávěrky skladu a zvolíte možnost **Úprava** &gt; **Na skladě**.</span><span class="sxs-lookup"><span data-stu-id="113bb-106">**Note:** To open the **Adjustment of on-hand inventory** page, on the **Closing and adjustment** page, select the record of a completed inventory close process, and then click **Adjustment** &gt; **On-hand**.</span></span> <span data-ttu-id="113bb-107">**Příklad:** V únoru dojde k následujícím transakcím:</span><span class="sxs-lookup"><span data-stu-id="113bb-107">**Example:** You have the following transactions in February:</span></span>

-   <span data-ttu-id="113bb-108">1. únor: Finanční příjem zásob v množství 2 kusů v hodnotě 10,00 USD.</span><span class="sxs-lookup"><span data-stu-id="113bb-108">February 1: An inventory financial receipt for a quantity of 2 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="113bb-109">5. únor: Finanční příjem zásob v množství 1 kus v hodnotě 13,00 USD.</span><span class="sxs-lookup"><span data-stu-id="113bb-109">February 5: An inventory financial receipt for a quantity of 1 at a cost of USD 13.00</span></span>
-   <span data-ttu-id="113bb-110">19. únor: Finanční výdej zásob v množství 1 kus a s průběžnou průměrnou cenou 11,00 USD.</span><span class="sxs-lookup"><span data-stu-id="113bb-110">February 19: An inventory financial issue for a quantity of 1 at a running average cost of USD 11.00</span></span>

<span data-ttu-id="113bb-111">Pro tuto položku byl nastaven skladový model podle metody FIFO a uzávěrka skladu byla provedena k 28. únoru.</span><span class="sxs-lookup"><span data-stu-id="113bb-111">This item was set up with the first in, first out (FIFO) inventory model, and inventory close was performed as of February 28.</span></span> <span data-ttu-id="113bb-112">Finanční transakce výdeje v hodnotě 11,00 USD bude vyrovnána s finančním příjmem datovaným k 1. únoru a dále bude provedena úprava v hodnotě 1,00 USD.</span><span class="sxs-lookup"><span data-stu-id="113bb-112">The financial issue transaction of USD 11.00 will be settled against the financial receipt that is dated February 1, and an adjustment of USD 1.00 will be made.</span></span> <span data-ttu-id="113bb-113">Následující skladové příjmy pak budou obsahovat otevřená skladová množství:</span><span class="sxs-lookup"><span data-stu-id="113bb-113">The following inventory receipts will then contain open inventory quantities:</span></span>

-   <span data-ttu-id="113bb-114">1. února: Množství 1 s náklady 10,00 USD</span><span class="sxs-lookup"><span data-stu-id="113bb-114">February 1: A quantity of 1 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="113bb-115">5. února: Množství 1 s náklady 13,00 USD</span><span class="sxs-lookup"><span data-stu-id="113bb-115">February 5: A quantity of 1 at a cost of USD 13.00</span></span>

<span data-ttu-id="113bb-116">Chcete-li nastavit náklady těchto dvou položek na 15,00 USD, upravte pomocí možnosti úpravy množství na skladě k poslední uzávěrce skladu otevřené množství na skladě.</span><span class="sxs-lookup"><span data-stu-id="113bb-116">To set the cost of these two items to USD 15.00, use the on-hand adjustment option to adjust the open on-hand quantities as of the last inventory close period.</span></span> <span data-ttu-id="113bb-117">**Poznámka:** Datem zaúčtování transakce úpravy množství na skladě bude datum poslední uzávěrky skladu.</span><span class="sxs-lookup"><span data-stu-id="113bb-117">**Note:** The posting date of the on-hand adjustment transaction will be the date of the last inventory close.</span></span> <span data-ttu-id="113bb-118">Toto datum nelze změnit.</span><span class="sxs-lookup"><span data-stu-id="113bb-118">This date can't be modified.</span></span>
