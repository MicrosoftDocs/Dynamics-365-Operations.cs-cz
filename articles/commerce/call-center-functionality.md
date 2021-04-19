---
title: Funkce prodeje kontaktního střediska
description: Toto téma obsahuje přehled prodejní funkce kontaktního střediska v aplikaci Dynamics 365 Commerce.
author: josaw1
ms.date: 04/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f1660399e7e88a8f7c96714f9af271b73a17eca2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799606"
---
# <a name="call-center-sales-functionality"></a><span data-ttu-id="ce29f-103">Funkce prodeje kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="ce29f-103">Call center sales functionality</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="ce29f-104">V aplikaci Dynamics 365 Commerce je kontaktní středisko typu kanálu, který lze definovat v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="ce29f-104">In Dynamics 365 Commerce, a call center is a type of channel that can be defined in the application.</span></span> <span data-ttu-id="ce29f-105">Definování konkrétního kanálu pro entity kontaktního střediska umožňuje systému navázat několik výchozích hodnot specifických dat a výchozích nastavení pro prodejní objednávky vytvořené uživatelem kanálu kontaktního střediska.</span><span class="sxs-lookup"><span data-stu-id="ce29f-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="ce29f-106">Kontaktní středisko, které zahrnuje moderní ceny a promoakce, katalogy, dárkové poukazy, věrnostní programy a kupóny.</span><span class="sxs-lookup"><span data-stu-id="ce29f-106">Call center features include advanced price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="ce29f-107">Objednávky kontaktního střediska jsou rovněž využity aplikací pokladních míst (POS) na podporu scénáře splnění objednávky mezi více kanály.</span><span class="sxs-lookup"><span data-stu-id="ce29f-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="ce29f-108">Je důležité poznamenat, zatímco modul kontaktního střediska lze využít v jiných odvětvích mimo Commerce, aktuální verze call centra aplikace nebyla optimalizována pro použití ve zpracování – business-to-business (B2B) scénáři nebo scénáři, kde mají objednávky velký počet řádků prodeje.</span><span class="sxs-lookup"><span data-stu-id="ce29f-108">It's important to note that while the call center module can be utilized by other industries outside of Commerce, the current release of the call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large number of sales lines.</span></span> <span data-ttu-id="ce29f-109">Doporučujeme, aby uživatelé, kteří chtějí využívat funkce call center pro zpracování objednávek mimo typické zpracování přímých transakcí zákazníka, vynaložili dostatečný čas na testování a ověření, že povolení funkce kontaktního střediska splní funkční požadavky a požadavky na výkon.</span><span class="sxs-lookup"><span data-stu-id="ce29f-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="ce29f-110">Kromě podpory vytvoření objednávky modul kontaktního střediska také obsahuje praktickou aplikaci zákaznického servisu, která umožňuje uživatelům ověřit všechny příslušné zákaznické účty a zkontrolovat všechny související objednávky zákazníků a atributy.</span><span class="sxs-lookup"><span data-stu-id="ce29f-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="ce29f-111">Servisní obrazovka odběratele je navržena tak, aby uživateli umožnila rychlý přístup k souvisejícím datům objednávky, která umožní odpovídat na nejčastější dotazy související s objednávkami přijatými od odběratelů.</span><span class="sxs-lookup"><span data-stu-id="ce29f-111">The customer service screen is designed to enable a user to quickly access order-related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="ce29f-112">Tato stránka obsahuje odkazy na relevantní dokumentaci týkající se nastavení, konfigurace a funkčního použití funkcí kontaktního střediska.</span><span class="sxs-lookup"><span data-stu-id="ce29f-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features.</span></span>


## <a name="configure-the-call-center"></a><span data-ttu-id="ce29f-113">Konfigurace parametrů kontaktního střediska.</span><span class="sxs-lookup"><span data-stu-id="ce29f-113">Configure the call center</span></span>

[<span data-ttu-id="ce29f-114">Nastavení kanálů kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="ce29f-114">Set up call center channels</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="ce29f-115">Konfigurace zpracování objednávky</span><span class="sxs-lookup"><span data-stu-id="ce29f-115">Configure order processing</span></span>

[<span data-ttu-id="ce29f-116">Nastavení a práce s výstrahami u podvodů kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="ce29f-116">Set up and work with call center fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="ce29f-117">Konfigurace a práce s blokováním objednávek kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="ce29f-117">Configure and work with call center order holds</span></span>](work-with-order-holds.md)

## <a name="configure-payment-processing"></a><span data-ttu-id="ce29f-118">Konfigurace zpracování platby</span><span class="sxs-lookup"><span data-stu-id="ce29f-118">Configure payment processing</span></span>

[<span data-ttu-id="ce29f-119">Platební metody v kontaktních střediscích</span><span class="sxs-lookup"><span data-stu-id="ce29f-119">Payment methods in call centers</span></span>](work-with-payments.md)

## <a name="configure-delivery-modes"></a><span data-ttu-id="ce29f-120">Konfigurace způsobů dodání</span><span class="sxs-lookup"><span data-stu-id="ce29f-120">Configure delivery modes</span></span>

[<span data-ttu-id="ce29f-121">Konfigurace způsobů dodání a poplatků call centra</span><span class="sxs-lookup"><span data-stu-id="ce29f-121">Configure call center delivery modes and charges</span></span>](configure-call-center-delivery.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="ce29f-122">Konfigurace přímého marketingu</span><span class="sxs-lookup"><span data-stu-id="ce29f-122">Configure direct marketing</span></span>

[<span data-ttu-id="ce29f-123">Katalogy kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="ce29f-123">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="ce29f-124">Nastavení analýzy recency, frekvence a peněžního období</span><span class="sxs-lookup"><span data-stu-id="ce29f-124">Set up Recency, Frequency, and Monetary (RFM) analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="ce29f-125">Konfigurace programů trvání</span><span class="sxs-lookup"><span data-stu-id="ce29f-125">Configure continuity programs</span></span>

[<span data-ttu-id="ce29f-126">Nastavení programů kontinuity pro kontaktní střediska</span><span class="sxs-lookup"><span data-stu-id="ce29f-126">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]