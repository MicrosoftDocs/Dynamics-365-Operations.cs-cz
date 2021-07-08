---
title: Parametry pro hlavní plán neexistují
description: Při pokusu o potvrzení plánované objednávky se zobrazí chybová zpráva s oznámením, že pro hlavní plán neexistují žádné parametry.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4b64af2e30109b8560d40c4c532504611528bbe
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294031"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a><span data-ttu-id="67c28-103">Parametry pro hlavní plán neexistují</span><span class="sxs-lookup"><span data-stu-id="67c28-103">Parameters for the master plan don't exist</span></span>

<span data-ttu-id="67c28-104">Kód chyby: SYS25368</span><span class="sxs-lookup"><span data-stu-id="67c28-104">Error code: SYS25368</span></span>

## <a name="symptoms"></a><span data-ttu-id="67c28-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="67c28-105">Symptoms</span></span>

<span data-ttu-id="67c28-106">Když se pokusíte potvrdit objednávku, zobrazí se následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="67c28-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="67c28-107">Parametry hlavního plánu %1 neexistují.</span><span class="sxs-lookup"><span data-stu-id="67c28-107">Parameters for master plan %1 do not exist.</span></span>

## <a name="cause"></a><span data-ttu-id="67c28-108">Příčina</span><span class="sxs-lookup"><span data-stu-id="67c28-108">Cause</span></span>

<span data-ttu-id="67c28-109">Z důvodu problémů s konfigurací systém nemůže najít nastavení pro zadaný plán.</span><span class="sxs-lookup"><span data-stu-id="67c28-109">Because of configuration issues, the system can't find the settings for the specified plan.</span></span>

## <a name="resolution"></a><span data-ttu-id="67c28-110">Řešení</span><span class="sxs-lookup"><span data-stu-id="67c28-110">Resolution</span></span>

- <span data-ttu-id="67c28-111">Přejděte na **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány** a ujistěte se, že plán, který má zadaný název, existuje.</span><span class="sxs-lookup"><span data-stu-id="67c28-111">Go to **Master planning \> Setup \> Plans \> Master plans**, and make sure that a plan that has the specified name exists.</span></span>
