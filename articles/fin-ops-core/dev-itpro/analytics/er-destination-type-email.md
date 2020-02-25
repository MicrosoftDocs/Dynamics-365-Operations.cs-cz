---
title: Typ cílového umístění elektronického výkaznictví e-mailu
description: Toto téma obsahuje informace o tom, jak konfigurovat cíl e-mailu pro každou komponentu SLOŽKA nebo SOUBOR formátu elektronického výkaznictví, který je nakonfigurován pro generování odchozích dokumentů.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 086114d6a8d425ca01521d9607e4a70ec5aa766b
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019666"
---
# <span data-ttu-id="cb382-103"><a name="EmailDestinationType">E-mailový cíl</a></span><span class="sxs-lookup"><span data-stu-id="cb382-103"><a name="EmailDestinationType">Email destination</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb382-104">Můžete konfigurovat cíl e-mailu pro každou komponentu SLOŽKA nebo SOUBOR formátu elektronického výkaznictví, který je nakonfigurován pro generování odchozích dokumentů.</span><span class="sxs-lookup"><span data-stu-id="cb382-104">You can configure an email destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="cb382-105">Vygenerovaný dokument je na základě nastavení cíle dodán jako příloha elektronické pošty.</span><span class="sxs-lookup"><span data-stu-id="cb382-105">Based on the destination setting, a generated document is delivered as an attachment of an electronic mail.</span></span>

<span data-ttu-id="cb382-106">Nastavením možnosti **Povoleno** na **Ano** odešlete výstupní soubor prostřednictvím e-mailu.</span><span class="sxs-lookup"><span data-stu-id="cb382-106">Set **Enabled** to **Yes** to send an output file by email.</span></span> <span data-ttu-id="cb382-107">Po povolení této možnosti můžete zadat příjemce e-mailů a upravit předmět a tělo e-mailové zprávy.</span><span class="sxs-lookup"><span data-stu-id="cb382-107">After this option is enabled, you can specify the email recipients and edit the subject and body of the email message.</span></span> <span data-ttu-id="cb382-108">Můžete nastavit konstantní texty pro předmět a tělo e-mailu nebo můžete použít [vzorce](er-formula-language.md) elektronického výkaznictví k dynamickému vytvoření textů e-mailů.</span><span class="sxs-lookup"><span data-stu-id="cb382-108">You can set up constant texts for the email subject and body, or you can use ER [formulas](er-formula-language.md) to dynamically create email texts.</span></span> 

<span data-ttu-id="cb382-109">E-mailové adresy pro ER lze konfigurovat dvěma způsoby.</span><span class="sxs-lookup"><span data-stu-id="cb382-109">You can configure email addresses for ER in two ways.</span></span> <span data-ttu-id="cb382-110">Konfiguraci lze dokončit stejným způsobem, jakým ji dokončí funkce správy tisku, nebo můžete e-mailovou adresu vyřešit přímým odkazem na konfiguraci elektronického výkaznictví pomocí vzorce.</span><span class="sxs-lookup"><span data-stu-id="cb382-110">The configuration can be completed in the same way that the Print management feature completes it, or you can resolve an email address by using a direct reference to the ER configuration through a formula.</span></span>

