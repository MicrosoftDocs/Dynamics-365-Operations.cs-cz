---
title: "Mobilní schvalování faktur"
description: "Toto téma poskytuje praktický přístup k navrhování mobilních scénářů v aplikaci Dynamics 365 for Finance and Operations převzetím schválení faktur dodavatele pro mobilní zařízení jako příklad použití."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c579db5a922d81a2781ec2011e148db54fac288d
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="mobile-invoice-approvals"></a><span data-ttu-id="bf32e-103">Mobilní schvalování faktur</span><span class="sxs-lookup"><span data-stu-id="bf32e-103">Mobile invoice approvals</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bf32e-104">Mobilní funkce v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition umožňují podnikovým uživatelům navrhovat mobilní prostředí.</span><span class="sxs-lookup"><span data-stu-id="bf32e-104">Mobile capabilities in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition let a business user design mobile experiences.</span></span> <span data-ttu-id="bf32e-105">Pro pokročilé scénáře platforma také vývojářům umožňuje rozšířit možnosti podle vlastních potřeb.</span><span class="sxs-lookup"><span data-stu-id="bf32e-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="bf32e-106">Nejúčinnějším způsobem, jak se naučit některé nové pojmy v oblasti mobilních zařízení, je projít proces navrhování několik scénářů.</span><span class="sxs-lookup"><span data-stu-id="bf32e-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="bf32e-107">Toto téma poskytuje praktický přístup k navrhování mobilních scénářů převzetím schválení faktur dodavatele pro mobilní zařízení jako příklad použití.</span><span class="sxs-lookup"><span data-stu-id="bf32e-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="bf32e-108">Toto téma by vám mělo pomoci navrhnout jiné varianty scénářů a lze je také použít pro další scénáře, které nesouvisejí s fakturami dodavatele.</span><span class="sxs-lookup"><span data-stu-id="bf32e-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="bf32e-109">Požadavky</span><span class="sxs-lookup"><span data-stu-id="bf32e-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="bf32e-110">Předpoklad</span><span class="sxs-lookup"><span data-stu-id="bf32e-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="bf32e-111">popis</span><span class="sxs-lookup"><span data-stu-id="bf32e-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf32e-112">Předběžná verze mobilní příručky</span><span class="sxs-lookup"><span data-stu-id="bf32e-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="bf32e-113">Mobilní platforma</span><span class="sxs-lookup"><span data-stu-id="bf32e-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="bf32e-114">Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="bf32e-114">Dynamics 365 for Finance and Operations</span></span>                                                                             | <span data-ttu-id="bf32e-115">Prostředí, které má Microsoft Dynamics 365 for Operations verzi 1611 a Microsoft Dynamics for Operations aktualizaci platformy 3 (listopad 2016)</span><span class="sxs-lookup"><span data-stu-id="bf32e-115">An environment that has Microsoft Dynamics 365 for Operations version 1611 and Microsoft Dynamics for Operations platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="bf32e-116">Nainstalujte opravu hotfix KB 3204341.</span><span class="sxs-lookup"><span data-stu-id="bf32e-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="bf32e-117">Záznamník úloh může omylem zaznamenat dva příkazy k zavření rozevíracích dialogových oken, které jsou součástí aktualizace 3 Dynamics 365 for Operations (aktualizace z listopadu 2016)</span><span class="sxs-lookup"><span data-stu-id="bf32e-117">Task recorder can erroneously record two Close commands for dropdown dialogs this is included in Dynamics 365 for Operation platform update 3 (November 2016 update)</span></span> |
| <span data-ttu-id="bf32e-118">Nainstalujte opravu hotfix KB 3207800.</span><span class="sxs-lookup"><span data-stu-id="bf32e-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="bf32e-119">Tato oprava hotfix umožňuje zobrazovat přílohy v mobilním klientovi, který je zahrnutý v aktualizaci 3 platformy Dynamics 365 for Operations (aktualizace z listopadu 2016).</span><span class="sxs-lookup"><span data-stu-id="bf32e-119">This hotfix enables attachments to be viewed on the mobile client this is included in Dynamics 365 for Operation platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="bf32e-120">Nainstalujte opravu hotfix KB 3208224.</span><span class="sxs-lookup"><span data-stu-id="bf32e-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="bf32e-121">Kód aplikace pro mobilní aplikaci schvalování faktur dodavatele je zahrnut v aplikaci Microsoft Dynamics AX 7.0.1 (květen 2016).</span><span class="sxs-lookup"><span data-stu-id="bf32e-121">Application code for the mobile vendor invoice approval application this is included in Microsoft Dynamics AX application 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="bf32e-122">Zařízení se systémem Android nebo iOS nebo se systémem Windows, které má nainstalovanou mobilní aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="bf32e-122">An Android or iOS or a Windows device that has the mobile app installed for Finance and Operations</span></span> | <span data-ttu-id="bf32e-123">Vyhledejte aplikaci v příslušném obchodě s aplikacemi.</span><span class="sxs-lookup"><span data-stu-id="bf32e-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="bf32e-124">Úvod</span><span class="sxs-lookup"><span data-stu-id="bf32e-124">Introduction</span></span>
<span data-ttu-id="bf32e-125">Mobilní schválení faktur dodavatele vyžadují tři opravy hotfix, které jsou uvedeny v části "Předpoklady".</span><span class="sxs-lookup"><span data-stu-id="bf32e-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="bf32e-126">Tyto opravy hotfix neposkytují pracovní prostor pro schválení faktury.</span><span class="sxs-lookup"><span data-stu-id="bf32e-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="bf32e-127">Chcete-li zjistit, co je pracovní prostor v souvislosti s mobilními zařízeními, přečtěte si příručku pro mobilní zařízení, která je uvedena v části "Předpoklady".</span><span class="sxs-lookup"><span data-stu-id="bf32e-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="bf32e-128">Musí být navržen pracovní prostor schválení faktury.</span><span class="sxs-lookup"><span data-stu-id="bf32e-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="bf32e-129">Každá organizace ladí a definuje svůj svůj obchodní proces pro faktury dodavatele jinak.</span><span class="sxs-lookup"><span data-stu-id="bf32e-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="bf32e-130">Dříve, než navrhnete mobilní prostředí pro schválení faktury dodavatele, měli byste zvážit následující aspekty obchodního procesu.</span><span class="sxs-lookup"><span data-stu-id="bf32e-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="bf32e-131">Základem je využívat tyto datové body co nejvíce, aby se optimalizovalo uživatelské prostředí v zařízení.</span><span class="sxs-lookup"><span data-stu-id="bf32e-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="bf32e-132">Která pole z hlavičky faktury bude uživatel chtít vidět v mobilním prostředí a v jakém pořadí?</span><span class="sxs-lookup"><span data-stu-id="bf32e-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="bf32e-133">Která pole z řádek faktury bude uživatel chtít vidět v mobilního prostředí a v jakém pořadí?</span><span class="sxs-lookup"><span data-stu-id="bf32e-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="bf32e-134">Kolik má faktura řádků?</span><span class="sxs-lookup"><span data-stu-id="bf32e-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="bf32e-135">Uplatněte zde pravidlo 80-20 a optimalizujte pro 80 procent.</span><span class="sxs-lookup"><span data-stu-id="bf32e-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="bf32e-136">Budou uživatelé chtít vidět rozúčtování (kódování faktury) v mobilním zařízení během kontrol?</span><span class="sxs-lookup"><span data-stu-id="bf32e-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="bf32e-137">Pokud je odpověď na tuto otázku Ano, zvažte následující otázky:</span><span class="sxs-lookup"><span data-stu-id="bf32e-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="bf32e-138">Kolik rozúčtování (rozšířená cena, DPH, poplatky, rozdělení atd.) je pro řádek faktury k dispozici?</span><span class="sxs-lookup"><span data-stu-id="bf32e-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="bf32e-139">Znovu použijte pravidlo 80-20.</span><span class="sxs-lookup"><span data-stu-id="bf32e-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="bf32e-140">Mají faktury také rozúčtování v hlavičce faktury?</span><span class="sxs-lookup"><span data-stu-id="bf32e-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="bf32e-141">Pokud ano, budou tato rozúčtování k dispozici v zařízení?</span><span class="sxs-lookup"><span data-stu-id="bf32e-141">If so, should these accounting distributions be available on the device?</span></span>

