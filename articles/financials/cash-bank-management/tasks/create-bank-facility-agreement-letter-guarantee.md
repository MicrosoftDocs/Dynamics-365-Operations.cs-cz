--- 
title: "Vytvoření smlouvy bankovního zařízení pro záruční listinu"
description: "Tento úkol vytvoří smlouvu bankovního zařízení ke zpracování záruční listiny."
author: ShylaThompson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 04ee7b1483f3b8a7cda7fce5439586f0a2979e51
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-bank-facility-agreement-for-the-letter-of-guarantee"></a><span data-ttu-id="e3e1e-103">Vytvoření smlouvy bankovního zařízení pro záruční listinu</span><span class="sxs-lookup"><span data-stu-id="e3e1e-103">Create a bank facility agreement for the letter of guarantee</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e3e1e-104">Tento úkol vytvoří smlouvu bankovního zařízení ke zpracování záruční listiny.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-104">This task creates a bank facility agreement to process a letter of guarantee.</span></span> <span data-ttu-id="e3e1e-105">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-105">This task uses the USMF demo company.</span></span> 


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="e3e1e-106">Vytvoření smlouvy o bankovních zařízeních</span><span class="sxs-lookup"><span data-stu-id="e3e1e-106">Create Bank facility agreement</span></span>
1. <span data-ttu-id="e3e1e-107">Přejděte do nabídky Pokladna a banka > Záruční listiny > Smlouvy bankovního zařízení.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-107">Go to Cash and bank management > Letters of guarantee > Bank facility agreements.</span></span>
2. <span data-ttu-id="e3e1e-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-108">Click New.</span></span>
3. <span data-ttu-id="e3e1e-109">V poli Číslo smlouvy zadejte číslo bankovní smlouvy pro transakci.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-109">In the Agreement number field, enter the bank agreement number for the transaction.</span></span>
4. <span data-ttu-id="e3e1e-110">V poli Bankovní účet vyberte číslo bankovního účtu, pro který je záruční listina otevřena.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-110">In the Bank account field, select the bank account number for which the letter of guarantee is open.</span></span> 
5. <span data-ttu-id="e3e1e-111">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e3e1e-112">Do pole Počáteční datum zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-112">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="e3e1e-113">Do pole Konečné datum zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-113">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="e3e1e-114">Přepněte rozšíření oddílu Obecné.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-114">Toggle the expansion of the General section.</span></span>
9. <span data-ttu-id="e3e1e-115">Klikněte na Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-115">Click Add line.</span></span>
10. <span data-ttu-id="e3e1e-116">V poli Typ zařízení kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-116">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="e3e1e-117">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="e3e1e-118">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-118">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="e3e1e-119">V poli Limit zadejte částku sjednanou s bankou.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-119">In the Limit field, enter the amount negotiated with the bank.</span></span>
14. <span data-ttu-id="e3e1e-120">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-120">Click Save.</span></span>
15. <span data-ttu-id="e3e1e-121">Rozbalte oddíl Záruční listina.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-121">Toggle the expansion of the Letter of guarantee section.</span></span>
16. <span data-ttu-id="e3e1e-122">Vyberte možnost v poli Metoda výpočtu.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-122">In the Calculation method field, select an option.</span></span>
    * <span data-ttu-id="e3e1e-123">Podle potřeby zadejte metodu výpočtu a podrobnosti o procentech pro možnosti Marže v hotovosti, Provize z výdejů, Provize z rozšíření, Provize hodnotu zvýšení nebo Provize ze snížené hodnoty.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-123">Enter the calculation method and percentage details for the Cash margin, Issuance commission, Extension commission, Increase value commission, or Decrease value commission, as appropriate.</span></span>   
17. <span data-ttu-id="e3e1e-124">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-124">Click Save.</span></span>

## <a name="extend-bank-facility-agreement"></a><span data-ttu-id="e3e1e-125">Rozšíření smlouvy bankovního zařízení</span><span class="sxs-lookup"><span data-stu-id="e3e1e-125">Extend bank facility agreement</span></span>
1. <span data-ttu-id="e3e1e-126">Kliknutím na možnost Rozšířit otevřete dialog Zanechat.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-126">Click Extend to open the drop dialog.</span></span>
2. <span data-ttu-id="e3e1e-127">Zadejte hodnotu do pole Nové číslo smlouvy.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-127">In the New agreement number field, type a value.</span></span>
3. <span data-ttu-id="e3e1e-128">Do pole Konečné datum zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-128">In the End date field, enter a date and time.</span></span>
4. <span data-ttu-id="e3e1e-129">Klepněte na položku Rozšířit.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-129">Click Extend.</span></span>
5. <span data-ttu-id="e3e1e-130">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-130">Click Save.</span></span>
6. <span data-ttu-id="e3e1e-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e3e1e-131">Close the page.</span></span>


