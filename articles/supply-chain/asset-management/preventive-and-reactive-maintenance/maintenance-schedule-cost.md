---
title: Náklady rozvrhu údržby
description: Toto téma popisuje náklady rozvrhu údržby v modulu Správa majetku.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 405fd7fbbbb8862446d09b9ea33ef14348e691f9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813766"
---
# <a name="maintenance-schedule-cost"></a><span data-ttu-id="fe5d9-103">Náklady rozvrhu údržby</span><span class="sxs-lookup"><span data-stu-id="fe5d9-103">Maintenance schedule cost</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="fe5d9-104">V modulu Správa majetku lze vypočítat rozpočtové náklady na řádcích rozvrhu údržby.</span><span class="sxs-lookup"><span data-stu-id="fe5d9-104">In Asset Management, you can calculate budget costs on maintenance schedule lines.</span></span> <span data-ttu-id="fe5d9-105">To je užitečné v případě, že chcete získat přehled o očekávaných nákladech, například nákladech na plánované preventivní práce údržby pro další rok.</span><span class="sxs-lookup"><span data-stu-id="fe5d9-105">This is useful if you want to get an overview of expected costs, for example, costs relating to planned preventive maintenance jobs for the next year.</span></span> <span data-ttu-id="fe5d9-106">Výpočty jsou založeny na stávajících řádcích rozvrhu údržby typu „Plány údržby“ a „Pořadí údržby“ a „Požadavky na údržbu“.</span><span class="sxs-lookup"><span data-stu-id="fe5d9-106">The calculations are based on existing maintenance schedule lines of type "Maintenance plans" and "Maintenance rounds" and "Maintenance requests".</span></span>

1. <span data-ttu-id="fe5d9-107">Klinkěte na položky **Správa majetku** > **Dotazy** > **Majetek** > **Náklady rozvrhu údržby**.</span><span class="sxs-lookup"><span data-stu-id="fe5d9-107">Click **Asset management** > **Inquiries** > **Assets** > **Maintenance schedule cost**.</span></span>

2. <span data-ttu-id="fe5d9-108">V dialogovém okně **Náklady rozvrhu údržby** můžete vybrat **sadu finančních dimenzí**, pokud chcete zobrazit náklady seskupené ve finančních dimenzích.</span><span class="sxs-lookup"><span data-stu-id="fe5d9-108">In the **Maintenance schedule cost** dialog, you can select a **Financial dimension set** if you want to see costs grouped in financial dimensions.</span></span>

>[!NOTE]
><span data-ttu-id="fe5d9-109">Sady finančních dimenzí se nastavují v části **Hlavní kniha** > **Účtová osnova** > **Dimenze** > **Sady finančních dimenzí**.</span><span class="sxs-lookup"><span data-stu-id="fe5d9-109">Financial dimension sets are set up in **General ledger** > **Chart of accounts** > **Dimensions** > **Financial dimension sets**.</span></span>

3. <span data-ttu-id="fe5d9-110">V poli **Úroveň** určete, jak detailní mají být řádky rozvrhu údržby v případě funkčních míst.</span><span class="sxs-lookup"><span data-stu-id="fe5d9-110">You can use the **Level** field to indicate how detailed you want the maintenance schedule lines to be regarding functional locations.</span></span> <span data-ttu-id="fe5d9-111">Pokud například do pole zadáte číslo „1“ a máte strukturu funkčních míst o více úrovních, budou na nejvyšší úrovni zobrazeny všechny řádky rozvrhu údržby pro funkční místo, a proto lze hodiny na řádku navýšit z funkčních míst na nižší úrovni.</span><span class="sxs-lookup"><span data-stu-id="fe5d9-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="fe5d9-112">Pokud do pole **Úroveň** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechny řádky rozvrhu údržby na všech úrovních funkčních míst, ke kterým se vztahují.</span><span class="sxs-lookup"><span data-stu-id="fe5d9-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="fe5d9-113">Chcete-li provést výpočet pro určitý majetek, klikněte na položku **Filtr** na záložce s náhledem **Záznamy k zahrnutí** a vyberte příslušný majetek.</span><span class="sxs-lookup"><span data-stu-id="fe5d9-113">If you want to make a calculation for specific assets, click **Filter** on the **Records to include** FastTab, and select the relevant assets.</span></span> <span data-ttu-id="fe5d9-114">Je-li to nutné, můžete také datum **Očekávané zahájení** pro výpočet nákladů nebo vybrat jiný **Stav** pro výpočet nákladů.</span><span class="sxs-lookup"><span data-stu-id="fe5d9-114">If required, you can also specify an **Expected start** date for the cost calculation or select a different **Status** for the cost calculation</span></span>

5. <span data-ttu-id="fe5d9-115">Výpočet nákladů zahájíte klepnutím na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe5d9-115">Click **OK** to start the cost calculation.</span></span>

6. <span data-ttu-id="fe5d9-116">Na kartě **Náklady rozvrhu údržby** ve skupinách podokna akce **Seskupit podle...** vyberte odpovídající tlačítka pro zobrazení požadované úrovně podrobností výpočtu nákladů.</span><span class="sxs-lookup"><span data-stu-id="fe5d9-116">On the **Maintenance schedule cost** tab > in the **Group by...** Action Pane groups, click the relevant buttons to show the required detail level of the cost calculation.</span></span> <span data-ttu-id="fe5d9-117">Vybraná tlačítka skupiny podokna akcí jsou zvýrazněna.</span><span class="sxs-lookup"><span data-stu-id="fe5d9-117">The selected Action Pane group buttons are highlighted.</span></span> <span data-ttu-id="fe5d9-118">Kliknutím na tlačítko jej aktivujte nebo deaktivujte.</span><span class="sxs-lookup"><span data-stu-id="fe5d9-118">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="fe5d9-119">Chcete-li provést nový výpočet nákladů, klikněte na tlačítko **Vypočítat náklady**.</span><span class="sxs-lookup"><span data-stu-id="fe5d9-119">Click the **Calculate cost** button if you want to make a new cost calculation.</span></span>

<span data-ttu-id="fe5d9-120">Na následujícím obrázku jsou uvedeny výsledky výpočtu nákladů rozvrhu údržby.</span><span class="sxs-lookup"><span data-stu-id="fe5d9-120">The illustration below shows the results of a maintenance schedule cost calculation.</span></span>

![Obrázek č. 1](media/17-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]