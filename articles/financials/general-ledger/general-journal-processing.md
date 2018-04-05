---
title: "Zpracování hlavního deníku"
description: "Tento článek popisuje možnosti v aplikaci Microsoft Dynamics 365 for Finance and Operations, které usnadňují zpracování deníku hlavní knihy a které lze také použít k zaručení správnosti pořízených dat a dodržení interní kontroly."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: eb46613f805999753c2ab73ffb91a6fdae04c68e
ms.contentlocale: cs-cz
ms.lasthandoff: 03/26/2018

---

# <a name="general-journal-processing"></a><span data-ttu-id="44de3-103">Zpracování hlavního deníku</span><span class="sxs-lookup"><span data-stu-id="44de3-103">General journal processing</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="44de3-104">Tento článek popisuje možnosti v aplikaci Microsoft Dynamics 365 for Finance and Operations, které usnadňují zpracování deníku hlavní knihy a které lze také použít k zaručení správnosti pořízených dat a dodržení interní kontroly.</span><span class="sxs-lookup"><span data-stu-id="44de3-104">This articles describes capabilities in Microsoft Dynamics 365 for Finance and Operations that can help make general journal processing easier, and that can also help guarantee that correct data is captured and internal control isn't compromised.</span></span>  

<span data-ttu-id="44de3-105">Názvy deníků</span><span class="sxs-lookup"><span data-stu-id="44de3-105">Journal names</span></span>

<span data-ttu-id="44de3-106">Jednou z nejdůležitějších oblastí nastavení jsou názvy deníků.</span><span class="sxs-lookup"><span data-stu-id="44de3-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="44de3-107">Je vhodné definovat konkrétní názvy pro každý účel, například mezipodnikové, úprava časového rozlišení a opravy chyb.</span><span class="sxs-lookup"><span data-stu-id="44de3-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="44de3-108">Můžete přizpůsobit každý název deníku pro rychlé a bezpečné zvýšení zadávání dat pro každý účel.</span><span class="sxs-lookup"><span data-stu-id="44de3-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="44de3-109">Na stránce **Názvy deníků** můžete nastavit následující prvky:</span><span class="sxs-lookup"><span data-stu-id="44de3-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="44de3-110">**Schválení workflowu** – Chcete-li zlepšit interní kontrolu, definujte workflowy deníků, které stanovují limity významnosti pro kroky kontroly a schvalování na základě kritérií, jako je například celková částka na straně Má dáti.</span><span class="sxs-lookup"><span data-stu-id="44de3-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="44de3-111">Workflowy pro hlavní deníky můžete nastavit na stránce **Workflowy hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="44de3-111">You set up workflows for the general journals on the** General ledger workflows** page.</span></span>
-   <span data-ttu-id="44de3-112">**Výchozí hodnoty** – vyberte výchozí hodnoty pro protiúčty, měnu a finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="44de3-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="44de3-113">**Kontrola deníku** – lze nastavit omezení pro společnost a typ účtu a rovněž pro hodnoty segmentů.</span><span class="sxs-lookup"><span data-stu-id="44de3-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="44de3-114">**Příklady**</span><span class="sxs-lookup"><span data-stu-id="44de3-114">**Examples**</span></span>

