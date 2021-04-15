---
title: Používání cenového modulu Dynamics 365 Commerce s Dynamics 365 Sales
description: V tomto tématu je popsán způsob použití cenového modulu v aplikaci Microsoft Dynamics 365 Commerce k vytvoření prodejních nabídek v Dynamics 365 Sales.
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: 364cc5adf0358ffa952750149ad31d62cbd35e87
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751427"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a><span data-ttu-id="02e6b-103">Používání cenového modulu Dynamics 365 Commerce s Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="02e6b-103">Use the Dynamics 365 Commerce pricing engine with Dynamics 365 Sales</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="02e6b-104">V tomto tématu je popsán způsob použití cenového modulu v aplikaci Microsoft Dynamics 365 Commerce k vytvoření prodejních nabídek v Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="02e6b-104">This topic describes how to use the Microsoft Dynamics 365 Commerce pricing engine to create sales quotations in Dynamics 365 Sales.</span></span>

<span data-ttu-id="02e6b-105">Cenový modul Dynamics 365 Commerce podporuje většinu scénářů cen mezi podniky a spotřebiteli (B2C), jako jsou ceny na úrovni obchodů, ceny založené na přidělení a věrnosti, kombinační slevy, množstevní slevy a mezní slevy.</span><span class="sxs-lookup"><span data-stu-id="02e6b-105">The Dynamics 365 Commerce pricing engine supports most business-to-consumer (B2C) pricing scenarios, such as store-level pricing, affiliation-based and loyalty-based pricing, mix-and-match discounts, quantity discounts, and threshold discounts.</span></span> <span data-ttu-id="02e6b-106">Cenový modul používá složitá pravidla k určení nejvhodnější ceny pro danou nabídku nebo objednávku.</span><span class="sxs-lookup"><span data-stu-id="02e6b-106">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span>

<span data-ttu-id="02e6b-107">Když používáte [duální zápis](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), máte tři možnosti pro vaše potřeby něco ocenit.</span><span class="sxs-lookup"><span data-stu-id="02e6b-107">When you use [dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), you have three options for your pricing needs.</span></span> <span data-ttu-id="02e6b-108">Můžete použít statické ceny, které vycházejí z ceníku v Dynamics 365 Sales, cenový modul Dynamics 365 Supply Chain Management nebo cenový modul v Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="02e6b-108">You can use the static pricing that comes from the price list in Dynamics 365 Sales, the pricing engine in Dynamics 365 Supply Chain Management, or the pricing engine in Dynamics 365 Commerce.</span></span> <span data-ttu-id="02e6b-109">Z těchto možností je pro scénáře B2C nejvhodnější cenový modul Commerce.</span><span class="sxs-lookup"><span data-stu-id="02e6b-109">Among these options, the Commerce pricing engine is best suited to B2C scenarios.</span></span>

## <a name="use-the-commerce-pricing-engine-in-sales"></a><span data-ttu-id="02e6b-110">Používání cenového modulu Commerce v Sales</span><span class="sxs-lookup"><span data-stu-id="02e6b-110">Use the Commerce pricing engine in Sales</span></span>

> [!NOTE]
> <span data-ttu-id="02e6b-111">V současné době lze cenový modul Commerce použít pouze pro vytvoření nabídky v Sales.</span><span class="sxs-lookup"><span data-stu-id="02e6b-111">Currently, the Commerce pricing engine can be used only for quotation creation in the Sales.</span></span> <span data-ttu-id="02e6b-112">Integrace prodejní objednávky s cenovým modulem Commerce ještě není k dispozici.</span><span class="sxs-lookup"><span data-stu-id="02e6b-112">Sales order integration with the Commerce pricing engine isn't yet available.</span></span>

<span data-ttu-id="02e6b-113">Když uživatelé iniciují nabídku v Sales, zkopíruje architektura duálního zápisu podrobnosti nabídky do Commerce.</span><span class="sxs-lookup"><span data-stu-id="02e6b-113">When users initiate a quotation in Sales, the dual-write framework copies the quotation details to Commerce.</span></span> <span data-ttu-id="02e6b-114">Veškeré změny stávajících řádků nabídek nebo nově přidaných řádků nabídek v Sales jsou zkopírovány do Commerce.</span><span class="sxs-lookup"><span data-stu-id="02e6b-114">Any changes to existing quotation lines or any newly added quotation lines in Sales are copied to Commerce.</span></span> <span data-ttu-id="02e6b-115">Pokud uživatelé chtějí k ocenění nabídky použít cenový modul Commerce, mohou si vybrat možnost **Cenová nabídka** a aktualizovat ceny nabídky na základě cenového modulu Commerce.</span><span class="sxs-lookup"><span data-stu-id="02e6b-115">When users want to use the Commerce pricing engine to price the quotation, they can select **Price quote** to update the prices of the quotation, based on the Commerce pricing engine.</span></span> <span data-ttu-id="02e6b-116">Ceny se poté automaticky aktualizují v aplikacích Sales i Commerce.</span><span class="sxs-lookup"><span data-stu-id="02e6b-116">Prices are then automatically updated in both Sales and Commerce.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="02e6b-117">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="02e6b-117">Prerequisites</span></span>

- <span data-ttu-id="02e6b-118">Než budete moci použít cenový modul Commerce v Sales, musíte postupovat podle pokynů v části [Zpeněžení potenciálního zákazníka ve dvojím připisování](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).</span><span class="sxs-lookup"><span data-stu-id="02e6b-118">Before you can use the Commerce pricing engine in Sales, you must follow the steps in [Prospect-to-cash in dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).</span></span>
- <span data-ttu-id="02e6b-119">Vyhodnocení obchodní dohody pro ruční zadávání musíte vypnout pomocí následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="02e6b-119">You must turn off trade agreement evaluation for manual entry by following these steps:</span></span>

    1. <span data-ttu-id="02e6b-120">V prostředí Commerce přejděte do nabídky **Pohledávky \> Nastavení \> Parametry pohledávek**.</span><span class="sxs-lookup"><span data-stu-id="02e6b-120">In your Commerce environment, go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    1. <span data-ttu-id="02e6b-121">Na kartě **Ceny** na pevné záložce **Hodnocení obchodní smlouvy** vypněte zaškrtávací políčko **Ruční zadání**.</span><span class="sxs-lookup"><span data-stu-id="02e6b-121">On the **Prices** tab, on the **Trade agreement evaluation** FastTab, clear the **Manual entry** check box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="02e6b-122">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="02e6b-122">Additional resources</span></span>

[<span data-ttu-id="02e6b-123">Zpeněžení potenciálního zákazníka ve dvojím připisování</span><span class="sxs-lookup"><span data-stu-id="02e6b-123">Prospect-to-cash in dual-write</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]