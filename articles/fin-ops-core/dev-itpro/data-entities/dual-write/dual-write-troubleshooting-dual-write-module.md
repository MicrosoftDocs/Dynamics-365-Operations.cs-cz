---
title: Řešení problémů s duálním zápisem ve finančních a provozních aplikacích
description: Tento článek obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy s modulem dvojího zapisování ve finančních a provozních aplikacích.
author: RamaKrishnamoorthy
ms.date: 04/18/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2743b99538b332af7cc6ad8d951eede562c14235
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111163"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a>Řešení problémů s duálním zápisem ve finančních a provozních aplikacích

[!include [banner](../../includes/banner.md)]



Tento článek obsahuje informace o odstraňování potíží pro integrací dvojitého zápisu mezi finančními a provozními aplikacemi a Dataverse. Konkrétně toto téma obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy s modulem **Dvojího zapisování** v finančních a provozních aplikacích.

> [!IMPORTANT]
> Některé problémy, které tento článek řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD). Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Ve finanční a provozní aplikaci nelze modul dvojího zápisu načíst

Pokud nemůžete otevřít stránku **Dvojího zapisování** výběrem dlaždice **Dvojího zapisování** v pracovním prostoru **Správa dat**, služba integrace dat je pravděpodobně mimo provoz. Vytvořte lístek podpory pro vyžádání restartu služby Data Integration Service.

## <a name="error-when-you-try-to-create-a-new-table-map"></a>Chyba při pokusu o vytvoření nového mapování tabulky

**Požadovaná pověření pro opravu problému:** Stejný uživatel, který má nastaven dvojitý zápis.

Při pokusu o konfiguraci nové tabulky pro dvojitého zápisu se může zobrazit následující chybová zpráva. Jediným uživatelem, který může vytvořit mapu, je uživatel, který má nastaveno připojení s dvojitým zápisem.

*Stavový kód odpovědi neoznačuje úspěch: 401 (Neautorizováno).*

## <a name="error-when-you-open-the-dual-write-user-interface"></a>Chyba při otevření uživatelského rozhraní s dvojím zapisováním

Při pokusu o přístup dvojího zápisu z pracovního prostoru **Správa dat** se může zobrazit následující chybová zpráva:

*login.microsoftonline.com se odmítlo připojit.*

Chcete-li tento problém vyřešit, přihlaste se pomocí okna InPrivate v aplikaci Microsoft Edge, anonymního okna v Chromium nebo anonymního okna v Google Chrome. Je také nutné zrušit blokování nebo vymazat soubory cookie třetích stran.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>Chyba při propojení prostředí pro dvojí zapisování nebo přidání nového mapování tabulky

**Požadovaná role pro opravu problému**: Správce systému v finančních a provozních aplikacích i prostředí Dataverse.

Při připojování nebo vytváření map se může objevit následující chyba:

```dos
Response status code does not indicate success: 403 (tokenexchange).
Session ID: \<your session id\>
Root activity ID: \<your root activity\> id
```

K této chybě může dojít, pokud nemáte dostatečná oprávnění k propojení s dvojím zápisem nebo vytvářením map. K této chybě může také dojít, pokud prostředí Dataverse bylo resetováno bez zrušení propojení dvojitého zápisu. Libovolný uživatel s rolí správce systému v finančních a provozních aplikacích a prostředí Dataverse může obě prostředí propojit. Přidávat nové mapy tabulky může pouze uživatel, který nastavuje připojení s dvojitým zápisem. Po dokončení nastavení může libovolný uživatel s rolí správce systému sledovat stav a upravit mapování.

## <a name="error-when-you-stop-the-table-mapping"></a>Chyba při zastavení mapování tabulky

Při pokusu o zastavení mapování tabulky se může zobrazit následující chybová zpráva:

