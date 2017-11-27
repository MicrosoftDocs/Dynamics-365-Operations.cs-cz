---
title: "Určení verze kusovníku"
description: "Pokud má položka při rozpadu poptávky výchozí typ plánované objednávky Výroba, modul plánování najde platnou verzi kusovníku na základě pracoviště."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, InventItemOrderSetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7e6745a52138e545b557fa1aa286cd49481b2ecd
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="determine-the-bom-version"></a><span data-ttu-id="cdf2e-103">Určení verze kusovníku</span><span class="sxs-lookup"><span data-stu-id="cdf2e-103">Determine the BOM version</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="cdf2e-104">Pokud má položka při rozpadu poptávky výchozí typ plánované objednávky Výroba, modul plánování najde platnou verzi kusovníku na základě pracoviště.</span><span class="sxs-lookup"><span data-stu-id="cdf2e-104">During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site.</span></span> 

<span data-ttu-id="cdf2e-105">Dimenze pracoviště je vždy známa a je uvedena v transakci poptávky.</span><span class="sxs-lookup"><span data-stu-id="cdf2e-105">The site dimension is always known and is stated on the demand transaction.</span></span> <span data-ttu-id="cdf2e-106">K určení použité verze kusovníku se využívá následující proces:</span><span class="sxs-lookup"><span data-stu-id="cdf2e-106">The following process is used to determine the BOM version to use:</span></span>

-   <span data-ttu-id="cdf2e-107">Pokud pro položku existuje verze kusovníku definovaná na pracovišti uvedeném v poptávce, bude použit kusovník specifický pro pracoviště.</span><span class="sxs-lookup"><span data-stu-id="cdf2e-107">If there is a BOM version defined for the item at the demand site, the site-specific BOM is used.</span></span>
-   <span data-ttu-id="cdf2e-108">Pokud pro položku neexistuje verze kusovníku definovaná pro pracoviště uvedené v poptávce, bude použit obecný kusovník.</span><span class="sxs-lookup"><span data-stu-id="cdf2e-108">If there is no site-specific BOM version defined for an item at the demand site, a general BOM is used.</span></span> <span data-ttu-id="cdf2e-109">Obecný kusovník není vázán na pracoviště a platí pro více pracovišť.</span><span class="sxs-lookup"><span data-stu-id="cdf2e-109">A general BOM does not state a site, and it is valid for multiple sites.</span></span> <span data-ttu-id="cdf2e-110">Pokud existuje obecný kusovník, bude použit.</span><span class="sxs-lookup"><span data-stu-id="cdf2e-110">If there is a general BOM, it is used.</span></span>
-   <span data-ttu-id="cdf2e-111">V případě, že neexistuje žádná obecná verze kusovníku, kterou by bylo možné použít, rozpad poptávky se v tomto bodě zastaví.</span><span class="sxs-lookup"><span data-stu-id="cdf2e-111">If there is no general BOM version to use, the demand explosion stops at this point.</span></span>

<span data-ttu-id="cdf2e-112">Platná verze kusovníku, bez ohledu na to, zda se jedná o specifický kusovník pracoviště nebo obecný kusovník, musí splňovat vyžadovaná kritéria data a množství.</span><span class="sxs-lookup"><span data-stu-id="cdf2e-112">A valid BOM version, whether site-specific or general, must meet the required criteria for date and quantity.</span></span>






