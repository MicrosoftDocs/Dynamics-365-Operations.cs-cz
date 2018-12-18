---
title: "Domovská stránka Správa organizace"
description: "Toto téma odkazuje na zdroje, které vám pomůžou používat aplikaci Microsoft Dynamics 365 for Finance and Operations ve vaší organizaci."
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 0a693529b55b66eb940f8215a336d5c4ae0acedd
ms.contentlocale: cs-cz
ms.lasthandoff: 12/18/2018

---

# <a name="organization-administration-home-page"></a><span data-ttu-id="2d8b6-103">Domovská stránka Správa organizace</span><span class="sxs-lookup"><span data-stu-id="2d8b6-103">Organization administration home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d8b6-104">Toto téma odkazuje na obsah, který pomůže uživatelům Power users a správcům nakonfigurovat aplikaci Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-104">This topic points to content that will help power users and administrators configure Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="2d8b6-105">Tento obsah jim pomůže nakonfigurovat systém tak, aby fungoval pro vaši organizaci a obchod hladce a efektivně.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-105">This content will help them configure the system to work smoothly and effectively for your organization and business.</span></span>

<span data-ttu-id="2d8b6-106">Většina zde uvedeného obsahu se použije k funkcím v modulu **Správa organizace**.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-106">Much of the content listed here applies to features in the **Organizational administration** module.</span></span> <span data-ttu-id="2d8b6-107">Existuje však několik úlohy, jako je vytváření a používání šablony záznamu, které lze provést v kterémkoli modulu, aby vaše organizace mohla pracovat efektivněji.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-107">However, there are a couple of tasks, such as creating and using a record template, that can be performed in any module to help your organization run more efficiently.</span></span>

## <a name="number-sequences"></a><span data-ttu-id="2d8b6-108">Číselné řady</span><span class="sxs-lookup"><span data-stu-id="2d8b6-108">Number sequences</span></span>

<span data-ttu-id="2d8b6-109">Číselné řady v aplikaci slouží ke generování čitelných, jedinečných identifikátorů pro hlavní datové záznamy a záznamy transakcí, které požadují identifikátory.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-109">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="2d8b6-110">Hlavní záznam dat nebo záznam transakce, která vyžaduje identifikátor, je označován jako *odkaz*.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-110">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span> <span data-ttu-id="2d8b6-111">Než bude možné vytvořit nové záznamy pro odkaz, musíte nastavit číselné řady a spojit je s odkazem.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-111">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span>

- [<span data-ttu-id="2d8b6-112">Přehled číselných řad</span><span class="sxs-lookup"><span data-stu-id="2d8b6-112">Number sequence overview</span></span>](number-sequence-overview.md)
- <span data-ttu-id="2d8b6-113">[Nastavení číselných řad pomocí průvodce](tasks/set-up-number-sequences-wizard.md) (Průvodce záznamem úloh)</span><span class="sxs-lookup"><span data-stu-id="2d8b6-113">[Set up number sequences by using a wizard](tasks/set-up-number-sequences-wizard.md) (Task guide)</span></span>
- <span data-ttu-id="2d8b6-114">[Nastavení jednotlivých číselných řad](tasks/set-up-number-sequences-individual-basis.md) (Průvodce záznamem úloh)</span><span class="sxs-lookup"><span data-stu-id="2d8b6-114">[Set up number sequences on an individual basis](tasks/set-up-number-sequences-individual-basis.md) (Task guide)</span></span>

## <a name="organizations"></a><span data-ttu-id="2d8b6-115">Organizace</span><span class="sxs-lookup"><span data-stu-id="2d8b6-115">Organizations</span></span>

<span data-ttu-id="2d8b6-116">Organizace představuje skupinu lidí, kteří spolupracují na provádění obchodního procesu nebo dosažení cíle.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-116">An organization is a group of people who are working together to carry out a business process or achieve a goal.</span></span> <span data-ttu-id="2d8b6-117">Organizační hierarchie představuje vztahy mezi organizacemi, které tvoří váš podnik.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-117">Organizational hierarchies represent the relationships between the organizations that make up your business.</span></span>

<span data-ttu-id="2d8b6-118">Před nastavením organizací a organizačních hierarchií v Microsoft Dynamics 365 for Finance and Operations se ujistěte, že máte plán, jak bude vaše společnost modelována.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-118">Before you set up organizations and organization hierarchies in Finance and Operations, make sure that you plan how your business will be modeled.</span></span> <span data-ttu-id="2d8b6-119">Organizační model má podstatný vliv na implementaci aplikace Finance and Operations a obchodní procesy.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-119">The organization model has a significant effect on the implementation of Finance and Operations and on business processes.</span></span>

