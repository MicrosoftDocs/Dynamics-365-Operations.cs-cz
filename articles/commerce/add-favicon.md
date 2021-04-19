---
title: Přidání ikony oblíbené položky
description: Toto téma vysvětluje, jak přidat ikonu oblíbené položky na váš web.
author: bicyclingfool
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9268bc74a4131256f5a2e88df833104db271b56a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797712"
---
# <a name="add-a-favicon"></a><span data-ttu-id="13352-103">Přidání ikony oblíbené položky</span><span class="sxs-lookup"><span data-stu-id="13352-103">Add a favicon</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="13352-104">Toto téma vysvětluje, jak přidat ikonu oblíbené položky na váš web.</span><span class="sxs-lookup"><span data-stu-id="13352-104">This topic explains how to add a favicon to your site.</span></span>

<span data-ttu-id="13352-105">Ikona oblíbené položky je malý grafický soubor, který se mimo jiná umsítění zobrazuje na kartě webového prohlížeče, v adresním řádku, v historii procházení a v záložkách nebo oblíbených položkách.</span><span class="sxs-lookup"><span data-stu-id="13352-105">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="13352-106">Doporučujeme přidat ikonu oblíbené položky na svůj web, protože reprezentuje a posiluje vaši značku a pomáhá rozlišit váš web od jiných webů, které vaši zákazníci navštěvují.</span><span class="sxs-lookup"><span data-stu-id="13352-106">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="13352-107">Ačkoli lze na web přidat více ikon oblíbené položky různých velikostí a typů souborů, tohle téma ukazuje, jak přidat jednu ikonu oblíbené položky.</span><span class="sxs-lookup"><span data-stu-id="13352-107">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="13352-108">Stejný proces a umístění se však používají k přidání dalších ikon oblíbené položky.</span><span class="sxs-lookup"><span data-stu-id="13352-108">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="13352-109">Odeslání ikony oblíbené položky do kolekce prostředků webu</span><span class="sxs-lookup"><span data-stu-id="13352-109">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="13352-110">Chcete-li odeslat ikonu oblíbené položky do kolekce prostředků vašeho webu, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="13352-110">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="13352-111">V levém navigačním podokně vyberte položku **Knihovna médií**.</span><span class="sxs-lookup"><span data-stu-id="13352-111">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="13352-112">Na panelu příkazů vyberte možnost **Odeslat \> Odeslání mediálních položek**.</span><span class="sxs-lookup"><span data-stu-id="13352-112">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="13352-113">V okně Průzkumník souborů přejděte na obrazový soubor ikony oblíbené položky, který chcete nahrát, vyberte jej a poté vyberte **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="13352-113">In the File Explorer window, browse to the favicon image file that you want to upload, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="13352-114">V dialogovém okně **Odeslat mediální položku** zadejte požadovaný název a alternativní text.</span><span class="sxs-lookup"><span data-stu-id="13352-114">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="13352-115">Chcete-li publikovat obrázky ihned po odeslání, zaškrtněte políčko **Publikovat mediální položky po odeslání**.</span><span class="sxs-lookup"><span data-stu-id="13352-115">If you want to publish the image immediately after upload, select the **Publish media items after upload** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="13352-116">Pokud nezaškrtnete políčko **Publikovat prostředky po odeslání**, je nutné vrátit se na stránku **Prostředky** a ručně publikovat ikonu oblíbené položky později.</span><span class="sxs-lookup"><span data-stu-id="13352-116">If you don't select the **Publish media items after upload** check box, you must return to **Media items** page and manually publish the favicon later.</span></span>

1. <span data-ttu-id="13352-117">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="13352-117">Select **OK**.</span></span>
1. <span data-ttu-id="13352-118">V podokně vlastností vpravo zkopírujte veřejnou adresu URL ikony oblíbené položky.</span><span class="sxs-lookup"><span data-stu-id="13352-118">In the property pane on the right, copy the public URL of the favicon.</span></span> <span data-ttu-id="13352-119">Tuto adresu URL budete později používat.</span><span class="sxs-lookup"><span data-stu-id="13352-119">You will use this URL later.</span></span>

## <a name="create-the-html-for-your-favicon"></a><span data-ttu-id="13352-120">Vytvoření kódu HTML pro ikonu oblíbené položky</span><span class="sxs-lookup"><span data-stu-id="13352-120">Create the HTML for your favicon</span></span>

<span data-ttu-id="13352-121">Chcete-li vytvořit kód HTML pro ikonu oblíbené položky, použijte následující řetězec HTML.</span><span class="sxs-lookup"><span data-stu-id="13352-121">To create the HTML for the favicon, use the following HTML string.</span></span> <span data-ttu-id="13352-122">Pro atribut **href** nahraďte **"Public\_URL\_for\_your\_favicon"** veřejnou adresou URL, kterou jste dříve zkopírovali.</span><span class="sxs-lookup"><span data-stu-id="13352-122">For the **href** attribute, replace **Public\_URL\_for\_your\_favicon** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-fragment-that-contains-a-metatag-for-your-favicon"></a><span data-ttu-id="13352-123">Vytvořte fragment, který obsahuje metaznačku pro vaši ikonu oblíbené položky</span><span class="sxs-lookup"><span data-stu-id="13352-123">Create a fragment that contains a metatag for your favicon</span></span>

