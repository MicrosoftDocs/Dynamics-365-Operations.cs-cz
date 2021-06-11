---
title: Vyvolání toků automatizace procesů k vytvoření objednávek kvality
description: Toto téma poskytuje zdroje pro použití Power Automate, chcete-li automatizovat obchodní procesy na příkladu kvalitních objednávek.
author: cabeln
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f35adab3075ba810964a41899ba95ae40c115e83
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115168"
---
# <a name="invoke-process-automation-flows-to-create-quality-orders"></a><span data-ttu-id="371ad-103">Vyvolání toků automatizace procesů k vytvoření objednávek kvality</span><span class="sxs-lookup"><span data-stu-id="371ad-103">Invoke process automation flows to create quality orders</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="371ad-104">Organizace mají rostoucí poptávku po automatizaci standardních obchodních procesů, poskytování pohodlnějších interakcí zaměstnancům a využívání různých datových signálů a systémů k automatickému řízení obchodních procesů.</span><span class="sxs-lookup"><span data-stu-id="371ad-104">Organizations have an increasing demand to automate standard business processes, provide more convenient interactions to the staff, and utilize various data signals and systems to drive business processes automatically.</span></span> <span data-ttu-id="371ad-105">S automatizací robotických procesů (RPA) a Microsoft Power Automate mohou podniky využívat prostředí bez kódu k automatizaci opakujících se procesů, čímž získají efektivitu a přesnost.</span><span class="sxs-lookup"><span data-stu-id="371ad-105">With robotic process automation (RPA) and Microsoft Power Automate, businesses can use a no-code experience to automate repetitive processes, thus gaining efficiency and accuracy.</span></span>

<span data-ttu-id="371ad-106">Stahovatelná šablona řešení pro automatizaci pro Supply Chain Management ukazuje, jak lze použít Power Automate k automatizaci obchodních procesů pomocí příkladu objednávek kvality.</span><span class="sxs-lookup"><span data-stu-id="371ad-106">The downloadable automation solution template for Supply Chain Management showcases how Power Automate can be used to automate business processes using quality orders as an example.</span></span>

<span data-ttu-id="371ad-107">Můžete si stáhnout šablonu řešení automatizace [zde](https://aka.ms/D365SCMQualityOrderRPASolution).</span><span class="sxs-lookup"><span data-stu-id="371ad-107">You can download the automation solution template [here](https://aka.ms/D365SCMQualityOrderRPASolution).</span></span>

<span data-ttu-id="371ad-108">Přehled této funkce a jejích schopností najdete v následujícím videu: [Využijte RPA k vytváření objednávek kvality v Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span><span class="sxs-lookup"><span data-stu-id="371ad-108">For an overview of this feature and its capabilities, see the following video: [Utilize RPA to create quality orders in Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span></span>

<span data-ttu-id="371ad-109">![Možnosti automatizace pomocí RPA](media/rpa-automation-options.png "Možnosti automatizace pomocí RPA")</span><span class="sxs-lookup"><span data-stu-id="371ad-109">![Automation options with RPA](media/rpa-automation-options.png "Automation options with RPA")</span></span>

<span data-ttu-id="371ad-110">Šablona řešení Power Automate zahrnuje tok automatizace cloudu a tok automatizace stolních počítačů, které automatizují vytváření objednávek kvality v Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="371ad-110">The Power Automate solution template includes a cloud automation flow and a desktop automation flow that automate the creation of quality orders in Supply Chain Management.</span></span>

<span data-ttu-id="371ad-111">Automatizaci lze spustit v reakci na mnoho událostí a signálů, včetně vstupů uživatelů nebo signálů strojů (včetně internetu věcí (IoT)).</span><span class="sxs-lookup"><span data-stu-id="371ad-111">The automation can be started in response to many events and signals, including user input or machine signals (including the Internet of Things (IoT)).</span></span> <span data-ttu-id="371ad-112">Příklad aplikace Power Application *Q-Order* je součástí šablony řešení.</span><span class="sxs-lookup"><span data-stu-id="371ad-112">The *Q-Order* Power Application example is included in the solution template.</span></span> <span data-ttu-id="371ad-113">Umožňuje uživateli naskenovat QR kód položky, zadat množství a připojit obrázky pomocí fotoaparátu.</span><span class="sxs-lookup"><span data-stu-id="371ad-113">It allows the user to scan an item QR code, enter quantity, and attach pictures using a camera.</span></span>

<span data-ttu-id="371ad-114">Zahrnuty jsou parametry řešení pro konfiguraci automatizace pro konkrétní případ použití ve výrobním zařízení.</span><span class="sxs-lookup"><span data-stu-id="371ad-114">Solution parameters are included to configure the automation for a specific use case in a production facility.</span></span>

<span data-ttu-id="371ad-115">![Vytvořit objednávku kvality](media/rpa-create-quality-roder.png "Vytvořit objednávku kvality")</span><span class="sxs-lookup"><span data-stu-id="371ad-115">![Create quality order](media/rpa-create-quality-roder.png "Create quality order")</span></span>

<span data-ttu-id="371ad-116">Úplný podrobný průvodce, jak stáhnout, nainstalovat a použít ukázkové řešení pro automatizaci vytváření objednávek kvality, najdete v článku [Automatizovat vytváření objednávek kvality v Dynamics 365 Supply Chain Management s využitím automatizace robotických procesů Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span><span class="sxs-lookup"><span data-stu-id="371ad-116">For a complete step-by-step guide about how to download, install, and use the sample solution for automating quality order creation, see [Automate quality order creation on Dynamics 365 Supply Chain Management with Robotic Process Automation using Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span></span>

