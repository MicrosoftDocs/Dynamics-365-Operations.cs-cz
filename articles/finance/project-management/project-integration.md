---
title: Klientská integrace aplikace Microsoft Project
description: Plánování a údržba plánu projektu může být složitá. Projektoví manažeři proto potřebují používat nástroje, které jim pomohou spravovat tento úkol. Integrace s klientem Microsoft Project poskytuje podporu pro otevření a správu strukturovaného rozpisu prací na projektu.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 610990612d5fb38025bf39cc648d0c9572da37b6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174777"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="1f8cf-104">Klientská integrace aplikace Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="1f8cf-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f8cf-105">Plánování a údržba plánu projektu může být složitá. Projektoví manažeři proto potřebují používat nástroje, které jim pomohou spravovat tento úkol.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="1f8cf-106">Integrace s klientem Microsoft Project poskytuje podporu pro otevření a správu strukturovaného rozpisu prací na projektu.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="1f8cf-107">Projektový manažer může publikovat jakékoliv změny zpět do strukturovaného rozpisu prací na projektu aplikace Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="1f8cf-108">Pokud používáte aktualizaci z července (verze 10.0.4), musíte nainstalovat KB 4054797 a 4055884.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="1f8cf-109">Konfigurace doplňku klienta Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="1f8cf-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="1f8cf-110">Chcete-li povolit integraci s klientem Microsoft Project, musí být nainstalován doplněk Microsoft Dynamics 365 v klientovi uživatele aplikace Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="1f8cf-111">Otevřete **Pracovní prostor Správa projektu**.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="1f8cf-112">•   Klikněte na tlačítko **Konfigurace doplňku klienta Microsoft Project** z části pracovního prostoru **Odkazy** > **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="1f8cf-113">•   Klikněte na **Otevřít**, poté klikněte po zobrazení výzvy na **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="1f8cf-114">Otevření a úprava stávajícího konceptu strukturovaného rozpisu prací v klientovi Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="1f8cf-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="1f8cf-115">Pokud má projekt již v aplikaci Dynamics 365 Finance vytvořený strukturovaný rozpis prací, lze ho otevřít v aplikaci klienta Microsoft Project, pokud je strukturovaný rozpis prací ve stavu konceptu.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="1f8cf-116">Chcete-li ho otevřít ze stránky **Projekt**, klikněte na odkaz **Otevřít v aplikaci Microsoft Project** z karty **Plán**. Tuto stránku lze rovněž otevřít z aplikace klienta Microsoft Project kliknutím na **Otevřít** na kartě **Microsoft Dynamics 365**. Zvolte **Právnická osoba** a **Projekt** ze seznamu.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="1f8cf-117">Používáte-li jako prohlížeč Internet Explorer, musíte kliknout na tlačítko **Uložit** pro ruční otevření z umístění, do kterého je soubor stažený.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="1f8cf-118">Klikněte na tlačítko **Uložit a otevřít** a otevřete soubor v klientovi Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="1f8cf-119">Při ukládání neměňte název souboru.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="1f8cf-120">Před provedením jakýchkoliv úprav souboru pomocí klienta aplikace Microsoft Project je třeba ho nejprve rezervovat. Klikněte na tlačítko **Rezervovat** na kartě **Microsoft Dynamics 365**. Ostatním uživatelům zabráníte v souběžných úpravách strukturovaného rozpisu prací aplikace Finance.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="1f8cf-121">Chcete-li publikovat strukturovaný rozpis prací po dokončení úprav, klikněte na tlačítko **Vrátit se změnami** na kartě **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="1f8cf-122">Je-li projektový tým již přidán do projektu Finance, seznam zdrojů bude vyplněn členy týmu.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="1f8cf-123">Není-li tým ještě přidán do projektu, můžete vybrat zdroje a vytvořit tým v klientovi Microsoft Project kliknutím na tlačítko **Zdroje** na kartě **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="1f8cf-124">Následující data budou synchronizována zpět do aplikace Finance jako součást procesu vrácení se změnami:</span><span class="sxs-lookup"><span data-stu-id="1f8cf-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="1f8cf-125">•   Název úkolu</span><span class="sxs-lookup"><span data-stu-id="1f8cf-125">•   Task name</span></span>

