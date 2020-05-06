---
title: Začínáme se službou nákladového účetnictví
description: V tomto tématu jsou uvedeny podrobné informace o licencích a pokyny k instalaci služby nákladového účetnictví.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: cbbce7eaac264973bf0b95ad5175bf70ed2b4ae9
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276896"
---
# <a name="get-started-with-the-cost-accounting-service"></a><span data-ttu-id="27b4d-103">Začínáme se službou nákladového účetnictví</span><span class="sxs-lookup"><span data-stu-id="27b4d-103">Get started with the cost accounting service</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="27b4d-104">Tato funkce popsaná v tomto tématu je k dispozici jako součást soukromé verze Preview.</span><span class="sxs-lookup"><span data-stu-id="27b4d-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="27b4d-105">Obsah tohoto tématu a funkce, které popisuje, se mohou změnit.</span><span class="sxs-lookup"><span data-stu-id="27b4d-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="27b4d-106">Další informace o předchozích verzích naleznete v tématu [Často kladené dotazy k aktualizacím služby One Version](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="27b4d-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="27b4d-107">Služba nákladového účetnictví umožňuje provádět účetnictví pro více skladů ve vámi vytvořených hlavních knihách nákladového účetnictví.</span><span class="sxs-lookup"><span data-stu-id="27b4d-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="27b4d-108">Jednotlivé hlavní knihy nákladového účetnictví se přidružují ke *konvencím*.</span><span class="sxs-lookup"><span data-stu-id="27b4d-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="27b4d-109">Konvence je kolekce následujících typů zásad účetnictví:</span><span class="sxs-lookup"><span data-stu-id="27b4d-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="27b4d-110">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="27b4d-110">Cost object</span></span>
- <span data-ttu-id="27b4d-111">Základ pro měření vstupu</span><span class="sxs-lookup"><span data-stu-id="27b4d-111">Input measurement basis</span></span>
- <span data-ttu-id="27b4d-112">Předpoklad toku nákladů</span><span class="sxs-lookup"><span data-stu-id="27b4d-112">Cost flow assumption</span></span>
- <span data-ttu-id="27b4d-113">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="27b4d-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="27b4d-114">I po zapnutí služby nákladového účetnictví můžete v systému Microsoft Dynamics 365 Supply Chain Management stále provádět skladové účetnictví obvyklým způsobem.</span><span class="sxs-lookup"><span data-stu-id="27b4d-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="27b4d-115">Služba nákladového účetnictví je doplněk.</span><span class="sxs-lookup"><span data-stu-id="27b4d-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="27b4d-116">Chcete-li zpřístupnit její funkce, musíte ji nainstalovat z Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="27b4d-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="27b4d-117">Proto ji můžete vyhodnotit v testovacím prostředí před tím, než ji zapnete v provozním prostředí.</span><span class="sxs-lookup"><span data-stu-id="27b4d-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="27b4d-118">Služba nákladového účetnictví aktuálně nepodporuje všechny funkce správy nákladů, které jsou integrovány v aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="27b4d-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="27b4d-119">Proto je důležité, abyste vyhodnotili, zda sada funkcí, která je aktuálně k dispozici, bude vyhovovat vašim požadavkům.</span><span class="sxs-lookup"><span data-stu-id="27b4d-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="licensing"></a><span data-ttu-id="27b4d-120">Licence</span><span class="sxs-lookup"><span data-stu-id="27b4d-120">Licensing</span></span>

<span data-ttu-id="27b4d-121">Služba nákladového účetnictví je licencována společně se standardními funkcemi skladového účetnictví, které jsou k dispozici pro řešení Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="27b4d-121">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="27b4d-122">Chcete-li používat službu nákladového účetnictví, nemusíte kupovat další licenci.</span><span class="sxs-lookup"><span data-stu-id="27b4d-122">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><span data-ttu-id="27b4d-123">Instalace doplňku</span><span class="sxs-lookup"><span data-stu-id="27b4d-123">Install the add-in</span></span>

> [!IMPORTANT]
> <span data-ttu-id="27b4d-124">Chcete-li použít službu nákladového účetnictví, je nutné mít prostředí LCS s vysokou dostupností (nikoli prostředí OneBox) a musíte používat Dynamics 365 Supply Chain Management verze 10.0.11 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="27b4d-124">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="27b4d-125">Chcete-li použít službu nákladového účetnictví, nainstalujte doplněk služby nákladového účetnictví pro Supply Chain Management, jak je popsáno v následujícím postupu.</span><span class="sxs-lookup"><span data-stu-id="27b4d-125">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="27b4d-126">Přihlaste se do LCS.</span><span class="sxs-lookup"><span data-stu-id="27b4d-126">Sign in to LCS.</span></span>

