---
title: Řešení potíží s příchozími skladovými operacemi
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s příchozími skladovými operacemi v Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 6f6d689c596b4ec924cb50ec3bea8ce907e6dc6b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920980"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="8d51a-103">Řešení potíží s příchozími skladovými operacemi</span><span class="sxs-lookup"><span data-stu-id="8d51a-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d51a-104">Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s příchozími skladovými operacemi v Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8d51a-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="8d51a-105">Zobrazuje se následující chybová zpráva: „Objednávka kvality %1 byla vygenerována.</span><span class="sxs-lookup"><span data-stu-id="8d51a-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="8d51a-106">Profil seskupení nebyl nalezen. Zkontrolujte svou konfiguraci."</span><span class="sxs-lookup"><span data-stu-id="8d51a-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8d51a-107">Popis problému</span><span class="sxs-lookup"><span data-stu-id="8d51a-107">Issue description</span></span>

<span data-ttu-id="8d51a-108">Tato chybová zpráva souvisí s přijímacím procesem, kde je zapnutá správa kvality (QMS).</span><span class="sxs-lookup"><span data-stu-id="8d51a-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="8d51a-109">V závislosti na konfiguracích ve vašem prostředí mohou problém vyřešit další podrobnosti o transakci, která generuje chybovou zprávu.</span><span class="sxs-lookup"><span data-stu-id="8d51a-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8d51a-110">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="8d51a-110">Issue resolution</span></span>

<span data-ttu-id="8d51a-111">Nejprve zkontrolujte nastavení [výdeje v seskupení](set-up-cluster-picking.md) a ujistěte se, že jsou vaše profily seskupení nastaveny správně.</span><span class="sxs-lookup"><span data-stu-id="8d51a-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="8d51a-112">Položku nabídky mobilního zařízení nemůžete použít pro výběr seskupení, pokud nejsou nastaveny profily seskupení.</span><span class="sxs-lookup"><span data-stu-id="8d51a-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="8d51a-113">V závislosti na vašem prostředí budete možná muset zkontrolovat další související konfigurace.</span><span class="sxs-lookup"><span data-stu-id="8d51a-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="8d51a-114">Přijímání smíšených registračních značek nefunguje pro žádný dispoziční kód kromě kreditu.</span><span class="sxs-lookup"><span data-stu-id="8d51a-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8d51a-115">Popis problému</span><span class="sxs-lookup"><span data-stu-id="8d51a-115">Issue description</span></span>

<span data-ttu-id="8d51a-116">Když je pole **Akce** pro kód dispozice je nastaveno na *Kredit* nebo *Odpad*, můžete použít pouze položku nabídky [Přijetí smíšené registrační značky](mixed-license-plate-receiving.md) ke zpracování vrácených položek.</span><span class="sxs-lookup"><span data-stu-id="8d51a-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8d51a-117">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="8d51a-117">Issue resolution</span></span>

<span data-ttu-id="8d51a-118">Společnost Microsoft vyhodnotila tento problém a zjistila, že jde o omezení funkcí.</span><span class="sxs-lookup"><span data-stu-id="8d51a-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="8d51a-119">V současné době jsou pro příjem smíšených registračních značek podporovány pouze [dispoziční kódy](../service-management/set-up-disposition-codes.md), kde je pole **Akce** nastaveno na *Kredit* nebo *Odpad*.</span><span class="sxs-lookup"><span data-stu-id="8d51a-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="8d51a-120">Když spustím pravidelnou úlohu Aktualizovat potvrzení o přijetí produktu, potvrdí se nepotvrzené nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="8d51a-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8d51a-121">Popis problému</span><span class="sxs-lookup"><span data-stu-id="8d51a-121">Issue description</span></span>

<span data-ttu-id="8d51a-122">Po spuštění periodického úkolu *Aktualizovat příjemky produktů* systém automaticky potvrzuje nepotvrzené nákupní objednávky, které mají stav transakce zásob *Registrovaný*.</span><span class="sxs-lookup"><span data-stu-id="8d51a-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8d51a-123">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="8d51a-123">Issue resolution</span></span>

<span data-ttu-id="8d51a-124">Nová funkce zpracování příchozího nákladu *Příjem většího množství nákladu* opravuje tento problém.</span><span class="sxs-lookup"><span data-stu-id="8d51a-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="8d51a-125">Chcete-li tuto funkci zapnout, přejděte k pracovnímu prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte následující funkce (v pořadí, v jakém jsou uvedeny):</span><span class="sxs-lookup"><span data-stu-id="8d51a-125">To turn on this feature, go to the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="8d51a-126">Přiřadit transakce zásob nákupní objednávky k vytížení</span><span class="sxs-lookup"><span data-stu-id="8d51a-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="8d51a-127">Nadměrné přijetí množství vytížení</span><span class="sxs-lookup"><span data-stu-id="8d51a-127">Over receipt of load quantities</span></span>

