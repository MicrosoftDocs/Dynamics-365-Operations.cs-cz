---
title: Přidání adresy do servisní zakázky
description: Toto téma popisuje postup přidání adresy odběratele do servisní zakázky.
author: ShylaThompson
manager: tfehr
ms.date: 05/02/2018
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
ms.openlocfilehash: 41497eacae8bcc0e57df8062f7f318a39c2b4909
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423996"
---
# <a name="add-an-address-to-a-service-order"></a><span data-ttu-id="98394-103">Přidání adresy do servisní zakázky</span><span class="sxs-lookup"><span data-stu-id="98394-103">Add an address to a service order</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="98394-104">Toto téma popisuje postup přidání adresy odběratele do servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="98394-104">This topic describes how to add a customer address to a service order.</span></span> <span data-ttu-id="98394-105">Při vytváření servisní zakázky se informace o adrese přenáší z projektu, ke kterému je servisní zakázka připojena.</span><span class="sxs-lookup"><span data-stu-id="98394-105">When you create a service order, the address information is transferred from the project that the service order is attached to.</span></span> <span data-ttu-id="98394-106">Pro odběratele, dodavatele, pracoviště, sklady, servisní zakázky a projekty však můžete vybrat alternativní umístění z adres, které jsou již zadány v aplikaci Microsoft Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="98394-106">However, you can select an alternative location from addresses that are already entered in Microsoft Dynamics AX for customers, vendors, sites, warehouses, service orders, and projects.</span></span>

<span data-ttu-id="98394-107">Můžete také vytvořit adresy nové.</span><span class="sxs-lookup"><span data-stu-id="98394-107">You can also create a new address.</span></span> <span data-ttu-id="98394-108">Ve výchozím stavu je nová adresa převedena do projektu.</span><span class="sxs-lookup"><span data-stu-id="98394-108">By default, the new address is transferred to the project.</span></span> <span data-ttu-id="98394-109">Můžete však zadat, aby nová adresa byla relevantní pouze pro tuto instanci služby.</span><span class="sxs-lookup"><span data-stu-id="98394-109">However, you can specify that the new address is only relevant for this instance of the service.</span></span> <span data-ttu-id="98394-110">V takovém případě nová adresa do projektu převedena nebude.</span><span class="sxs-lookup"><span data-stu-id="98394-110">If you do, the new address is not transferred to the project.</span></span>

## <a name="create-a-customer-address-for-a-service-order"></a><span data-ttu-id="98394-111">Vytvoření adresy zákazníka pro servisní zakázku</span><span class="sxs-lookup"><span data-stu-id="98394-111">Create a customer address for a service order</span></span>

<span data-ttu-id="98394-112">Pro přidání adresy do servisní zakázky postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="98394-112">To add an address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="98394-113">Klikněte na uzel **Řízení služeb** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="98394-113">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="98394-114">Otevřete servisní zakázku, pro kterou chcete vytvořit adresu.</span><span class="sxs-lookup"><span data-stu-id="98394-114">Open the service order that you want to create an address for.</span></span>

3.  <span data-ttu-id="98394-115">V **podokně akcí** klepněte na tlačítko **Upravit** a klepněte na možnost **Zobrazení záhlaví**.</span><span class="sxs-lookup"><span data-stu-id="98394-115">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="98394-116">Na pevné záložce **adresy** klepněte na tlačítko **přidání adresy**.</span><span class="sxs-lookup"><span data-stu-id="98394-116">On the **Address** FastTab, click **Add address**.</span></span>

5.  <span data-ttu-id="98394-117">Ve formuláři **Nová adresa** zadejte jedinečný název adresy a vyplňte zbývající pole.</span><span class="sxs-lookup"><span data-stu-id="98394-117">In the **New address** form, enter a unique name for the address and complete the remaining fields.</span></span> 
    

    > [!WARNING]
    > <P><span data-ttu-id="98394-118">Zadáte-li stejný název, jaký používá existující adresa, informace zadané do zbývajících polí přepíší informace pro existující adresu.</span><span class="sxs-lookup"><span data-stu-id="98394-118">If you enter the same name as an existing address, the information that you enter in the remaining fields will overwrite information for the existing address.</span></span></P>


6.  <span data-ttu-id="98394-119">Klepnutím na tlačítko **OK** zkopírujete novou adresu do servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="98394-119">Click **OK** to copy the new address to your service order.</span></span>

## <a name="specify-an-alternative-address-on-a-service-order"></a><span data-ttu-id="98394-120">Zadání alternativní adresy pro servisní zakázku</span><span class="sxs-lookup"><span data-stu-id="98394-120">Specify an alternative address on a service order</span></span>

<span data-ttu-id="98394-121">Pro přidání alternativní adresy do servisní zakázky postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="98394-121">To add an alternative address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="98394-122">Klikněte na uzel **Řízení služeb** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="98394-122">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="98394-123">Otevřete servisní zakázku, pro kterou chcete zadat alternativní adresu.</span><span class="sxs-lookup"><span data-stu-id="98394-123">Open the service order that you want to enter an alternative address for.</span></span>

3.  <span data-ttu-id="98394-124">V **podokně akcí** klepněte na tlačítko **Upravit** a klepněte na možnost **Zobrazení záhlaví**.</span><span class="sxs-lookup"><span data-stu-id="98394-124">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="98394-125">Na pevné záložce **adresy** klepněte na tlačítko **Jiná adresa**.</span><span class="sxs-lookup"><span data-stu-id="98394-125">On the **Address** FastTab, click **Other address**.</span></span>

5.  <span data-ttu-id="98394-126">Ve formuláři **výběr adresy** v poli **typ záznamu** vyberte **servisní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="98394-126">In the **Address selection** form, in the **Record type** field, select **Service orders**.</span></span>

6.  <span data-ttu-id="98394-127">Vyberte adresu a klepnutím na tlačítko **OK** ji zkopírujete do servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="98394-127">Select an address, and then click **OK** to copy it to your service order.</span></span>


  