*\[Zakázáno\], \[{"stav": 403, "zdroj":","zpráva":"Chyba z výměny klienta: Uživatel nemá přístup k připojení dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], vzdálený server vrátil chybu: (403) Zakázáno.*

K této chybě dojde, pokud propojené prostředí Dataverse není k dispozici.

Chcete-li tento problém vyřešit, vytvořte lístek pro tým pro integraci dat. Připojte sledování sítě, aby mohl tým pro integraci dat označit mapy jako **nespuštěný** na back endu.

## <a name="enable-parallel-processing-in-finance-and-operations-apps-to-improve-performance"></a>Povolte paralelní zpracování ve finančních a provozních aplikacích pro zlepšení výkonu

Povolení paralelního zpracování může zkrátit čas potřebný k importu dat z aplikací Dynamics 365 pro zapojení zákazníků a Microsoft Dataverse do finančních a provozních aplikací. 

Chcete-li povolit paralelní zpracování ve finančních a provozních aplikacích, postupujte následujícím způsobem.

1. Přihlaste se do svého prostředí finančních a provozních aplikací.
2. Přejděte na **Správa dat > Parametry rámce**.
3. Vyberte **Nastavení entity** a vyberte **Konfigurace parametrů provádění entity**.
4. Přidejte parametry pro paralelní zpracování:
    - **Počet záznamů prahu importu** – Počet záznamů, které musí být splněny, než bude povoleno paralelní zpracování.
    - **Počet importu úkolů** – Počet vláken (úloh), které se mají spustit paralelně.
5. Zvolte možnost **Uložit**.


## <a name="errors-while-trying-to-start-a-table-mapping"></a>Chyby při pokusu o spuštění mapování tabulky

### <a name="unable-to-complete-initial-data-sync"></a>Počáteční synchronizaci dat nelze dokončit

Při pokusu o spuštění počáteční synchronizace dat se může zobrazit následující chybová zpráva:

*Nelze dokončit počáteční synchronizaci dat. Chyba: selhání dvojitého zápisu – registrace modulu plug-in se nezdařila: nelze vytvořit metadata vyhledávání dvojitého zápisu. Odkaz na objekt chyby není nastaven na instanci objektu.*

Při pokusu o nastavení tohoto stavu mapování na **Spuštěno** se může zobrazit tato chybová zpráva. Oprava závisí na příčině chyby:

+ Pokud mapování obsahuje závislá mapování, ujistěte se, že je povoleno mapování závislých položek tohoto mapování tabulky.
+ Mapování pravděpodobně neobsahuje zdrojové nebo cílové sloupce. Pokud ve sloupci ve finanční a provozní aplikaci chybí pole, postupujte podle kroků v oddílu [Problém chybějících sloupců tabulky při mapování](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps). Pokud v prostředí Dataverse chybí sloupec, klikněte na tlačítko **Aktualizovat tabulky** u mapování, aby byly sloupce automaticky vloženy zpět do mapování.

### <a name="version-mismatch-error-and-upgrading-dual-write-solutions"></a>Chyba nesouladu verzí a inovace řešení pro dvojí zápis

Při pokusu o zastavení mapování tabulky se mohou zobrazit následující chybové zprávy:

+ *Skupiny zákazníků (msdyn_customergroups): Selhání duálního zápisu - řešení Dynamics 365 for Sales „Dynamics365Company“ má nesoulad verzí. Verze: '2.0.2.10' Požadovaná verze: '2.0.133'*
+ *Řešení Dynamics 365 for Sales „Dynamics365FinanceExtended“ má nesoulad verzí. Verze: '1.0.0.0' Požadovaná verze: '2.0.227'*
+ *Řešení Dynamics 365 for Sales „Dynamics365FinanceAndOperationsCommon“ má nesoulad verzí. Verze: '1.0.0.0' Požadovaná verze: '2.0.133'*
+ *Řešení Dynamics 365 for Sales „CurrencyExchangeRates“ má nesoulad verzí. Verze: '1.0.0.0' Požadovaná verze: '2.0.133'*
+ *Řešení Dynamics 365 for Sales „Dynamics365SupplyChainExtended“ má nesoulad verzí. Verze: '1.0.0.0' Požadovaná verze: '2.0.227'*

Chcete-li problémy vyřešit, aktualizujte řešení dvojitého zápisu v Dataverse. Nezapomeňte upgradovat na nejnovější řešení, které odpovídá požadované verzi řešení.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

