---
title: "Dokumenty odůvodnění plánování budgetu"
description: "Dokumenty odůvodnění poskytují komentáře pro osoby požadující rozpočet k vysvětlení, proč je konkrétní rozpočet nezbytný."
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b38050e8a792622b772882ec4a0cddce8661a720
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="budget-planning-justification-documents"></a><span data-ttu-id="460db-103">Dokumenty odůvodnění plánování budgetu</span><span class="sxs-lookup"><span data-stu-id="460db-103">Budget planning justification documents</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="460db-104">Dokumenty odůvodnění poskytují komentáře pro osoby požadující rozpočet k vysvětlení, proč je konkrétní rozpočet nezbytný.</span><span class="sxs-lookup"><span data-stu-id="460db-104">Justification documents provide a narrative for those requesting a budget to explain why a specific budget is necessary.</span></span> 

<span data-ttu-id="460db-105">Šablona plánu rozpočtu se vytváří správcem rozpočtu v aplikaci Microsoft Word a přiřazuje se k aktuálnímu procesu plánování rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="460db-105">A budget plan template is created by the budget manager in Microsoft Word and assigned to the current budget planning process.</span></span> <span data-ttu-id="460db-106">Vlastníci rozpočtu mohou potom otevřít šablonu a data v aplikaci Word se automaticky vyplní na základě jejich žádosti o rozpočet.</span><span class="sxs-lookup"><span data-stu-id="460db-106">Budget owners can then open the template and have data automatically populated in Word based on their budget request.</span></span> <span data-ttu-id="460db-107">Mohou poté přidat další text nebo data před uložením a přiložením svého přizpůsobeného dokumentu odůvodnění k plánu rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="460db-107">They can then add additional text or data prior to saving and attaching their personalized justification document to their budget plan.</span></span>

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a><span data-ttu-id="460db-108">Nastavení doplňku Microsoft Dynamics Office pro Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="460db-108">Set up Microsoft Dynamics Office Add-in for Microsoft Word</span></span>

1.  <span data-ttu-id="460db-109">Otevřete nový dokument aplikace Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="460db-109">Open a new Microsoft Word document.</span></span>
2.  <span data-ttu-id="460db-110">Klikněte na tlačítko **Vložit** na pásu karet a klikněte na **Obchod**.</span><span class="sxs-lookup"><span data-stu-id="460db-110">Click **Insert** on the ribbon, and click **Store**.</span></span>
3.  <span data-ttu-id="460db-111">Vyhledejte doplněk Microsoft Dynamics Office a klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="460db-111">Search for Microsoft Dynamics Office Add-in and click **Add**.</span></span>
4.  <span data-ttu-id="460db-112">V aplikaci Word klikněte v pravém podokně na možnost **Přidat informace serveru**.</span><span class="sxs-lookup"><span data-stu-id="460db-112">In Word, in the right pane, click **Add server information**.</span></span>
5.  <span data-ttu-id="460db-113">Zadejte nebo vložte adresu URL serveru a klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="460db-113">Type or paste the server URL and click **OK**.</span></span>

##### <a name="define-the-justification-template-in-microsoft-word"></a><span data-ttu-id="460db-114">Definování šablony odůvodnění v aplikaci Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="460db-114">Define the Justification template in Microsoft Word</span></span>

