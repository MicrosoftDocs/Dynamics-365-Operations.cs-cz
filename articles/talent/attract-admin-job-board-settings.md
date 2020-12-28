---
title: Povolení integraci Broadbean v aplikaci Attract
description: V tomto tématu je vysvětleno, jak nakonfigurovat aplikaci Microsoft Dynamics 365 Talent - Attract, aby publikovala práce na externí pracovní vývěsky, jako je Broadbean.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 10b612711e81b2b368ed23fdd95ab6a66451f0ca
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460627"
---
# <a name="enable-broadbean-integration-in-attract"></a><span data-ttu-id="9fce6-103">Povolení integraci Broadbean v aplikaci Attract</span><span class="sxs-lookup"><span data-stu-id="9fce6-103">Enable Broadbean integration in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9fce6-104">Chcete dostat své otevřené pozice před co největší množství kvalifikovaných kandidátů.</span><span class="sxs-lookup"><span data-stu-id="9fce6-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="9fce6-105">Náborové weby, například Broadbean, vám pomohou dosáhnout tohoto cíle.</span><span class="sxs-lookup"><span data-stu-id="9fce6-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="9fce6-106">Microsoft Dynamics 365 Talent: Attract vám nyní umožní publikovat pracovní místa na Broadbean a společnost Microsoft neustále v této oblasti poskytuje nové nabídky.</span><span class="sxs-lookup"><span data-stu-id="9fce6-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

> [!NOTE]
> - <span data-ttu-id="9fce6-107">Chcete-li publikovat pracovní místa na externí weby, musíte mít [doplněk komplexního náboru](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="9fce6-107">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="9fce6-108">Chcete-li publikovat práce do služby Broadbean prostřednictvím aplikace Attract, musíte mít předplatné Broadbean.</span><span class="sxs-lookup"><span data-stu-id="9fce6-108">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="9fce6-109">Tato funkce je aktuálně v náhledu</span><span class="sxs-lookup"><span data-stu-id="9fce6-109">This feature is currently in preview.</span></span> <span data-ttu-id="9fce6-110">Pokud chcete provést akci, musíte [ji zapnout v nastavení pro správu Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="9fce6-110">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

## <a name="configure-broadbean-integration"></a><span data-ttu-id="9fce6-111">Konfigurace integrace s Broadbean</span><span class="sxs-lookup"><span data-stu-id="9fce6-111">Configure Broadbean integration</span></span>

1. <span data-ttu-id="9fce6-112">Přihlaste se do aplikace Attract jako správce.</span><span class="sxs-lookup"><span data-stu-id="9fce6-112">Sign in to Attract as an admin.</span></span>

2. <span data-ttu-id="9fce6-113">Zvolte tlačítko **Nastavení** tlačítko (symbol ozubeného kola) v pravém horním rohu stránky a vyberte **Centrum pro správu**.</span><span class="sxs-lookup"><span data-stu-id="9fce6-113">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>

3. <span data-ttu-id="9fce6-114">Kontaktujte Broadbean a zadejte informace do polí **Uživatelské jméno**, **ID klienta** a **Token šifrování**.</span><span class="sxs-lookup"><span data-stu-id="9fce6-114">Contact Broadbean, and enter your information in the **Username**, **Client ID**, and **Encryption Token** fields.</span></span>

4. <span data-ttu-id="9fce6-115">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="9fce6-115">Select **Save**.</span></span>

> [!WARNING]
> <span data-ttu-id="9fce6-116">Vaše přihlašovací údaje do Broadbean jsou citlivé a důvěrné.</span><span class="sxs-lookup"><span data-stu-id="9fce6-116">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="9fce6-117">Proto je uchovávejte a sdílejte zodpovědně.</span><span class="sxs-lookup"><span data-stu-id="9fce6-117">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="9fce6-118">Tyto údaje může zobrazit kdokoli, kdo má roli správce v aplikaci Attract.</span><span class="sxs-lookup"><span data-stu-id="9fce6-118">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="9fce6-119">Společnost Microsoft a Attract nejsou zahrnuty při vytváření a údržbě těchto hodnot.</span><span class="sxs-lookup"><span data-stu-id="9fce6-119">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="9fce6-120">Je to vaše zodpovědnost udržovat je v aktuálním stavu v aplikaci Attract a pracovat s Broadbeanem na řešení problémů, které se týkají vašich přihlašovacích údajů.</span><span class="sxs-lookup"><span data-stu-id="9fce6-120">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>
