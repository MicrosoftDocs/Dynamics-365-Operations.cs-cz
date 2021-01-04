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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6afa52fa2c784fd7afbdc8db0e079af0689b4bec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441224"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a><span data-ttu-id="5f215-103">Nastavení zařízení banky a zaúčtování profilů pro akreditiv</span><span class="sxs-lookup"><span data-stu-id="5f215-103">Set up bank facilities and posting profiles for letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5f215-104">Tento postup vás provede vytvořením bankovního zařízení a účetního profilu potřebného pro zpracování akreditivu.</span><span class="sxs-lookup"><span data-stu-id="5f215-104">This procedure walks through creating a Bank facility and posting profile required to process Letters of credit.</span></span> 

<span data-ttu-id="5f215-105">Tento úkol využívá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="5f215-105">This tasks uses the demo company 'USMF'.</span></span>






## <a name="general-ledger-parameter"></a><span data-ttu-id="5f215-106">Parametr hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="5f215-106">General ledger parameter</span></span>
1. <span data-ttu-id="5f215-107">Přejděte do nabídky Pokladna a banka > Nastavení > Parametry pokladny a banky.</span><span class="sxs-lookup"><span data-stu-id="5f215-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="5f215-108">Rozbalte oddíl Bankovní dokument.</span><span class="sxs-lookup"><span data-stu-id="5f215-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="5f215-109">Vyberte možnost Povolit import akreditivu.</span><span class="sxs-lookup"><span data-stu-id="5f215-109">Select the Enable import letter of credit option.</span></span>
4. <span data-ttu-id="5f215-110">Vyberte možnost Povolit export akreditivu.</span><span class="sxs-lookup"><span data-stu-id="5f215-110">Select the Enable export letter of credit option.</span></span>
5. <span data-ttu-id="5f215-111">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5f215-111">Click Save.</span></span>
6. <span data-ttu-id="5f215-112">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5f215-112">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="5f215-113">Vytvoření bankovního zařízení</span><span class="sxs-lookup"><span data-stu-id="5f215-113">Create Bank facility</span></span>
1. <span data-ttu-id="5f215-114">Přejděte do nabídky Pokladna a banka > Nastavení > Bankovní zařízení.</span><span class="sxs-lookup"><span data-stu-id="5f215-114">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="5f215-115">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="5f215-115">Click New.</span></span>
3. <span data-ttu-id="5f215-116">V poli Skupina zařízení zadejte název skupiny bankovních zařízení.</span><span class="sxs-lookup"><span data-stu-id="5f215-116">In the Facility group field, enter the bank facility group name.</span></span>
4. <span data-ttu-id="5f215-117">V poli Popis zadejte popis skupiny bankovních zařízení.</span><span class="sxs-lookup"><span data-stu-id="5f215-117">In the Description field, enter the bank facility group description.</span></span>
5. <span data-ttu-id="5f215-118">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5f215-118">Click Save.</span></span>
6. <span data-ttu-id="5f215-119">Klikněte na kartu Typy zařízení.</span><span class="sxs-lookup"><span data-stu-id="5f215-119">Click the Facility types tab.</span></span>
7. <span data-ttu-id="5f215-120">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="5f215-120">Click New.</span></span>
8. <span data-ttu-id="5f215-121">Do pole Typ zařízení zadejte jedinečný kód.</span><span class="sxs-lookup"><span data-stu-id="5f215-121">In the Facility type field, enter a unique code.</span></span>
9. <span data-ttu-id="5f215-122">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="5f215-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="5f215-123">V poli Skupina zařízení kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5f215-123">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="5f215-124">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5f215-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="5f215-125">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="5f215-125">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="5f215-126">V poli Druh zařízení vyberte povahu bankovního zařízení.</span><span class="sxs-lookup"><span data-stu-id="5f215-126">In the Facility nature field, select the nature of the bank facility.</span></span>
14. <span data-ttu-id="5f215-127">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5f215-127">Click Save.</span></span>
15. <span data-ttu-id="5f215-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5f215-128">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="5f215-129">Účetní profil banky</span><span class="sxs-lookup"><span data-stu-id="5f215-129">Bank posting profile</span></span>
1. <span data-ttu-id="5f215-130">Přejděte do nabídky Pokladna a banka > Nastavení > Profil účtování bankovních dokumentů.</span><span class="sxs-lookup"><span data-stu-id="5f215-130">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="5f215-131">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="5f215-131">Click New.</span></span>
3. <span data-ttu-id="5f215-132">V poli Číslo účtu/skupiny kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5f215-132">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5f215-133">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5f215-133">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="5f215-134">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="5f215-134">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="5f215-135">Vyberte hlavní účet pro vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="5f215-135">Select the main account for settlement.</span></span>
    * <span data-ttu-id="5f215-136">Tento účet se používá při výpočtu prognózy pro cashflow.</span><span class="sxs-lookup"><span data-stu-id="5f215-136">This account is used when calculating cash flow forecast.</span></span>  
7. <span data-ttu-id="5f215-137">V poli Poplatkový účet vyberte účet pro výdajové transakce.</span><span class="sxs-lookup"><span data-stu-id="5f215-137">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="5f215-138">V poli Maržový účet vyberte účet pro transakce marže.</span><span class="sxs-lookup"><span data-stu-id="5f215-138">In the Margin account field, select the account for margin transactions.</span></span>
    * <span data-ttu-id="5f215-139">Tento účet je debetován, pokud je počáteční marže zaúčtována a kreditován po zaúčtování platby.</span><span class="sxs-lookup"><span data-stu-id="5f215-139">This account is debited when the opening margin is posted and credited when the payment is posted.</span></span>  
9. <span data-ttu-id="5f215-140">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5f215-140">Click Save.</span></span>

