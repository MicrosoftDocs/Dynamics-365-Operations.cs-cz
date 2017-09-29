---
title: "Nastavení zmocnění přímému debetu SEPA"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8b50c2d585c7e0bcd8dc15aa70446cd7346ad33c
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---

# <a name="set-up-sepa-direct-debit-mandate"></a><span data-ttu-id="d3c89-102">Nastavení zmocnění přímému debetu SEPA</span><span class="sxs-lookup"><span data-stu-id="d3c89-102">Set up SEPA direct debit mandate</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="d3c89-103">Přímý debet SEPA (Jednotná oblast pro platby v eurech) umožňuje příjemci vybírat finanční prostředky z bankovního účtu odběratele za předpokladu, že odběratel udělil příjemci podepsané zmocnění.</span><span class="sxs-lookup"><span data-stu-id="d3c89-103">A Single Euro Payment Area (SEPA) direct debit lets a creditor collect funds from a customer's bank account, provided that the customer has granted a signed mandate to the creditor.</span></span> <span data-ttu-id="d3c89-104">Zmocnění, které odběratel podepisuje, opravňuje příjemce k výběru plateb a vydávání příkazů bance odběratele k vyplacení shromážděných prostředků.</span><span class="sxs-lookup"><span data-stu-id="d3c89-104">The mandate that the customer signs authorizes the creditor to collect a payment and instructs the customer's bank to pay the collection.</span></span> <span data-ttu-id="d3c89-105">Toto téma je uspořádáno tak, aby zobrazovalo proces nastavení zmocnění přímého debetu SEPA.</span><span class="sxs-lookup"><span data-stu-id="d3c89-105">This topic is organized to show the process for setting up SEPA direct debit mandates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d3c89-106">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="d3c89-106">Prerequisites</span></span>
<span data-ttu-id="d3c89-107">Následující tabulka zobrazuje požadavky, které musí být splněny, než začnete.</span><span class="sxs-lookup"><span data-stu-id="d3c89-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="d3c89-108">Kategorie</span><span class="sxs-lookup"><span data-stu-id="d3c89-108">Category</span></span>       | <span data-ttu-id="d3c89-109">Předpoklad</span><span class="sxs-lookup"><span data-stu-id="d3c89-109">Prerequisite</span></span>                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c89-110">Země / oblast</span><span class="sxs-lookup"><span data-stu-id="d3c89-110">Country/region</span></span> | <span data-ttu-id="d3c89-111">Primární adresa pro právnickou osobu musí být v těchto zemích či oblastech: Belgie, Francie, Itálie, Německo, Nizozemsko, Rakousko nebo Španělsko.</span><span class="sxs-lookup"><span data-stu-id="d3c89-111">The primary address for the legal entity must be in the following countries/regions: Austria, Belgium, Germany, Spain, France, Italy, or the Netherlands.</span></span> |

1. <span data-ttu-id="d3c89-112">Nastavení číselné řady pro zmocněníy přímého debetu Každý přímý debet musí mít jedinečné číslo.</span><span class="sxs-lookup"><span data-stu-id="d3c89-112">Set up a number sequence for direct debit mandates Each direct debit mandate must have a unique number.</span></span> <span data-ttu-id="d3c89-113">Na stránce **Číselné řady** vytvořte číselnou řadu pro zmocnění k přímému debetu.</span><span class="sxs-lookup"><span data-stu-id="d3c89-113">Use the **Number sequences** page to create a number sequence for direct debit mandates.</span></span> <span data-ttu-id="d3c89-114">Tento identifikátor slouží k přiřazení číselné řady k systému zmocnění k přímému debetu na stránce **Parametry pohledávek**.</span><span class="sxs-lookup"><span data-stu-id="d3c89-114">You will use this identifier to assign the number sequence to the direct debit mandate system on the **Accounts receivable parameters** page.</span></span>

