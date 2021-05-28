---
title: Daně z online objednávek jsou nesprávně vypočítány
description: Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když jsou daně z online objednávek nesprávně vypočítány nebo když daňová skupina na prodejním řádku není správně nastavena.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f7cef533d76bdddfbad2e8c5f84f81ef62bccc38
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021096"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a><span data-ttu-id="4c457-103">Daně z online objednávek jsou nesprávně vypočítány</span><span class="sxs-lookup"><span data-stu-id="4c457-103">Taxes on online orders are incorrectly calculated</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4c457-104">Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když jsou daně z online objednávek nesprávně vypočítány nebo když daňová skupina na prodejním řádku není správně nastavena.</span><span class="sxs-lookup"><span data-stu-id="4c457-104">This topic provides troubleshooting guidance that can help when taxes on online orders are incorrectly calculated, or when the tax group on the sales line isn't correctly set.</span></span>

## <a name="description"></a><span data-ttu-id="4c457-105">popis</span><span class="sxs-lookup"><span data-stu-id="4c457-105">Description</span></span>

<span data-ttu-id="4c457-106">Při zadání objednávky elektronického obchodu jsou daně nesprávně vypočítány nebo je nesprávně nastavena daňová skupina na prodejním řádku.</span><span class="sxs-lookup"><span data-stu-id="4c457-106">When an e-commerce order is placed, the taxes are incorrectly calculated, or the tax group on the sales line is incorrectly set.</span></span>

## <a name="resolution"></a><span data-ttu-id="4c457-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="4c457-107">Resolution</span></span>

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a><span data-ttu-id="4c457-108">Konfigurace DPH pro maloobchod v centrále Commerce</span><span class="sxs-lookup"><span data-stu-id="4c457-108">Configure the sales tax for a retail store in Commerce headquarters</span></span>

