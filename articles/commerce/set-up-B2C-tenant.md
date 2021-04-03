---
title: Nastavení klienta B2C v Commerce
description: Tohle téma popisuje, jak nastavíte své klienty Azure Active Directory (Azure AD) business-to-consumer (B2C) pro ověření webu uživatele v aplikaci Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4ee667bb49e70e0c881a2db1248b3f0c7fc017ce
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478133"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a><span data-ttu-id="ab917-103">Nastavení klienta B2C v Commerce</span><span class="sxs-lookup"><span data-stu-id="ab917-103">Set up a B2C tenant in Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ab917-104">Tohle téma popisuje, jak nastavíte své klienty Azure Active Directory (Azure AD) business-to-consumer (B2C) pro ověření webu uživatele v aplikaci Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ab917-104">This topic describes how to set up your Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants for user site authentication in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ab917-105">Dynamics 365 Commerce používá Azure AD B2C pro podporu toků přihlašovacích údajů a ověřování uživatele.</span><span class="sxs-lookup"><span data-stu-id="ab917-105">Dynamics 365 Commerce uses Azure AD B2C to support user credential and authentication flows.</span></span> <span data-ttu-id="ab917-106">Uživatel se může registrovat, přihlásit a obnovit své heslo pomocí těchto toků.</span><span class="sxs-lookup"><span data-stu-id="ab917-106">A user can sign up, sign in, and reset their password through these flows.</span></span> <span data-ttu-id="ab917-107">Azure AD B2C ukládá citlivé informace o ověřování uživatele, například jeho uživatelské jméno a heslo.</span><span class="sxs-lookup"><span data-stu-id="ab917-107">Azure AD B2C stores sensitive user authentication information, such as username and password.</span></span> <span data-ttu-id="ab917-108">Záznam uživatele v klientovi B2C uloží buď záznam místního účtu B2C nebo záznam zprostředkovatele sociální identity B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-108">The user record in the B2C tenant will store either a B2C local account record or a B2C social identity provider record.</span></span> <span data-ttu-id="ab917-109">Tyto záznamy B2C budou odkazovat zpět na záznam odběratele v prostředí Commerce.</span><span class="sxs-lookup"><span data-stu-id="ab917-109">These B2C records will link back to the customer record in the Commerce environment.</span></span>

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a><span data-ttu-id="ab917-110">Vytvoření nebo připojení ke stávajícími klientovi AAD B2C v portálu Azure</span><span class="sxs-lookup"><span data-stu-id="ab917-110">Create or link to an existing AAD B2C tenant in the Azure portal</span></span>

