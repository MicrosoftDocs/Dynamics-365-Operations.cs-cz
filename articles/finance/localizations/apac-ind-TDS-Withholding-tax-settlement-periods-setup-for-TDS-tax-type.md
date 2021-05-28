---
title: Nastavení období vyrovnání srážkové daně pro typ daně TDS
description: Toto téma vysvětluje, jak nastavit období vypořádání pro období vypořádání daně odečtené u zdroje (TDS).
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
ms.openlocfilehash: 9430bc1386f127d02b598d6cad1b53f66e0cf2ba
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023075"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a><span data-ttu-id="040da-103">Nastavení období vyrovnání srážkové daně pro typ daně TDS</span><span class="sxs-lookup"><span data-stu-id="040da-103">Set up withholding tax settlement periods for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="040da-104">Toto téma vysvětluje, jak nastavit období vypořádání pro období vypořádání daně odečtené u zdroje (TDS).</span><span class="sxs-lookup"><span data-stu-id="040da-104">This topic explains how to set up settlement periods for Tax Deducted at Source (TDS) settlement periods.</span></span>

1. <span data-ttu-id="040da-105">Přejděte na **Daň \> Nepřímé daně \> Srážková daň \> Období vypořádání srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="040da-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="040da-106">[![Stránka období vyrovnání srážkové daně](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span><span class="sxs-lookup"><span data-stu-id="040da-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span></span>

2. <span data-ttu-id="040da-107">V poli **Typ daně** vyberte **TDS** a nastavte období vypořádání srážkové daně pro typ daně TDS.</span><span class="sxs-lookup"><span data-stu-id="040da-107">In the **Tax type** field, select **TDS** to set up withholding tax settlement periods for the TDS tax type.</span></span>
3. <span data-ttu-id="040da-108">Volbou možnosti **Nová položka** vytvořte řádek.</span><span class="sxs-lookup"><span data-stu-id="040da-108">Select **New** to create a line.</span></span>
4. <span data-ttu-id="040da-109">Do pole **Období vypořádání** zadejte název období vypořádání TDS.</span><span class="sxs-lookup"><span data-stu-id="040da-109">In the **Settlement period** field, enter a name for the TDS settlement period.</span></span>
5. <span data-ttu-id="040da-110">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="040da-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="040da-111">V poli **Autorita srážkové daně** vyberte autoritu TDS, pro kterou definujete období vypořádání TDS.</span><span class="sxs-lookup"><span data-stu-id="040da-111">In the **Withholding tax authority** field, select the TDS authority that you're defining the TDS settlement period for.</span></span>
7. <span data-ttu-id="040da-112">Na pevné záložce **Obecné** v poli **Interval období** vyberte typ intervalu období pro období vypořádání TDS.</span><span class="sxs-lookup"><span data-stu-id="040da-112">On the **General** FastTab, in the **Period interval** field, select the type of period interval for the TDS settlement period.</span></span>
8. <span data-ttu-id="040da-113">Do pole **Počet jednotek** zadejte počet jednotek pro typ intervalu období.</span><span class="sxs-lookup"><span data-stu-id="040da-113">In the **Number of units** field, specify the number of units for the period interval type.</span></span>
9. <span data-ttu-id="040da-114">Na pevné záložce **Období** v poli **Od data** vyberte datum zahájení období vypořádání TDS.</span><span class="sxs-lookup"><span data-stu-id="040da-114">On the **Periods** FastTab, in the **From date** field, select the start date for the TDS settlement period.</span></span> <span data-ttu-id="040da-115">V poli **Do data** vyberte koncové datum.</span><span class="sxs-lookup"><span data-stu-id="040da-115">In the **To date** field, select the end date.</span></span>
10. <span data-ttu-id="040da-116">Chcete-li vytvořit následující období vypořádání TDS pro stávající období na základě intervalu období a jednotek období, vyberte **Nové období**.</span><span class="sxs-lookup"><span data-stu-id="040da-116">To create a subsequent TDS settlement period for an existing period, based on the period interval and period units, select **New period**.</span></span>
11. <span data-ttu-id="040da-117">Chcete-li zobrazit podrobnosti pravidelného vypořádání TDS, které se spouští pro konkrétní období vypořádání, vyberte **Platby srážkové daně** k otevření stránky **Platba srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="040da-117">To view the details of the periodic TDS settlement that is run for a specific settlement period, select **Withholding tax payments** to open the **Withholding tax payment** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="040da-118">Chcete-li spustit proces periodického vypořádání TDS, přejděte na **Hlavní kniha \> Pefiodické \> Srážková daň \> Platba srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="040da-118">To run the periodic TDS settlement process, go to **General ledger \> Periodic \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="040da-119">[![Stránka Platba srážkové daně](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span><span class="sxs-lookup"><span data-stu-id="040da-119">[![Withholding tax payment page](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span></span>

12. <span data-ttu-id="040da-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="040da-120">Close the page.</span></span>
