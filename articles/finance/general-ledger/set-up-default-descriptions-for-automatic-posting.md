---
title: Nastavení výchozích popisů pro automatické zaúčtování
description: Toto téma popisuje jak nastavit výchozí text, který se používá k popisu účetních zápisů, které jsou automaticky zaúčtovány do hlavní knihy. Můžete nastavit výchozí text s popisem pomocí volného textu nebo výběrem pevných proměnných.
author: aprilolson
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3963b4ed63021dd3c84a0d87b768486dcb0f386d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837074"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a><span data-ttu-id="ca001-104">Nastavení výchozích popisů pro automatické zaúčtování</span><span class="sxs-lookup"><span data-stu-id="ca001-104">Set up default descriptions for automatic posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca001-105">Toto téma popisuje jak nastavit výchozí text, který se používá k popisu účetních zápisů, které jsou automaticky zaúčtovány do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="ca001-105">This topic explains how to set up default text that is used to describe accounting entries that are posted automatically to the general ledger.</span></span> <span data-ttu-id="ca001-106">Můžete nastavit výchozí text s popisem pomocí volného textu nebo výběrem pevných proměnných.</span><span class="sxs-lookup"><span data-stu-id="ca001-106">You can set up default description text by using free-form text or by selecting fixed variables.</span></span>

