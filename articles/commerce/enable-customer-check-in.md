---
title: Povolit oznámení o přihlášení zákazníka v místě prodeje (POS)
description: Toto téma popisuje, jak povolit oznámení o přihlášení zákazníka v místě prodeje Microsoft Dynamics 365 Commerce (POS).
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e4defc15d9ef198a361934d51e31016747dbb5ab
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937567"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a><span data-ttu-id="899da-103">Povolit oznámení o přihlášení zákazníka v místě prodeje (POS)</span><span class="sxs-lookup"><span data-stu-id="899da-103">Enable customer check-in notifications in point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="899da-104">Toto téma popisuje, jak povolit oznámení o přihlášení zákazníka v místě prodeje Microsoft Dynamics 365 Commerce (POS).</span><span class="sxs-lookup"><span data-stu-id="899da-104">This topic describes how to enable customer check-in notifications in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="899da-105">Ve svých e-mailech „objednávka je připravena k vyzvednutí“ mohou organizace poskytnout odkaz nebo tlačítko, které zákazníkům umožní upozornit obchod, že jsou v areálu a čekají, až jim bude doručen jejich balíček.</span><span class="sxs-lookup"><span data-stu-id="899da-105">In their "order ready for pickup" emails, organizations can provide a link or button that lets customers notify the store that they are on the premises and waiting for their package to be brought out to them.</span></span> <span data-ttu-id="899da-106">Zákazníci poté obdrží potvrzení o přihlášení a obchod obdrží oznámení jako úkol ve své aplikaci POS.</span><span class="sxs-lookup"><span data-stu-id="899da-106">Customers then receive a check-in confirmation, and the store receives a notification as a task in its POS application.</span></span> <span data-ttu-id="899da-107">Tento úkol slouží jako výzva prodejnímu pracovníkovi k doručení objednávky do vozidla zákazníka.</span><span class="sxs-lookup"><span data-stu-id="899da-107">This task serves as a prompt for a sales associate to deliver the order to the customer's vehicle.</span></span> <span data-ttu-id="899da-108">Zákazník tedy nemusí vstoupit do obchodu.</span><span class="sxs-lookup"><span data-stu-id="899da-108">Therefore, the customer doesn't have to enter the store.</span></span>

<span data-ttu-id="899da-109">Workflow přihlášení zákazníka lze také nakonfigurovat tak, aby shromažďoval od zákazníků další informace, například číslo jejich parkovacího místa, značku, model a barvu jejich vozidla a pokyny k dodání.</span><span class="sxs-lookup"><span data-stu-id="899da-109">The customer check-in workflow can also be configured to collect additional information from customers, such as their parking spot number, the make, model, and color of their vehicle, and delivery instructions.</span></span> <span data-ttu-id="899da-110">Obsluha obchodu může tyto informace použít k usnadnění plnění objednávky.</span><span class="sxs-lookup"><span data-stu-id="899da-110">The retail store attendant can use this information to facilitate order fulfillment.</span></span>

## <a name="enable-customer-check-in"></a><span data-ttu-id="899da-111">Aktivace přihlášení zákazníka</span><span class="sxs-lookup"><span data-stu-id="899da-111">Enable customer check-in</span></span>

<span data-ttu-id="899da-112">Když je zapnuta funkce přihlášení zákazníka, vygeneruje Commerce ID potvrzení objednávky (označované také jako referenční číslo kanálu).</span><span class="sxs-lookup"><span data-stu-id="899da-112">When the customer check-in feature is turned on, Commerce generates an order confirmation ID (also known as the channel reference ID).</span></span> <span data-ttu-id="899da-113">Také generuje ID potvrzení objednávky pro objednávky, které jsou vytvořeny prostřednictvím prodejních míst (POS) nebo kanálů call centra.</span><span class="sxs-lookup"><span data-stu-id="899da-113">It also generates order confirmation IDs for orders that are created through point of sale (POS) or call center channels.</span></span> 

<span data-ttu-id="899da-114">Chcete-li zapnout funkci přihlášení zákazníka v centrále Commerce, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="899da-114">To turn on the customer check-in feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="899da-115">Přejděte na **Pracovní prostory \> Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="899da-115">Go to **Workspaces \> Feature management**.</span></span>
2. <span data-ttu-id="899da-116">Vyhledejte funkci **Vygenerovat konzistentní formát ID referenčního kanálu napříč kanály**.</span><span class="sxs-lookup"><span data-stu-id="899da-116">Search for the **Generate a consistent channel reference ID format across channels** feature.</span></span> 
3. <span data-ttu-id="899da-117">Vyberte funkci a poté v podokně vlastností vyberte možnost **Povolit nyní**.</span><span class="sxs-lookup"><span data-stu-id="899da-117">Select the feature, and then select **Enable now** in the properties pane.</span></span> 

## <a name="create-a-check-in-confirmation-page"></a><span data-ttu-id="899da-118">Vytvořte stránku s potvrzením přihlášení</span><span class="sxs-lookup"><span data-stu-id="899da-118">Create a check-in confirmation page</span></span>

