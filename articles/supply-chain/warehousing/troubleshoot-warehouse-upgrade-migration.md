---
title: Odstraňování problémů s upgradem a migrací na pokročilou správu skladu
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s upgradem a migrací na pokročilou správu skladu.
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
ms.openlocfilehash: f5bfee31ce27e919086f978fb3ff88ca61a65eba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208080"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a><span data-ttu-id="c40ed-103">Odstraňování problémů s upgradem a migrací na pokročilou správu skladu</span><span class="sxs-lookup"><span data-stu-id="c40ed-103">Troubleshoot upgrade and migration to advanced warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c40ed-104">Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s upgradem a migrací na pokročilou správu skladu.</span><span class="sxs-lookup"><span data-stu-id="c40ed-104">This topic describes how to fix common issues that you might encounter while you upgrade and migrate to advanced warehouse management.</span></span>

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a><span data-ttu-id="c40ed-105">Zobrazuje se následující chybová zpráva: „java.security.cert.certPathValidatorException: Nebyla nalezena důvěryhodná kotva pro certifikační cestu.“</span><span class="sxs-lookup"><span data-stu-id="c40ed-105">I receive the following error message: "java.security.cert.certPathValidatorException: Trust anchor for certification path is not found."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c40ed-106">Popis problému</span><span class="sxs-lookup"><span data-stu-id="c40ed-106">Issue description</span></span>

<span data-ttu-id="c40ed-107">Tato chybová zpráva se zobrazí v aplikaci skladu, protože certifikáty podepsané svým držitelem nejsou důvěryhodné v Android 8+ v místních prostředích.</span><span class="sxs-lookup"><span data-stu-id="c40ed-107">You receive this error message in the warehouse app, because self-signed certificates aren't trusted on Android 8+ in on-premises environments.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c40ed-108">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="c40ed-108">Issue resolution</span></span>

<span data-ttu-id="c40ed-109">Použijte externí (veřejný) certifikační autoritu (CA).</span><span class="sxs-lookup"><span data-stu-id="c40ed-109">Use an external (public) certifying authority (CA).</span></span> <span data-ttu-id="c40ed-110">Oprava tohoto problému je k dispozici ve verzi 1.9.0.0 aplikace skladu.</span><span class="sxs-lookup"><span data-stu-id="c40ed-110">A fix for this issue is available in version 1.9.0.0 of the warehouse app.</span></span> <span data-ttu-id="c40ed-111">Další informace o tomto problému a jeho řešení najdete v tématu [Odstraňování problémů s připojením aplikace skladu](troubleshoot-warehouse-app-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c40ed-111">For more information about this issue and how to fix it, see [Troubleshoot warehouse app connection issues](troubleshoot-warehouse-app-connection.md).</span></span>

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a><span data-ttu-id="c40ed-112">Jaký je schválený proces přechodu od základního skladování k pokročilému skladování?</span><span class="sxs-lookup"><span data-stu-id="c40ed-112">What is the approved process for moving from basic warehousing to advanced warehousing?</span></span>

### <a name="issue-description"></a><span data-ttu-id="c40ed-113">Popis problému</span><span class="sxs-lookup"><span data-stu-id="c40ed-113">Issue description</span></span>

<span data-ttu-id="c40ed-114">Momentálně běžíte pod správou skladu/zásob a používáte základní funkce skladu a chcete přejít na pokročilé skladování, abyste mohli využívat výhod mobilních zařízení, vln a práce.</span><span class="sxs-lookup"><span data-stu-id="c40ed-114">You're currently running under stock/inventory management and using basic stock functionality, and you want to move to advanced warehousing to take advantage of mobile devices, waves, and work.</span></span> <span data-ttu-id="c40ed-115">Při pokusu o tento krok však dochází k problémům.</span><span class="sxs-lookup"><span data-stu-id="c40ed-115">However, you're experiencing issues when you try to make this move.</span></span> <span data-ttu-id="c40ed-116">Například nemůžete změnit své produkty tak, aby používaly dimenze úložiště (web, sklad a umístění), protože produkty mají proti nim transakce.</span><span class="sxs-lookup"><span data-stu-id="c40ed-116">For example, you can't change your products so that they use storage dimensions (site, warehouse, and location), because the products have transactions against them.</span></span> <span data-ttu-id="c40ed-117">Musíte se tedy naučit schválený proces přechodu od základního skladování k pokročilému skladování.</span><span class="sxs-lookup"><span data-stu-id="c40ed-117">Therefore, you must learn the approved process for moving from basic warehousing to advanced warehousing.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c40ed-118">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="c40ed-118">Issue resolution</span></span>

<span data-ttu-id="c40ed-119">Další informace o procesu přechodu ze základního skladování na pokročilé skladování najdete v následujících příspěvcích na blogu a v dokumentaci:</span><span class="sxs-lookup"><span data-stu-id="c40ed-119">For more information about the process for moving from basic warehousing to advanced warehousing, see the following blog posts and documentation:</span></span>

- [<span data-ttu-id="c40ed-120">Povolit procesy správy skladu pro existující položky a sklady</span><span class="sxs-lookup"><span data-stu-id="c40ed-120">Enable warehouse management process for existing items and warehouses</span></span>](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [<span data-ttu-id="c40ed-121">Migrace Microsoft Dynamics AX WMS do nové skladové a přepravní funkce R3</span><span class="sxs-lookup"><span data-stu-id="c40ed-121">Migration of Microsoft Dynamics AX WMS to new R3 warehouse and transportation functionality</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [<span data-ttu-id="c40ed-122">Migrace položek WMSI/WMS2</span><span class="sxs-lookup"><span data-stu-id="c40ed-122">WMSI/WMS2 item migration</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [<span data-ttu-id="c40ed-123">Upgrade správy skladu z Microsoft Dynamics AX 2012 do Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c40ed-123">Upgrade warehouse management from Microsoft Dynamics AX 2012 to Supply Chain Management</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]