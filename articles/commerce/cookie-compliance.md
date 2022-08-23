---
title: Zásady zacházení se soubory cookie
description: V tomto článku jsou popsány důležité informace týkající se kompatibility souborů cookie a výchozích zásad obsažených v aplikaci Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 03/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 20bdc6466c5d89709f8ba790eb567bd7d8bbb15c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273605"
---
# <a name="cookie-compliance"></a>Zásady zacházení se soubory cookie

[!include [banner](includes/banner.md)]

V tomto článku jsou popsány důležité informace týkající se kompatibility souborů cookie a výchozích zásad obsažených v aplikaci Microsoft Dynamics 365 Commerce.

Ochrana osobních údajů je důležitým faktorem při použití všech technologií sledování, které ovlivňují zákazníky elektronického obchodu. Z důvodu norem dodržování ochrany osobních údajů, jako je obecné nařízení o ochraně osobních údajů (GDPR) v Evropské unii (EU), je třeba zvážit elektronické zásady ochrany osobních údajů pro všechny weby, které jsou v současné době aktivní. Vzhledem k tomu, že je většina webů elektronického obchodování ve výchozím nastavení globálně přístupná, je důležité prostudovat standardy kompatibility pro web elektronického obchodování.

Chcete-li získat další informace o základních principech, které společnost Microsoft používá pro vyhovění souborů cookie, navštivte [centrum zabezpečení společnosti Microsoft](https://www.microsoft.com/trust-center). Na tomto webu můžete také získat další informace o oblastech dodržování předpisů a ochrany osobních údajů.

Následující tabulka ukazuje aktuální referenční seznam souborů cookie, které vkládají weby Dynamics 365 Commerce.

| Název souboru cookie                               | Použití                                                        | Životnost |
| ------------------------------------------- | ------------------------------------------------------------ |  ------- |
| .AspNet.Cookies                             | Uložit ověřovací soubory cookie Microsoft Azure Active Directory (Azure AD) pro jednotné přihlašovaní (SSO). Ukládá šifrované základní informace o uživateli (jméno, příjmení, e-mail). | Relace |
| \_msdyn365___cart_                           | ID nákupního košíku použitého k získání seznamu produktů přidaných do instance košíku. | Relace |
| \_msdyn365___checkout_cart_                           | ID nákupního košíku použitého k získání seznamu produktů přidaných do instance nákupního košíku. | Relace |
| \_msdyn365___ucc_                            | Sledování souhlasu se soubory cookies.                          | 1 rok |
| ai_session                                  | Zjistí, kolik relací uživatelské aktivity zahrnovalo určité stránky a funkce aplikace. | 30 min |
| ai_user                                     | Zjistí, kolik lidí použilo aplikaci a její funkce. Uživatelé se počítají pomocí anonymních ID. | 1 rok |
| b2cru                                       | Dynamicky ukládá adresu URL přesměrování.                              | Relace |
| JSESSIONID                                  | Používá platební konektor Adyen k uložení relace uživatele.       | Relace |
| OpenIdConnect.nonce.&#42;                       | Ověřování                                               | 11 minut |
| x-ms-cpim-cache:.&#42;                          | Používá se pro udržování stavu žádosti.                      | Relace |
| x-ms-cpim-csrf                              | Token CRSF používaný k ochraně před CRSF.     | Relace |
| x-ms-cpim-dc                                | Používá se k směrování požadavků do příslušné instance serveru pro ověřování produkce. | Relace |
| x-ms-cpim-rc.&#42;                              | Používá se k směrování požadavků do příslušné instance serveru pro ověřování produkce. | Relace |
| x-ms-cpim-slice                             | Používá se k směrování požadavků do příslušné instance serveru pro ověřování produkce. | Relace |
| x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0 | Používá se k udržování relace SSO.                        | Relace |
| x-ms-cpim-trans                             | Používá se pro sledování transakcí (počet otevřených karet, které se autentizují proti webu typu B2C), včetně aktuální transakce. | Relace |
| \_msdyn365___muid_                            | Používá se, pokud je pro prostředí aktivováno experimentování; využíváno jako ID uživatele pro experimentální účely. | 1 rok |
| \_msdyn365___exp_                             | Používá se, pokud je pro prostředí aktivováno experimentování; slouží k měření vyvažování zatížení výkonu.         | 1 hodina |
| d365mkt                                       | Používá se, pokud je v nástroji pro tvorbu webu Commerce povolena detekce založená na poloze ke sledování adresy IP uživatele pro návrhy umístění obchodu **Nastavení webu \> Obecné \> Povolit zjišťování obchodů na základě polohy**.      | 1 hodina |
| \_msdyn365___tuid_                           | Používá se pouze v případě, že je pro prostředí aktivováno experimentování; generuje GUID, který má sloužit jako identifikátor uživatele. Hodnota se změní, pokud se změní stav přihlášení uživatele.      | 1 rok |
| \_msdyn365___aud_0                          | Ukládá hodnoty segmentů používané cílením a používá se pouze v případě, že je cílení nakonfigurováno na stránce nebo fragmentu požadovaném uživatelem webu. Soubor cookie je umístěn, pouze pokud hodnoty segmentu pocházejí od poskytovatele segmentace třetí strany.      | 7 dnů |
| \_msdyn365___aud_1                           | Ukládá hodnoty segmentů používané cílením a používá se pouze v případě, že je cílení nakonfigurováno na stránce nebo fragmentu požadovaném uživatelem webu. Soubor cookie je umístěn, pouze pokud hodnoty segmentu pocházejí od poskytovatele segmentace třetí strany.      | 7 dnů |
| \_msdyn365___aud_2                           | Ukládá hodnoty segmentů používané cílením a používá se pouze v případě, že je cílení nakonfigurováno na stránce nebo fragmentu požadovaném uživatelem webu. Soubor cookie je umístěn, pouze pokud hodnoty segmentu pocházejí od poskytovatele segmentace třetí strany.      | 7 dnů |
| d365gi                                       | Tento soubor cookie ukládá údaje o zeměpisné poloze při použití geolokační služby třetí strany.      | 1 den |

Pokud uživatel webu vybere nějaké odkazy na sociální média v rámci webu, soubory cookie v následující tabulce budou sledovány také v jeho prohlížeči.


| Doména                      | Cookie               | popis                                                  | Zdroj                                          |
| --------------------------- | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| .linkedin.com                | UserMatchHistory         | Synchronizace ID reklam LinkedIn                                      | Značka LinkedIn Feed a Insight                                |
| .linkedin.com               | li_sugr                  | Identifikátor prohlížeče                                           | Značka LinkedIn Insight Tag, pokud adresa IP není v určené zemi |
| .linkedin.com               | BizographicsOptOut       | Určuje stav odhlášení ze sledování třetích stran.              | Ovládací prvky pro hosty LinkedIn a oborová odhlášení           |
| .linkedin.com               | \_guid                    | Identifikátor prohlížeče pro Google Ads.                            | Kanál LinkedIn                                                |
| .linkedin.com               | li_oatml                 | Nepřímý identifikátor člena pro sledování, retargeting a analýzu konverzí. | Značka LinkedIn Ads a Insight                                |
| Různé domény první strany | li_fat_id                | Nepřímý identifikátor člena pro sledování, retargeting a analýzu konverzí. | Značka LinkedIn Ads a Insight                                |
| .adsymptotic.com            | U                        | Identifikátor prohlížeče                                           | Značka LinkedIn Insight Tag, pokud adresa IP není v určené zemi |
| .linkedin.com                | bcookie                  | Soubor cookie s ID prohlížeče                                            | Žádosti na LinkedIn                                         |
| .linkedin.com                | bscookie                 | Zabezpečený soubor cookie prohlížeče                                        | Žádosti na LinkedIn                                         |
| .linkedin.com               | lang                     | Nastaví výchozí národní prostředí a jazyk.                                 | Žádosti na LinkedIn                                         |
| .linkedin.com                | lidc                     | Používá se pro směrování.                                             | Žádosti na LinkedIn                                         |
| .linkedin.com               | aam_uuid                 | Správce souborů cookie Adobe Audience Manager                                                     | Nastaveno pro synchronizaci ID                                              |
| .linkedin.com               | \_ga                      | Soubor cookie Google Analytics                                            | Google Analytics                                             |
| .linkedin.com               | \_gat                     | Soubor cookie Google Analytics                                             | Google Analytics                                             |
| .linkedin.com               | liap                     | Soubor cookie Google Analytics                                             | Google Analytics                                             |
| .linkedin.com               | lissc                    |                                                              |                                                              |
| .facebook.com               | c_user                   | Cookie obsahuje ID uživatele aktuálně přihlášeného uživatele.  |   Facebook                                                           |
| .facebook.com               | datr                     | Slouží k identifikaci webového prohlížeče, který se používá k připojení k Facebooku nezávisle na přihlášeném uživateli. | Facebook                                                             |
| .facebook.com               | wd                       | Ukládá rozměry okna prohlížeče a používá ho Facebook k optimalizaci vykreslení stránky. | Facebook                                                             |
| .facebook.com               | xs                       | Dvouciferné číslo představující číslo relace. Druhá část hodnoty je tajný klíč relace. |  Facebook                                                            |
| .facebook.com               | fr                       | Obsahuje jedinečné ID prohlížeče a uživatele, které se používají pro cílenou reklamu. |  Facebook                                                            |
| .facebook.com               | sb                       | Používá se ke zlepšení návrhů přátel Facebook.                                |  Facebook                                                            |
| .facebook.com               | spin                     |                                                              |  Facebook                                                            |
| .twitter.com                | guest_id                 |                                                              |  Twitter                                                            |
| .twitter.com                | kdt                      |                                                              |  Twitter                                                             |
| .twitter.com                | personalization_id       | Cookie obsahuje ID uživatele aktuálně přihlášeného uživatele.  |  Twitter                                                             |
| .twitter.com                | remember_checked_on      |                                                              | Twitter                                                              |
| .twitter.com                | twid                     |                                                              |  Twitter                                                             |
| .pinterest.com              | \_auth                    | Cookie obsahuje ID uživatele aktuálně přihlášeného uživatele.  |   Pinterest                                                           |
| .pinterest.com              | \_b                       |                                                              |   Pinterest                                                           |
| .pinterest.com              | \_pinterest_pfob          |                                                              |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_referrer      | Cookie obsahuje stránky, když uživatel vybere tlačítko Pinterest.      |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_sess          | Cookie obsahuje stránky, když uživatel vybere tlačítko Pinterest.      |  Pinterest                                                            |
| .pinterest.com              | \_routing_id              |                                                              |  Pinterest                                                            |
| .pinterest.com              | bei                      |                                                              |  Pinterest                                                            |
| .pinterest.com              | cm_sub                   | Obsahuje ID uživatele a časové razítko, když byl soubor cookie vytvořen. |  Pinterest                                                            |
| .pinterest.com              | csrftoken                | Cookie obsahuje stránky, když uživatel vybere tlačítko Pinterest.      | Pinterest                                                             |
| .pinterest.com              | sessionFunnelEventLogged | Cookie obsahuje stránky, když uživatel vybere tlačítko Pinterest.      | Pinterest                                                             |
| .pinterest.com              | Místní úložiště            |                                                              |  Pinterest                                                            |
| .pinterest.com              | Servisní pracovníci          |                                                              |  Pinterest                                                            |


## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a>Souhlas uživatele webu se soubory cookie na webu elektronického obchodu 

Pokud funkce nebo modul webu elektronického obchodu používá nepodstatný soubor cookie, je nutné před sledováním souboru cookie získat souhlas uživatele webu. Aby uživatelé webu mohli poskytovat souhlas se soubory cookie na webu elektronického obchodu, musí autor webu přidat a nakonfigurovat modul souhlasu se soubory cookie v modulu záhlaví stránky, aby bylo zajištěno zobrazení a přijetí souhlasu. Před vykreslením funkce nebo modulu používajícího nepodstatný soubor cookie na stránce webu musí být udělen souhlas uživatele webu.

## <a name="additional-resources"></a>Další prostředky

[Funkce a možnosti usnadnění přístupu](accessibility.md)

[Přehled dodržování předpisů](compliance-overview.md)

[Přidání stránky se zásadami ochrany osobních údajů](add-privacy-page.md)

[Nahrazení ID uživatelů přidružených ke změnám sledovaných obsahů](replace-IDs-tracked-changes.md)

[Modul souhlasu se soubory cookie](cookie-consent-module.md) 
 
[Modul záhlaví](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
