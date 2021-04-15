---
title: Konfigurace parametrů správy zaměstnaneckých výhod podle společnosti
description: Nakonfigurujte parametry pro správu zaměstnaneckých výhod podle společnosti v Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 87d4f1e7580b333fd17d3b779aafa47c5baed424
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805651"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="c3752-103">Konfigurace parametrů správy zaměstnaneckých výhod podle společnosti</span><span class="sxs-lookup"><span data-stu-id="c3752-103">Configure Benefits management parameters per company</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c3752-104">Pro každou organizaci, která nabízí zaměstnanecké výhody, musíte nakonfigurovat nastavení e-mailů s potvrzením zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="c3752-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="c3752-105">Konfigurace nastavení e-mailu s potvrzením</span><span class="sxs-lookup"><span data-stu-id="c3752-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="c3752-106">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Parametry lidských zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="c3752-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="c3752-107">Na kartě **Správa zaměstnaneckých výhod** zadejte hodnoty pro následující pole:</span><span class="sxs-lookup"><span data-stu-id="c3752-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="c3752-108">Pole</span><span class="sxs-lookup"><span data-stu-id="c3752-108">Field</span></span> | <span data-ttu-id="c3752-109">popis</span><span class="sxs-lookup"><span data-stu-id="c3752-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c3752-110">**Odeslat e-mail s potvrzením**</span><span class="sxs-lookup"><span data-stu-id="c3752-110">**Send confirmation email**</span></span> | <span data-ttu-id="c3752-111">Když je tato funkce zapnutá, bude zaměstnancům zaslán potvrzovací e-mail, když se registrují k zaměstnaneckým výhodám v samoobsluze pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="c3752-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="c3752-112">**E-mailová šablona pro potvrzení**</span><span class="sxs-lookup"><span data-stu-id="c3752-112">**Confirmation email template**</span></span> | <span data-ttu-id="c3752-113">Vyberte šablonu e-mailu organizace, kterou chcete použít k odeslání potvrzení registrace.</span><span class="sxs-lookup"><span data-stu-id="c3752-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="c3752-114">Pokud nevyberete šablonu, bude zaslán následující obecný e-mail:</span><span class="sxs-lookup"><span data-stu-id="c3752-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="c3752-115">%EmployeeFirstName%,</span><span class="sxs-lookup"><span data-stu-id="c3752-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="c3752-116">Gratulujeme!</span><span class="sxs-lookup"><span data-stu-id="c3752-116">Congratulations!</span></span> <span data-ttu-id="c3752-117">úspěšně jste se registrovali k zaměstnaneckým výhodám.</span><span class="sxs-lookup"><span data-stu-id="c3752-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="c3752-118">Děkujeme,</span><span class="sxs-lookup"><span data-stu-id="c3752-118">Thank you,</span></span><br><span data-ttu-id="c3752-119">Zaměstnanecké výhody společnosti <název společnosti/organizace>.</span><span class="sxs-lookup"><span data-stu-id="c3752-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="c3752-120">**Výchozí e-mailová adresa odesílatele**</span><span class="sxs-lookup"><span data-stu-id="c3752-120">**Default email sender address**</span></span> | <span data-ttu-id="c3752-121">E-mailová adresa, která se použije k odeslání potvrzovacího e-mailu.</span><span class="sxs-lookup"><span data-stu-id="c3752-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="c3752-122">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="c3752-122">Select **Save**.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]