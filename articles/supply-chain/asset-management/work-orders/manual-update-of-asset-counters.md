---
title: Ruční aktualizace čítačů majetku
description: Toto téma popisuje manuální aktualizaci čítačů majetku ve správě majetku.
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875548"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="07557-103">Ruční aktualizace čítačů majetku</span><span class="sxs-lookup"><span data-stu-id="07557-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="07557-104">Čítače slouží k vytváření registrací položek majetku, které se týkají například počtu hodin v provozu nebo vyrobeného množství.</span><span class="sxs-lookup"><span data-stu-id="07557-104">Counters are used to create registrations on an asset regarding, for example, number of hours in operation, or the number of quantities produced.</span></span>

<span data-ttu-id="07557-105">Pokud je vybraný typ čítače nastaven na hodnotu zdědit hodnoty čítačů (pevná záložka **Správa majetku** > **Nastavení** > **Typy majetku** > **Čítače** > **Obecné** > přepínací tlačítko **zdědit hodnoty čítačů majetku** nastavené na hodnotu Ano), po vytvoření nového řádku čítače tohoto typu bude každý podřízený majetek, který používá stejný typ čítače, automaticky aktualizován.</span><span class="sxs-lookup"><span data-stu-id="07557-105">If the counter type selected for a counter is set to inherit counter values (**Asset management** > **Setup** > **Asset types** > **Counters** > **General** FastTab > **Inherit asset counter values** toggle button set to "Yes"), then, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="07557-106">V položce **Všechen majetek** vytváříte hodiny nebo registrace čítačů množství na majetku na základě vašich hodnot majetku.</span><span class="sxs-lookup"><span data-stu-id="07557-106">In **All assets**, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="07557-107">Klikněte na **Správa majetku** > **Společné** > **Majetek** > **Všechen majetek**.</span><span class="sxs-lookup"><span data-stu-id="07557-107">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="07557-108">Vyberte majetek v seznamu a klikněte na možnost **Čítače**.</span><span class="sxs-lookup"><span data-stu-id="07557-108">Select the asset in the list, and click **Counters**.</span></span> <span data-ttu-id="07557-109">Ve formuláři **Čítače majetku** se zobrazí seznam všech předchozích registrací čítačů vybraného majetku.</span><span class="sxs-lookup"><span data-stu-id="07557-109">In the **Asset counters** form, you see a list of all previous counter registrations on the selected asset.</span></span>

3. <span data-ttu-id="07557-110">Kliknutím na tlačítko **Nový** vytvořte novou registraci.</span><span class="sxs-lookup"><span data-stu-id="07557-110">Click **New** to create a new registration.</span></span> <span data-ttu-id="07557-111">ID majetku je vloženo automaticky.</span><span class="sxs-lookup"><span data-stu-id="07557-111">The asset ID is automatically inserted.</span></span>

4. <span data-ttu-id="07557-112">V poli **Čítač** vyberte relevantní čítač.</span><span class="sxs-lookup"><span data-stu-id="07557-112">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="07557-113">K dispozici jsou pouze čítače související s typem majetku vybraným pro majetek.</span><span class="sxs-lookup"><span data-stu-id="07557-113">Only counters related to the asset type selected on the asset are available.</span></span> <span data-ttu-id="07557-114">Související jednotka je automaticky vložena do pole **Jednotka**.</span><span class="sxs-lookup"><span data-stu-id="07557-114">The related unit is automatically inserted in the **Unit** field.</span></span>

5. <span data-ttu-id="07557-115">Vyberte datum a čas pro registraci čítače.</span><span class="sxs-lookup"><span data-stu-id="07557-115">Select date and time for the counter registration.</span></span>

6. <span data-ttu-id="07557-116">Do pole **Hodnota** zadejte číslo od poslední registrace čítače, nebo v poli **Agregovaná hodnota** zadejte celkové číslo.</span><span class="sxs-lookup"><span data-stu-id="07557-116">In the **Value** field, insert the number since the last counter registration, or, in the **Aggregated value** field, insert the total count number.</span></span>

- <span data-ttu-id="07557-117">Pokud fyzicky instalujete do majetku nový čítač, je nutné provést registraci v položce majetku v **Čítačích majetku**.</span><span class="sxs-lookup"><span data-stu-id="07557-117">If you physically install a new counter on an asset, you need to register the change on the asset in **Asset counters**.</span></span> <span data-ttu-id="07557-118">Dále je nutné vytvořit dva řádky registrace s identickými časovými razítky a na řádku, který se týká nového čítače, zaškrtněte tlačítko **Vynulovat čítač**.</span><span class="sxs-lookup"><span data-stu-id="07557-118">Next, you must create two registration lines with identical timestamps, and on the line regarding the new counter, you select the **Counter reset** check box.</span></span> <span data-ttu-id="07557-119">Po vytvoření dvou řádků registrace musí být první řádek pro čítač, který nahrazujete.</span><span class="sxs-lookup"><span data-stu-id="07557-119">When you create the two registration lines, the first line must be for the counter that you are replacing.</span></span> <span data-ttu-id="07557-120">V poli **Celkem** je celkové číslo součtem čítače všech registrovaných hodnot tohoto typu čítače.</span><span class="sxs-lookup"><span data-stu-id="07557-120">In the **Totals** field, the total count number is the sum of the counter total of all registered values on that counter type.</span></span>  
- <span data-ttu-id="07557-121">Pokud je u majetku zaškrtnuto políčko **Vynulovat čítač** s použitím plánu údržby s typem intervalu "jednou z..." nebo "po dosažení...", čítač je v novém řádku čítače stále aktivní, protože vytváříte oddělený řádek čítače a začínáte znovu s novým čítačem.</span><span class="sxs-lookup"><span data-stu-id="07557-121">If the **Counter reset** check box is selected on an asset using a maintenance plan with a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line because you create a separate counter line and start over with a new counter.</span></span>

![Obrázek č. 1](media/11-work-orders.png)


<span data-ttu-id="07557-123">Chcete-li provést registrace čítačů u několika majetků, lze to provést v **Správa majetku** > **Dotazy** > **Majetek** > **Čítače majetku**.</span><span class="sxs-lookup"><span data-stu-id="07557-123">If you need to make counter registrations on several assets, that can be done in **Asset management** > **Inquiries** > **Assets** > **Asset counters**.</span></span>

>[!NOTE]
><span data-ttu-id="07557-124">Můžete nastavit rozsah pro definování odchylek ručních registrací čítačů a typ zprávy, která se má zobrazit, pokud se registrace nacházejí mimo definovaný rozsah.</span><span class="sxs-lookup"><span data-stu-id="07557-124">You can set up a range to define deviations in manual counter registrations, and the type of message that should be displayed if registrations are outside the defined range.</span></span> <span data-ttu-id="07557-125">Informace o nastavení čítačů naleznete v tématu [Čítače](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="07557-125">Refer to the [Counters](../setup-for-objects/counters.md) topic regarding setup of counters.</span></span>
