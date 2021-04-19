---
title: Vytvořit právnické osoby
description: Toto téma popisuje, jak vytvořit právnické osoby v Microsoft Dynamics 365 Commerce, které je nutné před vytvořením kanálů vytvořit a nakonfigurovat.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 225fd6a07fee29414ac30a4602b4dfccdc4d742b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800607"
---
# <a name="create-legal-entities"></a><span data-ttu-id="d1e60-103">Vytvořit právnické osoby</span><span class="sxs-lookup"><span data-stu-id="d1e60-103">Create legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d1e60-104">Toto téma popisuje, jak vytvořit právnické osoby v Microsoft Dynamics 365 Commerce, které je nutné před vytvořením kanálů vytvořit a nakonfigurovat.</span><span class="sxs-lookup"><span data-stu-id="d1e60-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

<span data-ttu-id="d1e60-105">Právnická osoba je organizace, která má registrovanou nebo uzákoněnou právní strukturu.</span><span class="sxs-lookup"><span data-stu-id="d1e60-105">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="d1e60-106">Právnické osoby mohou uzavírat právní smlouvy a je po nich vyžadována příprava výkazů s informacemi o jejich výkonu.</span><span class="sxs-lookup"><span data-stu-id="d1e60-106">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="d1e60-107">Společnost je typ právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="d1e60-107">A company is a type of legal entity.</span></span> <span data-ttu-id="d1e60-108">V současné době jsou společnosti pouze druhem právnické osoby, kterou můžete vytvořit, a každá právnická osoba je spojena s identifikátorem společnosti.</span><span class="sxs-lookup"><span data-stu-id="d1e60-108">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="d1e60-109">Toto přiřazení existuje vzhledem k tomu, že některé funkční oblasti v aplikaci používají ID společnosti nebo *DataAreaId* ve svých datových modelech.</span><span class="sxs-lookup"><span data-stu-id="d1e60-109">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="d1e60-110">V těchto funkčních oblastech jsou společnosti používány jako hranice pro zabezpečení dat.</span><span class="sxs-lookup"><span data-stu-id="d1e60-110">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="d1e60-111">Uživatelé mohou přistupovat k datům pouze pro společnost, ke které jsou aktuálně přihlášeni.</span><span class="sxs-lookup"><span data-stu-id="d1e60-111">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="d1e60-112">Při vytváření kanálu je nutné určit právnickou osobu, ke které daný kanál náleží.</span><span class="sxs-lookup"><span data-stu-id="d1e60-112">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="d1e60-113">Vytvořit novou právnickou osobu</span><span class="sxs-lookup"><span data-stu-id="d1e60-113">Create a new legal entity</span></span>

<span data-ttu-id="d1e60-114">Chcete-li vytvořit novou právnickou osobu v Dynamics 365 Commerce, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="d1e60-114">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="d1e60-115">V navigačním podokně přejděte na **Moduly \> Nastavení centrály \> Právnické osoby**.</span><span class="sxs-lookup"><span data-stu-id="d1e60-115">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="d1e60-116">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d1e60-116">On the action pane, select **New**.</span></span> <span data-ttu-id="d1e60-117">Vpravo sezobrazí podokno **Nová právnická osoba**.</span><span class="sxs-lookup"><span data-stu-id="d1e60-117">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="d1e60-118">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="d1e60-118">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="d1e60-119">Do pole **Společnost** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d1e60-119">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="d1e60-120">V poli **Země/oblast** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d1e60-120">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="d1e60-121">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1e60-121">Select **OK**.</span></span> 

   ![Vytvoření právnické osoby](media/legal-entities.png)