- [<span data-ttu-id="2d8b6-120">Organizace a organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="2d8b6-120">Organizations and organizational hierarchies</span></span>](organizations-organizational-hierarchies.md)
- [<span data-ttu-id="2d8b6-121">Plánování organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="2d8b6-121">Plan your organizational hierarchy</span></span>](plan-organizational-hierarchy.md)
- <span data-ttu-id="2d8b6-122">[Vytvoření organizační hierarchie](tasks/create-organization-hierarchy.md) (Průvodce záznamem úloh)</span><span class="sxs-lookup"><span data-stu-id="2d8b6-122">[Create an organization hierarchy](tasks/create-organization-hierarchy.md) (Task guide)</span></span>
- <span data-ttu-id="2d8b6-123">[Vytvoření právnické osoby](tasks/create-legal-entity.md) (Průvodce záznamem úloh)</span><span class="sxs-lookup"><span data-stu-id="2d8b6-123">[Create a legal entity](tasks/create-legal-entity.md) (Task guide)</span></span>
- <span data-ttu-id="2d8b6-124">[Vytvoření provozní jednotky](tasks/create-operating-unit.md) (Průvodce záznamem úloh)</span><span class="sxs-lookup"><span data-stu-id="2d8b6-124">[Create an operating unit](tasks/create-operating-unit.md) (Task guide)</span></span>

## <a name="address-books"></a><span data-ttu-id="2d8b6-125">Adresáře</span><span class="sxs-lookup"><span data-stu-id="2d8b6-125">Address books</span></span>

<span data-ttu-id="2d8b6-126">Globální adresář je centralizovaným úložištěm pro hlavní data, která musí být uložena pro všechny interní a externí osoby a organizace, se kterými společnost přichází do styku.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-126">The global address book is a centralized repository for master data that must be stored for all internal and external persons and organizations that the company interacts with.</span></span> <span data-ttu-id="2d8b6-127">Data přidružená k záznamům strany zahrnují název strany, adresu a kontaktní informace.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-127">The data that is associated with party records includes the party's name, address, and contact information.</span></span>

<span data-ttu-id="2d8b6-128">Po vytvoření globálního adresáře můžete vytvořit další adresáře podle potřeby, například samostatný adresář pro každou společnost v organizaci a pro každé odvětví obchodu.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-128">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span>

- [<span data-ttu-id="2d8b6-129">Globální adresář</span><span class="sxs-lookup"><span data-stu-id="2d8b6-129">Global address book</span></span>](overview-global-address-book.md)
- [<span data-ttu-id="2d8b6-130">Plán konfigurace globálního adresáře a dalších adresářů</span><span class="sxs-lookup"><span data-stu-id="2d8b6-130">Plan how to configure the global address book and additional address books</span></span>](plan-configuration-global-address-book-additional-address-books.md)
- [<span data-ttu-id="2d8b6-131">Konfigurace globálního adresáře</span><span class="sxs-lookup"><span data-stu-id="2d8b6-131">Configure the global address book</span></span>](tasks/configure-global-address-book.md)
- [<span data-ttu-id="2d8b6-132">Často kladené dotazy týkající se adresářů</span><span class="sxs-lookup"><span data-stu-id="2d8b6-132">Address books FAQ</span></span>](qa-address-books.md)

## <a name="workflow"></a><span data-ttu-id="2d8b6-133">Workflow</span><span class="sxs-lookup"><span data-stu-id="2d8b6-133">Workflow</span></span>

<span data-ttu-id="2d8b6-134">Workflow je systém, který byl nainstalován společně s aplikací Finance and Operations a jehož pomocí lze vytvářet individuální workflowy nebo obchodní procesy.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-134">Workflow is a system that is installed with Finance and Operations that you can use to create individual workflows, or business processes.</span></span> <span data-ttu-id="2d8b6-135">Když vytváříte workflow, určete tok dokumentu nebo jeho procházení systémem pomocí zobrazení toho, kdo musí splnit úkol, provádět rozhodování nebo schválení dokumentu.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-135">When you create a workflow, you specify how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span>

- [<span data-ttu-id="2d8b6-136">Přehled workflowu</span><span class="sxs-lookup"><span data-stu-id="2d8b6-136">Workflow overview</span></span>](overview-workflow-system.md)
- [<span data-ttu-id="2d8b6-137">Prvky workflowu</span><span class="sxs-lookup"><span data-stu-id="2d8b6-137">Workflow elements</span></span>](workflow-elements.md)
- [<span data-ttu-id="2d8b6-138">Akce workflowu</span><span class="sxs-lookup"><span data-stu-id="2d8b6-138">Workflow actions</span></span>](workflow-actions.md)
- [<span data-ttu-id="2d8b6-139">Vytvoření workflow</span><span class="sxs-lookup"><span data-stu-id="2d8b6-139">Create a workflow</span></span>](create-workflow.md)

## <a name="electronic-signatures"></a><span data-ttu-id="2d8b6-140">Elektronické podpisy</span><span class="sxs-lookup"><span data-stu-id="2d8b6-140">Electronic signatures</span></span>

<span data-ttu-id="2d8b6-141">Elektronický podpis potvrzuje identitu osoby, která spouští nebo schvaluje určitý proces využívající výpočetní techniku.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-141">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="2d8b6-142">V některých průmyslových odvětvích má elektronický podpis stejnou právní hodnotu jako ruční podpis.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-142">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span> <span data-ttu-id="2d8b6-143">Elektronické podpisy jsou vyžadovány předpisy v několika průmyslových odvětvích, například ve farmaceutickém, potravinářském, leteckém a zbrojním průmyslu.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-143">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span>

