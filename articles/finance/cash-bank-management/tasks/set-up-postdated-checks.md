---
title: Nastavení postdatovaných šeků
description: Toto téma vysvětluje, jak určit, zda se mají zaúčtovat položky deníku pro postdatované šeky a které účetní deníky se mají použít pro vymazání položek a plateb dodavatele.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0d4afd74f9a0f9018629fa92ab6595bfa94f973
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026198"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="2995f-103">Nastavení postdatovaných šeků</span><span class="sxs-lookup"><span data-stu-id="2995f-103">Set up postdated checks</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2995f-104">Toto téma vysvětluje, jak určit, zda se mají zaúčtovat položky deníku pro postdatované šeky a které účetní deníky se mají použít pro vymazání položek a plateb dodavatele.</span><span class="sxs-lookup"><span data-stu-id="2995f-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="2995f-105">Můžete také určit clearingové účty pro vydané šeky, přijaté šeky a srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="2995f-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="2995f-106">Postdatované šeky jsou vydány za účelem provedení a přijetí platby v budoucí datu.</span><span class="sxs-lookup"><span data-stu-id="2995f-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="2995f-107">Můžete zadat, zda se má šek odrazit ve vašich účetních knihách před datem splatnosti.</span><span class="sxs-lookup"><span data-stu-id="2995f-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="2995f-108">Role tohoto postupu je Pokladník.</span><span class="sxs-lookup"><span data-stu-id="2995f-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="2995f-109">Tato procedura používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="2995f-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="2995f-110">Nastavení postdatovaných šeků</span><span class="sxs-lookup"><span data-stu-id="2995f-110">Set up postdated checks</span></span>
1. <span data-ttu-id="2995f-111">Přejděte do nabídky Pokladna a banka > Nastavení > Parametry pokladny a banky.</span><span class="sxs-lookup"><span data-stu-id="2995f-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="2995f-112">Klikněte na kartu Postdatované šeky.</span><span class="sxs-lookup"><span data-stu-id="2995f-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="2995f-113">Zaškrtněte políčko Povolit postdatované šeky nebo jeho zaškrtnutí zrušte.</span><span class="sxs-lookup"><span data-stu-id="2995f-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="2995f-114">Zaškrtněte políčko Zaúčtovat položky deníku pro postdatované šeky nebo jeho zaškrtnutí zrušte.</span><span class="sxs-lookup"><span data-stu-id="2995f-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="2995f-115">V poli Clearingový účet pro vydané šeky zadejte požadované hodnoty.</span><span class="sxs-lookup"><span data-stu-id="2995f-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="2995f-116">V poli Clearingový účet pro přijaté šeky zadejte požadované hodnoty.</span><span class="sxs-lookup"><span data-stu-id="2995f-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="2995f-117">V poli Hlavní deník pro položky clearingu zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2995f-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="2995f-118">V poli Přenést postdatované šeky do tohoto deníku plateb dodavatelů zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2995f-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="2995f-119">Zadejte požadované hodnoty do pole Clearingový účet srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="2995f-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="2995f-120">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="2995f-120">Click Save.</span></span>
11. <span data-ttu-id="2995f-121">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2995f-121">Close the page.</span></span>
12. <span data-ttu-id="2995f-122">Přejděte do nabídky Závazky > Nastavení platby > Metody platby.</span><span class="sxs-lookup"><span data-stu-id="2995f-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="2995f-123">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="2995f-123">Click New.</span></span>
14. <span data-ttu-id="2995f-124">V poli Způsob platby zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2995f-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="2995f-125">Zvolením možnosti Clearingové zaúčtování postdatovaných šeků určete, že je částka šeku zaúčtována na clearingový účet.</span><span class="sxs-lookup"><span data-stu-id="2995f-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="2995f-126">V poli Typ účtu vyberte „Banka“.</span><span class="sxs-lookup"><span data-stu-id="2995f-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="2995f-127">Pole pro protiúčet způsobu platby bude prázdné.</span><span class="sxs-lookup"><span data-stu-id="2995f-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="2995f-128">Zadejte požadované hodnoty do pole Platební účet.</span><span class="sxs-lookup"><span data-stu-id="2995f-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="2995f-129">Vyberte bankovní účet, který se používá k odečtu částky faktury.</span><span class="sxs-lookup"><span data-stu-id="2995f-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="2995f-130">Klikněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="2995f-130">Click Save.</span></span>
19. <span data-ttu-id="2995f-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2995f-131">Close the page.</span></span>
> [!NOTE]
> <span data-ttu-id="2995f-132">Abyste mohli odeslat šek po datu splatnosti na bankovní účet, když je datum relace větší nebo rovno datu splatnosti, musíte povolit funkci **Ověření data splatnosti zaúčtování deníku plateb s postdatovanými šeky na bankovní účet**.</span><span class="sxs-lookup"><span data-stu-id="2995f-132">To be able to post a postdated check to a bank account when the session date is greater than or equal to the maturity date, you must enable the feature **Maturity date validation of posting payment journal with postdated checks to bank account**.</span></span> <span data-ttu-id="2995f-133">Tato funkce umožňuje účtovat deníky plateb pro dodavatele nebo zákazníky s postdatovanými šeky, když je datum relace větší nebo rovno datu splatnosti.</span><span class="sxs-lookup"><span data-stu-id="2995f-133">This feature allows you to post payment journals for vendors or customers with postdated checks, when the session date is greater than or equal to the maturity date.</span></span>
> 
> <span data-ttu-id="2995f-134">Při nastavování **Způsobu platby** (**Závazky> Nastavení platby > Způsoby platby**) nevyplňujte **Překlenovací účet**.</span><span class="sxs-lookup"><span data-stu-id="2995f-134">When setting the **Method of payment** (**Accounts payable > Payment setup > Methods of payment**), do not fill in **Bridging account**.</span></span> <span data-ttu-id="2995f-135">V tomto případě je offsetový účet vyplněn bankovním účtem, který je nastaven ve **Způsobu platby**.</span><span class="sxs-lookup"><span data-stu-id="2995f-135">In this case, the offset account is filled in with the bank account, which is set up in the **Method of payment**.</span></span>
>  
> <span data-ttu-id="2995f-136">Pokud je funkce povolena a datum relace je menší než datum splatnosti, zobrazí se při zaúčtování deníku plateb následující chybová zpráva: „Datum splatnosti musí být menší nebo rovno datu relace, pokud je typ offsetového účtu Banka“.</span><span class="sxs-lookup"><span data-stu-id="2995f-136">When the feature is enabled and the session date is less than the maturity date, the following error message is displayed when posting a payment journal, "Maturity date must be less or equal to the session date if offset account type is Bank".</span></span> <span data-ttu-id="2995f-137">Pokud tato funkce není povolena, můžete zaúčtovat deník plateb s postdatovaným šekem, když je datum relace menší než datum splatnosti.</span><span class="sxs-lookup"><span data-stu-id="2995f-137">If the feature is not enabled, you can post a payment journal with a postdated check when the session date is less than the maturity date.</span></span>    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