1. <span data-ttu-id="d1e60-123">V sekci **Obecné** zadejte následující obecné informace o právnické odobě:</span><span class="sxs-lookup"><span data-stu-id="d1e60-123">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="d1e60-124">Pokud je požadován vyhledávací název, zadejte vyhledávací název.</span><span class="sxs-lookup"><span data-stu-id="d1e60-124">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="d1e60-125">Vyhledávací název je alternativní název, který lze použít k hledání tohoto právního subjektu.</span><span class="sxs-lookup"><span data-stu-id="d1e60-125">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="d1e60-126">Vyberte, zda je tato právnická osoba používána jako konsolidační společnost.</span><span class="sxs-lookup"><span data-stu-id="d1e60-126">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="d1e60-127">Vyberte, zda je tato právnická osoba používána jako eliminační společnost.</span><span class="sxs-lookup"><span data-stu-id="d1e60-127">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="d1e60-128">Vyberte **výchozí jazyk** pro entitu.</span><span class="sxs-lookup"><span data-stu-id="d1e60-128">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="d1e60-129">Vyberte **časové pásmo** pro entitu.</span><span class="sxs-lookup"><span data-stu-id="d1e60-129">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="d1e60-130">V části **Adresy** vyberte **Upravit** a zadejte údaje adresy, například název ulice, číslo, PSČ a město.</span><span class="sxs-lookup"><span data-stu-id="d1e60-130">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="d1e60-131">V části **Kontaktní informace** zadejte informace o metodách komunikace, například e-mailové adresy, adresy URL a telefonní čísla.</span><span class="sxs-lookup"><span data-stu-id="d1e60-131">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="d1e60-132">V části **Statutární vykazování** zadejte registrační čísla, která se používají pro statutární vykazování.</span><span class="sxs-lookup"><span data-stu-id="d1e60-132">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="d1e60-133">V části **Registrační čísla** zadejte informace vyžadované právnickou osobou.</span><span class="sxs-lookup"><span data-stu-id="d1e60-133">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="d1e60-134">V části **Informace o bankovním účtu** zadejte bankovní účty a směrové kódy pro právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="d1e60-134">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="d1e60-135">V části **Zahraniční obchod a logistika** zadejte dodací informace pro právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="d1e60-135">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="d1e60-136">V části **Číselné řady** můžete zobrazit číselné řady, které jsou spojeny s právním subjektem.</span><span class="sxs-lookup"><span data-stu-id="d1e60-136">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="d1e60-137">Tato možnost bude prázdná, aby začínala hodnotou.</span><span class="sxs-lookup"><span data-stu-id="d1e60-137">This will be empty to start with.</span></span>
1. <span data-ttu-id="d1e60-138">V části **Obrázek řídicího panelu** můžete zobrazit nebo změnit obrázek loga a/nebo řídicího panelu přidružený k právnické osobě.</span><span class="sxs-lookup"><span data-stu-id="d1e60-138">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="d1e60-139">V části **Daňová registrace** zadejte registrační čísla, která se používají při styku s finančními úřady.</span><span class="sxs-lookup"><span data-stu-id="d1e60-139">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="d1e60-140">V části **Daň 1099** zadejte informace 1099 pro právní subjekt.</span><span class="sxs-lookup"><span data-stu-id="d1e60-140">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="d1e60-141">V části **Daňové informace** zadejte daňové informace pro právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="d1e60-141">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="d1e60-142">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d1e60-142">Select **Save**.</span></span>

<span data-ttu-id="d1e60-143">Na následujícím obrázku je podrobný příklad právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="d1e60-143">The following image shows details of an example legal entity.</span></span>

![Obecná část právnické osoby](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="d1e60-145">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="d1e60-145">Additional resources</span></span>

[<span data-ttu-id="d1e60-146">Přehled organizací a organizačních hierarchií</span><span class="sxs-lookup"><span data-stu-id="d1e60-146">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="d1e60-147">Plánování organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="d1e60-147">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="d1e60-148">Organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="d1e60-148">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="d1e60-149">Přehled kanálů</span><span class="sxs-lookup"><span data-stu-id="d1e60-149">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="d1e60-150">Předpoklady nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="d1e60-150">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
