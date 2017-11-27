---
title: "Nastavení zmocnění přímého inkasa SEPA"
description: "Přímý debet SEPA (Jednotná oblast pro platby v eurech) umožňuje příjemci vybírat finanční prostředky z bankovního účtu odběratele za předpokladu, že odběratel udělil příjemci podepsané zmocnění."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5b9afeb24692010ca5de33156f372d86f167161e
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-sepa-direct-debit-mandate"></a><span data-ttu-id="d2ae4-103">Nastavení zmocnění přímého inkasa SEPA</span><span class="sxs-lookup"><span data-stu-id="d2ae4-103">Set up SEPA direct debit mandate</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d2ae4-104">Přímý debet SEPA (Jednotná oblast pro platby v eurech) umožňuje příjemci vybírat finanční prostředky z bankovního účtu odběratele za předpokladu, že odběratel udělil příjemci podepsané zmocnění.</span><span class="sxs-lookup"><span data-stu-id="d2ae4-104">A Single Euro Payment Area (SEPA) direct debit lets a creditor collect funds from a customer's bank account, provided that the customer has granted a signed mandate to the creditor.</span></span> <span data-ttu-id="d2ae4-105">Zmocnění, které odběratel podepisuje, opravňuje příjemce k výběru plateb a vydávání příkazů bance odběratele k vyplacení shromážděných prostředků.</span><span class="sxs-lookup"><span data-stu-id="d2ae4-105">The mandate that the customer signs authorizes the creditor to collect a payment and instructs the customer's bank to pay the collection.</span></span> <span data-ttu-id="d2ae4-106">Toto téma je uspořádáno tak, aby zobrazovalo proces nastavení zmocnění přímého debetu SEPA.</span><span class="sxs-lookup"><span data-stu-id="d2ae4-106">This topic is organized to show the process for setting up SEPA direct debit mandates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d2ae4-107">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="d2ae4-107">Prerequisites</span></span>
<span data-ttu-id="d2ae4-108">Následující tabulka zobrazuje požadavky, které musí být splněny, než začnete.</span><span class="sxs-lookup"><span data-stu-id="d2ae4-108">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="d2ae4-109">Kategorie</span><span class="sxs-lookup"><span data-stu-id="d2ae4-109">Category</span></span>       | <span data-ttu-id="d2ae4-110">Předpoklad</span><span class="sxs-lookup"><span data-stu-id="d2ae4-110">Prerequisite</span></span>                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ae4-111">Země / oblast</span><span class="sxs-lookup"><span data-stu-id="d2ae4-111">Country/region</span></span> | <span data-ttu-id="d2ae4-112">Primární adresa pro právnickou osobu musí být v těchto zemích či oblastech: Belgie, Francie, Itálie, Německo, Nizozemsko, Rakousko nebo Španělsko.</span><span class="sxs-lookup"><span data-stu-id="d2ae4-112">The primary address for the legal entity must be in the following countries/regions: Austria, Belgium, Germany, Spain, France, Italy, or the Netherlands.</span></span> |

1. <span data-ttu-id="d2ae4-113">Nastavení číselné řady pro zmocněníy přímého debetu Každý přímý debet musí mít jedinečné číslo.</span><span class="sxs-lookup"><span data-stu-id="d2ae4-113">Set up a number sequence for direct debit mandates Each direct debit mandate must have a unique number.</span></span> <span data-ttu-id="d2ae4-114">Na stránce **Číselné řady** vytvořte číselnou řadu pro zmocnění k přímému debetu.</span><span class="sxs-lookup"><span data-stu-id="d2ae4-114">Use the **Number sequences** page to create a number sequence for direct debit mandates.</span></span> <span data-ttu-id="d2ae4-115">Tento identifikátor slouží k přiřazení číselné řady k systému zmocnění k přímému debetu na stránce **Parametry pohledávek**.</span><span class="sxs-lookup"><span data-stu-id="d2ae4-115">You will use this identifier to assign the number sequence to the direct debit mandate system on the **Accounts receivable parameters** page.</span></span>

