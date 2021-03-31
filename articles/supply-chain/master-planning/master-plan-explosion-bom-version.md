---
title: Rozpad verze kusovníku
description: Tento článek popisuje scénář hlavního plánování, který zahrnuje rozpad verze kusovníku.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 617d9c3f05f2db30ec075a07b54c4827e668c20e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220841"
---
# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="f2950-103">Rozpad verze kusovníku</span><span class="sxs-lookup"><span data-stu-id="f2950-103">Explosion of a BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2950-104">Tento článek popisuje scénář hlavního plánování, který zahrnuje rozpad verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="f2950-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="f2950-105">Rozpad poptávky verze kusovníku vytvoří poptávku pro každou řádkovou položku kusovníku na konkrétním pracovišti a v určitém skladu (pokud taková možnost existuje).</span><span class="sxs-lookup"><span data-stu-id="f2950-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="f2950-106">Kusovník určitého pracoviště může mít pro každý řádek definovaný konkrétní sklad.</span><span class="sxs-lookup"><span data-stu-id="f2950-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="f2950-107">Nastavení dimenzí položky na každém řádku kusovníku dále určuje, zda je zadání skladu povinné.</span><span class="sxs-lookup"><span data-stu-id="f2950-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="f2950-108">Výsledná poptávka pro každý řádek kusovníku se potom stane výchozím bodem pro další rozpad poptávky.</span><span class="sxs-lookup"><span data-stu-id="f2950-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="f2950-109">Pro tento scénář hlavního plánování platí následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="f2950-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="f2950-110">Dimenze pracoviště je povinná a v případě transakce poptávky musí být zadaná.</span><span class="sxs-lookup"><span data-stu-id="f2950-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="f2950-111">Dimenze pracoviště je konzistentní.</span><span class="sxs-lookup"><span data-stu-id="f2950-111">The site dimension is consistent.</span></span> <span data-ttu-id="f2950-112">To znamená, že pracoviště v poptávce nižší úrovně je stejné, jako pracoviště v původní transakci poptávky.</span><span class="sxs-lookup"><span data-stu-id="f2950-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="f2950-113">Následující obrázek ilustruje, jakým způsobem postupuje rozpad poptávky při hlavním plánování.</span><span class="sxs-lookup"><span data-stu-id="f2950-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![Rozpad poptávky pomocí verze kusovníku](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a><span data-ttu-id="f2950-115">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="f2950-115">Additional resources</span></span>
--------

[<span data-ttu-id="f2950-116">Určení verze kusovníku</span><span class="sxs-lookup"><span data-stu-id="f2950-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="f2950-117">Přehled hlavního plánování a funkce více pracovišť</span><span class="sxs-lookup"><span data-stu-id="f2950-117">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]