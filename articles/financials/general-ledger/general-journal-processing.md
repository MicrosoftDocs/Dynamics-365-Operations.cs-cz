---
title: Zpracování hlavního deníku
description: Toto téma popisuje možnosti v aplikaci Microsoft Dynamics 365 for Finance and Operations, které usnadňují zpracování deníku hlavní knihy a které lze také použít k zaručení správnosti pořízených dat a dodržení interní kontroly.
author: ShylaThompson
manager: AnnBe
ms.date: 09/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e77aafafed5c972a6ad8c064107306d3ebde0b79
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550321"
---
# <a name="general-journal-processing"></a><span data-ttu-id="f426a-103">Zpracování hlavního deníku</span><span class="sxs-lookup"><span data-stu-id="f426a-103">General journal processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f426a-104">Toto téma popisuje možnosti v aplikaci Microsoft Dynamics 365 for Finance and Operations, které usnadňují zpracování deníku hlavní knihy a které lze také použít k zaručení správnosti pořízených dat a dodržení interní kontroly.</span><span class="sxs-lookup"><span data-stu-id="f426a-104">This topic describes capabilities in Microsoft Dynamics 365 for Finance and Operations that can help make general journal processing easier, and that can also help ensure that correct data is captured and internal control isn't compromised.</span></span>  

## <a name="journal-names"></a><span data-ttu-id="f426a-105">Názvy deníků</span><span class="sxs-lookup"><span data-stu-id="f426a-105">Journal names</span></span>

<span data-ttu-id="f426a-106">Jednou z nejdůležitějších oblastí nastavení jsou názvy deníků.</span><span class="sxs-lookup"><span data-stu-id="f426a-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="f426a-107">Je vhodné definovat konkrétní názvy pro každý účel, například mezipodnikové, úprava časového rozlišení a opravy chyb.</span><span class="sxs-lookup"><span data-stu-id="f426a-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="f426a-108">Můžete přizpůsobit každý název deníku pro rychlé a bezpečné zvýšení zadávání dat pro každý účel.</span><span class="sxs-lookup"><span data-stu-id="f426a-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="f426a-109">Na stránce **Názvy deníků** můžete nastavit následující prvky:</span><span class="sxs-lookup"><span data-stu-id="f426a-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="f426a-110">**Schválení workflowu** – Chcete-li zlepšit interní kontrolu, definujte workflowy deníků, které stanovují limity významnosti pro kroky kontroly a schvalování na základě kritérií, jako je například celková částka na straně Má dáti.</span><span class="sxs-lookup"><span data-stu-id="f426a-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="f426a-111">Nastavit workflowy pro hlavní deníky můžete na stránce **Workflowy hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="f426a-111">You set up workflows for the general journals on the **General ledger workflows** page.</span></span>
-   <span data-ttu-id="f426a-112">**Výchozí hodnoty** – vyberte výchozí hodnoty pro protiúčty, měnu a finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="f426a-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="f426a-113">**Kontrola deníku** – lze nastavit omezení pro společnost a typ účtu a rovněž pro hodnoty segmentů.</span><span class="sxs-lookup"><span data-stu-id="f426a-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="f426a-114">**Příklady**</span><span class="sxs-lookup"><span data-stu-id="f426a-114">**Examples**</span></span>

<span data-ttu-id="f426a-115">Název deníku lze použít pouze pro úpravy.</span><span class="sxs-lookup"><span data-stu-id="f426a-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="f426a-116">V tomto případě můžete určit, že pouze typ účtu **Hlavní kniha** je platný napříč všemi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="f426a-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> 

