---
title: Nastavení zásad proplachování na řádcích kusovníku není respektováno
description: Nastavení zásad proplachování na řádcích kusovníků není respektováno.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026339"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a><span data-ttu-id="a9ec4-103">Nastavení zásad proplachování na řádcích kusovníku není respektováno</span><span class="sxs-lookup"><span data-stu-id="a9ec4-103">Flushing principle settings on BOM lines aren't respected</span></span>

<span data-ttu-id="a9ec4-104">Číslo článku znalostní báze: 4612725</span><span class="sxs-lookup"><span data-stu-id="a9ec4-104">KB number: 4612725</span></span>

## <a name="symptoms"></a><span data-ttu-id="a9ec4-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="a9ec4-105">Symptoms</span></span>

<span data-ttu-id="a9ec4-106">K tomuto problému dochází, když je pole **Automatická spotřeba kusovníku** na kartě **Automatická aktualizace** stránky **Parametry řízení výroby** nastaveno na *Princip vyprazdňování*.</span><span class="sxs-lookup"><span data-stu-id="a9ec4-106">This issue occurs when the **Automatic BOM consumption** field on the **Automatic update** tab of the **Production control parameters** page is set to *Flushing principle*.</span></span> <span data-ttu-id="a9ec4-107">Toto nastavení označuje, že všechny řádky kusovníku (BOM) by měly být automaticky spotřebovány, když je přijata nákupní objednávka.</span><span class="sxs-lookup"><span data-stu-id="a9ec4-107">This setting indicates that all bill of materials (BOM) lines should automatically be consumed when a purchase order is received.</span></span> <span data-ttu-id="a9ec4-108">Pokud je pole **Princip vyprazdňování** na řádcích kusovníku výslovně nastaveno na *Ruční*, můžete očekávat, že řádky kusovníku nebudou automaticky spotřebovány.</span><span class="sxs-lookup"><span data-stu-id="a9ec4-108">If the **Flushing principle** field on BOM lines is explicitly set to *Manual*, you might expect that the BOM lines won't automatically be consumed.</span></span> <span data-ttu-id="a9ec4-109">Když však nastane tento problém, řádky kusovníku, kde je pole **Princip vyprazdňování** nastaveno na *Ruční* jsou přesto automaticky spotřebovány.</span><span class="sxs-lookup"><span data-stu-id="a9ec4-109">However, when this issue occurs, BOM lines where the **Flushing principle** field is set to *Manual* are automatically consumed anyway.</span></span>

## <a name="resolution"></a><span data-ttu-id="a9ec4-110">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="a9ec4-110">Resolution</span></span>

<span data-ttu-id="a9ec4-111">Pokud dochází k tomuto problému, mohou být nastaveny parametry řízení výroby tak, aby přepsaly nastavení **Princip vyprazdňování** na řádcích kusovníku.</span><span class="sxs-lookup"><span data-stu-id="a9ec4-111">If you're experiencing this issue, your production control parameters might be set up to override the **Flushing principle** setting on BOM lines.</span></span> <span data-ttu-id="a9ec4-112">Na stránce **Parametry řízení výroby** na kartě **Automatická aktualizace** zkontrolujte hodnotu pole **Automatická spotřeba kusovníku**.</span><span class="sxs-lookup"><span data-stu-id="a9ec4-112">On the **Production control parameters** page, on the **Automatic update** tab, check the value of the **Automatic BOM consumption** field.</span></span> <span data-ttu-id="a9ec4-113">Pokud je nastavena na *Vždy*, bude systém ignorovat nastavení **Princip vyprazdňování** na všech řádcích kusovníku a vždy tyto řádky vyprázdní.</span><span class="sxs-lookup"><span data-stu-id="a9ec4-113">If it's set to *Always*, the system will disregard the **Flushing principle** setting on all BOM lines and will always flush the lines.</span></span> <span data-ttu-id="a9ec4-114">Aby systém respektoval nastavení **Princip vyprazdňování** na řádcích kusovníku, změňte hodnotu **Automatická spotřeba kusovníku** na *Princip vyprazdňování*.</span><span class="sxs-lookup"><span data-stu-id="a9ec4-114">To make the system respect the **Flushing principle** setting on BOM lines, change the value of the **Automatic BOM consumption** field to *Flushing principle*.</span></span>