<span data-ttu-id="1f8cf-126">•   Počáteční datum</span><span class="sxs-lookup"><span data-stu-id="1f8cf-126">•   Start date</span></span>

<span data-ttu-id="1f8cf-127">•   Datum dokončení</span><span class="sxs-lookup"><span data-stu-id="1f8cf-127">•   Finish date</span></span>

<span data-ttu-id="1f8cf-128">•   Předchůdci</span><span class="sxs-lookup"><span data-stu-id="1f8cf-128">•   Predecessors</span></span>

<span data-ttu-id="1f8cf-129">•   Názvy zdrojů</span><span class="sxs-lookup"><span data-stu-id="1f8cf-129">•   Resource names</span></span>

<span data-ttu-id="1f8cf-130">•   Kategorie</span><span class="sxs-lookup"><span data-stu-id="1f8cf-130">•   Category</span></span>

<span data-ttu-id="1f8cf-131">•   Kategorie prostředků</span><span class="sxs-lookup"><span data-stu-id="1f8cf-131">•   Resource category</span></span>

<span data-ttu-id="1f8cf-132">•   Pracovní hodiny</span><span class="sxs-lookup"><span data-stu-id="1f8cf-132">•   Work hours</span></span>

<span data-ttu-id="1f8cf-133">•   Poznámky</span><span class="sxs-lookup"><span data-stu-id="1f8cf-133">•   Notes</span></span>

<span data-ttu-id="1f8cf-134">•   Priorita</span><span class="sxs-lookup"><span data-stu-id="1f8cf-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="1f8cf-135">Pokud přidáte další sloupce do souboru klienta aplikace Microsoft Project, nebudou uloženy do souboru a nezobrazí se při opakovaném otevření souboru.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="1f8cf-136">Vytvoření strukturovaného rozpisu prací pro existující projekt pomocí klienta aplikace Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="1f8cf-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="1f8cf-137">Pro vytvoření nového strukturovaného rozpisu prací pomocí klienta Microsoft Project postupujte podle těchto kroků:</span><span class="sxs-lookup"><span data-stu-id="1f8cf-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="1f8cf-138">Otevřete klienta Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="1f8cf-139">Na kartě **Microsoft Dynamics 365** klikněte na **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="1f8cf-140">Vyberte **Právnická osoba** pro projekt.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="1f8cf-141">Vyberte **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="1f8cf-142">Klikněte na **Rezervovat** na kartě **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="1f8cf-143">Až budete připraveni publikovat do Finance, klikněte na **Vrátit se změnami** na kartě **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="1f8cf-144">Nahrazení stávajícího strukturovaného rozpisu prací pro existující projekt pomocí klienta aplikace Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="1f8cf-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="1f8cf-145">Chcete-li vytvořit nový strukturovaný rozpis prací pomocí klienta Microsoft Project a nahradit existující strukturovaný rozpis prací pro existující projekt, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="1f8cf-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="1f8cf-146">Otevřete klienta Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="1f8cf-147">Vytvořte plán v klientovi Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="1f8cf-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="1f8cf-148">Na kartě **Microsoft Dynamics 365**klikněte na **Uložit změny** > **Nahradit existující projekt**.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="1f8cf-149">Vyberte **Právnická osoba** pro projekt.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="1f8cf-150">Vyberte **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="1f8cf-151">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="1f8cf-152">Vytvoření nového projektu z klienta Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="1f8cf-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="1f8cf-153">Otevřete klienta Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="1f8cf-154">Vytvořte plán v klientovi Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="1f8cf-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="1f8cf-155">Na kartě **Microsoft Dynamics 365**klikněte na **Uložit změny** > **Uložit do nového projektu**.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="1f8cf-156">Vyberte **Právnická osoba** pro projekt.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="1f8cf-157">Zadejte **ID projektu**, pokud je to nutné.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="1f8cf-158">Zadejte **Název projektu**.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="1f8cf-159">Vyberte **Typ projektu**, **Skupina projektu** a **ID smlouvy projektu**.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="1f8cf-160">Také můžete vytvořit novou projektovou smlouvu kliknutím na **Nová**.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="1f8cf-161">Vyberte **Kalendář**, který se použije pro zdroje.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="1f8cf-162">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-162">Click **OK**.</span></span>
