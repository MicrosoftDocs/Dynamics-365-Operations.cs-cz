---
title: Vytvoření seznamů úkolů a přidání úkolů
description: Tohle téma popisuje, jak vytvořit seznamy úkolů a jak do nich přidat úkoly v řešení Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 1cab31784db9f3242dce20e98762088436a5a8f8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410846"
---
# <a name="create-task-lists-and-add-tasks"></a><span data-ttu-id="c526d-103">Vytvoření seznamů úkolů a přidání úkolů</span><span class="sxs-lookup"><span data-stu-id="c526d-103">Create task lists and add tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c526d-104">Tohle téma popisuje, jak vytvořit seznamy úkolů a jak do nich přidat úkoly v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c526d-104">This topic describes how to create task lists and add tasks to them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c526d-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="c526d-105">Overview</span></span>

<span data-ttu-id="c526d-106">*Úkol* definuje určitou část práce nebo akci, kterou musí dokončit v určitém termínu splnění nebo před ním.</span><span class="sxs-lookup"><span data-stu-id="c526d-106">A *task* defines a specific piece of work or an action that someone must complete on or before a specified due date.</span></span> <span data-ttu-id="c526d-107">V Dynamics 365 Commerce může úkol obsahovat podrobné pokyny a informace o kontaktní osobě.</span><span class="sxs-lookup"><span data-stu-id="c526d-107">In Dynamics 365 Commerce, a task can include detailed instructions and information about a contact person.</span></span> <span data-ttu-id="c526d-108">Může rovněž zahrnovat odkazy na operace administrativy, operace pokladního místa (POS) nebo stránky webu, aby se zvýšila produktivita a byl poskytnut kontext, který vlastník úkolu potřebuje k efektivnímu dokončení úkolu.</span><span class="sxs-lookup"><span data-stu-id="c526d-108">It can also include links to back-office operations, point of sale (POS) operations, or site pages, to help improve productivity and provide the context that the task owner requires to complete the task efficiently.</span></span>

<span data-ttu-id="c526d-109">*Seznam úkolů* je sada úkolů, které je nutné provést jako součást obchodního procesu.</span><span class="sxs-lookup"><span data-stu-id="c526d-109">A *task list* is a collection of tasks that must be completed as part of a business process.</span></span> <span data-ttu-id="c526d-110">Může se například jednat o seznam úkolů, které musí nový pracovník provést během náboru, seznam úkolů pro pokladníky na noční směně nebo seznam úkolů, které musí být provedeny v rámci přípravy obchodu na nadcházející letní sezónu.</span><span class="sxs-lookup"><span data-stu-id="c526d-110">For example, there might be a task list that a new worker must complete during onboarding, a task list for cashiers who work evening shifts, or a task list that must be completed to prepare the store for an upcoming holiday season.</span></span> <span data-ttu-id="c526d-111">V Commerce lze každý seznam úkolů s cílovým datem přiřadit libovolnému počtu obchodů nebo zaměstnanců a lze u něj nastavit opakování.</span><span class="sxs-lookup"><span data-stu-id="c526d-111">In Commerce, every task list that has a target date can be assigned to any number of stores or employees, and it can be configured to recur.</span></span>

<span data-ttu-id="c526d-112">Seznamy úkolů mohou v administrativě Commerce vytvářet manažeři i pracovníci a poté je přiřadit k sadě obchodů.</span><span class="sxs-lookup"><span data-stu-id="c526d-112">Both managers and workers can create task lists in Commerce back office, and then assign them to a set of stores.</span></span>

## <a name="create-a-task-list"></a><span data-ttu-id="c526d-113">Vytvoření seznamu úkolů</span><span class="sxs-lookup"><span data-stu-id="c526d-113">Create a task list</span></span>

<span data-ttu-id="c526d-114">Pokud chcete vytvořit seznam úkolů, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="c526d-114">To create a task list, follow these steps.</span></span>