<span data-ttu-id="4c457-109">Chcete-li nakonfigurovat DPH pro maloobchod v centrále Commerce, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="4c457-109">To configure the sales tax for a retail store in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="4c457-110">Přejděte na **Retail a Commerce \> Kanály \> Všechny obchody**.</span><span class="sxs-lookup"><span data-stu-id="4c457-110">Go to **Retail and Commerce \> Channels \> All stores**.</span></span>
1. <span data-ttu-id="4c457-111">Vyberte obchod, pro který chcete nakonfigurovat DPH.</span><span class="sxs-lookup"><span data-stu-id="4c457-111">Select the store to configure sales tax for.</span></span>
1. <span data-ttu-id="4c457-112">Na kartě s náhledem **Všeobecné** v části **Prodejní daň** nakonfigurujte informace o DPH pro obchod.</span><span class="sxs-lookup"><span data-stu-id="4c457-112">On the **General** FastTab, in the **Sales tax** section, configure the sales tax information for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="4c457-113">U vyzvednutí produktu z obchodu daňová skupina pochází z obchodu, který je vybrán pro vyzvednutí.</span><span class="sxs-lookup"><span data-stu-id="4c457-113">For product pickup from a store, the tax group comes from the store that is selected for pickup.</span></span> <span data-ttu-id="4c457-114">Další informace naleznete v tématu [Nastavení dalších daňových možností pro obchody](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="4c457-114">For more information, see [Set other tax options for stores](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a><span data-ttu-id="4c457-115">Konfigurace DPH pro adresu zákazníka v centrále Commerce</span><span class="sxs-lookup"><span data-stu-id="4c457-115">Configure the sales tax for a customer's address in Commerce headquarters</span></span>

<span data-ttu-id="4c457-116">Chcete-li nakonfigurovat DPH pro adresu zákazníka v centrále Commerce, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="4c457-116">To configure the sales tax for a customer's address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="4c457-117">Přejděte na **Pohledávky \> Odběratelé \> Všichni odběratelé**.</span><span class="sxs-lookup"><span data-stu-id="4c457-117">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="4c457-118">Vyberte zákazníka, pro kterého chcete nakonfigurovat DPH.</span><span class="sxs-lookup"><span data-stu-id="4c457-118">Select the customer to configure sales taxes for.</span></span>
1. <span data-ttu-id="4c457-119">Na kartě s náhledem **Adresy** vyberte adresu, pro kterou chcete konfigurovat DPH, vyberte **Další možnost** a potom vyberte **Pokročilé**.</span><span class="sxs-lookup"><span data-stu-id="4c457-119">On the **Addresses** FastTab, select the address to configure sales taxes for, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="4c457-120">Na kartě s náhledem **Obecné** vyberte **Daňová skupina**.</span><span class="sxs-lookup"><span data-stu-id="4c457-120">On the **General** FastTab, select the **Tax group**.</span></span>
1. <span data-ttu-id="4c457-121">V poli **DPH** vyberte příslušnou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4c457-121">In the **Sales tax** field, select the appropriate value.</span></span>

> [!NOTE]
> <span data-ttu-id="4c457-122">U dopravy, která zahrnuje DPH na adrese zákazníka, určuje doručovací adresa řádku daňovou skupinu pro řádek.</span><span class="sxs-lookup"><span data-stu-id="4c457-122">For shipping that involves sales tax on the customer's address, the delivery address of the line determines the tax group for the line.</span></span> <span data-ttu-id="4c457-123">Pokud zákazník odesílá na existující adresu, která má již nakonfigurovanou daňovou skupinu, bude použita stávající daňová skupina.</span><span class="sxs-lookup"><span data-stu-id="4c457-123">If the customer is shipping to an existing address that has a tax group that is already configured, the existing tax group will be used.</span></span> <span data-ttu-id="4c457-124">Ve výchozím nastavení adresy nemají při vytvoření daňovou skupinu.</span><span class="sxs-lookup"><span data-stu-id="4c457-124">By default, addresses don't have a tax group when they are created.</span></span>

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a><span data-ttu-id="4c457-125">Konfigurace obecné skupiny DPH v centrále Commerce</span><span class="sxs-lookup"><span data-stu-id="4c457-125">Configure general sales tax groups in Commerce headquarters</span></span>

<span data-ttu-id="4c457-126">Chcete-li nakonfigurovat obecné skupiny DPH v centrále Commerce, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="4c457-126">To configure general sales tax groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="4c457-127">Přejděte na **Daň \> Nepřímé daně \> DPH \> Skupina DPH**.</span><span class="sxs-lookup"><span data-stu-id="4c457-127">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax group**.</span></span>
1. <span data-ttu-id="4c457-128">Na levém navigačním panelu vyberte daňovou skupinu, kterou chcete nakonfigurovat.</span><span class="sxs-lookup"><span data-stu-id="4c457-128">In the left navigation, select the tax group to configure.</span></span>
1. <span data-ttu-id="4c457-129">Na kartě s náhledem **Maloobchodní daň podle cíle** nakonfigurujte daně pro skupinu DPH.</span><span class="sxs-lookup"><span data-stu-id="4c457-129">On the **Retail destination based tax** FastTab, configure the taxes for the sales tax group.</span></span>

> [!NOTE]
> <span data-ttu-id="4c457-130">U dopravy, která nezahrnuje DPH na adrese zákazníka, určuje daňovou skupinu dodací adresa řádku a daně podle cíle, které jsou nakonfigurovány pro daňovou skupinu.</span><span class="sxs-lookup"><span data-stu-id="4c457-130">For shipping that doesn't involve sales tax on the customer's address, the delivery address of the line and the destination-based taxes that are configured for the tax group determine the tax group.</span></span> <span data-ttu-id="4c457-131">Další informace viz [Nastavení daní pro online obchody podle cílového místa](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="4c457-131">For more information, see [Set up taxes for online stores based on destination](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4c457-132">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="4c457-132">Additional resources</span></span>

[<span data-ttu-id="4c457-133">Konfigurace DPH pro online objednávky</span><span class="sxs-lookup"><span data-stu-id="4c457-133">Configure sales tax for online orders</span></span>](../sales-tax-config.md)