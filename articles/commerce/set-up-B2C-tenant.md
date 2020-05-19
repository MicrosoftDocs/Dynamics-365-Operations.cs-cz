---
title: Nastavení klienta B2C v Commerce
description: Tohle téma popisuje, jak nastavíte své klienty Azure Active Directory (Azure AD) business-to-consumer (B2C) pro ověření webu uživatele v aplikaci Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: BriShoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: 22d62419c703c64470723cf82864a4782306ea8a
ms.sourcegitcommit: 1b00e21faf89de8b3450936253a4c02cb4d12a3d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2020
ms.locfileid: "3295262"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a><span data-ttu-id="626b7-103">Nastavení klienta B2C v Commerce</span><span class="sxs-lookup"><span data-stu-id="626b7-103">Set up a B2C tenant in Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="626b7-104">Tohle téma popisuje, jak nastavíte své klienty Azure Active Directory (Azure AD) business-to-consumer (B2C) pro ověření webu uživatele v aplikaci Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="626b7-104">This topic describes how to set up your Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants for user site authentication in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="626b7-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="626b7-105">Overview</span></span>

<span data-ttu-id="626b7-106">Dynamics 365 Commerce používá Azure AD B2C pro podporu toků přihlašovacích údajů a ověřování uživatele.</span><span class="sxs-lookup"><span data-stu-id="626b7-106">Dynamics 365 Commerce uses Azure AD B2C to support user credential and authentication flows.</span></span> <span data-ttu-id="626b7-107">Uživatel se může registrovat, přihlásit a obnovit své heslo pomocí těchto toků.</span><span class="sxs-lookup"><span data-stu-id="626b7-107">A user can sign up, sign in, and reset their password through these flows.</span></span> <span data-ttu-id="626b7-108">Azure AD B2C ukládá citlivé informace o ověřování uživatele, například jeho uživatelské jméno a heslo.</span><span class="sxs-lookup"><span data-stu-id="626b7-108">Azure AD B2C stores sensitive user authentication information, such as username and password.</span></span> <span data-ttu-id="626b7-109">Záznam uživatele v klientovi B2C uloží buď záznam místního účtu B2C nebo záznam zprostředkovatele sociální identity B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-109">The user record in the B2C tenant will store either a B2C local account record or a B2C social identity provider record.</span></span> <span data-ttu-id="626b7-110">Tyto záznamy B2C budou odkazovat zpět na záznam odběratele v prostředí Commerce.</span><span class="sxs-lookup"><span data-stu-id="626b7-110">These B2C records will link back to the customer record in the Commerce environment.</span></span>

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a><span data-ttu-id="626b7-111">Vytvoření nebo připojení ke stávajícími klientovi AAD B2C v portálu Azure</span><span class="sxs-lookup"><span data-stu-id="626b7-111">Create or link to an existing AAD B2C tenant in the Azure portal</span></span>

