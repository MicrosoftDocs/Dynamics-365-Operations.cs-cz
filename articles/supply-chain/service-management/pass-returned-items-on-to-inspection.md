---
title: Postoupení vrácených položek ke kontrole
description: Při registraci vrácené položky určete, že má být položka před vrácením do zásob nebo vyřazením jinou formou odeslána ke kontrole.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7207c54a88b8a7fc6c38db50c4916d1fc16b5ec4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006663"
---
# <a name="pass-returned-items-on-to-inspection"></a><span data-ttu-id="39515-103">Postoupení vrácených položek ke kontrole</span><span class="sxs-lookup"><span data-stu-id="39515-103">Pass returned items on to inspection</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="39515-104">Při registraci vrácené položky můžete určit, že má být položka před vrácením do zásob nebo vyřazením jinou formou odeslána ke kontrole.</span><span class="sxs-lookup"><span data-stu-id="39515-104">When registering a returned item, you may determine that an item should be sent for inspection before it is returned to inventory or disposed of in some other way.</span></span>

1.  <span data-ttu-id="39515-105">Klikněte na **Řízení zásob** \> **Deníky** \> **Doručení položky** \> **Doručení položky**.</span><span class="sxs-lookup"><span data-stu-id="39515-105">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>
    
    <span data-ttu-id="39515-106">\-nebo-</span><span class="sxs-lookup"><span data-stu-id="39515-106">\-or-</span></span>
    
    <span data-ttu-id="39515-107">Klikněte na **Řízení zásob** \> **Deníky** \> **Doručení položky** \> **Výstup výroby**.</span><span class="sxs-lookup"><span data-stu-id="39515-107">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Production input**.</span></span>

2.  <span data-ttu-id="39515-108">Zaregistrujte příjem položky běžným postupem ve formuláři **Deník skl. míst**.</span><span class="sxs-lookup"><span data-stu-id="39515-108">On the **Location journal** form, register the receipt of an item as usual.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="39515-109">Další informace o registraci příjmu vrácených položek naleznete v tématu <A href="register-the-receipt-of-returned-items.md">Registrace příjmu vrácených položek</A></span><span class="sxs-lookup"><span data-stu-id="39515-109">For information about registering the receipt of returned items, see <A href="register-the-receipt-of-returned-items.md">Register the receipt of returned items</A></span></span></P>



3.  <span data-ttu-id="39515-110">Na kartě **výchozí hodnoty** v oblasti **režim zpracování** zaškrtněte políčko **řízení karantény**.</span><span class="sxs-lookup"><span data-stu-id="39515-110">On the **Default values** tab, in the **Mode of handling** area, select the **Quarantine management** box.</span></span>

<span data-ttu-id="39515-111">Tím systém vyzvete k vytvoření karanténního příkazu a osoba nebo oddělení provádějící kontroly na tento příkaz odpoví pomocí formuláře **Karanténní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="39515-111">This will prompt the system to create a quarantine order, and the person or department that performs inspections will respond to this order using the **Quarantine order** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="39515-112">Viz také</span><span class="sxs-lookup"><span data-stu-id="39515-112">See also</span></span>

[<span data-ttu-id="39515-113">Podrobení vrácených položek kontrole</span><span class="sxs-lookup"><span data-stu-id="39515-113">Take returned items through inspection</span></span>](take-returned-items-through-inspection.md)

[<span data-ttu-id="39515-114">Určení způsobu nakládání s vrácenými položkami</span><span class="sxs-lookup"><span data-stu-id="39515-114">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

