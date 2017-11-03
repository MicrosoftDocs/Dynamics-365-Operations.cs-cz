---
title: "Zabezpečení uživatele portálu pro dodavatele"
description: "V tomto článku se vysvětluje, jak nastavit zabezpečení pro externí dodavatele, kteří používají portál pro dodavatele. Informace v tomto tématu platí pouze pro verze aplikace Dynamics AX z února a května 2016."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f79f686720d615da6996f854a9e4cc18f840337f
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="vendor-portal-user-security"></a><span data-ttu-id="c2b41-104">Zabezpečení uživatele portálu pro dodavatele</span><span class="sxs-lookup"><span data-stu-id="c2b41-104">Vendor portal user security</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c2b41-105">V tomto článku se vysvětluje, jak nastavit zabezpečení pro externí dodavatele, kteří používají portál pro dodavatele.</span><span class="sxs-lookup"><span data-stu-id="c2b41-105">This article explains how to set up security for external vendors who use the Vendor portal.</span></span> <span data-ttu-id="c2b41-106">Informace v tomto tématu platí pouze pro verze aplikace Dynamics AX z února a května 2016.</span><span class="sxs-lookup"><span data-stu-id="c2b41-106">This information applies only to the February 2016 &amp; May 2016 versions of Dynamics AX.</span></span>

<span data-ttu-id="c2b41-107">Funkce portálu dodavatele byla v Dynamics 365 for Operations verze 1611 nahrazena rozšířenou funkcí spolupráce dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="c2b41-107">The Vendor portal functionality has been replaced by extended vendor collaboration functionality in Dynamics 365 for Operations version 1611.</span></span> <span data-ttu-id="c2b41-108">Další informace o nastavení zabezpečení pro dodavatelskou spolupráci naleznete v tématu [Nastavení a správa dodavatelské spolupráce](set-up-maintain-vendor-collaboration.md).</span><span class="sxs-lookup"><span data-stu-id="c2b41-108">For more information about setting up security for vendor collaboration, see [Set up and maintain vendor collaboration](set-up-maintain-vendor-collaboration.md).</span></span> <span data-ttu-id="c2b41-109">Portál pro dodavatele poskytuje omezenou sadu informací o nákupních objednávkách (POs) pro externí dodavatele.</span><span class="sxs-lookup"><span data-stu-id="c2b41-109">The Vendor portal exposes a limited set of information about purchase orders (POs) to external vendors.</span></span> <span data-ttu-id="c2b41-110">Je důležité, aby byla správně nastavena oprávnění uživatelů k portálu pro dodavatele v aplikaci Microsoft Dynamics AX, aby dodavatelé neměli nežádoucí přístup k dalším informacím v instalaci aplikace Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="c2b41-110">It's important that you correctly set up user permissions for the Vendor portal in Microsoft Dynamics AX, so that vendors don't have unintended access to additional information in your Dynamics AX installation.</span></span> <span data-ttu-id="c2b41-111">**Upozornění:** Na rozdíl od jiných uživatelů externí dodavatelé nemají roli **Systémový uživatel**.</span><span class="sxs-lookup"><span data-stu-id="c2b41-111">**Important:** Unlike other users, external vendors should not have the **SystemUser** role.</span></span> <span data-ttu-id="c2b41-112">Role **Systémový uživatel** poskytuje přístup ke skupině oprávnění, která nejsou vhodná pro externí uživatele.</span><span class="sxs-lookup"><span data-stu-id="c2b41-112">The **SystemUser** role grants access to a set of privileges that aren't suitable for external users.</span></span>

## <a name="setting-up-a-vendor-portal-user"></a><span data-ttu-id="c2b41-113">Nastavení uživatele dodavatelského portálu</span><span class="sxs-lookup"><span data-stu-id="c2b41-113">Setting up a Vendor portal user</span></span>
<span data-ttu-id="c2b41-114">Před vytvořením uživatelského účtu pro někoho, kdo bude používat portál pro dodavatele, musíte povolit dodavatele pro spolupráci s portálem pro dodavatele.</span><span class="sxs-lookup"><span data-stu-id="c2b41-114">Before you create a user account for someone who will use the Vendor portal, you must set up the vendor to allow for Vendor portal collaboration.</span></span> <span data-ttu-id="c2b41-115">Použijte pole **Spolupráce v rámci nákupní objednávky** na kartě **Obecné** na stránce **Dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="c2b41-115">Use the **Purchase order collaboration** field on the **General** tab on the **Vendors** page.</span></span> <span data-ttu-id="c2b41-116">Externí dodavatelé, kteří používají portál pro dodavatele musí mít následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="c2b41-116">External vendors that use the Vendor portal must have the following setup:</span></span>

