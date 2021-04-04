---
title: Vytvoření položky nabídky na mobilním zařízení pro konsolidaci registračních značek
description: Tato procedura ukazuje, jak vytvořit položku nabídky mobilního zařízení pro práci s konsolidací registračních značek.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54457261d4f80648050845f309bcbbcc16caa629
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239007"
---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="49956-103">Vytvoření položky nabídky na mobilním zařízení pro konsolidaci registračních značek</span><span class="sxs-lookup"><span data-stu-id="49956-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="49956-104">Tato procedura ukazuje, jak vytvořit položku nabídky mobilního zařízení pro práci s konsolidací registračních značek.</span><span class="sxs-lookup"><span data-stu-id="49956-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="49956-105">To umožňuje pracovníkům skladu konsolidovat položky na jednom licenčním štítku s položkami na jiném licenčním štítku ve stejném umístění.</span><span class="sxs-lookup"><span data-stu-id="49956-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="49956-106">Mohou je použít například v případě, že následující pracovní kroky byly stejné u obou pracovních příkazů, takže je práci potřeba provést jednou pro sloučené položky.</span><span class="sxs-lookup"><span data-stu-id="49956-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="49956-107">Tento postup můžete projít v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="49956-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="49956-108">Tento úkol obvykle provádí vedoucí skladu.</span><span class="sxs-lookup"><span data-stu-id="49956-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="49956-109">Tento postup je určen pro funkci, která byla přidána do Dynamics 365 for Operations, verze 1611.</span><span class="sxs-lookup"><span data-stu-id="49956-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="49956-110">Přejděte do nabídky Řízení skladu > Nastavení > Mobilní zařízení > Položky nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="49956-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="49956-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="49956-111">Click New.</span></span>
3. <span data-ttu-id="49956-112">Do pole Položky nabídky mobilního zařízení zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="49956-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="49956-113">Zadejte hodnotu do pole Titul.</span><span class="sxs-lookup"><span data-stu-id="49956-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="49956-114">V poli Režim vyberte „Nepřímý“.</span><span class="sxs-lookup"><span data-stu-id="49956-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="49956-115">V poli Kód aktivity vyberte "Konsolidovat registrační značky".</span><span class="sxs-lookup"><span data-stu-id="49956-115">In the Activity code field, select 'Consolidate license plates'.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]