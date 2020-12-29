---
title: Přidání závady do pracovního příkazu
description: Toto téma popisuje postup přidávání registrací závad do pracovních příkazů v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e82026f1d73e7368d93109bc0b895b7368ac84d4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423842"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="41205-103">Přidání chyby do pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="41205-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="41205-104">Můžete přidat závady nastavené v návrháři závad do pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="41205-104">You can add faults that were set up in the fault designer to a work order.</span></span> <span data-ttu-id="41205-105">Majetek vybraný v pracovním příkazu musí obsahovat typy majetku, ke kterým je připojen jeden nebo více záznamů závad.</span><span class="sxs-lookup"><span data-stu-id="41205-105">One or more fault records must be connected to the asset types that are used for the asset that is selected in the work order.</span></span> <span data-ttu-id="41205-106">Další informace o funkcích správy případů naleznete v tématu [Správa chyb](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="41205-106">For more information about the setup, see [Fault management](../setup-for-work-orders/fault-management.md).</span></span>

1. <span data-ttu-id="41205-107">Vyberte **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="41205-107">Select **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="41205-108">Vyberte pracovní příkaz, u kterého chcete provést registraci chyby, a v podokně akcí na kartě **Pracovní příkaz** ve skupině **Majetek** vyberte **Chyba majetku**.</span><span class="sxs-lookup"><span data-stu-id="41205-108">Select the work order to make a fault registration on, and then, on the Action Pane, on the **Work order** tab, in the **Asset** group, select **Asset fault**.</span></span>

3. <span data-ttu-id="41205-109">Na pevné záložce **Příznaky** vyberte **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="41205-109">On the **Symptoms** FastTab, select **Add line**.</span></span> <span data-ttu-id="41205-110">Do pole **Závada** se automaticky zadá pořadové číslo závady.</span><span class="sxs-lookup"><span data-stu-id="41205-110">A sequential fault number is automatically entered in the **Fault** field.</span></span>

4. <span data-ttu-id="41205-111">V poli **Příznak závady** vyberte příslušný příznak.</span><span class="sxs-lookup"><span data-stu-id="41205-111">In the **Fault symptom** field, select the relevant symptom.</span></span>

5. <span data-ttu-id="41205-112">V polích **Oblast chyby** a **Typ chyby** vyberte příslušné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="41205-112">In the **Fault area** and **Fault type** fields, select the appropriate values.</span></span>

6. <span data-ttu-id="41205-113">Do pole **Datum poruchy** se automaticky vloží aktuální datum.</span><span class="sxs-lookup"><span data-stu-id="41205-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="41205-114">Můžete vybrat jiné datum podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="41205-114">You can select a different date as you require.</span></span>

7. <span data-ttu-id="41205-115">Na pevné záložce **Příčiny vybraného příznaku** přidejte řádek popisující příčinu problému.</span><span class="sxs-lookup"><span data-stu-id="41205-115">On the **Causes for selected symptom** FastTab, add a line to describe the cause of the issue.</span></span>

8. <span data-ttu-id="41205-116">Na pevné záložce **Náprava vybraného příznaku** přidejte řádek popisující možné řešení problému.</span><span class="sxs-lookup"><span data-stu-id="41205-116">On the **Remedies for selected symptom** FastTab, add a line to describe a possible solution to the issue.</span></span>

9. <span data-ttu-id="41205-117">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="41205-117">Select **Save**.</span></span>

<span data-ttu-id="41205-118">Následující obrázek znázorňuje příklad stránky registrace závady.</span><span class="sxs-lookup"><span data-stu-id="41205-118">The illustration below shows an example of a fault registration.</span></span>

![Obrázek č. 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="41205-120">Zobrazení závad majetku</span><span class="sxs-lookup"><span data-stu-id="41205-120">View asset faults</span></span>

<span data-ttu-id="41205-121">V seznamu **Závady majetku** můžete získat přehled o všech závadách zaregistrovaných u majetku.</span><span class="sxs-lookup"><span data-stu-id="41205-121">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="41205-122">Na stránce seznamu **Závady majetku** můžete získat přehled o všech závadách zaregistrovaných u majetku.</span><span class="sxs-lookup"><span data-stu-id="41205-122">On the **Asset faults** list page, you can get an overview of all faults that have been registered on assets.</span></span> <span data-ttu-id="41205-123">Chcete-li stránku otevřít , vyberte **Správa majetku** > **Dotazy** > **Závada majetku** > **Závady majetku** a otevřete seznam.</span><span class="sxs-lookup"><span data-stu-id="41205-123">To open the page, select **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="41205-124">Tisk sestavy závad majetku</span><span class="sxs-lookup"><span data-stu-id="41205-124">Print asset fault report</span></span>

<span data-ttu-id="41205-125">Na stránce se seznamem **Všechen majetek** můžete vytisknout sestavu závad majetku zobrazující všechny registrace závad a grafický přehled statistik závad.</span><span class="sxs-lookup"><span data-stu-id="41205-125">From the **All assets** list page, you can print an asset fault report that shows all fault registrations and a graphical overview of fault statistics.</span></span>

1. <span data-ttu-id="41205-126">Vyberte **Správa majetku** > **Společné** > **Majetek** > **Všechen majetek**.</span><span class="sxs-lookup"><span data-stu-id="41205-126">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="41205-127">Vyberte majetek, pro který chcete vytisknout sestavu chyb.</span><span class="sxs-lookup"><span data-stu-id="41205-127">Select the asset to print a fault report for.</span></span>

3. <span data-ttu-id="41205-128">Na panelu akcí na kartě **Obecné** ve skupině **Sestavy** vyberte **Závada majetku**.</span><span class="sxs-lookup"><span data-stu-id="41205-128">On the Action Pane, on the **General** tab, in the **Reports** group, select **Asset fault**.</span></span>

4. <span data-ttu-id="41205-129">Zadejte konkrétní období nebo vyberte typ závady.</span><span class="sxs-lookup"><span data-stu-id="41205-129">Enter a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="41205-130">Klepnutím na tlačítko **OK** sestavu vytisknete.</span><span class="sxs-lookup"><span data-stu-id="41205-130">Select **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="41205-131">Můžete také vytisknout sestavu závad pro několik majetků nebo typů majetku výběrem **Správa majetku** > **Sestavy** > **Majatek** > **Závada majetku**.</span><span class="sxs-lookup"><span data-stu-id="41205-131">To print a fault report for several assets or asset types, select **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

