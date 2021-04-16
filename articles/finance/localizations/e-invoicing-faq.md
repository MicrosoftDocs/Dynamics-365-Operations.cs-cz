---
title: Elektronická fakturace – Často kladené otázky
description: Toto téma poskytuje informace o často kladených otázkách týkajících se Elektronické fakturace.
author: gionoder
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 41cddcdad5043ec314a94dda67f4f2e9de406cac
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840165"
---
# <a name="electronic-invoicing-faq"></a>Elektronická fakturace – Často kladené otázky

[!include [banner](../includes/banner.md)]

Toto téma poskytuje odpovědi na často kladené otázky týkající se Elektronické fakturace. Elektronická fakturace rozšiřuje možnosti elektronické fakturace, které existují v aplikacích Dynamics 365 Finance, Dynamics 365 Supply Chain Management a Dynamics 365 Project Operations. 

## <a name="what-is-important-about-electronic-invoicing-and-why-should-it-matter-to-my-organization"></a>Co je důležité na elektronické fakturaci a proč by se o ni má organizace měla zajímat?

Jak se organizace globálně rozrůstají a rozšiřují své stopy napříč regiony, provozní složitost a rizika se stále prohlubují. Udržování souladu s předpisy a přizpůsobování se často se měnícím zákonům je stále větší výzvou a je zvláště důležité, pokud jde o fakturaci. Fakturace byla tradičně drahá a náchylná k chybám, protože společnosti spoléhají na papírové dokumenty a ruční náročné procesy.  

Organizace se začaly odklánět od papírových faktur, aby snížily náklady a urychlily celkový proces. Vlády se stále více obracejí k elektronické fakturaci jako klíčové součásti digitalizace daní. Vlády mohou minimalizovat daňové úniky a manipulaci a omezovat podvody důsledným trváním na tom, aby organizace digitálně předkládaly daňové informace daňovým úřadům v reálném čase. 

Svět se přesouvá ke zpracování bezpapírových dokumentů a bez zavedení elektronické fakturace mohou zákazníci riskovat problémy s dodržováním předpisů, zbytečné náklady a zaostávat za konkurencí. 

## <a name="doesnt-finance-supply-chain-management-and-project-operations-already-include-electronic-invoicing-functionality-what-value-does-this-provide-to-me-as-a-customer"></a>Nezahrnují aplikace Finance, Supply Chain Management a Project Operations již funkci elektronické fakturace? Jakou hodnotu to pro mě jako zákazníka poskytuje? 

Elektronická fakturace rozšiřuje možnosti elektronické fakturace, které existují v aplikacích Finance, Supply Chain Management a Project Operations. Funkce také zjednodušuje dodržování nejnovějších standardů elektronické fakturace a poskytuje koherentní prostředí při zpracování a výměně elektronických faktur pro různé geografické oblasti. Možnosti elektronické fakturace odemknou řadu výhod, včetně: 

   - Rychlejšího a snadnějšího přijetí požadavků konkrétních zemí / regionů.
   - Standardizace implementací řešení elektronické fakturace. 
   - Vylepšené sledovatelnosti zpracování elektronických faktur.  
   - Snadnější údržby v souladu s měnícími se právními požadavky a místními podnikovými postupy. 
   - Zjednodušeného balení řešení.
   - Možností škálování u velkého objemu odeslaných dokumentů, což má za následek rychlejší zpracování.
   - Možnosti sdílet vaše řešení s jinými společnostmi.

## <a name="does-electronic-invoicing-support-the-on-premises-installations-of-finance-supply-chain-management-and-project-operations"></a>Podporuje elektronická fakturace místní instalace aplikací Finance, Supply Chain Management a Project Operations? 

Aktuální platforma neumožňuje použití místní verze a neexistují žádné plány na její podporu v budoucnu.

## <a name="does-electronic-invoicing-interface-with-the-vendor-import-automation-feature"></a>Má elektronická fakturace rozhraní s funkcí automatizace importu od dodavatele?