> [!NOTE]
> <span data-ttu-id="bf32e-142">Toto téma nevysvětluje, jak upravit rozúčtování, protože tato funkce není aktuálně podporována pro mobilní scénáře.</span><span class="sxs-lookup"><span data-stu-id="bf32e-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="bf32e-143">Budou uživatelé chtít vidět přílohy pro fakturu na zařízení?</span><span class="sxs-lookup"><span data-stu-id="bf32e-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="bf32e-144">Návrh mobilního prostředí pro schválení faktur se liší v závislosti na odpovědích na tyto otázky.</span><span class="sxs-lookup"><span data-stu-id="bf32e-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="bf32e-145">Cílem je optimalizovat uživatelské prostředí pro obchodní proces na mobilních zařízeních v organizaci.</span><span class="sxs-lookup"><span data-stu-id="bf32e-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="bf32e-146">Ve zbývající části tohoto tématu se podíváme na dvě varianty scénáře, které jsou založeny na různých odpovědích na předchozí dotazy.</span><span class="sxs-lookup"><span data-stu-id="bf32e-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="bf32e-147">Platí zásada, abyste při práci s návrhářem mobilních aplikací nezapomněli publikovat změny, aby se zabránilo ztrátě aktualizací.</span><span class="sxs-lookup"><span data-stu-id="bf32e-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="bf32e-148">Návrh scénáře schválení jednoduché faktury pro společnosti Contoso</span><span class="sxs-lookup"><span data-stu-id="bf32e-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf32e-149">Atribut scénáře</span><span class="sxs-lookup"><span data-stu-id="bf32e-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="bf32e-150">Odpověď</span><span class="sxs-lookup"><span data-stu-id="bf32e-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bf32e-151">Která pole z hlavičky faktury bude uživatel chtít vidět v mobilním prostředí a v jakém pořadí?</span><span class="sxs-lookup"><span data-stu-id="bf32e-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="bf32e-152">Název dodavatele</span><span class="sxs-lookup"><span data-stu-id="bf32e-152">Vendor name</span></span></li>
<li><span data-ttu-id="bf32e-153">Faktura celkem</span><span class="sxs-lookup"><span data-stu-id="bf32e-153">Invoice total</span></span></li>
<li><span data-ttu-id="bf32e-154">Účet faktury</span><span class="sxs-lookup"><span data-stu-id="bf32e-154">Invoice account</span></span></li>
<li><span data-ttu-id="bf32e-155">Číslo faktury</span><span class="sxs-lookup"><span data-stu-id="bf32e-155">Invoice number</span></span></li>
<li><span data-ttu-id="bf32e-156">Datum fakturace</span><span class="sxs-lookup"><span data-stu-id="bf32e-156">Invoice date</span></span></li>
<li><span data-ttu-id="bf32e-157">Popis faktury</span><span class="sxs-lookup"><span data-stu-id="bf32e-157">Invoice description</span></span></li>
<li><span data-ttu-id="bf32e-158">Datum splatnosti</span><span class="sxs-lookup"><span data-stu-id="bf32e-158">Due date</span></span></li>
<li><span data-ttu-id="bf32e-159">Měna faktury</span><span class="sxs-lookup"><span data-stu-id="bf32e-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf32e-160">Která pole z řádek faktury bude uživatel chtít vidět v mobilního prostředí a v jakém pořadí?</span><span class="sxs-lookup"><span data-stu-id="bf32e-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="bf32e-161">Kategorie zásobování</span><span class="sxs-lookup"><span data-stu-id="bf32e-161">Procurement category</span></span></li>
<li><span data-ttu-id="bf32e-162">Množství</span><span class="sxs-lookup"><span data-stu-id="bf32e-162">Quantity</span></span></li>
<li><span data-ttu-id="bf32e-163">Jedn. cena</span><span class="sxs-lookup"><span data-stu-id="bf32e-163">Unit price</span></span></li>
<li><span data-ttu-id="bf32e-164">Čistá částka řádku</span><span class="sxs-lookup"><span data-stu-id="bf32e-164">Line net amount</span></span></li>
<li><span data-ttu-id="bf32e-165">Částka sestavy 1099</span><span class="sxs-lookup"><span data-stu-id="bf32e-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf32e-166">Kolik má faktura řádků?</span><span class="sxs-lookup"><span data-stu-id="bf32e-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="bf32e-167">Uplatněte zde pravidlo 80-20 a optimalizujte pro 80 procent.</span><span class="sxs-lookup"><span data-stu-id="bf32e-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="bf32e-168">1</span><span class="sxs-lookup"><span data-stu-id="bf32e-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf32e-169">Budou uživatelé chtít vidět rozúčtování (kódování faktury) v mobilním zařízení během kontrol?</span><span class="sxs-lookup"><span data-stu-id="bf32e-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="bf32e-170">Ano</span><span class="sxs-lookup"><span data-stu-id="bf32e-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf32e-171">Kolik rozúčtování (rozšířená cena, DPH, poplatky atd.) je pro řádek faktury k dispozici?</span><span class="sxs-lookup"><span data-stu-id="bf32e-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="bf32e-172">Znovu použijte pravidlo 80-20.</span><span class="sxs-lookup"><span data-stu-id="bf32e-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="bf32e-173">Rozšířená cena: 2 DPH 2: 0 Poplatky: 0</span><span class="sxs-lookup"><span data-stu-id="bf32e-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf32e-174">Mají faktury také rozúčtování v hlavičce faktury?</span><span class="sxs-lookup"><span data-stu-id="bf32e-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="bf32e-175">Pokud ano, budou tato rozúčtování k dispozici v zařízení?</span><span class="sxs-lookup"><span data-stu-id="bf32e-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="bf32e-176">Nepoužito</span><span class="sxs-lookup"><span data-stu-id="bf32e-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf32e-177">Budou uživatelé chtít vidět přílohy pro fakturu na zařízení?</span><span class="sxs-lookup"><span data-stu-id="bf32e-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="bf32e-178">Ano</span><span class="sxs-lookup"><span data-stu-id="bf32e-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="bf32e-179">Vytvoření pracovního prostoru</span><span class="sxs-lookup"><span data-stu-id="bf32e-179">Create the workspace</span></span>

