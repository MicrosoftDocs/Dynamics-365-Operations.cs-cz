---
title: Nastavení zařízení banky a zaúčtování profilů pro akreditiv
description: Tento postup vás provede vytvořením bankovního zařízení a účetního profilu potřebného pro zpracování akreditivu.
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
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7e72847b9046968c87d9602e141bae6c603c1c63
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976314"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a><span data-ttu-id="53a44-103">Nastavení zařízení banky a zaúčtování profilů pro akreditiv</span><span class="sxs-lookup"><span data-stu-id="53a44-103">Set up bank facilities and posting profiles for letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="53a44-104">Tento postup vás provede vytvořením bankovního zařízení a účetního profilu potřebného pro zpracování akreditivu.</span><span class="sxs-lookup"><span data-stu-id="53a44-104">This procedure walks through creating a Bank facility and posting profile required to process Letters of credit.</span></span> 

<span data-ttu-id="53a44-105">Tento úkol využívá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="53a44-105">This tasks uses the demo company 'USMF'.</span></span>






## <a name="general-ledger-parameter"></a><span data-ttu-id="53a44-106">Parametr hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="53a44-106">General ledger parameter</span></span>
1. <span data-ttu-id="53a44-107">Přejděte do nabídky Pokladna a banka > Nastavení > Parametry pokladny a banky.</span><span class="sxs-lookup"><span data-stu-id="53a44-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="53a44-108">Rozbalte oddíl Bankovní dokument.</span><span class="sxs-lookup"><span data-stu-id="53a44-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="53a44-109">Vyberte možnost Povolit import akreditivu.</span><span class="sxs-lookup"><span data-stu-id="53a44-109">Select the Enable import letter of credit option.</span></span>
4. <span data-ttu-id="53a44-110">Vyberte možnost Povolit export akreditivu.</span><span class="sxs-lookup"><span data-stu-id="53a44-110">Select the Enable export letter of credit option.</span></span>
5. <span data-ttu-id="53a44-111">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="53a44-111">Click Save.</span></span>
6. <span data-ttu-id="53a44-112">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="53a44-112">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="53a44-113">Vytvoření bankovního zařízení</span><span class="sxs-lookup"><span data-stu-id="53a44-113">Create Bank facility</span></span>
1. <span data-ttu-id="53a44-114">Přejděte do nabídky Pokladna a banka > Nastavení > Bankovní zařízení.</span><span class="sxs-lookup"><span data-stu-id="53a44-114">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="53a44-115">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="53a44-115">Click New.</span></span>
3. <span data-ttu-id="53a44-116">V poli Skupina zařízení zadejte název skupiny bankovních zařízení.</span><span class="sxs-lookup"><span data-stu-id="53a44-116">In the Facility group field, enter the bank facility group name.</span></span>
4. <span data-ttu-id="53a44-117">V poli Popis zadejte popis skupiny bankovních zařízení.</span><span class="sxs-lookup"><span data-stu-id="53a44-117">In the Description field, enter the bank facility group description.</span></span>
5. <span data-ttu-id="53a44-118">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="53a44-118">Click Save.</span></span>
6. <span data-ttu-id="53a44-119">Klikněte na kartu Typy zařízení.</span><span class="sxs-lookup"><span data-stu-id="53a44-119">Click the Facility types tab.</span></span>
7. <span data-ttu-id="53a44-120">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="53a44-120">Click New.</span></span>
8. <span data-ttu-id="53a44-121">Do pole Typ zařízení zadejte jedinečný kód.</span><span class="sxs-lookup"><span data-stu-id="53a44-121">In the Facility type field, enter a unique code.</span></span>
9. <span data-ttu-id="53a44-122">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="53a44-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="53a44-123">V poli Skupina zařízení kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="53a44-123">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="53a44-124">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="53a44-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="53a44-125">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="53a44-125">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="53a44-126">V poli Druh zařízení vyberte povahu bankovního zařízení.</span><span class="sxs-lookup"><span data-stu-id="53a44-126">In the Facility nature field, select the nature of the bank facility.</span></span>
14. <span data-ttu-id="53a44-127">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="53a44-127">Click Save.</span></span>
15. <span data-ttu-id="53a44-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="53a44-128">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="53a44-129">Účetní profil banky</span><span class="sxs-lookup"><span data-stu-id="53a44-129">Bank posting profile</span></span>
1. <span data-ttu-id="53a44-130">Přejděte do nabídky Pokladna a banka > Nastavení > Profil účtování bankovních dokumentů.</span><span class="sxs-lookup"><span data-stu-id="53a44-130">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="53a44-131">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="53a44-131">Click New.</span></span>
3. <span data-ttu-id="53a44-132">V poli Číslo účtu/skupiny kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="53a44-132">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="53a44-133">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="53a44-133">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="53a44-134">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="53a44-134">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="53a44-135">Vyberte hlavní účet pro vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="53a44-135">Select the main account for settlement.</span></span>
    * <span data-ttu-id="53a44-136">Tento účet se používá při výpočtu prognózy pro cashflow.</span><span class="sxs-lookup"><span data-stu-id="53a44-136">This account is used when calculating cash flow forecast.</span></span>  
7. <span data-ttu-id="53a44-137">V poli Poplatkový účet vyberte účet pro výdajové transakce.</span><span class="sxs-lookup"><span data-stu-id="53a44-137">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="53a44-138">V poli Maržový účet vyberte účet pro transakce marže.</span><span class="sxs-lookup"><span data-stu-id="53a44-138">In the Margin account field, select the account for margin transactions.</span></span>
    * <span data-ttu-id="53a44-139">Tento účet je debetován, pokud je počáteční marže zaúčtována a kreditován po zaúčtování platby.</span><span class="sxs-lookup"><span data-stu-id="53a44-139">This account is debited when the opening margin is posted and credited when the payment is posted.</span></span>  
9. <span data-ttu-id="53a44-140">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="53a44-140">Click Save.</span></span>

