---
title: Funkce aplikace Store Commerce
description: Tento článek popisuje funkce, které jsou k dispozici v aplikaci Store Commerce pro Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2022-09-30
ms.openlocfilehash: d713cc0e9537ae20ffddee6e77779a16e74bd779
ms.sourcegitcommit: eb9a53d5cf10f1ada68757536d6a94b2cb00929d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/27/2022
ms.locfileid: "9725631"
---
# <a name="store-commerce-app-capabilities"></a>Funkce aplikace Store Commerce

[!include [banner](includes/banner.md)]

Aplikace Store Commerce je aplikace moderního pokladního místa (POS) pro Microsoft Dynamics 365 Commerce. Umožňuje podnikům zpracovávat transakce v obchodě a řídit operace back-office, jako je inventarizace a zpracování objednávek. Aplikace také umožňuje podnikům řídit vztahy se zákazníky s loajalitou a klientelou. 

Aplikace Store Commerce, založená na Commerce Scale Unit (CSU), poskytuje kompletní vícekanálové řešení. Zákazník si například může koupit produkt online a vyzvednout si ho v nedalekém obchodě, a tak pokračovat ve své nákupní cestě napříč kanály, aniž by ztratil jakákoli data. 

Tento článek poskytuje přehled podpory pro aplikace Store Commerce.

## <a name="platform"></a>Platforma

