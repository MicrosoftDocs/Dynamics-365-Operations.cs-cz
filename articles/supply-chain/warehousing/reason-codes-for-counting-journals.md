---
title: Kódy důvodů pro inventury zásob
description: Toto téma popisuje, jak nastavit a použít kódy důvodů pro úlohy účtování.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: d72b171bfe149b25f5055d5bebef85b49e952295
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228482"
---
# <a name="reason-codes-for-inventory-counting"></a><span data-ttu-id="5adec-103">Kódy důvodů pro inventury zásob</span><span class="sxs-lookup"><span data-stu-id="5adec-103">Reason codes for inventory counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5adec-104">Kódy důvodů umožňují analyzovat výsledky procesu inventury a jakýkoli nesoulad, který se vyskytne během tohoto procesu.</span><span class="sxs-lookup"><span data-stu-id="5adec-104">Reason codes let you analyze the results of a counting process and any discrepancies that occur during that process.</span></span> <span data-ttu-id="5adec-105">Můžete určit důvod pro provádění inventury, například rozbitou paletu nebo úpravu zásob, založenou na vzorku zásob.</span><span class="sxs-lookup"><span data-stu-id="5adec-105">You can specify the reason for doing the count, such as a broken pallet or a stock adjustment that is based on inventory samples.</span></span>

## <a name="recommendation"></a><span data-ttu-id="5adec-106">Doporučení</span><span class="sxs-lookup"><span data-stu-id="5adec-106">Recommendation</span></span>

<span data-ttu-id="5adec-107">Před nastavením systému doporučujeme nejprve definovat strategii pro práci s kódy důvodu.</span><span class="sxs-lookup"><span data-stu-id="5adec-107">Before you set up the system, we recommend that you define a strategy for working with reason codes.</span></span> <span data-ttu-id="5adec-108">Zkuste například zodpovědět následující otázky:</span><span class="sxs-lookup"><span data-stu-id="5adec-108">For example, try to answer the following questions:</span></span>

- <span data-ttu-id="5adec-109">Měly by být kódy důvodů povinné na skladech?</span><span class="sxs-lookup"><span data-stu-id="5adec-109">Should reason codes be mandatory on warehouses?</span></span>
- <span data-ttu-id="5adec-110">Měly by být kódy důvodů povinné nebo volitelné na některých položkách?</span><span class="sxs-lookup"><span data-stu-id="5adec-110">Should reason codes be mandatory or optional on some items?</span></span>
- <span data-ttu-id="5adec-111">Kolik kódů důvodů vyžadujete?</span><span class="sxs-lookup"><span data-stu-id="5adec-111">How many reason codes do you require?</span></span>
- <span data-ttu-id="5adec-112">Jak by měli uživatelé čteček čárových kódů používat kódy důvodů?</span><span class="sxs-lookup"><span data-stu-id="5adec-112">How should users of barcode scanners use reason codes?</span></span> <span data-ttu-id="5adec-113">Měly by být kódy důvodů předvybrané, povinné nebo bez možnosti úpravy?</span><span class="sxs-lookup"><span data-stu-id="5adec-113">Should the reason codes be preselected, mandatory, or not editable?</span></span>
- <span data-ttu-id="5adec-114">Vyžadují pracovníci skladu různé chování kódů důvodů na mobilních čtečkách?</span><span class="sxs-lookup"><span data-stu-id="5adec-114">Do warehouse workers require different reason code behavior on mobile scanners?</span></span> <span data-ttu-id="5adec-115">Je-li odpověď ano, můžete vytvořit další položky nabídky a přiřadit je k různým osobám.</span><span class="sxs-lookup"><span data-stu-id="5adec-115">If the answer is yes, you can create more menu items and assign them to different people.</span></span>

## <a name="where-reason-codes-apply"></a><span data-ttu-id="5adec-116">Kde se kódy důvodů používají</span><span class="sxs-lookup"><span data-stu-id="5adec-116">Where reason codes apply</span></span>

