---
title: Nastavení úřadů srážkové daně pro typ daně TDS
description: Toto téma vysvětluje, jak nastavit autority daně odečtené u zdroje (TDS).
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
ms.openlocfilehash: 5375363a9b1383a83e80fc3c4b841780adab4172
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023080"
---
# <a name="set-up-withholding-tax-authorities-for-the-tds-tax-type"></a><span data-ttu-id="7d839-103">Nastavení úřadů srážkové daně pro typ daně TDS</span><span class="sxs-lookup"><span data-stu-id="7d839-103">Set up withholding tax authorities for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d839-104">Toto téma vysvětluje, jak nastavit autority daně odečtené u zdroje (TDS).</span><span class="sxs-lookup"><span data-stu-id="7d839-104">This topic explains how to set up Tax Deducted at Source (TDS) authorities.</span></span>

1. <span data-ttu-id="7d839-105">Přejděte na **Daň \> Nepřímé daně \> Autority nepřímé daně**.</span><span class="sxs-lookup"><span data-stu-id="7d839-105">Go to **Tax \> Indirect taxes \> Withholding tax authorities**.</span></span>

    <span data-ttu-id="7d839-106">[![Stránka Autority srážkové daně](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span><span class="sxs-lookup"><span data-stu-id="7d839-106">[![Withholding tax authorities page](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span></span>

2. <span data-ttu-id="7d839-107">V poli **Typ daně** vyberte **TDS** a nastavte autority srážkové daně pro typ daně TDS.</span><span class="sxs-lookup"><span data-stu-id="7d839-107">In the **Tax type** field, select **TDS** to set up withholding tax authorities for the TDS tax type.</span></span>
3. <span data-ttu-id="7d839-108">V podokně Akce vyberte možnost **Nový** a vytvořte řádek.</span><span class="sxs-lookup"><span data-stu-id="7d839-108">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="7d839-109">Do pole **Autorita srážkové daně** zadejte název autority TDS.</span><span class="sxs-lookup"><span data-stu-id="7d839-109">In the **Withholding tax authority** field, enter a name for the TDS authority.</span></span>
5. <span data-ttu-id="7d839-110">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="7d839-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="7d839-111">Na pevné záložce **Obecné** v poli **Účet dodavatele** vyberte účet dodavatele pro autoritu TDS.</span><span class="sxs-lookup"><span data-stu-id="7d839-111">On the **General** FastTab, in the **Vendor account** field, select the vendor account for the TDS authority.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7d839-112">Musíte určit název banky, kde budou uloženy finanční prostředky, které dluží dodavateli autority TDS.</span><span class="sxs-lookup"><span data-stu-id="7d839-112">You must define the name of the bank where funds that are owed to the TDS authority vendor will be deposited.</span></span> <span data-ttu-id="7d839-113">Název banky je definován na stránce **Bankovní účty** stránka (**Závazky \> Všichni dodavatelé \> Dodavatel \> Nastavení \> Bankovní účty**).</span><span class="sxs-lookup"><span data-stu-id="7d839-113">The bank's name is defined on the **Bank accounts** page (**Accounts payable \> All vendors \> Vendor \> Set up \> Bank accounts**).</span></span>

7. <span data-ttu-id="7d839-114">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="7d839-114">Close the page.</span></span>
