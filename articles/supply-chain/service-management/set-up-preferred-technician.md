---
title: Nastavení upřednostňovaného technika
description: Můžete vybrat libovolného pracovníka jako upřednostňovaného technika pro servisní zakázky nebo servisní smlouvy.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 850d91372fb1a918840ebc316a4479f4a70bdc24
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423491"
---
# <a name="set-up-a-preferred-technician"></a><span data-ttu-id="5f3f9-103">Nastavení upřednostňovaného technika</span><span class="sxs-lookup"><span data-stu-id="5f3f9-103">Set up a preferred technician</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="5f3f9-104">Můžete vybrat libovolného pracovníka jako upřednostňovaného technika pro servisní zakázky nebo servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-104">You can select any worker as a preferred technician for a service agreement or service order.</span></span> <span data-ttu-id="5f3f9-105">Je však vhodné přidat pracovníka do příslušnému týmu pro zasílání, aby pracovník byl k dispozici na **expediční vývěsce**.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-105">However, it is a good idea to add the worker to the appropriate dispatch team so that the worker is included on the **Dispatch board**.</span></span>

## <a name="assign-employee-to-a-dispatch-team"></a><span data-ttu-id="5f3f9-106">Přiřazení zaměstnance do expedičního týmu</span><span class="sxs-lookup"><span data-stu-id="5f3f9-106">Assign employee to a dispatch team</span></span>

1.  <span data-ttu-id="5f3f9-107">Klikněte na **Lidské zdroje** \> **Společné** \> **Pracovníci** \> **Pracovníci**.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-107">Click **Human resources** \> **Common** \> **Workers** \> **Workers**.</span></span> <span data-ttu-id="5f3f9-108">Otevřete stránku podrobností pracovníka dvojitým klepnutím na jeho jméno.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-108">Double-click a worker to open the worker details page.</span></span> <span data-ttu-id="5f3f9-109">V **podokně akcí** klepněte na tlačítko **nastavení** \>**expediční tým** k otevření formuláře **expedice pracovníků**.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-109">On the **Action Pane**, click **Setup** \>**Dispatch team** to open the **Dispatch workers** form.</span></span>

2.  <span data-ttu-id="5f3f9-110">V poli **Expediční tým** vyberte tým, kterému chcete pracovníka přiřadit.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-110">In the **Dispatch team** field, select the team to assign the worker to.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a><span data-ttu-id="5f3f9-111">Přiřazení upřednostňovaného technika k servisní smlouvě</span><span class="sxs-lookup"><span data-stu-id="5f3f9-111">Assign a preferred technician to a service agreement</span></span>

1.  <span data-ttu-id="5f3f9-112">Klikněte na **Správa servisu** \> **Obecné** \> **Servisní smlouvy** \> **Servisní smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-112">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="5f3f9-113">Poklepáním na servisní smlouvu otevřete formulář Podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-113">Double-click a service agreement to open the details form.</span></span>

2.  <span data-ttu-id="5f3f9-114">Na kartě **Obecné** vyberte pole **Preferovaný technik** a přiřaďte odpovídajícího člena expedičního týmu jako upřednostňovaného technika pro servisní smlouvu.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-114">On the **General** tab, select the **Preferred technician** field, and then select a member of the appropriate dispatch team as the preferred technician for the service agreement.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-order"></a><span data-ttu-id="5f3f9-115">Přiřazení upřednostňovaného technika k servisní zakázce</span><span class="sxs-lookup"><span data-stu-id="5f3f9-115">Assign a preferred technician to a service order</span></span>

1.  <span data-ttu-id="5f3f9-116">Klikněte na **Řízení služeb** \> **Periodické** \> **Expediční vývěska**.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-116">Click **Service management** \> **Periodic** \> **Dispatch board**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="5f3f9-117">Ve formuláři <STRONG>Expediční vývěska</STRONG> zadejte rozsah dat pro expediční aktivity, které chcete zobrazit.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-117">In the <STRONG>Dispatch board</STRONG> form, specify a date range for dispatch activities to view.</span></span> <span data-ttu-id="5f3f9-118">Uveďte také, zda chcete zobrazit zavřené aktivity a zda chcete omezit seznam expedičních aktivity na týmy, které patří ke sledování nebo jsou pro sledování autorizovány.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-118">Also, specify whether to display closed activities and whether to limit the dispatch activity list to teams that you belong to or are authorized to monitor.</span></span> <span data-ttu-id="5f3f9-119">Klepnutím na tlačítko <STRONG>OK</STRONG> otevřete formulář <STRONG>Expediční vývěska</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-119">Click <STRONG>OK</STRONG> to open the <STRONG>Dispatch board</STRONG>.</span></span></P>



2.  <span data-ttu-id="5f3f9-120">Vyberte řádek servisní aktivity, kterou chcete upravit.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-120">Select the line of the service activity to modify.</span></span>

3.  <span data-ttu-id="5f3f9-121">Na kartě **Související** použijte seznam **Pracovník** a přiřaďte člena odpovídajícího expedičního týmu jako upřednostňovaného technika pro volání servisu.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-121">On the **Related** tab, use the **Worker** list to assign a member of the appropriate dispatch team as the preferred technician for the service call.</span></span>

## <a name="see-also"></a><span data-ttu-id="5f3f9-122">Viz také</span><span class="sxs-lookup"><span data-stu-id="5f3f9-122">See also</span></span>

[<span data-ttu-id="5f3f9-123">Přehled přípravy a zřízení servisních smluv</span><span class="sxs-lookup"><span data-stu-id="5f3f9-123">Develop and establish service agreements overview</span></span>](service-agreements.md)

[<span data-ttu-id="5f3f9-124">Ruční vytvoření servisních objednávek</span><span class="sxs-lookup"><span data-stu-id="5f3f9-124">Create service orders manually</span></span>](create-service-orders-manually.md)

<span data-ttu-id="5f3f9-125">[Servisní smlouvy (formulář)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="5f3f9-125">[Service agreements (form)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))</span></span>
  