<span data-ttu-id="f426a-117">[![Typy účtů kontroly deníku](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="f426a-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="f426a-118">Název deníku lze použít pouze pro konkrétní segment nebo pro rozsah u hlavních účtů.</span><span class="sxs-lookup"><span data-stu-id="f426a-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> 

<span data-ttu-id="f426a-119">[![Segment kontroly deníku](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="f426a-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="f426a-120">Možnost **Automatické storno** je k dispozici v hlavních denících.</span><span class="sxs-lookup"><span data-stu-id="f426a-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="f426a-121">Například máte úpravu časového rozlišení, u které skutečný dokument dosud nebyl zpracován, jak je uvedeno v následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="f426a-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="f426a-122">[![Stornování hlavního deníku](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="f426a-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="f426a-123">Doplněk Microsoft Excel pro položku deníku poskytuje další úroveň automatizace a usnadňuje zadávání dat.</span><span class="sxs-lookup"><span data-stu-id="f426a-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="f426a-124">Akce **Otevřít řádky v aplikaci Excel** je k dispozici na stránkách **Hlavní deník** a **Doklad deníku**.</span><span class="sxs-lookup"><span data-stu-id="f426a-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="f426a-125">Na stránce **Periodické deníky** můžete nastavit opakující se deníky pro automatizaci zpracování deníků.</span><span class="sxs-lookup"><span data-stu-id="f426a-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="f426a-126">Šablony dokladů lze použít kdykoli.</span><span class="sxs-lookup"><span data-stu-id="f426a-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="f426a-127">Na stránce **Hlavní deníky** najdete akce **Uložit** a **Vybrat šablonu dokladu** na stránce **Doklad deníku** v oblasti **Funkce** pro řádky dokladu.</span><span class="sxs-lookup"><span data-stu-id="f426a-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="f426a-128">Související nastavení</span><span class="sxs-lookup"><span data-stu-id="f426a-128">Related setup</span></span>
<span data-ttu-id="f426a-129">Následující nastavení není specifické pro hlavní deníky, pomůže vám však zajistit správné a snadné zadávání dat.</span><span class="sxs-lookup"><span data-stu-id="f426a-129">The following setup isn't specific to general journals, but will help ensure that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="f426a-130">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="f426a-130">Main account</span></span>

<span data-ttu-id="f426a-131">Nastavení hlavního účtu poskytuje mnoho možností pro zpracování hlavního deníku:</span><span class="sxs-lookup"><span data-stu-id="f426a-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="f426a-132">**Požadavek DC/CR** – tuto možnost použijte, pokud je hlavní účet omezený na transakce typu Má dáti nebo Dal.</span><span class="sxs-lookup"><span data-stu-id="f426a-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="f426a-133">Nastavení se kontroluje při ověření nebo zaúčtování deníku.</span><span class="sxs-lookup"><span data-stu-id="f426a-133">The setup is verified when a journal is validated or posted.</span></span>

-   <span data-ttu-id="f426a-134">**Výchozí protiúčet**</span><span class="sxs-lookup"><span data-stu-id="f426a-134">**Default offset account**</span></span>
-   <span data-ttu-id="f426a-135">**Pozastaveno** – pozastaví hlavní účet pro zadávání dat napříč všemi společnostmi nebo pro určitou společnost či právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="f426a-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entity.</span></span>
-   <span data-ttu-id="f426a-136">**Nepovolit ruční zadávání** – zabrání uživatelům ručně zadat hodnotu pro účet v denících.</span><span class="sxs-lookup"><span data-stu-id="f426a-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="f426a-137">**Výchozí/ověření měny**</span><span class="sxs-lookup"><span data-stu-id="f426a-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="f426a-138">**Přepsání právnické osoby** – toto nastavení je specifické pro definovanou společnost / právnickou osobu:</span><span class="sxs-lookup"><span data-stu-id="f426a-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="f426a-139">**Výchozí/ověření DPH**</span><span class="sxs-lookup"><span data-stu-id="f426a-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="f426a-140">**Výchozí dimenze** – **Nestanoveno** nebo **Pevná hodnota**.</span><span class="sxs-lookup"><span data-stu-id="f426a-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="f426a-141">**Pevná hodnota** vám pomůže zajistit, aby všechna zaúčtování pro tento hlavní účet vždy použila jakoukoli hodnotu dimenze, která je nastavena jako **Pevná**.</span><span class="sxs-lookup"><span data-stu-id="f426a-141">**Fixed value** will help ensure that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="f426a-142">**Ověření zaúčtování**</span><span class="sxs-lookup"><span data-stu-id="f426a-142">**Posting validation**</span></span>
    -   <span data-ttu-id="f426a-143">**Ověření uživatele** – tato možnost určuje, kteří uživatelé mohou účtovat do hlavního účtu.</span><span class="sxs-lookup"><span data-stu-id="f426a-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="f426a-144">**Ověření typu zaúčtování** – tato možnost určuje, které typy zaúčtování jsou povolené pro hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="f426a-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="f426a-145">Účetní struktury a struktury rozšířených pravidel</span><span class="sxs-lookup"><span data-stu-id="f426a-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="f426a-146">Účetní struktury a struktury rozšířených pravidel jsou velice důležité pro zajištění toho, aby byla data potřebná pro finanční vykazování a sledování výkonu zachycována během zpracování hlavního deníku a jakékoli dokumentace.</span><span class="sxs-lookup"><span data-stu-id="f426a-146">Accounting structures and advanced rules structures are extremely important for ensuring that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="f426a-147">Účetní struktury a struktury rozšířených pravidel vám umožní přizpůsobit zadávání dat.</span><span class="sxs-lookup"><span data-stu-id="f426a-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="f426a-148">Můžete povolit zadávání dat pouze pro finanční dimenze, které jsou relevantní v každé situaci a také můžete vynutit požadavek, aby byla vždy zaznamenána povinná a přesná data.</span><span class="sxs-lookup"><span data-stu-id="f426a-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that required and accurate data always be captured.</span></span>

<span data-ttu-id="f426a-149">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="f426a-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="f426a-150">[Plánování: Účtová osnova](plan-chart-of-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="f426a-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="f426a-151">Vytvoření rozšířených pravidel pro deníky</span><span class="sxs-lookup"><span data-stu-id="f426a-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="f426a-152">Vytvoření položky deníku pomocí šablony</span><span class="sxs-lookup"><span data-stu-id="f426a-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="f426a-153">Vytváření a ověřování deníků</span><span class="sxs-lookup"><span data-stu-id="f426a-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="f426a-154">Zaúčtování periodických deníků</span><span class="sxs-lookup"><span data-stu-id="f426a-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="f426a-155">Zpracování deníku přidělení hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="f426a-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a><span data-ttu-id="f426a-156">Simulovat zaúčtování</span><span class="sxs-lookup"><span data-stu-id="f426a-156">Simulate posting</span></span>
<span data-ttu-id="f426a-157">Možnost **Simulovat zaúčtování** můžete pro většinu deníků nalézt v nabídce **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="f426a-157">You can find **Simulate posting** on the **Validate** menu for most journals.</span></span> <span data-ttu-id="f426a-158">Při ověřování deníku pomocí funkce **Ověřit** systém otestuje deník ohledně konkrétních chybových podmínek.</span><span class="sxs-lookup"><span data-stu-id="f426a-158">When you validate a journal using the **Validate** function, the system tests the journal for specific error conditions.</span></span> <span data-ttu-id="f426a-159">Pokud použijete funkci **Simulovat zaúčtování**, systém spustí všechny stejné procesy, které běží v průběhu zaúčtování bez skutečného zaúčtování deníku.</span><span class="sxs-lookup"><span data-stu-id="f426a-159">If you use the **Simulate posting** function, the system runs all of the same processes that are run during posting without actually posting the journal.</span></span> <span data-ttu-id="f426a-160">Můžete poté zkontrolovat zprávy o zaúčtování, které se zobrazí, opravit nalezené chyby a poté kliknout na nabídku **Zaúčtovat** pro zaúčtování deníku.</span><span class="sxs-lookup"><span data-stu-id="f426a-160">You can then review the posting messages that are displayed, fix any errors that you find, and then click the **Post** menu to post the journal.</span></span> 

<span data-ttu-id="f426a-161">Možnost **Simulovat zaúčtování** není k dispozici pro dávkové zpracování.</span><span class="sxs-lookup"><span data-stu-id="f426a-161">**Simulate posting** is not available for batch processing.</span></span> <span data-ttu-id="f426a-162">Je však k dispozici kód pro simulaci zaúčtování v dávce a vývojáři mohou rozšiřovat kód pro přidání této funkcionality.</span><span class="sxs-lookup"><span data-stu-id="f426a-162">However, there is code available to simulate posting in batch and developers can extend the code to add that functionality.</span></span>  
