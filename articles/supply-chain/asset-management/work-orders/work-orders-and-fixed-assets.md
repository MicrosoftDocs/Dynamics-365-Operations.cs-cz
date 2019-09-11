---
title: Pracovní příkazy a dlouhodobý majetek
description: Toto téma vysvětluje, jak plánovat pracovní příkazy a dlouhodobý majetek v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f03b7fa073c4e5338b7b5681ba7b8c9fe00a657b
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875540"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="c5aa7-103">Pracovní příkazy a dlouhodobý majetek</span><span class="sxs-lookup"><span data-stu-id="c5aa7-103">Work orders and fixed assets</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="c5aa7-104">V modulu Správa majetku mohou být majetky spojeny v dlouhodobý majetek a pro tyto majetky můžete vytvořit pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="c5aa7-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="c5aa7-105">Pokud použijete tuto funkci, můžete získat úplný přehled o dlouhodobém majetku, souvisejících investičních projektech a nákladech registrovaných u investičních projektů v modulu **Řízení projektů a účetnictví** a v modulu **Dlouhodobý majetek** v Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c5aa7-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs registered on the investment projects in the **Project management and accounting** module and the **Fixed assets** module in Dynamics 365 for Finance and Operations.</span></span>

>[!NOTE]
><span data-ttu-id="c5aa7-106">Pole **Číslo dlouhodobého majetku** je vyplněno v projektu úlohy pracovního příkazu pouze v případě, že jako typ projektu v projektu pracovního příkazu je vybrán typ „Investice“.</span><span class="sxs-lookup"><span data-stu-id="c5aa7-106">The **Fixed asset number** field is only filled out on the work order job project if type "Investment" is selected as the project type on the work order job project.</span></span>

![Obrázek č. 1](media/24-work-orders.png)

<span data-ttu-id="c5aa7-108">Následující postup popisuje vztah mezi majetkem, pracovními příkazy, projekty úloh pracovních příkazů a dlouhodobým majetkem.</span><span class="sxs-lookup"><span data-stu-id="c5aa7-108">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="c5aa7-109">Vytvoříte majetek, který spojíte s dlouhodobým majetkem, jak je znázorněno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="c5aa7-109">You create an asset that you relate to a fixed asset, as shown in the figure below.</span></span>

![Obrázek č. 2](media/25-work-orders.png)

2. <span data-ttu-id="c5aa7-111">Při nastavení typů pracovních příkazů (**Správa majetku** > **Nastavení** > **Pracovní příkazy** > **Typy pracovních příkazů**) můžete vytvořit typ pracovního příkazu pro zpracování investic.</span><span class="sxs-lookup"><span data-stu-id="c5aa7-111">When you set up work order types (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="c5aa7-112">Viz také [Typy pracovních příkazů](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="c5aa7-112">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![Obrázek č. 3](media/26-work-orders.png)

3. <span data-ttu-id="c5aa7-114">Když nastavíte skupiny projektů pracovních příkazů (**Správa majetku** > **Nastavení** > **Pracovní příkazy** > **Nastavení projektu** >  odkaz **Skupina projektů**), vytvoříte vztah mezi typem pracovního příkazu, který se používá pro investice a skupinu projektů vytvořenou pro investice v modulu **Řízení projektů a účetnictví** (**Řízení projektů a účetnictví** > **Nastavení** > **Účtování** > **Skupiny projektů**).</span><span class="sxs-lookup"><span data-stu-id="c5aa7-114">When you set up work order project groups (**Asset management** > **Setup** > **Work orders** > **Project setup** > **Project group** link), you create a relation between the work order type used for investments and the project group created for investments in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![Obrázek č. 4](media/27-work-orders.png)

4. <span data-ttu-id="c5aa7-116">Když vytvoříte pracovní příkaz, který se vztahuje k objektu dlouhodobého majetku, vyberte typ pracovního příkazu, který se používá pro zpracování investic, například "investice".</span><span class="sxs-lookup"><span data-stu-id="c5aa7-116">When you create a work order that relates to a fixed asset object, you select the work order type used for handling investments, for example, "Investment".</span></span>

5. <span data-ttu-id="c5aa7-117">Při vytvoření pracovního příkazu se odpovídající typ pracovního příkazu zobrazí ve **Všech pracovních příkazech**.</span><span class="sxs-lookup"><span data-stu-id="c5aa7-117">When the work order is created, the related work order type is shown in **All work orders**.</span></span>

![Obrázek č. 5](media/28-work-orders.png)

6. <span data-ttu-id="c5aa7-119">Při vytvoření pracovního příkazu je projekt související s pracovním příkazem vytvořen v **Řízení projektů a účetnictví** > **Všechny projekty**.</span><span class="sxs-lookup"><span data-stu-id="c5aa7-119">When the work order is created, the project related to the work order is created in **Project management and accounting** > **All projects**.</span></span> <span data-ttu-id="c5aa7-120">Informace týkající se projektu můžete vidět, kliknete-li na odkaz **ID projektu** na pracovním příkazu (ve **Správě majetku** otevřete pracovní příkaz v zobrazení Podrobnosti > pevná záložka **Podrobnosti řádku** > karta **Obecné** > pole **ID projektu**).</span><span class="sxs-lookup"><span data-stu-id="c5aa7-120">You can see project-related information by clicking the **Project ID** link on the work order (in **Asset management**, open the work order in Details view > **Line details** FastTab > **General** tab > **Project ID** field).</span></span>

![Obrázek č. 6](media/29-work-orders.png)

7. <span data-ttu-id="c5aa7-122">V modulu **Dlouhodobý majetek** lze zobrazit přehled projektů přiřazených k dlouhodobému majetku (**Dlouhodobý majetek** > **Dlouhodobý majetek** > **Dlouhodobý majetek** > klikněte na položku dlouhodobého majetku v poli **Číslo dlouhodobého majetku** > zobrazení obsahu v podokně **Související informace** > oddíl **Přidružené projekty**).</span><span class="sxs-lookup"><span data-stu-id="c5aa7-122">In **Fixed assets**, you are able to see an overview of the projects associated with a fixed asset (**Fixed assets** > **Fixed assets** > **Fixed assets** > click on the fixed asset in the **Fixed asset number** field > view the contents in the **Related information** pane > **Associated projects** section).</span></span>

