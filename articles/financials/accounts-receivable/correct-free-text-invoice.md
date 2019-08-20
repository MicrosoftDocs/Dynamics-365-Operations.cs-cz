---
title: Oprava faktury s volným textem
description: Tento článek vysvětluje, jak opravit volnou fakturu, která byla zaúčtována, a znovu ji vystavit jako opravenou fakturu.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76cf1f24a31f246a41601908ebba308551925d90
ms.sourcegitcommit: d0fa8d0140fa81029527edb317623c1a7737c593
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863005"
---
# <a name="correct-a-free-text-invoice"></a><span data-ttu-id="c12a1-103">Oprava faktury s volným textem</span><span class="sxs-lookup"><span data-stu-id="c12a1-103">Correct a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c12a1-104">Tento článek vysvětluje, jak opravit volnou fakturu, která byla zaúčtována, a znovu ji vystavit jako opravenou fakturu.</span><span class="sxs-lookup"><span data-stu-id="c12a1-104">This article explains how to correct a free text invoice that has been posted and reissue it as a corrected invoice.</span></span>

<span data-ttu-id="c12a1-105">Pokud chcete upravit volnou fakturu, která již byla zaúčtována, otevřete ji.</span><span class="sxs-lookup"><span data-stu-id="c12a1-105">To correct a free text invoice that has already been posted, open the posted free text invoice.</span></span> <span data-ttu-id="c12a1-106">Na stránce **Faktura** vyberte možnost **Zrušit** a poté vyberte možnost **Správná faktura**.</span><span class="sxs-lookup"><span data-stu-id="c12a1-106">On the **Invoice** page, select **Cancel**, and then select **Correct invoice**.</span></span> <span data-ttu-id="c12a1-107">Vyberte kód důvodu, přidejte poznámky a vyberte datum pro novou, opravenou fakturu.</span><span class="sxs-lookup"><span data-stu-id="c12a1-107">Select a reason code, add comments, and select the date for new corrected invoice.</span></span> <span data-ttu-id="c12a1-108">Můžete upravit opravenou fakturu a zaúčtovat ji.</span><span class="sxs-lookup"><span data-stu-id="c12a1-108">You can modify the corrected invoice, and post it.</span></span> 

<span data-ttu-id="c12a1-109">Po zaúčtování opravené faktury se vytvoří zrušení faktury pro kreditní částku, která se rovná původní částce faktury.</span><span class="sxs-lookup"><span data-stu-id="c12a1-109">When you post the corrected invoice, a canceling invoice is created for a credit amount that equals the original invoice amount.</span></span> <span data-ttu-id="c12a1-110">Kombinovaný zůstatek původní faktury a zrušení faktury je tedy 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="c12a1-110">Therefore, the combined balance of the original invoice and the canceling invoice is 0 (zero).</span></span> <span data-ttu-id="c12a1-111">Zrušení faktury je vyrovnáno oproti původní faktuře.</span><span class="sxs-lookup"><span data-stu-id="c12a1-111">The canceling invoice is settled against the original invoice.</span></span> 

<span data-ttu-id="c12a1-112">Po zaúčtování opravené fakturu budete mít tři faktury:</span><span class="sxs-lookup"><span data-stu-id="c12a1-112">After you post the corrected invoice, you will have three invoices:</span></span>

-   <span data-ttu-id="c12a1-113">**Původní faktura** – Faktura obsahující informace, které opravujete.</span><span class="sxs-lookup"><span data-stu-id="c12a1-113">**Original invoice** – The invoice that includes the information that you're correcting.</span></span>
-   <span data-ttu-id="c12a1-114">**Zrušení faktury** – Systémem vygenerovaná faktura strany Dal, která byla vytvořena za účelem zrušení naposledy opravené faktury.</span><span class="sxs-lookup"><span data-stu-id="c12a1-114">**Canceling invoice** – The system-generated credit invoice that was created to cancel the invoice that was most recently corrected.</span></span>
-   <span data-ttu-id="c12a1-115">**Opravená faktura** – Faktura, která obsahuje informace o opravené faktuře.</span><span class="sxs-lookup"><span data-stu-id="c12a1-115">**Corrected invoice** – The invoice that contains the corrected invoice information.</span></span>

<span data-ttu-id="c12a1-116">Zrušení faktury a opravnou fakturu lze určit dvěma způsoby:</span><span class="sxs-lookup"><span data-stu-id="c12a1-116">You can identify canceling and correcting invoices in two ways:</span></span>

-   <span data-ttu-id="c12a1-117">Na stránce **Všechny volné faktury** je sloupec **Oprava**, ve kterém můžete vidět, které faktury jsou zrušeny a které jsou opravné.</span><span class="sxs-lookup"><span data-stu-id="c12a1-117">The **All free text invoices** page includes a **Correction** column, where you can see which invoices are canceling invoices and corrected invoices.</span></span>
-   <span data-ttu-id="c12a1-118">Záhlaví volné faktury zobrazuje stav **Zrušení faktury '\[číslo faktury\]'** nebo **Opravená faktura '\[číslo faktury\]'**.</span><span class="sxs-lookup"><span data-stu-id="c12a1-118">The header of the free text invoice shows a status of **Cancelling invoice '\[invoice number\]'** or **Corrected invoice '\[invoice number\]'**.</span></span>

> [!NOTE]
> <span data-ttu-id="c12a1-119">Tato funkce je k dispozici pouze tehdy, je-li vybrán konfigurační klíč **Oprava volné faktury**.</span><span class="sxs-lookup"><span data-stu-id="c12a1-119">This feature is available only if the **Free text invoice correction** configuration key is selected.</span></span> <span data-ttu-id="c12a1-120">Další informace o povolení konfiguračních klíčů naleznete v části Povolení (nebo zakázání) konfiguračních klíčů v tématu [Režimy údržby](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/maintenance-mode).</span><span class="sxs-lookup"><span data-stu-id="c12a1-120">For more information on how to enable Configuration keys refer to the Enable (or disable) configuration keys section in the [Maintenance mode](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/maintenance-mode) topic.</span></span> 



