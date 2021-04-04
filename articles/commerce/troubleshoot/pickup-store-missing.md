---
title: Maloobchod se neobjevuje v seznamu obchodů, ze kterých si můžete vyzvednout
description: Toto téma poskytuje pokyny pro řešení potíží, které vám mohou pomoci, když se maloobchod neobjeví v seznamu obchodů, kde lze vyzvednout položky.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 652f5f1a779a412c21c18814071ba0fb7dd2e155
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585238"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a><span data-ttu-id="a8bb1-103">Maloobchod se neobjevuje v seznamu obchodů, ze kterých si můžete vyzvednout</span><span class="sxs-lookup"><span data-stu-id="a8bb1-103">Retail store doesn't appear in the list of stores to pick up from</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a8bb1-104">Toto téma poskytuje pokyny pro řešení potíží, které vám mohou pomoci, když se maloobchod neobjeví v seznamu obchodů, kde lze vyzvednout položky.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-104">This topic provides troubleshooting guidance that can help when a retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="description"></a><span data-ttu-id="a8bb1-105">popis</span><span class="sxs-lookup"><span data-stu-id="a8bb1-105">Description</span></span>

<span data-ttu-id="a8bb1-106">Maloobchod se neobjevuje v seznamu obchodů, kde lze zboží vyzvednout.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-106">A retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="resolution"></a><span data-ttu-id="a8bb1-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="a8bb1-107">Resolution</span></span>

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a><span data-ttu-id="a8bb1-108">Konfigurace zeměpisné délky a šířky pro adresu obchodu v centrále Commerce</span><span class="sxs-lookup"><span data-stu-id="a8bb1-108">Configure the longitude and latitude for the store address in Commerce headquarters</span></span>

<span data-ttu-id="a8bb1-109">Pro konfiguraci zeměpisné délky a šířky pro adresu obchodu v centrále Commerce postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-109">To configure the longitude and latitude for the store address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a8bb1-110">Přejděte na **Retail a Commerce \> Kanály \> Obchody \> Všechny obchody**.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-110">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="a8bb1-111">Mezi možnostmi vyzvednutí na webu elektronického obchodování vyhledejte obchod, který chcete zobrazit.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-111">Find the store that you want to appear among the pickup options on the e-commerce site.</span></span> <span data-ttu-id="a8bb1-112">Poznamenejte si jeho hodnotu **Číslo provozní jednotky**.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-112">Make a note of its **Operating unit number** value.</span></span>
1. <span data-ttu-id="a8bb1-113">Přejděte do nabídky **Správa organizace \> Organizace \> Provozní jednotky**.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-113">Go to **Organization administration \> Organizations \> Operating units**.</span></span>
1. <span data-ttu-id="a8bb1-114">Vyhledejte číslo provozní jednotky, které jste si dříve poznamenali, a poté vyberte provozní jednotku ve výsledcích hledání.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-114">Search for the operating unit number that you noted earlier, and then select the operating unit in the search results.</span></span>
1. <span data-ttu-id="a8bb1-115">Na pevné záložce **Adresy** vyberte **Další možnosti** a poté vyberte **Rozšířené**.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-115">On the **Addresses** FastTab, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="a8bb1-116">Na pevné záložce **Všeobecné** zkontrolujte, že jsou správně nastavena pole **Zeměpisná délka** a **Zeměpisná šířka**.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-116">On the **General** FastTab, make sure that the **Longitude** and **Latitude** fields are correctly set.</span></span> <span data-ttu-id="a8bb1-117">V rámci tohoto kroku zkontrolujte, zda jsou hodnoty správně zadány jako kladná nebo záporná čísla.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-117">As part of this step, make sure that the values are correctly specified as positive or negative numbers.</span></span>

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a><span data-ttu-id="a8bb1-118">Konfigurace skupin plnění v centrále Commerce</span><span class="sxs-lookup"><span data-stu-id="a8bb1-118">Configure fulfillment groups in Commerce headquarters</span></span>

<span data-ttu-id="a8bb1-119">Konfiguraci skupin plnění v centrále Commerce provedete následovně.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-119">To configure fulfillment groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a8bb1-120">Přejděte na **Retail a Commerce \> Kanály \> Online obchody**.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-120">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="a8bb1-121">Vyberte online obchod, který chcete konfigurovat.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-121">Select the online store to configure.</span></span>
1. <span data-ttu-id="a8bb1-122">V podokně Akce vyberte kartu **Nastavení** a poté vyberte možnost **Přiřazení skupiny plnění**.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-122">On the Action Pane, select **Set up**, and then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="a8bb1-123">Na stránce **Přiřazení skupiny plnění** vyberte skupinu plnění pro online obchod.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-123">On the **Fulfillment group assignment** page, select the fulfillment group for the online store.</span></span>
1. <span data-ttu-id="a8bb1-124">V části **Nastavení** zkontrolujte, že maloobchod je správně nakonfigurován pro skupinu plnění.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-124">Under **Setup**, make sure that the retail store is correctly configured for the fulfillment group.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a8bb1-125">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="a8bb1-125">Additional resources</span></span> 

[<span data-ttu-id="a8bb1-126">Vytvoření provozní jednotky</span><span class="sxs-lookup"><span data-stu-id="a8bb1-126">Create an operating unit</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit)

[<span data-ttu-id="a8bb1-127">Nastavení online kanálu</span><span class="sxs-lookup"><span data-stu-id="a8bb1-127">Set up an online channel</span></span>](../channel-setup-online.md)