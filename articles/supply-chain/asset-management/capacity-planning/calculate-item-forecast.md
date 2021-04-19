---
title: Vypočítat prognózu položky
description: Toto téma vysvětluje, jak vypočítat prognózu položky v modulu Správa majetku.
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9392245abe5858b03b8324dcb471f5652aed7cd6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813886"
---
# <a name="calculate-item-forecast"></a><span data-ttu-id="6e9ee-103">Vypočítat prognózu položky</span><span class="sxs-lookup"><span data-stu-id="6e9ee-103">Calculate item forecast</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6e9ee-104">Stejně jako lze provádět výpočty vytížení kapacity, které jsou popsány v předchozím oddílu, můžete také provádět výpočty prognózy položek na:</span><span class="sxs-lookup"><span data-stu-id="6e9ee-104">Just as you can make capacity load calculations, which are described in the previous section, you can also make item forecast calculations on:</span></span>

- <span data-ttu-id="6e9ee-105">řádcích rozvrhu údržby</span><span class="sxs-lookup"><span data-stu-id="6e9ee-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="6e9ee-106">pracovních příkazech, které ještě nebyly naplánovány</span><span class="sxs-lookup"><span data-stu-id="6e9ee-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="6e9ee-107">naplánovaných pracovních příkazech</span><span class="sxs-lookup"><span data-stu-id="6e9ee-107">scheduled work orders</span></span>

<span data-ttu-id="6e9ee-108">To je užitečné v případě, že chcete získat přehled o očekávané spotřebě položek (náhradní díly a další položky vyžadované pro dokončení pracovních příkazů) za určité období.</span><span class="sxs-lookup"><span data-stu-id="6e9ee-108">This is useful if you want to get an overview of expected item consumption (spare parts as well as other items required for completing work orders) for a specific period.</span></span> <span data-ttu-id="6e9ee-109">Výpočet prognózy položek lze provést u veškerého majetku nebo vybraného majetku.</span><span class="sxs-lookup"><span data-stu-id="6e9ee-109">Calculation of item forecast can be done on all assets or selected assets.</span></span> <span data-ttu-id="6e9ee-110">Můžete také provést výpočet v aktivitě prostoje údržby (**Všechny aktivity prostoje údržby** nebo **Aktivní aktivity prostojů údržby**) nebo ve skupině pracovních příkazů (**Všechny skupiny pracovních příkazů** nebo **Aktivní skupiny pracovních příkazů**).</span><span class="sxs-lookup"><span data-stu-id="6e9ee-110">You can also make a calculation on a maintenance downtime activity (**All maintenance downtime activities** or **Active maintenance downtime activities**), or on a work order pool (**All work order pools** or **Active work order pools**).</span></span>

1. <span data-ttu-id="6e9ee-111">Klikněte na **Správa majetku** > **Dotazy** > **Prognóza položkyy**, nebo **Správa majetku** > **Společné** > **Skupiny pracovních příkazů** > **Všechny skupiny pracovních příkazů** / **Aktivní skupiny pracovních příkazů** > zvolte skupinu pracovních příkazů v seznamu > tlačítko **Prognóza položky**, nebo **Správa majetku** > **Společné** > **Aktivity prostojů údržby** > **Všechny Aktivity prostojů údržby** / **Aktivní Aktivity prostojů údržby** > zvolte aktivitu prostoje údržby v seznamu > tlačítko **Prognóza položky**.</span><span class="sxs-lookup"><span data-stu-id="6e9ee-111">Click **Asset management** > **Inquiries** > **Item forecast**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Item forecast** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance downtime activity in the list > **Item forecast** button.</span></span>

2. <span data-ttu-id="6e9ee-112">V dialogovém okně **Vypočítat prognóza položky** vyberte období pro výpočet v polích **Počáteční datum/čas** a **Koncové datum a čas**.</span><span class="sxs-lookup"><span data-stu-id="6e9ee-112">In the **Calculate item forecast** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="6e9ee-113">Chcete-li do výpočtu prognózy zahrnout řádky rozvrhu údržby, vyberte Ano na přepínači **Zahrnout rozvrh údržby**.</span><span class="sxs-lookup"><span data-stu-id="6e9ee-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the forecast calculation.</span></span>

4. <span data-ttu-id="6e9ee-114">Chcete-li do výpočtu prognózy zahrnout práce pracovního příkazu, vyberte Ano na přepínači **Zahrnout pracovní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="6e9ee-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the forecast calculation.</span></span>

5. <span data-ttu-id="6e9ee-115">V poli **Úroveň** určete, jak detailní mají být řádky prognózy položky v případě funkčních míst.</span><span class="sxs-lookup"><span data-stu-id="6e9ee-115">You can use the **Level** field to indicate how detailed you want the item forecast lines to be regarding functional locations.</span></span> 

      <span data-ttu-id="6e9ee-116">Pokud například do pole zadáte číslo „1“ a máte strukturu funkčních míst o více úrovních, budou na nejvyšší úrovni zobrazeny všechny řádky rozvrhu údržby a pracovní příkazy pro funkční místo, a proto lze hodiny na řádku navýšit z funkčních míst na nižší úrovni.</span><span class="sxs-lookup"><span data-stu-id="6e9ee-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
  
      <span data-ttu-id="6e9ee-117">Pokud do pole **Úroveň** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechny řádky rozvrhu údržby a všechny pracovní příkazy na všech úrovních funkčních míst, ke kterým se vztahují.</span><span class="sxs-lookup"><span data-stu-id="6e9ee-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="6e9ee-118">Výpočet zahájíte klepnutím na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e9ee-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="6e9ee-119">Ve skupině **Seskupit podle...** klikněte na odpovídající tlačítka pro zobrazení požadované úrovně podrobností výpočtu.</span><span class="sxs-lookup"><span data-stu-id="6e9ee-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="6e9ee-120">Na snímku obrazovky níže jsou vybraná tlačítka **Seskupit podle** označena modře.</span><span class="sxs-lookup"><span data-stu-id="6e9ee-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="6e9ee-121">Kliknutím na tlačítko jej aktivujte nebo deaktivujte.</span><span class="sxs-lookup"><span data-stu-id="6e9ee-121">Click on a button to activate or deactivate it.</span></span>

8. <span data-ttu-id="6e9ee-122">Chcete-li zobrazit produkt, sklad nebo sledovací dimenze související s položkami, klikněte na tlačítko **Zobrazit dimenze**.</span><span class="sxs-lookup"><span data-stu-id="6e9ee-122">Click the **Display dimensions** button if you want to see the product, storage, or tracking dimensions related to the items.</span></span> <span data-ttu-id="6e9ee-123">Zvolte příslušná zaškrtávací políčka a klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e9ee-123">Select the relevant check boxes, and click **OK**.</span></span>

![Obrázek č. 1](media/02-capacity-planning.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]