1. <span data-ttu-id="626b7-112">Přihlaste se do [portálu Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="626b7-112">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="626b7-113">Z nabídky portálu Azure vyberte možnost **Vytvořit prostředek**.</span><span class="sxs-lookup"><span data-stu-id="626b7-113">From the Azure portal menu, select **Create a resource**.</span></span> <span data-ttu-id="626b7-114">Ujistěte se, že používáte předplatné a adresář, který bude připojen k vašemu prostředí Commerce.</span><span class="sxs-lookup"><span data-stu-id="626b7-114">Be sure to use the subscription and directory that will be connected with your Commerce environment.</span></span>

    ![Vytvoření prostředku na portálu Azure](./media/B2CImage_1.png)

1. <span data-ttu-id="626b7-116">Přejděte na **Identita \> Azure Active Directory B2C**.</span><span class="sxs-lookup"><span data-stu-id="626b7-116">Go to **Identity \> Azure Active Directory B2C**.</span></span>
1. <span data-ttu-id="626b7-117">Na stránce **Vytvoření nového klienta B2C nebo připojení k existujícímu klientovi** použijte jednu z následujících možností, které nejlépe vyhovují potřebám vaší společnosti:</span><span class="sxs-lookup"><span data-stu-id="626b7-117">Once on the **Create New B2C Tenant or Link to existing Tenant** page, use one of the options below that best suits your company's needs:</span></span>

    - <span data-ttu-id="626b7-118">**Vytvořit nového klienta Azure AD B2C**: Touto možností vytvoříte nového klienta AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-118">**Create a new Azure AD B2C Tenant**: Use this option to create a new AAD B2C tenant.</span></span>
        1. <span data-ttu-id="626b7-119">Vyberte **Vytvořit nového klienta Azure AD B2C**.</span><span class="sxs-lookup"><span data-stu-id="626b7-119">Select **Create a new Azure AD B2C Tenant**.</span></span>
        1. <span data-ttu-id="626b7-120">Pro **Název organizace** zadejte název organizace.</span><span class="sxs-lookup"><span data-stu-id="626b7-120">Under **Organization name**, enter the organization name.</span></span>
        1. <span data-ttu-id="626b7-121">Pro **Počáteční název domény** zadejte počáteční název domény.</span><span class="sxs-lookup"><span data-stu-id="626b7-121">Under **Initial domain name**, enter the initial domain name.</span></span>
        1. <span data-ttu-id="626b7-122">Pro **Země nebo oblast** vyberte zemi nebo oblast.</span><span class="sxs-lookup"><span data-stu-id="626b7-122">For **Country or region**, select the country or region.</span></span>
        1. <span data-ttu-id="626b7-123">Volbou **Vytvořit** vytvoříte klienta.</span><span class="sxs-lookup"><span data-stu-id="626b7-123">Select **Create** to create the tenant.</span></span>

     ![Vytvoření nového klienta Azure AD](./media/B2CImage_2.png)

     - <span data-ttu-id="626b7-125">**Propojit existujícího klienta Azure AD B2C s mým předplatným Azure**: Tuto možnost použijte, pokud již existuje klient Azure AD B2C, který chcete propojit.</span><span class="sxs-lookup"><span data-stu-id="626b7-125">**Link an existing Azure AD B2C Tenant to my Azure subscription**: Use this option if you already have an Azure AD B2C tenant you want to link to.</span></span>
        1. <span data-ttu-id="626b7-126">Vyberte **Propojit existujícího klienta Azure AD B2C s mým předplatným Azure**.</span><span class="sxs-lookup"><span data-stu-id="626b7-126">Select **Link an existing Azure AD B2C Tenant to my Azure subscription**.</span></span>
        1. <span data-ttu-id="626b7-127">Pro **Klient Azure AD B2C** vyberte příslušného klienta B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-127">For **Azure AD B2C Tenant**, select the appropriate B2C tenant.</span></span> <span data-ttu-id="626b7-128">Pokud se v oblasti výběru zobrazí zpráva „Nebyly nalezeni žádní oprávnění klienti B2C“, nemáte žádného existující oprávněného klienta B2C a budete muset vytvořit nového.</span><span class="sxs-lookup"><span data-stu-id="626b7-128">If the message "No eligible B2C Tenants found" appears in the selection box, you do not have an existing eligible B2C tenant and will need to create a new one.</span></span>
        1. <span data-ttu-id="626b7-129">Pro **Skupina prostředků** vyberte možnost **Vytvořit novou**.</span><span class="sxs-lookup"><span data-stu-id="626b7-129">For **Resource group**, select **Create new**.</span></span> <span data-ttu-id="626b7-130">Zadejte **Název** pro skupinu prostředků, která bude obsahovat klienta, vyberte **Umístění skupiny prostředků** a pak vyberte možnost **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="626b7-130">Enter a **Name** for the resource group that will contain the tenant, select the **Resource group location**, and then select **Create**.</span></span>

    ![Propojení existujícího klienta Azure AD B2C s předplatným Azure](./media/B2CImage_3.png)

1. <span data-ttu-id="626b7-132">Po vytvoření nového adresáře Azure AD B2C (což může chvíli trvat) se na řídicím panelu zobrazí odkaz na nový adresář.</span><span class="sxs-lookup"><span data-stu-id="626b7-132">Once the new Azure AD B2C directory is created (this may take a few moments), a link to the new directory will appear on the dashboard.</span></span> <span data-ttu-id="626b7-133">Tento odkaz vás přesměruje na stránku „Vítá vás Azure Active Directory B2C“.</span><span class="sxs-lookup"><span data-stu-id="626b7-133">This link will direct you to the "Welcome to Azure Active Directory B2C" page.</span></span>

    ![Odkaz na nový adresář AAD](./media/B2CImage_4.png)

> [!NOTE]
> <span data-ttu-id="626b7-135">Pokud máte více předplatných v rámci účtu Azure nebo jste zřídili klienta B2C bez propojení s aktivním předplatným, banner **Řešení potíží** vás nasměruje k propojení klienta a předplatného.</span><span class="sxs-lookup"><span data-stu-id="626b7-135">If you have multiple subscriptions within your Azure account or have set up the B2C tenant without linking to an active subscription, a **Troubleshoot** banner will direct you to link the tenant to a subscription.</span></span> <span data-ttu-id="626b7-136">Vyberte zprávu řešení potíží a podle pokynů vyřešte problém s předplatným.</span><span class="sxs-lookup"><span data-stu-id="626b7-136">Select the troubleshooting message and follow the instructions to resolve the subscription issue.</span></span>

<span data-ttu-id="626b7-137">Na následujícím obrázku je znázorněn příklad banneru **Řešení potíží** v Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-137">The following image shows an example of an Azure AD B2C **Troubleshoot** banner.</span></span>

![Upozornění, že adresář nemá žádné aktivní předplatné](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a><span data-ttu-id="626b7-139">Vytvoření aplikace B2C</span><span class="sxs-lookup"><span data-stu-id="626b7-139">Create the B2C application</span></span>

<span data-ttu-id="626b7-140">Po vytvoření klienta B2C vytvoříte aplikaci B2C s klientem pro interakci s akcemi Commerce.</span><span class="sxs-lookup"><span data-stu-id="626b7-140">Once the B2C tenant has been created, you will create a B2C application within the tenant to interact with the Commerce actions.</span></span>

<span data-ttu-id="626b7-141">Chcete-li vytvořit aplikaci B2C, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="626b7-141">To create the B2C application, follow these steps.</span></span>

1. <span data-ttu-id="626b7-142">Na portálu Azure vyberte možnost **Aplikace** a pak vyberte možnost **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="626b7-142">In the Azure portal, select **Applications** and then select **Add**.</span></span>
1. <span data-ttu-id="626b7-143">V poli **Název** zadejte název požadované aplikace AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-143">Under **Name**, enter the name of the desired AAD B2C application.</span></span>
1. <span data-ttu-id="626b7-144">V části **Webová aplikace/webové rozhraní API** vyberte pro **Zahrnout webovou aplikaci/webové rozhraní API** možnost **Ano**.</span><span class="sxs-lookup"><span data-stu-id="626b7-144">Under **Web App/Web API**, for **Include web app / web API**, select **Yes**.</span></span>
1. <span data-ttu-id="626b7-145">Pro **Povolit implicitní tok** vyberte možnost **Ano** (výchozí hodnota).</span><span class="sxs-lookup"><span data-stu-id="626b7-145">For **Allow implicit flow**, select **Yes** (the default value).</span></span>
1. <span data-ttu-id="626b7-146">Pro **Adresa URL odpovědi** zadejte vyhrazené adresy URL pro odpovědi.</span><span class="sxs-lookup"><span data-stu-id="626b7-146">Under **Reply URL**, enter your dedicated reply URLs.</span></span> <span data-ttu-id="626b7-147">Viz [Adresy URL pro odpovědi](#reply-urls) níže, kde najdete informace o adresách URL odpovědí a jak je naformátovat.</span><span class="sxs-lookup"><span data-stu-id="626b7-147">See [Reply URLs](#reply-urls) below for information on reply URLs and how to format them here.</span></span>
1. <span data-ttu-id="626b7-148">Pro **Zahrnout nativního klienta** vyberte možnost **Ne** (výchozí hodnota).</span><span class="sxs-lookup"><span data-stu-id="626b7-148">For **Include native client**, select **No** (the default value).</span></span>
1. <span data-ttu-id="626b7-149">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="626b7-149">Select **Create**.</span></span>

### <a name="reply-urls"></a><span data-ttu-id="626b7-150">Adresy URL pro odpovědi</span><span class="sxs-lookup"><span data-stu-id="626b7-150">Reply URLs</span></span>

<span data-ttu-id="626b7-151">Adresy URL pro odpovědi jsou důležité, protože poskytují seznam povolených návratových domén, když váš web volá Azure AD B2C pro ověření uživatele.</span><span class="sxs-lookup"><span data-stu-id="626b7-151">Reply URLs are important as they provide an allow list of the return domains when your site calls Azure AD B2C to authenticate a user.</span></span> <span data-ttu-id="626b7-152">To umožňuje vrátit ověřeného uživatele zpět do domény, ze které se přihlásí (doména vašeho webu).</span><span class="sxs-lookup"><span data-stu-id="626b7-152">This permits the return of the authenticated user back to the domain from which they are signing into (your site domain).</span></span> 

<span data-ttu-id="626b7-153">V poli **Adresa URL odpovědi** na obrazovce **Azure AD B2C – aplikace \> Nová aplikace** je nutné přidat samostatné řádky pro doménu vašeho webu a (po zřízení vašeho prostředí) adresu URL generovanou řešením Commerce.</span><span class="sxs-lookup"><span data-stu-id="626b7-153">In the **Reply URL** box on the **Azure AD B2c - Applications \> New application** screen, you need to add separate lines for both your site domain and (once your environment is provisioned) the Commerce-generated URL.</span></span> <span data-ttu-id="626b7-154">Tyto adresy URL musí vždy používat platný formát adresy URL a musí to být pouze základní adresy URL (bez koncového lomítka nebo cesty).</span><span class="sxs-lookup"><span data-stu-id="626b7-154">These URLs must always use a valid URL format and must be base URLs only (no trailing forward slashes or paths).</span></span> <span data-ttu-id="626b7-155">Řetězec ``/_msdyn365/authresp`` pak musí být přidán k základní adrese URL, jako v následujících příkladech.</span><span class="sxs-lookup"><span data-stu-id="626b7-155">The string ``/_msdyn365/authresp`` then needs to be appended to the base URLs, as in the following examples.</span></span>

- ``https://fabrikam.com/_msdyn365/authresp``
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a><span data-ttu-id="626b7-156">Vytvoření zásad toku uživatele</span><span class="sxs-lookup"><span data-stu-id="626b7-156">Create user flow policies</span></span>

<span data-ttu-id="626b7-157">Toky uživatelů představují zásady, které Azure AD B2C používá k zajištění bezpečného přihlášení, registraci, úpravy profilu a obnově zapomenutého hesla.</span><span class="sxs-lookup"><span data-stu-id="626b7-157">User flows are the policies Azure AD B2C uses to provide secure sign in, sign up, edit profile, and forget password user experiences.</span></span> <span data-ttu-id="626b7-158">Dynamics 365 Commerce používá tyto toky k provádění akcí zásad pro interakci s klientem Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-158">Dynamics 365 Commerce uses these flows to perform the policy actions to interact with the Azure AD B2C tenant.</span></span> <span data-ttu-id="626b7-159">Pokud uživatel pracuje s těmito zásadami, je přesměrován na klienta Azure AD B2C, kde může provádět akce.</span><span class="sxs-lookup"><span data-stu-id="626b7-159">When a user interacts with these policies, they are redirected to the Azure AD B2C tenant to perform the actions.</span></span>

<span data-ttu-id="626b7-160">Azure AD B2C poskytuje tři základní typy toků uživatele:</span><span class="sxs-lookup"><span data-stu-id="626b7-160">Azure AD B2C provides three basic user flow types:</span></span>
- <span data-ttu-id="626b7-161">Registrace a přihlášení</span><span class="sxs-lookup"><span data-stu-id="626b7-161">Sign up and sign in</span></span>
- <span data-ttu-id="626b7-162">Úprava profilu</span><span class="sxs-lookup"><span data-stu-id="626b7-162">Profile editing</span></span>
- <span data-ttu-id="626b7-163">Obnovení hesla</span><span class="sxs-lookup"><span data-stu-id="626b7-163">Password reset</span></span>

<span data-ttu-id="626b7-164">Můžete zvolit, zda chcete použít výchozí toky uživatelů, které poskytuje Azure AD, čímž se zobrazí stránka hostovaná v AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-164">You can choose to use the default user flows provided by Azure AD, which will display a page hosted by AAD B2C.</span></span> <span data-ttu-id="626b7-165">Alternativně můžete vytvořit stránku HTML, která určí vzhled a chování těchto toků uživatelů.</span><span class="sxs-lookup"><span data-stu-id="626b7-165">Alternately, you can create an HTML page to control the look and feel of these user flow experiences.</span></span> 

<span data-ttu-id="626b7-166">Chcete-li přizpůsobit stránky zásad uživatelů pro Dynamics 365 Commerce, prostudujte si téma [Nastavení vlastních stránek pro přihlášení uživatelů](custom-pages-user-logins.md).</span><span class="sxs-lookup"><span data-stu-id="626b7-166">To customize the user policy pages for Dynamics 365 Commerce, see [Set up custom pages for user logins](custom-pages-user-logins.md).</span></span> <span data-ttu-id="626b7-167">Další informace naleznete v tématu [Přizpůsobení rozhraní uživatelských prostředí v Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span><span class="sxs-lookup"><span data-stu-id="626b7-167">For additional information, see [Customize the interface of user experiences in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span></span>

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a><span data-ttu-id="626b7-168">Vytvoření zásady toku uživatele pro registraci a přihlášení</span><span class="sxs-lookup"><span data-stu-id="626b7-168">Create a sign up and sign in user flow policy</span></span>

<span data-ttu-id="626b7-169">Chcete-li vytvořit zásadu toku uživatele pro registraci a přihlášení, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="626b7-169">To create a sign up and sign in user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="626b7-170">Na portálu Azure vyberte možnost **Toky uživatelů (zásady)** v levém navigačním podokně.</span><span class="sxs-lookup"><span data-stu-id="626b7-170">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="626b7-171">Na stránce **Azure AD B2C – toky uživatelů (zásady)** vyberte možnost **Nový tok uživatele**.</span><span class="sxs-lookup"><span data-stu-id="626b7-171">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="626b7-172">Na kartě **Doporučené** vyberte možnost **Registrace a přihlášení**.</span><span class="sxs-lookup"><span data-stu-id="626b7-172">On the **Recommended** tab, select **Sign up and sign in**.</span></span>
1. <span data-ttu-id="626b7-173">V položce **Název** zadejte název zásady.</span><span class="sxs-lookup"><span data-stu-id="626b7-173">Under **Name**, enter a policy name.</span></span> <span data-ttu-id="626b7-174">Tento název se pak zobrazí s použitím předpony, kterou přiřadí portál (například „B2C_1_“).</span><span class="sxs-lookup"><span data-stu-id="626b7-174">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="626b7-175">V části **Zprostředkovatelé identity** zaškrtněte příslušné políčko.</span><span class="sxs-lookup"><span data-stu-id="626b7-175">Under **Identity providers**, select the appropriate check box.</span></span>
1. <span data-ttu-id="626b7-176">V části **Vícefaktorové ověřování** vyberte vhodnou volbu pro vaši společnost.</span><span class="sxs-lookup"><span data-stu-id="626b7-176">Under **Multifactor Authentication**, select the appropriate choice for your company.</span></span> 
1. <span data-ttu-id="626b7-177">V části **Atributy a deklarace identit uživatelů** vyberte možnosti pro získání atributů nebo deklarací identit pro vrácení (podle potřeby).</span><span class="sxs-lookup"><span data-stu-id="626b7-177">Under **User attributes and claims**, select options to collect attributes or return claims as appropriate.</span></span> <span data-ttu-id="626b7-178">Commerce vyžaduje následující výchozí možnosti:</span><span class="sxs-lookup"><span data-stu-id="626b7-178">Commerce requires the following default options:</span></span>

    | <span data-ttu-id="626b7-179">**Získat atribut**</span><span class="sxs-lookup"><span data-stu-id="626b7-179">**Collect  attribute**</span></span> | <span data-ttu-id="626b7-180">**Vrátit deklaraci identity**</span><span class="sxs-lookup"><span data-stu-id="626b7-180">**Return  claim**</span></span> |
    | ---------------------- | ----------------- |
    | <span data-ttu-id="626b7-181">E-mailová adresa</span><span class="sxs-lookup"><span data-stu-id="626b7-181">Email Address</span></span>          | <span data-ttu-id="626b7-182">E-mailové adresy</span><span class="sxs-lookup"><span data-stu-id="626b7-182">Email Addresses</span></span>   |
    | <span data-ttu-id="626b7-183">Křestní jméno</span><span class="sxs-lookup"><span data-stu-id="626b7-183">Given Name</span></span>             | <span data-ttu-id="626b7-184">Křestní jméno</span><span class="sxs-lookup"><span data-stu-id="626b7-184">Given Name</span></span>        |
    |                        | <span data-ttu-id="626b7-185">Poskytovatel identity</span><span class="sxs-lookup"><span data-stu-id="626b7-185">Identity Provider</span></span> |
    | <span data-ttu-id="626b7-186">Příjmení</span><span class="sxs-lookup"><span data-stu-id="626b7-186">Surname</span></span>                | <span data-ttu-id="626b7-187">Příjmení</span><span class="sxs-lookup"><span data-stu-id="626b7-187">Surname</span></span>           |
    |                        | <span data-ttu-id="626b7-188">ID objektu uživatele</span><span class="sxs-lookup"><span data-stu-id="626b7-188">User’s Object ID</span></span>  |

1. <span data-ttu-id="626b7-189">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="626b7-189">Select **Create**.</span></span>

<span data-ttu-id="626b7-190">Následující obrázek je příkladem toku uživatele pro registraci a přihlášení Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-190">The following image is an example of the Azure AD B2C sign up and sign in user flow.</span></span>

![Nastavení zásady registrace a přihlášení](./media/B2CImage_11.png)

<span data-ttu-id="626b7-192">Následující obrázek znázorňuje možnost **Spustit tok uživatele** v toku uživatele pro registraci a přihlášení Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-192">The following image shows the **Run user flow** option in the Azure AD B2C sign up and sign in user flow.</span></span>

![Možnost Spustit tok uživatele v toku zásady](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a><span data-ttu-id="626b7-194">Vytvoření zásady toku uživatele pro úpravu profilu</span><span class="sxs-lookup"><span data-stu-id="626b7-194">Create a profile editing user flow policy</span></span>

<span data-ttu-id="626b7-195">Chcete-li vytvořit zásadu toku uživatele pro úpravu profilu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="626b7-195">To create a profile editing user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="626b7-196">Na portálu Azure vyberte možnost **Toky uživatelů (zásady)** v levém navigačním podokně.</span><span class="sxs-lookup"><span data-stu-id="626b7-196">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="626b7-197">Na stránce **Azure AD B2C – toky uživatelů (zásady)** vyberte možnost **Nový tok uživatele**.</span><span class="sxs-lookup"><span data-stu-id="626b7-197">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="626b7-198">Na kartě **Doporučené** vyberte možnost **Úprava profilu**.</span><span class="sxs-lookup"><span data-stu-id="626b7-198">On the **Recommended** tab, select **Profile editing**.</span></span>
1. <span data-ttu-id="626b7-199">V části **Název** zadejte tok uživatele pro úpravu profilu.</span><span class="sxs-lookup"><span data-stu-id="626b7-199">Under **Name**, enter the profile editing user flow.</span></span> <span data-ttu-id="626b7-200">Tento název se pak zobrazí s použitím předpony, kterou přiřadí portál (například „B2C_1_“).</span><span class="sxs-lookup"><span data-stu-id="626b7-200">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="626b7-201">V části **Zprostředkovatelé identity** vyberte možnost **Přihlášení k místnímu účtu**.</span><span class="sxs-lookup"><span data-stu-id="626b7-201">Under **Identity providers**, select **Local Account SignIn**.</span></span>
1. <span data-ttu-id="626b7-202">V části **Atributy uživatele** zaškrtněte některé z následujících políček:</span><span class="sxs-lookup"><span data-stu-id="626b7-202">Under **User attributes**, select the following check boxes:</span></span>
    - <span data-ttu-id="626b7-203">**E-mailové adresy** (pouze **Vrátit deklaraci identity**)</span><span class="sxs-lookup"><span data-stu-id="626b7-203">**Email Addresses** (**Return claim** only)</span></span>
    - <span data-ttu-id="626b7-204">**Křestní jméno** (**Získat atribut** a **Vrátit deklaraci identity**)</span><span class="sxs-lookup"><span data-stu-id="626b7-204">**Given Name** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="626b7-205">**Zprostředkovatel identity** (pouze **Vrátit deklaraci identity**)</span><span class="sxs-lookup"><span data-stu-id="626b7-205">**Identity Provider** (**Return claim** only)</span></span>
    - <span data-ttu-id="626b7-206">**Příjmení** (**Získat atribut** a **Vrátit deklaraci identity**)</span><span class="sxs-lookup"><span data-stu-id="626b7-206">**Surname** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="626b7-207">**ID objektu uživatele** (pouze **Vrátit deklaraci identity**)</span><span class="sxs-lookup"><span data-stu-id="626b7-207">**User's Object ID** (**Return claim** only)</span></span>
1. <span data-ttu-id="626b7-208">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="626b7-208">Select **Create**.</span></span>

<span data-ttu-id="626b7-209">Na následujícím obrázku je znázorněn příklad toku uživatele pro upravu profilu Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-209">The following image shows an example of the Azure AD B2C profile editing user flow.</span></span>

![Vytvoření toku uživatele pro úpravu profilu](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a><span data-ttu-id="626b7-211">Vytvoření zásady toku uživatele pro resetování hesla</span><span class="sxs-lookup"><span data-stu-id="626b7-211">Create a password reset user flow policy</span></span>

<span data-ttu-id="626b7-212">Chcete-li vytvořit zásadu toku uživatele pro resetování hesla, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="626b7-212">To create a password reset user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="626b7-213">Na portálu Azure vyberte možnost **Toky uživatelů (zásady)** v levém navigačním podokně.</span><span class="sxs-lookup"><span data-stu-id="626b7-213">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="626b7-214">Na stránce **Azure AD B2C – toky uživatelů (zásady)** vyberte možnost **Nový tok uživatele**.</span><span class="sxs-lookup"><span data-stu-id="626b7-214">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="626b7-215">Na kartě **Doporučené** vyberte možnost **Resetování hesla**.</span><span class="sxs-lookup"><span data-stu-id="626b7-215">On the **Recommended** tab, select **Password Reset**.</span></span>
1. <span data-ttu-id="626b7-216">V poli **Název** zadejte název toku uživatele pro resetování hesla.</span><span class="sxs-lookup"><span data-stu-id="626b7-216">Under **Name**, enter a name for the password reset user flow.</span></span>
1. <span data-ttu-id="626b7-217">V části **Zprostředkovatelé identity** vyberte možnost **Resetovat heslo pomocí e-mailové adresy**.</span><span class="sxs-lookup"><span data-stu-id="626b7-217">Under **Identity providers**, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="626b7-218">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="626b7-218">Select **Create**.</span></span>
1. <span data-ttu-id="626b7-219">V části **Deklarace identity aplikace** zaškrtněte některé z následujících políček:</span><span class="sxs-lookup"><span data-stu-id="626b7-219">Under **Application claims**, select the following check boxes:</span></span>
    - <span data-ttu-id="626b7-220">**E-mailové adresy**</span><span class="sxs-lookup"><span data-stu-id="626b7-220">**Email addresses**</span></span>
    - <span data-ttu-id="626b7-221">**Křestní jméno**</span><span class="sxs-lookup"><span data-stu-id="626b7-221">**Given Name**</span></span>
    - <span data-ttu-id="626b7-222">**Příjmení**</span><span class="sxs-lookup"><span data-stu-id="626b7-222">**Surname**</span></span>
    - <span data-ttu-id="626b7-223">**ID objektu uživatele**</span><span class="sxs-lookup"><span data-stu-id="626b7-223">**User's Object ID**</span></span>
1. <span data-ttu-id="626b7-224">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="626b7-224">Select **Create**.</span></span>

<span data-ttu-id="626b7-225">Následující obrázek znázorňuje, kde nastavit možnost **Resetovat heslo pomocí e-mailové adresy** v toku uživatele pro resetování hesla Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-225">The following image shows where to set **Reset Password using mail address** in the Azure AD B2C password reset user flow.</span></span>

![Nastavení možnosti „Resetovat heslo pomocí e-mailové adresy“ v zásadě pro resetování hesla](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a><span data-ttu-id="626b7-227">Přidání zprostředkovatelů sociální identity (volitelné)</span><span class="sxs-lookup"><span data-stu-id="626b7-227">Add social identity providers (Optional)</span></span>

<span data-ttu-id="626b7-228">Zprostředkovatelé sociální identity umožňují uživatelům používat účty sociálních sítí k ověřování.</span><span class="sxs-lookup"><span data-stu-id="626b7-228">Social identity providers allow users to use their social accounts for authentication.</span></span> <span data-ttu-id="626b7-229">Přidání ověření zprostředkovatele sociální identity je volitelné v Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="626b7-229">Adding social identity provider authentication is optional in Dynamics 365 Commerce.</span></span> 

<span data-ttu-id="626b7-230">Pokud není přidáno ověřování zprostředkovatele sociální identity, budou výchozí profily Azure AD B2C hlavními profily pro vaše uživatele.</span><span class="sxs-lookup"><span data-stu-id="626b7-230">If social identity provider authentication is not added, the default Azure AD B2C profiles will be the main profiles for your user base.</span></span> <span data-ttu-id="626b7-231">Uživatelé budou moci vybrat vlastní uživatelské jméno (jejich upřednostňovaná e-mailová adresa) a nastavit heslo.</span><span class="sxs-lookup"><span data-stu-id="626b7-231">Users will select their own username (their preferred email address) and set a password.</span></span> <span data-ttu-id="626b7-232">Azure AD B2C bude uživatele ověřovat přímo.</span><span class="sxs-lookup"><span data-stu-id="626b7-232">Azure AD B2C will authenticate users directly.</span></span> 

<span data-ttu-id="626b7-233">Je-li přidáno ověřování zprostředkovatele sociální identity a uživatel si zvolí jednoho ze nabízených zprostředkovatelů sociální identity, bude v klientu Azure AD B2C vytvořena entita.</span><span class="sxs-lookup"><span data-stu-id="626b7-233">If social identity provider authentication is added and a user chooses one of the social identity providers offered, an entity is still created in the Azure AD B2C tenant.</span></span> <span data-ttu-id="626b7-234">Azure AD B2C poté ověří přihlašovací údaje uživatele pomocí zprostředkovatele sociální identity.</span><span class="sxs-lookup"><span data-stu-id="626b7-234">Azure AD B2C will then authenticate the user's credentials with the social identity provider.</span></span>

> [!NOTE]
> <span data-ttu-id="626b7-235">Přihlášení zprostředkovatele identity vytvoří záznam v klientovi B2C, ale v jiném formátu než místní účty, protože pro ověření bude volat externí odkaz na zprostředkovatele sociální identity.</span><span class="sxs-lookup"><span data-stu-id="626b7-235">The identity provider sign in creates a record in the B2C tenant, but in a different format than local accounts since it will call the external social identity provider reference for authentication.</span></span> <span data-ttu-id="626b7-236">Uživatel může použít stejnou e-mailovou adresu v rámci zprostředkovatelů sociální identity, což znamená, že uživatelské jméno e-mailu použité pro ověření nemusí být jedinečné pro klienta.</span><span class="sxs-lookup"><span data-stu-id="626b7-236">The user can use the same email address across social identity providers, meaning that the email username used for authentication may not be unique to the tenant.</span></span> <span data-ttu-id="626b7-237">Azure AD B2C pouze vynutí, aby uživatelé měli jedinečnou e-mailovou adresu v místních účtech B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-237">Azure AD B2C will only enforce that users have a unique email address on local B2C accounts.</span></span>

<span data-ttu-id="626b7-238">Před přidáním zprostředkovatele sociální identity pro ověřování je nutné přejít na portál zprostředkovatele identity a nastavit aplikaci zprostředkovatele identity tak, jak je uvedeno v dokumentaci k Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-238">Before you can add a social identity provider for authentication, you must go to the identity provider's portal and set up an identity provider application as instructed in the Azure AD B2C documentation.</span></span> <span data-ttu-id="626b7-239">Níže je uveden seznam odkazů na dokumentaci.</span><span class="sxs-lookup"><span data-stu-id="626b7-239">A list of links to the documentation is provided below.</span></span>

- [<span data-ttu-id="626b7-240">Amazon</span><span class="sxs-lookup"><span data-stu-id="626b7-240">Amazon</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [<span data-ttu-id="626b7-241">Azure AD (jeden klient)</span><span class="sxs-lookup"><span data-stu-id="626b7-241">Azure AD (Single Tenant)</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [<span data-ttu-id="626b7-242">Účet Microsoft</span><span class="sxs-lookup"><span data-stu-id="626b7-242">Microsoft Account</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [<span data-ttu-id="626b7-243">Facebook</span><span class="sxs-lookup"><span data-stu-id="626b7-243">Facebook</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [<span data-ttu-id="626b7-244">GitHub</span><span class="sxs-lookup"><span data-stu-id="626b7-244">GitHub</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [<span data-ttu-id="626b7-245">Google</span><span class="sxs-lookup"><span data-stu-id="626b7-245">Google</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [<span data-ttu-id="626b7-246">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="626b7-246">LinkedIn</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [<span data-ttu-id="626b7-247">OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="626b7-247">OpenID Connect</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [<span data-ttu-id="626b7-248">Twitter</span><span class="sxs-lookup"><span data-stu-id="626b7-248">Twitter</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a><span data-ttu-id="626b7-249">Přidání a nastavení zprostředkovatele sociální identity</span><span class="sxs-lookup"><span data-stu-id="626b7-249">Add and set up a social identity provider</span></span>

<span data-ttu-id="626b7-250">Chcete-li přidat a nastavit zprostředkovatele sociální identity, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="626b7-250">To add and set up a social identity provider, follow these steps.</span></span>  

1. <span data-ttu-id="626b7-251">V portálu Azure přejděte k **Zprostředkovatelé identity**.</span><span class="sxs-lookup"><span data-stu-id="626b7-251">In the Azure portal, navigate to **Identity Providers**.</span></span>
1. <span data-ttu-id="626b7-252">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="626b7-252">Select **Add**.</span></span> <span data-ttu-id="626b7-253">Zobrazí se obrazovka **Přidání zprostředkovatele identity**.</span><span class="sxs-lookup"><span data-stu-id="626b7-253">The **Add identity provider** screen appears.</span></span>
1. <span data-ttu-id="626b7-254">V části **Název** zadejte název, který se zobrazí uživatelům na vaší obrazovce pro přihlášení.</span><span class="sxs-lookup"><span data-stu-id="626b7-254">Under **Name**, enter the name to be displayed to users on your sign in screen.</span></span>
1. <span data-ttu-id="626b7-255">V části **Typ zprostředkovatele identity** vyberte zprostředkovatele identity ze seznamu.</span><span class="sxs-lookup"><span data-stu-id="626b7-255">Under **Identity provider type**, select an identity provider from the list.</span></span>
1. <span data-ttu-id="626b7-256">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="626b7-256">Select **OK**.</span></span>
1. <span data-ttu-id="626b7-257">Volbou **Nastavit tohoto zprostředkovatele identity** přistoupíte na obrazovku **Nastavení zprostředkovatele sociální identity**.</span><span class="sxs-lookup"><span data-stu-id="626b7-257">Select **Set up this identity provider** to access the **Set up the social identity provider** screen.</span></span>
1. <span data-ttu-id="626b7-258">V poli **ID klienta** zadejte ID klienta, které jste získali z nastavení aplikace zprostředkovatele identity.</span><span class="sxs-lookup"><span data-stu-id="626b7-258">Under **Client ID**, enter the client ID as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="626b7-259">V poli **Tajný klíč klienta** zadejte tajný klíč klienta, které jste získali z nastavení aplikace zprostředkovatele identity.</span><span class="sxs-lookup"><span data-stu-id="626b7-259">Under **Client secret**, enter the client secret as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="626b7-260">Připojte tok uživatele pro zásady přihlášení a registrace:</span><span class="sxs-lookup"><span data-stu-id="626b7-260">Attach user flow for sign in sign up policies:</span></span>
1. <span data-ttu-id="626b7-261">Přejděte na **Azure AD B2C – toky uživatelů (zásady) \> {vaše zásada pro přihlášení a registraci} \> Zprostředkovatelé identity**.</span><span class="sxs-lookup"><span data-stu-id="626b7-261">Go to **Azure AD B2C – User flows (policies) \> {your sign-in sign-up policy} \> Identity providers**.</span></span>
1. <span data-ttu-id="626b7-262">Chcete-li připojit zásadu toku uživatele pro přihlášení/registraci, vyberte každého zprostředkovatele identity, kterého jste pro svůj účet nastavili.</span><span class="sxs-lookup"><span data-stu-id="626b7-262">To attach the sign in/sign up user flow policy, select each identity provider you have set up for your account.</span></span> <span data-ttu-id="626b7-263">Chcete-li je otestovat, vyberte možnost **Spustit tok uživatele** pro každého zprostředkovatele identity.</span><span class="sxs-lookup"><span data-stu-id="626b7-263">To test these, select **Run user flow** for each identity provider.</span></span> <span data-ttu-id="626b7-264">Na nové kartě se zobrazí stránka pro přihlášení s oblastí výběru nového zprostředkovatele identity.</span><span class="sxs-lookup"><span data-stu-id="626b7-264">A new tab will display the sign-in page displaying the new identity provider selection box.</span></span>

<span data-ttu-id="626b7-265">Následující obrázek znázorňuje příklad obrazovek **Přidání zprostředkovatele identity** a **Nastavení zprostředkovatele** sociální identity v Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-265">The following image shows examples of the **Add identity provider** and **Set up the social identity provider** screens in Azure AD B2C.</span></span>

![Přidání poskytovatele sociální identity do aplikace](./media/B2CImage_14.png)

<span data-ttu-id="626b7-267">Následující obrázek znázorňuje příklad, jak vybrat zprostředkovatele identity na stránce **Zprostředkovatelé identity** v Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-267">The following image shows an example of how to select identity providers on the Azure AD B2C **Identity Providers** page.</span></span>

![Výběr jednotlivých zprostředkovatelů sociální identity a povolení vaší zásady](./media/B2CImage_16.png)

<span data-ttu-id="626b7-269">Následující obrázek znázorňuje příklad výchozí přihlašovací obrazovky se zobrazeným tlačítkem pro přihlášení zprostředkovatele sociální identity.</span><span class="sxs-lookup"><span data-stu-id="626b7-269">The following image shows an example of a default sign-in screen with a social identity provider sign-in button displayed.</span></span>

![Příklad výchozí obrazovky pro přihlášení se zobrazeným tlačítkem pro přihlášení zprostředkovatele sociální identity](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a><span data-ttu-id="626b7-271">Aktualizace Commerce Headquarters o nové informace Azure AD B2C</span><span class="sxs-lookup"><span data-stu-id="626b7-271">Update Commerce headquarters with the new Azure AD B2C information</span></span>

<span data-ttu-id="626b7-272">Po dokončení výše uvedených kroků pro zřízení Azure AD B2C musí být aplikace Azure AD B2C registrována ve vašem prostředí Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="626b7-272">Once the Azure AD B2C provisioning steps above are completed, the Azure AD B2C application must be registered in your Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="626b7-273">Chcete-li aktualizovat Headquarters o nové informace Azure AD B2C, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="626b7-273">To update headquarters with the new Azure AD B2C information, follow these steps.</span></span>

1. <span data-ttu-id="626b7-274">V Commerce přejděte na **Sdílené parametry Commerce** a vyberte **Zprostředkovatelé identity** v levé nabídce.</span><span class="sxs-lookup"><span data-stu-id="626b7-274">In Commerce, go to **Commerce Shared Parameters** and select **Identity Providers** in the left menu.</span></span>
1. <span data-ttu-id="626b7-275">V části **Zprostředkovatelé identity** postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="626b7-275">Under **Identity Providers**, do the following:</span></span>
    1. <span data-ttu-id="626b7-276">V poli **Vystavitel** zadejte adresu URL vystavitele zprostředkovatele identity.</span><span class="sxs-lookup"><span data-stu-id="626b7-276">In the **Issuer** box, enter the identity provider issuer URL.</span></span> <span data-ttu-id="626b7-277">Chcete-li najít adresu URL svého vystavitele, viz [Získání adresy URL vystavitele](#obtain-issuer-url) níže.</span><span class="sxs-lookup"><span data-stu-id="626b7-277">To find your issuer URL, see [Obtain issuer URL](#obtain-issuer-url) below.</span></span>
    1. <span data-ttu-id="626b7-278">Do pole **Název** zadejte název záznamu vystavitele.</span><span class="sxs-lookup"><span data-stu-id="626b7-278">In the **Name** box, enter a name for your issuer record.</span></span>
    1. <span data-ttu-id="626b7-279">Do pole **Typ** zadejte **Azure AD B2C (id_token)**.</span><span class="sxs-lookup"><span data-stu-id="626b7-279">In the **Type** box, enter **Azure AD B2C (id_token)**.</span></span>
1. <span data-ttu-id="626b7-280">V části **Předávající strany** s výše vybranou položkou zprostředkovatele identity B2C postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="626b7-280">Under **Relying Parties**, with the above B2C identity provider item selected, do the following:</span></span>
    1. <span data-ttu-id="626b7-281">V poli **ID klienta** zadejte ID aplikace B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-281">In the **ClientID** box, enter your B2C application ID.</span></span> <span data-ttu-id="626b7-282">To lze nalézt v poli **ID aplikace** na stránce vlastností aplikace B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-282">You can find this in the **Application ID** box of your B2C application's properties page.</span></span>
    1. <span data-ttu-id="626b7-283">Do pole **Typ** zadejte **Veřejné**.</span><span class="sxs-lookup"><span data-stu-id="626b7-283">In the **Type** box, enter **Public**.</span></span>
    1. <span data-ttu-id="626b7-284">Do pole **Typ uživatele** zadejte **Zákazník**.</span><span class="sxs-lookup"><span data-stu-id="626b7-284">In the **User Type** box, enter **Customer**.</span></span>
1. <span data-ttu-id="626b7-285">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="626b7-285">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="626b7-286">Ve vyhledávacím poli Commerce Search vyhledejte **Plán distribuce**.</span><span class="sxs-lookup"><span data-stu-id="626b7-286">In the Commerce search box, search for **Distribution schedule**</span></span>
1. <span data-ttu-id="626b7-287">V levé navigační nabídce stránky **Plán distribuce** vyberte úlohu **1110 Globální konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="626b7-287">In the left navigation menu of the **Distribution schedules** page, select job **1110 Global configuration**.</span></span>
1. <span data-ttu-id="626b7-288">V podokně akcí zvolte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="626b7-288">On the action pane, select **Run Now**.</span></span>

### <a name="obtain-issuer-url"></a><span data-ttu-id="626b7-289">Získání adresy URL vystavitele</span><span class="sxs-lookup"><span data-stu-id="626b7-289">Obtain issuer URL</span></span>

<span data-ttu-id="626b7-290">Chcete-li získat adresu URL vystavitele svého zprostředkovatele identity, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="626b7-290">To obtain your identity provider issuer URL, follow these steps.</span></span>

1. <span data-ttu-id="626b7-291">V následujícím formátu vytvořte adresu URL metadat s použitím vašeho klienta a zásady B2C: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span><span class="sxs-lookup"><span data-stu-id="626b7-291">Create a metadata address URL in the following format using your B2C tenant and policy: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span></span>
    - <span data-ttu-id="626b7-292">Příklad: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span><span class="sxs-lookup"><span data-stu-id="626b7-292">Example: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span></span>
1. <span data-ttu-id="626b7-293">Do adresního řádku prohlížeče zadejte adresu URL metadat.</span><span class="sxs-lookup"><span data-stu-id="626b7-293">Enter the metadata address URL into a browser address bar.</span></span>
1. <span data-ttu-id="626b7-294">V metadatech zkopírujte adresu URL vystavitele zprostředkovatele identity (hodnota pro **„vystavitel“**).</span><span class="sxs-lookup"><span data-stu-id="626b7-294">In the metadata, copy the identity provider issuer URL (the value for **"issuer"**).</span></span>
    - <span data-ttu-id="626b7-295">Příklad: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span><span class="sxs-lookup"><span data-stu-id="626b7-295">Example: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span></span>

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a><span data-ttu-id="626b7-296">Konfigurace klienta B2C v konfigurátoru webů Commerce</span><span class="sxs-lookup"><span data-stu-id="626b7-296">Configure your B2C tenant in Commerce site builder</span></span>

<span data-ttu-id="626b7-297">Po dokončení nastavení klienta Azure AD B2C musíte nakonfigurovat klienta B2C v konfigurátoru webů Commerce.</span><span class="sxs-lookup"><span data-stu-id="626b7-297">Once setup of your Azure AD B2C tenant is completed, you must configure the B2C tenant in Commerce site builder.</span></span> <span data-ttu-id="626b7-298">Kroky konfigurace zahrnují získání informací o aplikaci B2C z portálu Azure, zadání informací o aplikaci B2C do konfigurátru webů a následné přidružení aplikace B2C k vašemu webu a kanálu.</span><span class="sxs-lookup"><span data-stu-id="626b7-298">Configuration steps include collecting B2C application information from the Azure portal, entering that B2C application information into site builder, and then associating the B2C application with your site and channel.</span></span>

### <a name="collect-the-required-application-information"></a><span data-ttu-id="626b7-299">Získání požadovaných informací o aplikaci</span><span class="sxs-lookup"><span data-stu-id="626b7-299">Collect the required application information</span></span>

<span data-ttu-id="626b7-300">Chcete-li získat požadované informace o aplikaci, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="626b7-300">To collect the required application information, follow these steps.</span></span>

1. <span data-ttu-id="626b7-301">V portálu Azure přejděte na **Domovská stránka \> Azure AD B2C – aplikace**.</span><span class="sxs-lookup"><span data-stu-id="626b7-301">In the Azure portal, go to **Home \> Azure AD B2C - Applications**.</span></span>
1. <span data-ttu-id="626b7-302">Pro získání podrobností o aplikaci vyberte svou aplikaci a v levém navigačním podokně vyberte **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="626b7-302">Select your application, and then in the left navigation pane select **Properties** to obtain the application details.</span></span>
1. <span data-ttu-id="626b7-303">Z pole **ID aplikace** získejte ID aplikace B2C vytvořené ve vašem klientovi B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-303">From the **Application ID** box, collect the application ID of the B2C application created in your B2C tenant.</span></span> <span data-ttu-id="626b7-304">Později bude zadáno jako **GUID klienta** v konfigurátoru webů.</span><span class="sxs-lookup"><span data-stu-id="626b7-304">This will later be entered as the **Client GUID** in site builder.</span></span>
1. <span data-ttu-id="626b7-305">V poli **AdresaURL odpovědi** získejte adresu URL odpovědi.</span><span class="sxs-lookup"><span data-stu-id="626b7-305">Under **Reply URL**, collect the reply URL.</span></span>
1. <span data-ttu-id="626b7-306">Přejděte na **Domovská stránka \> Azure AD B2C – toky uživatelů (zásady)** a získejte názvy jednotlivých zásad toku uživatelů.</span><span class="sxs-lookup"><span data-stu-id="626b7-306">Go to **Home \> Azure AD B2C – User flows (policies)**, and then collect the names of each user flow policy.</span></span>

<span data-ttu-id="626b7-307">Na následujícím obrázku je znázorněn příklad stránky **Azure AD B2C – aplikace**.</span><span class="sxs-lookup"><span data-stu-id="626b7-307">The following image shows an example of the **Azure AD B2C - Applications** page.</span></span>

![Přechod k aplikaci B2C ve vašem klientovi](./media/B2CImage_19.png)

<span data-ttu-id="626b7-309">Na následujícím obrázku je znázorněn příklad stránky **Vlastnosti** aplikace v Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-309">The following image shows an example of an application **Properties** page in Azure AD B2C.</span></span> 

![Kopírování ID aplikace z vlastností aplikace B2C](./media/B2CImage_21.png)

<span data-ttu-id="626b7-311">Následující obrázek znázorňuje příklad zásad toku uživatelů na stránce **Azure AD B2C – toky uživatelů (zásady)**.</span><span class="sxs-lookup"><span data-stu-id="626b7-311">The following image shows an example of user flow policies on the **Azure AD B2C – User flows (policies)** page.</span></span>

![Získání názvů jednotlivých toků zásad B2C](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a><span data-ttu-id="626b7-313">Zadání informací o aplikaci klienta AAD B2C do platformy Commerce</span><span class="sxs-lookup"><span data-stu-id="626b7-313">Enter your AAD B2C tenant application information into Commerce</span></span>

<span data-ttu-id="626b7-314">Před přidružením klienta B2C ke svým webům je nutné zadat podrobnosti o klientovi Azure AD B2C do konfigurátoru webů Commerce.</span><span class="sxs-lookup"><span data-stu-id="626b7-314">You must enter details of the Azure AD B2C tenant into Commerce site builder before associating the B2C tenant with your site(s).</span></span>

<span data-ttu-id="626b7-315">Chcete-li do platformy Commerce přidat informace o aplikaci klienta AAD B2C, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="626b7-315">To add your AAD B2C tenant application information to Commerce, follow these steps.</span></span>

1. <span data-ttu-id="626b7-316">Přihlaste se jako správce ke konfigurátoru webů Commerce pro vaše prostředí.</span><span class="sxs-lookup"><span data-stu-id="626b7-316">Sign in as an administrator to Commerce site builder for your environment.</span></span>
1. <span data-ttu-id="626b7-317">V levém navigačním podokně vyberte **Nastavení klienta**, čímž jej rozbalíte.</span><span class="sxs-lookup"><span data-stu-id="626b7-317">In the left navigation pane, select **Tenant Settings**  to expand it.</span></span>
1. <span data-ttu-id="626b7-318">V části **Nastavení klienta** vyberte **Nastavení B2C**.</span><span class="sxs-lookup"><span data-stu-id="626b7-318">Under **Tenant Settings**, select **B2C Settings**.</span></span> 
1. <span data-ttu-id="626b7-319">V hlavním okně vedle položky **Aplikace B2C** vyberte možnost **Spravovat**.</span><span class="sxs-lookup"><span data-stu-id="626b7-319">In the main window next **B2C Applications**, select **Manage**.</span></span> <span data-ttu-id="626b7-320">(Pokud se klient zobrazí v seznamu aplikací B2C, pak již byl přidán správcem.</span><span class="sxs-lookup"><span data-stu-id="626b7-320">(If your tenant appears in the B2C Applications list, then it was already added by an administrator.</span></span> <span data-ttu-id="626b7-321">Ověřte, že položky v kroku 6 odpovídají vaší aplikaci B2C.)</span><span class="sxs-lookup"><span data-stu-id="626b7-321">Verify that the items in step 6 below match your B2C Application.)</span></span>
1. <span data-ttu-id="626b7-322">Vyberte **Přidat aplikaci B2C**.</span><span class="sxs-lookup"><span data-stu-id="626b7-322">Select **Add B2C Application**.</span></span>
1. <span data-ttu-id="626b7-323">Ve zobrazeném formuláři zadejte následující požadované položky s použitím hodnot z klienta a aplikace B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-323">Enter the following required items in the form displayed, using values from your B2C tenant and application.</span></span> <span data-ttu-id="626b7-324">Pole, která nejsou vyžadována (bez hvězdičky), mohou být ponechána prázdná.</span><span class="sxs-lookup"><span data-stu-id="626b7-324">Fields that are not required (those without an asterisk) may be left blank.</span></span>

    - <span data-ttu-id="626b7-325">**Název aplikace**: název aplikace B2C, například „Fabrikam B2C“.</span><span class="sxs-lookup"><span data-stu-id="626b7-325">**Application Name**: The name for your B2C Application, for example "Fabrikam B2C".</span></span>
    - <span data-ttu-id="626b7-326">**Název klienta**: Název klienta B2C (použijte například "fabrikam", pokud se doména pro klienta B2C zobrazuje jako "fabrikam.onmicrosoft.com").</span><span class="sxs-lookup"><span data-stu-id="626b7-326">**Tenant Name**: The name of your B2C tenant (for example, use "fabrikam" if the domain appears as "fabrikam.onmicrosoft.com" for the B2C tenant).</span></span> 
    - <span data-ttu-id="626b7-327">**ID zásady zapomenutého hesla**: ID zásady toku uživatele pro zapomenuté heslo, například „B2C_1_ResetovaniHesla“.</span><span class="sxs-lookup"><span data-stu-id="626b7-327">**Forget Password Policy ID**: The forget password user flow policy ID, for example "B2C_1_PasswordReset".</span></span>
    - <span data-ttu-id="626b7-328">**ID zásady registrace a přihlášení**: ID zásady toku uživatele pro registraci a přihlášení, například „B2C_1_registrace_prihlaseni“.</span><span class="sxs-lookup"><span data-stu-id="626b7-328">**Signup Signin Policy ID**: The sign up and sign in user flow policy ID, for example "B2C_1_signup_signin".</span></span>
    - <span data-ttu-id="626b7-329">**GUID klienta**: ID aplikace B2C, například „22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6“.</span><span class="sxs-lookup"><span data-stu-id="626b7-329">**Client GUID**: The B2C application ID, for example "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span></span>
    - <span data-ttu-id="626b7-330">**ID zásady úpravy profilu**: ID zásady toku uživatele pro úpravu profilu, například „B2C_1A_UpravaProfilu“.</span><span class="sxs-lookup"><span data-stu-id="626b7-330">**Edit Profile Policy ID**: The profile editing user flow policy ID, for example "B2C_1A_ProfileEdit".</span></span>

1. <span data-ttu-id="626b7-331">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="626b7-331">Select **OK**.</span></span> <span data-ttu-id="626b7-332">Nyní by se měl zobrazit název vaší aplikace B2C v seznamu.</span><span class="sxs-lookup"><span data-stu-id="626b7-332">You should now see the name of your B2C application appear in the list.</span></span>
1. <span data-ttu-id="626b7-333">Klepnutím na tlačítko **Uložit** uložte změny.</span><span class="sxs-lookup"><span data-stu-id="626b7-333">Select **Save** to save your changes.</span></span>

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a><span data-ttu-id="626b7-334">Přidružení aplikace B2C k webu a kanálu</span><span class="sxs-lookup"><span data-stu-id="626b7-334">Associate the B2C application to your site and channel</span></span>

> [!WARNING]
> <span data-ttu-id="626b7-335">Pokud je váš web již přidružen k aplikaci B2C, změna na jinou aplikaci B2C odstraní aktuální odkazy vytvořené pro uživatele, které jsou již zaregistrováni v tomto prostředí.</span><span class="sxs-lookup"><span data-stu-id="626b7-335">If your site is already associated with a B2C application, changing to a different B2C application will remove the current references established for users already signed up in this environment.</span></span> <span data-ttu-id="626b7-336">V případě změny nebudou mít uživatelé k dispozici žádná pověření přidružená k aktuálně přiřazené aplikaci B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-336">If changed, any credentials associated with the currently-assigned B2C application will not be available to users.</span></span> 
> 
> <span data-ttu-id="626b7-337">Aplikaci B2C aktualizujte pouze v případě, že aplikaci B2C kanálu zřizujete poprvé, nebo pokud čekáte, že se uživatelé znovu zaregistrují s novými pověřeními pro tento kanál pomocí nové aplikace B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-337">Only update the B2C application if you are setting up the channel's B2C application for the first time or if you intend to have users re-sign up with new credentials to this channel with the new B2C application.</span></span> <span data-ttu-id="626b7-338">Buďte opatrní při přiřazování kanálů k aplikacím B2C a pojmenovávejte aplikace srozumitelně.</span><span class="sxs-lookup"><span data-stu-id="626b7-338">Take caution when associating channels to B2C applications, and name applications clearly.</span></span> <span data-ttu-id="626b7-339">Není-li kanál přidružen k aplikaci B2C v níže uvedených krocích, uživatelé přihlašující se k tomuto kanálu pro váš web budou zadáni do aplikace B2C, která se zobrazí jako **výchozí** v seznamu aplikací B2C v umístění **Nastavení klienta \> Nastavení B2C**.</span><span class="sxs-lookup"><span data-stu-id="626b7-339">If a channel is not associated to a B2C application in the steps below, users signing into that channel for your site will be entered into the B2C application showing as **default** in the **Tenant Settings \> B2C Settings** list of B2C applications.</span></span>

<span data-ttu-id="626b7-340">Chcete-li přidružit aplikaci B2C k webu a kanálu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="626b7-340">To associate the B2C application to your site and channel, follow these steps.</span></span>

1. <span data-ttu-id="626b7-341">Přejděte na svůj web konfigurátoru webů Commerce.</span><span class="sxs-lookup"><span data-stu-id="626b7-341">Navigate to your site in Commerce site builder.</span></span>
1. <span data-ttu-id="626b7-342">V levém navigačním podokně vyberte **Nastavení webu** a rozbalte je.</span><span class="sxs-lookup"><span data-stu-id="626b7-342">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="626b7-343">Pod položkou **Nastavení webu** vyberte možnost **Kanály**.</span><span class="sxs-lookup"><span data-stu-id="626b7-343">Below **Site Settings**, select **Channels**.</span></span>
1. <span data-ttu-id="626b7-344">V hlavním okně v části **Kanály** vyberte svůj kanál.</span><span class="sxs-lookup"><span data-stu-id="626b7-344">In the main window under **Channels**, select your channel.</span></span>
1. <span data-ttu-id="626b7-345">V podokně vlastností kanálu vpravo vyberte název svojí aplikace B2C z rozevírací nabídky **Vybrat aplikaci B2C**.</span><span class="sxs-lookup"><span data-stu-id="626b7-345">In the channel properties pane on the right, select your B2C application name from the **Select B2C Application** drop down menu.</span></span>
1. <span data-ttu-id="626b7-346">Vyberte možnost **Zavřít** a pak vyberte možnost **Uložit a publikovat**.</span><span class="sxs-lookup"><span data-stu-id="626b7-346">Select **Close**, and then select **Save and Publish**.</span></span>

## <a name="additional-b2c-information"></a><span data-ttu-id="626b7-347">Doplňkové informace o B2C</span><span class="sxs-lookup"><span data-stu-id="626b7-347">Additional B2C information</span></span>

### <a name="customer-migration"></a><span data-ttu-id="626b7-348">Migrace zákazníků</span><span class="sxs-lookup"><span data-stu-id="626b7-348">Customer migration</span></span>

<span data-ttu-id="626b7-349">Pokud uvažujete o migraci záznamů zákazníků z předchozí platformy zprotředkovatele identity, spolupracujte s týmem Dynamics 365 Commerce, abyste zkontrolovali potřeby zákazníka ohledně migrace.</span><span class="sxs-lookup"><span data-stu-id="626b7-349">If you are considering migrating customer records from a previous identity provider platform, please work with the Dynamics 365 Commerce team to review your customer migration needs.</span></span>

<span data-ttu-id="626b7-350">Další dokumentaci Azure AD B2C ohledně migrace zákazníků najdete v tématu [Migrace uživatelů do Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span><span class="sxs-lookup"><span data-stu-id="626b7-350">For additional Azure AD B2C documentation on customer migration, see [Migrate users to Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span></span>

### <a name="custom-policies"></a><span data-ttu-id="626b7-351">Vlastní zásady</span><span class="sxs-lookup"><span data-stu-id="626b7-351">Custom policies</span></span>

<span data-ttu-id="626b7-352">Další informace o přizpůsobení interakcí a toků zásad Azure AD B2C nad rámec toho, co je nabídnuto standardními zásadami B2C, naleznete v tématu [Vlastní zásady v Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span><span class="sxs-lookup"><span data-stu-id="626b7-352">For additional information regarding customizing Azure AD B2C interactions and policy flows beyond what is offered by B2C standard policies, see [Custom policies in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span></span> 

### <a name="secondary-admin"></a><span data-ttu-id="626b7-353">Sekundární správce</span><span class="sxs-lookup"><span data-stu-id="626b7-353">Secondary admin</span></span>

<span data-ttu-id="626b7-354">Nepovinný sekundární účet správce lze přidat do oddílu **Uživatelé** v klientovi B2C.</span><span class="sxs-lookup"><span data-stu-id="626b7-354">An optional, secondary administrator account can be added in the **Users** section of your B2C tenant.</span></span> <span data-ttu-id="626b7-355">Může se jednat o přímý nebo obecný účet.</span><span class="sxs-lookup"><span data-stu-id="626b7-355">This can be a direct account or a general account.</span></span> <span data-ttu-id="626b7-356">Potřebujete-li sdílet účet v prostředcích týmu, je možné také vytvořit běžný účet.</span><span class="sxs-lookup"><span data-stu-id="626b7-356">If you need to share an account across team resources, a common account can also be created.</span></span> <span data-ttu-id="626b7-357">Vzhledem k citlivosti dat uložených v Azure AD B2C je třeba společný účet pečlivě monitorovat dle bezpečnostních postupů společnosti.</span><span class="sxs-lookup"><span data-stu-id="626b7-357">Due to the sensitivity of the data stored in Azure AD B2C, a common account should be monitored closely per your company's security practices.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="626b7-358">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="626b7-358">Additional resources</span></span>

[<span data-ttu-id="626b7-359">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="626b7-359">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="626b7-360">Nasazení nového webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="626b7-360">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="626b7-361">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="626b7-361">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="626b7-362">Přiřazení online webu ke kanálu</span><span class="sxs-lookup"><span data-stu-id="626b7-362">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="626b7-363">Správa souborů robots.txt</span><span class="sxs-lookup"><span data-stu-id="626b7-363">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="626b7-364">Nahrání souborů pro hromadné přesmerování adres URL</span><span class="sxs-lookup"><span data-stu-id="626b7-364">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="626b7-365">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="626b7-365">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="626b7-366">Konfigurace několika klientů B2C v prostředí Commerce</span><span class="sxs-lookup"><span data-stu-id="626b7-366">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="626b7-367">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="626b7-367">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="626b7-368">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="626b7-368">Enable location-based store detection</span></span>](enable-store-detection.md)
