---
title: Workflow dodavatele
description: Upravte informace o dodavateli a použijte k jejich schválení workflow.
author: mikefalkner
manager: annbe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 950a1852acf9f3e4747ce2d55738c0eb3a646897
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546771"
---
# <a name="vendor-workflow"></a><span data-ttu-id="6f389-103">Workflow dodavatele</span><span class="sxs-lookup"><span data-stu-id="6f389-103">Vendor workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f389-104">Při použití workflow dodavatele jsou změny určitých polí odeslány do workflow ke schválení před tím, než jsou přidány k dodavateli.</span><span class="sxs-lookup"><span data-stu-id="6f389-104">When the vendor workflow is used, changes that are made to specific fields are sent to the workflow for approval before they are added to the vendor.</span></span>

## <a name="set-up-the-vendor-workflow"></a><span data-ttu-id="6f389-105">Nastavení workflow dodavatele</span><span class="sxs-lookup"><span data-stu-id="6f389-105">Set up the vendor workflow</span></span>

<span data-ttu-id="6f389-106">Než budete funkci workflow moci používat, musíte ji povolit.</span><span class="sxs-lookup"><span data-stu-id="6f389-106">Before you can use the workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="6f389-107">Přejděte do nabídky **Závazky \> Nastavení \> Parametry závazků**.</span><span class="sxs-lookup"><span data-stu-id="6f389-107">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
2. <span data-ttu-id="6f389-108">Na kartě **Obecné** na pevné záložce **Schválení dodavatele** nastavte možnost **Povolit schválení dodavatele** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="6f389-108">On the **General** tab, on the **Vendor approval** FastTab, set the **Enable vendor approvals** option to **Yes**.</span></span>
3. <span data-ttu-id="6f389-109">V poli **Chování datových entit** vyberte chování, které chcete použít při importu dat:</span><span class="sxs-lookup"><span data-stu-id="6f389-109">In the **Data entity behavior** field, select the behavior that should be used when data is imported:</span></span>

    - <span data-ttu-id="6f389-110">**Povolit změny bez schválení** – datová entita může aktualizovat záznam dodavatele bez jeho zpracování přes workflow.</span><span class="sxs-lookup"><span data-stu-id="6f389-110">**Allow changes without approval** – The data entity can update the vendor record without processing it through the workflow.</span></span>
    - <span data-ttu-id="6f389-111">**Odmítnout změny** – změny záznamu dodavatele nelze provést.</span><span class="sxs-lookup"><span data-stu-id="6f389-111">**Reject changes** – Changes can't be made to the vendor record.</span></span> <span data-ttu-id="6f389-112">Import se nezdaří u polí, která jsou povolena pro workflow.</span><span class="sxs-lookup"><span data-stu-id="6f389-112">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="6f389-113">**Vytvořit návrhy změny** – všechna pole se změní, kromě polí, která jsou povolena pro workflow.</span><span class="sxs-lookup"><span data-stu-id="6f389-113">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="6f389-114">Nové hodnoty těchto polí budou přidány k dodavateli jako navržené změny a workflow se spustí automaticky.</span><span class="sxs-lookup"><span data-stu-id="6f389-114">The new values for those fields will be added to the vendor as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="6f389-115">Vyberte v seznamu polí dodavatele zaškrtávací políčko **Povolit** pro každé pole, které musí být schváleno před tím, než lze provést změny.</span><span class="sxs-lookup"><span data-stu-id="6f389-115">In the list of vendor fields, select the **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="6f389-116">Přejděte do nabídky **Závazky \> Nastavení \> Workflow závazků**.</span><span class="sxs-lookup"><span data-stu-id="6f389-116">Go to **Accounts payable \> Setup \> Accounts payable workflows**.</span></span>
