---
title: Zahrnutí hmotnosti kontejneru a objemu při naložení
description: Toto téma popisuje, jak nastavit a použít funkci zahrnutí hmotnosti kontejneru a objemu v nákladech.
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adbaa379889d373d597b2f6882b78f82bd71ae57
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549214"
---
# <a name="include-container-weight-and-volume-on-load"></a><span data-ttu-id="4a348-103">Zahrnutí hmotnosti kontejneru a objemu při naložení</span><span class="sxs-lookup"><span data-stu-id="4a348-103">Include container weight and volume on load</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a348-104">Funkce pro zahrnutí hmotnosti kontejneru a objemu v nákladu poskytuje jasnou představu celkové hmotnosti a objemu kontejnerů a zboží, které bude součástí nákladu.</span><span class="sxs-lookup"><span data-stu-id="4a348-104">The functionality for including the container weight and volume on a load gives a clear representation of the total weight and volume of containers and items that are going on a load.</span></span>

<span data-ttu-id="4a348-105">Náklad obsahuje jednu nebo více dodávek a tyto dodávky obsahují různé položky, které patří do jedné nebo více prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="4a348-105">A load contains a single shipment or multiple shipments, and these shipments contain distinct items that belong to a single sales order or multiple sales orders.</span></span> <span data-ttu-id="4a348-106">Položky jsou uloženy uvnitř kontejneru a kontejnery jsou naloženy na náklad.</span><span class="sxs-lookup"><span data-stu-id="4a348-106">The items are stored inside a container, and containers are loaded on a load.</span></span> <span data-ttu-id="4a348-107">Položky mimo kontejner mohou být též součástí nákladu.</span><span class="sxs-lookup"><span data-stu-id="4a348-107">Items that are outside a container can also be part of a load.</span></span> <span data-ttu-id="4a348-108">Na základě těchto podmínek systém vypočítá hodnoty hmotnosti a objemu v nákladu podle hmotnosti a objemu obou kontejnerů a zboží.</span><span class="sxs-lookup"><span data-stu-id="4a348-108">Based on these conditions, the system calculates values for the weight and volume on the load by considering the weight and volume of both containers and items.</span></span>

<span data-ttu-id="4a348-109">Nejsou-li vypočtené hodnoty přesné, lze je upravit zadáním skutečných hodnot hmotnosti a objemu v nákladu.</span><span class="sxs-lookup"><span data-stu-id="4a348-109">If the calculated values aren’t precise, you can adjust them by entering the actual values for the weight and volume on the load.</span></span> <span data-ttu-id="4a348-110">Hodnoty hmotnosti a objemu se používají v procesech správy přepravy.</span><span class="sxs-lookup"><span data-stu-id="4a348-110">The values for the weight and volume are used in transportation management processes.</span></span> <span data-ttu-id="4a348-111">Například hodnoty se používají v pracovní ploše sazby trasy, kde pomáhají definovat sazbu a trasu pro náklad, a také se používají pro úhrady za přepravu a přihlášení řidiče.</span><span class="sxs-lookup"><span data-stu-id="4a348-111">For example, the values are used in the rate route workbench, where they help define the rate and route for loads, and they are also used for transportation tenders and driver check-in.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="4a348-112">Kdy se to používá</span><span class="sxs-lookup"><span data-stu-id="4a348-112">Where it applies</span></span>

<span data-ttu-id="4a348-113">Funkce pro zahrnutí objemu a hmotnosti kontejneru do nákladu se použije v procesech správy přepravy, jako je například pracovní plocha sazeb trasy, úhrady za přepravu nebo přihlášení řidiče.</span><span class="sxs-lookup"><span data-stu-id="4a348-113">The functionality for including the container weight and volume on a load applies in transportation management processes, such as the rate route workbench, transportation tenders, and driver check-in.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="4a348-114">Způsob nastavení</span><span class="sxs-lookup"><span data-stu-id="4a348-114">How it is set up</span></span>

<span data-ttu-id="4a348-115">Počet kontejnerů, které je potřeba zvážit pro náklad, je vypočítán za základě hmotnosti a objemu kontejneru, a na použitém procentu kontejneru.</span><span class="sxs-lookup"><span data-stu-id="4a348-115">The number of containers that should be considered for a load is calculated based on the weight and volume of the container, and on the percentage of the container is used.</span></span>

-   <span data-ttu-id="4a348-116">Chcete-li nastavit hmotnost a objem kontejneru, klikněte na **Řízení skladu** \> **Nastavení** \> **Kontejnery** \> **Typy kontejnerů**.</span><span class="sxs-lookup"><span data-stu-id="4a348-116">To set the weight and volume for a container, click **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>

-   <span data-ttu-id="4a348-117">Chcete-li nastavit procento využití kontejneru, klikněte na **Řízení skladu** \> **Nastavení** \> **Kontejnery** \> **Skupiny kontejnerů** a zadejte hodnotu do pole **Procento využití kontejneru**.</span><span class="sxs-lookup"><span data-stu-id="4a348-117">To set the container utilization percentage, click **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**, and then enter a value in the **Container utilization percentage** field.</span></span>
