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
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a><span data-ttu-id="a86b8-103">Přehled integrace Dynamics 365 Commerce a Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a86b8-103">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="a86b8-104">Toto téma představuje přehled integrace Microsoft Dynamics 365 Commerce a Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="a86b8-104">This topic presents an overview of Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="a86b8-105">Dynamics 365 Commerce se integruje s Teams a pomáhá zákazníkům a jejich zaměstnancům zlepšit produktivitu synchronizací správy úkolů mezi těmito dvěma aplikacemi.</span><span class="sxs-lookup"><span data-stu-id="a86b8-105">Dynamics 365 Commerce is integrating with Teams to help customers and their employees improve productivity by synchronizing task management between the two applications.</span></span> <span data-ttu-id="a86b8-106">Bezproblémová správa úkolů, kterou poskytuje integrace Commerce a Teams, umožňuje manažerům obchodu a zaměstnancům vytvářet seznamy úkolů, přiřazovat úkoly do více obchodů a sledovat stav úkolů v obchodech z kterékoli aplikace.</span><span class="sxs-lookup"><span data-stu-id="a86b8-106">The seamless task management that Commerce and Teams integration provides lets store managers and employees create task lists, assign tasks to multiple stores, and track the status of tasks across stores, from either application.</span></span>

<span data-ttu-id="a86b8-107">Integrace Commerce a Teams je k dispozici od vydání Commerce verze 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="a86b8-107">Commerce and Teams integration is available as of the Commerce version 10.0.18 release.</span></span>

## <a name="key-features"></a><span data-ttu-id="a86b8-108">Klíčové funkce</span><span class="sxs-lookup"><span data-stu-id="a86b8-108">Key features</span></span>

<span data-ttu-id="a86b8-109">Zde jsou některé z klíčových funkcí, které integrace Commerce a Microsoft Teams poskytuje:</span><span class="sxs-lookup"><span data-stu-id="a86b8-109">Here are some of the key features that the Commerce and Microsoft Teams integration provides:</span></span>

- <span data-ttu-id="a86b8-110">Zřizujte Teams využíváním výhod dobře definovaných informací z Commerce, jako je organizační struktura a informace o obchodech, pracovnících, oprávněních a obchodním kontextu.</span><span class="sxs-lookup"><span data-stu-id="a86b8-110">Provision Teams by taking advantage of well-defined information from Commerce, such as the organizational structure and information about stores, workers, permissions, and business context.</span></span>
- <span data-ttu-id="a86b8-111">Snadno synchronizujte probíhající změny (například přidávání nových obchodů nebo najímání nových zaměstnanců) mezi Commerce a Teams, ale udržujte Commerce jako hlavní zdroj dat organizační struktury.</span><span class="sxs-lookup"><span data-stu-id="a86b8-111">Easily synchronize ongoing changes (for example, the addition of new stores or hiring of new employees) between Commerce and Teams, but keep Commerce as the master source of organizational structure data.</span></span>
- <span data-ttu-id="a86b8-112">Integrujte správu úloh mezi Commerce a Teams a pomozte pracovníkům skladu, manažerům obchodů, regionálním manažerům a správcům komunikace zvládnout správu úkolů z obou aplikací.</span><span class="sxs-lookup"><span data-stu-id="a86b8-112">Integrate task management between Commerce and Teams to help store workers, store managers, regional managers, and communications managers handle task management from either application.</span></span>

## <a name="prerequisites-for-using-integration-features"></a><span data-ttu-id="a86b8-113">Předpoklady pro použití integračních funkcí</span><span class="sxs-lookup"><span data-stu-id="a86b8-113">Prerequisites for using integration features</span></span>

<span data-ttu-id="a86b8-114">Než začnete používat integrační funkce Microsoft Teams, musí být splněny následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="a86b8-114">The following prerequisites must be in place before you can start to use Microsoft Teams integration features:</span></span>

- <span data-ttu-id="a86b8-115">Standardní licence Microsoft 365 Business (Tato licence zahrnuje Teams.)</span><span class="sxs-lookup"><span data-stu-id="a86b8-115">Microsoft 365 Business Standard License (This license includes Teams.)</span></span>
- <span data-ttu-id="a86b8-116">Účty Azure Active Directory(Azure AD) pro všechny manažery a pracovníky obchodu</span><span class="sxs-lookup"><span data-stu-id="a86b8-116">Azure Active Directory (Azure AD) accounts for all store managers and workers</span></span>
- <span data-ttu-id="a86b8-117">Systémy POS (Point of Sale), které jsou konfigurovány s ověřováním Azure AD</span><span class="sxs-lookup"><span data-stu-id="a86b8-117">Point of sale (POS) systems that are configured with Azure AD authentication</span></span>

## <a name="conceptual-architecture"></a><span data-ttu-id="a86b8-118">Koncepční architektura</span><span class="sxs-lookup"><span data-stu-id="a86b8-118">Conceptual architecture</span></span>

<span data-ttu-id="a86b8-119">Následující obrázek ukazuje koncepční architekturu integrace Dynamics 365 Commerce a Microsoft Teams, přičemž jako příklad použijeme obchod v San Francisku.</span><span class="sxs-lookup"><span data-stu-id="a86b8-119">The following illustration shows the conceptual architecture of Dynamics 365 Commerce and Microsoft Teams integration, using a San Francisco store as an example.</span></span> <span data-ttu-id="a86b8-120">Teams i aplikace Commerce POS používají Microsoft Planner jako úložiště, takže úkoly publikované z Teams se zobrazují v aplikaci POS a úlohy ad hoc vytvořené manažery obchodů v aplikaci POS se objevují v Teams, což vede k bezproblémovému prostředí pro správu úloh mezi aplikacemi.</span><span class="sxs-lookup"><span data-stu-id="a86b8-120">Both Teams and the Commerce POS application use Microsoft Planner as a repository so that tasks published from Teams appear in the POS application and ad hoc tasks created by store managers in the POS application appear in Teams, resulting in a seamless task management experience between the applications.</span></span>    

![Architektura integrace Commerce a Teams](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a><span data-ttu-id="a86b8-122">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="a86b8-122">Additional resources</span></span>

[<span data-ttu-id="a86b8-123">Povolení integrace Dynamics 365 Commerce a Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a86b8-123">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="a86b8-124">Zřízení Microsoft Teams z Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a86b8-124">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="a86b8-125">Synchronizace správy úkolů mezi Microsoft Teams a Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="a86b8-125">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="a86b8-126">Správa uživatelských rolí v Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a86b8-126">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="a86b8-127">Mapování obchodů a týmů, pokud v Microsoft Teams již existují přednastavené týmy</span><span class="sxs-lookup"><span data-stu-id="a86b8-127">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="a86b8-128">Nejčastější dotazy k integraci Dynamics 365 Commerce a Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a86b8-128">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
