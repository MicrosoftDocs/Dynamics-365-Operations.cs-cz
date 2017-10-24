--- 
title: "Nastavení bankovních účtů odběratelů a zákazníků pro přímé debety ve formátu ISO20022"
description: "Tato úloha vás provede nastavením bankovního účtu odběratele a zmocněním k přímému debetu odběratele, které jsou požadovány pro generování souboru plateb odběratele pro přímý debet ISO20022."
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 5b4652b76e089d6beb2ce1513d06cf07a5ea3195
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="780a7-103">Nastavení bankovních účtů odběratelů a zákazníků pro přímé debety ve formátu ISO20022</span><span class="sxs-lookup"><span data-stu-id="780a7-103">Set up customers and customer bank accounts for ISO20022 direct debits</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="780a7-104">Tato úloha vás provede nastavením bankovního účtu odběratele a zmocněním k přímému debetu odběratele, které jsou požadovány pro generování souboru plateb odběratele pro přímý debet ISO20022.</span><span class="sxs-lookup"><span data-stu-id="780a7-104">This task walks you through setting up a customer bank account and a customer direct debit mandate which are required to generate the customer payment file like ISO20022 direct debit.</span></span> <span data-ttu-id="780a7-105">V závislosti na formátech platby odběratele, které jsou nastavené, mohou být pro odběratele nebo bankovní účet odběratele potřeba další informace, které nejsou zahrnuty v tomto postupu.</span><span class="sxs-lookup"><span data-stu-id="780a7-105">Depending on the customer payment formats tha are set up, additional information, not covered in this procedure, might be required for a customer or a customer bank account.</span></span> 

<span data-ttu-id="780a7-106">Tento úkol byl vytvořen za použití ukázkových dat společnosti DEMF s primární adresou právnické osoby v Německu.</span><span class="sxs-lookup"><span data-stu-id="780a7-106">This task was created using the demo data company DEMF with a legal entity primary address in Germany.</span></span>



<span data-ttu-id="780a7-107">Toto je čtvrtý z pěti postupů, které společně popisují proces platby odběratele pomocí konfigurací elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="780a7-107">This is the fourth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-a-customer-bank-account"></a><span data-ttu-id="780a7-108">Nastavení bankovního účtu odběratele</span><span class="sxs-lookup"><span data-stu-id="780a7-108">Set up a customer bank account</span></span>
1. <span data-ttu-id="780a7-109">Přejděte na Pohledávky > Zákazníci > Všichni odběratelé.</span><span class="sxs-lookup"><span data-stu-id="780a7-109">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="780a7-110">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="780a7-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="780a7-111">V poli Účet můžete například filtrovat pomocí hodnoty „DE-010“.</span><span class="sxs-lookup"><span data-stu-id="780a7-111">For example, filter on the Account field with a value of 'DE-010 '.</span></span>
3. <span data-ttu-id="780a7-112">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="780a7-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="780a7-113">V podokně akcí klikněte na možnost Odběratel.</span><span class="sxs-lookup"><span data-stu-id="780a7-113">On the Action Pane, click Customer.</span></span>
5. <span data-ttu-id="780a7-114">Klikněte na možnost Bankovní účty.</span><span class="sxs-lookup"><span data-stu-id="780a7-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="780a7-115">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="780a7-115">Click New.</span></span>
7. <span data-ttu-id="780a7-116">Zadejte hodnotu do pole Bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="780a7-116">In the Bank account field, type a value.</span></span>
8. <span data-ttu-id="780a7-117">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="780a7-117">In the Name field, type a value.</span></span>
    * <span data-ttu-id="780a7-118">Zadejte například banka EUR.</span><span class="sxs-lookup"><span data-stu-id="780a7-118">For example, enter 'EUR bank'.</span></span>  
9. <span data-ttu-id="780a7-119">V poli Bankovní skupiny zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="780a7-119">In the Bank groups field, enter or select a value.</span></span>
10. <span data-ttu-id="780a7-120">Zadejte hodnotu do pole IBAN.</span><span class="sxs-lookup"><span data-stu-id="780a7-120">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="780a7-121">Zadejte například DE36200400000628808808.</span><span class="sxs-lookup"><span data-stu-id="780a7-121">For example, enter 'DE36200400000628808808'.</span></span>  
11. <span data-ttu-id="780a7-122">V poli Kód SWIFT zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="780a7-122">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="780a7-123">Například zadejte COBADEFFXXX.</span><span class="sxs-lookup"><span data-stu-id="780a7-123">For example: Enter 'COBADEFFXXX'.</span></span>  <span data-ttu-id="780a7-124">Všimněte si, že pro spoustu formátů platby není povinný SWIFT\BIC, doporučujeme ho však pro bankovní účet zaregistrovat.</span><span class="sxs-lookup"><span data-stu-id="780a7-124">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
12. <span data-ttu-id="780a7-125">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="780a7-125">Click Save.</span></span>
13. <span data-ttu-id="780a7-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="780a7-126">Close the page.</span></span>
14. <span data-ttu-id="780a7-127">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="780a7-127">Click Edit.</span></span>
15. <span data-ttu-id="780a7-128">Rozbalte položku Výchozí nastavení plateb.</span><span class="sxs-lookup"><span data-stu-id="780a7-128">Expand the Payment defaults section.</span></span>
16. <span data-ttu-id="780a7-129">V poli Bankovní účet zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="780a7-129">In the Bank account field, enter or select a value.</span></span>

## <a name="add-a-direct-debit-mandate"></a><span data-ttu-id="780a7-130">Přidání zmocnění k přímému debetu</span><span class="sxs-lookup"><span data-stu-id="780a7-130">Add a direct debit mandate</span></span>
1. <span data-ttu-id="780a7-131">Rozbalte část Zmocnění k přímému debetu.</span><span class="sxs-lookup"><span data-stu-id="780a7-131">Expand the Direct debit mandates section.</span></span>
2. <span data-ttu-id="780a7-132">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="780a7-132">Click Add.</span></span>
3. <span data-ttu-id="780a7-133">V poli Bankovní účet věřitele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="780a7-133">In the Creditor bank account field, enter or select a value.</span></span>
    * <span data-ttu-id="780a7-134">Vyberte například DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="780a7-134">For example, select DEMF OPER.</span></span>  
4. <span data-ttu-id="780a7-135">Do pole Datum podpisu zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="780a7-135">In the Signature date field, enter a date.</span></span>
5. <span data-ttu-id="780a7-136">Klepnutím na tlačítko Ano dojde k potvrzení aktualizace data.</span><span class="sxs-lookup"><span data-stu-id="780a7-136">Click Yes to confirm the date update.</span></span>
6. <span data-ttu-id="780a7-137">V poli Místo podpisu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="780a7-137">In the Signature location field, enter or select a value.</span></span>
7. <span data-ttu-id="780a7-138">Do pole Očekávaný počet plateb zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="780a7-138">In the Expected number of payments field, enter a number.</span></span>
8. <span data-ttu-id="780a7-139">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="780a7-139">Click OK.</span></span>
9. <span data-ttu-id="780a7-140">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="780a7-140">Click Save.</span></span>


