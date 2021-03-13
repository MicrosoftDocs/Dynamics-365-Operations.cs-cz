---
title: Odkazy na původní faktury v dobropisech
description: Toto téma vysvětluje, jak nastavit a vytisknout původní čísla faktur v souvisejících dobropisech.
author: ilkond
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 673288f04b33aa2a578f9e2e7913dbe7ac309644
ms.sourcegitcommit: 7cdec5469ff0da145ac4e01caf3287d0627ae2dc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2021
ms.locfileid: "5099995"
---
# <a name="references-to-original-invoices-in-credit-notes"></a><span data-ttu-id="fbf1d-103">Odkazy na původní faktury v dobropisech</span><span class="sxs-lookup"><span data-stu-id="fbf1d-103">References to original invoices in credit notes</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="fbf1d-104">V některých zemích a regionech existuje zákonný požadavek, aby tištěné dobropisy obsahovaly odkazy na původní faktury.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-104">In some countries and regions, there is a legal requirement that printed credit notes include references to the original invoices.</span></span> <span data-ttu-id="fbf1d-105">Toto téma vysvětluje, jak nastavit a vytisknout původní čísla faktur v souvisejících dobropisech.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-105">This topic explains how to set up and print the original invoice numbers in related credit notes.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fbf1d-106">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="fbf1d-106">Prerequisites</span></span>

