---
title: Typy pracovních příkazů
description: Toto téma vysvětluje typy pracovních příkazů v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3e813bd4f2d47b928b6184bb063d9afa45695727
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569724"
---
# <a name="work-order-types"></a><span data-ttu-id="2331f-103">Typy pracovních příkazů</span><span class="sxs-lookup"><span data-stu-id="2331f-103">Work order types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="2331f-104">Typy pracovních příkazů se používají ke kategorizaci pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="2331f-104">Work order types are used to categorize work orders.</span></span> <span data-ttu-id="2331f-105">Můžete mít například pracovní příkazy, které souvisejí s preventivní údržbou nebo opravnou údržbou.</span><span class="sxs-lookup"><span data-stu-id="2331f-105">For example, you might have work orders that are related to preventive maintenance or corrective maintenance.</span></span>

<span data-ttu-id="2331f-106">Typ pracovního příkazu definuje umístění s modelem životního cyklu pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="2331f-106">A work order type defines an affiliation with a work order lifecycle model.</span></span> <span data-ttu-id="2331f-107">Model životního cyklu pracovních příkazů definuje stavy životního cyklu pracovního příkazu, které lze nastavit v rámci pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="2331f-107">A work order lifecycle model defines the work order lifecycle states that can be set on a work order.</span></span> <span data-ttu-id="2331f-108">(Příklady stavů životního cyklu pracovního příkazu jsou **Vytvořeno**, **Zpracovávání** a **Dokončeno**.)</span><span class="sxs-lookup"><span data-stu-id="2331f-108">(Examples of work order lifecycle states include **Created**, **In Process**, and **Finished**.)</span></span>

<span data-ttu-id="2331f-109">Další informace o stavech životního cyklu pracovního příkazu a fázích projektu naleznete v tématu [stavy životního cyklu pracovního příkazu](work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="2331f-109">For more information about work order lifecycle states and project stages, see [Work order lifecycle states](work-order-lifecycle-states.md).</span></span>

1. <span data-ttu-id="2331f-110">Vyberte **Správa majetku** \> **Nastavení** \> **Pracovní příkazy** \> **Typy pracovních příkazů**.</span><span class="sxs-lookup"><span data-stu-id="2331f-110">Select **Asset management** \> **Setup** \> **Work orders** \> **Work order types**.</span></span>
2. <span data-ttu-id="2331f-111">Zvolte **Nový** pro vytvoření typu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="2331f-111">Select **New** to create a work order type.</span></span>
3. <span data-ttu-id="2331f-112">V poli **Typ pracovního příkazu** zadejte ID pro typ pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="2331f-112">In the **Work order type** field, enter an ID for the work order type.</span></span>
4. <span data-ttu-id="2331f-113">Do pole **Název** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="2331f-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="2331f-114">Zvolte model životního cyklu v poli **Model životního cyklu pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="2331f-114">In the **Work order lifecycle model** field, select a lifecycle model.</span></span>
5. <span data-ttu-id="2331f-115">Nastavte možnost **Jeden pracovník údržby** na **Ano**, chcete-li, aby všechny úlohy pracovních příkazů související s pracovním pořadím tohoto typu byly naplánovány na téhož pracovníka údržby.</span><span class="sxs-lookup"><span data-stu-id="2331f-115">Set the **One maintenance worker** option to **Yes** if all work order jobs that are related to a work order of this type should be scheduled to the same maintenance worker.</span></span>
6. <span data-ttu-id="2331f-116">V poli **Typ nákladů** vyberte **Opravné**, **Preventivní** nebo **Investiční**.</span><span class="sxs-lookup"><span data-stu-id="2331f-116">In the **Cost type** field, select **Corrective**, **Preventive**, or **Investment**, as appropriate.</span></span> <span data-ttu-id="2331f-117">Všechny úlohy pracovního příkazu v pracovním příkazu musí mít stejný typ nákladů.</span><span class="sxs-lookup"><span data-stu-id="2331f-117">All work order jobs on a work order must have the same cost type.</span></span>
7. <span data-ttu-id="2331f-118">V oddílu **Povinné** nastavte příslušné možnosti na **Ano**, chcete-li určit, které informace týkající se poruchy nebo prostoje údržby jsou přidány k pracovnímu příkazu tohoto typu.</span><span class="sxs-lookup"><span data-stu-id="2331f-118">In the **Mandatory** section, set the relevant options to **Yes** to specify which fault-related or maintenance downtime–related information is added to a work order of this type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2331f-119">Možnosti v oddílu **Povinné** souvisejí s možnostmi na pevné záložce **Ověřit** na stránce **Stavy životního cyklu pracovního příkazu** (**Správa majetku** \> **Nastavení** \> **Pracovní příkazy** \> **Stavy životního cyklu**).</span><span class="sxs-lookup"><span data-stu-id="2331f-119">The options in the **Mandatory** section are related to the options on the **Validate** FastTab of the **Work order lifecycle states** page (**Asset management** \> **Setup** \> **Work orders** \> **Lifecycle states**).</span></span>

8. <span data-ttu-id="2331f-120">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="2331f-120">Select **Save**.</span></span>

![Typy pracovních příkazů](media/16-setup-for-work-orders.png)
