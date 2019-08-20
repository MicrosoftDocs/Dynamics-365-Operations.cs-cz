---
title: Funkční místa a majetek
description: Toto téma popisuje funkční místa a majetek v modulu Správa majetku. Správa majetku je rozšířený modul pro správu majetku a úloh údržby v aplikaci Microsoft Dynamics 365 for Finance and Operations.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 351e27dfbbd5227a9642f14a48afe194c447a0f3
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783138"
---
# <a name="functional-locations-and-assets"></a><span data-ttu-id="d6313-104">Funkční místa a majetek</span><span class="sxs-lookup"><span data-stu-id="d6313-104">Functional locations and assets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="d6313-105">Toto téma popisuje funkční místa a majetek v modulu Správa majetku.</span><span class="sxs-lookup"><span data-stu-id="d6313-105">This topic describes functional locations and assets in Asset Management.</span></span> <span data-ttu-id="d6313-106">Správa majetku je rozšířený modul pro správu majetku a úloh údržby v aplikaci Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d6313-106">Asset Management is an advanced module for managing assets and maintenance jobs in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="overview"></a><span data-ttu-id="d6313-107">Přehled</span><span class="sxs-lookup"><span data-stu-id="d6313-107">Overview</span></span>

<span data-ttu-id="d6313-108">Správa majetku je bezproblémově integrována s několika moduly v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d6313-108">Asset Management is integrated seamlessly with several modules in Finance and Operations.</span></span> <span data-ttu-id="d6313-109">Následující ilustrace znázorňuje rozhraní s jinými moduly.</span><span class="sxs-lookup"><span data-stu-id="d6313-109">The following illustration shows the interfaces with other modules.</span></span>

![Obrázek č. 1](media/01-overview-image.png)

<span data-ttu-id="d6313-111">Správa majetku umožňuje efektivně spravovat a provádět všechny úkoly související se správou a údržbou mnoha typů zařízení ve vaší firmě.</span><span class="sxs-lookup"><span data-stu-id="d6313-111">Asset Management lets you efficiently manage and perform all tasks that are related to managing and servicing many types of equipment in your company.</span></span> <span data-ttu-id="d6313-112">Toto zařízení zahrnuje stroje, výrobní zařízení a vozidla.</span><span class="sxs-lookup"><span data-stu-id="d6313-112">This equipment includes machines, production equipment, and vehicles.</span></span> <span data-ttu-id="d6313-113">Správa majetku též podporuje řešení napříč četnými průmyslovými odvětvími.</span><span class="sxs-lookup"><span data-stu-id="d6313-113">Asset Management also supports solutions across numerous industries.</span></span>

<span data-ttu-id="d6313-114">Následující ilustrace znázorňuje přehled hlavních funkcí, které jsou pokryty správou majetku.</span><span class="sxs-lookup"><span data-stu-id="d6313-114">The following illustration shows an overview of the main functionality that is covered by Asset Management.</span></span>

![Obrázek č. 2](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a><span data-ttu-id="d6313-116">Funkční místa a majetek</span><span class="sxs-lookup"><span data-stu-id="d6313-116">Functional locations and assets</span></span>

<span data-ttu-id="d6313-117">Funkční místa slouží ke správě majetku na místech.</span><span class="sxs-lookup"><span data-stu-id="d6313-117">Functional locations are used to manage assets on locations.</span></span> <span data-ttu-id="d6313-118">Tato správa zahrnuje sledování nákladů na majetek na funkčních místech.</span><span class="sxs-lookup"><span data-stu-id="d6313-118">This management includes tracking of asset costs on functional locations.</span></span> <span data-ttu-id="d6313-119">Funkční místa jsou strukturovaná hierarchicky a místa mohou mít dílčí místa.</span><span class="sxs-lookup"><span data-stu-id="d6313-119">Functional locations are structured hierarchically, and locations can have sub-locations.</span></span> <span data-ttu-id="d6313-120">Struktura funkčních míst je statická.</span><span class="sxs-lookup"><span data-stu-id="d6313-120">The structure of functional locations is static.</span></span> <span data-ttu-id="d6313-121">Jinými slovy, místa nemohou změnit místo.</span><span class="sxs-lookup"><span data-stu-id="d6313-121">In other words, locations can't change place.</span></span> <span data-ttu-id="d6313-122">Majetek může být instalován na funkčních místech a podle potřeby může být později instalován na jiná funkční místa.</span><span class="sxs-lookup"><span data-stu-id="d6313-122">Assets can be installed on functional locations and, as required, can be installed on other functional locations later.</span></span>

<span data-ttu-id="d6313-123">Náklady na majetek se vždy řídí místem majetku.</span><span class="sxs-lookup"><span data-stu-id="d6313-123">Asset costs always follow the location of the asset.</span></span> <span data-ttu-id="d6313-124">Jinými slovy, pokud je majetek instalován na novém funkčním místě, majetek automaticky použije finanční dimenze, které souvisejí s novým funkčním místem.</span><span class="sxs-lookup"><span data-stu-id="d6313-124">In other words, if you install an asset on a new functional location, the asset automatically uses the financial dimensions that are related to the new functional location.</span></span> <span data-ttu-id="d6313-125">Proto jsou náklady na majetek vždy spojeny s funkčním místem, na kterém je majetek aktuálně nainstalován.</span><span class="sxs-lookup"><span data-stu-id="d6313-125">Therefore, asset costs are always related to the functional location that the asset is  currently installed on.</span></span> <span data-ttu-id="d6313-126">Toto automatické zpracování finančních dimenzí zaručuje úplné sledování nákladů, když vaše společnost provádí kontrola a hlášení projektu na funkčních místech.</span><span class="sxs-lookup"><span data-stu-id="d6313-126">This automatic handling of financial dimensions helps guarantee complete tracking of costs when your company does project controlling and reporting on functional locations.</span></span>

<span data-ttu-id="d6313-127">Způsob vytvoření hierarchie funkčních míst závisí na požadavcích vaší společnosti na údržbu interního vybavení nebo na údržbě vybavení zákazníka.</span><span class="sxs-lookup"><span data-stu-id="d6313-127">The way that you build your hierarchy of functional locations depends on your company's requirements for maintaining internal equipment or servicing customer equipment.</span></span> <span data-ttu-id="d6313-128">Následující obrázek znázorňuje příklad funkčních míst, která jsou založena na zeměpisných lokalitách.</span><span class="sxs-lookup"><span data-stu-id="d6313-128">The following figure shows an example of functional locations that are based on geographical locations.</span></span>

![Obrázek č. 3](media/03-overview-image.png)

<span data-ttu-id="d6313-130">Následující obrázek znázorňuje příklad funkčních míst, která jsou založena na zákaznících.</span><span class="sxs-lookup"><span data-stu-id="d6313-130">The following figure shows an example of functional locations that are based on customers.</span></span>

![Obrázek č. 4](media/04-overview-image.png)
