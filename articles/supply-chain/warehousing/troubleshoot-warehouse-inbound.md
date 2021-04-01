---
title: Řešení potíží s příchozími skladovými operacemi
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s příchozími skladovými operacemi v Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6875c3c644b9993a384ba4d8623640536d7307e1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250875"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="0d89b-103">Řešení potíží s příchozími skladovými operacemi</span><span class="sxs-lookup"><span data-stu-id="0d89b-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d89b-104">Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s příchozími skladovými operacemi v Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0d89b-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="0d89b-105">Zobrazuje se následující chybová zpráva: „Objednávka kvality %1 byla vygenerována.</span><span class="sxs-lookup"><span data-stu-id="0d89b-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="0d89b-106">Profil seskupení nebyl nalezen. Zkontrolujte svou konfiguraci."</span><span class="sxs-lookup"><span data-stu-id="0d89b-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="0d89b-107">Popis problému</span><span class="sxs-lookup"><span data-stu-id="0d89b-107">Issue description</span></span>

<span data-ttu-id="0d89b-108">Tato chybová zpráva souvisí s přijímacím procesem, kde je zapnutá správa kvality (QMS).</span><span class="sxs-lookup"><span data-stu-id="0d89b-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="0d89b-109">V závislosti na konfiguracích ve vašem prostředí mohou problém vyřešit další podrobnosti o transakci, která generuje chybovou zprávu.</span><span class="sxs-lookup"><span data-stu-id="0d89b-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0d89b-110">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="0d89b-110">Issue resolution</span></span>

<span data-ttu-id="0d89b-111">Nejprve zkontrolujte nastavení [výdeje v seskupení](set-up-cluster-picking.md) a ujistěte se, že jsou vaše profily seskupení nastaveny správně.</span><span class="sxs-lookup"><span data-stu-id="0d89b-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="0d89b-112">Položku nabídky mobilního zařízení nemůžete použít pro výběr seskupení, pokud nejsou nastaveny profily seskupení.</span><span class="sxs-lookup"><span data-stu-id="0d89b-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="0d89b-113">V závislosti na vašem prostředí budete možná muset zkontrolovat další související konfigurace.</span><span class="sxs-lookup"><span data-stu-id="0d89b-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="0d89b-114">Přijímání smíšených registračních značek nefunguje pro žádný dispoziční kód kromě kreditu.</span><span class="sxs-lookup"><span data-stu-id="0d89b-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="0d89b-115">Popis problému</span><span class="sxs-lookup"><span data-stu-id="0d89b-115">Issue description</span></span>

<span data-ttu-id="0d89b-116">Když je pole **Akce** pro kód dispozice je nastaveno na *Kredit* nebo *Odpad*, můžete použít pouze položku nabídky [Přijetí smíšené registrační značky](mixed-license-plate-receiving.md) ke zpracování vrácených položek.</span><span class="sxs-lookup"><span data-stu-id="0d89b-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0d89b-117">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="0d89b-117">Issue resolution</span></span>

<span data-ttu-id="0d89b-118">Společnost Microsoft vyhodnotila tento problém a zjistila, že jde o omezení funkcí.</span><span class="sxs-lookup"><span data-stu-id="0d89b-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="0d89b-119">V současné době jsou pro příjem smíšených registračních značek podporovány pouze [dispoziční kódy](../service-management/set-up-disposition-codes.md), kde je pole **Akce** nastaveno na *Kredit* nebo *Odpad*.</span><span class="sxs-lookup"><span data-stu-id="0d89b-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="0d89b-120">Když spustím pravidelnou úlohu Aktualizovat potvrzení o přijetí produktu, potvrdí se nepotvrzené nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="0d89b-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="0d89b-121">Popis problému</span><span class="sxs-lookup"><span data-stu-id="0d89b-121">Issue description</span></span>

<span data-ttu-id="0d89b-122">Po spuštění periodického úkolu *Aktualizovat příjemky produktů* systém automaticky potvrzuje nepotvrzené nákupní objednávky, které mají stav transakce zásob *Registrovaný*.</span><span class="sxs-lookup"><span data-stu-id="0d89b-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0d89b-123">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="0d89b-123">Issue resolution</span></span>

<span data-ttu-id="0d89b-124">Nová funkce zpracování příchozího nákladu *Příjem většího množství nákladu* opravuje tento problém.</span><span class="sxs-lookup"><span data-stu-id="0d89b-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="0d89b-125">Chcete-li tuto funkci zapnout, přejděte na [správu funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte následující funkce (v pořadí, v jakém jsou uvedeny):</span><span class="sxs-lookup"><span data-stu-id="0d89b-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="0d89b-126">Přiřadit transakce zásob nákupní objednávky k vytížení</span><span class="sxs-lookup"><span data-stu-id="0d89b-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="0d89b-127">Nadměrné přijetí množství vytížení</span><span class="sxs-lookup"><span data-stu-id="0d89b-127">Over receipt of load quantities</span></span>

<span data-ttu-id="0d89b-128">Další informace viz [Zaúčtujte registrované množství produktu oproti nákupním objednávkám](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="0d89b-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]