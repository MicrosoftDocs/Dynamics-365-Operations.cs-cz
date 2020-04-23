---
title: Výpočet vytížení kapacity na plánovaných pracovních příkazech
description: Toto téma vysvětluje, jak vypočítat vytížení kapacity na plánovaných pracovních příkazech v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b817909ac0950b773cba775be2502b5796c6d8d6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215348"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a><span data-ttu-id="7fa06-103">Výpočet vytížení kapacity na plánovaných pracovních příkazech</span><span class="sxs-lookup"><span data-stu-id="7fa06-103">Calculate capacity load on scheduled work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="7fa06-104">Chcete-li získat přehled o vytížení práce zdrojů pro určité období, můžete vypočítat vytížení kapacity na plánovaných pracovních příkazech.</span><span class="sxs-lookup"><span data-stu-id="7fa06-104">You can calculate capacity load on scheduled work orders to get an overview of the work load on resources for a specific period.</span></span> <span data-ttu-id="7fa06-105">Výpočty lze provádět u následujících zdrojů: pracovníci údržby, skupiny pracovníků, nástroje a majetek.</span><span class="sxs-lookup"><span data-stu-id="7fa06-105">Calculations can be made for the following resources: Maintenance workers, worker groups, tools, and assets.</span></span>

1. <span data-ttu-id="7fa06-106">Klikněte na **Správa majeku** > **Dotazy** > **Plán** > **Vytížení kapacity**.</span><span class="sxs-lookup"><span data-stu-id="7fa06-106">Click **Asset management** > **Inquiries** > **Schedule** > **Capacity load**.</span></span>

2. <span data-ttu-id="7fa06-107">V dialogovém okně **Vypočítat vytížení kapacity** > pole **Zobrazit** vyberte typ vytížení, který chcete vypočítat: **Kapacita**, **Rezervované** nebo **Zůstatek**.</span><span class="sxs-lookup"><span data-stu-id="7fa06-107">In the **Calculate capacity load** dialog > **Show** field, select which load type you want to calculate: **Capacity**, **Reserved**, or **Remainder**.</span></span>

3. <span data-ttu-id="7fa06-108">Nechcete-li zobrazit výsledky obsahující nulu, vyberte možnost **Ano** na přepínacím tlačítku **Přeskočit nulu**.</span><span class="sxs-lookup"><span data-stu-id="7fa06-108">Select **Yes** on the **Skip zero** toggle button if you do not want to show results containing zero.</span></span>

4. <span data-ttu-id="7fa06-109">Vyberte typy zdroje, pro které chcete vypočítat vytížení kapacity volbou **Ano** na příslušném přepínači: **Pracovník**, **Skupina pracovníků údržby**, **Nástroj** a **Majetek**.</span><span class="sxs-lookup"><span data-stu-id="7fa06-109">Select the resource types for which you want to calculate capacity load by selecting **Yes** on the relevant toggle buttons: **Worker**, **Maintenance worker group**, **Tool**, and **Asset**.</span></span>

5. <span data-ttu-id="7fa06-110">V poli **Od data** vyberte počáteční datum výpočtu.</span><span class="sxs-lookup"><span data-stu-id="7fa06-110">Select the start date for the calculation in the **From date** field.</span></span>

6. <span data-ttu-id="7fa06-111">V poli **Typ intervalu** vyberte interval pro výpočet: **Den**, **Týden**, **Měsíc** nebo **Čtvrtletí**.</span><span class="sxs-lookup"><span data-stu-id="7fa06-111">In the **Interval type** field, select the interval for the calculation: **Day**, **Week**, **Month**, or **Quarter**.</span></span>

7. <span data-ttu-id="7fa06-112">V poli **Frekvence období** zadejte počet intervalů, které chcete vypočítat.</span><span class="sxs-lookup"><span data-stu-id="7fa06-112">In the **Period frequency** field, insert the number of intervals you want to calculate.</span></span> <span data-ttu-id="7fa06-113">Pokud jste například jako typ intervalu vybrali možnost **den** a do pole zadáte číslo "5", bude proveden výpočet pěti dnů od počátečního data.</span><span class="sxs-lookup"><span data-stu-id="7fa06-113">For example, if you have selected **Day** as the interval type, and you enter the number "5" in this field, a calculation of five days from the start date will be made.</span></span>

8. <span data-ttu-id="7fa06-114">Výpočet zahájíte klepnutím na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fa06-114">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="7fa06-115">Níže uvedený údaj ukazuje výsledek výpočtu, který pokrývá tři týdny pro typ vytížení **Rezervováno**.</span><span class="sxs-lookup"><span data-stu-id="7fa06-115">The figure below shows the result of a calculation covering three weeks for the load type **Reserved**.</span></span>

![Obrázek č. 1](media/08-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="7fa06-117">Pokud pro výpočet vyberete typ vytížení **Kapacita** nebo **Zůstatek**, zobrazí se stejný výsledek v případě, že pro zdroje ve vybraném období nebyly provedeny žádné rezervace.</span><span class="sxs-lookup"><span data-stu-id="7fa06-117">If you select the load types **Capacity** or **Remainder** for your calculation, the same result will be displayed if no reservations have been made for the resources in the selected period.</span></span>

<span data-ttu-id="7fa06-118">Informace o způsobu výpočtu vytížení kapacity na řádcích plánu údržby a neplánovaných pracovních příkazech naleznete v tématu [Výpočet vytížení kapacity](../capacity-planning/calculate-capacity-load.md).</span><span class="sxs-lookup"><span data-stu-id="7fa06-118">For information about how to calculate capacity load on maintenance schedule lines and not scheduled work orders, refer to [Calculate capacity load](../capacity-planning/calculate-capacity-load.md).</span></span>

