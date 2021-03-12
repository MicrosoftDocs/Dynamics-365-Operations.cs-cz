---
title: Vytvořit právnické osoby
description: Toto téma popisuje, jak vytvořit právnické osoby v Microsoft Dynamics 365 Commerce, které je nutné před vytvořením kanálů vytvořit a nakonfigurovat.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9491feb004366a02155225bfb323773e130f3dc9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993596"
---
# <a name="create-legal-entities"></a><span data-ttu-id="e284c-103">Vytvořit právnické osoby</span><span class="sxs-lookup"><span data-stu-id="e284c-103">Create legal entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e284c-104">Toto téma popisuje, jak vytvořit právnické osoby v Microsoft Dynamics 365 Commerce, které je nutné před vytvořením kanálů vytvořit a nakonfigurovat.</span><span class="sxs-lookup"><span data-stu-id="e284c-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

## <a name="overview"></a><span data-ttu-id="e284c-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="e284c-105">Overview</span></span>

<span data-ttu-id="e284c-106">Právnická osoba je organizace, která má registrovanou nebo uzákoněnou právní strukturu.</span><span class="sxs-lookup"><span data-stu-id="e284c-106">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="e284c-107">Právnické osoby mohou uzavírat právní smlouvy a je po nich vyžadována příprava výkazů s informacemi o jejich výkonu.</span><span class="sxs-lookup"><span data-stu-id="e284c-107">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="e284c-108">Společnost je typ právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="e284c-108">A company is a type of legal entity.</span></span> <span data-ttu-id="e284c-109">V současné době jsou společnosti pouze druhem právnické osoby, kterou můžete vytvořit, a každá právnická osoba je spojena s identifikátorem společnosti.</span><span class="sxs-lookup"><span data-stu-id="e284c-109">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="e284c-110">Toto přiřazení existuje vzhledem k tomu, že některé funkční oblasti v aplikaci používají ID společnosti nebo *DataAreaId* ve svých datových modelech.</span><span class="sxs-lookup"><span data-stu-id="e284c-110">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="e284c-111">V těchto funkčních oblastech jsou společnosti používány jako hranice pro zabezpečení dat.</span><span class="sxs-lookup"><span data-stu-id="e284c-111">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="e284c-112">Uživatelé mohou přistupovat k datům pouze pro společnost, ke které jsou aktuálně přihlášeni.</span><span class="sxs-lookup"><span data-stu-id="e284c-112">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="e284c-113">Při vytváření kanálu je nutné určit právnickou osobu, ke které daný kanál náleží.</span><span class="sxs-lookup"><span data-stu-id="e284c-113">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="e284c-114">Vytvořit novou právnickou osobu</span><span class="sxs-lookup"><span data-stu-id="e284c-114">Create a new legal entity</span></span>

<span data-ttu-id="e284c-115">Chcete-li vytvořit novou právnickou osobu v Dynamics 365 Commerce, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="e284c-115">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="e284c-116">V navigačním podokně přejděte na **Moduly \> Nastavení centrály \> Právnické osoby**.</span><span class="sxs-lookup"><span data-stu-id="e284c-116">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="e284c-117">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="e284c-117">On the action pane, select **New**.</span></span> <span data-ttu-id="e284c-118">Vpravo sezobrazí podokno **Nová právnická osoba**.</span><span class="sxs-lookup"><span data-stu-id="e284c-118">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="e284c-119">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="e284c-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="e284c-120">Do pole **Společnost** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e284c-120">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="e284c-121">V poli **Země/oblast** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e284c-121">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="e284c-122">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e284c-122">Select **OK**.</span></span> 

   ![Vytvoření právnické osoby](media/legal-entities.png)

