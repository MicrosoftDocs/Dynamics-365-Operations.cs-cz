---
title: Vypočítat vytížení kapacity
description: Toto téma vysvětluje, jak vypočítat vytížení kapacity v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c6d15861492a46ddb1222db2210f8c751ed38cb3
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886786"
---
# <a name="calculate-capacity-load"></a><span data-ttu-id="89993-103">Vypočítat vytížení kapacity</span><span class="sxs-lookup"><span data-stu-id="89993-103">Calculate capacity load</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="89993-104">Ve správě majetku lze vypočítat vytížení kapacity na</span><span class="sxs-lookup"><span data-stu-id="89993-104">In Asset Management, you can calculate capacity load on</span></span>

- <span data-ttu-id="89993-105">řádcích rozvrhu údržby</span><span class="sxs-lookup"><span data-stu-id="89993-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="89993-106">pracovních příkazech, které ještě nebyly naplánovány</span><span class="sxs-lookup"><span data-stu-id="89993-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="89993-107">naplánovaných pracovních příkazech</span><span class="sxs-lookup"><span data-stu-id="89993-107">scheduled work orders</span></span>

<span data-ttu-id="89993-108">To je užitečné v případě, že chcete získat přehled očekávaného vytížení kapacity pro určité období.</span><span class="sxs-lookup"><span data-stu-id="89993-108">This is useful if you want to get an overview of expected capacity load for a specific period.</span></span> <span data-ttu-id="89993-109">Výpočet vytížení kapacity lze provést u veškerého majetku nebo vybraného majetku.</span><span class="sxs-lookup"><span data-stu-id="89993-109">Calculation of capacity load can be done on all assets or selected assets.</span></span> <span data-ttu-id="89993-110">Můžete také provést výpočet pro aktivity prostojů údržby nebo fondu pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="89993-110">You can also make a calculation on maintenance downtime activities or work order pools.</span></span>

1. <span data-ttu-id="89993-111">Klikněte na **Správa majetku** > **Dotazy** > **Vytížení kapacity**, nebo **Správa majetku** > **Společné** > **Skupiny pracovních příkazů** > **Všechny skupiny pracovních příkazů** / **Aktivní skupiny pracovních příkazů** > zvolte skupinu pracovních příkazů v seznamu > tlačítko **Vytížení kapacity**, nebo **Správa majetku** > **Společné** > **Aktivity prostojů údržby** > **Všechny Aktivity prostojů údržby** / **Aktivní Aktivity prostojů údržby** > zvolte aktivitu údržby v seznamu > tlačítko **Vytížení kapacity**.</span><span class="sxs-lookup"><span data-stu-id="89993-111">Click **Asset management** > **Inquiries** > **Capacity load**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Capacity load** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance activity in the list > **Capacity load** button.</span></span>

2. <span data-ttu-id="89993-112">V dialogovémokně **Vypočítat vytížení kapacity** vyberte období pro výpočet v polích **Počáteční datum/čas** a **Koncové datum a čas**.</span><span class="sxs-lookup"><span data-stu-id="89993-112">In the **Calculate capacity load** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="89993-113">Chcete-li do výpočtu zahrnout řádky rozvrhu údržby, vyberte Ano na přepínači **Zahrnout rozvrh údržby**.</span><span class="sxs-lookup"><span data-stu-id="89993-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the calculation.</span></span>

4. <span data-ttu-id="89993-114">Chcete-li do výpočtu zahrnout práce pracovního příkazu, vyberte Ano na přepínači **Zahrnout pracovní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="89993-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the calculation.</span></span>

5. <span data-ttu-id="89993-115">V poli **Úroveň** určete, jak detailní mají být řádky vytížení kapacity v případě funkčních míst.</span><span class="sxs-lookup"><span data-stu-id="89993-115">You can use the **Level** field to indicate how detailed you want the capacity load lines to be regarding functional locations.</span></span> <span data-ttu-id="89993-116">Pokud například do pole zadáte číslo „1“ a máte strukturu funkčních míst o více úrovních, budou na nejvyšší úrovni zobrazeny všechny řádky rozvrhu údržby a pracovní příkazy pro funkční místo, a proto lze hodiny na řádku navýšit z funkčních míst na nižší úrovni.</span><span class="sxs-lookup"><span data-stu-id="89993-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="89993-117">Pokud do pole **Úroveň** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechny řádky rozvrhu údržby a všechny pracovní příkazy na všech úrovních funkčních míst, ke kterým se vztahují.</span><span class="sxs-lookup"><span data-stu-id="89993-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="89993-118">Výpočet zahájíte klepnutím na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="89993-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="89993-119">Ve skupině podoken akcí **Seskupit podle...** klikněte na odpovídající tlačítka pro zobrazení požadované úrovně podrobností výpočtu.</span><span class="sxs-lookup"><span data-stu-id="89993-119">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="89993-120">Vybraná tlačítka skupiny podokna akcí jsou zvýrazněna modrou barvou.</span><span class="sxs-lookup"><span data-stu-id="89993-120">The selected action pane group buttons are highlighted in blue color.</span></span> <span data-ttu-id="89993-121">Kliknutím na tlačítko jej aktivujte nebo deaktivujte.</span><span class="sxs-lookup"><span data-stu-id="89993-121">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="89993-122">Následující obrázek ukazuje příklad rozhraní.</span><span class="sxs-lookup"><span data-stu-id="89993-122">The figure below shows an example of the interface.</span></span>

![Obrázek č. 1](media/01-capacity-planning.png)

>[!NOTE]
><span data-ttu-id="89993-124">Chcete-li se zaměřit pouze na plánování kapacity týkající se plánovaných pracovních příkazů, nahlédněte do části [Výpočet vytížení kapacity na plánovaných pracovních příkazech](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span><span class="sxs-lookup"><span data-stu-id="89993-124">If you want to focus only on capacity planning regarding scheduled work orders, refer to [Calculate capacity load on scheduled work orders](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span></span>