6. <span data-ttu-id="6f389-117">Vyberte možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="6f389-117">Select **New**.</span></span>
7. <span data-ttu-id="6f389-118">Zvolte **Workflow navrhovaných změn dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="6f389-118">Select **Proposed vendor changes workflow**.</span></span> 
8. <span data-ttu-id="6f389-119">Nastavte workflow tak, aby odpovídalo vašemu procesu schvalování.</span><span class="sxs-lookup"><span data-stu-id="6f389-119">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="6f389-120">Prvek schválení workflow **Schválení workflow pro navrhovanou změnu dodavatele** použije změny pro dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6f389-120">The **Workflow approval for proposed vendor change** workflow approval element will apply the changes to the vendor.</span></span>

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="6f389-121">Změna informace o dodavateli a odeslání změn do workflow</span><span class="sxs-lookup"><span data-stu-id="6f389-121">Change vendor information and submit the changes to the workflow</span></span>

<span data-ttu-id="6f389-122">Při změně pole, které je povoleno pro workflow, se zobrazí stránka **Navrhované změny**.</span><span class="sxs-lookup"><span data-stu-id="6f389-122">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="6f389-123">Tato stránka zobrazí původní hodnotu pole a novou hodnotu, kterou jste zadali.</span><span class="sxs-lookup"><span data-stu-id="6f389-123">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="6f389-124">Pole, které jste změnili, se vrátí na původní hodnotu.</span><span class="sxs-lookup"><span data-stu-id="6f389-124">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="6f389-125">Stavová zpráva také informuje o tom, že vaše změny nebyly odeslány.</span><span class="sxs-lookup"><span data-stu-id="6f389-125">A status message also informs you that your changes haven't been submitted.</span></span> 

<span data-ttu-id="6f389-126">Vždy, když změníte pole, které je povoleno pro workflow, bude toto pole přidáno do seznamu na stránce **Navrhované změny**.</span><span class="sxs-lookup"><span data-stu-id="6f389-126">Every time that you change a field that is enabled for the workflow, that field is added to the list on the **Proposed changes** page.</span></span> <span data-ttu-id="6f389-127">Chcete-li zrušit navrženou hodnotu pro pole, použijte tlačítko **Zahodit** vedle pole v seznamu.</span><span class="sxs-lookup"><span data-stu-id="6f389-127">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="6f389-128">Chcete-li zahodit všechny změny, použijte tlačítko **Zahodit všechny změny** v dolní části stránky.</span><span class="sxs-lookup"><span data-stu-id="6f389-128">To discard all changes, use the **Discard all changes** button at the bottom of the page.</span></span> <span data-ttu-id="6f389-129">Vyberte **OK** a stránku zavřete.</span><span class="sxs-lookup"><span data-stu-id="6f389-129">Select **OK** to close the page.</span></span>

<span data-ttu-id="6f389-130">Až budete mít alespoň jednu navrženou změnu, zobrazí se další dvě karty v podokně akcí: **Navržené změny** a **Workflow**.</span><span class="sxs-lookup"><span data-stu-id="6f389-130">After you have at least one proposed change, two additional tabs appear on the action pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="6f389-131">Vyberte **Navržené změny**, otevře se stránka **Navržené změny** a zkontrolujte své změny.</span><span class="sxs-lookup"><span data-stu-id="6f389-131">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="6f389-132">Zvolte **Workflow \> Odeslat změny do workflow**.</span><span class="sxs-lookup"><span data-stu-id="6f389-132">Select **Workflow \> Submit to submit the changes to workflow**.</span></span>

    <span data-ttu-id="6f389-133">Stav na stránce se změní na **Změny čekající na schválení**.</span><span class="sxs-lookup"><span data-stu-id="6f389-133">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="6f389-134">Workflow postupuje podle standardního procesu workflow v aplikaci Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6f389-134">The workflow follows the standard workflow process in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="6f389-135">Schvalovatel je přesměrován na stránku **Dodavatel**, kde můžete zkontrolovat změny na stránce **Navržené změny** a poté vybrat **Workflowu \> Schválit** ke schválení workflow.</span><span class="sxs-lookup"><span data-stu-id="6f389-135">The approver is directed to the **Vendor** page, where he or she can review the changes on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="6f389-136">Po dokončení všech schválení jsou pole aktualizována hodnotami, které jste navrhli.</span><span class="sxs-lookup"><span data-stu-id="6f389-136">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>