1. <span data-ttu-id="e284c-124">V sekci **Obecné** zadejte následující obecné informace o právnické odobě:</span><span class="sxs-lookup"><span data-stu-id="e284c-124">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="e284c-125">Pokud je požadován vyhledávací název, zadejte vyhledávací název.</span><span class="sxs-lookup"><span data-stu-id="e284c-125">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="e284c-126">Vyhledávací název je alternativní název, který lze použít k hledání tohoto právního subjektu.</span><span class="sxs-lookup"><span data-stu-id="e284c-126">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="e284c-127">Vyberte, zda je tato právnická osoba používána jako konsolidační společnost.</span><span class="sxs-lookup"><span data-stu-id="e284c-127">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="e284c-128">Vyberte, zda je tato právnická osoba používána jako eliminační společnost.</span><span class="sxs-lookup"><span data-stu-id="e284c-128">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="e284c-129">Vyberte **výchozí jazyk** pro entitu.</span><span class="sxs-lookup"><span data-stu-id="e284c-129">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="e284c-130">Vyberte **časové pásmo** pro entitu.</span><span class="sxs-lookup"><span data-stu-id="e284c-130">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="e284c-131">V části **Adresy** vyberte **Upravit** a zadejte údaje adresy, například název ulice, číslo, PSČ a město.</span><span class="sxs-lookup"><span data-stu-id="e284c-131">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="e284c-132">V části **Kontaktní informace** zadejte informace o metodách komunikace, například e-mailové adresy, adresy URL a telefonní čísla.</span><span class="sxs-lookup"><span data-stu-id="e284c-132">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="e284c-133">V části **Statutární vykazování** zadejte registrační čísla, která se používají pro statutární vykazování.</span><span class="sxs-lookup"><span data-stu-id="e284c-133">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="e284c-134">V části **Registrační čísla** zadejte informace vyžadované právnickou osobou.</span><span class="sxs-lookup"><span data-stu-id="e284c-134">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="e284c-135">V části **Informace o bankovním účtu** zadejte bankovní účty a směrové kódy pro právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="e284c-135">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="e284c-136">V části **Zahraniční obchod a logistika** zadejte dodací informace pro právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="e284c-136">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="e284c-137">V části **Číselné řady** můžete zobrazit číselné řady, které jsou spojeny s právním subjektem.</span><span class="sxs-lookup"><span data-stu-id="e284c-137">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="e284c-138">Tato možnost bude prázdná, aby začínala hodnotou.</span><span class="sxs-lookup"><span data-stu-id="e284c-138">This will be empty to start with.</span></span>
1. <span data-ttu-id="e284c-139">V části **Obrázek řídicího panelu** můžete zobrazit nebo změnit obrázek loga a/nebo řídicího panelu přidružený k právnické osobě.</span><span class="sxs-lookup"><span data-stu-id="e284c-139">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="e284c-140">V části **Daňová registrace** zadejte registrační čísla, která se používají při styku s finančními úřady.</span><span class="sxs-lookup"><span data-stu-id="e284c-140">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="e284c-141">V části **Daň 1099** zadejte informace 1099 pro právní subjekt.</span><span class="sxs-lookup"><span data-stu-id="e284c-141">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="e284c-142">V části **Daňové informace** zadejte daňové informace pro právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="e284c-142">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="e284c-143">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e284c-143">Select **Save**.</span></span>

<span data-ttu-id="e284c-144">Na následujícím obrázku je podrobný příklad právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="e284c-144">The following image shows details of an example legal entity.</span></span>

![Obecná část právnické osoby](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="e284c-146">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="e284c-146">Additional resources</span></span>

[<span data-ttu-id="e284c-147">Přehled organizací a organizačních hierarchií</span><span class="sxs-lookup"><span data-stu-id="e284c-147">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="e284c-148">Plánování organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="e284c-148">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="e284c-149">Organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="e284c-149">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="e284c-150">Přehled kanálů</span><span class="sxs-lookup"><span data-stu-id="e284c-150">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="e284c-151">Předpoklady nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="e284c-151">Channel setup prerequisites</span></span>](channels-prerequisites.md)
