---
title: Správa šablon e-mailů
description: Můžete přenést informace z databáze organizace do záložek v novém dokumentu a použít je v rámci šablon, které vám pomohou efektivně komunikovat s uchazeči a kandidáty.
author: ShielaSogge
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMApplicationWordBookmark, HRMApplicationEmailTemplate
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f8eface8fd47378e25c7baeca9a84fa41097dfbe
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "309603"
---
# <a name="manage-email-templates"></a><span data-ttu-id="41c5e-103">Správa šablon e-mailů</span><span class="sxs-lookup"><span data-stu-id="41c5e-103">Manage email templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="41c5e-104">Můžete přenést informace z databáze organizace do záložek v novém dokumentu a použít je v rámci šablon, které vám pomohou efektivně komunikovat s uchazeči a kandidáty.</span><span class="sxs-lookup"><span data-stu-id="41c5e-104">You can transfer information from your organization’s database to the bookmarks in a new document and use it in templates that help you communicate efficiently with applicants and candidates.</span></span> <span data-ttu-id="41c5e-105">Chcete-li to provést, vytvořte šablonu, která obsahuje nějaký standardní text a několik záložek, kam mají být vložena systémová data.</span><span class="sxs-lookup"><span data-stu-id="41c5e-105">To do this, you create a template that contains standard text and some bookmarks where the system data should be inserted.</span></span> <span data-ttu-id="41c5e-106">Můžete například vložit adresu a kontaktní informace uchazeče do dokumentu aplikace Microsoft Word, který lze použít při komunikaci s daným uchazečem.</span><span class="sxs-lookup"><span data-stu-id="41c5e-106">For example, you can insert address and contact information for an applicant into a Microsoft Word document that you can use when communicating with that applicant.</span></span> <span data-ttu-id="41c5e-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="41c5e-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="select-which-bookmarks-to-use-in-your-email-templates"></a><span data-ttu-id="41c5e-108">Výběr toho, které záložky se mají použít v šablonách pro e-mail</span><span class="sxs-lookup"><span data-stu-id="41c5e-108">Select which bookmarks to use in your email templates</span></span>
1. <span data-ttu-id="41c5e-109">Přejděte na Záložky přihlášek.</span><span class="sxs-lookup"><span data-stu-id="41c5e-109">Go to Application bookmarks.</span></span>
2. <span data-ttu-id="41c5e-110">Vyhledejte na seznamu požadovanou korespondenční akci a vyberte ji.</span><span class="sxs-lookup"><span data-stu-id="41c5e-110">In the list, find and select the desired correspondence action.</span></span>
3. <span data-ttu-id="41c5e-111">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="41c5e-111">Click Edit.</span></span>
4. <span data-ttu-id="41c5e-112">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="41c5e-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="41c5e-113">Vyberte pole, která chcete být schopni používat v šabloně e-mailu pro vybranou akci Korespondence a přesuňte je do pole Záložka.</span><span class="sxs-lookup"><span data-stu-id="41c5e-113">Select the fields you would like to be able to use in an email template for the selected Correspondence action and move them to the Bookmark fields.</span></span>  
5. <span data-ttu-id="41c5e-114">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="41c5e-114">Close the page.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="41c5e-115">Vytvoření šablony e-mailů</span><span class="sxs-lookup"><span data-stu-id="41c5e-115">Create an email template</span></span>
1. <span data-ttu-id="41c5e-116">Přejděte na Lidské zdroje > Nábor > Komunikace > Šablony e-mailových přihlášek.</span><span class="sxs-lookup"><span data-stu-id="41c5e-116">Go to Human resources > Recruitment > Communication > Application e-mail templates.</span></span>
2. <span data-ttu-id="41c5e-117">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="41c5e-117">Click New.</span></span>
3. <span data-ttu-id="41c5e-118">V poli Korespondenční akce vyberte Pohovor.</span><span class="sxs-lookup"><span data-stu-id="41c5e-118">In the Correspondence action field, select 'Interview'.</span></span>
    * <span data-ttu-id="41c5e-119">Vyberte akci korespondence, která obsahuje záložky pro tento typ e-mailové komunikace.</span><span class="sxs-lookup"><span data-stu-id="41c5e-119">Select the correspondence action that contains the bookmarks to use for this type of email communication.</span></span>  
4. <span data-ttu-id="41c5e-120">Zadejte hodnotu do pole Šablona e-mailu.</span><span class="sxs-lookup"><span data-stu-id="41c5e-120">In the E-mail template field, type a value.</span></span>
5. <span data-ttu-id="41c5e-121">Zadejte hodnotu do pole Předmět.</span><span class="sxs-lookup"><span data-stu-id="41c5e-121">In the Subject field, type a value.</span></span>
6. <span data-ttu-id="41c5e-122">Zadejte hodnotu do pole Text.</span><span class="sxs-lookup"><span data-stu-id="41c5e-122">In the Text field, type a value.</span></span>
7. <span data-ttu-id="41c5e-123">Vyhledejte na seznamu požadované pole záložek a vyberte je.</span><span class="sxs-lookup"><span data-stu-id="41c5e-123">In the list, find and select the desired bookmark field.</span></span>
8. <span data-ttu-id="41c5e-124">Pokračujte v zadávání e-mailové zprávy vložením polí záložky v místě potřeby.</span><span class="sxs-lookup"><span data-stu-id="41c5e-124">Continue typing your email message, inserting the bookmark fields where you need them.</span></span>
    * <span data-ttu-id="41c5e-125">Pokračujte v zadávání e-mailové zprávy vložením polí záložky v místě potřeby.</span><span class="sxs-lookup"><span data-stu-id="41c5e-125">Continue typing your email message inserting the bookmark fields where desired.</span></span>  
9. <span data-ttu-id="41c5e-126">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="41c5e-126">Click Save.</span></span>

