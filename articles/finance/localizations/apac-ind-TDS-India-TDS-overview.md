---
title: Přehled indické daně odečtené u zdroje (TDS)
description: Toto téma poskytuje podrobné informace o indické dani odečtené u zdroje (TDS). Dokumentace TDS pokrývá funkčnost této funkce.
author: kailiang
ms.date: 03/19/2021
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
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 28ee843036e11bd37b97a065ce53d2eb860c79d9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023101"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a><span data-ttu-id="ea3c7-104">Přehled indické daně odečtené u zdroje (TDS)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-104">Indian Tax Deducted at Source (TDS) overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea3c7-105">Toto téma poskytuje podrobné informace o indické dani odečtené u zdroje (TDS).</span><span class="sxs-lookup"><span data-stu-id="ea3c7-105">This topic provides detailed information about Indian Tax Deducted at Source (TDS).</span></span>

<span data-ttu-id="ea3c7-106">Dokumentace TDS pokrývá funkčnost této funkce.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-106">The TDS documentation covers the functionality of this capability.</span></span> <span data-ttu-id="ea3c7-107">Vysvětluje také, jak provést základní nastavení pro TDS, vypočítat TDS u transakcí, provést proces vypořádání TDS, zaznamenat čísla certifikátů TDS a generovat dotazy TDS, příkazy TDS a certifikáty TDS.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-107">It also explains how to do the basic setup for TDS, calculate TDS on transactions, complete the TDS settlement process, record TDS certificate numbers, and generate TDS inquiries, TDS statements, and TDS certificates.</span></span> <span data-ttu-id="ea3c7-108">Dokumentace obsahuje následující témata:</span><span class="sxs-lookup"><span data-stu-id="ea3c7-108">The documentation includes the following topics:</span></span>

