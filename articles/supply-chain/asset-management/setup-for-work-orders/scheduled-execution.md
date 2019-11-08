---
title: Plánované provedení
description: Tohle téma popisuje plánované provedení v modulu Správa majetku.
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
ms.openlocfilehash: 89e13179e17b7cf075d631bc65d82da5f24da624
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569839"
---
# <a name="scheduled-execution"></a><span data-ttu-id="0ea90-103">Plánované provedení</span><span class="sxs-lookup"><span data-stu-id="0ea90-103">Scheduled execution</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="0ea90-104">Úrovně služeb pracovního příkazu lze použít k nastavení plánovaného provedení.</span><span class="sxs-lookup"><span data-stu-id="0ea90-104">You can use work order service levels to set up scheduled execution.</span></span> <span data-ttu-id="0ea90-105">(Další informace o úrovních služeb pracovního příkazu naleznete v tématu [Úroveň služby a popis](service-level-and-description.md).) Naplánované provádění poskytuje flexibilitu v plánování práce pro pracovníky údržby, protože lze nastavit podrobnější nebo méně podrobné požadavky pro interval, po který má být pracovní příkaz dokončen.</span><span class="sxs-lookup"><span data-stu-id="0ea90-105">(For more information about work order service levels, see [Service level and description](service-level-and-description.md).) Scheduled execution provides flexibility in work planning for maintenance workers, because you can set up more detailed or less detailed requirements for the interval that a work order should be completed during.</span></span> <span data-ttu-id="0ea90-106">Například pracovníka údržby, který dokončuje úlohu rychleji než je očekáváno ve výrobním zařízení, může přejít k jiné blízké úloze, která byla naplánována pro aktuální týden, ale ne nutně pro aktuální den.</span><span class="sxs-lookup"><span data-stu-id="0ea90-106">For example, a maintenance worker who completes a job faster than expected in a production facility might be able to move on to another nearby job that was planned for the current week but not necessarily for the current day.</span></span> <span data-ttu-id="0ea90-107">Tento přístup umožňuje optimalizaci plánování pracovníků a dokončení úlohy.</span><span class="sxs-lookup"><span data-stu-id="0ea90-107">This approach allows for optimization of worker planning and job completion.</span></span>

<span data-ttu-id="0ea90-108">Plánovaná úloha nastavení, která souvisí s pracovními příkazy, může být obecná nebo specifická.</span><span class="sxs-lookup"><span data-stu-id="0ea90-108">Scheduled execution setup, which is related to work orders, can be generic or specific.</span></span> <span data-ttu-id="0ea90-109">Můžete nastavit obecné řádky, které nejsou omezeny na specifické typy pracovních objednávek, typy majetku a tak dále.</span><span class="sxs-lookup"><span data-stu-id="0ea90-109">You can set up generic lines that aren't limited to specific work order types, asset types, and so on.</span></span> <span data-ttu-id="0ea90-110">Případně můžete vytvořit naplánované řádky provedení, které se vztahují na určitý typ pracovního příkazu, typ majetku, typ úlohy údržby atd.</span><span class="sxs-lookup"><span data-stu-id="0ea90-110">Alternatively, you can create scheduled execution lines that apply to a specific work order type, asset type, maintenance job type, and so on.</span></span>

1. <span data-ttu-id="0ea90-111">Vyberte **Správa majetku** \> **Nastavení** \> **Pracovní příkazy** \> **Plánované provedení**.</span><span class="sxs-lookup"><span data-stu-id="0ea90-111">Select **Asset management** \> **Setup** \> **Work orders** \> **Scheduled execution**.</span></span>
2. <span data-ttu-id="0ea90-112">Vybere **Nový** k vytvoření řádku plánovaného provedení.</span><span class="sxs-lookup"><span data-stu-id="0ea90-112">Select **New** to create a scheduled execution line.</span></span>
3. <span data-ttu-id="0ea90-113">V polích **Funkční umístění**, **Typ pracovního příkazu**, **Typ majetku**, **Výrobce**, **Model**, **Kategorie typu úlohy údržby**, **Typ úlohy údržby**, **Varianta typu úlohy údržby** a **Obchod** vyberte hodnoty podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="0ea90-113">In the **Functional location**, **Work order type**, **Asset type**, **Manufacturer**, **Model**, **Maintenance job type category**, **Maintenance job type**, **Maintenance job type variant**, and **Trade** fields, select values as you require.</span></span>
4. <span data-ttu-id="0ea90-114">V vyberte úroveň služeb pracovního příkazu v poli **Úroveň služeb**.</span><span class="sxs-lookup"><span data-stu-id="0ea90-114">In the **Service level** field, select a work order service level.</span></span> <span data-ttu-id="0ea90-115">Pokud toto pole ponecháte prázdné, provedete nejobecnější typ řádku plánovaného provedení.</span><span class="sxs-lookup"><span data-stu-id="0ea90-115">If you leave this field blank, you make the most generic type of scheduled execution line.</span></span> <span data-ttu-id="0ea90-116">Příklad obecného řádku naleznete v prvním záznamu na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="0ea90-116">For an example of a generic line, see the first record in the illustration that follows.</span></span> <span data-ttu-id="0ea90-117">Tento řádek umožňuje naplánovat všechny pracovní příkazy, které nemají žádnou úroveň služby pracovního příkazu pro určité datum a čas.</span><span class="sxs-lookup"><span data-stu-id="0ea90-117">That line enables all work orders that have no work order service level to be scheduled for a specific date and time.</span></span>
5. <span data-ttu-id="0ea90-118">V poli **Plánované provedení** vyberte časový interval.</span><span class="sxs-lookup"><span data-stu-id="0ea90-118">In the **Scheduled execution** field, select the time interval.</span></span>
6. <span data-ttu-id="0ea90-119">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="0ea90-119">Select **Save**.</span></span>

![Plánované provedení](media/20-setup-for-work-orders.png)