- <span data-ttu-id="fbf1d-107">V pracovním prostoru **Správa funkcí** zapněte funkci **Rozvržení opravné fakturace v sestavách faktur dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-107">In the **Feature management** workspace, turn on the **Credit invoicing layout for sales and project invoice reports** feature.</span></span> <span data-ttu-id="fbf1d-108">Další informace naleznete v tématu [Přehled správy funkcí](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fbf1d-108">For more information, see [Feature management overview](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="fbf1d-109">Tiskové formáty požadovaných dokumentů musí být nakonfigurovány ve správě tisku.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-109">The printable formats of the required documents must be configured in Print management.</span></span>

<span data-ttu-id="fbf1d-110">Funkce popsané v tomto tématu platí pro následující dokumenty:</span><span class="sxs-lookup"><span data-stu-id="fbf1d-110">The functionality that is described in this topic applies to the following documents:</span></span>

<span data-ttu-id="fbf1d-111">**Pohledávky**</span><span class="sxs-lookup"><span data-stu-id="fbf1d-111">**Accounts receivable**</span></span>

- <span data-ttu-id="fbf1d-112">Dobropis s volným textem</span><span class="sxs-lookup"><span data-stu-id="fbf1d-112">Free text credit note</span></span>
- <span data-ttu-id="fbf1d-113">Dobropis zákazníkům</span><span class="sxs-lookup"><span data-stu-id="fbf1d-113">Customer credit note</span></span>

<span data-ttu-id="fbf1d-114">**Řízení projektů a účetnictví**</span><span class="sxs-lookup"><span data-stu-id="fbf1d-114">**Project management and accounting**</span></span>

- <span data-ttu-id="fbf1d-115">Dobropis projektu</span><span class="sxs-lookup"><span data-stu-id="fbf1d-115">Project credit note</span></span>

## <a name="configure-accounts-receivable-parameters"></a><span data-ttu-id="fbf1d-116">Konfigurujte parametry pohledávek.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-116">Configure Accounts receivable parameters</span></span>

<span data-ttu-id="fbf1d-117">Pomocí těchto kroků nastavíte parametr, který řídí, zda se odkazy na původní faktury vytisknou na souvisejících dobropisech.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-117">Follow these steps to set the parameter that controls whether references to the original invoices are printed in related credit notes.</span></span>

1. <span data-ttu-id="fbf1d-118">Přejděte do **Pohledávky** \> **Nastavení** \> **Parametry pohledávek**.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-118">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="fbf1d-119">Na kartě **Aktualizace** na pevné záložce **Faktura** nastavte možnost **Použije rozvržení opravné fakturace v sestavách prodejních faktur a projektů** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-119">On the **Updates** tab, on the **Invoice** FastTab, set the **Apply the credit invoicing layout into sales and project invoice reports** option to **Yes**.</span></span>

![Konfigurace parametrů pohledávek](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a><span data-ttu-id="fbf1d-121">Definujte odkazy na původní faktury</span><span class="sxs-lookup"><span data-stu-id="fbf1d-121">Define references to original invoices</span></span>

<span data-ttu-id="fbf1d-122">Pomocí následujících postupů definujte odkazy na původní faktury na základě typu dokumentu.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-122">Use the following procedures to define references to original invoices, based on the document type.</span></span>

### <a name="free-text-credit-note"></a><span data-ttu-id="fbf1d-123">Dobropis s volným textem</span><span class="sxs-lookup"><span data-stu-id="fbf1d-123">Free text credit note</span></span>

1. <span data-ttu-id="fbf1d-124">Přejděte na **Pohledávky** \> **Faktury** \> **Všechny volné faktury**.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-124">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="fbf1d-125">Vytvořte nový dobropis nebo vyberte stávající dobropis.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-125">Create a new credit note, or select an existing credit note.</span></span>
3. <span data-ttu-id="fbf1d-126">Otevřete fakturu.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-126">Open the invoice.</span></span>
4. <span data-ttu-id="fbf1d-127">V podokně akcí na kartě **Faktura** ve skupině **Funkce** zvolte **Opravná fakturace**.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-127">On the Action Pane, on the **Invoice** tab, in the **Functions** group, select **Credit invoicing**.</span></span>
5. <span data-ttu-id="fbf1d-128">Zadejte odkaz na původní fakturu a vyberte důvod opravy.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-128">Enter the reference to the original invoice, and select the reason for the correction.</span></span>

![Definování odkazu na fakturu s volným textem](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a><span data-ttu-id="fbf1d-130">Dobropis zákazníkům</span><span class="sxs-lookup"><span data-stu-id="fbf1d-130">Customer credit note</span></span>

1. <span data-ttu-id="fbf1d-131">Přejděte na **Pohledávky** \> **Objednávky** \> **Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-131">Go to **Accounts receivable** \> **Orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="fbf1d-132">Vyberte a otevřete fakturovanou prodejní objednávku, kterou je třeba opravit.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-132">Select and open the invoiced sales order that must be corrected.</span></span>
3. <span data-ttu-id="fbf1d-133">V podokně akcí na kartě **Prodej** ve skupině **Dobropis** zvolte **Dobropis**.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-133">On the Action Pane, on the **Sell** tab, in the **Credit note** group, select **Credit note**.</span></span>
4. <span data-ttu-id="fbf1d-134">Zadejte důvod opravy.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-134">Enter the reason for the correction.</span></span> <span data-ttu-id="fbf1d-135">Odkaz na původní fakturu se vytvoří automaticky.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-135">The reference to the original invoice is automatically established.</span></span>

![Definování odkazu na prodejní objednávku](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a><span data-ttu-id="fbf1d-137">Dobropis projektu</span><span class="sxs-lookup"><span data-stu-id="fbf1d-137">Project credit note</span></span>

1. <span data-ttu-id="fbf1d-138">Přejděte na **Řízení projektu a účetnictví** \> **Faktury projektu** \> **Faktury projektu**.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-138">Go to **Project management and accounting** \> **Project invoices** \> **Project invoices**.</span></span>
2. <span data-ttu-id="fbf1d-139">Vyberte a otevřete fakturu projektu, kterou je třeba opravit.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-139">Select and open the project invoice that must be corrected.</span></span>
3. <span data-ttu-id="fbf1d-140">V podokně akcí na kartě **Faktura projektu** ve skupině **Funkce** zvolte **Vybrat pro dobropis**.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-140">On the Action Pane, on the **Project invoice** tab, in the **Functions** group, select **Select for credit note**.</span></span>
4. <span data-ttu-id="fbf1d-141">Vyberte **Opravná fakturace**.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-141">Select **Credit invoicing**.</span></span>
5. <span data-ttu-id="fbf1d-142">Zadejte důvod opravy.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-142">Enter the reason for the correction.</span></span> <span data-ttu-id="fbf1d-143">Odkaz na původní fakturu se vytvoří automaticky.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-143">The reference to the original invoice is automatically established.</span></span>

![Definování odkazu na projektovou fakturu](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a><span data-ttu-id="fbf1d-145">Tisk dobropisů</span><span class="sxs-lookup"><span data-stu-id="fbf1d-145">Printing credit notes</span></span>

<span data-ttu-id="fbf1d-146">Když vytisknete deobropisy s volným textem, dobropisy zákazníků a projektů, budou obsahovat odkaz na původní fakturu a důvod opravy.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-146">When you print free text, customer, and project credit notes, they will include the reference to the original invoice and the correction reason.</span></span>

![Vytištěný dobropis](media/credit-note-FTI.jpg)

> [!NOTE]
> <span data-ttu-id="fbf1d-148">Ujistěte se, že jsou tiskové formáty dokumentů správně nakonfigurovány za předpokladu, že budou vytištěny odkazy na původní faktury.</span><span class="sxs-lookup"><span data-stu-id="fbf1d-148">Make sure that the printable formats of the documents are correctly configured, on the assumption that references to original invoices will be printed.</span></span>
