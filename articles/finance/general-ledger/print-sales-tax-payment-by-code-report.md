---
title: Tisk platby DPH podle sestavy kódu
description: Toto téma obsahuje informace o nastavení a akcích, které jsou nutné k vytištění platby DPH podle kódu v měně účtování nebo kódu DPH.
author: anasyash
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: dd490663e66d1eda0eb0ea052e5b54fb867f81df
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990283"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a><span data-ttu-id="7191f-103">Tisk platby DPH podle sestavy kódu</span><span class="sxs-lookup"><span data-stu-id="7191f-103">Print the Sales tax payment by code report</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7191f-104">Chcete-li vytisknout **platbu DPH podle kódu**, přejděte na **Daně** \> **Dotazy a sestavy** \> **Sestavy DPH** \> **Platba DPH podle kódu**.</span><span class="sxs-lookup"><span data-stu-id="7191f-104">To print the **Sales tax payment by code** report, go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span> <span data-ttu-id="7191f-105">Ve výchozím nastavení jsou částky sestavy generovány v zúčtovací měně právnické osoby pro všechny kódy vykazování, které jsou nastaveny na stránce **Kódy vykazování DPH**.</span><span class="sxs-lookup"><span data-stu-id="7191f-105">By default, report amounts are generated in the accounting currency of the legal entity for all reporting codes that are set up on the **Sales tax reporting codes** page.</span></span>

<span data-ttu-id="7191f-106">Tuto sestavu lze rovněž vygenerovat tak, aby v měnách kódů DPH pro všechny kódy vykazování přiřazené ke kódům DPH na stránce **kódy DPH** byla zobrazena částka platby DPH.</span><span class="sxs-lookup"><span data-stu-id="7191f-106">You can also generate this report so that it shows the sales tax payment amounts in the currencies of sales tax codes for all reporting codes that are assigned to sales tax codes on the **Sales tax codes** page.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="7191f-107">Zapnutí funkce</span><span class="sxs-lookup"><span data-stu-id="7191f-107">Turn on the feature</span></span>

<span data-ttu-id="7191f-108">V pracovním prostoru **Správa funkcí** zapněte následující funkci: **Generovat sestavu plateb DPH podle kódu v měně kódu DPH**.</span><span class="sxs-lookup"><span data-stu-id="7191f-108">In the **Feature management** workspace, turn on the following feature: **Generate the Sales tax payment by code report in the sales tax code currency**.</span></span>

## <a name="run-the-report"></a><span data-ttu-id="7191f-109">Spuštění sestavy </span><span class="sxs-lookup"><span data-stu-id="7191f-109">Run the report</span></span>

1. <span data-ttu-id="7191f-110">Přejděte na **Daň** \> **Dotazy a sestavy** \> **Sestavy DPH** \> **Platby DPH dle kódu**.</span><span class="sxs-lookup"><span data-stu-id="7191f-110">Go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span>
2. <span data-ttu-id="7191f-111">V poli **Měna sestavy** vyberte některou z následujících hodnot:</span><span class="sxs-lookup"><span data-stu-id="7191f-111">In the **Report currency** field, select one of the following values:</span></span>

    - <span data-ttu-id="7191f-112">**Zúčtovací měna** – tisk částek sestavy v zúčtovací měně.</span><span class="sxs-lookup"><span data-stu-id="7191f-112">**Accounting currency** – Print the report amounts in the accounting currency.</span></span>
    - <span data-ttu-id="7191f-113">**Měna kódu DPH** – Tisk částek sestavy v měnách kódů DPH.</span><span class="sxs-lookup"><span data-stu-id="7191f-113">**Sales tax code currency** – Print the report amounts in the currencies of sales tax codes.</span></span>

    ![Dialogové okno Platba DPH dle kódu (sestava)](media/Sales-tax-payment-by-code.png)

<span data-ttu-id="7191f-115">Následující obrázek znázorňuje příklad vygenerované sestavy.</span><span class="sxs-lookup"><span data-stu-id="7191f-115">The following illustration shows an example of the report that is generated.</span></span> <span data-ttu-id="7191f-116">Sestava ukazuje, že kód vykazování **101** má měnu **EUR**, pokud je pole **Měna DPH** nastaveno na **EUR** pro kód DPH, ke kterému je kód vykazování přiřazen.</span><span class="sxs-lookup"><span data-stu-id="7191f-116">The report shows that reporting code **101** has the **EUR** currency if the **Sales tax currency** field is set to **EUR** for the sales tax code that the reporting code is assigned to.</span></span>

![Příkald sestavy Platba DPH podle kódu](media/Sales-tax-payment-by-code-2.png)