<span data-ttu-id="5adec-117">Můžete vytvořit více zásad kódů důvodů a každá zásady kódů důvodů může mít dvě zásady kódů důvodu inventury.</span><span class="sxs-lookup"><span data-stu-id="5adec-117">You can create multiple reason code policies, and each reason code policy can have two counting reason code policies.</span></span> <span data-ttu-id="5adec-118">Zásady kódů důvodů inventury lze použít na úrovni skladu nebo na úrovni položky.</span><span class="sxs-lookup"><span data-stu-id="5adec-118">The counting reason code policies can be used at the warehouse level or the item level.</span></span>

## <a name="set-up-reason-code-policies"></a><span data-ttu-id="5adec-119">Nastavení zásad kódů důvodů</span><span class="sxs-lookup"><span data-stu-id="5adec-119">Set up reason code policies</span></span>

1. <span data-ttu-id="5adec-120">Vyberte **Řízení zásob** \> **Nastavení** \> **Zásoby** \> **Zásady kódů důvodů inventury** a vytvořte novou zásadu kódů důvodů.</span><span class="sxs-lookup"><span data-stu-id="5adec-120">Select **Inventory management** \> **Setup** \> **Inventory** \> **Counting reason code policies**, and create a new reason code policy.</span></span>
2. <span data-ttu-id="5adec-121">V poli **Typ kódu důvodů inventury** vyberte buď **Povinné** nebo **volitelné** a určete, zda výběr kódu důvodů má být volitelná nebo povinná akce v jednom z následujících deníků inventur:</span><span class="sxs-lookup"><span data-stu-id="5adec-121">In the **Counting reason code type** field, select either **Mandatory** or **Optional** to specify whether selection of a reason code should be an optional or mandatory action in one of the following counting journals:</span></span>

    - <span data-ttu-id="5adec-122">Cyklická inventura (mobilní zařízení)</span><span class="sxs-lookup"><span data-stu-id="5adec-122">Cycle Count (mobile device)</span></span>
    - <span data-ttu-id="5adec-123">Místní inventura (mobilní zařízení)</span><span class="sxs-lookup"><span data-stu-id="5adec-123">Spot Count (mobile device)</span></span>
    - <span data-ttu-id="5adec-124">Prahová inventura (mobilní zařízení)</span><span class="sxs-lookup"><span data-stu-id="5adec-124">Threshold Count (mobile device)</span></span>
    - <span data-ttu-id="5adec-125">Příchozí úprava (mobilní zařízení)</span><span class="sxs-lookup"><span data-stu-id="5adec-125">Adjustment In (mobile device)</span></span>
    - <span data-ttu-id="5adec-126">Odchozí úprava (mobilní zařízení)</span><span class="sxs-lookup"><span data-stu-id="5adec-126">Adjustment Out (mobile device)</span></span>
    - <span data-ttu-id="5adec-127">Deník inventur (plně funkční klient)</span><span class="sxs-lookup"><span data-stu-id="5adec-127">Counting Journal (rich client)</span></span>

<span data-ttu-id="5adec-128">Můžete také nastavit kódy důvodů pro jednotlivé sklady a produkty.</span><span class="sxs-lookup"><span data-stu-id="5adec-128">You can also set up reason codes for individual warehouses and for products.</span></span> <span data-ttu-id="5adec-129">Nastavení kódů důvodů pro produkty může nebrat v úvahu nastavení skladů.</span><span class="sxs-lookup"><span data-stu-id="5adec-129">The reason code setup for products can disregard the setup for warehouses.</span></span>

## <a name="mandatory-reason-codes"></a><span data-ttu-id="5adec-130">Povinné kódy důvodů</span><span class="sxs-lookup"><span data-stu-id="5adec-130">Mandatory reason codes</span></span>

<span data-ttu-id="5adec-131">Pokud je nastaven parametr **Povinné** v konfiguraci kódů důvodů pro sklady pro nebo položky, deník inventur nelze dokončit a uzavřít, dokud neí zadán kód důvodu.</span><span class="sxs-lookup"><span data-stu-id="5adec-131">If the **Mandatory** parameter is set in the configuration of reason codes for warehouses or items, the counting journal can't be completed and closed until a reason code is provided.</span></span>

