---
title: Hlavní kniha globálního účetnictví zásob
description: Toto téma popisuje účetní knihy Globálního účetnictví zásob, které jsou definovány kombinací měny, kalendáře, konvence a přidružení k právnické osobě.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea3434675aa3b7f2304be93ef9b489747994fa9d
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273124"
---
# <a name="global-inventory-accounting-ledger"></a><span data-ttu-id="162a9-103">Hlavní kniha globálního účetnictví zásob</span><span class="sxs-lookup"><span data-stu-id="162a9-103">Global Inventory Accounting ledger</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="162a9-104">Globální účetnictví zásob má vlastní sadu účetních knih.</span><span class="sxs-lookup"><span data-stu-id="162a9-104">Global Inventory Accounting has its own set of ledgers.</span></span> <span data-ttu-id="162a9-105">Pokaždé, když je pro příslušnou právnickou osobu zpracována transakce související se zásobami, může systém podle potřeby tuto transakci zaúčtovat do libovolného počtu účetních knih globálního účetnictví zásob.</span><span class="sxs-lookup"><span data-stu-id="162a9-105">Each time an inventory-related transaction is processed for a relevant legal entity, the system can account for that transaction in any number of Global Inventory Accounting ledgers, as required.</span></span>

<span data-ttu-id="162a9-106">Hlavní kniha je registr opatření na straně má dáti a dal.</span><span class="sxs-lookup"><span data-stu-id="162a9-106">A ledger is a register of debit and credit measures.</span></span> <span data-ttu-id="162a9-107">Tato opatření jsou klasifikována pomocí nákladových položek a účtů podřízené knihy.</span><span class="sxs-lookup"><span data-stu-id="162a9-107">These measures are classified by using cost elements and subledger accounts.</span></span> <span data-ttu-id="162a9-108">Hlavní kniha Globálního účetnictví zásob je definována kombinací měny, kalendáře, konvence a přidružení k právnické osobě.</span><span class="sxs-lookup"><span data-stu-id="162a9-108">A Global Inventory Accounting ledger is defined by its combination of a currency, a calendar, a convention, and an association with a legal entity.</span></span>

<span data-ttu-id="162a9-109">Chcete-li nastavit své účetní knihy globálního účetnictví zásob, přejděte na **Globální účetnictví zásob \> Založit \> Účetní knihy globálního účetnictví zásob**.</span><span class="sxs-lookup"><span data-stu-id="162a9-109">To set up your Global Inventory Accounting ledgers, go to **Global inventory accounting \> Setup \> Global inventory accounting ledgers**.</span></span> <span data-ttu-id="162a9-110">U každé účetní knihy je třeba nastavit tato pole:</span><span class="sxs-lookup"><span data-stu-id="162a9-110">For each ledger, set the following fields:</span></span>

