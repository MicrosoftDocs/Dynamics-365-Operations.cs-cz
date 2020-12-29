---
title: Ruční aktualizace čítačů majetku
description: Toto téma popisuje manuální aktualizaci čítačů majetku ve správě majetku.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23a94415a662059ddbd41cc6a0ba9dab24aae44e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423631"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="6eced-103">Ruční aktualizace čítačů majetku</span><span class="sxs-lookup"><span data-stu-id="6eced-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="6eced-104">Čítače slouží k vytváření registrací majetku, jako jsou například registrace o počtu hodin, kdy byl majetek v provozu, nebo množství, které bylo vyrobeno.</span><span class="sxs-lookup"><span data-stu-id="6eced-104">Counters are used to create registrations on an asset, such as registrations about the number of hours that the asset has been in operation or the quantity that has been produced.</span></span>

<span data-ttu-id="6eced-105">Typ čítače vybraný pro čítač může být nastaven tak, aby zdědil hodnoty čítačů.</span><span class="sxs-lookup"><span data-stu-id="6eced-105">The counter type that is selected for a counter might be set to inherit counter values.</span></span> <span data-ttu-id="6eced-106">Jinými slovy, možnost **Zdědit hodnoty čítače majetku** je nastavena na **Ano** na pevné záložce **Obecné** stránky **Čítače** (**Správa majetku** > **Nastavení** > **Typy majetku** > **Čítače**).</span><span class="sxs-lookup"><span data-stu-id="6eced-106">In other words, the **Inherit asset counter values** option is set to **Yes** on the **General** FastTab of the **Counters** page (**Asset management** > **Setup** > **Asset types** > **Counters**).</span></span> <span data-ttu-id="6eced-107">V takovém případě dojde při vytvoření nového řádku čítače daného typu k automatické aktualizaci všech podřízených položek, které používají stejný typ čítače.</span><span class="sxs-lookup"><span data-stu-id="6eced-107">In this case, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="6eced-108">Na stránce **Všechen majetek** vytváříte hodiny nebo registrace čítačů množství na majetku na základě vašich hodnot majetku.</span><span class="sxs-lookup"><span data-stu-id="6eced-108">On the **All assets** page, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="6eced-109">Vyberte **Správa majetku** > **Společné** > **Majetek** > **Všechen majetek**.</span><span class="sxs-lookup"><span data-stu-id="6eced-109">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="6eced-110">Vyberte majetek a pak v podokně akcí na kartě **majetek** ve skupině **Preventivní** vyberte možnost **čítače**.</span><span class="sxs-lookup"><span data-stu-id="6eced-110">Select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span> <span data-ttu-id="6eced-111">Na stránce **Čítače majetku** se zobrazí seznam všech předchozích registrací čítačů u vybraného majetku.</span><span class="sxs-lookup"><span data-stu-id="6eced-111">The **Asset counters** page shows a list of all previous counter registrations that have been made on the selected asset.</span></span>

3. <span data-ttu-id="6eced-112">Zvolte **Nový** pro vytvoření registrace.</span><span class="sxs-lookup"><span data-stu-id="6eced-112">Select **New** to create a registration.</span></span> <span data-ttu-id="6eced-113">ID majetku je automaticky zadáno do pole **Majetek**.</span><span class="sxs-lookup"><span data-stu-id="6eced-113">The asset ID is automatically entered in the **Asset** field.</span></span>

4. <span data-ttu-id="6eced-114">V poli **Čítač** vyberte relevantní čítač.</span><span class="sxs-lookup"><span data-stu-id="6eced-114">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="6eced-115">Vybrat lze pouze čítače související s typem majetku vybraným pro majetek.</span><span class="sxs-lookup"><span data-stu-id="6eced-115">Only counters that are related to the asset type selected on the asset are available for selection.</span></span> <span data-ttu-id="6eced-116">Související jednotka je automaticky zadána do pole **Jednotka**.</span><span class="sxs-lookup"><span data-stu-id="6eced-116">The related unit is automatically entered in the **Unit** field.</span></span>

5. <span data-ttu-id="6eced-117">V poli **zaregistrováno** vyberte datum a čas pro registraci čítače.</span><span class="sxs-lookup"><span data-stu-id="6eced-117">In the **Registered** field, select the date and time for the counter registration.</span></span>

