---
title: "Import dat ze šablon datových entit aplikace Excel s více listy"
description: "Toto téma popisuje, jak importovat data pomocí šablon datových entit aplikace Excel do aplikace Microsoft Dynamics 365 for Finance and Operations."
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 48239b48cbc24e34d74bbac36e8f827a15d7b840
ms.contentlocale: cs-cz
ms.lasthandoff: 08/13/2018

---

# <a name="import-data-from-excel-data-entity-templates-that-have-multiple-worksheets"></a><span data-ttu-id="33ff5-103">Import dat ze šablon datových entit aplikace Excel s více listy</span><span class="sxs-lookup"><span data-stu-id="33ff5-103">Import data from Excel data entity templates that have multiple worksheets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33ff5-104">Správa dat v aplikaci Microsoft Dynamics 365 for Finance and Operations podporuje šablony na základě aplikace Microsoft Excel pro datové entity.</span><span class="sxs-lookup"><span data-stu-id="33ff5-104">Data management in Microsoft Dynamics 365 for Finance and Operations supports Microsoft Excel-based templates for data entities.</span></span> <span data-ttu-id="33ff5-105">Tyto šablony mohou obsahovat jeden nebo více listů.</span><span class="sxs-lookup"><span data-stu-id="33ff5-105">These templates can contain one or more worksheets.</span></span> <span data-ttu-id="33ff5-106">Šablony s více listy se často používají tehdy, když je vhodné spravovat data v jednom souboru a importovat je do vícero datových entit.</span><span class="sxs-lookup"><span data-stu-id="33ff5-106">Templates with multiple worksheets are often used when it is convenient to manage data in a single file and import it to multiple data entities.</span></span> <span data-ttu-id="33ff5-107">Příkladem by byla pracoviště a sklady.</span><span class="sxs-lookup"><span data-stu-id="33ff5-107">An example would be sites and warehouses.</span></span>

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a><span data-ttu-id="33ff5-108">Nahrajte soubor jednou a namapujte ho na všechny entity</span><span class="sxs-lookup"><span data-stu-id="33ff5-108">Upload a file once and map it to all entities</span></span>
<span data-ttu-id="33ff5-109">Podíváme se na příklad, kde existuje jeden soubor aplikace Excel s listy nazvanými **Pracoviště** a **Sklady**.</span><span class="sxs-lookup"><span data-stu-id="33ff5-109">Let's take an example where there is one Excel file with worksheets called **Sites** and **Warehouses**.</span></span> <span data-ttu-id="33ff5-110">Chcete-li nastavit projekt importu dat, přidali byste první datovou entitu **Pracoviště** a poté odeslali soubor.</span><span class="sxs-lookup"><span data-stu-id="33ff5-110">To set up the data import project, you would add the first data entity, **Sites** and then upload the file.</span></span> <span data-ttu-id="33ff5-111">Budete moci vybrat **Pracoviště** jako list, který bude použit pro tuto entitu.</span><span class="sxs-lookup"><span data-stu-id="33ff5-111">You will be able to select **Sites** as the worksheet to be used for this entity.</span></span>

<span data-ttu-id="33ff5-112">Pokud přidáte druhou entitu **Sklady**, aniž byste opustili formulář **Přidat soubor**, vyhledávání listu vám umožní vybrat list **Sklady** bez nutnosti znovu odeslat soubor.</span><span class="sxs-lookup"><span data-stu-id="33ff5-112">If you add the second entity **Warehouses** without leaving the **Add file** form, the worksheet lookup will let you select the **Warehouses** worksheet without having to upload the file again.</span></span> <span data-ttu-id="33ff5-113">Jediný důvod k odeslání nového souboru by byl ten, kdyby data **Sklady** byla v jiném souboru.</span><span class="sxs-lookup"><span data-stu-id="33ff5-113">The only reason to upload a new file would be if the **Warehouses** data was in a different file.</span></span>

![Více listů](./media/AddFileMultipleWorkSheets.png)

## <a name="fix-worksheet-to-entity-mapping"></a><span data-ttu-id="33ff5-115">Opravení listu pro mapování entit</span><span class="sxs-lookup"><span data-stu-id="33ff5-115">Fix worksheet to entity mapping</span></span>

