---
title: Přehled nebezpečných materiálů
description: Toto téma poskytuje přehled funkcí, které souvisejí s manipulací a dokumentací nebezpečných materiálů během správy informací o produktu a správy skladu.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 227111f4703d9dc381270382dcb796874d7de937
ms.sourcegitcommit: c009ec75f53872272f11c92a1ce81a391e3845a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/18/2020
ms.locfileid: "3699593"
---
# <a name="hazardous-materials-overview"></a><span data-ttu-id="47ea6-103">Přehled nebezpečných materiálů</span><span class="sxs-lookup"><span data-stu-id="47ea6-103">Hazardous materials overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47ea6-104">Aby organizace, které přepravují materiály klasifikované jako nebezpečné zboží, dodržovaly přepravní předpisy, musí ke svým zásilkám přiložit dodatečné doklady.</span><span class="sxs-lookup"><span data-stu-id="47ea6-104">To remain compliant with shipping and transport regulations, organizations that ship materials that are classified as dangerous goods must include additional paperwork with their shipments.</span></span> <span data-ttu-id="47ea6-105">Funkce nebezpečných materiálů umožňuje zákazníkům ukládat informace související s uvolněnými položkami.</span><span class="sxs-lookup"><span data-stu-id="47ea6-105">The hazardous materials feature lets customers store information that is related to released items.</span></span> <span data-ttu-id="47ea6-106">Tyto informace lze poté použít k přípravě dokumentace o dodávce.</span><span class="sxs-lookup"><span data-stu-id="47ea6-106">This information can then be used to help prepare shipping documentation.</span></span> <span data-ttu-id="47ea6-107">Organizace, která přepravuje nebezpečné zboží, musí mít vlastní procesy a postupy pro správu přepravního procesu.</span><span class="sxs-lookup"><span data-stu-id="47ea6-107">An organization that ships dangerous goods must have its own processes and procedures for managing the shipping process.</span></span> <span data-ttu-id="47ea6-108">Microsoft Dynamics 365 Supply Chain Management je jen nástroj, který může pomoci vygenerovat požadované dokumenty.</span><span class="sxs-lookup"><span data-stu-id="47ea6-108">Microsoft Dynamics 365 Supply Chain Management is just a tool that can help generate the required documents.</span></span>

<span data-ttu-id="47ea6-109">Následující diagram znázorňuje kroky potřebné k nastavení a používání funkce nebezpečných materiálů.</span><span class="sxs-lookup"><span data-stu-id="47ea6-109">The following diagram illustrates the steps needed to set up and use the hazardous materials feature.</span></span>

<span data-ttu-id="47ea6-110">![Nastavení a použití funkce nebezpečných materiálů](media/hazmat-overview.png "Nastavení a použití funkce nebezpečných materiálů")</span><span class="sxs-lookup"><span data-stu-id="47ea6-110">![Setup and use of the hazardous materials feature](media/hazmat-overview.png "Setup and use of the hazardous materials feature")</span></span>

<span data-ttu-id="47ea6-111">Funkce nebezpečných materiálů je nastavena ve správě informací o produktu a poskytuje dokumenty, které lze vytisknout prostřednictvím správy skladu.</span><span class="sxs-lookup"><span data-stu-id="47ea6-111">The hazardous materials feature is set up in Product information management and provides documents that can be printed through Warehouse management.</span></span> <span data-ttu-id="47ea6-112">Obecně řečeno, tyto oblasti jsou dvě hlavní oblasti, kde budete kontrolovat, nastavovat a používat tuto funkci:</span><span class="sxs-lookup"><span data-stu-id="47ea6-112">Therefore, broadly speaking, those areas are the two main areas where you will review, set up, and use this feature's functionality:</span></span>

- <span data-ttu-id="47ea6-113">**Správa informací o produktech** – Nastavení kódů, které budou použity na uvolněný produkt.</span><span class="sxs-lookup"><span data-stu-id="47ea6-113">**Product information management** – Set up the codes that will be applied to a released product.</span></span>
- <span data-ttu-id="47ea6-114">**Řízení skladu** – Práce s dodatečnými dodacími doklady, které budou pro zásilky vytištěny.</span><span class="sxs-lookup"><span data-stu-id="47ea6-114">**Warehouse management** – Work with additional shipping documents that will be printed for shipments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="47ea6-115">Funkce nebezpečných materiálů v modulu Supply Chain Management poskytují kolekci užitečných polí s informacemi o produktu a souvisejících funkcích, které vám mohou pomoci zaznamenat a odkazovat na informace související s vašimi nebezpečnými produkty.</span><span class="sxs-lookup"><span data-stu-id="47ea6-115">The hazardous materials features in Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="47ea6-116">Tyto funkce vám také mohou pomoci navrhnout a vytisknout dodací doklady, které obsahují některé totožné informace o všech nebezpečných materiálech, které přepravujete.</span><span class="sxs-lookup"><span data-stu-id="47ea6-116">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="47ea6-117">Systém však automaticky nezajistí vaši plnou kompatibilitu se všemi platnými regulacemi vaší země nebo oblasti.</span><span class="sxs-lookup"><span data-stu-id="47ea6-117">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="47ea6-118">Ačkoli jsou tyto nástroje určeny k tomu, aby vám pomohly dodržovat společné předpisy, nejsou samy o sobě dostatečné ani zaručené.</span><span class="sxs-lookup"><span data-stu-id="47ea6-118">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="47ea6-119">Vaše organizace je odpovědná za to, že si je vědoma všech příslušných předpisů a že podniká všechny kroky nezbytné k jejich dodržování.</span><span class="sxs-lookup"><span data-stu-id="47ea6-119">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="47ea6-120">Řízení informací o produktech</span><span class="sxs-lookup"><span data-stu-id="47ea6-120">Product information management</span></span>

