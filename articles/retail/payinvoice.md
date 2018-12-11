---
title: "Nastavení scénářů plateb faktur"
description: "Toto téma popisuje, jak nakonfigurovat Dynamics 365 for Retail pro podporu různých scénářů týkajících se plateb faktur."
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 3331b984693c58c6ee8c49b98ed7d3a8df5b79ff
ms.openlocfilehash: 53c4b9a9c9dac1add7021d909b2c8900d11e5c0c
ms.contentlocale: cs-cz
ms.lasthandoff: 12/04/2018

---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="f6ab1-103">Nastavení scénářů plateb faktur</span><span class="sxs-lookup"><span data-stu-id="f6ab1-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f6ab1-104">Funkcionalita Platba faktur v aplikaci Dynamics 365 for Retail byla rozšířena, aby podporovala:</span><span class="sxs-lookup"><span data-stu-id="f6ab1-104">The Pay invoice functionality in Dynamics 365 for Retail has been expanded to support:</span></span>
- <span data-ttu-id="f6ab1-105">Proplacení vícero faktur prodejní objednávky v jedné transakci POS</span><span class="sxs-lookup"><span data-stu-id="f6ab1-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="f6ab1-106">Platba různých typů faktur odběratele, včetně volných faktur, faktur na základě projektu a dobropisů.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="f6ab1-107">Chcete-li povolit tyto scénáře, je třeba nakonfigurovat funkční profil pro obchody podle níže uvedených pokynů.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>  

1. <span data-ttu-id="f6ab1-108">Přejděte na **Maloobchod > Nastavení kanálu > Nastavení POS > Profily POS > Funkční profily** a zvolte profil, který je navázaný na obchody, u kterých chcete provést změny.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-108">Go to **Retail > Channel setup > POS setup > POS profiles > Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>

1. <span data-ttu-id="f6ab1-109">Na kartě **Funkce** nakonfigurujte následující parametry podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="f6ab1-110">**Faktura prodejní objednávky** - Zvolte **Ano**, čímž povolíte uživateli zaplatit jednu nebo více faktur na základě prodejní objednávky v jedné transakci POS.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-110">**Sales order invoice** - Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>

    - <span data-ttu-id="f6ab1-111">**Volná faktura** - Zvolte **Ano**, čímž povolíte uživateli zaplatit jednu nebo více volných faktur v jedné transakci POS.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-111">**Free text invoice** - Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>

    - <span data-ttu-id="f6ab1-112">**Faktura projektu** - Zvolte **Ano**, čímž povolíte uživateli zaplatit jednu nebo více faktur na základě projektu v jedné transakci POS.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-112">**Project invoice** - Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>

    - <span data-ttu-id="f6ab1-113">**Dobropis prodejní objednávky** - Zvolte **Ano**, čímž povolíte uživateli vyrovnat více dobropisů na základě prodejní objednávky proti otevřeným fakturám nebo zpracovat refundaci zákazníkovi pro otevřený dobropis.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-113">**Sales order credit note** - Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="f6ab1-114">Platba nebo vyrovnání dílčích částek není ještě podporována.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-114">Payment or settlement of partial amounts is not yet supported.</span></span>

