---
title: Dokumenty majetku
description: V tomto tématu jsou vysvětleny dokumenty majetku v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5b791fd3e060c4f4ecdb1ca599a6041d421db74
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024516"
---
# <a name="asset-documents"></a><span data-ttu-id="03b11-103">Dokumenty majetku</span><span class="sxs-lookup"><span data-stu-id="03b11-103">Asset documents</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="03b11-104">V tomto tématu jsou vysvětleny dokumenty majetku v modulu Správa majetku.</span><span class="sxs-lookup"><span data-stu-id="03b11-104">This topic explains asset documents in Asset Management.</span></span>

<span data-ttu-id="03b11-105">V modulu Správa majetku můžete vytvořit dokumenty tak, že budou automaticky spojeny např. s typy úloh, výrobci majetku, typy majetku nebo majetkem.</span><span class="sxs-lookup"><span data-stu-id="03b11-105">In Asset Management, you can set up documents so that they are automatically related to job types, asset manufacturers, asset types, or assets, for example.</span></span> <span data-ttu-id="03b11-106">Tato funkce je užitečná, když jsou vydány aktualizované verze dokumentů.</span><span class="sxs-lookup"><span data-stu-id="03b11-106">This functionality is useful when updated document versions are released.</span></span> <span data-ttu-id="03b11-107">V takovém případě stačí pouze vložit aktualizovaný dokument do standardního umístění, které používáte pro dokumenty Finance and Operations, a připojit dokument k záznamu o majetku, který jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="03b11-107">In that case, you just have to put the updated document in the standard location that you use for your Finance and Operations documents, and attach the document to the asset document record that you've created.</span></span> <span data-ttu-id="03b11-108">K aktualizovanému dokumentu pak lze získat přístup z položek nabídky **Všechen majetek**, **Aktivní majetek**, **Můj aktivní majetek** a **Všechny pracovní příkazy** a **Aktivní úlohy pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="03b11-108">The updated document can then be accessed from the **All assets**, **Active assets**, **My active assets**, **All work orders**, and **Active work order jobs** menu items.</span></span> <span data-ttu-id="03b11-109">Proces připojování dokumentů k záznamu dokumentu aktiv používá standardní systém zpracování dokumentů.</span><span class="sxs-lookup"><span data-stu-id="03b11-109">The process for attaching documents to an asset document record uses the standard document handling system.</span></span>

<span data-ttu-id="03b11-110">**Příklad 1:** dokument, který souvisí s typem práce, může popisovat postup pro tento typ úlohy.</span><span class="sxs-lookup"><span data-stu-id="03b11-110">**Example 1:** A document that is related to a job type might describe a procedure for that job type.</span></span>

<span data-ttu-id="03b11-111">**Příklad 2:** dokument, který souvisí s kombinací typu majetku, výrobce a modelu, může být standardní příručkou vybraného modelu výrobce majetku.</span><span class="sxs-lookup"><span data-stu-id="03b11-111">**Example 2:** A document that is related to a combination of an asset type, manufacturer, and model might be the standard manual for the selected asset manufacturer model.</span></span>

## <a name="create-asset-document-relation"></a><span data-ttu-id="03b11-112">Vytvořit vztah dokumentu majetku</span><span class="sxs-lookup"><span data-stu-id="03b11-112">Create asset document relation</span></span>

