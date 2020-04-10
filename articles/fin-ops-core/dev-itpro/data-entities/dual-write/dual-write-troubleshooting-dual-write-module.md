---
title: Poradce při potížích s modulem duálního zápisu v aplikacích Finance and Operations
description: Toto téma obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy s modulem dvojího zapisování v aplikacích Finance and Operations.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
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
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172753"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="2fcb3-103">Poradce při potížích s modulem duálního zápisu v aplikacích Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2fcb3-103">Troubleshoot issues with the Dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="2fcb3-104">Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="2fcb3-105">Konkrétně toto téma obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy s modulem **Dvojího zapisování** v aplikacích Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2fcb3-106">Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="2fcb3-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="2fcb3-107">Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="2fcb3-108">V aplikaci Finance and Operations nelze načíst modul dvojího napisování</span><span class="sxs-lookup"><span data-stu-id="2fcb3-108">You can't load the Dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="2fcb3-109">Pokud nemůžete otevřít stránku **Dvojího zapisování** výběrem dlaždice **Dvojího zapisování** v pracovním prostoru **Správa dat**, služba integrace dat je pravděpodobně mimo provoz.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="2fcb3-110">Vytvořte lístek podpory pro vyžádání restartu služby Data Integration Service.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a><span data-ttu-id="2fcb3-111">Chyba při pokusu o vytvoření nového mapování entity</span><span class="sxs-lookup"><span data-stu-id="2fcb3-111">Error when you try to create a new entity mapping</span></span>

<span data-ttu-id="2fcb3-112">**Požadovaná pověření pro opravu problému:** Správce klienta Azure AD</span><span class="sxs-lookup"><span data-stu-id="2fcb3-112">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="2fcb3-113">Při pokusu o konfiguraci nové entity pro dvojího psaní se může zobrazit následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="2fcb3-113">You might receive the following error message when you try to configure a new entity for dual-write:</span></span>

<span data-ttu-id="2fcb3-114">*Stavový kód odpovědi neoznačuje úspěch: 401 (Neautorizováno)*</span><span class="sxs-lookup"><span data-stu-id="2fcb3-114">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>

<span data-ttu-id="2fcb3-115">K této chybě dochází, protože pouze správce klenta Azure AD může přidat nové mapování entit.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-115">This error occurs because only an Azure AD tenant admin can add a new entity mapping.</span></span>

<span data-ttu-id="2fcb3-116">Chcete-li tento problém vyřešit, přihlaste se k aplikaci Finance and Operations jako správce klienta Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-116">To fix the issue, sign in to the Finance and Operations app as an Azure AD admin tenant.</span></span> <span data-ttu-id="2fcb3-117">Je také nutné přejít na web.PowerApps.com a znovu ověřit připojení.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-117">You must also go to web.PowerApps.com and revalidate your connection.</span></span>

## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="2fcb3-118">Chyba při otevření uživatelského rozhraní s dvojím zapisováním</span><span class="sxs-lookup"><span data-stu-id="2fcb3-118">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="2fcb3-119">Při pokusu o přístup dvojího zápisu z pracovního prostoru **Správa dat** se může zobrazit následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="2fcb3-119">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="2fcb3-120">*login.microsoftonline.com se odmítlo připojit.*</span><span class="sxs-lookup"><span data-stu-id="2fcb3-120">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="2fcb3-121">Chcete-li tento problém vyřešit, přihlaste se pomocí okna InPrivate v aplikaci Microsoft Edge, anonymního okna v Chromium nebo anonymního okna v Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-121">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="2fcb3-122">Je také nutné zrušit blokování nebo vymazat soubory cookie třetích stran.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-122">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="2fcb3-123">Chyba při propojení prostředí pro dvojí zapisování nebo přidání nového mapování entit</span><span class="sxs-lookup"><span data-stu-id="2fcb3-123">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="2fcb3-124">**Požadovaná pověření pro opravu problému:** Správce klienta Azure AD</span><span class="sxs-lookup"><span data-stu-id="2fcb3-124">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="2fcb3-125">Při připojování nebo vytváření map se může objevit následující chyba:</span><span class="sxs-lookup"><span data-stu-id="2fcb3-125">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="2fcb3-126">*Stavový kód odpovědi neoznačuje úspěch: 403 (tokenexchange).<br> ID relace: \<ID vaší relace\><br> ID kořenové aktivity: \<ID vaší kořenové aktivity\>*</span><span class="sxs-lookup"><span data-stu-id="2fcb3-126">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="2fcb3-127">K této chybě může dojít, pokud nemáte dostatečná oprávnění k propojení s dvojím zápisem nebo vytvářením map.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-127">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="2fcb3-128">Chcete-li propojit prostředí a přidat nová mapování entit, je nutné použít účet správce klienta Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-128">You must use an Azure AD tenant admin account to link environments and add new entity mappings.</span></span> <span data-ttu-id="2fcb3-129">Po instalaci však můžete pomocí účtu, který není účet správce, sledovat stav a upravit mapování.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-129">However, after setup, you can use a non-admin account to monitor status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="2fcb3-130">Chyba při zastavení mapování entit</span><span class="sxs-lookup"><span data-stu-id="2fcb3-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="2fcb3-131">Při pokusu o zastavení mapování entit se může zobrazit následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="2fcb3-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="2fcb3-132">*\[Zakázáno\], \[{"stav": 403, "zdroj":","zpráva":"Chyba z výměny klienta: Uživatel nemá přístup k připojení dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], vzdálený server vrátil chybu: (403) Zakázáno.*</span><span class="sxs-lookup"><span data-stu-id="2fcb3-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="2fcb3-133">K této chybě dojde, pokud propojené prostředí Common Data Service není k dispozici.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="2fcb3-134">Chcete-li tento problém vyřešit, vytvořte lístek pro tým pro integraci dat.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="2fcb3-135">Připojte sledování sítě, aby mohl tým pro integraci dat označit mapy jako **nespuštěný** na back endu.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>
