---
title: Nastavení údajů skupiny TDS, PAN a TAN pro dodavatele a zákazníky
description: Toto téma vysvětluje, jak pro dodavatele a zákazníky nastavit informace o skupině daně stržené u zdroje (TDS), trvalém čísle účtu (PAN) a čísle daňového účtu (TAN).
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
ms.openlocfilehash: fd33b1775afefed798f1e9bb7601f4112222c430
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023089"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a><span data-ttu-id="35e3d-103">Nastavení údajů skupiny TDS, PAN a TAN pro dodavatele a zákazníky</span><span class="sxs-lookup"><span data-stu-id="35e3d-103">TDS group, PAN, and TAN information setup for vendors and customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35e3d-104">Toto téma vysvětluje, jak pro dodavatele a zákazníky nastavit informace o skupině daně stržené u zdroje (TDS), trvalém čísle účtu (PAN) a čísle daňového účtu (TAN).</span><span class="sxs-lookup"><span data-stu-id="35e3d-104">This topic explains how to set up information about the Tax Deducted at Source (TDS) group, permanent account number (PAN), and tax account number (TAN) for vendors and customers.</span></span>

1. <span data-ttu-id="35e3d-105">Přejděte na **Závazky \> Dodavatelé \> Všichni dodavatelé** nebo **Pohledávky \> Zákazníci \> Všichni zákazníci**.</span><span class="sxs-lookup"><span data-stu-id="35e3d-105">Go to **Accounts payable \> Vendors \> All vendors** or **Accounts receivable \> Customers \> All customers**.</span></span>

    <span data-ttu-id="35e3d-106">[![Stránka Všichni dodavatelé](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span><span class="sxs-lookup"><span data-stu-id="35e3d-106">[![All vendors page](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span></span>

2. <span data-ttu-id="35e3d-107">V podokně akcí vyberte **Nový** pro vytvoření dodavatele nebo zákazníka a zadejte požadované údaje.</span><span class="sxs-lookup"><span data-stu-id="35e3d-107">On the Action Pane, select **New** to create a vendor or customer, and enter the required details.</span></span> <span data-ttu-id="35e3d-108">Případně vyberte existujícího dodavatele nebo zákazníka.</span><span class="sxs-lookup"><span data-stu-id="35e3d-108">Alternatively, select an existing vendor or customer.</span></span>
3. <span data-ttu-id="35e3d-109">Na pevné záložce **Faktura a dodání** v části **Srážková daň** nastavte možnost **Vypočítat srážkovou daň** na **Ano** k výpočtu srážkové daně, TDS nebo daně vybrané u zdroje (TCS) pro dodavatele nebo zákazníka.</span><span class="sxs-lookup"><span data-stu-id="35e3d-109">On the **Invoice and delivery** FastTab, in the **Withholding tax** section, set the **Calculate withholding tax** option to **Yes** to calculate withholding tax, TDS, or Tax Collected at Source (TCS) for the vendor or customer.</span></span>
4. <span data-ttu-id="35e3d-110">TDS pro nákupní fakturu se počítá na základě výchozí skupiny TDS, která je definována pro dodavatele nebo zákazníka.</span><span class="sxs-lookup"><span data-stu-id="35e3d-110">TDS for a purchase invoice is calculated based on the default TDS group that is defined for the vendor or customer.</span></span> <span data-ttu-id="35e3d-111">V poli **Skupina TDS** vyberte výchozí skupinu TDS.</span><span class="sxs-lookup"><span data-stu-id="35e3d-111">In the **TDS group** field, select the default TDS group.</span></span>

    > [!NOTE]
    > <span data-ttu-id="35e3d-112">Když v seznamu vyberete skupinu TDS v poli **Skupina TDS**, pole **Skupina pro srážkovou daň** a **Skupina TCS** nebudou k dispozici.</span><span class="sxs-lookup"><span data-stu-id="35e3d-112">When you select a TDS group in the **TDS group** field, the **Withholding tax group** and **TCS group** fields become unavailable.</span></span>

5. <span data-ttu-id="35e3d-113">Na pevné záložce **Daňové údaje** v části **Údaje PAN** v poli **Stav** vyberte stav stálého čísla účtu pro dodavatele nebo zákazníka:</span><span class="sxs-lookup"><span data-stu-id="35e3d-113">On the **Tax information** FastTab, in the **PAN information** section, in the **Status** field, select the status of the permanent account number for the vendor or customer:</span></span>

    - <span data-ttu-id="35e3d-114">**Není dostupný** – Prodejce nebo zákazník nemá PAN.</span><span class="sxs-lookup"><span data-stu-id="35e3d-114">**Not available** – The vendor or customer doesn't have a PAN.</span></span>
    - <span data-ttu-id="35e3d-115">**Přijato** – Prodejce nebo zákazník má PAN.</span><span class="sxs-lookup"><span data-stu-id="35e3d-115">**Received** – The vendor or customer has a PAN.</span></span>
    - <span data-ttu-id="35e3d-116">**Požádáno** – Prodejce nebo zákazník požádal o PAN.</span><span class="sxs-lookup"><span data-stu-id="35e3d-116">**Applied** – The vendor or customer has applied for a PAN.</span></span>
    - <span data-ttu-id="35e3d-117">**Neplatný** – Prodejce nebo zákazník má PAN, ale není platné.</span><span class="sxs-lookup"><span data-stu-id="35e3d-117">**Invalid** – The vendor or customer has a PAN, but it isn't valid.</span></span>

6. <span data-ttu-id="35e3d-118">Pokud jste vybrali **Přijato** v poli **Stav**, což označuje, že prodejce nebo zákazník má PAN, zadejte PAN do pole **Číslo**.</span><span class="sxs-lookup"><span data-stu-id="35e3d-118">If you selected **Received** in the **Status** field to indicate that the vendor or customer has a PAN, enter the PAN in the **Number** field.</span></span> <span data-ttu-id="35e3d-119">PAN musí obsahovat pět abecedních znaků, poté čtyři číselné znaky a jeden abecední znak.</span><span class="sxs-lookup"><span data-stu-id="35e3d-119">The PAN must consist of five alphabetic characters, then four numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="35e3d-120">Následuje příklad: **ABCDE1260A**.</span><span class="sxs-lookup"><span data-stu-id="35e3d-120">Here is an example: **ABCDE1260A**.</span></span>
7. <span data-ttu-id="35e3d-121">Pokud jste vybrali **Požádáno** v poli **Stav**, což označuje, že prodejce nebo zákazník požádal o PAN, zadejte referenční číslo do pole **Referenční číslo**.</span><span class="sxs-lookup"><span data-stu-id="35e3d-121">If you selected **Applied** in the **Status** field to indicate that the vendor or customer has applied for PAN, enter the reference number in the **Reference number** field.</span></span>
8. <span data-ttu-id="35e3d-122">V poli **Povaha posuzovaného** vyberte povahu hodnocené kategorie, do které dodavatel nebo zákazník patří:</span><span class="sxs-lookup"><span data-stu-id="35e3d-122">In the **Nature of assessee** field, select the nature of assessee category that the vendor or customer belongs to:</span></span>

    - <span data-ttu-id="35e3d-123">Společnost</span><span class="sxs-lookup"><span data-stu-id="35e3d-123">Company</span></span>
    - <span data-ttu-id="35e3d-124">HUF</span><span class="sxs-lookup"><span data-stu-id="35e3d-124">HUF</span></span>
    - <span data-ttu-id="35e3d-125">Potvrdit</span><span class="sxs-lookup"><span data-stu-id="35e3d-125">Firm</span></span>
    - <span data-ttu-id="35e3d-126">Fyzická osoba</span><span class="sxs-lookup"><span data-stu-id="35e3d-126">Individual</span></span>
    - <span data-ttu-id="35e3d-127">AOP</span><span class="sxs-lookup"><span data-stu-id="35e3d-127">AOP</span></span>
    - <span data-ttu-id="35e3d-128">BOI</span><span class="sxs-lookup"><span data-stu-id="35e3d-128">BOI</span></span>
    - <span data-ttu-id="35e3d-129">Obecní úřad</span><span class="sxs-lookup"><span data-stu-id="35e3d-129">Local authority</span></span>
    - <span data-ttu-id="35e3d-130">Další</span><span class="sxs-lookup"><span data-stu-id="35e3d-130">Others</span></span>

    <span data-ttu-id="35e3d-131">[![Pevná záložka Daňové údaje](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span><span class="sxs-lookup"><span data-stu-id="35e3d-131">[![Tax information FastTab](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span></span>

9. <span data-ttu-id="35e3d-132">V podokně akcí na kartě **Dodavatel** ve skupině **Registrovat** výběrem možnosti **ID registrace** otevřete stránku **Spravovat adresy**.</span><span class="sxs-lookup"><span data-stu-id="35e3d-132">On the Action Pane, on the **Vendor** tab, in the **Registration** group, select **Registration IDs** to open the **Manage addresses** page.</span></span>
10. <span data-ttu-id="35e3d-133">Na stránce **Spravovat adresy** na pevné záložce **Daňové údaje** vyberte možnosti **Přidat** nebo **Upravit** k otevření stránky **Spravovat daňové údaje**, kde můžete udržovat záznam o registraci k dani.</span><span class="sxs-lookup"><span data-stu-id="35e3d-133">On the **Manage addresses** page, on the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>
11. <span data-ttu-id="35e3d-134">Na stránce **Spravovat daňové údaje** na pevné záložce **Srážková daň** do pole **Číslo daňového účtu (TAN)** zadejte TAN.</span><span class="sxs-lookup"><span data-stu-id="35e3d-134">On the **Manage tax information** page, on the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the TAN.</span></span> <span data-ttu-id="35e3d-135">TAN musí obsahovat čtyři abecední znaky, poté pět číselných znaků a jeden abecední znak.</span><span class="sxs-lookup"><span data-stu-id="35e3d-135">The TAN must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="35e3d-136">Následuje příklad: **AFGH54821T**.</span><span class="sxs-lookup"><span data-stu-id="35e3d-136">Here is an example: **AFGH54821T**.</span></span>
12. <span data-ttu-id="35e3d-137">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="35e3d-137">Close the page.</span></span>
