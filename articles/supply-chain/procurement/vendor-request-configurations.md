---
title: Konfigurace oslovení dodavatele
description: Toto téma popisuje pole, která je třeba vygenerovat v novém oslovení dodavatele.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: d238e0dbb754e88dcffa171456aa0a2336238cab
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "332511"
---
# <a name="vendor-request-configurations"></a><span data-ttu-id="7246e-103">Konfigurace oslovení dodavatele</span><span class="sxs-lookup"><span data-stu-id="7246e-103">Vendor request configurations</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="7246e-104">Pro dokončení oslovení dodavatele musí kontaktní osoba dodavatele dokončit průvodce registrace potenciálního dodavatele.</span><span class="sxs-lookup"><span data-stu-id="7246e-104">To complete a vendor request, a vendor contact person must complete the prospective vendor registration wizard.</span></span>

<span data-ttu-id="7246e-105">Ve formuláři **Konfigurace oslovení dodavatele**, můžete vytvořit profily určující požadovaná pole a pole viditelná v průvodci registrace potenciálního dodavatele.</span><span class="sxs-lookup"><span data-stu-id="7246e-105">In the **Vendor request configurations** form, you can create profiles that specify required fields and visible fields in the prospective vendor registration wizard.</span></span>

<span data-ttu-id="7246e-106">Průvodce registrace potenciálního dodavatele se spustí dotazem na uživatele potenciálního dodavatele, ve které zemi/oblasti dodavatel podniká.</span><span class="sxs-lookup"><span data-stu-id="7246e-106">The vendor registration wizard will start out by asking the prospective vendor user which country/region the vendor is doing business in.</span></span> <span data-ttu-id="7246e-107">Tato informace určuje použitelnou konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="7246e-107">This information determines the applicable configuration.</span></span> <span data-ttu-id="7246e-108">Pokud není žádná konfigurace určena pro zemi nebo oblast, použije se výchozí konfigurace.</span><span class="sxs-lookup"><span data-stu-id="7246e-108">If no specific configuration is defined for a country/region, a default configuration will be used.</span></span>

### <a name="set-up-a-vendor-request-configuration"></a><span data-ttu-id="7246e-109">Nastavení konfigurace oslovení dodavatele</span><span class="sxs-lookup"><span data-stu-id="7246e-109">Set up a vendor request configuration</span></span>

<span data-ttu-id="7246e-110">Ve výchozím nastavení je konfigurace dodavatele k dispozici ve formuláři Konfigurace oslovení dodavatele.</span><span class="sxs-lookup"><span data-stu-id="7246e-110">By default, there is a vendor configuration available in the Vendor request configurations form.</span></span>

<span data-ttu-id="7246e-111">Nelze vybrat země/oblasti pro výchozí konfiguraci, takže nelze změnit část **Země/oblasti**.</span><span class="sxs-lookup"><span data-stu-id="7246e-111">It is not possible to select country/regions for the default configuration, so the **Countries/regions** section cannot be changed.</span></span>

1. <span data-ttu-id="7246e-112">Klikněte na **Zásobování a zdroje** > **Nastavení** > **Dodavateée**a klikněte na **Konfigurace oslovení dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="7246e-112">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2. <span data-ttu-id="7246e-113">Klikněte na kartu **Pole** pro nastavení stavu uvedených polích.</span><span class="sxs-lookup"><span data-stu-id="7246e-113">Click the **Fields** tab to set the status of the listed fields.</span></span>
3. <span data-ttu-id="7246e-114">Skryté (není viditelné)</span><span class="sxs-lookup"><span data-stu-id="7246e-114">Hidden (Not visible)</span></span>
4. <span data-ttu-id="7246e-115">Zobrazené (viditelné, ale nepovinné)</span><span class="sxs-lookup"><span data-stu-id="7246e-115">Displayed (Visible but not mandatory)</span></span>
5. <span data-ttu-id="7246e-116">Požadované (viditelné a povinné)</span><span class="sxs-lookup"><span data-stu-id="7246e-116">Required (Visible and mandatory)</span></span>
6. <span data-ttu-id="7246e-117">Klikněte na kartu **Obsah** a určete, zda text bude zobrazený v průvodci a zda se má zobrazovat potvrzení o nutnosti přijetí uživatelem potenciálního dodavatele předtím, že se v průvodci přesune na další krok.</span><span class="sxs-lookup"><span data-stu-id="7246e-117">Click the **Content** tab to specify if text is going to be shown on the wizard and if there should be an acknowledgement that the prospective vendor user must accept this before moving to the next step in the wizard.</span></span> <span data-ttu-id="7246e-118">Potvrzení bude požadováno pro všechny smluvní podmínky, které musí uživatel potvrdit, aby mohl pokračovat.</span><span class="sxs-lookup"><span data-stu-id="7246e-118">The acknowledgement will be requested for any terms and conditions that the user must accept to continue.</span></span>

<span data-ttu-id="7246e-119">Lze také zadat potvrzovací zprávu, která se zobrazí po dokončení průvodce, a můžete přidat jeden nebo více dotazníků.</span><span class="sxs-lookup"><span data-stu-id="7246e-119">You can also enter a confirmation message that will be displayed when the wizard is finalized, and you can add one or more questionnaires.</span></span>

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a><span data-ttu-id="7246e-120">Vytvoření konfigurace dodavatele pro určitou zemi/oblast</span><span class="sxs-lookup"><span data-stu-id="7246e-120">Create a vendor configuration for a specific country/region</span></span>
1.  <span data-ttu-id="7246e-121">Klikněte na **Zásobování a zdroje** > **Nastavení** > **Dodavateée**a klikněte na **Konfigurace oslovení dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="7246e-121">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="7246e-122">Klikněte na tlačítko **Nový** pro vytvoření nové konfigurace a zadejte název konfigurace.</span><span class="sxs-lookup"><span data-stu-id="7246e-122">Click **New** to create a new configuration, and provide a name for the configuration.</span></span>
3.  <span data-ttu-id="7246e-123">Klikněte na tlačítko **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="7246e-123">Click **Save**.</span></span>
4.  <span data-ttu-id="7246e-124">Otevřete kartu **Země/oblasti** a vyberte zemi nebo oblast, pro kterou má být použita konfigurace.</span><span class="sxs-lookup"><span data-stu-id="7246e-124">Open the **Country/regions** tab to select the country/region that the configuration should be used for.</span></span>
5.  <span data-ttu-id="7246e-125">Dokončete konfiguraci podle následujících pokynů pro výchozí konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="7246e-125">Complete the configuration by following the guidelines for the default configuration.</span></span>