### <a name="set-up-reason-codes-for-warehouses"></a><span data-ttu-id="5adec-132">Nastavení kódů důvodů pro sklady</span><span class="sxs-lookup"><span data-stu-id="5adec-132">Set up reason codes for warehouses</span></span>

1. <span data-ttu-id="5adec-133">Zvolte postupně možnosti **Řízení zásob** \> **Nastavení** \> **Rozdělení zásob** \> **Sklady**.</span><span class="sxs-lookup"><span data-stu-id="5adec-133">Select **Inventory Management** \> **Setup** \> **Inventory breakdown** \> **Warehouses**.</span></span>
2. <span data-ttu-id="5adec-134">Na kartě **Sklad** v poli **Zásady kódu důvodů inventry** vyberte některou z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="5adec-134">On the **Warehouse** tab, in the **Counting reason code policy** field, select one of the following options:</span></span>

    - <span data-ttu-id="5adec-135">**Prázdné** – Parametr, který je nastaven pro položku, se používá k určení, zda deníky inventur jsou pro produkt povinné.</span><span class="sxs-lookup"><span data-stu-id="5adec-135">**Blank** – The parameter that is set up for the item is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="5adec-136">**Povinné** – Kód důvodu je vyžadován vždy na denících inventury pro sklad.</span><span class="sxs-lookup"><span data-stu-id="5adec-136">**Mandatory** – A reason code is always required on counting journals for the warehouse.</span></span>
    - <span data-ttu-id="5adec-137">**Volitelné** – Kód důvodu není vyžadován na denících inventury pro sklad.</span><span class="sxs-lookup"><span data-stu-id="5adec-137">**Optional** – A reason code isn't required on counting journals for the warehouse.</span></span>

### <a name="set-up-reason-codes-for-products"></a><span data-ttu-id="5adec-138">Nastavení kódů důvodů pro produkty</span><span class="sxs-lookup"><span data-stu-id="5adec-138">Set up reason codes for products</span></span>

1. <span data-ttu-id="5adec-139">Zvolte **Řízení informací o produktech** \> **Produkty** \> **Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="5adec-139">Select **Product information management** \> **Products** \> **Released products**.</span></span>
2. <span data-ttu-id="5adec-140">Na kartě **Produkt** vyberte **Zásady kódu důvodů inventry** a poté vyberte některou z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="5adec-140">On the **Product** tab, select **Counting reason code policy**, and then select one of the following options:</span></span>

    - <span data-ttu-id="5adec-141">**Prázdné** – Parametr, který je nastaven pro sklad, se používá k určení, zda deníky inventur jsou pro produkt povinné.</span><span class="sxs-lookup"><span data-stu-id="5adec-141">**Blank** – The parameter that is set up for the warehouse is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="5adec-142">**Povinné** – Kód důvodu je vyžadován vždy na denících inventury pro produkt.</span><span class="sxs-lookup"><span data-stu-id="5adec-142">**Mandatory** – A reason code is always required on counting journals for the product.</span></span> <span data-ttu-id="5adec-143">Toto nastavení přepíše všechna nastavení kódu důvodu na úrovni skladu.</span><span class="sxs-lookup"><span data-stu-id="5adec-143">This setting overrides any reason code setting at the warehouse level.</span></span>
    - <span data-ttu-id="5adec-144">**Volitelné** – Kód důvodu není vyžadován na denících inventury pro produkt.</span><span class="sxs-lookup"><span data-stu-id="5adec-144">**Optional** – A reason code isn't required on counting journals for the product.</span></span> <span data-ttu-id="5adec-145">Toto nastavení přepíše všechna nastavení kódu důvodu na úrovni skladu.</span><span class="sxs-lookup"><span data-stu-id="5adec-145">This setting overrides any reason code setting at the warehouse level.</span></span>

### <a name="use-reason-codes-in-counting-journals"></a><span data-ttu-id="5adec-146">Použití kódů důvodů v deníku inventury</span><span class="sxs-lookup"><span data-stu-id="5adec-146">Use reason codes in counting journals</span></span>

