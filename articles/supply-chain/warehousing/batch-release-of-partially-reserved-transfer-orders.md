---
title: Vydání dávky částečně rezervovaných převodních příkazů
description: Toto téma popisuje, jak nastavit a použít vydání dávky částečně rezervovaných převodních příkazů z mobilního zařízení.
author: pjacobse
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSFulfillmentPolicy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 173e003fbddb0b021f87a8e28a553f4578b16e9b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977456"
---
# <a name="batch-release-of-partially-reserved-transfer-orders"></a><span data-ttu-id="13c86-103">Vydání dávky částečně rezervovaných převodních příkazů</span><span class="sxs-lookup"><span data-stu-id="13c86-103">Batch release of partially reserved transfer orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13c86-104">Funkce pro vydání dávky částečně rezervovaných převodních příkazů umožňuje částečně vydat převodní příkazy do skladu pomocí dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="13c86-104">The functionality for batch release of partially reserved transfer orders lets you partially release transfer orders to a warehouse by using a batch job.</span></span>
<span data-ttu-id="13c86-105">Vzhledem k tomu, že máte možnost vydat částečné množství, nemusíte čekat, než bude celé množství objednávky k dispozici ve skladu předtím, než objednávku vydáte.</span><span class="sxs-lookup"><span data-stu-id="13c86-105">Because you have the option to release a partial quantity, you don’t have to wait for the whole order quantity to be available in the warehouse before you release an order.</span></span>

<span data-ttu-id="13c86-106">Vydání objednávek pro sklad je rozšířený proces správy skladu.</span><span class="sxs-lookup"><span data-stu-id="13c86-106">The release of orders to a warehouse is an advanced warehouse management process.</span></span> <span data-ttu-id="13c86-107">Tento proces zahrnuje činnosti jako například výdej, balení a expedici, které může pracovník skladu provést pomocí mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="13c86-107">This process involves activities, such as picking, packing, and shipping, that a warehouse worker can perform by using a mobile device.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="13c86-108">Kdy se to používá</span><span class="sxs-lookup"><span data-stu-id="13c86-108">Where it applies</span></span>

<span data-ttu-id="13c86-109">Pro tuto funkci jsou převodní příkazy vydány do skladu pomocí dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="13c86-109">For this functionality, transfer orders are released to a warehouse by using a batch job.</span></span> <span data-ttu-id="13c86-110">Tato funkce je užitečná, pokud nemáte dostatek zásob ve skladu, ale stále chcete převést zboží z jednoho skladu do druhého.</span><span class="sxs-lookup"><span data-stu-id="13c86-110">This functionality is useful when you don’t have enough inventory in the warehouse, but you still want to transfer items from one warehouse to another.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="13c86-111">Způsob nastavení</span><span class="sxs-lookup"><span data-stu-id="13c86-111">How it is set up</span></span>

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="13c86-112">Určení kritérií plnění pro převodní příkazy a prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="13c86-112">Specify fulfillment criteria for transfer orders and sales orders</span></span>

<span data-ttu-id="13c86-113">Než může být objednávka částečně uvolněna do skladu v dávce, musí být splněna kritéria plnění.</span><span class="sxs-lookup"><span data-stu-id="13c86-113">Before an order can be partially released to a warehouse in a batch, the fulfillment criteria must be met.</span></span> <span data-ttu-id="13c86-114">Tato kritéria plnění jsou určena zásadami plnění.</span><span class="sxs-lookup"><span data-stu-id="13c86-114">These fulfillment criteria are determined by the fulfillment policy.</span></span>

<span data-ttu-id="13c86-115">Zásady plnění pro převodní příkazy a prodejní objednávky jsou určené na úrovni společnosti.</span><span class="sxs-lookup"><span data-stu-id="13c86-115">Fulfillment policies for transfer orders and sales orders are specified at the company level.</span></span> <span data-ttu-id="13c86-116">V závislosti na nastavení zásad plnění bude vydání objednávek v dávce přijato nebo zamítnuto.</span><span class="sxs-lookup"><span data-stu-id="13c86-116">Depending on the setup of the fulfillment policy, the release of orders in a batch will be accepted or rejected.</span></span> <span data-ttu-id="13c86-117">Objednávky budou poté podle toho zpracovány.</span><span class="sxs-lookup"><span data-stu-id="13c86-117">The orders will then be processed accordingly.</span></span>

