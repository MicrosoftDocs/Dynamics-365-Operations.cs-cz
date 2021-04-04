---
title: Pokyny pro nastavení duálního zápisu
description: Toto téma popisuje scénáře, které jsou podporovány pro nastavení dvojího zápisu.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: dee6bc52a0967dfd6134258d3a02dc18feb404a5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560218"
---
# <a name="guidance-for-dual-write-setup"></a><span data-ttu-id="5359d-103">Pokyny pro nastavení duálního zápisu</span><span class="sxs-lookup"><span data-stu-id="5359d-103">Guidance for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5359d-104">Můžete nastavit připojení dvojího zápisu mezi prostředím Finance and Operations a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="5359d-104">You can set up a dual-write connection between a Finance and Operations environment and a Dataverse environment.</span></span>

+ <span data-ttu-id="5359d-105">**Prostředí Finance and Operations** poskytuje základní platformu pro aplikace **Finance and Operations** (například Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce a Dynamics 365 Human Resources).</span><span class="sxs-lookup"><span data-stu-id="5359d-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="5359d-106">Prostředí **Dataverse** poskytuje základní platformu pro **aplikace Customer Engagement** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing a Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="5359d-106">A **Dataverse environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5359d-107">Modul personalistiky v aplikaci Dynamics 365 Finance podporuje připojení pro duální zápis, ale aplikace Dynamics 365 Human Resources ne.</span><span class="sxs-lookup"><span data-stu-id="5359d-107">The Human Resources module in Dynamics 365 Finance supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="5359d-108">Nastavení mechanismu se liší v závislosti na vašem předplatném a prostředí:</span><span class="sxs-lookup"><span data-stu-id="5359d-108">The setup mechanism varies, depending on your subscription and the environment:</span></span>

+ <span data-ttu-id="5359d-109">U nových instancí aplikací Finance and Operations začíná nastavení připojení dvojího zapisování v Lifecycle Services (LCS) Microsoft Dynamics.</span><span class="sxs-lookup"><span data-stu-id="5359d-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="5359d-110">Máte-li licenci pro Microsoft Power Platform, obdržíte nové prostředí Dataverse, pokud je váš klient neobsahuje.</span><span class="sxs-lookup"><span data-stu-id="5359d-110">If you have a license for Microsoft Power Platform, you will get a new Dataverse environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="5359d-111">Pro existující instance aplikací Finance and Operations začíná nastavení připojení dvojího zapisování do prostředí Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5359d-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="5359d-112">Než začnete s duálním zápisem na entitě, můžete spustit počáteční synchronizaci pro zpracování existujících dat na obou stranách: u aplikací Finance and Operations a aplikací pro zapojení zákazníků.</span><span class="sxs-lookup"><span data-stu-id="5359d-112">Before you start dual-write on an entity, you can run an initial synchronization to handle existing data on both sides: Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="5359d-113">Pokud nepotřebujete synchronizovat data mezi dvěma prostředími, můžete počáteční synchronizaci přeskočit.</span><span class="sxs-lookup"><span data-stu-id="5359d-113">You can skip the initial synchronization if you don't have to sync data between the two environments.</span></span>

<span data-ttu-id="5359d-114">Počáteční synchronizace umožňuje obousměrně kopírovat existující data z jedné aplikace do jiné.</span><span class="sxs-lookup"><span data-stu-id="5359d-114">An initial synchronization lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="5359d-115">Existuje několik scénářů instalace v závislosti na tom, která prostředí již máte a jaký typ dat se v nich nachází.</span><span class="sxs-lookup"><span data-stu-id="5359d-115">There are several setup scenarios, depending on the environments that you already have and the type of data in them.</span></span>

