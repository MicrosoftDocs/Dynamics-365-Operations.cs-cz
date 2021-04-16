---
title: Nastavení bankovních účtů odběratelů a zákazníků pro přímé debety ve formátu ISO20022
description: Tato úloha vás provede nastavením bankovního účtu odběratele a zmocněním k přímému debetu odběratele, které jsou požadovány pro generování souboru plateb odběratele pro přímý debet ISO20022.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 78523e6f221973194560466e006639f4bb53614b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819499"
---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="34c9c-103">Nastavení bankovních účtů odběratelů a zákazníků pro přímé debety ve formátu ISO20022</span><span class="sxs-lookup"><span data-stu-id="34c9c-103">Set up customers and customer bank accounts for ISO20022 direct debits</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34c9c-104">Tato úloha vás provede nastavením bankovního účtu odběratele a zmocněním k přímému debetu odběratele, které jsou požadovány pro generování souboru plateb odběratele pro přímý debet ISO20022.</span><span class="sxs-lookup"><span data-stu-id="34c9c-104">This task walks you through setting up a customer bank account and a customer direct debit mandate which are required to generate the customer payment file like ISO20022 direct debit.</span></span> <span data-ttu-id="34c9c-105">V závislosti na formátech platby odběratele, které jsou nastavené, mohou být pro odběratele nebo bankovní účet odběratele potřeba další informace, které nejsou zahrnuty v tomto postupu.</span><span class="sxs-lookup"><span data-stu-id="34c9c-105">Depending on the customer payment formats tha are set up, additional information, not covered in this procedure, might be required for a customer or a customer bank account.</span></span> 

<span data-ttu-id="34c9c-106">Tento úkol byl vytvořen za použití ukázkových dat společnosti DEMF s primární adresou právnické osoby v Německu.</span><span class="sxs-lookup"><span data-stu-id="34c9c-106">This task was created using the demo data company DEMF with a legal entity primary address in Germany.</span></span>



<span data-ttu-id="34c9c-107">Toto je čtvrtý z pěti postupů, které společně popisují proces platby odběratele pomocí konfigurací elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="34c9c-107">This is the fourth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-a-customer-bank-account"></a><span data-ttu-id="34c9c-108">Nastavení bankovního účtu odběratele</span><span class="sxs-lookup"><span data-stu-id="34c9c-108">Set up a customer bank account</span></span>
1. <span data-ttu-id="34c9c-109">Přejděte na Pohledávky > Zákazníci > Všichni odběratelé.</span><span class="sxs-lookup"><span data-stu-id="34c9c-109">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="34c9c-110">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="34c9c-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="34c9c-111">V poli Účet můžete například filtrovat pomocí hodnoty „DE-010“.</span><span class="sxs-lookup"><span data-stu-id="34c9c-111">For example, filter on the Account field with a value of 'DE-010 '.</span></span>
3. <span data-ttu-id="34c9c-112">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="34c9c-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="34c9c-113">V podokně akcí klikněte na možnost Odběratel.</span><span class="sxs-lookup"><span data-stu-id="34c9c-113">On the Action Pane, click Customer.</span></span>
5. <span data-ttu-id="34c9c-114">Klikněte na možnost Bankovní účty.</span><span class="sxs-lookup"><span data-stu-id="34c9c-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="34c9c-115">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="34c9c-115">Click New.</span></span>
7. <span data-ttu-id="34c9c-116">Zadejte hodnotu do pole Bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="34c9c-116">In the Bank account field, type a value.</span></span>
8. <span data-ttu-id="34c9c-117">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="34c9c-117">In the Name field, type a value.</span></span>
    * <span data-ttu-id="34c9c-118">Zadejte například banka EUR.</span><span class="sxs-lookup"><span data-stu-id="34c9c-118">For example, enter 'EUR bank'.</span></span>  
9. <span data-ttu-id="34c9c-119">V poli Bankovní skupiny zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="34c9c-119">In the Bank groups field, enter or select a value.</span></span>
10. <span data-ttu-id="34c9c-120">Zadejte hodnotu do pole IBAN.</span><span class="sxs-lookup"><span data-stu-id="34c9c-120">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="34c9c-121">Zadejte například DE36200400000628808808.</span><span class="sxs-lookup"><span data-stu-id="34c9c-121">For example, enter 'DE36200400000628808808'.</span></span>  
11. <span data-ttu-id="34c9c-122">V poli Kód SWIFT zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="34c9c-122">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="34c9c-123">Například zadejte COBADEFFXXX.</span><span class="sxs-lookup"><span data-stu-id="34c9c-123">For example: Enter 'COBADEFFXXX'.</span></span>  <span data-ttu-id="34c9c-124">Všimněte si, že pro spoustu formátů platby není povinný SWIFT\BIC, doporučujeme ho však pro bankovní účet zaregistrovat.</span><span class="sxs-lookup"><span data-stu-id="34c9c-124">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
12. <span data-ttu-id="34c9c-125">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="34c9c-125">Click Save.</span></span>
13. <span data-ttu-id="34c9c-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="34c9c-126">Close the page.</span></span>
14. <span data-ttu-id="34c9c-127">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="34c9c-127">Click Edit.</span></span>
15. <span data-ttu-id="34c9c-128">Rozbalte položku Výchozí nastavení plateb.</span><span class="sxs-lookup"><span data-stu-id="34c9c-128">Expand the Payment defaults section.</span></span>
16. <span data-ttu-id="34c9c-129">V poli Bankovní účet zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="34c9c-129">In the Bank account field, enter or select a value.</span></span>

## <a name="add-a-direct-debit-mandate"></a><span data-ttu-id="34c9c-130">Přidání zmocnění k přímému debetu</span><span class="sxs-lookup"><span data-stu-id="34c9c-130">Add a direct debit mandate</span></span>
1. <span data-ttu-id="34c9c-131">Rozbalte část Zmocnění k přímému debetu.</span><span class="sxs-lookup"><span data-stu-id="34c9c-131">Expand the Direct debit mandates section.</span></span>
2. <span data-ttu-id="34c9c-132">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="34c9c-132">Click Add.</span></span>
3. <span data-ttu-id="34c9c-133">V poli Bankovní účet věřitele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="34c9c-133">In the Creditor bank account field, enter or select a value.</span></span>
    * <span data-ttu-id="34c9c-134">Vyberte například DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="34c9c-134">For example, select DEMF OPER.</span></span>  
4. <span data-ttu-id="34c9c-135">Do pole Datum podpisu zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="34c9c-135">In the Signature date field, enter a date.</span></span>
5. <span data-ttu-id="34c9c-136">Klepnutím na tlačítko Ano dojde k potvrzení aktualizace data.</span><span class="sxs-lookup"><span data-stu-id="34c9c-136">Click Yes to confirm the date update.</span></span>
6. <span data-ttu-id="34c9c-137">V poli Místo podpisu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="34c9c-137">In the Signature location field, enter or select a value.</span></span>
7. <span data-ttu-id="34c9c-138">Do pole Očekávaný počet plateb zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="34c9c-138">In the Expected number of payments field, enter a number.</span></span>
8. <span data-ttu-id="34c9c-139">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="34c9c-139">Click OK.</span></span>
9. <span data-ttu-id="34c9c-140">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="34c9c-140">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]