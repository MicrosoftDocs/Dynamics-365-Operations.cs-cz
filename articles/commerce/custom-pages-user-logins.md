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
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5d9f2febc912b35897b063019146d219cadea1fa
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517225"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="7f481-103">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="7f481-103">Set up custom pages for user sign-ins</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7f481-104">V tomto tématu je popsán způsob vytváření vlastních stránek v řešení Microsoft Dynamics 365 Commerce, které zpracovávají přizpůsobená přihlášení uživatelů klientů B2C (business-to-consumer) služby Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="7f481-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

## <a name="overview"></a><span data-ttu-id="7f481-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="7f481-105">Overview</span></span>

<span data-ttu-id="7f481-106">Chcete-li použít vlastní stránky, které jsou vytvořeny v řešení Dynamics 365 Commerce pro zpracování toků přihlášení uživatelů, je nutné nastavit zásady Azure AD, které budou odkazovány v prostředí Commerce.</span><span class="sxs-lookup"><span data-stu-id="7f481-106">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="7f481-107">Pomocí aplikace Azure AD B2C můžete konfigurovat následující zásady Azure AD B2C: „Registrace a přihlášení“, „Úprava profilu“ a „Resetování hesla“.</span><span class="sxs-lookup"><span data-stu-id="7f481-107">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="7f481-108">Na název klienta a zásad Azure AD B2C lze poté odkazovat během procesu zřizování prováděného pro prostředí Commerce pomocí služeb Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="7f481-108">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="7f481-109">Vlastní stránky Commerce lze sestavit pomocí modulu přihlášení, registrace, úpravy profilu účtu nebo obnovy hesla.</span><span class="sxs-lookup"><span data-stu-id="7f481-109">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="7f481-110">V konfiguracích zásad Azure AD B2C na portálu Azure by pak měly být odkazovány adresy URL publikované pro tyto vlastní stránky.</span><span class="sxs-lookup"><span data-stu-id="7f481-110">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="7f481-111">Nastavení zásad B2C</span><span class="sxs-lookup"><span data-stu-id="7f481-111">Set up B2C policies</span></span>

