---
title: Vytvoření platby DPH
description: Úloha Vyrovnat a zaúčtovat DPH slouží k vyrovnání zůstatků DPH na účtech DPH a jejich vyrovnání na účtu pro vyrovnání DPH za dané období.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0d72c88d6ba851e96ca07b896630549690e9396
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "321747"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="9b91d-103">Vytvoření platby DPH</span><span class="sxs-lookup"><span data-stu-id="9b91d-103">Create a sales tax payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9b91d-104">Úloha Vyrovnat a zaúčtovat DPH slouží k vyrovnání zůstatků DPH na účtech DPH a jejich vyrovnání na účtu pro vyrovnání DPH za dané období.</span><span class="sxs-lookup"><span data-stu-id="9b91d-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="9b91d-105">Přejděte na Daň > Přiznání > DPH > Vyrovnat a zaúčtovat DPH.</span><span class="sxs-lookup"><span data-stu-id="9b91d-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="9b91d-106">V poli Období vyrovnání kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="9b91d-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="9b91d-107">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="9b91d-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9b91d-108">Zadejte datum do pole Od data.</span><span class="sxs-lookup"><span data-stu-id="9b91d-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="9b91d-109">Není-li vybrána možnost Zahrnout opravy na stránce Parametry hlavní knihy, vyrovnání lze zpracovat pro různé verze.</span><span class="sxs-lookup"><span data-stu-id="9b91d-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="9b91d-110">Na začátku je první vyrovnání pro interval období, které lze zpracovat pouze jedou pro interval období.</span><span class="sxs-lookup"><span data-stu-id="9b91d-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="9b91d-111">Nejnovější opravy vyrovnají transakce DPH, které byly zaúčtovány po vytvoření původní verze.</span><span class="sxs-lookup"><span data-stu-id="9b91d-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="9b91d-112">Zadejte datum do pole Datum transakce.</span><span class="sxs-lookup"><span data-stu-id="9b91d-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="9b91d-113">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9b91d-113">Click OK.</span></span>

