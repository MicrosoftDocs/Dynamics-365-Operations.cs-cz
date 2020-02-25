---
title: Stavy dokumentu a životního cyklu
description: V tomto tématu jsou popsány různé stavy dokumentu pro prvky stránky v řešení Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b4f1c462f734b2d58843308f0f877fe18a4d9af7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002974"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="cb02c-103">Stavy dokumentu a životního cyklu</span><span class="sxs-lookup"><span data-stu-id="cb02c-103">Document states and lifecycle</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="cb02c-104">V tomto tématu jsou popsány různé stavy dokumentu pro prvky stránky v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cb02c-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="cb02c-105">Popisy stavů dokumentu</span><span class="sxs-lookup"><span data-stu-id="cb02c-105">Document state descriptions</span></span>

<span data-ttu-id="cb02c-106">V tématu [Prvky stránky](page-elements-overview.md) jsou uvedeny různé typy dokumentů v systému správy obsahu (CMS).</span><span class="sxs-lookup"><span data-stu-id="cb02c-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="cb02c-107">Tyto typy dokumentů mohou mít v nástroji pro tvorbu obsahu několik stavů.</span><span class="sxs-lookup"><span data-stu-id="cb02c-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="cb02c-108">Stavy dokumentu pomáhají předcházet konfliktům dat a posilují správy verzí.</span><span class="sxs-lookup"><span data-stu-id="cb02c-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="cb02c-109">Určují, kdo může dokumenty měnit, kdy lze dokumenty změnit a kdy mohou změny zobrazit jiní uživatelé.</span><span class="sxs-lookup"><span data-stu-id="cb02c-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="cb02c-110">V následující tabulce jsou uvedeny možné stavy dokumentu pro prvky stránky v řešení Commerce.</span><span class="sxs-lookup"><span data-stu-id="cb02c-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="cb02c-111">Stav dokumentu</span><span class="sxs-lookup"><span data-stu-id="cb02c-111">Document state</span></span> | <span data-ttu-id="cb02c-112">Popis</span><span class="sxs-lookup"><span data-stu-id="cb02c-112">Description</span></span> |
|---|---|
| <span data-ttu-id="cb02c-113">Rezervováno</span><span class="sxs-lookup"><span data-stu-id="cb02c-113">Checked out</span></span> | <span data-ttu-id="cb02c-114">Je-li položka CMS rezervována pro vás, nemůže být upravována jinými ověřenými uživateli systému.</span><span class="sxs-lookup"><span data-stu-id="cb02c-114">When a CMS item is checked out to you, it can't be edited by any other authenticated system users.</span></span> <span data-ttu-id="cb02c-115">Jakékoli změny položky, které provedete, budou viditelné pouze pro vás.</span><span class="sxs-lookup"><span data-stu-id="cb02c-115">Any changes that you make to the item are visible only to you.</span></span> |
| <span data-ttu-id="cb02c-116">Vráceno</span><span class="sxs-lookup"><span data-stu-id="cb02c-116">Checked in</span></span> | <span data-ttu-id="cb02c-117">Při vrácení položky CMS se změnami jsou všechny změny viditelné pro ostatní ověřené uživatele systému a tito uživatelé si pak mohou položku rezervovat a upravit.</span><span class="sxs-lookup"><span data-stu-id="cb02c-117">When a CMS item is checked in, all changes are visible to other authenticated system users, and those users can then check out the item and edit it.</span></span> <span data-ttu-id="cb02c-118">Při každém vrácení se změnami se vytvoří záznam verze dokumentu v historii položky.</span><span class="sxs-lookup"><span data-stu-id="cb02c-118">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="cb02c-119">Publikováno</span><span class="sxs-lookup"><span data-stu-id="cb02c-119">Published</span></span> | <span data-ttu-id="cb02c-120">Je-li publikována položka CMS, je vložena na živý web a může být v Internetu zjistitelná neověřenými externími uživateli.</span><span class="sxs-lookup"><span data-stu-id="cb02c-120">When a CMS item is published, it's pushed to your live site and becomes discoverable on the internet by non-authenticated external users.</span></span> <span data-ttu-id="cb02c-121">Položky lze publikovat pouze v případě, že byly vráceny se změnami.</span><span class="sxs-lookup"><span data-stu-id="cb02c-121">Items can be published only if they have been checked in.</span></span> |
| <span data-ttu-id="cb02c-122">Uloženo</span><span class="sxs-lookup"><span data-stu-id="cb02c-122">Saved</span></span> | <span data-ttu-id="cb02c-123">Změny provedené u rezervované položky CMS lze uložit do CMS před tím, než je položka vrácena se změnami nebo publikována.</span><span class="sxs-lookup"><span data-stu-id="cb02c-123">Changes that have been made to a checked-out CMS item can be saved to the CMS before the item is checked in or published.</span></span> <span data-ttu-id="cb02c-124">Tyto uložené změny nejsou viditelné pro ostatní ověřené uživatele systému, dokud není položka vrácena se změnami.</span><span class="sxs-lookup"><span data-stu-id="cb02c-124">These saved changes aren't visible to other authenticated system users until the item is checked in.</span></span> <span data-ttu-id="cb02c-125">Nejsou viditelné pro externí uživatele, dokud není položka publikována.</span><span class="sxs-lookup"><span data-stu-id="cb02c-125">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="cb02c-126">Zahozená rezervace</span><span class="sxs-lookup"><span data-stu-id="cb02c-126">Discarded check out</span></span> | <span data-ttu-id="cb02c-127">Pokud dojde k zahození rezervované položky CMS, budou odstraněny všechny uložené změny a položka bude vrácena na verzi, která byla naposledy vrácena se změnami.</span><span class="sxs-lookup"><span data-stu-id="cb02c-127">When a checked-out CMS item is discarded, all saved changes are deleted, and the item reverts to the version that was most recently checked in.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="cb02c-128">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="cb02c-128">Additional resources</span></span>

[<span data-ttu-id="cb02c-129">Způsoby přidání obsahu</span><span class="sxs-lookup"><span data-stu-id="cb02c-129">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="cb02c-130">Glosář modelu stránky</span><span class="sxs-lookup"><span data-stu-id="cb02c-130">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="cb02c-131">Práce se skupinami publikování</span><span class="sxs-lookup"><span data-stu-id="cb02c-131">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="cb02c-132">Práce s moduly</span><span class="sxs-lookup"><span data-stu-id="cb02c-132">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="cb02c-133">Práce s fragmenty</span><span class="sxs-lookup"><span data-stu-id="cb02c-133">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="cb02c-134">Přehled šablon a rozvržení</span><span class="sxs-lookup"><span data-stu-id="cb02c-134">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="cb02c-135">Přizpůsobení navigace na webu</span><span class="sxs-lookup"><span data-stu-id="cb02c-135">Customize site navigation</span></span>](customize-site-navigation.md)