<span data-ttu-id="5adec-147">V deníku inventur můžete přidat kódy důvodů pro inventury následujících typů:</span><span class="sxs-lookup"><span data-stu-id="5adec-147">In a counting journal, you can add reason codes for counts of the following types:</span></span>

- <span data-ttu-id="5adec-148">Cyklická inventura</span><span class="sxs-lookup"><span data-stu-id="5adec-148">Cycle Count</span></span>
- <span data-ttu-id="5adec-149">Místní inventura</span><span class="sxs-lookup"><span data-stu-id="5adec-149">Spot Count</span></span>
- <span data-ttu-id="5adec-150">Prahová inventura</span><span class="sxs-lookup"><span data-stu-id="5adec-150">Threshold Count</span></span>
- <span data-ttu-id="5adec-151">Příchozí úprava</span><span class="sxs-lookup"><span data-stu-id="5adec-151">Adjustment In</span></span>
- <span data-ttu-id="5adec-152">Odchozí úprava</span><span class="sxs-lookup"><span data-stu-id="5adec-152">Adjustment Out</span></span>

<span data-ttu-id="5adec-153">Kódy důvodů jsou přidány do řádků deníku v denících inventur tyou **Deník inventur**.</span><span class="sxs-lookup"><span data-stu-id="5adec-153">Reason codes are added to the journal lines in counting journals of the **Counting journal** type.</span></span>

1. <span data-ttu-id="5adec-154">Zvolte **Řízení zásob** \> **Položky deníku** \> **Inventura zboží** \> **Inventura**.</span><span class="sxs-lookup"><span data-stu-id="5adec-154">Select **Inventory management** \> **Journal entries** \> **Item counting** \> **Counting**.</span></span>
2. <span data-ttu-id="5adec-155">V podrobnostech řádku deníku inventury v poli **Kód důvodů inventury** vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="5adec-155">In the line details of the counting journal, in the **Counting reason code** field, select an option.</span></span>

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a><span data-ttu-id="5adec-156">Zobrazení historie inventur, jak ji zanamenaly kódy důvodů</span><span class="sxs-lookup"><span data-stu-id="5adec-156">View the counting history as it's recorded by reason codes</span></span>

- <span data-ttu-id="5adec-157">Vyberte **Řízení zásob** \> **Dotazy a sestavy** \> **Historie inventury** a pak v poli **Kód důvodů inventury** zobrazte historii inventury, která byla zaznamenána pomocí kódu důvodu.</span><span class="sxs-lookup"><span data-stu-id="5adec-157">Select **Inventory management** \> **Inquiries and reports** \> **Counting history**, and then, in the **Counting reason code** field, view the counting history that has been recorded through a reason code.</span></span>

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a><span data-ttu-id="5adec-158">Použití kódu důvodů pro úpravu množství</span><span class="sxs-lookup"><span data-stu-id="5adec-158">Use a reason code for a quantity adjustment</span></span>

1. <span data-ttu-id="5adec-159">Na stránce **Zásoby na skladě** vyberte **Upravit množství**.</span><span class="sxs-lookup"><span data-stu-id="5adec-159">On the **On-hand inventory** page, select **Adjust quantity**.</span></span> <span data-ttu-id="5adec-160">Můžete otevřít stránku **Zásoby na skladě** několika způsoby.</span><span class="sxs-lookup"><span data-stu-id="5adec-160">You can open the **On-hand inventory** page in several ways.</span></span> <span data-ttu-id="5adec-161">Například zvolte **Řízení zásob** \> **Dotazy a sestavy** \> **Zásoby na skladě**.</span><span class="sxs-lookup"><span data-stu-id="5adec-161">For example, select **Inventory management** \> **Inquiries and reports** \> **On-hand inventory**.</span></span>
2. <span data-ttu-id="5adec-162">Zvolte **Upravit množství** a pak v poli **Kód důvodů inventury** vyberte kód důvodu.</span><span class="sxs-lookup"><span data-stu-id="5adec-162">Select **Adjust quantity**, and then, in the **Counting reason code** field, select a reason code.</span></span>

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a><span data-ttu-id="5adec-163">Konfigurace kódů důvodů pro položky nabídky mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="5adec-163">Configure reason codes for mobile device menu items</span></span>