2. <span data-ttu-id="d2ae4-116">Nastavení parametrů pohledávek pro zmocněníy přímého debetu Na stránce **Parametry pohledávek** nastavte parametry pro zmocněníy přímého debetu.</span><span class="sxs-lookup"><span data-stu-id="d2ae4-116">Set up Accounts receivable parameters for direct debit mandates Use the **Accounts receivable parameters** page to set up parameters for direct debit mandates.</span></span> <span data-ttu-id="d2ae4-117">Chcete-li nastavit parametry, na kartě **Přímý debet** změňte výchozí parametry.</span><span class="sxs-lookup"><span data-stu-id="d2ae4-117">To set up the parameters, on the **Direct debit** tab, change the default parameters as you require.</span></span> <span data-ttu-id="d2ae4-118">Poté na kartě **Číselné řady** aktualizujte pole **ID zmocnění přímého debetu** číselnou řadou, kterou jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="d2ae4-118">Then, on the **Number sequences** tab, update the **Direct debit mandate ID** field with the number sequence that you set up earlier.</span></span>

3. <span data-ttu-id="d2ae4-119">Nastavení metody platby zmocnění přímého debetu: K nastavení metody platby pro zmocnění k přímému debetu je nutné provést následující kroky pro metodu platby:</span><span class="sxs-lookup"><span data-stu-id="d2ae4-119">Set up a method of payment for direct debit mandates You must set up a method of payment for direct debit mandates.</span></span> <span data-ttu-id="d2ae4-120">Tuto metodu platby použijte u faktur pro generování přímých debetních plateb.</span><span class="sxs-lookup"><span data-stu-id="d2ae4-120">You use this method of payment to query for invoices to generate direct debit payments for.</span></span> <span data-ttu-id="d2ae4-121">Na stránce **Metody platby** nastavte metodu platby.</span><span class="sxs-lookup"><span data-stu-id="d2ae4-121">Use the **Methods of payment** page to set up the method of payment.</span></span> <span data-ttu-id="d2ae4-122">K nastavení metody platby pro zmocnění k přímému debetu je nutné provést následující kroky pro metodu platby:</span><span class="sxs-lookup"><span data-stu-id="d2ae4-122">To set up a method of payment for direct debit mandates, you must follow these additional steps for a method of payment:</span></span>

-   <span data-ttu-id="d2ae4-123">V poli **Typ platby** vyberte možnost **Elektronická platba**.</span><span class="sxs-lookup"><span data-stu-id="d2ae4-123">In the **Payment type** field, select **Electronic payment**.</span></span>
-   <span data-ttu-id="d2ae4-124">Volitelné: Pokud předpokládáte, že odběratelé mají více zmocnění, vyberte v poli **Období** možnost **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="d2ae4-124">Optional: If you expect each of your customers to have multiple mandates, in the **Period** field, select **Invoice**.</span></span> <span data-ttu-id="d2ae4-125">Tímto se vytvoří samostatná platba pro každou fakturu, a každá platba bude používat zmocnění, které je určeno pro fakturu.</span><span class="sxs-lookup"><span data-stu-id="d2ae4-125">A separate payment will be created for each invoice, and each payment will use the mandate that is specified for the invoice.</span></span>
-   <span data-ttu-id="d2ae4-126">Zvolte možnost **Požadovat zmocnění**, aby se platby vytvářely pomocí zmocnění k přímému debetu.</span><span class="sxs-lookup"><span data-stu-id="d2ae4-126">Select the **Require mandate** option to create payments by using direct debit mandates.</span></span> <span data-ttu-id="d2ae4-127">Možnost **Požadovat zmocnění** je k dispozici pouze v případě, že v poli **Typ platby** vyberete možnost **Elektronická platba**.</span><span class="sxs-lookup"><span data-stu-id="d2ae4-127">The **Require mandate** option is available only if you select **Electronic payment** in the **Payment type** field.</span></span>

<span data-ttu-id="d2ae4-128">Viz také</span><span class="sxs-lookup"><span data-stu-id="d2ae4-128">See Also</span></span>

[<span data-ttu-id="d2ae4-129">Přehled přímého inkasa</span><span class="sxs-lookup"><span data-stu-id="d2ae4-129">Direct debit overview</span></span>](sepa-direct-debit-overview.md) 

[<span data-ttu-id="d2ae4-130">Vytvoření zmocnění k přímému debetu pro odběratele</span><span class="sxs-lookup"><span data-stu-id="d2ae4-130">Create a direct debit mandate for a customer</span></span>](tasks/create-direct-debit-mandate-customer.md) 


