---
title: Zrušení práce skladu pro zpracování výjimek
description: V tomto tématu je popsána funkce zrušení práce, která vedoucímu skladu umožňuje blokovat práci.
author: omulvad
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cb725885fb48293a08915f13a4fb14085e930444
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205798"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a><span data-ttu-id="31f95-103">Zrušení práce skladu pro zpracování výjimek</span><span class="sxs-lookup"><span data-stu-id="31f95-103">Cancel warehouse work for exception handling</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31f95-104">Funkce Zrušit práci v aplikaci Microsoft Dynamics 365 Supply Chain Management umožňuje správci zrušit určitou aktuálně probíhající práci skladu, ale je blokována systémem nebo ji nelze dokončit z důvodu výjimečných okolností.</span><span class="sxs-lookup"><span data-stu-id="31f95-104">The Cancel work functionality in Microsoft Dynamics 365 Supply Chain Management lets the admin user cancel specific warehouse work that is currently in progress, but that is blocked by the system or can't be completed because of exceptional circumstances.</span></span> <span data-ttu-id="31f95-105">Tato funkce je atraktivní a zabezpečená alternativa se správnými opravnými skripty SQL, které opravují nekonzistentní data.</span><span class="sxs-lookup"><span data-stu-id="31f95-105">This functionality is an attractive and secure alternative to SQL corrective scripts that fix inconsistent data.</span></span> <span data-ttu-id="31f95-106">Avšak vzhledem k tomu, že tyto skripty jsou obvykle vyžadovány odborníky z oblasti IT, funkce zrušení práce mohou používat uživatelé ve společnosti, kteří mají oprávnění správce.</span><span class="sxs-lookup"><span data-stu-id="31f95-106">However, whereas these scripts are typically requested from IT professionals, the Cancel work functionality can be used by users in the company who have admin rights.</span></span>

<span data-ttu-id="31f95-107">K funkci Zrušit práci můžete přejít klknutím na položky **Řízení skladu** \> **Pravidelné úkoly** \> **Vymazat \> Zrušit práci**.</span><span class="sxs-lookup"><span data-stu-id="31f95-107">You can access the Cancel work functionality at **Warehouse management** \> **Periodic tasks** \> **Clean up \> Cancel work**.</span></span> <span data-ttu-id="31f95-108">V dialogovém okně **Zrušit práci** zadejte ID práce pro práci, kterou chcete zrušit, a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="31f95-108">In the **Cancel work** dialog box, specify the work ID of the work to cancel, and then select **OK**.</span></span>

## <a name="warehouse-work-that-can-be-canceled"></a><span data-ttu-id="31f95-109">Skladová práce, kterou lze zrušit</span><span class="sxs-lookup"><span data-stu-id="31f95-109">Warehouse work that can be canceled</span></span>

<span data-ttu-id="31f95-110">Během operací vyskladnění může pracovník narazit na situace, kdy zaregistroval množství, která byla vydána z místa uložení do svého umístění uživatele, ale nemohl registrovat operaci výběru.</span><span class="sxs-lookup"><span data-stu-id="31f95-110">During warehouse picking operations, a worker might encounter situations where they have registered quantities as picked from a storage location to their user location, but then they can't register the put operation.</span></span> <span data-ttu-id="31f95-111">Nekonzistentní data skladu jsou často, ale ne vždy, důvodem zablokování práce.</span><span class="sxs-lookup"><span data-stu-id="31f95-111">Inconsistent warehouse data is often, but not always, the reason why work is blocked.</span></span>

<span data-ttu-id="31f95-112">Na rozdíl od běžné funkce zrušení, ke které lze získat přístup pomocí tlačítka **zrušit** v záhlaví práce, nemusí funkce zrušení práce vyžadovat, aby byl poslední dokončený řádek práce řádkem **vyzvednout**.</span><span class="sxs-lookup"><span data-stu-id="31f95-112">Unlike the regular Cancel functionality that can be accessed by using the **Cancel** button on the work header, the Cancel work functionality doesn't require that the last completed work line be a work line of the **put** type.</span></span> <span data-ttu-id="31f95-113">Jinými slovy, pro funkci zrušení práce lze spustit logiku zrušení i v případě, že se množství položky na řádku práce nachází v umístění uživatele.</span><span class="sxs-lookup"><span data-stu-id="31f95-113">In other words, for the Cancel work functionality, cancellation logic can be run even if the item quantity on a work line is in a user location.</span></span>

> [!NOTE]
> <span data-ttu-id="31f95-114">V případě práce, která musí být zrušena z provozních důvodů, musí uživatelé skladu nadále používat pravidelné funkce zrušení na stránce práce.</span><span class="sxs-lookup"><span data-stu-id="31f95-114">For work that must be canceled for operational reasons, warehouse users must continue to use the regular Cancel functionality on the work page.</span></span>

<span data-ttu-id="31f95-115">Pomocí funkce Zrušit práci lze zrušit pouze práci typu **Prodej**, **Problém s převodem**, **Vyzvednutí surovin** nebo **Doplnění**.</span><span class="sxs-lookup"><span data-stu-id="31f95-115">Only work of the **Sales**, **Transfer issue**, **Raw material picking**, or **Replenishment** type can be canceled by using the Cancel work functionality.</span></span> <span data-ttu-id="31f95-116">Logika zrušení nebude spuštěna pro zmrazenou práci výběru surovin nebo práci, kterou lze zrušit pomocí běžné funkce zrušení (Další informace naleznete v předchozí poznámce).</span><span class="sxs-lookup"><span data-stu-id="31f95-116">Cancellation logic won't be run for frozen raw material picking work or work that can be canceled by using the regular Cancel functionality (see the preceding note).</span></span>

<span data-ttu-id="31f95-117">Chcete-li odblokovat práci, systém zruší všechny zbývající řádky práce a opraví data skladu přidružená k ID práce, kterou daný uživatel určil.</span><span class="sxs-lookup"><span data-stu-id="31f95-117">To unblock the work, the system cancels any remaining work lines and fixes the warehouse data that is associated with the work ID that the user specified.</span></span> <span data-ttu-id="31f95-118">Všechny běžné operace zpracování skladu, které zahrnují ovlivněné množství zboží, mohou být opět obnoveny.</span><span class="sxs-lookup"><span data-stu-id="31f95-118">Any regular warehouse-handling operations that involve the affected item quantity can then resume.</span></span>

<span data-ttu-id="31f95-119">Chcete-li po zrušení práce vložit ovlivněnou položku do určitého umístění, musí uživatel použít operaci pohybu zásob nebo úpravy množství v mobilním zařízení.</span><span class="sxs-lookup"><span data-stu-id="31f95-119">To put the affected item in a specific location after the work is canceled, the user must use an inventory movement or quantity adjustment operation on a mobile device.</span></span>
