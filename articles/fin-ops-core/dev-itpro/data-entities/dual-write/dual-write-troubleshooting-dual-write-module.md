---
title: Poradce při potížích s modulem dvojitého zápisu v aplikacích Finance and Operations
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2241e7e6219f95115f55bc45a4d94550276e1e21
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683616"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="93c5e-103">Poradce při potížích s modulem dvojitého zápisu v aplikacích Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="93c5e-103">Troubleshoot issues with the dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="93c5e-104">Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="93c5e-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="93c5e-105">Konkrétně toto téma obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy s modulem **Dvojího zapisování** v aplikacích Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="93c5e-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="93c5e-106">Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="93c5e-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="93c5e-107">Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.</span><span class="sxs-lookup"><span data-stu-id="93c5e-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="93c5e-108">V aplikaci Finance and Operations nelze načíst modul dvojitého zápisu</span><span class="sxs-lookup"><span data-stu-id="93c5e-108">You can't load the dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="93c5e-109">Pokud nemůžete otevřít stránku **Dvojího zapisování** výběrem dlaždice **Dvojího zapisování** v pracovním prostoru **Správa dat**, služba integrace dat je pravděpodobně mimo provoz.</span><span class="sxs-lookup"><span data-stu-id="93c5e-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="93c5e-110">Vytvořte lístek podpory pro vyžádání restartu služby Data Integration Service.</span><span class="sxs-lookup"><span data-stu-id="93c5e-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-table-map"></a><span data-ttu-id="93c5e-111">Chyba při pokusu o vytvoření nového mapování tabulky</span><span class="sxs-lookup"><span data-stu-id="93c5e-111">Error when you try to create a new table map</span></span>

<span data-ttu-id="93c5e-112">**Požadovaná pověření pro opravu problému:** Stejný uživatel, který má nastaven dvojitý zápis.</span><span class="sxs-lookup"><span data-stu-id="93c5e-112">**Required credentials to fix the issue:** The same user that setup dual-write.</span></span>

<span data-ttu-id="93c5e-113">Při pokusu o konfiguraci nové entity pro dvojitého zápisu se může zobrazit následující chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="93c5e-113">You might receive the following error message when you try to configure a new entity for dual-write.</span></span> <span data-ttu-id="93c5e-114">Jediným uživatelem, který může vytvořit mapu, je uživatel, který má nastaveno připojení s dvojitým zápisem.</span><span class="sxs-lookup"><span data-stu-id="93c5e-114">The only user that can create a map is the user who setup the dual-write connection.</span></span>

<span data-ttu-id="93c5e-115">*Stavový kód odpovědi neoznačuje úspěch: 401 (Neautorizováno)*</span><span class="sxs-lookup"><span data-stu-id="93c5e-115">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>


## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="93c5e-116">Chyba při otevření uživatelského rozhraní s dvojím zapisováním</span><span class="sxs-lookup"><span data-stu-id="93c5e-116">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="93c5e-117">Při pokusu o přístup dvojího zápisu z pracovního prostoru **Správa dat** se může zobrazit následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="93c5e-117">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="93c5e-118">*login.microsoftonline.com se odmítlo připojit.*</span><span class="sxs-lookup"><span data-stu-id="93c5e-118">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="93c5e-119">Chcete-li tento problém vyřešit, přihlaste se pomocí okna InPrivate v aplikaci Microsoft Edge, anonymního okna v Chromium nebo anonymního okna v Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="93c5e-119">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="93c5e-120">Je také nutné zrušit blokování nebo vymazat soubory cookie třetích stran.</span><span class="sxs-lookup"><span data-stu-id="93c5e-120">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a><span data-ttu-id="93c5e-121">Chyba při propojení prostředí pro dvojí zapisování nebo přidání nového mapování tabulky</span><span class="sxs-lookup"><span data-stu-id="93c5e-121">Error when you link the environment for dual-write or add a new table mapping</span></span>

<span data-ttu-id="93c5e-122">**Požadovaná role pro opravu problému:** Správce systému v obou aplikacích Finance and Operations a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="93c5e-122">**Required role to fix the issue:** System administrator in both Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="93c5e-123">Při připojování nebo vytváření map se může objevit následující chyba:</span><span class="sxs-lookup"><span data-stu-id="93c5e-123">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="93c5e-124">*Stavový kód odpovědi neoznačuje úspěch: 403 (tokenexchange).<br> ID relace: \<your session id\><br> ID kořenové aktivity: \<your root activity id\>*</span><span class="sxs-lookup"><span data-stu-id="93c5e-124">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="93c5e-125">K této chybě může dojít, pokud nemáte dostatečná oprávnění k propojení s dvojím zápisem nebo vytvářením map.</span><span class="sxs-lookup"><span data-stu-id="93c5e-125">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="93c5e-126">K této chybě může také dojít, pokud prostředí Dataverse bylo resetováno bez zrušení propojení dvojitého zápisu.</span><span class="sxs-lookup"><span data-stu-id="93c5e-126">This error can also occur if the Dataverse environment was reset without unlinking dual-write.</span></span> <span data-ttu-id="93c5e-127">Libovolný uživatel s rolí správce systému v aplikacích Finance and Operations a prostředí Dataverse může obě prostředí propojit.</span><span class="sxs-lookup"><span data-stu-id="93c5e-127">Any user with system administrator role in both Finance and Operations apps and Dataverse can link the environments.</span></span> <span data-ttu-id="93c5e-128">Přidávat nové mapy tabulky může pouze uživatel, který nastavuje připojení s dvojitým zápisem.</span><span class="sxs-lookup"><span data-stu-id="93c5e-128">Only the user who setup the dual-write connection can add new table maps.</span></span> <span data-ttu-id="93c5e-129">Po dokončení nastavení může libovolný uživatel s rolí správce systému sledovat stav a upravit mapování.</span><span class="sxs-lookup"><span data-stu-id="93c5e-129">After setup, any user with system administrator role can monitor the status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-table-mapping"></a><span data-ttu-id="93c5e-130">Chyba při zastavení mapování tabulky</span><span class="sxs-lookup"><span data-stu-id="93c5e-130">Error when you stop the table mapping</span></span>