1. <span data-ttu-id="03b11-113">Vyberte **Správa majetku** \> **Nastavení** \> **Dokumenty majetku**.</span><span class="sxs-lookup"><span data-stu-id="03b11-113">Select **Asset management** \> **Setup** \> **Asset documents**.</span></span>
2. <span data-ttu-id="03b11-114">Vyberte **Nový**, chcete-li vytvořit záznam o dokumentu majetku.</span><span class="sxs-lookup"><span data-stu-id="03b11-114">Select **New** to create an asset document record.</span></span>
3. <span data-ttu-id="03b11-115">V závislosti na tom, jak konkrétní vztah dokumentu chcete, proveďte příslušné výběry v jednom nebo více následujících polí: **Typ majetku**, **Výrobce**, **Model**, **Majetek**, **Kategorie typu práce**, **Typ práce**, **Varianta typu práce** a **Požadavek na práci**.</span><span class="sxs-lookup"><span data-stu-id="03b11-115">Depending on how specific you want the document relation to be, make relevant selections in one or more of the following fields: **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement**.</span></span> <span data-ttu-id="03b11-116">Možnosti, které jsou k dispozici v poli **Varianta typu práce** a **Požadavek na práci** závisejí na vašem výběru v poli **Typ práce**.</span><span class="sxs-lookup"><span data-stu-id="03b11-116">The options that are available in the **Job type variant** and **Job requirement** fields depend on your selection in the **Job type** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="03b11-117">Pokud systém vyhledává dokumenty, které by měly souviset s majetkem nebo pracovním příkazem, bude Správa majetku procházet všemi záznamy dokumentu majetku a zkontroluje možnou shodu.</span><span class="sxs-lookup"><span data-stu-id="03b11-117">When the system searches for documents that should be related to an asset or a work order, Asset Management goes through all asset document records to check for a possible match.</span></span> <span data-ttu-id="03b11-118">Vždy zkontroluje nejdříve nejkonkrétnější kombinaci.</span><span class="sxs-lookup"><span data-stu-id="03b11-118">It always checks the most specific combination first.</span></span> <span data-ttu-id="03b11-119">Jinými slovy, Správa majetku nejprve zkontroluje shodu v poli **Požadavek na práci**.</span><span class="sxs-lookup"><span data-stu-id="03b11-119">In other words, Asset Management first checks for a match for the **Job requirement** field.</span></span> <span data-ttu-id="03b11-120">Pokud není nalezena shoda, zkontroluje shodu v poli **Varianta typu práce**.</span><span class="sxs-lookup"><span data-stu-id="03b11-120">If no match is found, it checks for a match for the **Job type variant** field.</span></span> <span data-ttu-id="03b11-121">Pokud není nalezena shoda, zkontroluje shodu v poli **Typ práce** a tak dále.</span><span class="sxs-lookup"><span data-stu-id="03b11-121">If no match is found, it checks for a match for the **Job type** field, and so on.</span></span> <span data-ttu-id="03b11-122">Jak vidíte v rozvržení stránky **Dokumenty práce**, toto chování znamená, že pro nalezení nejspecifičtější kombinace zkontroluje Správa majetku každý záznam zprava doleva pro nalezení shody.</span><span class="sxs-lookup"><span data-stu-id="03b11-122">As you can see in the layout of the **Asset documents** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="03b11-123">Několik dokumentů může souviset s majetkem nebo pracovním příkazem.</span><span class="sxs-lookup"><span data-stu-id="03b11-123">Several documents might be related to an asset or a work order.</span></span> <span data-ttu-id="03b11-124">Úroveň servisu můžete upravit podle požadavku na údržbu nebo podle požadovaného pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="03b11-124">You can edit the service level on a maintenance request or a work order as you require.</span></span>

4. <span data-ttu-id="03b11-125">Vyberte **Přílohy**.</span><span class="sxs-lookup"><span data-stu-id="03b11-125">Select **Attachments**.</span></span> <span data-ttu-id="03b11-126">Zobrazí se standardní stránka **Zpracování dokumentu** zpracování dokumentu.</span><span class="sxs-lookup"><span data-stu-id="03b11-126">The standard **Document handling** page appears.</span></span>
5. <span data-ttu-id="03b11-127">Nastavte doklady nebo poznámky, které by měly být připojeny k záznamu dokumentu majetku.</span><span class="sxs-lookup"><span data-stu-id="03b11-127">Set up the documents or notes that should be attached to the asset document record.</span></span> <span data-ttu-id="03b11-128">Po připojení dokumentů zobrazí pole **Přílohy** počet dokumentů, které souvisejí se záznamem.</span><span class="sxs-lookup"><span data-stu-id="03b11-128">After you attach documents, the **Attachments** field shows the number of documents that are related to the record.</span></span>
