---
title: Synchronizace smluvních faktur v Field Service na volné textové faktury v Supply Chain Management
description: Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci smluvních faktur v Dynamics 365 Field Service do volných faktur v Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 943bf04378a8202d676cbabb282a0a6208a92ef3
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209989"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a><span data-ttu-id="bfd51-103">Synchronizace smluvních faktur v Field Service na volné textové faktury v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="bfd51-103">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="bfd51-104">Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci smluvních faktur v Dynamics 365 Field Service do volných faktur v Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bfd51-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Dynamics 365 Field Service to free text invoices in Dynamics 365 Supply Chain Management.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="bfd51-105">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="bfd51-105">Templates and tasks</span></span>

<span data-ttu-id="bfd51-106">Následující šablona a základní úlohy se používají ke spuštění synchronizace faktur dohod pracovních příkazů v modulu Field Service do prodejních objednávek v modulu Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bfd51-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Supply Chain Management.</span></span>

<span data-ttu-id="bfd51-107">**Název šablony v integraci dat**</span><span class="sxs-lookup"><span data-stu-id="bfd51-107">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="bfd51-108">Smluvní faktury (Field Service do Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="bfd51-108">Agreement invoices (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="bfd51-109">**Názvy úkolů v projektu integrace dat**</span><span class="sxs-lookup"><span data-stu-id="bfd51-109">**Names of the tasks in the Data integration project**</span></span>

- <span data-ttu-id="bfd51-110">Záhlaví faktury</span><span class="sxs-lookup"><span data-stu-id="bfd51-110">Invoice headers</span></span>
- <span data-ttu-id="bfd51-111">Řádky faktury</span><span class="sxs-lookup"><span data-stu-id="bfd51-111">Invoice lines</span></span>

<span data-ttu-id="bfd51-112">Následující úlohy synchronizace jsou vyžadovány před zobrazením synchronizace faktur dohod:</span><span class="sxs-lookup"><span data-stu-id="bfd51-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="bfd51-113">Obchodní vztahy (Sales do Supply Chain Management) – Přímo</span><span class="sxs-lookup"><span data-stu-id="bfd51-113">Accounts (Sales to Supply Chain Management) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="bfd51-114">Sada entit</span><span class="sxs-lookup"><span data-stu-id="bfd51-114">Entity set</span></span>

| <span data-ttu-id="bfd51-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="bfd51-115">Field Service</span></span>  | <span data-ttu-id="bfd51-116">Správa dodavatelsko-odběratelského řetězce</span><span class="sxs-lookup"><span data-stu-id="bfd51-116">Supply Chain Management</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="bfd51-117">faktury</span><span class="sxs-lookup"><span data-stu-id="bfd51-117">invoices</span></span>       | <span data-ttu-id="bfd51-118">Záhlaví volné faktury CDS odběratele</span><span class="sxs-lookup"><span data-stu-id="bfd51-118">CDS customer free text invoice headers</span></span> |
| <span data-ttu-id="bfd51-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="bfd51-119">invoicedetails</span></span> | <span data-ttu-id="bfd51-120">Řádky volné faktury CDS odběratele</span><span class="sxs-lookup"><span data-stu-id="bfd51-120">CDS customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="bfd51-121">Tok entity</span><span class="sxs-lookup"><span data-stu-id="bfd51-121">Entity flow</span></span>

<span data-ttu-id="bfd51-122">Faktury vytvořené z dohody v aplikaci Field Service lze synchronizovat s modulem Supply Chain Management prostřednictvím projektu integrace dat Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="bfd51-122">Invoices that are created from an agreement in Field Service can be synchronized to Supply Chain Management via a Common Data Service Data integration project.</span></span> <span data-ttu-id="bfd51-123">Aktualizace těchto faktur budou synchronizovány s volnými textovými fakturami v modulu Supply Chain Management, pokud je stav účtování volné textové faktury **Zpracovává se**.</span><span class="sxs-lookup"><span data-stu-id="bfd51-123">Updates to these invoices will be synchronized to the free text invoices in Supply Chain Management if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="bfd51-124">Po zaúčtování volných textových faktur v modulu Supply Chain Management a aktualizaci stavu účetnictví na **Dokončeno** již nemůžete synchronizovat aktualizace z Field Service.</span><span class="sxs-lookup"><span data-stu-id="bfd51-124">After the free text invoices are posted in Supply Chain Management, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="bfd51-125">Řešení Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="bfd51-125">Field Service CRM solution</span></span>

<span data-ttu-id="bfd51-126">Bylo přidáno pole **Má řádky s původem smlouvy** bylo přidáno do entity **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="bfd51-126">The **Has Lines With Agreement Origin** field has been added to the **Invoice** entity.</span></span> <span data-ttu-id="bfd51-127">Toto pole pomáhá zajistit, že jsou synchronizovány pouze faktury, které jsou vytvořeny z dohody.</span><span class="sxs-lookup"><span data-stu-id="bfd51-127">This field helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="bfd51-128">Hodnota je **true**, pokud faktura obsahuje alespoň jednu řádku faktury, která pochází z dohody.</span><span class="sxs-lookup"><span data-stu-id="bfd51-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="bfd51-129">Pole **Má původ faktury** bylo přidáno do entity **Řádek faktury**.</span><span class="sxs-lookup"><span data-stu-id="bfd51-129">The **Has Agreement Origin** field has been added to the **Invoice Line** entity.</span></span> <span data-ttu-id="bfd51-130">Toto pole pomáhá zajistit, že jsou synchronizovány pouze řádky faktury, které jsou vytvořeny z dohody.</span><span class="sxs-lookup"><span data-stu-id="bfd51-130">This field helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="bfd51-131">Hodnota je **true**, pokud řádek faktury pochází z dohody.</span><span class="sxs-lookup"><span data-stu-id="bfd51-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="bfd51-132">**Datum faktury** je povinné pole v modulu Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bfd51-132">**Invoice date** is a mandatory field in Supply Chain Management.</span></span> <span data-ttu-id="bfd51-133">Proto musí mít pole hodnotu v poli Field Service předtím, než dojde k synchronizaci.</span><span class="sxs-lookup"><span data-stu-id="bfd51-133">Therefore, the field must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="bfd51-134">Aby bylo možné tento požadavek splnit, je přidána následující logika:</span><span class="sxs-lookup"><span data-stu-id="bfd51-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="bfd51-135">Pokud je pole **Datum faktury** v entitě **Faktura** prázdné (tj. neobsahuje žádnou hodnotu), je nastaveno na současné datum, když je přidán řádek faktury pocházející z dohody.</span><span class="sxs-lookup"><span data-stu-id="bfd51-135">If the **Invoice Date** field is blank on the **Invoice** entity (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="bfd51-136">Uživatel může pole **Datum faktury** změnit.</span><span class="sxs-lookup"><span data-stu-id="bfd51-136">The user can change the **Invoice Date** field.</span></span> <span data-ttu-id="bfd51-137">Avšak pokud se uživatel pokusí uložit fakturu, která pochází z dohody, přijímá chybu obchodního procesu v případě, že je pole **datum faktury** na faktuře prázdné.</span><span class="sxs-lookup"><span data-stu-id="bfd51-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** field is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="bfd51-138">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="bfd51-138">Prerequisites and mapping setup</span></span>

### <a name="in-supply-chain-management"></a><span data-ttu-id="bfd51-139">V Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="bfd51-139">In Supply Chain Management</span></span>

<span data-ttu-id="bfd51-140">Původ faktury je nutné nastavit pro integraci, aby bylo možné rozlišit volné textové faktury v modulu Supply Chain Management, které jsou vytvořeny z faktury dohod v modulu Field Service.</span><span class="sxs-lookup"><span data-stu-id="bfd51-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Supply Chain Management that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="bfd51-141">Když má faktura původ **Integrace faktury dohody**, je pole **Externí faktura** zobrazeno v záhlaví **Prodejní faktura**.</span><span class="sxs-lookup"><span data-stu-id="bfd51-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="bfd51-142">Kromě zobrazení v záhlaví faktury lze použít informace **číslo externí faktury**, které slouží k zajištění, že faktury vytvořené z faktur dohod Field Service jsou filtrovány během synchronizace faktury z Supply Chain Management do Field Service.</span><span class="sxs-lookup"><span data-stu-id="bfd51-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Supply Chain Management to Field Service.</span></span>

1. <span data-ttu-id="bfd51-143">Přejděte do nabídky **Pohledávky** \> **Nastavení** \> **Kódy původu faktury**.</span><span class="sxs-lookup"><span data-stu-id="bfd51-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="bfd51-144">Vyberte **nový** pro vytvoření nového původu faktury.</span><span class="sxs-lookup"><span data-stu-id="bfd51-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="bfd51-145">V **Původ faktury** zadejte název pro původní fakturu, jako je například **FS**.</span><span class="sxs-lookup"><span data-stu-id="bfd51-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="bfd51-146">Do pole **Popis** zadejte popis, například **Faktura dohody v modulu Field Service**.</span><span class="sxs-lookup"><span data-stu-id="bfd51-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="bfd51-147">Zaškrtněte políčko **Přiřazení typů původu**.</span><span class="sxs-lookup"><span data-stu-id="bfd51-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="bfd51-148">Nastavte hodnotu v poli **Typ původu faktury** na **Integrace faktury dohody**.</span><span class="sxs-lookup"><span data-stu-id="bfd51-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="bfd51-149">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="bfd51-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="bfd51-150">V projektu Integrace dat</span><span class="sxs-lookup"><span data-stu-id="bfd51-150">In the Data Integration project</span></span>

<span data-ttu-id="bfd51-151">Úloha: **Řádky faktury**</span><span class="sxs-lookup"><span data-stu-id="bfd51-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="bfd51-152">Ujistěte se, že výchozí hodnota pro pole Supply Chain Management **Zobrazená hodnota hlavního účtu** je aktualizována, aby odpovídala požadované hodnotě.</span><span class="sxs-lookup"><span data-stu-id="bfd51-152">Make sure that the default value for the Supply Chain Management field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="bfd51-153">Výchozí hodnota šablony je **401100**.</span><span class="sxs-lookup"><span data-stu-id="bfd51-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="bfd51-154">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="bfd51-154">Template mapping in Data integration</span></span>

<span data-ttu-id="bfd51-155">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="bfd51-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a><span data-ttu-id="bfd51-156">Smluvní faktury (Field Service do Supply Chain Management): záhlaví faktur</span><span class="sxs-lookup"><span data-stu-id="bfd51-156">Agreement invoices (Field Service to Supply Chain Management): Invoice headers</span></span>

<span data-ttu-id="bfd51-157">[![Mapování šablony v integraci dat](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="bfd51-157">[![Template mapping in Data integration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a><span data-ttu-id="bfd51-158">Smluvní faktury (Field Service do Supply Chain Management): řádky faktur</span><span class="sxs-lookup"><span data-stu-id="bfd51-158">Agreement invoices (Field Service to Supply Chain Management): Invoice lines</span></span>

<span data-ttu-id="bfd51-159">[![Mapování šablony v integraci dat](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="bfd51-159">[![Template mapping in Data integration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>
