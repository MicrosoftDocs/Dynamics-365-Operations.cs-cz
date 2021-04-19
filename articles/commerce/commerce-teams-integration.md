---
title: Přehled integrace Dynamics 365 Commerce a Microsoft Teams
description: Toto téma představuje přehled integrace Microsoft Dynamics 365 Commerce a Microsoft Teams.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3b7872757815d4eec0393e8b1c8c6ff5467e9473
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842625"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a>Přehled integrace Dynamics 365 Commerce a Microsoft Teams

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Toto téma představuje přehled integrace Microsoft Dynamics 365 Commerce a Microsoft Teams.

Dynamics 365 Commerce se integruje s Teams a pomáhá zákazníkům a jejich zaměstnancům zlepšit produktivitu synchronizací správy úkolů mezi těmito dvěma aplikacemi. Bezproblémová správa úkolů, kterou poskytuje integrace Commerce a Teams, umožňuje manažerům obchodu a zaměstnancům vytvářet seznamy úkolů, přiřazovat úkoly do více obchodů a sledovat stav úkolů v obchodech z kterékoli aplikace.

Integrace Commerce a Teams je k dispozici od vydání Commerce verze 10.0.18.

## <a name="key-features"></a>Klíčové funkce

Zde jsou některé z klíčových funkcí, které integrace Commerce a Microsoft Teams poskytuje:

- Zřizujte Teams využíváním výhod dobře definovaných informací z Commerce, jako je organizační struktura a informace o obchodech, pracovnících, oprávněních a obchodním kontextu.
- Snadno synchronizujte probíhající změny (například přidávání nových obchodů nebo najímání nových zaměstnanců) mezi Commerce a Teams, ale udržujte Commerce jako hlavní zdroj dat organizační struktury.
- Integrujte správu úloh mezi Commerce a Teams a pomozte pracovníkům skladu, manažerům obchodů, regionálním manažerům a správcům komunikace zvládnout správu úkolů z obou aplikací.

## <a name="prerequisites-for-using-integration-features"></a>Předpoklady pro použití integračních funkcí

Než začnete používat integrační funkce Microsoft Teams, musí být splněny následující předpoklady:

- Standardní licence Microsoft 365 Business (Tato licence zahrnuje Teams.)
- Účty Azure Active Directory(Azure AD) pro všechny manažery a pracovníky obchodu
- Systémy POS (Point of Sale), které jsou konfigurovány s ověřováním Azure AD

## <a name="conceptual-architecture"></a>Koncepční architektura

Následující obrázek ukazuje koncepční architekturu integrace Dynamics 365 Commerce a Microsoft Teams, přičemž jako příklad použijeme obchod v San Francisku. Teams i aplikace Commerce POS používají Microsoft Planner jako úložiště, takže úkoly publikované z Teams se zobrazují v aplikaci POS a úlohy ad hoc vytvořené manažery obchodů v aplikaci POS se objevují v Teams, což vede k bezproblémovému prostředí pro správu úloh mezi aplikacemi.    

![Architektura integrace Commerce a Teams](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a>Další prostředky

[Povolení integrace Dynamics 365 Commerce a Microsoft Teams](enable-teams-integration.md)

[Zřízení Microsoft Teams z Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Synchronizace správy úkolů mezi Microsoft Teams a Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Správa uživatelských rolí v Microsoft Teams](manage-user-roles-teams.md)

[Mapování obchodů a týmů, pokud v Microsoft Teams již existují přednastavené týmy](map-stores-existing-teams.md)

[Nejčastější dotazy k integraci Dynamics 365 Commerce a Microsoft Teams](teams-integration-faq.md)