<span data-ttu-id="5adec-164">Můžete konfigurovat kódy důvodů pro jakýkoliv typ inventury na položce nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="5adec-164">You can configure reason codes for any type of count on a mobile device menu item.</span></span> <span data-ttu-id="5adec-165">Konfigurace položky nabídky mobilního zařízení obsahuje následující informace:</span><span class="sxs-lookup"><span data-stu-id="5adec-165">The configuration of the mobile device menu item includes the following information:</span></span>

- <span data-ttu-id="5adec-166">Zda je kód důvodu zobrazen pro pracovníka na mobilním zařízení při inventuře.</span><span class="sxs-lookup"><span data-stu-id="5adec-166">Whether the reason code is shown to the mobile device worker during counting.</span></span>
- <span data-ttu-id="5adec-167">Výchozí kód důvodu, který se zobrazí na položce nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="5adec-167">The default reason code that is shown on a mobile device menu item.</span></span>
- <span data-ttu-id="5adec-168">Zda uživatel může upravit kód důvodu.</span><span class="sxs-lookup"><span data-stu-id="5adec-168">Whether the user can edit the reason code.</span></span>

### <a name="set-up-reason-codes-on-a-mobile-device"></a><span data-ttu-id="5adec-169">Nastavení kódů důvodů na mobilním zařízení</span><span class="sxs-lookup"><span data-stu-id="5adec-169">Set up reason codes on a mobile device</span></span>

1. <span data-ttu-id="5adec-170">Přejděte do nabídky **Řízení skladu** \> **Nastavení** \> **Mobilní zařízení** \> **Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="5adec-170">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="5adec-171">Na kartě **Cyklická inventura** zvolte **Cyklická inventura**.</span><span class="sxs-lookup"><span data-stu-id="5adec-171">On the **Cycle count** tab, select **Cycle counting**.</span></span>
3. <span data-ttu-id="5adec-172">V poli **Výchozí kód důvodů inventury** nastavte výchozí kód důvodu, který má být zaznamenán po provedení inventury pomocí položky nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="5adec-172">In the **Default counting reason code** field, set the default reason code that should be recorded when counting is done by using the mobile device menu item.</span></span>
4. <span data-ttu-id="5adec-173">V poli **Zobrazit kód důvodů inventury** vyberte **Řádek** pro zobrazení kódu důvodu poté, co je zaznamenána každá odchylka.</span><span class="sxs-lookup"><span data-stu-id="5adec-173">In the **Display counting reason code** field, select **Line** to show the reason code after each variance is recorded.</span></span> <span data-ttu-id="5adec-174">Popřípadě zvolte **Skrýt**, pokud nemá být kód důvodu zobrazen.</span><span class="sxs-lookup"><span data-stu-id="5adec-174">Alternatively, select **Hide** if the reason code shouldn't be shown.</span></span>
5. <span data-ttu-id="5adec-175">Nastavte možnost **Upravit kód důvodů inventury** buď na možnost **Ano** nebo **Ne**.</span><span class="sxs-lookup"><span data-stu-id="5adec-175">Set the **Edit counting reason code** option to either **Yes** or **No**.</span></span> <span data-ttu-id="5adec-176">Pokud tuto možnost nastavíte na **Ano**, pracovník může upravovat kód důvodu, když se zobrazí během inventury na mobilním zařízení.</span><span class="sxs-lookup"><span data-stu-id="5adec-176">If you set this option to **Yes**, the worker can edit the reason code when it's shown on the mobile device during counting.</span></span>

