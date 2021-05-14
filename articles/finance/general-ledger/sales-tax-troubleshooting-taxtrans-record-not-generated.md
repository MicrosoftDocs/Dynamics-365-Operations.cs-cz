---
title: Záznam TaxTrans se negeneruje
description: Toto téma poskytuje informace o řešení potíží, které mohou pomoci, když se záznam TaxTrans negeneruje.
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0c7414cc39198ff4d5be9b4c41ca62f9c78c9250
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947607"
---
# <a name="taxtrans-record-isnt-generated"></a><span data-ttu-id="84c6d-103">Záznam TaxTrans se negeneruje</span><span class="sxs-lookup"><span data-stu-id="84c6d-103">TaxTrans record isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84c6d-104">Pokud vyberete pro transakci možnost **Zaúčtování DPH**, ale stránka **Zaúčtování DPH** buď nezobrazuje žádné daňové řádky, nebo chybí daňový řádek, záznam **TaxTrans** se možná nevygeneroval.</span><span class="sxs-lookup"><span data-stu-id="84c6d-104">If you select **Posted sales tax** for a transaction, but the **Posted sales tax** page either shows no tax lines or is missing a tax line, the **TaxTrans** record might not have been generated.</span></span>

<span data-ttu-id="84c6d-105">[![Stránka Zaúčtování DPH neobsahuje žádné řádkové položky](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="84c6d-105">[![Posted sales tax page that has no line items](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span></span>

<span data-ttu-id="84c6d-106">Chcete-li tento problém vyřešit, postupujte podle pokynů v následujících částech.</span><span class="sxs-lookup"><span data-stu-id="84c6d-106">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a><span data-ttu-id="84c6d-107">Kontrola DPH před zaúčtováním</span><span class="sxs-lookup"><span data-stu-id="84c6d-107">Check the sales tax before you post the transaction</span></span>

1. <span data-ttu-id="84c6d-108">Před zaúčtováním transakce na stránce **Zaúčtování faktury** vyberte ke kontrole výpočtu možnost **DPH**.</span><span class="sxs-lookup"><span data-stu-id="84c6d-108">Before you post the transaction, on the **Posting invoice** page, select **Sales tax** to check the calculation.</span></span>

    <span data-ttu-id="84c6d-109">[![Tlačítko DPH na stránce Zaúčtování faktury](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="84c6d-109">[![Sales tax button on the Posting invoice page](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span></span>

2. <span data-ttu-id="84c6d-110">Na stránce **Dočasné transakce DPH** zkontrolujte výsledek výpočtu.</span><span class="sxs-lookup"><span data-stu-id="84c6d-110">On the **Temporary sales tax transactions** page, review the result of the calculation.</span></span> <span data-ttu-id="84c6d-111">Pokud není vypočítána žádná daň, viz [Daň se nevypočítá nebo je částka daně nulová](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span><span class="sxs-lookup"><span data-stu-id="84c6d-111">If no tax is calculated, see [Tax isn't calculated or the tax amount is zero](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span></span>

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a><span data-ttu-id="84c6d-112">Nalezení záznamu TaxTrans ve všech zaúčtovaných DPH</span><span class="sxs-lookup"><span data-stu-id="84c6d-112">Find the TaxTrans record in all posted sales tax</span></span>

1. <span data-ttu-id="84c6d-113">Přejděte na k nabídce **Daň** \> **Dotazy a sestavy** \> **Dotazy na DPH** > **Zaúčtování DPH**.</span><span class="sxs-lookup"><span data-stu-id="84c6d-113">Go to **Tax** \> **Inquiries and reports** \> **Sales tax inquiries** > **Posted sales tax**.</span></span>
2. <span data-ttu-id="84c6d-114">V záhlaví sloupce **Doklad** vyberte symbol filtru a najděte záznam **TaxTrans**.</span><span class="sxs-lookup"><span data-stu-id="84c6d-114">In the **Voucher** column heading, select the filter symbol to find the **TaxTrans** record.</span></span>
3. <span data-ttu-id="84c6d-115">Pokud najdete záznamy o DPH, které hledáte, zkontrolujte datum.</span><span class="sxs-lookup"><span data-stu-id="84c6d-115">If you find the sales tax records that you're looking for, check the date.</span></span> <span data-ttu-id="84c6d-116">Pokud se datum liší od data záhlaví deníku, vytvořte požadavek na službu Microsoft pro další podporu.</span><span class="sxs-lookup"><span data-stu-id="84c6d-116">If the date differs from the date of the journal header, create a Microsoft service request for additional support.</span></span>

    <span data-ttu-id="84c6d-117">[![Zaúčtovaná stránka DPH](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="84c6d-117">[![Posted sales tax page](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span></span>

## <a name="debug-to-check-details"></a><span data-ttu-id="84c6d-118">Ladění ke kontrole podrobností</span><span class="sxs-lookup"><span data-stu-id="84c6d-118">Debug to check details</span></span>

1. <span data-ttu-id="84c6d-119">Informace o tom, jak ladit a zjistit, zda se správně vygenerovaly záznamy **TmpTaxWorkTrans** a **TaxUncommitted**, viz [Nesprávná hodnota pole v záznamu TaxTrans](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span><span class="sxs-lookup"><span data-stu-id="84c6d-119">For information about how to debug and determine whether **TmpTaxWorkTrans** and **TaxUncommitted** are correctly generated, see [Field value in TaxTrans is incorrect](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span></span>
2. <span data-ttu-id="84c6d-120">Je-li záznam **TaxTmpWorkTrans** nebo **TaxUncommitted** správně vygenerován, přidejte zarážku na **TaxPost::SaveAndPost()** a **Tax::SaveAndPost** k ladění důvodu, proč se nevložil záznam **TaxTrans**.</span><span class="sxs-lookup"><span data-stu-id="84c6d-120">If **TaxTmpWorkTrans** or **TaxUncommitted** is correctly generated, add a breakpoint at **TaxPost::SaveAndPost()** and **Tax::SaveAndPost** to debug the reason why **TaxTrans** isn't inserted.</span></span>

    <span data-ttu-id="84c6d-121">[![Zarážky přidané v kódu](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="84c6d-121">[![Breakpoints added in code](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span></span>

    <span data-ttu-id="84c6d-122">[![Výsledky přidaných zarážek](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="84c6d-122">[![Results of added breakpoints](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="84c6d-123">Zjištění, zda existuje přizpůsobení</span><span class="sxs-lookup"><span data-stu-id="84c6d-123">Determine whether customization exists</span></span>

<span data-ttu-id="84c6d-124">Pokud jste dokončili kroky v předchozích částech, ale problém se vám nepodařilo vyřešit, zjistěte, zda existuje přizpůsobení.</span><span class="sxs-lookup"><span data-stu-id="84c6d-124">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="84c6d-125">Pokud neexistuje žádné přizpůsobení, vytvořte požadavek na službu Microsoft pro další podporu.</span><span class="sxs-lookup"><span data-stu-id="84c6d-125">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
