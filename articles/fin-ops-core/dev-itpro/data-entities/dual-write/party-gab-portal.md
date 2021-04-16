---
title: Používání Power Portal s datovým modelem strany
description: Toto téma popisuje změny webových rolí portálu Power Portal kvůli datovému modelu strany v duálním zápisu.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: a2ea914344341ee26138e853727c551bdd5d733e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833083"
---
# <a name="using-power-portal-with-the-party-data-model"></a><span data-ttu-id="25d05-103">Používání Power Portal s datovým modelem strany</span><span class="sxs-lookup"><span data-stu-id="25d05-103">Using Power Portal with the Party data model</span></span>

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="25d05-104">Verze řešení orchestrace aplikace s duálním zápisem 2.0.999.0 a novější zahrnuje změny datového modelu strany a globálního adresáře u tabulek Účet a Kontakt.</span><span class="sxs-lookup"><span data-stu-id="25d05-104">The Dual-write application orchestration solution version 2.0.999.0 and later includes data model changes to party and global address book for the Account and Contact tables.</span></span> <span data-ttu-id="25d05-105">Změny umožňují vztahy N:N, které podporují pokročilé obchodní scénáře.</span><span class="sxs-lookup"><span data-stu-id="25d05-105">The changes allow many-to-many relationships that support advanced business scenarios.</span></span> <span data-ttu-id="25d05-106">Tyto změny nejsou podporovány webovými rolemi portálu, včetně zákaznického portálu, které jsou dodávány jako integrované nebo které ve vašem prostředí existovaly před instalací duálního zápisu.</span><span class="sxs-lookup"><span data-stu-id="25d05-106">These changes are not supported by portal web roles, including the customer portal, that are shipped out-of-the-box or that existed in your environment before you installed dual-write.</span></span> <span data-ttu-id="25d05-107">Aby webové role fungovaly podle očekávání, musíte pomocí nového datového modelu vytvořit nové webové role.</span><span class="sxs-lookup"><span data-stu-id="25d05-107">For the web roles to work as expected, you need to create new web roles using the new data model.</span></span> 

<span data-ttu-id="25d05-108">Stručně řečeno, změnil se způsob interakce tabulek, ale oprávnění k tabulkám na zákaznickém portálu se nezměnila.</span><span class="sxs-lookup"><span data-stu-id="25d05-108">In summary, the way the tables interact has changed, but the table permissions in the customer portal haven't changed.</span></span> <span data-ttu-id="25d05-109">Toto téma vysvětluje, jak vytvořit nové webové role, které fungují s novým rozšířeným datovým modelem.</span><span class="sxs-lookup"><span data-stu-id="25d05-109">This topic explains how to create new web roles that work with the new advanced data model.</span></span>

<span data-ttu-id="25d05-110">Tento diagram ukazuje relaci tabulky **bez** datového modelu strany a globálního adresáře:</span><span class="sxs-lookup"><span data-stu-id="25d05-110">This diagram shows the table relationship **without** the party and global address book data model:</span></span>

   ![bez modelu strany](media/without-party-model.PNG)