1. <span data-ttu-id="c526d-115">Přejděte na **Retail a Commerce \> Správa úkolů \> Řízení správy úkolů**.</span><span class="sxs-lookup"><span data-stu-id="c526d-115">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="c526d-116">Vyberte možnost **Nový** a poté zadejte hodnoty do polí **Název**, **Popis** a **Vlastník**.</span><span class="sxs-lookup"><span data-stu-id="c526d-116">Select **New**, and then enter values in the **Name**, **Description**, and **Owner** fields.</span></span>
1. <span data-ttu-id="c526d-117">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="c526d-117">Select **Save**.</span></span>

## <a name="add-tasks-to-a-task-list"></a><span data-ttu-id="c526d-118">Přidání úkolů do seznamu úkolů</span><span class="sxs-lookup"><span data-stu-id="c526d-118">Add tasks to a task list</span></span>

<span data-ttu-id="c526d-119">Chcete-li přidat úkol do seznamu úkolů, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="c526d-119">To add tasks to a task list, follow these steps.</span></span>
 
1. <span data-ttu-id="c526d-120">Na pevné záložce **Úkoly** v existujícím seznamu úkolů přidejte úkol výběrem možnosti **Nový**.</span><span class="sxs-lookup"><span data-stu-id="c526d-120">On the **Tasks** FastTab of an existing task list, select **New** to add a task.</span></span>
1. <span data-ttu-id="c526d-121">V dialogovém okně **Vytvořit nový úkol** zadejte v poli **Název** jedinečný název úkolu.</span><span class="sxs-lookup"><span data-stu-id="c526d-121">In the **Create a new task** dialog box, in the **Name** field, enter a name for the task.</span></span>
1. <span data-ttu-id="c526d-122">Do pole **Posun termínu splnění od cílového data** zadejte kladnou nebo zápornou celočíselnou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c526d-122">In the **Due data offset from target date** field, enter a positive or negative integer value.</span></span> <span data-ttu-id="c526d-123">Zadáte například hodnotu **-2** v případě, že má být úkol dokončen dva dny před termínem splnění seznamu úkolů.</span><span class="sxs-lookup"><span data-stu-id="c526d-123">For example, enter **-2** if the task should be completed two days before the task list's due date.</span></span>
1. <span data-ttu-id="c526d-124">Do pole **Poznámky** zadejte podrobné pokyny.</span><span class="sxs-lookup"><span data-stu-id="c526d-124">In the **Notes** field, enter detailed instructions.</span></span>
1. <span data-ttu-id="c526d-125">V poli **Kontaktní osoba** zadejte název odborníka na danou problematiku, kterého může vlastník úkolu kontaktovat v případě, že potřebuje pomoc.</span><span class="sxs-lookup"><span data-stu-id="c526d-125">In the **Contact person** field, enter the name of a subject matter expert that the task owner can contact if he or she needs help.</span></span>
1. <span data-ttu-id="c526d-126">V poli **Odkaz na úkol** zadejte odkaz na základě povahy úkolu.</span><span class="sxs-lookup"><span data-stu-id="c526d-126">In the **Task link** field, enter a link, based on the nature of the task.</span></span>

> [!TIP]
> <span data-ttu-id="c526d-127">Ačkoli můžete při vytváření seznamu úkolů použít pole **Přiřazeno k** pro přiřazení úkolů některému uživateli, doporučujeme vyhnout se přiřazování úkolů při vytváření seznamu úkolů.</span><span class="sxs-lookup"><span data-stu-id="c526d-127">Although you can use the **Assigned to** field to assign tasks to someone while you're creating a task list, we recommend that you avoid assigning tasks during task list creation.</span></span> <span data-ttu-id="c526d-128">Namísto toho přiřaďte úkoly po vytvoření instance seznamu pro jednotlivé obchody.</span><span class="sxs-lookup"><span data-stu-id="c526d-128">Instead, assign the tasks after the list is instantiated for individual stores.</span></span>

## <a name="use-task-links-to-help-improve-worker-productivity"></a><span data-ttu-id="c526d-129">Použití odkazů na úkoly pro zvýšení produktivity pracovníků</span><span class="sxs-lookup"><span data-stu-id="c526d-129">Use task links to help improve worker productivity</span></span>