1. <span data-ttu-id="27b4d-127">Přejděte na **Správu funkcí Preview**.</span><span class="sxs-lookup"><span data-stu-id="27b4d-127">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="27b4d-128">Vyberte znaménko plus (**+**).</span><span class="sxs-lookup"><span data-stu-id="27b4d-128">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="27b4d-129">Do pole **Kód** zadejte pro službu nákladového účetnictví svůj beta klíč pro doplněk.</span><span class="sxs-lookup"><span data-stu-id="27b4d-129">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="27b4d-130">(Váš klíč by měl být doručen e-mailem.)</span><span class="sxs-lookup"><span data-stu-id="27b4d-130">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="27b4d-131">Vyberte **Odblokovat**.</span><span class="sxs-lookup"><span data-stu-id="27b4d-131">Select **Unblock**.</span></span>

1. <span data-ttu-id="27b4d-132">Otevřete prostředí LCS, do kterého chcete službu přidat.</span><span class="sxs-lookup"><span data-stu-id="27b4d-132">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="27b4d-133">Přejděte na **Úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="27b4d-133">Go to **Full details**.</span></span>

1. <span data-ttu-id="27b4d-134">Přejděte na záložku s náhledem **Doplňky prostředí**.</span><span class="sxs-lookup"><span data-stu-id="27b4d-134">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="27b4d-135">Vyberte možnost **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="27b4d-135">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="27b4d-136">Vyberte **Služba nákladového účetnictví**.</span><span class="sxs-lookup"><span data-stu-id="27b4d-136">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="27b4d-137">Postupujte podle pokynů instalační příručky a vyjádřete souhlas s podmínkami a ujednáními.</span><span class="sxs-lookup"><span data-stu-id="27b4d-137">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="27b4d-138">Vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="27b4d-138">Select **Install**.</span></span>

1. <span data-ttu-id="27b4d-139">Na záložce s náhledem **Doplňky prostředí** byste měli vidět, že je instalována služba nákladového účetnictví.</span><span class="sxs-lookup"><span data-stu-id="27b4d-139">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="27b4d-140">Po několika minutách by se stav měl změnit z **Probíhá instalace** na **Nainstalováno**.</span><span class="sxs-lookup"><span data-stu-id="27b4d-140">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="27b4d-141">(Tato změna se může projevit až po aktualizaci stránky.) V tomto okamžiku je služba nákladového účetnictví připravena k použití.</span><span class="sxs-lookup"><span data-stu-id="27b4d-141">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="27b4d-142">Nastavení integrace</span><span class="sxs-lookup"><span data-stu-id="27b4d-142">Set up the integration</span></span>

<span data-ttu-id="27b4d-143">Chcete-li nastavit integraci mezi službou nákladového účetnictví a Dynamics 365 Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="27b4d-143">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="27b4d-144">Přejděte do nabídky **Správa systému > Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="27b4d-144">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="27b4d-145">Vyberte možnost **Zkontrolovat aktualizace**.</span><span class="sxs-lookup"><span data-stu-id="27b4d-145">Select **Check for updates**.</span></span>

1. <span data-ttu-id="27b4d-146">Otevřete kartu **Vše** a vyhledejte funkci nazvanou *Služba nákladového účetnictví*.</span><span class="sxs-lookup"><span data-stu-id="27b4d-146">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="27b4d-147">Vyberte **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="27b4d-147">Select **Enable now**.</span></span>

1. <span data-ttu-id="27b4d-148">Přejděte do nabídky **Nákladové účetnictví > Služba nákladového účetnictví > Nastavení > Parametry služby nákladového účetnictví > Parametry integrace**.</span><span class="sxs-lookup"><span data-stu-id="27b4d-148">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="27b4d-149">V poli **ID aplikace** zadejte následující kód:</span><span class="sxs-lookup"><span data-stu-id="27b4d-149">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="27b4d-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="27b4d-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="27b4d-151">Do pole **Koncový bod datové služby** zadejte následující adresu URL:</span><span class="sxs-lookup"><span data-stu-id="27b4d-151">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="27b4d-152">Do pole **Koncový bod nákladového účetnictví** zadejte následující adresu URL:</span><span class="sxs-lookup"><span data-stu-id="27b4d-152">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="27b4d-153">Služba nákladového účetnictví je nyní připravena k použití.</span><span class="sxs-lookup"><span data-stu-id="27b4d-153">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="27b4d-154">Související prostředky</span><span class="sxs-lookup"><span data-stu-id="27b4d-154">Related resources</span></span>

[<span data-ttu-id="27b4d-155">Domovská stránka služby nákladového účetnictví</span><span class="sxs-lookup"><span data-stu-id="27b4d-155">Cost accounting service home page</span></span>](cost-accounting-service-home.md)
