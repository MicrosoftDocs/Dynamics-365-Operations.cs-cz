---
title: Konfigurace nastavení e-mailu v aplikaci Attract
description: V tomto tématu je vysvětleno, jak nakonfigurovat nastavení e-mailu odeslaného v aplikaci Microsoft Dynamics 365 Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: e641e3f0d1873d91be1a1dc9bc22eb734a2b21d5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460537"
---
# <a name="configure-email-settings-in-attract"></a><span data-ttu-id="ae66c-103">Konfigurace nastavení e-mailu v aplikaci Attract</span><span class="sxs-lookup"><span data-stu-id="ae66c-103">Configure email settings in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ae66c-104">Vaše značka vytváří vztah důvěryhodnosti a pomůže vám vytvořit vztah s uchazeči ještě než zažádají o pozice u vás.</span><span class="sxs-lookup"><span data-stu-id="ae66c-104">Your brand establishes trust and helps you build a relationship with candidates before they even apply for your positions.</span></span> <span data-ttu-id="ae66c-105">Pozitivní vnímání značky přitahuje nejlepší talenty a zvyšuje loajalitu stávajících zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="ae66c-105">Positive brand perception attracts top talent and increases the loyalty of existing employees.</span></span> <span data-ttu-id="ae66c-106">Microsoft Dynamics 365 Talent: Attract umožňuje konfigurovat e-maily tak, aby odrážely značku vaší společnosti.</span><span class="sxs-lookup"><span data-stu-id="ae66c-106">Microsoft Dynamics 365 Talent: Attract lets you configure emails so that they reflect your company's brand.</span></span> <span data-ttu-id="ae66c-107">Proto můžete poskytnout konzistentní zkušenosti uchazečům o práci při procházení procesu žádosti.</span><span class="sxs-lookup"><span data-stu-id="ae66c-107">Therefore, you can provide a consistent experience to job candidates as they progress through the application process.</span></span>

<span data-ttu-id="ae66c-108">Attract umožňuje provést následující akce:</span><span class="sxs-lookup"><span data-stu-id="ae66c-108">Attract lets you perform these actions:</span></span>

- <span data-ttu-id="ae66c-109">Konfigurace nastavení e-mailu tak, aby byl použit účet e-mailové služby Microsoft Exchange společnosti.</span><span class="sxs-lookup"><span data-stu-id="ae66c-109">Configure email settings so that your company's Microsoft Exchange email service account is used.</span></span> <span data-ttu-id="ae66c-110">Tímto způsobem uchazeči ví, že e-maily přicházejí z vaší společnosti.</span><span class="sxs-lookup"><span data-stu-id="ae66c-110">In this way, candidates know that the emails are coming from your company.</span></span> <span data-ttu-id="ae66c-111">Můžete například nakonfigurovat nastavení tak, aby uchazeči dostávali e-maily z adresy `recruiting@contoso.com` místo z adresy `contoso@microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="ae66c-111">For example, you can configure your settings so that candidates receive emails from `recruiting@contoso.com` instead of `contoso@microsoft.com`.</span></span>
- <span data-ttu-id="ae66c-112">Vytvořte konzistentní uvádění značky ve veškeré e-mailové komunikaci nastavením globálního záhlaví a zápatí pro všechny e-mailové šablony.</span><span class="sxs-lookup"><span data-stu-id="ae66c-112">Create consistent branding for all your email communications by setting a global header and footer for email templates.</span></span> 

> [!NOTE]
> <span data-ttu-id="ae66c-113">Chcete-li nastavit Attract tak, aby pro odesílání e-mailů používal účet e-mailové služby vaší společnosti, potřebujete doplněk Comprehensive hiring.</span><span class="sxs-lookup"><span data-stu-id="ae66c-113">To configure Attract so that it uses your company's email service account to send email, you need the Comprehensive hiring add-on.</span></span>

## <a name="connect-an-email-service-account"></a><span data-ttu-id="ae66c-114">Propojení účtu e-mailové služby</span><span class="sxs-lookup"><span data-stu-id="ae66c-114">Connect an email service account</span></span>

<span data-ttu-id="ae66c-115">Připojením e-mailového účtu vaší společnosti můžete vytvořit e-mailové prostředí s informacemi o vašich uchazečích o zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="ae66c-115">By connecting your company's email service account, you can create a branded email experience for your job candidates.</span></span> <span data-ttu-id="ae66c-116">Pokud účet společnosti nepřipojíte, Attract použije výchozí účet e-mailové služby společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ae66c-116">If you don't connect your company account, Attract uses the default Microsoft-branded email service account.</span></span>

