---
title: Nastavení platebního kalendáře s přidělením TDS
description: Toto téma vysvětluje, jak nastavit plány plateb s alokací daně odečtené u zdroje (TDS).
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
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023096"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a><span data-ttu-id="5eccb-103">Nastavení platebního kalendáře s přidělením TDS</span><span class="sxs-lookup"><span data-stu-id="5eccb-103">Set up payment schedules with TDS allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5eccb-104">Toto téma vysvětluje, jak nastavit plány plateb s alokací daně odečtené u zdroje (TDS).</span><span class="sxs-lookup"><span data-stu-id="5eccb-104">This topic explains how to set up payment schedules with Tax Deducted at Source (TDS) allocation.</span></span>

1. <span data-ttu-id="5eccb-105">Přejděte do nabídky **Závazky \> Nastavení platby \> Platební kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="5eccb-105">Go to **Accounts payable \> Payment setup \> Payment schedules**.</span></span>

    <span data-ttu-id="5eccb-106">[![Stránka Platební kalendáře](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span><span class="sxs-lookup"><span data-stu-id="5eccb-106">[![Payment schedules page](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span></span>

2. <span data-ttu-id="5eccb-107">V podokně akcí vyberte **Nový** pro vytvoření platebního kalendáře a zadejte požadované údaje.</span><span class="sxs-lookup"><span data-stu-id="5eccb-107">On the Action Pane, select **New** to create a payment schedule, and enter the required details.</span></span>
3. <span data-ttu-id="5eccb-108">V poli **Přidělení** vyberte metodu, která se použije k alokaci platby pro časový plán plateb:</span><span class="sxs-lookup"><span data-stu-id="5eccb-108">In the **Allocation** field, select the method to use to allocate the payment for the payment schedule:</span></span>

    - <span data-ttu-id="5eccb-109">Celkem</span><span class="sxs-lookup"><span data-stu-id="5eccb-109">Total</span></span>
    - <span data-ttu-id="5eccb-110">Pevná částka</span><span class="sxs-lookup"><span data-stu-id="5eccb-110">Fixed amount</span></span>
    - <span data-ttu-id="5eccb-111">Fixní množství</span><span class="sxs-lookup"><span data-stu-id="5eccb-111">Fixed quantity</span></span>
    - <span data-ttu-id="5eccb-112">Určeno</span><span class="sxs-lookup"><span data-stu-id="5eccb-112">Specified</span></span>

    <span data-ttu-id="5eccb-113">Pole **Přidělení srážkové daně** zobrazuje metodu přidělení TDS pro plán plateb.</span><span class="sxs-lookup"><span data-stu-id="5eccb-113">The **Withholding tax allocation** field shows the TDS allocation method for the payment schedule.</span></span> <span data-ttu-id="5eccb-114">Pokud vyberete **Součet** v poli **Přidělení**, pole **Přidělení srážkové daně** je automaticky nastaveno na **Součet**.</span><span class="sxs-lookup"><span data-stu-id="5eccb-114">If you select **Total** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Total**.</span></span> <span data-ttu-id="5eccb-115">Pokud vyberete **Pevná částka**, **Pevné množství** nebo **Specifikováno** v poli **Přidělení**, pole **Přidělení srážkové daně** je automaticky nastaveno na **Proporčně**.</span><span class="sxs-lookup"><span data-stu-id="5eccb-115">If you select **Fixed amount**, **Fixed quantity**, or **Specified** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Proportionally**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5eccb-116">Pokud je pole **Přidělení srážkové daně** nastaveno na **Součet**, splátky plateb se počítají na základě hrubé částky, která zahrnuje částku TDS.</span><span class="sxs-lookup"><span data-stu-id="5eccb-116">If the **Withholding tax allocation** field is set to **Total**, the payment installments are calculated based on the gross amount, which includes the TDS amount.</span></span> <span data-ttu-id="5eccb-117">Pokud je pole **Přidělení srážkové daně** nastaveno na **Proporčně**, splátky plateb se počítají na základě čisté částky faktury po odečtení částky TDS.</span><span class="sxs-lookup"><span data-stu-id="5eccb-117">If the **Withholding tax allocation** field is set to **Proportionally**, the payment installments are calculated based on the net invoice amount after the TDS amount is deducted.</span></span>

4. <span data-ttu-id="5eccb-118">Zadejte další požadované údaje a poté zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5eccb-118">Enter the other required details, and then close the page.</span></span>
