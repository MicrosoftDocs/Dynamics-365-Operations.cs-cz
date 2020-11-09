---
title: Poradce při potížích s modulem dvojitého zápisu v aplikacích Finance and Operations
description: Toto téma obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy s modulem dvojího zapisování v aplikacích Finance and Operations.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f99f3760e75ec1bbf2ccdea497cf2eec3e28e233
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997367"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>Poradce při potížích s modulem dvojitého zápisu v aplikacích Finance and Operations

[!include [banner](../../includes/banner.md)]

Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Common Data Service. Konkrétně toto téma obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy s modulem **Dvojího zapisování** v aplikacích Finance and Operations.

> [!IMPORTANT]
> Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD). Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>V aplikaci Finance and Operations nelze načíst modul dvojitého zápisu

Pokud nemůžete otevřít stránku **Dvojího zapisování** výběrem dlaždice **Dvojího zapisování** v pracovním prostoru **Správa dat** , služba integrace dat je pravděpodobně mimo provoz. Vytvořte lístek podpory pro vyžádání restartu služby Data Integration Service.

## <a name="error-when-you-try-to-create-a-new-entity-map"></a>Chyba při pokusu o vytvoření nového mapování entity

**Požadovaná pověření pro opravu problému:** Stejný uživatel, který má nastaven dvojitý zápis.

Při pokusu o konfiguraci nové entity pro dvojitého zápisu se může zobrazit následující chybová zpráva. Jediným uživatelem, který může vytvořit mapu, je uživatel, který má nastaveno připojení s dvojitým zápisem.

*Stavový kód odpovědi neoznačuje úspěch: 401 (Neautorizováno)*


## <a name="error-when-you-open-the-dual-write-user-interface"></a>Chyba při otevření uživatelského rozhraní s dvojím zapisováním

Při pokusu o přístup dvojího zápisu z pracovního prostoru **Správa dat** se může zobrazit následující chybová zpráva:

*login.microsoftonline.com se odmítlo připojit.*

Chcete-li tento problém vyřešit, přihlaste se pomocí okna InPrivate v aplikaci Microsoft Edge, anonymního okna v Chromium nebo anonymního okna v Google Chrome. Je také nutné zrušit blokování nebo vymazat soubory cookie třetích stran.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a>Chyba při propojení prostředí pro dvojí zapisování nebo přidání nového mapování entit

**Požadovaná role pro opravu problému:** Správce systému v obou aplikacích Finance and Operations a Common Data Service.

Při připojování nebo vytváření map se může objevit následující chyba:

*Stavový kód odpovědi neoznačuje úspěch: 403 (tokenexchange).<br> ID relace: \<your session id\><br> ID kořenové aktivity: \<your root activity id\>*

K této chybě může dojít, pokud nemáte dostatečná oprávnění k propojení s dvojím zápisem nebo vytvářením map. K této chybě může také dojít, pokud prostředí Common Data Service bylo resetováno bez zrušení propojení dvojitého zápisu. Libovolný uživatel s rolí správce systému v aplikacích Finance and Operations a prostředí Common Data Service může obě prostředí propojit. Přidávat nové mapy entit může pouze uživatel, který nastavuje připojení s dvojitým zápisem. Po dokončení nastavení může libovolný uživatel s rolí správce systému sledovat stav a upravit mapování.

## <a name="error-when-you-stop-the-entity-mapping"></a>Chyba při zastavení mapování entit

Při pokusu o zastavení mapování entit se může zobrazit následující chybová zpráva:

*\[Zakázáno\], \[{"stav": 403, "zdroj":","zpráva":"Chyba z výměny klienta: Uživatel nemá přístup k připojení dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], vzdálený server vrátil chybu: (403) Zakázáno.*

K této chybě dojde, pokud propojené prostředí Common Data Service není k dispozici.

Chcete-li tento problém vyřešit, vytvořte lístek pro tým pro integraci dat. Připojte sledování sítě, aby mohl tým pro integraci dat označit mapy jako **nespuštěný** na back endu.

## <a name="error-while-trying-to-start-an-entity-mapping"></a>Chyba při pokusu o spuštění mapování entit

Při pokusu o nastavení tohoto stavu mapování na **Spuštěno** se může zobrazit chybová zpráva podobná následující:

*Nelze dokončit počáteční synchronizaci dat. Chyba: selhání dvojitého zápisu – registrace modulu plug-in se nezdařila: nelze vytvořit metadata vyhledávání dvojitého zápisu. Odkaz na objekt chyby není nastaven na instanci objektu.*

Oprava této chyby závisí na příčině chyby:

+ Pokud mapování obsahuje závislá mapování, ujistěte se, že je povoleno mapování závislých položek tohoto mapování entit.
+ Mapování pravděpodobně neobsahuje zdrojová nebo cílová pole. Pokud v aplikaci Finance and Operations chybí pole, postupujte podle kroků v oddílu [Problém chybějících polí entity při mapování](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps). Pokud v prostředí Common Data Service chybí pole, klikněte na tlačítko **Aktualizovat entity** na mapování, aby byla pole automaticky vložena zpět do mapování.
