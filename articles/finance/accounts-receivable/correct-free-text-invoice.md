---
title: Oprava faktury s volným textem
description: Tento článek vysvětluje, jak opravit volnou fakturu, která byla zaúčtována, a znovu ji vystavit jako opravenou fakturu.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f04e70c9afb66be015ce18cebebd711f00d764b7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827571"
---
# <a name="correct-a-free-text-invoice"></a><span data-ttu-id="3c589-103">Oprava faktury s volným textem</span><span class="sxs-lookup"><span data-stu-id="3c589-103">Correct a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c589-104">Tento článek vysvětluje, jak opravit volnou fakturu, která byla zaúčtována, a znovu ji vystavit jako opravenou fakturu.</span><span class="sxs-lookup"><span data-stu-id="3c589-104">This article explains how to correct a free text invoice that has been posted and reissue it as a corrected invoice.</span></span>

<span data-ttu-id="3c589-105">Pokud chcete upravit volnou fakturu, která již byla zaúčtována, otevřete ji.</span><span class="sxs-lookup"><span data-stu-id="3c589-105">To correct a free text invoice that has already been posted, open the posted free text invoice.</span></span> <span data-ttu-id="3c589-106">Na stránce **Faktura** vyberte možnost **Zrušit** a poté vyberte možnost **Správná faktura**.</span><span class="sxs-lookup"><span data-stu-id="3c589-106">On the **Invoice** page, select **Cancel**, and then select **Correct invoice**.</span></span> <span data-ttu-id="3c589-107">Vyberte kód důvodu, přidejte poznámky a vyberte datum pro novou, opravenou fakturu.</span><span class="sxs-lookup"><span data-stu-id="3c589-107">Select a reason code, add comments, and select the date for new corrected invoice.</span></span> <span data-ttu-id="3c589-108">Můžete upravit opravenou fakturu a zaúčtovat ji.</span><span class="sxs-lookup"><span data-stu-id="3c589-108">You can modify the corrected invoice, and post it.</span></span> 

<span data-ttu-id="3c589-109">Po zaúčtování opravené faktury se vytvoří zrušení faktury pro kreditní částku, která se rovná původní částce faktury.</span><span class="sxs-lookup"><span data-stu-id="3c589-109">When you post the corrected invoice, a canceling invoice is created for a credit amount that equals the original invoice amount.</span></span> <span data-ttu-id="3c589-110">Kombinovaný zůstatek původní faktury a zrušení faktury je tedy 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="3c589-110">Therefore, the combined balance of the original invoice and the canceling invoice is 0 (zero).</span></span> <span data-ttu-id="3c589-111">Zrušení faktury je vyrovnáno oproti původní faktuře.</span><span class="sxs-lookup"><span data-stu-id="3c589-111">The canceling invoice is settled against the original invoice.</span></span> 

<span data-ttu-id="3c589-112">Po zaúčtování opravené fakturu budete mít tři faktury:</span><span class="sxs-lookup"><span data-stu-id="3c589-112">After you post the corrected invoice, you will have three invoices:</span></span>

-   <span data-ttu-id="3c589-113">**Původní faktura** – Faktura obsahující informace, které opravujete.</span><span class="sxs-lookup"><span data-stu-id="3c589-113">**Original invoice** – The invoice that includes the information that you're correcting.</span></span>
-   <span data-ttu-id="3c589-114">**Zrušení faktury** – Systémem vygenerovaná faktura strany Dal, která byla vytvořena za účelem zrušení naposledy opravené faktury.</span><span class="sxs-lookup"><span data-stu-id="3c589-114">**Canceling invoice** – The system-generated credit invoice that was created to cancel the invoice that was most recently corrected.</span></span>
-   <span data-ttu-id="3c589-115">**Opravená faktura** – Faktura, která obsahuje informace o opravené faktuře.</span><span class="sxs-lookup"><span data-stu-id="3c589-115">**Corrected invoice** – The invoice that contains the corrected invoice information.</span></span>

<span data-ttu-id="3c589-116">Zrušení faktury a opravnou fakturu lze určit dvěma způsoby:</span><span class="sxs-lookup"><span data-stu-id="3c589-116">You can identify canceling and correcting invoices in two ways:</span></span>

-   <span data-ttu-id="3c589-117">Na stránce **Všechny volné faktury** je sloupec **Oprava**, ve kterém můžete vidět, které faktury jsou zrušeny a které jsou opravné.</span><span class="sxs-lookup"><span data-stu-id="3c589-117">The **All free text invoices** page includes a **Correction** column, where you can see which invoices are canceling invoices and corrected invoices.</span></span>
-   <span data-ttu-id="3c589-118">Záhlaví volné faktury zobrazuje stav **Zrušení faktury '\[číslo faktury\]'** nebo **Opravená faktura '\[číslo faktury\]'**.</span><span class="sxs-lookup"><span data-stu-id="3c589-118">The header of the free text invoice shows a status of **Cancelling invoice '\[invoice number\]'** or **Corrected invoice '\[invoice number\]'**.</span></span>

> [!NOTE]
> <span data-ttu-id="3c589-119">Tato funkce je k dispozici pouze tehdy, je-li vybrán konfigurační klíč **Oprava volné faktury**.</span><span class="sxs-lookup"><span data-stu-id="3c589-119">This feature is available only if the **Free text invoice correction** configuration key is selected.</span></span> <span data-ttu-id="3c589-120">Další informace o povolení konfiguračních klíčů naleznete v části Povolení (nebo zakázání) konfiguračních klíčů v tématu [Režimy údržby](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="3c589-120">For more information on how to enable Configuration keys refer to the Enable (or disable) configuration keys section in the [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) topic.</span></span> 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]