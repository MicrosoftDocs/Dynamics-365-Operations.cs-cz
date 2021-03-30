---
title: Správa leasingů prostřednictvím rámce importu leasingu
description: Toto téma vysvětluje, jak pomocí rámce importu leasingu upravit více leasingů najednou.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 90727e8624c8edb7cd9458089dd9d6dfaad67a7f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207224"
---
# <a name="manage-leases-through-the-lease-import-framework"></a>Správa leasingů prostřednictvím rámce importu leasingu

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak pomocí rámce importu leasingu upravit více leasingů v jednom kroku. Pomocí této funkce můžete ušetřit čas a můžete také zajistit přesnější úpravy snížením pravděpodobnosti lidské chyby. Tato funkce navíc může propojit Microsoft Dynamics 365 Finance s externími datovými entitami pro efektivní odesílání dat.

K integraci leasingu majektu s externími systémy lze použít následující datové entity:

- Pracovní leasing
- Pracovní platební smlouva
- Pracovní smlouva o zachraňovacích nákladech

Proces importu můžete použít k úpravě leasingu, aktualizaci nefinančních informací nebo přidání nových leasingů. Před importem si můžete data leasingu prohlédnout a upravit.

Systém může spustit následující tři procesy prostřednictvím sady pro import leasingu.

| Typ procesu  | popis |
|---------------|-------------|
| Přidat záznam    | Migrované leasingy, které mají tento typ procesu, vytvoří leasing v systému. Časový plán splátek musí být potvrzen ručně a po migraci musí být ručně zaúčtován záznam deníku počátečního uznání. |
| Aktualizovat záznam | Migrované leasingy, které mají tento typ procesu, aktualizují hodnoty pole pro leasing, který je již v systému. Pouze pole, která byla vybrána na stránce **Aktualizovat výběr polí** jsou aktualizována. Doporučili jsme vám vybrat nefinanční pole na stránce **Aktualizovat výběr polí**, protože tento typ procesu neupravuje leasing. |
| Upravit záznam | Migrované leasingy, které mají tento typ procesu, upravují leasing. Tato úprava způsobí změnu finančního leasingu. Po zpracování leasingu systém vytvoří nový plán splátek pomocí nových dat ze sady pro import leasingu. Systém nepotvrzuje plán splátek ani nezaúčtuje záznam deníku úprav. |

Po odeslání informací prostřednictvím pracovního prostoru **Správa dat** otevřete stránku **Importovat záhlaví** (**Leasing majetku \> Rámec importu leasingu \> Importovat záhlaví**). Tato stránka obsahuje seznam všech importů tří datových entit, které byly uvedeny dříve.

Chcete-li před spuštěním zpracování zobrazit data fázování leasingu, vyberte **Data fázování**.

Funkce porovnání umožňuje porovnat záznam, který importujete, s odpovídajícím záznamem, který je již ve vašem systému. Chcete-li porovnat jednotlivý záznam leasingu, vyberte leasing a poté vyberte **Porovnat**. Tento krok byste měli provést a vygenerovat tak sestavu **Rozdíly** před migrací záznamů o leasingu. Funkce Porovnat porovnává hodnoty ve datech fázování s hodnotami pro leasing, která jsou aktuálně v systému.

> [!NOTE]
> Funkce porovnání nefunguje u leasingů, které mají typ zpracování **Přidat záznam**, protože proti tomuto leasingu není co porovnávat.
>
> Chcete-li porovnat více leasingů najednou, přejděte na **Leasing majetku \> Rámec importu leasingu \> Periodické \> Porovnat** a vyberte **Porovnat**.

U každé entity si můžete prohlédnout rozdíly mezi tím, co je aktuálně v systému, a tím, co je v tabulkách fázování. Pro každou entitu v tabulkách fázování vyberte **Zobrazit rozdíly**. Zobrazí se dialogové okno, které zobrazuje aktuální hodnotu a navrhovanou hodnotu fázování.

Hodnotu fázování můžete také aktualizovat změnou v sloupci **Nová hodnota** a poté vybrat **Aktualizovat fázování**.

Můžete ověřit leasingy, abyste zajistili, že záznamy lze přenést do systému bez chyb. Před migrací záznamu o leasingu systém spustí několik ověření, aby bylo zajištěno, že bude záznam úspěšně importován. Chcete-li ověřit individuální leasing, vyberte **Ověřit**.

> [!NOTE]
> Chcete-li ověřit více leasingů najednou, přejděte na **Leasing majetku \> Rámec importu leasingu \> Periodické \> Ověřit** a vyberte **Porovnat**.

Chcete-li zpracovat individuální leasing, vyberte **Migrace záznamů o lesaingu** na stránce **Importovat záhlaví**. Při migraci leasingu provede systém akci uvedenou v poli **Typ zpracování**.

> [!NOTE]
> Chcete-li ověřit více leasingů najednou, přejděte na **Leasing majetku \> Rámec importu leasingu \> Periodické \> Ověřit** a vyberte **Porovnat**.

Po porovnání leasingu můžete spustit sestavu a zobrazit rozdíly pro každý leasing, který je zahrnut v ID importu. Chcete-li spustit sestavu pro jeden leasing, vyberte tento leasing v datech fázování a poté vyberte **Porovnat a zobrazit sestavu \> Sestava o rozdílech**.

> [!NOTE]
> Chcete-li ověřit více leasingů najednou, přejděte na **Leasing majetku \> Dotazy a sestavy \> Sestava rozdílů** a vyberte **Porovnat**.

## <a name="set-up-update-fields"></a>Nastavení polí aktualizací

Pokud používáte rámec importu leasingu k aktualizaci leasingu a typ zpracování je **Aktualizovat záznam**, můžete vybrat konkrétní pole k aktualizaci.

1. Přejděte na **Leasing majetku \> Rámec importu leasingu \> Nastavení \> Aktualizovat výběr pole**.
2. Na stránce, která se zobrazí, vyberte pole, která chcete aktualizovat, a poté je výběrem zelené šipky přesuňte na seznam **Vybraná pole**. Pouze pole v seznamu **Vybraná pole** lze aktualizovat pomocí sady pro import leasingu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]