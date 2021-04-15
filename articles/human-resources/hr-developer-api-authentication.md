---
title: Ověřování
description: Tento článek obsahuje přehled informací o ověřování pomocí rozhraní API (Microsoft Dynamics 365 Human Resources data Application Programming Interface).
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3dffe1db98ba39fde2229e69bc70bdbf113ff6ad
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793674"
---
# <a name="authentication"></a>Ověřování

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek obsahuje přehled informací o ověřování pomocí rozhraní API (Microsoft Dynamics 365 Human Resources data Application Programming Interface).

## <a name="overview"></a>Přehled

Datové rozhraní API pro Human Resources je implementací OData. Další informace naleznete v tématu[Protokol Open Data (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).

Vaše aplikace musí být ověřena jako autorizovaný volající před tím, než rozhraní API bude obsluhovat žádosti z vaší aplikace.

## <a name="fundamentals"></a>Základy

Chcete-li volat datové rozhraní API, aplikace musí získat přístupový token z platformy Microsoft Identity. Přístupový token obsahuje informace o vaší přihlášce a oprávnění, které musí volat zdroje v aplikaci Human Resources.

### <a name="access-token"></a>Token přístupu

Přístupové tokeny vydané platformou Microsoft Identity jsou webové tokeny JavaScript Object Notation (JSON) (JWT) využívající šifrování base64. Obsahují informace (nároky), které rozhraní API dat (a jiná webová rozhraní zabezpečená platformou Microsoft Identity) používají k ověření volajícího a ověření, zda má volající správná oprávnění k provádění požadované operace. Během volání můžete považovat přístupové tokeny za neprůhledné. Měli byste vždy přenášet přístupové tokeny prostřednictvím zabezpečeného kanálu, jako je například protokol TLS (Transport Layer Security) a protokol HTTP (Hypertext Transfer Protocol Secure).

Zde je příklad přístupového tokenu vydaného platformou Microsoft Identity.

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

Chcete-li volat datové rozhraní API, připojte přístupový token k záhlaví autorizace v požadavku HTTP. Následuje příklad.

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a>Registrace nové aplikace pomocí portálu Azure

1. Přihlaste se na [portál Microsoft Azure](https://portal.azure.com) pomocí pracovního nebo školního účtu nebo osobního účtu Microsoft.

2. Pokud váš účet poskytuje přístup k více než jednomu klientovi, vyberte jej v pravém horním rohu a nastavte relaci portálu na požadovaného klienta Azure Active Directory (Azure AD).

3. V levém podokně vyberte službu **Azure Active Directory** a poté vyberte možnost **registrace aplikace \> Nová registrace.**

4. Jakmile se zobrazí stránka **Registrovat aplikaci**, zadejte informace o registraci aplikace:

    - **Název**: zadejte smysluplný název aplikace, který bude zobrazen uživatelům aplikace.
    - **Podporované typy účtů**: Vyberte typy účtů, které by vaše aplikace měla podporovat.

        | Typy podporovaných účtů | Popis |
        |-------------------------|-------------|
        | Účty pouze v tomto organizačním adresáři | Tuto možnost vyberte, pokud vytváříte obchodní aplikaci. Tato možnost není k dispozici, dokud neprovedete registraci aplikace v adresáři.<p>Tato možnost je mapována na pouze jednoduchého klienta **Azure AD**.</p><p>Tato možnost je výchozí, pokud neprovádíte registraci aplikace mimo adresář. V takovém případě je **Azure AD výchozí volbou více klientů a osobních účtů Microsoft**.</p> |
        | Účty v libovolném organizačním adresáři | Tuto možnost vyberte, chcete-li zaměřit všechny zákazníky z obchodního a vzdělávacího sektoru.<p>Tato možnost je mapována pouze na vícenásobného klienta **Azure AD**.</p><p>Pokud jste aplikaci registrovali jako pouze jednoduchého klienta **Azure AD**, můžete použít list **Ověřování** k jeho aktualizaci na pouze vícenásobného klienta **Azure AD a následně zpět na pouze jednoduchého klienta** **Azure AD**.</p> |
        | Účty v libovolném organizačním adresáři a osobních účtech Microsoft | Tuto možnost vyberte, chcete-li zaměřit nejširší sadu odběratelů.<p>Tato možnost je namapována na vícenásobného klienta **Azure AD a osobní účty Microsoft**.</p><p>Pokud jste zaregistrovali aplikaci jako vícenásobného klienta **Azure AD a osobní účty Microsoft**, nemůžete změnit toto nastavení v uživatelském rozhraní (UI). Místo toho je nutné pomocí editoru manifestu aplikace změnit podporované typy účtů.</p> |

    - **URI přesměrování (volitelný)** – vyberte typ aplikace, kterou vytváříte **: web** nebo **veřejný klient (Mobile & Desktop)**. Poté zadejte identifikátor URI přesměrování aplikace (nebo adresu URL odpovědi).

        - U webových aplikací je to základní adresa URL aplikace. Například `http://localhost:31544` může být adresa URL webové aplikace, která je spuštěna v místním počítači. Uživatelé se pak pomocí této adresy URL přihlásí do aplikace webového klienta.
        - Pro veřejné klientské aplikace zadejte identifikátor URI, který Azure AD používá k vrácení odpovědí na tokeny. Zadejte hodnotu, která je specifická pro vaši aplikaci, například `myapp://auth`.

        Chcete-li zobrazit konkrétní příklady webových aplikací nebo nativních aplikací, přejděte na [platformu Microsoft Identity (dříve Azure Active Directory pro vývojáře)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).

5. V části **Oprávnění API** vyberte **Přidat oprávnění**. Pak na kartě **Rozhraní API používaná mojí organizací** vyhledejte **Dynamics 365 Human Resources** a přidejte do aplikace oprávnění **user\_impersonation**. ID aplikace Human Resources je f9be0c49-aa22-4ec6-911a-c5da515226ff. Pomocí tohoto ID můžete zajistit, že jste zvolili správnou aplikaci.

6. Vyberte **Registrovat**.

   [![Registrace nové aplikace na portálu Azure](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)

Azure AD přiřadí vaší aplikaci jedinečné ID aplikace (ID klienta) a přejde na stránku **přehledu** vaší aplikace. Chcete-li do aplikace přidat více možností, můžete vybrat další možnosti konfigurace, jako jsou například možnosti pro obchodní značky a pro certifikáty a tajné klíče.

## <a name="retrieving-an-access-token"></a>Načítání přístupového tokenu

Informace o tom, jakým způsobem načtete přístupový token pro volání rozhraní API dat aplikace Human Resources, závisí na tom, jaké technologie používáte k vývoji klientských aplikací. Můžete například provést [testování pomocí nástroje třetí strany](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (jako je Postman), vývoj aplikace konzoly C# nebo webové služby nebo vytvoření klienta JavaScript/TypeScript.

Příklad klientské aplikace C#:
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

Jakmile načtete přístupový token, předáte token v záhlaví autorizace jako token nosiče s každým požadavkem, který odešlete do datového rozhraní API, jak je popsáno výše.


[!INCLUDE[footer-include](../includes/footer-banner.md)]