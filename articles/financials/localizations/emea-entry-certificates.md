---
title: "Vstupní certifikáty EU"
description: "V tomto článku jsou informace o vstupních certifikátech Evropské unie (EU)."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustEntryCertificateJour_W, CustParameters, CustTable, SalesTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 11464
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9b3346a5229d0cc9e7af74f17ea6a327e5ba253a
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="eu-entry-certificates"></a><span data-ttu-id="785c0-103">Vstupní certifikáty EU</span><span class="sxs-lookup"><span data-stu-id="785c0-103">EU entry certificates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="785c0-104">V tomto článku jsou informace o vstupních certifikátech Evropské unie (EU).</span><span class="sxs-lookup"><span data-stu-id="785c0-104">This article provides information about European Union (EU) entry certificates.</span></span>

<span data-ttu-id="785c0-105">K dispozici máte následující úkoly pro vstupní certifikáty Evropské unie (EU):</span><span class="sxs-lookup"><span data-stu-id="785c0-105">You can complete the following tasks for a European Union (EU) entry certificate:</span></span>

-   <span data-ttu-id="785c0-106">Vytvoření a vystavení vstupního certifikátu EU spolu s dodacím listem nebo fakturou odběratele pro dodávku zboží nebo služby do zemí/regionů EU.</span><span class="sxs-lookup"><span data-stu-id="785c0-106">Create and issue an EU entry certificate together with a packing slip or customer invoice for the delivery of items or services to EU countries/regions.</span></span>
-   <span data-ttu-id="785c0-107">Zobrazení vstupního certifikátu EU s podpisem zákazníka EU.</span><span class="sxs-lookup"><span data-stu-id="785c0-107">Receive the EU entry certificate that is signed by an EU customer.</span></span>
-   <span data-ttu-id="785c0-108">Odeslání podepsaného vstupního certifikátu EU přijatého od odběratele nebo třetí strany odpovědné za dodání položek odběrateli.</span><span class="sxs-lookup"><span data-stu-id="785c0-108">Upload the signed EU entry certificate that is received either from the customer or from a third party who is responsible for delivering items to the customer.</span></span>
-   <span data-ttu-id="785c0-109">Přidružení odeslaného vstupního certifikátu EU k faktuře odběratele.</span><span class="sxs-lookup"><span data-stu-id="785c0-109">Associate the uploaded EU entry certificate with a customer invoice.</span></span>
-   <span data-ttu-id="785c0-110">Aktualizace stavu odeslaného vstupního certifikátu EU.</span><span class="sxs-lookup"><span data-stu-id="785c0-110">Update the status of the uploaded EU entry certificate.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="785c0-111">Požadavky</span><span class="sxs-lookup"><span data-stu-id="785c0-111">Prerequisites</span></span>
<span data-ttu-id="785c0-112">Následující tabulka zobrazuje požadavky, které musí být splněny, než začnete.</span><span class="sxs-lookup"><span data-stu-id="785c0-112">The following table shows the prerequisites that must be in place before you start.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="785c0-113">Kategorie</span><span class="sxs-lookup"><span data-stu-id="785c0-113">Category</span></span></th>
<th><span data-ttu-id="785c0-114">Předpoklad</span><span class="sxs-lookup"><span data-stu-id="785c0-114">Prerequisite</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="785c0-115">Země / oblast</span><span class="sxs-lookup"><span data-stu-id="785c0-115">Country/region</span></span></td>
<td><span data-ttu-id="785c0-116">Primární adresa právnické osoby musí být v členském státě EU.</span><span class="sxs-lookup"><span data-stu-id="785c0-116">The primary address of the legal entity must be in a EU member state.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="785c0-117">Související úkoly nastavení</span><span class="sxs-lookup"><span data-stu-id="785c0-117">Related set up tasks</span></span></td>
<td><ul>
<li><span data-ttu-id="785c0-118">Na stránce <strong>Parametry pohledávek</strong> vyberte možnosti <strong>Povolit správu vstupních certifikátů</strong> a <strong>Povolit vystavování vstupních certifikátů</strong>.</span><span class="sxs-lookup"><span data-stu-id="785c0-118">On the <strong>Accounts receivable parameters</strong> page, select the <strong>Enable entry certificate management</strong> and <strong>Enable entry certificate issuing</strong> options.</span></span></li>
<li><span data-ttu-id="785c0-119">Na stránce <strong>Odběratelé</strong> na pevné záložce <strong>Faktury a dodávky</strong> vyberte možnost <strong>Požadován vstupní certifikát</strong>, čímž označíte, že vstupní certifikát EU je povinný pro odběratele.</span><span class="sxs-lookup"><span data-stu-id="785c0-119">On the <strong>Customers</strong> page, on the <strong>Invoice and delivery</strong> FastTab, select the <strong>Entry certificate required</strong> option to indicate that an EU entry certificate is mandatory for the customer.</span></span> <span data-ttu-id="785c0-120">Vyberte možnost <strong>Vystavit vstupní certifikát</strong>, pokud chcete vystavit vstupní certifikát EU právnické osoby pro odběratele.</span><span class="sxs-lookup"><span data-stu-id="785c0-120">Select the <strong>Issue entry certificate</strong> option to issue an EU entry certificate of the legal entity to the customer.</span></span></li>
<li><span data-ttu-id="785c0-121">Na stránce <strong>Parametry pohledávek</strong> vyberte kód číselné řady pro odkaz <strong>Vstupní certifikát</strong>.</span><span class="sxs-lookup"><span data-stu-id="785c0-121">On the <strong>Accounts receivable parameters</strong> page, select a number sequence code for the <strong>Entry certificate</strong> reference.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="785c0-122">Související transakce</span><span class="sxs-lookup"><span data-stu-id="785c0-122">Related transactions</span></span></td>
<td><ul>
<li><span data-ttu-id="785c0-123">Vytvoření účtu odběratele.</span><span class="sxs-lookup"><span data-stu-id="785c0-123">Create a customer account.</span></span></li>
<li><span data-ttu-id="785c0-124">Vytvořte prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="785c0-124">Create a sales order.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="creating-registering-and-uploading-an-eu-entry-certificate"></a><span data-ttu-id="785c0-125">Vytváření, registrace a odesílání vstupního certifikátu EU</span><span class="sxs-lookup"><span data-stu-id="785c0-125">Creating, registering, and uploading an EU entry certificate</span></span>
<span data-ttu-id="785c0-126">Vstupní certifikát EU můžete vytvořit automaticky nebo ručně.</span><span class="sxs-lookup"><span data-stu-id="785c0-126">You can create an EU entry certificate automatically or manually.</span></span> <span data-ttu-id="785c0-127">Vstupní certifikát EU se vytvoří a vytiskne automaticky při zaúčtování dodacího listu nebo faktury odběratele pomocí stránky **Zaúčtování dodacího listu** nebo **Zaúčtování faktury**.</span><span class="sxs-lookup"><span data-stu-id="785c0-127">An EU entry certificate is created and printed automatically when you post a packing slip or invoice for a customer by using the **Packing slip posting** page or the **Posting invoice** page.</span></span> <span data-ttu-id="785c0-128">Pokud chcete ručně vytvořit nebo znovu vytisknout vstupní certifikát EU pro fakturu zákazníka, použijte stránku **Deník faktur**.</span><span class="sxs-lookup"><span data-stu-id="785c0-128">To manually create or reprint an EU entry certificate for a customer invoice, use the **Invoice journal** page.</span></span> <span data-ttu-id="785c0-129">Dále můžete zadat podrobnosti o vstupním certifikátu EU vystaveném třetí stranou na stránce **Deník vstupního certifikátu**.</span><span class="sxs-lookup"><span data-stu-id="785c0-129">Additionally, you can use the **Entry certificate journal** page to enter details about an EU entry certificate that is issued by a third party.</span></span>