<span data-ttu-id="44de3-115">Název deníku lze použít pouze pro úpravy.</span><span class="sxs-lookup"><span data-stu-id="44de3-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="44de3-116">V tomto případě můžete určit, že pouze typ účtu **Hlavní kniha** je platný napříč všemi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="44de3-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> <span data-ttu-id="44de3-117">[![Typy účtů kontroly deníku](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="44de3-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="44de3-118">Název deníku lze použít pouze pro konkrétní segment nebo pro rozsah u hlavních účtů.</span><span class="sxs-lookup"><span data-stu-id="44de3-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> <span data-ttu-id="44de3-119">[![Segment kontroly deníku](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="44de3-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="44de3-120">Možnost **Automatické storno** je k dispozici v hlavních denících.</span><span class="sxs-lookup"><span data-stu-id="44de3-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="44de3-121">Například máte úpravu časového rozlišení, u které skutečný dokument dosud nebyl zpracován, jak je uvedeno v následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="44de3-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="44de3-122">[![Stornování hlavního deníku](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="44de3-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="44de3-123">Doplněk Microsoft Excel pro položku deníku poskytuje další úroveň automatizace a usnadňuje zadávání dat.</span><span class="sxs-lookup"><span data-stu-id="44de3-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="44de3-124">Akce **Otevřít řádky v aplikaci Excel** je k dispozici na stránkách **Hlavní deník** a **Doklad deníku**.</span><span class="sxs-lookup"><span data-stu-id="44de3-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="44de3-125">Na stránce **Periodické deníky** můžete nastavit opakující se deníky pro automatizaci zpracování deníků.</span><span class="sxs-lookup"><span data-stu-id="44de3-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="44de3-126">Šablony dokladů lze použít kdykoli.</span><span class="sxs-lookup"><span data-stu-id="44de3-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="44de3-127">Na stránce **Hlavní deníky** najdete akce **Uložit** a **Vybrat šablonu dokladu** na stránce **Doklad deníku** v oblasti **Funkce** pro řádky dokladu.</span><span class="sxs-lookup"><span data-stu-id="44de3-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="44de3-128">Související nastavení</span><span class="sxs-lookup"><span data-stu-id="44de3-128">Related setup</span></span>
<span data-ttu-id="44de3-129">Následující nastavení není specifické pro hlavní deníky, pomůže vám však zajistit správné a snadné zadávání dat.</span><span class="sxs-lookup"><span data-stu-id="44de3-129">The following setup isn't specific to general journals, but will help guarantee that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="44de3-130">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="44de3-130">Main account</span></span>

<span data-ttu-id="44de3-131">Nastavení hlavního účtu poskytuje mnoho možností pro zpracování hlavního deníku:</span><span class="sxs-lookup"><span data-stu-id="44de3-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="44de3-132">**Požadavek DC/CR** – tuto možnost použijte, pokud je hlavní účet omezený na transakce typu Má dáti nebo Dal.</span><span class="sxs-lookup"><span data-stu-id="44de3-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="44de3-133">Nastavení se kontroluje při ověření nebo zaúčtování deníku.</span><span class="sxs-lookup"><span data-stu-id="44de3-133">The setup is verified when a journal is validated or posted.</span></span>
-   <span data-ttu-id="44de3-134">**Výchozí protiúčet**</span><span class="sxs-lookup"><span data-stu-id="44de3-134">**Default offset account**</span></span>
-   <span data-ttu-id="44de3-135">**Pozastaveno** – pozastaví hlavní účet pro zadávání dat napříč všemi společnostmi nebo pro určité společnosti či právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="44de3-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entities.</span></span>
-   <span data-ttu-id="44de3-136">**Nepovolit ruční zadávání** – zabrání uživatelům ručně zadat hodnotu pro účet v denících.</span><span class="sxs-lookup"><span data-stu-id="44de3-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="44de3-137">**Výchozí/ověření měny**</span><span class="sxs-lookup"><span data-stu-id="44de3-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="44de3-138">**Přepsání právnické osoby** – toto nastavení je specifické pro definovanou společnost / právnickou osobu:</span><span class="sxs-lookup"><span data-stu-id="44de3-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="44de3-139">**Výchozí/ověření DPH**</span><span class="sxs-lookup"><span data-stu-id="44de3-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="44de3-140">**Výchozí dimenze** – **Nestanoveno** nebo **Pevná hodnota**.</span><span class="sxs-lookup"><span data-stu-id="44de3-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="44de3-141">**Pevná hodnota** vám pomůže zajistit, aby všechna zaúčtování pro tento hlavní účet vždy použila jakoukoli hodnotu dimenze, která je nastavena jako **Pevná**.</span><span class="sxs-lookup"><span data-stu-id="44de3-141">**Fixed value** will help guarantee that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="44de3-142">**Ověření zaúčtování**</span><span class="sxs-lookup"><span data-stu-id="44de3-142">**Posting validation**</span></span>
    -   <span data-ttu-id="44de3-143">**Ověření uživatele** – tato možnost určuje, kteří uživatelé mohou účtovat do hlavního účtu.</span><span class="sxs-lookup"><span data-stu-id="44de3-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="44de3-144">**Ověření typu zaúčtování** – tato možnost určuje, které typy zaúčtování jsou povolené pro hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="44de3-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="44de3-145">Účetní struktury a struktury rozšířených pravidel</span><span class="sxs-lookup"><span data-stu-id="44de3-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="44de3-146">Účetní struktury a struktury rozšířených pravidel jsou velice důležité pro zajištění toho, aby byla data potřebná pro finanční vykazování a sledování výkonu zachycována během zpracování hlavního deníku a jakékoli dokumentace.</span><span class="sxs-lookup"><span data-stu-id="44de3-146">Accounting structures and advanced rules structures are extremely important for guaranteeing that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="44de3-147">Účetní struktury a struktury rozšířených pravidel vám umožní přizpůsobit zadávání dat.</span><span class="sxs-lookup"><span data-stu-id="44de3-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="44de3-148">Můžete povolit zadávání dat pouze pro finanční dimenze, které jsou relevantní v každé situaci a také můžete vynutit požadavek, aby byla vždy zaznamenána povinná a správná data.</span><span class="sxs-lookup"><span data-stu-id="44de3-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that mandatory and correct data always be captured.</span></span>

<span data-ttu-id="44de3-149">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="44de3-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="44de3-150">[Plánování: Účtová osnova](plan-chart-of-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="44de3-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="44de3-151">Vytvoření rozšířených pravidel pro deníky</span><span class="sxs-lookup"><span data-stu-id="44de3-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="44de3-152">Vytvoření položky deníku pomocí šablony</span><span class="sxs-lookup"><span data-stu-id="44de3-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="44de3-153">Vytváření a ověřování deníků</span><span class="sxs-lookup"><span data-stu-id="44de3-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="44de3-154">Účtování periodických deníků</span><span class="sxs-lookup"><span data-stu-id="44de3-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="44de3-155">Zpracování deníku přidělení hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="44de3-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)



