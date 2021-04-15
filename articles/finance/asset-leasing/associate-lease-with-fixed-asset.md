---
title: Přidružení dlouhodobého majetku k leasingům
description: V tématu je vysvětleno, jak přidružit existující dlouhodobý majetek k novému leasingu.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0e2261755d98ee38564b4b864daf8e79551d1239
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814073"
---
# <a name="associate-fixed-assets-with-leases"></a><span data-ttu-id="fd91c-103">Přidružení dlouhodobého majetku k leasingům</span><span class="sxs-lookup"><span data-stu-id="fd91c-103">Associate fixed assets with leases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd91c-104">V tématu je vysvětleno, jak přidružit existující dlouhodobý majetek k novému leasingu.</span><span class="sxs-lookup"><span data-stu-id="fd91c-104">The topic explains how to associate an existing fixed asset with a new lease.</span></span> <span data-ttu-id="fd91c-105">Když přidružíte dlouhodobý majetek k leasingu, bude hodnotou používaného majetku při počátečním uznání pořizovací cena dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="fd91c-105">When you associate a fixed asset with a lease, the right-of-use (ROU) asset value at initial recognition will be the acquisition cost of the fixed asset.</span></span>

<span data-ttu-id="fd91c-106">Než budete moci přidružit dlouhodobý majetek k leasingu, musíte vytvořit záznam pro dlouhodobý majetek v části Dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="fd91c-106">Before you can associate a fixed asset with a lease, you must create a record for the fixed asset in Fixed assets.</span></span> <span data-ttu-id="fd91c-107">Pak na stránce **Shrnutí leasingu** musíte vytvořit leasing a propojit majetek s tímto leasingem.</span><span class="sxs-lookup"><span data-stu-id="fd91c-107">Then, on the **Lease summary** page, you must create a lease and link the asset to that lease.</span></span>

1. <span data-ttu-id="fd91c-108">Přidejte leasing podle pokynů v části [Přidání nebo kopírování leasingů](add-lease.md).</span><span class="sxs-lookup"><span data-stu-id="fd91c-108">Add a lease by following the steps in [Add or copy leases](add-lease.md).</span></span> <span data-ttu-id="fd91c-109">Na stránce **Přidat leasing** v poli **Číslo dlouhodobého majetku** vyberte majetek, který ještě nebyl získán.</span><span class="sxs-lookup"><span data-stu-id="fd91c-109">On the **Add lease** page, in the **Fixed asset number** field, select the asset that hasn't yet been acquired.</span></span>
2. <span data-ttu-id="fd91c-110">Vyberte **Knihy** a potvrďte platební kalendář.</span><span class="sxs-lookup"><span data-stu-id="fd91c-110">Select **Books**, and confirm the payment schedule.</span></span>
3. <span data-ttu-id="fd91c-111">Vyberte **Počáteční uznání**.</span><span class="sxs-lookup"><span data-stu-id="fd91c-111">Select **Initial recognition**.</span></span>
4. <span data-ttu-id="fd91c-112">Vyberte **Deník leasingu majetku**.</span><span class="sxs-lookup"><span data-stu-id="fd91c-112">Select **Asset leasing journal**.</span></span>

    <span data-ttu-id="fd91c-113">Položka deníku počátečního uznání pro leasing debetuje dlouhodobý majetek pro částku, která je obvykle debetována z účtu používaného majetku.</span><span class="sxs-lookup"><span data-stu-id="fd91c-113">The initial recognition journal entry for the lease debits the fixed asset for the amount that is usually debited to the ROU asset account.</span></span>

    <span data-ttu-id="fd91c-114">Nyní můžete zobrazit typ transakce a knihu pro dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="fd91c-114">You can now view the transaction type and book for the fixed asset.</span></span>

