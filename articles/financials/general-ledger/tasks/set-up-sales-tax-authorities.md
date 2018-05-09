--- 
title: "Nastavení daňových úřadů"
description: "Finanční úřady jsou entity, pro které je třeba vykazovat a platit shromážděné DPH."
author: twheeloc
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
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2ba2412d81fa6b0a60ff18c9fe065882c864f01c
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-sales-tax-authorities"></a><span data-ttu-id="f4adb-103">Nastavení daňových úřadů</span><span class="sxs-lookup"><span data-stu-id="f4adb-103">Set up sales tax authorities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f4adb-104">Finanční úřady jsou entity, pro které je třeba vykazovat a platit shromážděné DPH.</span><span class="sxs-lookup"><span data-stu-id="f4adb-104">Sales tax authorities are entities to which collected sales tax needs to be reported and paid.</span></span> <span data-ttu-id="f4adb-105">Můžete finančnímu úřadu platit DPH přímo nebo prostřednictvím účtu dodavatele, který pro daný finanční úřad vytvoříte.</span><span class="sxs-lookup"><span data-stu-id="f4adb-105">You can pay sales taxes to the authority directly or through a vendor account that you create for the sales tax authority.</span></span> <span data-ttu-id="f4adb-106">Pokud to provedete, může společnost použít své obvyklé platební postupy, aby DPH odvedla finančnímu úřadu včas.</span><span class="sxs-lookup"><span data-stu-id="f4adb-106">If you do this, the company can use its usual payment routines to pay the sales tax authority on time.</span></span> <span data-ttu-id="f4adb-107">Jestliže nenastavíte finanční úřad jako dodavatele, musí někdo připravit ruční platbu finančnímu úřadu k příslušnému datu splatnosti.</span><span class="sxs-lookup"><span data-stu-id="f4adb-107">If you do not set up the tax authority as a vendor, someone must prepare a manual payment to the tax authority on the appropriate due date.</span></span> <span data-ttu-id="f4adb-108">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="f4adb-108">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="f4adb-109">Přejděte na Daň > Nepřímé daně > DPH > Finanční úřady.</span><span class="sxs-lookup"><span data-stu-id="f4adb-109">Go to Tax > Indirect taxes > Sales tax > Sales tax authorities.</span></span>
2. <span data-ttu-id="f4adb-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="f4adb-110">Click New.</span></span>
3. <span data-ttu-id="f4adb-111">Zadejte hodnotu do pole Úřad.</span><span class="sxs-lookup"><span data-stu-id="f4adb-111">In the Authority field, type a value.</span></span>
4. <span data-ttu-id="f4adb-112">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="f4adb-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f4adb-113">V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="f4adb-113">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f4adb-114">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="f4adb-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f4adb-115">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="f4adb-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f4adb-116">Vyberte rozvržení sestavy pro svou zemi či oblast (pokud je k dispozici).</span><span class="sxs-lookup"><span data-stu-id="f4adb-116">Select the report layout for your country/region, if one is available.</span></span> <span data-ttu-id="f4adb-117">Jestliže rozvržení sestav neodpovídá požadavkům finančního úřadu, použijte výchozí rozvržení.</span><span class="sxs-lookup"><span data-stu-id="f4adb-117">If the report layouts do not correspond to the requirements of the sales tax authority, use default layout.</span></span>
9. <span data-ttu-id="f4adb-118">Zadejte hodnoty do formuláře a polí Zaokrouhlení a určete tak způsob zaokrouhlení celkové částky k úhradě.</span><span class="sxs-lookup"><span data-stu-id="f4adb-118">Enter values in the Rounding form and the Round-off fields to specify how the tax total amount to be paid should be rounded.</span></span> <span data-ttu-id="f4adb-119">Rozdíly zaokrouhlení budou zaúčtovány v části Účty pro automatické transakce nastavené v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="f4adb-119">Any rounding differences will be posted to Accounts for automatic transactions set up in General ledger.</span></span>
10. <span data-ttu-id="f4adb-120">V poli Zaokrouhlení zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="f4adb-120">In the Round-off field, enter a number.</span></span>
11. <span data-ttu-id="f4adb-121">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="f4adb-121">Click Save.</span></span>


