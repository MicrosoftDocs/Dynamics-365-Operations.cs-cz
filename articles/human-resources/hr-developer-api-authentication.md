---
title: Ověřování
description: Tento článek obsahuje přehled informací o ověřování pomocí rozhraní API (Microsoft Dynamics 365 Human Resources data Application Programming Interface).
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 963bec2b817c59e3b5860c5ff5885e165ec8656a
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115553"
---
# <a name="authentication"></a><span data-ttu-id="09fd5-103">Ověřování</span><span class="sxs-lookup"><span data-stu-id="09fd5-103">Authentication</span></span>

<span data-ttu-id="09fd5-104">Tento článek obsahuje přehled informací o ověřování pomocí rozhraní API (Microsoft Dynamics 365 Human Resources data Application Programming Interface).</span><span class="sxs-lookup"><span data-stu-id="09fd5-104">This article provides overview information about how to authenticate with the Microsoft Dynamics 365 Human Resources data application programming interface (API).</span></span>

## <a name="overview"></a><span data-ttu-id="09fd5-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="09fd5-105">Overview</span></span>

<span data-ttu-id="09fd5-106">Datové rozhraní API pro Human Resources je implementací OData.</span><span class="sxs-lookup"><span data-stu-id="09fd5-106">The data API for Human Resources is an OData implementation.</span></span> <span data-ttu-id="09fd5-107">Další informace naleznete v tématu[Protokol Open Data (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span><span class="sxs-lookup"><span data-stu-id="09fd5-107">For more information, see [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span></span>

<span data-ttu-id="09fd5-108">Vaše aplikace musí být ověřena jako autorizovaný volající před tím, než rozhraní API bude obsluhovat žádosti z vaší aplikace.</span><span class="sxs-lookup"><span data-stu-id="09fd5-108">Your application must authenticate as an authorized caller before the API will service requests from your application.</span></span>

## <a name="fundamentals"></a><span data-ttu-id="09fd5-109">Základy</span><span class="sxs-lookup"><span data-stu-id="09fd5-109">Fundamentals</span></span>

<span data-ttu-id="09fd5-110">Chcete-li volat datové rozhraní API, aplikace musí získat přístupový token z platformy Microsoft Identity.</span><span class="sxs-lookup"><span data-stu-id="09fd5-110">To call the data API, your application must acquire an access token from the Microsoft identity platform.</span></span> <span data-ttu-id="09fd5-111">Přístupový token obsahuje informace o vaší přihlášce a oprávnění, které musí volat zdroje v aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="09fd5-111">The access token contains information about your application and the permission that it has to call resources in Human Resources.</span></span>

### <a name="access-token"></a><span data-ttu-id="09fd5-112">Token přístupu</span><span class="sxs-lookup"><span data-stu-id="09fd5-112">Access token</span></span>

<span data-ttu-id="09fd5-113">Přístupové tokeny vydané platformou Microsoft Identity jsou webové tokeny JavaScript Object Notation (JSON) (JWT) využívající šifrování base64.</span><span class="sxs-lookup"><span data-stu-id="09fd5-113">Access tokens issued by the Microsoft identity platform are base64–encoded JavaScript Object Notation (JSON) Web Tokens (JWTs).</span></span> <span data-ttu-id="09fd5-114">Obsahují informace (nároky), které rozhraní API dat (a jiná webová rozhraní zabezpečená platformou Microsoft Identity) používají k ověření volajícího a ověření, zda má volající správná oprávnění k provádění požadované operace.</span><span class="sxs-lookup"><span data-stu-id="09fd5-114">They contain information (claims) that the data API (and other web APIs that are secured by the Microsoft identity platform) use to validate the caller and make sure that the caller has the correct permissions to perform the operation they're requesting.</span></span> <span data-ttu-id="09fd5-115">Během volání můžete považovat přístupové tokeny za neprůhledné.</span><span class="sxs-lookup"><span data-stu-id="09fd5-115">During calls, you can treat access tokens as opaque.</span></span> <span data-ttu-id="09fd5-116">Měli byste vždy přenášet přístupové tokeny prostřednictvím zabezpečeného kanálu, jako je například protokol TLS (Transport Layer Security) a protokol HTTP (Hypertext Transfer Protocol Secure).</span><span class="sxs-lookup"><span data-stu-id="09fd5-116">You should always transmit access tokens over a secure channel, such as Transport Layer Security (TLS) and Hypertext Transfer Protocol Secure (HTTPS).</span></span>

<span data-ttu-id="09fd5-117">Zde je příklad přístupového tokenu vydaného platformou Microsoft Identity.</span><span class="sxs-lookup"><span data-stu-id="09fd5-117">Here is an example of an access token that is issued by the Microsoft identity platform.</span></span>

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

<span data-ttu-id="09fd5-118">Chcete-li volat datové rozhraní API, připojte přístupový token k záhlaví autorizace v požadavku HTTP.</span><span class="sxs-lookup"><span data-stu-id="09fd5-118">To call the data API, you attach the access token as a bearer token to the authorization header in your HTTP request.</span></span> <span data-ttu-id="09fd5-119">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="09fd5-119">Here is an example.</span></span>

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a><span data-ttu-id="09fd5-120">Registrace nové aplikace pomocí portálu Azure</span><span class="sxs-lookup"><span data-stu-id="09fd5-120">Register a new application by using the Azure portal</span></span>

1. <span data-ttu-id="09fd5-121">Přihlaste se na [portál Microsoft Azure](https://portal.azure.com) pomocí pracovního nebo školního účtu nebo osobního účtu Microsoft.</span><span class="sxs-lookup"><span data-stu-id="09fd5-121">Sign in to the [Microsoft Azure portal](https://portal.azure.com) with a work or school account, or a personal Microsoft account.</span></span>

2. <span data-ttu-id="09fd5-122">Pokud váš účet poskytuje přístup k více než jednomu klientovi, vyberte jej v pravém horním rohu a nastavte relaci portálu na požadovaného klienta Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="09fd5-122">If your account gives you access to more than one tenant, select your account in the upper-right corner, and set your portal session to the Azure Active Directory (Azure AD) tenant that you want.</span></span>

3. <span data-ttu-id="09fd5-123">V levém podokně vyberte službu **Azure Active Directory** a poté vyberte možnost **registrace aplikace \> Nová registrace.**</span><span class="sxs-lookup"><span data-stu-id="09fd5-123">In the left pane, select the **Azure Active Directory** service, and then select **App registrations \> New registration**.</span></span>

4. <span data-ttu-id="09fd5-124">Jakmile se zobrazí stránka **Registrovat aplikaci**, zadejte informace o registraci aplikace:</span><span class="sxs-lookup"><span data-stu-id="09fd5-124">When the **Register an application** page appears, enter your application's registration information:</span></span>

    - <span data-ttu-id="09fd5-125">**Název**: zadejte smysluplný název aplikace, který bude zobrazen uživatelům aplikace.</span><span class="sxs-lookup"><span data-stu-id="09fd5-125">**Name**: Enter a meaningful application name that will be shown to users of the app.</span></span>
    - <span data-ttu-id="09fd5-126">**Podporované typy účtů**: Vyberte typy účtů, které by vaše aplikace měla podporovat.</span><span class="sxs-lookup"><span data-stu-id="09fd5-126">**Supported account types**: Select the types of accounts that your app should support.</span></span>

        | <span data-ttu-id="09fd5-127">Typy podporovaných účtů</span><span class="sxs-lookup"><span data-stu-id="09fd5-127">Supported account types</span></span> | <span data-ttu-id="09fd5-128">Popis</span><span class="sxs-lookup"><span data-stu-id="09fd5-128">Description</span></span> |
        |-------------------------|-------------|
        | <span data-ttu-id="09fd5-129">Účty pouze v tomto organizačním adresáři</span><span class="sxs-lookup"><span data-stu-id="09fd5-129">Accounts in this organizational directory only</span></span> | <span data-ttu-id="09fd5-130">Tuto možnost vyberte, pokud vytváříte obchodní aplikaci.</span><span class="sxs-lookup"><span data-stu-id="09fd5-130">Select this option if you're building a line-of-business app.</span></span> <span data-ttu-id="09fd5-131">Tato možnost není k dispozici, dokud neprovedete registraci aplikace v adresáři.</span><span class="sxs-lookup"><span data-stu-id="09fd5-131">This option isn't available unless you're registering the app in a directory.</span></span><p><span data-ttu-id="09fd5-132">Tato možnost je mapována na pouze jednoduchého klienta **Azure AD**.</span><span class="sxs-lookup"><span data-stu-id="09fd5-132">This option is mapped to **Azure AD only single-tenant**.</span></span></p><p><span data-ttu-id="09fd5-133">Tato možnost je výchozí, pokud neprovádíte registraci aplikace mimo adresář.</span><span class="sxs-lookup"><span data-stu-id="09fd5-133">This option is the default option unless you're registering the app outside a directory.</span></span> <span data-ttu-id="09fd5-134">V takovém případě je **Azure AD výchozí volbou více klientů a osobních účtů Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="09fd5-134">In that case, the default option is **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p> |
        | <span data-ttu-id="09fd5-135">Účty v libovolném organizačním adresáři</span><span class="sxs-lookup"><span data-stu-id="09fd5-135">Accounts in any organizational directory</span></span> | <span data-ttu-id="09fd5-136">Tuto možnost vyberte, chcete-li zaměřit všechny zákazníky z obchodního a vzdělávacího sektoru.</span><span class="sxs-lookup"><span data-stu-id="09fd5-136">Select this option to target all business and educational customers.</span></span><p><span data-ttu-id="09fd5-137">Tato možnost je mapována pouze na vícenásobného klienta **Azure AD**.</span><span class="sxs-lookup"><span data-stu-id="09fd5-137">This option is mapped to **Azure AD only multi-tenant**.</span></span></p><p><span data-ttu-id="09fd5-138">Pokud jste aplikaci registrovali jako pouze jednoduchého klienta **Azure AD**, můžete použít list **Ověřování** k jeho aktualizaci na pouze vícenásobného klienta **Azure AD a následně zpět na pouze jednoduchého klienta** **Azure AD**.</span><span class="sxs-lookup"><span data-stu-id="09fd5-138">If you registered the app as **Azure AD only single-tenant**, you can use the **Authentication** blade to update it to **Azure AD only multi-tenant** and then back to **Azure AD only single-tenant**.</span></span></p> |
        | <span data-ttu-id="09fd5-139">Účty v libovolném organizačním adresáři a osobních účtech Microsoft</span><span class="sxs-lookup"><span data-stu-id="09fd5-139">Accounts in any organizational directory and personal Microsoft accounts</span></span> | <span data-ttu-id="09fd5-140">Tuto možnost vyberte, chcete-li zaměřit nejširší sadu odběratelů.</span><span class="sxs-lookup"><span data-stu-id="09fd5-140">Select this option to target the widest set of customers.</span></span><p><span data-ttu-id="09fd5-141">Tato možnost je namapována na vícenásobného klienta **Azure AD a osobní účty Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="09fd5-141">This option is mapped to **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p><p><span data-ttu-id="09fd5-142">Pokud jste zaregistrovali aplikaci jako vícenásobného klienta **Azure AD a osobní účty Microsoft**, nemůžete změnit toto nastavení v uživatelském rozhraní (UI).</span><span class="sxs-lookup"><span data-stu-id="09fd5-142">If you registered the app as **Azure AD multi-tenant and personal Microsoft accounts**, you can't change this setting in the user interface (UI).</span></span> <span data-ttu-id="09fd5-143">Místo toho je nutné pomocí editoru manifestu aplikace změnit podporované typy účtů.</span><span class="sxs-lookup"><span data-stu-id="09fd5-143">Instead, you must use the application manifest editor to change the supported account types.</span></span></p> |

    - <span data-ttu-id="09fd5-144">**URI přesměrování (volitelný)** – vyberte typ aplikace, kterou vytváříte **: web** nebo **veřejný klient (Mobile & Desktop)**.</span><span class="sxs-lookup"><span data-stu-id="09fd5-144">**Redirect URI (optional)** – Select the type of app that you're building: **Web** or **Public client (mobile & desktop)**.</span></span> <span data-ttu-id="09fd5-145">Poté zadejte identifikátor URI přesměrování aplikace (nebo adresu URL odpovědi).</span><span class="sxs-lookup"><span data-stu-id="09fd5-145">Then enter the redirect URI (or reply URL) for the app.</span></span>

        - <span data-ttu-id="09fd5-146">U webových aplikací je to základní adresa URL aplikace.</span><span class="sxs-lookup"><span data-stu-id="09fd5-146">For web apps, provide the base URL of the app.</span></span> <span data-ttu-id="09fd5-147">Například `http://localhost:31544` může být adresa URL webové aplikace, která je spuštěna v místním počítači.</span><span class="sxs-lookup"><span data-stu-id="09fd5-147">For example, `http://localhost:31544` might be the URL for a web app that runs on your local machine.</span></span> <span data-ttu-id="09fd5-148">Uživatelé se pak pomocí této adresy URL přihlásí do aplikace webového klienta.</span><span class="sxs-lookup"><span data-stu-id="09fd5-148">Users then use this URL to sign in to a web client app.</span></span>
        - <span data-ttu-id="09fd5-149">Pro veřejné klientské aplikace zadejte identifikátor URI, který Azure AD používá k vrácení odpovědí na tokeny.</span><span class="sxs-lookup"><span data-stu-id="09fd5-149">For public client apps, provide the URI that Azure AD uses to return token responses.</span></span> <span data-ttu-id="09fd5-150">Zadejte hodnotu, která je specifická pro vaši aplikaci, například `myapp://auth`.</span><span class="sxs-lookup"><span data-stu-id="09fd5-150">Enter a value that is specific to your app, such as `myapp://auth`.</span></span>

        <span data-ttu-id="09fd5-151">Chcete-li zobrazit konkrétní příklady webových aplikací nebo nativních aplikací, přejděte na [platformu Microsoft Identity (dříve Azure Active Directory pro vývojáře)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span><span class="sxs-lookup"><span data-stu-id="09fd5-151">To see specific examples for web apps or native apps, see the quickstarts in [Microsoft identity platform (formerly Azure Active Directory for developers)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span></span>

5. <span data-ttu-id="09fd5-152">V části **Oprávnění API** vyberte **Přidat oprávnění**.</span><span class="sxs-lookup"><span data-stu-id="09fd5-152">Under **API permissions**, select **Add a permission**.</span></span> <span data-ttu-id="09fd5-153">Pak na kartě **Rozhraní API používaná mojí organizací** vyhledejte **Dynamics 365 Human Resources** a přidejte do aplikace oprávnění **user\_impersonation**.</span><span class="sxs-lookup"><span data-stu-id="09fd5-153">Then, on the **APIs my organization uses** tab, search for **Dynamics 365 Human Resources**, and add the **user\_impersonation** permission to your app.</span></span> <span data-ttu-id="09fd5-154">ID aplikace Human Resources je f9be0c49-aa22-4ec6-911a-c5da515226ff.</span><span class="sxs-lookup"><span data-stu-id="09fd5-154">The Application ID for Human Resources is f9be0c49-aa22-4ec6-911a-c5da515226ff.</span></span> <span data-ttu-id="09fd5-155">Pomocí tohoto ID můžete zajistit, že jste zvolili správnou aplikaci.</span><span class="sxs-lookup"><span data-stu-id="09fd5-155">Use this ID to ensure you have chosen the correct application.</span></span>

6. <span data-ttu-id="09fd5-156">Vyberte **Registrovat**.</span><span class="sxs-lookup"><span data-stu-id="09fd5-156">Select **Register**.</span></span>

   <span data-ttu-id="09fd5-157">[![Registrace nové aplikace na portálu Azure](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="09fd5-157">[![Registering a new app in the Azure portal](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span></span>

<span data-ttu-id="09fd5-158">Azure AD přiřadí vaší aplikaci jedinečné ID aplikace (ID klienta) a přejde na stránku **přehledu** vaší aplikace.</span><span class="sxs-lookup"><span data-stu-id="09fd5-158">Azure AD assigns a unique application ID (client ID) to your app, and takes you to the **Overview** page for your app.</span></span> <span data-ttu-id="09fd5-159">Chcete-li do aplikace přidat více možností, můžete vybrat další možnosti konfigurace, jako jsou například možnosti pro obchodní značky a pro certifikáty a tajné klíče.</span><span class="sxs-lookup"><span data-stu-id="09fd5-159">To add more capabilities to your app, you can select other configuration options, such as options for branding and for certificates and secrets.</span></span>

## <a name="retrieving-an-access-token"></a><span data-ttu-id="09fd5-160">Načítání přístupového tokenu</span><span class="sxs-lookup"><span data-stu-id="09fd5-160">Retrieving an access token</span></span>

<span data-ttu-id="09fd5-161">Informace o tom, jakým způsobem načtete přístupový token pro volání rozhraní API dat aplikace Human Resources, závisí na tom, jaké technologie používáte k vývoji klientských aplikací.</span><span class="sxs-lookup"><span data-stu-id="09fd5-161">The specifics of how you retrieve an access token for calling the Human Resources data API will depend on what technologies you're using to develop your client application.</span></span> <span data-ttu-id="09fd5-162">Můžete například provést [testování pomocí nástroje třetí strany](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (jako je Postman), vývoj aplikace konzoly C# nebo webové služby nebo vytvoření klienta JavaScript/TypeScript.</span><span class="sxs-lookup"><span data-stu-id="09fd5-162">For example, you might be [testing with a third party utility](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (such as Postman), developing a C# console application or web service, or building a javascript/TypeScript client.</span></span>

<span data-ttu-id="09fd5-163">Příklad klientské aplikace C#:</span><span class="sxs-lookup"><span data-stu-id="09fd5-163">Example C# client application:</span></span>
```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;

// requires appropriate NuGet package references in the project
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace TalentODataPoC
{
    class Program
    {
        // prereq: This client app must be registered in Azure Active Directory. The app must be
        // registered as requiring permission to the Dynamics 365 for Talent API (with the Dynamics
        // HCM Workload delegated permission).
        static string clientId = "4fc703ef-672c-4e2c-813f-2f9d29d726db"; // This value should be obtained from AAD and must match your registered app
        static string talentNamespaceUri = "";

        public static async Task CallTalentODataService()
        {
            // authority URI
            UriBuilder uri = new UriBuilder("https://login.microsoftonline.com/common");
            AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

            // request token for the resource we want to access (Human Resources). This will authenticate
            // the user and return an access token containing claims for the authenticated user.
            var authResult = await authenticationContext.AcquireTokenAsync(
                "http://hr.talent.dynamics.com", /*Talent app id or resource URI*/
                clientId, /*registered client app id*/
                new Uri("https://localhost"), /*redirect URI, as registered in your AAD app*/
                new PlatformParameters(PromptBehavior.SelectAccount));

            // create the authorization header, which needs to be passed in the Header of the HTTP Requests to Talent
            string authHeader = authResult.CreateAuthorizationHeader();

            // HINT: paste the JWT into https://jwt.ms to decode and view it
            Console.Write("authHeader: ");
            Console.WriteLine(authHeader);
            Console.WriteLine();

            HttpClient client = new HttpClient();
            client.DefaultRequestHeaders.Add("Authorization", authHeader);

            string s;

            Console.Write("Talent Namespace URI: ");
            Console.WriteLine(talentNamespaceUri);
            Console.WriteLine();

            // call the OData service to get JobType data from Talent
            var resultOdata = await client.GetAsync(talentNamespaceUri + "data/JobTypes");
            s = await resultOdata.Content.ReadAsStringAsync();
            Console.WriteLine(s);
            Console.WriteLine();
        }

        static void Main(string[] args)
        {
            Console.WriteLine();

            // if the user passes in a single parameter, assume it is the namespaceUri for Talent
            if (args.Length == 1)
            {
                talentNamespaceUri = args[0];
            } else if (args.Length == 0)
            {
                Console.WriteLine("Enter Talent URL including namespace.");
                Console.WriteLine("Example: https://aos-rts-sf-21454f9d830-prod-westus2.hr.talent.dynamics.com/namespaces/2328af1a-2d45-4c6a-99e3-12a4c3867dcf/");
                Console.Write("> ");
                talentNamespaceUri = Console.ReadLine();
                if (!talentNamespaceUri.EndsWith("/"))
                {
                    talentNamespaceUri = talentNamespaceUri + "/";
                }
            } else
            {
                Console.WriteLine("Unexpected Arguments");
                System.Environment.Exit(1);
            }

            Task t = Program.CallTalentODataService();
            t.Wait();
        }
    }
}
```

<span data-ttu-id="09fd5-164">Jakmile načtete přístupový token, předáte token v záhlaví autorizace jako token nosiče s každým požadavkem, který odešlete do datového rozhraní API, jak je popsáno výše.</span><span class="sxs-lookup"><span data-stu-id="09fd5-164">Once you've retrieved an access token, you'll pass the token in the Authorization header as a bearer token with each request you send to the data API, as described above.</span></span>
