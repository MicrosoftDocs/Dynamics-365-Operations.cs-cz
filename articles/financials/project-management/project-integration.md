---
title: "Klientská integrace aplikace Microsoft Project"
description: "Plánování a údržba plánu projektu může být složitá. Projektoví manažeři proto potřebují používat nástroje, které jim pomohou spravovat tento úkol. Integrace s klientem Microsoft Project poskytuje podporu pro otevření a správu strukturovaného rozpisu prací na projektu."
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a54e1281dc54e1656298ea86c0724ad18ceff9a2
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="microsoft-project-client-integration"></a><span data-ttu-id="a3354-104">Klientská integrace aplikace Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="a3354-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3354-105">Plánování a údržba plánu projektu může být složitá. Projektoví manažeři proto potřebují používat nástroje, které jim pomohou spravovat tento úkol.</span><span class="sxs-lookup"><span data-stu-id="a3354-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="a3354-106">Integrace s klientem Microsoft Project poskytuje podporu pro otevření a správu strukturovaného rozpisu prací na projektu.</span><span class="sxs-lookup"><span data-stu-id="a3354-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="a3354-107">Projektový manažer může publikovat jakékoliv změny zpět do strukturovaného rozpisu prací na projektu aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a3354-107">The project manager can publish any changes back to the Finance and Operations project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="a3354-108">Pokud používáte aplikaci Microsoft Dynamics 365 for Finance and Operations v aktualizaci z července 2017, musíte si nainstalovat KB 4054797 a 4055884.</span><span class="sxs-lookup"><span data-stu-id="a3354-108">If you are using Microsoft Dynamics 365 for Finance and Operations, July update, you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="a3354-109">Konfigurace doplňku klienta Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="a3354-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="a3354-110">Chcete-li povolit integraci s klientem Microsoft Project, musí být nainstalován doplněk Microsoft Dynamics 365 v klientovi uživatele aplikace Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="a3354-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="a3354-111">Otevřete **Pracovní prostor Správa projektu**.</span><span class="sxs-lookup"><span data-stu-id="a3354-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="a3354-112">•   Klikněte na tlačítko **Konfigurace doplňku klienta Microsoft Project** z části pracovního prostoru **Odkazy** > **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="a3354-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="a3354-113">•   Klikněte na **Otevřít**, poté klikněte po zobrazení výzvy na **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="a3354-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="a3354-114">Otevření a úprava stávajícího konceptu strukturovaného rozpisu prací v klientovi Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="a3354-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="a3354-115">Pokud má projekt již v aplikaci Finance and Operation vytvořený strukturovaný rozpis prací, lze ho otevřít v aplikaci klienta Microsoft Project, pokud je strukturovaný rozpis prací ve stavu konceptu.</span><span class="sxs-lookup"><span data-stu-id="a3354-115">If a project in Finance and Operations already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="a3354-116">Chcete-li ho otevřít ze stránky **Projekt**, klikněte na odkaz **Otevřít v aplikaci Microsoft Project** z karty **Plán**. Tuto stránku lze rovněž otevřít z aplikace klienta Microsoft Project kliknutím na **Otevřít** na kartě **Microsoft Dynamics 365**. Zvolte **Právnická osoba** a **Projekt** ze seznamu.</span><span class="sxs-lookup"><span data-stu-id="a3354-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="a3354-117">Používáte-li jako prohlížeč Internet Explorer, musíte kliknout na tlačítko **Uložit** pro ruční otevření z umístění, do kterého je soubor stažený.</span><span class="sxs-lookup"><span data-stu-id="a3354-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="a3354-118">Klikněte na tlačítko **Uložit a otevřít** a otevřete soubor v klientovi Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="a3354-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="a3354-119">Při ukládání neměňte název souboru.</span><span class="sxs-lookup"><span data-stu-id="a3354-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="a3354-120">Před provedením jakýchkoliv úprav souboru pomocí klienta aplikace Microsoft Project je třeba ho nejprve rezervovat. Klikněte na tlačítko **Rezervovat** na kartě **Microsoft Dynamics 365**. Ostatním uživatelům zabráníte v souběžných úpravách strukturovaného rozpisu prací aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a3354-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance and Operations at the same time.</span></span> <span data-ttu-id="a3354-121">Chcete-li publikovat strukturovaný rozpis prací po dokončení úprav, klikněte na tlačítko **Vrátit se změnami** na kartě **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="a3354-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="a3354-122">Je-li projektový tým již přidán do projektu Finance and Operations, seznam zdrojů bude vyplněn členy týmu.</span><span class="sxs-lookup"><span data-stu-id="a3354-122">If a project team has already been added to the project in Finance and Operations, the resource list will be populated with the team members.</span></span> <span data-ttu-id="a3354-123">Není-li tým ještě přidán do projektu, můžete vybrat zdroje a vytvořit tým v klientovi Microsoft Project klikinutím na tlačítko **Zdroje** na kartě **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="a3354-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="a3354-124">Následující data budou synchronizována zpět do aplikace Finance and Operation jako součást procesu vrácení se změnami:</span><span class="sxs-lookup"><span data-stu-id="a3354-124">The following data will be synced back to Finance and Operations as part of the check in process:</span></span>