<span data-ttu-id="8d51a-128">Další informace viz [Zaúčtujte registrované množství produktu oproti nákupním objednávkám](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="8d51a-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a><span data-ttu-id="8d51a-129">Když zaregistruji příchozí objednávky, zobrazí se následující chybová zpráva: „Množství není platné“.</span><span class="sxs-lookup"><span data-stu-id="8d51a-129">When I register inbound orders, I receive the following error message: "The quantity is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8d51a-130">Popis problému</span><span class="sxs-lookup"><span data-stu-id="8d51a-130">Issue description</span></span>

<span data-ttu-id="8d51a-131">Pokud je pole **Zásady seskupování registračních značek** nastaveno na *Definováno uživatelem* pro položku nabídky mobilního zařízení, která je použita k registraci příchozích objednávek, zobrazí se chybová zpráva („Množství není platné“) a registraci nelze dokončit.</span><span class="sxs-lookup"><span data-stu-id="8d51a-131">If the **License plate grouping policy** field is set to *User defined* for a mobile device menu item that is used to register inbound orders, you receive an error message ("The quantity is not valid"), and you can't complete the registration.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="8d51a-132">Příčina problému</span><span class="sxs-lookup"><span data-stu-id="8d51a-132">Issue cause</span></span>

<span data-ttu-id="8d51a-133">Když je *Definováno uživatelem* použito jako zásada pro seskupování registračních značek, systém rozdělí příchozí zásoby na samostatné registrační značky, jak udává skupina klasifikace jednotek.</span><span class="sxs-lookup"><span data-stu-id="8d51a-133">When *User defined* is used as a license plate grouping policy, the system splits the incoming inventory into separate license plates, as indicated by the unit sequence group.</span></span> <span data-ttu-id="8d51a-134">Pokud se ke sledování přijímané položky použije číslo dávky nebo sériové číslo, je třeba zadat množství každé dávky nebo série pro každou registrační značku, která je registrována.</span><span class="sxs-lookup"><span data-stu-id="8d51a-134">If batch or serial numbers are used to track the item that is being received, the quantities of each batch or serial must be specified per license plate that is registered.</span></span> <span data-ttu-id="8d51a-135">Pokud množství, které je zadáno pro registrační značku, překročí množství, které ještě musí být přijato pro aktuální dimenze, zobrazí se chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="8d51a-135">If the quantity that is specified for a license plate exceeds the quantity that must still be received for the current dimensions, you receive the error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8d51a-136">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="8d51a-136">Issue resolution</span></span>

<span data-ttu-id="8d51a-137">Když zaregistrujete položku pomocí položky nabídky mobilního zařízení, kde je pole **Zásady seskupování registračních značek** nastaveno na *Definováno uživatelem*, může systém vyžadovat potvrzení nebo zadání čísel registračních značek, čísel dávek nebo sériových čísel.</span><span class="sxs-lookup"><span data-stu-id="8d51a-137">When you register an item by using a mobile device menu item where the **License plate grouping policy** field is set to *User defined*, the system might require that you confirm or enter license plate numbers, batch numbers, or serial numbers.</span></span>

<span data-ttu-id="8d51a-138">Na potvrzovací stránce registrační značky systém zobrazí množství, které je přiděleno pro aktuální registrační značku.</span><span class="sxs-lookup"><span data-stu-id="8d51a-138">On the license plate confirmation page, the system will show the quantity that is allocated for the current license plate.</span></span> <span data-ttu-id="8d51a-139">Na potvrzovací stránce dávky nebo série systém zobrazí množství, které ještě musí být přijato pro aktuální registrační značku.</span><span class="sxs-lookup"><span data-stu-id="8d51a-139">On the batch or serial confirmation pages, the system will show the quantity that must still be received on the current license plate.</span></span> <span data-ttu-id="8d51a-140">Bude také obsahovat pole, kde můžete zadat množství, které bude registrováno pro tuto kombinaci registrační značky a čísla dávky nebo sériového čísla.</span><span class="sxs-lookup"><span data-stu-id="8d51a-140">It will also include a field where you can enter the quantity to register for that combination of license plate and batch or serial number.</span></span> <span data-ttu-id="8d51a-141">V takovém případě se ujistěte, že množství, které je registrováno pro registrační značku, nepřekročí množství, které ještě musí být přijato.</span><span class="sxs-lookup"><span data-stu-id="8d51a-141">In this case, make sure that the quantity that is being registered for the license plate doesn't exceed the quantity that must still be received.</span></span>

<span data-ttu-id="8d51a-142">Případně pokud se při registraci příchozí objednávky vygeneruje příliš mnoho registračních značek, hodnotu pole **Zásady seskupování registračních značek** lze změnit na *Seskupení registračních značek*, položce lze přiřadit novou skupinu klasifikace jednotek nebo možnost **Seskupení registračních značek** pro skupinu klasifikace jednotek může být deaktivována.</span><span class="sxs-lookup"><span data-stu-id="8d51a-142">Alternatively, if too many license plates are being generated on inbound order registration, the value of the **License plate grouping policy** field can be changed to *License plate grouping*, a new unit sequence group can be assigned to the item, or the **License plate grouping** option for the unit sequence group can be inactivated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
