---
title: Rozšíření aplikace Talent o Power Apps a Power Automate
description: Tento článek popisuje několik příkladů scénářů rozšíření pro aplikaci Microsoft Dynamics 365 Human Resources používající Microsoft Power Apps a Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core;Experience Apps;Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b28480ff584870e931fdc288a2652a5649268576
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893070"
---
# <a name="extend-with-power-apps-and-power-automate"></a><span data-ttu-id="08d0e-103">Rozšíření o Power Apps a Power Automate</span><span class="sxs-lookup"><span data-stu-id="08d0e-103">Extend with Power Apps and Power Automate</span></span>

<span data-ttu-id="08d0e-104">Tento článek popisuje několik příkladů scénářů rozšíření pro aplikaci Microsoft Dynamics 365 Human Resources používající Microsoft Power Apps a Microsoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="08d0e-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Human Resources that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="08d0e-105">Můžete importovat balíček řešení přidružený ke každému příkladu do prostředí Power Apps.</span><span class="sxs-lookup"><span data-stu-id="08d0e-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="08d0e-106">Poté můžete tyto balíčky použít pokyny jako návod nebo jako počáteční body pro implementaci scénářů, které jsou použitelné pro vaši organizaci.</span><span class="sxs-lookup"><span data-stu-id="08d0e-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08d0e-107">Pokud chcete používat šablony a aplikace, které jsou popsány v tomto tématu „tak, jak jsou“, nezapomeňte je otestovat, abyste se ujistili, že pokrývají všechny scénáře, které jsou specifické pro vaši implementaci.</span><span class="sxs-lookup"><span data-stu-id="08d0e-107">If you want to use the templates and apps that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="08d0e-108">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="08d0e-108">Prerequisites</span></span>

- <span data-ttu-id="08d0e-109">Pro import balíčků, musí mít uživatelé oprávnění **Tvůrce prostředí**.</span><span class="sxs-lookup"><span data-stu-id="08d0e-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="08d0e-110">Pro export nebo import aplikací musí mít uživatelé licenci Power Apps Plan 2 nebo zkušební licenci Power Apps Plan 2.</span><span class="sxs-lookup"><span data-stu-id="08d0e-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="integration-with-microsoft-365-power-automate"></a><span data-ttu-id="08d0e-111">Integrace s Microsoft 365, Power Automate</span><span class="sxs-lookup"><span data-stu-id="08d0e-111">Integration with Microsoft 365, Power Automate</span></span>

<span data-ttu-id="08d0e-112">Aplikaci **Integrace s Microsoft 365** lze použít k extrakci informací o týmu pro přihlášené uživatele z Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="08d0e-112">The **Integration with Microsoft 365** app can be used to extract team information for signed-in users from Microsoft 365.</span></span> <span data-ttu-id="08d0e-113">Uvádí zaměstnance v aplikaci Human Resources pro zjištění typů identifikace zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="08d0e-113">It references workers in Human Resources to extract employee identification types.</span></span> <span data-ttu-id="08d0e-114">Manažeři mohou kontrolovat data vypršení platnosti typů ID zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="08d0e-114">Managers can check expiration dates of employee ID types.</span></span> <span data-ttu-id="08d0e-115">Mohou také odeslat připomenutí e-mailem v případě, že končí platnost typu ID zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="08d0e-115">They can also send an email reminder if the employee ID type is expiring.</span></span> <span data-ttu-id="08d0e-116">Power Automate se integruje s Power Apps pro odeslání tohoto připomenutí.</span><span class="sxs-lookup"><span data-stu-id="08d0e-116">Power Automate integrates with Power Apps to send this reminder.</span></span> <span data-ttu-id="08d0e-117">Po odeslání připomenutí bude odesláno potvrzení zpět do Power Apps z Power Automate.</span><span class="sxs-lookup"><span data-stu-id="08d0e-117">Confirmation will be sent back to Power Apps from Power Automate when the reminder is sent.</span></span> <span data-ttu-id="08d0e-118">Typy identifikace zahrnují řidičský průkaz, cestovní pas a jiné přijatelné formy průkazů totožnosti.</span><span class="sxs-lookup"><span data-stu-id="08d0e-118">Identification types include driver's license, passport, and other acceptable forms of ID.</span></span>

<span data-ttu-id="08d0e-119">Tuto aplikaci můžete rozšířit na další scénáře.</span><span class="sxs-lookup"><span data-stu-id="08d0e-119">You can extend this app for other scenarios.</span></span> <span data-ttu-id="08d0e-120">Lze ji použít například pro zobrazení informací o dovolené týmu, událostech kalendáře a jakýchkoliv událostech specifických pro tým.</span><span class="sxs-lookup"><span data-stu-id="08d0e-120">For example, you can use it to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="08d0e-121">Chcete-li stáhnout aplikací **Integrace s Microsoft 365, Power Automate**, přejděte na stránku [Integrace s Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) na stránce Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="08d0e-121">To download the **Integration with Microsoft 365, Power Automate** app, go to [Integration with Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="08d0e-122">Power Automate – připojení k SQL a provedení</span><span class="sxs-lookup"><span data-stu-id="08d0e-122">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="08d0e-123">Šablona **Power Automate – připojení k SQL a provedení** se připojuje k serveru Microsoft SQL Server a povoluje spuštění SQL dotazů.</span><span class="sxs-lookup"><span data-stu-id="08d0e-123">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="08d0e-124">Přestože tato šablona čte a aktualizuje tabulky SQL, můžete ji rozšířit a použít pro jiné scénáře.</span><span class="sxs-lookup"><span data-stu-id="08d0e-124">Although this template reads and updates SQL tables, you can extend it and use it for other scenarios.</span></span> <span data-ttu-id="08d0e-125">Například ji můžete použít k vyplnění tabulky fázování v Common Data Service záznamy z SQL Serveru a pravidelné synchronizaci tabulky fázování pomocí přírůstkového nabízení z SQL Serveru.</span><span class="sxs-lookup"><span data-stu-id="08d0e-125">For example, you can use it to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="08d0e-126">Rozšířený dotaz je integrován s tokem za účelem povolení transformace dat a přírůstkového nabízení.</span><span class="sxs-lookup"><span data-stu-id="08d0e-126">Advanced Query is integrated with Flow to enable Data transformation and incremental push.</span></span>

<span data-ttu-id="08d0e-127">Chcete-li stáhnout šablonu **Power Automate – připojení k SQL a provedení**, přejděte na [Power Automate – připojení k SQL a provedení](https://go.microsoft.com/fwlink/?linkid=2081789) v Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="08d0e-127">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="08d0e-128">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="08d0e-128">Additional resources</span></span>

[<span data-ttu-id="08d0e-129">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="08d0e-129">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>