-   <span data-ttu-id="13c86-118">Chcete-li vytvořit zásady plnění pro převodní příkazy a prodejní objednávky, klikněte na **Řízení skladu** \> **Nastavení** \> **Uvolnit do skladu** \> **Zásady plnění** a pak vytvořte zásadu plnění zadáním názvu a popisu.</span><span class="sxs-lookup"><span data-stu-id="13c86-118">To create fulfillment policies for transfer orders and sales orders, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then create a fulfillment policy by entering a name and a description.</span></span>

-   <span data-ttu-id="13c86-119">Chcete-li určit sazbu plnění, typ hodnoty a zprávu, která se zobrazí v případě porušení zásady plnění, klikněte na **Řízení skladu** \> **Nastavení** \> **Uvolnit do skladu** \> **Zásady plnění** a následně nastavte pole **Sazba plnění**, **Typ hodnoty** a **Zprávy porušení plnění**.</span><span class="sxs-lookup"><span data-stu-id="13c86-119">To specify a fulfillment rate, a value type, and the message that is shown if the fulfillment policy is violated, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then set the **Fulfillment rate**, **Value type**, and **Fulfillment violation message** fields.</span></span>

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="13c86-120">Nastavení zásad plnění pro převodní příkazy a prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="13c86-120">Set the fulfillment policies for transfer orders and sales orders</span></span>

-   <span data-ttu-id="13c86-121">Chcete-li nastavit zásady plnění pro převodní příkazy, klikněte **Řízení zásob** \> **Nastavení** \> **Parametry modulu Řízení zásob a skladu** \> **Převodní příkazy** \> **Řízení skladu** a poté vyberte zásadu plnění převodních příkazů.</span><span class="sxs-lookup"><span data-stu-id="13c86-121">To set the fulfillment policies for transfer orders, click **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters** \> **Transfer orders** \> **Warehouse management**, and then select a transfer order fulfillment policy.</span></span>

-   <span data-ttu-id="13c86-122">Chcete-li nastavit zásady plnění pro prodejní objednávky, klikněte na **Pohledávky** \> **Nastavení** \> **Parametry pohledávek** \> **Řízení skladu** a poté vyberte zásadu plnění prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="13c86-122">To set the fulfillment policies for sales orders, click **Accounts receivable** \> **Setup** \> **Accounts receivable parameters** \> **Warehouse management**, and then select a sales order fulfillment policy.</span></span>

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a><span data-ttu-id="13c86-123">Povolení vydání v dávce a určení množství, které je třeba uvolnit v dávce</span><span class="sxs-lookup"><span data-stu-id="13c86-123">Allow release in a batch and specify the quantity that should be release in a batch</span></span>

<span data-ttu-id="13c86-124">Dávková úloha se používá k uvolnění objednávek do skladu v dávce.</span><span class="sxs-lookup"><span data-stu-id="13c86-124">A batch job is used to release orders to a warehouse in a batch.</span></span> <span data-ttu-id="13c86-125">Parametry rozlišující objednávky, které mají být spuštěny v dávkové úloze, se nastavují na samotné dávkové úloze.</span><span class="sxs-lookup"><span data-stu-id="13c86-125">The parameters that distinguish the orders that should be run in a batch job are set on the batch job itself.</span></span>

<span data-ttu-id="13c86-126">Parametr **Množství** určuje, zda má být v dávce uvolněné fyzicky rezervované množství nebo celé množství.</span><span class="sxs-lookup"><span data-stu-id="13c86-126">The **Quantity** parameter specifies whether the whole quantity or the physically reserved quantity should be released in the batch.</span></span> <span data-ttu-id="13c86-127">Parametr **Povolit uvolnění částečně uvolněných objednávek** určuje, zda by objednávky v dávce měly být přijaty nebo zamítnuty, pokud byly částečně uvolněny dříve.</span><span class="sxs-lookup"><span data-stu-id="13c86-127">The **Allow release of partially released orders** parameter determines whether orders in the batch should be accepted or rejected if they were partially released earlier.</span></span>

-   <span data-ttu-id="13c86-128">Chcete-li nastavit **množství** a **Povolit uvolnění částečně uvolněných objednávek** pro převodní příkazy, klikněte na **Řízení skladu** \> **Uvolnit do skladu** \> **Automaticky uvolnit převodní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="13c86-128">To set the **Quantity** and **Allow release of partially released orders** parameters for transfer orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of transfer orders**.</span></span>

-   <span data-ttu-id="13c86-129">Chcete-li nastavit **množství** a **Povolit uvolnění částečně uvolněných objednávek** pro prodejní objednávky, klikněte na **Řízení skladu** \> **Uvolnit do skladu** \> **Automaticky uvolnit prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="13c86-129">To set the **Quantity** and **Allow release of partially released orders** parameters for sales orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of sales orders**.</span></span>
