---
title: Přehled dvojitého zápisu
description: Toto téma poskytuje přehled dvojího zapisování, které poskytuje interakci prakticky v reálném čase mezi aplikacemi Customer Engagement a aplikacemi Finance and Operations.
author: RamaKrishnamoorthy
ms.date: 02/06/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.custom: intro-internal
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 69abd2b6d4026ef1b5b85d52c561bb060cf82123
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781457"
---
# <a name="dual-write-overview"></a>Přehled dvojitého zápisu

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="what-is-dual-write"></a>Co je dvojí zapisování?

Dvojí zapisování je předpřipravená infrastruktura poskytující prakticky v reálném čase mezi aplikacemi pro zapojení zákazníků a aplikacemi Finance and Operations. Při zpracování dat o zákaznících, produktech, osobách a operacích mimo hranice aplikací jsou všechna oddělení v organizaci oprávněna.

Dvojí zapisování poskytuje pevně spojenou obousměrnou integraci mezi aplikacemi Finance and Operations a Dataverse. Jakákoli změna dat v aplikacích Finance and Operations způsobí zápis do aplikace Dataverse a jakákoli změna dat v Dataverse způsobí zápis do aplikací Finance and Operations. Tento automatizovaný tok dat poskytuje integrované uživatelské prostředí pro celé aplikace.

![Datový vztah mezi aplikacemi.](media/dual-write-overview.jpg)

Dvojí zápis má dva aspekty: aspekt *infrastruktury* a aspekt *aplikace*.

### <a name="infrastructure"></a>Infrastruktura

Infrastruktura dvojího zapisování je rozšiřitelná a spolehlivá a obsahuje následující klíčové funkce:

+ Synchronní a obousměrný tok dat mezi aplikacemi
+ Synchronizace spolu s režimy přehrát, pozastavit a catchup pro podporu systému při režimech online a offline/asynchronní.
+ Možnost synchronizace počátečních dat mezi aplikacemi
+ Kombinované zobrazení protokolů aktivit a chyb pro správce dat
+ Možnost konfigurovat vlastní výstrahy a prahové hodnoty a přihlásit se k odběru oznámení
+ Intuitivní uživatelské rozhraní (UI) pro filtrování a transformace
+ Schopnost nastavit a zobrazit závislosti a vztahy tabulky
+ Rozšiřitelnost pro standardní i pro vlastní tabulky a mapy
+ Spolehlivé řízení životního cyklu aplikací
+ Přednastavené možnosti nastavení pro nové odběratele

### <a name="application"></a>Přihláška

Duální zápis vytvoří mapování mezi koncepty v aplikacích Finance and Operations a koncepty v aplikacích pro zapojení zákazníků. Tato integrace podporuje následující scénáře:

+ Integrovaná hlavní data odběratelů
+ Přístup k věrnostním kartám odběratelů a k bodům odměny
+ Sjednocené prostředí základního produktu
+ Povědomí o organizační hierarchii
+ Integrovaná hlavní data dodavatelů
+ Přístup k referenčním datům financování a daně
+ Práce modulu ceny na požádání
+ Integrované prostředí zpeněžení
+ Schopnost poskytovat interní majetek i aktiva pro odběratele prostřednictvím agentů polí
+ Integrované prostředí vynucení platby
+ Integrované aktivity a poznámky pro data a dokumenty odběratelů
+ Možnost vyhledat dostupnost a podrobnosti zásob na skladě
+ Prostředí P2C
+ Schopnost zpracovávat více adres a rolí prostřednictvím koncepce strany
+ Správa jednoho zdroje pro uživatele
+ Integrované kanály pro maloobchod a marketing
+ Zviditelnění promoakcí a slev
+ Funkce požadavku na služby
+ Zjednodušené servisní operace

## <a name="top-reasons-to-use-dual-write"></a>Hlavní důvody pro použití dvojího zapisování

