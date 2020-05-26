---
title: Tisk platby DPH podle sestavy kódu
description: Toto téma obsahuje informace o nastavení a akcích, které jsou nutné k vytištění platby DPH podle kódu v měně účtování nebo kódu DPH.
author: anasyash
manager: AnnBe
ms.date: 04/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 3c3b251aadfa997f453e60b0842f89a6f09eb9cb
ms.sourcegitcommit: 88347d0f0ac862a77f269a05f1801d30dc93586e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2020
ms.locfileid: "3260248"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a><span data-ttu-id="c0bea-103">Tisk platby DPH podle sestavy kódu</span><span class="sxs-lookup"><span data-stu-id="c0bea-103">Print the Sales tax payment by code report</span></span> 

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="c0bea-104">Chcete-li vytisknout **platbu DPH podle kódu**, přejděte na **Daně** \> **Dotazy a sestavy** \> **Sestavy DPH** \> **Platba DPH podle kódu**.</span><span class="sxs-lookup"><span data-stu-id="c0bea-104">To print the **Sales tax payment by code** report, go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span> <span data-ttu-id="c0bea-105">Ve výchozím nastavení jsou částky sestavy generovány v zúčtovací měně právnické osoby pro všechny kódy vykazování, které jsou nastaveny na stránce **Kódy vykazování DPH**.</span><span class="sxs-lookup"><span data-stu-id="c0bea-105">By default, report amounts are generated in the accounting currency of the legal entity for all reporting codes that are set up on the **Sales tax reporting codes** page.</span></span>

<span data-ttu-id="c0bea-106">Tuto sestavu lze rovněž vygenerovat tak, aby v měnách kódů DPH pro všechny kódy vykazování přiřazené ke kódům DPH na stránce **kódy DPH** byla zobrazena částka platby DPH.</span><span class="sxs-lookup"><span data-stu-id="c0bea-106">You can also generate this report so that it shows the sales tax payment amounts in the currencies of sales tax codes for all reporting codes that are assigned to sales tax codes on the **Sales tax codes** page.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="c0bea-107">Zapnutí funkce</span><span class="sxs-lookup"><span data-stu-id="c0bea-107">Turn on the feature</span></span>

<span data-ttu-id="c0bea-108">V pracovním prostoru **Správa funkcí** zapněte následující funkci: **Generovat sestavu plateb DPH podle kódu v měně kódu DPH**.</span><span class="sxs-lookup"><span data-stu-id="c0bea-108">In the **Feature management** workspace, turn on the following feature: **Generate the Sales tax payment by code report in the sales tax code currency**.</span></span>

## <a name="run-the-report"></a><span data-ttu-id="c0bea-109">Spuštění sestavy </span><span class="sxs-lookup"><span data-stu-id="c0bea-109">Run the report</span></span>

1. <span data-ttu-id="c0bea-110">Přejděte na **Daň** \> **Dotazy a sestavy** \> **Sestavy DPH** \> **Platby DPH dle kódu**.</span><span class="sxs-lookup"><span data-stu-id="c0bea-110">Go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span>
2. <span data-ttu-id="c0bea-111">V poli **Měna sestavy** vyberte některou z následujících hodnot:</span><span class="sxs-lookup"><span data-stu-id="c0bea-111">In the **Report currency** field, select one of the following values:</span></span>

    - <span data-ttu-id="c0bea-112">**Zúčtovací měna** – tisk částek sestavy v zúčtovací měně.</span><span class="sxs-lookup"><span data-stu-id="c0bea-112">**Accounting currency** – Print the report amounts in the accounting currency.</span></span>
    - <span data-ttu-id="c0bea-113">**Měna kódu DPH** – Tisk částek sestavy v měnách kódů DPH.</span><span class="sxs-lookup"><span data-stu-id="c0bea-113">**Sales tax code currency** – Print the report amounts in the currencies of sales tax codes.</span></span>

    ![Dialogové okno Platba DPH dle kódu (sestava)](media/Sales-tax-payment-by-code.png)

<span data-ttu-id="c0bea-115">Následující obrázek znázorňuje příklad vygenerované sestavy.</span><span class="sxs-lookup"><span data-stu-id="c0bea-115">The following illustration shows an example of the report that is generated.</span></span> <span data-ttu-id="c0bea-116">Sestava ukazuje, že kód vykazování **101** má měnu **EUR**, pokud je pole **Měna DPH** nastaveno na **EUR** pro kód DPH, ke kterému je kód vykazování přiřazen.</span><span class="sxs-lookup"><span data-stu-id="c0bea-116">The report shows that reporting code **101** has the **EUR** currency if the **Sales tax currency** field is set to **EUR** for the sales tax code that the reporting code is assigned to.</span></span>

![Příkald sestavy Platba DPH podle kódu](media/Sales-tax-payment-by-code-2.png)