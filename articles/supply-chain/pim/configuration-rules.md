---
title: Konfigurační pravidla
description: Tento článek obsahuje obecné informace o pravidlech konfigurace. Konfigurační pravidla definují vztah mezi položkami v kusovníku pro produkty, které používají technologii konfigurace založené na dimenzích.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b8b3de89235c6dac52f059af9665ea70f80d83a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007784"
---
# <a name="configuration-rules"></a><span data-ttu-id="a64bc-104">Konfigurační pravidla</span><span class="sxs-lookup"><span data-stu-id="a64bc-104">Configuration rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a64bc-105">Tento článek obsahuje obecné informace o pravidlech konfigurace.</span><span class="sxs-lookup"><span data-stu-id="a64bc-105">This article provides general information about configuration rules.</span></span> <span data-ttu-id="a64bc-106">Konfigurační pravidla definují vztah mezi položkami v kusovníku pro produkty, které používají technologii konfigurace založené na dimenzích.</span><span class="sxs-lookup"><span data-stu-id="a64bc-106">Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.</span></span>

<span data-ttu-id="a64bc-107">Konfigurační pravidla jsou k dispozici při definování modelů konfigurace založené na dimenzích.</span><span class="sxs-lookup"><span data-stu-id="a64bc-107">Configuration rules are available when you define dimension-based configuration models.</span></span> <span data-ttu-id="a64bc-108">Konfigurační pravidla se používají k vynucení nebo zakázání kombinace specifických položek v kusovníku.</span><span class="sxs-lookup"><span data-stu-id="a64bc-108">Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM).</span></span> <span data-ttu-id="a64bc-109">Poté, co byl vytvořen kusovník, a příslušné položky byly přiřazeny k jejich odpovídajícím konfiguračním skupinám, lze definovat jedno nebo více konfiguračních pravidel.</span><span class="sxs-lookup"><span data-stu-id="a64bc-109">After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined.</span></span> <span data-ttu-id="a64bc-110">Pokud dvě položky patří dohromady, operátor **Vybrat** slouží k jejich zařazení.</span><span class="sxs-lookup"><span data-stu-id="a64bc-110">If two items belong together, the **Select** operator is used to ensure inclusion.</span></span> <span data-ttu-id="a64bc-111">Pokud se dvě položky vzájemně vylučují, operátor **Zrušit výběr** slouží k jejich vyloučení.</span><span class="sxs-lookup"><span data-stu-id="a64bc-111">If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion.</span></span>  

<span data-ttu-id="a64bc-112">**Poznámka:** Tyto informace se týkají pouze základních produktů, které používají konfiguraci založenou na dimenzích.</span><span class="sxs-lookup"><span data-stu-id="a64bc-112">**Note:** This information applies only to product masters that use the dimension-based configuration technology.</span></span>  

<span data-ttu-id="a64bc-113">Stávající konfigurace nejsou následnými změnami konfiguračních pravidel ovlivněny.</span><span class="sxs-lookup"><span data-stu-id="a64bc-113">Existing configurations aren't affected by subsequent changes to the configuration rules.</span></span> <span data-ttu-id="a64bc-114">Je však důležité tato pravidla stanovit před definováním nové konfigurace nebo je zkontrolovat, jestliže si myslíte, že došlo ke změně pravidel.</span><span class="sxs-lookup"><span data-stu-id="a64bc-114">However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed.</span></span>  

<span data-ttu-id="a64bc-115">**Poznámka:** Metoda **Vybrat** znamená, že odvozená konfigurační skupina, číslo položky a konfigurace se vyberou automaticky.</span><span class="sxs-lookup"><span data-stu-id="a64bc-115">**Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected.</span></span> <span data-ttu-id="a64bc-116">Metoda **Zrušit výběr** znamená, že odvozenou konfigurační skupinu, číslo položky a konfiguraci nelze vybrat.</span><span class="sxs-lookup"><span data-stu-id="a64bc-116">For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.</span></span>

<a name="additional-resources"></a><span data-ttu-id="a64bc-117">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="a64bc-117">Additional resources</span></span>
--------

[<span data-ttu-id="a64bc-118">Přehled konfigurace produktu založeného na dimenzích</span><span class="sxs-lookup"><span data-stu-id="a64bc-118">Dimension-based product configuration overview</span></span>](dimension-based-product-configuration.md)