<span data-ttu-id="899da-119">Na svém webu elektronického obchodu musíte vytvořit novou stránku, která bude sloužit jako prostředí pro potvrzení přihlášení.</span><span class="sxs-lookup"><span data-stu-id="899da-119">On your e-commerce site, you must create a new page that will serve as the check-in confirmation experience.</span></span> <span data-ttu-id="899da-120">Prostřednictvím další konfigurace může stránka také obsahovat formulář, který shromažďuje další informace od zákazníků, aby se usnadnilo plnění objednávky.</span><span class="sxs-lookup"><span data-stu-id="899da-120">Through additional configuration, the page can also include a form that collects additional information from customers to facilitate order fulfillment.</span></span> <span data-ttu-id="899da-121">Informace o tom, jak nastavit stránku a modul, najdete v části [Modul přihlášení zákazníka](check-in-pickup-module.md).</span><span class="sxs-lookup"><span data-stu-id="899da-121">For information about how to set up the page and module, see [Customer check-in module](check-in-pickup-module.md).</span></span>

## <a name="configure-the-transactional-email-template"></a><span data-ttu-id="899da-122">Konfigurace šablony transakčního e-mailu</span><span class="sxs-lookup"><span data-stu-id="899da-122">Configure the transactional email template</span></span>

<span data-ttu-id="899da-123">Musíte přidat odkaz nebo tlačítko **Jsem tady** na šablonu pro transakční e-mail, který zákazníci obdrží, když je jejich objednávka připravena k vyzvednutí.</span><span class="sxs-lookup"><span data-stu-id="899da-123">You must add an **I am here** link or button to the template for the transactional email that customers receive when their order is ready for pickup.</span></span> <span data-ttu-id="899da-124">Tímto odkazem nebo tlačítkem zákazníci upozorní obchod, že dorazili, aby si vyzvedli objednávku.</span><span class="sxs-lookup"><span data-stu-id="899da-124">Customers will use this link or button to notify the store that they have arrived to pick up their order.</span></span> 

<span data-ttu-id="899da-125">Přidejte odkaz nebo tlačítko na šablonu, která je namapována na typ oznámení **Balení dokončeno** a způsob doručení, který používáte k plnění objednávky.</span><span class="sxs-lookup"><span data-stu-id="899da-125">Add the link or button to the template that is mapped to the **Packing completed** notification type and the mode of delivery that you're using for curbside order fulfillment.</span></span> <span data-ttu-id="899da-126">V šabloně vytvořte odkaz nebo tlačítko HTML, které odkazuje na adresu URL stránky s potvrzením přihlášení, kterou jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="899da-126">In the template, create an HTML link or button that points to the URL of the check-in confirmation page that you created.</span></span> <span data-ttu-id="899da-127">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="899da-127">Here is an example.</span></span>

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
<span data-ttu-id="899da-128">Další informace o konfiguraci e-mailových šablon najdete v tématu [Přizpůsobení transakčních e-mailů podle způsobu doručení](customize-email-delivery-mode.md).</span><span class="sxs-lookup"><span data-stu-id="899da-128">For more information about how to configure email templates, see [Customize transactional emails by mode of delivery](customize-email-delivery-mode.md).</span></span> 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a><span data-ttu-id="899da-129">V POS je vytvořena úloha potvrzení odbavení</span><span class="sxs-lookup"><span data-stu-id="899da-129">A check-in confirmation task is created in POS</span></span>

<span data-ttu-id="899da-130">Poté, co zákazník upozorní obchod, že je přítomen k vyzvednutí, obdrží oznámení o potvrzení přihlášení a v seznamu úkolů v POS pro obchod, kde si zákazník vyzvedává objednávku, se vytvoří úkol.</span><span class="sxs-lookup"><span data-stu-id="899da-130">After a customer notifies the store that they are present for pickup, they receive a check-in confirmation notification, and a task is created in the tasks list in POS for the store where the customer is picking up the order.</span></span> <span data-ttu-id="899da-131">Úkol obsahuje všechny informace o zákazníkovi a objednávce, které jsou nutné pro splnění objednávky.</span><span class="sxs-lookup"><span data-stu-id="899da-131">The task contains all the customer and order information that is required to fulfill the order.</span></span> <span data-ttu-id="899da-132">V poli úkolu se v poli s pokyny zobrazují všechny informace, které byly od zákazníka shromážděny prostřednictvím formuláře s doplňujícími informacemi.</span><span class="sxs-lookup"><span data-stu-id="899da-132">In the task, the instructions field shows any information that was collected from the customer through the additional information form.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="899da-133">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="899da-133">Additional resources</span></span>

[<span data-ttu-id="899da-134">Přihlášení k modulu vyzvednutí</span><span class="sxs-lookup"><span data-stu-id="899da-134">Check-in for pickup module</span></span>](check-in-pickup-module.md)
