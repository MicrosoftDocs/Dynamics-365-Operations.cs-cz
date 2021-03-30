---
title: Nastavení daňových úřadů
description: Finanční úřady jsou entity, pro které je třeba vykazovat a platit shromážděné DPH.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eff67bc32eafea86d0ff582c56059c28706ed2a1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222225"
---
# <a name="set-up-sales-tax-authorities"></a><span data-ttu-id="44b05-103">Nastavení daňových úřadů</span><span class="sxs-lookup"><span data-stu-id="44b05-103">Set up sales tax authorities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="44b05-104">Finanční úřady jsou entity, pro které je třeba vykazovat a platit shromážděné DPH.</span><span class="sxs-lookup"><span data-stu-id="44b05-104">Sales tax authorities are entities to which collected sales tax needs to be reported and paid.</span></span> <span data-ttu-id="44b05-105">Můžete finančnímu úřadu platit DPH přímo nebo prostřednictvím účtu dodavatele, který pro daný finanční úřad vytvoříte.</span><span class="sxs-lookup"><span data-stu-id="44b05-105">You can pay sales taxes to the authority directly or through a vendor account that you create for the sales tax authority.</span></span> <span data-ttu-id="44b05-106">Pokud to provedete, může společnost použít své obvyklé platební postupy, aby DPH odvedla finančnímu úřadu včas.</span><span class="sxs-lookup"><span data-stu-id="44b05-106">If you do this, the company can use its usual payment routines to pay the sales tax authority on time.</span></span> <span data-ttu-id="44b05-107">Jestliže nenastavíte finanční úřad jako dodavatele, musí někdo připravit ruční platbu finančnímu úřadu k příslušnému datu splatnosti.</span><span class="sxs-lookup"><span data-stu-id="44b05-107">If you do not set up the tax authority as a vendor, someone must prepare a manual payment to the tax authority on the appropriate due date.</span></span> <span data-ttu-id="44b05-108">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="44b05-108">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="44b05-109">Přejděte na Daň > Nepřímé daně > DPH > Finanční úřady.</span><span class="sxs-lookup"><span data-stu-id="44b05-109">Go to Tax > Indirect taxes > Sales tax > Sales tax authorities.</span></span>
2. <span data-ttu-id="44b05-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="44b05-110">Click New.</span></span>
3. <span data-ttu-id="44b05-111">Zadejte hodnotu do pole Úřad.</span><span class="sxs-lookup"><span data-stu-id="44b05-111">In the Authority field, type a value.</span></span>
4. <span data-ttu-id="44b05-112">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="44b05-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="44b05-113">V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="44b05-113">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="44b05-114">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="44b05-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="44b05-115">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="44b05-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="44b05-116">Vyberte rozvržení sestavy pro svou zemi či oblast (pokud je k dispozici).</span><span class="sxs-lookup"><span data-stu-id="44b05-116">Select the report layout for your country/region, if one is available.</span></span> <span data-ttu-id="44b05-117">Jestliže rozvržení sestav neodpovídá požadavkům finančního úřadu, použijte výchozí rozvržení.</span><span class="sxs-lookup"><span data-stu-id="44b05-117">If the report layouts do not correspond to the requirements of the sales tax authority, use default layout.</span></span>
9. <span data-ttu-id="44b05-118">Zadejte hodnoty do formuláře a polí Zaokrouhlení a určete tak způsob zaokrouhlení celkové částky k úhradě.</span><span class="sxs-lookup"><span data-stu-id="44b05-118">Enter values in the Rounding form and the Round-off fields to specify how the tax total amount to be paid should be rounded.</span></span> <span data-ttu-id="44b05-119">Rozdíly zaokrouhlení budou zaúčtovány v části Účty pro automatické transakce nastavené v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="44b05-119">Any rounding differences will be posted to Accounts for automatic transactions set up in General ledger.</span></span>
10. <span data-ttu-id="44b05-120">V poli Zaokrouhlení zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="44b05-120">In the Round-off field, enter a number.</span></span>
11. <span data-ttu-id="44b05-121">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="44b05-121">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]