<span data-ttu-id="93c5e-131">Při pokusu o zastavení mapování tabulky se může zobrazit následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="93c5e-131">You might receive the following error message when you try to stop the table mappings:</span></span>

<span data-ttu-id="93c5e-132">*\[Zakázáno\], \[{"stav": 403, "zdroj":","zpráva":"Chyba z výměny klienta: Uživatel nemá přístup k připojení dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], vzdálený server vrátil chybu: (403) Zakázáno.*</span><span class="sxs-lookup"><span data-stu-id="93c5e-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="93c5e-133">K této chybě dojde, pokud propojené prostředí Dataverse není k dispozici.</span><span class="sxs-lookup"><span data-stu-id="93c5e-133">This error occurs when the linked Dataverse environment isn't available.</span></span>

<span data-ttu-id="93c5e-134">Chcete-li tento problém vyřešit, vytvořte lístek pro tým pro integraci dat.</span><span class="sxs-lookup"><span data-stu-id="93c5e-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="93c5e-135">Připojte sledování sítě, aby mohl tým pro integraci dat označit mapy jako **nespuštěný** na back endu.</span><span class="sxs-lookup"><span data-stu-id="93c5e-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>

## <a name="error-while-trying-to-start-an-table-mapping"></a><span data-ttu-id="93c5e-136">Chyba při pokusu o spuštění mapování tabulky</span><span class="sxs-lookup"><span data-stu-id="93c5e-136">Error while trying to start an table mapping</span></span>

<span data-ttu-id="93c5e-137">Při pokusu o nastavení tohoto stavu mapování na **Spuštěno** se může zobrazit chybová zpráva podobná následující:</span><span class="sxs-lookup"><span data-stu-id="93c5e-137">You might receive an error like the following when you try to set that state of a mapping to **Running**:</span></span>

<span data-ttu-id="93c5e-138">*Nelze dokončit počáteční synchronizaci dat. Chyba: selhání dvojitého zápisu – registrace modulu plug-in se nezdařila: nelze vytvořit metadata vyhledávání dvojitého zápisu. Odkaz na objekt chyby není nastaven na instanci objektu.*</span><span class="sxs-lookup"><span data-stu-id="93c5e-138">*Unable to complete initial data sync. Error: dual-write failure - plugin registration failed: Unable to build dual-write lookup metadata. Error object reference not set to an instance of an object.*</span></span>

<span data-ttu-id="93c5e-139">Oprava této chyby závisí na příčině chyby:</span><span class="sxs-lookup"><span data-stu-id="93c5e-139">The fix for this error depends on the cause of the error:</span></span>

+ <span data-ttu-id="93c5e-140">Pokud mapování obsahuje závislá mapování, ujistěte se, že je povoleno mapování závislých položek tohoto mapování tabulky.</span><span class="sxs-lookup"><span data-stu-id="93c5e-140">If the mapping has dependent mappings, then make sure to enable the dependent mappings of this table mapping.</span></span>
+ <span data-ttu-id="93c5e-141">Mapování pravděpodobně neobsahuje zdrojová nebo cílová pole.</span><span class="sxs-lookup"><span data-stu-id="93c5e-141">The mapping might be missing source or destination fields.</span></span> <span data-ttu-id="93c5e-142">Pokud v aplikaci Finance and Operations chybí pole, postupujte podle kroků v oddílu [Problém chybějících polí entity při mapování](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span><span class="sxs-lookup"><span data-stu-id="93c5e-142">If a field in the Finance and Operations app is missing, then follow the steps in the section [Missing entity fields issue on maps](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span></span> <span data-ttu-id="93c5e-143">Pokud v prostředí Dataverse chybí pole, klikněte na tlačítko **Aktualizovat tabulky** u mapování, aby byla pole automaticky vložena zpět do mapování.</span><span class="sxs-lookup"><span data-stu-id="93c5e-143">If a field in Dataverse is missing, then click **Refresh tables** button on the mapping so that the fields are automatically populated back into the mapping.</span></span>
