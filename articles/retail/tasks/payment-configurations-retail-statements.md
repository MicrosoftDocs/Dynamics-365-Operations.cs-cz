---
title: " Konfigurace plateb pro maloobchodní výkazy"
description: Tato procedura ukazuje konfigurace pro metody plateb maloobchodu, které ovlivní způsob pro vytváření a účtování výkazy maloobchodu.
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
ms.openlocfilehash: 8f49a3ae05d35b0f0ca6a08007f5b05321c1f5ab
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564263"
---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="9de36-103"> Konfigurace plateb pro maloobchodní výkazy</span><span class="sxs-lookup"><span data-stu-id="9de36-103">Payment configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9de36-104">Tato procedura ukazuje konfigurace pro metody plateb maloobchodu, které ovlivní způsob pro vytváření a účtování výkazy maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="9de36-104">This procedure demonstrates configurations for Retail store payment methods, which affect how Retail statements get created and posted.</span></span>

<span data-ttu-id="9de36-105">Tento záznam používá ukázkovou společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="9de36-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="9de36-106">Přejděte do nabídky Maloobchodní a velkoobchodní prodej > Kanály > Maloobchody > Všechny maloobchody.</span><span class="sxs-lookup"><span data-stu-id="9de36-106">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="9de36-107">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="9de36-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9de36-108">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="9de36-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9de36-109">V podokně akcí klikněte na možnost Nastavit.</span><span class="sxs-lookup"><span data-stu-id="9de36-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="9de36-110">Klikněte na Způsoby platby.</span><span class="sxs-lookup"><span data-stu-id="9de36-110">Click Payment methods.</span></span>
6. <span data-ttu-id="9de36-111">Rozbalte nebo sbalte oddíl zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="9de36-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="9de36-112">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="9de36-112">Click Edit.</span></span>
    * <span data-ttu-id="9de36-113">Určete, zda mají být přijaté částky pro tento způsob zaúčtovány na účet hlavní knihy nebo bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="9de36-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="9de36-114">Vyberte účet, kam mají být zaúčtovány částky přijaté pro tento způsob platby.</span><span class="sxs-lookup"><span data-stu-id="9de36-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="9de36-115">Vyberte účet pro zaúčtování možných rozdílů mezi celkovou přijatou částkou transakce a částkou, která byla započtena pro tento způsob platby.</span><span class="sxs-lookup"><span data-stu-id="9de36-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="9de36-116">V tomto poli můžete zadat částku pro určení, kdy má být částka rozdílu zaúčtována na jiný účet rozdílů.</span><span class="sxs-lookup"><span data-stu-id="9de36-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="9de36-117">To slouží ke sledování velkých rozdílů.</span><span class="sxs-lookup"><span data-stu-id="9de36-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="9de36-118">Vyberte účet, který chcete zaúčtovat možné rozdíly mezi celkovou přijatou částkou transakce a vypočtenou částkou, když překročí hodnotu, která je definována v poli „Maximální částka rozdílu“.</span><span class="sxs-lookup"><span data-stu-id="9de36-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="9de36-119">Vyberte možnost „Ano“ pro zaúčtování částek pro odvod do banky na samostatný účet.</span><span class="sxs-lookup"><span data-stu-id="9de36-119">Select "Yes" to post bank drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="9de36-120">V tomto poli můžete vybrat, zda částky pro odvod do banky mají být zaúčtovány na účet hlavní knihy nebo bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="9de36-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="9de36-121">Vyberte účet, kam se mají zaúčtovat částky pro odvod do banky.</span><span class="sxs-lookup"><span data-stu-id="9de36-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="9de36-122">Vyberte typ bankovní transakce, který se má použít při zaúčtování částek pro odvod do banky na bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="9de36-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="9de36-123">Vyberte možnost „Ano“ pro zaúčtování částek pro odvod do trezoru na samostatný účet.</span><span class="sxs-lookup"><span data-stu-id="9de36-123">Select "Yes" to post safe drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="9de36-124">Vyberte, zda částky pro odvod do trezoru mají být zaúčtovány na účet hlavní knihy nebo bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="9de36-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="9de36-125">Vyberte účet, kam se mají zaúčtovat částky pro odvod do trezoru.</span><span class="sxs-lookup"><span data-stu-id="9de36-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="9de36-126">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="9de36-126">Click Save.</span></span>