1.  <span data-ttu-id="460db-115">Klikněte na tlačítko **Návrh** v doplňku Microsoft Dynamics Office poté, co se přihlásíte.</span><span class="sxs-lookup"><span data-stu-id="460db-115">Click **Design** in the Microsoft Dynamics Office Add-in after you’ve logged in.</span></span>
2.  <span data-ttu-id="460db-116">Pro informace záhlaví použijte tlačítko **Přidat pole**.</span><span class="sxs-lookup"><span data-stu-id="460db-116">For header information, use the **Add fields** button.</span></span>
3.  <span data-ttu-id="460db-117">Vyberte zdroj dat entity BudgetPlanJustification a klikněte na **Další**.</span><span class="sxs-lookup"><span data-stu-id="460db-117">Select the entity data source of BudgetPlanJustification, and click **Next**.</span></span> <span data-ttu-id="460db-118">**Poznámka:** Tato entita je vyžadována pro každý dokument odůvodnění.</span><span class="sxs-lookup"><span data-stu-id="460db-118">**Note:** This entity is required for any justification document.</span></span> <span data-ttu-id="460db-119">Ostatní entity lze použít, ale odeslání zpět do aplikace Microsoft Dynamics 365 for Finance and Operations se nezdaří, pokud není tato entita zahrnuta.</span><span class="sxs-lookup"><span data-stu-id="460db-119">Other entities can be used but the upload back to Microsoft Dynamics 365 for Finance and Operations will fail if this entity isn’t included.</span></span>
4.  <span data-ttu-id="460db-120">Přidejte popisky BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter a DocumentNumber do dokumentu aplikace Word.</span><span class="sxs-lookup"><span data-stu-id="460db-120">Add the BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter, and DocumentNumber labels and values in the Word document.</span></span> <span data-ttu-id="460db-121">**Poznámka:** V případě potřeby můžete použít vlastní popisky, spíše než standardní popisky.</span><span class="sxs-lookup"><span data-stu-id="460db-121">**Note:** You can use your own custom labels, rather than the standard labels, if needed.</span></span>
5.  <span data-ttu-id="460db-122">Klikněte na **Hotovo** pro dokončení části záhlaví.</span><span class="sxs-lookup"><span data-stu-id="460db-122">Click **Done** to complete the header section.</span></span>
6.  <span data-ttu-id="460db-123">Pro získání podrobností o částkách plánu rozpočtu na úrovni řádků klikněte na tlačítko **Přidat tabulku**.</span><span class="sxs-lookup"><span data-stu-id="460db-123">For line level detail of budget plan amounts, click **Add table**.</span></span>
7.  <span data-ttu-id="460db-124">Znovu vyberte zdroj dat entity BudgetPlanJustification a klikněte na **Další**.</span><span class="sxs-lookup"><span data-stu-id="460db-124">Again, select the entity data source of BudgetPlanJustification, and click **Next**.</span></span>
8.  <span data-ttu-id="460db-125">Přidejte pole pro EffectiveDate, ScenarioName, AccountDisplayValue a AccountingCurrencyExpenseAmount.</span><span class="sxs-lookup"><span data-stu-id="460db-125">Add fields for EffectiveDate, ScenarioName, AccountDisplayValue, and AccountingCurrencyExpenseAmount.</span></span> <span data-ttu-id="460db-126">**Poznámka:** Jsou-li k dispozici komentáře k přidání do jednotlivých řádků plánu rozpočtu, můžete je přidat do tabulky zde.</span><span class="sxs-lookup"><span data-stu-id="460db-126">**Note:** If comments are available to add within individual budget plan lines, those can be added to the table here.</span></span>
9.  <span data-ttu-id="460db-127">Přidejte jakékoliv doplňující pokyny pro koncového uživatele a proveďte jakékoli nezbytné formátování nebo úpravu stylů v dokumentu.</span><span class="sxs-lookup"><span data-stu-id="460db-127">Add any additional instructions to provide to the end user, and perform any necessary formatting or styling to the document.</span></span>
10. <span data-ttu-id="460db-128">Než budete pokračovat, uložte dokument do místního počítače a zavřete soubor.</span><span class="sxs-lookup"><span data-stu-id="460db-128">Save the document to your local computer and close the file before continuing.</span></span>

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a><span data-ttu-id="460db-129">Nastavení procesu plánování rozpočtu pro použití šablony odůvodnění</span><span class="sxs-lookup"><span data-stu-id="460db-129">Set up the Budget planning process to use the Justification template</span></span>

1.  <span data-ttu-id="460db-130">V aplikaci Finance and Operations přejděte na **Rozpočtování** &gt; **Nastavení** &gt; **Plánování rozpočtu** &gt; **Šablony dokumentů odůvodnění**.</span><span class="sxs-lookup"><span data-stu-id="460db-130">In Finance and Operations, go to **Budgeting** &gt; **Setup** &gt; **Budget planning** &gt; **Justification document templates**.</span></span>
2.  <span data-ttu-id="460db-131">Klikněte na tlačítko **Nový** a přejděte do nově vytvořeného dokumentu aplikace Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="460db-131">Click **New** and browse to your newly created Microsoft Word document.</span></span>
3.  <span data-ttu-id="460db-132">Zadejte název a popis zobrazení šablony.</span><span class="sxs-lookup"><span data-stu-id="460db-132">Enter a template display name and description.</span></span> <span data-ttu-id="460db-133">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="460db-133">Click **OK**.</span></span>
4.  <span data-ttu-id="460db-134">Přejděte do **Rozpočtování** &gt; **Nastavení** &gt; **Plánování** **rozpočtu** &gt; **Proces plánování rozpočtu**.</span><span class="sxs-lookup"><span data-stu-id="460db-134">Go to **Budgeting** &gt; **Setup** &gt; **Budget** **planning** &gt; **Budget planning process**.</span></span>
5.  <span data-ttu-id="460db-135">Vyberte proces, kde by měla být použita šablona odůvodnění, a klikněte na tlačítko **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="460db-135">Select the process where the justification template should be used, and click **Edit**.</span></span>
6.  <span data-ttu-id="460db-136">V poli **Šablona dokumentu odůvodnění** vyberte odpovídající šablonu a uložte ji.</span><span class="sxs-lookup"><span data-stu-id="460db-136">In the **Justification document template** field, select the appropriate template and save.</span></span>

##### <a name="edit-and-save-personalized-justification-documents"></a><span data-ttu-id="460db-137">Upravte a uložte přizpůsobené dokumenty odůvodnění.</span><span class="sxs-lookup"><span data-stu-id="460db-137">Edit and save personalized justification documents</span></span>

1.  <span data-ttu-id="460db-138">V aplikaci Finance and Operations vytvořte nový plán rozpočtu nebo otevřete existující plán rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="460db-138">In Finance and Operations, create a new budget plan or open an existing budget plan.</span></span>
2.  <span data-ttu-id="460db-139">V rozevírací nabídce **Odůvodnění** vyberte **Vytvořit nové odůvodnění**.</span><span class="sxs-lookup"><span data-stu-id="460db-139">In the **Justification** drop-down menu, select **Create new justification**.</span></span>
3.  <span data-ttu-id="460db-140">Po vyplnění podrobností vyberte z rozevírací nabídky **Odůvodnění** možnost odeslání přizpůsobeného dokumentu.</span><span class="sxs-lookup"><span data-stu-id="460db-140">After filling in the details, select to upload the personalized document from the **Justification** drop-down menu.</span></span>