<span data-ttu-id="7f481-112">Po nastavení klienta Azure AD B2C a jeho přidružení k prostředí Commerce přejděte na stránku **Azure AD B2C** na portálu Azure a pak v nabídce v části **Zásady** vyberte možnost **Toky uživatelů (zásady)**.</span><span class="sxs-lookup"><span data-stu-id="7f481-112">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![Příkaz Toky uživatelů (zásady) v nabídce](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="7f481-114">Nyní můžete nakonfigurovat toky přihlášení uživatelů „Registrace a přihlášení“ a „Resetování hesla“.</span><span class="sxs-lookup"><span data-stu-id="7f481-114">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="7f481-115">Konfigurace zásady „Registrace a přihlášení“</span><span class="sxs-lookup"><span data-stu-id="7f481-115">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="7f481-116">Chcete-li konfigurovat zásadu „Registrace a přihlášení“, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="7f481-116">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="7f481-117">Vyberte možnost **Nový tok uživatele** a poté na kartě **Doporučené** vyberte zásadu **Registrace a přihlášení**.</span><span class="sxs-lookup"><span data-stu-id="7f481-117">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="7f481-118">Zadejte název zásady (například **B2C\_1\_Registrace_a_prihlaseni**).</span><span class="sxs-lookup"><span data-stu-id="7f481-118">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="7f481-119">V části **Poskytovatelé identit** vyberte poskytovatele identit, kteří mají být použiti pro zásadu.</span><span class="sxs-lookup"><span data-stu-id="7f481-119">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="7f481-120">Musí být vybrána alespoň možnost **Registrace e-mailu**.</span><span class="sxs-lookup"><span data-stu-id="7f481-120">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="7f481-121">Ve sloupci **Shromáždit atribut** zaškrtněte políčka **E-mailová adresa**, **Křestní jméno** a **Příjmení**.</span><span class="sxs-lookup"><span data-stu-id="7f481-121">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="7f481-122">Ve sloupci **Vrátit deklaraci identity** zaškrtněte políčka **E-mailová adresa**, **Křestní jméno**, **Poskytovatelé identit**, **Příjmení** a **ID objektu uživatele**.</span><span class="sxs-lookup"><span data-stu-id="7f481-122">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![Vybrané atributy a deklarace identity](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="7f481-124">Zvolte **OK** pro vytvoření zásady.</span><span class="sxs-lookup"><span data-stu-id="7f481-124">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="7f481-125">Poklepejte na název nové zásady a poté v navigačním podokně vyberte možnost **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="7f481-125">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="7f481-126">Nastavte možnost **Povolit JavaScript s vynucením rozložení stránky (Preview)** na **Zapnuto**.</span><span class="sxs-lookup"><span data-stu-id="7f481-126">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![Stránka vlastností pro novou zásadu](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="7f481-128">Název zásady bude plně odkazován v prostředí Commerce.</span><span class="sxs-lookup"><span data-stu-id="7f481-128">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="7f481-129">(Předpona **B2C\_1\_** bude zahrnuta do odkazu.) Zásady nelze po vytvoření přejmenovat.</span><span class="sxs-lookup"><span data-stu-id="7f481-129">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="7f481-130">Pokud nahrazujete existující zásady pro vaše prostředí Commerce, můžete odstranit původní zásady a vytvořit novou zásadu se stejným názvem.</span><span class="sxs-lookup"><span data-stu-id="7f481-130">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="7f481-131">Je-li však prostředí již zřízeno, můžete název nové zásady odeslat prostřednictvím požadavku na službu.</span><span class="sxs-lookup"><span data-stu-id="7f481-131">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="7f481-132">K této zásadě se vrátíte a dokončíte nastavení po vytvoření vlastních stránek.</span><span class="sxs-lookup"><span data-stu-id="7f481-132">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="7f481-133">Nyní se uzavřením zásady vraťte na stránku **Toky uživatelů (zásady)** na portálu Azure.</span><span class="sxs-lookup"><span data-stu-id="7f481-133">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="7f481-134">Konfigurace zásady „Úprava profilu“</span><span class="sxs-lookup"><span data-stu-id="7f481-134">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="7f481-135">Chcete-li konfigurovat zásadu „Úprava profilu“ , postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="7f481-135">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="7f481-136">Vyberte možnost **Nový tok uživatele** a poté na kartě **Doporučené** vyberte zásadu **Úprava profilu**.</span><span class="sxs-lookup"><span data-stu-id="7f481-136">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="7f481-137">Zadejte název zásady (například **B2C\_1\_Uprava_profilu**).</span><span class="sxs-lookup"><span data-stu-id="7f481-137">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="7f481-138">V části **Poskytovatelé identit** vyberte poskytovatele identit, kteří mají být použiti pro zásadu.</span><span class="sxs-lookup"><span data-stu-id="7f481-138">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="7f481-139">Je nutné vybrat alespoň **Přihlášení k místnímu účtu**.</span><span class="sxs-lookup"><span data-stu-id="7f481-139">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="7f481-140">Ve sloupci **Shromáždit atribut** zaškrtněte políčka **E-mailová adresa** a **Příjmení**.</span><span class="sxs-lookup"><span data-stu-id="7f481-140">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="7f481-141">Ve sloupci **Vrátit deklaraci identity** zaškrtněte políčka **E-mailová adresa**, **Křestní jméno**, **Poskytovatelé identit**, **Příjmení** a **ID objektu uživatele**.</span><span class="sxs-lookup"><span data-stu-id="7f481-141">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="7f481-142">Zvolte **OK** pro vytvoření zásady.</span><span class="sxs-lookup"><span data-stu-id="7f481-142">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="7f481-143">Poklepejte na název nové zásady a poté v navigačním podokně vyberte možnost **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="7f481-143">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="7f481-144">Nastavte možnost **Povolit JavaScript s vynucením rozložení stránky (Preview)** na **Zapnuto**.</span><span class="sxs-lookup"><span data-stu-id="7f481-144">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="7f481-145">K této zásadě se vrátíte a dokončíte nastavení po vytvoření vlastních stránek.</span><span class="sxs-lookup"><span data-stu-id="7f481-145">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="7f481-146">Nyní se uzavřením zásady vraťte na stránku **Toky uživatelů (zásady)** na portálu Azure.</span><span class="sxs-lookup"><span data-stu-id="7f481-146">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="7f481-147">Konfigurace zásady „Resetování hesla“</span><span class="sxs-lookup"><span data-stu-id="7f481-147">Configure the "Password reset" policy</span></span>

<span data-ttu-id="7f481-148">Chcete-li konfigurovat zásadu „Resetování hesla“ , postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="7f481-148">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="7f481-149">Vyberte možnost **Nový tok uživatele** a poté na kartě **Preview** vyberte zásadu **Resetování hesla v1.1**.</span><span class="sxs-lookup"><span data-stu-id="7f481-149">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![Zásada Resetování hesla v1.1 vybraná na kartě Preview](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="7f481-151">Zadejte název zásady (například **B2C\_1\_Zapomenute_heslo**).</span><span class="sxs-lookup"><span data-stu-id="7f481-151">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="7f481-152">V části **Poskytovatelé identit** vyberte možnost **Resetovat heslo pomocí e-mailové adresy**.</span><span class="sxs-lookup"><span data-stu-id="7f481-152">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="7f481-153">Ve sloupci **Vrátit deklaraci identity** zaškrtněte políčka **E-mailová adresa**, **Křestní jméno**, **Příjmení** a **ID objektu uživatele**.</span><span class="sxs-lookup"><span data-stu-id="7f481-153">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![Vybrané deklarace identity](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="7f481-155">Zvolte **OK** pro vytvoření zásady.</span><span class="sxs-lookup"><span data-stu-id="7f481-155">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="7f481-156">Poklepejte na název nové zásady a poté v navigačním podokně vyberte možnost **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="7f481-156">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="7f481-157">Nastavte možnost **Povolit JavaScript s vynucením rozložení stránky (Preview)** na **Zapnuto**.</span><span class="sxs-lookup"><span data-stu-id="7f481-157">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="7f481-158">K této zásadě se vrátíte a dokončíte nastavení po vytvoření vlastních stránek.</span><span class="sxs-lookup"><span data-stu-id="7f481-158">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="7f481-159">Nyní se uzavřením zásady vraťte na stránku **Toky uživatelů (zásady)** na portálu Azure.</span><span class="sxs-lookup"><span data-stu-id="7f481-159">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="7f481-160">Vytvoření vlastních stránek</span><span class="sxs-lookup"><span data-stu-id="7f481-160">Build the custom pages</span></span>

<span data-ttu-id="7f481-161">Chcete-li vytvořit vlastní stránky pro zpracování přihlášení uživatelů, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="7f481-161">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="7f481-162">Ve vývojových nástrojech Commerce přejděte na web.</span><span class="sxs-lookup"><span data-stu-id="7f481-162">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="7f481-163">Vytvořte následujících pět šablon a pět stránek:</span><span class="sxs-lookup"><span data-stu-id="7f481-163">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="7f481-164">Šablona a stránka **Přihlášení**, které používají modul přihlášení.</span><span class="sxs-lookup"><span data-stu-id="7f481-164">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="7f481-165">Šablona a stránka **Registrace**, které používají modul registrace.</span><span class="sxs-lookup"><span data-stu-id="7f481-165">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="7f481-166">Šablona a stránka **Resetování hesla**, které používají modul pro resetování hesla.</span><span class="sxs-lookup"><span data-stu-id="7f481-166">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="7f481-167">Šablona a stránka **Ověření resetování hesla**, které používají modul pro ověření resetování hesla.</span><span class="sxs-lookup"><span data-stu-id="7f481-167">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="7f481-168">Šablona a stránka **Úprava profilu**, které používají modul úpravy profilu účtu.</span><span class="sxs-lookup"><span data-stu-id="7f481-168">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="7f481-169">Při vytváření stránek postupujte podle následujících pokynů:</span><span class="sxs-lookup"><span data-stu-id="7f481-169">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="7f481-170">Pro každou stránku nebo modul použijte rozložení a styl, které nejlépe vyhovují vašim obchodním požadavkům.</span><span class="sxs-lookup"><span data-stu-id="7f481-170">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="7f481-171">Publikujte všechny stránky a adresy URL, které jsou potřeba při nastavení Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="7f481-171">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="7f481-172">Po publikování stránek a adres URL shromážděte adresy URL, které je nutné použít pro konfigurace zásad Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="7f481-172">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="7f481-173">Přípona **?preloadscripts=true** bude přidána do každé adresy URL při jejím použití.</span><span class="sxs-lookup"><span data-stu-id="7f481-173">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7f481-174">Opakovaně nepoužívejte univerzální záhlaví a zápatí s relativními odkazy.</span><span class="sxs-lookup"><span data-stu-id="7f481-174">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="7f481-175">Vzhledem k tomu, že tyto stránky budou hostovány v doméně Azure AD B2C při jejich použití, měly by být pro všechny odkazy použity pouze absolutní adresy URL.</span><span class="sxs-lookup"><span data-stu-id="7f481-175">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="7f481-176">Konfigurace zásad Azure AD B2C s informacemi o vlastní stránce</span><span class="sxs-lookup"><span data-stu-id="7f481-176">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="7f481-177">Na portálu Azure přejděte zpět na stránku **Azure AD B2C** a poté v nabídce v části **Zásady** vyberte možnost **Toky uživatelů (zásady)**.</span><span class="sxs-lookup"><span data-stu-id="7f481-177">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="7f481-178">Aktualizace zásady „Registrace a přihlášení“ o informace o vlastní stránce</span><span class="sxs-lookup"><span data-stu-id="7f481-178">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="7f481-179">Chcete-li aktualizovat zásadu „Registrace a přihlášení“ o informace o vlastní stránce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="7f481-179">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="7f481-180">V zásadě **Registrace a přihlášení**, kterou jste již konfigurovali, vyberte v navigačním podokně možnost **Rozložení stránek**.</span><span class="sxs-lookup"><span data-stu-id="7f481-180">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="7f481-181">Vyberte rozložení **Jednotná stránka pro registraci nebo přihlášení**.</span><span class="sxs-lookup"><span data-stu-id="7f481-181">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="7f481-182">Nastavte volbu **Použít obsah vlastní stránky** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="7f481-182">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="7f481-183">Do pole **Identifikátor URI vlastní stránky** zadejte úplnou adresu URL pro přihlášení.</span><span class="sxs-lookup"><span data-stu-id="7f481-183">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="7f481-184">Zahrňte příponu **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="7f481-184">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="7f481-185">Zadejte například ``www.<my domain>.com/sign-in?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="7f481-185">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="7f481-186">V poli **Verze rozložení stránky (Preview)** vyberte **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="7f481-186">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="7f481-187">Vyberte rozložení **Stránka pro registraci místního účtu**.</span><span class="sxs-lookup"><span data-stu-id="7f481-187">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="7f481-188">Nastavte volbu **Použít obsah vlastní stránky** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="7f481-188">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="7f481-189">Do pole **Identifikátor URI vlastní stránky** zadejte úplnou adresu URL pro registraci.</span><span class="sxs-lookup"><span data-stu-id="7f481-189">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="7f481-190">Zahrňte příponu **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="7f481-190">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="7f481-191">Zadejte například ``www.<my domain>.com/sign-up?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="7f481-191">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="7f481-192">V poli **Verze rozložení stránky (Preview)** vyberte **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="7f481-192">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="7f481-193">V části **Atributy uživatele** postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="7f481-193">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="7f481-194">Pro atributy **E-mailová adresa**, **Křestní jméno** a **Příjmení** vyberte v poli **Vyžaduje ověření** hodnotu **Ne**.</span><span class="sxs-lookup"><span data-stu-id="7f481-194">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="7f481-195">Pro atributy **Křestní jméno** a **Příjmení** vyberte v poli **Volitelné** hodnotu **Ne**.</span><span class="sxs-lookup"><span data-stu-id="7f481-195">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![Konfigurace zásady Stránka pro registraci místního účtu](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="7f481-197">Aktualizace zásady „Úprava profilu“ o informace o vlastní stránce</span><span class="sxs-lookup"><span data-stu-id="7f481-197">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="7f481-198">Chcete-li aktualizovat zásadu „Editace profilu“ o informace o vlastní stránce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="7f481-198">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="7f481-199">V zásadě **Úprava profilu**, kterou jste již konfigurovali, vyberte v navigačním podokně možnost **Rozložení stránek**.</span><span class="sxs-lookup"><span data-stu-id="7f481-199">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="7f481-200">Vyberte rozložení **Stránka Úprava profilu**.</span><span class="sxs-lookup"><span data-stu-id="7f481-200">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="7f481-201">Nastavte volbu **Použít obsah vlastní stránky** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="7f481-201">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="7f481-202">Do pole **Identifikátor URI vlastní stránky** zadejte úplnou adresu URL profilu.</span><span class="sxs-lookup"><span data-stu-id="7f481-202">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="7f481-203">Zahrňte příponu **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="7f481-203">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="7f481-204">Zadejte například ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="7f481-204">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="7f481-205">V poli **Verze rozložení stránky (Preview)** vyberte **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="7f481-205">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="7f481-206">V části **Atributy uživatele** postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="7f481-206">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="7f481-207">Pro atributy **E-mailová adresa** a **Křestní jméno** vyberte v poli **Vyžaduje ověření** hodnotu **Ne**.</span><span class="sxs-lookup"><span data-stu-id="7f481-207">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="7f481-208">Pro atributy **Křestní jméno** a **Příjmení** vyberte v poli **Volitelné** hodnotu **Ne**.</span><span class="sxs-lookup"><span data-stu-id="7f481-208">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="7f481-209">Aktualizace zásady „Resetování hesla“ o informace o vlastní stránce</span><span class="sxs-lookup"><span data-stu-id="7f481-209">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="7f481-210">Chcete-li aktualizovat zásadu „Resetování hesla“ o informace o vlastní stránce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="7f481-210">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="7f481-211">V zásadě **Resetování hesla**, kterou jste již konfigurovali, vyberte v navigačním podokně možnost **Rozložení stránek**.</span><span class="sxs-lookup"><span data-stu-id="7f481-211">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="7f481-212">Vyberte rozložení **Stránka Nové heslo**.</span><span class="sxs-lookup"><span data-stu-id="7f481-212">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="7f481-213">Nastavte volbu **Použít obsah vlastní stránky** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="7f481-213">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="7f481-214">Do pole **Identifikátor URI vlastní stránky** zadejte úplnou adresu URL pro resetování hesla.</span><span class="sxs-lookup"><span data-stu-id="7f481-214">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="7f481-215">Zahrňte příponu **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="7f481-215">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="7f481-216">Zadejte například ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="7f481-216">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="7f481-217">V poli **Verze rozložení stránky (Preview)** vyberte **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="7f481-217">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="7f481-218">Vyberte rozložení **Stránk Ověření účtu**.</span><span class="sxs-lookup"><span data-stu-id="7f481-218">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="7f481-219">Nastavte volbu **Použít obsah vlastní stránky** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="7f481-219">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="7f481-220">Do pole **Identifikátor URI vlastní stránky** zadejte úplnou adresu URL pro ověření.</span><span class="sxs-lookup"><span data-stu-id="7f481-220">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="7f481-221">Zahrňte příponu **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="7f481-221">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="7f481-222">Zadejte například ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="7f481-222">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="7f481-223">V poli **Verze rozložení stránky (Preview)** vyberte **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="7f481-223">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="7f481-224">Přizpůsobení výchozích textových řetězců pro popisky a popisy</span><span class="sxs-lookup"><span data-stu-id="7f481-224">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="7f481-225">V knihovně modulů jsou moduly přihlášení předvyplněny výchozími textovými řetězci pro popisky a popisy.</span><span class="sxs-lookup"><span data-stu-id="7f481-225">In the module library, sign-in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="7f481-226">Tyto řetězce můžete upravit v sadě SDK (Software Development Kit) tak, že aktualizujete hodnoty v souboru global.json pro modul přihlášení.</span><span class="sxs-lookup"><span data-stu-id="7f481-226">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="7f481-227">Například výchozí text odkazu zapomenutého hesla je **Zapomenuté heslo?**.</span><span class="sxs-lookup"><span data-stu-id="7f481-227">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="7f481-228">Tento výchozí text je zobrazen na přihlašovací stránce.</span><span class="sxs-lookup"><span data-stu-id="7f481-228">The following shows this default text on the sign-in page.</span></span>

![Výchozí text odkazu zapomenutého hesla na přihlašovací stránce](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="7f481-230">V souboru global.json pro modul přihlášení v knihovně modulů je však možné upravit text na **Zapomněli jste heslo?**, jak je znázorněno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="7f481-230">However, in the global.json file for the module library sign-in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![Aktualizovaný text odkazu v souboru global.json v modulu přihlášení](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="7f481-232">Po aktualizaci souboru global.json a publikování změn se nový text odkazu zobrazí v modulu přihlášení, a to jak v řešení Commerce, tak na aktivní přihlašovací stránce.</span><span class="sxs-lookup"><span data-stu-id="7f481-232">After you update the global.json file and publish your changes, the new link text appears in the sign-in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7f481-233">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="7f481-233">Additional resources</span></span>

[<span data-ttu-id="7f481-234">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="7f481-234">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="7f481-235">Nasazení nového klienta elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="7f481-235">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="7f481-236">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="7f481-236">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="7f481-237">Přidružení webu Dynamics 365 Commerce k online kanálu</span><span class="sxs-lookup"><span data-stu-id="7f481-237">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="7f481-238">Správa souborů robots.txt</span><span class="sxs-lookup"><span data-stu-id="7f481-238">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="7f481-239">Hromadné odeslání přesměrování URL adresy</span><span class="sxs-lookup"><span data-stu-id="7f481-239">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="7f481-240">Nastavení klienta B2C v Commerce</span><span class="sxs-lookup"><span data-stu-id="7f481-240">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="7f481-241">Konfigurace několika klientů B2C v prostředí Commerce</span><span class="sxs-lookup"><span data-stu-id="7f481-241">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="7f481-242">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="7f481-242">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="7f481-243">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="7f481-243">Enable location-based store detection</span></span>](enable-store-detection.md)
