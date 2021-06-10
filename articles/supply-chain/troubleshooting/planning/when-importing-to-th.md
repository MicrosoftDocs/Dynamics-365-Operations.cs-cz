---
title: Zobrazí se výzva k uložení nastavení pokrytí položky, i když jste neprovedli žádné změny
description: Zobrazí se výzva k uložení nastavení pokrytí položky, i když jste neprovedli žádné změny.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049456"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a><span data-ttu-id="c41f0-103">Zobrazí se výzva k uložení nastavení pokrytí položky, i když jste neprovedli žádné změny</span><span class="sxs-lookup"><span data-stu-id="c41f0-103">You're prompted to save item coverage settings even though you made no changes</span></span>

<span data-ttu-id="c41f0-104">Číslo článku znalostní báze: 4615588</span><span class="sxs-lookup"><span data-stu-id="c41f0-104">KB number: 4615588</span></span>

## <a name="symptoms"></a><span data-ttu-id="c41f0-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="c41f0-105">Symptoms</span></span>

<span data-ttu-id="c41f0-106">V některých scénářích se může zobrazit následující zpráva po otevření stránky **Pokrytí položky** po importu položek pomocí entity *Pokrytí položky V2*:</span><span class="sxs-lookup"><span data-stu-id="c41f0-106">In some scenarios, you might receive the following message when you open the **Item coverage** page after you import items through the *Item coverage V2* entity:</span></span>

> <span data-ttu-id="c41f0-107">Chcete před zavřením uložit změny?</span><span class="sxs-lookup"><span data-stu-id="c41f0-107">Do you want to save your changes before closing?</span></span>

<span data-ttu-id="c41f0-108">Tuto zprávu obdržíte, i když jste neprovedli žádné změny.</span><span class="sxs-lookup"><span data-stu-id="c41f0-108">You receive this message even though you haven't made any changes.</span></span>

## <a name="resolution"></a><span data-ttu-id="c41f0-109">Řešení</span><span class="sxs-lookup"><span data-stu-id="c41f0-109">Resolution</span></span>

<span data-ttu-id="c41f0-110">Stránka **Pokrytí položky** obsahuje složitou výchozí logiku, která může způsobit, že se zpráva zobrazí poté, co byly v databázi nedávno provedeny přímé změny, například prostřednictvím importu entity.</span><span class="sxs-lookup"><span data-stu-id="c41f0-110">The **Item coverage** page includes complex defaulting logic that might cause the message to be shown after direct changes have recently been made in the database, such as through entity import.</span></span> <span data-ttu-id="c41f0-111">Například pole entity `AREGENERALSETTINGSOVERRIDDEN` je nastaveno na *Ne*, ale importujete soubor, který poskytuje nové nebo upravené hodnoty pro pole, jako je `PRODUCTCOVERAGEGROUPID` a/nebo `VENDORACCOUNTNUMBER`.</span><span class="sxs-lookup"><span data-stu-id="c41f0-111">For example, the `AREGENERALSETTINGSOVERRIDDEN` entity field is set to *No*, but you import a file that provides new or modified values for fields such as `PRODUCTCOVERAGEGROUPID` and/or `VENDORACCOUNTNUMBER`.</span></span> <span data-ttu-id="c41f0-112">V tomto případě, jelikož je pole `AREGENERALSETTINGSOVERRIDDEN` nastaveno na *Ne*, hodnoty se automaticky vymažou z polí, když otevřete stránku **Pokrytí položky** poprvé po importu.</span><span class="sxs-lookup"><span data-stu-id="c41f0-112">In this case, because the `AREGENERALSETTINGSOVERRIDDEN` field is set to *No*, the values are automatically cleared from the fields when you open the **Item coverage** page for the first time after the import.</span></span> <span data-ttu-id="c41f0-113">Pokud změny uložíte podle pokynů v okně se zprávou, uloží se do databáze.</span><span class="sxs-lookup"><span data-stu-id="c41f0-113">If you save the changes as the message box prompts, they are stored in the database.</span></span> <span data-ttu-id="c41f0-114">Jinak obdržíte stejnou zprávu při příštím otevření stránky.</span><span class="sxs-lookup"><span data-stu-id="c41f0-114">Otherwise, you will receive the same message the next time that you open the page.</span></span>

<span data-ttu-id="c41f0-115">Chcete-li zabránit tomuto chování, ale také zahrnout hodnoty pro pole, jako je `PRODUCTCOVERAGEGROUPID` prostřednictvím importu entity, nastavte `AREGENERALSETTINGSOVERRIDDEN` na *Ano* při importu.</span><span class="sxs-lookup"><span data-stu-id="c41f0-115">To prevent this behavior but also include values for fields such as `PRODUCTCOVERAGEGROUPID` through entity import, set `AREGENERALSETTINGSOVERRIDDEN` to *Yes* when you import.</span></span>
