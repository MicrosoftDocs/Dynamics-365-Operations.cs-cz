---
title: Přidání existující aktivity k verzi výrobního toku
description: Při vytvoření nových verzí výrobních toků se můžete rozhodnout přidat aktivity vytvořené pro starší verze do nové verze.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2fd6fe4ad25bde26a4212e236c9298a7ab832b66
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825103"
---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a><span data-ttu-id="fa64e-103">Přidání existující aktivity k verzi výrobního toku</span><span class="sxs-lookup"><span data-stu-id="fa64e-103">Add an existing activity to a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fa64e-104">Při vytvoření nových verzí výrobních toků se můžete rozhodnout přidat aktivity vytvořené pro starší verze do nové verze.</span><span class="sxs-lookup"><span data-stu-id="fa64e-104">When creating new versions of production flows, you can choose to add activities created for the older versions, to the new version.</span></span> <span data-ttu-id="fa64e-105">Tato procedura ukazuje, jak je vytvořena nová verze pro stávající výrobní tok bez kopírování aktivit.</span><span class="sxs-lookup"><span data-stu-id="fa64e-105">This procedure shows how a new version is created for an existing production flow, without copying the activities.</span></span> <span data-ttu-id="fa64e-106">V dalším kroku je přidána existující aktivita do nové verze.</span><span class="sxs-lookup"><span data-stu-id="fa64e-106">In the next step, an existing activity is added to the new version.</span></span> 

<span data-ttu-id="fa64e-107">Tento úkol vyžaduje výrobní tok s verzí a již vytvořenými aktivitami.</span><span class="sxs-lookup"><span data-stu-id="fa64e-107">This task requires production flow with version and activities already created.</span></span>


## <a name="create-a-new-production-flow-version"></a><span data-ttu-id="fa64e-108">Vytvořit novou verzi výrobního toku</span><span class="sxs-lookup"><span data-stu-id="fa64e-108">Create a new production flow version</span></span>
1. <span data-ttu-id="fa64e-109">Přejděte na Řízení výroby > Nastavení > Tok štíhlé výroby > Výrobního toky.</span><span class="sxs-lookup"><span data-stu-id="fa64e-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="fa64e-110">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="fa64e-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="fa64e-111">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="fa64e-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="fa64e-112">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="fa64e-112">Click Edit.</span></span>
5. <span data-ttu-id="fa64e-113">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="fa64e-113">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="fa64e-114">Do pole Datum vypršení platnosti zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="fa64e-114">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="fa64e-115">Všimněte si, že před vytvořením nové verze výrobního toku je třeba zkontrolovat datum vypršení platnosti a čas aktivní verze.</span><span class="sxs-lookup"><span data-stu-id="fa64e-115">Note that before you create a new production flow version, make sure to check the expiration date and time of the active version.</span></span> <span data-ttu-id="fa64e-116">Nová verze bude vytvořena s datem začátku platnosti, které se připojuje k datu vypršení platnosti vybrané verze.</span><span class="sxs-lookup"><span data-stu-id="fa64e-116">The new version will be created with an effective start date, which connects to the expiry date of the selected version.</span></span>  
7. <span data-ttu-id="fa64e-117">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fa64e-117">Click Add.</span></span>
8. <span data-ttu-id="fa64e-118">Vyberte Ne v poli Kopírovat z verze.</span><span class="sxs-lookup"><span data-stu-id="fa64e-118">Select No in the Copy from version field.</span></span>
    * <span data-ttu-id="fa64e-119">Vyberte Ne, chcete-li začít prázdnou verzí, pokud většina aktivit zkopírované verze bude nahrazeno novými aktivitami.</span><span class="sxs-lookup"><span data-stu-id="fa64e-119">Select No to start with an empty version if most of the activities of the copied version will be replaced by new activities.</span></span> <span data-ttu-id="fa64e-120">Ručně přidejte nezměněné aktivity k funkci Přidat existující ve formuláři Aktivita.</span><span class="sxs-lookup"><span data-stu-id="fa64e-120">Add the unchanged activities to the Add existing function in the activity form manually.</span></span>  
9. <span data-ttu-id="fa64e-121">Vyberte Ne v poli Duplicitní kanbanová pravidla.</span><span class="sxs-lookup"><span data-stu-id="fa64e-121">Select No in the Duplicate kanban rules field.</span></span>
    * <span data-ttu-id="fa64e-122">Když aktivity nejsou zkopírovány do nové verze, není možné kopírovat kanbanová pravidla v době vytvoření nové verze.</span><span class="sxs-lookup"><span data-stu-id="fa64e-122">When the activities are not copied to the new version, it is not possible to copy the kanban rules at the time of creation of the new version.</span></span>   <span data-ttu-id="fa64e-123">Místo toho budete používat funkci vytvoření náhradního kanbanu později ve formuláři kanbanového pravidla pro nahrazení kanbanových pravidel staré verze toku produkce kanbanovými pravidly používajícími aktivity nové verze.</span><span class="sxs-lookup"><span data-stu-id="fa64e-123">Instead you will use the create replacement kanban function later in the kanban rule form, to replace kanban rules of the old production flow version with kanban rules using the activities of the new version.</span></span>  
10. <span data-ttu-id="fa64e-124">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="fa64e-124">Click OK.</span></span>
11. <span data-ttu-id="fa64e-125">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="fa64e-125">In the list, find and select the desired record.</span></span>

## <a name="add-an-existing-activity"></a><span data-ttu-id="fa64e-126">Přidání existující aktivity</span><span class="sxs-lookup"><span data-stu-id="fa64e-126">Add an existing activity</span></span>
1. <span data-ttu-id="fa64e-127">Klepněte na aktivity.</span><span class="sxs-lookup"><span data-stu-id="fa64e-127">Click Activities.</span></span>
2. <span data-ttu-id="fa64e-128">Klepnutím na možnost Přidat existující otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="fa64e-128">Click Add existing to open the drop dialog.</span></span>
    * <span data-ttu-id="fa64e-129">Najděte a vyberte existující aktivitu, kterou chcete přidat do nové verze výrobního toku.</span><span class="sxs-lookup"><span data-stu-id="fa64e-129">Find and select an existing activity to be added to the new production flow version.</span></span>  <span data-ttu-id="fa64e-130">Všimněte si, že v seznamu jsou uvedeny všechny aktivity, které byly vytvořeny pro tento výrobní tok pro všechny předchozí verze toku.</span><span class="sxs-lookup"><span data-stu-id="fa64e-130">Note that the list shows all activities that have been created for this production flow for all previous versions of the flow.</span></span>  
3. <span data-ttu-id="fa64e-131">V poli Aktivita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fa64e-131">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="fa64e-132">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="fa64e-132">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]