---
title: Nastavení zařízení banky a zaúčtování profilů pro záruční listiny
description: Tato úloha vytvoří bankovní zařízení a účetní profil potřebný pro zpracování záruční listiny.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff5402b11cd2ccdfde2881268d9cd936947cd77e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441223"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="35513-103">Nastavení zařízení banky a zaúčtování profilů pro záruční listiny</span><span class="sxs-lookup"><span data-stu-id="35513-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="35513-104">Tato úloha vytvoří bankovní zařízení a účetní profil potřebný pro zpracování záruční listiny.</span><span class="sxs-lookup"><span data-stu-id="35513-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="35513-105">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="35513-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="35513-106">Parametr hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="35513-106">General ledger parameter</span></span>
1. <span data-ttu-id="35513-107">Přejděte do nabídky Pokladna a banka > Nastavení > Parametry pokladny a banky.</span><span class="sxs-lookup"><span data-stu-id="35513-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="35513-108">Rozbalte oddíl Bankovní dokument.</span><span class="sxs-lookup"><span data-stu-id="35513-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="35513-109">Vyberte možnost Povolit záruční listinu.</span><span class="sxs-lookup"><span data-stu-id="35513-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="35513-110">V poli Deník transakce kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="35513-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="35513-111">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="35513-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="35513-112">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="35513-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="35513-113">Klikněte na kartu Číselné řady.</span><span class="sxs-lookup"><span data-stu-id="35513-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="35513-114">Definování kódu číselné řady pro číslo záruční listiny záruční a odkazy na transakce záruční listiny</span><span class="sxs-lookup"><span data-stu-id="35513-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="35513-115">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="35513-115">Click Save.</span></span>
9. <span data-ttu-id="35513-116">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="35513-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="35513-117">Vytvoření bankovního zařízení</span><span class="sxs-lookup"><span data-stu-id="35513-117">Create Bank facility</span></span>
1. <span data-ttu-id="35513-118">Přejděte do nabídky Pokladna a banka > Nastavení > Bankovní zařízení.</span><span class="sxs-lookup"><span data-stu-id="35513-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="35513-119">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="35513-119">Click New.</span></span>
3. <span data-ttu-id="35513-120">V poli Skupina zařízení zadejte název skupiny bankovních zařízení pro transakci záruční listiny.</span><span class="sxs-lookup"><span data-stu-id="35513-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="35513-121">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="35513-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="35513-122">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="35513-122">Click Save.</span></span>
6. <span data-ttu-id="35513-123">Klikněte na kartu Typy zařízení.</span><span class="sxs-lookup"><span data-stu-id="35513-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="35513-124">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="35513-124">Click New.</span></span>
8. <span data-ttu-id="35513-125">V poli Typ zařízení zadejte název typu bankovního zařízení, který se vztahuje se k zařízení smlouvy bankovního zařízení.</span><span class="sxs-lookup"><span data-stu-id="35513-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="35513-126">Zadejte hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="35513-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="35513-127">V poli Skupina zařízení kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="35513-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="35513-128">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="35513-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="35513-129">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="35513-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="35513-130">Vyberte možnost v poli Druh zařízení.</span><span class="sxs-lookup"><span data-stu-id="35513-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="35513-131">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="35513-131">Click Save.</span></span>
15. <span data-ttu-id="35513-132">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="35513-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="35513-133">Účetní profil banky</span><span class="sxs-lookup"><span data-stu-id="35513-133">Bank posting profile</span></span>
1. <span data-ttu-id="35513-134">Přejděte do nabídky Pokladna a banka > Nastavení > Profil účtování bankovních dokumentů.</span><span class="sxs-lookup"><span data-stu-id="35513-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="35513-135">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="35513-135">Click New.</span></span>
3. <span data-ttu-id="35513-136">V poli Číslo účtu/skupiny kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="35513-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="35513-137">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="35513-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="35513-138">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="35513-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="35513-139">V poli Účet vyrovnání vyberte hlavní účet pro vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="35513-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="35513-140">V poli Poplatkový účet vyberte účet pro výdajové transakce.</span><span class="sxs-lookup"><span data-stu-id="35513-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="35513-141">V poli Maržový účet vyberte účet pro transakci marže.</span><span class="sxs-lookup"><span data-stu-id="35513-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="35513-142">V poli Účet likvidace vyberte účet likvidace pro transakci záruční listiny.</span><span class="sxs-lookup"><span data-stu-id="35513-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="35513-143">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="35513-143">Click Save.</span></span>
11. <span data-ttu-id="35513-144">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="35513-144">Close the page.</span></span>

