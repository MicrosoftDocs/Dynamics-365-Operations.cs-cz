---
title: Naplánování pracovního příkazu na konkrétní datum a čas
description: Toto téma vysvětluje, jak naplánovat pracovní příkaz k určitému datu a času v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e81ea13a3463965c6e4785dac32f536d2e94a7ba
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215256"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a><span data-ttu-id="0e452-103">Naplánování pracovního příkazu na konkrétní datum a čas</span><span class="sxs-lookup"><span data-stu-id="0e452-103">Schedule work order on specific date and time</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="0e452-104">Je-li nutné naplánovat pracovní příkaz k určitému datu *a* času, můžete přepsat standardní proces plánování v modulu Správa majetku a vytvořit specifický plán pro pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="0e452-104">If a work order must be scheduled on a specific date *and* time, you can override the standard scheduling process in Asset Management and create a specific schedule for a work order.</span></span>

1. <span data-ttu-id="0e452-105">Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="0e452-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="0e452-106">V seznamu pracovních příkazů klikněte na ID pracovního příkazu ve sloupci **Pracovní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="0e452-106">In the work order list, click on the Work order ID in the **Work order** column.</span></span>

3. <span data-ttu-id="0e452-107">Klikněte na možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="0e452-107">Click **Edit**.</span></span>

4. <span data-ttu-id="0e452-108">Na pevné záložce **Záhlaví pracovního příkazu** vložte počáteční a koncové datum a čas do polí **Očekávaný začátek** a **Očekávaný konec**.</span><span class="sxs-lookup"><span data-stu-id="0e452-108">On the **Work order header** FastTab, insert start and end dates and times in the **Expected start** and **Expected end** fields.</span></span>

    ![Obrázek č. 1](media/05-work-order-scheduling.png)

5. <span data-ttu-id="0e452-110">Na kartě **Obecné** klikněte na možnost **Naplánovat** pro použití standardního procesu plánování, nebo klikněte na **Vypravit**, chcete-li přiřadit pracovní příkaz pro určitého pracovníka.</span><span class="sxs-lookup"><span data-stu-id="0e452-110">On the **General** tab, click **Schedule** to use the standard scheduling process, or click **Dispatch** if you want to assign the work order to a specific worker.</span></span>

6. <span data-ttu-id="0e452-111">Chcete-li přepsat všechny stávající rezervace kapacit, aby se zajistilo, že je v očekávaném období naplánována pracovní objednávka, proveďte výběr podle následujícího obrázku v dialogovém okně **Naplánovat pracovní příkaz** > sekce **Omezená kapacita**.</span><span class="sxs-lookup"><span data-stu-id="0e452-111">In order to override any existing capacity reservations to ensure that the work order is scheduled in the expected period, make the selections as shown in the figure below in the **Schedule work order** dialog > **Finite capacity** section.</span></span> <span data-ttu-id="0e452-112">To znamená, že proces plánování bude ignorovat existující rezervace kapacity, protože pracovní příkaz musí začínat očekávaným počátečním časem.</span><span class="sxs-lookup"><span data-stu-id="0e452-112">This means that the scheduling process will ignore existing capacity reservations because the work order must start on the expected start time.</span></span>

    ![Obrázek č. 2](media/06-work-order-scheduling.png)

7. <span data-ttu-id="0e452-114">Plánování zahájíte kliknutím na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e452-114">Click **OK** to start scheduling.</span></span>

8. <span data-ttu-id="0e452-115">Je-li výsledkem procesu plánování dvojitá rezervace, zobrazí se na obrazovce zpráva a můžete upravit související pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="0e452-115">If the scheduling process results in double bookings, you will see a message on the screen, and you can adjust the related work orders.</span></span>

>[!NOTE]
><span data-ttu-id="0e452-116">Chcete-li naplánovat pracovníka údržby pro daný pracovní příkaz, musí být pracovník údržby k dispozici v očekávaném počátečním datu a čase.</span><span class="sxs-lookup"><span data-stu-id="0e452-116">In order to schedule a maintenance worker for the work order, that maintenance worker must be available at the expected start date and time.</span></span> <span data-ttu-id="0e452-117">Dostupnost pracovníka je nastavena v [kalendáři pracovníka](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md).</span><span class="sxs-lookup"><span data-stu-id="0e452-117">Worker availability is set up in the [worker calendar](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md).</span></span> 