<span data-ttu-id="5359d-116">Podporovány jsou následující scénáře registrace:</span><span class="sxs-lookup"><span data-stu-id="5359d-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="5359d-117">Nová instance aplikace Finance and Operations a nová instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="5359d-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="5359d-118">Nová instance aplikace Finance and Operations a existující instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="5359d-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="5359d-119">Nová instance aplikace Finance and Operations, která má data, a nová instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="5359d-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="5359d-120">Nová instance aplikace Finance and Operations, která má data, a existující instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="5359d-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="5359d-121">Existující instance aplikace Finance and Operations a nová instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="5359d-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="5359d-122">Existující instance aplikace Finance and Operations a existující instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="5359d-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="5359d-123">Nová instance aplikace Finance and Operations a nová instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="5359d-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="5359d-124">Chcete-li nastavit připojení dvojího zapisování mezi novou instancí aplikace Finance and Operations, která neobsahuje žádná data a novou instanci aplikace pro zapojení zákazníků, postupujte podle kroků v [nastavení dvojího zápisu z Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="5359d-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="5359d-125">Po dokončení nastavení připojení dojde k automatickému provedení následujících akcí:</span><span class="sxs-lookup"><span data-stu-id="5359d-125">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="5359d-126">Je zajištěno nové prázdné prostředí Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5359d-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="5359d-127">Je zřízena nová prázdná instance aplikace pro zapojení zákazníků, kde je nainstalováno základní řešení CRM.</span><span class="sxs-lookup"><span data-stu-id="5359d-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="5359d-128">Pro data společnosti DAT je vytvořeno připojení s dvojím zapisováním.</span><span class="sxs-lookup"><span data-stu-id="5359d-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="5359d-129">Mapování tabulek je povoleno u živé synchronizace.</span><span class="sxs-lookup"><span data-stu-id="5359d-129">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="5359d-130">Obě prostředí jsou připravena k synchronizaci dat živého vysílání.</span><span class="sxs-lookup"><span data-stu-id="5359d-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="5359d-131">Nová instance aplikace Finance and Operations a existující instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="5359d-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="5359d-132">Chcete-li nastavit připojení dvojího zapisování mezi novou instancí aplikace Finance and Operations, která neobsahuje žádná data a existující instanci aplikace pro zapojení zákazníků, postupujte podle kroků v [nastavení dvojího zápisu z Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="5359d-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="5359d-133">Po dokončení nastavení připojení dojde k automatickému provedení následujících akcí:</span><span class="sxs-lookup"><span data-stu-id="5359d-133">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="5359d-134">Je zajištěno nové prázdné prostředí Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5359d-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="5359d-135">Pro data společnosti DAT je vytvořeno připojení s dvojím zapisováním.</span><span class="sxs-lookup"><span data-stu-id="5359d-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="5359d-136">Mapování tabulek je povoleno u živé synchronizace.</span><span class="sxs-lookup"><span data-stu-id="5359d-136">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="5359d-137">Obě prostředí jsou připravena k synchronizaci dat živého vysílání.</span><span class="sxs-lookup"><span data-stu-id="5359d-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="5359d-138">Chcete-li synchronizovat existující data Dataverse s aplikací Finance and Operations, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="5359d-138">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="5359d-139">Vytvořte v aplikaci Finance and Operations novou společnost.</span><span class="sxs-lookup"><span data-stu-id="5359d-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="5359d-140">Přidejte společnost do nastavení připojení s duálním zapisováním.</span><span class="sxs-lookup"><span data-stu-id="5359d-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="5359d-141">[Zavedení](bootstrap-company-data.md) dat Dataverse pomocí třímístného kódu společnosti pro Mezinárodní organizaci pro normalizaci (ISO).</span><span class="sxs-lookup"><span data-stu-id="5359d-141">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="5359d-142">Spusťte funkci **Počáteční synchronizace** pro tabulky, u kterých chcete synchronizovat data.</span><span class="sxs-lookup"><span data-stu-id="5359d-142">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="5359d-143">Odkazy na příklad a alternativní přístup najdete v části [Příklad](#example) dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="5359d-143">For links to an example and an alternative approach, see the [Example](#example) section later in this topic.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="5359d-144">Nová instance aplikace Finance and Operations, která má data, a nová instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="5359d-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="5359d-145">Chcete-li nastavit připojení dvojího zapisování mezi novou instancí aplikace Finance and Operations, která má ukázková data, a novou instanci aplikace pro zapojení zákazníků, postupujte podle kroků v [nové instanci aplikace Finance and Operations a v oddílu nové instance aplikace pro zapojení zákazníků](#new-new) dříve v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="5359d-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="5359d-146">Chcete-li v aplikaci synchronizovat data s aplikací pro zapojení zákazníků, postupujte po dokončení nastavení připojení následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="5359d-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="5359d-147">Otevřete aplikaci Finance and Operations ze stránky LCS, přihlaste se a pak přejděte ke **Správě dat \> Dvojí zápis**.</span><span class="sxs-lookup"><span data-stu-id="5359d-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="5359d-148">Spusťte funkci **Počáteční synchronizace** pro tabulky, u kterých chcete synchronizovat data.</span><span class="sxs-lookup"><span data-stu-id="5359d-148">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="5359d-149">Odkazy na příklad a alternativní přístup najdete v části [Příklad](#example).</span><span class="sxs-lookup"><span data-stu-id="5359d-149">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="5359d-150">Nová instance aplikace Finance and Operations, která má data, a existující instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="5359d-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="5359d-151">Chcete-li nastavit připojení dvojího zapisování mezi novou instancí aplikace Finance and Operations, která má data, a eistující instanci aplikace pro zapojení zákazníků, postupujte podle kroků v [nové instanci aplikace Finance and Operations a v oddílu existující instance aplikace pro zapojení zákazníků](#new-existing) dříve v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="5359d-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="5359d-152">Chcete-li v aplikaci synchronizovat data s aplikací pro zapojení zákazníků, postupujte po dokončení nastavení připojení následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="5359d-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="5359d-153">Otevřete aplikaci Finance and Operations ze stránky LCS, přihlaste se a pak přejděte ke **Správě dat \> Dvojí zápis**.</span><span class="sxs-lookup"><span data-stu-id="5359d-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="5359d-154">Spusťte funkci **Počáteční synchronizace** pro tabulky, u kterých chcete synchronizovat data.</span><span class="sxs-lookup"><span data-stu-id="5359d-154">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="5359d-155">Chcete-li synchronizovat existující data Dataverse s aplikací Finance and Operations, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="5359d-155">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="5359d-156">Vytvořte v aplikaci Finance and Operations novou společnost.</span><span class="sxs-lookup"><span data-stu-id="5359d-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="5359d-157">Přidejte společnost do nastavení připojení s duálním zapisováním.</span><span class="sxs-lookup"><span data-stu-id="5359d-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="5359d-158">[Zavedení](bootstrap-company-data.md) dat Dataverse pomocí třímístného kódu společnosti ISO.</span><span class="sxs-lookup"><span data-stu-id="5359d-158">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="5359d-159">Spusťte funkci **Počáteční synchronizace** pro tabulky, u kterých chcete synchronizovat data.</span><span class="sxs-lookup"><span data-stu-id="5359d-159">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="5359d-160">Odkazy na příklad a alternativní přístup najdete v části [Příklad](#example).</span><span class="sxs-lookup"><span data-stu-id="5359d-160">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="5359d-161">Existující instance aplikace Finance and Operations a nová instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="5359d-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="5359d-162">Nastavení připojení s dvojím zapisováním mezi existující instancí aplikace Finance and Operations a novou instancí aplikace pro zapojení zákazníků probíhá v prostředí Finance and Operation.</span><span class="sxs-lookup"><span data-stu-id="5359d-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="5359d-163">[Nastavit připojení z aplikace Finance and Operations](enable-dual-write.md)</span><span class="sxs-lookup"><span data-stu-id="5359d-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="5359d-164">Spusťte funkci **Počáteční synchronizace** pro tabulky, u kterých chcete synchronizovat data.</span><span class="sxs-lookup"><span data-stu-id="5359d-164">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="5359d-165">Odkazy na příklad a alternativní přístup najdete v části [Příklad](#example).</span><span class="sxs-lookup"><span data-stu-id="5359d-165">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="5359d-166">Existující instance aplikace Finance and Operations a existující instance aplikace pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="5359d-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="5359d-167">Nastavení připojení s dvojím zapisováním mezi existující instancí aplikace Finance and Operations a existující instancí aplikace pro zapojení zákazníků probíhá v prostředí Finance and Operation.</span><span class="sxs-lookup"><span data-stu-id="5359d-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="5359d-168">[Nastavit připojení z aplikace Finance and Operations](enable-dual-write.md)</span><span class="sxs-lookup"><span data-stu-id="5359d-168">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="5359d-169">Chcete-li synchronizovat existující data Dataverse s aplikací Finance and Operations, [zaveďte](bootstrap-company-data.md) data Dataverse pomocí třímístného kódu ISO společnosti.</span><span class="sxs-lookup"><span data-stu-id="5359d-169">To sync the existing Dataverse data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="5359d-170">Spusťte funkci **Počáteční synchronizace** pro tabulky, u kterých chcete synchronizovat data.</span><span class="sxs-lookup"><span data-stu-id="5359d-170">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="5359d-171">Odkazy na příklad a alternativní přístup najdete v části [Příklad](#example).</span><span class="sxs-lookup"><span data-stu-id="5359d-171">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="example"></a><span data-ttu-id="5359d-172">Příklad</span><span class="sxs-lookup"><span data-stu-id="5359d-172">Example</span></span>

<span data-ttu-id="5359d-173">Příklad viz [Povolení Customers V3 — mapa tabulek kontaktů](enable-entity-map.md#enable-table-map)</span><span class="sxs-lookup"><span data-stu-id="5359d-173">For an example, see [Enabling the Customers V3—Contacts table map](enable-entity-map.md#enable-table-map)</span></span>

<span data-ttu-id="5359d-174">Alternativní přístup založený na objemech dat v každé entitě, která musí spustit počáteční synchronizaci, najdete v části [Úvahy o počáteční synchronizaci](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="5359d-174">For an alternative approach that is based on data volumes in each entity that must run an initial synchronization, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]