<span data-ttu-id="cb382-111">[![Povolení cílového místa e-mailu](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span><span class="sxs-lookup"><span data-stu-id="cb382-111">[![Enable email destination](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span></span>

## <a name="email-address-types"></a><span data-ttu-id="cb382-112">Typy e-mailových adres</span><span class="sxs-lookup"><span data-stu-id="cb382-112">Email address types</span></span>

<span data-ttu-id="cb382-113">Po zvolení **Upravit** v polích **Komu** nebo **Kopie** se zobrazí dialogové okno **E-mail – komu**.</span><span class="sxs-lookup"><span data-stu-id="cb382-113">When you select **Edit** in the **To** or **Cc** fields, the **Email to** dialog box appears.</span></span> <span data-ttu-id="cb382-114">Můžete zvolit typ e-mailové adresy, který použijete.</span><span class="sxs-lookup"><span data-stu-id="cb382-114">You can then select the type of email address to use.</span></span> <span data-ttu-id="cb382-115">Typy e-mailů konfigurace **Konfigurační e-mail** a **Správa tisku** jsou aktuálně podporovány.</span><span class="sxs-lookup"><span data-stu-id="cb382-115">The **Configuration email** and **Print Management** email types are currently supported.</span></span>

<span data-ttu-id="cb382-116">[![Volba typu e-mailu](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span><span class="sxs-lookup"><span data-stu-id="cb382-116">[![Select email type](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span></span>

### <a name="print-management"></a><span data-ttu-id="cb382-117">Správa tisku</span><span class="sxs-lookup"><span data-stu-id="cb382-117">Print management</span></span>

<span data-ttu-id="cb382-118">Vyberete-li typ e-mailu **Správa tisku**, můžete zadat pevné e-mailové adresy do pole **Komu**.</span><span class="sxs-lookup"><span data-stu-id="cb382-118">If you select the **Print Management** email type, you can enter fixed email addresses in the **To** field.</span></span> 

<span data-ttu-id="cb382-119">[![Konfigurace pevných e-mailových adres](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span><span class="sxs-lookup"><span data-stu-id="cb382-119">[![Configure fixed email addresses](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span></span>

<span data-ttu-id="cb382-120">Pro použití jiných než pevných e-mailových adres je nutné vybrat typ zdroje e-mailu pro cíl souboru.</span><span class="sxs-lookup"><span data-stu-id="cb382-120">To use email addresses that aren't fixed, you must select the email source type for a file destination.</span></span> <span data-ttu-id="cb382-121">Podporovány jsou následující hodnoty: **Odběratel**, **Dodavatel**, **Potenciální zákazník**, **Kontakt**, **Konkurent**, **Pracovník**, **Uchazeč**, **Potenciální dodavatel** a **Zakázaný dodavatel**.</span><span class="sxs-lookup"><span data-stu-id="cb382-121">The following values are supported: **Customer**, **Vendor**, **Prospect**, **Contact**, **Competitor**, **Worker**, **Applicant**, **Prospective vendor**, and **Disallowed vendor**.</span></span> <span data-ttu-id="cb382-122">Po výběru typu zdroje e-mailu použijte tlačítko vedle pole **E-mail – zdrojový účet** a otevřete formulář **Návrhář receptur**.</span><span class="sxs-lookup"><span data-stu-id="cb382-122">After you select an email source type, use the button next to the **Email source account** field to open the **Formula designer** form.</span></span> <span data-ttu-id="cb382-123">Pomocí tohoto formuláře můžete připojit vzorec, který se vrací za běhu **účet strany** vybraného typu zdroje ze zpracovaného dokumentu do cíle e-mailu.</span><span class="sxs-lookup"><span data-stu-id="cb382-123">You can use this form to attach a formula that returns at runtime, the **party account** of the selected source type from the processed document to the email destination.</span></span>

<span data-ttu-id="cb382-124">[![Konfigurace účtu zdroje e-mailu](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span><span class="sxs-lookup"><span data-stu-id="cb382-124">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span></span>

<span data-ttu-id="cb382-125">Vzorce jsou specifické pro konfiguraci elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="cb382-125">Formulas are specific to the ER configuration.</span></span> <span data-ttu-id="cb382-126">V poli **Vzorec** zadejte odkaz specifický pro dokument pro stranu typu Odběratel nebo Dodavatel.</span><span class="sxs-lookup"><span data-stu-id="cb382-126">In the **Formula** field, enter a document-specific reference to a customer or vendor party type.</span></span> <span data-ttu-id="cb382-127">Namísto zadávání můžete najít uzel zdroje dat, který reprezentuje účet odběratele nebo dodavatele, a volbou možnosti **Přidat zdroj dat** aktualizovat vzorec.</span><span class="sxs-lookup"><span data-stu-id="cb382-127">Instead of typing, you can find the data source node that represents the customer or vendor account, and then select **Add data source** to update the formula.</span></span> <span data-ttu-id="cb382-128">Příklad: Pokud používáte konfiguraci **platební převod ISO 20022**, uzel představující účet dodavatele má tvar `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span><span class="sxs-lookup"><span data-stu-id="cb382-128">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents a vendor account is `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span></span>

<span data-ttu-id="cb382-129">Zadáte-li hodnotu řetězce, například `"DE-001"`, a uložíte vzorec, bude kontaktní osobě dodavatele zaslán e-mail, **DE-001**.</span><span class="sxs-lookup"><span data-stu-id="cb382-129">If you enter a string value, such as `"DE-001"`, and save a formula, an email will be sent to the contact person of the vendor, **DE-001**.</span></span>


<span data-ttu-id="cb382-130">[![Stránka návrháře vzorců elektronického výkaznictví](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span><span class="sxs-lookup"><span data-stu-id="cb382-130">[![ER formula designer page](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span></span>

<span data-ttu-id="cb382-131">[![Konfigurace účtu zdroje e-mailu](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span><span class="sxs-lookup"><span data-stu-id="cb382-131">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span></span>



### <a name="configuration-email"></a><span data-ttu-id="cb382-132">Konfigurační e-mail</span><span class="sxs-lookup"><span data-stu-id="cb382-132">Configuration email</span></span>

<span data-ttu-id="cb382-133">Použijte tento typ e-mailu, pokud má použitá konfigurace uzel ve zdrojích dat, které vrací **e-mailovou adresu**.</span><span class="sxs-lookup"><span data-stu-id="cb382-133">Use this email type if the configuration that you use has a node in the data sources that returns an **email address**.</span></span> <span data-ttu-id="cb382-134">Zdroje dat a funkce můžete použít v návrháři receptur, abyste získali správně naformátovanou e-mailovou adresu.</span><span class="sxs-lookup"><span data-stu-id="cb382-134">You can use data sources and functions in the formula designer to get a correctly formatted email address.</span></span> <span data-ttu-id="cb382-135">Příklad: Pokud používáte konfiguraci **platební převod ISO 20022**, uzel představující e-mailovou adresu kontaktní osoby dodavatele má tvar `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span><span class="sxs-lookup"><span data-stu-id="cb382-135">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents an email address of a vendor's contact person is `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span></span>

<span data-ttu-id="cb382-136">[![Konfigurace zdroje e-mailové adresy](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span><span class="sxs-lookup"><span data-stu-id="cb382-136">[![Configure email address source](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb382-137">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="cb382-137">Additional resources</span></span>

- [<span data-ttu-id="cb382-138">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="cb382-138">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="cb382-139">Místa určení elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="cb382-139">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="cb382-140">Návrhář receptur v elektronickém výkaznictví</span><span class="sxs-lookup"><span data-stu-id="cb382-140">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
