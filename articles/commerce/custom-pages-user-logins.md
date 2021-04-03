---
title: Nastavení vlastních stránek pro přihlášení uživatelů
description: V tomto tématu je popsán způsob vytváření vlastních stránek v řešení Microsoft Dynamics 365 Commerce, které zpracovávají přizpůsobená přihlášení uživatelů klientů B2C (business-to-consumer) služby Azure Active Directory (Azure AD).
author: brianshook
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3328fad5328ae1954a6749f9a5eebcb71c723698
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477941"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="59608-103">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="59608-103">Set up custom pages for user sign-ins</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="59608-104">V tomto tématu je popsán způsob vytváření vlastních stránek v řešení Microsoft Dynamics 365 Commerce, které zpracovávají přizpůsobená přihlášení uživatelů klientů B2C (business-to-consumer) služby Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="59608-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

<span data-ttu-id="59608-105">Chcete-li použít vlastní stránky, které jsou vytvořeny v řešení Dynamics 365 Commerce pro zpracování toků přihlášení uživatelů, je nutné nastavit zásady Azure AD, které budou odkazovány v prostředí Commerce.</span><span class="sxs-lookup"><span data-stu-id="59608-105">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="59608-106">Pomocí aplikace Azure AD B2C můžete konfigurovat následující zásady Azure AD B2C: „Registrace a přihlášení“, „Úprava profilu“ a „Resetování hesla“.</span><span class="sxs-lookup"><span data-stu-id="59608-106">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="59608-107">Na název klienta a zásad Azure AD B2C lze poté odkazovat během procesu zřizování prováděného pro prostředí Commerce pomocí služeb Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="59608-107">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="59608-108">Vlastní stránky Commerce lze sestavit pomocí modulu přihlášení, registrace, úpravy profilu účtu nebo obnovy hesla.</span><span class="sxs-lookup"><span data-stu-id="59608-108">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="59608-109">V konfiguracích zásad Azure AD B2C na portálu Azure by pak měly být odkazovány adresy URL publikované pro tyto vlastní stránky.</span><span class="sxs-lookup"><span data-stu-id="59608-109">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="59608-110">Nastavení zásad B2C</span><span class="sxs-lookup"><span data-stu-id="59608-110">Set up B2C policies</span></span>

