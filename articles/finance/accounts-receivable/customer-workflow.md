---
title: Workflow odběratele
description: Toto téma obsahuje informace o workflow odběratele. Změníte specifická pole pro odběratele a poté odešlete tyto změny ke schválení pomocí workflow, než budou přidána k odběrateli.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: af66887dda551d3820b744fbb96d7d13c897e71b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236883"
---
# <a name="customer-workflow"></a><span data-ttu-id="78eae-104">Workflow odběratele</span><span class="sxs-lookup"><span data-stu-id="78eae-104">Customer workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78eae-105">Do verze 8.0.4 bylo přidáno workflow odběratele.</span><span class="sxs-lookup"><span data-stu-id="78eae-105">The customer workflow has been added to version 8.0.4.</span></span> <span data-ttu-id="78eae-106">Můžete změnit specifická pole pro odběratele a poté odeslat tyto změny ke schválení pomocí workflow, než budou přidána k odběrateli.</span><span class="sxs-lookup"><span data-stu-id="78eae-106">You can change specific fields for a customer and then send those changes for approval by using the workflow before they are added to the customer.</span></span>

## <a name="set-up-the-customer-workflow"></a><span data-ttu-id="78eae-107">Nastavení workflow odběratele</span><span class="sxs-lookup"><span data-stu-id="78eae-107">Set up the customer workflow</span></span>

<span data-ttu-id="78eae-108">Než můžete použít funkci workflow odběratele, musíte ji povolit.</span><span class="sxs-lookup"><span data-stu-id="78eae-108">Before you can use the customer workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="78eae-109">Přejděte do **Pohledávky \> Nastavení \> Parametry pohledávek**.</span><span class="sxs-lookup"><span data-stu-id="78eae-109">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="78eae-110">Na kartě **Obecné** na pevné záložce **Schválení odběratele** nastavte možnost **Povolit schválení odběratele** na **Ano** pro povolení funkce.</span><span class="sxs-lookup"><span data-stu-id="78eae-110">On the **General** tab, on the **Customer approval** FastTab, set the **Enable customer approvals** option to **Yes** to enable the feature.</span></span>
3. <span data-ttu-id="78eae-111">V poli **Chování datových entit** zvolte chování, které mají datové entity použít při importu dat:</span><span class="sxs-lookup"><span data-stu-id="78eae-111">In the **Data entity behavior** field, select the behavior that the data entities should use when data is imported:</span></span>

    - <span data-ttu-id="78eae-112">**Povolit změny bez schválení** – Entita může aktualizovat záznam odběratele bez jeho zpracování pomocí workflow.</span><span class="sxs-lookup"><span data-stu-id="78eae-112">**Allow changes without approval** – An entity can update the customer record without processing it through the workflow.</span></span>
    - <span data-ttu-id="78eae-113">**Zamítnout změny** – Změny záznamu odběratele nelze provést.</span><span class="sxs-lookup"><span data-stu-id="78eae-113">**Reject changes** – Changes can't be made to the customer record.</span></span> <span data-ttu-id="78eae-114">Import se nezdaří pro pole, která jsou povolena pro workflow.</span><span class="sxs-lookup"><span data-stu-id="78eae-114">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="78eae-115">**Vytvořit návrhy změny** – Budou změněna všechna pole, kromě polí, která jsou povolena pro workflow.</span><span class="sxs-lookup"><span data-stu-id="78eae-115">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="78eae-116">Nové hodnoty pro tato pole budou přidány k odběrateli jako navrhované změny a workflow se automaticky spustí.</span><span class="sxs-lookup"><span data-stu-id="78eae-116">The new values for those fields will be added to the customer as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="78eae-117">V seznamu polí odběratele zvolte zaškrtávací políčko **Povolit** pro každé pole, které musí být schváleno předtím, než lze provést změny.</span><span class="sxs-lookup"><span data-stu-id="78eae-117">In the list of customer fields, select then **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="78eae-118">Přejděte do **Pohledávky \> Nastavení \> Workflow pohledávek**.</span><span class="sxs-lookup"><span data-stu-id="78eae-118">Go to **Accounts receivable \> Setup \> Accounts receivable workflows**.</span></span>
