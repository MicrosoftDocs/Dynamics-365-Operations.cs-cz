---
title: Plán pro globální adresář a další adresáře
description: Toto téma popisuje, co je třeba zvážit a jaká rozhodnutí je třeba učinit během procesu plánování, před nastavením a konfigurací globálního adresáře a jakéhokoli dalšího adresáře.
author: msftbrking
manager: AnnBe
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aeed503500abf4f4b7ccf166f589d09bba306689
ms.sourcegitcommit: 7a855deed9f95ca2589f38db214890464b2b9061
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/13/2020
ms.locfileid: "2951202"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a><span data-ttu-id="a5299-103">Plán pro globální adresář a další adresáře</span><span class="sxs-lookup"><span data-stu-id="a5299-103">Plan for the global address book and other address books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5299-104">Toto téma popisuje, co je třeba zvážit a jaká rozhodnutí je třeba učinit během procesu plánování, před nastavením a konfigurací globálního adresáře a jakéhokoli dalšího adresáře.</span><span class="sxs-lookup"><span data-stu-id="a5299-104">This topic describes the considerations and decisions that you must make during the planning process, before you set up and configure the global address book and any additional address books.</span></span> <span data-ttu-id="a5299-105">Některá rozhodnutí vyžadují potvrzení rozhodnutí, která byla učiněna pro další oblasti produktu, jako je například hierarchie organizace.</span><span class="sxs-lookup"><span data-stu-id="a5299-105">Some of the decisions will require that you confirm the decisions that have been made for other areas of the product, such as the organization hierarchy.</span></span>

## <a name="global-address-book"></a><span data-ttu-id="a5299-106">Globální adresář</span><span class="sxs-lookup"><span data-stu-id="a5299-106">Global address book</span></span>

<span data-ttu-id="a5299-107">Než začnete pracovat s globálním adresářem, je třeba určit pro něj výchozí hodnoty.</span><span class="sxs-lookup"><span data-stu-id="a5299-107">Before you begin to work with the global address book, you must determine the default values for it.</span></span> <span data-ttu-id="a5299-108">Tyto výchozí hodnoty jsou následně použity pro všechny další adresáře, které vytvoříte.</span><span class="sxs-lookup"><span data-stu-id="a5299-108">These default values are then used for any additional address books that you create.</span></span>

<span data-ttu-id="a5299-109">**Rozhodnutí**</span><span class="sxs-lookup"><span data-stu-id="a5299-109">**Decisions**</span></span>

- <span data-ttu-id="a5299-110">V jakém pořadí se mají názvy zobrazit pro záznamy strany typu **Osoba**?</span><span class="sxs-lookup"><span data-stu-id="a5299-110">What sequence should names be displayed in for party records of the **Person** type?</span></span> <span data-ttu-id="a5299-111">Například jedna sekvence je příjmení, druhé jméno a křestní jméno.</span><span class="sxs-lookup"><span data-stu-id="a5299-111">For example, one sequence is last name, middle name, first name.</span></span>
- <span data-ttu-id="a5299-112">Mají být záznamy strany odstraněny z adresáře při odstranění záznamu role?</span><span class="sxs-lookup"><span data-stu-id="a5299-112">Should party records be deleted from the address book when the role record is deleted?</span></span> <span data-ttu-id="a5299-113">Například pokud dojde k odstranění záznamu odběratele, má být záznam strany také odstraněn?</span><span class="sxs-lookup"><span data-stu-id="a5299-113">For example, if a customer record is deleted, should the party record also be deleted?</span></span>
- <span data-ttu-id="a5299-114">Když je vytvořen nový záznam, má být uživatelům zasláno oznámení, je-li nalezen duplicitní záznam v globálním adresáři?</span><span class="sxs-lookup"><span data-stu-id="a5299-114">When a new record is created, should users be notified if a duplicate record is found in the global address book?</span></span>
- <span data-ttu-id="a5299-115">Má být číslo systému univerzální číslování dat (DUNS) zahrnuto do informací pro záznam strany?</span><span class="sxs-lookup"><span data-stu-id="a5299-115">Should the Data Universal Numbering System (DUNS) number be included in a party record's information?</span></span>
- <span data-ttu-id="a5299-116">Pokud je číslo DUNS zahrnuto v záznamu strany, je třeba ověřit jedinečnost čísla?</span><span class="sxs-lookup"><span data-stu-id="a5299-116">If the DUNS number is included in a party record, should the uniqueness of the number be checked?</span></span>
- <span data-ttu-id="a5299-117">Chcete při vytvoření záznamu strany v globálním adresáři použít výchozí typ strany, osoby nebo organizace?</span><span class="sxs-lookup"><span data-stu-id="a5299-117">When a party record is created in the global address book, do you want a default party type, person, or organization?</span></span>
- <span data-ttu-id="a5299-118">Které role uživatele by měly mít přístup k soukromým adresám a kontaktním informacím v záznamech strany?</span><span class="sxs-lookup"><span data-stu-id="a5299-118">Which user roles should have access to the private addresses and contact information of party records?</span></span>

