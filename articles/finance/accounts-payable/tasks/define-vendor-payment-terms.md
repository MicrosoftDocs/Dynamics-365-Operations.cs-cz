---
title: Definování platebních podmínek dodavatelů
description: Toto téma vysvětluje, jak nastavit platební podmínky pro faktury dodavatele.
author: abruer
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f47fc0cd67cddef3c73f9c4c6b8dd6f41bbe85ec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838902"
---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="6d26a-103">Definování platebních podmínek dodavatelů</span><span class="sxs-lookup"><span data-stu-id="6d26a-103">Define vendor payment terms</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6d26a-104">Toto téma vysvětluje, jak nastavit platební podmínky pro faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6d26a-104">This topic explains how to set up payment terms for vendor invoices.</span></span> <span data-ttu-id="6d26a-105">Tento úkol využívá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="6d26a-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="6d26a-106">Přejděte do **Podokno navigace > Moduly > Závazky > Nastavení platby > Podmínky platby**.</span><span class="sxs-lookup"><span data-stu-id="6d26a-106">Go to **Navigation pane > Modules > Accounts payable > Payment setup > Terms of payment**.</span></span>
2. <span data-ttu-id="6d26a-107">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="6d26a-107">Select **New**.</span></span> <span data-ttu-id="6d26a-108">Stránku Podmínky platby lze použít pro definování způsobu výpočtu data splatnosti.</span><span class="sxs-lookup"><span data-stu-id="6d26a-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="6d26a-109">Nepoužívá se při definování způsobu výpočtu data platební slevy.</span><span class="sxs-lookup"><span data-stu-id="6d26a-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="6d26a-110">V poli **Platební podmínky** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="6d26a-110">In the **Terms of payment** field, type a value.</span></span>
4. <span data-ttu-id="6d26a-111">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="6d26a-111">In the **Description field**, type a value.</span></span>
5. <span data-ttu-id="6d26a-112">Zadejte číslo do pole **Dny**.</span><span class="sxs-lookup"><span data-stu-id="6d26a-112">In the **Days** field, enter a number.</span></span> <span data-ttu-id="6d26a-113">Číslo zadané v tomto poli se použije pro přidání k datu splatnosti nebo na konec období identifikované podle způsobu platby.</span><span class="sxs-lookup"><span data-stu-id="6d26a-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="6d26a-114">Například když si zvolíte **Netto**, číslo bude přidáno do data splatnosti.</span><span class="sxs-lookup"><span data-stu-id="6d26a-114">For example, if you select **Net**, the number will be added to the due date.</span></span> <span data-ttu-id="6d26a-115">Pokud vyberete možnost **Aktuální měsíc**, číslo se přidá k poslednímu dni aktuálního měsíce pro výpočet data splatnosti.</span><span class="sxs-lookup"><span data-stu-id="6d26a-115">If you select **Current month**, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="6d26a-116">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="6d26a-116">Select **Save**.</span></span>
7. <span data-ttu-id="6d26a-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6d26a-117">Close the page.</span></span>
8. <span data-ttu-id="6d26a-118">Přejděte do nabídky **Závazky > Nastavení platby > Platební slevy**.</span><span class="sxs-lookup"><span data-stu-id="6d26a-118">Go to **Accounts payable > Payment setup > Cash discounts**.</span></span>
9. <span data-ttu-id="6d26a-119">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="6d26a-119">Select **New**.</span></span>
10. <span data-ttu-id="6d26a-120">V poli **Platební slevy** zadejte ID.</span><span class="sxs-lookup"><span data-stu-id="6d26a-120">In the **Cash discount** field, enter an ID.</span></span>
11. <span data-ttu-id="6d26a-121">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="6d26a-121">In the **Description** field, type a value.</span></span>
12. <span data-ttu-id="6d26a-122">Pokud dodavatel nabízí vrstvenou slevu, vyberte následující platební slevu po vypršení platnosti aktuální.</span><span class="sxs-lookup"><span data-stu-id="6d26a-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="6d26a-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6d26a-123">Close the page.</span></span>
14. <span data-ttu-id="6d26a-124">Zadejte číslo do pole **Dny**.</span><span class="sxs-lookup"><span data-stu-id="6d26a-124">In the **Days** field, enter a number.</span></span> <span data-ttu-id="6d26a-125">Množství zadané v poli **Dny** se použije k výpočtu data platební slevy, a to na základě možností vybraných v poli **Netto/Aktuální**.</span><span class="sxs-lookup"><span data-stu-id="6d26a-125">The quantity entered in the **Days** field will be used to calculate the Cash discount date, based on what option was selected in the **Net/Current** field.</span></span> <span data-ttu-id="6d26a-126">Pokud byla vybrána možnost **Netto**, množství bude přidáno k datu faktury pro určení data platební slevy.</span><span class="sxs-lookup"><span data-stu-id="6d26a-126">If **Net** was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="6d26a-127">Pokud byla vybrána možnost **Aktuální měsíc**, množství bude přidáno ke konci aktuálního měsíce pro určení data platební slevy.</span><span class="sxs-lookup"><span data-stu-id="6d26a-127">If **Current month** was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="6d26a-128">Zadejte procentuální hodnotu platební slevy do pole **Sleva**.</span><span class="sxs-lookup"><span data-stu-id="6d26a-128">Enter the percentage of the cash discount in the **Discount** field.</span></span> 
16. <span data-ttu-id="6d26a-129">Zadejte hlavní účet, na který budou platební slevy zaúčtovány pro faktury odběratelů, a poté zadejte hlavní účet, na který budou platební slevy zaúčtovány pro faktury dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="6d26a-129">Enter the main account to which the cash discount will be posted for customer invoices, then enter the main account to which the cash discount will be posted for vendor invoices.</span></span> <span data-ttu-id="6d26a-130">Je-li hodnota **Slevové protiúčty** nastavena na **Použít hlavní účet pro slevu dodavatele**, použije se Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="6d26a-130">If **Discount offset accounts** is set to **Use main account for vendor discount**, then the Main account will be used.</span></span> <span data-ttu-id="6d26a-131">Pokud je možnost nastavena na **Účty na řádcích faktury**, platební sleva se zaúčtuje do účtů majetku / nákladů na řádky faktury.</span><span class="sxs-lookup"><span data-stu-id="6d26a-131">If the option is set to **Accounts on the invoice lines**, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
17. <span data-ttu-id="6d26a-132">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="6d26a-132">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]