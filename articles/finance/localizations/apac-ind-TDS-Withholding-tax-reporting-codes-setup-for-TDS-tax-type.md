---
title: Nastavení kódů vykazování srážkové daně pro typy daně TDS
description: Kódy vykazování srážkové daně se používají ke generování výkazů Form 26Q a Form 27Q pro daň odečtenou u zdroje (TDS). Toto téma vysvětluje, jak nastavit kroky pro kódů vykazování srážkové daně, abyste mohli nastavit kódy vykazování TDS.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1f9325d182f89b98e8b943ae047c55e7e1aeb02f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023098"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a><span data-ttu-id="85027-104">Nastavení kódů vykazování srážkové daně pro typy daně TDS</span><span class="sxs-lookup"><span data-stu-id="85027-104">Set up withholding tax reporting codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85027-105">Kódy vykazování srážkové daně se používají ke generování výkazů Form 26Q a Form 27Q pro daň odečtenou u zdroje (TDS).</span><span class="sxs-lookup"><span data-stu-id="85027-105">Withholding tax reporting codes are used to generate Form 26Q and Form 27Q statements for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="85027-106">Toto téma vysvětluje, jak nastavit kroky pro kódů vykazování srážkové daně, abyste mohli nastavit kódy vykazování TDS.</span><span class="sxs-lookup"><span data-stu-id="85027-106">This topic explains how to set up withholding tax reporting codes steps so that you can set up TDS reporting codes.</span></span>

1. <span data-ttu-id="85027-107">Přejděte do nabídky **Daň \> Nastavení \> Srážková daň \> Kódy vykazování srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="85027-107">Go to **Tax \> Setup \> Withholding tax \> Withholding tax reporting codes**.</span></span>

    <span data-ttu-id="85027-108">[![Stránka s kódy pro vykazování srážkové daně](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span><span class="sxs-lookup"><span data-stu-id="85027-108">[![Withholding tax reporting codes page](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span></span>

2. <span data-ttu-id="85027-109">V poli **Typ daně** vyberte **TDS** pro definování kódů vykazování srážkové daně pro typ daně TDS.</span><span class="sxs-lookup"><span data-stu-id="85027-109">In the **Tax type** field, select **TDS** to define withholding tax reporting codes for the TDS tax type.</span></span>
3. <span data-ttu-id="85027-110">V poli **Komponenta srážkové daně** vyberte komponentu TDS, pro kterou definujete kód vykazování srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="85027-110">In the **Withholding tax component** field, select the TDS component to that you're defining the withholding tax reporting code for.</span></span> <span data-ttu-id="85027-111">V poli **Skupina komponent srážkové daně** se zobrazuje skupina komponent TDS, která byla definována pro komponentu TDS, kterou definujete.</span><span class="sxs-lookup"><span data-stu-id="85027-111">The **Withholding tax component group** field shows the TDS component group that was defined for the TDS component that you're defining.</span></span>

    <span data-ttu-id="85027-112">Pole **Kód sekce** na pevné záložce **Obecné** zobrazuje kód sekce, který je připojen ke skupině komponent TDS.</span><span class="sxs-lookup"><span data-stu-id="85027-112">The **Section code** field on the **General** FastTab shows the section code that is attached to the TDS component group.</span></span>

4. <span data-ttu-id="85027-113">Na pevné záložce **Obecné** v poli **Kód vykazování** vyberte kód vykazování TDS:</span><span class="sxs-lookup"><span data-stu-id="85027-113">On the **General** FastTab, in the **Reporting code** field, select the TDS reporting code:</span></span>

    - <span data-ttu-id="85027-114">TDS</span><span class="sxs-lookup"><span data-stu-id="85027-114">TDS</span></span>
    - <span data-ttu-id="85027-115">TCS</span><span class="sxs-lookup"><span data-stu-id="85027-115">TCS</span></span>
    - <span data-ttu-id="85027-116">Příplatek</span><span class="sxs-lookup"><span data-stu-id="85027-116">Surcharge</span></span>
    - <span data-ttu-id="85027-117">PE\_Cess</span><span class="sxs-lookup"><span data-stu-id="85027-117">PE\_Cess</span></span>
    - <span data-ttu-id="85027-118">SHE\_Cess</span><span class="sxs-lookup"><span data-stu-id="85027-118">SHE\_Cess</span></span>

5. <span data-ttu-id="85027-119">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="85027-119">Close the page.</span></span>
