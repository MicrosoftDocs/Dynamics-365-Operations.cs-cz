---
title: Refundace odběratelům
description: Tento článek vysvětluje, jak lze vytvořit transakce refundace pro skupinu odběratelů. Jestliže u odběratele figuruje kreditní zůstatek, můžete refundovat kladné zůstatky množství zůstatku odběratele.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
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
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97982dec140ed440682ae507f40557670ebccd3e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836621"
---
# <a name="reimburse-customers"></a><span data-ttu-id="b9909-104">Refundace odběratelům</span><span class="sxs-lookup"><span data-stu-id="b9909-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9909-105">Tento článek vysvětluje, jak lze vytvořit transakce refundace pro skupinu odběratelů.</span><span class="sxs-lookup"><span data-stu-id="b9909-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="b9909-106">Jestliže u odběratele figuruje kreditní zůstatek, můžete refundovat kladné zůstatky množství zůstatku odběratele.</span><span class="sxs-lookup"><span data-stu-id="b9909-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="b9909-107">Následující tabulka zobrazuje požadavky, které musí být splněny, než začnete.</span><span class="sxs-lookup"><span data-stu-id="b9909-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="b9909-108">Předpoklad</span><span class="sxs-lookup"><span data-stu-id="b9909-108">Prerequisite</span></span>                                                            | <span data-ttu-id="b9909-109">Popis</span><span class="sxs-lookup"><span data-stu-id="b9909-109">Description</span></span>                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9909-110">Určete minimální částku refundace pro právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="b9909-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="b9909-111">Na stránce **Parametry pohledávek** v části **Hlavní** v poli **Minimální refundace** zadejte minimální množství, které může být vráceno u přeplatků odběratele.</span><span class="sxs-lookup"><span data-stu-id="b9909-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="b9909-112">Volitelné: přidejte účet dodavatele pro každého odběratele, kterému lze refundovat.</span><span class="sxs-lookup"><span data-stu-id="b9909-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="b9909-113">Na stránce **Odběratelé** na pevné záložce **Různé podrobnosti** v poli **Účet dodavatele** vyberte účet dodavatele pro odběratele.</span><span class="sxs-lookup"><span data-stu-id="b9909-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span>                                           |

<span data-ttu-id="b9909-114">Při vytváření transakcí refundace bude vytvořena faktura dodavatele s částkou kreditního zůstatku.</span><span class="sxs-lookup"><span data-stu-id="b9909-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="b9909-115">Proces refundace odstraní kreditní zůstatek účtu odběratele a vytvoří zůstatek splatnosti pro účet dodavatele, který odpovídá odběrateli.</span><span class="sxs-lookup"><span data-stu-id="b9909-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1.  <span data-ttu-id="b9909-116">V modulu Pohledávky můžete spustit proces **Refundace**.</span><span class="sxs-lookup"><span data-stu-id="b9909-116">In Accounts receivable, run the **Reimbursement** process.</span></span>
2.  <span data-ttu-id="b9909-117">Proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="b9909-117">Follow one of these steps:</span></span>
    -   <span data-ttu-id="b9909-118">Chcete-li provést refundaci pro konkrétní účty odběratele, klikněte na volbu **Zvolit** a zadejte do dotazu požadované účty odběratele.</span><span class="sxs-lookup"><span data-stu-id="b9909-118">To reimburse specific customer accounts, click **Select**, and specify the customer accounts in the query.</span></span>
    -   <span data-ttu-id="b9909-119">Chcete-li provést refundaci pro všechny účty odběratele, klepněte na volbu **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9909-119">To reimburse all customer accounts, click **OK**.</span></span>

    <span data-ttu-id="b9909-120">Částky úvěru jsou převedeny na účty dodavatelů daných odběratelů a jsou zpracovány jako běžné platby.</span><span class="sxs-lookup"><span data-stu-id="b9909-120">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="b9909-121">Pokud některý odběratel nemá účet dodavatele, automaticky se pro odběratele vytvoří jednorázový účet dodavatele.</span><span class="sxs-lookup"><span data-stu-id="b9909-121">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>
3.  <span data-ttu-id="b9909-122">K zobrazení transakcí refundace, které byly vytvořeny pomocí periodické úlohy, použijte stránku **Refundace**.</span><span class="sxs-lookup"><span data-stu-id="b9909-122">To view the reimbursement transactions that were created, use the **Reimbursement** page.</span></span>
4.  <span data-ttu-id="b9909-123">V části Závazky vytvořte platbu pro faktury dodavatele, které byly vytvořeny procesem refundace.</span><span class="sxs-lookup"><span data-stu-id="b9909-123">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span>




