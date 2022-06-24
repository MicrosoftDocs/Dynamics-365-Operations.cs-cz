---
title: Elektronická fakturace – Často kladené otázky
description: Tento článek poskytuje informace o často kladených otázkách týkajících se Elektronické fakturace.
author: gionoder
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: fbb43438a9da567460eb744afb64dae5274f04a9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904347"
---
# <a name="electronic-invoicing-faq"></a>Časté otázky k elektronické fakturaci

[!include [banner](../includes/banner.md)]

Tento článek poskytuje odpovědi na často kladené otázky týkající se služby elektronické fakturace. Elektronická fakturace rozšiřuje možnosti elektronické fakturace, které existují v aplikacích Dynamics 365 Finance, Dynamics 365 Supply Chain Management a Dynamics 365 Project Operations. 

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

## <a name="does-electronic-invoicing-service-support-the-on-premises-installations-of-finance-supply-chain-management-and-project-operations"></a>Podporuje služba elektronické fakturace místní instalace aplikací Finance, Supply Chain Management a Project Operations? 

Aktuální platforma neumožňuje použití místní verze a neexistují žádné plány na její podporu v budoucnu.

## <a name="does-electronic-invoicing-service-interface-with-the-vendor-import-automation-feature"></a>Má služba elektronické fakturace rozhraní s funkcí automatizace importu od dodavatele?

Ne. Existují plány doplnit toto rozhraní, ale není určen žádný termín implementace. Po naplánování budou datumy oznámeny v [Plánech vydání](/dynamics365/release-plans/).

## <a name="how-does-electronic-invoicing-service-handle-file-attachments-into-the-electronic-invoice-is-a-sharepoint-server-needed-when-embedding-pdf-files-into-the-xml-file"></a>Jak služba elektronické fakturace zpracovává souborové přílohy k elektronické faktuře? Je při vkládání souborů PDF do souboru XML potřeba server SharePoint?

Se soubory připojenými k elektronické faktuře se zachází jako s vloženými binárními daty v prvku XML. Server SharePoint není pro vložení souborů PDF potřebný, ale příloha musí být uložena v systému pro správu dokumentů Finance, Supply Chain Management a Project Operations.

## <a name="is-electronic-invoicing-service-available-according-to-the-regulations-of-my-countryregion"></a>Je služba elektronické fakturace k dispozici podle předpisů mé země/oblasti?

Služba elektronické fakturace je platforma mikroslužeb, která bude globálně dostupná.

Společnost Microsoft plánuje zveřejnit formáty a integrace elektronických faktur pro země, které jsou funkčně lokalizovány společností Microsoft. Další informace najdete v tématu [Dostupnost funkcí elektronické fakturace](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features).

Pokud formát elektronické fakturace pro vaši zemi / region není uveden, je plánováno, že platforma v budoucnosti tento scénář podpoří. I nadále můžete využívat výhod možností konfigurace, které Elektronická fakturace má, a konfigurovat formát elektronické fakturace sami, nebo můžete spolupracovat s partnerem / nezávislým prodejcem softwaru a nakonfigurovat je pro vaši organizaci.

## <a name="is-dynamics-365-for-regulatory-services-a-new-module-like-human-resources-or-project-operations-that-is-linked-to-finance-or-supply-chain-management-are-there-extra-costs-for-that"></a>Je Dynamics 365 for Regulatory Services novým modulem, podobně jako Human Resources nebo Project Operations, který je propojen s Finance nebo Supply Chain Management? Připlácí se něco?

Dynamics 365 for Regulatory Services (RCS) je cloudová služba pro konfiguraci prostředků globalizace. RCS je zdarma pro všechny držitele licencí Finance, Supply Chain Management a Project Operations.

Chcete-li si zaregistrovat službu RCS, přejděte na stránku <https://marketing.configure.global.dynamics.com/>.

Pro více informací viz [Regulatory Configuration Services (RCS) - funkce globalizace](rcs-globalization-feature.md).

## <a name="do-i-need-to-sign-up-to-get-electronic-invoicing-service-or-just-turn-it-on-in-feature-management"></a>Musím se zaregistrovat, abych získal službu elektronické fakturace, nebo ji prostě zapnu ve správě funkcí?

Pokud máte licenci pro aplikace Finance, Supply Chain Management a Project Operations, přečtěte si téma [Začněte se správou služby doplňku elektronické fakturace](e-invoicing-get-started-service-administration.md) a zaregistrujte si elektronickou fakturaci.

