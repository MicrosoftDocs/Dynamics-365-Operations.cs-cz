---
title: Vytvoření platby DPH
description: Procedura úlohy Vyrovnat a zaúčtovat DPH slouží k vyrovnání zůstatků DPH na účtech DPH a jejich vyrovnání na účtu pro vyrovnání DPH za dané období.
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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9b5e3e26e19bd0a9dbf878626328da267b61964f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968697"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="1fe72-103">Vytvoření platby DPH</span><span class="sxs-lookup"><span data-stu-id="1fe72-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1fe72-104">Procedura úlohy Vyrovnat a zaúčtovat DPH slouží k vyrovnání zůstatků DPH na účtech DPH a jejich vyrovnání na účtu pro vyrovnání DPH za dané období.</span><span class="sxs-lookup"><span data-stu-id="1fe72-104">The settle and post sales tax job procedure settles sales tax balances on the sales tax accounts, and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="1fe72-105">Přejděte na **Daň > Přiznání > DPH > Vyrovnat a zaúčtovat DPH**.</span><span class="sxs-lookup"><span data-stu-id="1fe72-105">Go to **Tax > Declarations > Sales tax > Settle and post sales tax**.</span></span>
2. <span data-ttu-id="1fe72-106">V poli **Období vyrovnání** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="1fe72-106">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="1fe72-107">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="1fe72-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1fe72-108">Do pole **Od data** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="1fe72-108">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="1fe72-109">Není-li vybrána možnost **Zahrnout opravy** na stránce **Parametry hlavní knihy**, vyrovnání lze zpracovat pro různé verze.</span><span class="sxs-lookup"><span data-stu-id="1fe72-109">If you don't select the **Include corrections** option on the **General ledger parameters** page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="1fe72-110">Na začátku je první vyrovnání pro interval období, které lze zpracovat pouze jednou pro interval období.</span><span class="sxs-lookup"><span data-stu-id="1fe72-110">Original is the first settlement for a period interval and can be processed only once for a period interval.</span></span> <span data-ttu-id="1fe72-111">Nejnovější opravy vyrovnají transakce DPH, které byly zaúčtovány po vytvoření původní verze.</span><span class="sxs-lookup"><span data-stu-id="1fe72-111">The latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="1fe72-112">Zadejte datum do pole **Datum transakce**.</span><span class="sxs-lookup"><span data-stu-id="1fe72-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="1fe72-113">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="1fe72-113">Click **OK**.</span></span>

