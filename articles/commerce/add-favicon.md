---
title: Přidání ikony oblíbené položky
description: Toto téma vysvětluje, jak přidat ikonu oblíbené položky na váš web.
author: bicyclingfool
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 58cb6c592351a96876532ef53d5d477ff93fafa1
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696984"
---
# <a name="add-a-favicon"></a><span data-ttu-id="3d800-103">Přidání ikony oblíbené položky</span><span class="sxs-lookup"><span data-stu-id="3d800-103">Add a favicon</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="3d800-104">Toto téma vysvětluje, jak přidat ikonu oblíbené položky na váš web.</span><span class="sxs-lookup"><span data-stu-id="3d800-104">This topic explains how to add a favicon to your site.</span></span>

## <a name="overview"></a><span data-ttu-id="3d800-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="3d800-105">Overview</span></span>

<span data-ttu-id="3d800-106">Ikona oblíbené položky je malý grafický soubor, který se mimo jiná umsítění zobrazuje na kartě webového prohlížeče, v adresním řádku, v historii procházení a v záložkách nebo oblíbených položkách.</span><span class="sxs-lookup"><span data-stu-id="3d800-106">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="3d800-107">Doporučujeme přidat ikonu oblíbené položky na svůj web, protože reprezentuje a posiluje vaši značku a pomáhá rozlišit váš web od jiných webů, které vaši zákazníci navštěvují.</span><span class="sxs-lookup"><span data-stu-id="3d800-107">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="3d800-108">Ačkoli lze na web přidat více ikon oblíbené položky různých velikostí a typů souborů, tohle téma ukazuje, jak přidat jednu ikonu oblíbené položky.</span><span class="sxs-lookup"><span data-stu-id="3d800-108">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="3d800-109">Stejný proces a umístění se však používají k přidání dalších ikon oblíbené položky.</span><span class="sxs-lookup"><span data-stu-id="3d800-109">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="3d800-110">Odeslání ikony oblíbené položky do kolekce prostředků webu</span><span class="sxs-lookup"><span data-stu-id="3d800-110">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="3d800-111">Chcete-li odeslat ikonu oblíbené položky do kolekce prostředků vašeho webu, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="3d800-111">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="3d800-112">Přejděte na **Prostředky \> Odeslat \> Odeslat prostředky**.</span><span class="sxs-lookup"><span data-stu-id="3d800-112">Go to **Assets \> Upload \> Upload assets**.</span></span>
1. <span data-ttu-id="3d800-113">Vyhledejte a vyberte ikonu oblíbené položky v místním systému souborů.</span><span class="sxs-lookup"><span data-stu-id="3d800-113">Find and select the favicon on your local file system.</span></span>
1. <span data-ttu-id="3d800-114">Zadejte název a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="3d800-114">Enter a title, and then select **OK**.</span></span> 
1. <span data-ttu-id="3d800-115">V podokně vlastností vpravo zkopírujte veřejnou adresu URL ikony oblíbené položky.</span><span class="sxs-lookup"><span data-stu-id="3d800-115">In the property pane on the right, copy the public URL of the favicon.</span></span>

> [!NOTE]
> <span data-ttu-id="3d800-116">Pokud nevyberete možnost **Publikovat prostředky po odeslání**, je nutné vrátit se na stránku **Prostředky** a ručně publikovat ikonu oblíbené položky později.</span><span class="sxs-lookup"><span data-stu-id="3d800-116">If you don't select the **Publish assets after upload** option, you must return to **Assets** page and manually publish the favicon later.</span></span>

## <a name="create-the-html-for-the-favicon"></a><span data-ttu-id="3d800-117">Vytvoření kódu HTML pro ikonu oblíbené položky</span><span class="sxs-lookup"><span data-stu-id="3d800-117">Create the HTML for the favicon</span></span>

<span data-ttu-id="3d800-118">Chcete-li vytvořit kód HTML pro ikonu oblíbené položky, použijte následující fragment kódu HTML.</span><span class="sxs-lookup"><span data-stu-id="3d800-118">To create the HTML for the favicon, use the following HTML snippet.</span></span> <span data-ttu-id="3d800-119">Pro atribut **href** nahraďte **"Public\_URL\_for\_your\_favicon"** veřejnou adresou URL, kterou jste dříve zkopírovali.</span><span class="sxs-lookup"><span data-stu-id="3d800-119">For the **href** attribute, replace **"Public\_URL\_for\_your\_favicon"** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a><span data-ttu-id="3d800-120">Přidání kódu HTML ikony oblíbené položky do prvků \<head\> na stránkách</span><span class="sxs-lookup"><span data-stu-id="3d800-120">Add the HTML for the favicon to the \<head\> element of your pages</span></span>

<span data-ttu-id="3d800-121">Chcete-li přidat ikonu oblíbené položky vašeho webu, použijte stejný postup, který se používá k přidání jakéhokoli typu kódu HTML nebo skriptu do prvku **\<head\>** na stránkách webu.</span><span class="sxs-lookup"><span data-stu-id="3d800-121">To add a favicon to your site, use the same procedure that is used to add any type of HTML or script to the **\<head\>** element of your site pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3d800-122">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="3d800-122">Additional resources</span></span>

[<span data-ttu-id="3d800-123">Přidání loga</span><span class="sxs-lookup"><span data-stu-id="3d800-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="3d800-124">Volba motivu webu</span><span class="sxs-lookup"><span data-stu-id="3d800-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="3d800-125">Přidání uvítací zprávy</span><span class="sxs-lookup"><span data-stu-id="3d800-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="3d800-126">Přidání oznámení o vlastnických právech</span><span class="sxs-lookup"><span data-stu-id="3d800-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="3d800-127">Přidání jazyků na web</span><span class="sxs-lookup"><span data-stu-id="3d800-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="3d800-128">Přidání kódu skriptu na webové stránky pro podporu telemetrie</span><span class="sxs-lookup"><span data-stu-id="3d800-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