6. <span data-ttu-id="6eced-118">Do pole **Hodnota** zadejte číslo od poslední registrace čítače.</span><span class="sxs-lookup"><span data-stu-id="6eced-118">In the **Value** field, enter the number since the last counter registration.</span></span> <span data-ttu-id="6eced-119">Případně zadejte do pole **Agregovaná hodnota** číslo celkového součtu.</span><span class="sxs-lookup"><span data-stu-id="6eced-119">Alternatively, in the **Aggregated value** field, enter the total count number.</span></span>

<span data-ttu-id="6eced-120">Mějte na paměti následující body:</span><span class="sxs-lookup"><span data-stu-id="6eced-120">Note the following points:</span></span>

- <span data-ttu-id="6eced-121">Pokud fyzicky instalujete do majetku nový čítač, je nutné provést registraci v položce majetku na stránce **Čítače majetku**.</span><span class="sxs-lookup"><span data-stu-id="6eced-121">If you physically install a new counter on an asset, you must register the change on the asset on the **Asset counters** page.</span></span> <span data-ttu-id="6eced-122">Dále je nutné vytvořit dva řádky pro registraci, které mají totožná časová razítka.</span><span class="sxs-lookup"><span data-stu-id="6eced-122">Next, you must create two registration lines that have identical timestamps.</span></span> <span data-ttu-id="6eced-123">První řádek musí být pro čítač, který nahrazujete.</span><span class="sxs-lookup"><span data-stu-id="6eced-123">The first line must be for the counter that you're replacing.</span></span> <span data-ttu-id="6eced-124">V řádku, který se vztahuje k novému čítači, zaškrtněte políčko **Vynulovat čítač**.</span><span class="sxs-lookup"><span data-stu-id="6eced-124">On the line that is related to the new counter, select the **Counter reset** check box.</span></span> <span data-ttu-id="6eced-125">V poli **Celkem** je celkové číslo součtem čítače všech registrovaných hodnot tohoto typu čítače.</span><span class="sxs-lookup"><span data-stu-id="6eced-125">In the **Totals** field, the total count number is the sum of the counter totals of all registered values on that counter type.</span></span>

- <span data-ttu-id="6eced-126">Pokud je u majetku zaškrtnuto políčko **Vynulovat čítač** s použitím plánu údržby s typem intervalu "jednou z..." nebo "po dosažení...", čítač je v novém řádku čítače stále aktivní, protože vytváříte oddělený řádek čítače a začínáte znovu s novým čítačem.</span><span class="sxs-lookup"><span data-stu-id="6eced-126">If the **Counter reset** check box is selected on an asset using a maintenance plan that has a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line, because you create a separate counter line and start over with a new counter.</span></span>

<span data-ttu-id="6eced-127">Následující ilustrace znázorňuje příklad stránky **Čítače majetku**.</span><span class="sxs-lookup"><span data-stu-id="6eced-127">The illustration below shows an example of the **Asset counters** page.</span></span>

![Obrázek č. 1](media/11-work-orders.png)

<span data-ttu-id="6eced-129">Na stránce **Čítače majetku** (**Správa majetku** > **Dotazy** > **Majetek** > **Čítače majetku**) můžete zaregistrovat čítače u několika majetků najednou.</span><span class="sxs-lookup"><span data-stu-id="6eced-129">On the **Asset counters** page (**Asset management** > **Inquiries** > **Assets** > **Asset counters**), you can make counter registrations on several assets at the same time, as you require.</span></span>

>[!NOTE]
><span data-ttu-id="6eced-130">Rozsah lze nastavit tak, aby definoval odchylky v ručních registracích čítačů.</span><span class="sxs-lookup"><span data-stu-id="6eced-130">You can set up a range to define deviations in manual counter registrations.</span></span> <span data-ttu-id="6eced-131">Můžete také určit typ zprávy, která se zobrazí v případě, že se registrace nacházejí mimo definovaný rozsah.</span><span class="sxs-lookup"><span data-stu-id="6eced-131">You can also specify the type of message that is shown if registrations are outside the defined range.</span></span> <span data-ttu-id="6eced-132">Další informace o nastavení čítačů naleznete v tématu [Čítače](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="6eced-132">For more information about how to set up counters, see [Counters](../setup-for-objects/counters.md).</span></span>