6. <span data-ttu-id="78eae-119">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="78eae-119">Select **New**.</span></span>
7. <span data-ttu-id="78eae-120">Zvolte **Workflow navrhované změny odběratele**.</span><span class="sxs-lookup"><span data-stu-id="78eae-120">Select **Proposed customer change workflow**.</span></span> 
8. <span data-ttu-id="78eae-121">Nastavte workflow, aby odpovídalo vašemu schvalovacímu procesu.</span><span class="sxs-lookup"><span data-stu-id="78eae-121">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="78eae-122">Prvek schválení workflow **Schválení workflow pro navrhovanou změnu odběratele** použije změny odběratele.</span><span class="sxs-lookup"><span data-stu-id="78eae-122">The **Workflow approval for proposed customer change** workflow approval element will apply the changes to the customer.</span></span>

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="78eae-123">Změna informací odběratele a odeslání změn do workflow</span><span class="sxs-lookup"><span data-stu-id="78eae-123">Change customer information and submit the changes to the workflow</span></span>

<span data-ttu-id="78eae-124">Když změníte pole, které je povoleno pro workflow, zobrazí se stránka **Navrhované změny**.</span><span class="sxs-lookup"><span data-stu-id="78eae-124">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="78eae-125">Tato stránka zobrazí původní hodnotu pole a novou hodnotu, kterou jste zadali.</span><span class="sxs-lookup"><span data-stu-id="78eae-125">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="78eae-126">Pole, které jste změnili, se vrátí na svou původní hodnotu.</span><span class="sxs-lookup"><span data-stu-id="78eae-126">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="78eae-127">Stavová zpráva na stránce vás informuje o tom, že změny nebyly odeslány.</span><span class="sxs-lookup"><span data-stu-id="78eae-127">A status message on the page informs you that your changes haven't been submitted.</span></span>

<span data-ttu-id="78eae-128">Pokaždé, když změníte pole, které je povoleno pro workflow, přidá se toto pole k seznamu navržených změn.</span><span class="sxs-lookup"><span data-stu-id="78eae-128">Every time that you change a field that is enabled for the workflow, that field is added to the list of proposed changes.</span></span> <span data-ttu-id="78eae-129">Chcete-li zahodit navrhovanou hodnotu pro pole, použijte tlačítko **Zahodit** vedle pole v seznamu.</span><span class="sxs-lookup"><span data-stu-id="78eae-129">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="78eae-130">Chcete-li zahodit všechny změny, použijte tlačítko **Zahodit všechny změny** ve spodní části stránky.</span><span class="sxs-lookup"><span data-stu-id="78eae-130">To discard all changes, use the **Discard all change** button at the bottom of the page.</span></span> <span data-ttu-id="78eae-131">Zvolte **OK** pro zavření stránky.</span><span class="sxs-lookup"><span data-stu-id="78eae-131">Select **OK** to close the page.</span></span>

<span data-ttu-id="78eae-132">Jakmile máte alespoň jednu navrhovanou změnu, zobrazí se další dvě nabídky v podokně akcí: **Navrhované změny** a **Workflow**.</span><span class="sxs-lookup"><span data-stu-id="78eae-132">After you have at least one proposed change, two additional menus appear on the Action Pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="78eae-133">Zvolte **Navrhované změny** pro otevření stránky **Navrhované změny** a zkontrolujte své změny.</span><span class="sxs-lookup"><span data-stu-id="78eae-133">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="78eae-134">Zvolte **Workflow \> Odeslat** pro odeslání změn do workflow.</span><span class="sxs-lookup"><span data-stu-id="78eae-134">Select **Workflow \> Submit** to submit the changes to the workflow.</span></span>

    <span data-ttu-id="78eae-135">Stav na stránce se změní na **Změny čekající na schválení**.</span><span class="sxs-lookup"><span data-stu-id="78eae-135">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="78eae-136">Pracovní postup následuje standardní procesu pracovního postupu v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="78eae-136">The workflow follows the standard workflow process in the application.</span></span> <span data-ttu-id="78eae-137">Schvalovatel je přesměrován na stránku **Zákazník**, kde může zkontrolovat změny na stránce **Navrhované změny** a poté zvolit **Workflow \> Schválit** pro schválení pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="78eae-137">The approver is directed to the **Customer** page where the changes can be reviewed on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="78eae-138">Po dokončení všech schválení jsou pole aktualizována hodnotami, které jste navrhli.</span><span class="sxs-lookup"><span data-stu-id="78eae-138">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]