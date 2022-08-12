---
title: Často kladené dotazy ke sloučení infrastruktiry Dynamics 365 Human Resources
description: Tento článek odpovídá na často kladené otázky o sloučení infrastruktury pro aplikace Microsoft Dynamics 365 Human Resources a finanční a provozní aplikace.
author: twheeloc
ms.date: 08/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fd71d728f9c97dc9e2c44a7e7a0e773be891b818
ms.sourcegitcommit: 6d9fcb52d723ac5022a3002e0ced8e7b56e9bc2a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/27/2022
ms.locfileid: "9203192"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Často kladené dotazy ke sloučení infrastruktiry Dynamics 365 Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="what-is-dynamics-365-human-resources"></a>Co je Dynamics 365 Human Resources?

Microsoft Dynamics 365 Human Resources poskytuje nástroje, které pomáhají personálním týmům zvýšit organizační agilitu, transformovat prostředí zaměstnanců a optimalizovat personální programy tak, aby se vytvořilo pracoviště, kde mohou lidé i firma prosperovat. Další informace o Dynamics 365 Human Resources viz [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **Transformace prostředí pro zaměstnance.** Udržte si špičkové výkony tím, že zmocníte manažery a zaměstnance prostřednictvím propojených samoobslužných prostředí, která podporují zapojení a růst.
- **Optimalizace personálních programů.** Snižte provozní náklady a vytvořte programy řízení dovolené a nepřítomnosti, času, benefitů a odměn zaměřené na lidi.
- **Zvýšení organizační agility.** Umožněte personálnímu oddělení pracovat s obratností, kterou firma vyžaduje, využitím Dataverse a Microsoft Power Platform k centralizaci dat o lidech a snadno rozšiřte Dynamics 365 Human Resources.
- **Objevte informace o pracovnících.** Rozhodujte se na základě dat prostřednictvím schopnosti analyzovat a vizualizovat data lidí na bohatých řídicích panelech, které jsou dostupné na jakémkoli zařízení.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Hodnota a výhody sloučení infrastruktury

### <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Co je sloučení infrastruktury Dynamics 365 Human Resources?

V současné době existují dvě samostatné sady funkcí HR na dvou různých infrastrukturách v Dynamics 365:

- **Dynamics 365 Human Resources** – Samostatná aplikace, která běží na nezávislé infrastruktuře. Když byla tato aplikace spuštěna, infrastruktura byla oddělena od ostatních provozních aplikací Dynamics 365. Naši zákazníci používají tuto aplikaci ke zvýšení organizační agility, optimalizaci personálních programů, transformaci prostředí zaměstnanců a získání přehledu o pracovnících.
- **Modul HR** – Starší sada funkcí, která byla dříve součástí skladové položky (SKU) licence Unified Operations. Modul HR běží na finanční a provozní infrastruktuře, která je stejná ve všech provozních aplikacích. Tyto aplikace zahrnují Dynamics 365 Finance, Dynamics 365 Project Operations a Dynamics 365 Supply Chain Management. Zákazníci získali funkce HR v rámci Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management.

Během posledních tří let společnost Microsoft nepřidala do modulu HR žádné nové funkce ani vylepšení. Místo toho se naše investice do plánu zaměřily na aplikace Dynamics 365 Human Resources.

Začleněním těchto dvou sad funkcí do stejné infrastruktury pomůžeme zákazníkům získat následující výhody:

- Vylepšení, která byla přidána do Dynamics 365 Human Resources za poslední tři roky, včetně rozšířené dovolené a nepřítomnosti, správy dávek a výkaznictví.
- Vylepšená rozšiřitelnost díky Microsoft Power Platform a schopnost rozšířit obchodní logiku o personalizaci stránek.
- Vylepšené nasazení, aplikace a údržba, které jsou konzistentní z hlediska správy životního cyklu aplikací (ALM), Lifecycle Services, geografické dostupnosti, rozšiřitelnosti a další.
- Více technologických inovací, protože náš technický tým využívá sdílené služby, nástroje a snížené náklady na platformu.

Tento přechod se dotkne zákazníků, kteří aktuálně využívají Dynamics 365 Human Resources nebo starší modul HR.

## <a name="glossary-of-terms-used-in-this-faq"></a>Slovníček termínů použitých v těchto častých otázkách

- **Dynamics 365 Human Resources** – Náš současný a budoucí produkt, který nabízí funkce personalistiky na trhu.
- **Modul HR** – Starší sada funkcí, která byla dříve součástí nabídky licence Unified Operations. Funkce jsou aktivní, když zákazník vlastní Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management.
- **Finanční a provozní infrastruktura** – Vývojová architektura, kterou používá provozní portfolio, včetně Dynamics 365 Finance, Dynamics 365 Supply Chain Management a Dynamics 365 Project Operations. Tato infrastruktura bude v budoucnu využívána. V těchto častých otázkách termín *sloučená infrastruktura* odkazuje na finanční a provozní prostředí.
- **Infrastruktura Human Resources** – Vývojová architektura, která byla historicky používána pro aplikace Dynamics 365 Human Resources. Projekt sloučení infrastruktury přináší Dynamics 365 Human Resources do finanční a provozní infrastruktury. Samostatná infrastruktura bude ukončena.

## <a name="general-questions-about-the-infrastructure-merge"></a>Obecné otázky týkající se sloučení infrastruktury

### <a name="will-customers-lose-any-features-or-capabilities"></a>Přijdou zákazníci o nějaké funkce nebo funkce?

Naším cílem je minimalizovat dopad, který má tento přechod na zákazníky. Nebudeme odstraňovat žádné funkce ani schopnosti. Mezi Dynamics 365 Human Resources a modulem HR bude funkční parita. V případech, kdy funkce existuje v obou infrastrukturách, bude využito prostředí Dynamics 365 Human Resources.

### <a name="will-the-user-experience-change"></a>Změní se prostředí?

Uživatelské prostředí bude konzistentní se standardní platformou Dynamics 365. Přestože obecné prostředí pro řídicí panel a nabídky zůstane podobné, bude sladěno se standardním prostředím aplikace Dynamics 365 Finance. Navigace bude zahrnovat moduly i pracovní plochy, umožní oblíbené položky a další. Pracovní prostory Dynamics 365 Human Resources, jako např. **Personální management** a **Lidé**, se začlení do finanční a provozní infrastruktury. V budoucnu budou nové funkce poskytovány prostřednictvím správy funkcí, která zákazníkům umožní zobrazit nové funkce a rozhodnout se, které z nich chtějí používat. Více informací viz [Přehled správy funkcí](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a [Dokumentace uživatelského rozhraní](../fin-ops-core/fin-ops/get-started/user-interface-elements.md?toc=/dynamics365/human-resources/toc.json).

### <a name="when-will-the-dynamics-365-human-resources-infrastructure-merge-be-completed"></a>Kdy bude sloučení infrastruktury Dynamics 365 Human Resources provedeno?

Sloučení infrastruktury bude probíhat ve fázích, aby zákazníci měli čas na plánování a provedení nezbytných kroků. Začali jsme zavádět funkce ve vlně 2 vydání Dynamics 2021. Plánujeme dokončit veškerý vývoj produktu pro tento projekt do konce 2. vlny vydání v roce 2022. Upozorňujeme, že časové osy se mohou změnit. Pro nejaktuálnější informace viz [plány vydání](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance).

### <a name="what-training-and-resources-will-be-available-to-help-with-the-infrastructure-merge"></a>Jaké školení a zdroje budou k dispozici na pomoc se sloučením infrastruktury?

Poskytneme dokumentaci, která bude podrobně popisovat každý krok sloučení infrastruktury. Podle potřeby poskytneme další školicí zdroje, jako jsou videa a workshopy, abychom pomohli zákazníkům a partnerům s hladkým přechodem.

### <a name="will-there-be-changes-in-development-capabilities-after-the-infrastructure-merge-is-completed"></a>Dojde ke změnám ve vývojových schopnostech po dokončení sloučení infrastruktury?

Chcete-li se dozvědět více o možnostech vývoje, viz [Vývoj a přizpůsobení domovské stránky](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

## <a name="feature-availability-questions"></a>Otázky na dostupnost funkcí

### <a name="will-the-linkedin-talent-hub-integration-work-on-the-finance-and-operations-infrastructure"></a>Bude integrace LinkedIn Talent Hub fungovat ve finanční a provozní infrastruktuře?

Ne, integrace LinkedIn Talent Hub nebude součástí sloučené infrastruktury. Veřejná rozhraní pro programování aplikací (API) jsou k dispozici pro vytváření integrací s řešeními pro nábor a sledování uchazečů. Zákazníci, kteří plánují používat LinkedIn Talent Hub, by měli spolupracovat se svým partnerem Microsoft na integraci pomocí poskytovaných rozhraní API. Další informace o rozhraní API pro integraci systému sledování žadatelů (ATS) naleznete v tématu [Představení API pro integraci systému sledování žadatelů](./hr-admin-integration-ats-api-introduction.md).

### <a name="will-the-capabilities-that-are-currently-available-only-in-dynamics-365-human-resources-for-example-leave-management-and-benefits-management-be-available-after-the-merge-is-completed"></a>Budou funkce, které jsou aktuálně dostupné pouze v Dynamics 365 Human Resources (například správa dovolené a správa výhod), k dispozici po dokončení sloučení?

Ano. Všechny funkce aplikace Dynamics 365 Human Resources se zavádějí do finanční a provozní infrastruktury. Funkce budou zpřístupněny ve fázích. Chcete-li získat aktuální informace o dostupnosti funkcí pro sloučenou infrastrukturu, pravidelně kontrolujte [plány vydání](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance).

### <a name="will-ceridian-integrations-with-dynamics-365-human-resources-be-available-after-the-infrastructure-merge-is-completed"></a>Budou integrace Ceridian s Dynamics 365 Human Resources k dispozici i po dokončení sloučení infrastruktury?

Ceridian je v procesu vytváření integrace V2 s Dynamics 365 Human Resources, který využívá rozhraní API mezd. Integrace založená na souborech, která aktuálně existuje v Dynamics 365 Human Resources, nebude migrována do finanční a provozní infrastruktury. Další informace viz [Úvod k Payroll API](./hr-admin-integration-payroll-api-introduction.md).

### <a name="will-applicant-tracking-or-onboardingoffboarding-of-employees-functionality-be-included"></a>Bude zahrnuto sledování žadatelů nebo onboarding/offboarding funkcí zaměstnance?

V předchozích verzích jsme vytvořili ATS Integration API, abychom partnerům a zákazníkům umožnili vytvářet integrace ATS s Human Resources. Další funkce související s ATS byly k dispozici ve vlně 1 2022. V budoucích verzích budeme tato rozhraní API nadále vylepšovat.

Funkce HR, která v současnosti existuje ve finanční a provozní infrastruktuře, zahrnuje některé funkce pro řízení náboru, které neexistují v Dynamics 365 Human Resources. Po dokončení sloučení infrastruktury, budou tyto funkce dostupné pro všechny zákazníky Human Resources. Tato funkce poskytuje odlehčenou funkcionalitu ATS. V budoucnu však neplánujeme tuto funkci rozšiřovat. Zákazníci, kteří vyžadují pokročilejší funkce, mohou využít výhod partnerských integrací ATS. Další informace o rozhraní API pro integraci ATS naleznete v tématu [Představení API pro integraci systému sledování žadatelů](./hr-admin-integration-ats-api-introduction.md).

### <a name="will-the-dynamics-ax-2012-upgrade-tools-be-used-to-upgrade-the-hr-module-in-ax-2012-to-the-dynamics-365-human-resources-app"></a>Budou použity nástroje pro upgrade Dynamics AX 2012 k upgradu modulu HR v AX 2012 do aplikace Dynamics 365 Human Resources?

Ano. Upgrade z Dynamics AX 2012 na Dynamics 365 Human Resources využije stejnou cestu k upgradu a nástroje, které se používají k upgradu na nejnovější verzi ostatních provozních aplikací Dynamics 365, jako je Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management.

Další informace o migraci na finanční a provozní infrastrukturu viz [Časté otázky týkající se migrace zákazníků Human Resouces](./customer-migration.md).
