---
title: Pracovní příkazy a dlouhodobý majetek
description: Toto téma vysvětluje, jak plánovat pracovní příkazy a dlouhodobý majetek v modulu Správa majetku.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 65adcd07f1649b2e4eb2e2528507bb15631782ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816717"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="ae320-103">Pracovní příkazy a dlouhodobý majetek</span><span class="sxs-lookup"><span data-stu-id="ae320-103">Work orders and fixed assets</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="ae320-104">V modulu Správa majetku mohou být majetky spojeny v dlouhodobý majetek a pro tyto majetky můžete vytvořit pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="ae320-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="ae320-105">Pokud použijete tuto funkci, můžete získat úplný přehled o dlouhodobém majetku, souvisejících investičních projektech a nákladech registrovaných u investičních projektů v modulu **Řízení projektů a účetnictví** a v modulu **Dlouhodobý majetek** v Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ae320-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs that are registered on the investment projects in the **Project management and accounting** and **Fixed assets** modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

>[!NOTE]
><span data-ttu-id="ae320-106">Pole **Číslo dlouhodobého majetku** je vyplněno v projektu úlohy pracovního příkazu pouze v případě, že jako typ projektu v projektu pracovního příkazu je vybrán typ **Investice**.</span><span class="sxs-lookup"><span data-stu-id="ae320-106">The **Fixed asset number** field on the work order job project is set only if **Investment** is selected as the project type on the work order job project.</span></span>

<span data-ttu-id="ae320-107">Na následujícím obrázku je znázorněn vztah mezi investičním projektem v modulu **řízení projektu a účetnictví** a projektem pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="ae320-107">The illustration below shows the relation between an investment project in the **Project management and accounting** module and a work order job project.</span></span>

![Obrázek č. 1](media/24-work-orders.png)

<span data-ttu-id="ae320-109">Následující postup popisuje vztah mezi majetkem, pracovními příkazy, projekty úloh pracovních příkazů a dlouhodobým majetkem.</span><span class="sxs-lookup"><span data-stu-id="ae320-109">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="ae320-110">Vytvoříte majetek, který je spojen s dlouhodobým majetkem.</span><span class="sxs-lookup"><span data-stu-id="ae320-110">You create an asset that you relate to a fixed asset.</span></span>

![Obrázek č. 2](media/25-work-orders.png)

2. <span data-ttu-id="ae320-112">Při nastavení typů pracovních příkazů na stránce **Typy pracovních příkazů** (**Správa majetku** > **Nastavení** > **Pracovní příkazy** > **Typy pracovních příkazů**) můžete vytvořit typ pracovního příkazu pro zpracování investic.</span><span class="sxs-lookup"><span data-stu-id="ae320-112">When you set up work order types on the **Work order types** page (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="ae320-113">Viz také [Typy pracovních příkazů](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="ae320-113">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![Obrázek č. 3](media/26-work-orders.png)

3. <span data-ttu-id="ae320-115">Když nastavíte skupiny projektů pracovních příkazů na kartě **Skupina projektů** stránky **Nastavení projektu pracovního příkazu** (**Správa majetku** > **Nastavení** > **Pracovní příkazy** > **Nastavení projektu**), vytvoříte vztah mezi typem pracovního příkazu, který se používá pro investice a skupinu projektů vytvořenou pro investice na stránce **Skupiny projektu** v modulu **Řízení projektů a účetnictví** (**Řízení projektů a účetnictví** > **Nastavení** > **Účtování** > **Skupiny projektů**).</span><span class="sxs-lookup"><span data-stu-id="ae320-115">When you set up work order project groups on the **Project group** tab of the **Work order project setup** page (**Asset management** > **Setup** > **Work orders** > **Project setup**), you create a relation between the work order type that is used for investments and the project group that was created for investments on the **Project groups** page in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![Obrázek č. 4](media/27-work-orders.png)

4. <span data-ttu-id="ae320-117">Když vytvoříte pracovní příkaz, který se vztahuje k objektu dlouhodobého majetku, vyberte typ pracovního příkazu, který se používá pro zpracování investic, například **Investice**.</span><span class="sxs-lookup"><span data-stu-id="ae320-117">When you create a work order that is related to a fixed asset, you select the work order type that is used to handle investments, such as **Investment**.</span></span>

5. <span data-ttu-id="ae320-118">Při vytvoření pracovního příkazu se odpovídající typ pracovního příkazu zobrazí na stránce **Všechny pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="ae320-118">When the work order is created, the related work order type is shown on the **All work orders** page.</span></span>

![Obrázek č. 5](media/28-work-orders.png)

6. <span data-ttu-id="ae320-120">Po vytvoření pracovního příkazu se na stránce **Všechny projekty** v modulu **Řízení projektů a účetnictví** vytvoří projekt související s pracovním příkazem (**Řízení projektů a účetnictví** > **Projekty** > **Všechny projekty**).</span><span class="sxs-lookup"><span data-stu-id="ae320-120">When the work order is created, the project that is related to the work order is created on the **All projects** page in the **Project management and accounting** module (**Project management and accounting** > **Projects** > **All projects**).</span></span> <span data-ttu-id="ae320-121">Chcete-li zobrazit informace související s projektem, vyberte odkaz v poli **ID projektu** na kartě **Obecné** na pevné záložce **Podrobnosti řádku** v zobrazení Podrobnosti na stránce **Všechny pracovní příkazy** v modulu **Správa majetku** (**Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy**).</span><span class="sxs-lookup"><span data-stu-id="ae320-121">To view project-related information, select the link in the **Project ID** field on the **General** tab on the **Line details** FastTab in the details view of the **All work orders** page in the **Asset management** module (**Asset management** > **Commom** > **Work orders** > **All work orders**).</span></span>

![Obrázek č. 6](media/29-work-orders.png)

7. <span data-ttu-id="ae320-123">Chcete-li zobrazit přehled projektů spojených s dlouhodobým majetkem, vyberte možnost **Dlouhodobý majetek** > **Dlouhodobý majetek** > **Dlouhodobý majetek** a pak v poli **Číslo dlouhodobého majetku** otevřete zobrazení podrobností.</span><span class="sxs-lookup"><span data-stu-id="ae320-123">To see an overview of the projects associated with a fixed asset, select **Fixed assets** > **Fixed assets** > **Fixed assets**, and then, in the **Fixed asset number** field, select the link for the fixed asset to open the details view.</span></span> <span data-ttu-id="ae320-124">Rozbalte podokno **Související informace** na pravé straně stránky a vyberte pevnou záložku **Související projekty**.</span><span class="sxs-lookup"><span data-stu-id="ae320-124">Expand the **Related information** pane on the right side of the page, and select the **Associated projects** FastTab.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]