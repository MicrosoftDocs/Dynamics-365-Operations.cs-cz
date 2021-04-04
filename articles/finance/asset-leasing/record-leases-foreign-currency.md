---
title: Záznam leasingů v cizích měnách
description: Toto téma vysvětluje, jak zaznamenávat leasingy v jiných měnách, než je měna účetnictví nebo vykazování.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: fd4d04ae7e89b8ce41ed745c643b8e736484789d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241483"
---
# <a name="record-leases-in-foreign-currencies"></a><span data-ttu-id="50543-103">Záznam leasingů v cizích měnách</span><span class="sxs-lookup"><span data-stu-id="50543-103">Record leases in foreign currencies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50543-104">Majetkové leasingové účty pro leasingy, které jsou v jiných měnách než v účetní měně nebo měně vykazování, jsou stanoveny na stránce **Nastavení hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="50543-104">Asset leasing accounts for leases that are in currencies other than the accounting currency or the reporting currency are established on the **Ledger setup** page.</span></span> <span data-ttu-id="50543-105">Všechny leasingy by měly být zadány v měně transakce.</span><span class="sxs-lookup"><span data-stu-id="50543-105">All leases should be entered in their transaction currency.</span></span> <span data-ttu-id="50543-106">Jinými slovy, měly by být zadány v měně uvedené v leasingové smlouvě.</span><span class="sxs-lookup"><span data-stu-id="50543-106">In other words, they should be entered in the currency that is specified in the lease contract.</span></span> <span data-ttu-id="50543-107">Toto téma vysvětluje, jak zaznamenávat leasingy v jiných měnách, než je měna účetnictví nebo vykazování.</span><span class="sxs-lookup"><span data-stu-id="50543-107">This topic explains how to record leases in currencies other than the accounting or reporting currency.</span></span>

<span data-ttu-id="50543-108">Pokud zadáte leasing v cizí měně, používaný majetek se odepisuje jak v účetní měně, tak v měně vykazování.</span><span class="sxs-lookup"><span data-stu-id="50543-108">If you enter a lease in a foreign currency, the right-of-use (ROU) asset is depreciated in both the accounting currency and the reporting currency.</span></span> <span data-ttu-id="50543-109">Tyto měny jsou konfigurovány na stránce **Nastavení hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="50543-109">These currencies are configured on the **Ledger setup** page.</span></span> <span data-ttu-id="50543-110">Toto chování se také používá u dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="50543-110">This behavior is also used in Fixed assets.</span></span> <span data-ttu-id="50543-111">Když vytvoříte leasing v cizí měně, vyberte měnu transakce v poli **Měna**.</span><span class="sxs-lookup"><span data-stu-id="50543-111">When you create a lease in a foreign currency, select the transaction currency in the **Currency** field.</span></span>

<span data-ttu-id="50543-112">Směnný kurz účetní měny je výchozí hodnota v poli **Směnný kurz účetní měny**.</span><span class="sxs-lookup"><span data-stu-id="50543-112">The exchange rate of the accounting currency is the default value in **Accounting currency exchange rate** field.</span></span> <span data-ttu-id="50543-113">Směnný kurz měny vykazování je výchozí hodnota v poli **Směnný kurz měny vykazování**.</span><span class="sxs-lookup"><span data-stu-id="50543-113">The exchange rate of the reporting currency is the default value in the **Reporting currency exchange rate** field.</span></span> <span data-ttu-id="50543-114">Tyto směnné kurzy byly účinné k datu zahájení leasingu.</span><span class="sxs-lookup"><span data-stu-id="50543-114">These exchange rates were effective on the commencement date of the lease.</span></span> <span data-ttu-id="50543-115">Pole **Směnný kurz účetní měny** a **Směnný kurz měny vykazování** jsou na pevné záložce **Finanční informace a informace o výměně zpráv** na stránce **Podrobnosti o pronájmu**.</span><span class="sxs-lookup"><span data-stu-id="50543-115">The **Accounting currency exchange rate** and **Reporting currency exchange rate** fields, are in the **Financial and reporting exchange information** FastTab, on the **Lease details** page.</span></span>

