---
title: Refundace odběratelům
description: Tento článek vysvětluje, jak lze vytvořit transakce refundace pro skupinu odběratelů. Jestliže u odběratele figuruje kreditní zůstatek, můžete refundovat kladné zůstatky množství zůstatku odběratele.
author: JodiChristiansen
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65ee884fb22c1a38e2d3022085fed7e3e6077d1f
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644530"
---
# <a name="reimburse-customers"></a><span data-ttu-id="06a6e-104">Refundace odběratelům</span><span class="sxs-lookup"><span data-stu-id="06a6e-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06a6e-105">Tento článek vysvětluje, jak lze vytvořit transakce refundace pro skupinu odběratelů.</span><span class="sxs-lookup"><span data-stu-id="06a6e-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="06a6e-106">Jestliže u odběratele figuruje kreditní zůstatek, můžete refundovat kladné zůstatky množství zůstatku odběratele.</span><span class="sxs-lookup"><span data-stu-id="06a6e-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="06a6e-107">Následující tabulka zobrazuje požadavky, které musí být splněny, než začnete.</span><span class="sxs-lookup"><span data-stu-id="06a6e-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="06a6e-108">Předpoklad</span><span class="sxs-lookup"><span data-stu-id="06a6e-108">Prerequisite</span></span>                                                            | <span data-ttu-id="06a6e-109">Popis</span><span class="sxs-lookup"><span data-stu-id="06a6e-109">Description</span></span> |
|-------------------------------------------------------------------------|-------------|
| <span data-ttu-id="06a6e-110">Určete minimální částku refundace pro právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="06a6e-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="06a6e-111">Na stránce **Parametry pohledávek** v části **Hlavní** v poli **Minimální refundace** zadejte minimální množství, které může být vráceno u přeplatků odběratele.</span><span class="sxs-lookup"><span data-stu-id="06a6e-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="06a6e-112">Volitelné: přidejte účet dodavatele pro každého odběratele, kterému lze refundovat.</span><span class="sxs-lookup"><span data-stu-id="06a6e-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="06a6e-113">Na stránce **Odběratelé** na pevné záložce **Různé podrobnosti** v poli **Účet dodavatele** vyberte účet dodavatele pro odběratele.</span><span class="sxs-lookup"><span data-stu-id="06a6e-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span> |

<span data-ttu-id="06a6e-114">Při vytváření transakcí refundace bude vytvořena faktura dodavatele s částkou kreditního zůstatku.</span><span class="sxs-lookup"><span data-stu-id="06a6e-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="06a6e-115">Proces refundace odstraní kreditní zůstatek účtu odběratele a vytvoří zůstatek splatnosti pro účet dodavatele, který odpovídá odběrateli.</span><span class="sxs-lookup"><span data-stu-id="06a6e-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1. <span data-ttu-id="06a6e-116">V Pohledávkách spusťte proces **Úhrada** proces (**Pohledávky \> Pravidelné úkoly \> Úhrada**).</span><span class="sxs-lookup"><span data-stu-id="06a6e-116">In Accounts receivable, run the **Reimbursement** process (**Accounts receivable \> Periodic tasks \> Reimbursement**).</span></span>
2. <span data-ttu-id="06a6e-117">Chcete-li seskupit všechny transakce, bez ohledu na dimenze hlavní knihy, nastavte možnost **Souhrn zákazníka** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="06a6e-117">To group all transactions, regardless of ledger dimensions, set the **Summarize customer** option to **Yes**.</span></span> <span data-ttu-id="06a6e-118">Chcete-li seskupit pouze transakce, které mají podobné dimenze hlavní knihy, nastavte možnost na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="06a6e-118">To group only transactions that have similar ledger dimensions, set the option to **No**.</span></span>
3. <span data-ttu-id="06a6e-119">Vyberte **Zahrnout zákazníky s nevyřízenými debetními transakcemi**, pokud chcete vybrat zákazníky, kteří mají nevyrovnané částky debetu.</span><span class="sxs-lookup"><span data-stu-id="06a6e-119">Select **Include customers with outstanding debit transactions** to select customers who have unsettled debit amounts.</span></span>
4. <span data-ttu-id="06a6e-120">K úhradě konkrétních zákaznických účtů na pevné záložce **Záznamy, které mají být zahrnuty** vyberte **Filtr** a poté v dotazu zadejte zákaznické účty.</span><span class="sxs-lookup"><span data-stu-id="06a6e-120">To reimburse specific customer accounts, on the **Records to include** FastTab, select **Filter**, and then specify the customer accounts in the query.</span></span>

    <span data-ttu-id="06a6e-121">Částky úvěru jsou převedeny na účty dodavatelů daných odběratelů a jsou zpracovány jako běžné platby.</span><span class="sxs-lookup"><span data-stu-id="06a6e-121">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="06a6e-122">Pokud některý odběratel nemá účet dodavatele, automaticky se pro odběratele vytvoří jednorázový účet dodavatele.</span><span class="sxs-lookup"><span data-stu-id="06a6e-122">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>

5. <span data-ttu-id="06a6e-123">Chcete-li zobrazit transakce úhrad, které byly vytvořeny, použijte sestavu **Úhrada** (**Pohledávky \> Dotazy a sestavy \> Sestava úhrady**).</span><span class="sxs-lookup"><span data-stu-id="06a6e-123">To view the reimbursement transactions that were created, use the **Reimbursement** report (**Accounts Receivable \> Inquiries and reports \> Reimbursement report**).</span></span>
6. <span data-ttu-id="06a6e-124">V části Závazky vytvořte platbu pro faktury dodavatele, které byly vytvořeny procesem refundace.</span><span class="sxs-lookup"><span data-stu-id="06a6e-124">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span> <span data-ttu-id="06a6e-125">Informace o tom, jak platit dodavatelům, najdete na stránce [Přehled plateb dodavatele](../accounts-payable/Vendor-payments-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="06a6e-125">For information about how to pay vendors, see [Vendor payment overview](../accounts-payable/Vendor-payments-workspace.md).</span></span>
