---
title: Záznamy zákazníků se nezobrazují v centrále Commerce
description: Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když se záznamy zákazníků okamžitě nezobrazí v centrále Commerce.
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
ms.openlocfilehash: 790468ac244f1647c07024604886c65d22feca24
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585230"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a><span data-ttu-id="da923-103">Záznamy zákazníků se nezobrazují v centrále Commerce</span><span class="sxs-lookup"><span data-stu-id="da923-103">Customer records don't appear in Commerce headquarters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="da923-104">Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když se záznamy zákazníků okamžitě nezobrazí v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="da923-104">This topic provides troubleshooting guidance that can help when customer records don't immediately appear in Commerce headquarters.</span></span>

## <a name="description"></a><span data-ttu-id="da923-105">popis</span><span class="sxs-lookup"><span data-stu-id="da923-105">Description</span></span>

<span data-ttu-id="da923-106">Když vytvoříte nový záznam zákazníka pomocí toku přihlášení na webu elektronického obchodu, odpovídající záznam zákazníka se okamžitě nezobrazí v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="da923-106">When you create a new customer record by using the sign-up flow in the e-commerce storefront, the corresponding customer record doesn't immediately appear in Commerce headquarters.</span></span>

## <a name="resolution"></a><span data-ttu-id="da923-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="da923-107">Resolution</span></span>

### <a name="disable-customer-creation-in-async-mode"></a><span data-ttu-id="da923-108">Zakázání vytváření zákazníků v asynchronním režimu</span><span class="sxs-lookup"><span data-stu-id="da923-108">Disable customer creation in async mode</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da923-109">Pokud zakážete asynchronní vytváření zákazníků, může to ovlivnit výkon systému, protože vytvoření každého záznamu vytvoří požadavek v reálném čase na centrálu Commerce.</span><span class="sxs-lookup"><span data-stu-id="da923-109">If you disable asynchronous customer creation, system performance could be affected, because creation of each record will produce a real-time request to Commerce headquarters.</span></span> <span data-ttu-id="da923-110">Kromě toho, pokud je sídlo společnosti Commerce nefunkční (například během servisních toků), jakékoli nové toky vytváření zákazníků způsobí chyby.</span><span class="sxs-lookup"><span data-stu-id="da923-110">In addition, if Commerce headquarters is down (for example, during servicing flows), any new customer creation flows will produce errors.</span></span>

<span data-ttu-id="da923-111">Chcete-li zakázat vytváření zákazníků v asynchronním režimu v centrále Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="da923-111">To disable customer creation in async mode in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="da923-112">Přejděte na **Retail a Commerce \> Nastavení kanálu \> Nastavení online obchodu \> Funkční profily**.</span><span class="sxs-lookup"><span data-stu-id="da923-112">Go to **Retail and Commerce \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="da923-113">Pokud pro svůj online kanál ještě nepoužíváte funkční profil, vytvořte si ho.</span><span class="sxs-lookup"><span data-stu-id="da923-113">If you aren't already using a functionality profile for your online channel, create one.</span></span>
1. <span data-ttu-id="da923-114">Ujistěte se, že možnost **Vytvořit zákazníka v asynchronním režimu** je nastavena na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="da923-114">Make sure that the **Create customer in async mode** option is set to **No**.</span></span>
1. <span data-ttu-id="da923-115">Přejděte na **Retail a Commerce \> Kanály \> Online obchody**.</span><span class="sxs-lookup"><span data-stu-id="da923-115">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="da923-116">Vyberte online obchod, pro který zakážete asynchronní vytváření zákazníků.</span><span class="sxs-lookup"><span data-stu-id="da923-116">Select the online store to disable asynchronous customer creation for.</span></span>
1. <span data-ttu-id="da923-117">Na kartě **Všeobecné** zkontrolujte se, že pole **Funkční profil** je nastaveno na funkční profil, který používáte pro svůj online kanál.</span><span class="sxs-lookup"><span data-stu-id="da923-117">On the **General** tab, make sure that the **Functionality profile** field is set to the functionality profile that you're using for your online channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="da923-118">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="da923-118">Additional resources</span></span>

[<span data-ttu-id="da923-119">Nastavení klienta B2C v Commerce</span><span class="sxs-lookup"><span data-stu-id="da923-119">Setup a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)