### <a name="creating-an-eu-entry-certificate-automatically-or-manually"></a><span data-ttu-id="785c0-130">Vytváření vstupního certifikátu EU automaticky nebo ručně</span><span class="sxs-lookup"><span data-stu-id="785c0-130">Creating an EU entry certificate automatically or manually</span></span>

<span data-ttu-id="785c0-131">Vstupní certifikát EU můžete vytvořit automaticky pomocí dodacího listu na stránce **Všechny prodejní objednávky** nebo pomocí faktury na stránce **Prodejní objednávka**.</span><span class="sxs-lookup"><span data-stu-id="785c0-131">You can create an EU entry certificate automatically by using a packing slip on the **All sales orders** page or by using an invoice on the **Sales order** page.</span></span> <span data-ttu-id="785c0-132">Chcete-li ručně vytvořit vstupní certifikát EU, lze použít fakturu na stránce **Deník faktur**.</span><span class="sxs-lookup"><span data-stu-id="785c0-132">To manually create an EU entry certificate, you can use an invoice on the **Invoice journal** page.</span></span> <span data-ttu-id="785c0-133">Před ručním vytvořením vstupního certifikátu EU je však nutné změnit stav certifikátu faktury.</span><span class="sxs-lookup"><span data-stu-id="785c0-133">However, you must change the certification status of the invoice before you manually create an EU entry certificate.</span></span>

### <a name="registering-an-eu-entry-certificate"></a><span data-ttu-id="785c0-134">Registrace vstupního certifikátu EU</span><span class="sxs-lookup"><span data-stu-id="785c0-134">Registering an EU entry certificate</span></span>

