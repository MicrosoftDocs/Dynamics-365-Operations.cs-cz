---
title: Vrácení peněz za vrácenou objednávku je odmítnuto
description: Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když je vrácení platby za vrácenou objednávku odmítnuto, protože kreditní karta použitá k fakturaci se liší od karty použité během původní autorizace platby.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: 99fd4b816b1a3a1fe3c2d1579be45b43fdc3d385
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020749"
---
# <a name="refund-on-a-return-order-is-declined"></a><span data-ttu-id="9db02-103">Vrácení peněz za vrácenou objednávku je odmítnuto</span><span class="sxs-lookup"><span data-stu-id="9db02-103">Refund on a return order is declined</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9db02-104">Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když je vrácení platby za vrácenou objednávku odmítnuto, protože kreditní karta použitá k fakturaci se liší od karty použité během původní autorizace platby.</span><span class="sxs-lookup"><span data-stu-id="9db02-104">This topic provides troubleshooting guidance that can help when a refund on a return order is declined because the credit card that is used for invoicing differs from the card that was used during the original payment authorization.</span></span>

## <a name="description"></a><span data-ttu-id="9db02-105">popis</span><span class="sxs-lookup"><span data-stu-id="9db02-105">Description</span></span>

<span data-ttu-id="9db02-106">Vrácení peněz je odmítnuto, pokud se kreditní karta použitá k fakturaci zpáteční objednávky liší od karty použité při původní autorizaci platby.</span><span class="sxs-lookup"><span data-stu-id="9db02-106">A refund is declined when the credit card that is used to invoice a return order differs from the card that was used during the original payment authorization.</span></span> <span data-ttu-id="9db02-107">Zobrazí se následující chybová zpráva: „Některé platby nejsou pro zaúčtování ve správném stavu.</span><span class="sxs-lookup"><span data-stu-id="9db02-107">You receive the following error message: "Some payments are not in the correct status for posting.</span></span> <span data-ttu-id="9db02-108">Před fakturací prosím znovu ověřte stav všech plateb.“</span><span class="sxs-lookup"><span data-stu-id="9db02-108">Please re-validate the status of all payments prior to invoicing."</span></span>

<span data-ttu-id="9db02-109">Podrobnosti o autorizaci platby budou obsahovat následující chybovou zprávu: „Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"</span><span class="sxs-lookup"><span data-stu-id="9db02-109">The payment authorization details will include the following error message: "Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"</span></span>

![Zamítnutá refundace při chybě objednávky vrácení](media/refund-order-decline.jpg)

## <a name="resolution"></a><span data-ttu-id="9db02-111">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="9db02-111">Resolution</span></span>

### <a name="enable-blind-returns-in-adyen"></a><span data-ttu-id="9db02-112">Povolit slepé vrácení v Adyen</span><span class="sxs-lookup"><span data-stu-id="9db02-112">Enable blind returns in Adyen</span></span>

<span data-ttu-id="9db02-113">Chcete-li povolit vracení naslepo, postupujte podle pokynů v [Odstraňování potíží s platebním konektorem Dynamics 365 pro Adyen](adyen-support.md) ke kontaktování týmu podpory Adyen a požádání o povolení vrácení peněz na vašem obchodním účtu Adyen.</span><span class="sxs-lookup"><span data-stu-id="9db02-113">To enable blind returns, follow the steps in [Troubleshoot Dynamics 365 Payment Connector for Adyen issues](adyen-support.md) to contact the Adyen support team and request that blind returns be enabled on your Adyen merchant account.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9db02-114">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="9db02-114">Additional resources</span></span>

[<span data-ttu-id="9db02-115">Platební konektor Dynamics 365 pro Adyen</span><span class="sxs-lookup"><span data-stu-id="9db02-115">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="9db02-116">Nastavení konektoru plateb Adyen pro Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="9db02-116">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