<span data-ttu-id="59608-111">Po nastavení klienta Azure AD B2C a jeho přidružení k prostředí Commerce přejděte na stránku **Azure AD B2C** na portálu Azure a pak v nabídce v části **Zásady** vyberte možnost **Toky uživatelů (zásady)**.</span><span class="sxs-lookup"><span data-stu-id="59608-111">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![Příkaz Toky uživatelů (zásady) v nabídce](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="59608-113">Nyní můžete nakonfigurovat toky přihlášení uživatelů „Registrace a přihlášení“ a „Resetování hesla“.</span><span class="sxs-lookup"><span data-stu-id="59608-113">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="59608-114">Konfigurace zásady „Registrace a přihlášení“</span><span class="sxs-lookup"><span data-stu-id="59608-114">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="59608-115">Chcete-li konfigurovat zásadu „Registrace a přihlášení“, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="59608-115">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="59608-116">Vyberte možnost **Nový tok uživatele** a poté na kartě **Doporučené** vyberte zásadu **Registrace a přihlášení**.</span><span class="sxs-lookup"><span data-stu-id="59608-116">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="59608-117">Zadejte název zásady (například **B2C\_1\_Registrace_a_prihlaseni**).</span><span class="sxs-lookup"><span data-stu-id="59608-117">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="59608-118">V části **Poskytovatelé identit** vyberte poskytovatele identit, kteří mají být použiti pro zásadu.</span><span class="sxs-lookup"><span data-stu-id="59608-118">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="59608-119">Musí být vybrána alespoň možnost **Registrace e-mailu**.</span><span class="sxs-lookup"><span data-stu-id="59608-119">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="59608-120">Ve sloupci **Shromáždit atribut** zaškrtněte políčka **E-mailová adresa**, **Křestní jméno** a **Příjmení**.</span><span class="sxs-lookup"><span data-stu-id="59608-120">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="59608-121">Ve sloupci **Vrátit deklaraci identity** zaškrtněte políčka **E-mailová adresa**, **Křestní jméno**, **Poskytovatelé identit**, **Příjmení** a **ID objektu uživatele**.</span><span class="sxs-lookup"><span data-stu-id="59608-121">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![Vybrané atributy a deklarace identity](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="59608-123">Zvolte **OK** pro vytvoření zásady.</span><span class="sxs-lookup"><span data-stu-id="59608-123">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="59608-124">Poklepejte na název nové zásady a poté v navigačním podokně vyberte možnost **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="59608-124">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="59608-125">Nastavte možnost **Povolit JavaScript s vynucením rozložení stránky (Preview)** na **Zapnuto**.</span><span class="sxs-lookup"><span data-stu-id="59608-125">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![Stránka vlastností pro novou zásadu](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="59608-127">Název zásady bude plně odkazován v prostředí Commerce.</span><span class="sxs-lookup"><span data-stu-id="59608-127">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="59608-128">(Předpona **B2C\_1\_** bude zahrnuta do odkazu.) Zásady nelze po vytvoření přejmenovat.</span><span class="sxs-lookup"><span data-stu-id="59608-128">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="59608-129">Pokud nahrazujete existující zásady pro vaše prostředí Commerce, můžete odstranit původní zásady a vytvořit novou zásadu se stejným názvem.</span><span class="sxs-lookup"><span data-stu-id="59608-129">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="59608-130">Je-li však prostředí již zřízeno, můžete název nové zásady odeslat prostřednictvím požadavku na službu.</span><span class="sxs-lookup"><span data-stu-id="59608-130">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="59608-131">K této zásadě se vrátíte a dokončíte nastavení po vytvoření vlastních stránek.</span><span class="sxs-lookup"><span data-stu-id="59608-131">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="59608-132">Nyní se uzavřením zásady vraťte na stránku **Toky uživatelů (zásady)** na portálu Azure.</span><span class="sxs-lookup"><span data-stu-id="59608-132">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="59608-133">Konfigurace zásady „Úprava profilu“</span><span class="sxs-lookup"><span data-stu-id="59608-133">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="59608-134">Chcete-li konfigurovat zásadu „Úprava profilu“ , postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="59608-134">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="59608-135">Vyberte možnost **Nový tok uživatele** a poté na kartě **Doporučené** vyberte zásadu **Úprava profilu**.</span><span class="sxs-lookup"><span data-stu-id="59608-135">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="59608-136">Zadejte název zásady (například **B2C\_1\_Uprava_profilu**).</span><span class="sxs-lookup"><span data-stu-id="59608-136">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="59608-137">V části **Poskytovatelé identit** vyberte poskytovatele identit, kteří mají být použiti pro zásadu.</span><span class="sxs-lookup"><span data-stu-id="59608-137">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="59608-138">Je nutné vybrat alespoň **Přihlášení k místnímu účtu**.</span><span class="sxs-lookup"><span data-stu-id="59608-138">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="59608-139">Ve sloupci **Shromáždit atribut** zaškrtněte políčka **E-mailová adresa** a **Příjmení**.</span><span class="sxs-lookup"><span data-stu-id="59608-139">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="59608-140">Ve sloupci **Vrátit deklaraci identity** zaškrtněte políčka **E-mailová adresa**, **Křestní jméno**, **Poskytovatelé identit**, **Příjmení** a **ID objektu uživatele**.</span><span class="sxs-lookup"><span data-stu-id="59608-140">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="59608-141">Zvolte **OK** pro vytvoření zásady.</span><span class="sxs-lookup"><span data-stu-id="59608-141">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="59608-142">Poklepejte na název nové zásady a poté v navigačním podokně vyberte možnost **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="59608-142">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="59608-143">Nastavte možnost **Povolit JavaScript s vynucením rozložení stránky (Preview)** na **Zapnuto**.</span><span class="sxs-lookup"><span data-stu-id="59608-143">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="59608-144">K této zásadě se vrátíte a dokončíte nastavení po vytvoření vlastních stránek.</span><span class="sxs-lookup"><span data-stu-id="59608-144">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="59608-145">Nyní se uzavřením zásady vraťte na stránku **Toky uživatelů (zásady)** na portálu Azure.</span><span class="sxs-lookup"><span data-stu-id="59608-145">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="59608-146">Konfigurace zásady „Resetování hesla“</span><span class="sxs-lookup"><span data-stu-id="59608-146">Configure the "Password reset" policy</span></span>

<span data-ttu-id="59608-147">Chcete-li konfigurovat zásadu „Resetování hesla“ , postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="59608-147">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="59608-148">Vyberte možnost **Nový tok uživatele** a poté na kartě **Preview** vyberte zásadu **Resetování hesla v1.1**.</span><span class="sxs-lookup"><span data-stu-id="59608-148">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![Zásada Resetování hesla v1.1 vybraná na kartě Preview](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="59608-150">Zadejte název zásady (například **B2C\_1\_Zapomenute_heslo**).</span><span class="sxs-lookup"><span data-stu-id="59608-150">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="59608-151">V části **Poskytovatelé identit** vyberte možnost **Resetovat heslo pomocí e-mailové adresy**.</span><span class="sxs-lookup"><span data-stu-id="59608-151">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="59608-152">Ve sloupci **Vrátit deklaraci identity** zaškrtněte políčka **E-mailová adresa**, **Křestní jméno**, **Příjmení** a **ID objektu uživatele**.</span><span class="sxs-lookup"><span data-stu-id="59608-152">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![Vybrané deklarace identity](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="59608-154">Zvolte **OK** pro vytvoření zásady.</span><span class="sxs-lookup"><span data-stu-id="59608-154">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="59608-155">Poklepejte na název nové zásady a poté v navigačním podokně vyberte možnost **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="59608-155">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="59608-156">Nastavte možnost **Povolit JavaScript s vynucením rozložení stránky (Preview)** na **Zapnuto**.</span><span class="sxs-lookup"><span data-stu-id="59608-156">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="59608-157">K této zásadě se vrátíte a dokončíte nastavení po vytvoření vlastních stránek.</span><span class="sxs-lookup"><span data-stu-id="59608-157">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="59608-158">Nyní se uzavřením zásady vraťte na stránku **Toky uživatelů (zásady)** na portálu Azure.</span><span class="sxs-lookup"><span data-stu-id="59608-158">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="59608-159">Vytvoření vlastních stránek</span><span class="sxs-lookup"><span data-stu-id="59608-159">Build the custom pages</span></span>

<span data-ttu-id="59608-160">Chcete-li vytvořit vlastní stránky pro zpracování přihlášení uživatelů, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="59608-160">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="59608-161">Ve vývojových nástrojech Commerce přejděte na web.</span><span class="sxs-lookup"><span data-stu-id="59608-161">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="59608-162">Vytvořte následujících pět šablon a pět stránek:</span><span class="sxs-lookup"><span data-stu-id="59608-162">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="59608-163">Šablona a stránka **Přihlášení**, které používají modul přihlášení.</span><span class="sxs-lookup"><span data-stu-id="59608-163">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="59608-164">Šablona a stránka **Registrace**, které používají modul registrace.</span><span class="sxs-lookup"><span data-stu-id="59608-164">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="59608-165">Šablona a stránka **Resetování hesla**, které používají modul pro resetování hesla.</span><span class="sxs-lookup"><span data-stu-id="59608-165">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="59608-166">Šablona a stránka **Ověření resetování hesla**, které používají modul pro ověření resetování hesla.</span><span class="sxs-lookup"><span data-stu-id="59608-166">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="59608-167">Šablona a stránka **Úprava profilu**, které používají modul úpravy profilu účtu.</span><span class="sxs-lookup"><span data-stu-id="59608-167">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="59608-168">Při vytváření stránek postupujte podle následujících pokynů:</span><span class="sxs-lookup"><span data-stu-id="59608-168">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="59608-169">Pro každou stránku nebo modul použijte rozložení a styl, které nejlépe vyhovují vašim obchodním požadavkům.</span><span class="sxs-lookup"><span data-stu-id="59608-169">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="59608-170">Publikujte všechny stránky a adresy URL, které jsou potřeba při nastavení Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="59608-170">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="59608-171">Po publikování stránek a adres URL shromážděte adresy URL, které je nutné použít pro konfigurace zásad Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="59608-171">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="59608-172">Přípona **?preloadscripts=true** bude přidána do každé adresy URL při jejím použití.</span><span class="sxs-lookup"><span data-stu-id="59608-172">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59608-173">Opakovaně nepoužívejte univerzální záhlaví a zápatí s relativními odkazy.</span><span class="sxs-lookup"><span data-stu-id="59608-173">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="59608-174">Vzhledem k tomu, že tyto stránky budou hostovány v doméně Azure AD B2C při jejich použití, měly by být pro všechny odkazy použity pouze absolutní adresy URL.</span><span class="sxs-lookup"><span data-stu-id="59608-174">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="59608-175">Konfigurace zásad Azure AD B2C s informacemi o vlastní stránce</span><span class="sxs-lookup"><span data-stu-id="59608-175">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="59608-176">Na portálu Azure přejděte zpět na stránku **Azure AD B2C** a poté v nabídce v části **Zásady** vyberte možnost **Toky uživatelů (zásady)**.</span><span class="sxs-lookup"><span data-stu-id="59608-176">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="59608-177">Aktualizace zásady „Registrace a přihlášení“ o informace o vlastní stránce</span><span class="sxs-lookup"><span data-stu-id="59608-177">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="59608-178">Chcete-li aktualizovat zásadu „Registrace a přihlášení“ o informace o vlastní stránce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="59608-178">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="59608-179">V zásadě **Registrace a přihlášení**, kterou jste již konfigurovali, vyberte v navigačním podokně možnost **Rozložení stránek**.</span><span class="sxs-lookup"><span data-stu-id="59608-179">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="59608-180">Vyberte rozložení **Jednotná stránka pro registraci nebo přihlášení**.</span><span class="sxs-lookup"><span data-stu-id="59608-180">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="59608-181">Nastavte volbu **Použít obsah vlastní stránky** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="59608-181">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="59608-182">Do pole **Identifikátor URI vlastní stránky** zadejte úplnou adresu URL pro přihlášení.</span><span class="sxs-lookup"><span data-stu-id="59608-182">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="59608-183">Zahrňte příponu **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="59608-183">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="59608-184">Zadejte například ``www.<my domain>.com/sign-in?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="59608-184">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="59608-185">V poli **Verze rozložení stránky (Preview)** vyberte **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="59608-185">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="59608-186">Vyberte rozložení **Stránka pro registraci místního účtu**.</span><span class="sxs-lookup"><span data-stu-id="59608-186">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="59608-187">Nastavte volbu **Použít obsah vlastní stránky** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="59608-187">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="59608-188">Do pole **Identifikátor URI vlastní stránky** zadejte úplnou adresu URL pro registraci.</span><span class="sxs-lookup"><span data-stu-id="59608-188">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="59608-189">Zahrňte příponu **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="59608-189">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="59608-190">Zadejte například ``www.<my domain>.com/sign-up?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="59608-190">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="59608-191">V poli **Verze rozložení stránky (Preview)** vyberte **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="59608-191">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="59608-192">V části **Atributy uživatele** postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="59608-192">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="59608-193">Pro atributy **E-mailová adresa**, **Křestní jméno** a **Příjmení** vyberte v poli **Vyžaduje ověření** hodnotu **Ne**.</span><span class="sxs-lookup"><span data-stu-id="59608-193">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="59608-194">Pro atributy **Křestní jméno** a **Příjmení** vyberte v poli **Volitelné** hodnotu **Ne**.</span><span class="sxs-lookup"><span data-stu-id="59608-194">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![Konfigurace zásady Stránka pro registraci místního účtu](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="59608-196">Aktualizace zásady „Úprava profilu“ o informace o vlastní stránce</span><span class="sxs-lookup"><span data-stu-id="59608-196">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="59608-197">Chcete-li aktualizovat zásadu „Editace profilu“ o informace o vlastní stránce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="59608-197">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="59608-198">V zásadě **Úprava profilu**, kterou jste již konfigurovali, vyberte v navigačním podokně možnost **Rozložení stránek**.</span><span class="sxs-lookup"><span data-stu-id="59608-198">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="59608-199">Vyberte rozložení **Stránka Úprava profilu**.</span><span class="sxs-lookup"><span data-stu-id="59608-199">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="59608-200">Nastavte volbu **Použít obsah vlastní stránky** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="59608-200">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="59608-201">Do pole **Identifikátor URI vlastní stránky** zadejte úplnou adresu URL profilu.</span><span class="sxs-lookup"><span data-stu-id="59608-201">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="59608-202">Zahrňte příponu **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="59608-202">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="59608-203">Zadejte například ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="59608-203">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="59608-204">V poli **Verze rozložení stránky (Preview)** vyberte **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="59608-204">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="59608-205">V části **Atributy uživatele** postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="59608-205">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="59608-206">Pro atributy **E-mailová adresa** a **Křestní jméno** vyberte v poli **Vyžaduje ověření** hodnotu **Ne**.</span><span class="sxs-lookup"><span data-stu-id="59608-206">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="59608-207">Pro atributy **Křestní jméno** a **Příjmení** vyberte v poli **Volitelné** hodnotu **Ne**.</span><span class="sxs-lookup"><span data-stu-id="59608-207">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="59608-208">Aktualizace zásady „Resetování hesla“ o informace o vlastní stránce</span><span class="sxs-lookup"><span data-stu-id="59608-208">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="59608-209">Chcete-li aktualizovat zásadu „Resetování hesla“ o informace o vlastní stránce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="59608-209">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="59608-210">V zásadě **Resetování hesla**, kterou jste již konfigurovali, vyberte v navigačním podokně možnost **Rozložení stránek**.</span><span class="sxs-lookup"><span data-stu-id="59608-210">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="59608-211">Vyberte rozložení **Stránka Nové heslo**.</span><span class="sxs-lookup"><span data-stu-id="59608-211">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="59608-212">Nastavte volbu **Použít obsah vlastní stránky** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="59608-212">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="59608-213">Do pole **Identifikátor URI vlastní stránky** zadejte úplnou adresu URL pro resetování hesla.</span><span class="sxs-lookup"><span data-stu-id="59608-213">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="59608-214">Zahrňte příponu **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="59608-214">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="59608-215">Zadejte například ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="59608-215">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="59608-216">V poli **Verze rozložení stránky (Preview)** vyberte **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="59608-216">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="59608-217">Vyberte rozložení **Stránk Ověření účtu**.</span><span class="sxs-lookup"><span data-stu-id="59608-217">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="59608-218">Nastavte volbu **Použít obsah vlastní stránky** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="59608-218">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="59608-219">Do pole **Identifikátor URI vlastní stránky** zadejte úplnou adresu URL pro ověření.</span><span class="sxs-lookup"><span data-stu-id="59608-219">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="59608-220">Zahrňte příponu **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="59608-220">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="59608-221">Zadejte například ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="59608-221">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="59608-222">V poli **Verze rozložení stránky (Preview)** vyberte **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="59608-222">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="59608-223">Přizpůsobení výchozích textových řetězců pro popisky a popisy</span><span class="sxs-lookup"><span data-stu-id="59608-223">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="59608-224">V knihovně modulů jsou moduly přihlášení předvyplněny výchozími textovými řetězci pro popisky a popisy.</span><span class="sxs-lookup"><span data-stu-id="59608-224">In the module library, sign-in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="59608-225">Tyto řetězce můžete upravit v sadě SDK (Software Development Kit) tak, že aktualizujete hodnoty v souboru global.json pro modul přihlášení.</span><span class="sxs-lookup"><span data-stu-id="59608-225">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="59608-226">Například výchozí text odkazu zapomenutého hesla je **Zapomenuté heslo?**.</span><span class="sxs-lookup"><span data-stu-id="59608-226">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="59608-227">Tento výchozí text je zobrazen na přihlašovací stránce.</span><span class="sxs-lookup"><span data-stu-id="59608-227">The following shows this default text on the sign-in page.</span></span>

![Výchozí text odkazu zapomenutého hesla na přihlašovací stránce](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="59608-229">V souboru global.json pro modul přihlášení v knihovně modulů je však možné upravit text na **Zapomněli jste heslo?**, jak je znázorněno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="59608-229">However, in the global.json file for the module library sign-in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![Aktualizovaný text odkazu v souboru global.json v modulu přihlášení](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="59608-231">Po aktualizaci souboru global.json a publikování změn se nový text odkazu zobrazí v modulu přihlášení, a to jak v řešení Commerce, tak na aktivní přihlašovací stránce.</span><span class="sxs-lookup"><span data-stu-id="59608-231">After you update the global.json file and publish your changes, the new link text appears in the sign-in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59608-232">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="59608-232">Additional resources</span></span>

[<span data-ttu-id="59608-233">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="59608-233">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="59608-234">Nasazení nového klienta elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="59608-234">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="59608-235">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="59608-235">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="59608-236">Přidružení webu Dynamics 365 Commerce k online kanálu</span><span class="sxs-lookup"><span data-stu-id="59608-236">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="59608-237">Správa souborů robots.txt</span><span class="sxs-lookup"><span data-stu-id="59608-237">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="59608-238">Hromadné odeslání přesměrování URL adresy</span><span class="sxs-lookup"><span data-stu-id="59608-238">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="59608-239">Nastavení klienta B2C v Commerce</span><span class="sxs-lookup"><span data-stu-id="59608-239">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="59608-240">Konfigurace několika klientů B2C v prostředí Commerce</span><span class="sxs-lookup"><span data-stu-id="59608-240">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="59608-241">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="59608-241">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="59608-242">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="59608-242">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