<span data-ttu-id="25d05-112">Tento diagram ukazuje relaci tabulky **s** datovým modelem strany a globálního adresáře:</span><span class="sxs-lookup"><span data-stu-id="25d05-112">This diagram shows the table relationship **with** the party and global address book data model:</span></span>

   ![s modelem strany](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a><span data-ttu-id="25d05-114">Vytvořte nové oprávnění k tabulce</span><span class="sxs-lookup"><span data-stu-id="25d05-114">Create a new table permission</span></span>

<span data-ttu-id="25d05-115">Chcete-li vytvořit tato nová oprávnění k tabulce, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="25d05-115">To create these new table permissions, follow these steps:</span></span>

1. <span data-ttu-id="25d05-116">Přihlaste se do [Power Apps](https://make.powerapps.com) a přejděte do svých aplikací.</span><span class="sxs-lookup"><span data-stu-id="25d05-116">Sign in to [Power Apps](https://make.powerapps.com), and go to your apps.</span></span>
2. <span data-ttu-id="25d05-117">Vyberte aplikaci pro správu portálu.</span><span class="sxs-lookup"><span data-stu-id="25d05-117">Select your Portal Management app.</span></span>
3. <span data-ttu-id="25d05-118">Na postranním panelu vyberte možnost **Zabezpečení > Oprávnění tabulky**.</span><span class="sxs-lookup"><span data-stu-id="25d05-118">In the side bar, select **Security > Table permissions**.</span></span>

    <span data-ttu-id="25d05-119">Musíte vytvořit tři nová oprávnění:</span><span class="sxs-lookup"><span data-stu-id="25d05-119">You must create three new permissions:</span></span>

    + <span data-ttu-id="25d05-120">Spojení kontakt – strana</span><span class="sxs-lookup"><span data-stu-id="25d05-120">Contact to Party connection</span></span>
    + <span data-ttu-id="25d05-121">Spojení strana – účet</span><span class="sxs-lookup"><span data-stu-id="25d05-121">Party to Account connection</span></span>
    + <span data-ttu-id="25d05-122">Spojení účet – objednávka</span><span class="sxs-lookup"><span data-stu-id="25d05-122">Account to Order connection</span></span>

4. <span data-ttu-id="25d05-123">Vytvořte a uložte nové oprávnění pro spojení kontakt – strana a nastavte tyto parametry:</span><span class="sxs-lookup"><span data-stu-id="25d05-123">Create and save a new permission for the Contact to Party connection, setting these parameters:</span></span>

    + <span data-ttu-id="25d05-124">**Název**: Spojení strana – účet (nebo podle vašeho výběru)</span><span class="sxs-lookup"><span data-stu-id="25d05-124">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="25d05-125">**Název tabulky**: msdyn_contactforparty</span><span class="sxs-lookup"><span data-stu-id="25d05-125">**Table Name**: msdyn_contactforparty</span></span>
    + <span data-ttu-id="25d05-126">**Web**: Zákaznický portál</span><span class="sxs-lookup"><span data-stu-id="25d05-126">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="25d05-127">**Rozsah**: Kontakt</span><span class="sxs-lookup"><span data-stu-id="25d05-127">**Scope**: Contact</span></span>
    + <span data-ttu-id="25d05-128">**Oprávnění**: Vybrat vše</span><span class="sxs-lookup"><span data-stu-id="25d05-128">**Privileges**: Select all</span></span>
    + <span data-ttu-id="25d05-129">**Webové role**: Ověření uživatelé, Zástupce zákazníka (nebo podle vašeho výběru)</span><span class="sxs-lookup"><span data-stu-id="25d05-129">**Web roles**: Authenticated Users, Customer Representative (or your choice)</span></span>

5. <span data-ttu-id="25d05-130">Vytvořte a uložte nové oprávnění pro spojení strana – účet a nastavte tyto parametry:</span><span class="sxs-lookup"><span data-stu-id="25d05-130">Create and save a new permission for the Party to Account connection, setting these parameters:</span></span>

    + <span data-ttu-id="25d05-131">**Název**: Spojení strana – účet (nebo podle vašeho výběru)</span><span class="sxs-lookup"><span data-stu-id="25d05-131">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="25d05-132">**Název tabulky**: account</span><span class="sxs-lookup"><span data-stu-id="25d05-132">**Table Name**: account</span></span>
    + <span data-ttu-id="25d05-133">**Web**: Zákaznický portál</span><span class="sxs-lookup"><span data-stu-id="25d05-133">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="25d05-134">**Rozsah**: Nadřazený objekt</span><span class="sxs-lookup"><span data-stu-id="25d05-134">**Scope**: Parent</span></span>
    + <span data-ttu-id="25d05-135">**Oprávnění**: Vybrat vše</span><span class="sxs-lookup"><span data-stu-id="25d05-135">**Privileges**: Select all</span></span>
    + <span data-ttu-id="25d05-136">**Oprávnění nadřazené tabulky**: Spojení kontakt – strana</span><span class="sxs-lookup"><span data-stu-id="25d05-136">**Parent Table Permission**: Contact to Party Connection</span></span>

6. <span data-ttu-id="25d05-137">Vytvořte a uložte nové oprávnění pro spojení účet – objednávka a nastavte tyto parametry:</span><span class="sxs-lookup"><span data-stu-id="25d05-137">Create and save a new permission for the Account to Order connection, setting these parameters:</span></span>

    + <span data-ttu-id="25d05-138">**Název**: Spojení účet – objednávka (nebo podle vašeho výběru)</span><span class="sxs-lookup"><span data-stu-id="25d05-138">**Name**: Account to Order Connection (or your choice)</span></span>
    + <span data-ttu-id="25d05-139">**Název tabulky**: salesorder</span><span class="sxs-lookup"><span data-stu-id="25d05-139">**Table Name**: salesorder</span></span>
    + <span data-ttu-id="25d05-140">**Web**: Zákaznický portál</span><span class="sxs-lookup"><span data-stu-id="25d05-140">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="25d05-141">**Rozsah**: Nadřazený objekt</span><span class="sxs-lookup"><span data-stu-id="25d05-141">**Scope**: Parent</span></span>
    + <span data-ttu-id="25d05-142">**Oprávnění**: Vybrat vše</span><span class="sxs-lookup"><span data-stu-id="25d05-142">**Privileges**: Select all</span></span>
    + <span data-ttu-id="25d05-143">**Oprávnění nadřazené tabulky**: Spojení strana – účet</span><span class="sxs-lookup"><span data-stu-id="25d05-143">**Parent Table Permission**: Party to Account Connection</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
