---
title: Sjednocená číselná řady pro ID úloh
description: Tato funkce poskytuje jednu jednotnou číselnou řadu, která generuje ID úloh pro moduly řízení výroby, provádění výroby a modul času a docházky.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 00212803c46d898a39eafbc5c62016eb829535e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824934"
---
# <a name="unified-number-sequence-for-job-ids"></a><span data-ttu-id="47305-103">Sjednocená číselná řady pro ID úloh</span><span class="sxs-lookup"><span data-stu-id="47305-103">Unified number sequence for job IDs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47305-104">Tato funkce poskytuje jednu jednotnou číselnou řadu, která generuje ID úloh pro moduly řízení výroby, provádění výroby a modul času a docházky.</span><span class="sxs-lookup"><span data-stu-id="47305-104">This feature provides a single, unified number sequence that generates job IDs for the Production control, Manufacturing execution, and Time and attendance modules.</span></span> <span data-ttu-id="47305-105">Dříve jste pro každý z těchto modulů mohli zvolit jinou číselnou řadu, což mohlo vést ke konfliktním ID úloh, pokud dvě nebo více těchto řad používaly stejný formát.</span><span class="sxs-lookup"><span data-stu-id="47305-105">Previously, you were able to choose a different number sequence for each of these modules, which could result in conflicting job IDs if two or more of these sequences used an identical format.</span></span> <span data-ttu-id="47305-106">Takový konflikt může způsobit poškození dat.</span><span class="sxs-lookup"><span data-stu-id="47305-106">Such a conflict can cause data corruption.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="47305-107">Zapnutí této funkce ve vašem systému</span><span class="sxs-lookup"><span data-stu-id="47305-107">Turn on this feature for your system</span></span>

<span data-ttu-id="47305-108">Pokud váš systém ještě neobsahuje funkci popsanou v tomto tématu, přejděte na stránku [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte funkci *Sjednocená číselná řada pro ID úloh*.</span><span class="sxs-lookup"><span data-stu-id="47305-108">If your system doesn't already include the feature described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Unified number sequence for job IDs* feature.</span></span>

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a><span data-ttu-id="47305-109">Nastavení sjednocené číselné řady pro ID úloh</span><span class="sxs-lookup"><span data-stu-id="47305-109">Set up the unified number sequence for job IDs</span></span>

<span data-ttu-id="47305-110">Po povolení této funkce budou nastavení číselné řady **Identifikace úlohy**, která se nachází na stránkách parametrů pro moduly Řízení výroby, Provádění výroby a Čas a docházka, zastaralá a bude přidáno nové pole **Sjednocené ID úlohy**.</span><span class="sxs-lookup"><span data-stu-id="47305-110">After enabling this feature, the existing **Job identification** number-sequence settings located on the parameters pages for the Production control, Manufacturing execution, and Time and attendance modules will be deprecated and a new **Unified job ID** field will be added.</span></span> <span data-ttu-id="47305-111">Hodnota **Sjednocené ID úlohy** je sdílena všemi třemi moduly, čímž je zajištěno, že všechny moduly odkazují na stejnou číselnou řadu.</span><span class="sxs-lookup"><span data-stu-id="47305-111">The **Unified job ID** value is shared by all three modules, thus ensuring that all modules reference the same number sequence.</span></span> <span data-ttu-id="47305-112">ID úloh proto budou ve všech třech modulech jedinečná a ke konfliktu nikdy nedojde.</span><span class="sxs-lookup"><span data-stu-id="47305-112">Job IDs will therefore be unique across all three modules and a conflict will never occur.</span></span>

<span data-ttu-id="47305-113">Nastavení sjednocené číselné řady pro ID úloh:</span><span class="sxs-lookup"><span data-stu-id="47305-113">To set up the unified number sequence for job IDs:</span></span>

1. <span data-ttu-id="47305-114">Zapněte funkci, jak je popsáno v předchozí části.</span><span class="sxs-lookup"><span data-stu-id="47305-114">Turn on the feature as described in the previous section.</span></span>
1. <span data-ttu-id="47305-115">Buď identifikujte číselnou řadu, kterou chcete použít pro vaše sjednocená ID úlohy, nebo vytvořte novou.</span><span class="sxs-lookup"><span data-stu-id="47305-115">Either identify the number sequence you want to use for your unified job IDs, or create a new one.</span></span> <span data-ttu-id="47305-116">Další informace naleznete v tématu [Přehled číselných řad](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="47305-116">For more information, see [Number sequences overview](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span></span>
1. <span data-ttu-id="47305-117">Přejděte na stránku **Parametry řízení výroby**, **Parametry provedení výroby** nebo **Parametry času a docházky**.</span><span class="sxs-lookup"><span data-stu-id="47305-117">Go to the **Production control parameters**, **Manufacturing execution parameters**, or **Time and attendance parameters** page.</span></span> <span data-ttu-id="47305-118">Nezáleží na tom, kterou z nich si vyberete, protože když toto nastavení provedete na kterékoli z těchto stránek, všechny ostatní stránky se automaticky aktualizují.</span><span class="sxs-lookup"><span data-stu-id="47305-118">It doesn't matter which one you choose because when you make this setting on any of those pages, all of the other pages will update automatically.</span></span>
1. <span data-ttu-id="47305-119">Otevřete kartu **Číselné řady** na stránce s vybranými parametry.</span><span class="sxs-lookup"><span data-stu-id="47305-119">Open the **Number sequences** tab on your selected parameters page.</span></span>
1. <span data-ttu-id="47305-120">Přiřaďte **Kód číselné řady**, který jste dříve identifikovali, k řádku **Sjednocená ID úloh** v mřížce.</span><span class="sxs-lookup"><span data-stu-id="47305-120">Assign the **Number sequence code** that you identified previously to the **Unified job IDs** row of the grid.</span></span>
