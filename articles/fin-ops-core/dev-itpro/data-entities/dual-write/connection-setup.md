---
title: Podporované scénáře pro nastavení dvojího zápisu
description: Toto téma popisuje scénáře, které jsou podporovány pro nastavení dvojího zápisu.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 1319f1228b635e207754f7c2516cb2b5353a9edd
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112402"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="ad218-103">Podporované scénáře pro nastavení dvojího zápisu</span><span class="sxs-lookup"><span data-stu-id="ad218-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="ad218-104">Můžete nastavit připojení dvojího zápisu mezi prostředím Finance and Operations a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ad218-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="ad218-105">**Prostředí Finance and Operations** poskytuje základní platformu pro aplikace **Finance and Operations** (například Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail a Dynamics 365 Human Resources).</span><span class="sxs-lookup"><span data-stu-id="ad218-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="ad218-106">**Prostředí Common Data Service** poskytuje základní platformu pro **aplikace řízené modelem Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing a Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="ad218-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

<span data-ttu-id="ad218-107">Nastavení mechanismu se liší v závislosti na vašem předplatném a prostředí.</span><span class="sxs-lookup"><span data-stu-id="ad218-107">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="ad218-108">U nových instancí aplikací Finance and Operations začíná nastavení připojení dvojího zapisování v Lifecycle Services (LCS) Microsoft Dynamics.</span><span class="sxs-lookup"><span data-stu-id="ad218-108">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="ad218-109">Máte-li licenci pro Microsoft Power Platform, obdržíte nové prostředí Common Data Service, pokud je váš klient neobsahuje.</span><span class="sxs-lookup"><span data-stu-id="ad218-109">If you have a license for Microsoft Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="ad218-110">Pro existující instance aplikací Finance and Operations začíná nastavení připojení dvojího zapisování do prostředí Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ad218-110">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="ad218-111">Podporovány jsou následující scénáře registrace:</span><span class="sxs-lookup"><span data-stu-id="ad218-111">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="ad218-112">Nová instance aplikace Finance and Operations a nová instance aplikace řízené modelem</span><span class="sxs-lookup"><span data-stu-id="ad218-112">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="ad218-113">Nová instance aplikace Finance and Operations a existující instance aplikace řízené modelem</span><span class="sxs-lookup"><span data-stu-id="ad218-113">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="ad218-114">Nová instance aplikace Finance and Operations, která má ukázková data, a nová instance aplikace řízené modelem</span><span class="sxs-lookup"><span data-stu-id="ad218-114">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="ad218-115">Nová instance aplikace Finance and Operations, která má ukázková data, a existující instance aplikace řízené modelem</span><span class="sxs-lookup"><span data-stu-id="ad218-115">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="ad218-116">Existující instance aplikace Finance and Operations a nová nebo existující instance aplikace řízené modelem</span><span class="sxs-lookup"><span data-stu-id="ad218-116">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="ad218-117">Nová instance aplikace Finance and Operations a nová instance aplikace řízené modelem</span><span class="sxs-lookup"><span data-stu-id="ad218-117">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="ad218-118">Chcete-li nastavit připojení dvojího zapisování mezi novou instancí aplikace Finance and Operations, která neobsahuje žádná data a novou instanci aplikace řízené modelem v aplikaci Dynamics 365, postupujte podle kroků v [nastavení dvojího zápisu z Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="ad218-118">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="ad218-119">Po dokončení nastavení připojení dojde k automatickému provedení následujících akcí:</span><span class="sxs-lookup"><span data-stu-id="ad218-119">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="ad218-120">Je zajištěno nové prázdné prostředí Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ad218-120">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="ad218-121">Je zřízena nová prázdná instance aplikace řízené modelem, kde je nainstalováno základní řešení CRM.</span><span class="sxs-lookup"><span data-stu-id="ad218-121">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="ad218-122">Pro data společnosti DAT je vytvořeno připojení s dvojím zapisováním.</span><span class="sxs-lookup"><span data-stu-id="ad218-122">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="ad218-123">Mapování entit je povoleno pro živou synchronizaci.</span><span class="sxs-lookup"><span data-stu-id="ad218-123">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="ad218-124">Obě prostředí jsou připravena k synchronizaci dat živého vysílání.</span><span class="sxs-lookup"><span data-stu-id="ad218-124">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a><span data-ttu-id="ad218-125">Nová instance aplikace Finance and Operations a existující instance aplikace řízené modelem</span><span class="sxs-lookup"><span data-stu-id="ad218-125">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="ad218-126">Chcete-li nastavit připojení dvojího zapisování mezi novou instancí aplikace Finance and Operations, která neobsahuje žádná data a existující instanci aplikace řízené modelem v aplikaci Dynamics 365, postupujte podle kroků v [nastavení dvojího zápisu z Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="ad218-126">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="ad218-127">Po dokončení nastavení připojení dojde k automatickému provedení následujících akcí:</span><span class="sxs-lookup"><span data-stu-id="ad218-127">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="ad218-128">Je zajištěno nové prázdné prostředí Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ad218-128">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="ad218-129">Pro data společnosti DAT je vytvořeno připojení s dvojím zapisováním.</span><span class="sxs-lookup"><span data-stu-id="ad218-129">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="ad218-130">Mapování entit je povoleno pro živou synchronizaci.</span><span class="sxs-lookup"><span data-stu-id="ad218-130">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="ad218-131">Obě prostředí jsou připravena k synchronizaci dat živého vysílání.</span><span class="sxs-lookup"><span data-stu-id="ad218-131">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="ad218-132">Chcete-li synchronizovat existující data Common Data Service s aplikací Finance and Operations, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="ad218-132">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="ad218-133">Vytvořte v aplikaci Finance and Operations novou společnost.</span><span class="sxs-lookup"><span data-stu-id="ad218-133">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="ad218-134">Přidejte společnost do nastavení připojení s duálním zapisováním.</span><span class="sxs-lookup"><span data-stu-id="ad218-134">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="ad218-135">[Zavedení](bootstrap-company-data.md) dat Common Data Service pomocí třímístného kódu společnosti pro Mezinárodní organizaci pro normalizaci (ISO).</span><span class="sxs-lookup"><span data-stu-id="ad218-135">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="ad218-136">Vzhledem k tomu, že dvojí zapisování je v režimu synchronizace živého vysílání, data aplikace Common Data Service automaticky začnou proudit do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ad218-136">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a><span data-ttu-id="ad218-137">Nová instance aplikace Finance and Operations, která má ukázková data, a nová instance aplikace řízené modelem</span><span class="sxs-lookup"><span data-stu-id="ad218-137">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="ad218-138">Chcete-li nastavit připojení dvojího zapisování mezi novou instancí aplikace Finance and Operations, která má ukázková data, a novou instanci aplikace řízené modelem v aplikaci Dynamics 365, postupujte podle kroků v [nové instanci aplikace Finance and Operations a v oddílu nové instance aplikace řízené podle modelu](#new-new) dříve v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="ad218-138">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="ad218-139">Chcete-li v aplikaci synchronizovat ukázková data s aplikací řízenou modelem, postupujte po dokončení nastavení připojení následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="ad218-139">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="ad218-140">Otevřete aplikaci Finance and Operations ze stránky LCS, přihlaste se a pak přejděte ke **Správě dat \> Dvojí zápis**.</span><span class="sxs-lookup"><span data-stu-id="ad218-140">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="ad218-141">Spusťte funkci **Počáteční synchronizace** pro entity, pro které chcete synchronizovat data.</span><span class="sxs-lookup"><span data-stu-id="ad218-141">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a><span data-ttu-id="ad218-142">Nová instance aplikace Finance and Operations, která má ukázková data, a existující instance aplikace řízené modelem</span><span class="sxs-lookup"><span data-stu-id="ad218-142">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="ad218-143">Chcete-li nastavit připojení dvojího zapisování mezi novou instancí aplikace Finance and Operations, která má ukázková data, a existující instanci aplikace řízené modelem v aplikaci Dynamics 365, postupujte podle kroků v [nové instanci aplikace Finance and Operations a v existující instanci aplikace řízené podle modelu](#new-existing) dříve v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="ad218-143">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="ad218-144">Chcete-li v aplikaci synchronizovat ukázková data s aplikací řízenou modelem, postupujte po dokončení nastavení připojení následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="ad218-144">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="ad218-145">Otevřete aplikaci Finance and Operations ze stránky LCS, přihlaste se a pak přejděte ke **Správě dat \> Dvojí zápis**.</span><span class="sxs-lookup"><span data-stu-id="ad218-145">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="ad218-146">Spusťte funkci **Počáteční synchronizace** pro entity, pro které chcete synchronizovat data.</span><span class="sxs-lookup"><span data-stu-id="ad218-146">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="ad218-147">Chcete-li synchronizovat existující data Common Data Service s aplikací Finance and Operations, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="ad218-147">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="ad218-148">Vytvořte v aplikaci Finance and Operations novou společnost.</span><span class="sxs-lookup"><span data-stu-id="ad218-148">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="ad218-149">Přidejte společnost do nastavení připojení s duálním zapisováním.</span><span class="sxs-lookup"><span data-stu-id="ad218-149">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="ad218-150">[Zavedení](bootstrap-company-data.md) dat Common Data Service pomocí třímístného kódu společnosti ISO.</span><span class="sxs-lookup"><span data-stu-id="ad218-150">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="ad218-151">Vzhledem k tomu, že dvojí zapisování je v režimu synchronizace živého vysílání, data aplikace Common Data Service automaticky začnou proudit do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ad218-151">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="ad218-152">Existující instance aplikace Finance and Operations a nová nebo existující instance aplikace řízené modelem</span><span class="sxs-lookup"><span data-stu-id="ad218-152">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="ad218-153">Nastavení připojení s dvojím zapisováním mezi existující instancí aplikace Finance and Operations a novou nebo existující instancí aplikace řízené modelem v aplikaci Dynamics 365 probíhá v prostředí Finance and Operation.</span><span class="sxs-lookup"><span data-stu-id="ad218-153">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="ad218-154">Nastavit připojení z aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ad218-154">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="ad218-155">Chcete-li synchronizovat existující data Common Data Service s aplikací Finance and Operations, [zaveďte](bootstrap-company-data.md) data Common Data Service pomocí třímístného kódu ISO společnosti.</span><span class="sxs-lookup"><span data-stu-id="ad218-155">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="ad218-156">Vzhledem k tomu, že dvojí zapisování je v režimu synchronizace živého vysílání, data aplikace Common Data Service automaticky začnou proudit do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ad218-156">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
