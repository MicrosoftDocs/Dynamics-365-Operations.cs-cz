---
title: Vytvoření pracovních příkazů
description: Toto téma vysvětluje, jak vytvořit pracovní příkazy v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
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
ms.openlocfilehash: f94f8bc20753e38ce1cb6eccdfbc85c2e491ffad
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423853"
---
# <a name="creating-work-orders"></a><span data-ttu-id="c9c9e-103">Vytvoření pracovních příkazů</span><span class="sxs-lookup"><span data-stu-id="c9c9e-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c9c9e-104">Když jste naplánovali preventivní práce údržby můžete v dalším kroku pro práce vytvořit pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="c9c9e-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="c9c9e-105">To je možné provést v jednom z rozvrhů údržby.</span><span class="sxs-lookup"><span data-stu-id="c9c9e-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="c9c9e-106">Naplánované práce v rozvrhu údržby mohou mít různé typy odkazů:</span><span class="sxs-lookup"><span data-stu-id="c9c9e-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="c9c9e-107">Typ odkazu</span><span class="sxs-lookup"><span data-stu-id="c9c9e-107">Reference type</span></span> | <span data-ttu-id="c9c9e-108">Popis</span><span class="sxs-lookup"><span data-stu-id="c9c9e-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9c9e-109">Plány údržby</span><span class="sxs-lookup"><span data-stu-id="c9c9e-109">Maintenance plans</span></span>     | <span data-ttu-id="c9c9e-110">Práce preventivní údržby na základě typů plánu údržby Čas nebo Počítadlo.</span><span class="sxs-lookup"><span data-stu-id="c9c9e-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="c9c9e-111">Pořadí údržby</span><span class="sxs-lookup"><span data-stu-id="c9c9e-111">Maintenance rounds</span></span>    | <span data-ttu-id="c9c9e-112">Práce preventivní údržby obsahující několik majetků, které vyžadují podobný typ údržby.</span><span class="sxs-lookup"><span data-stu-id="c9c9e-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="c9c9e-113">Požadavek na údržbu</span><span class="sxs-lookup"><span data-stu-id="c9c9e-113">Maintenance request</span></span>   | <span data-ttu-id="c9c9e-114">Ručně vytvořený požadavek na údržbu nebo opravu majetku, který lze převést na pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="c9c9e-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="c9c9e-115">Klikněte na **Správa majetku** > **Společné** > **Všechny rozvrhy údržby** nebo **Otevřené řádky rozvrhu údržby** nebo **Otevřené fondy rozvrhu údržby**.</span><span class="sxs-lookup"><span data-stu-id="c9c9e-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="c9c9e-116">Vyberte naplánované práce údržby, pro které chcete vytvořit pracovní příkaz, a klikněte na **Pracovní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="c9c9e-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="c9c9e-117">V dialogovém okně **Vytvořit pracovní příkazy**, v poli **Hodiny prognózy údržby** se zobrazí celkový počet hodin prognózy pro vybrané řádky.</span><span class="sxs-lookup"><span data-stu-id="c9c9e-117">In the **Create work orders** dialog, the total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="c9c9e-118">V oddílu **Parametry** vyberte, kolik pracovních příkazů se má vytvořit.</span><span class="sxs-lookup"><span data-stu-id="c9c9e-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="c9c9e-119">Pro každý řádek rozvrhu údržby můžete vytvořit jeden pracovní příkaz, nebo několik pracovních příkazů na základě výběrů v části **Jeden pracovní příkaz na**.</span><span class="sxs-lookup"><span data-stu-id="c9c9e-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="c9c9e-120">Vyberte **Typ pracovního příkazu**, který bude použit pro všechny vytvořené pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="c9c9e-120">Select a **Work order type** that will be used on all the work orders you create.</span></span> <span data-ttu-id="c9c9e-121">Na následujícím obrázku je uveden příklad dialogového okna **Vytvořit pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="c9c9e-121">The illustration below shows an example of the **Create work orders** dialog.</span></span>

![Obrázek č. 1](media/18-preventive-maintenance.png)

5. <span data-ttu-id="c9c9e-123">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9c9e-123">Click **OK**.</span></span> <span data-ttu-id="c9c9e-124">Je vytvořen jeden nebo více pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="c9c9e-124">One or more work orders are created.</span></span>

