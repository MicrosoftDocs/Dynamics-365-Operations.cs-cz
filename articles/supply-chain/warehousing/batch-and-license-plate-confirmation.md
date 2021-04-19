---
title: Potvrzení dávky a poznávací značky
description: Toto téma popisuje, jak nastavit a použít potvrzení dávky a registrační značky z mobilního zařízení.
author: Mirzaab
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c588e6ed11d275b75133e2824f3d385048050426
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837530"
---
# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="c0093-103">Potvrzení dávky a poznávací značky</span><span class="sxs-lookup"><span data-stu-id="c0093-103">Batch and license plate confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0093-104">Potvrzení dávky vám umožňuje potvrdit z mobilního zařízení, že byla vydána správná dávka.</span><span class="sxs-lookup"><span data-stu-id="c0093-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="c0093-105">Při počátečním vyskladnění práce pouze pro položky *Batch-above\[location\]*, kde batch-above označuje že dávka je umístěna výše než umístění v hierarchii vyhledávání, musíte ověřit, že vyskladněná dávka se shoduje dávkou na řádku práce.</span><span class="sxs-lookup"><span data-stu-id="c0093-105">On the initial pick of work for *Batch-above\[location\]* items only, where batch-above indicates that batch is placed higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span>

<span data-ttu-id="c0093-106">Potvrzení registrační značky vám umožňuje potvrdit z mobilního zařízení, že byla vydána správná registrační značka.</span><span class="sxs-lookup"><span data-stu-id="c0093-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="c0093-107">Při vyskladnění práce ze skladového místa fáze musíte ověřit, že vyskladněná registrační značka odpovídá registrační značce, která je přidružena k práci.</span><span class="sxs-lookup"><span data-stu-id="c0093-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="c0093-108">Pokud práce začala naskenováním poznávací značky, tento krok potvrzení bude přeskočen.</span><span class="sxs-lookup"><span data-stu-id="c0093-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="c0093-109">Kdy se to používá</span><span class="sxs-lookup"><span data-stu-id="c0093-109">Where it applies</span></span>

<span data-ttu-id="c0093-110">Potvrzení platí v následujících situacích:</span><span class="sxs-lookup"><span data-stu-id="c0093-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="c0093-111">Potvrzení dávky se týká počátečního vyskladnění práce pro dávku nad položky.</span><span class="sxs-lookup"><span data-stu-id="c0093-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="c0093-112">Potvrzení poznávací značky platí pro vyskladnění ze skladových míst fáze.</span><span class="sxs-lookup"><span data-stu-id="c0093-112">License plate confirmation applies to picks from stage locations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c0093-113">U potvrzení registrační značky není doplňování podporováno.</span><span class="sxs-lookup"><span data-stu-id="c0093-113">Replenishment is not supported for license plate confirmation.</span></span> <span data-ttu-id="c0093-114">Při provádění doplňovacích prací není vytvořen žádný krok potvrzení registrační značky.</span><span class="sxs-lookup"><span data-stu-id="c0093-114">When executing replenishment work, no license plate confirmation step is created.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="c0093-115">Nastavení potvrzení dávky a poznávací značky</span><span class="sxs-lookup"><span data-stu-id="c0093-115">Set up batch and license plate confirmation</span></span>

<span data-ttu-id="c0093-116">Můžete nakonfigurovat potvrzení dávky a poznávací značky z položek nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="c0093-116">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>

1. <span data-ttu-id="c0093-117">Z položek nabídky mobilního zařízení vstupte do nastavení potvrzení práce.</span><span class="sxs-lookup"><span data-stu-id="c0093-117">From the mobile device menu items, enter the work confirmation setup.</span></span>  
1. <span data-ttu-id="c0093-118">Vyberte možnost pro potvrzení dávky nebo registrační značky.</span><span class="sxs-lookup"><span data-stu-id="c0093-118">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="c0093-119">Obě možnosti jsou k dispozici pro vyskladnění typu práce, které nemají povolené automatické potvrzení.</span><span class="sxs-lookup"><span data-stu-id="c0093-119">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
