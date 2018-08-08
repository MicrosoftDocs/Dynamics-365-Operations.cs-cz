--- 
title: "Stanovení způsobu platby odběratele"
description: "Vytvořte metodu platby pro úhrady odběratelů."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: b7c4c0670dbb2acd3fea1973d8a6f4f38bc94d4c
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---
# <a name="establish-customer-method-of-payment"></a><span data-ttu-id="34396-103">Stanovení způsobu platby odběratele</span><span class="sxs-lookup"><span data-stu-id="34396-103">Establish customer method of payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="34396-104">Vytvořte metodu platby pro úhrady odběratelů.</span><span class="sxs-lookup"><span data-stu-id="34396-104">Create a method of payment for customer payments.</span></span> <span data-ttu-id="34396-105">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="34396-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="34396-106">Přejděte do nabídky Pohledávky > Nastavení platby > Metody platby.</span><span class="sxs-lookup"><span data-stu-id="34396-106">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="34396-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="34396-107">Click New.</span></span>
3. <span data-ttu-id="34396-108">V poli Metoda platby zadejte Identifikátor pro metodu platby.</span><span class="sxs-lookup"><span data-stu-id="34396-108">In the Method of payment field, enter an ID for the method of payment.</span></span>
    * <span data-ttu-id="34396-109">ID metody platby je zobrazeno ve fakturách a platbách, proto vyberte dostatečně popisný název, aby bylo možné pochopit, jaký typ platby je zaznamenán, a pro jaký bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="34396-109">The Method of payment ID is shown on invoices and payments, so make it descriptive enough to understand what type of payment is being recorded, and for what bank account.</span></span>  
4. <span data-ttu-id="34396-110">Zadejte popis do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="34396-110">In the Description field, enter a description.</span></span>
5. <span data-ttu-id="34396-111">Vyberte, jaký stav platby je nutný pro zaúčtování platby.</span><span class="sxs-lookup"><span data-stu-id="34396-111">Select what payment status is required in order for payments to be posted.</span></span>
    * <span data-ttu-id="34396-112">Při vytváření platby odběratele je možné je zaúčtovat pouze pokud stav platby odpovídá stavu platby, který je definován zde.</span><span class="sxs-lookup"><span data-stu-id="34396-112">When creating a customer payment, it can only be posted when the payment status matches the payment status you define here.</span></span>  
6. <span data-ttu-id="34396-113">Vyberte způsob jakým odběratelé musí vytvářet platby pro faktury.</span><span class="sxs-lookup"><span data-stu-id="34396-113">Select how customers payments should be created for invoices.</span></span>
    * <span data-ttu-id="34396-114">Tato možnost se používá pouze při spuštění návrhu platby.</span><span class="sxs-lookup"><span data-stu-id="34396-114">This option is only used when running a payment proposal.</span></span> <span data-ttu-id="34396-115">Návrh platby lze použít pro platby odběratelů při provádění přímých debetů a zavedení fondů z bankovních účtů zákazníků.</span><span class="sxs-lookup"><span data-stu-id="34396-115">A payment proposal could be used for customer payments when doing direct debits, and pulling the funds from the customers' bank accounts.</span></span>  
7. <span data-ttu-id="34396-116">Vyberte typ platby.</span><span class="sxs-lookup"><span data-stu-id="34396-116">Select the type of payment.</span></span>
    * <span data-ttu-id="34396-117">Typ platby vám pomůže určit, zda u platby dojde k ověření, nebo nikoli.</span><span class="sxs-lookup"><span data-stu-id="34396-117">The payment type will help determine whether some validation will occur or not on the payment.</span></span>  
8. <span data-ttu-id="34396-118">Vyberte, do jakého typu účtu budou platby zaúčtovány.</span><span class="sxs-lookup"><span data-stu-id="34396-118">Select what account type payments will post to.</span></span>
    * <span data-ttu-id="34396-119">Banka obvykle vybírá tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="34396-119">Typically, Bank would be selected for this option.</span></span>  
9. <span data-ttu-id="34396-120">Vyberte bankovní účet, do kterého bude zaznamenána tato platba.</span><span class="sxs-lookup"><span data-stu-id="34396-120">Select the bank account into which this payment will be recorded.</span></span>
10. <span data-ttu-id="34396-121">Zadejte typ bankovní transakce pro identifikaci typu platby používané bankou.</span><span class="sxs-lookup"><span data-stu-id="34396-121">Enter the Bank transaction type to identify the type of payment used by your bank.</span></span>
    * <span data-ttu-id="34396-122">Typ bankovní transakce se používá v průběhu procesu odsouhlasení banky, umožňuje odsouhlasení usnadnit.</span><span class="sxs-lookup"><span data-stu-id="34396-122">The bank transaction type is used during the bank reconciliation process, and can make reconciliation easier.</span></span>  
11. <span data-ttu-id="34396-123">Určete, zda platby budou dočasně zaúčtovávat na překlenovací účet.</span><span class="sxs-lookup"><span data-stu-id="34396-123">Select whether this payment will temporarily post to a bridging account.</span></span>
    * <span data-ttu-id="34396-124">Pokud budete chtít vyzkoušet plovoucí čas pro platbu a banku tak odbavit, použijte funkci Překlenování.</span><span class="sxs-lookup"><span data-stu-id="34396-124">If you want to try the float time for a payment to clear the bank, use the Bridging functionality.</span></span> <span data-ttu-id="34396-125">Platba se dočasně zaúčtuje do účtu hlavní knihy, dokud nedojde k odbavení banky, což způsobí přesunutí platby na bankovní účet, která jste definovali zde.</span><span class="sxs-lookup"><span data-stu-id="34396-125">The payment will temporarily post to a Ledger account until it clears the bank, at which time the payment will move to the bank account you defined here.</span></span>  
12. <span data-ttu-id="34396-126">Zadejte hlavní účet použitý pro překlenovací zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="34396-126">Enter the main account used for the bridging posting.</span></span>
    * <span data-ttu-id="34396-127">Toto je hlavní účet, na který se platba dočasně zaúčtuje, používáte-li překlenování.</span><span class="sxs-lookup"><span data-stu-id="34396-127">This is the main account to which the payment will temporarily post if using bridging.</span></span>  
13. <span data-ttu-id="34396-128">Použijte kartu Formátu souboru pro definování nastavení pro elektronické platby.</span><span class="sxs-lookup"><span data-stu-id="34396-128">Use the File format tab to define setting for electronic payments.</span></span>
14. <span data-ttu-id="34396-129">Použijte kartu Řízení platby k definování polí, která jsou povinná.</span><span class="sxs-lookup"><span data-stu-id="34396-129">Use the Payment control tab to define fields that are mandatory.</span></span>
    * <span data-ttu-id="34396-130">Pokud například potřebujete, aby všechny platby s touto metodou byly uloženy, můžete vybrat tuto možnost na této kartě.</span><span class="sxs-lookup"><span data-stu-id="34396-130">For example, if you require all payments with this method of payment to be deposited, you can choose that option on this tab.</span></span>  
15. <span data-ttu-id="34396-131">Na kartě Atributy platby definujte, které atributy platby chcete použít pro tuto metodu platby.</span><span class="sxs-lookup"><span data-stu-id="34396-131">Use the Payment attributes tab to define which payment attributes you want to use for this method of payment.</span></span>
16. <span data-ttu-id="34396-132">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="34396-132">Click Save.</span></span>


