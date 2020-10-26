---
title: Požadavků na položku servisní objednávky
description: Pokud pro objednávku služeb potřebujete rezervovat konkrétní zboží, můžete vytvořit požadavky na skladovou položku.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8866d8a4d6ad879f2c43b470af98457cb7c75721
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985733"
---
# <a name="service-order-item-requirements"></a><span data-ttu-id="8b95b-103">Požadavků na položku servisní objednávky</span><span class="sxs-lookup"><span data-stu-id="8b95b-103">Service order item requirements</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="8b95b-104">Můžete vytvářet objednávky služeb ke sledování a řízení služeb, které poskytujete odběratelům.</span><span class="sxs-lookup"><span data-stu-id="8b95b-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="8b95b-105">Pokud pro objednávku služeb potřebujete rezervovat konkrétní zboží, můžete vytvořit požadavky na skladovou položku.</span><span class="sxs-lookup"><span data-stu-id="8b95b-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="8b95b-106">Požadavek na položku může být okamžitě spotřebován ze skladu nebo může spustit výrobní zakázku zboží.</span><span class="sxs-lookup"><span data-stu-id="8b95b-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="8b95b-107">Použitím požadavků zboží namísto transakcí zboží můžete naplánovat dodávku těsně před vlastním použitím zboží, vytvořit prodejní objednávku, zahrnout zboží do rámce obchodní smlouvy nebo zahrnout požadavek na zboží do provozního plánování.</span><span class="sxs-lookup"><span data-stu-id="8b95b-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="8b95b-108">Požadavky zboží pro objednávky služeb jsou zpracovávány prostřednictvím projektu.</span><span class="sxs-lookup"><span data-stu-id="8b95b-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="8b95b-109">Chcete-li vytvořit pro objednávku služeb požadavek zboží, objednávka musí být přiřazena k projektu.</span><span class="sxs-lookup"><span data-stu-id="8b95b-109">To create an item requirement on a service order, the service order must be attached to a project.</span></span>

<span data-ttu-id="8b95b-110">Pokud je pro servisní zakázku vytvořen požadavek na položku, lze jej zobrazit v okně **Projekt** v rámci jednotlivé servisní zakázky nebo prostřednictvím formuláře **Prodejní objednávka** .</span><span class="sxs-lookup"><span data-stu-id="8b95b-110">As soon as an item requirement is created for a service order, it can be viewed from **Project** in the individual service order or through the **Sales order** form.</span></span>

## <a name="view-an-item-requirement-from-a-service-order"></a><span data-ttu-id="8b95b-111">Zobrazení požadavku na položku ze servisní zakázky</span><span class="sxs-lookup"><span data-stu-id="8b95b-111">View an item requirement from a service order</span></span>

1.  <span data-ttu-id="8b95b-112">Klikněte na uzel **Řízení služeb** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky** .</span><span class="sxs-lookup"><span data-stu-id="8b95b-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders** .</span></span>

2.  <span data-ttu-id="8b95b-113">Klikněte na **Expedice** a pak kliknutím na **Požadavek na položku** otevřete formulář **Požadavky na položku** .</span><span class="sxs-lookup"><span data-stu-id="8b95b-113">Click **Dispatch** , and then click **Item requirement** to open the **Item requirements** form.</span></span>

3.  <span data-ttu-id="8b95b-114">Klepněte na kartu **Projekt** a zkontrolujte, zda jsou v poli **Servisní zakázka** uvedeny servisní zakázky požadavků zboží.</span><span class="sxs-lookup"><span data-stu-id="8b95b-114">Click the **Project** tab, and check the **Service order** field to see the service orders of the item requirement.</span></span>

## <a name="delete-service-orders-with-item-requirements"></a><span data-ttu-id="8b95b-115">Odstranění servisních zakázek s požadavky na položky</span><span class="sxs-lookup"><span data-stu-id="8b95b-115">Delete service orders with item requirements</span></span>

<span data-ttu-id="8b95b-116">Pokud je pro určitou servisní zakázku vytvořen požadavek na položku, nelze danou servisní zakázku odstranit.</span><span class="sxs-lookup"><span data-stu-id="8b95b-116">If an item requirement is created on a service order, you cannot delete the service order.</span></span> <span data-ttu-id="8b95b-117">Požadavek na servisní zakázku je nutné nejprve odstranit a teprve poté lze odstranit i servisní zakázku.</span><span class="sxs-lookup"><span data-stu-id="8b95b-117">You must delete the item requirement before you can delete the service order.</span></span>

1.  <span data-ttu-id="8b95b-118">Klikněte na uzel **Řízení služeb** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky** .</span><span class="sxs-lookup"><span data-stu-id="8b95b-118">Click **Service management** \> **Common** \> **Service orders** \> **Service orders** .</span></span>

2.  <span data-ttu-id="8b95b-119">Klikněte na **Expedice** a pak kliknutím na **Požadavek na položku** otevřete formulář **Požadavky na položku** .</span><span class="sxs-lookup"><span data-stu-id="8b95b-119">Click **Dispatch** , and then click **Item requirement** to open the **Item requirements** form.</span></span> <span data-ttu-id="8b95b-120">V tomto formuláři jsou všechny požadavky na zboží, které jsou pro danou servisní zakázku vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="8b95b-120">This form lists the item requirements that are created on the service order.</span></span>

3.  <span data-ttu-id="8b95b-121">Vyberte řádek požadavku na zboží, který má být odebrán, a klepněte na možnost **Odstranit** .</span><span class="sxs-lookup"><span data-stu-id="8b95b-121">Select the item requirement to delete, and then click **Delete** .</span></span>

<span data-ttu-id="8b95b-122">- nebo -</span><span class="sxs-lookup"><span data-stu-id="8b95b-122">–or–</span></span>

1.  <span data-ttu-id="8b95b-123">Klikněte na **Řízení a účetnictví projektů** \> **Společné** \> **Projekty** \> **Všechny projekty** .</span><span class="sxs-lookup"><span data-stu-id="8b95b-123">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects** .</span></span>

2.  <span data-ttu-id="8b95b-124">Otevřete projekt se servisní zakázkou, v níž je vytvořen požadavek na zboží.</span><span class="sxs-lookup"><span data-stu-id="8b95b-124">Open the project that has the service order in which an item requirement is created.</span></span>

3.  <span data-ttu-id="8b95b-125">Ve formuláři **Projekty** , v pravém podokně, klikněte na možnost **požadavky položky** .</span><span class="sxs-lookup"><span data-stu-id="8b95b-125">In the **Projects** form, in the right pane, click **Item requirements** .</span></span> <span data-ttu-id="8b95b-126">Zobrazí se formulář **Požadavky položky** se seznamem požadavků na položky asociovanými s vybraným projektem.</span><span class="sxs-lookup"><span data-stu-id="8b95b-126">The **Item requirements** form lists the item requirements that are associated with the selected project.</span></span>

4.  <span data-ttu-id="8b95b-127">Vyberte řádek požadavku na zboží, který má být odebrán, a klepněte na možnost **Odstranit** .</span><span class="sxs-lookup"><span data-stu-id="8b95b-127">Select the item requirement to delete, and then click **Delete** .</span></span>

## <a name="see-also"></a><span data-ttu-id="8b95b-128">Viz také</span><span class="sxs-lookup"><span data-stu-id="8b95b-128">See also</span></span>

<span data-ttu-id="8b95b-129">[Požadavky položky (formulář)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="8b95b-129">[Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span></span>

