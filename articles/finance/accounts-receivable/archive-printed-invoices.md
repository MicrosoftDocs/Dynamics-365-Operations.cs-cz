---
title: Archivovat vytištěné faktury zákazníků s hash čísly
description: Toto téma vysvětluje, jak povolit archivaci, aby bylo možné ukládat tištěné faktury zákazníků s čísly hash.
author: ilyako
manager: AnnBe
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d502ec5d286573c72e207419b66f283183009c09
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557473"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a><span data-ttu-id="bda6f-103">Archivovat vytištěné faktury zákazníků s hash čísly</span><span class="sxs-lookup"><span data-stu-id="bda6f-103">Archive printed customer invoices with hash numbers</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="bda6f-104">V některých zemích existuje zákonný požadavek ukládat vypočítaná čísla hash v systému společně s výtisky některých dokumentů.</span><span class="sxs-lookup"><span data-stu-id="bda6f-104">In some countries, there is a legal requirement to store calculated hash numbers in the system together with printouts of some documents.</span></span> <span data-ttu-id="bda6f-105">Čísla hash lze použít pro hlášení orgánům a během auditů.</span><span class="sxs-lookup"><span data-stu-id="bda6f-105">Hash numbers can be used for reporting to authorities and during audits.</span></span>

<span data-ttu-id="bda6f-106">Toto téma vysvětluje, jak konfigurovat archivaci, aby bylo možné ukládat tištěné faktury zákazníků s čísly hash.</span><span class="sxs-lookup"><span data-stu-id="bda6f-106">This topic explains how to configure archiving in order to store printed customer invoices with hash numbers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bda6f-107">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="bda6f-107">Prerequisites</span></span>

- <span data-ttu-id="bda6f-108">V pracovním prostoru **Správa funkcí** zapněte funkci **Archivovat vytištěné faktury zákazníků s hashovými čísly**.</span><span class="sxs-lookup"><span data-stu-id="bda6f-108">In the **Feature management** workspace, turn on the feature, **Archive printed customer invoices with hash numbers**.</span></span> <span data-ttu-id="bda6f-109">Další informace naleznete v tématu [Přehled správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bda6f-109">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="bda6f-110">Nakonfigurujte tiskové formáty požadovaných dokumentů v části **Správa tisku**.</span><span class="sxs-lookup"><span data-stu-id="bda6f-110">Configure the printable formats of required documents in **Print management**.</span></span>

<span data-ttu-id="bda6f-111">Tato funkce se vztahuje na následující dokumenty.</span><span class="sxs-lookup"><span data-stu-id="bda6f-111">This functionality is applicable to the following documents.</span></span>

<span data-ttu-id="bda6f-112">**Pohledávky**</span><span class="sxs-lookup"><span data-stu-id="bda6f-112">**Accounts receivable**</span></span>
- <span data-ttu-id="bda6f-113">Faktura zákazníka</span><span class="sxs-lookup"><span data-stu-id="bda6f-113">Customer invoice</span></span>
- <span data-ttu-id="bda6f-114">Dobropis zákazníkům</span><span class="sxs-lookup"><span data-stu-id="bda6f-114">Customer credit note</span></span>
- <span data-ttu-id="bda6f-115">Volné faktury</span><span class="sxs-lookup"><span data-stu-id="bda6f-115">Free text invoice</span></span>
- <span data-ttu-id="bda6f-116">Dobropis s volným textem</span><span class="sxs-lookup"><span data-stu-id="bda6f-116">Free text credit note</span></span>

<span data-ttu-id="bda6f-117">**Řízení projektů a účetnictví**</span><span class="sxs-lookup"><span data-stu-id="bda6f-117">**Project management and accounting**</span></span>
- <span data-ttu-id="bda6f-118">Faktura projektu</span><span class="sxs-lookup"><span data-stu-id="bda6f-118">Project invoice</span></span>
- <span data-ttu-id="bda6f-119">Dobropis projektu</span><span class="sxs-lookup"><span data-stu-id="bda6f-119">Project credit note</span></span>

## <a name="configure-customer-master-data"></a><span data-ttu-id="bda6f-120">Konfigurace hlavních dat zákazníků</span><span class="sxs-lookup"><span data-stu-id="bda6f-120">Configure customer master data</span></span>
<span data-ttu-id="bda6f-121">Chcete-li nakonfigurovat údaje o zákazníkovi a zapnout možnost automatického ukládání tištěných faktur jako přílohy, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="bda6f-121">Complete the following steps to configure customer data and turn on the ability to automatically save printed invoices as attachments.</span></span>

1. <span data-ttu-id="bda6f-122">Přejděte na **Pohledávky** > **Všichni zákazníci**.</span><span class="sxs-lookup"><span data-stu-id="bda6f-122">Go to **Accounts receivable** > **All customers**.</span></span> 
2. <span data-ttu-id="bda6f-123">Vyberte zákazníka a na kartě s náhledem **Faktura a doručení** v části **ELEKTRONICKÁ FAKTURA** v poli **Příloha e-faktury** vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="bda6f-123">Select a customer, and on the **Invoice and delivery** FastTab, in the **E-INVOCE** section, in the **eInvoice attachment** field, select **Yes**.</span></span>

## <a name="print-invoices"></a><span data-ttu-id="bda6f-124">Tisk faktur</span><span class="sxs-lookup"><span data-stu-id="bda6f-124">Print invoices</span></span>
<span data-ttu-id="bda6f-125">Můžete zaúčtovat a vytisknout libovolný volný text, zákaznickou a projektovou fakturu nebo dobropis pro zákazníka nakonfigurovaný v předchozím postupu.</span><span class="sxs-lookup"><span data-stu-id="bda6f-125">You can post and print any free text, customer, and project invoice or credit note for the customer configured in the previous procedure.</span></span>

<span data-ttu-id="bda6f-126">Otevřete stránku **Přílohy** pro vytištěnou fakturu.</span><span class="sxs-lookup"><span data-stu-id="bda6f-126">Open the **Attachments** page for the printed invoice.</span></span> <span data-ttu-id="bda6f-127">Na kartě s náhledem **Příloha** ve skupině polí **Další detaily** poli v **Číslo hash dokumentu** vyhledejte uložené hash číslo vypočítané pro vytištěnou fakturu.</span><span class="sxs-lookup"><span data-stu-id="bda6f-127">On the **Attachment** FastTab, in the **Additional details** field group, in **Document hash number** field, find the stored hash number calculated for the printed invoice.</span></span>

![Hash číslo přílohy](media/attach-hash-num.jpg)