2. <span data-ttu-id="d3c89-115">Nastavení parametrů pohledávek pro zmocněníy přímého debetu Na stránce **Parametry pohledávek** nastavte parametry pro zmocněníy přímého debetu.</span><span class="sxs-lookup"><span data-stu-id="d3c89-115">Set up Accounts receivable parameters for direct debit mandates Use the **Accounts receivable parameters** page to set up parameters for direct debit mandates.</span></span> <span data-ttu-id="d3c89-116">Chcete-li nastavit parametry, na kartě **Přímý debet** změňte výchozí parametry.</span><span class="sxs-lookup"><span data-stu-id="d3c89-116">To set up the parameters, on the **Direct debit** tab, change the default parameters as you require.</span></span> <span data-ttu-id="d3c89-117">Poté na kartě **Číselné řady** aktualizujte pole **ID zmocnění přímého debetu** číselnou řadou, kterou jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="d3c89-117">Then, on the **Number sequences** tab, update the **Direct debit mandate ID** field with the number sequence that you set up earlier.</span></span>

3. <span data-ttu-id="d3c89-118">Nastavení metody platby zmocnění přímého debetu: K nastavení metody platby pro zmocnění k přímému debetu je nutné provést následující kroky pro metodu platby:</span><span class="sxs-lookup"><span data-stu-id="d3c89-118">Set up a method of payment for direct debit mandates You must set up a method of payment for direct debit mandates.</span></span> <span data-ttu-id="d3c89-119">Tuto metodu platby použijte u faktur pro generování přímých debetních plateb.</span><span class="sxs-lookup"><span data-stu-id="d3c89-119">You use this method of payment to query for invoices to generate direct debit payments for.</span></span> <span data-ttu-id="d3c89-120">Na stránce **Metody platby** nastavte metodu platby.</span><span class="sxs-lookup"><span data-stu-id="d3c89-120">Use the **Methods of payment** page to set up the method of payment.</span></span> <span data-ttu-id="d3c89-121">K nastavení metody platby pro zmocnění k přímému debetu je nutné provést následující kroky pro metodu platby:</span><span class="sxs-lookup"><span data-stu-id="d3c89-121">To set up a method of payment for direct debit mandates, you must follow these additional steps for a method of payment:</span></span>

-   <span data-ttu-id="d3c89-122">V poli **Typ platby** vyberte možnost **Elektronická platba**.</span><span class="sxs-lookup"><span data-stu-id="d3c89-122">In the **Payment type** field, select **Electronic payment**.</span></span>
-   <span data-ttu-id="d3c89-123">Volitelné: Pokud předpokládáte, že odběratelé mají více zmocnění, vyberte v poli **Období** možnost **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="d3c89-123">Optional: If you expect each of your customers to have multiple mandates, in the **Period** field, select **Invoice**.</span></span> <span data-ttu-id="d3c89-124">Tímto se vytvoří samostatná platba pro každou fakturu, a každá platba bude používat zmocnění, které je určeno pro fakturu.</span><span class="sxs-lookup"><span data-stu-id="d3c89-124">A separate payment will be created for each invoice, and each payment will use the mandate that is specified for the invoice.</span></span>
-   <span data-ttu-id="d3c89-125">Zvolte možnost **Požadovat zmocnění**, aby se platby vytvářely pomocí zmocnění k přímému debetu.</span><span class="sxs-lookup"><span data-stu-id="d3c89-125">Select the **Require mandate** option to create payments by using direct debit mandates.</span></span> <span data-ttu-id="d3c89-126">Možnost **Požadovat zmocnění** je k dispozici pouze v případě, že v poli **Typ platby** vyberete možnost **Elektronická platba**.</span><span class="sxs-lookup"><span data-stu-id="d3c89-126">The **Require mandate** option is available only if you select **Electronic payment** in the **Payment type** field.</span></span>

<span data-ttu-id="d3c89-127">Viz také</span><span class="sxs-lookup"><span data-stu-id="d3c89-127">See Also</span></span>

[<span data-ttu-id="d3c89-128">Přehled přímého inkasa</span><span class="sxs-lookup"><span data-stu-id="d3c89-128">Direct debit overview</span></span>](sepa-direct-debit-overview.md) 

[<span data-ttu-id="d3c89-129">Vytvoření zmocnění k přímému debetu pro odběratele</span><span class="sxs-lookup"><span data-stu-id="d3c89-129">Create a direct debit mandate for a customer</span></span>](tasks/create-direct-debit-mandate-customer.md) 