<span data-ttu-id="c526d-130">Commerce vám umožňuje propojit úkoly s konkrétními operacemi POS, jako je například spuštění sestavy prodeje, zobrazení školicího videa online pro orientaci nového zaměstnance nebo provedení operace administrativy.</span><span class="sxs-lookup"><span data-stu-id="c526d-130">Commerce lets you link tasks to specific POS operations, such as running a sales report, viewing an online training video for new employee orientation, or performing a back-office operation.</span></span> <span data-ttu-id="c526d-131">Tato funkce pomáhá vlastníkům úkolů získat informace, které potřebují k efektivnímu dokončení úkolu.</span><span class="sxs-lookup"><span data-stu-id="c526d-131">This feature helps task owners get the information that they need to complete a task efficiently.</span></span>

<span data-ttu-id="c526d-132">Chcete-li při vytváření úlohy přidat odkazy na úkoly, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="c526d-132">To add task links while you create a task, follow these steps.</span></span>

1. <span data-ttu-id="c526d-133">Na pevné záložce **Úkoly** v existujícím seznamu úkolů vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="c526d-133">On the **Tasks** FastTab of an existing task list, select **Edit**.</span></span>
1. <span data-ttu-id="c526d-134">V dialogovém okně **Upravit úkol** v poli **Odkaz na úkol** vyberte jednu nebo více z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="c526d-134">In the **Edit task** dialog box, in the **Task link** field, select one or more of the following options:</span></span>

    - <span data-ttu-id="c526d-135">Vyberte **položku nabídky**, pro kterou chcete konfigurovat operaci zálohování, například „Produktové sady“.</span><span class="sxs-lookup"><span data-stu-id="c526d-135">Select **Menu item** to configure a back-office operation, such as "Product kits."</span></span>
    - <span data-ttu-id="c526d-136">Vyberte **Operace POS**, chcete-li konfigurovat operaci POS, například „Prodejní sestavy“.</span><span class="sxs-lookup"><span data-stu-id="c526d-136">Select **POS Operation** to configure a POS operation, such as "Sales reports."</span></span>
    - <span data-ttu-id="c526d-137">Vyberte možnost **Adresa URL** pro konfiguraci absolutní adresy URL.</span><span class="sxs-lookup"><span data-stu-id="c526d-137">Select **URL** to configure an absolute URL.</span></span>

<span data-ttu-id="c526d-138">Na následujícím obrázku je znázorněn výběr propojení úkolů v dialogovém okně **Upravit úkol**.</span><span class="sxs-lookup"><span data-stu-id="c526d-138">The following illustration shows the selection of task links in the **Edit task** dialog box.</span></span>

![Výběr odkazů na úkoly v dialogovém okně Upravit úkol](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a><span data-ttu-id="c526d-140">Konfigurace operace POS, aby ji bylo možné propojit s úkolem</span><span class="sxs-lookup"><span data-stu-id="c526d-140">Configure a POS operation so that it can be linked to a task</span></span>

<span data-ttu-id="c526d-141">Chcete-li nakonfigurovat operaci POS, aby ji bylo možné propojit s úkolem, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="c526d-141">To configure a POS operation so that it can be linked to a task, follow these steps.</span></span>

1. <span data-ttu-id="c526d-142">Přejděte do nabídky **Retail a Commerce \> Instalace kanálu \> Nastavení POS \> POS \> Operace POS**.</span><span class="sxs-lookup"><span data-stu-id="c526d-142">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="c526d-143">Vyberte možnost **Upravit**, vyhledejte operaci POS a zaškrtněte u ní políčko **Povolit správu úkolů**.</span><span class="sxs-lookup"><span data-stu-id="c526d-143">Select **Edit**, find the POS operation, and then select the **Enable Task Management** check box for it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c526d-144">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="c526d-144">Additional resources</span></span>

[<span data-ttu-id="c526d-145">Přehled správy úkolů</span><span class="sxs-lookup"><span data-stu-id="c526d-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="c526d-146">Konfigurace správy úkolů</span><span class="sxs-lookup"><span data-stu-id="c526d-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="c526d-147">Přiřazení seznamů úkolů k obchodům nebo zaměstnancům</span><span class="sxs-lookup"><span data-stu-id="c526d-147">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="c526d-148">Správa úkolů v POS</span><span class="sxs-lookup"><span data-stu-id="c526d-148">Task management in POS</span></span>](task-mgmt-POS.md)
