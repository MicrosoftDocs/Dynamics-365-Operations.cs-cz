---
title: Zpracování příjemek výdajů
description: Toto téma obsahuje informace o zpracování příjemky pomocí technologie OCR. Tato funkce je navržena pro zlepšení uživatelského prostředí při vytváření sestav výdajů v aplikaci Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 2e819521828b054f70476b1eb061ee08c486d09f
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113679"
---
# <a name="public-preview-expense-receipt-processing"></a><span data-ttu-id="7c538-104">Veřejná verze Preview: Zpracování příjemek výdajů</span><span class="sxs-lookup"><span data-stu-id="7c538-104">Public Preview: Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


<span data-ttu-id="7c538-105">Zadání výdajů bylo rozšířeno o zavedení zpracování příjemky pomocí technologie OCR.</span><span class="sxs-lookup"><span data-stu-id="7c538-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="7c538-106">Tato funkce je navržena pro zlepšení uživatelského prostředí při vytváření sestav výdajů.</span><span class="sxs-lookup"><span data-stu-id="7c538-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="7c538-107">Klíčové funkce</span><span class="sxs-lookup"><span data-stu-id="7c538-107">Key features</span></span>

- <span data-ttu-id="7c538-108">Název obchodníka, datum a celková částka se extrahují z příjemky.</span><span class="sxs-lookup"><span data-stu-id="7c538-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="7c538-109">Tato funkce se pokusí spárovat nepřipojené příjemky k nepřipojeným výdajovým transakcím.</span><span class="sxs-lookup"><span data-stu-id="7c538-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="7c538-110">Uživatelé mohou vytvářet ručně zadané výdajové transakce z příjemek.</span><span class="sxs-lookup"><span data-stu-id="7c538-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="7c538-111">Příklady použití</span><span class="sxs-lookup"><span data-stu-id="7c538-111">Usage examples</span></span>

- <span data-ttu-id="7c538-112">**Automaticky připojte příjemky, které zahrnují transakce kreditních karet, při vytvoření vyúčtování výdajů.**</span><span class="sxs-lookup"><span data-stu-id="7c538-112">**Automatically attach receipts that include credit card transactions when an expense report is created.**</span></span>

    1. <span data-ttu-id="7c538-113">Otevřete pracovní prostor **Správa výdajů**.</span><span class="sxs-lookup"><span data-stu-id="7c538-113">Open the **Expense management** workspace.</span></span>
    2. <span data-ttu-id="7c538-114">Na kartě **Příjemky** ověřte, zda existují nepřipojené příjemky.</span><span class="sxs-lookup"><span data-stu-id="7c538-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="7c538-115">Na kartě **Příjemky** můžete také odesílat příjemky.</span><span class="sxs-lookup"><span data-stu-id="7c538-115">You can also upload receipts on the **Receipts** tab.</span></span>
    3. <span data-ttu-id="7c538-116">Na kartě **Výdaje** ověřte, zda existují nepřipojené výdaje.</span><span class="sxs-lookup"><span data-stu-id="7c538-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="7c538-117">Správce výdajů obvykle importuje tyto výdaje od zprostředkovatele kreditních karet.</span><span class="sxs-lookup"><span data-stu-id="7c538-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
    4. <span data-ttu-id="7c538-118">Vyberte **Nová sestava výdajů**.</span><span class="sxs-lookup"><span data-stu-id="7c538-118">Select **New expense report**.</span></span> <span data-ttu-id="7c538-119">Všimněte si, že při vytváření vyúčtování výdajů lze nyní rovněž zahrnout výdaje a příjemky.</span><span class="sxs-lookup"><span data-stu-id="7c538-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="7c538-120">Pokud přidáte výdaje i příjemky, bude spuštěno automatické párování příjemek oproti výdajům.</span><span class="sxs-lookup"><span data-stu-id="7c538-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

- <span data-ttu-id="7c538-121">**Vytvořte výdaje nebo spárujte výdaj z příjemky.**</span><span class="sxs-lookup"><span data-stu-id="7c538-121">**Create an expense, or match an expense from a receipt.**</span></span>

    1. <span data-ttu-id="7c538-122">Ve vyúčtování výdajů na kartě **Příjemky** připojte příjemku výběrem možnosti **Přidat příjemky**.</span><span class="sxs-lookup"><span data-stu-id="7c538-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
    2. <span data-ttu-id="7c538-123">V části pod odeslaným obrázkem příjemky si povšimněte možností **Vytvořit** a **Spárovat**.</span><span class="sxs-lookup"><span data-stu-id="7c538-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

        - <span data-ttu-id="7c538-124">Chcete vytvořit ručně zadanou výdajovou transakci a vyplnit hodnoty extrahované z příjemky, vyberte možnost **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="7c538-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
        - <span data-ttu-id="7c538-125">Pokud vyberete možnost **Spárovat**, systém se pokusí spárovat existující výdaj s příjemkou.</span><span class="sxs-lookup"><span data-stu-id="7c538-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="7c538-126">Instalace</span><span class="sxs-lookup"><span data-stu-id="7c538-126">Installation</span></span>

<span data-ttu-id="7c538-127">Tato funkce se používá v kombinaci s funkcí **Sestavy výdajů v nové podobě**, která usnadňuje práci s výdaji.</span><span class="sxs-lookup"><span data-stu-id="7c538-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span>

