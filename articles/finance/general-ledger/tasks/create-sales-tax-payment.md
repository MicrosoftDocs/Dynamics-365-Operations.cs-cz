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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99059a8e5d6f4bf125266ad2a98cb73751529e6b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139914"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="b38cf-103">Vytvoření platby DPH</span><span class="sxs-lookup"><span data-stu-id="b38cf-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b38cf-104">Úloha Vyrovnat a zaúčtovat DPH slouží k vyrovnání zůstatků DPH na účtech DPH a jejich vyrovnání na účtu pro vyrovnání DPH za dané období.</span><span class="sxs-lookup"><span data-stu-id="b38cf-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="b38cf-105">Přejděte na Daň > Přiznání > DPH > Vyrovnat a zaúčtovat DPH.</span><span class="sxs-lookup"><span data-stu-id="b38cf-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="b38cf-106">V poli Období vyrovnání kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b38cf-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="b38cf-107">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="b38cf-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b38cf-108">Zadejte datum do pole Od data.</span><span class="sxs-lookup"><span data-stu-id="b38cf-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="b38cf-109">Není-li vybrána možnost Zahrnout opravy na stránce Parametry hlavní knihy, vyrovnání lze zpracovat pro různé verze.</span><span class="sxs-lookup"><span data-stu-id="b38cf-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="b38cf-110">Na začátku je první vyrovnání pro interval období, které lze zpracovat pouze jedou pro interval období.</span><span class="sxs-lookup"><span data-stu-id="b38cf-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="b38cf-111">Nejnovější opravy vyrovnají transakce DPH, které byly zaúčtovány po vytvoření původní verze.</span><span class="sxs-lookup"><span data-stu-id="b38cf-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="b38cf-112">Zadejte datum do pole Datum transakce.</span><span class="sxs-lookup"><span data-stu-id="b38cf-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="b38cf-113">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b38cf-113">Click OK.</span></span>

