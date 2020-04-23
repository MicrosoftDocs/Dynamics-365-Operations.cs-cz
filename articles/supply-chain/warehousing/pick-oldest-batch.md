---
title: Vyskladnění nejstarší dávky na mobilním zařízení
description: Toto téma popisuje, jak nastavit a použít možnosti, když chcete vyskladnit nejstarší dávku z mobilního zařízení.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f235c34d6369c6f0584a7bac1c1be75f3d84c9c0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215624"
---
# <a name="pick-oldest-batch-on-a-mobile-device"></a><span data-ttu-id="cf81f-103">Vyskladnění nejstarší dávky na mobilním zařízení</span><span class="sxs-lookup"><span data-stu-id="cf81f-103">Pick oldest batch on a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf81f-104">Ke konfiguraci použít **Vyskladnit nejstarší dávku** lze přejít prostřednictvím nabídky mobilního zařízení a umožňuje vynutit nebo upozornit pracovníky skladu na vyskladnění nejstarší dávky na aktuálním místě.</span><span class="sxs-lookup"><span data-stu-id="cf81f-104">You can access the configuration **Pick oldest batch** via a mobile device menu and it allows you to force or warn warehouse workers to pick the oldest batch in their current location.</span></span>  

## <a name="where-it-applies"></a><span data-ttu-id="cf81f-105">Kdy se to používá</span><span class="sxs-lookup"><span data-stu-id="cf81f-105">Where it applies</span></span>
<span data-ttu-id="cf81f-106">Možnost Vyskladnit nejstarší dávku je nakonfigurována pro položky nabídky mobilního zařízení a má vliv na vyskladnění dávky pod položkami.</span><span class="sxs-lookup"><span data-stu-id="cf81f-106">Pick oldest batch is configured on mobile device menu items and effects the pick for batch below items.</span></span>

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a><span data-ttu-id="cf81f-107">Nastavení konfigurace pro vyskladnění nejstarší dávky</span><span class="sxs-lookup"><span data-stu-id="cf81f-107">How to set up the configuration for Pick oldest batch</span></span> 
<span data-ttu-id="cf81f-108">Pro položky, které jsou nastaveny na použít stávající práce lze možnost **Vyskladnit nejstarší dávku** nastavit na hodnoty **žádná**, **upozornit** nebo **Vynutit** z nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="cf81f-108">For items that are set to use existing work, **Pick oldest batch** can be set to **None**, **Warn**, or **Force** from a mobile device menu.</span></span>

<span data-ttu-id="cf81f-109">**Žádná**: Pracovníci nebudou dostávat žádné zprávy a budou mít dovoleny vybrat všechny dávky v umístění.</span><span class="sxs-lookup"><span data-stu-id="cf81f-109">**None**: Workers will not receive any messages and they will be allowed to pick any batch in their location.</span></span>

<span data-ttu-id="cf81f-110">**Upozornit** a **Vynutit**: seznam dávek s nejstarším datem vypršení platnosti se zobrazí nad ovládacím prvkem dávky, když pracovník vybere dávku.</span><span class="sxs-lookup"><span data-stu-id="cf81f-110">**Warn** and **Force**:  A list of the batch(es) with the oldest expiration date will be displayed above the batch control when the worker selects a batch.</span></span> <span data-ttu-id="cf81f-111">Pokud je skladové místo řízeno registrační značkou, seznam registračních značek vozidel, které mají nejstarší dávku, se zobrazí nad ovládacím prvkem registrační značky vozidla.</span><span class="sxs-lookup"><span data-stu-id="cf81f-111">If the location is license plate controlled, a list of license plates that have the oldest batch will be displayed above the license plate control.</span></span> 
-   <span data-ttu-id="cf81f-112">**Upozornění**: Pokud zaměstnanec zvolí registrační značku nebo dávku, které nejsou uvedeny v seznamu, ovládací prvek bude ignorován a zobrazí se upozornění, že existuje starší dávka k výběru.</span><span class="sxs-lookup"><span data-stu-id="cf81f-112">**Warn**: If a worker chooses a license plate or batch that is not on the shown list, the control will be blanked and a warning will be shown that there is an older batch to select.</span></span> <span data-ttu-id="cf81f-113">Aby bylo možné pokračovat v práci, pracovník může vybrat stejnou registrační značku nebo dávku znovu.</span><span class="sxs-lookup"><span data-stu-id="cf81f-113">To be allowed to continue the work, the worker can select the same license plate or batch again.</span></span>  
-   <span data-ttu-id="cf81f-114">**Vynutit**: Zaměstnanci budou dále dostávat zprávy, že existuje starší dávka pro výdej.</span><span class="sxs-lookup"><span data-stu-id="cf81f-114">**Force**: Workers will continue to receive the message that there is an older batch to pick.</span></span>
