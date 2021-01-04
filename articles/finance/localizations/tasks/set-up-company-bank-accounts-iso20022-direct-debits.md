---
title: Nastavení bankovních účtů společnosti pro přímé debety ve formátu ISO20022
description: Tato úloha vás provede nastavením informací o bankovním účtu společnosti potřebném pro generování souborů platby dodavatele.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 652d8aa8f78d9a12ee390d23904f2c94d9bcf684
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441078"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="e106b-103">Nastavení bankovních účtů společnosti pro přímé debety ve formátu ISO20022</span><span class="sxs-lookup"><span data-stu-id="e106b-103">Set up company bank accounts for ISO20022 direct debits</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e106b-104">Tato úloha vás provede nastavením informací o bankovním účtu společnosti potřebném pro generování souborů platby dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e106b-104">This task walks you through setting up the company specific bank account information that is required for generating customer payment files.</span></span> <span data-ttu-id="e106b-105">Tento postup používá jako příklad formát přímého debetu ISO 20022.</span><span class="sxs-lookup"><span data-stu-id="e106b-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> <span data-ttu-id="e106b-106">Jiné formáty mohou vyžadovat další informace o nastavení jako ID společnosti nebo Třídicí kód.</span><span class="sxs-lookup"><span data-stu-id="e106b-106">Other formats might require additional setup information like the Company ID or the Sort code.</span></span>



<span data-ttu-id="e106b-107">Tento úkol byl vytvořen pomocí ukázkových dat společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="e106b-107">This task was created using the demo data company DEMF.</span></span>



<span data-ttu-id="e106b-108">Toto je druhý z pěti postupů, které společně popisují proces platby odběratele pomocí konfigurací elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="e106b-108">This is the second of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-the-iban-and-swift-codes"></a><span data-ttu-id="e106b-109">Nastavení kódů IBAN a SWIFT</span><span class="sxs-lookup"><span data-stu-id="e106b-109">Set up the IBAN and SWIFT codes</span></span>
1. <span data-ttu-id="e106b-110">Přejděte do části Pokladna a banka > Bankovní účty.</span><span class="sxs-lookup"><span data-stu-id="e106b-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="e106b-111">Použijte rychlý filtr k filtrování v poli Bankovní účet s hodnotou 'DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="e106b-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="e106b-112">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e106b-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e106b-113">Příklad: kliknutím na DEMF OPER můžete otevřít podrobnosti o bankovním účtu.</span><span class="sxs-lookup"><span data-stu-id="e106b-113">For example, click 'DEMF OPER' to open the bank account details.</span></span>  
4. <span data-ttu-id="e106b-114">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="e106b-114">Click Edit.</span></span>
5. <span data-ttu-id="e106b-115">Rozbalte nebo sbalte oddíl Další identifikace.</span><span class="sxs-lookup"><span data-stu-id="e106b-115">Expand or collapse the Additional identification section.</span></span>
6. <span data-ttu-id="e106b-116">Zadejte hodnotu do pole IBAN.</span><span class="sxs-lookup"><span data-stu-id="e106b-116">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="e106b-117">Zadejte například DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="e106b-117">For example, enter 'DE89370400440532013000'.</span></span>  
7. <span data-ttu-id="e106b-118">V poli Kód SWIFT zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e106b-118">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="e106b-119">Zadejte například DEUTDEFF.</span><span class="sxs-lookup"><span data-stu-id="e106b-119">For example, enter 'DEUTDEFF'.</span></span>    <span data-ttu-id="e106b-120">Všimněte si, že pro spoustu formátů platby není povinný SWIFT\BIC, doporučujeme ho však pro bankovní účet zaregistrovat.</span><span class="sxs-lookup"><span data-stu-id="e106b-120">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="e106b-121">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e106b-121">Click Save.</span></span>

## <a name="set-up-a-bank-account-for-the-legal-entity"></a><span data-ttu-id="e106b-122">Nastavení bankovního účtu pro právnickou osobu</span><span class="sxs-lookup"><span data-stu-id="e106b-122">Set up a bank account for the legal entity</span></span>
1. <span data-ttu-id="e106b-123">Přejděte do části na Správa organizace > Organizace > Právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="e106b-123">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="e106b-124">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="e106b-124">Click Edit.</span></span>
3. <span data-ttu-id="e106b-125">Rozbalte nebo sbalte oddíl Informace o bankovním účtu.</span><span class="sxs-lookup"><span data-stu-id="e106b-125">Expand or collapse the Bank account information section.</span></span>
4. <span data-ttu-id="e106b-126">V poli Bankovní účet kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="e106b-126">In the Bank account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e106b-127">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e106b-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e106b-128">Příklad: vyberte bankovní účet DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="e106b-128">For example, select the "DEMF OPER" bank account.</span></span>  
6. <span data-ttu-id="e106b-129">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e106b-129">Click Save.</span></span>