| Schopnost | Popis | Dokumentace | Doplňkový obsah |
|---|---|---|---|
| Omnikanál | Dynamics 365 Commerce poskytuje komplexní omnikanálové řešení, které sjednocuje administrativu, obchod, kontaktní středisko a digitální zkušenosti. | [Přehled](index.md) | [Technické přednášky](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/dynamics-365-commerce-overview-november-2-2020) |
| Bezobslužná aplikace Commerce | Commerce Scale Unit hostuje bezobslužný komerční modul. Ten slouží jako centrální bod pro veškerou obchodní logiku a pohání kompletní vícekanálové řešení. | <p>[Přehled architektury](commerce-architecture.md)</p><p>[Bezobslužná architektura](dev-itpro/retail-server-architecture.md)</p> | [Technické přednášky](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-commerce-architecture-overview-december-4-2020) |
| Commerce Headquarters | Commerce headquarters poskytuje funkce backoffice, které umožňují konfiguraci produktů, zaměstnanců, obchodních procesů, cen a dalších funkcí, které jsou pro podnikání vyžadovány. | [Přehled architektury](commerce-architecture.md) | |
| Pokladní místo (POS) | Aplikace Store Commerce je prostředí z POS pro Dynamics 365 Commerce. Poskytuje bohaté a komplexní funkce POS, které pomáhají obchodním partnerům, pokladním a manažerům poskytovat vynikající služby zákazníkům. Kromě toho poskytuje prodejcům několik možností nasazení, pomáhá zlepšovat výkon a nabízí vylepšenou správu životního cyklu aplikací (ALM). | [Aplikace Store Commerce](dev-itpro/store-commerce.md) | <p>[Technické přednášky](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/modernize-the-dynamics-365-commerce-in-store-technology-using-the-new-store-commerce-app-march-30-2022)</p><p>[Video](https://youtu.be/7B332XH_zfs)</p><p>[Migrace z MPOS do Store Commerce](dev-itpro/pos-extension/migrate-mpos-store-commerce.md)</p> |
| Cloudové nasazení | Pro rozložení zátěže a geografickou blízkost lze nasadit více instancí Commerce Scale Units. | [Cloudové nasazení](../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md) | |
| Místní nasazení | Pomocí místního nasazení podnikových dat mohou zákazníci Commerce lépe vlastnit a spravovat prostředí Dynamics 365. | [Místní nasazení](../fin-ops-core/dev-itpro/deployment/deploy-retail-onprem.md) | |

## <a name="device-management"></a>Správa zařízení

| Schopnost | Popis | Dokumentace | Doplňkový obsah |
|---|---|---|---|
| Více provedení | Aplikace Store Commerce je podporována na různých typech zařízení, jako jsou počítače, tablety a mobilní zařízení. Responzivní uživatelské rozhraní (UI) umožňuje rozložení automatickou změnu velikosti a přizpůsobení velikosti obrazovky. | [Vizuální konfigurace](pos-screen-layouts.md) | |
| Mezi platformami | Aplikace Store Commerce je podporována na webových platformách a v platformě Windows, iOS a Android. | [Platformy](dev-itpro/hybridapp.md) | |
| Značka | Návrhář obrazovky vám umožňuje přizpůsobit rozvržení obrazovky tak, aby vyhovovala vašim obchodním požadavkům. Kromě toho lze motivy, rozložení, barvy a obrázky vytvářet na základě rolí zaměstnanců a poté je lze sdílet mezi uživateli pro konzistenci značky a snadné použití. | [Vizuální konfigurace](pos-screen-layouts.md) | [Video](https://www.youtube.com/watch?v=ldqCw2wf5fY) |
| Topologie | V závislosti na dostupnosti sítě jsou podporovány různé topologie v obchodě. | <p>[Topologie](dev-itpro/retail-modern-pos-architecture.md)</p><p>[Infografika](dev-itpro/retail-in-store-topology.md)</p> | |
| Správa více zařízení | Z Commerce headquarters lze snadno spravovat více zařízení napříč obchody. | [Aktivace](set-up-activation-accounts-validate-devices-hq.md) | [Technické přednášky](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/commerce-mass-deployment-with-sccm-system-center-configuration-manager-october-6-2022) |

## <a name="employee-management"></a>Správa zaměstnanců

| Schopnost | Popis | Dokumentace | Doplňkový obsah |
|---|---|---|---|
| Přihlášení | Každý zaměstnanec obchodu může mít vyhrazené přihlášení. Typy přihlášení zahrnují uživatelské jméno, čárový kód, čtečku magnetických proužků (MSR), biometrické údaje a Azure Active Directory (Azure AD). | <p>[Azure AD](aad-pos-logon.md)</p><p>[Rozšířené přihlášení](extended-logon.md)</p> | |
| Oprávnění | Pro zaměstnance jsou podporovány různé úrovně oprávnění, například oprávnění k vytváření objednávek a oprávnění k úpravě objednávek. | [Oprávnění](tasks/create-pos-permission-groups.md) | |
| Správa času a docházky | Docházku lze řídit pomocí funkce Time Clock. Údaje o docházce lze zpracovat do mezd pomocí aplikace Dynamics 365 Human Resources. | [Správa času](retail-time-attendance.md) | |
| Provize z prodeje | Prodeje sledované podle obchodního zástupce se lze používat k výpočtu provize nebo jiné pobídky. | [Komise](pos-sales-groups-track-commissions.md) | |

## <a name="merchandising"></a>Podpora prodeje

| Schopnost | Popis | Dokumentace | Doplňkový obsah |
|---|---|---|---|
| Správa sortimentu | Manažeři merchandisingu mohou produkty třídit tak, aby byly k dispozici k prodeji v konkrétním kanálu a během určitého období. | [Sortimenty](assortments.md) | |
| Katalogy | Manažeři merchandisingu mohou spravovat katalogy, aby identifikovali produkty, které chcete nabízet, s cenou podle katalogu. | [Katalogy](/dynamicsax-2012/appuser-itpro/about-retail-product-catalogs) | |
| Správa produktů a kategorií | V Commerce headquarters mohou merchandisingoví manažeři vytvářet produkty, které mají varianty, atributy, měrnou jednotku a tak dále. Mohou také definovat hierarchii kategorií pro organizaci produktů. | [Produkt](retail-hierarchies.md) | |
| Sady | Manažeři merchandisingu mohou seskupovat produkty tak, aby byly prodávány jako balíček nebo sada. | [Sady](/dynamicsax-2012/appuser-itpro/about-setting-up-retail-product-kits) | |
| Informační kódy | Pomocí informačních kódů můžete pokladní vyzvat k zadání informací při různých činnostech na pokladně, jako je prodej zboží, vrácení zboží nebo výběr zákazníka. | [Informační kódy](/dynamicsax-2012/appuser-itpro/about-info-codes-retail) | |
| Propojené položky | Použijte propojené položky k upsell produktů, když je položka přidána do transakce. | [Propojené položky](/dynamicsax-2012/appuser-itpro/set-up-products-for-cross-selling-and-up-selling) | |
| Záruky | Prodloužené záruky lze prodávat společně s produkty. | [Záruka](extended-warranty.md) | |
| Tisk štítků | Lze vygenerovat štítky, které obsahují informace o výrobku, jako je číslo šarže, sériové číslo a datum spotřeby. | [Tisk štítků](/dynamicsax-2012/appuser-itpro/create-and-print-labels-overview) | |

## <a name="assisted-selling"></a>Asistovaný prodej

| Schopnost | Popis | Dokumentace | Doplňkový obsah |
|---|---|---|---|
| Procházení produktů | Procházejte produkty podle kategorie. | [Hierarchie výrobků](retail-hierarchies.md) | |
| Hledání produktu | Vyhledávejte produkty podle názvu a upřesněte vyhledávání pomocí atributů produktu, jako je značka, cena a materiál. Tato funkce je založena na Azure Cognitive Search. | [Hledání využívající cloud](cloud-powered-search-overview.md) | |
| Strnka Podrobnosti o produktu | Bohaté stránky s podrobnostmi o produktu mohou obsahovat obrázky, popis, atributy produktu a doporučené produkty. Doporučení využívají službu doporučení. | | |
| Porovnání produktů | Porovnejte více produktů a pomozte zákazníkům vybrat si jeden a přidat jej do transakce. | | |
| Nekonečná ulička | Snadno vyhledávejte zásoby v jiných obchodech a vytvářejte objednávky. | [Vyhledávání zásob](pos-inventory-lookup-operation.md) | [Technické přednášky](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Doporučení | Používejte upsell a cross-sell produktů pomocí služby doporučení. Tato služba využívá patentovanou technologii k navrhování doporučení na základě nákupních trendů a charakteristik, jako jsou nově příchozí, podobný vzhled a nejprodávanější. Tato doporučení jsou k dispozici na stránkách s podrobnostmi o produktu, stránky **Podrobnosti o zákazníkovi** a stránky **Transakce**. | [Doporučení](product-recommendations.md) | [Technické přednášky](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-recommendations-march-2-2021) |

## <a name="customer-relationship"></a>Vztah s odběratelem

| Schopnost | Popis | Dokumentace | Doplňkový obsah |
|---|---|---|---|
| Správa zákazníků | Vytvoření, úprava nebo správa bankovních účtů odběratelů Zákaznické účty lze spravovat v asynchronním režimu, aby se zabránilo zpracování v reálném čase. | [Řízení](customer-mgmt-stores.md) | |
| Atributy odběratele | Rámec atributů zákazníků umožňuje získat další data související se zákazníky na základě obchodních požadavků. | [Atributy](dev-itpro/customer-attributes.md) | |
| Stránka podrobností o zákazníkovi | Bohatá stránka s podrobnostmi o zákaznících poskytuje vícekanálový pohled na interakce zákazníka napříč všemi kanály. Tyto interakce zahrnují nákupy, seznamy přání a věrnostní body. | | |
| Vyhledávání zákazníka využívající cloud | Vyhledávejte zákazníky podle jména, telefonního čísla, e-mailové adresy, věrnostní karty, adresy a tak dále. | [Hledání využívající cloud](pos-search-improvements.md#customer-search) | |
| Věrnost a odměny | Zákazníci se mohou zapojit do věrnostních programů a získávat a uplatňovat věrnostní body napříč kanály. | [Loajalita](set-up-customer-loyalty-program.md) | |
| Clienteling | Spravujte klíčové zákazníky pomocí knihy klientů a sledujte aktivity a poznámky v profilu zákazníka. Integrace Dynamics 365 Customer Insights umožňuje zaměstnancům získat podněty ohledně další nejlepší akce pro každého zákazníka. | [Clienteling](clienteling-overview.md#activities-and-notes) | |

## <a name="pricing-and-discounts"></a>Tvorba cen a slevy

| Schopnost | Popis | Dokumentace | Doplňkový obsah |
|---|---|---|---|
| Obchodní dohody | Cenoví manažeři mohou používat obchodní dohody k definování speciálních cen na základě dlouhodobých obchodů pro konkrétní zákazníky. | [Ceny](price-management.md)| [Video](https://www.youtube.com/watch?v=r2VD8IxHesM) |
| Prodejní smlouvy | Cenoví manažeři mohou používat prodejní smlouvy k definování smluvních cen v obchodních scénářích mezi podniky (B2B). | [Ceny](price-management.md) | |
| Úpravy cen | Správci cen mohou pomocí funkce úprav cen vytvářet, sledovat a spravovat cenové přirážky pro své produkty v průběhu času. | [Úpravy cen](price-adjustments-discounts.md) | |
| Slevy | Cenoví manažeři mohou nastavit několik typů slev a spustit různé propagační akce. Tyto slevy zahrnují jednoduché slevy, množstevní slevy, prahové slevy, kombinované slevy, slevy na základě nabídky a slevy na dopravu. | [Slevy](retail-discounts-overview.md) | |
| Kupóny | Cenoví manažeři mohou nastavit kódy kuponů nebo čárové kódy, propojit je se slevami a distribuovat je zákazníkům. Obchodní partneři mohou přidávat kupony do prodejních transakcí nebo je odstraňovat. | [Kupóny](coupons.md) | |
| Cenové skupiny | Cenoví manažeři mohou využít schopnost cenové skupiny k definování kontextových cen na základě kanálů, katalogů, přidružení nebo věrnostních programů. | [Ceny](price-management.md) | |
| Dostupné propagace | Obchodní partneři mohou snadno vyhledat dostupné propagační akce pro produkty v obchodě, produkty, které byly přidány k transakci atd. | [Cenové funkce](pos-pricing-functions.md) | |
| Kontroly ceny | Obchodní partneři mohou rychle zkontrolovat aktivní prodejní ceny produktů v obchodě. | [Cenové funkce](pos-pricing-functions.md) | |
| Přepsání ceny | Obchodní partneři, kteří mají požadovaná oprávnění, mohou přepsat systémem nakonfigurované nebo vypočítané ceny. | [Cenové funkce](pos-pricing-functions.md) | |
| Ruční slevy | Obchodní partneři, kteří mají požadovaná oprávnění, mohou uplatnit manuální slevy na prodejní transakce nebo prodejní linky. | [Cenové funkce](pos-pricing-functions.md) | |

## <a name="electronic-payments"></a>Elektronické platby

| Schopnost | Popis | Dokumentace | Doplňkový obsah |
|---|---|---|---|
| Dal a Má dáti | Aplikace Store Commerce podporuje hlavní platby kreditními a debetními kartami prostřednictvím platební brány Adyen a plnění objednávek prostřednictvím služby PayPal. Sada Payments SDK umožňuje připojení externí brány, která jsou podporována integracemi nezávislých dodavatelů softwaru (ISV). | <p>[Adyen](dev-itpro/adyen-connector.md?tabs=10-0-23)</p><p>[PayPal](paypal.md)</p><p>[Platby](payment-methods.md)</p> | <p>[Technické přednášky](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-configuration-february-9-2021)</p><p>[Technické přednášky](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-overview-processing-february-4-2021)</p> |
| Podpora digitální peněženky | Aplikace Store Commerce podporuje platby prostřednictvím platebních metod digitální peněženky, které nepoužívají rozsahy bankovních identifikačních čísel (BIN) jako tradiční kreditní a debetní karty. Platební metody lze namapovat na platby digitální peněženkou, jako je Adyen. | [Peněženka](wallets.md) | |
| Podpora dárkové karty | Bankovní identifikační číslo Dárková karta Dynamics 365, dárkové karty Stored Value Solutions (SVS) a Givex. Dárkové poukazy lze zakoupit a uplatnit v objednávce. | [Dárkové poukazy](dev-itpro/gift-card.md) | [Technické přednášky](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/d365-commerce-internal-gift-cards-november-16-2021) |
| Ochrana proti podvodům | Dynamics 365 Fraud Protection vám pomůže předcházet podvodným aktivitám a identifikovat místa, kde mohou být podvody nepovšimnuty. | [Ochrana proti podvodům](dev-itpro/dfp.md) | [Video](https://www.youtube.com/watch?v=j_1nEiq3LfM) |

## <a name="taxes-and-charges"></a>Daně a poplatky

| Schopnost | Popis | Dokumentace | Doplňkový obsah |
|---|---|---|---|
| Daně | Alikace Store Commerce podporuje spoustu typů nepřímých daní, jako daň z prodeje, daň z přidané hodnoty (DPH), daň ze zboží a služeb tax (GST), poplatky jednotkové poplatky a srážková daň. | [Daně](/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json) | |
| Poplatky | Poplatky lze konfigurovat na úrovni řádku, na úrovni záhlaví, jako automatické poplatky, podle kanálu a tak dále. | [Poplatky](omni-auto-charges.md) | |

## <a name="order-processing-and-fulfillment"></a>Zpracování a plnění objednávek

| Schopnost | Popis | Dokumentace | Doplňkový obsah |
|---|---|---|---|
| Tvorba objednávky | Objednávku lze vytvořit k odeslání nebo k vyzvednutí v blízké prodejně. Pro vyzvednutí lze poskytnout časové sloty. | [Přehled](customer-orders-overview.md) | |
| Úprava objednávky | Objednávku lze upravit, vrátit, zrušit a podobně. | <p>[Zrušit](customer-orders-overview.md#cancel-a-customer-order)</p><p>[Vrácení](pos-returns.md)</p> | |
| Hledání | Vyhledávejte a filtrujte objednávky pomocí informací specifických pro objednávku. | [Hledání](enhancedorderrecall.md) | |
| Atributy objednávky | Rámec atributů objednávky umožňuje získat další informace související se zákazníky na základě obchodních požadavků. | [Atributy](dev-itpro/order-attributes.md) | |
| Přímá dodávka | Položky mohou být označeny pro přímé doručení prodejcem na adresu zákazníka. Přímé doručení je též známa jako rozvážka. | [Přímá dodávka](/dynamics365/supply-chain/sales-marketing/tasks/ship-orders-direct-deliveries) | |
| Nabídka | Zaměstnanci obchodu mohou vytvářet nabídky pro zákazníky a mohou specifikovat speciální cenu, manuální slevy a datum platnosti nabídky. | [Nabídka](/dynamics365/supply-chain/sales-marketing/tasks/create-edit-sales-quotations) | |
| Plnění | Obchody mohou vybírat, balit a odesílat objednávky. K balíkům, které jsou připraveny k odeslání, lze přidat dodací list. | [Plnění](order-fulfillment-overview.md) | [Technické přednášky](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-supporting-buy-online-pickup-in-store-curbside-with-dynamics-365-commerce-pos-february-3-2021) |
| Distribuovaná správa objednávek | Aplikace Store Commerce podporuje inteligentní optimalizaci plnění objednávek, kde lze obchodní strategie konfigurovat na základě povahy podnikání, typu zákazníka, původu objednávky a způsobu doručení objednávky. | [DOM](dom.md) | |

## <a name="inventory-management"></a>Řízení zásob

| Schopnost | Popis | Dokumentace | Doplňkový obsah |
|---|---|---|---|
| Buyer's push | Zefektivněte distribuci dostupného inventáře z distribučního centra do více obchodů nebo skladů. | [Buyer's push](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [Technické přednášky](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Cross-docking | Zjednodušte distribuci zásob na příchozích objednávkách do více obchodů nebo skladů. | [Cross docking](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [Technické přednášky](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Příchozí zásoby | Příjem zásob od dodavatele prostřednictvím nákupní objednávky nebo z jiného skladu prostřednictvím převodního příkazu. Vytvořte příchozí nákupní objednávku nebo požadavek převodní objednávky. | [Příchozí](pos-inbound-inventory-operation.md) | [Technické přednášky](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Odchozí zásoby | Odešlete zásoby do jiného skladu prostřednictvím převodního příkazu a vytvořte požadavek na odchozí převodní příkaz. | [Odchozí](pos-outbound-inventory-operation.md) | [Technické přednášky](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Vyhledávání zásob | Kontrolujte skladové zásoby produktů v obchodech a skladech a kontrolujte zásoby dostupné k příslibu (ATP) v budoucích datech. | [Vyhledávání zásob](pos-inventory-lookup-operation.md) | [Technické přednášky](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Úprava zásob | Upravte zásoby do nebo ze skladu v obchodě tak, aby splňovaly specifické obchodní požadavky bez použití prodeje, příjmu nebo přepočítávání. | [Úprava zásob](work-with-store-inventory.md) | [Technické přednášky](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Počty na skladě | Počítejte fyzické zásoby a upravte inventář systémového účetnictví tak, aby tomu odpovídal. | [Inventura](work-with-store-inventory.md) | [Technické přednášky](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Přesun zásob | Přesouvejte inventář mezi místy v obchodě. | [Přesun](work-with-store-inventory.md) | [Technické přednášky](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |

## <a name="financials"></a>Finance

| Schopnost | Popis | Dokumentace | Doplňkový obsah |
|---|---|---|---|
| Řízení hotovosti | Aplikace Store Commerce podporuje správu hotovosti a dalších specifikovaných nabídek v obchodě. Kromě toho lze povolit odsouhlasení směn v obchodě pro pokročilé možnosti správy hotovosti. | [Hotovost](cash-mgmt.md) | |
| Finanční výkazy a odsouhlasení | Hotovostní a transakční transakce pro obchod se zaznamenávají v Commerce headquarters prostřednictvím procesů účtování výpisů. | [Výkazy](retail-statements.md) | |
| Transakce příjmů a výdajů | Zpracovávejte drobné hotovostní transakce v obchodě a zaznamenávejte příjmy, které nepřicházejí tradičním způsobem, jako jsou ztráty a nálezy, podíl na tržbách z kavárny ve vaší hale a služby čištění koberců. | [Výkazy](retail-statements.md) | |
| Proplacení faktury | Zachyťte platby na fakturách. | [Faktura](payinvoice.md) | |

## <a name="employee-productivity"></a>Produktivita zaměstnanců

| Schopnost | Popis | Dokumentace | Doplňkový obsah |
|---|---|---|---|
| Správa úkolů | Vytvářejte seznamy úkolů a úkoly a přiřazujte je obchodům a zaměstnancům. Sledujte stav úkolů napříč obchody. Bezproblémová integrace s Microsoft Teams je zajištěna. | <p>[Správa úkolů](task-mgmt-overview.md)</p><p>[Microsoft Teams](commerce-teams-integration.md)</p> | [Video](https://www.youtube.com/watch?v=ES1whB4C2lU) |

## <a name="hardware-and-peripherals"></a>Hardware a periferní zařízení

| Schopnost | Popis | Dokumentace | Doplňkový obsah |
|---|---|---|---|
| Připojení periferních zařízení | Připojte se k periferním zařízením, jako jsou tiskárny, pokladní zásuvky, skenery a platební zařízení k terminálu POS. | [Periferní zařízení](retail-peripherals-overview.md) ||
| Sdílená periferní zařízení | Tiskárny účtenek, pokladní zásuvky a platební zařízení lze sdílet mezi mnoha terminály jejich připojením ke sdílené hardwarové stanici. | <p>[Hardwarová stanice](retail-peripherals-overview.md) ||
| Simulátor POS a periferních zařízení | Simulátor periferních zařízení podporuje testování scénářů, které obvykle vyžadují fyzická periferní zařízení POS. Zahrnuje také simulátor POS, který umožňuje testování kompatibility fyzických periferních zařízení bez nutnosti nasazení klienta POS. | [Simulátor](dev-itpro/retail-peripheral-simulator.md) | |

## <a name="receipts"></a>Příjemky

| Schopnost | Popis | Dokumentace | Doplňkový obsah |
|---|---|---|---|
| Tisk účtenek | Účtenky různých typů, jako jsou prodejní stvrzenky, stvrzenky z kreditních karet, dárkové stvrzenky a faktury, lze tisknout standardně nebo po potvrzení pokladnou u pokladny. Lze je také přetisknout z deníku. | [Tisk](receipt-templates-printing.md) | |
| Účtenky e-mailem | Účtenky mohou být zaslány e-mailem z POS po dokončení pokladny. | [E-mail](email-receipts.md) | |
| Design účtenky | Účtenky z obchodu lze přizpůsobit tak, aby zobrazovaly data a rozložení vhodné pro prodejce a typ transakce. Účtenky lze také rozšířit tak, aby zobrazovaly vlastní údaje, které prodejce požaduje. | [Návrh](receipt-templates-printing.md) | |

## <a name="offline-support"></a>Offline podpora

| Schopnost | Popis | Dokumentace | Doplňkový obsah |
|---|---|---|---|
| Bezproblémové offline | Bezproblémové offline vám umožní pokračovat v transakcích, i když je připojení k internetu omezené nebo nedostupné. Vyloučení dat vám pomůže snížit velikost dat offline databází a maximalizovat výkon. | [Offline](pos-operations.md) | |
| Přepínání na základě výkonu | Při zjištění snížení výkonu přepněte do režimu offline. | [Offline](dev-itpro/implementation-considerations-offline.md) | [Video](https://youtu.be/sQU-2pgHToI) |
| Offline řídicí panel | Řídicí panel **Stav offline** zobrazuje offline stav, chyby a podrobnosti o datech pro každé zařízení. Proto je snadné spravovat stav mnoha zařízení. | [Offline](dev-itpro/implementation-considerations-offline.md) | [Video](https://youtu.be/sQU-2pgHToI)|

## <a name="extensibility"></a>Rozšiřitelnost

| Schopnost | Popis | Dokumentace | Doplňkový obsah |
|---|---|---|---|
| Commerce Headquarters | Řešení Commerce headquarters lze přizpůsobit přidáním nebo úpravou obchodních procesů. Commerce headquarters podporuje použití metadat a kódem řízený model rozšíření pro přidání vlastních funkcí. Lze jej snadno integrovat do externích řešení. | [Přehled](dev-itpro/extend-customer-cdx-package.md) | [Technické přednášky](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-unlock-the-power-of-dynamics-365-commerce-commerce-extensibility-overview-february-23-2021) |
| Bezobslužná aplikace Commerce | Rámec rozhraní Extensible Omni-channel API lze použít k přizpůsobení a přidání obchodní logiky. Rozhraní API, která mají obslužné nástroje požadavků a vzory rozšíření před spuštěním a po spuštění. | [CSU](dev-itpro/retail-server-customer-consumer-api.md) | [Technické přednášky](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| Sada Commerce SDK | Sada Commerce SDK obsahuje kód, ukázky kódu, šablony a nástroje, které jsou nutné k rozšíření nebo přizpůsobení funkčnosti Dynamics 365 Commerce. SDK je publikována v různých repozitářích (repo) na GitHub v závislosti na komponentách rozšíření. | [SDK](dev-itpro/retail-sdk/sdk-github.md) | [Technické přednášky](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| Pokladní místo | Aplikaci Store Commerce lze rozšířit nezávisle pomocí funkce rozšíření POS sady Commerce SDK. Rámec podporuje přizpůsobení uživatelského prostředí (UX), pracovních postupů a obchodní logiky. | [POS](dev-itpro/pos-extension/pos-extension-overview.md) | [Technické přednášky](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |

## <a name="reporting"></a>Vykazování

| Schopnost | Popis | Dokumentace | Doplňkový obsah |
|---|---|---|---|
| Prodejní sestavy | Vedoucí prodejen mají k dispozici zprávy o prodeji podle zaměstnanců, registru, typu platby, vráceného zboží, produktu atd. Manažeři mohou tyto zprávy prohlížet a používat je k přidělování provizí a identifikaci produktových trendů. | | |

## <a name="diagnostics"></a>Diagnostika

| Schopnost | Popis | Dokumentace | Doplňkový obsah |
|---|---|---|---|
| Operational Insights | Metriky spolehlivosti a výkonu služby spravované obchodem jsou dostupné u předplatného Application Insights zákazníka. K dispozici jsou pokročilé možnosti upozornění a monitorování. | | |
| Kontrola stavu | Dostupnost periferií připojených k POS lze ověřit spuštěním operace kontroly stavu. Jednotlivé periferní problémy pak lze opravit a ověřit. | [Kontrola stavu](pos-healthcheck.md) | [Video](https://www.youtube.com/watch?v=RfPDNmnqYvY) |

## <a name="globalization"></a>Globalizace

| Schopnost | Popis | Dokumentace | Doplňkový obsah |
|---|---|---|---|
| Podpora více trhů | Funkce specifické pro daný trh, jako je fiskální integrace, GST, pokročilá fakturace a platby předem, jsou podporovány ihned po instalaci. Tato schopnost pokrývá několik trhů v Evropě, Americe, Rusku, Asii, Saúdské Arábii a tak dále. | [Globalizace](localizations/fiscal-integration-for-retail-channel.md) | |

## <a name="compliance"></a>Dodržování předpisů

| Schopnost | Popis | Dokumentace | Doplňkový obsah |
|---|---|---|---|
| Standardy společnosti Microsoft | Aplikace Store Commerce splňuje standardy společnosti Microsoft pro zabezpečení, soukromí, dostupnost, obecné nařízení o ochraně osobních údajů (GDPR), datovou hranici Evropské unie (EU) atd. | | |