<span data-ttu-id="2d8b6-144">V aplikaci Finance and Operations můžete používat elektronické podpisy pro důležité obchodní procesy.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-144">In Finance and Operations, you can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="2d8b6-145">Některé procesy obsahují vestavěné prvky pro práci s elektronickými podpisy.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-145">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="2d8b6-146">Kromě toho můžete vytvářet vlastní požadavky na podpisy, připojené k libovolné databázové tabulce a poli.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-146">You can also create custom signature requirements for any database table and field.</span></span>

- [<span data-ttu-id="2d8b6-147">Přehled elektronických podpisů</span><span class="sxs-lookup"><span data-stu-id="2d8b6-147">Electronic signature overview</span></span>](electronic-signature-overview.md)
- <span data-ttu-id="2d8b6-148">[Nastavení parametrů elektronického podpisu](tasks/set-up-electronic-signatures.md) (Průvodce záznamem úloh)</span><span class="sxs-lookup"><span data-stu-id="2d8b6-148">[Set up electronic signatures](tasks/set-up-electronic-signatures.md) (Task guide)</span></span>

## <a name="case-management"></a><span data-ttu-id="2d8b6-149">Správa případů</span><span class="sxs-lookup"><span data-stu-id="2d8b6-149">Case management</span></span>

<span data-ttu-id="2d8b6-150">Plánováním, sledováním a analýzou případů můžete vytvořit efektivní řešení, která lze použít pro podobné případy.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-150">By planning, tracking, and analyzing cases, you can develop efficient resolutions that can be used for similar issues.</span></span> <span data-ttu-id="2d8b6-151">Například když zástupci servisu zákazníka nebo pracovníci lidských zdrojů vytváří případy, mohou najít informace v článcích znalostní databáze o tom, jak pracovat nebo vyřešit případy efektivněji.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-151">For example, when customer service representatives or Human Resources generalists create cases, they can find information in knowledge articles to help them work with or resolve a case more efficiently.</span></span>

- [<span data-ttu-id="2d8b6-152">Přehled správy příkazů</span><span class="sxs-lookup"><span data-stu-id="2d8b6-152">Case management overview</span></span>](cases.md)
- [<span data-ttu-id="2d8b6-153">Konfigurace bezpečnosti případu, procesů a kategorií</span><span class="sxs-lookup"><span data-stu-id="2d8b6-153">Configure case security, processes, and categories</span></span>](plan-case-management.md)

## <a name="record-templates"></a><span data-ttu-id="2d8b6-154">Šablony záznamu</span><span class="sxs-lookup"><span data-stu-id="2d8b6-154">Record templates</span></span>

<span data-ttu-id="2d8b6-155">Šablony záznamu vám mohou pomoci vytvořit záznamy rychleji.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-155">Record templates can help you to create records more quickly.</span></span> <span data-ttu-id="2d8b6-156">Můžete vytvořit šablonu záznamu tak, že hodnoty pole, které jsou často používány, nemusí být zadány explicitně pro každý nový záznam.</span><span class="sxs-lookup"><span data-stu-id="2d8b6-156">You can create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span>

- [<span data-ttu-id="2d8b6-157">Šablony záznamu</span><span class="sxs-lookup"><span data-stu-id="2d8b6-157">Record templates</span></span>](record-templates.md)
- <span data-ttu-id="2d8b6-158">[Vytvoření šablony záznamu pro usnadnění zadávání dat](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (Průvodce záznamem úloh)</span><span class="sxs-lookup"><span data-stu-id="2d8b6-158">[Create a record template to facilitate data entry](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (Task guide)</span></span>
- <span data-ttu-id="2d8b6-159">[Vytvoření nového záznamu s použitím šablony záznamu](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (Průvodce záznamem úloh)</span><span class="sxs-lookup"><span data-stu-id="2d8b6-159">[Use a record template to create a new record](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (Task guide)</span></span>

## <a name="general-organization-administration"></a><span data-ttu-id="2d8b6-160">Obecná správa organizace</span><span class="sxs-lookup"><span data-stu-id="2d8b6-160">General organization administration</span></span>

- <span data-ttu-id="2d8b6-161">[Změna nápisu nebo loga](../get-started/tasks/change-banner-or-logo.md) (Průvodce záznamem úloh)</span><span class="sxs-lookup"><span data-stu-id="2d8b6-161">[Change the banner or logo](../get-started/tasks/change-banner-or-logo.md) (Task guide)</span></span>
- [<span data-ttu-id="2d8b6-162">Konfigurace správy dokumentů</span><span class="sxs-lookup"><span data-stu-id="2d8b6-162">Configure document management</span></span>](configure-document-management.md)
- [<span data-ttu-id="2d8b6-163">Konfigurace a odeslání e-mailu</span><span class="sxs-lookup"><span data-stu-id="2d8b6-163">Configure and send email</span></span>](configure-email.md)
- [<span data-ttu-id="2d8b6-164">Údaje data a času a časové pásmo</span><span class="sxs-lookup"><span data-stu-id="2d8b6-164">Date/time data and time zones</span></span>](date-time-zones.md)