Dvojí zapisování poskytuje integraci dat mezi aplikacemi Microsoft Dynamics 365. Toto robustní rozhraní spojuje prostředí a umožňuje různým obchodním aplikacím vzájemnou spolupráci. Zde jsou uvedeny hlavní důvody, proč byste měli používat dvojí zápis:

+ Dvojí zapisování poskytuje úzce spojenou, prakticky v reálném čase a obousměrnou integraci mezi aplikacemi finance and operations a aplikacemi customer engagement. Tato integrace činí z Microsoft Dynamics 365 univerzální nástroj pro všechna vaše obchodní řešení. Zákazníci, kteří používají Dynamics 365 Finance a Dynamics 365 Supply Chain Management, ale používají řešení pro řízení vztahů se zákazníky (CRM) jiného typu než nabízí společnost Microsoft, přecházení k Dynamics 365 díky podpoře dvojího zapisování.
+ Data od odběratelů, produktů, operací, projektů a Internetu věcí (IoT) automaticky proudí do Dataverse pomocí dvojího zapisování. Toto připojení je užitečné pro podniky, které se zajímaní o rozšíření Power Platform.
+ Infrastruktura dvojího zapisování se řídí podle principu "bez kódu/nízký kód". Chcete-li rozšířit standardní mapy tabulek a tabulek a zahrnout vlastní mapy, je nezbytné pouze minimální úsilí.
+ Dvojí zapisování podporuje režim online i režim offline. Společnost Microsoft je jediná společnost nabízející podporu pro režimy online a offline.

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a>Co znamená duální zápis pro vývojáře a architekty aplikací pro zapojení zákazníků?

Duální zápis automatizuje tok dat mezi aplikacemi Finance and Operations a aplikacemi pro zapojení zákazníků. Duální zápis se skládá ze dvou řešení AppSource, která jsou nainstalována na Dataverse. Tato řešení rozšiřují schéma tabulky, moduly plugin a pracovní postupy v Dataverse, aby mohly škálovat na velikost ERP. Pro úspěšnou implementaci musí vývojáři a architekti aplikací pro zapojení zákazníků tyto změny pochopit a spolupracovat se svými protějšky v aplikacích Finance and Operations.

Kvůli vytvoření parity s aplikacemi Finance and Operations provádí duální zápis některé zásadní změny ve schématu Dataverse. Pokud plánu rozumíte, můžete se v budoucnu vyhnout úpravám návrhu a vývoje.

+ Když je instalován balíček duálního zápisu AppSource, Dataverse bude mít nové koncety, jako je společnost nebo zainteresovaná strana. Tyto koncepty pomáhají aplikacím postaveným na Dataverse, včetně Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service a Dynamics 365 Field Service, bezproblémově komunikovat s aplikacemi Finance and Operations.

+ Aktivity a poznámky jsou sjednoceny a rozšířeny tak, aby podporovaly C1 (uživatelé systému) i C2 (zákazníci v systému).

+ Aby se zabránilo ztrátě dat při přenosu měny mezi aplikacemi Finance and Operations a Dataverse, budete moci rozšířit počet desetinných míst v datovém typu měny aplikací pro zapojení zákazníků. Tato funkce automaticky přenese existující řádky do nového rozšířeného stavu ve vrstvě metadat. Během tohoto procesu je hodnota měny převedena na desítková data, nikoli na peněžní, a hodnota měny podporuje 10 desetinných míst. Pro tuto funkci je třeba se registrovat a organizace, které nepotřebují více než 4 desetinná místa přesnosti, se registrovat nemusí. Další informace viz [Migrace datového typu měny pro duální zápis](currrency-decimal-places.md).

+ [Platnost od](../../dev-tools/date-effectivity.md) bude přidán do Dataverse. Bude podporovat minulá, současná a budoucí data ve stejné tabulce.

+ [Převody jednotek](../../../../supply-chain/pim/tasks/manage-unit-measure.md) produktu jsou podporovány pro produkty, nabídky, objednávky a faktury.

Další informace o nadcházejících změnách najdete v části [Co je nového nebo co se změnilo ohledně duálního zápisu](whats-new-dual-write.md).



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]