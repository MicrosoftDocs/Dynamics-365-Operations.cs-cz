---
title: Naplánované práce údržby pracovního příkazu
description: Toto téma vysvětluje naplánované práce údržby pracovního příkazu v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4b3cc32d6ff263967c1ee843702c28968219ac33
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887175"
---
# <a name="scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="a40f8-103">Naplánované práce údržby pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="a40f8-103">Scheduled work order maintenance jobs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="a40f8-104">Stránka **Naplánované práce údržby pracovního příkazu** slouží k získání přehledu o pracovních příkazech přidělených zdroji.</span><span class="sxs-lookup"><span data-stu-id="a40f8-104">The **Scheduled work order maintenance jobs** page is used to get an overview of the work orders allocated to a resource.</span></span> <span data-ttu-id="a40f8-105">Pracovní příkazy používající typy prostředků "Lidské zdroje", "Nástroj" a "Stroj" jsou zobrazeny v seznamu.</span><span class="sxs-lookup"><span data-stu-id="a40f8-105">Work orders using resource types "Human resources", "Tool", and "Machine" are shown in the list.</span></span> <span data-ttu-id="a40f8-106">Seznam lze použít k získání přehledu o pracovních příkazech přidělených konkrétnímu zdroji.</span><span class="sxs-lookup"><span data-stu-id="a40f8-106">The list can be used to get an overview of work orders allocated to a specific resource.</span></span> <span data-ttu-id="a40f8-107">Lze jej také použít k rychlému vyhledání pracovních příkazů přidělených pracovníkovi údržby, který dnes ráno onemocní, a poté rychle přidělit práci jinému pracovníkovi údržby.</span><span class="sxs-lookup"><span data-stu-id="a40f8-107">You can also use it to quickly find a work order allocated to a maintenance worker who, for example, called in sick this morning, and then quickly allocate another maintenance worker to the job.</span></span>

## <a name="view-scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="a40f8-108">Zobrazit naplánované práce údržby pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="a40f8-108">View scheduled work order maintenance jobs</span></span>

1. <span data-ttu-id="a40f8-109">Kliknete na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Naplánované práce údržby pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="a40f8-109">Click **Asset management** > **Common** > **Work orders** > **Scheduled work order maintenance jobs**.</span></span> <span data-ttu-id="a40f8-110">Zobrazí se seznam všech pracovních příkazů nastavených na stav životního cyklu pracovního příkazu "Plánováno" nebo "Probíhá".</span><span class="sxs-lookup"><span data-stu-id="a40f8-110">You see a list of all work orders set to work order lifecycle state "Scheduled" or "In progress".</span></span>

2. <span data-ttu-id="a40f8-111">Seznam lze například seřadit podle pracovníka údržby.</span><span class="sxs-lookup"><span data-stu-id="a40f8-111">You can sort the list, for example, by maintenance worker.</span></span> <span data-ttu-id="a40f8-112">Pomocí filtru můžete také omezit seznam tak, aby zobrazoval pracovní příkazy přidělené konkrétnímu zdroji nebo pracovníkovi údržby.</span><span class="sxs-lookup"><span data-stu-id="a40f8-112">You can also use the filter to limit the list to display work orders allocated to a specific resource or maintenance worker.</span></span>

3. <span data-ttu-id="a40f8-113">Na pracovním příkazu můžete zobrazit poznámky a v případě potřeby přidat nové poznámky výběrem úlohy pracovního příkazu v seznamu a kliknutím na položku **Poznámky**.</span><span class="sxs-lookup"><span data-stu-id="a40f8-113">You can see notes on the work order and, if required, add new notes by selecting the work order job in the list and clicking **Notes**.</span></span>

4. <span data-ttu-id="a40f8-114">Chcete-li přidělit jednoho pracovníka údržby na pracovní příkaz, vyberte pracovní příkaz v seznamu a klikněte na možnost **Pracovní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="a40f8-114">If you want to allocate one maintenance worker to a work order, select the work order in the list, and click **Work order**.</span></span>

5. <span data-ttu-id="a40f8-115">Otevře se stránka **Pracovní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="a40f8-115">The **Work order** page opens.</span></span> <span data-ttu-id="a40f8-116">Kliknutím na položku **Vypravit** naplánujte pracovní příkaz konkrétnímu pracovníkovi údržby.</span><span class="sxs-lookup"><span data-stu-id="a40f8-116">Click **Dispatch** to schedule the work order to a specific maintenance worker.</span></span>

>[!NOTE]
><span data-ttu-id="a40f8-117">Další informace o plánování několika pracovních příkazů nebo jednoho pracovního příkazu v [Plánování pracovních příkazů](../work-order-scheduling/schedule-work-orders.md) a [Vypravování pracovního příkazu](../work-order-scheduling/dispatch-work-order.md).</span><span class="sxs-lookup"><span data-stu-id="a40f8-117">Read more about scheduling several work orders or one work order in [Schedule work orders](../work-order-scheduling/schedule-work-orders.md) and [Dispatch work order](../work-order-scheduling/dispatch-work-order.md).</span></span>

<span data-ttu-id="a40f8-118">Na následujícím obrázku je uveden příklad stránky **Naplánované práce údržby pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="a40f8-118">The figure below shows an example of the **Scheduled work order maintenance jobs** page.</span></span>

![Obrázek č. 1](media/07-work-order-scheduling.png)

