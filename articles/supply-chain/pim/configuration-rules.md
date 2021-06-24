---
title: Konfigurační pravidla
description: Tento článek obsahuje obecné informace o pravidlech konfigurace. Konfigurační pravidla definují vztah mezi položkami v kusovníku pro produkty, které používají technologii konfigurace založené na dimenzích.
author: cvocph
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 70aff927dfea602ee6c4ad5c195274248f831bcb
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6190177"
---
# <a name="configuration-rules"></a><span data-ttu-id="5cf8b-104">Konfigurační pravidla</span><span class="sxs-lookup"><span data-stu-id="5cf8b-104">Configuration rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5cf8b-105">Tento článek obsahuje obecné informace o pravidlech konfigurace.</span><span class="sxs-lookup"><span data-stu-id="5cf8b-105">This article provides general information about configuration rules.</span></span> <span data-ttu-id="5cf8b-106">Konfigurační pravidla definují vztah mezi položkami v kusovníku pro produkty, které používají technologii konfigurace založené na dimenzích.</span><span class="sxs-lookup"><span data-stu-id="5cf8b-106">Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.</span></span>

<span data-ttu-id="5cf8b-107">Konfigurační pravidla jsou k dispozici při definování modelů konfigurace založené na dimenzích.</span><span class="sxs-lookup"><span data-stu-id="5cf8b-107">Configuration rules are available when you define dimension-based configuration models.</span></span> <span data-ttu-id="5cf8b-108">Konfigurační pravidla se používají k vynucení nebo zakázání kombinace specifických položek v kusovníku.</span><span class="sxs-lookup"><span data-stu-id="5cf8b-108">Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM).</span></span> <span data-ttu-id="5cf8b-109">Poté, co byl vytvořen kusovník, a příslušné položky byly přiřazeny k jejich odpovídajícím konfiguračním skupinám, lze definovat jedno nebo více konfiguračních pravidel.</span><span class="sxs-lookup"><span data-stu-id="5cf8b-109">After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined.</span></span> <span data-ttu-id="5cf8b-110">Pokud dvě položky patří dohromady, operátor **Vybrat** slouží k jejich zařazení.</span><span class="sxs-lookup"><span data-stu-id="5cf8b-110">If two items belong together, the **Select** operator is used to ensure inclusion.</span></span> <span data-ttu-id="5cf8b-111">Pokud se dvě položky vzájemně vylučují, operátor **Zrušit výběr** slouží k jejich vyloučení.</span><span class="sxs-lookup"><span data-stu-id="5cf8b-111">If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion.</span></span>  

<span data-ttu-id="5cf8b-112">**Poznámka:** Tyto informace se týkají pouze základních produktů, které používají konfiguraci založenou na dimenzích.</span><span class="sxs-lookup"><span data-stu-id="5cf8b-112">**Note:** This information applies only to product masters that use the dimension-based configuration technology.</span></span>  

<span data-ttu-id="5cf8b-113">Stávající konfigurace nejsou následnými změnami konfiguračních pravidel ovlivněny.</span><span class="sxs-lookup"><span data-stu-id="5cf8b-113">Existing configurations aren't affected by subsequent changes to the configuration rules.</span></span> <span data-ttu-id="5cf8b-114">Je však důležité tato pravidla stanovit před definováním nové konfigurace nebo je zkontrolovat, jestliže si myslíte, že došlo ke změně pravidel.</span><span class="sxs-lookup"><span data-stu-id="5cf8b-114">However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed.</span></span>  

<span data-ttu-id="5cf8b-115">**Poznámka:** Metoda **Vybrat** znamená, že odvozená konfigurační skupina, číslo položky a konfigurace se vyberou automaticky.</span><span class="sxs-lookup"><span data-stu-id="5cf8b-115">**Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected.</span></span> <span data-ttu-id="5cf8b-116">Metoda **Zrušit výběr** znamená, že odvozenou konfigurační skupinu, číslo položky a konfiguraci nelze vybrat.</span><span class="sxs-lookup"><span data-stu-id="5cf8b-116">For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5cf8b-117">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="5cf8b-117">Additional resources</span></span>

[<span data-ttu-id="5cf8b-118">Přehled konfigurace produktu založeného na dimenzích</span><span class="sxs-lookup"><span data-stu-id="5cf8b-118">Dimension-based product configuration overview</span></span>](dimension-based-product-configuration.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]