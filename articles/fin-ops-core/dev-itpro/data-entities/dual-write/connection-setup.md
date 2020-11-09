---
title: Pokyny, jak nastavit duální zápis
description: Toto téma popisuje scénáře, které jsou podporovány pro nastavení dvojího zápisu.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 2d77a1458f3f4c79b231e6a6d7cc320b8ee1fad9
ms.sourcegitcommit: ee643d651d57560bccae2f99238faa39881f5c64
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088499"
---
# <a name="guidance-for-how-to-set-up-dual-write"></a><span data-ttu-id="6ac95-103">Pokyny, jak nastavit duální zápis</span><span class="sxs-lookup"><span data-stu-id="6ac95-103">Guidance for how to set up dual-write</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="6ac95-104">Můžete nastavit připojení dvojího zápisu mezi prostředím Finance and Operations a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6ac95-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="6ac95-105">**Prostředí Finance and Operations** poskytuje základní platformu pro **aplikace Finance and Operations** (například Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management a Dynamics 365 Retail).</span><span class="sxs-lookup"><span data-stu-id="6ac95-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Retail).</span></span>
+ <span data-ttu-id="6ac95-106">**Prostředí Common Data Service** poskytuje základní platformu pro **aplikace pro zapojení zákazníků** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing a Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="6ac95-106">A **Common Data Service environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

>[!IMPORTANT]
><span data-ttu-id="6ac95-107">Modul personalistiky v aplikaci Finance and Operations podporuje připojení pro duální zápis, ale aplikace Dynamics 365 Human Resources ne.</span><span class="sxs-lookup"><span data-stu-id="6ac95-107">Human Resources in Finance and Operations supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="6ac95-108">Nastavení mechanismu se liší v závislosti na vašem předplatném a prostředí.</span><span class="sxs-lookup"><span data-stu-id="6ac95-108">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="6ac95-109">U nových instancí aplikací Finance and Operations začíná nastavení připojení dvojího zapisování v Lifecycle Services (LCS) Microsoft Dynamics.</span><span class="sxs-lookup"><span data-stu-id="6ac95-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="6ac95-110">Máte-li licenci pro Power Platform, obdržíte nové prostředí Common Data Service, pokud je váš klient neobsahuje.</span><span class="sxs-lookup"><span data-stu-id="6ac95-110">If you have a license for Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="6ac95-111">Pro existující instance aplikací Finance and Operations začíná nastavení připojení dvojího zapisování do prostředí Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6ac95-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="6ac95-112">Než začnete s duálním zápisem na entitě, můžete spustit počáteční synchronizaci pro zpracování existujících dat na obou stranách aplikací Finance and Operations a aplikací pro zapojení zákazníků.</span><span class="sxs-lookup"><span data-stu-id="6ac95-112">Before you start dual-write on an entity, you can run an initial sync to handle existing data on both sides of Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="6ac95-113">Pokud nepotřebujete synchronizovat data mezi dvěma prostředími, můžete počáteční synchronizaci přeskočit.</span><span class="sxs-lookup"><span data-stu-id="6ac95-113">You can skip the initial sync if you don't need to synchronize data between the two environments.</span></span>

<span data-ttu-id="6ac95-114">Počáteční synchronizace umožňuje obousměrně kopírovat existující data z jedné aplikace do jiné.</span><span class="sxs-lookup"><span data-stu-id="6ac95-114">An initial sync lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="6ac95-115">Existuje několik různých scénářů instalace v závislosti na tom, která prostředí již máte a jaký typ dat je v prostředích.</span><span class="sxs-lookup"><span data-stu-id="6ac95-115">There are several different setup scenarios depending on which environments you already have and what type of data is in the environments.</span></span>