> [!NOTE]
> <span data-ttu-id="5adec-177">Tlačítko **Cyklická inventura** může být povoleno na jakékoliv položce nabídky mobilního zařízení, na kterém lze provést inventuru.</span><span class="sxs-lookup"><span data-stu-id="5adec-177">The **Cycle counting** button can be enabled on any mobile device menu item where counting can be done.</span></span> <span data-ttu-id="5adec-178">Příklad zahrnuje položky nabídky pro místní inventury, práci řízenou uživatelem a práci řízenou systémem.</span><span class="sxs-lookup"><span data-stu-id="5adec-178">Example include the menu items for spot counts, user-directed work, and system-directed work.</span></span>

## <a name="cycle-count-approvals"></a><span data-ttu-id="5adec-179">Schválení cyklické inventury</span><span class="sxs-lookup"><span data-stu-id="5adec-179">Cycle count approvals</span></span>

<span data-ttu-id="5adec-180">Před schválením inventury uživatel může změnit kód důvodu, který je přidružen k inventuře.</span><span class="sxs-lookup"><span data-stu-id="5adec-180">Before a count is approved, the user can change the reason code that is associated with the count.</span></span> <span data-ttu-id="5adec-181">Po schválení inventury se zadává kód důvodu do řádků deníku inventur.</span><span class="sxs-lookup"><span data-stu-id="5adec-181">When the count is approved, the reason code is entered on the counting journal lines.</span></span>

### <a name="modify-cycle-count-approvals"></a><span data-ttu-id="5adec-182">Úprava schválení cyklické inventury</span><span class="sxs-lookup"><span data-stu-id="5adec-182">Modify cycle count approvals</span></span>

1. <span data-ttu-id="5adec-183">Vyberte **Řízení skladu** \> **Cyklická inventura** \> **Cyklická inventura práce čeká na kontrolu**.</span><span class="sxs-lookup"><span data-stu-id="5adec-183">Select **Warehouse management** \> **Cycle counting** \> **Cycle count work pending review**.</span></span>
2. <span data-ttu-id="5adec-184">Zvolte **Cyklická inventura** a pak v poli **Kód důvodu** vyberte nový kód důvodu.</span><span class="sxs-lookup"><span data-stu-id="5adec-184">Select **Cycle counting**, and then, in the **Reason code** field, select a new reason code.</span></span>

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a><span data-ttu-id="5adec-185">Úprava položky nabídky mobilního zařízení pro příchozí a odchozí úpravu</span><span class="sxs-lookup"><span data-stu-id="5adec-185">Modify the mobile device menu item for Adjustment in and Adjustment out</span></span>

1. <span data-ttu-id="5adec-186">Vyberte **Řízení skladu** \> **Nastavení** \> **Mobilní zařízení** \> **Položky nabídky mobilního zařízení** a poté vyberte **Příchozí a odchozí úpravy**.</span><span class="sxs-lookup"><span data-stu-id="5adec-186">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**, and then select **Adjustment in and out**.</span></span>
2. <span data-ttu-id="5adec-187">Nastavte hodnotu možnosti **Použít stávající práci** na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="5adec-187">Set the **Use existing work** option to **No**.</span></span>
3. <span data-ttu-id="5adec-188">V poli **Proces pro vytvoření práce** vyberte **Příchozí úprava**.</span><span class="sxs-lookup"><span data-stu-id="5adec-188">In the **Work creation process** field, select **Adjustment in**.</span></span>

<span data-ttu-id="5adec-189">Následující pole budou přidána do položky nabídky mobilního zařízení, když je během procesu vytváření práce vybrána **Příchozí úprava** nebo **Odchozí úprava**:</span><span class="sxs-lookup"><span data-stu-id="5adec-189">The following fields will be added to the mobile device menu item when **Adjustment in** or **Adjustment out** is selected during the work creation process:</span></span>

- <span data-ttu-id="5adec-190">Výchozí kód důvodů inventury</span><span class="sxs-lookup"><span data-stu-id="5adec-190">Default counting reason code</span></span>
- <span data-ttu-id="5adec-191">Zobrazit kód důvodů inventury</span><span class="sxs-lookup"><span data-stu-id="5adec-191">Display counting reason code</span></span>
- <span data-ttu-id="5adec-192">Upravit kód důvodů inventury</span><span class="sxs-lookup"><span data-stu-id="5adec-192">Edit counting reason code</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]