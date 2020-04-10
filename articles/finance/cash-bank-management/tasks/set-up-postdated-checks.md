---
title: Nastavení postdatovaných šeků
description: Toto téma vysvětluje, jak určit, zda se mají zaúčtovat položky deníku pro postdatované šeky a které účetní deníky se mají použít pro vymazání položek a plateb dodavatele.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22e67aa051b5ea8267df7efac40e007d0f11a83d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141101"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="4870d-103">Nastavení postdatovaných šeků</span><span class="sxs-lookup"><span data-stu-id="4870d-103">Set up postdated checks</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4870d-104">Toto téma vysvětluje, jak určit, zda se mají zaúčtovat položky deníku pro postdatované šeky a které účetní deníky se mají použít pro vymazání položek a plateb dodavatele.</span><span class="sxs-lookup"><span data-stu-id="4870d-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="4870d-105">Můžete také určit clearingové účty pro vydané šeky, přijaté šeky a srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="4870d-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="4870d-106">Postdatované šeky jsou vydány za účelem provedení a přijetí platby v budoucí datu.</span><span class="sxs-lookup"><span data-stu-id="4870d-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="4870d-107">Můžete zadat, zda se má šek odrazit ve vašich účetních knihách před datem splatnosti.</span><span class="sxs-lookup"><span data-stu-id="4870d-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="4870d-108">Role tohoto postupu je Pokladník.</span><span class="sxs-lookup"><span data-stu-id="4870d-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="4870d-109">Tato procedura používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="4870d-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="4870d-110">Nastavení postdatovaných šeků</span><span class="sxs-lookup"><span data-stu-id="4870d-110">Set up postdated checks</span></span>
1. <span data-ttu-id="4870d-111">Přejděte do nabídky Pokladna a banka > Nastavení > Parametry pokladny a banky.</span><span class="sxs-lookup"><span data-stu-id="4870d-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="4870d-112">Klikněte na kartu Postdatované šeky.</span><span class="sxs-lookup"><span data-stu-id="4870d-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="4870d-113">Zaškrtněte políčko Povolit postdatované šeky nebo jeho zaškrtnutí zrušte.</span><span class="sxs-lookup"><span data-stu-id="4870d-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="4870d-114">Zaškrtněte políčko Zaúčtovat položky deníku pro postdatované šeky nebo jeho zaškrtnutí zrušte.</span><span class="sxs-lookup"><span data-stu-id="4870d-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="4870d-115">V poli Clearingový účet pro vydané šeky zadejte požadované hodnoty.</span><span class="sxs-lookup"><span data-stu-id="4870d-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="4870d-116">V poli Clearingový účet pro přijaté šeky zadejte požadované hodnoty.</span><span class="sxs-lookup"><span data-stu-id="4870d-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="4870d-117">V poli Hlavní deník pro položky clearingu zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4870d-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="4870d-118">V poli Přenést postdatované šeky do tohoto deníku plateb dodavatelů zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4870d-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="4870d-119">Zadejte požadované hodnoty do pole Clearingový účet srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="4870d-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="4870d-120">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="4870d-120">Click Save.</span></span>
11. <span data-ttu-id="4870d-121">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4870d-121">Close the page.</span></span>
12. <span data-ttu-id="4870d-122">Přejděte do nabídky Závazky > Nastavení platby > Metody platby.</span><span class="sxs-lookup"><span data-stu-id="4870d-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="4870d-123">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="4870d-123">Click New.</span></span>
14. <span data-ttu-id="4870d-124">V poli Způsob platby zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4870d-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="4870d-125">Zvolením možnosti Clearingové zaúčtování postdatovaných šeků určete, že je částka šeku zaúčtována na clearingový účet.</span><span class="sxs-lookup"><span data-stu-id="4870d-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="4870d-126">V poli Typ účtu vyberte „Banka“.</span><span class="sxs-lookup"><span data-stu-id="4870d-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="4870d-127">Pole pro protiúčet způsobu platby bude prázdné.</span><span class="sxs-lookup"><span data-stu-id="4870d-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="4870d-128">Zadejte požadované hodnoty do pole Platební účet.</span><span class="sxs-lookup"><span data-stu-id="4870d-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="4870d-129">Vyberte bankovní účet, který se používá k odečtu částky faktury.</span><span class="sxs-lookup"><span data-stu-id="4870d-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="4870d-130">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="4870d-130">Click Save.</span></span>
19. <span data-ttu-id="4870d-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4870d-131">Close the page.</span></span>

