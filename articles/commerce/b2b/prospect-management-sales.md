---
title: Správa uživatelů obchodních partnerů na webech B2B elektronického obchodování pomocí aplikace Dynamics 365 Sales
description: Toto téma popisuje, jak používat Microsoft Dynamics 365 Sales ke správě schválení obchodních partnerů na webech elektronického obchodování Dynamics 365 Commerce typu business-to-business (B2B).
author: shajain
ms.date: 2/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: c6ac5409de5101c91b9348de800e3eaea9895c23
ms.sourcegitcommit: 4d52c67f52ad0add63cd905df61367b344389069
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/16/2022
ms.locfileid: "8312573"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites-using-dynamics-365-sales"></a>Správa uživatelů obchodních partnerů na webech B2B elektronického obchodování pomocí aplikace Dynamics 365 Sales

[!include [banner](../../includes/banner.md)]

Toto téma popisuje, jak používat Microsoft Dynamics 365 Sales ke správě schválení obchodních partnerů na webech elektronického obchodování Dynamics 365 Commerce typu business-to-business (B2B). Organizace, které již investovaly do řešení Dynamics 365 Sales, mohou využít jeho koncepty potenciálních zákazníků a příležitostí pro proces schvalování obchodních partnerů B2B elektronického obchodování.

Základní informace o procesu schvalování obchodních partnerů B2B najdete v tématu [Správa uživatelů obchodních partnerů na webech elektronického obchodu B2B](manage-b2b-users.md).

Potenciální obchodní partneři mohou zahájit proces onboardingu na web B2B elektronického obchodování zasláním žádosti o onboarding prostřednictvím odkazu na webu B2B. Po odeslání požadavku a spuštění příslušných úloh (např. **P-0001** a **Synchronizovat objednávky a požadavky kanálu**) v centrále Commerce je žádost o onboarding uložena na stránce **Všichni potenciální partneři** v centrále Commerce. Proces schvalování potenciálních obchodních partnerů pak lze dokončit v aplikaci Sales.

Poté, co je povolena integrace mezi Sales a Commerce, vytvoření potenciálního obchodního partnera v Commerce způsobí vytvoření *potencionálního zákazníka* v Sales.

Následující obrázek ukazuje příklad stránky vytvoření potenciálního zákazníka pro potenciálního obchodního partnera v Sales.

![Stránka vytvoření potenciálního zákazníka v Dynamics 365 Sales.](../media/LeadInSales.png)

Na obrázku je v oddílu **Kontakt** zobrazena osoba, která odeslala žádost o onboarding, a sekce **Společnost** ukazuje organizaci. Poznámka v sekci **Časová osa** ukazuje, že potenciální zákazník byl vytvořen infrastrukturou duálního zápisu. Protože byl vytvořen infrastrukturou s duálním zápisem, tento potenciální zákazník se neobjeví v rozbalovacím seznamu **Moji otevření potencionální zákazníci**. Místo toho se zobrazí v novém zobrazení s názvem **Všichni obchodní potencionální zákazníci B2B**.

Podle standardního procesu kvalifikace potenciálního zákazníka v Sales jsou vytvořeny záznamy *příležitosti*, záznam *kontaktu* a záznam *účtu*, když je uživatel kvalifikován jako potenciální zákazník. Infrastruktura duálního zápisu se používá k zápisu kontaktů a záznamů o účtu do Commerce. Kontakt je vytvořen jako zákazník typu *osoba* a společnost je vytvořena jako zákazník typu *organizace*. Pokud uživatel vybere pro tuto příležitost možnost **Uzavřít jako Získáno**, je potenciální partner v Commerce schválen. Schválení potenciálního partnera způsobí vytvoření zákaznické hierarchie.

Všechny zbývající obchodní procesy probíhají v Commerce. Tyto procesy zahrnují zaslání e-mailu obchodnímu partnerovi, definování správy úvěrového limitu pro uživatele a přidání dalších uživatelů na web B2B. Pokud však uživatel diskvalifikuje potenciálního zákazníka nebo označí příležitost jako ztracenou, potenciální partner v Commerce je označen jako odmítnutý a žadateli je zaslán e-mail s odmítnutím onboardingu.

## <a name="enable-integration-between-sales-and-commerce"></a>Povolení integrace mezi Sales a Commerce

Integrace mezi Sales a Commerce závisí na infrastruktuře duálního zápisu. Proto by měl být duální zápis povolen a funkční, aby zákazníci, kteří jsou vytvořeni v jednom systému, byli zapsáni do druhého systému. Další informace o infrastruktuře duálního zápisu najdete v tématu [Přehled duálního zápisu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview).

Po dokončení nastavení duálního zápisu může implementační partner přejít na [Microsoft AppSource](https://appsource.microsoft.com/) a vyhledat řešení, které je pojmenováno [Řešení duálního zápisu Commerce](https://partner.microsoft.com/dashboard/commercial-marketplace/offers/7ca1d8c9-dc79-4cb7-a82e-8dc96a25acca/overview). Nainstalujte balíček pomocí standardního průvodce instalací a poté jej otestujte vytvořením potenciálního partnera na webu B2B. Po vytvoření potenciálního partnera ověřte, zda je požadavek zobrazen v části **Všichni potenciální partneři** v Commerce, a poté ověřte, že se potenciální partner zobrazuje jako potenciální zákazník v Sales.

## <a name="additional-resources"></a>Další prostředky

[Správa uživatelů obchodních partnerů na webech elektronického obchodu B2B](manage-b2b-users.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
