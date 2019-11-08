---
title: Úrovně služby Majetek
description: V tomto tématu jsou vysvětleny úrovně služby Majetek v modulu Správa majetku.
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
ms.openlocfilehash: d1e2f8d2ac0c48d4f92b15ec345ffa650b71df0b
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571017"
---
# <a name="asset-service-levels"></a><span data-ttu-id="5da2c-103">Úrovně služby Majetek</span><span class="sxs-lookup"><span data-stu-id="5da2c-103">Asset service levels</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5da2c-104">V tomto tématu jsou vysvětleny úrovně služby Majetek v modulu Správa majetku.</span><span class="sxs-lookup"><span data-stu-id="5da2c-104">This topic explains asset service levels in Asset Management.</span></span> <span data-ttu-id="5da2c-105">Úrovně služby Majetek jsou spojeny s majetkem a jsou převedeny do požadavků na údržbu a pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="5da2c-105">Asset service levels are related to assets, and are transferred to maintenance requests and work orders.</span></span> <span data-ttu-id="5da2c-106">Používají se k výpočtu priority pracovních příkazů během plánování pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="5da2c-106">They are used to calculate the priority of work orders during work order scheduling.</span></span> <span data-ttu-id="5da2c-107">Úrovně služby majetek lze změnit, pokud jsou požadovány změny.</span><span class="sxs-lookup"><span data-stu-id="5da2c-107">Asset service levels can be changed, if changes are required.</span></span>

<span data-ttu-id="5da2c-108">Další informace o nastavení, které souvisí s výpočtem skóre hodnocení pro plánování pracovních příkazů, naleznete v tématu [Parametry Správy majetku](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5da2c-108">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span> <span data-ttu-id="5da2c-109">Je nutné nastavit alespoň jeden výchozí záznam pro úroveň služby Majetek.</span><span class="sxs-lookup"><span data-stu-id="5da2c-109">You must set up at least one default record for the asset service level.</span></span> <span data-ttu-id="5da2c-110">Tento výchozí záznam se používá v případě, že během plánování pracovních příkazů nebyla nalezena žádná jiná shoda.</span><span class="sxs-lookup"><span data-stu-id="5da2c-110">This default record is used if no other match is found during work order scheduling.</span></span>

<span data-ttu-id="5da2c-111">**Příklad 1:** výchozí úroveň služby, která se používá v případě, že nebyla nalezena žádná jiná shoda.</span><span class="sxs-lookup"><span data-stu-id="5da2c-111">**Example 1:** The default service level that is used if no other match is found.</span></span> <span data-ttu-id="5da2c-112">V tomto záznamu vyberete pouze úroveň služby.</span><span class="sxs-lookup"><span data-stu-id="5da2c-112">In this record, you select only a service level.</span></span>

<span data-ttu-id="5da2c-113">**Příklad 2:** vysoká úroveň služby, která slouží k naplánování prací pro motor kamionu Volvo.</span><span class="sxs-lookup"><span data-stu-id="5da2c-113">**Example 2:** A high service level that is used to schedule jobs for a Volvo truck engine.</span></span> <span data-ttu-id="5da2c-114">V tomto záznamu vyberete příslušný typ majetku (například **Motor nákladního vozu**), výrobce (**Volvo**) a úroveň služby.</span><span class="sxs-lookup"><span data-stu-id="5da2c-114">In this record, you select a relevant asset type (such as **Truck Engine**), a manufacturer (**Volvo**), and a service level.</span></span>

## <a name="set-up-asset-service-levels"></a><span data-ttu-id="5da2c-115">Nastavení úrovní služby Majetek</span><span class="sxs-lookup"><span data-stu-id="5da2c-115">Set up asset service levels</span></span>

1. <span data-ttu-id="5da2c-116">Vyberte **Správa majetku** \> **Nastavení** \> **Úrovně služby Majetek**.</span><span class="sxs-lookup"><span data-stu-id="5da2c-116">Select **Asset management** \> **Setup** \> **Asset service levels**.</span></span>
2. <span data-ttu-id="5da2c-117">Zvolte **Nový** pro vytvoření záznamu.</span><span class="sxs-lookup"><span data-stu-id="5da2c-117">Select **New** to create a record.</span></span>
3. <span data-ttu-id="5da2c-118">V závislosti a úrovni podrobností vyžadované pro úroveň služeb majetku proveďte příslušné výběry v polích **Funkční umístění**, **Typ majetku**, **Výrobce**, **Model**, **Majetek**, **Typ pracovního příkazu** a **Úroveň služby**.</span><span class="sxs-lookup"><span data-stu-id="5da2c-118">Depending on the detail level that is required for the asset service level, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Work order type**, and **Service level** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5da2c-119">Pokud je úroveň služby Majetek použita pro požadavky na údržbu a pracovní příkazy, bude správa majetku procházet všemi záznamy o úrovni služby Majetek, aby zkontrolovala možnou shodu.</span><span class="sxs-lookup"><span data-stu-id="5da2c-119">When the asset service level is used for maintenance requests and work orders, Asset Management goes through all asset service level records to check for a possible match.</span></span> <span data-ttu-id="5da2c-120">Vždy zkontroluje nejdříve nejkonkrétnější kombinaci.</span><span class="sxs-lookup"><span data-stu-id="5da2c-120">It always checks the most specific combination first.</span></span> <span data-ttu-id="5da2c-121">Jinými slovy, Správa majetku nejprve zkontroluje shodu v poli **Typ pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="5da2c-121">In other words, Asset Management first checks for a match for the **Work order type** field.</span></span> <span data-ttu-id="5da2c-122">Pokud není nalezena shoda, zkontroluje shodu v poli **Majetek** a tak dále.</span><span class="sxs-lookup"><span data-stu-id="5da2c-122">If no match is found, it checks for a match for the **Asset** field, and so on.</span></span> <span data-ttu-id="5da2c-123">Jak vidíte v rozvržení stránky **Úrovně služby Majetek**, toto chování znamená, že pro nalezení nejspecifičtější kombinace zkontroluje Správa majetku každý záznam zprava doleva pro nalezení shody.</span><span class="sxs-lookup"><span data-stu-id="5da2c-123">As you can see in the layout of the **Asset service levels** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="5da2c-124">Není-li nalezena shoda, použije se výchozí záznam, který nemá žádné výběry v těchto polích.</span><span class="sxs-lookup"><span data-stu-id="5da2c-124">If no match is found, the default record that has no selections in those fields is used.</span></span>

4. <span data-ttu-id="5da2c-125">V poli **Úroveň služby** vyberte číslo označující úroveň služby (priorita).</span><span class="sxs-lookup"><span data-stu-id="5da2c-125">In the **Service level** field, select a number that indicates the service level (priority).</span></span>


> [!NOTE]
> <span data-ttu-id="5da2c-126">Pokud změníte záznam úrovně služby Majetek na stránce **Úrovně služby Majetek** poté, co jste jej již použili v pracovním příkazu, nebude odpovídajícím způsobem aktualizována úroveň služby v požadavcích na údržbu a pracovních příkazech.</span><span class="sxs-lookup"><span data-stu-id="5da2c-126">If you change an asset service level record on the **Asset service levels** page after you've already used it on a work order, the service level on maintenance requests and work orders isn't updated accordingly.</span></span>