<span data-ttu-id="a3354-125">•   Název úkolu</span><span class="sxs-lookup"><span data-stu-id="a3354-125">•   Task name</span></span>

<span data-ttu-id="a3354-126">•   Počáteční datum</span><span class="sxs-lookup"><span data-stu-id="a3354-126">•   Start date</span></span>

<span data-ttu-id="a3354-127">•   Datum dokončení</span><span class="sxs-lookup"><span data-stu-id="a3354-127">•   Finish date</span></span>

<span data-ttu-id="a3354-128">•   Předchůdci</span><span class="sxs-lookup"><span data-stu-id="a3354-128">•   Predecessors</span></span>

<span data-ttu-id="a3354-129">•   Názvy zdrojů</span><span class="sxs-lookup"><span data-stu-id="a3354-129">•   Resource names</span></span>

<span data-ttu-id="a3354-130">•   Kategorie</span><span class="sxs-lookup"><span data-stu-id="a3354-130">•   Category</span></span>

<span data-ttu-id="a3354-131">•   Kategorie prostředků</span><span class="sxs-lookup"><span data-stu-id="a3354-131">•   Resource category</span></span>

<span data-ttu-id="a3354-132">•   Pracovní hodiny</span><span class="sxs-lookup"><span data-stu-id="a3354-132">•   Work hours</span></span>

<span data-ttu-id="a3354-133">•   Poznámky</span><span class="sxs-lookup"><span data-stu-id="a3354-133">•   Notes</span></span>

<span data-ttu-id="a3354-134">•   Priorita</span><span class="sxs-lookup"><span data-stu-id="a3354-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="a3354-135">Pokud přidáte další sloupce do souboru klienta aplikace Microsoft Project, nebudou uloženy do souboru a nezobrazí se při opakovaném otevření souboru.</span><span class="sxs-lookup"><span data-stu-id="a3354-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="a3354-136">Vytvoření strukturovaného rozpisu prací pro existující projekt pomocí klienta aplikace Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="a3354-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="a3354-137">Pro vytvoření nového strukturovaného rozpisu prací pomocí klienta Microsoft Project postupujte podle těchto kroků:</span><span class="sxs-lookup"><span data-stu-id="a3354-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="a3354-138">Otevřete klienta Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="a3354-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="a3354-139">Na kartě **Microsoft Dynamics 365** klikněte na **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="a3354-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="a3354-140">Vyberte **Právnická osoba** pro projekt.</span><span class="sxs-lookup"><span data-stu-id="a3354-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="a3354-141">Vyberte **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="a3354-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="a3354-142">Klikněte na **Rezervovat** na kartě **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="a3354-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="a3354-143">Až budete připraveni publikovat do Finance and Operations, klikněte na **Vrátit se změnami** na kartě **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="a3354-143">When ready to publish to Finance and Operations, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="a3354-144">Nahrazení stávajícího strukturovaného rozpisu prací pro existující projekt pomocí klienta aplikace Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="a3354-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="a3354-145">Chcete-li vytvořit nový strukturovaný rozpis prací pomocí klienta Microsoft Project a nahradit existující strukturovaný rozpis prací pro existující projekt, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="a3354-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="a3354-146">Otevřete klienta Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="a3354-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="a3354-147">Vytvořte plán v klientovi Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="a3354-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="a3354-148">Na kartě **Microsoft Dynamics 365** klikněte na **Uložit změny** > **Nahradit stávající projekt**.</span><span class="sxs-lookup"><span data-stu-id="a3354-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="a3354-149">Vyberte **Právnická osoba** pro projekt.</span><span class="sxs-lookup"><span data-stu-id="a3354-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="a3354-150">Vyberte **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="a3354-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="a3354-151">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3354-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="a3354-152">Vytvoření nového projektu z klienta Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="a3354-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="a3354-153">Otevřete klienta Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="a3354-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="a3354-154">Vytvořte plán v klientovi Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="a3354-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="a3354-155">Na kartě **Microsoft Dynamics 365** klikněte na **Uložit změny** > **Uložit do nového projektu**.</span><span class="sxs-lookup"><span data-stu-id="a3354-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="a3354-156">Vyberte **Právnická osoba** pro projekt.</span><span class="sxs-lookup"><span data-stu-id="a3354-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="a3354-157">Zadejte **ID projektu**, pokud je to nutné.</span><span class="sxs-lookup"><span data-stu-id="a3354-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="a3354-158">Zadejte **Název projektu**.</span><span class="sxs-lookup"><span data-stu-id="a3354-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="a3354-159">Vyberte **Typ projektu**, **Skupina projektu** a **ID smlouvy projektu**.</span><span class="sxs-lookup"><span data-stu-id="a3354-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="a3354-160">Také můžete vytvořit novou projektovou smlouvu kliknutím na **Nová**.</span><span class="sxs-lookup"><span data-stu-id="a3354-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="a3354-161">Vyberte **Kalendář**, který se použije pro zdroje.</span><span class="sxs-lookup"><span data-stu-id="a3354-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="a3354-162">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3354-162">Click **OK**.</span></span>

