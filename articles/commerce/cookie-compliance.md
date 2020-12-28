---
title: Shoda souborů cookie
description: V tomto tématu jsou popsány důležité informace týkající se kompatibility souborů cookie a výchozích zásad obsažených v aplikaci Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 08/31/2020
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
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4f54b9b8130a167dbecdb13fccd7039f827f6ed0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410683"
---
# <a name="cookie-compliance"></a>Shoda souborů cookie

[!include [banner](includes/banner.md)]

V tomto tématu jsou popsány důležité informace týkající se kompatibility souborů cookie a výchozích zásad obsažených v aplikaci Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Ochrana osobních údajů je důležitým faktorem při použití všech technologií sledování, které ovlivňují zákazníky elektronického obchodu. Z důvodu norem dodržování ochrany osobních údajů, jako je obecné nařízení o ochraně osobních údajů (GDPR) v Evropské unii (EU), je třeba zvážit elektronické zásady ochrany osobních údajů pro všechny weby, které jsou v současné době aktivní. Vzhledem k tomu, že je většina webů elektronického obchodování ve výchozím nastavení globálně přístupná, je důležité prostudovat standardy kompatibility pro web elektronického obchodování.

Chcete-li získat další informace o základních principech, které společnost Microsoft používá pro vyhovění souborů cookie, navštivte [centrum zabezpečení společnosti Microsoft](https://www.microsoft.com/trust-center). Na tomto webu můžete také získat další informace o oblastech dodržování předpisů a ochrany osobních údajů.

Následující tabulka ukazuje aktuální referenční seznam souborů cookie, které vkládají weby Dynamics 365 Commerce.

| Název souboru cookie                               | Použití                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| .AspNet.Cookies                             | Uložit ověřovací soubory cookie Microsoft Azure Active Directory (Azure AD) pro jednotné přihlašovaní (SSO). Ukládá šifrované základní informace o uživateli (jméno, příjmení, e-mail). |
| &#95;msdyn365___cart&#95;                           | ID nákupního košíku použitého k získání seznamu produktů přidaných do instance košíku. |
| &#95;msdyn365___ucc&#95;                            | Sledování souhlasu se soubory cookies.                          |
| ai_session                                  | Zjistí, kolik relací uživatelské aktivity zahrnovalo určité stránky a funkce aplikace. |
| ai_user                                     | Zjistí, kolik lidí použilo aplikaci a její funkce. Uživatelé se počítají pomocí anonymních ID. |
| b2cru                                       | Dynamicky ukládá adresu URL přesměrování.                              |
| JSESSIONID                                  | Používá platební konektor Adyen k uložení relace uživatele.       |
| OpenIdConnect.nonce.&#42;                       | Ověřování                                               |
| x-ms-cpim-cache:.&#42;                          | Používá se pro udržování stavu žádosti.                      |
| x-ms-cpim-csrf                              | Token CRSF používaný k ochraně před CRSF.     |
| x-ms-cpim-dc                                | Používá se k směrování požadavků do příslušné instance serveru pro ověřování produkce. |
| x-ms-cpim-rc.&#42;                              | Používá se k směrování požadavků do příslušné instance serveru pro ověřování produkce. |
| x-ms-cpim-slice                             | Používá se k směrování požadavků do příslušné instance serveru pro ověřování produkce. |
| x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0 | Používá se k udržování relace SSO.                        |
| x-ms-cpim-trans                             | Používá se pro sledování transakcí (počet otevřených karet, které se autentizují proti webu typu B2C), včetně aktuální transakce. |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a>Souhlas uživatele webu se soubory cookie na webu elektronického obchodu 

Pokud funkce nebo modul webu elektronického obchodu používá nepodstatný soubor cookie, je nutné před sledováním souboru cookie získat souhlas uživatele webu. Aby uživatelé webu mohli poskytovat souhlas se soubory cookie na webu elektronického obchodu, musí autor webu přidat a nakonfigurovat modul souhlasu se soubory cookie v modulu záhlaví stránky, aby bylo zajištěno zobrazení a přijetí souhlasu. Před vykreslením funkce nebo modulu používajícího nepodstatný soubor cookie na stránce webu musí být udělen souhlas uživatele webu.

## <a name="additional-resources"></a>Další prostředky

[Funkce a možnosti usnadnění přístupu](accessibility.md)

[Přehled dodržování předpisů](compliance-overview.md)

[Přidání stránky se zásadami ochrany osobních údajů](add-privacy-page.md)

[Nahrazení ID uživatelů přidružených ke změnám sledovaných obsahů](replace-IDs-tracked-changes.md)

[Modul souhlasu se soubory cookie](cookie-consent-module.md) 
 
[Modul záhlaví](author-header-module.md)