## <a name="does-electronic-invoicing-service-work-with-tier-1-virtual-machines-what-is-the-minimal-required-environment"></a>Funguje služba elektronické fakturace s virtuálními počítači úrovně 1? Jaké je minimální požadované prostředí?

Integrace se službou elektronické fakturace vyžaduje k hostování aplikací Finance nebo Supply Chain Management virtuální stroj alespoň úrovně 2. Další informace o plánování prostředí naleznete v části [Plánování prostředí](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

## <a name="does-electronic-invoicing-service-have-a-test-mode-for-testing-invoice-submission"></a>Má služba Elektronická fakturace testovací režim pro testování odeslání faktury?

Toho lze dosáhnout konfigurací. Chcete-li otestovat odeslání faktury, můžete se připojit k Finance nebo Supply Chain Management z prostředí akceptačního testování uživatele (UAT) a odeslat testovací faktury. Elektronická fakturace podporuje konfiguraci testovacích digitálních certifikátů a v případě e-faktur vyžadujících digitální schválení také nastavení adresy URL ze zkušebních webových služeb zveřejněných daňovými úřady.

## <a name="is-there-any-documentation-about-the-out-of-box-country-specific-electronic-invoicing-features"></a>Existuje nějaká dokumentace o funkcích Elektronické fakturace specifických pro určitou zemi?

Ano. Informace o dostupnosti funkcí Elektronické fakturace a formátech, které podporuje, najdete v části [Dostupnost funkcí elektronické fakturace](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features).

## <a name="does-the-electronic-invoicing-service-allow-a-legal-entity-in-finance-or-supply-chain-management-that-is-configured-for-a-specific-country-to-consume-electronic-invoicing-features-from-different-countryregions"></a>Umožňuje služba elektronické fakturace právnické osobě ve Finance nebo Supply Chain Management, který je nakonfigurován pro konkrétní zemi, využívat funkce elektronické fakturace z jiných zemí/oblastí?

Ano. Funkce elektronické fakturace lze využít ke zpracování odeslání obchodních dokumentů nezávisle na zemi právnické osoby, pokud platí následující:

   - Generovaný obchodní dokument používá odpovídající mapování modelu dokumentu.
   - Ve funkci elektronické fakturace existuje shoda mezi obchodním dokumentem a pravidly použitelnosti.

## <a name="does-the-electronic-invoicing-service-use-the-same-configuration-and-design-experience-provided-by-the-electronic-reporting-module-in-finance-and-supply-chain-management"></a>Využívá služba elektronické fakturace stejnou konfiguraci a design, jaké poskytuje modul elektronického výkaznictví ve Finance a Supply Chain Management? 

Ano. Stejné nástroje pro návrháře, které se používají v modulu elektronického výkaznictví (ER) ve Finance a Supply Chain Management, se používají k vytváření a konfiguraci mapování datových modelů a konfigurací formátů souborů. Tyto návrhářské nástroje se také používají v Regulatory Configuration Services (RCS) k vytváření a konfiguraci mapování datových modelů a konfigurací formátu souborů, které se používají při konfiguraci funkcí elektronické fakturace.

## <a name="can-the-applicability-rules-be-extended-and-configured-so-that-they-arent-tied-to-any-specific-parameter-such-as-a-legal-entity"></a>Lze pravidla použitelnosti rozšířit a nakonfigurovat tak, aby nebyla vázána na žádný konkrétní parametr, například na právnickou osobu?

Ano. Pravidla použitelnosti jsou plně konfigurovatelná. Můžete přidávat nebo odebírat klauzule, vytvářet logické operace a seskupovat a oddělovat klauzule. Další informace naleznete v tématu [Pravidla použitelnosti](e-invoicing-configuration-rcs.md?toc=/dynamics365/finance/toc.json#applicability-rules).

## <a name="does-the-electronic-invoicing-service-support-adding-other-er-format-configurations-to-generate-other-types-of-documents-does-it-support-sending-the-documents-electronically-to-customers-such-as-a-delivery-note"></a>Podporuje služba elektronické fakturace přidávání dalších konfigurací formátu ER pro generování dalších typů dokumentů? Podporuje elektronické zasílání dokumentů zákazníkům, například dodací list?

K vytvoření požadovaných výstupních souborů můžete použít jiné konfigurace formátu ER. Konfigurace formátu ER však musí být odvozena ze stejného mapování modelu faktury ER, které je nakonfigurováno ve službě Finance nebo Supply Chain Management pro generování obchodních dokumentů. Odeslání výstupního souboru přímo zákazníkovi jako transakce EDI není elektronickou fakturací podporováno přímo.

## <a name="does-the-electronic-invoicing-service-support-exchanging-electronic-invoices-with-customers-does-it-support-configuring-different-invoice-formats-for-the-same-invoice"></a>Podporuje služba elektronické fakturace výměnu elektronických faktur se zákazníky? Podporuje konfiguraci různých formátů faktur pro stejnou fakturu?

Schopnost přijímat a importovat elektronické faktury dodavatele je v plánu, ale automatické odesílání elektronických faktur zákazníkům není aktuálně podporováno.

## <a name="does-the-electronic-invoicing-service-extend-to-support-exchanging-edi-messages-with-other-companies"></a>Rozšiřuje služba elektronické fakturace podporu výměny zpráv EDI s jinými společnostmi?

Služby elektronické fakturace se zaměřují na výměnu typů zpráv elektronických faktur založených na požadavcích dodržování předpisů. Příjem a import elektronických faktur dodavatele je v plánu, ale odesílání souborů elektronických faktur zákazníkům není aktuálně podporováno přímo, s výjimkou scénářů, kdy je odeslání elektronické faktury zákazníkovi regulačním požadavkem.

## <a name="does-the-electronic-invoicing-service-support-importing-or-merging-customizations-made-in-the-er-format-configurations-from-the-legacy-electronic-invoicing-feature"></a>Podporuje služba elektronické fakturace import nebo slučování přizpůsobení provedených v konfiguracích formátu ER ze starší funkce elektronické fakturace?

Konfigurace formátu ER můžete znovu použít ve službě elektronické fakturace. Konfigurace formátu ER však musí být odvozena ze stejného mapování modelu faktury ER, na jehož použití byla funkce elektronické fakturace navržena a které je nakonfigurováno ve službě Finance nebo Supply Chain Management pro generování obchodních dokumentů.

## <a name="does-the-electronic-invoicing-service-support-issuing-electronic-invoices-from-custom-made-tables-if-so-how-do-you-create-the-er-data-model-configurations-for-these-new-tables-and-entities"></a>Podporuje služba elektronické fakturace vydávání elektronických faktur z vlastních tabulek? Pokud ano, jak vytvoříte konfigurace datového modelu ER pro tyto nové tabulky a entity?

Ano. Vyžaduje však přizpůsobení mapování modelu faktury a přidání potřebných odkazů do tabulek na míru, nebo v závislosti na složitosti vytvoření nového mapování modelu faktury.

## <a name="does-the-electronic-invoicing-service-support-different-web-service-endpoints"></a>Podporuje služba elektronické fakturace různé koncové body webových služeb?

Elektronická fakturace podporuje různé koncové body webových služeb. Můžete použít konfigurovatelnou integraci s webovými službami REST nebo celou řadu parametrizovaných integrací webových služeb specifických pro jednotlivé země. Pro stejné webové služby a rozhraní API lze konfigurovat různé koncové body pomocí různých verzí konfigurací. Další informace viz [Seznam parametrů podle akce](e-invoicing-setup.md#list-of-parameters-by-action).

## <a name="is-electronic-invoicing-integrated-with-the-various-invoice-operators-apis-from-the-nordic-countries-or-should-that-be-handled-on-a-case-by-case-basis"></a>Je elektronická fakturace integrována do různých API operátorů faktur ze severských zemí, nebo by to mělo být řešeno případ od případu?

Společnost Microsoft neustále rozšiřuje funkční pokrytí, aby poskytovala okamžité integrace pomocí funkcí elektronické fakturace. Další informace o podporovaných formátech a integracích viz [Dostupnost funkcí elektronické fakturace](e-invoicing-configuration-rcs.md?toc=/dynamics365/finance/toc.json#availability-of-electronic-invoicing-features).

> [!NOTE] 
> Pokud jste nenašli odpověď, kterou hledáte, pošlete svou otázku e-mailem týmu vývoje produktů na adresu <D365EInvoicePreview@microsoft.com>. Budeme vás kontaktovat nebo vylepšíme rozsah témat těchto často kladených otázek.
