---
title: Řešení potíží s modulem duálního zápisu v aplikacích Finance and Operations
description: Toto téma obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy s modulem dvojího zapisování v aplikacích Finance and Operations.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
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
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 9bff8ad0c5716648dec6eadfb21412a2b17f155e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561219"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a><span data-ttu-id="c8903-103">Řešení potíží s modulem duálního zápisu v aplikacích Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c8903-103">Troubleshoot dual-write issues in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c8903-104">Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="c8903-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="c8903-105">Konkrétně toto téma obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy s modulem **Dvojího zapisování** v aplikacích Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c8903-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8903-106">Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="c8903-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="c8903-107">Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.</span><span class="sxs-lookup"><span data-stu-id="c8903-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="c8903-108">V aplikaci Finance and Operations nelze načíst modul dvojitého zápisu</span><span class="sxs-lookup"><span data-stu-id="c8903-108">You can't load the dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="c8903-109">Pokud nemůžete otevřít stránku **Dvojího zapisování** výběrem dlaždice **Dvojího zapisování** v pracovním prostoru **Správa dat**, služba integrace dat je pravděpodobně mimo provoz.</span><span class="sxs-lookup"><span data-stu-id="c8903-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="c8903-110">Vytvořte lístek podpory pro vyžádání restartu služby Data Integration Service.</span><span class="sxs-lookup"><span data-stu-id="c8903-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-table-map"></a><span data-ttu-id="c8903-111">Chyba při pokusu o vytvoření nového mapování tabulky</span><span class="sxs-lookup"><span data-stu-id="c8903-111">Error when you try to create a new table map</span></span>

<span data-ttu-id="c8903-112">**Požadovaná pověření pro opravu problému:** Stejný uživatel, který má nastaven dvojitý zápis.</span><span class="sxs-lookup"><span data-stu-id="c8903-112">**Required credentials to fix the issue:** The same user that setup dual-write.</span></span>

<span data-ttu-id="c8903-113">Při pokusu o konfiguraci nové tabulky pro dvojitého zápisu se může zobrazit následující chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="c8903-113">You might receive the following error message when you try to configure a new table for dual-write.</span></span> <span data-ttu-id="c8903-114">Jediným uživatelem, který může vytvořit mapu, je uživatel, který má nastaveno připojení s dvojitým zápisem.</span><span class="sxs-lookup"><span data-stu-id="c8903-114">The only user that can create a map is the user who setup the dual-write connection.</span></span>

<span data-ttu-id="c8903-115">*Stavový kód odpovědi neoznačuje úspěch: 401 (Neautorizováno)*</span><span class="sxs-lookup"><span data-stu-id="c8903-115">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>


## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="c8903-116">Chyba při otevření uživatelského rozhraní s dvojím zapisováním</span><span class="sxs-lookup"><span data-stu-id="c8903-116">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="c8903-117">Při pokusu o přístup dvojího zápisu z pracovního prostoru **Správa dat** se může zobrazit následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="c8903-117">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="c8903-118">*login.microsoftonline.com se odmítlo připojit.*</span><span class="sxs-lookup"><span data-stu-id="c8903-118">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="c8903-119">Chcete-li tento problém vyřešit, přihlaste se pomocí okna InPrivate v aplikaci Microsoft Edge, anonymního okna v Chromium nebo anonymního okna v Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="c8903-119">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="c8903-120">Je také nutné zrušit blokování nebo vymazat soubory cookie třetích stran.</span><span class="sxs-lookup"><span data-stu-id="c8903-120">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a><span data-ttu-id="c8903-121">Chyba při propojení prostředí pro dvojí zapisování nebo přidání nového mapování tabulky</span><span class="sxs-lookup"><span data-stu-id="c8903-121">Error when you link the environment for dual-write or add a new table mapping</span></span>

<span data-ttu-id="c8903-122">**Požadovaná role pro opravu problému:** Správce systému v obou aplikacích Finance and Operations a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="c8903-122">**Required role to fix the issue:** System administrator in both Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="c8903-123">Při připojování nebo vytváření map se může objevit následující chyba:</span><span class="sxs-lookup"><span data-stu-id="c8903-123">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="c8903-124">*Stavový kód odpovědi neoznačuje úspěch: 403 (tokenexchange).<br> ID relace: \<your session id\><br> ID kořenové aktivity: \<your root activity id\>*</span><span class="sxs-lookup"><span data-stu-id="c8903-124">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="c8903-125">K této chybě může dojít, pokud nemáte dostatečná oprávnění k propojení s dvojím zápisem nebo vytvářením map.</span><span class="sxs-lookup"><span data-stu-id="c8903-125">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="c8903-126">K této chybě může také dojít, pokud prostředí Dataverse bylo resetováno bez zrušení propojení dvojitého zápisu.</span><span class="sxs-lookup"><span data-stu-id="c8903-126">This error can also occur if the Dataverse environment was reset without unlinking dual-write.</span></span> <span data-ttu-id="c8903-127">Libovolný uživatel s rolí správce systému v aplikacích Finance and Operations a prostředí Dataverse může obě prostředí propojit.</span><span class="sxs-lookup"><span data-stu-id="c8903-127">Any user with system administrator role in both Finance and Operations apps and Dataverse can link the environments.</span></span> <span data-ttu-id="c8903-128">Přidávat nové mapy tabulky může pouze uživatel, který nastavuje připojení s dvojitým zápisem.</span><span class="sxs-lookup"><span data-stu-id="c8903-128">Only the user who setup the dual-write connection can add new table maps.</span></span> <span data-ttu-id="c8903-129">Po dokončení nastavení může libovolný uživatel s rolí správce systému sledovat stav a upravit mapování.</span><span class="sxs-lookup"><span data-stu-id="c8903-129">After setup, any user with system administrator role can monitor the status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-table-mapping"></a><span data-ttu-id="c8903-130">Chyba při zastavení mapování tabulky</span><span class="sxs-lookup"><span data-stu-id="c8903-130">Error when you stop the table mapping</span></span>

