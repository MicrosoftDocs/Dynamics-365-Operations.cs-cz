---
title: Příjem registračních značek prostřednictvím mobilní aplikace Warehousing
description: V tomto tématu je vysvětleno, jak nastavit mobilní aplikaci Warehousing na podporu použití procesu příjmu registračních značek pro příjem fyzických zásob.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 98cd608edea1d5365d0d3532244f1fcdb6293d3c
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261310"
---
# <a name="license-plate-receiving-via-the-warehousing-mobile-app"></a><span data-ttu-id="1ec3e-103">Příjem registračních značek prostřednictvím mobilní aplikace Warehousing</span><span class="sxs-lookup"><span data-stu-id="1ec3e-103">License plate receiving via the Warehousing mobile app</span></span>

<span data-ttu-id="1ec3e-104">V tomto tématu je vysvětleno, jak nastavit mobilní aplikaci Warehousing, aby podporovala použití procesu příjmu registračních značek pro příjem fyzických zásob.</span><span class="sxs-lookup"><span data-stu-id="1ec3e-104">This topic explains how to set up the Warehousing mobile app so that it supports using a license plate receiving process to receive physical inventory.</span></span>

<span data-ttu-id="1ec3e-105">Pomocí této funkce můžete rychle zaznamenat příjem příchozích zásob, který souvisí s avízem expedice zboží (ASN).</span><span class="sxs-lookup"><span data-stu-id="1ec3e-105">You can use this functionality to quickly record the receipt of inbound inventory that is related to an advance ship notice (ASN).</span></span> <span data-ttu-id="1ec3e-106">Systém při expedici převodního příkazu procesy správy skladu automaticky vytvoří avízo expedice zboží.</span><span class="sxs-lookup"><span data-stu-id="1ec3e-106">The system automatically creates an ASN when warehouse management processes are used to ship a transfer order.</span></span> <span data-ttu-id="1ec3e-107">U procesu nákupní objednávky lze ASN zaznamenat ručně nebo je lze automaticky importovat pomocí procesu příchozí datové entity ASN.</span><span class="sxs-lookup"><span data-stu-id="1ec3e-107">For the purchase order process, an ASN can be manually recorded, or it can be automatically imported by using an inbound ASN data entity process.</span></span>

<span data-ttu-id="1ec3e-108">Data ASN jsou spojena s náklady a zásilkami prostřednictvím *struktur balení*, kde palety (nadřazené registrační značky) mohou obsahovat případy (vnořené registrační značky).</span><span class="sxs-lookup"><span data-stu-id="1ec3e-108">The ASN data is linked to loads and shipments via the *packing structures*, where pallets (parent license plates) can contain cases (nested license plates).</span></span>

> [!NOTE]
> <span data-ttu-id="1ec3e-109">Chcete-li snížit počet skladových transakcí v případě, že jsou použity struktury balení, které mají vnořené registrační značky, systém zaznamená fyzické množství na skladě na nadřízené registrační značce.</span><span class="sxs-lookup"><span data-stu-id="1ec3e-109">To reduce the number of inventory transactions when packing structures that have nested license plates are used, the system records the physical on-hand inventory on the parent license plate.</span></span> <span data-ttu-id="1ec3e-110">Chcete-li aktivovat pohyb fyzického množství na skladě z nadřazené registrační značky na základě dat struktury balení, musí mobilní zařízení poskytnout položku nabídky, která je založena na procesu tvorby práce *Zabalit do vnořených registračních značek*.</span><span class="sxs-lookup"><span data-stu-id="1ec3e-110">To trigger the movement of the physical on-hand inventory from the parent license plate to the nested license plates, based on the packing structure data, the mobile device must provide a menu item that is based on the *Pack to nested license plates* work creation process.</span></span>

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a><span data-ttu-id="1ec3e-111">Zobrazit nebo přeskočit stránku Souhrn přijetí</span><span class="sxs-lookup"><span data-stu-id="1ec3e-111">Show or skip the receiving summary page</span></span>

<span data-ttu-id="1ec3e-112">Můžete použít funkci *Určit, zda zobrazit stránku souhn upříjmu na mobilních zařízeních*, chcete-li využít další detailní tok aplikací Warehouse v rámci procesu získávání registrační značky.</span><span class="sxs-lookup"><span data-stu-id="1ec3e-112">You can use the *Control whether to display a receiving summary page on mobile devices* feature to take advantage of an additional detailed Warehouse app flow as part of the license plate receiving process.</span></span>

<span data-ttu-id="1ec3e-113">Než můžete použít tuto funkci, musíte ji zapnout ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="1ec3e-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="1ec3e-114">Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji.</span><span class="sxs-lookup"><span data-stu-id="1ec3e-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="1ec3e-115">V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:</span><span class="sxs-lookup"><span data-stu-id="1ec3e-115">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="1ec3e-116">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="1ec3e-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="1ec3e-117">**Název funkce:** *Určit, zda zobrazit stránku souhn upříjmu na mobilních zařízeních*</span><span class="sxs-lookup"><span data-stu-id="1ec3e-117">**Feature name:** *Control whether to display a receiving summary page on mobile devices*</span></span>

<span data-ttu-id="1ec3e-118">Je-li tato funkce zapnuta, položky nabídky mobilního zařízení pro příjem registračních značek nebo příjem a zaskladnění registračních značek poskytnou nastavení **Zobrazit stránku souhnu příjmu**.</span><span class="sxs-lookup"><span data-stu-id="1ec3e-118">When this feature is turned on, mobile device menu items for license plate receiving or license plate receiving and put-away will provide a **Display receiving summary page** setting.</span></span> <span data-ttu-id="1ec3e-119">Toto nastavení má následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="1ec3e-119">This setting has the following options:</span></span>

