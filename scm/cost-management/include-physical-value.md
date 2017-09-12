---
title: Zahrnovat fyzickou hodnotu
description: "Pole Zahrnout fyzickou hodnotu na pevné záložce Skladový model na stránce Skupiny modelů položky se používá k určení toho, zda se fyzicky aktualizované transakce promítnou do výpočtu průběžných průměrných nákladových ceny položky."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: fa59031ed2144c2e92399933cd5dd40bfca0f2ae
ms.contentlocale: cs-cz
ms.lasthandoff: 07/18/2017

---

# <a name="include-physical-value"></a><span data-ttu-id="693ee-103">Zahrnovat fyzickou hodnotu</span><span class="sxs-lookup"><span data-stu-id="693ee-103">Include physical value</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="693ee-104">Pole Zahrnout fyzickou hodnotu na pevné záložce Skladový model na stránce Skupiny modelů položky se používá k určení toho, zda se fyzicky aktualizované transakce promítnou do výpočtu průběžných průměrných nákladových ceny položky.</span><span class="sxs-lookup"><span data-stu-id="693ee-104">You use the Include physical value check box on the Inventory model FastTab of the Item model groups page to specify whether physically updated transactions are considered when the running average cost price is calculated for an item.</span></span>

<span data-ttu-id="693ee-105">Zaškrtávací pole **Zahrnovat fyzickou hodnotu** má následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="693ee-105">The **Include physical value** check box has the following values.</span></span>

| <span data-ttu-id="693ee-106">Hodnota</span><span class="sxs-lookup"><span data-stu-id="693ee-106">Value</span></span>    | <span data-ttu-id="693ee-107">Výsledek</span><span class="sxs-lookup"><span data-stu-id="693ee-107">Result</span></span>                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="693ee-108">Vybrané</span><span class="sxs-lookup"><span data-stu-id="693ee-108">Selected</span></span> | <span data-ttu-id="693ee-109">Při výpočtu průběžné průměrné nákladové ceny jsou použity fyzicky i finančně aktualizované transakce.</span><span class="sxs-lookup"><span data-stu-id="693ee-109">Both physically updated transactions and financially updated transactions are used to calculate the running average cost price.</span></span> |
| <span data-ttu-id="693ee-110">Proplaceno</span><span class="sxs-lookup"><span data-stu-id="693ee-110">Cleared</span></span>  | <span data-ttu-id="693ee-111">Pouze finančně aktualizované transakce jsou použity pro výpočet průběžné průměrné nákladové ceny.</span><span class="sxs-lookup"><span data-stu-id="693ee-111">Only financially updated transactions are used to calculate the running average cost price.</span></span>                                     |

<span data-ttu-id="693ee-112">Toto políčko má účinky, které se liší v závislosti na skladovém modelu, který používáte.</span><span class="sxs-lookup"><span data-stu-id="693ee-112">The check box has slightly different effects, depending on the inventory model that you use.</span></span>

-   <span data-ttu-id="693ee-113">Označíte-li pole **Zahrnout fyzickou hodnotu** při použití metody FIFO, LIFO nebo skladového modelu s datem LIFO, uzávěrka skladu provede také úpravy u fyzicky aktualizovaných transakcí.</span><span class="sxs-lookup"><span data-stu-id="693ee-113">If you select the **Include physical value** check box when you use the FIFO (First in, first out), LIFO (Last in, first out), or LIFO date inventory model, inventory close also makes adjustments to physically updated transactions.</span></span>
-   <span data-ttu-id="693ee-114">Pokud jste pro tyto skladové modely neoznačili políčko **Zahrnovat fyzickou hodnotu**, budou při uzávěrce skladu provedena vyrovnání pouze pro finančně aktualizované transakce.</span><span class="sxs-lookup"><span data-stu-id="693ee-114">If you don't select the **Include physical value** check box when you use these inventory models, inventory close makes settlements only to financially updated transactions.</span></span>
-   <span data-ttu-id="693ee-115">Pokud použijete skladové modely s použitím váženého průměru nebo data váženého průměru, budou při uzávěrce skladu vyrovnány pouze finančně aktualizované transakce, bez ohledu na to, zda je zaškrtnuto políčko **Zahrnovat fyzickou hodnotu**, či nikoli.</span><span class="sxs-lookup"><span data-stu-id="693ee-115">When you use the weighted average or weighted average date inventory model, inventory close settles only financially updated transactions, regardless of whether you select the **Include physical value** check box.</span></span>

<span data-ttu-id="693ee-116">**Příklad 1:** Označíte pole**Zahrnovat fyzickou hodnotu** a obdržíte následující nákupní objednávky:</span><span class="sxs-lookup"><span data-stu-id="693ee-116">**Example 1** You've selected the **Include physical value** check box and receive the following purchase orders:</span></span>

-   <span data-ttu-id="693ee-117">Nákupní objednávka na 2 kusy v ceně 10,00 USD byla aktualizována podle dodacího listu</span><span class="sxs-lookup"><span data-stu-id="693ee-117">A purchase order for a quantity of 2 and a cost price of USD 10.00 that has been packing slip–updated</span></span>
-   <span data-ttu-id="693ee-118">Nákupní objednávka na 3 kusy v ceně 12,00 USD byla aktualizována podle faktury</span><span class="sxs-lookup"><span data-stu-id="693ee-118">A purchase order for a quantity of 3 and a cost price of USD 12.00 that has been invoice-updated</span></span>

<span data-ttu-id="693ee-119">V tomto případě bude průběžná průměrná nákladová cena 11,20 USD, protože při výpočtu nákladové ceny jsou použity fyzicky i finančně aktualizované transakce.</span><span class="sxs-lookup"><span data-stu-id="693ee-119">In this case, the running average cost price will be USD 11.20, because both physically updated transactions and financially updated transactions are used to calculate the cost price.</span></span> <span data-ttu-id="693ee-120">**Příklad 2:** Neoznačíte pole **Zahrnovat fyzickou hodnotu** a nákladová cena v rámci konfigurace položky je 10,00 USD.</span><span class="sxs-lookup"><span data-stu-id="693ee-120">**Example 2** You haven't selected the **Include physical value** check box, and the cost price on the item setup is USD 10.00.</span></span> <span data-ttu-id="693ee-121">Obdržíte nákupní objednávku na 20 kusů v ceně 12,00 USD, která byla aktualizována podle dodacího listu.</span><span class="sxs-lookup"><span data-stu-id="693ee-121">You receive a purchase order for a quantity of 20 and a cost price of USD 12.00 that has been packing slip–updated.</span></span> <span data-ttu-id="693ee-122">Při zaúčtování prodejní objednávky se zaúčtuje částka nákladů 10,00 USD, protože průběžná průměrná nákladová cena nebude zahrnovat fyzicky zaúčtované transakce.</span><span class="sxs-lookup"><span data-stu-id="693ee-122">When a sales order is posted, the posted cost amount is USD 10.00, because the running average cost price won't include physically posted transactions.</span></span> <span data-ttu-id="693ee-123">**Poznámka:** Pokud pro porovnání označíte pole **Zahrnovat fyzickou hodnotu** pro toto zboží při zaúčtování prodejní objednávky, zaúčtované náklady budou 12,00 USD.</span><span class="sxs-lookup"><span data-stu-id="693ee-123">**Note:** For comparison, if you select the **Include physical value** check box for this item, when a sales order is posted, the posted cost amount will be USD 12.00.</span></span>