<span data-ttu-id="c8903-131">Při pokusu o zastavení mapování tabulky se může zobrazit následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="c8903-131">You might receive the following error message when you try to stop the table mappings:</span></span>

<span data-ttu-id="c8903-132">*\[Zakázáno\], \[{"stav": 403, "zdroj":","zpráva":"Chyba z výměny klienta: Uživatel nemá přístup k připojení dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], vzdálený server vrátil chybu: (403) Zakázáno.*</span><span class="sxs-lookup"><span data-stu-id="c8903-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="c8903-133">K této chybě dojde, pokud propojené prostředí Dataverse není k dispozici.</span><span class="sxs-lookup"><span data-stu-id="c8903-133">This error occurs when the linked Dataverse environment isn't available.</span></span>

<span data-ttu-id="c8903-134">Chcete-li tento problém vyřešit, vytvořte lístek pro tým pro integraci dat.</span><span class="sxs-lookup"><span data-stu-id="c8903-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="c8903-135">Připojte sledování sítě, aby mohl tým pro integraci dat označit mapy jako **nespuštěný** na back endu.</span><span class="sxs-lookup"><span data-stu-id="c8903-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>

## <a name="error-while-trying-to-start-a-table-mapping"></a><span data-ttu-id="c8903-136">Chyba při pokusu o spuštění mapování tabulky</span><span class="sxs-lookup"><span data-stu-id="c8903-136">Error while trying to start a table mapping</span></span>

<span data-ttu-id="c8903-137">Při pokusu o nastavení tohoto stavu mapování na **Spuštěno** se může zobrazit chybová zpráva podobná následující:</span><span class="sxs-lookup"><span data-stu-id="c8903-137">You might receive an error like the following when you try to set that state of a mapping to **Running**:</span></span>

<span data-ttu-id="c8903-138">*Nelze dokončit počáteční synchronizaci dat. Chyba: selhání dvojitého zápisu – registrace modulu plug-in se nezdařila: nelze vytvořit metadata vyhledávání dvojitého zápisu. Odkaz na objekt chyby není nastaven na instanci objektu.*</span><span class="sxs-lookup"><span data-stu-id="c8903-138">*Unable to complete initial data sync. Error: dual-write failure - plugin registration failed: Unable to build dual-write lookup metadata. Error object reference not set to an instance of an object.*</span></span>

<span data-ttu-id="c8903-139">Oprava této chyby závisí na příčině chyby:</span><span class="sxs-lookup"><span data-stu-id="c8903-139">The fix for this error depends on the cause of the error:</span></span>

+ <span data-ttu-id="c8903-140">Pokud mapování obsahuje závislá mapování, ujistěte se, že je povoleno mapování závislých položek tohoto mapování tabulky.</span><span class="sxs-lookup"><span data-stu-id="c8903-140">If the mapping has dependent mappings, then make sure to enable the dependent mappings of this table mapping.</span></span>
+ <span data-ttu-id="c8903-141">Mapování pravděpodobně neobsahuje zdrojové nebo cílové sloupce.</span><span class="sxs-lookup"><span data-stu-id="c8903-141">The mapping might be missing source or destination columns.</span></span> <span data-ttu-id="c8903-142">Pokud ve sloupci v aplikaci Finance and Operations chybí pole, postupujte podle kroků v oddílu [Problém chybějících sloupců tabulky při mapování](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps).</span><span class="sxs-lookup"><span data-stu-id="c8903-142">If a column in the Finance and Operations app is missing, then follow the steps in the section [Missing table columns issue on maps](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps).</span></span> <span data-ttu-id="c8903-143">Pokud v prostředí Dataverse chybí sloupec, klikněte na tlačítko **Aktualizovat tabulky** u mapování, aby byly sloupce automaticky vloženy zpět do mapování.</span><span class="sxs-lookup"><span data-stu-id="c8903-143">If a column in Dataverse is missing, then click **Refresh tables** button on the mapping so that the columns are automatically populated back into the mapping.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]