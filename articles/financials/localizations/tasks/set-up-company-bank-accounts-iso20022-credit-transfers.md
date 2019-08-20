---
title: Nastavení bankovních účtů společnosti pro převody kreditu ve formátu ISO20022
description: Tento postup popisuje způsob nastavení informací o konkrétním bankovním účtu společnosti, které jsou vyžadované pro generování souboru platby.
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
ms.openlocfilehash: 2bbbf55ed28ad2131d7e1253dd44842d85d39315
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848737"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="61f49-103">Nastavení bankovních účtů společnosti pro převody kreditu ve formátu ISO20022</span><span class="sxs-lookup"><span data-stu-id="61f49-103">Set up company bank accounts for ISO20022 credit transfers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="61f49-104">Tento postup popisuje způsob nastavení informací o konkrétním bankovním účtu společnosti, které jsou vyžadované pro generování souboru platby.</span><span class="sxs-lookup"><span data-stu-id="61f49-104">This procedure shows how to set up company-specific bank account information that is required for payment file generation.</span></span> <span data-ttu-id="61f49-105">Můžete nastavit informace požadované ke generování formátu pro převod kreditu ISO 20022, ale v závislosti na formátu mohou být požadovány další informace, jako je ID společnosti nebo kód třídění.</span><span class="sxs-lookup"><span data-stu-id="61f49-105">You set up information required to generate ISO 20022 credit transfer format but depending on the format there might be other information required, such as the Company ID or the Sort code.</span></span> 

<span data-ttu-id="61f49-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="61f49-106">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="61f49-107">Toto je druhý z pěti úkolů, které společně popisují proces platby dodavatele pomocí konfigurací elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="61f49-107">This is the second procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="61f49-108">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="61f49-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-iban-and-swift-code"></a><span data-ttu-id="61f49-109">Nastavení kódu IBAN a SWIFT</span><span class="sxs-lookup"><span data-stu-id="61f49-109">Set up IBAN and SWIFT code</span></span>
1. <span data-ttu-id="61f49-110">Přejděte do části Pokladna a banka > Bankovní účty.</span><span class="sxs-lookup"><span data-stu-id="61f49-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="61f49-111">Použijte rychlý filtr k filtrování v poli Bankovní účet s hodnotou 'DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="61f49-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="61f49-112">Kliknutím na tlačítko DEMF OPER otevřete podrobnosti o účtu.</span><span class="sxs-lookup"><span data-stu-id="61f49-112">Click DEMF OPER to open bank account details.</span></span>
4. <span data-ttu-id="61f49-113">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="61f49-113">Click Edit.</span></span>
5. <span data-ttu-id="61f49-114">Rozbalte oddíl Další identifikace.</span><span class="sxs-lookup"><span data-stu-id="61f49-114">Expand the Additional identification section.</span></span>
6. <span data-ttu-id="61f49-115">Zadejte do pole IBAN hodnotu „DE89370400440532013000“.</span><span class="sxs-lookup"><span data-stu-id="61f49-115">In the IBAN field, type 'DE89370400440532013000'.</span></span>
7. <span data-ttu-id="61f49-116">V poli Kód SWIFT zadejte hodnotu DEUTDEFF.</span><span class="sxs-lookup"><span data-stu-id="61f49-116">In the SWIFT code field, type 'DEUTDEFF'.</span></span>
    * <span data-ttu-id="61f49-117">Všimněte si, že pro spoustu formátů platby není požadován SWIFT\BIC, doporučujeme ho však pro bankovní účet zaregistrovat.</span><span class="sxs-lookup"><span data-stu-id="61f49-117">Note that SWIFT\BIC is not required for many payment formats, however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="61f49-118">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="61f49-118">Click Save.</span></span>

## <a name="set-up-bank-account-for-the-legal-entity"></a><span data-ttu-id="61f49-119">Nastavení bankovního účtu pro právnickou osobu</span><span class="sxs-lookup"><span data-stu-id="61f49-119">Set up bank account for the legal entity</span></span>
1. <span data-ttu-id="61f49-120">Přejděte do části na Správa organizace > Organizace > Právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="61f49-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="61f49-121">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="61f49-121">Click Edit.</span></span>
3. <span data-ttu-id="61f49-122">Rozbalte část informací o bankovním účtu.</span><span class="sxs-lookup"><span data-stu-id="61f49-122">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="61f49-123">V poli Bankovní účet zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="61f49-123">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="61f49-124">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="61f49-124">Click Save.</span></span>

