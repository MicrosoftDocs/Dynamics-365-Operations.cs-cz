---
title: Určení verze kusovníku
description: Pokud má položka při rozpadu poptávky výchozí typ plánované objednávky Výroba, modul plánování najde platnou verzi kusovníku na základě pracoviště.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf125e2b75c4dfa406f4f05b249e6fdb49c84b7d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "325082"
---
# <a name="determine-the-bom-version"></a><span data-ttu-id="fb3e1-103">Určení verze kusovníku</span><span class="sxs-lookup"><span data-stu-id="fb3e1-103">Determine the BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb3e1-104">Pokud má položka při rozpadu poptávky výchozí typ plánované objednávky Výroba, modul plánování najde platnou verzi kusovníku na základě pracoviště.</span><span class="sxs-lookup"><span data-stu-id="fb3e1-104">During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site.</span></span> 

<span data-ttu-id="fb3e1-105">Dimenze pracoviště je vždy známa a je uvedena v transakci poptávky.</span><span class="sxs-lookup"><span data-stu-id="fb3e1-105">The site dimension is always known and is stated on the demand transaction.</span></span> <span data-ttu-id="fb3e1-106">K určení použité verze kusovníku se využívá následující proces:</span><span class="sxs-lookup"><span data-stu-id="fb3e1-106">The following process is used to determine the BOM version to use:</span></span>

-   <span data-ttu-id="fb3e1-107">Pokud pro položku existuje verze kusovníku definovaná na pracovišti uvedeném v poptávce, bude použit kusovník specifický pro pracoviště.</span><span class="sxs-lookup"><span data-stu-id="fb3e1-107">If there is a BOM version defined for the item at the demand site, the site-specific BOM is used.</span></span>
-   <span data-ttu-id="fb3e1-108">Pokud pro položku neexistuje verze kusovníku definovaná pro pracoviště uvedené v poptávce, bude použit obecný kusovník.</span><span class="sxs-lookup"><span data-stu-id="fb3e1-108">If there is no site-specific BOM version defined for an item at the demand site, a general BOM is used.</span></span> <span data-ttu-id="fb3e1-109">Obecný kusovník není vázán na pracoviště a platí pro více pracovišť.</span><span class="sxs-lookup"><span data-stu-id="fb3e1-109">A general BOM does not state a site, and it is valid for multiple sites.</span></span> <span data-ttu-id="fb3e1-110">Pokud existuje obecný kusovník, bude použit.</span><span class="sxs-lookup"><span data-stu-id="fb3e1-110">If there is a general BOM, it is used.</span></span>
-   <span data-ttu-id="fb3e1-111">V případě, že neexistuje žádná obecná verze kusovníku, kterou by bylo možné použít, rozpad poptávky se v tomto bodě zastaví.</span><span class="sxs-lookup"><span data-stu-id="fb3e1-111">If there is no general BOM version to use, the demand explosion stops at this point.</span></span>

<span data-ttu-id="fb3e1-112">Platná verze kusovníku, bez ohledu na to, zda se jedná o specifický kusovník pracoviště nebo obecný kusovník, musí splňovat vyžadovaná kritéria data a množství.</span><span class="sxs-lookup"><span data-stu-id="fb3e1-112">A valid BOM version, whether site-specific or general, must meet the required criteria for date and quantity.</span></span>





