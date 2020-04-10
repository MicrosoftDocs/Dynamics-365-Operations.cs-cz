---
title: " Konfigurace plateb pro maloobchodní výkazy"
description: Tato procedura ukazuje konfigurace pro metody plateb velkoobchodu, které ovlivní způsob pro vytváření a účtování výkazy maloobchodu.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 390ccdfde3f9bb93770d456af7532a42e81955a1
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140800"
---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="de853-103"> Konfigurace plateb pro maloobchodní výkazy</span><span class="sxs-lookup"><span data-stu-id="de853-103">Payment configurations for Retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de853-104">Tato procedura ukazuje konfigurace pro metody plateb velkoobchodu, které ovlivní způsob pro vytváření a účtování výkazy maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="de853-104">This procedure demonstrates configurations for Commerce store payment methods, which affect how statements get created and posted.</span></span>

<span data-ttu-id="de853-105">Tento záznam používá ukázkovou společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="de853-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="de853-106">Přejděte na Maloobchodní a velkoobchodní prodej > Kanály > Obchody > Všechny obchody.</span><span class="sxs-lookup"><span data-stu-id="de853-106">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="de853-107">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="de853-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="de853-108">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="de853-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="de853-109">V podokně akcí klikněte na možnost Nastavit.</span><span class="sxs-lookup"><span data-stu-id="de853-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="de853-110">Klikněte na Způsoby platby.</span><span class="sxs-lookup"><span data-stu-id="de853-110">Click Payment methods.</span></span>
6. <span data-ttu-id="de853-111">Rozbalte nebo sbalte oddíl zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="de853-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="de853-112">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="de853-112">Click Edit.</span></span>
    * <span data-ttu-id="de853-113">Určete, zda mají být přijaté částky pro tento způsob zaúčtovány na účet hlavní knihy nebo bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="de853-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="de853-114">Vyberte účet, kam mají být zaúčtovány částky přijaté pro tento způsob platby.</span><span class="sxs-lookup"><span data-stu-id="de853-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="de853-115">Vyberte účet pro zaúčtování možných rozdílů mezi celkovou přijatou částkou transakce a částkou, která byla započtena pro tento způsob platby.</span><span class="sxs-lookup"><span data-stu-id="de853-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="de853-116">V tomto poli můžete zadat částku pro určení, kdy má být částka rozdílu zaúčtována na jiný účet rozdílů.</span><span class="sxs-lookup"><span data-stu-id="de853-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="de853-117">To slouží ke sledování velkých rozdílů.</span><span class="sxs-lookup"><span data-stu-id="de853-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="de853-118">Vyberte účet, který chcete zaúčtovat možné rozdíly mezi celkovou přijatou částkou transakce a vypočtenou částkou, když překročí hodnotu, která je definována v poli „Maximální částka rozdílu“.</span><span class="sxs-lookup"><span data-stu-id="de853-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="de853-119">Vyberte možnost „Ano“ pro zaúčtování částek pro odvod do banky na samostatný účet.</span><span class="sxs-lookup"><span data-stu-id="de853-119">Select "Yes" to post bank drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="de853-120">V tomto poli můžete vybrat, zda částky pro odvod do banky mají být zaúčtovány na účet hlavní knihy nebo bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="de853-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="de853-121">Vyberte účet, kam se mají zaúčtovat částky pro odvod do banky.</span><span class="sxs-lookup"><span data-stu-id="de853-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="de853-122">Vyberte typ bankovní transakce, který se má použít při zaúčtování částek pro odvod do banky na bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="de853-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="de853-123">Vyberte možnost „Ano“ pro zaúčtování částek pro odvod do trezoru na samostatný účet.</span><span class="sxs-lookup"><span data-stu-id="de853-123">Select "Yes" to post safe drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="de853-124">Vyberte, zda částky pro odvod do trezoru mají být zaúčtovány na účet hlavní knihy nebo bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="de853-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="de853-125">Vyberte účet, kam se mají zaúčtovat částky pro odvod do trezoru.</span><span class="sxs-lookup"><span data-stu-id="de853-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="de853-126">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="de853-126">Click Save.</span></span>