<span data-ttu-id="33ff5-116">Mapování listu na datovou entitu v úloze importu lze opravit z mřížky.</span><span class="sxs-lookup"><span data-stu-id="33ff5-116">The mapping of the worksheet to a data entity in the import job can be fixed from the grid.</span></span> <span data-ttu-id="33ff5-117">Sloupec **List** v mřížce zobrazí listy ze souboru, který byl mapován.</span><span class="sxs-lookup"><span data-stu-id="33ff5-117">The **Worksheet** column in the grid shows the worksheets from the file that was mapped.</span></span> <span data-ttu-id="33ff5-118">Jiný list můžete vybrat z rozevírací nabídky.</span><span class="sxs-lookup"><span data-stu-id="33ff5-118">You can choose a different worksheet from the drop-down menu.</span></span> <span data-ttu-id="33ff5-119">Pokud je zvolený list již namapován na entitu v datovém projektu, systém zobrazí výzvu k potvrzení změny.</span><span class="sxs-lookup"><span data-stu-id="33ff5-119">If the chosen worksheet is already mapped to an entity in the data project, the system asks you to confirm the change.</span></span> <span data-ttu-id="33ff5-120">Doporučujeme, abyste v mřížce opravili všechna mapování.</span><span class="sxs-lookup"><span data-stu-id="33ff5-120">We recommend that you fix all mappings in the grid.</span></span>

![Aktualizace mapování listu](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a><span data-ttu-id="33ff5-122">Opětovné namapování na nový soubor</span><span class="sxs-lookup"><span data-stu-id="33ff5-122">Re-map to a new file</span></span>

<span data-ttu-id="33ff5-123">V případech, kdy musí být odeslána nová verze stejného nebo zcela nového souboru pro existující entity v datovém projektu, je třeba použít možnost **Přidat soubor** a znovu přidat entity, jako kdyby byly přidány poprvé.</span><span class="sxs-lookup"><span data-stu-id="33ff5-123">In cases where a new version of the same file or a completely new file must be uploaded for existing entities in a data project, you must use the **Add file** experience, and add the entities again as if they were being added for the first time.</span></span> <span data-ttu-id="33ff5-124">Systém potvrdí, že chcete přepsat existující entity v projektu dat, než budete pokračovat.</span><span class="sxs-lookup"><span data-stu-id="33ff5-124">The system will confirm that you want to overwrite the existing entities in the data project before proceeding.</span></span> <span data-ttu-id="33ff5-125">Entity, které nejsou znovu přidány (nebo přepsány) budou nadále udržovat mapování z přechozího souboru.</span><span class="sxs-lookup"><span data-stu-id="33ff5-125">Entities that are not added again (or overwritten) will continue to hold the previous mappings from the previous file.</span></span>

## <a name="upload-a-file-using-run-project"></a><span data-ttu-id="33ff5-126">Odeslání souboru pomocí spuštění projektu</span><span class="sxs-lookup"><span data-stu-id="33ff5-126">Upload a file using Run project</span></span>

<span data-ttu-id="33ff5-127">Můžete načíst soubor aplikace Excel při používání možnosti **Spustit projekt** pro provedení projektu importu.</span><span class="sxs-lookup"><span data-stu-id="33ff5-127">You can upload an Excel file while using the **Run project** option to execute an import project.</span></span> <span data-ttu-id="33ff5-128">Musíte si dávat pozor, abyste odeslali pouze soubory, které mají stejné listy jako existující mapování na datových entitách v datovém projektu.</span><span class="sxs-lookup"><span data-stu-id="33ff5-128">You must be careful to upload only files that have the same worksheets as the existing mappings on the data entities in the data project.</span></span> <span data-ttu-id="33ff5-129">Pokud není list nalezen v nově odeslaném souboru, systém zobrazí chybovou zprávu a zastaví import.</span><span class="sxs-lookup"><span data-stu-id="33ff5-129">If a worksheet is not found in the newly uploaded file, the system displays an error and will stop the import.</span></span> <span data-ttu-id="33ff5-130">Pokud u entity musí být změněno mapování na list, musí být nejprve aktualizováno mapování v datovém projektu z datového projektu předtím, než použijete soubor v možnosti **Spustit projekt**.</span><span class="sxs-lookup"><span data-stu-id="33ff5-130">If the mapping to the worksheet must be changed for an entity, then the mappings in the data project must be first updated from within the data project before using the file in the **Run project** experience.</span></span>

