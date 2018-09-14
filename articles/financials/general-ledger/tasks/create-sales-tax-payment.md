--- 
title: "Vytvoření platby DPH"
description: "Úloha Vyrovnat a zaúčtovat DPH slouží k vyrovnání zůstatků DPH na účtech DPH a jejich vyrovnání na účtu pro vyrovnání DPH za dané období."
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Dialog
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: b0d72c88d6ba851e96ca07b896630549690e9396
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="20f01-103">Vytvoření platby DPH</span><span class="sxs-lookup"><span data-stu-id="20f01-103">Create a sales tax payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="20f01-104">Úloha Vyrovnat a zaúčtovat DPH slouží k vyrovnání zůstatků DPH na účtech DPH a jejich vyrovnání na účtu pro vyrovnání DPH za dané období.</span><span class="sxs-lookup"><span data-stu-id="20f01-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="20f01-105">Přejděte na Daň > Přiznání > DPH > Vyrovnat a zaúčtovat DPH.</span><span class="sxs-lookup"><span data-stu-id="20f01-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="20f01-106">V poli Období vyrovnání kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="20f01-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="20f01-107">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="20f01-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="20f01-108">Zadejte datum do pole Od data.</span><span class="sxs-lookup"><span data-stu-id="20f01-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="20f01-109">Není-li vybrána možnost Zahrnout opravy na stránce Parametry hlavní knihy, vyrovnání lze zpracovat pro různé verze.</span><span class="sxs-lookup"><span data-stu-id="20f01-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="20f01-110">Na začátku je první vyrovnání pro interval období, které lze zpracovat pouze jedou pro interval období.</span><span class="sxs-lookup"><span data-stu-id="20f01-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="20f01-111">Nejnovější opravy vyrovnají transakce DPH, které byly zaúčtovány po vytvoření původní verze.</span><span class="sxs-lookup"><span data-stu-id="20f01-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="20f01-112">Zadejte datum do pole Datum transakce.</span><span class="sxs-lookup"><span data-stu-id="20f01-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="20f01-113">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="20f01-113">Click OK.</span></span>