1. <span data-ttu-id="ae66c-117">Zvolte tlačítko **Nastavení** (symbol ozubeného kola) v pravém horním rohu stránky a vyberte **Centrum pro správu**.</span><span class="sxs-lookup"><span data-stu-id="ae66c-117">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="ae66c-118">Na kartě **Nastavení e-mailu** v části **Účty e-mailové služby** vyberte možnost **Připojit účet společnosti**.</span><span class="sxs-lookup"><span data-stu-id="ae66c-118">On the **Email settings** tab, under **Email service accounts**, select **Connect a company account**.</span></span>

    ![Připojení účtu e-mailové služby společnosti v aplikaci Attract](./media/attract-admin-email-service-accounts.png)

    <span data-ttu-id="ae66c-120">Další informace o postupu při vytváření sdíleného e-mailového účtu naleznete v tématu [Sdílené poštovní schránky v aplikaci Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span><span class="sxs-lookup"><span data-stu-id="ae66c-120">For more information about how to create a shared email account, see [Shared mailboxes in Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span></span>

3. <span data-ttu-id="ae66c-121">V přihlašovacím okně společnosti Microsoft se přihlaste pomocí svých podnikových přihlašovacích údajů.</span><span class="sxs-lookup"><span data-stu-id="ae66c-121">In the Microsoft sign-in window, sign in by using your corporate credentials.</span></span>
4. <span data-ttu-id="ae66c-122">Pokud jste ještě nenastavili účet e-mailové služby nebo pokud chcete přidat nový, vyberte možnost **Přidat nový účet služby** a pak zadejte své e-mailové informace.</span><span class="sxs-lookup"><span data-stu-id="ae66c-122">If you haven't yet set up an email service account, or if you want to add a new one, select **Add new service account**, and then enter your email information.</span></span> <span data-ttu-id="ae66c-123">Pokud jste již nastavili účet e-mailové služby, který chcete použít, vyberte jej.</span><span class="sxs-lookup"><span data-stu-id="ae66c-123">If you've already set up the email service account that you want to use, select it.</span></span>

<span data-ttu-id="ae66c-124">Po úspěšné konfiguraci účtu e-mailové služby se tento účet zobrazí v části **Účty e-mailové služby**.</span><span class="sxs-lookup"><span data-stu-id="ae66c-124">When your email service account is successfully configured, you will see it listed under **Email service accounts**.</span></span>

## <a name="disconnect-an-email-service-account"></a><span data-ttu-id="ae66c-125">Odpojení účtu e-mailové služby</span><span class="sxs-lookup"><span data-stu-id="ae66c-125">Disconnect an email service account</span></span>

<span data-ttu-id="ae66c-126">Chcete-li přestat používat doménu společnosti v e-mailové komunikaci prostřednictvím aplikace Attract, můžete odpojit účet e-mailové služby.</span><span class="sxs-lookup"><span data-stu-id="ae66c-126">If you want to stop using your company's domain in email communications through Attract, you can disconnect an email service account.</span></span>

1. <span data-ttu-id="ae66c-127">Zvolte tlačítko **Nastavení** (symbol ozubeného kola) v pravém horním rohu stránky a vyberte **Centrum pro správu**.</span><span class="sxs-lookup"><span data-stu-id="ae66c-127">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="ae66c-128">Na kartě **Nastavení e-mailu** vyberte v části **Účty e-mailové služby** tlačítko **Další** (tři svislé tečky) vedle účtu e-mailové služby, který chcete odpojit.</span><span class="sxs-lookup"><span data-stu-id="ae66c-128">On the **Email settings** tab, under **Email service accounts**, select the **More** button (three vertical dots) next to the email service account that you want to disconnect.</span></span>
3. <span data-ttu-id="ae66c-129">Vyberte **Odpojit e-mailový účet**.</span><span class="sxs-lookup"><span data-stu-id="ae66c-129">Select **Disconnect email account**.</span></span>

    ![Odpojení účtu e-mailové služby společnosti v aplikaci Attract](./media/attract-admin-disconnect-email-account.png)

4. <span data-ttu-id="ae66c-131">Po zobrazení výzvy k potvrzení operace vyberte možnost **Odpojit.**</span><span class="sxs-lookup"><span data-stu-id="ae66c-131">When you're prompted to confirm the operation, select **Disconnect**.</span></span>

    ![Potvrzení odpojení účtu e-mailové služby společnosti v aplikaci Attract](./media/attract-admin-email-confirm-disconnect.png)

<span data-ttu-id="ae66c-133">Pokud nepřipojíte jiný účet e-mailové služby, budou e-maily odeslané z aplikace Attract používat výchozí e-mailovou službu se značkou Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ae66c-133">If you don't connect a different email service account, emails that are sent from Attract will use the default Microsoft-branded email service account.</span></span>

## <a name="configure-email-template-settings"></a><span data-ttu-id="ae66c-134">Konfigurace nastavení šablony</span><span class="sxs-lookup"><span data-stu-id="ae66c-134">Configure email template settings</span></span>

<span data-ttu-id="ae66c-135">Můžete odeslat obrázek loga společnosti a další informace jako značku pro vaše e-mailové zprávy.</span><span class="sxs-lookup"><span data-stu-id="ae66c-135">You can upload an image of your company's logo and other information as a branded header for your emails.</span></span> <span data-ttu-id="ae66c-136">Můžete také poskytnout odkazy na zásady ochrany osobních údajů a podmínky použití v zápatích e-mailů.</span><span class="sxs-lookup"><span data-stu-id="ae66c-136">You can also provide links to your privacy policy and terms of use in email footers.</span></span>

> [!NOTE]
> <span data-ttu-id="ae66c-137">Musíte dodržovat platné zákony vaší země nebo oblasti a také země nebo oblasti, které se vztahují na příjemce e-mailu.</span><span class="sxs-lookup"><span data-stu-id="ae66c-137">You must comply with all applicable laws of your country or region, and also the country or region that governs the email recipient.</span></span> <span data-ttu-id="ae66c-138">Tyto zákony zahrnují předpisy o ochraně proti nevyžádané poště.</span><span class="sxs-lookup"><span data-stu-id="ae66c-138">These laws include anti-spam regulations.</span></span>

1. <span data-ttu-id="ae66c-139">Zvolte tlačítko **Nastavení** (symbol ozubeného kola) v pravém horním rohu stránky a vyberte **Centrum pro správu**.</span><span class="sxs-lookup"><span data-stu-id="ae66c-139">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="ae66c-140">Na kartě **Nastavení e-mailu** ve skupinovém rámečku **nastavení šablony e-mailu** přetáhněte obrázek, který chcete použít jako záhlaví e-mailu, do pole s obrázkem, nebo klepnutím na tlačítko v poli obrázek vyhledejte soubor.</span><span class="sxs-lookup"><span data-stu-id="ae66c-140">On the **Email settings** tab, under **Email template settings**, drag the image that you want to use as your email header into the image box, or click in the image box to browse for the file.</span></span> <span data-ttu-id="ae66c-141">Chcete-li nahradit existující obrázek, musíte nejprve vybrat **odebrat** vedle obrázku.</span><span class="sxs-lookup"><span data-stu-id="ae66c-141">To replace an existing image, you must first select **Remove** next to it.</span></span> <span data-ttu-id="ae66c-142">Obraz musí být soubor JPEG, JPG, PNG nebo SVG.</span><span class="sxs-lookup"><span data-stu-id="ae66c-142">The image must be a JPEG, JPG, PNG, or SVG file.</span></span> <span data-ttu-id="ae66c-143">Doporučená velikost pro obrázky je mezi 25 a 800 pixelů široká a mezi 25 a 150 pixely vysoká.</span><span class="sxs-lookup"><span data-stu-id="ae66c-143">The recommended size for images is between 25 and 800 pixels wide, and between 25 and 150 pixels high.</span></span> <span data-ttu-id="ae66c-144">Maximální velikost souboru pro záhlaví je 1 megabajt (MB).</span><span class="sxs-lookup"><span data-stu-id="ae66c-144">The maximum file size for the header is 1 megabyte (MB).</span></span>

    ![Přidání obrázku pro záhlaví e-mailu vaší společnosti](./media/attract-admin-email-header.png)

3. <span data-ttu-id="ae66c-146">V části **Zásady ochrany osobních údajů pro komunikace** uveďte odkaz na zásady ochrany osobních údajů společnosti.</span><span class="sxs-lookup"><span data-stu-id="ae66c-146">Under **Your Privacy policy for communications**, provide a link to your company's privacy policy.</span></span> <span data-ttu-id="ae66c-147">V části **Podmínky pro komunikaci** zadejte odkaz na podmínky použití ve vaší společnosti.</span><span class="sxs-lookup"><span data-stu-id="ae66c-147">Under **Your Terms and conditions for communication**, provide a link to your company's terms of use.</span></span>

    ![Přidání odkazů na zásady ochrany osobních údajů společnosti a podmínky použití zápatí e-mailu](./media/attract-admin-email-footer.png)

4. <span data-ttu-id="ae66c-149">Výběrem možnosti **Uložit** uložte nastavení šablony e-mailu.</span><span class="sxs-lookup"><span data-stu-id="ae66c-149">Select **Save** to save your email template settings.</span></span>