<span data-ttu-id="47ea6-121">Správa informací o produktu poskytuje řadu nastavení tabulek, kde můžete zadat referenční informace pro různé seznamy nebezpečného zboží pro silniční, leteckou a námořní dopravu.</span><span class="sxs-lookup"><span data-stu-id="47ea6-121">Product information management provides a range of setup tables where you can enter reference information for the various dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="47ea6-122">Při vývoji této funkce se počítalo s následujícími společnými předpisy:</span><span class="sxs-lookup"><span data-stu-id="47ea6-122">The following common regulations were referenced when this functionality was developed:</span></span>

- <span data-ttu-id="47ea6-123">**ADR** – Nařízení vztahující se k mezinárodní přepravě nebezpečného zboží po silnici</span><span class="sxs-lookup"><span data-stu-id="47ea6-123">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="47ea6-124">**CFR 49** - Nařízení v USA pro přepravu nebezpečného zboží</span><span class="sxs-lookup"><span data-stu-id="47ea6-124">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="47ea6-125">**IMDG** – Kód mezinárodní námořní přepravy nebezpečného zboží</span><span class="sxs-lookup"><span data-stu-id="47ea6-125">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="47ea6-126">**IATA** – Nařízení mezinárodního sdružení letecké dopravy (IATA) o nebezpečném zboží</span><span class="sxs-lookup"><span data-stu-id="47ea6-126">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="47ea6-127">Každá sada předpisů poskytuje standardizované seznamy nebezpečných zboží a referenční kódy.</span><span class="sxs-lookup"><span data-stu-id="47ea6-127">Each set of regulations provides standardized lists of dangerous goods and reference codes.</span></span> <span data-ttu-id="47ea6-128">Proto Supply Chain Management poskytuje referenční tabulku pro společné kódy v těchto seznamech.</span><span class="sxs-lookup"><span data-stu-id="47ea6-128">Therefore, Supply Chain Management provides a reference table for the common codes on those lists.</span></span> <span data-ttu-id="47ea6-129">Každý seznam obsahuje také některé jedinečné kódy, které můžete definovat.</span><span class="sxs-lookup"><span data-stu-id="47ea6-129">Each list also has some unique codes that you can define.</span></span>

<span data-ttu-id="47ea6-130">Další informace, jak nastavit předpisy a hodnoty pro nebezpečné materiály a jak přiřadit hodnoty příslušným produktům, najdete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="47ea6-130">For more information about how to set up regulations and values for hazardous materials, and how to assign the values to relevant products, see the following topics:</span></span>

- [<span data-ttu-id="47ea6-131">Příprava nebezpečných materiálů</span><span class="sxs-lookup"><span data-stu-id="47ea6-131">Set up hazardous materials</span></span>](hazmat-setup.md)
- [<span data-ttu-id="47ea6-132">Nebezpečné materiály ve výrobcích, objednávkách, dodávkách a nákladech</span><span class="sxs-lookup"><span data-stu-id="47ea6-132">Hazardous materials in products, orders, shipments, and loads</span></span>](hazmat-items.md)

## <a name="warehouse-management"></a><span data-ttu-id="47ea6-133">Řízení skladu</span><span class="sxs-lookup"><span data-stu-id="47ea6-133">Warehouse management</span></span>

<span data-ttu-id="47ea6-134">Když připravujete dodávku v Řízení skladu, můžete vytisknout několik nových sestav, které používají informace, které jste nastavili v Řízení informací o produktech.</span><span class="sxs-lookup"><span data-stu-id="47ea6-134">When you prepare a shipment in Warehouse management, you will be able to print several new reports that use the information that you set up in Product information management.</span></span> <span data-ttu-id="47ea6-135">Další informace o dostupných sestavách a jejich použití najdete v části [Nebezpečné materiály – dotazy a sestavy](hazmat-reports.md).</span><span class="sxs-lookup"><span data-stu-id="47ea6-135">For more information about the available reports and how to use them, see [Hazardous materials inquiries and reports](hazmat-reports.md).</span></span>
