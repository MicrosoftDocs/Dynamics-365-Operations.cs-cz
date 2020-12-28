---
title: Předpoklady nastavení kanálu
description: Toto téma poskytuje přehled předpokladů nastavení kanálů v Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0da0457240cf12686fff2fa929c7fb510c11f242
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410742"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="5fc08-103">Předpoklady nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="5fc08-103">Channel setup prerequisites</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5fc08-104">Toto téma poskytuje přehled předpokladů nastavení kanálů v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5fc08-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5fc08-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="5fc08-105">Overview</span></span>

<span data-ttu-id="5fc08-106">Před vytvořením kanálu Dynamics 365 Commerce je nutné provést několik požadovaných úloh.</span><span class="sxs-lookup"><span data-stu-id="5fc08-106">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="5fc08-107">Následující seznamy požadovaných úloh jsou uspořádány podle typu kanálů.</span><span class="sxs-lookup"><span data-stu-id="5fc08-107">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="5fc08-108">Některá dokumentace se stále píše a odkazy budou aktualizovány při publikování nového obsahu.</span><span class="sxs-lookup"><span data-stu-id="5fc08-108">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="5fc08-109">Inicializace</span><span class="sxs-lookup"><span data-stu-id="5fc08-109">Initialization</span></span>

- [<span data-ttu-id="5fc08-110">Inicializovat počáteční data</span><span class="sxs-lookup"><span data-stu-id="5fc08-110">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="5fc08-111">Globální předpoklady vyžadované pro všechny typy kanálů</span><span class="sxs-lookup"><span data-stu-id="5fc08-111">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="5fc08-112">Definovat a konfigurovat strukturu právnické osoby</span><span class="sxs-lookup"><span data-stu-id="5fc08-112">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="5fc08-113">Konfigurace vaší organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="5fc08-113">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="5fc08-114">Nastavit sklad</span><span class="sxs-lookup"><span data-stu-id="5fc08-114">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="5fc08-115">Konfigurovat DPH</span><span class="sxs-lookup"><span data-stu-id="5fc08-115">Configure sales tax</span></span>](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="5fc08-116">Nastavení profilu oznámení e-mailem</span><span class="sxs-lookup"><span data-stu-id="5fc08-116">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="5fc08-117">Nastavení číselných řad</span><span class="sxs-lookup"><span data-stu-id="5fc08-117">Set up number sequences</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="5fc08-118">Nastavení výchozího zákazníka a adresáře</span><span class="sxs-lookup"><span data-stu-id="5fc08-118">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="5fc08-119">Předpoklady maloobchodní sítě</span><span class="sxs-lookup"><span data-stu-id="5fc08-119">Retail channel prerequisites</span></span>

- [<span data-ttu-id="5fc08-120">Informační kódy a skupiny informačních kódů</span><span class="sxs-lookup"><span data-stu-id="5fc08-120">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="5fc08-121">Nastavení funkčního profilu maloobchodu</span><span class="sxs-lookup"><span data-stu-id="5fc08-121">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="5fc08-122">Nastavení adresáře zaměstnanců</span><span class="sxs-lookup"><span data-stu-id="5fc08-122">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="5fc08-123">Nastavení rozvržení obrazovky</span><span class="sxs-lookup"><span data-stu-id="5fc08-123">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="5fc08-124">Nastavit hardwarovou stanici</span><span class="sxs-lookup"><span data-stu-id="5fc08-124">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="5fc08-125">Předpoklady kanálu kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="5fc08-125">Call Center channel prerequisites</span></span>

- <span data-ttu-id="5fc08-126">Parametry kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="5fc08-126">Call center parameters</span></span>
- [<span data-ttu-id="5fc08-127">Způsoby platby za objednávku a refundaci kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="5fc08-127">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="5fc08-128">Způsoby dodání a poplatků kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="5fc08-128">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="5fc08-129">Předpoklady online kanálu</span><span class="sxs-lookup"><span data-stu-id="5fc08-129">Online channel prerequisites</span></span>

- [<span data-ttu-id="5fc08-130">Vytvoření online funkčního profilu</span><span class="sxs-lookup"><span data-stu-id="5fc08-130">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="5fc08-131">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="5fc08-131">Additional resources</span></span>

[<span data-ttu-id="5fc08-132">Přehled kanálů</span><span class="sxs-lookup"><span data-stu-id="5fc08-132">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="5fc08-133">Přehled organizací a organizačních hierarchií</span><span class="sxs-lookup"><span data-stu-id="5fc08-133">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="5fc08-134">Nastavení organizačních hierarchií</span><span class="sxs-lookup"><span data-stu-id="5fc08-134">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="5fc08-135">Vytvořit právnické osoby</span><span class="sxs-lookup"><span data-stu-id="5fc08-135">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="5fc08-136">Nastavení maloobchodního kanálu</span><span class="sxs-lookup"><span data-stu-id="5fc08-136">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="5fc08-137">Nastavení online kanálu</span><span class="sxs-lookup"><span data-stu-id="5fc08-137">Set up an online channel</span></span>](channel-setup-online.md)
