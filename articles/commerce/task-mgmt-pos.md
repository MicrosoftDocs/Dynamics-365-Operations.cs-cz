---
title: Správa úkolů v POS
description: V tomto tématu je popsána správa úkolů v aplikaci pokladního místa (POS) pro Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 889cc90b534de33ccd0e2bea367b2da42b5d72e0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006178"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="d5ae4-103">Správa úkolů v POS</span><span class="sxs-lookup"><span data-stu-id="d5ae4-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d5ae4-104">V tomto tématu je popsána správa úkolů v aplikaci pokladního místa (POS) pro Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

## <a name="overview"></a><span data-ttu-id="d5ae4-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="d5ae4-105">Overview</span></span>

<span data-ttu-id="d5ae4-106">Aplikace Dynamics 365 Commerce POS disponuje funkcemi správy úkolů, které umožňují manažerům a pracovníkům v obchodech spravovat úkoly a aktualizovat jejich stav.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-106">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="d5ae4-107">Pracovníci obchodu mohou získat přístup k úlohám buď výběrem dlaždice **Úkoly** na domovské stránce POS, nebo výběrem oznámení úkolu.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-107">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="d5ae4-108">Ve výchozím nastavení jsou pracovníci obchodu přesměrováni na kartu **Moje úkoly**, kde si mohou prohlédnout úkoly, které jsou jim přiřazeny.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-108">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="d5ae4-109">Mohou se však snadno přepnout na karty **Úkoly po termínu**, **Otevřené úkoly** a **Seznamy úkolů**.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-109">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="d5ae4-110">Operace úkolů pro manažery obchodu</span><span class="sxs-lookup"><span data-stu-id="d5ae4-110">Task operations for store managers</span></span>

<span data-ttu-id="d5ae4-111">Manažeři obchodu mohou v aplikaci POS provádět následující operace s použitím tlačítek na panelu příkazů:</span><span class="sxs-lookup"><span data-stu-id="d5ae4-111">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="d5ae4-112">**Přiřadit** – přiřazení vybraných úkolů pracovníkovi obchodu.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-112">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="d5ae4-113">**Stav úkolu** – změna stavu vybraných úkolů.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-113">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="d5ae4-114">**Filtr** – ve výchozím nastavení jsou zobrazeny pouze aktivní úlohy.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-114">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="d5ae4-115">Použitím filtrů však mohou manažeři zobrazit všechny úkoly, dokonce i úkoly, které byly dokončeny nebo zrušeny.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-115">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="d5ae4-116">**Nový úkol** – vytvoření úkolu na stávajícím seznamu úkolů nebo vytvoření jednoúčelového úkolu.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-116">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="d5ae4-117">Pracovníci obchodu mohou v aplikaci POS provádět následující operace s použitím tlačítek na panelu příkazů:</span><span class="sxs-lookup"><span data-stu-id="d5ae4-117">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="d5ae4-118">**Stav úkolu** – změna stavu vybraných úkolů.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-118">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="d5ae4-119">**Filtr** – ve výchozím nastavení jsou zobrazeny pouze aktivní úlohy.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-119">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="d5ae4-120">Použitím filtrů však mohou pracovníci zobrazit všechny úkoly, dokonce i úkoly, které byly dokončeny nebo zrušeny.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-120">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="d5ae4-121">Na následujícím obrázku je zobrazena karta **Vlastní úkoly** v aplikaci Commerce POS.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-121">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![Karta Moje úkoly v aplikaci Commerce POS](media/POS-task-management.png)

<span data-ttu-id="d5ae4-123">Následující obrázek znázorňuje kartu **Seznamy úkolů**.</span><span class="sxs-lookup"><span data-stu-id="d5ae4-123">The following illustration shows the **Task lists** tab.</span></span>

![Karta Seznamy úkolů v aplikaci Commerce POS](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="d5ae4-125">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="d5ae4-125">Additional resources</span></span>

[<span data-ttu-id="d5ae4-126">Přehled správy úkolů</span><span class="sxs-lookup"><span data-stu-id="d5ae4-126">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="d5ae4-127">Konfigurace správy úkolů</span><span class="sxs-lookup"><span data-stu-id="d5ae4-127">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="d5ae4-128">Vytvoření seznamů úkolů a přidání úkolů</span><span class="sxs-lookup"><span data-stu-id="d5ae4-128">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="d5ae4-129">Přiřazení seznamů úkolů k obchodům nebo zaměstnancům</span><span class="sxs-lookup"><span data-stu-id="d5ae4-129">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)