<span data-ttu-id="13352-124">Chcete-li vytvořit fragment, který obsahuje metaznačku pro ikonu oblíbené položky, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="13352-124">To create a fragment that contains a metatag for your favicon, follow these steps.</span></span>

1. <span data-ttu-id="13352-125">Přejděte na **Fragmenty** a pak vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="13352-125">Go to **Fragments**, and select **New**.</span></span>
1. <span data-ttu-id="13352-126">V dialogovém okně **Nový fragment** vyberte jako modul, na němž je založen fragment **Metaznačky**.</span><span class="sxs-lookup"><span data-stu-id="13352-126">In the **New fragment** dialog box, select **Metatags** as the module that the fragment is based on.</span></span>
1. <span data-ttu-id="13352-127">Zadejte název fragmentu a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="13352-127">Enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="13352-128">Ve stromu hierarchie fragmentů vyberte podřízenou položku **Výchozí metaznačky**.</span><span class="sxs-lookup"><span data-stu-id="13352-128">In the fragment hierarchy tree, select the **Default metatags** child.</span></span>
1. <span data-ttu-id="13352-129">V pravém podokně pod **Metaznačky** vyberte **Přidat** a zadejte řetězec HTML, který jste pro oblíbenou položku vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="13352-129">In the right pane, under **Meta Tags**, select **Add**, and then enter the HTML string that you created earlier for the favicon.</span></span> 
1. <span data-ttu-id="13352-130">Chcete-li publikovat fragment, vyberte možnost **Dokončit úpravy** a volbou **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="13352-130">Select **Finish editing**, and then select **Publish** to publish the fragment.</span></span>

## <a name="add-the-metatag-fragment-to-the-html-head-section-of-your-pages"></a><span data-ttu-id="13352-131">Přidejte fragment s metaznačkami do sekce HTML na vašich stránkách</span><span class="sxs-lookup"><span data-stu-id="13352-131">Add the metatag fragment to the HTML head section of your pages</span></span>

<span data-ttu-id="13352-132">Pokud chcete přidat fragment metaznačky do části **hlavička** stránek, proveďte následující postup.</span><span class="sxs-lookup"><span data-stu-id="13352-132">To add the metatag fragment to the HTML **head** section of your pages, follow these steps.</span></span>

1. <span data-ttu-id="13352-133">Přejděte na **Šablony** a otevřete šablonu pro stránky, na které chcete přidat ikonu oblíbené položky. Potom vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="13352-133">Go to **Templates**, open the template for the pages that you want to add your favicon to, and then select **Edit**.</span></span>
1. <span data-ttu-id="13352-134">Ve stromu hierarchie šablon vyberte tlačítko se třemi tečkami (**...**) napravo od kontejneru **Hlavička HTML** a vyberte **Přidat fragment**.</span><span class="sxs-lookup"><span data-stu-id="13352-134">In the template hierarchy tree, select the ellipsis (**...**) button to the right of the **HTML head** container, and then select **Add fragment**.</span></span>
1. <span data-ttu-id="13352-135">V dialogovém okně **Vybrat fragment** vyberte fragment metaznačky, který jste vytvořili předtím, a pak vyberte tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="13352-135">In the **Select fragment** dialog box, select the metatag fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="13352-136">Chcete-li publikovat šablonu, vyberte možnost **Dokončit úpravy** a volbou **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="13352-136">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>

> [!NOTE]
> <span data-ttu-id="13352-137">Pokud váš web používá více než jednu šablonu, musíte do každé z nich přidat fragment s metaznačkami.</span><span class="sxs-lookup"><span data-stu-id="13352-137">If your site uses more than one template, you must add the metatags fragment to all of them.</span></span>

<span data-ttu-id="13352-138">Při náhledu stránek založených na šabloně, do které jste přidali fragment metaznaček, byste nyní měli na kartě prohlížeče vidět ikonu oblíbené položky.</span><span class="sxs-lookup"><span data-stu-id="13352-138">When you preview pages that are based on the template that you added the metatags fragment to, you should now see the favicon on the browser tab.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="13352-139">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="13352-139">Additional resources</span></span>

[<span data-ttu-id="13352-140">Přidání loga</span><span class="sxs-lookup"><span data-stu-id="13352-140">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="13352-141">Volba motivu webu</span><span class="sxs-lookup"><span data-stu-id="13352-141">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="13352-142">Práce se soubory přepisu šablon CSS</span><span class="sxs-lookup"><span data-stu-id="13352-142">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="13352-143">Přidání uvítací zprávy</span><span class="sxs-lookup"><span data-stu-id="13352-143">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="13352-144">Přidání oznámení o vlastnických právech</span><span class="sxs-lookup"><span data-stu-id="13352-144">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="13352-145">Přidání jazyků na web</span><span class="sxs-lookup"><span data-stu-id="13352-145">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="13352-146">Přidání kódu skriptu na webové stránky pro podporu telemetrie</span><span class="sxs-lookup"><span data-stu-id="13352-146">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
