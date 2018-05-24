---
title: "Zaúčtování deník doručení u vrácených produktů"
description: "Zaúčtování deník doručení u vrácených produktů"
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSArrivalOverview
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: cbe60846f0a16b5061349d9960c49bb5310bd6f9
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---


# <a name="post-arrival-journal-for-returned-products"></a><span data-ttu-id="a969a-103">Zaúčtování deník doručení u vrácených produktů</span><span class="sxs-lookup"><span data-stu-id="a969a-103">Post arrival journal for returned products</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a969a-104">Chcete-li zpracovat vrácení, nejprve ověřte vracené množství, aktualizujte pole množství v deníku doručení zboží.</span><span class="sxs-lookup"><span data-stu-id="a969a-104">To process a return, first validate the return quantity, update the quantity field in the item arrival journal.</span></span> <span data-ttu-id="a969a-105">Vyberte kód dispozice nebo označte, že vrácené zboží musí být prohlédnuto.</span><span class="sxs-lookup"><span data-stu-id="a969a-105">Then select a disposition code or indicate that the returned items have to be inspected.</span></span> <span data-ttu-id="a969a-106">Po provedení těchto kroků můžete pro vratku zaúčtovat deník doručení položek.</span><span class="sxs-lookup"><span data-stu-id="a969a-106">After completing these steps, you can post the item arrival journal for the return order.</span></span>

1.  <span data-ttu-id="a969a-107">Klikněte na **Řízení skladů** \> **Pravidelné** \> **Přehled příjezdů**.</span><span class="sxs-lookup"><span data-stu-id="a969a-107">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="a969a-108">Ve filtru **Název nastavení** vyberte **vratka**.</span><span class="sxs-lookup"><span data-stu-id="a969a-108">In the **Setup name** filter, select **Return order**.</span></span>

3.  <span data-ttu-id="a969a-109">Je-li seznam příjmů příliš dlouhý, můžete jej omezit pomocí polí v oblasti **Rozsah**.</span><span class="sxs-lookup"><span data-stu-id="a969a-109">If the list of receipts is long, use the fields in the **Range** area to narrow the list.</span></span>

4.  <span data-ttu-id="a969a-110">Vyhledejte řádek vratky, který chcete zaúčtovat, zaškrtněte u něj políčko **Vybrat pro doručení** a poté klepněte na položku **Zahájit doručení**.</span><span class="sxs-lookup"><span data-stu-id="a969a-110">Locate the line of the return order that you want to post, select its **Select for arrival** box, and then click **Start arrival**.</span></span>

5.  <span data-ttu-id="a969a-111">Klepněte na tlačítko **deníky** \> **Zobrazit doručení z příjemek** k otevření formuláře **deník skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="a969a-111">Click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="a969a-112">Chcete-li zobrazit podrobné informace, vyberte deník a poté klepněte na položku <STRONG>Řádky</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a969a-112">To view detailed information, select a journal, and then click <STRONG>Lines</STRONG>.</span></span></P>


6.  <span data-ttu-id="a969a-113">Proveďte nutné aktualizace a poté klepněte na položku **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="a969a-113">Make any necessary updates, and then click **Post**.</span></span>

<span data-ttu-id="a969a-114">Po zaúčtování deníku budou vrácené položky registrovány na skladě a ve formuláři **Vratky** bude uvedeno, že byly dodány položky na sklad.</span><span class="sxs-lookup"><span data-stu-id="a969a-114">After the journal is posted, the returned items are registered in inventory, and the **Return orders** form indicates that the items have arrived at the warehouse.</span></span>

## <a name="see-also"></a><span data-ttu-id="a969a-115">Viz také</span><span class="sxs-lookup"><span data-stu-id="a969a-115">See also</span></span>

<span data-ttu-id="a969a-116">[Deník skl. míst (formulář)](https://technet.microsoft.com/en-us/library/aa584822\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="a969a-116">[Location journal (form)](https://technet.microsoft.com/en-us/library/aa584822\(v=ax.60\))</span></span>

  