1. <span data-ttu-id="ab917-111">Přihlaste se do [portálu Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="ab917-111">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="ab917-112">Z nabídky portálu Azure vyberte možnost **Vytvořit prostředek**.</span><span class="sxs-lookup"><span data-stu-id="ab917-112">From the Azure portal menu, select **Create a resource**.</span></span> <span data-ttu-id="ab917-113">Ujistěte se, že používáte předplatné a adresář, který bude připojen k vašemu prostředí Commerce.</span><span class="sxs-lookup"><span data-stu-id="ab917-113">Be sure to use the subscription and directory that will be connected with your Commerce environment.</span></span>

    ![Vytvoření prostředku na portálu Azure](./media/B2CImage_1.png)

1. <span data-ttu-id="ab917-115">Přejděte na **Identita \> Azure Active Directory B2C**.</span><span class="sxs-lookup"><span data-stu-id="ab917-115">Go to **Identity \> Azure Active Directory B2C**.</span></span>
1. <span data-ttu-id="ab917-116">Na stránce **Vytvoření nového klienta B2C nebo připojení k existujícímu klientovi** použijte jednu z následujících možností, které nejlépe vyhovují potřebám vaší společnosti:</span><span class="sxs-lookup"><span data-stu-id="ab917-116">Once on the **Create New B2C Tenant or Link to existing Tenant** page, use one of the options below that best suits your company's needs:</span></span>

    - <span data-ttu-id="ab917-117">**Vytvořit nového klienta Azure AD B2C**: Touto možností vytvoříte nového klienta AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-117">**Create a new Azure AD B2C Tenant**: Use this option to create a new AAD B2C tenant.</span></span>
        1. <span data-ttu-id="ab917-118">Vyberte **Vytvořit nového klienta Azure AD B2C**.</span><span class="sxs-lookup"><span data-stu-id="ab917-118">Select **Create a new Azure AD B2C Tenant**.</span></span>
        1. <span data-ttu-id="ab917-119">Pro **Název organizace** zadejte název organizace.</span><span class="sxs-lookup"><span data-stu-id="ab917-119">Under **Organization name**, enter the organization name.</span></span>
        1. <span data-ttu-id="ab917-120">Pro **Počáteční název domény** zadejte počáteční název domény.</span><span class="sxs-lookup"><span data-stu-id="ab917-120">Under **Initial domain name**, enter the initial domain name.</span></span>
        1. <span data-ttu-id="ab917-121">Pro **Země nebo oblast** vyberte zemi nebo oblast.</span><span class="sxs-lookup"><span data-stu-id="ab917-121">For **Country or region**, select the country or region.</span></span>
        1. <span data-ttu-id="ab917-122">Volbou **Vytvořit** vytvoříte klienta.</span><span class="sxs-lookup"><span data-stu-id="ab917-122">Select **Create** to create the tenant.</span></span>

     ![Vytvoření nového klienta Azure AD](./media/B2CImage_2.png)

     - <span data-ttu-id="ab917-124">**Propojit existujícího klienta Azure AD B2C s mým předplatným Azure**: Tuto možnost použijte, pokud již existuje klient Azure AD B2C, který chcete propojit.</span><span class="sxs-lookup"><span data-stu-id="ab917-124">**Link an existing Azure AD B2C Tenant to my Azure subscription**: Use this option if you already have an Azure AD B2C tenant you want to link to.</span></span>
        1. <span data-ttu-id="ab917-125">Vyberte **Propojit existujícího klienta Azure AD B2C s mým předplatným Azure**.</span><span class="sxs-lookup"><span data-stu-id="ab917-125">Select **Link an existing Azure AD B2C Tenant to my Azure subscription**.</span></span>
        1. <span data-ttu-id="ab917-126">Pro **Klient Azure AD B2C** vyberte příslušného klienta B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-126">For **Azure AD B2C Tenant**, select the appropriate B2C tenant.</span></span> <span data-ttu-id="ab917-127">Pokud se v oblasti výběru zobrazí zpráva „Nebyly nalezeni žádní oprávnění klienti B2C“, nemáte žádného existující oprávněného klienta B2C a budete muset vytvořit nového.</span><span class="sxs-lookup"><span data-stu-id="ab917-127">If the message "No eligible B2C Tenants found" appears in the selection box, you do not have an existing eligible B2C tenant and will need to create a new one.</span></span>
        1. <span data-ttu-id="ab917-128">Pro **Skupina prostředků** vyberte možnost **Vytvořit novou**.</span><span class="sxs-lookup"><span data-stu-id="ab917-128">For **Resource group**, select **Create new**.</span></span> <span data-ttu-id="ab917-129">Zadejte **Název** pro skupinu prostředků, která bude obsahovat klienta, vyberte **Umístění skupiny prostředků** a pak vyberte možnost **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="ab917-129">Enter a **Name** for the resource group that will contain the tenant, select the **Resource group location**, and then select **Create**.</span></span>

    ![Propojení existujícího klienta Azure AD B2C s předplatným Azure](./media/B2CImage_3.png)

1. <span data-ttu-id="ab917-131">Po vytvoření nového adresáře Azure AD B2C (což může chvíli trvat) se na řídicím panelu zobrazí odkaz na nový adresář.</span><span class="sxs-lookup"><span data-stu-id="ab917-131">Once the new Azure AD B2C directory is created (this may take a few moments), a link to the new directory will appear on the dashboard.</span></span> <span data-ttu-id="ab917-132">Tento odkaz vás přesměruje na stránku „Vítá vás Azure Active Directory B2C“.</span><span class="sxs-lookup"><span data-stu-id="ab917-132">This link will direct you to the "Welcome to Azure Active Directory B2C" page.</span></span>

    ![Odkaz na nový adresář AAD](./media/B2CImage_4.png)

> [!NOTE]
> <span data-ttu-id="ab917-134">Pokud máte více předplatných v rámci účtu Azure nebo jste zřídili klienta B2C bez propojení s aktivním předplatným, banner **Řešení potíží** vás nasměruje k propojení klienta a předplatného.</span><span class="sxs-lookup"><span data-stu-id="ab917-134">If you have multiple subscriptions within your Azure account or have set up the B2C tenant without linking to an active subscription, a **Troubleshoot** banner will direct you to link the tenant to a subscription.</span></span> <span data-ttu-id="ab917-135">Vyberte zprávu řešení potíží a podle pokynů vyřešte problém s předplatným.</span><span class="sxs-lookup"><span data-stu-id="ab917-135">Select the troubleshooting message and follow the instructions to resolve the subscription issue.</span></span>

<span data-ttu-id="ab917-136">Na následujícím obrázku je znázorněn příklad banneru **Řešení potíží** v Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-136">The following image shows an example of an Azure AD B2C **Troubleshoot** banner.</span></span>

![Upozornění, že adresář nemá žádné aktivní předplatné](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a><span data-ttu-id="ab917-138">Vytvoření aplikace B2C</span><span class="sxs-lookup"><span data-stu-id="ab917-138">Create the B2C application</span></span>

<span data-ttu-id="ab917-139">Po vytvoření klienta B2C vytvoříte aplikaci B2C s klientem pro interakci s akcemi Commerce.</span><span class="sxs-lookup"><span data-stu-id="ab917-139">Once the B2C tenant has been created, you will create a B2C application within the tenant to interact with the Commerce actions.</span></span>

<span data-ttu-id="ab917-140">Chcete-li vytvořit aplikaci B2C, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="ab917-140">To create the B2C application, follow these steps.</span></span>

1. <span data-ttu-id="ab917-141">Na portálu Azure vyberte možnost **Aplikace (starší verze)** a pak vyberte možnost **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="ab917-141">In the Azure portal, select **Applications(Legacy)** and then select **Add**.</span></span>
1. <span data-ttu-id="ab917-142">V poli **Název** zadejte název požadované aplikace AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-142">Under **Name**, enter the name of the desired AAD B2C application.</span></span>
1. <span data-ttu-id="ab917-143">V části **Webová aplikace/webové rozhraní API** vyberte pro **Zahrnout webovou aplikaci/webové rozhraní API** možnost **Ano**.</span><span class="sxs-lookup"><span data-stu-id="ab917-143">Under **Web App/Web API**, for **Include web app / web API**, select **Yes**.</span></span>
1. <span data-ttu-id="ab917-144">Pro **Povolit implicitní tok** vyberte možnost **Ano** (výchozí hodnota).</span><span class="sxs-lookup"><span data-stu-id="ab917-144">For **Allow implicit flow**, select **Yes** (the default value).</span></span>
1. <span data-ttu-id="ab917-145">Pro **Adresa URL odpovědi** zadejte vyhrazené adresy URL pro odpovědi.</span><span class="sxs-lookup"><span data-stu-id="ab917-145">Under **Reply URL**, enter your dedicated reply URLs.</span></span> <span data-ttu-id="ab917-146">Viz [Adresy URL pro odpovědi](#reply-urls) níže, kde najdete informace o adresách URL odpovědí a jak je naformátovat.</span><span class="sxs-lookup"><span data-stu-id="ab917-146">See [Reply URLs](#reply-urls) below for information on reply URLs and how to format them here.</span></span>
1. <span data-ttu-id="ab917-147">Pro **Zahrnout nativního klienta** vyberte možnost **Ne** (výchozí hodnota).</span><span class="sxs-lookup"><span data-stu-id="ab917-147">For **Include native client**, select **No** (the default value).</span></span>
1. <span data-ttu-id="ab917-148">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="ab917-148">Select **Create**.</span></span>

### <a name="reply-urls"></a><span data-ttu-id="ab917-149">Adresy URL pro odpovědi</span><span class="sxs-lookup"><span data-stu-id="ab917-149">Reply URLs</span></span>

<span data-ttu-id="ab917-150">Adresy URL pro odpovědi jsou důležité, protože poskytují seznam povolených návratových domén, když váš web volá Azure AD B2C pro ověření uživatele.</span><span class="sxs-lookup"><span data-stu-id="ab917-150">Reply URLs are important as they provide an allow list of the return domains when your site calls Azure AD B2C to authenticate a user.</span></span> <span data-ttu-id="ab917-151">To umožňuje vrátit ověřeného uživatele zpět do domény, ze které se přihlásí (doména vašeho webu).</span><span class="sxs-lookup"><span data-stu-id="ab917-151">This permits the return of the authenticated user back to the domain from which they are signing into (your site domain).</span></span> 

<span data-ttu-id="ab917-152">V poli **Adresa URL odpovědi** na obrazovce **Azure AD B2C – aplikace \> Nová aplikace** je nutné přidat samostatné řádky pro doménu vašeho webu a (po zřízení vašeho prostředí) adresu URL generovanou řešením Commerce.</span><span class="sxs-lookup"><span data-stu-id="ab917-152">In the **Reply URL** box on the **Azure AD B2c - Applications \> New application** screen, you need to add separate lines for both your site domain and (once your environment is provisioned) the Commerce-generated URL.</span></span> <span data-ttu-id="ab917-153">Tyto adresy URL musí vždy používat platný formát adresy URL a musí to být pouze základní adresy URL (bez koncového lomítka nebo cesty).</span><span class="sxs-lookup"><span data-stu-id="ab917-153">These URLs must always use a valid URL format and must be base URLs only (no trailing forward slashes or paths).</span></span> <span data-ttu-id="ab917-154">Řetězec ``/_msdyn365/authresp`` pak musí být přidán k základní adrese URL, jako v následujících příkladech.</span><span class="sxs-lookup"><span data-stu-id="ab917-154">The string ``/_msdyn365/authresp`` then needs to be appended to the base URLs, as in the following examples.</span></span>

- <span data-ttu-id="ab917-155">``https://www.fabrikam.com/_msdyn365/authresp``(Doména by se měla zcela shodovat s doménou elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="ab917-155">``https://www.fabrikam.com/_msdyn365/authresp`` (The domain should match the e-commerce domain completely.</span></span> <span data-ttu-id="ab917-156">Pokud máte více domén, musíte přidat tuto adresu URL pro každou doménu.)</span><span class="sxs-lookup"><span data-stu-id="ab917-156">If you have multiple domains, you need to add this URL for each domain.)</span></span>
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a><span data-ttu-id="ab917-157">Vytvoření zásad toku uživatele</span><span class="sxs-lookup"><span data-stu-id="ab917-157">Create user flow policies</span></span>

<span data-ttu-id="ab917-158">Toky uživatelů představují zásady, které Azure AD B2C používá k zajištění bezpečného přihlášení, registraci, úpravy profilu a obnově zapomenutého hesla.</span><span class="sxs-lookup"><span data-stu-id="ab917-158">User flows are the policies Azure AD B2C uses to provide secure sign in, sign up, edit profile, and forget password user experiences.</span></span> <span data-ttu-id="ab917-159">Dynamics 365 Commerce používá tyto toky k provádění akcí zásad pro interakci s klientem Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-159">Dynamics 365 Commerce uses these flows to perform the policy actions to interact with the Azure AD B2C tenant.</span></span> <span data-ttu-id="ab917-160">Pokud uživatel pracuje s těmito zásadami, je přesměrován na klienta Azure AD B2C, kde může provádět akce.</span><span class="sxs-lookup"><span data-stu-id="ab917-160">When a user interacts with these policies, they are redirected to the Azure AD B2C tenant to perform the actions.</span></span>

<span data-ttu-id="ab917-161">Azure AD B2C poskytuje tři základní typy toků uživatele:</span><span class="sxs-lookup"><span data-stu-id="ab917-161">Azure AD B2C provides three basic user flow types:</span></span>
- <span data-ttu-id="ab917-162">Registrace a přihlášení</span><span class="sxs-lookup"><span data-stu-id="ab917-162">Sign up and sign in</span></span>
- <span data-ttu-id="ab917-163">Úprava profilu</span><span class="sxs-lookup"><span data-stu-id="ab917-163">Profile editing</span></span>
- <span data-ttu-id="ab917-164">Obnovení hesla</span><span class="sxs-lookup"><span data-stu-id="ab917-164">Password reset</span></span>

<span data-ttu-id="ab917-165">Můžete zvolit, zda chcete použít výchozí toky uživatelů, které poskytuje Azure AD, čímž se zobrazí stránka hostovaná v AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-165">You can choose to use the default user flows provided by Azure AD, which will display a page hosted by AAD B2C.</span></span> <span data-ttu-id="ab917-166">Alternativně můžete vytvořit stránku HTML, která určí vzhled a chování těchto toků uživatelů.</span><span class="sxs-lookup"><span data-stu-id="ab917-166">Alternately, you can create an HTML page to control the look and feel of these user flow experiences.</span></span> 

<span data-ttu-id="ab917-167">Chcete-li přizpůsobit stránky zásad uživatelů pro Dynamics 365 Commerce, prostudujte si téma [Nastavení vlastních stránek pro přihlášení uživatelů](custom-pages-user-logins.md).</span><span class="sxs-lookup"><span data-stu-id="ab917-167">To customize the user policy pages for Dynamics 365 Commerce, see [Set up custom pages for user logins](custom-pages-user-logins.md).</span></span> <span data-ttu-id="ab917-168">Další informace naleznete v tématu [Přizpůsobení rozhraní uživatelských prostředí v Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span><span class="sxs-lookup"><span data-stu-id="ab917-168">For additional information, see [Customize the interface of user experiences in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span></span>

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a><span data-ttu-id="ab917-169">Vytvoření zásady toku uživatele pro registraci a přihlášení</span><span class="sxs-lookup"><span data-stu-id="ab917-169">Create a sign up and sign in user flow policy</span></span>

<span data-ttu-id="ab917-170">Chcete-li vytvořit zásadu toku uživatele pro registraci a přihlášení, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="ab917-170">To create a sign up and sign in user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="ab917-171">Na portálu Azure vyberte možnost **Toky uživatelů (zásady)** v levém navigačním podokně.</span><span class="sxs-lookup"><span data-stu-id="ab917-171">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="ab917-172">Na stránce **Azure AD B2C – toky uživatelů (zásady)** vyberte možnost **Nový tok uživatele**.</span><span class="sxs-lookup"><span data-stu-id="ab917-172">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="ab917-173">Na kartě **Doporučené** vyberte možnost **Registrace a přihlášení**.</span><span class="sxs-lookup"><span data-stu-id="ab917-173">On the **Recommended** tab, select **Sign up and sign in**.</span></span>
1. <span data-ttu-id="ab917-174">V položce **Název** zadejte název zásady.</span><span class="sxs-lookup"><span data-stu-id="ab917-174">Under **Name**, enter a policy name.</span></span> <span data-ttu-id="ab917-175">Tento název se pak zobrazí s použitím předpony, kterou přiřadí portál (například „B2C_1_“).</span><span class="sxs-lookup"><span data-stu-id="ab917-175">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="ab917-176">V části **Zprostředkovatelé identity** zaškrtněte příslušné políčko.</span><span class="sxs-lookup"><span data-stu-id="ab917-176">Under **Identity providers**, select the appropriate check box.</span></span>
1. <span data-ttu-id="ab917-177">V části **Vícefaktorové ověřování** vyberte vhodnou volbu pro vaši společnost.</span><span class="sxs-lookup"><span data-stu-id="ab917-177">Under **Multifactor Authentication**, select the appropriate choice for your company.</span></span> 
1. <span data-ttu-id="ab917-178">V části **Atributy a deklarace identit uživatelů** vyberte možnosti pro získání atributů nebo deklarací identit pro vrácení (podle potřeby).</span><span class="sxs-lookup"><span data-stu-id="ab917-178">Under **User attributes and claims**, select options to collect attributes or return claims as appropriate.</span></span> <span data-ttu-id="ab917-179">Commerce vyžaduje následující výchozí možnosti:</span><span class="sxs-lookup"><span data-stu-id="ab917-179">Commerce requires the following default options:</span></span>

    | <span data-ttu-id="ab917-180">**Získat atribut**</span><span class="sxs-lookup"><span data-stu-id="ab917-180">**Collect  attribute**</span></span> | <span data-ttu-id="ab917-181">**Vrátit deklaraci identity**</span><span class="sxs-lookup"><span data-stu-id="ab917-181">**Return  claim**</span></span> |
    | ---------------------- | ----------------- |
    | <span data-ttu-id="ab917-182">E-mailová adresa</span><span class="sxs-lookup"><span data-stu-id="ab917-182">Email Address</span></span>          | <span data-ttu-id="ab917-183">E-mailové adresy</span><span class="sxs-lookup"><span data-stu-id="ab917-183">Email Addresses</span></span>   |
    | <span data-ttu-id="ab917-184">Křestní jméno</span><span class="sxs-lookup"><span data-stu-id="ab917-184">Given Name</span></span>             | <span data-ttu-id="ab917-185">Křestní jméno</span><span class="sxs-lookup"><span data-stu-id="ab917-185">Given Name</span></span>        |
    |                        | <span data-ttu-id="ab917-186">Poskytovatel identity</span><span class="sxs-lookup"><span data-stu-id="ab917-186">Identity Provider</span></span> |
    | <span data-ttu-id="ab917-187">Příjmení</span><span class="sxs-lookup"><span data-stu-id="ab917-187">Surname</span></span>                | <span data-ttu-id="ab917-188">Příjmení</span><span class="sxs-lookup"><span data-stu-id="ab917-188">Surname</span></span>           |
    |                        | <span data-ttu-id="ab917-189">ID objektu uživatele</span><span class="sxs-lookup"><span data-stu-id="ab917-189">User’s Object ID</span></span>  |

1. <span data-ttu-id="ab917-190">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="ab917-190">Select **Create**.</span></span>

<span data-ttu-id="ab917-191">Následující obrázek je příkladem toku uživatele pro registraci a přihlášení Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-191">The following image is an example of the Azure AD B2C sign up and sign in user flow.</span></span>

![Nastavení zásady registrace a přihlášení](./media/B2CImage_11.png)

<span data-ttu-id="ab917-193">Následující obrázek znázorňuje možnost **Spustit tok uživatele** v toku uživatele pro registraci a přihlášení Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-193">The following image shows the **Run user flow** option in the Azure AD B2C sign up and sign in user flow.</span></span>

![Možnost Spustit tok uživatele v toku zásady](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a><span data-ttu-id="ab917-195">Vytvoření zásady toku uživatele pro úpravu profilu</span><span class="sxs-lookup"><span data-stu-id="ab917-195">Create a profile editing user flow policy</span></span>

<span data-ttu-id="ab917-196">Chcete-li vytvořit zásadu toku uživatele pro úpravu profilu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="ab917-196">To create a profile editing user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="ab917-197">Na portálu Azure vyberte možnost **Toky uživatelů (zásady)** v levém navigačním podokně.</span><span class="sxs-lookup"><span data-stu-id="ab917-197">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="ab917-198">Na stránce **Azure AD B2C – toky uživatelů (zásady)** vyberte možnost **Nový tok uživatele**.</span><span class="sxs-lookup"><span data-stu-id="ab917-198">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="ab917-199">Na kartě **Doporučené** vyberte možnost **Úprava profilu**.</span><span class="sxs-lookup"><span data-stu-id="ab917-199">On the **Recommended** tab, select **Profile editing**.</span></span>
1. <span data-ttu-id="ab917-200">V části **Název** zadejte tok uživatele pro úpravu profilu.</span><span class="sxs-lookup"><span data-stu-id="ab917-200">Under **Name**, enter the profile editing user flow.</span></span> <span data-ttu-id="ab917-201">Tento název se pak zobrazí s použitím předpony, kterou přiřadí portál (například „B2C_1_“).</span><span class="sxs-lookup"><span data-stu-id="ab917-201">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="ab917-202">V části **Zprostředkovatelé identity** vyberte možnost **Přihlášení k místnímu účtu**.</span><span class="sxs-lookup"><span data-stu-id="ab917-202">Under **Identity providers**, select **Local Account SignIn**.</span></span>
1. <span data-ttu-id="ab917-203">V části **Atributy uživatele** zaškrtněte některé z následujících políček:</span><span class="sxs-lookup"><span data-stu-id="ab917-203">Under **User attributes**, select the following check boxes:</span></span>
    - <span data-ttu-id="ab917-204">**E-mailové adresy** (pouze **Vrátit deklaraci identity**)</span><span class="sxs-lookup"><span data-stu-id="ab917-204">**Email Addresses** (**Return claim** only)</span></span>
    - <span data-ttu-id="ab917-205">**Křestní jméno** (**Získat atribut** a **Vrátit deklaraci identity**)</span><span class="sxs-lookup"><span data-stu-id="ab917-205">**Given Name** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="ab917-206">**Zprostředkovatel identity** (pouze **Vrátit deklaraci identity**)</span><span class="sxs-lookup"><span data-stu-id="ab917-206">**Identity Provider** (**Return claim** only)</span></span>
    - <span data-ttu-id="ab917-207">**Příjmení** (**Získat atribut** a **Vrátit deklaraci identity**)</span><span class="sxs-lookup"><span data-stu-id="ab917-207">**Surname** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="ab917-208">**ID objektu uživatele** (pouze **Vrátit deklaraci identity**)</span><span class="sxs-lookup"><span data-stu-id="ab917-208">**User's Object ID** (**Return claim** only)</span></span>
1. <span data-ttu-id="ab917-209">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="ab917-209">Select **Create**.</span></span>

<span data-ttu-id="ab917-210">Na následujícím obrázku je znázorněn příklad toku uživatele pro upravu profilu Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-210">The following image shows an example of the Azure AD B2C profile editing user flow.</span></span>

![Vytvoření toku uživatele pro úpravu profilu](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a><span data-ttu-id="ab917-212">Vytvoření zásady toku uživatele pro resetování hesla</span><span class="sxs-lookup"><span data-stu-id="ab917-212">Create a password reset user flow policy</span></span>

<span data-ttu-id="ab917-213">Chcete-li vytvořit zásadu toku uživatele pro resetování hesla, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="ab917-213">To create a password reset user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="ab917-214">Na portálu Azure vyberte možnost **Toky uživatelů (zásady)** v levém navigačním podokně.</span><span class="sxs-lookup"><span data-stu-id="ab917-214">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="ab917-215">Na stránce **Azure AD B2C – toky uživatelů (zásady)** vyberte možnost **Nový tok uživatele**.</span><span class="sxs-lookup"><span data-stu-id="ab917-215">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="ab917-216">Na kartě **Doporučené** vyberte možnost **Resetování hesla**.</span><span class="sxs-lookup"><span data-stu-id="ab917-216">On the **Recommended** tab, select **Password Reset**.</span></span>
1. <span data-ttu-id="ab917-217">V poli **Název** zadejte název toku uživatele pro resetování hesla.</span><span class="sxs-lookup"><span data-stu-id="ab917-217">Under **Name**, enter a name for the password reset user flow.</span></span>
1. <span data-ttu-id="ab917-218">V části **Zprostředkovatelé identity** vyberte možnost **Resetovat heslo pomocí e-mailové adresy**.</span><span class="sxs-lookup"><span data-stu-id="ab917-218">Under **Identity providers**, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="ab917-219">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="ab917-219">Select **Create**.</span></span>
1. <span data-ttu-id="ab917-220">V části **Deklarace identity aplikace** zaškrtněte některé z následujících políček:</span><span class="sxs-lookup"><span data-stu-id="ab917-220">Under **Application claims**, select the following check boxes:</span></span>
    - <span data-ttu-id="ab917-221">**E-mailové adresy**</span><span class="sxs-lookup"><span data-stu-id="ab917-221">**Email addresses**</span></span>
    - <span data-ttu-id="ab917-222">**Křestní jméno**</span><span class="sxs-lookup"><span data-stu-id="ab917-222">**Given Name**</span></span>
    - <span data-ttu-id="ab917-223">**Příjmení**</span><span class="sxs-lookup"><span data-stu-id="ab917-223">**Surname**</span></span>
    - <span data-ttu-id="ab917-224">**ID objektu uživatele**</span><span class="sxs-lookup"><span data-stu-id="ab917-224">**User's Object ID**</span></span>
1. <span data-ttu-id="ab917-225">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="ab917-225">Select **Create**.</span></span>

<span data-ttu-id="ab917-226">Následující obrázek znázorňuje, kde nastavit možnost **Resetovat heslo pomocí e-mailové adresy** v toku uživatele pro resetování hesla Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-226">The following image shows where to set **Reset Password using mail address** in the Azure AD B2C password reset user flow.</span></span>

![Nastavení možnosti „Resetovat heslo pomocí e-mailové adresy“ v zásadě pro resetování hesla](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a><span data-ttu-id="ab917-228">Přidání zprostředkovatelů sociální identity (volitelné)</span><span class="sxs-lookup"><span data-stu-id="ab917-228">Add social identity providers (Optional)</span></span>

<span data-ttu-id="ab917-229">Zprostředkovatelé sociální identity umožňují uživatelům používat účty sociálních sítí k ověřování.</span><span class="sxs-lookup"><span data-stu-id="ab917-229">Social identity providers allow users to use their social accounts for authentication.</span></span> <span data-ttu-id="ab917-230">Přidání ověření zprostředkovatele sociální identity je volitelné v Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ab917-230">Adding social identity provider authentication is optional in Dynamics 365 Commerce.</span></span> 

<span data-ttu-id="ab917-231">Pokud není přidáno ověřování zprostředkovatele sociální identity, budou výchozí profily Azure AD B2C hlavními profily pro vaše uživatele.</span><span class="sxs-lookup"><span data-stu-id="ab917-231">If social identity provider authentication is not added, the default Azure AD B2C profiles will be the main profiles for your user base.</span></span> <span data-ttu-id="ab917-232">Uživatelé budou moci vybrat vlastní uživatelské jméno (jejich upřednostňovaná e-mailová adresa) a nastavit heslo.</span><span class="sxs-lookup"><span data-stu-id="ab917-232">Users will select their own username (their preferred email address) and set a password.</span></span> <span data-ttu-id="ab917-233">Azure AD B2C bude uživatele ověřovat přímo.</span><span class="sxs-lookup"><span data-stu-id="ab917-233">Azure AD B2C will authenticate users directly.</span></span> 

<span data-ttu-id="ab917-234">Je-li přidáno ověřování zprostředkovatele sociální identity a uživatel si zvolí jednoho ze nabízených zprostředkovatelů sociální identity, bude v klientu Azure AD B2C vytvořena entita.</span><span class="sxs-lookup"><span data-stu-id="ab917-234">If social identity provider authentication is added and a user chooses one of the social identity providers offered, an entity is still created in the Azure AD B2C tenant.</span></span> <span data-ttu-id="ab917-235">Azure AD B2C poté ověří přihlašovací údaje uživatele pomocí zprostředkovatele sociální identity.</span><span class="sxs-lookup"><span data-stu-id="ab917-235">Azure AD B2C will then authenticate the user's credentials with the social identity provider.</span></span>

> [!NOTE]
> <span data-ttu-id="ab917-236">Přihlášení zprostředkovatele identity vytvoří záznam v klientovi B2C, ale v jiném formátu než místní účty, protože pro ověření bude volat externí odkaz na zprostředkovatele sociální identity.</span><span class="sxs-lookup"><span data-stu-id="ab917-236">The identity provider sign in creates a record in the B2C tenant, but in a different format than local accounts since it will call the external social identity provider reference for authentication.</span></span> <span data-ttu-id="ab917-237">Uživatel může použít stejnou e-mailovou adresu v rámci zprostředkovatelů sociální identity, což znamená, že uživatelské jméno e-mailu použité pro ověření nemusí být jedinečné pro klienta.</span><span class="sxs-lookup"><span data-stu-id="ab917-237">The user can use the same email address across social identity providers, meaning that the email username used for authentication may not be unique to the tenant.</span></span> <span data-ttu-id="ab917-238">Azure AD B2C pouze vynutí, aby uživatelé měli jedinečnou e-mailovou adresu v místních účtech B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-238">Azure AD B2C will only enforce that users have a unique email address on local B2C accounts.</span></span>

<span data-ttu-id="ab917-239">Před přidáním zprostředkovatele sociální identity pro ověřování je nutné přejít na portál zprostředkovatele identity a nastavit aplikaci zprostředkovatele identity tak, jak je uvedeno v dokumentaci k Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-239">Before you can add a social identity provider for authentication, you must go to the identity provider's portal and set up an identity provider application as instructed in the Azure AD B2C documentation.</span></span> <span data-ttu-id="ab917-240">Níže je uveden seznam odkazů na dokumentaci.</span><span class="sxs-lookup"><span data-stu-id="ab917-240">A list of links to the documentation is provided below.</span></span>

- [<span data-ttu-id="ab917-241">Amazon</span><span class="sxs-lookup"><span data-stu-id="ab917-241">Amazon</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [<span data-ttu-id="ab917-242">Azure AD (jeden klient)</span><span class="sxs-lookup"><span data-stu-id="ab917-242">Azure AD (Single Tenant)</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [<span data-ttu-id="ab917-243">Účet Microsoft</span><span class="sxs-lookup"><span data-stu-id="ab917-243">Microsoft Account</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [<span data-ttu-id="ab917-244">Facebook</span><span class="sxs-lookup"><span data-stu-id="ab917-244">Facebook</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [<span data-ttu-id="ab917-245">GitHub</span><span class="sxs-lookup"><span data-stu-id="ab917-245">GitHub</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [<span data-ttu-id="ab917-246">Google</span><span class="sxs-lookup"><span data-stu-id="ab917-246">Google</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [<span data-ttu-id="ab917-247">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="ab917-247">LinkedIn</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [<span data-ttu-id="ab917-248">OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="ab917-248">OpenID Connect</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [<span data-ttu-id="ab917-249">Twitter</span><span class="sxs-lookup"><span data-stu-id="ab917-249">Twitter</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a><span data-ttu-id="ab917-250">Přidání a nastavení zprostředkovatele sociální identity</span><span class="sxs-lookup"><span data-stu-id="ab917-250">Add and set up a social identity provider</span></span>

<span data-ttu-id="ab917-251">Chcete-li přidat a nastavit zprostředkovatele sociální identity, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="ab917-251">To add and set up a social identity provider, follow these steps.</span></span>  

1. <span data-ttu-id="ab917-252">V portálu Azure přejděte k **Zprostředkovatelé identity**.</span><span class="sxs-lookup"><span data-stu-id="ab917-252">In the Azure portal, navigate to **Identity Providers**.</span></span>
1. <span data-ttu-id="ab917-253">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="ab917-253">Select **Add**.</span></span> <span data-ttu-id="ab917-254">Zobrazí se obrazovka **Přidání zprostředkovatele identity**.</span><span class="sxs-lookup"><span data-stu-id="ab917-254">The **Add identity provider** screen appears.</span></span>
1. <span data-ttu-id="ab917-255">V části **Název** zadejte název, který se zobrazí uživatelům na vaší obrazovce pro přihlášení.</span><span class="sxs-lookup"><span data-stu-id="ab917-255">Under **Name**, enter the name to be displayed to users on your sign in screen.</span></span>
1. <span data-ttu-id="ab917-256">V části **Typ zprostředkovatele identity** vyberte zprostředkovatele identity ze seznamu.</span><span class="sxs-lookup"><span data-stu-id="ab917-256">Under **Identity provider type**, select an identity provider from the list.</span></span>
1. <span data-ttu-id="ab917-257">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="ab917-257">Select **OK**.</span></span>
1. <span data-ttu-id="ab917-258">Volbou **Nastavit tohoto zprostředkovatele identity** přistoupíte na obrazovku **Nastavení zprostředkovatele sociální identity**.</span><span class="sxs-lookup"><span data-stu-id="ab917-258">Select **Set up this identity provider** to access the **Set up the social identity provider** screen.</span></span>
1. <span data-ttu-id="ab917-259">V poli **ID klienta** zadejte ID klienta, které jste získali z nastavení aplikace zprostředkovatele identity.</span><span class="sxs-lookup"><span data-stu-id="ab917-259">Under **Client ID**, enter the client ID as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="ab917-260">V poli **Tajný klíč klienta** zadejte tajný klíč klienta, které jste získali z nastavení aplikace zprostředkovatele identity.</span><span class="sxs-lookup"><span data-stu-id="ab917-260">Under **Client secret**, enter the client secret as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="ab917-261">Připojte tok uživatele pro zásady přihlášení a registrace:</span><span class="sxs-lookup"><span data-stu-id="ab917-261">Attach user flow for sign in sign up policies:</span></span>
1. <span data-ttu-id="ab917-262">Přejděte na **Azure AD B2C – toky uživatelů (zásady) \> {vaše zásada pro přihlášení a registraci} \> Zprostředkovatelé identity**.</span><span class="sxs-lookup"><span data-stu-id="ab917-262">Go to **Azure AD B2C – User flows (policies) \> {your sign-in sign-up policy} \> Identity providers**.</span></span>
1. <span data-ttu-id="ab917-263">Chcete-li připojit zásadu toku uživatele pro přihlášení/registraci, vyberte každého zprostředkovatele identity, kterého jste pro svůj účet nastavili.</span><span class="sxs-lookup"><span data-stu-id="ab917-263">To attach the sign in/sign up user flow policy, select each identity provider you have set up for your account.</span></span> <span data-ttu-id="ab917-264">Chcete-li je otestovat, vyberte možnost **Spustit tok uživatele** pro každého zprostředkovatele identity.</span><span class="sxs-lookup"><span data-stu-id="ab917-264">To test these, select **Run user flow** for each identity provider.</span></span> <span data-ttu-id="ab917-265">Na nové kartě se zobrazí stránka pro přihlášení s oblastí výběru nového zprostředkovatele identity.</span><span class="sxs-lookup"><span data-stu-id="ab917-265">A new tab will display the sign-in page displaying the new identity provider selection box.</span></span>

<span data-ttu-id="ab917-266">Následující obrázek znázorňuje příklad obrazovek **Přidání zprostředkovatele identity** a **Nastavení zprostředkovatele** sociální identity v Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-266">The following image shows examples of the **Add identity provider** and **Set up the social identity provider** screens in Azure AD B2C.</span></span>

![Přidání poskytovatele sociální identity do aplikace](./media/B2CImage_14.png)

<span data-ttu-id="ab917-268">Následující obrázek znázorňuje příklad, jak vybrat zprostředkovatele identity na stránce **Zprostředkovatelé identity** v Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-268">The following image shows an example of how to select identity providers on the Azure AD B2C **Identity Providers** page.</span></span>

![Výběr jednotlivých zprostředkovatelů sociální identity a povolení vaší zásady](./media/B2CImage_16.png)

<span data-ttu-id="ab917-270">Následující obrázek znázorňuje příklad výchozí přihlašovací obrazovky se zobrazeným tlačítkem pro přihlášení zprostředkovatele sociální identity.</span><span class="sxs-lookup"><span data-stu-id="ab917-270">The following image shows an example of a default sign-in screen with a social identity provider sign-in button displayed.</span></span>

![Příklad výchozí obrazovky pro přihlášení se zobrazeným tlačítkem pro přihlášení zprostředkovatele sociální identity](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a><span data-ttu-id="ab917-272">Aktualizace Commerce Headquarters o nové informace Azure AD B2C</span><span class="sxs-lookup"><span data-stu-id="ab917-272">Update Commerce headquarters with the new Azure AD B2C information</span></span>

<span data-ttu-id="ab917-273">Po dokončení výše uvedených kroků pro zřízení Azure AD B2C musí být aplikace Azure AD B2C registrována ve vašem prostředí Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ab917-273">Once the Azure AD B2C provisioning steps above are completed, the Azure AD B2C application must be registered in your Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="ab917-274">Chcete-li aktualizovat Headquarters o nové informace Azure AD B2C, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="ab917-274">To update headquarters with the new Azure AD B2C information, follow these steps.</span></span>

1. <span data-ttu-id="ab917-275">V Commerce přejděte na **Sdílené parametry Commerce** a vyberte **Zprostředkovatelé identity** v levé nabídce.</span><span class="sxs-lookup"><span data-stu-id="ab917-275">In Commerce, go to **Commerce Shared Parameters** and select **Identity Providers** in the left menu.</span></span>
1. <span data-ttu-id="ab917-276">V části **Zprostředkovatelé identity** postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="ab917-276">Under **Identity Providers**, do the following:</span></span>
    1. <span data-ttu-id="ab917-277">V poli **Vystavitel** zadejte adresu URL vystavitele zprostředkovatele identity.</span><span class="sxs-lookup"><span data-stu-id="ab917-277">In the **Issuer** box, enter the identity provider issuer URL.</span></span> <span data-ttu-id="ab917-278">Chcete-li najít adresu URL svého vystavitele, viz [Získání adresy URL vystavitele](#obtain-issuer-url) níže.</span><span class="sxs-lookup"><span data-stu-id="ab917-278">To find your issuer URL, see [Obtain issuer URL](#obtain-issuer-url) below.</span></span>
    1. <span data-ttu-id="ab917-279">Do pole **Název** zadejte název záznamu vystavitele.</span><span class="sxs-lookup"><span data-stu-id="ab917-279">In the **Name** box, enter a name for your issuer record.</span></span>
    1. <span data-ttu-id="ab917-280">Do pole **Typ** zadejte **Azure AD B2C (id_token)**.</span><span class="sxs-lookup"><span data-stu-id="ab917-280">In the **Type** box, enter **Azure AD B2C (id_token)**.</span></span>
1. <span data-ttu-id="ab917-281">V části **Předávající strany** s výše vybranou položkou zprostředkovatele identity B2C postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="ab917-281">Under **Relying Parties**, with the above B2C identity provider item selected, do the following:</span></span>
    1. <span data-ttu-id="ab917-282">V poli **ID klienta** zadejte ID aplikace B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-282">In the **ClientID** box, enter your B2C application ID.</span></span> <span data-ttu-id="ab917-283">To lze nalézt v poli **ID aplikace** na stránce vlastností aplikace B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-283">You can find this in the **Application ID** box of your B2C application's properties page.</span></span>
    1. <span data-ttu-id="ab917-284">Do pole **Typ** zadejte **Veřejné**.</span><span class="sxs-lookup"><span data-stu-id="ab917-284">In the **Type** box, enter **Public**.</span></span>
    1. <span data-ttu-id="ab917-285">Do pole **Typ uživatele** zadejte **Zákazník**.</span><span class="sxs-lookup"><span data-stu-id="ab917-285">In the **User Type** box, enter **Customer**.</span></span>
1. <span data-ttu-id="ab917-286">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="ab917-286">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="ab917-287">Ve vyhledávacím poli Commerce Search vyhledejte **Plán distribuce**.</span><span class="sxs-lookup"><span data-stu-id="ab917-287">In the Commerce search box, search for **Distribution schedule**</span></span>
1. <span data-ttu-id="ab917-288">V levé navigační nabídce stránky **Plán distribuce** vyberte úlohu **1110 Globální konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="ab917-288">In the left navigation menu of the **Distribution schedules** page, select job **1110 Global configuration**.</span></span>
1. <span data-ttu-id="ab917-289">V podokně akcí zvolte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="ab917-289">On the action pane, select **Run Now**.</span></span>

### <a name="obtain-issuer-url"></a><span data-ttu-id="ab917-290">Získání adresy URL vystavitele</span><span class="sxs-lookup"><span data-stu-id="ab917-290">Obtain issuer URL</span></span>

<span data-ttu-id="ab917-291">Chcete-li získat adresu URL vystavitele svého zprostředkovatele identity, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="ab917-291">To obtain your identity provider issuer URL, follow these steps.</span></span>

1. <span data-ttu-id="ab917-292">V následujícím formátu vytvořte adresu URL metadat s použitím vašeho klienta a zásady B2C: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span><span class="sxs-lookup"><span data-stu-id="ab917-292">Create a metadata address URL in the following format using your B2C tenant and policy: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span></span>
    - <span data-ttu-id="ab917-293">Příklad: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span><span class="sxs-lookup"><span data-stu-id="ab917-293">Example: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span></span>
1. <span data-ttu-id="ab917-294">Do adresního řádku prohlížeče zadejte adresu URL metadat.</span><span class="sxs-lookup"><span data-stu-id="ab917-294">Enter the metadata address URL into a browser address bar.</span></span>
1. <span data-ttu-id="ab917-295">V metadatech zkopírujte adresu URL vystavitele zprostředkovatele identity (hodnota pro **„vystavitel“**).</span><span class="sxs-lookup"><span data-stu-id="ab917-295">In the metadata, copy the identity provider issuer URL (the value for **"issuer"**).</span></span>
    - <span data-ttu-id="ab917-296">Příklad: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span><span class="sxs-lookup"><span data-stu-id="ab917-296">Example: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span></span>

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a><span data-ttu-id="ab917-297">Konfigurace klienta B2C v konfigurátoru webů Commerce</span><span class="sxs-lookup"><span data-stu-id="ab917-297">Configure your B2C tenant in Commerce site builder</span></span>

<span data-ttu-id="ab917-298">Po dokončení nastavení klienta Azure AD B2C musíte nakonfigurovat klienta B2C v konfigurátoru webů Commerce.</span><span class="sxs-lookup"><span data-stu-id="ab917-298">Once setup of your Azure AD B2C tenant is completed, you must configure the B2C tenant in Commerce site builder.</span></span> <span data-ttu-id="ab917-299">Kroky konfigurace zahrnují získání informací o aplikaci B2C z portálu Azure, zadání informací o aplikaci B2C do konfigurátru webů a následné přidružení aplikace B2C k vašemu webu a kanálu.</span><span class="sxs-lookup"><span data-stu-id="ab917-299">Configuration steps include collecting B2C application information from the Azure portal, entering that B2C application information into site builder, and then associating the B2C application with your site and channel.</span></span>

### <a name="collect-the-required-application-information"></a><span data-ttu-id="ab917-300">Získání požadovaných informací o aplikaci</span><span class="sxs-lookup"><span data-stu-id="ab917-300">Collect the required application information</span></span>

<span data-ttu-id="ab917-301">Chcete-li získat požadované informace o aplikaci, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="ab917-301">To collect the required application information, follow these steps.</span></span>

1. <span data-ttu-id="ab917-302">V portálu Azure přejděte na **Domovská stránka \> Azure AD B2C – aplikace**.</span><span class="sxs-lookup"><span data-stu-id="ab917-302">In the Azure portal, go to **Home \> Azure AD B2C - Applications**.</span></span>
1. <span data-ttu-id="ab917-303">Pro získání podrobností o aplikaci vyberte svou aplikaci a v levém navigačním podokně vyberte **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="ab917-303">Select your application, and then in the left navigation pane select **Properties** to obtain the application details.</span></span>
1. <span data-ttu-id="ab917-304">Z pole **ID aplikace** získejte ID aplikace B2C vytvořené ve vašem klientovi B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-304">From the **Application ID** box, collect the application ID of the B2C application created in your B2C tenant.</span></span> <span data-ttu-id="ab917-305">Později bude zadáno jako **GUID klienta** v konfigurátoru webů.</span><span class="sxs-lookup"><span data-stu-id="ab917-305">This will later be entered as the **Client GUID** in site builder.</span></span>
1. <span data-ttu-id="ab917-306">V poli **AdresaURL odpovědi** získejte adresu URL odpovědi.</span><span class="sxs-lookup"><span data-stu-id="ab917-306">Under **Reply URL**, collect the reply URL.</span></span>
1. <span data-ttu-id="ab917-307">Přejděte na **Domovská stránka \> Azure AD B2C – toky uživatelů (zásady)** a získejte názvy jednotlivých zásad toku uživatelů.</span><span class="sxs-lookup"><span data-stu-id="ab917-307">Go to **Home \> Azure AD B2C – User flows (policies)**, and then collect the names of each user flow policy.</span></span>

<span data-ttu-id="ab917-308">Na následujícím obrázku je znázorněn příklad stránky **Azure AD B2C – aplikace**.</span><span class="sxs-lookup"><span data-stu-id="ab917-308">The following image shows an example of the **Azure AD B2C - Applications** page.</span></span>

![Přechod k aplikaci B2C ve vašem klientovi](./media/B2CImage_19.png)

<span data-ttu-id="ab917-310">Na následujícím obrázku je znázorněn příklad stránky **Vlastnosti** aplikace v Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-310">The following image shows an example of an application **Properties** page in Azure AD B2C.</span></span> 

![Kopírování ID aplikace z vlastností aplikace B2C](./media/B2CImage_21.png)

<span data-ttu-id="ab917-312">Následující obrázek znázorňuje příklad zásad toku uživatelů na stránce **Azure AD B2C – toky uživatelů (zásady)**.</span><span class="sxs-lookup"><span data-stu-id="ab917-312">The following image shows an example of user flow policies on the **Azure AD B2C – User flows (policies)** page.</span></span>

![Získání názvů jednotlivých toků zásad B2C](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a><span data-ttu-id="ab917-314">Zadání informací o aplikaci klienta AAD B2C do platformy Commerce</span><span class="sxs-lookup"><span data-stu-id="ab917-314">Enter your AAD B2C tenant application information into Commerce</span></span>

<span data-ttu-id="ab917-315">Před přidružením klienta B2C ke svým webům je nutné zadat podrobnosti o klientovi Azure AD B2C do konfigurátoru webů Commerce.</span><span class="sxs-lookup"><span data-stu-id="ab917-315">You must enter details of the Azure AD B2C tenant into Commerce site builder before associating the B2C tenant with your site(s).</span></span>

<span data-ttu-id="ab917-316">Chcete-li do platformy Commerce přidat informace o aplikaci klienta AAD B2C, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="ab917-316">To add your AAD B2C tenant application information to Commerce, follow these steps.</span></span>

1. <span data-ttu-id="ab917-317">Přihlaste se jako správce ke konfigurátoru webů Commerce pro vaše prostředí.</span><span class="sxs-lookup"><span data-stu-id="ab917-317">Sign in as an administrator to Commerce site builder for your environment.</span></span>
1. <span data-ttu-id="ab917-318">V levém navigačním podokně vyberte **Nastavení klienta**, čímž jej rozbalíte.</span><span class="sxs-lookup"><span data-stu-id="ab917-318">In the left navigation pane, select **Tenant Settings**  to expand it.</span></span>
1. <span data-ttu-id="ab917-319">V části **Nastavení klienta** vyberte **Nastavení B2C**.</span><span class="sxs-lookup"><span data-stu-id="ab917-319">Under **Tenant Settings**, select **B2C Settings**.</span></span> 
1. <span data-ttu-id="ab917-320">V hlavním okně vedle položky **Aplikace B2C** vyberte možnost **Spravovat**.</span><span class="sxs-lookup"><span data-stu-id="ab917-320">In the main window next **B2C Applications**, select **Manage**.</span></span> <span data-ttu-id="ab917-321">(Pokud se klient zobrazí v seznamu aplikací B2C, pak již byl přidán správcem.</span><span class="sxs-lookup"><span data-stu-id="ab917-321">(If your tenant appears in the B2C Applications list, then it was already added by an administrator.</span></span> <span data-ttu-id="ab917-322">Ověřte, že položky v kroku 6 odpovídají vaší aplikaci B2C.)</span><span class="sxs-lookup"><span data-stu-id="ab917-322">Verify that the items in step 6 below match your B2C Application.)</span></span>
1. <span data-ttu-id="ab917-323">Vyberte **Přidat aplikaci B2C**.</span><span class="sxs-lookup"><span data-stu-id="ab917-323">Select **Add B2C Application**.</span></span>
1. <span data-ttu-id="ab917-324">Ve zobrazeném formuláři zadejte následující požadované položky s použitím hodnot z klienta a aplikace B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-324">Enter the following required items in the form displayed, using values from your B2C tenant and application.</span></span> <span data-ttu-id="ab917-325">Pole, která nejsou vyžadována (bez hvězdičky), mohou být ponechána prázdná.</span><span class="sxs-lookup"><span data-stu-id="ab917-325">Fields that are not required (those without an asterisk) may be left blank.</span></span>

    - <span data-ttu-id="ab917-326">**Název aplikace**: název aplikace B2C, například „Fabrikam B2C“.</span><span class="sxs-lookup"><span data-stu-id="ab917-326">**Application Name**: The name for your B2C Application, for example "Fabrikam B2C".</span></span>
    - <span data-ttu-id="ab917-327">**Název klienta**: Název klienta B2C (použijte například "fabrikam", pokud se doména pro klienta B2C zobrazuje jako "fabrikam.onmicrosoft.com").</span><span class="sxs-lookup"><span data-stu-id="ab917-327">**Tenant Name**: The name of your B2C tenant (for example, use "fabrikam" if the domain appears as "fabrikam.onmicrosoft.com" for the B2C tenant).</span></span> 
    - <span data-ttu-id="ab917-328">**ID zásady zapomenutého hesla**: ID zásady toku uživatele pro zapomenuté heslo, například „B2C_1_ResetovaniHesla“.</span><span class="sxs-lookup"><span data-stu-id="ab917-328">**Forget Password Policy ID**: The forget password user flow policy ID, for example "B2C_1_PasswordReset".</span></span>
    - <span data-ttu-id="ab917-329">**ID zásady registrace a přihlášení**: ID zásady toku uživatele pro registraci a přihlášení, například „B2C_1_registrace_prihlaseni“.</span><span class="sxs-lookup"><span data-stu-id="ab917-329">**Signup Signin Policy ID**: The sign up and sign in user flow policy ID, for example "B2C_1_signup_signin".</span></span>
    - <span data-ttu-id="ab917-330">**GUID klienta**: ID aplikace B2C, například „22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6“.</span><span class="sxs-lookup"><span data-stu-id="ab917-330">**Client GUID**: The B2C application ID, for example "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span></span>
    - <span data-ttu-id="ab917-331">**ID zásady úpravy profilu**: ID zásady toku uživatele pro úpravu profilu, například „B2C_1A_UpravaProfilu“.</span><span class="sxs-lookup"><span data-stu-id="ab917-331">**Edit Profile Policy ID**: The profile editing user flow policy ID, for example "B2C_1A_ProfileEdit".</span></span>

1. <span data-ttu-id="ab917-332">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="ab917-332">Select **OK**.</span></span> <span data-ttu-id="ab917-333">Nyní by se měl zobrazit název vaší aplikace B2C v seznamu.</span><span class="sxs-lookup"><span data-stu-id="ab917-333">You should now see the name of your B2C application appear in the list.</span></span>
1. <span data-ttu-id="ab917-334">Klepnutím na tlačítko **Uložit** uložte změny.</span><span class="sxs-lookup"><span data-stu-id="ab917-334">Select **Save** to save your changes.</span></span>

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a><span data-ttu-id="ab917-335">Přidružení aplikace B2C k webu a kanálu</span><span class="sxs-lookup"><span data-stu-id="ab917-335">Associate the B2C application to your site and channel</span></span>

> [!WARNING]
> <span data-ttu-id="ab917-336">Pokud je váš web již přidružen k aplikaci B2C, změna na jinou aplikaci B2C odstraní aktuální odkazy vytvořené pro uživatele, které jsou již zaregistrováni v tomto prostředí.</span><span class="sxs-lookup"><span data-stu-id="ab917-336">If your site is already associated with a B2C application, changing to a different B2C application will remove the current references established for users already signed up in this environment.</span></span> <span data-ttu-id="ab917-337">V případě změny nebudou mít uživatelé k dispozici žádná pověření přidružená k aktuálně přiřazené aplikaci B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-337">If changed, any credentials associated with the currently-assigned B2C application will not be available to users.</span></span> 
> 
> <span data-ttu-id="ab917-338">Aplikaci B2C aktualizujte pouze v případě, že aplikaci B2C kanálu zřizujete poprvé, nebo pokud čekáte, že se uživatelé znovu zaregistrují s novými pověřeními pro tento kanál pomocí nové aplikace B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-338">Only update the B2C application if you are setting up the channel's B2C application for the first time or if you intend to have users re-sign up with new credentials to this channel with the new B2C application.</span></span> <span data-ttu-id="ab917-339">Buďte opatrní při přiřazování kanálů k aplikacím B2C a pojmenovávejte aplikace srozumitelně.</span><span class="sxs-lookup"><span data-stu-id="ab917-339">Take caution when associating channels to B2C applications, and name applications clearly.</span></span> <span data-ttu-id="ab917-340">Není-li kanál přidružen k aplikaci B2C v níže uvedených krocích, uživatelé přihlašující se k tomuto kanálu pro váš web budou zadáni do aplikace B2C, která se zobrazí jako **výchozí** v seznamu aplikací B2C v umístění **Nastavení klienta \> Nastavení B2C**.</span><span class="sxs-lookup"><span data-stu-id="ab917-340">If a channel is not associated to a B2C application in the steps below, users signing into that channel for your site will be entered into the B2C application showing as **default** in the **Tenant Settings \> B2C Settings** list of B2C applications.</span></span>

<span data-ttu-id="ab917-341">Chcete-li přidružit aplikaci B2C k webu a kanálu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="ab917-341">To associate the B2C application to your site and channel, follow these steps.</span></span>

1. <span data-ttu-id="ab917-342">Přejděte na svůj web konfigurátoru webů Commerce.</span><span class="sxs-lookup"><span data-stu-id="ab917-342">Navigate to your site in Commerce site builder.</span></span>
1. <span data-ttu-id="ab917-343">V levém navigačním podokně vyberte **Nastavení webu** a rozbalte je.</span><span class="sxs-lookup"><span data-stu-id="ab917-343">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="ab917-344">Pod položkou **Nastavení webu** vyberte možnost **Kanály**.</span><span class="sxs-lookup"><span data-stu-id="ab917-344">Below **Site Settings**, select **Channels**.</span></span>
1. <span data-ttu-id="ab917-345">V hlavním okně v části **Kanály** vyberte svůj kanál.</span><span class="sxs-lookup"><span data-stu-id="ab917-345">In the main window under **Channels**, select your channel.</span></span>
1. <span data-ttu-id="ab917-346">V podokně vlastností kanálu vpravo vyberte název svojí aplikace B2C z rozevírací nabídky **Vybrat aplikaci B2C**.</span><span class="sxs-lookup"><span data-stu-id="ab917-346">In the channel properties pane on the right, select your B2C application name from the **Select B2C Application** drop down menu.</span></span>
1. <span data-ttu-id="ab917-347">Vyberte možnost **Zavřít** a pak vyberte možnost **Uložit a publikovat**.</span><span class="sxs-lookup"><span data-stu-id="ab917-347">Select **Close**, and then select **Save and Publish**.</span></span>

## <a name="additional-b2c-information"></a><span data-ttu-id="ab917-348">Doplňkové informace o B2C</span><span class="sxs-lookup"><span data-stu-id="ab917-348">Additional B2C information</span></span>

### <a name="customer-migration"></a><span data-ttu-id="ab917-349">Migrace zákazníků</span><span class="sxs-lookup"><span data-stu-id="ab917-349">Customer migration</span></span>

<span data-ttu-id="ab917-350">Pokud uvažujete o migraci záznamů zákazníků z předchozí platformy zprotředkovatele identity, spolupracujte s týmem Dynamics 365 Commerce, abyste zkontrolovali potřeby zákazníka ohledně migrace.</span><span class="sxs-lookup"><span data-stu-id="ab917-350">If you are considering migrating customer records from a previous identity provider platform, please work with the Dynamics 365 Commerce team to review your customer migration needs.</span></span>

<span data-ttu-id="ab917-351">Další dokumentaci Azure AD B2C ohledně migrace zákazníků najdete v tématu [Migrace uživatelů do Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span><span class="sxs-lookup"><span data-stu-id="ab917-351">For additional Azure AD B2C documentation on customer migration, see [Migrate users to Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span></span>

### <a name="custom-policies"></a><span data-ttu-id="ab917-352">Vlastní zásady</span><span class="sxs-lookup"><span data-stu-id="ab917-352">Custom policies</span></span>

<span data-ttu-id="ab917-353">Další informace o přizpůsobení interakcí a toků zásad Azure AD B2C nad rámec toho, co je nabídnuto standardními zásadami B2C, naleznete v tématu [Vlastní zásady v Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span><span class="sxs-lookup"><span data-stu-id="ab917-353">For additional information regarding customizing Azure AD B2C interactions and policy flows beyond what is offered by B2C standard policies, see [Custom policies in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span></span> 

### <a name="secondary-admin"></a><span data-ttu-id="ab917-354">Sekundární správce</span><span class="sxs-lookup"><span data-stu-id="ab917-354">Secondary admin</span></span>

<span data-ttu-id="ab917-355">Nepovinný sekundární účet správce lze přidat do oddílu **Uživatelé** v klientovi B2C.</span><span class="sxs-lookup"><span data-stu-id="ab917-355">An optional, secondary administrator account can be added in the **Users** section of your B2C tenant.</span></span> <span data-ttu-id="ab917-356">Může se jednat o přímý nebo obecný účet.</span><span class="sxs-lookup"><span data-stu-id="ab917-356">This can be a direct account or a general account.</span></span> <span data-ttu-id="ab917-357">Potřebujete-li sdílet účet v prostředcích týmu, je možné také vytvořit běžný účet.</span><span class="sxs-lookup"><span data-stu-id="ab917-357">If you need to share an account across team resources, a common account can also be created.</span></span> <span data-ttu-id="ab917-358">Vzhledem k citlivosti dat uložených v Azure AD B2C je třeba společný účet pečlivě monitorovat dle bezpečnostních postupů společnosti.</span><span class="sxs-lookup"><span data-stu-id="ab917-358">Due to the sensitivity of the data stored in Azure AD B2C, a common account should be monitored closely per your company's security practices.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ab917-359">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="ab917-359">Additional resources</span></span>

[<span data-ttu-id="ab917-360">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="ab917-360">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="ab917-361">Nasazení nového klienta elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="ab917-361">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="ab917-362">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="ab917-362">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="ab917-363">Přidružení webu Dynamics 365 Commerce k online kanálu</span><span class="sxs-lookup"><span data-stu-id="ab917-363">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="ab917-364">Správa souborů robots.txt</span><span class="sxs-lookup"><span data-stu-id="ab917-364">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

<span data-ttu-id="ab917-365">[Hromadné odeslání přesměrování URL adresy](upload-bulk-redirects.md) Přidružení webu Dynamics 365 Commerce k online kanálu</span><span class="sxs-lookup"><span data-stu-id="ab917-365">[Upload URL redirects in bulk](upload-bulk-redirects.md)Associate a Dynamics 365 Commerce site with an online channel</span></span>

[<span data-ttu-id="ab917-366">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="ab917-366">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="ab917-367">Konfigurace více klientů B2C v prostředí Commerce</span><span class="sxs-lookup"><span data-stu-id="ab917-367">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="ab917-368">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="ab917-368">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="ab917-369">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="ab917-369">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
