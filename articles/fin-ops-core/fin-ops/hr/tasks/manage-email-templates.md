---
title: Správa šablon e-mailů
description: Toto téma vysvětluje, jak spravovat e-mailové šablony.
author: andreabichsel
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMApplicationWordBookmark, HRMApplicationEmailTemplate
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b9bd15e73535f1d07b664ed659f9f15b3b0b7594
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797456"
---
# <a name="manage-email-templates"></a><span data-ttu-id="af750-103">Správa šablon e-mailů</span><span class="sxs-lookup"><span data-stu-id="af750-103">Manage email templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="af750-104">Můžete přenést informace z databáze organizace do záložek v novém dokumentu a použít je v rámci šablon, které vám pomohou efektivně komunikovat s uchazeči a kandidáty.</span><span class="sxs-lookup"><span data-stu-id="af750-104">You can transfer information from your organization's database to the bookmarks in a new document and use it in templates that help you communicate efficiently with applicants and candidates.</span></span> <span data-ttu-id="af750-105">Chcete-li to provést, vytvořte šablonu, která obsahuje nějaký standardní text a několik záložek, kam mají být vložena systémová data.</span><span class="sxs-lookup"><span data-stu-id="af750-105">To do this, you create a template that contains standard text and some bookmarks where the system data should be inserted.</span></span> <span data-ttu-id="af750-106">Můžete například vložit adresu a kontaktní informace uchazeče do dokumentu aplikace Microsoft Word, který lze použít při komunikaci s daným uchazečem.</span><span class="sxs-lookup"><span data-stu-id="af750-106">For example, you can insert address and contact information for an applicant into a Microsoft Word document that you can use when communicating with that applicant.</span></span> <span data-ttu-id="af750-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="af750-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="select-which-bookmarks-to-use-in-your-email-templates"></a><span data-ttu-id="af750-108">Výběr toho, které záložky se mají použít v šablonách pro e-mail</span><span class="sxs-lookup"><span data-stu-id="af750-108">Select which bookmarks to use in your email templates</span></span>
1. <span data-ttu-id="af750-109">V navigačním podokně přejděte na **Moduly > Lidské zdroje > Nábor > Komunikace > Záložky aplikací**.</span><span class="sxs-lookup"><span data-stu-id="af750-109">In the navigation pane, go to **Modules > Human Resources > Recruitment > Communication > Application bookmarks**.</span></span>
2. <span data-ttu-id="af750-110">Vyhledejte na seznamu požadovanou korespondenční akci a vyberte ji.</span><span class="sxs-lookup"><span data-stu-id="af750-110">In the list, find and select the desired correspondence action.</span></span>
3. <span data-ttu-id="af750-111">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="af750-111">Select **Edit**.</span></span>
4. <span data-ttu-id="af750-112">Vyberte pole, která chcete být schopni používat v šabloně e-mailu pro vybranou akci Korespondence a přesuňte je do pole Záložka.</span><span class="sxs-lookup"><span data-stu-id="af750-112">Select the fields you would like to be able to use in an email template for the selected Correspondence action and move them to the Bookmark fields.</span></span>  
5. <span data-ttu-id="af750-113">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="af750-113">Close the page.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="af750-114">Vytvoření šablonu e-mailu</span><span class="sxs-lookup"><span data-stu-id="af750-114">Create an email template</span></span>
1. <span data-ttu-id="af750-115">V navigačním podokně přejděte na **Moduly > Lidské zdroje > Nábor > Komunikace > Šablony e-mailu aplikace**.</span><span class="sxs-lookup"><span data-stu-id="af750-115">In the navigation pane, go to **Modules > Human resources > Recruitment > Communication > Application e-mail templates**.</span></span>
2. <span data-ttu-id="af750-116">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="af750-116">Select **New**.</span></span>
3. <span data-ttu-id="af750-117">V poli **Korespondenční akce** vyberte **Pohovor**.</span><span class="sxs-lookup"><span data-stu-id="af750-117">In the **Correspondence action** field, select **Interview**.</span></span> <span data-ttu-id="af750-118">Vyberte akci korespondence, která obsahuje záložky pro tento typ e-mailové komunikace.</span><span class="sxs-lookup"><span data-stu-id="af750-118">Select the correspondence action that contains the bookmarks to use for this type of email communication.</span></span>  
4. <span data-ttu-id="af750-119">Zadejte hodnotu do pole **Šablona e-mailu**.</span><span class="sxs-lookup"><span data-stu-id="af750-119">In the **E-mail template** field, type a value.</span></span>
5. <span data-ttu-id="af750-120">Zadejte hodnotu do pole **Předmět**.</span><span class="sxs-lookup"><span data-stu-id="af750-120">In the **Subject** field, type a value.</span></span>
6. <span data-ttu-id="af750-121">Zadejte hodnotu do pole **Text**.</span><span class="sxs-lookup"><span data-stu-id="af750-121">In the **Text** field, type a value.</span></span>
7. <span data-ttu-id="af750-122">Vyhledejte na seznamu požadované pole záložek a vyberte je.</span><span class="sxs-lookup"><span data-stu-id="af750-122">In the list, find and select the desired bookmark field.</span></span>
8. <span data-ttu-id="af750-123">Pokračujte v zadávání e-mailové zprávy vložením polí záložky v místě potřeby.</span><span class="sxs-lookup"><span data-stu-id="af750-123">Continue typing your email message, inserting the bookmark fields where you need them.</span></span>
9. <span data-ttu-id="af750-124">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="af750-124">Select **Save**.</span></span>

