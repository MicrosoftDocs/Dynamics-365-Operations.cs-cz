---
title: Řešení potíží s modulem duálního zápisu v aplikacích Finance and Operations
description: Toto téma obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy s modulem dvojího zapisování v aplikacích Finance and Operations.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9bff8ad0c5716648dec6eadfb21412a2b17f155e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561219"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a>Řešení potíží s modulem duálního zápisu v aplikacích Finance and Operations

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Dataverse. Konkrétně toto téma obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy s modulem **Dvojího zapisování** v aplikacích Finance and Operations.

> [!IMPORTANT]
> Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD). Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>V aplikaci Finance and Operations nelze načíst modul dvojitého zápisu

Pokud nemůžete otevřít stránku **Dvojího zapisování** výběrem dlaždice **Dvojího zapisování** v pracovním prostoru **Správa dat**, služba integrace dat je pravděpodobně mimo provoz. Vytvořte lístek podpory pro vyžádání restartu služby Data Integration Service.

## <a name="error-when-you-try-to-create-a-new-table-map"></a>Chyba při pokusu o vytvoření nového mapování tabulky

**Požadovaná pověření pro opravu problému:** Stejný uživatel, který má nastaven dvojitý zápis.

Při pokusu o konfiguraci nové tabulky pro dvojitého zápisu se může zobrazit následující chybová zpráva. Jediným uživatelem, který může vytvořit mapu, je uživatel, který má nastaveno připojení s dvojitým zápisem.

*Stavový kód odpovědi neoznačuje úspěch: 401 (Neautorizováno)*


## <a name="error-when-you-open-the-dual-write-user-interface"></a>Chyba při otevření uživatelského rozhraní s dvojím zapisováním

Při pokusu o přístup dvojího zápisu z pracovního prostoru **Správa dat** se může zobrazit následující chybová zpráva:

*login.microsoftonline.com se odmítlo připojit.*

Chcete-li tento problém vyřešit, přihlaste se pomocí okna InPrivate v aplikaci Microsoft Edge, anonymního okna v Chromium nebo anonymního okna v Google Chrome. Je také nutné zrušit blokování nebo vymazat soubory cookie třetích stran.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>Chyba při propojení prostředí pro dvojí zapisování nebo přidání nového mapování tabulky

**Požadovaná role pro opravu problému:** Správce systému v obou aplikacích Finance and Operations a Dataverse.

Při připojování nebo vytváření map se může objevit následující chyba:

*Stavový kód odpovědi neoznačuje úspěch: 403 (tokenexchange).<br> ID relace: \<your session id\><br> ID kořenové aktivity: \<your root activity id\>*

K této chybě může dojít, pokud nemáte dostatečná oprávnění k propojení s dvojím zápisem nebo vytvářením map. K této chybě může také dojít, pokud prostředí Dataverse bylo resetováno bez zrušení propojení dvojitého zápisu. Libovolný uživatel s rolí správce systému v aplikacích Finance and Operations a prostředí Dataverse může obě prostředí propojit. Přidávat nové mapy tabulky může pouze uživatel, který nastavuje připojení s dvojitým zápisem. Po dokončení nastavení může libovolný uživatel s rolí správce systému sledovat stav a upravit mapování.

## <a name="error-when-you-stop-the-table-mapping"></a>Chyba při zastavení mapování tabulky

Při pokusu o zastavení mapování tabulky se může zobrazit následující chybová zpráva:

*\[Zakázáno\], \[{"stav": 403, "zdroj":","zpráva":"Chyba z výměny klienta: Uživatel nemá přístup k připojení dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], vzdálený server vrátil chybu: (403) Zakázáno.*

K této chybě dojde, pokud propojené prostředí Dataverse není k dispozici.

Chcete-li tento problém vyřešit, vytvořte lístek pro tým pro integraci dat. Připojte sledování sítě, aby mohl tým pro integraci dat označit mapy jako **nespuštěný** na back endu.

## <a name="error-while-trying-to-start-a-table-mapping"></a>Chyba při pokusu o spuštění mapování tabulky

Při pokusu o nastavení tohoto stavu mapování na **Spuštěno** se může zobrazit chybová zpráva podobná následující:

*Nelze dokončit počáteční synchronizaci dat. Chyba: selhání dvojitého zápisu – registrace modulu plug-in se nezdařila: nelze vytvořit metadata vyhledávání dvojitého zápisu. Odkaz na objekt chyby není nastaven na instanci objektu.*

Oprava této chyby závisí na příčině chyby:

+ Pokud mapování obsahuje závislá mapování, ujistěte se, že je povoleno mapování závislých položek tohoto mapování tabulky.
+ Mapování pravděpodobně neobsahuje zdrojové nebo cílové sloupce. Pokud ve sloupci v aplikaci Finance and Operations chybí pole, postupujte podle kroků v oddílu [Problém chybějících sloupců tabulky při mapování](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps). Pokud v prostředí Dataverse chybí sloupec, klikněte na tlačítko **Aktualizovat tabulky** u mapování, aby byly sloupce automaticky vloženy zpět do mapování.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]