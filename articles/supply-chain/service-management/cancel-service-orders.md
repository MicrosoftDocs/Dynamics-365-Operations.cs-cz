---
title: Zrušit servisní zakázky
description: Servisní zakázku nebo řádek servisní zakázky můžete zrušit z dané servisní zakázky, více servisních zakázek můžete zrušit spuštěním periodické úlohy.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a253a9c9ae4d7c34403db9bb5f3d63bc77e11101
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259667"
---
# <a name="cancel-service-orders"></a><span data-ttu-id="fa6ab-103">Zrušit servisní zakázky</span><span class="sxs-lookup"><span data-stu-id="fa6ab-103">Cancel service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="fa6ab-104">Servisní zakázku nebo řádek servisní zakázky můžete zrušit z dané servisní zakázky, více servisních zakázek můžete zrušit spuštěním periodické úlohy.</span><span class="sxs-lookup"><span data-stu-id="fa6ab-104">You can cancel a service order or service order line from the service order itself, or you can cancel multiple service orders by running a periodic job.</span></span>


> [!NOTE]
> <P><span data-ttu-id="fa6ab-105">Servisní zakázky nelze zrušit v případě, že fáze servisní zakázky neumožňuje zrušení, pokud servisní zakázka obsahuje požadavky na položky nebo pokud již byla servisní zakázka zaúčtována.</span><span class="sxs-lookup"><span data-stu-id="fa6ab-105">Service orders cannot be canceled if the stage of the service order does not allow cancelation, if the service order has item requirements, or if the service order has already been posted.</span></span></P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a><span data-ttu-id="fa6ab-106">Zrušení servisní zakázky ve formuláři Servisní zakázky</span><span class="sxs-lookup"><span data-stu-id="fa6ab-106">Cancel a service order in the Service orders form</span></span>

1.  <span data-ttu-id="fa6ab-107">Klikněte na uzel **Řízení služeb** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="fa6ab-107">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="fa6ab-108">Vyberte webovou servisní zakázku a v podokně akcí klikněte na **Zrušit objednávku**.</span><span class="sxs-lookup"><span data-stu-id="fa6ab-108">Select the service order, and on the Action Pane, click **Cancel order**.</span></span>

## <a name="cancel-a-service-order-line"></a><span data-ttu-id="fa6ab-109">Zrušení řádku servisní zakázky</span><span class="sxs-lookup"><span data-stu-id="fa6ab-109">Cancel a service order line</span></span>

1.  <span data-ttu-id="fa6ab-110">Klikněte na uzel **Řízení služeb** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="fa6ab-110">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="fa6ab-111">V dolním podokně dvakrát klikněte na řádek servisní zakázky, který chcete zrušit.</span><span class="sxs-lookup"><span data-stu-id="fa6ab-111">Double-click the service order that contains the line you want to cancel.</span></span>

2.  <span data-ttu-id="fa6ab-112">Vyberte řádek servisní zakázky, kterou chcete zrušit, a klepněte na tlačítko **Zrušit řádek objednávky** ke změně stavu řádku na **zrušeno**.</span><span class="sxs-lookup"><span data-stu-id="fa6ab-112">Select the service order line that you want to cancel, and then click **Cancel order line** to change the status of the line to **Canceled**.</span></span>


> [!TIP]
> <P><span data-ttu-id="fa6ab-113">Chcete-li odvolat zrušení řádku servisní zakázky a změnit stav zpět na <STRONG>vytvořeno</STRONG>, klepněte na tlačítko <STRONG>odvolat zrušení</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="fa6ab-113">To reverse the cancellation of a service order line and change the status back to <STRONG>Created</STRONG>, click <STRONG>Revoke cancel</STRONG>.</span></span></P>


## <a name="cancel-multiple-service-orders"></a><span data-ttu-id="fa6ab-114">Zrušení více servisních zakázek</span><span class="sxs-lookup"><span data-stu-id="fa6ab-114">Cancel multiple service orders</span></span>

1.  <span data-ttu-id="fa6ab-115">Klepněte na tlačítko **řízení servisu** \> **Periodicky** \> **servisní zakázky** \> **Zrušit servisní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="fa6ab-115">Click **Service management** \> **Periodic** \> **Service orders** \> **Cancel service orders**.</span></span>

2.  <span data-ttu-id="fa6ab-116">Klikněte na tlačítko **Vybrat**.</span><span class="sxs-lookup"><span data-stu-id="fa6ab-116">Click the **Select** button.</span></span>

3.  <span data-ttu-id="fa6ab-117">Ve formuláři **Dotaz** ve sloupci **Kritéria** vyberte servisní zakázky, které chcete zrušit.</span><span class="sxs-lookup"><span data-stu-id="fa6ab-117">In the **Inquiry** form, in the **Criteria** column, select the service orders that you want to cancel.</span></span>

4.  <span data-ttu-id="fa6ab-118">Klepnutím na tlačítko **OK** zavřete formulář **Dotaz**.</span><span class="sxs-lookup"><span data-stu-id="fa6ab-118">Click **OK** to close the **Inquiry** form.</span></span>

5.  <span data-ttu-id="fa6ab-119">Jestliže chcete generovat informační protokol, který zobrazí zrušené servisní zakázky, zaškrtněte políčko **Zobrazit informační protokol**.</span><span class="sxs-lookup"><span data-stu-id="fa6ab-119">Select the **Show Infolog** check box to generate an Infolog that lists the canceled service orders.</span></span>

6.  <span data-ttu-id="fa6ab-120">Chcete-li odvolat stav **Zrušené** servisní zakázky, zaškrtněte políčko **Odvolat storno**.</span><span class="sxs-lookup"><span data-stu-id="fa6ab-120">Select the **Revoke cancel** check box if you want to reverse the **Canceled** status of a service order.</span></span>

7.  <span data-ttu-id="fa6ab-121">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="fa6ab-121">Click **OK**.</span></span>

<span data-ttu-id="fa6ab-122">Vybrané servisní zakázky budou buď zrušeny, nebo bude jejich stav **Zrušeno** odvolán na stav **Zpracovává se**.</span><span class="sxs-lookup"><span data-stu-id="fa6ab-122">The selected service orders are either canceled or their progress status of **Canceled** has been reversed to **In process**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="fa6ab-123">Pokud zaškrtnete políčko <STRONG>Odvolat zrušení</STRONG>, servisní zakázky se stavem <STRONG>Zrušeno</STRONG> budou vráceny zpět a stav <STRONG>Zpracovává se</STRONG> nebude zrušen.</span><span class="sxs-lookup"><span data-stu-id="fa6ab-123">If you select the <STRONG>Revoke cancel</STRONG> check box, service orders with a progress status of <STRONG>Canceled</STRONG> are reversed and service orders with a progress status of <STRONG>In process</STRONG> are not canceled.</span></span></P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]