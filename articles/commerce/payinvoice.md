---
title: Nastavení scénářů plateb faktur
description: Toto téma popisuje, jak nakonfigurovat Dynamics 365 Commerce pro podporu různých scénářů týkajících se plateb faktur.
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9fe8fde32549568812a724311781d3515ef7036c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458631"
---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="0ca78-103">Nastavení scénářů plateb faktur</span><span class="sxs-lookup"><span data-stu-id="0ca78-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0ca78-104">Funkcionalita Platba faktur v aplikaci Dynamics 365 Commerce byla rozšířena, aby podporovala:</span><span class="sxs-lookup"><span data-stu-id="0ca78-104">The Pay invoice functionality in Dynamics 365 Commerce has been expanded to support:</span></span>

- <span data-ttu-id="0ca78-105">Proplacení vícero faktur prodejní objednávky v jedné transakci POS.</span><span class="sxs-lookup"><span data-stu-id="0ca78-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="0ca78-106">Platba různých typů faktur odběratele, včetně volných faktur, faktur na základě projektu a dobropisů.</span><span class="sxs-lookup"><span data-stu-id="0ca78-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="0ca78-107">Chcete-li povolit tyto scénáře, je třeba nakonfigurovat funkční profil pro obchody podle níže uvedených pokynů.</span><span class="sxs-lookup"><span data-stu-id="0ca78-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>

1. <span data-ttu-id="0ca78-108">Přejděte na **Retail a Commerce \> Nastavení kanálu \> Nastavení POS \> Profily POS \> Funkční profily** a zvolte profil, který je navázaný na obchody, u kterých chcete provést změny.</span><span class="sxs-lookup"><span data-stu-id="0ca78-108">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>
2. <span data-ttu-id="0ca78-109">Na kartě **Funkce** nakonfigurujte následující parametry podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="0ca78-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="0ca78-110">**Faktura prodejní objednávky** - Zvolte **Ano**, čímž povolíte uživateli zaplatit jednu nebo více faktur na základě prodejní objednávky v jedné transakci POS.</span><span class="sxs-lookup"><span data-stu-id="0ca78-110">**Sales order invoice** – Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="0ca78-111">**Volná faktura** - Zvolte **Ano**, čímž povolíte uživateli zaplatit jednu nebo více volných faktur v jedné transakci POS.</span><span class="sxs-lookup"><span data-stu-id="0ca78-111">**Free text invoice** – Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="0ca78-112">**Faktura projektu** - Zvolte **Ano**, čímž povolíte uživateli zaplatit jednu nebo více faktur na základě projektu v jedné transakci POS.</span><span class="sxs-lookup"><span data-stu-id="0ca78-112">**Project invoice** – Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="0ca78-113">**Dobropis prodejní objednávky** - Zvolte **Ano**, čímž povolíte uživateli vyrovnat více dobropisů na základě prodejní objednávky proti otevřeným fakturám nebo zpracovat refundaci zákazníkovi pro otevřený dobropis.</span><span class="sxs-lookup"><span data-stu-id="0ca78-113">**Sales order credit note** – Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="0ca78-114">Platba nebo vyrovnání dílčích částek není ještě podporována.</span><span class="sxs-lookup"><span data-stu-id="0ca78-114">Payment or settlement of partial amounts is not yet supported.</span></span>