## <a name="additional-address-books"></a><span data-ttu-id="a5299-119">Další adresáře</span><span class="sxs-lookup"><span data-stu-id="a5299-119">Additional address books</span></span>

<span data-ttu-id="a5299-120">Po vytvoření globálního adresáře můžete vytvořit další adresáře podle potřeby, například samostatný adresář pro každou společnost v organizaci a pro každé odvětví obchodu.</span><span class="sxs-lookup"><span data-stu-id="a5299-120">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> <span data-ttu-id="a5299-121">Například společnost Fabrikam je mezinárodní organizace, která má více společností a více odvětví obchodu.</span><span class="sxs-lookup"><span data-stu-id="a5299-121">For example, Fabrikam is an international organization that has multiple companies and multiple lines of business.</span></span> <span data-ttu-id="a5299-122">Společnost Fabrikam plánuje vytvořit adresář pro každé odvětví obchodu.</span><span class="sxs-lookup"><span data-stu-id="a5299-122">Fabrikam plans to create an address book for each line of business.</span></span> <span data-ttu-id="a5299-123">Pro odvětví obchodu realizované ve více než jednom místě, například odvětví pneumatických nástrojů, společnost Fabrikam plánuje vytvořit adresář pro každé místo.</span><span class="sxs-lookup"><span data-stu-id="a5299-123">For lines of business that occur in more than one location, such as the pneumatic tools business, Fabrikam plans to create an address book for each location.</span></span> <span data-ttu-id="a5299-124">Chris, správce IT ve společnosti Fabrikam, vytvořil následující seznam adresářů, které jsou požadovány.</span><span class="sxs-lookup"><span data-stu-id="a5299-124">Chris, the IT manager at Fabrikam, has created the following list of address books that are required.</span></span> <span data-ttu-id="a5299-125">Tento seznam také popisuje záznamy strany, které musí každý adresáře obsahovat.</span><span class="sxs-lookup"><span data-stu-id="a5299-125">This list also describes the party records that each address book must include.</span></span>

- <span data-ttu-id="a5299-126">**Kontrakty veřejného sektoru (PubSC)** – Záznamy strany pro všechny strany, které jsou zahrnuty do kontraktů veřejného sektoru, které společnost Fabrikam získala.</span><span class="sxs-lookup"><span data-stu-id="a5299-126">**Public Sector Contracts (PubSC)** – Party records for all parties that are involved in the public sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="a5299-127">**Kontrakty soukromého sektoru (PriSC)** – Záznamy strany pro všechny strany, které jsou zahrnuty do kontraktů soukromého sektoru, které společnost Fabrikam získala.</span><span class="sxs-lookup"><span data-stu-id="a5299-127">**Private Sector Contracts (PriSC)** – Party records for all parties that are involved in the private sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="a5299-128">**Elektronické nástroje (ET)** – Strany záznamů pro všechny strany, která se účastní nákupu nebo prodeje elektronických nástrojů nebo jinak využívají elektronické nástroje, které poskytla nebo které nakupují pro společnost Fabrikam (Fabrikam – Japonsko).</span><span class="sxs-lookup"><span data-stu-id="a5299-128">**Electronic Tools (ET)** – Party records for all parties that are involved in the purchase or sale of electronic tools, or that otherwise interact with the electronic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="a5299-129">**Pneumatické nástroje (PTJPN)** – Strany záznamů pro všechny strany, která se účastní nákupu nebo prodeje pneumatických nástrojů nebo jinak využívají pneumatické nástroje, které poskytla nebo které nakupují pro společnost Fabrikam (Fabrikam – Japonsko).</span><span class="sxs-lookup"><span data-stu-id="a5299-129">**Pneumatic Tools (PTJPN)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="a5299-130">**Pneumatické nástroje (PTUSA)** – Strany záznamů pro všechny strany, která se účastní nákupu nebo prodeje pneumatických nástrojů nebo jinak využívají pneumatické nástroje, které poskytla nebo které nakupují pro společnost Fabrikam (Fabrikam – USA).</span><span class="sxs-lookup"><span data-stu-id="a5299-130">**Pneumatic Tools (PTUSA)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-US company.</span></span>

<span data-ttu-id="a5299-131">**Rozhodnutí:**</span><span class="sxs-lookup"><span data-stu-id="a5299-131">**Decision:**</span></span>

- <span data-ttu-id="a5299-132">Kolik dalších adresářů vytvoříte?</span><span class="sxs-lookup"><span data-stu-id="a5299-132">How many additional address books will you create?</span></span>