<span data-ttu-id="785c0-135">Pokud je registrace povinná, můžete vstupní certifikát EU vystavený třetí stranou registrovat na stránce**Deník vstupního certifikátu**.</span><span class="sxs-lookup"><span data-stu-id="785c0-135">If registration is required, you can use the **Entry certificate journal** page to register an EU entry certificate that is issued by a third party.</span></span>

### <a name="uploading-a-received-eu-entry-certificate"></a><span data-ttu-id="785c0-136">Odeslání přijatého vstupního certifikátu EU</span><span class="sxs-lookup"><span data-stu-id="785c0-136">Uploading a received EU entry certificate</span></span>

<span data-ttu-id="785c0-137">Pomocí stránky **Přílohy** odešlete přijatý vstupní certifikát EU s podpisem zákazníka ze země EU.</span><span class="sxs-lookup"><span data-stu-id="785c0-137">Use the **Attachments** page to upload a received EU entry certificate that is signed by an EU customer.</span></span> <span data-ttu-id="785c0-138">Poté, co je certifikát odeslán, je možné jej přiřadit k faktuře jako důkaz dodání položek.</span><span class="sxs-lookup"><span data-stu-id="785c0-138">After the certificate is uploaded, you can associate it with an invoice as proof that the items were delivered.</span></span> <span data-ttu-id="785c0-139">Tento doklad je vyžadován, pokud musíte vystavit fakturu, která neobsahuje daň z přidané hodnoty (DPH), a používá se rovněž při auditu.</span><span class="sxs-lookup"><span data-stu-id="785c0-139">This proof is required if you must issue an invoice that doesn't include value-added tax (VAT), and it's also used during auditing.</span></span>

### <a name="optional-updating-the-certification-status-and-printing-status-of-an-invoice"></a><span data-ttu-id="785c0-140">Volitelné: Aktualizace stavu certifikátu a tisk stavu faktury</span><span class="sxs-lookup"><span data-stu-id="785c0-140">Optional: Updating the certification status and printing status of an invoice</span></span>

<span data-ttu-id="785c0-141">Můžete aktualizovat stav vstupního certifikátu a stav tisku faktury odběratele pomocí stránky **Deník faktur**.</span><span class="sxs-lookup"><span data-stu-id="785c0-141">You can update the entry certification status and printing status of a customer invoice by using the **Invoice journal** page.</span></span>

## <a name="technical-information-for-system-administrators"></a><span data-ttu-id="785c0-142">Technické informace pro správce systému</span><span class="sxs-lookup"><span data-stu-id="785c0-142">Technical information for system administrators</span></span>
<span data-ttu-id="785c0-143">Pokud nemáte přístup ke stránkám, které se používají k dokončení tohoto úkolu, obraťte se na správce systému a poskytněte informace, které jsou uvedeny v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="785c0-143">If you don't have access to the pages that are used to complete this task, contact your system administrator, and provide the information that is shown in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="785c0-144">Kategorie</span><span class="sxs-lookup"><span data-stu-id="785c0-144">Category</span></span></th>
<th><span data-ttu-id="785c0-145">Předpoklad</span><span class="sxs-lookup"><span data-stu-id="785c0-145">Prerequisite</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="785c0-146">Role a funkční oprávnění zabezpečení</span><span class="sxs-lookup"><span data-stu-id="785c0-146">Security roles and duties</span></span></td>
<td><span data-ttu-id="785c0-147">K nastavení a vytvoření vstupních certifikátů EU pro produkty nebo služby musíte být členem role zabezpečení, která zahrnuje následující úkoly:</span><span class="sxs-lookup"><span data-stu-id="785c0-147">To set up and create EU entry certificates for items or services, you must be a member of a security role that includes the following duties:</span></span>
<ul>
<li><span data-ttu-id="785c0-148"><strong>Úředník pohledávek</strong> (CustInvoiceAccountsReceivableClerk)</span><span class="sxs-lookup"><span data-stu-id="785c0-148"><strong>Accounts receivable clerk</strong> (CustInvoiceAccountsReceivableClerk)</span></span></li>
<li><span data-ttu-id="785c0-149"><strong>Zástupce odběratelského servisu</strong> (TradeCustomerServiceRepresentative)</span><span class="sxs-lookup"><span data-stu-id="785c0-149"><strong>Customer service representative</strong> (TradeCustomerServiceRepresentative)</span></span></li>
<li><span data-ttu-id="785c0-150"><strong>Úředník prodeje</strong> (TradeSalesClerk)</span><span class="sxs-lookup"><span data-stu-id="785c0-150"><strong>Sales clerk</strong> (TradeSalesClerk)</span></span></li>
<li><span data-ttu-id="785c0-151"><strong>Úředník expedice</strong> (InventShippingClerk)</span><span class="sxs-lookup"><span data-stu-id="785c0-151"><strong>Shipping clerk</strong> (InventShippingClerk)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>






