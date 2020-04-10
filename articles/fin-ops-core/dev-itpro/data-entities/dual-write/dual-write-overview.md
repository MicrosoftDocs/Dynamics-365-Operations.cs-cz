---
title: Přehled dvojího zapisování
description: Toto téma obsahuje přehled dvojího zapisování. Dvojí zapisování je infrastruktura poskytující prakticky v reálném čase mezi aplikacemi řízených modelem Microsoft Dynamics 365 a Finance and Operations.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 64626ebdd7fbad3d47a4b4c6bbc45bf3bc0c8277
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172777"
---
# <a name="dual-write-overview"></a>Přehled dvojího zapisování

[!include [banner](../../includes/banner.md)]



## <a name="what-is-dual-write"></a>Co je dvojí zapisování?

Dvojí zapisování je předpřipravená infrastruktura poskytující prakticky v reálném čase mezi aplikacemi řízených modelem v Microsoft Dynamics 365 a Finance and Operations. Při zpracování dat o zákaznících, produktech, osobách a operacích mimo hranice aplikací jsou všechna oddělení v organizaci oprávněna.

Dvojí zapisování poskytuje pevně spojenou obousměrnou integraci mezi aplikacemi Finance and Operations a Common Data Service. Jakákoli změna dat v aplikacích Finance and Operations způsobí zápis do aplikace Common Data Service a jakákoli změna dat v Common Data Service způsobí zápis do aplikací Finance and Operations. Tento automatizovaný tok dat poskytuje integrované uživatelské prostředí pro celé aplikace.

![Datový vztah mezi aplikacemi](media/dual-write-overview.jpg)

Dvojí zápis má dva aspekty: aspekt *infrastruktury* a aspekt *aplikace*.

### <a name="infrastructure"></a>Infrastruktura

Infrastruktura dvojího zapisování je rozšiřitelná a spolehlivá a obsahuje následující klíčové funkce:

+ Synchronní a obousměrný tok dat mezi aplikacemi
+ Synchronizace spolu s režimy přehrát, pozastavit a catchup pro podporu systému při režimech online a offline/asynchronní.
+ Možnost synchronizace počátečních dat mezi aplikacemi
+ Konsolidované zobrazení protokolů aktivit a chyb pro správce dat
+ Možnost konfigurovat vlastní výstrahy a prahové hodnoty a přihlásit se k odběru oznámení
+ Intuitivní uživatelské rozhraní (UI) pro filtrování a transformace
+ Schopnost nastavit a zobrazit závislosti a vztahy entity
+ Rozšiřitelnost pro standardní i pro vlastní entity a mapy
+ Spolehlivé řízení životního cyklu aplikací
+ Přednastavené možnosti nastavení pro nové odběratele

### <a name="application"></a>Přihláška

Dvojí zapisování vytvoří mapování mezi koncepty v aplikacích Finance and Operations a koncepty v aplikacích řízených modelem v Dynamics 365. Tato integrace podporuje následující scénáře:

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

+ Dvojí zapisování poskytuje úzce spojenou, prakticky v reálném čase a obousměrnou integraci mezi aplikacemi Finance and Operations a aplikacemi řízenými modelem v aplikaci Dynamics 365. Tato integrace činí z Microsoft Dynamics 365 univerzální nástroj pro všechna vaše obchodní řešení. Zákazníci, kteří používají Dynamics 365 Finance a Dynamics 365 Supply Chain Management, ale používají řešení pro řízení vztahů se zákazníky (CRM) jiného typu než nabízí společnost Microsoft, přecházení k Dynamics 365 díky podpoře dvojího zapisování.
+ Data od odběratelů, produktů, operací, projektů a Internetu věcí (IoT) automaticky proudí do Common Data Service pomocí dvojího zapisování. Toto připojení je velmi užitečné pro podniky, které se zajímaní o rozšíření Microsoft Power Platform.
+ Infrastruktura dvojího zapisování se řídí podle principu "bez kódu/nízký kód". Chcete-li rozšířit standardní mapy tabulek a tabulek a zahrnout vlastní mapy, je nezbytné pouze minimální úsilí.
+ Dvojí zapisování podporuje režim online i režim offline. Společnost Microsoft je jediná společnost nabízející podporu pro režimy online a offline.

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a>Co znamená dvojí zapisování pro uživatele a architekty produktů CRM?

Dvojí zapisování automatizuje tok dat mezi aplikacemi Finance and Operations a Common Data Service. V budoucích verzích budou pojmy v aplikacích řízených modelem v aplikaci Dynamics 365 (například odběratel, kontakt, nabídka a objednávka) odstupňovány pro zákazníky se středním podílem na trhu a s vyšším podílem na trhu.

V prvním vydání je většina automatizace zpracována řešeními dvojího zápisu. V příštích verzích se tyto řešení stanou součástí aplikace Common Data Service. Pochopíte-li nadcházející změny v aplikaci Common Data Service, můžete v dlouhodobém období ušetřit úsilí. Následují některé zásadní změny:

+ Common Data Service bude mít nové koncepce, jako je například společnost nebo smluvní strana. Tyto koncepce budou mít vliv na všechny aplikace vytvořené na Common Data Service, například Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service a Dynamics 365 Field Service.
+ Aktivity a poznámky jsou sjednoceny a rozšířeny tak, aby podporovaly C1 (uživatelé systému) i C2 (zákazníci v systému).
+ Následují některé nadcházející změny v Common Data Service:

    - Datový typ desetinné číslo nahradí datový typ peníze.
    - Datum vyčerpání bude podporovat minulá, současná a budoucí data na stejném místě.
    - Pro měnu a směnné kurzy bude existovat více podpor a bude revidováno rozhraní (API) pro aplikaci **Směnný kurz**.
    - Převody jednotek budou podporovány.

Další informace o nadcházejících změnách naleznete v tématu [Data v Common Data Service - fáze 1 a 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1).
