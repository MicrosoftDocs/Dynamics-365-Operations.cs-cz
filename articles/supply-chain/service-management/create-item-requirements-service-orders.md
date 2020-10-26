---
title: Vytvoření požadavků položky pro servisní zakázky
description: Pokud pro objednávku služeb potřebujete rezervovat konkrétní zboží, můžete vytvořit požadavky na skladovou položku.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 18484b637723cef43cad288c08ddfe53cddf9e03
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978476"
---
# <a name="create-item-requirements-for-service-orders"></a><span data-ttu-id="6b494-103">Vytvoření požadavků položky pro servisní zakázky</span><span class="sxs-lookup"><span data-stu-id="6b494-103">Create item requirements for service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6b494-104">Můžete vytvářet objednávky služeb ke sledování a řízení služeb, které poskytujete odběratelům.</span><span class="sxs-lookup"><span data-stu-id="6b494-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="6b494-105">Pokud pro objednávku služeb potřebujete rezervovat konkrétní zboží, můžete vytvořit požadavky na skladovou položku.</span><span class="sxs-lookup"><span data-stu-id="6b494-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="6b494-106">Požadavek na položku může být okamžitě spotřebován ze skladu nebo může spustit výrobní zakázku zboží.</span><span class="sxs-lookup"><span data-stu-id="6b494-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="6b494-107">Použitím požadavků zboží namísto transakcí zboží můžete naplánovat dodávku těsně před vlastním použitím zboží, vytvořit prodejní objednávku, zahrnout zboží do rámce obchodní smlouvy nebo zahrnout požadavek na zboží do provozního plánování.</span><span class="sxs-lookup"><span data-stu-id="6b494-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="6b494-108">Požadavky zboží pro objednávky služeb jsou zpracovávány prostřednictvím projektu.</span><span class="sxs-lookup"><span data-stu-id="6b494-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="6b494-109">Chcete-li vytvořit pro objednávku služeb požadavek zboží, objednávka musí být přiřazena k projektu.</span><span class="sxs-lookup"><span data-stu-id="6b494-109">To create an item requirement on a service order, the service order must be assigned to a project.</span></span> <span data-ttu-id="6b494-110">Po vytvoření požadavku na položku pro servisní zakázku můžete zobrazit požadavek na položku ve formuláři **Projekty** pro vybraný projekt.</span><span class="sxs-lookup"><span data-stu-id="6b494-110">After you create an item requirement for a service order, you can view the item requirement in the **Projects** form for the selected project.</span></span>

## <a name="create-an-item-requirement-for-a-service-order"></a><span data-ttu-id="6b494-111">Vytvoření požadavku položky pro servisní zakázku</span><span class="sxs-lookup"><span data-stu-id="6b494-111">Create an item requirement for a service order</span></span>

1.  <span data-ttu-id="6b494-112">Klikněte na uzel **Řízení služeb** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky** .</span><span class="sxs-lookup"><span data-stu-id="6b494-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders** .</span></span>

2.  <span data-ttu-id="6b494-113">Vyberte servisní zakázku, pro kterou chcete vytvořit požadavek na položky.</span><span class="sxs-lookup"><span data-stu-id="6b494-113">Select the service order that you want to create an item requirement for.</span></span>

3.  <span data-ttu-id="6b494-114">V **podokně akcí** na kartě **Expedice** klikněte na **Požadavek na položku** .</span><span class="sxs-lookup"><span data-stu-id="6b494-114">On the **Action Pane** , on the **Dispatch** tab, click **Item requirement** .</span></span>

4.  <span data-ttu-id="6b494-115">Ve formuláři **Požadavky na položku** zadejte informace pro požadovanou položku.</span><span class="sxs-lookup"><span data-stu-id="6b494-115">In the **Item requirements** form, enter information for the required item.</span></span> <span data-ttu-id="6b494-116">Další informace o daných polích ve formuláři lze najít v tématu [Požadavky na položku (formulář)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="6b494-116">For more information about the specific fields, see [Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).</span></span>

## <a name="create-an-item-requirement-for-a-service-agreement"></a><span data-ttu-id="6b494-117">Vytvoření požadavku položky pro servisní smlouvu</span><span class="sxs-lookup"><span data-stu-id="6b494-117">Create an item requirement for a service agreement</span></span>

1.  <span data-ttu-id="6b494-118">Klikněte na **Správa servisu** \> **Obecné** \> **Servisní smlouvy** \> **Servisní smlouvy** .</span><span class="sxs-lookup"><span data-stu-id="6b494-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements** .</span></span>

2.  <span data-ttu-id="6b494-119">Otevřete servisní smlouvu, pro kterou chcete vytvořit požadavek na položky.</span><span class="sxs-lookup"><span data-stu-id="6b494-119">Open the service agreement for which you want to create an item requirement.</span></span>

3.  <span data-ttu-id="6b494-120">Na pevné záložce **Řádky** kliknutím na tlačítko **Přidat** vytvořte nový řádek.</span><span class="sxs-lookup"><span data-stu-id="6b494-120">On the **Lines** FastTab, click **Add** to create a new line.</span></span>

4.  <span data-ttu-id="6b494-121">V poli **Typ transakce** vyberte **Položka** .</span><span class="sxs-lookup"><span data-stu-id="6b494-121">In the **Transaction type** field, select **Item** .</span></span>

5.  <span data-ttu-id="6b494-122">V poli **Nastavení položky** vyberte **Požadavek na položku** .</span><span class="sxs-lookup"><span data-stu-id="6b494-122">In the **Item setup** field, select **Item requirement** .</span></span>

6.  <span data-ttu-id="6b494-123">V poli **Číslo položky** vyberte položku, která je vyžadována pro servisní smlouvu.</span><span class="sxs-lookup"><span data-stu-id="6b494-123">In the **Item number** field, select the item that is required for the service agreement.</span></span>

7.  <span data-ttu-id="6b494-124">Na pevné záložce **podrobnosti řádku** na kartě **dimenze produktu** v poli **pracoviště** vyberte skladové pracoviště pro položku.</span><span class="sxs-lookup"><span data-stu-id="6b494-124">On the **Line details** FastTab, on the **Product dimensions** tab, in the **Site** field, select the inventory site for the item.</span></span>

8.  <span data-ttu-id="6b494-125">Chcete-li vytvořit servisní zakázku z řádku smlouvy, na pevné záložce **Řádky** klepněte na možnost **Vytvořit servisní příkazy** a poté zadejte relevantní informace do formuláře **Vytvořit servisní příkazy** .</span><span class="sxs-lookup"><span data-stu-id="6b494-125">To create a service order from the agreement line, on the **Lines** FastTab, click **Create service orders** , and then enter the relevant information in the **Create service orders** form.</span></span> 


## <a name="see-also"></a><span data-ttu-id="6b494-126">Viz také</span><span class="sxs-lookup"><span data-stu-id="6b494-126">See also</span></span>

<span data-ttu-id="6b494-127">[Automatické vytvoření servisních zakázek](create-service-orders-automatically.md)</span><span class="sxs-lookup"><span data-stu-id="6b494-127">[Create service orders automatically](create-service-orders-automatically.md).</span></span>

  