-   <span data-ttu-id="c2b41-117">Účet uživatele Microsoft Azure Active Directory (AAD) musí být registrován pro dodavatele na stránce **Uživatelé** v aplikaci Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="c2b41-117">A Microsoft Azure Active Directory (AAD) user account must be registered for the vendor on the **Users** page in Dynamics AX.</span></span>
-   <span data-ttu-id="c2b41-118">Dodavatel musí mít role zabezpečení **Dodavatel (externí)**, ne roli **Systémový uživatel**.</span><span class="sxs-lookup"><span data-stu-id="c2b41-118">The vendor must have the **Vendor (external)** security role, not the **SystemUser** role.</span></span> <span data-ttu-id="c2b41-119">**Poznámka:** Role **Systémový uživatel** je automaticky přidělena, když vytvoříte nový účet uživatele v aplikaci Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="c2b41-119">**Note:** The **SystemUser** role is automatically granted when you create a new user account in Dynamics AX.</span></span> <span data-ttu-id="c2b41-120">Proto je nutné odebrat tuto roli a potvrdit varovnou zprávu, která se zobrazí.</span><span class="sxs-lookup"><span data-stu-id="c2b41-120">Therefore, you must remove that role and acknowledge the warning message that you receive.</span></span>
-   <span data-ttu-id="c2b41-121">Dodavatelský uživatel nemá oprávnění k přidání dalších polí z tabulky nákupní objednávky do jejich zobrazení nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="c2b41-121">The vendor user should not be granted permission to add additional fields from the PO tables to their view of the PO.</span></span> <span data-ttu-id="c2b41-122">Na kartě **Přizpůsobení** na kartě **Uživatelé**, nastavte možnost **Explicitní individuální nastavení je povoleno** pro uživatele na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="c2b41-122">On the **Personalization** tab, on the **Users** tab, set the **Explicit personalization allowed** option for the user to **No**.</span></span>
-   <span data-ttu-id="c2b41-123">Uživatelský účet musí být přidružen k registrované kontaktní osobě.</span><span class="sxs-lookup"><span data-stu-id="c2b41-123">The user account must be associated with a registered contact person.</span></span> <span data-ttu-id="c2b41-124">Na stránce **Uživatelé** vyberte kontaktní osobu v poli **Jméno**.</span><span class="sxs-lookup"><span data-stu-id="c2b41-124">On the **Users** page, select a contact person in the **Name** field.</span></span> <span data-ttu-id="c2b41-125">Osoba, kterou vyberete, má mít roli **Kontakt** pro příslušného dodavatele.</span><span class="sxs-lookup"><span data-stu-id="c2b41-125">The person that you select should have the **Contact** role for the relevant vendor.</span></span>

<span data-ttu-id="c2b41-126">Jestliže stejná osoba vyžaduje přístup k portálu pro dodavatele pro více dodavatelských účtů (případně pro jiné právnické osoby), jednotlivé účty dané osoby uživatele být přidruženy ke stejné registrované kontaktní osobě.</span><span class="sxs-lookup"><span data-stu-id="c2b41-126">If the same person requires access to the Vendor portal for multiple vendor accounts (for different legal entities, perhaps), each of that person's user accounts must be associated with the same registered contact person.</span></span> <span data-ttu-id="c2b41-127">Role **Dodavatel (externí)** obsahuje všechny základní funkce, které jsou zapotřebí k používání funkce, které jsou k dispozici na portálu pro dodavatele.</span><span class="sxs-lookup"><span data-stu-id="c2b41-127">The **Vendor (external)** role includes all the basic capabilities that are required in order to use the functionality that is available in the Vendor portal.</span></span> <span data-ttu-id="c2b41-128">Toto nastavení pomáhá zajistit, že uživatelské rozhraní, které externí uživatel vidí, se zaměřuje pouze na očekávané scénáře.</span><span class="sxs-lookup"><span data-stu-id="c2b41-128">This setup helps guarantee that the user interface that the external user sees is focused on the intended scenario only.</span></span>

<a name="see-also"></a><span data-ttu-id="c2b41-129">Viz také</span><span class="sxs-lookup"><span data-stu-id="c2b41-129">See also</span></span>
--------

[<span data-ttu-id="c2b41-130">Dodavatelská spolupráce</span><span class="sxs-lookup"><span data-stu-id="c2b41-130">Vendor collaboration</span></span>](collaborate-vendors-vendor-portal.md)




