---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (17. září 2018)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 213324f9074f88d9fdc8efdfa46bc3ed7817d1e8
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "856800"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-17-2018"></a><span data-ttu-id="ad033-103">Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (17. září 2018)</span><span class="sxs-lookup"><span data-stu-id="ad033-103">What's new or changed in Dynamics 365 for Talent Core HR (September 17, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ad033-104">**Sestavení 8.1.154.0**</span><span class="sxs-lookup"><span data-stu-id="ad033-104">**Build 8.1.154.0**</span></span>

<span data-ttu-id="ad033-105">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Core HR.</span><span class="sxs-lookup"><span data-stu-id="ad033-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="leave-and-absence--accrue-time-based-on-hours-worked"></a><span data-ttu-id="ad033-106">Pracovní volno a Absence – časové rozlišení na základě odpracovaných hodin</span><span class="sxs-lookup"><span data-stu-id="ad033-106">Leave and Absence – Accrue time based on hours worked</span></span>

<span data-ttu-id="ad033-107">Nový typ časové rozlišení byl přidán k plánům pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="ad033-107">A new accrual type has been added to Leave plans.</span></span> <span data-ttu-id="ad033-108">Plán časového rozlišení může být nyní založen na odpracovaných měsících nebo hodinách.</span><span class="sxs-lookup"><span data-stu-id="ad033-108">The accrual schedule can now be based on months of service or hours worked.</span></span> <span data-ttu-id="ad033-109">Další informace naleznete v tématu [Časové rozlišení volna na základě odpracovaných hodin](leave-accrue-hours-worked.md).</span><span class="sxs-lookup"><span data-stu-id="ad033-109">For more information, see [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

## <a name="platform-update-18"></a><span data-ttu-id="ad033-110">Aktualizace platformy 18</span><span class="sxs-lookup"><span data-stu-id="ad033-110">Platform update 18</span></span>

<span data-ttu-id="ad033-111">Platform update 18 je nyní součástí vydání aplikace Talent.</span><span class="sxs-lookup"><span data-stu-id="ad033-111">Platform update 18 is now part of the Talent release.</span></span> 

-   <span data-ttu-id="ad033-112">Povinná a další pole lze skrýt pomocí individuálního nastavení.</span><span class="sxs-lookup"><span data-stu-id="ad033-112">Mandatory and other fields can be hidden via personalization.</span></span> <span data-ttu-id="ad033-113">To umožňuje uživateli vytvářet zjednodušené rozhraní, kde nejsou povinná pole převzatá obchodní logikou zobrazená.</span><span class="sxs-lookup"><span data-stu-id="ad033-113">This allows a user to create a simplified experience where mandatory fields that are defaulted by business logic are not shown.</span></span> <span data-ttu-id="ad033-114">Skrytá povinná pole jsou rovněž dočasně viditelná,. když jsou při pokusu o uložení prázdná.</span><span class="sxs-lookup"><span data-stu-id="ad033-114">Hidden mandatory fields are also temporarily made visible if they are empty when a save is attempted.</span></span>

-   <span data-ttu-id="ad033-115">V aktualizaci Platform update 18 má nyní webový klient aplikace Talent stejné vizuální prvky jako Microsoft Fluent Design.</span><span class="sxs-lookup"><span data-stu-id="ad033-115">In Platform update 18, the Talent web client now aligns its visuals with Microsoft Fluent Design.</span></span>

    -   <span data-ttu-id="ad033-116">Když jsou pole v režimu čtení, můžete jednoduše vybrat možnost úpravy v polích pro přepnutí formuláře k úpravám.</span><span class="sxs-lookup"><span data-stu-id="ad033-116">When fields are in “read mode”, you can simply select the edit option in the fields to switch the form to edit.</span></span>

    -   <span data-ttu-id="ad033-117">Změny v zobrazení polí v režimu čtení.</span><span class="sxs-lookup"><span data-stu-id="ad033-117">Changes in how fields display when in read mode.</span></span>

    -   <span data-ttu-id="ad033-118">Nadpisy v pracovních prostorech a na stránkách jsou tučně.</span><span class="sxs-lookup"><span data-stu-id="ad033-118">Headings in workspaces and pages are bold.</span></span>

-   <span data-ttu-id="ad033-119">Chování nenahrazujícího vyhledávání se zlepšilo.</span><span class="sxs-lookup"><span data-stu-id="ad033-119">The behavior of non-replacing lookups has been improved.</span></span> <span data-ttu-id="ad033-120">Další informace naleznete v tématu [Vylepšené chování pro nenahrazující vyhledávání](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fbusiness-applications-release-notes%2FOctober18%2Fdynamics365-finance-operations%2Fnon-replacing-lookups&data=02%7C01%7C%7Ce0b3b3bee47b4424aaa208d619ce86f2%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636724772137980342&sdata=RN1qjtZSLtS010zgs0KlcwFrrB8Z7uWWGtFjdxdaamg%3D&reserved=0).</span><span class="sxs-lookup"><span data-stu-id="ad033-120">For more information, see [Improved behavior for non-replacing lookups](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fbusiness-applications-release-notes%2FOctober18%2Fdynamics365-finance-operations%2Fnon-replacing-lookups&data=02%7C01%7C%7Ce0b3b3bee47b4424aaa208d619ce86f2%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636724772137980342&sdata=RN1qjtZSLtS010zgs0KlcwFrrB8Z7uWWGtFjdxdaamg%3D&reserved=0).</span></span>

## <a name="bug-fixes"></a><span data-ttu-id="ad033-121">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="ad033-121">Bug fixes</span></span>

<span data-ttu-id="ad033-122">Tato verze obsahuje několik dalších oprav chyb, včetně toho, že odkazy na ACA ADA a I9 budou nyní povoleny pouze pro americké společnosti.</span><span class="sxs-lookup"><span data-stu-id="ad033-122">This release includes several additional bug fixes, including references to ACA, ADA, and I9 now will only be enabled in US companies.</span></span>