- <span data-ttu-id="1ec3e-120">**Zobrazit podrobný souhrn** – během příjmu registrační značky se zaměstnanci zobrazí další stránka s úplnými informacemi o ASN.</span><span class="sxs-lookup"><span data-stu-id="1ec3e-120">**Display a detailed summary** – During license plate receiving, workers will see an extra page that shows the full ASN information.</span></span>
- <span data-ttu-id="1ec3e-121">**Přeskočit souhrn** – pracovníci nebudou moci zobrazit úplné informace o ASN.</span><span class="sxs-lookup"><span data-stu-id="1ec3e-121">**Skip the summary** – Workers won't see the full ASN information.</span></span> <span data-ttu-id="1ec3e-122">Pracovníci skladu také nebudou moci v průběhu procesu příjmu nastavovat dispoziční kód ani přidávat výjimky.</span><span class="sxs-lookup"><span data-stu-id="1ec3e-122">Warehouse workers also won't be able to set a disposition code or add exceptions during the receiving process.</span></span>

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a><span data-ttu-id="1ec3e-123">Zabránit použití převodním příkazem expedovaných registračních značek v jiných skladech než je cílový Sklad</span><span class="sxs-lookup"><span data-stu-id="1ec3e-123">Prevent transfer order–shipped license plates from being used at warehouses other than the destination warehouse</span></span>

<span data-ttu-id="1ec3e-124">Proces příjmu registrační značky je možné použít v případě, že ASN obsahuje ID registrační značky, které již existuje, a má fyzická data na skladě v jiném skladovém místě, než je skladové místo, kde se registrují registrační značky.</span><span class="sxs-lookup"><span data-stu-id="1ec3e-124">A license plate receiving process can't be used if an ASN contains a license plate ID that already exists and has physical on-hand data at a warehouse location other than the warehouse location where the license plate registration is occurring.</span></span>

<span data-ttu-id="1ec3e-125">Pro scénáře převodního příkazu, u nichž tranzitní sklad nesleduje registrační značky (a proto nesleduje fyzické zásoby na skladě na registrační značku), můžete pomocí funkce *Zabránit použití převodním příkazem expedovaných registračních značek v jiných skladech než je cílový sklad*, aby se zabránilo fyzické aktualizaci množství na skladě u registračních značek, které jsou v tranzitu.</span><span class="sxs-lookup"><span data-stu-id="1ec3e-125">For transfer order scenarios where the transit warehouse doesn't track license plates (and therefore also doesn't track physical on-hand inventory per license plate), you can use the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature to prevent physical on-hand updates of license plates that are in transit.</span></span>

<span data-ttu-id="1ec3e-126">Než můžete použít tuto funkci, musíte ji zapnout ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="1ec3e-126">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="1ec3e-127">Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji.</span><span class="sxs-lookup"><span data-stu-id="1ec3e-127">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="1ec3e-128">V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:</span><span class="sxs-lookup"><span data-stu-id="1ec3e-128">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="1ec3e-129">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="1ec3e-129">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="1ec3e-130">**Název funkcee:** *Zabránit použití převodním příkazem expedovaných registračních značek v jiných skladech než je cílový sklad*</span><span class="sxs-lookup"><span data-stu-id="1ec3e-130">**Feature name:** *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse*</span></span>

<span data-ttu-id="1ec3e-131">Chcete-li spravovat funkce, když je tato funkce dostupná, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="1ec3e-131">To manage the functionality when this feature is available, follow these steps.</span></span>

1. <span data-ttu-id="1ec3e-132">Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**.</span><span class="sxs-lookup"><span data-stu-id="1ec3e-132">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="1ec3e-133">Na kartě **Obecné**, na pevné záložce **Registrační značky** nastavte pole **Zásady tranzitu registračních značek skladu** na jednu z následujících hodnot:</span><span class="sxs-lookup"><span data-stu-id="1ec3e-133">On the **General** tab, on the **License plates** FastTab, set the **Transit warehouse license plate policy** field to one of the following values:</span></span>

    - <span data-ttu-id="1ec3e-134">**Povolit opakované použití nesledované registrační značky** - systém pracuje stejným způsobem, když není k dispozici funkce *Zabránit použití převodním příkazem expedovaných registračních značek v jiných skladech než je cílový sklad*.</span><span class="sxs-lookup"><span data-stu-id="1ec3e-134">**Allow reuse of non-tracked license plate** – The system works the same way that it works when the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature isn't available.</span></span> <span data-ttu-id="1ec3e-135">Tato hodnota je výchozím nastavením při prvním zapnutí funkce.</span><span class="sxs-lookup"><span data-stu-id="1ec3e-135">This value is the default setting when you first activate the feature.</span></span>
    - <span data-ttu-id="1ec3e-136">**Zabránit opakovanému použití nesledované registrační značky** – budou povoleny pouze aktualizace množství na skladě, které souvisí s odeslanou registrační značkou v cílovém skladě, dokud nebude přijat převodní příkaz.</span><span class="sxs-lookup"><span data-stu-id="1ec3e-136">**Prevent reuse of non-tracked license plate** – Only on-hand updates that are related to a shipped license plate will be allowed at the destination warehouse until the transfer order has been received.</span></span>

## <a name="more-information"></a><span data-ttu-id="1ec3e-137">Další informace</span><span class="sxs-lookup"><span data-stu-id="1ec3e-137">More information</span></span>

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

<span data-ttu-id="1ec3e-138">Další informace o položkách nabídky mobilního zařízení naleznete v tématu [Nastavení mobilních zařízení pro práci ve skladu](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="1ec3e-138">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>