<span data-ttu-id="7c538-128">Chcete-li používat tyto pokročilé možnosti výdajů, nainstalujte doplněk služby správy výdajů pro Microsoft Dynamics 365 Finance a zapněte funkce ve vaší instanci.</span><span class="sxs-lookup"><span data-stu-id="7c538-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="7c538-129">K doplňku můžete získat přístup z projektu v Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="7c538-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="7c538-130">Přihlaste se k LCS a otevřete požadované prostředí.</span><span class="sxs-lookup"><span data-stu-id="7c538-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="7c538-131">Přejděte na **Úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="7c538-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="7c538-132">Vyberte **Správa** nebo přejděte na pevnou záložku **Doplňky prostředí**.</span><span class="sxs-lookup"><span data-stu-id="7c538-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="7c538-133">Vyberte možnost **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="7c538-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="7c538-134">Vyberte možnost **Služba správy výdajů**.</span><span class="sxs-lookup"><span data-stu-id="7c538-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="7c538-135">Postupujte podle pokynů instalační příručky a vyjádřete souhlas s podmínkami a ujednáními.</span><span class="sxs-lookup"><span data-stu-id="7c538-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="7c538-136">Vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="7c538-136">Select **Install**.</span></span>

<span data-ttu-id="7c538-137">V pracovním prostoru **Správa funkcí** zapněte následující funkce:</span><span class="sxs-lookup"><span data-stu-id="7c538-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="7c538-138">Sestavy výdajů v nové podobě</span><span class="sxs-lookup"><span data-stu-id="7c538-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="7c538-139">Automatická spárovat a vytvořit výdaj z příjemky</span><span class="sxs-lookup"><span data-stu-id="7c538-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="7c538-140">Pokud tyto funkce zapnete, dojde k následujícím akcím:</span><span class="sxs-lookup"><span data-stu-id="7c538-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="7c538-141">Existující pracovní prostor **Správa výdajů** je nahrazen novým pracovním prostorem.</span><span class="sxs-lookup"><span data-stu-id="7c538-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="7c538-142">Bude přidána nová položka nabídky pro viditelnost pole výdajů.</span><span class="sxs-lookup"><span data-stu-id="7c538-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="7c538-143">Předchozí stránku **Sestavy výdajů** můžete stále otevřít přechodem na **Správa výdajů > Moje výdaje > Sestavy výdajů**.</span><span class="sxs-lookup"><span data-stu-id="7c538-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="7c538-144">Pracovní postupy a jakákoliv schválení vás stále zavedou na existující stránku sestav výdajů.</span><span class="sxs-lookup"><span data-stu-id="7c538-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="7c538-145">Příjemky budou zpracovány pomocí Microsoft Azure Cognitive Services a metadata budou extrahována a přidána.</span><span class="sxs-lookup"><span data-stu-id="7c538-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="7c538-146">Je přidána možnost, která umožňuje vytvořit sestavu výdajů, která obsahuje spárované nepřipojené příjemky.</span><span class="sxs-lookup"><span data-stu-id="7c538-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="7c538-147">Možnost, která je přidána do sestav výdajů, umožňuje vytvořit řádek výdajů z příjemky, nebo se pokusí o spárování existující příjemky s existujícím řádkem výdajů.</span><span class="sxs-lookup"><span data-stu-id="7c538-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="7c538-148">Další informace o přepracované funkci sestav výdajů naleznete v tématu [Sestavy výdajů v nové podobě](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="7c538-148">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="7c538-149">Časté dotazy</span><span class="sxs-lookup"><span data-stu-id="7c538-149">Frequently asked questions</span></span>

<span data-ttu-id="7c538-150">**Používá společnost Microsoft moje data pro své modely?**</span><span class="sxs-lookup"><span data-stu-id="7c538-150">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="7c538-151">Ne, společnost Microsoft vytvořila obecný model strojového učení pro svou službu zpracování příjemek.</span><span class="sxs-lookup"><span data-stu-id="7c538-151">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="7c538-152">Tento model není založen na příjemkách, které jste odeslali.</span><span class="sxs-lookup"><span data-stu-id="7c538-152">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="7c538-153">**Kde je tato funkce dostupná a zpracovaná?**</span><span class="sxs-lookup"><span data-stu-id="7c538-153">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="7c538-154">V současné době jsou podporovány Spojené státy.</span><span class="sxs-lookup"><span data-stu-id="7c538-154">Currently, the United States is supported.</span></span>

<span data-ttu-id="7c538-155">**Kam moje příjemky směřují?**</span><span class="sxs-lookup"><span data-stu-id="7c538-155">**Where do my receipts go?**</span></span>

<span data-ttu-id="7c538-156">Aplikace Finance bude kontaktovat Cognitive Services za účelem extrahování dat polí.</span><span class="sxs-lookup"><span data-stu-id="7c538-156">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="7c538-157">Služby Cognitive Services si ponechají kopii vaší příjemky po dobu 24 hodin během zpracování.</span><span class="sxs-lookup"><span data-stu-id="7c538-157">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="7c538-158">Po dokončení zpracování služby Cognitive Services odstraní příjemku.</span><span class="sxs-lookup"><span data-stu-id="7c538-158">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="7c538-159">Příjemky jsou stále uloženy v aplikaci Finance.</span><span class="sxs-lookup"><span data-stu-id="7c538-159">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="7c538-160">Další informace naleznete v tématu [Povolení pochopení příjemek s novou funkcí rozpoznávání formulářů](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="7c538-160">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