<span data-ttu-id="6ac95-116">Podporovány jsou následující scénáře registrace:</span><span class="sxs-lookup"><span data-stu-id="6ac95-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="6ac95-117">Nová instance aplikace Finance and Operations a nová instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="6ac95-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="6ac95-118">Nová instance aplikace Finance and Operations a existující instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="6ac95-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="6ac95-119">Nová instance aplikace Finance and Operations, která má data, a nová instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="6ac95-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="6ac95-120">Nová instance aplikace Finance and Operations, která má data, a existující instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="6ac95-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="6ac95-121">Existující instance aplikace Finance and Operations a nová instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="6ac95-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="6ac95-122">Existující instance aplikace Finance and Operations a existující instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="6ac95-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="6ac95-123">Nová instance aplikace Finance and Operations a nová instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="6ac95-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="6ac95-124">Chcete-li nastavit připojení dvojího zapisování mezi novou instancí aplikace Finance and Operations, která neobsahuje žádná data a novou instanci aplikace pro zapojení zákazníků, postupujte podle kroků v [nastavení dvojího zápisu z Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="6ac95-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="6ac95-125">Po dokončení nastavení připojení dojde k automatickému provedení následujících akcí:</span><span class="sxs-lookup"><span data-stu-id="6ac95-125">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="6ac95-126">Je zajištěno nové prázdné prostředí Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6ac95-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="6ac95-127">Je zřízena nová prázdná instance aplikace pro zapojení zákazníků, kde je nainstalováno základní řešení CRM.</span><span class="sxs-lookup"><span data-stu-id="6ac95-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="6ac95-128">Pro data společnosti DAT je vytvořeno připojení s dvojím zapisováním.</span><span class="sxs-lookup"><span data-stu-id="6ac95-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="6ac95-129">Mapování entit je povoleno pro živou synchronizaci.</span><span class="sxs-lookup"><span data-stu-id="6ac95-129">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="6ac95-130">Obě prostředí jsou připravena k synchronizaci dat živého vysílání.</span><span class="sxs-lookup"><span data-stu-id="6ac95-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="6ac95-131">Nová instance aplikace Finance and Operations a existující instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="6ac95-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="6ac95-132">Chcete-li nastavit připojení dvojího zapisování mezi novou instancí aplikace Finance and Operations, která neobsahuje žádná data a existující instanci aplikace pro zapojení zákazníků, postupujte podle kroků v [nastavení dvojího zápisu z Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="6ac95-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="6ac95-133">Po dokončení nastavení připojení dojde k automatickému provedení následujících akcí:</span><span class="sxs-lookup"><span data-stu-id="6ac95-133">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="6ac95-134">Je zajištěno nové prázdné prostředí Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6ac95-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="6ac95-135">Pro data společnosti DAT je vytvořeno připojení s dvojím zapisováním.</span><span class="sxs-lookup"><span data-stu-id="6ac95-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="6ac95-136">Mapování entit je povoleno pro živou synchronizaci.</span><span class="sxs-lookup"><span data-stu-id="6ac95-136">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="6ac95-137">Obě prostředí jsou připravena k synchronizaci dat živého vysílání.</span><span class="sxs-lookup"><span data-stu-id="6ac95-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="6ac95-138">Chcete-li synchronizovat existující data Common Data Service s aplikací Finance and Operations, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="6ac95-138">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="6ac95-139">Vytvořte v aplikaci Finance and Operations novou společnost.</span><span class="sxs-lookup"><span data-stu-id="6ac95-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="6ac95-140">Přidejte společnost do nastavení připojení s duálním zapisováním.</span><span class="sxs-lookup"><span data-stu-id="6ac95-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="6ac95-141">[Zavedení](bootstrap-company-data.md) dat Common Data Service pomocí třímístného kódu společnosti pro Mezinárodní organizaci pro normalizaci (ISO).</span><span class="sxs-lookup"><span data-stu-id="6ac95-141">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="6ac95-142">Spusťte funkci **Počáteční synchronizace** pro entity, pro které chcete synchronizovat data.</span><span class="sxs-lookup"><span data-stu-id="6ac95-142">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="6ac95-143">Příklad a alternativní přístup viz [Příklad](#example).</span><span class="sxs-lookup"><span data-stu-id="6ac95-143">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="6ac95-144">Nová instance aplikace Finance and Operations, která má data, a nová instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="6ac95-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="6ac95-145">Chcete-li nastavit připojení dvojího zapisování mezi novou instancí aplikace Finance and Operations, která má ukázková data, a novou instanci aplikace pro zapojení zákazníků, postupujte podle kroků v [nové instanci aplikace Finance and Operations a v oddílu nové instance aplikace pro zapojení zákazníků](#new-new) dříve v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="6ac95-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="6ac95-146">Chcete-li v aplikaci synchronizovat data s aplikací pro zapojení zákazníků, postupujte po dokončení nastavení připojení následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="6ac95-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="6ac95-147">Otevřete aplikaci Finance and Operations ze stránky LCS, přihlaste se a pak přejděte ke **Správě dat \> Dvojí zápis**.</span><span class="sxs-lookup"><span data-stu-id="6ac95-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="6ac95-148">Spusťte funkci **Počáteční synchronizace** pro entity, pro které chcete synchronizovat data.</span><span class="sxs-lookup"><span data-stu-id="6ac95-148">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="6ac95-149">Příklad a alternativní přístup viz [Příklad](#example).</span><span class="sxs-lookup"><span data-stu-id="6ac95-149">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="6ac95-150">Nová instance aplikace Finance and Operations, která má data, a existující instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="6ac95-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="6ac95-151">Chcete-li nastavit připojení dvojího zapisování mezi novou instancí aplikace Finance and Operations, která má data, a eistující instanci aplikace pro zapojení zákazníků, postupujte podle kroků v [nové instanci aplikace Finance and Operations a v oddílu existující instance aplikace pro zapojení zákazníků](#new-existing) dříve v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="6ac95-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="6ac95-152">Chcete-li v aplikaci synchronizovat data s aplikací pro zapojení zákazníků, postupujte po dokončení nastavení připojení následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="6ac95-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="6ac95-153">Otevřete aplikaci Finance and Operations ze stránky LCS, přihlaste se a pak přejděte ke **Správě dat \> Dvojí zápis**.</span><span class="sxs-lookup"><span data-stu-id="6ac95-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="6ac95-154">Spusťte funkci **Počáteční synchronizace** pro entity, pro které chcete synchronizovat data.</span><span class="sxs-lookup"><span data-stu-id="6ac95-154">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="6ac95-155">Chcete-li synchronizovat existující data Common Data Service s aplikací Finance and Operations, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="6ac95-155">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="6ac95-156">Vytvořte v aplikaci Finance and Operations novou společnost.</span><span class="sxs-lookup"><span data-stu-id="6ac95-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="6ac95-157">Přidejte společnost do nastavení připojení s duálním zapisováním.</span><span class="sxs-lookup"><span data-stu-id="6ac95-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="6ac95-158">[Zavedení](bootstrap-company-data.md) dat Common Data Service pomocí třímístného kódu společnosti ISO.</span><span class="sxs-lookup"><span data-stu-id="6ac95-158">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="6ac95-159">Spusťte funkci **Počáteční synchronizace** pro entity, pro které chcete synchronizovat data.</span><span class="sxs-lookup"><span data-stu-id="6ac95-159">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="6ac95-160">Příklad a alternativní přístup viz [Příklad](#example).</span><span class="sxs-lookup"><span data-stu-id="6ac95-160">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="6ac95-161">Existující instance aplikace Finance and Operations a nová instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="6ac95-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="6ac95-162">Nastavení připojení s dvojím zapisováním mezi existující instancí aplikace Finance and Operations a novou instancí aplikace pro zapojení zákazníků probíhá v prostředí Finance and Operation.</span><span class="sxs-lookup"><span data-stu-id="6ac95-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="6ac95-163">[Nastavit připojení z aplikace Finance and Operations](enable-dual-write.md)</span><span class="sxs-lookup"><span data-stu-id="6ac95-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="6ac95-164">Spusťte funkci **Počáteční synchronizace** pro entity, pro které chcete synchronizovat data.</span><span class="sxs-lookup"><span data-stu-id="6ac95-164">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="6ac95-165">Příklad a alternativní přístup viz [Příklad](#example).</span><span class="sxs-lookup"><span data-stu-id="6ac95-165">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="6ac95-166">Existující instance aplikace Finance and Operations a existující instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="6ac95-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="6ac95-167">Nastavení připojení s dvojím zapisováním mezi existující instancí aplikace Finance and Operations a existující instancí aplikace pro zapojení zákazníků probíhá v prostředí Finance and Operation.</span><span class="sxs-lookup"><span data-stu-id="6ac95-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app  occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="6ac95-168">Nastavit připojení z aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6ac95-168">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="6ac95-169">Chcete-li synchronizovat existující data Common Data Service s aplikací Finance and Operations, [zaveďte](bootstrap-company-data.md) data Common Data Service pomocí třímístného kódu ISO společnosti.</span><span class="sxs-lookup"><span data-stu-id="6ac95-169">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="6ac95-170">Spusťte funkci **Počáteční synchronizace** pro entity, pro které chcete synchronizovat data.</span><span class="sxs-lookup"><span data-stu-id="6ac95-170">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="6ac95-171">Příklad a alternativní přístup viz [Příklad](#example).</span><span class="sxs-lookup"><span data-stu-id="6ac95-171">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="example"></a><span data-ttu-id="6ac95-172">Příklad</span><span class="sxs-lookup"><span data-stu-id="6ac95-172">Example</span></span>

<span data-ttu-id="6ac95-173">Příklad viz [Povolení Customers V3 — mapa entit kontaktů](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)</span><span class="sxs-lookup"><span data-stu-id="6ac95-173">For an example, see [Enabling the Customers V3—Contacts entity map](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)</span></span>

<span data-ttu-id="6ac95-174">Alternativní přístup založený na objemech dat v každé entitě, která potřebuje spustit počáteční synchronizaci, najdete v části [Úvahy o počáteční synchronizaci](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="6ac95-174">For an alternative approach based on data volumes in each entity that need to run initial sync, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>
