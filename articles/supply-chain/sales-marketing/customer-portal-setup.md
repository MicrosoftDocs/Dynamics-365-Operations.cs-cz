---
title: Instalace, nastavení a aktualizace zákaznického portálu
description: V tomto tématu jsou uvedeny podrobné informace o licencích a pokyny k nastavení zákaznického portálu.
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 0343100362c4d7bc3e09334fb7890919bdb84941
ms.sourcegitcommit: 7d943499f302298c6ff127f56cecc34af6cee289
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435600"
---
# <a name="install-set-up-and-update-the-customer-portal"></a><span data-ttu-id="69c38-103">Instalace, nastavení a aktualizace zákaznického portálu</span><span class="sxs-lookup"><span data-stu-id="69c38-103">Install, set up, and update the Customer portal</span></span>

## <a name="licensing-requirements"></a><span data-ttu-id="69c38-104">Požadavky na licence</span><span class="sxs-lookup"><span data-stu-id="69c38-104">Licensing requirements</span></span>

<span data-ttu-id="69c38-105">Chcete-li implementovat zákaznický portál, musíte mít následující licence:</span><span class="sxs-lookup"><span data-stu-id="69c38-105">To implement the Customer portal, you must have the following licenses:</span></span>

- <span data-ttu-id="69c38-106">**Portály Power Apps** - Tato licence je nutná k hostování zákaznického portálu.</span><span class="sxs-lookup"><span data-stu-id="69c38-106">**Power Apps portals** – This license is required to host the Customer portal.</span></span> <span data-ttu-id="69c38-107">Portály jsou licencovány na základě použití.</span><span class="sxs-lookup"><span data-stu-id="69c38-107">Portals are licensed based on usage.</span></span> <span data-ttu-id="69c38-108">Pro více informací viz [Licenční požadavky na portály Power Apps](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span><span class="sxs-lookup"><span data-stu-id="69c38-108">For more information, see the [Power Apps portals licensing requirements](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span></span>
- <span data-ttu-id="69c38-109">**Dvojí zápis** - Musíte mít potřebné licence, abyste mohli aktivovat dvojí zápis pro entity Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="69c38-109">**Dual-write** – You must have the necessary licenses to enable dual-write for Supply Chain Management entities.</span></span> <span data-ttu-id="69c38-110">Další informace naleznete v tématu [Systémové požadavky pro dvojí zápis](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span><span class="sxs-lookup"><span data-stu-id="69c38-110">For more information, see the [system requirements for dual-write](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span></span>

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a><span data-ttu-id="69c38-111">Závislosti na dvojím zápisu a portálech Power Apps</span><span class="sxs-lookup"><span data-stu-id="69c38-111">Dependencies on dual-write and Power Apps portals</span></span>

<span data-ttu-id="69c38-112">Zákaznický portál závisí na portálech Power Apps a duálním zápisu, jak ukazuje následující obrázek.</span><span class="sxs-lookup"><span data-stu-id="69c38-112">The Customer portal depends on Power Apps portals and dual-write, as shown in the following illustration.</span></span>

<span data-ttu-id="69c38-113">![Závislosti zákaznického portálu](media/customer-portal-elements.png "Závislosti zákaznického portálu")</span><span class="sxs-lookup"><span data-stu-id="69c38-113">![Customer portal dependencies](media/customer-portal-elements.png "Customer portal dependencies")</span></span>

<span data-ttu-id="69c38-114">Na rozdíl od jiných funkcí Supply Chain Management sídlí šablona zákaznického portálu v portálech Power Apps.</span><span class="sxs-lookup"><span data-stu-id="69c38-114">Unlike other features from Supply Chain Management, the Customer portal template resides in Power Apps portals.</span></span> <span data-ttu-id="69c38-115">Zákaznický portál je proto omezen funkcemi a možnostmi, které poskytují portály Power Apps a entity v dvojím zápisu.</span><span class="sxs-lookup"><span data-stu-id="69c38-115">Therefore, the Customer portal is limited by the functionality and capabilities that are provided by Power Apps portals and the entities in dual-write.</span></span>

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a><span data-ttu-id="69c38-116">Požadované nastavení pro aktivaci zákaznického portálu</span><span class="sxs-lookup"><span data-stu-id="69c38-116">Required setup to enable the Customer portal</span></span>

<span data-ttu-id="69c38-117">Poté, co jste se ujistili, že máte požadované licence, můžete nastavit duální zápis, jak je popsáno v [pokynech pro počáteční synchronizaci s dvojím zápisem](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span><span class="sxs-lookup"><span data-stu-id="69c38-117">After you've made sure that you have the required licenses, you can set up dual-write as described in the [dual-write initial synchronization instructions](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span></span>

<span data-ttu-id="69c38-118">U duálního zápisu nezapomeňte povolit následující mapování entit:</span><span class="sxs-lookup"><span data-stu-id="69c38-118">Be sure to enable the following entity mappings in dual-write:</span></span>

- <span data-ttu-id="69c38-119">Záhlaví prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="69c38-119">Sales Order Header</span></span>
- <span data-ttu-id="69c38-120">Detaily prod. objednávky</span><span class="sxs-lookup"><span data-stu-id="69c38-120">Sales Order Details</span></span>
- <span data-ttu-id="69c38-121">Účty</span><span class="sxs-lookup"><span data-stu-id="69c38-121">Accounts</span></span>
- <span data-ttu-id="69c38-122">Kontakty</span><span class="sxs-lookup"><span data-stu-id="69c38-122">Contacts</span></span>
- <span data-ttu-id="69c38-123">Produkty</span><span class="sxs-lookup"><span data-stu-id="69c38-123">Products</span></span>

<span data-ttu-id="69c38-124">Po dokončení tohoto nastavení můžete poskytnout šablonu zákaznického portálu.</span><span class="sxs-lookup"><span data-stu-id="69c38-124">After this setup is completed, you can provision the Customer portal template.</span></span>

## <a name="provision-the-customer-portal"></a><span data-ttu-id="69c38-125">Zřízení zákaznického portálu</span><span class="sxs-lookup"><span data-stu-id="69c38-125">Provision the Customer portal</span></span>

<span data-ttu-id="69c38-126">Než začnete, ujistěte se, že jste již dokončili [požadované nastavení](#required-setup).</span><span class="sxs-lookup"><span data-stu-id="69c38-126">Before you begin, make sure that you've already completed the [required setup](#required-setup).</span></span> <span data-ttu-id="69c38-127">Poté postupujte podle těchto pokynů a vytvořte zákaznický portál.</span><span class="sxs-lookup"><span data-stu-id="69c38-127">Then follow these steps to provision the Customer portal.</span></span>

1. <span data-ttu-id="69c38-128">Přejděte na [make.powerapps.com](https://make.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="69c38-128">Go to [make.powerapps.com](https://make.powerapps.com/).</span></span>
2. <span data-ttu-id="69c38-129">Ujistěte se, že používáte prostředí, ve kterém jste povolili duální zápis.</span><span class="sxs-lookup"><span data-stu-id="69c38-129">Make sure that you're using the environment where you enabled dual-write.</span></span>
3. <span data-ttu-id="69c38-130">Na kartě **Vytvořit** přejděte dolů do sekce **Začít od šablony** a vyberte šablonu s názvem **Zákaznický portál**.</span><span class="sxs-lookup"><span data-stu-id="69c38-130">On the **Create** tab, scroll down to the **Start from template** section, and select the template that is named **Customer Portal**.</span></span>
4. <span data-ttu-id="69c38-131">Postupujte podle pokynů na obrazovce.</span><span class="sxs-lookup"><span data-stu-id="69c38-131">Follow the on-screen instructions.</span></span>

<span data-ttu-id="69c38-132">Po dokončení zřizování máte přístup na zákaznický portál v části **Vaše aplikace** na **Domovské** stránce.</span><span class="sxs-lookup"><span data-stu-id="69c38-132">After provisioning is completed, you can access the Customer portal in the **Your apps** section of the **Home** page.</span></span>

> [!NOTE]
> <span data-ttu-id="69c38-133">Pokud řešení duálního zápisu není nainstalované v prostředí, ve kterém pracujete, zobrazí se chybová zpráva a zákaznický portál nebude zajištěn.</span><span class="sxs-lookup"><span data-stu-id="69c38-133">If the dual-write solution isn't installed in the environment that you're working in, you will receive an error message, and the Customer portal won't be provisioned.</span></span>

## <a name="update-the-customer-portal"></a><span data-ttu-id="69c38-134">Aktualizace zákaznického portálu</span><span class="sxs-lookup"><span data-stu-id="69c38-134">Update the Customer portal</span></span>

<span data-ttu-id="69c38-135">Další funkce mohou být přidány do zákaznického portálu později.</span><span class="sxs-lookup"><span data-stu-id="69c38-135">More functionality might be added to the Customer portal later.</span></span> <span data-ttu-id="69c38-136">Jakékoli změny, které společnost Microsoft provede u základních komponent řešení, se automaticky objeví ve vašem prostředí.</span><span class="sxs-lookup"><span data-stu-id="69c38-136">Any changes that Microsoft makes to the underlying solution components will automatically appear in your environment.</span></span> <span data-ttu-id="69c38-137">Web poskytnutý ve vašem prostředí však nebude automaticky odrážet změny provedené v konfiguračních datech.</span><span class="sxs-lookup"><span data-stu-id="69c38-137">However, the website that is provisioned in your environment won't automatically reflect changes that are made to the configuration data.</span></span> <span data-ttu-id="69c38-138">Tyto změny budete muset použít ručně tak, že získáte kód z nové šablony a sloučíte jej s poskytnutým webem.</span><span class="sxs-lookup"><span data-stu-id="69c38-138">You will have to manually apply those changes by getting the code from the new template and merging it with the provisioned website.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="69c38-139">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="69c38-139">Additional resources</span></span>

<span data-ttu-id="69c38-140">Chcete-li se dozvědět, jak můžete nastavit a přizpůsobit zákaznický portál, měli byste začít prostudováním následující dokumentace pro základní technologie:</span><span class="sxs-lookup"><span data-stu-id="69c38-140">To learn how you can set up and customize the Customer portal, you should start by reviewing the following documentation for the underlying technologies:</span></span>

- [<span data-ttu-id="69c38-141">Dokumentace portálů Power Apps</span><span class="sxs-lookup"><span data-stu-id="69c38-141">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="69c38-142">Dokumentace dvojitého zápisu</span><span class="sxs-lookup"><span data-stu-id="69c38-142">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

<span data-ttu-id="69c38-143">Abyste mohli účinně spravovat své portály, musíte porozumět portálům Power Apps a životním cyklům Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="69c38-143">To effectively manage your portals, you must understand the Power Apps portals and Common Data Service lifecycle.</span></span> <span data-ttu-id="69c38-144">Další informace naleznete v následujících zdrojích:</span><span class="sxs-lookup"><span data-stu-id="69c38-144">For more information, see the following resources:</span></span>

- [<span data-ttu-id="69c38-145">O životním cyklu portálu</span><span class="sxs-lookup"><span data-stu-id="69c38-145">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="69c38-146">Upgradujte portál</span><span class="sxs-lookup"><span data-stu-id="69c38-146">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="69c38-147">Migrace konfigurace portálu</span><span class="sxs-lookup"><span data-stu-id="69c38-147">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="69c38-148">Správa životního cyklu řešení: aplikace Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="69c38-148">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)
