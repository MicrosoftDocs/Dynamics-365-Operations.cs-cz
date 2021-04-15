---
title: Nastavení globální srážkové daně
description: Toto téma uvádí kroky pro nastavení globální srážkové daně z prodeje a nákupu.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 3270b3f75d719fef9a7eb991c49e9d6585cd44d8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815301"
---
# <a name="set-up-global-withholding-tax"></a><span data-ttu-id="452c1-103">Nastavení globální srážkové daně</span><span class="sxs-lookup"><span data-stu-id="452c1-103">Set up global withholding tax</span></span>

<span data-ttu-id="452c1-104">Toto téma uvádí kroky pro nastavení globální srážkové daně z prodeje a nákupu.</span><span class="sxs-lookup"><span data-stu-id="452c1-104">This topic lists the steps for setting up global withholding tax for sales and purchases.</span></span> 

1. <span data-ttu-id="452c1-105">Nastavte daňové úřady pro srážkovou daň na stránce **Daňové úřady pro srážkovou daň**.</span><span class="sxs-lookup"><span data-stu-id="452c1-105">Set up withholding tax authorities on the **Withholding tax authorities** page.</span></span>

2. <span data-ttu-id="452c1-106">Nastavte období vyrovnání srážkové daně na stránce **Období vyrovnání srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="452c1-106">Set up withholding settlement periods on the **Withholding tax settlement periods** page.</span></span>

3. <span data-ttu-id="452c1-107">Nastavte skupinu pro zaúčtování srážkové daně do hlavní knihy na **Srážková daň > skupina pro zaúčtování do hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="452c1-107">Set up withholding ledger posting group on the **Withholding tax > ledger posting group** page.</span></span>

   > [!Note] 
   >
   > <span data-ttu-id="452c1-108">Účet **Srážkové daně** bude přiřazen k hlavnímu účtu s **Typem zaúčtování** srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="452c1-108">**Withholding tax** account will be assigned with a main account with **Posting type** of Withholding tax.</span></span> <span data-ttu-id="452c1-109">Účet pro **Zápočet srážkové daně** bude také přiřazen k hlavnímu účtu s **Typem zaúčtování** "Zápočet srážkové daně".</span><span class="sxs-lookup"><span data-stu-id="452c1-109">**Withholding tax offset** account will also be assigned with a main account with **Posting type** "Withholding tax offset".</span></span> <span data-ttu-id="452c1-110">Přejděte na **Hlavní kniha > Účetní osnova > Účty > Hlavní účty**, nastavte **Typ zaúčtování** v podformuláři **Ověření zaúčtování** pro hlavní účty.</span><span class="sxs-lookup"><span data-stu-id="452c1-110">Go to **General ledger > Chart of accounts > Accounts > Main accounts**, set up the **Posting type** in the **Posting validation** sub-form for the main accounts.</span></span>

4. <span data-ttu-id="452c1-111">Nastavte kódy srážkové daně na stránce **Kódy srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="452c1-111">Set up withholding tax codes on the **Withholding tax codes** page.</span></span>

5. <span data-ttu-id="452c1-112">Nastavte skupiny srážkové daně na stránce **Skupiny srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="452c1-112">Set up withholding tax groups on the **Withholding tax groups** page.</span></span>

6. <span data-ttu-id="452c1-113">Nastavte typy výnosů ze srážkové daně na stránce **Typy** **výnosů ze srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="452c1-113">Set up withholding tax revenue types on the **Withholding tax revenue** **types** page.</span></span>

7. <span data-ttu-id="452c1-114">Nastavte skupiny srážkové daně na stránce **Skupiny srážkové daně položky** pro položku nebo službu.</span><span class="sxs-lookup"><span data-stu-id="452c1-114">Set up withholding tax groups on the **Item withholding tax groups** page for an item or service.</span></span>

8. <span data-ttu-id="452c1-115">Nastavte **Minimální částku faktury** na stránce **Parametry hlavní knihy > Srážková daň**.</span><span class="sxs-lookup"><span data-stu-id="452c1-115">Set up **Minimum invoice amount** on the **General ledger parameters > Withholding tax** page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]