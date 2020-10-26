---
title: Stavy dokumentu a životního cyklu
description: V tomto tématu jsou popsány různé stavy dokumentu pro prvky stránky v řešení Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
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
ms.openlocfilehash: 8aad7ef8425e46182c669686710dfc178abc418f
ms.sourcegitcommit: 83ec80382bfeb693d5c5949b6f65296bd50eed12
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974023"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="802eb-103">Stavy dokumentu a životního cyklu</span><span class="sxs-lookup"><span data-stu-id="802eb-103">Document states and lifecycle</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="802eb-104">V tomto tématu jsou popsány různé stavy dokumentu pro prvky stránky v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="802eb-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="802eb-105">Popisy stavů dokumentu</span><span class="sxs-lookup"><span data-stu-id="802eb-105">Document state descriptions</span></span>

<span data-ttu-id="802eb-106">V tématu [Prvky stránky](page-elements-overview.md) jsou uvedeny různé typy dokumentů v systému správy obsahu (CMS).</span><span class="sxs-lookup"><span data-stu-id="802eb-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="802eb-107">Tyto typy dokumentů mohou mít v nástroji pro tvorbu obsahu několik stavů.</span><span class="sxs-lookup"><span data-stu-id="802eb-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="802eb-108">Stavy dokumentu pomáhají předcházet konfliktům dat a posilují správy verzí.</span><span class="sxs-lookup"><span data-stu-id="802eb-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="802eb-109">Určují, kdo může dokumenty měnit, kdy lze dokumenty změnit a kdy mohou změny zobrazit jiní uživatelé.</span><span class="sxs-lookup"><span data-stu-id="802eb-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="802eb-110">V následující tabulce jsou uvedeny možné stavy dokumentu pro prvky stránky v řešení Commerce.</span><span class="sxs-lookup"><span data-stu-id="802eb-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="802eb-111">Stav dokumentu</span><span class="sxs-lookup"><span data-stu-id="802eb-111">Document state</span></span>      | <span data-ttu-id="802eb-112">Akce konfigurátoru webu</span><span class="sxs-lookup"><span data-stu-id="802eb-112">Site builder action</span></span>        | <span data-ttu-id="802eb-113">popis</span><span class="sxs-lookup"><span data-stu-id="802eb-113">Description</span></span>                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="802eb-114">Rezervováno</span><span class="sxs-lookup"><span data-stu-id="802eb-114">Checked out</span></span>         | <span data-ttu-id="802eb-115">Vyberte možnost **Upravit** .</span><span class="sxs-lookup"><span data-stu-id="802eb-115">Select **Edit** .</span></span>           | <span data-ttu-id="802eb-116">Příslušný dokument je rezervován pro vás.</span><span class="sxs-lookup"><span data-stu-id="802eb-116">The applicable document is checked out to you.</span></span> <span data-ttu-id="802eb-117">V době, kdy je dokument v tomto stavu, nemůže být změněn jinými ověřenými uživateli systému a veškeré změny provedené v dokumentu jsou viditelné pouze pro vás.</span><span class="sxs-lookup"><span data-stu-id="802eb-117">While a document is in this state, it can't be changed by other authenticated system users, and any changes that you make to the document are visible only to you.</span></span> |
| <span data-ttu-id="802eb-118">Uloženo</span><span class="sxs-lookup"><span data-stu-id="802eb-118">Saved</span></span>               | <span data-ttu-id="802eb-119">Zvolte **Uložit** .</span><span class="sxs-lookup"><span data-stu-id="802eb-119">Select **Save** .</span></span>           | <span data-ttu-id="802eb-120">Změny provedené v rezervovaném dokumentu budou uloženy do databáze, ale dokument ještě nebyl vrácen se změnami ani publikován.</span><span class="sxs-lookup"><span data-stu-id="802eb-120">Changes that have been made to a checked-out document are saved to the database, but the document isn't yet checked in or published.</span></span> <span data-ttu-id="802eb-121">Tyto uložené změny nejsou viditelné pro ostatní ověřené uživatele systému, dokud autor nevybere **Dokončit úpravy** .</span><span class="sxs-lookup"><span data-stu-id="802eb-121">The saved changes aren't visible to other authenticated system users until the author selects **Finish editing** .</span></span> <span data-ttu-id="802eb-122">Nejsou viditelné pro externí uživatele, dokud není položka publikována.</span><span class="sxs-lookup"><span data-stu-id="802eb-122">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="802eb-123">Zahozená rezervace</span><span class="sxs-lookup"><span data-stu-id="802eb-123">Discarded check out</span></span> | <span data-ttu-id="802eb-124">Vyberte **Zrušit úpravy** .</span><span class="sxs-lookup"><span data-stu-id="802eb-124">Select **Discard edits** .</span></span>  | <span data-ttu-id="802eb-125">Všechny změny v rezervovaném dokumentu budou odstraněny a položka se vrátí k poslední verzi, která byla vrácena se změnami.</span><span class="sxs-lookup"><span data-stu-id="802eb-125">All changes to the checked-out document are discarded, and the item reverts to the last version that was checked in.</span></span> |
| <span data-ttu-id="802eb-126">Vráceno</span><span class="sxs-lookup"><span data-stu-id="802eb-126">Checked in</span></span>          | <span data-ttu-id="802eb-127">Vyberte **Dokončit úpravy** .</span><span class="sxs-lookup"><span data-stu-id="802eb-127">Select **Finish editing** .</span></span> | <span data-ttu-id="802eb-128">Upravený dokument je vrácen se změnami.</span><span class="sxs-lookup"><span data-stu-id="802eb-128">The edited document is checked in.</span></span> <span data-ttu-id="802eb-129">Všechny změny jsou viditelné pro ostatní ověřené uživatele systému a tito uživatelé pak mohou dokument upravovat.</span><span class="sxs-lookup"><span data-stu-id="802eb-129">All changes are visible to other authenticated system users, and those users can then edit the document.</span></span> <span data-ttu-id="802eb-130">Při každém vrácení se změnami se vytvoří záznam verze dokumentu v historii položky.</span><span class="sxs-lookup"><span data-stu-id="802eb-130">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="802eb-131">Publikováno</span><span class="sxs-lookup"><span data-stu-id="802eb-131">Published</span></span>           | <span data-ttu-id="802eb-132">Zvolte **Publikovat** .</span><span class="sxs-lookup"><span data-stu-id="802eb-132">Select **Publish** .</span></span>        | <span data-ttu-id="802eb-133">Dokument je publikován a změny jsou vloženy do živého pracoviště a mohou být vyřízeny externími uživateli.</span><span class="sxs-lookup"><span data-stu-id="802eb-133">The document is published, and the changes are pushed to your live site and become discoverable by external users.</span></span> <span data-ttu-id="802eb-134">Položky lze publikovat pouze v případě, že byly nejprve vráceny se změnami výběrem **Dokončit úpravy** .</span><span class="sxs-lookup"><span data-stu-id="802eb-134">Items can be published only if they have first been checked in by selecting **Finish editing** .</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="802eb-135">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="802eb-135">Additional resources</span></span>

[<span data-ttu-id="802eb-136">Způsoby přidání obsahu</span><span class="sxs-lookup"><span data-stu-id="802eb-136">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="802eb-137">Glosář modelu stránky</span><span class="sxs-lookup"><span data-stu-id="802eb-137">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="802eb-138">Práce s publikovacími skupinami</span><span class="sxs-lookup"><span data-stu-id="802eb-138">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="802eb-139">Povolení a používání sdílení napříč kanály</span><span class="sxs-lookup"><span data-stu-id="802eb-139">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="802eb-140">Práce s moduly</span><span class="sxs-lookup"><span data-stu-id="802eb-140">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="802eb-141">Práce s fragmenty</span><span class="sxs-lookup"><span data-stu-id="802eb-141">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="802eb-142">Přehled šablon a rozvržení</span><span class="sxs-lookup"><span data-stu-id="802eb-142">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="802eb-143">Přizpůsobení navigace na webu</span><span class="sxs-lookup"><span data-stu-id="802eb-143">Customize site navigation</span></span>](customize-site-navigation.md)
