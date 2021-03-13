---
title: Funkční místa a majetek
description: Toto téma popisuje funkční místa a majetek v modulu Správa majetku. Správa majetku je rozšířený modul pro správu majetku a úloh údržby v aplikaci Dynamics 365 Supply Chain Management.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f93a68f19b0b952eb2964b404bb957865c625cd
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018039"
---
# <a name="functional-locations-and-assets"></a><span data-ttu-id="14532-104">Funkční místa a majetek</span><span class="sxs-lookup"><span data-stu-id="14532-104">Functional locations and assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="14532-105">Toto téma popisuje funkční místa a majetek v modulu Správa majetku.</span><span class="sxs-lookup"><span data-stu-id="14532-105">This topic describes functional locations and assets in Asset Management.</span></span> <span data-ttu-id="14532-106">Správa majetku je rozšířený modul pro správu majetku a úloh údržby v aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="14532-106">Asset Management is an advanced module for managing assets and maintenance jobs in Dynamics 365 Supply Chain Management.</span></span>

## <a name="overview"></a><span data-ttu-id="14532-107">Přehled</span><span class="sxs-lookup"><span data-stu-id="14532-107">Overview</span></span>

<span data-ttu-id="14532-108">Správa majetku je bezproblémově integrována s několika moduly v dalších aplikacích Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="14532-108">Asset Management is integrated seamlessly with several modules with other Finance and Operations apps.</span></span> <span data-ttu-id="14532-109">Následující ilustrace znázorňuje rozhraní s jinými moduly.</span><span class="sxs-lookup"><span data-stu-id="14532-109">The following illustration shows the interfaces with other modules.</span></span>

![Diagram znázorňující způsob, jakým jsou rozhraní správy majetku s jinými moduly](media/01-overview-image.png)

<span data-ttu-id="14532-111">Správa majetku umožňuje efektivně spravovat a provádět všechny úkoly související se správou a údržbou mnoha typů zařízení ve vaší firmě.</span><span class="sxs-lookup"><span data-stu-id="14532-111">Asset Management lets you efficiently manage and perform all tasks that are related to managing and servicing many types of equipment in your company.</span></span> <span data-ttu-id="14532-112">Toto zařízení zahrnuje stroje, výrobní zařízení a vozidla.</span><span class="sxs-lookup"><span data-stu-id="14532-112">This equipment includes machines, production equipment, and vehicles.</span></span> <span data-ttu-id="14532-113">Správa majetku též podporuje řešení napříč četnými průmyslovými odvětvími.</span><span class="sxs-lookup"><span data-stu-id="14532-113">Asset Management also supports solutions across numerous industries.</span></span>

<span data-ttu-id="14532-114">Následující ilustrace znázorňuje přehled hlavních funkcí, které jsou pokryty správou majetku.</span><span class="sxs-lookup"><span data-stu-id="14532-114">The following illustration shows an overview of the main functionality that is covered by Asset Management.</span></span>

![Diagram znázorňující hlavní funkce ve správě majetku](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a><span data-ttu-id="14532-116">Funkční místa a majetek</span><span class="sxs-lookup"><span data-stu-id="14532-116">Functional locations and assets</span></span>

<span data-ttu-id="14532-117">Funkční místa slouží ke správě majetku na místech.</span><span class="sxs-lookup"><span data-stu-id="14532-117">Functional locations are used to manage assets on locations.</span></span> <span data-ttu-id="14532-118">Tato správa zahrnuje sledování nákladů na majetek na funkčních místech.</span><span class="sxs-lookup"><span data-stu-id="14532-118">This management includes tracking of asset costs on functional locations.</span></span> <span data-ttu-id="14532-119">Funkční místa jsou strukturovaná hierarchicky a místa mohou mít dílčí místa.</span><span class="sxs-lookup"><span data-stu-id="14532-119">Functional locations are structured hierarchically, and locations can have sub-locations.</span></span> <span data-ttu-id="14532-120">Struktura funkčních míst je statická.</span><span class="sxs-lookup"><span data-stu-id="14532-120">The structure of functional locations is static.</span></span> <span data-ttu-id="14532-121">Jinými slovy, místa nemohou změnit místo.</span><span class="sxs-lookup"><span data-stu-id="14532-121">In other words, locations can't change place.</span></span> <span data-ttu-id="14532-122">Majetek může být instalován na funkčních místech a podle potřeby může být později instalován na jiná funkční místa.</span><span class="sxs-lookup"><span data-stu-id="14532-122">Assets can be installed on functional locations and, as required, can be installed on other functional locations later.</span></span>

<span data-ttu-id="14532-123">Náklady na majetek se vždy řídí místem majetku.</span><span class="sxs-lookup"><span data-stu-id="14532-123">Asset costs always follow the location of the asset.</span></span> <span data-ttu-id="14532-124">Jinými slovy, pokud je majetek instalován na novém funkčním místě, majetek automaticky použije finanční dimenze, které souvisejí s novým funkčním místem.</span><span class="sxs-lookup"><span data-stu-id="14532-124">In other words, if you install an asset on a new functional location, the asset automatically uses the financial dimensions that are related to the new functional location.</span></span> <span data-ttu-id="14532-125">Proto jsou náklady na majetek vždy spojeny s funkčním místem, na kterém je majetek aktuálně nainstalován.</span><span class="sxs-lookup"><span data-stu-id="14532-125">Therefore, asset costs are always related to the functional location that the asset is  currently installed on.</span></span> <span data-ttu-id="14532-126">Toto automatické zpracování finančních dimenzí zaručuje úplné sledování nákladů, když vaše společnost provádí kontrola a hlášení projektu na funkčních místech.</span><span class="sxs-lookup"><span data-stu-id="14532-126">This automatic handling of financial dimensions helps guarantee complete tracking of costs when your company does project controlling and reporting on functional locations.</span></span>

<span data-ttu-id="14532-127">Způsob vytvoření hierarchie funkčních míst závisí na požadavcích vaší společnosti na údržbu interního vybavení nebo na údržbě vybavení zákazníka.</span><span class="sxs-lookup"><span data-stu-id="14532-127">The way that you build your hierarchy of functional locations depends on your company's requirements for maintaining internal equipment or servicing customer equipment.</span></span> <span data-ttu-id="14532-128">Následující obrázek znázorňuje příklad funkčních míst, která jsou založena na zeměpisných lokalitách.</span><span class="sxs-lookup"><span data-stu-id="14532-128">The following figure shows an example of functional locations that are based on geographical locations.</span></span>

![Diagram znázorňující funkční místa na základě geografických umístění](media/03-overview-image.png)

<span data-ttu-id="14532-130">Následující obrázek znázorňuje příklad funkčních míst, která jsou založena na zákaznících.</span><span class="sxs-lookup"><span data-stu-id="14532-130">The following figure shows an example of functional locations that are based on customers.</span></span>

![Diagram znázorňující funkční místa na základě zákazníků](media/04-overview-image.png)