- [<span data-ttu-id="ea3c7-109">Základní nastavení pro TDS</span><span class="sxs-lookup"><span data-stu-id="ea3c7-109">Basic setup for TDS</span></span>](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [<span data-ttu-id="ea3c7-110">Návrhář vzorců a funkce mezního limitu použitá pro výpočet TDS</span><span class="sxs-lookup"><span data-stu-id="ea3c7-110">Formula designer and threshold limit functionality used for TDS calculation</span></span>](apac-ind-TDS-Formula-designer.md)
- [<span data-ttu-id="ea3c7-111">Výpočet TDS na faktury, platby, směnky a mezipodnikové transakce</span><span class="sxs-lookup"><span data-stu-id="ea3c7-111">Calculation of TDS on invoices, payments, promissory notes, and intercompany transactions</span></span>](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [<span data-ttu-id="ea3c7-112">Pravidelný proces vypořádání TDS a vypořádání částek TDS k dodavatelů autorit TDS</span><span class="sxs-lookup"><span data-stu-id="ea3c7-112">Periodic TDS settlement process and settlement of TDS amounts to TDS authority vendors</span></span>](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [<span data-ttu-id="ea3c7-113">Záznam a aktualizace čísel a dat certifikátu TDS</span><span class="sxs-lookup"><span data-stu-id="ea3c7-113">Recording and updating TDS certificate numbers and dates</span></span>](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a><span data-ttu-id="ea3c7-114">Úvod do TDS</span><span class="sxs-lookup"><span data-stu-id="ea3c7-114">Introduction to TDS</span></span>

<span data-ttu-id="ea3c7-115">Podle zákona o dani z příjmu z roku 1961 je daň z příjmu odebírána u zdroje příjemcem služby v době zálohy nebo zúčtování kreditu, podle toho, co nastane dříve.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-115">Per the Income tax Act, 1961, income tax is deducted at the source by the receiver of the service at the time of advance payment or accounting of credit, whichever occurs first.</span></span> <span data-ttu-id="ea3c7-116">Osoba, která provádí platbu, musí odečíst částku daně a zaplatit pouze čistý zůstatek poskytovateli služby.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-116">The person who makes the payment must deduct the tax amount and pay only the net balance to the provider of the service.</span></span> <span data-ttu-id="ea3c7-117">TDS se aplikuje na služby, které stanoví vláda, a daň se odečte za použití sazeb stanovených vládou pro určité období.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-117">TDS is applied on services that the government specifies, and the tax is deducted by using the rates that the government specifies for a period.</span></span> <span data-ttu-id="ea3c7-118">Míra odpočtu je založena na stavu subjektu, který přijímá platbu nebo poskytuje službu.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-118">The rate of deduction is based on the status of the entity that receives the payment or provides the service.</span></span> <span data-ttu-id="ea3c7-119">Stavy zahrnují **Osoba**, **Hinduistická nerozdělená rodina** (**HUF**), **Společnost**, **Firma**, **Sdružení osob** (**AOP**), **Organizace jednotlivců** (**BOI**) a **Obecní úřad**.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-119">Statuses include **Individual**, **Hindu Undivided Family** (**HUF**), **Company**, **Firm**, **Association of Persons** (**AOP**), **Body of Individuals** (**BOI**), and **Local authority**.</span></span>

<span data-ttu-id="ea3c7-120">V následujících částech je uveden seznam služeb, na které se TDS aplikuje, jak stanoví vláda Indie.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-120">The following sections list the services that TDS is applied on, as specified by the Government of India.</span></span>

<span data-ttu-id="ea3c7-121">**Obyvatelé**</span><span class="sxs-lookup"><span data-stu-id="ea3c7-121">**Residents**</span></span>

- <span data-ttu-id="ea3c7-122">Příjmy z platů (pod §192)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-122">Income from salaries (Under section 192)</span></span>
- <span data-ttu-id="ea3c7-123">Příjem z úroků z cenných papírů (podle §193)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-123">Income from interest on securities (Under section 193)</span></span>
- <span data-ttu-id="ea3c7-124">Příjmy z dividend (podle §194)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-124">Income from dividend (Under section 194)</span></span>
- <span data-ttu-id="ea3c7-125">Příjmy z úroků (podle §194A)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-125">Income from interest (Under section 194A)</span></span>
- <span data-ttu-id="ea3c7-126">Příjmy z loterií nebo soutěží (podle §194B)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-126">Income from lotteries or puzzles (Under section 194B)</span></span>
- <span data-ttu-id="ea3c7-127">Vítězství na dostizích atd. (Podle § 194BB)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-127">Winning from horse races etc. (Under section 194BB)</span></span>
- <span data-ttu-id="ea3c7-128">Dodavatelé a subdodavatelé (podle §194C)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-128">Contractors and sub-contractors (Under section 194C)</span></span>
- <span data-ttu-id="ea3c7-129">Pojistná provize (podle §194D)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-129">Insurance commission (Under section 194D)</span></span>
- <span data-ttu-id="ea3c7-130">Příjem z vkladu v rámci národního systému spoření (podle §194EE)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-130">Income from deposit under national saving scheme (Under section 194EE)</span></span>
- <span data-ttu-id="ea3c7-131">Příjem ze podílového fondu nebo UTI (podle §194F)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-131">Income from mutual fund or UTI (Under section 194F)</span></span>
- <span data-ttu-id="ea3c7-132">Provize, odměna, cena atd. za prodej nebo loterii (podle §194G)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-132">Commission, Remuneration, Prize etc., on sale or lottery (Under section 194G)</span></span>
- <span data-ttu-id="ea3c7-133">Výplata provize nebo zprostředkování (podle §194H)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-133">Payment of Commission or brokerage (Under section 194H)</span></span>
- <span data-ttu-id="ea3c7-134">Nájemné (podle §194I)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-134">Rent (Under section 194I)</span></span>
- <span data-ttu-id="ea3c7-135">Profesionální služby (podle §194J)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-135">Professional service (Under section 194J)</span></span>
- <span data-ttu-id="ea3c7-136">Příjmy z jednotek (podle §194K)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-136">Income from Units (Under section 194K)</span></span>
- <span data-ttu-id="ea3c7-137">Výplata kompenzace při nabytí určitého nemovitého majetku (podle §194LA)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-137">Payment of compensation on acquisition of certain immovable property (Under section 194LA)</span></span>

<span data-ttu-id="ea3c7-138">**Nerezidenti**</span><span class="sxs-lookup"><span data-stu-id="ea3c7-138">**Non-residents**</span></span>

- <span data-ttu-id="ea3c7-139">Platby nerezidentním sportovcům nebo sportovním svazům (podle §194E)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-139">Payments to Non-resident sportsmen or sports association (Under section 194E)</span></span>
- <span data-ttu-id="ea3c7-140">Ostatní částky (podle §195)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-140">Other sums (Under section 195)</span></span>
- <span data-ttu-id="ea3c7-141">Příjmy za jednotky nerezidentů (podle §196A)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-141">Income in respect of units of non-residents (Under section 196A)</span></span>

    - <span data-ttu-id="ea3c7-142">Výnosy z dluhopisů nebo akcií indické společnosti v cizí měně (podle §196C)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-142">Income from foreign currency bonds or shares of Indian Company (Under section 196C)</span></span>
    - <span data-ttu-id="ea3c7-143">Příjmy zahraničních institucionálních investorů z cenných papírů (podle §196D)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-143">Incomes of foreign institutional investors from securities (Under section 196D)</span></span>
    - <span data-ttu-id="ea3c7-144">Plat a všechny ostatní kladné příjmy podle jakéhokoli paragrafu o příjmu (§192)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-144">Salary and all other positive incomes under any head on income (Section 192)</span></span>
    - <span data-ttu-id="ea3c7-145">Úroky z cenných papírů (§193)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-145">Interest on securities (Section 193)</span></span>
    - <span data-ttu-id="ea3c7-146">Úroky jiné než úroky z cenných papírů (§194A)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-146">Interest other than interest on securities (Section 194A)</span></span>
    - <span data-ttu-id="ea3c7-147">Platby dodavatelům a subdodavatelům (§194C)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-147">Payments to contractors and sub-contractors (Section 194C)</span></span>
    - <span data-ttu-id="ea3c7-148">Výhry z loterie nebo křížovek (§194B)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-148">Winnings from Lottery or crossword puzzles (Section 194B)</span></span>
    - <span data-ttu-id="ea3c7-149">Výhry z dostihů atd. (§194BB)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-149">Winnings from horse races (Section 194BB)</span></span>
    - <span data-ttu-id="ea3c7-150">Pojišťovací provize pokrývající všechny platby za pojišťovací činnost (§194D)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-150">Insurance Commission covering all payments for procuring Insurance business (Section 194D)</span></span>
    - <span data-ttu-id="ea3c7-151">Jakýkoli jiný úrok než úrok z cenných papírů splatný nerezidentům, kteří nejsou společností, nebo zahraniční společnosti (§195)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-151">Any interest other than interest on securities payable to non-residents not being a company or to a foreign company (Section 195)</span></span>
    - <span data-ttu-id="ea3c7-152">Platba nerezidentnímu sportovci včetně sportovce nebo sportovního svazu nebo instituce.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-152">Payment to non-resident sportsman including athlete or sports association or institution.</span></span> <span data-ttu-id="ea3c7-153">V případě nerezidentního sportovce platby v souvislosti s reklamami a články o jakékoli hře/sportu v Indii v novinách, časopisech atd.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-153">In case of non-resident sportsman, payments in respect of advertisements as well as articles on any game/sports in India in newspapers, magazines, and so.</span></span> <span data-ttu-id="ea3c7-154">jsou zahrnuty (§194E)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-154">is included (Section 194E)</span></span>
    - <span data-ttu-id="ea3c7-155">Platba za vklady v rámci NSS \[Národní systém spoření\] (§194EE)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-155">Payment in respect of deposits under NSS \[National Savings Scheme\] (Section 194EE)</span></span>
    - <span data-ttu-id="ea3c7-156">Platba na účet zpětného odkupu podílových listů podílovým fondem nebo UTI (§194F)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-156">Payment on account of repurchase of Units by Mutual Fund or UTI (Section 194F)</span></span>
    - <span data-ttu-id="ea3c7-157">Výplata provize nebo zprostředkování (§194H)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-157">Payment for Commission or brokerage (Section 194H)</span></span>
    - <span data-ttu-id="ea3c7-158">Platba nájemného (§194I)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-158">Payment of rent (Section 194I)</span></span>
    - <span data-ttu-id="ea3c7-159">Úhrada poplatků za odborné nebo technické služby (§194J)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-159">Payment of fees for professional or technical services (Section 194J)</span></span>
    - <span data-ttu-id="ea3c7-160">Provize prodejcům, distributorům, kupujícím a prodejcům loterijních tiketů, včetně odměn nebo výher za tyto tikety (§194G)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-160">Commission to Stockiest, distributors, buyers and sellers of Lottery tickets including remuneration or prize on such tickets (Section 194G)</span></span>
    - <span data-ttu-id="ea3c7-161">Výnosy z podílových listů nakoupených v cizí měně nebo dlouhodobý kapitálový zisk z převodu těchto podílových jednotek nakoupených v cizí měně (§196B)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-161">Income from Units purchased in foreign currency or long-term capital gain arising from the transfer of such Units purchased in foreign currency (Section 196B)</span></span>
    - <span data-ttu-id="ea3c7-162">Výplata jakýchkoli příjmů nerezidentům z úroků nebo dividend z dluhopisů a akcií (§196C)</span><span class="sxs-lookup"><span data-stu-id="ea3c7-162">Payment of any income to non-residents in respect of interest or dividend on bonds and shares (Section 196C)</span></span>

<span data-ttu-id="ea3c7-163">TDS se počítá za nákupy, prodeje, výnosy z prodeje, dobropisy, akvizice dlouhodobého majetku, zálohy, zálohy, směnky, daň z prací a mezipodnikové transakce.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-163">TDS is calculated on purchases, sales, sales returns, credit notes, fixed asset acquisitions, prepayments, advance payments, promissory notes, works tax, and intercompany transactions.</span></span>

> [!NOTE]
> <span data-ttu-id="ea3c7-164">V aktuálním indickém daňovém scénáři se TDS nevypočítává z prodejních transakcí.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-164">In the current Indian tax scenario, TDS isn't calculated on sales transactions.</span></span> <span data-ttu-id="ea3c7-165">Systém však zahrnuje rezervu na výpočet TDS zpětně získatelných u prodejních transakcí, zejména u transakcí mezi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-165">However, the system includes a provision to calculate TDS recoverable on sales transactions, especially for intercompany transactions.</span></span>

<span data-ttu-id="ea3c7-166">Výpočet TDS vždy zohledňuje prahovou hodnotu a prahovou hodnotu výjimky, které jsou definovány pro komponentu TDS.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-166">The calculation of TDS always considers the threshold and the exception threshold that are defined for the TDS component.</span></span>

<span data-ttu-id="ea3c7-167">Musí být spuštěn pravidelný proces vypořádání TDS a platby TDS musí být vypořádány prodejcům autorit TDS.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-167">The periodic TDS settlement process must be run, and the TDS payments must be settled to TDS authority vendors.</span></span>

<span data-ttu-id="ea3c7-168">Je možné zaznamenávat a aktualizovat čísla a data certifikátů TDS, která jsou přijímána od prodejců nebo zákazníků.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-168">The certificate numbers and dates for TDS certificates that are received from vendors or customers can be recorded and updated.</span></span> <span data-ttu-id="ea3c7-169">Navíc lze ve Finance generovat čtvrtletní výkazy formuláře 26Q a formuláře 27Q a certifikát formuláře 16A pro TDS.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-169">Additionally, Form 26Q and Form 27Q quarterly statements, and the Form 16A certificate for TDS, can be generated in Finance.</span></span>

## <a name="setting-up-and-working-with-tds"></a><span data-ttu-id="ea3c7-170">Nastavení a práce s TDS</span><span class="sxs-lookup"><span data-stu-id="ea3c7-170">Setting up and working with TDS</span></span>

<span data-ttu-id="ea3c7-171">Zde je přehled procesu nastavení a práce s TDS:</span><span class="sxs-lookup"><span data-stu-id="ea3c7-171">Here is an overview of the process for setting up and working with TDS:</span></span>

1. <span data-ttu-id="ea3c7-172">**Nastavení TDS:**</span><span class="sxs-lookup"><span data-stu-id="ea3c7-172">**TDS setup:**</span></span>

    - <span data-ttu-id="ea3c7-173">Nastavení parametrů:</span><span class="sxs-lookup"><span data-stu-id="ea3c7-173">Parameter setup:</span></span>

        - <span data-ttu-id="ea3c7-174">V parametrech hlavní knihy aktivujte parametry související s TDS.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-174">In General ledger parameters, activate parameters that are related to TDS.</span></span>
        - <span data-ttu-id="ea3c7-175">V parametrech hlavní knihy nastavte číselnou řadu pro platby srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-175">In General ledger parameters, set up the number sequence for withholding tax payments.</span></span>
        - <span data-ttu-id="ea3c7-176">Nastavte parametry v závazcích a pohledávkách.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-176">Set up parameters in Accounts payable and Accounts receivable.</span></span>

    - <span data-ttu-id="ea3c7-177">Základní nastavení:</span><span class="sxs-lookup"><span data-stu-id="ea3c7-177">Basic setup:</span></span>

        - <span data-ttu-id="ea3c7-178">Nastavte registrační čísla TDS pro společnost, zákazníky a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-178">Set up TDS registration numbers for a company, customers, and vendors.</span></span>
        - <span data-ttu-id="ea3c7-179">Nastavení skupin komponent TDS.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-179">Set up TDS component groups.</span></span>
        - <span data-ttu-id="ea3c7-180">Nastavte komponenty TDS, připojte k nim skupiny komponent TDS a definujte pro ně prahovou hodnotu a prahovou hodnotu výjimky.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-180">Set up TDS components, attach TDS component groups to them, and define the threshold and exception threshold for them.</span></span>
        - <span data-ttu-id="ea3c7-181">Nastavte oprávnění TDS.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-181">Set up TDS authorities.</span></span>
        - <span data-ttu-id="ea3c7-182">Nastavte období vyrovnání TDS.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-182">Set up TDS settlement periods.</span></span>
        - <span data-ttu-id="ea3c7-183">Nastavte daňové kódy TDS a připojte k nim komponenty TDS.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-183">Set up TDS tax codes, and attach TDS components to them.</span></span>
        - <span data-ttu-id="ea3c7-184">Nastavte daňové skupiny TDS a připojte k nim daňové kódy TDS.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-184">Set up TDS tax groups, and attach TDS tax codes to them.</span></span>
        - <span data-ttu-id="ea3c7-185">V návrháři vzorců definujte vzorec pro výpočet TDS pro skupinu TDS.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-185">In the formula designer, define a formula to calculate TDS for a TDS group.</span></span>
        - <span data-ttu-id="ea3c7-186">Zaznamenejte čísla koncesních certifikátů TDS.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-186">Record TDS concession certificate numbers.</span></span>

    - <span data-ttu-id="ea3c7-187">Účty hlavní knihy a nastavení společnosti:</span><span class="sxs-lookup"><span data-stu-id="ea3c7-187">Ledger accounts and company setup:</span></span>

        - <span data-ttu-id="ea3c7-188">Nastavte účty hlavní knihy pohledávky a zakázky.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-188">Set up TDS payable and receivable ledger accounts.</span></span>
        - <span data-ttu-id="ea3c7-189">Nastavte pro společnost daňový odpočet a číslo účtu inkasa (TAN) a kategorii typu odpočtu.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-189">Set up a Tax Deduction and Collection Account Number (TAN) and a deductor type category for the company.</span></span>

    - <span data-ttu-id="ea3c7-190">Další nastavení:</span><span class="sxs-lookup"><span data-stu-id="ea3c7-190">Other setup:</span></span>

        - <span data-ttu-id="ea3c7-191">Nastavte plán plateb, který zahrnuje přidělení TDS.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-191">Set up a payment schedule that includes TDS allocation.</span></span>
        - <span data-ttu-id="ea3c7-192">Nastavte typ platebního poplatku pro platby úřadu TCS.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-192">Set up a payment fee type for payments to the TDS authority.</span></span>
        - <span data-ttu-id="ea3c7-193">Nastavte informace o skupinách TDS, stálých číslech účtů (PAN) a TAN pro dodavatele a zákazníky.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-193">Set up information about TDS groups, permanent account numbers (PANs), and TANs for vendors and customers.</span></span>

2. <span data-ttu-id="ea3c7-194">**Výpočet TDS v transakcích:**</span><span class="sxs-lookup"><span data-stu-id="ea3c7-194">**Calculation of TDS in transactions:**</span></span>

    - <span data-ttu-id="ea3c7-195">Faktury a platby</span><span class="sxs-lookup"><span data-stu-id="ea3c7-195">Invoices and payments</span></span>
    - <span data-ttu-id="ea3c7-196">Vlastní směnky</span><span class="sxs-lookup"><span data-stu-id="ea3c7-196">Promissory notes</span></span>
    - <span data-ttu-id="ea3c7-197">Platby předem</span><span class="sxs-lookup"><span data-stu-id="ea3c7-197">Advance payments</span></span>
    - <span data-ttu-id="ea3c7-198">Zálohy</span><span class="sxs-lookup"><span data-stu-id="ea3c7-198">Prepayments</span></span>

3. <span data-ttu-id="ea3c7-199">**Vyrovnání TDS:**</span><span class="sxs-lookup"><span data-stu-id="ea3c7-199">**TDS settlement:**</span></span>

    - <span data-ttu-id="ea3c7-200">Periodický proces vypořádání TDS</span><span class="sxs-lookup"><span data-stu-id="ea3c7-200">Periodic TDS settlement process</span></span>
    - <span data-ttu-id="ea3c7-201">Vypořádání plateb TDS prodejcům autorit TDS a generování challan TDS</span><span class="sxs-lookup"><span data-stu-id="ea3c7-201">Settlement of TDS payments to TDS authority vendors and generation of TDS challan</span></span>

4. <span data-ttu-id="ea3c7-202">**Dotazy, výkazy a certifikát TDS:**</span><span class="sxs-lookup"><span data-stu-id="ea3c7-202">**TDS inquiries, statements, and certificate:**</span></span>

    - <span data-ttu-id="ea3c7-203">Zaznamenejte a aktualizujte čísla a data certifikátu TDS.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-203">Record and update TDS certificate numbers and dates.</span></span>
    - <span data-ttu-id="ea3c7-204">Vygenerujte dotaz TDS a zaúčtovaný dotaz TDS.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-204">Generate a TDS inquiry and a posted TDS inquiry.</span></span>
    - <span data-ttu-id="ea3c7-205">Generujte čtvrtletní výkazy Formuláře 27A, Formuláře 26Q a Formuláře 27Q TDS a e-TDS.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-205">Generate Form 27A, Form 26Q, and Form 27Q TDS and e-TDS quarterly statements.</span></span>
    - <span data-ttu-id="ea3c7-206">Vygenerujte certifikát TDS formuláře 16A.</span><span class="sxs-lookup"><span data-stu-id="ea3c7-206">Generate a Form 16A TDS certificate.</span></span>
