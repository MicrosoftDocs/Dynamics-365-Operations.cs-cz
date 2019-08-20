---
title: Stanovení způsobu platby odběratele
description: Vytvořte metodu platby pro úhrady odběratelů.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 477f1ff72fd8012c3403d22aa128d97e45d5559f
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842898"
---
# <a name="establish-customer-method-of-payment"></a><span data-ttu-id="e730a-103">Stanovení způsobu platby odběratele</span><span class="sxs-lookup"><span data-stu-id="e730a-103">Establish customer method of payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e730a-104">Vytvořte metodu platby pro úhrady odběratelů.</span><span class="sxs-lookup"><span data-stu-id="e730a-104">Create a method of payment for customer payments.</span></span> <span data-ttu-id="e730a-105">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="e730a-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="e730a-106">Přejděte do nabídky Pohledávky > Nastavení platby > Metody platby.</span><span class="sxs-lookup"><span data-stu-id="e730a-106">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="e730a-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e730a-107">Click New.</span></span>
3. <span data-ttu-id="e730a-108">V poli Metoda platby zadejte Identifikátor pro metodu platby.</span><span class="sxs-lookup"><span data-stu-id="e730a-108">In the Method of payment field, enter an ID for the method of payment.</span></span>
    * <span data-ttu-id="e730a-109">ID metody platby je zobrazeno ve fakturách a platbách, proto vyberte dostatečně popisný název, aby bylo možné pochopit, jaký typ platby je zaznamenán, a pro jaký bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="e730a-109">The Method of payment ID is shown on invoices and payments, so make it descriptive enough to understand what type of payment is being recorded, and for what bank account.</span></span>  
4. <span data-ttu-id="e730a-110">Zadejte popis do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="e730a-110">In the Description field, enter a description.</span></span>
5. <span data-ttu-id="e730a-111">Vyberte, jaký stav platby je nutný pro zaúčtování platby.</span><span class="sxs-lookup"><span data-stu-id="e730a-111">Select what payment status is required in order for payments to be posted.</span></span>
    * <span data-ttu-id="e730a-112">Při vytváření platby odběratele je možné je zaúčtovat pouze pokud stav platby odpovídá stavu platby, který je definován zde.</span><span class="sxs-lookup"><span data-stu-id="e730a-112">When creating a customer payment, it can only be posted when the payment status matches the payment status you define here.</span></span>  
6. <span data-ttu-id="e730a-113">Vyberte způsob jakým odběratelé musí vytvářet platby pro faktury.</span><span class="sxs-lookup"><span data-stu-id="e730a-113">Select how customers payments should be created for invoices.</span></span>
    * <span data-ttu-id="e730a-114">Tato možnost se používá pouze při spuštění návrhu platby.</span><span class="sxs-lookup"><span data-stu-id="e730a-114">This option is only used when running a payment proposal.</span></span> <span data-ttu-id="e730a-115">Návrh platby lze použít pro platby odběratelů při provádění přímých debetů a zavedení fondů z bankovních účtů zákazníků.</span><span class="sxs-lookup"><span data-stu-id="e730a-115">A payment proposal could be used for customer payments when doing direct debits, and pulling the funds from the customers' bank accounts.</span></span>  
7. <span data-ttu-id="e730a-116">Vyberte typ platby.</span><span class="sxs-lookup"><span data-stu-id="e730a-116">Select the type of payment.</span></span>
    * <span data-ttu-id="e730a-117">Typ platby vám pomůže určit, zda u platby dojde k ověření, nebo nikoli.</span><span class="sxs-lookup"><span data-stu-id="e730a-117">The payment type will help determine whether some validation will occur or not on the payment.</span></span>  
8. <span data-ttu-id="e730a-118">Vyberte, do jakého typu účtu budou platby zaúčtovány.</span><span class="sxs-lookup"><span data-stu-id="e730a-118">Select what account type payments will post to.</span></span>
    * <span data-ttu-id="e730a-119">Banka obvykle vybírá tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="e730a-119">Typically, Bank would be selected for this option.</span></span>  
9. <span data-ttu-id="e730a-120">Vyberte bankovní účet, do kterého bude zaznamenána tato platba.</span><span class="sxs-lookup"><span data-stu-id="e730a-120">Select the bank account into which this payment will be recorded.</span></span>
10. <span data-ttu-id="e730a-121">Zadejte typ bankovní transakce pro identifikaci typu platby používané bankou.</span><span class="sxs-lookup"><span data-stu-id="e730a-121">Enter the Bank transaction type to identify the type of payment used by your bank.</span></span>
    * <span data-ttu-id="e730a-122">Typ bankovní transakce se používá v průběhu procesu odsouhlasení banky, umožňuje odsouhlasení usnadnit.</span><span class="sxs-lookup"><span data-stu-id="e730a-122">The bank transaction type is used during the bank reconciliation process, and can make reconciliation easier.</span></span>  
11. <span data-ttu-id="e730a-123">Určete, zda platby budou dočasně zaúčtovávat na překlenovací účet.</span><span class="sxs-lookup"><span data-stu-id="e730a-123">Select whether this payment will temporarily post to a bridging account.</span></span>
    * <span data-ttu-id="e730a-124">Pokud budete chtít vyzkoušet plovoucí čas pro platbu a banku tak odbavit, použijte funkci Překlenování.</span><span class="sxs-lookup"><span data-stu-id="e730a-124">If you want to try the float time for a payment to clear the bank, use the Bridging functionality.</span></span> <span data-ttu-id="e730a-125">Platba se dočasně zaúčtuje do účtu hlavní knihy, dokud nedojde k odbavení banky, což způsobí přesunutí platby na bankovní účet, která jste definovali zde.</span><span class="sxs-lookup"><span data-stu-id="e730a-125">The payment will temporarily post to a Ledger account until it clears the bank, at which time the payment will move to the bank account you defined here.</span></span>  
12. <span data-ttu-id="e730a-126">Zadejte hlavní účet použitý pro překlenovací zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="e730a-126">Enter the main account used for the bridging posting.</span></span>
    * <span data-ttu-id="e730a-127">Toto je hlavní účet, na který se platba dočasně zaúčtuje, používáte-li překlenování.</span><span class="sxs-lookup"><span data-stu-id="e730a-127">This is the main account to which the payment will temporarily post if using bridging.</span></span>  
13. <span data-ttu-id="e730a-128">Použijte kartu Formátu souboru pro definování nastavení pro elektronické platby.</span><span class="sxs-lookup"><span data-stu-id="e730a-128">Use the File format tab to define setting for electronic payments.</span></span>
14. <span data-ttu-id="e730a-129">Použijte kartu Řízení platby k definování polí, která jsou povinná.</span><span class="sxs-lookup"><span data-stu-id="e730a-129">Use the Payment control tab to define fields that are mandatory.</span></span>
    * <span data-ttu-id="e730a-130">Pokud například potřebujete, aby všechny platby s touto metodou byly uloženy, můžete vybrat tuto možnost na této kartě.</span><span class="sxs-lookup"><span data-stu-id="e730a-130">For example, if you require all payments with this method of payment to be deposited, you can choose that option on this tab.</span></span>  
15. <span data-ttu-id="e730a-131">Na kartě Atributy platby definujte, které atributy platby chcete použít pro tuto metodu platby.</span><span class="sxs-lookup"><span data-stu-id="e730a-131">Use the Payment atrributes tab to define which payment attributes you want to use for this method of payment.</span></span>
16. <span data-ttu-id="e730a-132">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e730a-132">Click Save.</span></span>