Ne. Existují plány doplnit toto rozhraní, ale není určen žádný termín implementace. Po naplánování budou datumy oznámeny v [Plánech vydání](https://docs.microsoft.com/dynamics365/release-plans/).

## <a name="how-does-electronic-invoicing-handle-file-attachments-into-the-electronic-invoice-is-a-sharepoint-server-needed-when-embedding-pdf-files-into-the-xml-file"></a>Jak elektronická fakturace zpracovává souborové přílohy k elektronické faktuře? Je při vkládání souborů PDF do souboru XML potřeba server SharePoint?

Se soubory připojenými k elektronické faktuře se zachází jako s vloženými binárními daty v prvku XML. Server SharePoint není pro vložení souborů PDF potřebný, ale příloha musí být uložena v systému pro správu dokumentů Finance, Supply Chain Management a Project Operations.

## <a name="is-electronic-invoicing-available-according-to-the-regulations-of-my-countryregion"></a>Je elektronická fakturace k dispozici podle předpisů mé země / regionu?

Elektronická fakturace je platforma mikroslužeb, která bude globálně dostupná.

Společnost Microsoft plánuje zveřejnit formáty a integrace elektronických faktur pro země, které jsou funkčně lokalizovány společností Microsoft. Další informace najdete v tématu [Dostupnost funkcí elektronické fakturace](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features).

Pokud formát elektronické fakturace pro vaši zemi / region není uveden, je plánováno, že platforma v budoucnosti tento scénář podpoří. I nadále můžete využívat výhod možností konfigurace, které Elektronická fakturace má, a konfigurovat formát elektronické fakturace sami, nebo můžete spolupracovat s partnerem / nezávislým prodejcem softwaru a nakonfigurovat je pro vaši organizaci.

## <a name="is-dynamics-365-for-regulatory-services-a-new-module-like-human-resources-or-project-operations-that-is-linked-to-finance-or-supply-chain-management-are-there-extra-costs-for-that"></a>Je Dynamics 365 for Regulatory Services novým modulem, podobně jako Human Resources nebo Project Operations, který je propojen s Finance nebo Supply Chain Management? Připlácí se něco?

Dynamics 365 for Regulatory Services (RCS) je cloudová služba pro konfiguraci prostředků globalizace. RCS je zdarma pro všechny držitele licencí Finance, Supply Chain Management a Project Operations.

Chcete-li si zaregistrovat službu RCS, přejděte na stránku <https://marketing.configure.global.dynamics.com/>.

Pro více informací viz [Regulatory Configuration Services (RCS) - funkce globalizace](rcs-globalization-feature.md).

## <a name="do-i-need-to-sign-up-to-get-electronic-invoicing--or-just-turn-it-on-in-feature-management"></a>Musím se zaregistrovat, abych získal Elektronickou fakturaci, nebo ji prostě zapnu ve správě funkcí?

Pokud máte licenci pro aplikace Finance, Supply Chain Management a Project Operations, přečtěte si téma [Začněte se správou služby doplňku elektronické fakturace](e-invoicing-get-started-service-administration.md) a zaregistrujte si elektronickou fakturaci.

## <a name="does-electronic-invoicing-work-with-tier-1-virtual-machines-what-is-the-minimal-required-environment"></a>Funguje elektronická fakturace s virtuálními počítači úrovně 1? Jaké je minimální požadované prostředí?

Integrace s Elektronickou fakturací vyžaduje k hostování aplikací Finance nebo Supply Chain Management virtuální stroj alespoň úrovně 2. Další informace o plánování prostředí naleznete v části [Plánování prostředí](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

## <a name="does-electronic-invoicing-have-a-test-mode-for-testing-invoice-submission"></a>Má Elektronická fakturace testovací režim pro testování odeslání faktury?

Toho lze dosáhnout konfigurací. Chcete-li otestovat odeslání faktury, můžete se připojit k Finance nebo Supply Chain Management z prostředí akceptačního testování uživatele (UAT) a odeslat testovací faktury. Elektronická fakturace podporuje konfiguraci testovacích digitálních certifikátů a v případě e-faktur vyžadujících digitální schválení také nastavení adresy URL ze zkušebních webových služeb zveřejněných daňovými úřady.

## <a name="is-there-any-documentation-about-the-out-of-box-country-specific-electronic-invoicing-features"></a>Existuje nějaká dokumentace o funkcích Elektronické fakturace specifických pro určitou zemi?

Ano. Informace o dostupnosti funkcí Elektronické fakturace a formátech, které podporuje, najdete v části [Dostupnost funkcí elektronické fakturace](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features).

> [!NOTE] 
> Pokud jste nenašli odpověď, kterou hledáte, pošlete svou otázku e-mailem týmu vývoje produktů na adresu <D365EInvoicePreview@microsoft.com>. Budeme vás kontaktovat nebo vylepšíme rozsah témat těchto často kladených otázek.
