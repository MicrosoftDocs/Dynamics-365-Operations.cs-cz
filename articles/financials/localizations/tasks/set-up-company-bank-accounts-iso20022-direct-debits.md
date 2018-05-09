--- 
title: "Nastavení bankovních účtů společnosti pro přímé debety ve formátu ISO20022"
description: "Tato úloha vás provede nastavením informací o bankovním účtu společnosti potřebném pro generování souborů platby dodavatele."
author: mrolecki
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1170f3f562e509d47fc07bb8a3662ec8e8356b50
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="fd13a-103">Nastavení bankovních účtů společnosti pro přímé debety ve formátu ISO20022</span><span class="sxs-lookup"><span data-stu-id="fd13a-103">Set up company bank accounts for ISO20022 direct debits</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fd13a-104">Tato úloha vás provede nastavením informací o bankovním účtu společnosti potřebném pro generování souborů platby dodavatele.</span><span class="sxs-lookup"><span data-stu-id="fd13a-104">This task walks you through setting up the company specific bank account information that is required for generating customer payment files.</span></span> <span data-ttu-id="fd13a-105">Tento postup používá jako příklad formát přímého debetu ISO 20022.</span><span class="sxs-lookup"><span data-stu-id="fd13a-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> <span data-ttu-id="fd13a-106">Jiné formáty mohou vyžadovat další informace o nastavení jako ID společnosti nebo Třídicí kód.</span><span class="sxs-lookup"><span data-stu-id="fd13a-106">Other formats might require additional setup information like the Company ID or the Sort code.</span></span>



<span data-ttu-id="fd13a-107">Tento úkol byl vytvořen pomocí ukázkových dat společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="fd13a-107">This task was created using the demo data company DEMF.</span></span>



<span data-ttu-id="fd13a-108">Toto je druhý z pěti postupů, které společně popisují proces platby odběratele pomocí konfigurací elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="fd13a-108">This is the second of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-the-iban-and-swift-codes"></a><span data-ttu-id="fd13a-109">Nastavení kódů IBAN a SWIFT</span><span class="sxs-lookup"><span data-stu-id="fd13a-109">Set up the IBAN and SWIFT codes</span></span>
1. <span data-ttu-id="fd13a-110">Přejděte do části Pokladna a banka > Bankovní účty.</span><span class="sxs-lookup"><span data-stu-id="fd13a-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="fd13a-111">Použijte rychlý filtr k filtrování v poli Bankovní účet s hodnotou 'DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="fd13a-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="fd13a-112">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="fd13a-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="fd13a-113">Příklad: kliknutím na DEMF OPER můžete otevřít podrobnosti o bankovním účtu.</span><span class="sxs-lookup"><span data-stu-id="fd13a-113">For example, click 'DEMF OPER' to open the bank account details.</span></span>  
4. <span data-ttu-id="fd13a-114">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="fd13a-114">Click Edit.</span></span>
5. <span data-ttu-id="fd13a-115">Rozbalte nebo sbalte oddíl Další identifikace.</span><span class="sxs-lookup"><span data-stu-id="fd13a-115">Expand or collapse the Additional identification section.</span></span>
6. <span data-ttu-id="fd13a-116">Zadejte hodnotu do pole IBAN.</span><span class="sxs-lookup"><span data-stu-id="fd13a-116">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="fd13a-117">Zadejte například DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="fd13a-117">For example, enter 'DE89370400440532013000'.</span></span>  
7. <span data-ttu-id="fd13a-118">V poli Kód SWIFT zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fd13a-118">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="fd13a-119">Zadejte například DEUTDEFF.</span><span class="sxs-lookup"><span data-stu-id="fd13a-119">For example, enter 'DEUTDEFF'.</span></span>    <span data-ttu-id="fd13a-120">Všimněte si, že pro spoustu formátů platby není povinný SWIFT\BIC, doporučujeme ho však pro bankovní účet zaregistrovat.</span><span class="sxs-lookup"><span data-stu-id="fd13a-120">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="fd13a-121">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="fd13a-121">Click Save.</span></span>

## <a name="set-up-a-bank-account-for-the-legal-entity"></a><span data-ttu-id="fd13a-122">Nastavení bankovního účtu pro právnickou osobu</span><span class="sxs-lookup"><span data-stu-id="fd13a-122">Set up a bank account for the legal entity</span></span>
1. <span data-ttu-id="fd13a-123">Přejděte do části na Správa organizace > Organizace > Právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="fd13a-123">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="fd13a-124">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="fd13a-124">Click Edit.</span></span>
3. <span data-ttu-id="fd13a-125">Rozbalte nebo sbalte oddíl Informace o bankovním účtu.</span><span class="sxs-lookup"><span data-stu-id="fd13a-125">Expand or collapse the Bank account information section.</span></span>
4. <span data-ttu-id="fd13a-126">V poli Bankovní účet kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="fd13a-126">In the Bank account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="fd13a-127">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="fd13a-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="fd13a-128">Příklad: vyberte bankovní účet DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="fd13a-128">For example, select the "DEMF OPER" bank account.</span></span>  
6. <span data-ttu-id="fd13a-129">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="fd13a-129">Click Save.</span></span>


