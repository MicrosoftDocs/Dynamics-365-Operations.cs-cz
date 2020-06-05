---
title: Odhlášení z kolekce událostí webové aktivity
description: Toto téma vysvětluje, jak můžete dovolit návštěvníkům vašeho webu odhlásit se ze sbírání událostí webové aktivity v Microsoft Dynamics 365 Commerce.
author: aamiral
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4b0e48307527a8fea729d8dfdcdbc6337be0faf1
ms.sourcegitcommit: 8058db089b8768076ff1250be77d42a6e2b3f570
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378985"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="e3601-103">Odhlášení z kolekce událostí webové aktivity</span><span class="sxs-lookup"><span data-stu-id="e3601-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="e3601-104">V tomto tématu je vysvětleno, jak můžete zákazníkům dovolit odhlásit se ze sbírání událostí webové aktivity v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e3601-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e3601-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="e3601-105">Overview</span></span>

<span data-ttu-id="e3601-106">Dynamics 365 Commerce dovoluje správcům webu analyzovat webovou aktivitu uživatelů svých e-commerce webů.</span><span class="sxs-lookup"><span data-stu-id="e3601-106">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="e3601-107">Tímto způsobem mohou lépe porozumět tomu, jak jsou jejich stránky používány, a mohou je optimalizovat tak, aby poskytovaly lepší uživatelský dojem a splňovaly obchodní cíle.</span><span class="sxs-lookup"><span data-stu-id="e3601-107">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="e3601-108">Způsoby, jak správci mohou uplatnit možnost odhlášení</span><span class="sxs-lookup"><span data-stu-id="e3601-108">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="e3601-109">Správci mají tři možnosti, jak uplatnit možnost odhlášení.</span><span class="sxs-lookup"><span data-stu-id="e3601-109">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="e3601-110">Odhlášení jménem uživatelů</span><span class="sxs-lookup"><span data-stu-id="e3601-110">Opt out on behalf of users</span></span>

<span data-ttu-id="e3601-111">V modulu Správa účtu v centrále obchodu se správci mohou odhlašovat jménem uživatelů.</span><span class="sxs-lookup"><span data-stu-id="e3601-111">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="e3601-112">V klientovi centrály obchodu na stránce **Všichni zákazníci** vyhledejte a vyberte zákazníka.</span><span class="sxs-lookup"><span data-stu-id="e3601-112">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="e3601-113">Na stránce s podrobnostmi zákazníka, na pevné záložce **Maloobchod**, v sekci **Soukromí**, nastavte možnost **Nesledujte aktivitu na webu** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="e3601-113">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![Nastavení ochrany osobních údajů](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="e3601-115">Zvolte **Uložit** a pak zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e3601-115">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="e3601-116">Použití funkce odhlášení na základě modulu</span><span class="sxs-lookup"><span data-stu-id="e3601-116">Module-based opt-out experience</span></span>

<span data-ttu-id="e3601-117">Správci mohou nechat ověřené uživatele, aby se sami odhlásili ze sběru událostí webové aktivity.</span><span class="sxs-lookup"><span data-stu-id="e3601-117">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="e3601-118">Chcete-li tyto možnosti odhlášení poskytnout, přidejte do stránek profilu účtu odběratele modul odhlášení uživatele.</span><span class="sxs-lookup"><span data-stu-id="e3601-118">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="e3601-119">Vlastní rozšíření</span><span class="sxs-lookup"><span data-stu-id="e3601-119">Custom extensions</span></span>

<span data-ttu-id="e3601-120">Správci mohou vytvářet svá vlastní rozšíření pro správu možnosti odhlášení pro uživatele.</span><span class="sxs-lookup"><span data-stu-id="e3601-120">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="e3601-121">Další informace naleznete v tématu [Volání rozhraní API serveru](e-commerce-extensibility/call-retail-server-apis.md) a [Rozšiřitelnost online kanálu](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="e3601-121">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
