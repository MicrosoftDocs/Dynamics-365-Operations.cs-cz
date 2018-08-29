---
title: "Funkce prodeje kontaktního střediska"
description: "Toto téma obsahuje přehled o prodejní funkci kontaktního střediska v aplikaci Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 2b536ad4f29a3bb76294ef2fba30c529c24f1375
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---

# <a name="call-center-sales-functionality"></a><span data-ttu-id="3f7f0-103">Funkce prodeje kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="3f7f0-103">Call center sales functionality</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3f7f0-104">V aplikaci Dynamics 365 for Retail je kontaktní středisko typu maloobchodní sítě, které lze definovat v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="3f7f0-104">In Dynamics 365 for Retail, a call center is a type of Retail channel that can be defined in the application.</span></span> <span data-ttu-id="3f7f0-105">Definování konkrétního kanálu pro entity kontaktního střediska umožňuje systému navázat několik výchozích hodnot specifických dat a výchozích nastavení pro prodejní objednávky vytvořené uživatelem kanálu kontaktního střediska.</span><span class="sxs-lookup"><span data-stu-id="3f7f0-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="3f7f0-106">Kontaktní středisko, které zahrnuje moderní maloobchodní ceny a promoakce, katalogy, dárkové poukazy, věrnostní programy a kupóny.</span><span class="sxs-lookup"><span data-stu-id="3f7f0-106">Call center features include advanced retail price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="3f7f0-107">Objednávky kontaktního střediska jsou rovněž využity aplikací pokladních míst (POS) na podporu scénáře splnění objednávky mezi více kanály.</span><span class="sxs-lookup"><span data-stu-id="3f7f0-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="3f7f0-108">Je důležité poznamenat, zatímco modul kontaktního střediska lze využít v jiných odvětvích mimo Retail, aktuální verze call centra aplikace Dynamics 365 for Retail nebyla optimalizována pro použití ve zpracování – business-to-business (B2B) scénáři nebo scénáři, kde mají objednávky velký počet řádků prodeje.</span><span class="sxs-lookup"><span data-stu-id="3f7f0-108">It's important to note that while the call center module can be utilized by other industries outside of Retail, the current release of the Dynamics 365 for Retail call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large amount of sales lines.</span></span> <span data-ttu-id="3f7f0-109">Doporučujeme, aby uživatelé, kteří chtějí využívat funkce call center pro zpracování objednávek mimo typické zpracování přímých transakcí zákazníka, vynaložili dostatečný čas na testování a ověření, že povolení funkce kontaktního střediska splní funkční požadavky a požadavky na výkon.</span><span class="sxs-lookup"><span data-stu-id="3f7f0-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="3f7f0-110">Kromě podpory vytvoření objednávky modul kontaktního střediska také obsahuje praktickou aplikaci zákaznického servisu, která umožňuje uživatelům ověřit všechny příslušné zákaznické účty a zkontrolovat všechny související objednávky zákazníků a atributy.</span><span class="sxs-lookup"><span data-stu-id="3f7f0-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="3f7f0-111">Servisní obrazovka odběratele je navržena tak, aby uživateli umožnila rychlý přístup k souvisejícím datům objednávky, která umožní odpovídat na nejčastější dotazy související s objednávkami přijatými od odběratelů.</span><span class="sxs-lookup"><span data-stu-id="3f7f0-111">The customer service screen is designed to enable a user to quickly access order related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="3f7f0-112">Tato stránka obsahuje odkazy na relevantní dokumentaci týkající se nastavení, konfigurace a funkčního použití funkcí kontaktního střediska aplikace Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="3f7f0-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features in Dynamics 365 for Retail.</span></span>

## <a name="configure-the-call-center"></a><span data-ttu-id="3f7f0-113">Konfigurace parametrů kontaktního střediska.</span><span class="sxs-lookup"><span data-stu-id="3f7f0-113">Configure the call center</span></span>
[<span data-ttu-id="3f7f0-114">Nastavení možností zpracování objednávky</span><span class="sxs-lookup"><span data-stu-id="3f7f0-114">Set up order processing options</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="3f7f0-115">Konfigurace zpracování objednávky</span><span class="sxs-lookup"><span data-stu-id="3f7f0-115">Configure order processing</span></span>
[<span data-ttu-id="3f7f0-116">Nastavení výstrah u podvodů</span><span class="sxs-lookup"><span data-stu-id="3f7f0-116">Set up fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="3f7f0-117">Ruční blokování objednávek</span><span class="sxs-lookup"><span data-stu-id="3f7f0-117">Manual Order Holds</span></span>](work-with-order-holds.md)

## <a name="configure-payment-processing"></a><span data-ttu-id="3f7f0-118">Konfigurace zpracování platby</span><span class="sxs-lookup"><span data-stu-id="3f7f0-118">Configure payment processing</span></span>
[<span data-ttu-id="3f7f0-119">Platební metody v kontaktním středisku</span><span class="sxs-lookup"><span data-stu-id="3f7f0-119">Payment methods in a call center</span></span>](work-with-payments.md)

## <a name="configure-delivery-modes"></a><span data-ttu-id="3f7f0-120">Konfigurace způsobů dodání</span><span class="sxs-lookup"><span data-stu-id="3f7f0-120">Configure delivery modes</span></span>
[<span data-ttu-id="3f7f0-121">Konfigurace způsobů dodání a poplatků call centra</span><span class="sxs-lookup"><span data-stu-id="3f7f0-121">Configure call center delivery modes and charges</span></span>](configure-call-center-delivery.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="3f7f0-122">Konfigurace přímého marketingu</span><span class="sxs-lookup"><span data-stu-id="3f7f0-122">Configure direct marketing</span></span>
[<span data-ttu-id="3f7f0-123">Katalogy kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="3f7f0-123">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="3f7f0-124">Nastavení analýzy RFM</span><span class="sxs-lookup"><span data-stu-id="3f7f0-124">Set up RFM analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="3f7f0-125">Konfigurace programů trvání</span><span class="sxs-lookup"><span data-stu-id="3f7f0-125">Configure continuity programs</span></span>
[<span data-ttu-id="3f7f0-126">Nastavení programu kontinuity pro kontaktní středisko</span><span class="sxs-lookup"><span data-stu-id="3f7f0-126">Set up a continuity program for a call center</span></span>](set-up-continuity-program.md)


