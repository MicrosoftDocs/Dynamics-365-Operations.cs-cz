---
title: Poradce při potížích s modulem duálního zápisu v aplikacích Finance and Operations
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172753"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>Poradce při potížích s modulem duálního zápisu v aplikacích Finance and Operations

[!include [banner](../../includes/banner.md)]



Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Common Data Service. Konkrétně toto téma obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy s modulem **Dvojího zapisování** v aplikacích Finance and Operations.

> [!IMPORTANT]
> Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD). Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>V aplikaci Finance and Operations nelze načíst modul dvojího napisování

Pokud nemůžete otevřít stránku **Dvojího zapisování** výběrem dlaždice **Dvojího zapisování** v pracovním prostoru **Správa dat**, služba integrace dat je pravděpodobně mimo provoz. Vytvořte lístek podpory pro vyžádání restartu služby Data Integration Service.

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a>Chyba při pokusu o vytvoření nového mapování entity

**Požadovaná pověření pro opravu problému:** Správce klienta Azure AD

Při pokusu o konfiguraci nové entity pro dvojího psaní se může zobrazit následující chybová zpráva:

*Stavový kód odpovědi neoznačuje úspěch: 401 (Neautorizováno)*

K této chybě dochází, protože pouze správce klenta Azure AD může přidat nové mapování entit.

Chcete-li tento problém vyřešit, přihlaste se k aplikaci Finance and Operations jako správce klienta Azure AD. Je také nutné přejít na web.PowerApps.com a znovu ověřit připojení.

## <a name="error-when-you-open-the-dual-write-user-interface"></a>Chyba při otevření uživatelského rozhraní s dvojím zapisováním

Při pokusu o přístup dvojího zápisu z pracovního prostoru **Správa dat** se může zobrazit následující chybová zpráva:

*login.microsoftonline.com se odmítlo připojit.*

Chcete-li tento problém vyřešit, přihlaste se pomocí okna InPrivate v aplikaci Microsoft Edge, anonymního okna v Chromium nebo anonymního okna v Google Chrome. Je také nutné zrušit blokování nebo vymazat soubory cookie třetích stran.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a>Chyba při propojení prostředí pro dvojí zapisování nebo přidání nového mapování entit

**Požadovaná pověření pro opravu problému:** Správce klienta Azure AD

Při připojování nebo vytváření map se může objevit následující chyba:

*Stavový kód odpovědi neoznačuje úspěch: 403 (tokenexchange).<br> ID relace: \<ID vaší relace\><br> ID kořenové aktivity: \<ID vaší kořenové aktivity\>*

K této chybě může dojít, pokud nemáte dostatečná oprávnění k propojení s dvojím zápisem nebo vytvářením map. Chcete-li propojit prostředí a přidat nová mapování entit, je nutné použít účet správce klienta Azure AD. Po instalaci však můžete pomocí účtu, který není účet správce, sledovat stav a upravit mapování.

## <a name="error-when-you-stop-the-entity-mapping"></a>Chyba při zastavení mapování entit

Při pokusu o zastavení mapování entit se může zobrazit následující chybová zpráva:

*\[Zakázáno\], \[{"stav": 403, "zdroj":","zpráva":"Chyba z výměny klienta: Uživatel nemá přístup k připojení dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], vzdálený server vrátil chybu: (403) Zakázáno.*

K této chybě dojde, pokud propojené prostředí Common Data Service není k dispozici.

Chcete-li tento problém vyřešit, vytvořte lístek pro tým pro integraci dat. Připojte sledování sítě, aby mohl tým pro integraci dat označit mapy jako **nespuštěný** na back endu.