5. <span data-ttu-id="fd91c-115">Vyberte **Podrobnosti deníku**.</span><span class="sxs-lookup"><span data-stu-id="fd91c-115">Select **Journal details**.</span></span>
6. <span data-ttu-id="fd91c-116">Vyberte **Řádky** pro zobrazení jednotlivých řádků pro položku deníku.</span><span class="sxs-lookup"><span data-stu-id="fd91c-116">Select **Lines** to view the individual lines for the journal entry.</span></span>
7. <span data-ttu-id="fd91c-117">Vyberte řádek deníku, který obsahuje majetek, a poté vyberte kartu **Dlouhodobý majetek**.</span><span class="sxs-lookup"><span data-stu-id="fd91c-117">Select the journal line that contains the asset, and then select the **Fixed Assets** tab.</span></span>

    <span data-ttu-id="fd91c-118">Karta **Dlouhodobý majetek** ukazuje typ transakce a knihu.</span><span class="sxs-lookup"><span data-stu-id="fd91c-118">The **Fixed assets** tab shows the transaction type and the book.</span></span> <span data-ttu-id="fd91c-119">Ve výchozím nastavení je pole **Typ transakce** nastaveno na **Pořizovací cena** a pole **Kniha** je nastaveno na aktuální knihu pro dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="fd91c-119">By default, the **Transaction type** field is set to **Acquisition**, and the **Book** field is set to the current book for the fixed asset.</span></span>

<span data-ttu-id="fd91c-120">Po zaúčtování položky deníku počátečního uznání se transakce zobrazí jako transakce pořízení pro dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="fd91c-120">After you post the initial recognition journal entry, the transaction appears as an acquisition transaction for the fixed asset.</span></span> <span data-ttu-id="fd91c-121">Chcete-li zobrazit tabulku transakcí, přejděte na **Dlouhodobý majetek \> Dlouhodobý majetek \> Dlouhodobý majetek**, vyberte příslušný majetek a poté vyberte **Ocenění**.</span><span class="sxs-lookup"><span data-stu-id="fd91c-121">To view the transaction table, go to **Fixed assets \> Fixed assets \> Fixed assets**, select the appropriate asset, and then select **Valuations**.</span></span> <span data-ttu-id="fd91c-122">Měli byste vidět, že položka deníku počátečního uznání vytvořila transakci pořízení pro zadaný dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="fd91c-122">You should see that the initial recognition journal entry has created an acquisition transaction for the specified fixed asset.</span></span>

<span data-ttu-id="fd91c-123">Dlouhodobý majetek lze nyní odepisovat pomocí standardní funkce odpisování v části Dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="fd91c-123">The fixed asset can now be depreciated by using the standard depreciation functionality in Fixed assets.</span></span> <span data-ttu-id="fd91c-124">Další informace o odpisech naleznete v tématu [Odpisové metody a způsoby odpisu](../fixed-assets/depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="fd91c-124">For more information about depreciation, see [Depreciation methods and conventions](../fixed-assets/depreciation-methods-conventions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="fd91c-125">Pokud přidružíte dlouhodobý majetek k leasingu, tlačítka **Odpis majetku** a **Snížení hodnoty leasingu** jsou v leasingu majetku deaktivována.</span><span class="sxs-lookup"><span data-stu-id="fd91c-125">If you associate a fixed asset with a lease, the **Asset depreciation** and **Lease impairment** buttons are disabled in Asset leasing.</span></span> <span data-ttu-id="fd91c-126">Transakce odpisů majetku a snížení hodnoty leasingu si můžete prohlédnout v části Dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="fd91c-126">You can view asset depreciation and lease impairment transactions from Fixed assets.</span></span> <span data-ttu-id="fd91c-127">Tlačítko **Transakce majetku**, které otevírá formulář dotazu, je také deaktivováno.</span><span class="sxs-lookup"><span data-stu-id="fd91c-127">The **Asset transactions** button, which opens an inquiry form is also disabled.</span></span> <span data-ttu-id="fd91c-128">Můžete také otevřít formulář dotazu **Transakce majetku** v části Dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="fd91c-128">You can also open the **Asset transactions** inquiry form in Fixed assets.</span></span>  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]