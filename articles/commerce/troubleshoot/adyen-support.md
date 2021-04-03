---
title: Odstraňování potíží s platebním konektorem Dynamics 365 pro Adyen
description: Toto téma poskytuje pokyny pro řešení potíží, které vám mohou pomoci získat podporu, když máte problémy s Platebním konektorem Microsoft Dynamics 365 pro Adyen.
author: Reza-Assadi
manager: AnnBe
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
ms.openlocfilehash: f01db3fa670355696c094be544775a3abc557a70
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585224"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a><span data-ttu-id="b2690-103">Odstraňování potíží s platebním konektorem Dynamics 365 pro Adyen</span><span class="sxs-lookup"><span data-stu-id="b2690-103">Troubleshoot Dynamics 365 Payment Connector for Adyen issues</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b2690-104">Toto téma poskytuje pokyny pro řešení potíží, které vám mohou pomoci získat podporu, když máte problémy s Platebním konektorem Microsoft Dynamics 365 pro Adyen.</span><span class="sxs-lookup"><span data-stu-id="b2690-104">This topic provides troubleshooting guidance that can help you get support when you have issues with the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span>

## <a name="description"></a><span data-ttu-id="b2690-105">popis</span><span class="sxs-lookup"><span data-stu-id="b2690-105">Description</span></span>

<span data-ttu-id="b2690-106">Máte problémy s Platebním konektorem Dynamics 365 pro Adyen v následujících oblastech a potřebujete podporu od týmu Adyen:</span><span class="sxs-lookup"><span data-stu-id="b2690-106">You have issues with the Dynamics 365 Payment Connector for Adyen in the following areas, and you require support from the Adyen team:</span></span>

- <span data-ttu-id="b2690-107">Konfigurace pokladního místa (POS), moderního pokladního místa (MPOS), call centra nebo Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b2690-107">Configuration of Point of sale (POS), Modern point of sale (MPOS), call center, or Dynamics 365 Commerce</span></span>
- <span data-ttu-id="b2690-108">Referenční číslo poskytovatele platebních služeb Adyen (PSP) (například pokud máte dotazy ohledně odmítnutí, včetně odmítnutí ručního zadání klíče \[MKE\])</span><span class="sxs-lookup"><span data-stu-id="b2690-108">The Adyen payment service provider (PSP) reference number (for example, if you have questions about refusals, including manual key entry \[MKE\] refusals)</span></span>
- <span data-ttu-id="b2690-109">Cokoli, co nefunguje v testovacím nebo živém obchodním prostředí</span><span class="sxs-lookup"><span data-stu-id="b2690-109">Anything that isn't working in test or live merchant environments</span></span>

## <a name="resolution"></a><span data-ttu-id="b2690-110">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="b2690-110">Resolution</span></span>

<span data-ttu-id="b2690-111">Pomocí následující e-mailové šablony zahájíte proces podpory s týmem Adyen.</span><span class="sxs-lookup"><span data-stu-id="b2690-111">Use the following email template to start the support process with the Adyen team.</span></span> <span data-ttu-id="b2690-112">Chcete-li urychlit odstraňování problémů, ujistěte se, že e-mail obsahuje všechny požadované podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="b2690-112">To expedite troubleshooting, make sure that the email contains all the required details.</span></span>

| <span data-ttu-id="b2690-113">Pole</span><span class="sxs-lookup"><span data-stu-id="b2690-113">Field</span></span>        | <span data-ttu-id="b2690-114">Hodnota</span><span class="sxs-lookup"><span data-stu-id="b2690-114">Value</span></span> |
|--------------|-------|
| <span data-ttu-id="b2690-115">Do</span><span class="sxs-lookup"><span data-stu-id="b2690-115">To</span></span>           | `support@adyen.com` |
| <span data-ttu-id="b2690-116">Kopie</span><span class="sxs-lookup"><span data-stu-id="b2690-116">Cc</span></span>           | |
| <span data-ttu-id="b2690-117">Řádek předmětu</span><span class="sxs-lookup"><span data-stu-id="b2690-117">Subject line</span></span> | <span data-ttu-id="b2690-118">Požadavek na podporu Microsoft Dynamics</span><span class="sxs-lookup"><span data-stu-id="b2690-118">Microsoft Dynamics Support Request</span></span> |
| <span data-ttu-id="b2690-119">Hlavní část</span><span class="sxs-lookup"><span data-stu-id="b2690-119">Body</span></span>         | <p><span data-ttu-id="b2690-120">Dobrý den, podporo.</span><span class="sxs-lookup"><span data-stu-id="b2690-120">Hi Support,</span></span></p><p><span data-ttu-id="b2690-121">Poskytněte podporu pro následující problém:</span><span class="sxs-lookup"><span data-stu-id="b2690-121">Please provide support for the following issue:</span></span></p><ul><li><span data-ttu-id="b2690-122">Účet obchodníka</span><span class="sxs-lookup"><span data-stu-id="b2690-122">Merchant account</span></span></li><li><span data-ttu-id="b2690-123">Prostředí (test/prod)</span><span class="sxs-lookup"><span data-stu-id="b2690-123">Environment (Test/Prod)</span></span></li><li><span data-ttu-id="b2690-124">Kanál (POS / call centrum / elektronický obchod Commerce)</span><span class="sxs-lookup"><span data-stu-id="b2690-124">Channel (POS/call center/Commerce e-commerce)</span></span></li><li><span data-ttu-id="b2690-125">Referenční číslo PSP, pokud problém zahrnoval konkrétní transakci (referenční číslo PSP najdete na účtence, v Zákaznické oblasti Adyen nebo v nabídce transakcí na terminálu POS.)</span><span class="sxs-lookup"><span data-stu-id="b2690-125">PSP reference number, if the issue involved a specific transaction (You can find the PSP reference number on the receipt, in the Adyen Customer Area, or on the transactions menu on the POS terminal.)</span></span></li><li><span data-ttu-id="b2690-126">Screenshot nebo fotografie chybové zprávy, pokud existují</span><span class="sxs-lookup"><span data-stu-id="b2690-126">Screenshot or photo of the error message, if applicable</span></span></li><li><span data-ttu-id="b2690-127">Protokoly Prohlížeče událostí (ve formátu .txt)</span><span class="sxs-lookup"><span data-stu-id="b2690-127">Event Viewer logs (in .txt format)</span></span></li><li><span data-ttu-id="b2690-128">Popis problému a kroky k řešení potíží, které jste vyzkoušeli</span><span class="sxs-lookup"><span data-stu-id="b2690-128">Description of the issue and troubleshooting steps that you've tried</span></span></li></ul> |

## <a name="additional-resources"></a><span data-ttu-id="b2690-129">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="b2690-129">Additional resources</span></span>

[<span data-ttu-id="b2690-130">Příjem plateb pomocí konektoru Adyen pro Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b2690-130">Accept payments with the Adyen connector for Dynamics 365 Commerce</span></span>](https://www.adyen.com/partners/dynamics-365-commerce)

[<span data-ttu-id="b2690-131">Platební konektor Dynamics 365 pro Adyen</span><span class="sxs-lookup"><span data-stu-id="b2690-131">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="b2690-132">Nastavení konektoru plateb Adyen pro Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b2690-132">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
