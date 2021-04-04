---
title: Nastavení vývojového prostředí elektronického obchodování pro ladění proti virtuálnímu počítači maloobchodního serveru úrovně 1
description: Toto téma vysvětluje, jak nastavit vývojové prostředí elektronického obchodování pro ladění proti virtuálnímu počítači maloobchodního serveru úrovně 1.
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
ms.openlocfilehash: 35380a559a4f1b22bdf04ff25cb2bbfc51aff45b
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585222"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a><span data-ttu-id="6f0e6-103">Nastavení vývojového prostředí elektronického obchodování pro ladění proti virtuálnímu počítači maloobchodního serveru úrovně 1</span><span class="sxs-lookup"><span data-stu-id="6f0e6-103">Set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6f0e6-104">Toto téma vysvětluje, jak nastavit vývojové prostředí elektronického obchodování pro ladění proti virtuálnímu počítači maloobchodního serveru úrovně 1.</span><span class="sxs-lookup"><span data-stu-id="6f0e6-104">This topic explains how to set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine (VM).</span></span>

## <a name="description"></a><span data-ttu-id="6f0e6-105">popis</span><span class="sxs-lookup"><span data-stu-id="6f0e6-105">Description</span></span>

<span data-ttu-id="6f0e6-106">Microsoft Dynamics 365 Commerce úrovně 1 se obvykle nasazuje pro Commerce Runtime (CRT) a vývoj rozšíření pokladního místa (POS).</span><span class="sxs-lookup"><span data-stu-id="6f0e6-106">Microsoft Dynamics 365 Commerce Tier 1 environments are typically deployed for Commerce runtime (CRT) and point of sale (POS) extension development.</span></span> <span data-ttu-id="6f0e6-107">Jsou to samostatná prostředí.</span><span class="sxs-lookup"><span data-stu-id="6f0e6-107">They are standalone environments.</span></span> <span data-ttu-id="6f0e6-108">Vzhledem k povaze architektury softwaru jako služby (SaaS) neobsahují komponenty elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="6f0e6-108">Because of the software as a service (SaaS) nature of the architecture, they don't include e-commerce components.</span></span>

<span data-ttu-id="6f0e6-109">V některých scénářích můžete chtít otestovat volání rozšíření v prostředí úrovně 1, abyste mohli ladit rozšíření z komponent elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="6f0e6-109">In some scenarios, you might want to test calls to extensions in a Tier 1 environment, so that you can debug extensions from e-commerce components.</span></span> <span data-ttu-id="6f0e6-110">Obecné pokyny naleznete v části [Ladění proti vývojovému prostředí Commerce úrovně 1](../e-commerce-extensibility/debug-tier-1.md).</span><span class="sxs-lookup"><span data-stu-id="6f0e6-110">For general instructions, see [Debug against a Tier 1 Commerce development environment](../e-commerce-extensibility/debug-tier-1.md).</span></span>

<span data-ttu-id="6f0e6-111">Když ladíte proti prostředí úrovně 1, protože web nyní volá jiný maloobchodní server, volání mezi servery mohou způsobit různé chyby související se zásadami zabezpečení obsahu.</span><span class="sxs-lookup"><span data-stu-id="6f0e6-111">When you debug against a Tier 1 environment, because the site is now calling a different Retail Server, cross-server calls might cause various errors that are related to the content security policy.</span></span>

<span data-ttu-id="6f0e6-112">Následující obrázek ukazuje příklad chyby, ke které může dojít při výběru varianty na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="6f0e6-112">The following illustration shows an example of an error that might occur when a variant is selected on a product details page.</span></span>

![Chyba při výběru varianty na stránce s podrobnostmi o produktu](media/unhandled-rejection-error.jpg)

<span data-ttu-id="6f0e6-114">Následující obrázek ukazuje příklad podobné chyby v ladicích nástrojích prohlížeče (Vývojářské nástroje F12).</span><span class="sxs-lookup"><span data-stu-id="6f0e6-114">The following illustration shows an example of a similar error in a browser's debugger tools (F12 Developer Tools).</span></span> <span data-ttu-id="6f0e6-115">Chybová zpráva zmiňuje porušení směrnice o zásadách zabezpečení obsahu.</span><span class="sxs-lookup"><span data-stu-id="6f0e6-115">The error message mentions violation of the content security policy directive.</span></span>

![Chyba nástrojů ladicího programu](media/debugger-tools-error.JPG)

## <a name="resolution"></a><span data-ttu-id="6f0e6-117">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="6f0e6-117">Resolution</span></span>

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a><span data-ttu-id="6f0e6-118">Deaktivace zásad zabezpečení obsahu pro web v nástroji pro tvorbu webů Commerce</span><span class="sxs-lookup"><span data-stu-id="6f0e6-118">Disable the content security policy for the site in Commerce site builder</span></span>

1. <span data-ttu-id="6f0e6-119">Vyberte web, na kterém pracujete.</span><span class="sxs-lookup"><span data-stu-id="6f0e6-119">Select the site that you're working on.</span></span>
1. <span data-ttu-id="6f0e6-120">Vyberte **Nastavení** a pak vyberte **Rozšíření**.</span><span class="sxs-lookup"><span data-stu-id="6f0e6-120">Select **Settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="6f0e6-121">Na kartě **Zásady zabezpečení obsahu** vyberte **Deaktivovat zásady zabezpečení obsahu**.</span><span class="sxs-lookup"><span data-stu-id="6f0e6-121">On the **Content security policy** tab, select **Disable content security policy**.</span></span>
1. <span data-ttu-id="6f0e6-122">Vyberte možnost **Uložit a publikovat**.</span><span class="sxs-lookup"><span data-stu-id="6f0e6-122">Select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="6f0e6-123">Přihlášení mezi podniky a spotřebitelem (B2C) nebude fungovat v místním vývojovém prostředí.</span><span class="sxs-lookup"><span data-stu-id="6f0e6-123">Business-to-consumer (B2C) sign-in won't work in a local development environment.</span></span> <span data-ttu-id="6f0e6-124">Můžete však použít pokladny hosta nebo vytvořit falešné stránky k simulaci přihlášení uživatele podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="6f0e6-124">However, you can use guest checkouts or build page mocks to simulate a user sign-in as required.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6f0e6-125">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="6f0e6-125">Additional resources</span></span>

[<span data-ttu-id="6f0e6-126">Začněte s online vývojem rozšiřitelnosti elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="6f0e6-126">Get started with e-commerce online extensibility development</span></span>](../e-commerce-extensibility/sdk-getting-started.md)

[<span data-ttu-id="6f0e6-127">Správa zásady zabezpečení obsahu (CSP) na webu elektronického obchodování</span><span class="sxs-lookup"><span data-stu-id="6f0e6-127">Manage content security policy (CSP) on e-commerce site</span></span>](../manage-csp.md)
