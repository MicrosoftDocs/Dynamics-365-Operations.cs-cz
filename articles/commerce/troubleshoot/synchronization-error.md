---
title: Chyba synchronizace objednávky související s výchozí platební službou
description: Toto téma obsahuje pokyny pro řešení potíží, které vám pomohou opravit chybu, která může nastat při synchronizaci online objednávky.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 45eeae751051b58e1c9e725eb4ed4b5240026e7f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801428"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="eb303-103">Chyba synchronizace objednávky související s výchozí platební službou</span><span class="sxs-lookup"><span data-stu-id="eb303-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eb303-104">Toto téma obsahuje pokyny pro řešení potíží, které vám pomohou opravit chybu, která může nastat při synchronizaci online objednávky.</span><span class="sxs-lookup"><span data-stu-id="eb303-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="eb303-105">popis</span><span class="sxs-lookup"><span data-stu-id="eb303-105">Description</span></span>

<span data-ttu-id="eb303-106">Při synchronizaci online objednávky se zobrazí následující chybová zpráva: „Ke zpracování transakcí kreditní kartou musí existovat výchozí platební služba.“</span><span class="sxs-lookup"><span data-stu-id="eb303-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![Chybí výchozí chyba platební služby](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="eb303-108">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="eb303-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="eb303-109">Potvrzení nebo nastavení výchozí platební služby v centrále Commerce</span><span class="sxs-lookup"><span data-stu-id="eb303-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="eb303-110">K potvrzení nebo nastavení výchozí platební služby v centrále Commerce postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="eb303-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="eb303-111">Přejděte do nabídky **Pohledávky \> Nastavení platby \> Služby pro platby**.</span><span class="sxs-lookup"><span data-stu-id="eb303-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="eb303-112">Ujistěte se, že je možnost **Výchozí zpracovatel pro nové kreditní karty** je nastavena na **Ano** pro jednu platební službu.</span><span class="sxs-lookup"><span data-stu-id="eb303-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eb303-113">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="eb303-113">Additional resources</span></span>

[<span data-ttu-id="eb303-114">Nastavení platební karty, autorizace a záznam</span><span class="sxs-lookup"><span data-stu-id="eb303-114">Credit card setup, authorization, and capture</span></span>](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)
