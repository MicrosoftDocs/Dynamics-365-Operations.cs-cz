--- 
title: "Definování platebních podmínek dodavatelů"
description: "Nastavte platební podmínky pro faktury dodavatele."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a00ca73b1bc301960132a86846749d12c39ed3f7
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="5197b-103">Definování platebních podmínek dodavatelů</span><span class="sxs-lookup"><span data-stu-id="5197b-103">Define vendor payment terms</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5197b-104">Nastavte platební podmínky pro faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="5197b-104">Set up payment terms for vendor invoices.</span></span> <span data-ttu-id="5197b-105">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="5197b-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="5197b-106">Přejděte do nabídky Závazky > Nastavení platby > Podmínky platby.</span><span class="sxs-lookup"><span data-stu-id="5197b-106">Go to Accounts payable > Payment setup > Terms of payment.</span></span>
2. <span data-ttu-id="5197b-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="5197b-107">Click New.</span></span>
    * <span data-ttu-id="5197b-108">Stránku Podmínky platby lze použít pro definování způsobu výpočtu data splatnosti.</span><span class="sxs-lookup"><span data-stu-id="5197b-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="5197b-109">Nepoužívá se při definování způsobu výpočtu data platební slevy.</span><span class="sxs-lookup"><span data-stu-id="5197b-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="5197b-110">V poli Platební podmínky zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5197b-110">In the Terms of payment field, type a value.</span></span>
4. <span data-ttu-id="5197b-111">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="5197b-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5197b-112">Zadejte číslo do pole Dny.</span><span class="sxs-lookup"><span data-stu-id="5197b-112">In the Days field, enter a number.</span></span>
    * <span data-ttu-id="5197b-113">Číslo zadané v tomto poli se použije pro přidání k datu splatnosti nebo na konec období identifikované podle způsobu platby.</span><span class="sxs-lookup"><span data-stu-id="5197b-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="5197b-114">Například když si zvolíte Netto, číslo bude přidáno do data splatnosti.</span><span class="sxs-lookup"><span data-stu-id="5197b-114">For example, if you select Net, the number will be added to the due date.</span></span> <span data-ttu-id="5197b-115">Pokud vyberete možnost Aktuální měsíc, číslo se přidá k poslednímu dni aktuálního měsíce pro výpočet data splatnosti.</span><span class="sxs-lookup"><span data-stu-id="5197b-115">If you select Current month, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="5197b-116">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5197b-116">Click Save.</span></span>
7. <span data-ttu-id="5197b-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5197b-117">Close the page.</span></span>
8. <span data-ttu-id="5197b-118">Přejděte do nabídky Závazky > Nastavení platby > Platební slevy.</span><span class="sxs-lookup"><span data-stu-id="5197b-118">Go to Accounts payable > Payment setup > Cash discounts.</span></span>
9. <span data-ttu-id="5197b-119">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="5197b-119">Click New.</span></span>
10. <span data-ttu-id="5197b-120">V poli Platební slevy zadejte ID.</span><span class="sxs-lookup"><span data-stu-id="5197b-120">In the Cash discount field, enter an ID.</span></span>
11. <span data-ttu-id="5197b-121">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="5197b-121">In the Description field, type a value.</span></span>
12. <span data-ttu-id="5197b-122">Pokud dodavatel nabízí vrstvenou slevu, vyberte následující platební slevu po vypršení platnosti aktuální.</span><span class="sxs-lookup"><span data-stu-id="5197b-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="5197b-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5197b-123">Close the page.</span></span>
14. <span data-ttu-id="5197b-124">Zadejte číslo do pole Dny.</span><span class="sxs-lookup"><span data-stu-id="5197b-124">In the Days field, enter a number.</span></span>
    * <span data-ttu-id="5197b-125">Množství zadané v poli Dny se použije k výpočtu data platební slevy, a to na základě možností vybraných v poli Netto/Běžný.</span><span class="sxs-lookup"><span data-stu-id="5197b-125">The quantity entered in the Days field will be used to calculate the Cash discount date, based on what option was selected in the Net/Current field.</span></span> <span data-ttu-id="5197b-126">Pokud byla vybrána možnost Netto, množství bude přidáno k datu faktury pro určení data platební slevy.</span><span class="sxs-lookup"><span data-stu-id="5197b-126">If Net was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="5197b-127">Pokud byla vybrána možnost Aktuální měsíc, množství bude přidáno ke konci aktuálního měsíce pro určení data platební slevy.</span><span class="sxs-lookup"><span data-stu-id="5197b-127">If Current month was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="5197b-128">Zadejte procentuální hodnotu platební slevy do pole Sleva.</span><span class="sxs-lookup"><span data-stu-id="5197b-128">Enter the percentage of the cash discount in the Discount field.</span></span> 
16. <span data-ttu-id="5197b-129">Zadejte hlavního účtu, ke kterému bude platební sleva zaúčtována pro faktury odběratele.</span><span class="sxs-lookup"><span data-stu-id="5197b-129">Enter the main account to which the cash discount will be posted for customer invoices.</span></span>
17. <span data-ttu-id="5197b-130">Zadejte hlavního účtu, ke kterému bude platební sleva zaúčtována pro faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="5197b-130">Enter the main account to which the cash discount will be posted for vendor invoices.</span></span>
    * <span data-ttu-id="5197b-131">Je-li hodnota Slevové protiúčty nastavena na Použít hlavní účet pro slevu dodavatele, použije se Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="5197b-131">If 'Discount offset accounts' is set to Use main account for vendor discount, then the Main account will be used.</span></span>  <span data-ttu-id="5197b-132">Pokud je možnost nastavena na Účty na řádcích faktury, platební sleva se zaúčtuje do účtů majetku / nákladů na řádky faktury.</span><span class="sxs-lookup"><span data-stu-id="5197b-132">If the option is set to Accounts on the invoice lines, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
18. <span data-ttu-id="5197b-133">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5197b-133">Click Save.</span></span>


