---
title: Vytvoření pracovní třídy
description: Tento postup popisuje nastavení pracovní třídy.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6afbd9f54ef9046da10d0abc24ed545b5735a069
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146093"
---
# <a name="create-a-work-class"></a><span data-ttu-id="d7495-103">Vytvoření pracovní třídy</span><span class="sxs-lookup"><span data-stu-id="d7495-103">Create a work class</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d7495-104">Tento postup popisuje nastavení pracovní třídy.</span><span class="sxs-lookup"><span data-stu-id="d7495-104">This procedure shows you how to set up a work class.</span></span> <span data-ttu-id="d7495-105">Pracovní třídy se používají k nasměrování a/nebo omezení typu řádků pracovních příkazů, které pracovník skladu může v mobilním zařízení zpracovat.</span><span class="sxs-lookup"><span data-stu-id="d7495-105">Work classes are used to direct and/or limit the type of work order lines that a warehouse worker can process on a mobile device.</span></span> <span data-ttu-id="d7495-106">Řádky, které může pracovník zpracovat, se určují na základě pracovních tříd pro položky nabídky mobilního zařízení, k nimž má pracovník skladu přístup, a pro pracovní třídu specifikovanou na řádcích práce.</span><span class="sxs-lookup"><span data-stu-id="d7495-106">The lines that a worker can process are determined from the work classes on the mobile device menu items that the warehouse worker has access to and the work class that's specified on the work lines.</span></span> <span data-ttu-id="d7495-107">Pracovní třídy lze také použít k ověření skladového místa pro řádek pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="d7495-107">Work classes can also be used to validate the put location for a work order line.</span></span> <span data-ttu-id="d7495-108">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="d7495-108">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="d7495-109">Tento postup je určen pro vedoucího skladu.</span><span class="sxs-lookup"><span data-stu-id="d7495-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="d7495-110">Přejděte do nabídky Řízení skladu > Nastavení > Práce > Pracovní třídy.</span><span class="sxs-lookup"><span data-stu-id="d7495-110">Go to Warehouse management > Setup > Work > Work classes.</span></span>
2. <span data-ttu-id="d7495-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d7495-111">Click New.</span></span>
3. <span data-ttu-id="d7495-112">Zadejte hodnotu do pole ID pracovní třídy.</span><span class="sxs-lookup"><span data-stu-id="d7495-112">In the Work class ID field, type a value.</span></span>
4. <span data-ttu-id="d7495-113">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="d7495-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d7495-114">V poli Typ pořadí pracovních činností vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="d7495-114">In the Work order type field, select an option.</span></span>
6. <span data-ttu-id="d7495-115">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d7495-115">Click New.</span></span>
7. <span data-ttu-id="d7495-116">Zadejte hodnotu do pole Typ místa.</span><span class="sxs-lookup"><span data-stu-id="d7495-116">In the Location type field, type a value.</span></span>
    * <span data-ttu-id="d7495-117">Pokud vyberete typ umístění, nastaví se omezení s ohledem na to, kde je možné položky umístit poté, co byly vyskladněny.</span><span class="sxs-lookup"><span data-stu-id="d7495-117">If you select a location type, this sets a restriction on where items can be put after they've been picked.</span></span> <span data-ttu-id="d7495-118">Toto nastavení se používá, když se směrnice umístění pokusí o překlad umístění nebo když pracovník skladu ručně zadá umístění pro položku nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="d7495-118">This setting is used when a location directive tries to resolve the location, or if a warehouse worker manually provides the location for the mobile device menu item.</span></span>  
8. <span data-ttu-id="d7495-119">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d7495-119">Close the page.</span></span>