- <span data-ttu-id="162a9-111">**Název** – Zadejte název účetní knihy.</span><span class="sxs-lookup"><span data-stu-id="162a9-111">**Name** – Enter the name of the ledger.</span></span>
- <span data-ttu-id="162a9-112">**Popis** - zadejte popis účetní knihy.</span><span class="sxs-lookup"><span data-stu-id="162a9-112">**Description** – Enter a description of the ledger.</span></span>
- <span data-ttu-id="162a9-113">**Fiskální kalendář** - Určete fiskální kalendář pro hlavní knihu.</span><span class="sxs-lookup"><span data-stu-id="162a9-113">**Fiscal calendar** – Specify the fiscal calendar for the ledger.</span></span>
- <span data-ttu-id="162a9-114">**Typ měny a směnného kurzu** - Pomocí polí na této pevné záložce vyberte účetní měnu, kterou účetní kniha používá, a typ směnného kurzu.</span><span class="sxs-lookup"><span data-stu-id="162a9-114">**Currency and exchange rate type** – Use the fields on this FastTab to select the accounting currency that the ledger uses, and the exchange rate type.</span></span> <span data-ttu-id="162a9-115">Měna, kterou vyberete, se může lišit od měny, kterou právnická osoba používá.</span><span class="sxs-lookup"><span data-stu-id="162a9-115">The currency that you select can differ from the currency that the legal entity uses.</span></span> <span data-ttu-id="162a9-116">V globálním účetnictví zásob mohou uživatelé definovat tolik účetních knih pro výpočet nákladů, kolik požadují.</span><span class="sxs-lookup"><span data-stu-id="162a9-116">In Global Inventory Accounting, users can define as many costing ledgers as they require.</span></span> <span data-ttu-id="162a9-117">Globální účetnictví zásob podporuje účtování zásob ve více měnách a ve více oceněních.</span><span class="sxs-lookup"><span data-stu-id="162a9-117">Global Inventory Accounting supports inventory accounting in multiple currencies and in multiple valuations.</span></span> <span data-ttu-id="162a9-118">Nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="162a9-118">Set the following fields:</span></span>

    - <span data-ttu-id="162a9-119">**Měna** - Vyberte měnu výpočtu nákladů, ve které jsou udržovány hodnoty související se zásobami.</span><span class="sxs-lookup"><span data-stu-id="162a9-119">**Currency** – Select the costing currency that inventory-related values are maintained in.</span></span> <span data-ttu-id="162a9-120">Mezi tyto hodnoty patří hodnota zásob, náklady na prodané zboží, zásoby na cestě a všechny druhy odchylek.</span><span class="sxs-lookup"><span data-stu-id="162a9-120">These values include the inventory value, cost of goods sold, inventory in transit, and all kinds of variance.</span></span>
    - <span data-ttu-id="162a9-121">**Typ směnného kurzu** - Vyberte směnný kurz, který by měl systém použít k převodu částky transakce v měně transakce a standardních nákladů na položky do měny kalkulace.</span><span class="sxs-lookup"><span data-stu-id="162a9-121">**Exchange rate type** – Select the exchange rate that the system should use to convert the transaction amount in the transaction currency and the standard cost of the items into the costing currency.</span></span>

- <span data-ttu-id="162a9-122">**Název konvence** - Upřesněte konvenci.</span><span class="sxs-lookup"><span data-stu-id="162a9-122">**Convention name** – Specify a convention.</span></span> <span data-ttu-id="162a9-123">Konvence je kolekcí zásad, které určují, jak budou náklady účtovány v této účetní knize.</span><span class="sxs-lookup"><span data-stu-id="162a9-123">A convention is a collection of policies that establish how costs will be accounted in this ledger.</span></span>
- <span data-ttu-id="162a9-124">**Právnická osoba** - Hlavní kniha bude účtovat dokumenty, které jsou zaúčtovány vybrané právnické osobě.</span><span class="sxs-lookup"><span data-stu-id="162a9-124">**Legal entity** – The ledger will account the documents that are posted to the selected legal entity.</span></span>
- <span data-ttu-id="162a9-125">**Plnění** - Vyberte, zda mají být transakce zásob, které byly vytvořeny před vytvořením hlavní knihy, zpracovány podle měny a konvence v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="162a9-125">**Priming** – Select whether inventory transactions that were created before the ledger was created should be processed according to the currency and convention in the ledger.</span></span> <span data-ttu-id="162a9-126">Vyberte jednu z následujících hodnot:</span><span class="sxs-lookup"><span data-stu-id="162a9-126">Select one of the following values:</span></span>

    - <span data-ttu-id="162a9-127">**Aktivováno** - Hlavní kniha by měla zpracovat transakce, které byly vytvořeny před vytvořením hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="162a9-127">**Activated** – The ledger should process transactions that were created before the ledger was created.</span></span>
    - <span data-ttu-id="162a9-128">**Deaktivováno** - Hlavní kniha by měla zpracovat pouze transakce, které jsou vytvořeny po vytvoření hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="162a9-128">**Deactivated** – The ledger should process only transactions that are created after the ledger was created.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="162a9-129">**Nebudete** moci se vrátit a nastavit toto pole po zadání nových dokumentů.</span><span class="sxs-lookup"><span data-stu-id="162a9-129">You will **not** be able to come back and set this field after you enter new documents.</span></span>

- <span data-ttu-id="162a9-130">**Stav** - Systém automaticky nastaví stav nově vytvořených knih na *Připravit*.</span><span class="sxs-lookup"><span data-stu-id="162a9-130">**Status** – The system automatically sets the status of newly created ledgers to *Prepare*.</span></span>
