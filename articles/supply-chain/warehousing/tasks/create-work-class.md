--- 
title: "Vytvoření pracovní třídy"
description: "Tento postup popisuje nastavení pracovní třídy."
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 5def9be0966d65728ffb0897229c0d749e7e13a0
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-work-class"></a><span data-ttu-id="f3118-103">Vytvoření pracovní třídy</span><span class="sxs-lookup"><span data-stu-id="f3118-103">Create a work class</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f3118-104">Tento postup popisuje nastavení pracovní třídy.</span><span class="sxs-lookup"><span data-stu-id="f3118-104">This procedure shows you how to set up a work class.</span></span> <span data-ttu-id="f3118-105">Pracovní třídy se používají k nasměrování a/nebo omezení typu řádků pracovních příkazů, které pracovník skladu může v mobilním zařízení zpracovat.</span><span class="sxs-lookup"><span data-stu-id="f3118-105">Work classes are used to direct and/or limit the type of work order lines that a warehouse worker can process on a mobile device.</span></span> <span data-ttu-id="f3118-106">Řádky, které může pracovník zpracovat, se určují na základě pracovních tříd pro položky nabídky mobilního zařízení, k nimž má pracovník skladu přístup, a pro pracovní třídu specifikovanou na řádcích práce.</span><span class="sxs-lookup"><span data-stu-id="f3118-106">The lines that a worker can process are determined from the work classes on the mobile device menu items that the warehouse worker has access to and the work class that’s specified on the work lines.</span></span> <span data-ttu-id="f3118-107">Pracovní třídy lze také použít k ověření skladového místa pro řádek pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="f3118-107">Work classes can also be used to validate the put location for a work order line.</span></span> <span data-ttu-id="f3118-108">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="f3118-108">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="f3118-109">Tento postup je určen pro vedoucího skladu.</span><span class="sxs-lookup"><span data-stu-id="f3118-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="f3118-110">Přejděte do nabídky Řízení skladu > Nastavení > Práce > Pracovní třídy.</span><span class="sxs-lookup"><span data-stu-id="f3118-110">Go to Warehouse management > Setup > Work > Work classes.</span></span>
2. <span data-ttu-id="f3118-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="f3118-111">Click New.</span></span>
3. <span data-ttu-id="f3118-112">Zadejte hodnotu do pole ID pracovní třídy.</span><span class="sxs-lookup"><span data-stu-id="f3118-112">In the Work class ID field, type a value.</span></span>
4. <span data-ttu-id="f3118-113">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="f3118-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f3118-114">V poli Typ pořadí pracovních činností vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="f3118-114">In the Work order type field, select an option.</span></span>
6. <span data-ttu-id="f3118-115">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="f3118-115">Click New.</span></span>
7. <span data-ttu-id="f3118-116">Zadejte hodnotu do pole Typ místa.</span><span class="sxs-lookup"><span data-stu-id="f3118-116">In the Location type field, type a value.</span></span>
    * <span data-ttu-id="f3118-117">Pokud vyberete typ umístění, nastaví se omezení s ohledem na to, kde je možné položky umístit poté, co byly vyskladněny.</span><span class="sxs-lookup"><span data-stu-id="f3118-117">If you select a location type, this sets a restriction on where items can be put after they’ve been picked.</span></span> <span data-ttu-id="f3118-118">Toto nastavení se používá, když se směrnice umístění pokusí o překlad umístění nebo když pracovník skladu ručně zadá umístění pro položku nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="f3118-118">This setting is used when a location directive tries to resolve the location, or if a warehouse worker manually provides the location for the mobile device menu item.</span></span>  
8. <span data-ttu-id="f3118-119">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="f3118-119">Close the page.</span></span>