1. <span data-ttu-id="50543-116">Zaškrtněte políčko **Pevná sazba**, pokud chcete přepsat směnný kurz, který byl automaticky zadán, a poté zadejte nový kurz.</span><span class="sxs-lookup"><span data-stu-id="50543-116">Select the **Fixed rate** check box to override the exchange rate that was automatically entered, and then enter the new rate.</span></span>
2. <span data-ttu-id="50543-117">V ostatních polích zadejte informace, které jsou vyžadovány pro leasing, a poté vyberte **Vytvořit plány**.</span><span class="sxs-lookup"><span data-stu-id="50543-117">In the other fields, enter the information that is required for the lease, and then select **Create schedules**.</span></span>
3. <span data-ttu-id="50543-118">Na nové stránce **Podrobnosti o leasingu** vyberte **Knihy**.</span><span class="sxs-lookup"><span data-stu-id="50543-118">On the new **Lease details** page, select **Books**.</span></span>
4. <span data-ttu-id="50543-119">Na stránce **Leasingová kniha** na kartě **Finanční informace a informace o měně vykazování** ověřte hodnoty polí **Účetní měna počátečního používaného majetku** a **Měna vykazování počátečního používaného majetku**.</span><span class="sxs-lookup"><span data-stu-id="50543-119">On the **Lease book** page, on the **Financial and reporting exchange information** tab, verify the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span> <span data-ttu-id="50543-120">Každé z těchto polí zobrazuje přeložený zůstatek používaného majetku v odpovídající měně.</span><span class="sxs-lookup"><span data-stu-id="50543-120">Each of these fields shows the translated ROU asset balance in the corresponding currency.</span></span> <span data-ttu-id="50543-121">Tato pole se aktualizují vždy, když změníte jakékoli finanční informace.</span><span class="sxs-lookup"><span data-stu-id="50543-121">These fields are updated whenever you change any financial information.</span></span> <span data-ttu-id="50543-122">Vyberte **Vytvořit plány**, než potvrdíte časový plán plateb.</span><span class="sxs-lookup"><span data-stu-id="50543-122">Select **Create schedules** before you confirm the payment schedule.</span></span>

    <span data-ttu-id="50543-123">Položka deníku prvotního uznání zaznamenává používaný majetek, který používá směnné kurzy uvedené v leasingu.</span><span class="sxs-lookup"><span data-stu-id="50543-123">The initial recognition journal entry records the ROU asset that uses the currency exchange rates that are listed on the lease.</span></span> <span data-ttu-id="50543-124">Položka deníku zahrnuje také hodnoty polí **Účetní měna počátečního používaného majetku** a **Měna vykazování počátečního používaného majetku**.</span><span class="sxs-lookup"><span data-stu-id="50543-124">The journal entry also includes the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span>

## <a name="subsequent-measurement-for-foreign-currency-leases"></a><span data-ttu-id="50543-125">Následné ocenění pro leasingy v cizí měně</span><span class="sxs-lookup"><span data-stu-id="50543-125">Subsequent measurement for foreign currency leases</span></span>

<span data-ttu-id="50543-126">Odpisový plán zobrazuje očekávané částky odpisových nákladů v měně vykazování, měně účetnictví a měně transakce.</span><span class="sxs-lookup"><span data-stu-id="50543-126">The depreciation schedule shows the expected depreciation expense amounts in the reporting currency, the accounting currency, and the transaction currency.</span></span>

<span data-ttu-id="50543-127">Chcete-li zobrazit zůstatky používaného majetku a částky odpisů buď v měně vykazování, nebo v účetní měně, otevřete stránku **Odpisový plán majetku** a zaškrtněte políčko **Zobrazit částky v účetní měně** nebo **Zobrazit částky ve vykazované měně**.</span><span class="sxs-lookup"><span data-stu-id="50543-127">To view the ROU asset balances and depreciation amounts in either the reporting currency or the accounting currency, open the **Asset depreciation schedule** page, and select the **Show accounting currency amounts** or **Show reporting currency amounts** check box.</span></span>

<span data-ttu-id="50543-128">Když vytvoříte položky deníku odpisů proti leasingu denominovanému v cizí měně, použije položka směnné kurzy uvedené v leasingu.</span><span class="sxs-lookup"><span data-stu-id="50543-128">When you create the depreciation expense journal entries against a lease that is denominated in a foreign currency, the entry uses the exchange rates that are listed on the lease.</span></span> <span data-ttu-id="50543-129">Použije také hodnoty polí **Účetní měna počátečního používaného majetku** a **Měna vykazování počátečního používaného majetku**.</span><span class="sxs-lookup"><span data-stu-id="50543-129">It also uses the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span>

<span data-ttu-id="50543-130">Konečnou částku odpisových výdajů lze vypočítat pomocí mírně odlišného směnného kurzu, takže používaný majetek je plně odepsán jak v účetní měně, tak v měně vykazování.</span><span class="sxs-lookup"><span data-stu-id="50543-130">The final depreciation expense amount can be calculated by using a slightly different exchange rate, so that the ROU asset is fully depreciated in both the accounting currency and the reporting currency.</span></span>

<span data-ttu-id="50543-131">Pokud byl leasing překlasifikován na **Odložený nájem**, systém automaticky vymaže směnné kurzy účetní měny a měny vykazování, pokud již byly definovány.</span><span class="sxs-lookup"><span data-stu-id="50543-131">If the lease has been reclassified as **Deferred rent**, the system automatically clears the exchange rates of the accounting and reporting currencies, if they have already been defined.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]