> [!NOTE]
> <span data-ttu-id="ca001-107">U některých typů transakcí v některých zemích/oblastech lze také vložit text z polí do databáze aplikace Microsoft Dynamics AX, která se vztahuje na tyto typy transakcí.</span><span class="sxs-lookup"><span data-stu-id="ca001-107">For some transaction types in some countries or regions, you can also include text from fields in the Microsoft Dynamics AX database that are related to those transaction types.</span></span> <span data-ttu-id="ca001-108">Seznam typů transakcí a zemí a oblastí naleznete v části [Volitelné: Přídání dalšího textu do výchozího popisu](#optional-add-other-text-to-default-descriptions) dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="ca001-108">For a list of the transaction types, and the countries and regions, see the [Optional: Add other text to default descriptions](#optional-add-other-text-to-default-descriptions) section later in this topic.</span></span>

## <a name="set-up-default-descriptions"></a><span data-ttu-id="ca001-109">Nastavit výchozí popisy</span><span class="sxs-lookup"><span data-stu-id="ca001-109">Set up default descriptions</span></span>

1. <span data-ttu-id="ca001-110">Přejděte do nabídky **Správa organizace** \> **Nastavení** \> **Výchozí popisy**.</span><span class="sxs-lookup"><span data-stu-id="ca001-110">Go to **Organization administration** \> **Setup** \> **Default descriptions**.</span></span>
2. <span data-ttu-id="ca001-111">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="ca001-111">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="ca001-112">Vyberte v poli **Popis** typ transakce, pro který chcete vytvořit výchozí popis.</span><span class="sxs-lookup"><span data-stu-id="ca001-112">In the **Description** field, select the type of transaction to create a default description for.</span></span>
4. <span data-ttu-id="ca001-113">Vyberte v poli **Jazyk** požadovaný jazyk, který odpovídá tomuto popisu.</span><span class="sxs-lookup"><span data-stu-id="ca001-113">In the **Language** field, select the language that the description applies to.</span></span>
5. <span data-ttu-id="ca001-114">Zadejte do pole **Text** výchozí popis.</span><span class="sxs-lookup"><span data-stu-id="ca001-114">In the **Text** field, enter the default description.</span></span> <span data-ttu-id="ca001-115">V tomto poli můžete zadat text nebo můžete použít jeden nebo více následujících proměnných s volným textem:</span><span class="sxs-lookup"><span data-stu-id="ca001-115">You can type text in the field, or you can use one or more of the following free-text variables:</span></span>

    - <span data-ttu-id="ca001-116">**%1** – Přidejte datum transakce.</span><span class="sxs-lookup"><span data-stu-id="ca001-116">**%1** – Add the transaction date.</span></span>
    - <span data-ttu-id="ca001-117">**%2** – Přidejte identifikátor odpovídající typu dokumentu, který má být zaúčtován do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="ca001-117">**%2** – Add an identifier that corresponds to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="ca001-118">Například pro typy transakcí, které se vztahují k fakturám, proměnná **%2** přidává číslo faktury.</span><span class="sxs-lookup"><span data-stu-id="ca001-118">For example, for transaction types that are related to invoices, the **%2** variable adds the invoice number.</span></span>
    - <span data-ttu-id="ca001-119">**%3** – Přidá identifikátor vztahující se k typu dokumentu, který má být zaúčtován do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="ca001-119">**%3** – Add an identifier that is related to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="ca001-120">Například pro typy transakcí, které se vztahují k fakturám, proměnná **%3** přidává číslo účtu zákazníka.</span><span class="sxs-lookup"><span data-stu-id="ca001-120">For example, for transaction types that are related to invoices, the **%3** variable adds the customer account number.</span></span>

## <a name="optional-add-other-text-to-default-descriptions"></a><span data-ttu-id="ca001-121">Volitelné: Přidání dalšího textu do výchozích popisů</span><span class="sxs-lookup"><span data-stu-id="ca001-121">Optional: Add other text to default descriptions</span></span>

<span data-ttu-id="ca001-122">U některých typů transakcí v některých zemích/oblastech mohou výchozí popisy obsahovat text, který pochází z polí do databáze aplikace , která se vztahuje na tyto typy transakcí.</span><span class="sxs-lookup"><span data-stu-id="ca001-122">For some transaction types in some countries or regions, default descriptions can include text that comes from fields in your data that are related to those transaction types.</span></span> <span data-ttu-id="ca001-123">Tyto seznamy ukazují typy transakcí a země a oblasti, pro které je tato možnost k dispozici.</span><span class="sxs-lookup"><span data-stu-id="ca001-123">The following lists show the transaction types, and the countries and regions, that this option is available for.</span></span>

<span data-ttu-id="ca001-124">**Typy transakcí**</span><span class="sxs-lookup"><span data-stu-id="ca001-124">**Transaction types**</span></span>

<span data-ttu-id="ca001-125">Můžete přidat jiný text do výchozích popisů pro typy transakcí, které souvisejí s následujícími typy dokumentů:</span><span class="sxs-lookup"><span data-stu-id="ca001-125">You can add other text to default descriptions for transaction types that are related to the following document types:</span></span>

- <span data-ttu-id="ca001-126">Faktury odběratele</span><span class="sxs-lookup"><span data-stu-id="ca001-126">Customer invoices</span></span>
- <span data-ttu-id="ca001-127">Dobropisy zákazníkům</span><span class="sxs-lookup"><span data-stu-id="ca001-127">Customer credit notes</span></span>
- <span data-ttu-id="ca001-128">Platby hotovosti zákazníkům</span><span class="sxs-lookup"><span data-stu-id="ca001-128">Customer cash payments</span></span>
- <span data-ttu-id="ca001-129">Platby dodavatelů</span><span class="sxs-lookup"><span data-stu-id="ca001-129">Vendor payments</span></span>
- <span data-ttu-id="ca001-130">Prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="ca001-130">Sales orders</span></span>
- <span data-ttu-id="ca001-131">Nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="ca001-131">Purchase orders</span></span>
- <span data-ttu-id="ca001-132">Skladové deníky</span><span class="sxs-lookup"><span data-stu-id="ca001-132">Inventory journals</span></span>
- <span data-ttu-id="ca001-133">Hlavní plánování (MRP)</span><span class="sxs-lookup"><span data-stu-id="ca001-133">Master planning (MRP)</span></span>
- <span data-ttu-id="ca001-134">Dlouhodobý majetek</span><span class="sxs-lookup"><span data-stu-id="ca001-134">Fixed assets</span></span>

<span data-ttu-id="ca001-135">**Země a oblasti**</span><span class="sxs-lookup"><span data-stu-id="ca001-135">**Countries and regions**</span></span>

<span data-ttu-id="ca001-136">Tato možnost je k dispozici pro následující země či oblasti:</span><span class="sxs-lookup"><span data-stu-id="ca001-136">This option is available for the following countries and regions:</span></span>

- <span data-ttu-id="ca001-137">Brazílie</span><span class="sxs-lookup"><span data-stu-id="ca001-137">Brazil</span></span>
- <span data-ttu-id="ca001-138">Čína</span><span class="sxs-lookup"><span data-stu-id="ca001-138">China</span></span>
- <span data-ttu-id="ca001-139">Česká republika</span><span class="sxs-lookup"><span data-stu-id="ca001-139">Czech Republic</span></span>
- <span data-ttu-id="ca001-140">Východní Evropa</span><span class="sxs-lookup"><span data-stu-id="ca001-140">Eastern Europe</span></span>
- <span data-ttu-id="ca001-141">Maďarsko</span><span class="sxs-lookup"><span data-stu-id="ca001-141">Hungary</span></span>
- <span data-ttu-id="ca001-142">Indie</span><span class="sxs-lookup"><span data-stu-id="ca001-142">India</span></span>
- <span data-ttu-id="ca001-143">Japonsko</span><span class="sxs-lookup"><span data-stu-id="ca001-143">Japan</span></span>
- <span data-ttu-id="ca001-144">Litva</span><span class="sxs-lookup"><span data-stu-id="ca001-144">Lithuania</span></span>
- <span data-ttu-id="ca001-145">Lotyšsko</span><span class="sxs-lookup"><span data-stu-id="ca001-145">Latvia</span></span>
- <span data-ttu-id="ca001-146">Polsko</span><span class="sxs-lookup"><span data-stu-id="ca001-146">Poland</span></span>
- <span data-ttu-id="ca001-147">Rusko</span><span class="sxs-lookup"><span data-stu-id="ca001-147">Russia</span></span>

### <a name="add-text-to-default-descriptions"></a><span data-ttu-id="ca001-148">Přidání dalšího textu do výchozích popisů</span><span class="sxs-lookup"><span data-stu-id="ca001-148">Add text to default descriptions</span></span>

<span data-ttu-id="ca001-149">Po dokončení kroků uvedených v části [Nastavení výchozích popisů](#set-up-default-descriptions) dříve v tomto tématu postupujte takto pro přidání dalšího textu do výchozích popisů.</span><span class="sxs-lookup"><span data-stu-id="ca001-149">After you complete the steps in the [Set up default descriptions](#set-up-default-descriptions) section earlier in this topic, follow these steps to add other text to the default descriptions.</span></span>

1. <span data-ttu-id="ca001-150">Na pevné záložce **Parametry** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="ca001-150">On the **Parameters** FastTab, select **Add**.</span></span>
2. <span data-ttu-id="ca001-151">V poli **Referenční tabulka** vyberte tabulku databáze, ze které chcete přidat data parametru do popisu.</span><span class="sxs-lookup"><span data-stu-id="ca001-151">In the **Reference table** field, select the database table from which to add parameter data to the description.</span></span>
3. <span data-ttu-id="ca001-152">V poli **Referenční pole** vyberte pole databáze, ze kterého chcete přidat data parametru do popisu.</span><span class="sxs-lookup"><span data-stu-id="ca001-152">In the **Reference field** field, select the field from which to add parameter data to the description.</span></span>
4. <span data-ttu-id="ca001-153">Opakováním kroků 1 až 3 přidejte další parametry.</span><span class="sxs-lookup"><span data-stu-id="ca001-153">Repeat steps 1 through 3 to add more parameters.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]