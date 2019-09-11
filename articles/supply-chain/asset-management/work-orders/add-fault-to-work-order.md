---
title: Přidání závady do pracovního příkazu
description: Toto téma popisuje postup přidávání registrací závad do pracovních příkazů v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875551"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="6852a-103">Přidání závady do pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="6852a-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="6852a-104">Můžete přidat závady nastavené v návrháři závad do pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="6852a-104">You can add faults set up in the fault designer to a work order.</span></span> <span data-ttu-id="6852a-105">Majetek vybraný v pracovním příkazu musí obsahovat typy majetku, ke kterým je připojen jeden nebo více záznamů závad.</span><span class="sxs-lookup"><span data-stu-id="6852a-105">The asset selected in the work order must contain asset types that have one or more fault records connected to it.</span></span> <span data-ttu-id="6852a-106">Další informace o nastavení naleznete v části [Správa poruch](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="6852a-106">Read more about setup in the [Fault management](../setup-for-work-orders/fault-management.md) section.</span></span>

1. <span data-ttu-id="6852a-107">Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="6852a-107">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="6852a-108">V seznamu vyberte pracovní příkaz, na kterém chcete provést registraci poruch, a klikněte na **Závada majetku**.</span><span class="sxs-lookup"><span data-stu-id="6852a-108">In the list, select the work order on which you want to make a fault registration and click **Asset fault**.</span></span>

3. <span data-ttu-id="6852a-109">Na záložce s náhledem **Příznaky** klikněte **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="6852a-109">On the **Symptoms** FastTab, click **Add line**.</span></span> <span data-ttu-id="6852a-110">Do pole **Závada** se automaticky zadá pořadové číslo závady.</span><span class="sxs-lookup"><span data-stu-id="6852a-110">A sequential fault number is automatically inserted in the **Fault** field.</span></span>

4. <span data-ttu-id="6852a-111">V poli **Příznak poruchy** vyberte příslušný příznak.</span><span class="sxs-lookup"><span data-stu-id="6852a-111">Select the relevant symptom in the **Fault symptom** field.</span></span>

5. <span data-ttu-id="6852a-112">Vyberte **Oblast poruchy** a **Typ poruchy**.</span><span class="sxs-lookup"><span data-stu-id="6852a-112">Select **Fault area** and **Fault type**.</span></span>

6. <span data-ttu-id="6852a-113">Do pole **Datum poruchy** se automaticky vloží aktuální datum.</span><span class="sxs-lookup"><span data-stu-id="6852a-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="6852a-114">V případě potřeby můžete vybrat jiné datum.</span><span class="sxs-lookup"><span data-stu-id="6852a-114">You can select another date, if necessary.</span></span>

7. <span data-ttu-id="6852a-115">Na záložce s náhledem **Příčiny vybraného příznaku** přidejte řádek popisující příčinu problému.</span><span class="sxs-lookup"><span data-stu-id="6852a-115">On the **Causes for selected symptom** FastTab, add a line describing the cause of the problem.</span></span>

8. <span data-ttu-id="6852a-116">Na záložce s náhledem **Náprava vybraného příznaku** přidejte řádek popisující možné řešení problému.</span><span class="sxs-lookup"><span data-stu-id="6852a-116">On the **Remedies for selected symptom** FastTab, add a line describing a possible solution to the problem.</span></span>

9. <span data-ttu-id="6852a-117">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="6852a-117">Click **Save**.</span></span>

![Obrázek č. 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="6852a-119">Zobrazení závad majetku</span><span class="sxs-lookup"><span data-stu-id="6852a-119">View asset faults</span></span>

<span data-ttu-id="6852a-120">V seznamu **Závady majetku** můžete získat přehled o všech závadách zaregistrovaných u majetku.</span><span class="sxs-lookup"><span data-stu-id="6852a-120">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="6852a-121">Klikněte na **Správa majetku** > **Dotazy** > **Závada majetku** > **Závady majetku** a otevřete seznam.</span><span class="sxs-lookup"><span data-stu-id="6852a-121">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults** to open the list.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="6852a-122">Tisk sestavy závad majetku</span><span class="sxs-lookup"><span data-stu-id="6852a-122">Print asset fault report</span></span>

<span data-ttu-id="6852a-123">Na stránce se seznamem **Všechen majetek** můžete vytisknout sestavu závad majetku zobrazující všechny registrace závad, stejně jako grafický přehled statistik závad.</span><span class="sxs-lookup"><span data-stu-id="6852a-123">From the **All assets** list page, you can print an asset fault report displaying all fault registrations as well as a graphic overview of fault statistics.</span></span>

1. <span data-ttu-id="6852a-124">Klikněte na **Správa majetku** > **Společné** > **Majetek** > **Všechen majetek**.</span><span class="sxs-lookup"><span data-stu-id="6852a-124">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="6852a-125">V seznamu **Majetek** vyberte majetek, pro který chcete vytisknout sestavu závad.</span><span class="sxs-lookup"><span data-stu-id="6852a-125">In the **Assets** list, select the asset for which you want to print a fault report.</span></span>

3. <span data-ttu-id="6852a-126">Na kartě **Obecné** > část **Sestavy** klikněte na **Závada majetku**.</span><span class="sxs-lookup"><span data-stu-id="6852a-126">On the **General** tab > **Reports section**, click **Asset fault**.</span></span>

4. <span data-ttu-id="6852a-127">Vložte určité období nebo vyberte typ závady.</span><span class="sxs-lookup"><span data-stu-id="6852a-127">Insert a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="6852a-128">Klepnutím na tlačítko **OK** sestavu vytisknete.</span><span class="sxs-lookup"><span data-stu-id="6852a-128">Click **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="6852a-129">Můžete také vytisknout sestavu závad pro několik majetků nebo typů majetku kliknutím na **SPráva majetku** > **Sestavy** > **Majatek** > **Závada majetku**.</span><span class="sxs-lookup"><span data-stu-id="6852a-129">You can also print a fault report for several assets or asset types by clicking **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