1.  <span data-ttu-id="bf32e-180">V prohlížeči otevřete Finance and Operations a přihlaste se.</span><span class="sxs-lookup"><span data-stu-id="bf32e-180">In a browser, open Finance and Operations, and sign in.</span></span>
2.  <span data-ttu-id="bf32e-181">Po přihlášení přidejte k adrese URL text **&mode=mobile**, jak ukazuje následující příklad, a aktualizujte stránku: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard**&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="bf32e-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard**&mode=mobile**</span></span>
3.  <span data-ttu-id="bf32e-182">Klikněte na tlačítko **Nastavení** (ozubené kolo) v pravém horním rohu stránky, a pak klikněte na **Mobilní aplikace**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="bf32e-183">Návrhář mobilní aplikace se musí zobrazit stejně jako Záznam úloh.</span><span class="sxs-lookup"><span data-stu-id="bf32e-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="bf32e-184">Kliknutím na tlačítko **Přidat** vytvořte nový pracovní prostor.</span><span class="sxs-lookup"><span data-stu-id="bf32e-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="bf32e-185">V tomto příkladu pojmenujte pracovní prostor **Moje schválení**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="bf32e-186">Zadejte popis.</span><span class="sxs-lookup"><span data-stu-id="bf32e-186">Enter a description.</span></span>
6.  <span data-ttu-id="bf32e-187">Vyberte barvu pracovního prostoru.</span><span class="sxs-lookup"><span data-stu-id="bf32e-187">Select a workspace color.</span></span> <span data-ttu-id="bf32e-188">Barva pracovního prostoru bude použita pro celkový styl mobilního prostředí pro tento pracovní prostor.</span><span class="sxs-lookup"><span data-stu-id="bf32e-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="bf32e-189">Vyberte ikonu pracovního prostoru.</span><span class="sxs-lookup"><span data-stu-id="bf32e-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="bf32e-190">Klikněte na tlačítko **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-190">Click **Done**</span></span>
9.  <span data-ttu-id="bf32e-191">Kliknutím na **Publikovat pracovní prostor** uložte změny</span><span class="sxs-lookup"><span data-stu-id="bf32e-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="bf32e-192">Faktury dodavatele přiřazené mně</span><span class="sxs-lookup"><span data-stu-id="bf32e-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="bf32e-193">První mobilní stránka, kterou byste měli navrhnout, je seznam faktur, které jsou přiřazeny uživateli na revizi.</span><span class="sxs-lookup"><span data-stu-id="bf32e-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="bf32e-194">Při navrhování této mobilní stránky použijte stránku **VendMobileInvoiceAssignedToMeListPage** v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bf32e-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page in Finance and Operations.</span></span> <span data-ttu-id="bf32e-195">Před provedením tohoto postupu se ujistěte, že alespoň jedna dodavatelská faktura je vám přiřazena na revizi a že má řádek faktury dvě rozkontace.</span><span class="sxs-lookup"><span data-stu-id="bf32e-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="bf32e-196">Toto nastavení splňuje požadavky pro tento scénář.</span><span class="sxs-lookup"><span data-stu-id="bf32e-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="bf32e-197">V adrese URL aplikace Finance and Operations nahraďte název položky nabídky hodnotou **VendMobileInvoiceAssignedToMeListPage** k otevření mobilní verze stránky se seznamem **Nevyřízené faktury dodavatele přiřazené mně** v modulu **Závazky**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-197">In the Finance and Operations URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="bf32e-198">V závislosti na počtu faktur, které máte v systému přidělené, se na této stránce se zobrazí tyto faktury.</span><span class="sxs-lookup"><span data-stu-id="bf32e-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="bf32e-199">Pokud chcete najít konkrétní fakturu, můžete použít filtr vlevo.</span><span class="sxs-lookup"><span data-stu-id="bf32e-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="bf32e-200">Nevyžadujeme ale použití konkrétní faktury pro tento příklad.</span><span class="sxs-lookup"><span data-stu-id="bf32e-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="bf32e-201">Vyžadujeme pouze, aby vám byly přiřazeny některé faktury, které vám umožní navrhnout mobilní stránku.</span><span class="sxs-lookup"><span data-stu-id="bf32e-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="bf32e-202">Nové stránky, které jsou k dispozici, byly navrženy speciálně pro vývoj mobilních scénářů pro faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="bf32e-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="bf32e-203">Proto je nutné použít tyto stránky.</span><span class="sxs-lookup"><span data-stu-id="bf32e-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="bf32e-204">Adresa URL by měla vypadat jako následující adresa URL a po jejím zadání se musí zobrazit stránka, která je ukázána na obrázku: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Stránka Nevyřízené faktury, které jsou přiřazeny mně](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="bf32e-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
2.  <span data-ttu-id="bf32e-205">Klikněte na tlačítko **Nastavení** (ozubené kolo) v pravém horním rohu stránky, a pak klikněte na **Mobilní aplikace**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-205">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="bf32e-206">Vyberte pracovní prostor a klikněte na **Úpravy**</span><span class="sxs-lookup"><span data-stu-id="bf32e-206">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="bf32e-207">Klepněte na tlačítko **Přidat stránku** pro vytvoření první mobilní stránky.</span><span class="sxs-lookup"><span data-stu-id="bf32e-207">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="bf32e-208">Zadejte název jako například **Moje faktury dodavatele** a popis jako například **Faktury dodavatele přiřazené mně ke kontrole**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-208">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="bf32e-209">Klepněte na tlačítko **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-209">Click **Done**.</span></span>
7.  <span data-ttu-id="bf32e-210">V mobilním návrháři na kartě **Pole** klepněte na tlačítko **Vybrat pole**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-210">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="bf32e-211">Sloupce na stránce seznamu musí vypadat podobně jako na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="bf32e-211">The columns on the list page must resemble the following illustration.</span></span> <span data-ttu-id="bf32e-212">[![Sloupce na stránce Čekající faktury dodavatele přiřazené mně](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="bf32e-212">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
8.  <span data-ttu-id="bf32e-213">Přidejte požadované sloupce ze stránky seznamu, které musí být zobrazeny pro uživatele na mobilní stránce.</span><span class="sxs-lookup"><span data-stu-id="bf32e-213">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="bf32e-214">Pořadí, ve kterém přidáváte, je pořadí, ve kterém se pole zobrazí koncovému uživateli.</span><span class="sxs-lookup"><span data-stu-id="bf32e-214">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="bf32e-215">Jediný způsob, jak změnit pořadí polí, je opětovný výběr všech polí.</span><span class="sxs-lookup"><span data-stu-id="bf32e-215">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="bf32e-216">Na základě požadavků pro tento scénář je vyžadováno následující osm polí.</span><span class="sxs-lookup"><span data-stu-id="bf32e-216">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="bf32e-217">Nicméně někteří uživatelé mohou považovat osm polí za příliš mnoho informací v mobilním zařízení.</span><span class="sxs-lookup"><span data-stu-id="bf32e-217">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="bf32e-218">Nejdůležitější pole proto ukážeme v zobrazení mobilního seznamu.</span><span class="sxs-lookup"><span data-stu-id="bf32e-218">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="bf32e-219">Zbývající pole se zobrazí v zobrazení podrobností, které můžeme navrhnout později.</span><span class="sxs-lookup"><span data-stu-id="bf32e-219">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="bf32e-220">Nyní přidáme následující pole.</span><span class="sxs-lookup"><span data-stu-id="bf32e-220">For now, we will add the following fields.</span></span> <span data-ttu-id="bf32e-221">Klepněte na znaménko plus (**+**) v těchto sloupcích pro přidání na mobilní stránku.</span><span class="sxs-lookup"><span data-stu-id="bf32e-221">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="bf32e-222">Název dodavatele</span><span class="sxs-lookup"><span data-stu-id="bf32e-222">Vendor name</span></span>
    - <span data-ttu-id="bf32e-223">Faktura celkem</span><span class="sxs-lookup"><span data-stu-id="bf32e-223">Invoice total</span></span>
    - <span data-ttu-id="bf32e-224">Účet faktury</span><span class="sxs-lookup"><span data-stu-id="bf32e-224">Invoice account</span></span>
    - <span data-ttu-id="bf32e-225">Číslo faktury</span><span class="sxs-lookup"><span data-stu-id="bf32e-225">Invoice number</span></span>
    - <span data-ttu-id="bf32e-226">Datum fakturace</span><span class="sxs-lookup"><span data-stu-id="bf32e-226">Invoice date</span></span>

    <span data-ttu-id="bf32e-227">Po přidání polí musí mobilní stránka vypadat podobně jako na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="bf32e-227">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    <span data-ttu-id="bf32e-228">[![Stránka po přidání polí](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="bf32e-228">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>
9.  <span data-ttu-id="bf32e-229">Nyní také musíte přidat následující sloupce, abychom mohli později povolit akce pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="bf32e-229">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="bf32e-230">Zobrazit dokončené úkoly</span><span class="sxs-lookup"><span data-stu-id="bf32e-230">Show complete task</span></span>
    - <span data-ttu-id="bf32e-231">Zobrazit úkol delegování</span><span class="sxs-lookup"><span data-stu-id="bf32e-231">Show delegate task</span></span>
    - <span data-ttu-id="bf32e-232">Zobrazit úkol odvolání</span><span class="sxs-lookup"><span data-stu-id="bf32e-232">Show recall task</span></span>
    - <span data-ttu-id="bf32e-233">Zobrazit úkol odmítnutí</span><span class="sxs-lookup"><span data-stu-id="bf32e-233">Show reject task</span></span>
    - <span data-ttu-id="bf32e-234">Zobrazit úkol požadavku na dokončení</span><span class="sxs-lookup"><span data-stu-id="bf32e-234">Show request completion task</span></span>
    - <span data-ttu-id="bf32e-235">Zobrazit úkol opětovného odeslání</span><span class="sxs-lookup"><span data-stu-id="bf32e-235">Show resubmit task</span></span>

10. <span data-ttu-id="bf32e-236">Kliknutím na **Hotovo** ukončete režim úprav.</span><span class="sxs-lookup"><span data-stu-id="bf32e-236">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="bf32e-237">Klikněte na **Zpět** a potom na **Hotovo** pro odchod z pracovního prostoru</span><span class="sxs-lookup"><span data-stu-id="bf32e-237">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="bf32e-238">Kliknutím na **Publikovat pracovní prostor** uložte práci.</span><span class="sxs-lookup"><span data-stu-id="bf32e-238">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="bf32e-239">Povolte možnost **Zobrazit souhrn faktur u nevyřízených faktur dodavatele** ve formuláři Parametry závazků pod možností **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-239">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="bf32e-240">Všimněte si, že pouze tím, že tento parametr povolíte, budou součty faktury vypočteny tak, aby se zobrazovaly na stránce seznamu faktur dodavatele čekajících na vyřízení.</span><span class="sxs-lookup"><span data-stu-id="bf32e-240">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="bf32e-241">To je nová funkce v rámci nezbytné opravy hotfix 3208224.</span><span class="sxs-lookup"><span data-stu-id="bf32e-241">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="bf32e-242">Detaily faktury dodavatele</span><span class="sxs-lookup"><span data-stu-id="bf32e-242">Vendor invoice details</span></span>

<span data-ttu-id="bf32e-243">Pokud chcete navrhnout stránky podrobností faktury pro mobilní zařízení, použijte stránku **VendMobileInvoiceHeaderDetails** v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bf32e-243">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page in Finance and Operations.</span></span> <span data-ttu-id="bf32e-244">Všimněte si, že v závislosti na počtu faktur, které máte v systému, tato stránka zobrazuje nejstarší faktury (faktura, která byla vytvořena jako první).</span><span class="sxs-lookup"><span data-stu-id="bf32e-244">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="bf32e-245">Pokud chcete najít konkrétní fakturu, můžete použít filtr vlevo.</span><span class="sxs-lookup"><span data-stu-id="bf32e-245">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="bf32e-246">Nevyžadujeme ale použití konkrétní faktury pro tento příklad.</span><span class="sxs-lookup"><span data-stu-id="bf32e-246">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="bf32e-247">Vyžadujeme pouze některá data faktury, abychom mohli navrhnout mobilní stránku.</span><span class="sxs-lookup"><span data-stu-id="bf32e-247">We just require some invoice data so that we can design the mobile page.</span></span> <span data-ttu-id="bf32e-248">[![Stránka workflowu](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="bf32e-248">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1.  <span data-ttu-id="bf32e-249">V adrese URL Finance and Operations nahraďte název položky nabídky názvem **VendMobileInvoiceHeaderDetails** k otevření formuláře</span><span class="sxs-lookup"><span data-stu-id="bf32e-249">In the Finance and Operations URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>
2.  <span data-ttu-id="bf32e-250">Otevřete mobilní návrhář z tlačítka **Nastavení** (ozubené kolečko).</span><span class="sxs-lookup"><span data-stu-id="bf32e-250">Open the mobile designer from the **Settings** (gear) button.</span></span>
3.  <span data-ttu-id="bf32e-251">Kliknutím na tlačítko **Upravit** spusťte režim úprav v pracovním prostoru.</span><span class="sxs-lookup"><span data-stu-id="bf32e-251">Click the **Edit** button to start edit mode in the workspace.</span></span>
4.  <span data-ttu-id="bf32e-252">Vyberte stránku **Moje faktury dodavatele**, kterou jste dříve vytvořili, a potom klepněte na tlačítko **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-252">Select the **My vendor invoices **page that you created earlier, and then click **Edit**.</span></span>
5.  <span data-ttu-id="bf32e-253">Na kartě **Pole** klikněte na záhlaví sloupce **Mřížka**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-253">On the **Fields** tab, click the **Grid** column heading.</span></span>
6.  <span data-ttu-id="bf32e-254">Klikněte na **Vlastnosti** &gt; **Přidat stránku**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-254">Click **Properties** &gt; **Add page**.</span></span> <span data-ttu-id="bf32e-255">**Poznámka:** Po klepnutí na záhlaví **Mřížka** a přidání stránky je automaticky navázán vztah.</span><span class="sxs-lookup"><span data-stu-id="bf32e-255">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>
7.  <span data-ttu-id="bf32e-256">Zadejte název stránky, například **Detaily faktury** a popis, jako například **Zobrazení záhlaví faktury a podrobností řádku**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-256">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>
8.  <span data-ttu-id="bf32e-257">Klikněte na **Vybrat pole**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-257">Click **Select fields**.</span></span> <span data-ttu-id="bf32e-258">Všimněte si, že pořadí, ve kterém přidáváte, je pořadí, ve kterém se pole zobrazí koncovému uživateli.</span><span class="sxs-lookup"><span data-stu-id="bf32e-258">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="bf32e-259">Jediný způsob, jak změnit pořadí polí, je opětovný výběr všech polí.</span><span class="sxs-lookup"><span data-stu-id="bf32e-259">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 
9.  <span data-ttu-id="bf32e-260">Na základě požadavků pro tento scénář přidejte následující pole ze záhlaví:</span><span class="sxs-lookup"><span data-stu-id="bf32e-260">Add the following fields from the header, based on the requirements for this scenario:</span></span>
    - <span data-ttu-id="bf32e-261">Název dodavatele</span><span class="sxs-lookup"><span data-stu-id="bf32e-261">Vendor name</span></span>
    - <span data-ttu-id="bf32e-262">Faktura celkem</span><span class="sxs-lookup"><span data-stu-id="bf32e-262">Invoice total</span></span>
    - <span data-ttu-id="bf32e-263">Účet faktury</span><span class="sxs-lookup"><span data-stu-id="bf32e-263">Invoice account</span></span>
    - <span data-ttu-id="bf32e-264">Číslo faktury</span><span class="sxs-lookup"><span data-stu-id="bf32e-264">Invoice number</span></span>
    - <span data-ttu-id="bf32e-265">Datum fakturace</span><span class="sxs-lookup"><span data-stu-id="bf32e-265">Invoice date</span></span>
    - <span data-ttu-id="bf32e-266">Popis faktury</span><span class="sxs-lookup"><span data-stu-id="bf32e-266">Invoice description</span></span>
    - <span data-ttu-id="bf32e-267">Datum splatnosti</span><span class="sxs-lookup"><span data-stu-id="bf32e-267">Due date</span></span>
    - <span data-ttu-id="bf32e-268">Měna faktury</span><span class="sxs-lookup"><span data-stu-id="bf32e-268">Invoice currency</span></span>

10. <span data-ttu-id="bf32e-269">Z řádků mřížky na stránce přidejte následující pole:</span><span class="sxs-lookup"><span data-stu-id="bf32e-269">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="bf32e-270">Kategorie zásobování</span><span class="sxs-lookup"><span data-stu-id="bf32e-270">Procurement category</span></span>
    - <span data-ttu-id="bf32e-271">Množství</span><span class="sxs-lookup"><span data-stu-id="bf32e-271">Quantity</span></span>
    - <span data-ttu-id="bf32e-272">Jedn. cena</span><span class="sxs-lookup"><span data-stu-id="bf32e-272">Unit price</span></span>
    - <span data-ttu-id="bf32e-273">Čistá částka řádku</span><span class="sxs-lookup"><span data-stu-id="bf32e-273">Line net amount</span></span>
    - <span data-ttu-id="bf32e-274">Částka sestavy 1099</span><span class="sxs-lookup"><span data-stu-id="bf32e-274">1099 amount</span></span>

11. <span data-ttu-id="bf32e-275">Po přidání všech polí z předchozích dvou kroků klepněte na **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-275">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="bf32e-276">Stránka musí vypadat podobně jako na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="bf32e-276">The page must resemble the following illustration.</span></span>
<span data-ttu-id="bf32e-277">[![Stránka po přidání polí](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="bf32e-277">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>
12. <span data-ttu-id="bf32e-278">Kliknutím na **Hotovo** ukončete režim úprav.</span><span class="sxs-lookup"><span data-stu-id="bf32e-278">Click **Done** to exit edit mode.</span></span>
13. <span data-ttu-id="bf32e-279">Klikněte na **Zpět** a potom na **Hotovo** pro odchod z pracovního prostoru</span><span class="sxs-lookup"><span data-stu-id="bf32e-279">Click **Back** and then **Done** to exit the workspace</span></span>
14. <span data-ttu-id="bf32e-280">Kliknutím na **Publikovat pracovní prostor** uložte práci.</span><span class="sxs-lookup"><span data-stu-id="bf32e-280">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="bf32e-281">Akce workflowu</span><span class="sxs-lookup"><span data-stu-id="bf32e-281">Workflow actions</span></span>

<span data-ttu-id="bf32e-282">Chcete-li přidat akce pracovního postupu, použijte stránku **VendMobileInvoiceHeaderDetails** v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bf32e-282">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page in Finance and Operations.</span></span> <span data-ttu-id="bf32e-283">Chcete-li tuto stránku otevřít, nahraďte název položky nabídky v adrese URL, stejně jako dříve.</span><span class="sxs-lookup"><span data-stu-id="bf32e-283">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="bf32e-284">Pak otevřete mobilní návrhář z tlačítka **Nastavení** (ozubené kolečko).</span><span class="sxs-lookup"><span data-stu-id="bf32e-284">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="bf32e-285">Chcete-li přidat akce workflowu na stránce Podrobnosti, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="bf32e-285">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="bf32e-286">Musíte mít přiřazené faktury, které jsou v odpovídajícím stavu, abyste mohli provádět dostupné akce pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="bf32e-286">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="bf32e-287">Záznam akcí pracovního postupu</span><span class="sxs-lookup"><span data-stu-id="bf32e-287">Record workflow actions</span></span>
1.  <span data-ttu-id="bf32e-288">Kliknutím na tlačítko **Upravit** spusťte režim úprav v pracovním prostoru.</span><span class="sxs-lookup"><span data-stu-id="bf32e-288">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="bf32e-289">Vyberte stránku **Podrobnosti o faktuře** , kterou jste dříve vytvořili, a potom klepněte na tlačítko **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-289">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="bf32e-290">Na kartě **Akce** klikněte na **Přidat akci**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-290">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="bf32e-291">Zadejte název akce, jako například **Schválit** a popis jako například **Schválit fakturu**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-291">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="bf32e-292">Všimněte si, že změní název akce, kterou zde zadáte, na název akce, která se zobrazí uživateli v mobilní aplikaci.</span><span class="sxs-lookup"><span data-stu-id="bf32e-292">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="bf32e-293">Klepněte na tlačítko **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-293">Click **Done**.</span></span>
6.  <span data-ttu-id="bf32e-294">Klikněte na **Vybrat pole**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-294">Click **Select fields**.</span></span>
7.  <span data-ttu-id="bf32e-295">V procesu pracovního postupu, přejděte an stránku **VendMobileInvoiceHeaderDetails** a proveďte akci, kterou chcete nahrát.</span><span class="sxs-lookup"><span data-stu-id="bf32e-295">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="bf32e-296">Zadejte komentáře pracovního postupu během tohoto procesu tak, aby pole komentáře bylo také součástí mobilního prostředí.</span><span class="sxs-lookup"><span data-stu-id="bf32e-296">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="bf32e-297">Po spuštění akce pracovního postupu klepněte na **Hotovo** k dokončení úkolu Vybrat pole.</span><span class="sxs-lookup"><span data-stu-id="bf32e-297">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="bf32e-298">Kliknutím na **Hotovo** ukončete režim úprav.</span><span class="sxs-lookup"><span data-stu-id="bf32e-298">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="bf32e-299">Klikněte na **Zpět** a potom na **Hotovo** pro odchod z pracovního prostoru</span><span class="sxs-lookup"><span data-stu-id="bf32e-299">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="bf32e-300">Kliknutím na **Publikovat pracovní prostor** uložte práci.</span><span class="sxs-lookup"><span data-stu-id="bf32e-300">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="bf32e-301">Opakujte předchozí kroky k zaznamenání všech požadovaných akcí pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="bf32e-301">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="bf32e-302">Vytvoření souboru .js</span><span class="sxs-lookup"><span data-stu-id="bf32e-302">Create a .js file</span></span>
1. <span data-ttu-id="bf32e-303">Otevřete Poznámkový blok nebo Microsoft Visual Studio a vložte následující kód.</span><span class="sxs-lookup"><span data-stu-id="bf32e-303">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="bf32e-304">Uložit soubor jako soubor .js</span><span class="sxs-lookup"><span data-stu-id="bf32e-304">Save the file as a .js file.</span></span> <span data-ttu-id="bf32e-305">Tento kód provádí následující úkony:</span><span class="sxs-lookup"><span data-stu-id="bf32e-305">This code does the following:</span></span>
    - <span data-ttu-id="bf32e-306">Skryje sloupce týkající se pracovního postupu, které jsou navíc a které jsme přidali dříve na stránce Mobilní seznam.</span><span class="sxs-lookup"><span data-stu-id="bf32e-306">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="bf32e-307">Můžeme přidat tyto sloupce tak, aby aplikace měla tyto informace v kontextu a provést další krok.</span><span class="sxs-lookup"><span data-stu-id="bf32e-307">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="bf32e-308">Podle kroku pracovního postupu, který je aktivní, použije logiku, aby se zobrazily pouze akce.</span><span class="sxs-lookup"><span data-stu-id="bf32e-308">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

> [!NOTE]
> <span data-ttu-id="bf32e-309">Všimněte si, že název stránky a další ovládací prvky v kódu musí být stejné jako názvy v pracovním prostoru.</span><span class="sxs-lookup"><span data-stu-id="bf32e-309">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }

2.  <span data-ttu-id="bf32e-310">Nahrajte kód souboru do pracovního prostoru výběrem karty **Logika**</span><span class="sxs-lookup"><span data-stu-id="bf32e-310">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="bf32e-311">Kliknutím na **Hotovo** ukončete režim úprav.</span><span class="sxs-lookup"><span data-stu-id="bf32e-311">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="bf32e-312">Klikněte na **Zpět** a potom na **Hotovo** pro odchod z pracovního prostoru</span><span class="sxs-lookup"><span data-stu-id="bf32e-312">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="bf32e-313">Kliknutím na **Publikovat pracovní prostor** uložte práci.</span><span class="sxs-lookup"><span data-stu-id="bf32e-313">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="bf32e-314">Přílohy faktury dodavatele</span><span class="sxs-lookup"><span data-stu-id="bf32e-314">Vendor invoice attachments</span></span>

1.  <span data-ttu-id="bf32e-315">Klikněte na tlačítko **Nastavení** (ozubené kolo) v pravém horním rohu stránky, a pak klikněte na **Mobilní aplikace**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-315">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
2.  <span data-ttu-id="bf32e-316">Kliknutím na tlačítko **Upravit** spusťte režim úprav v pracovním prostoru.</span><span class="sxs-lookup"><span data-stu-id="bf32e-316">Click the **Edit** button to start edit mode in the workspace.</span></span>
3.  <span data-ttu-id="bf32e-317">Vyberte stránku **Podrobnosti o faktuře**, kterou jste dříve vytvořili, a potom klepněte na tlačítko **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-317">Select the **Invoice details **page that you created earlier, and then click **Edit**.</span></span>
4.  <span data-ttu-id="bf32e-318">Nastavte možnost **Správa dokumentů** na **Ano**, jak je ukázáno níže.</span><span class="sxs-lookup"><span data-stu-id="bf32e-318">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="bf32e-319">**Poznámka:** Pokud neexistují žádné požadavky na mobilním zařízení, můžete nechat tuto možnost nastavenou na **Ne**, což je výchozí nastavení.</span><span class="sxs-lookup"><span data-stu-id="bf32e-319">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
<span data-ttu-id="bf32e-320">![Správa dokumentů](./media/docmanagement-216x300.png)</span><span class="sxs-lookup"><span data-stu-id="bf32e-320">![Document management](./media/docmanagement-216x300.png)</span></span>
6.  <span data-ttu-id="bf32e-321">Kliknutím na **Hotovo** ukončete režim úprav.</span><span class="sxs-lookup"><span data-stu-id="bf32e-321">Click **Done** to exit edit mode.</span></span>
7.  <span data-ttu-id="bf32e-322">Klikněte na **Zpět** a potom na **Hotovo** pro odchod z pracovního prostoru</span><span class="sxs-lookup"><span data-stu-id="bf32e-322">Click **Back** and then **Done** to exit the workspace</span></span>
8.  <span data-ttu-id="bf32e-323">Kliknutím na **Publikovat pracovní prostor** uložte práci.</span><span class="sxs-lookup"><span data-stu-id="bf32e-323">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="bf32e-324">Distribuce řádky faktury dodavatele</span><span class="sxs-lookup"><span data-stu-id="bf32e-324">Vendor invoice line distributions</span></span>

<span data-ttu-id="bf32e-325">Požadavky pro tento scénář potvrzují, že budou existovat pouze distribuce na úrovni řádku a faktura bude mít vždy pouze jeden řádek.</span><span class="sxs-lookup"><span data-stu-id="bf32e-325">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="bf32e-326">Vzhledem k tomu, že tento scénář je jednoduchý, musí být natolik jednoduché, že uživatel nemusí zobrazit podrobnosti k zobrazení distribucí několik úrovní uživatelského prostředí na mobilním zařízení.</span><span class="sxs-lookup"><span data-stu-id="bf32e-326">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="bf32e-327">Faktury dodavatele v aplikaci Finance and Operations zahrnují možnost zobrazení všech distribucí z hlavičky faktury.</span><span class="sxs-lookup"><span data-stu-id="bf32e-327">Vendor invoices in Finance and Operations include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="bf32e-328">Toto prostředí potřebujeme pro mobilní scénář.</span><span class="sxs-lookup"><span data-stu-id="bf32e-328">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="bf32e-329">Proto použijeme stránku **VendMobileInvoiceAllDistributionTree** k navržení této části mobilního scénáře.</span><span class="sxs-lookup"><span data-stu-id="bf32e-329">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="bf32e-330">Znalost požadavků nám pomáhá určit, které konkrétní stránky používat a jak přesně optimalizovat mobilní prostředí pro uživatele, když navrhujeme scénář.</span><span class="sxs-lookup"><span data-stu-id="bf32e-330">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="bf32e-331">Ve druhém scénáři použijeme jinou stránku k zobrazení rozúčtování, protože se liší požadavky pro tento scénář.</span><span class="sxs-lookup"><span data-stu-id="bf32e-331">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="bf32e-332">V adrese URL nahraďte název položky nabídky jako předtím.</span><span class="sxs-lookup"><span data-stu-id="bf32e-332">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="bf32e-333">Stránky, které se objeví, by měly vypadat jako na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="bf32e-333">The page that appears should resemble the following illustration.</span></span>
<span data-ttu-id="bf32e-334">[![Stránka Všechny distribuce](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="bf32e-334">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>
2.  <span data-ttu-id="bf32e-335">Otevřete mobilní návrhář z tlačítka **Nastavení** (ozubené kolečko).</span><span class="sxs-lookup"><span data-stu-id="bf32e-335">Open the mobile designer from the **Settings** (gear) button.</span></span>
3.  <span data-ttu-id="bf32e-336">Kliknutím na tlačítko **Upravit** spusťte režim úprav v pracovním prostoru.</span><span class="sxs-lookup"><span data-stu-id="bf32e-336">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="bf32e-337">**Poznámka:** uvidíte, že byly automaticky vytvořeny dvě nové stránky.</span><span class="sxs-lookup"><span data-stu-id="bf32e-337">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="bf32e-338">Systém vytvoří tyto stránky, protože jste v předchozí části aktivovali správu dokumentů.</span><span class="sxs-lookup"><span data-stu-id="bf32e-338">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="bf32e-339">Tyto nové stránky můžete ignorovat.</span><span class="sxs-lookup"><span data-stu-id="bf32e-339">You can ignore these new pages.</span></span>
4.  <span data-ttu-id="bf32e-340">Klikněte na **Přidat stránku**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-340">Click **Add page**.</span></span>
5.  <span data-ttu-id="bf32e-341">Zadejte název stránky, například **zobrazení účetních** a popis, jako například **zobrazení účtování faktury**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-341">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>
6.  <span data-ttu-id="bf32e-342">Klepněte na tlačítko **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-342">Click **Done**.</span></span>
7.  <span data-ttu-id="bf32e-343">Na kartě **Pole** klikněte na **Vybrat pole**, ze stránek distribuce vyberte následující pole a potom klepněte na tlačítko **Hotovo**:</span><span class="sxs-lookup"><span data-stu-id="bf32e-343">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="bf32e-344">Částka</span><span class="sxs-lookup"><span data-stu-id="bf32e-344">Amount</span></span>
    2.  <span data-ttu-id="bf32e-345">Měna</span><span class="sxs-lookup"><span data-stu-id="bf32e-345">Currency</span></span>
    3.  <span data-ttu-id="bf32e-346">Účet hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="bf32e-346">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="bf32e-347">Nevybrali jsme slupec **Popis** z mřížky distribuce, protože požadavky pro tento scénář potvrdily, že výsledná cena je jediná částka, pro kterou bude existovat rozúčtování.</span><span class="sxs-lookup"><span data-stu-id="bf32e-347">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="bf32e-348">Uživatel proto nebude vyžadovat další pole k určení typu částky, pro niž je distribuce určená.</span><span class="sxs-lookup"><span data-stu-id="bf32e-348">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="bf32e-349">V dalším scénáři však **budeme** tyto informace používat, protože požadavky na tuto situaci určují, že jiné typy částek mají rozdělení (například DPH).</span><span class="sxs-lookup"><span data-stu-id="bf32e-349">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>
8.  <span data-ttu-id="bf32e-350">Kliknutím na **Hotovo** ukončete režim úprav.</span><span class="sxs-lookup"><span data-stu-id="bf32e-350">Click **Done** to exit edit mode.</span></span>
9.  <span data-ttu-id="bf32e-351">Klikněte na **Zpět** a potom na **Hotovo** pro odchod z pracovního prostoru</span><span class="sxs-lookup"><span data-stu-id="bf32e-351">Click **Back** and then **Done** to exit the workspace</span></span>
10. <span data-ttu-id="bf32e-352">Kliknutím na **Publikovat pracovní prostor** uložte práci.</span><span class="sxs-lookup"><span data-stu-id="bf32e-352">Click **Publish workspace** to save your work</span></span>

> [!NOTE] 
> <span data-ttu-id="bf32e-353">Mobilní stránka **Zobrazení účetnictví** není momentálně propojena s žádnou z mobilních stránek, které jsme doposud vytvořili.</span><span class="sxs-lookup"><span data-stu-id="bf32e-353">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="bf32e-354">Protože by měl uživatel být schopen přejít na stránku **zobrazení účetnictví** stránky ze stránky **Detaily faktury** na mobilním zařízení, musíme poskytnout navigaci ze stránky **Detaily faktury** na stránku **Zobrazit účetnictví**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-354">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="bf32e-355">Můžeme navázat tuto navigaci pomocí další logiky pomocí jazyka JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bf32e-355">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="bf32e-356">Otevřete soubor .js, který jste vytvořili dříve a přidejte zvýrazněné řádky v následujícím kódu.</span><span class="sxs-lookup"><span data-stu-id="bf32e-356">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="bf32e-357">Tento kód provádí dvě věci:</span><span class="sxs-lookup"><span data-stu-id="bf32e-357">This code does two things:</span></span>
    1.  <span data-ttu-id="bf32e-358">Pomáhá zajistit, že uživatelé nebudou moci přejít přímo z pracovního prostor na stránku **Zobrazení účtování**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-358">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="bf32e-359">Naváže ovládání navigace ze stránky **Detaily faktury** na stránku **Zobrazení účetnictví**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-359">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

> [!NOTE] 
> <span data-ttu-id="bf32e-360">Všimněte si, že název stránky a další ovládací prvky v kódu musí být stejné jako názvy v pracovním prostoru.</span><span class="sxs-lookup"><span data-stu-id="bf32e-360">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }

2.  <span data-ttu-id="bf32e-361">Nahrajte kód souboru do pracovního prostoru výběrem karty **Logika** pro přepis předchozího kódu</span><span class="sxs-lookup"><span data-stu-id="bf32e-361">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="bf32e-362">Kliknutím na **Hotovo** ukončete režim úprav.</span><span class="sxs-lookup"><span data-stu-id="bf32e-362">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="bf32e-363">Klikněte na **Zpět** a potom na **Hotovo** pro odchod z pracovního prostoru</span><span class="sxs-lookup"><span data-stu-id="bf32e-363">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="bf32e-364">Kliknutím na **Publikovat pracovní prostor** uložte práci.</span><span class="sxs-lookup"><span data-stu-id="bf32e-364">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="bf32e-365">Ověření</span><span class="sxs-lookup"><span data-stu-id="bf32e-365">Validation</span></span>

<span data-ttu-id="bf32e-366">Z mobilního zařízení otevřete aplikace a připojte se k vaší instanci aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bf32e-366">From your mobile device, open the app, and connect to your Finance and Operations instance.</span></span> <span data-ttu-id="bf32e-367">Ujistěte se, že jste přihlášení se do společnosti, kde vám byly faktury dodavatele přiřazeny k revizi.</span><span class="sxs-lookup"><span data-stu-id="bf32e-367">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="bf32e-368">Je třeba provést následující akce:</span><span class="sxs-lookup"><span data-stu-id="bf32e-368">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="bf32e-369">Viz pracovní prostor **Moje schválení**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-369">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="bf32e-370">Přejděte do pracovního prostoru **Moje schválení** a zobrazte stránku **Moje faktury dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-370">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="bf32e-371">Přejděte k podrobnostem na stránce **Moje faktury dodavatele** a zobrazte seznam faktur, které vám byly přiřazeny.</span><span class="sxs-lookup"><span data-stu-id="bf32e-371">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="bf32e-372">přejděte na podrobnosti jedné z faktu a zobrazte podrobnosti faktury záhlaví a podrobností řádků.</span><span class="sxs-lookup"><span data-stu-id="bf32e-372">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="bf32e-373">Na stránce Podrobnosti viz odkaz na přílohy a pomocí tohoto odkazu můžete přejít na seznam příloh a přílohy zobrazit.</span><span class="sxs-lookup"><span data-stu-id="bf32e-373">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="bf32e-374">na stránce podrobností zobrazte odkaz na stránku **Zobrazit účetnictví**  a pomocí tohoto odkazu můžete přejít na seznam příloh a přílohy zobrazit.</span><span class="sxs-lookup"><span data-stu-id="bf32e-374">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="bf32e-375">Na stránce Podrobnosti klepněte na nabídku **akce** a proveďte akce pracovního postupu, které jsou použitelné pro krok pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="bf32e-375">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="bf32e-376">Návrh scénáře schválení složité faktury pro společnosti Fabrikam</span><span class="sxs-lookup"><span data-stu-id="bf32e-376">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf32e-377">Atribut scénáře</span><span class="sxs-lookup"><span data-stu-id="bf32e-377">Scenario attribute</span></span></th>
<th><span data-ttu-id="bf32e-378">Odpověď</span><span class="sxs-lookup"><span data-stu-id="bf32e-378">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bf32e-379">Která pole z hlavičky faktury bude uživatel chtít vidět v mobilním prostředí a v jakém pořadí?</span><span class="sxs-lookup"><span data-stu-id="bf32e-379">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="bf32e-380">Název dodavatele</span><span class="sxs-lookup"><span data-stu-id="bf32e-380">Vendor name</span></span></li>
<li><span data-ttu-id="bf32e-381">Fakturovaná částka</span><span class="sxs-lookup"><span data-stu-id="bf32e-381">Invoice amount</span></span></li>
<li><span data-ttu-id="bf32e-382">Účet faktury</span><span class="sxs-lookup"><span data-stu-id="bf32e-382">Invoice account</span></span></li>
<li><span data-ttu-id="bf32e-383">Číslo faktury</span><span class="sxs-lookup"><span data-stu-id="bf32e-383">Invoice number</span></span></li>
<li><span data-ttu-id="bf32e-384">Datum fakturace</span><span class="sxs-lookup"><span data-stu-id="bf32e-384">Invoice date</span></span></li>
<li><span data-ttu-id="bf32e-385">Popis faktury</span><span class="sxs-lookup"><span data-stu-id="bf32e-385">Invoice description</span></span></li>
<li><span data-ttu-id="bf32e-386">Datum splatnosti</span><span class="sxs-lookup"><span data-stu-id="bf32e-386">Due date</span></span></li>
<li><span data-ttu-id="bf32e-387">Měna faktury</span><span class="sxs-lookup"><span data-stu-id="bf32e-387">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf32e-388">Která pole z řádek faktury bude uživatel chtít vidět v mobilního prostředí a v jakém pořadí?</span><span class="sxs-lookup"><span data-stu-id="bf32e-388">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="bf32e-389">Kategorie zásobování</span><span class="sxs-lookup"><span data-stu-id="bf32e-389">Procurement category</span></span></li>
<li><span data-ttu-id="bf32e-390">Množství</span><span class="sxs-lookup"><span data-stu-id="bf32e-390">Quantity</span></span></li>
<li><span data-ttu-id="bf32e-391">Jedn. cena</span><span class="sxs-lookup"><span data-stu-id="bf32e-391">Unit price</span></span></li>
<li><span data-ttu-id="bf32e-392">Čistá částka řádku</span><span class="sxs-lookup"><span data-stu-id="bf32e-392">Line net amount</span></span></li>
<li><span data-ttu-id="bf32e-393">Částka sestavy 1099</span><span class="sxs-lookup"><span data-stu-id="bf32e-393">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf32e-394">Kolik má faktura řádků?</span><span class="sxs-lookup"><span data-stu-id="bf32e-394">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="bf32e-395">Uplatněte zde pravidlo 80-20 a optimalizujte pro 80 procent.</span><span class="sxs-lookup"><span data-stu-id="bf32e-395">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="bf32e-396">5</span><span class="sxs-lookup"><span data-stu-id="bf32e-396">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf32e-397">Budou uživatelé chtít vidět rozúčtování (kódování faktury) v mobilním zařízení během kontrol?</span><span class="sxs-lookup"><span data-stu-id="bf32e-397">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="bf32e-398">Ano</span><span class="sxs-lookup"><span data-stu-id="bf32e-398">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf32e-399">Kolik rozúčtování (rozšířená cena, DPH, poplatky atd.) je pro řádek faktury k dispozici?</span><span class="sxs-lookup"><span data-stu-id="bf32e-399">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="bf32e-400">Znovu použijte pravidlo 80-20.</span><span class="sxs-lookup"><span data-stu-id="bf32e-400">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="bf32e-401">Rozšířená cena: 2 DPH 2: 2 Poplatky: 2</span><span class="sxs-lookup"><span data-stu-id="bf32e-401">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf32e-402">Mají faktury také rozúčtování v hlavičce faktury?</span><span class="sxs-lookup"><span data-stu-id="bf32e-402">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="bf32e-403">Pokud ano, budou tato rozúčtování k dispozici v zařízení?</span><span class="sxs-lookup"><span data-stu-id="bf32e-403">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="bf32e-404">Nepoužito</span><span class="sxs-lookup"><span data-stu-id="bf32e-404">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf32e-405">Budou uživatelé chtít vidět přílohy pro fakturu na zařízení?</span><span class="sxs-lookup"><span data-stu-id="bf32e-405">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="bf32e-406">Ano</span><span class="sxs-lookup"><span data-stu-id="bf32e-406">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="bf32e-407">Další kroky</span><span class="sxs-lookup"><span data-stu-id="bf32e-407">Next steps</span></span>

<span data-ttu-id="bf32e-408">Tyto změny lze provést pro scénář 1, na základě požadavků pro scénář 2.</span><span class="sxs-lookup"><span data-stu-id="bf32e-408">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="bf32e-409">Informace v této části slouží k vylepšení zkušenosti mobilní aplikace.</span><span class="sxs-lookup"><span data-stu-id="bf32e-409">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="bf32e-410">Vzhledem k tomu, že další řádky faktury jsou očekávány ve scénáři 2, následující změny návrhu vám pomohou optimalizovat uživatelské prostředí na mobilním zařízení:</span><span class="sxs-lookup"><span data-stu-id="bf32e-410">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="bf32e-411">Místo zobrazení řádků faktury na stránce Podrobnosti (jako v scénáři 1), mohou uživatelé zobrazit řádky na samostatné mobilní stránce.</span><span class="sxs-lookup"><span data-stu-id="bf32e-411">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="bf32e-412">Vzhledem k tomu, že v tomto případě se očekává více než jeden řádek faktury, pokud je použita stránka **VendMobileInvoiceAllDistributionTree** k vytvoření stránky distribucí pro mobilní telefon (jako v scénáři 1), může být matoucí pro uživatele při korelaci na rozdělování řádků.</span><span class="sxs-lookup"><span data-stu-id="bf32e-412">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="bf32e-413">Proto k návrhu stránek distribuce použijte stránku **VendMobileInvoiceLineDistributionTree**.</span><span class="sxs-lookup"><span data-stu-id="bf32e-413">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="bf32e-414">V ideálním případě by rozdělení v tomto scénáři měla zobrazovat v kontextu řádku faktury.</span><span class="sxs-lookup"><span data-stu-id="bf32e-414">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="bf32e-415">Proto se ujistěte, že uživatel může přejít k podrobnostem řádky, aby viděl stránku distribuce.</span><span class="sxs-lookup"><span data-stu-id="bf32e-415">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="bf32e-416">Použijte možnost odkazu stránky k navázat procházení na detaily, stejně jako u stránek záhlaví a podrobností v scénáři 1.</span><span class="sxs-lookup"><span data-stu-id="bf32e-416">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="bf32e-417">Vzhledem k tomu, že na rozdělení v scénáři 2 (prodejní daně, poplatky a tak dále) se očekává více než jeden typ částky, je užitečné zobrazit popis typu Částka.</span><span class="sxs-lookup"><span data-stu-id="bf32e-417">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="bf32e-418">(Tyto informace jsme v scénáři 1 vynechali).</span><span class="sxs-lookup"><span data-stu-id="bf32e-418">(We omitted this information in scenario 1.)</span></span>





