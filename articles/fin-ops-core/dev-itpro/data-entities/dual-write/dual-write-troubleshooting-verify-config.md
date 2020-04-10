---
title: Ověření, zda je v aplikacích Finance and Operations a Common Data Service nakonfigurován duální zápis
description: Toto téma vysvětluje, jak můžete určit, zda je dvojí zápis konfigurován v aplikacích Finance and Operations a Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2f2ba2564ad3e8e444e27fcc0c586ddf252afabd
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172638"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="114ec-103">Ověření, zda je v aplikacích Finance and Operations a Common Data Service nakonfigurován duální zápis</span><span class="sxs-lookup"><span data-stu-id="114ec-103">Verify that dual-write is configured in Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="114ec-104">Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="114ec-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="114ec-105">Konkrétně vysvětluje, jak můžete určit, zda je dvojí zápis konfigurován v aplikacích Finance and Operations a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="114ec-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Common Data Service.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="114ec-106">Ověření, zda je v aplikaci Finance and Operations nakonfigurován duální zápis</span><span class="sxs-lookup"><span data-stu-id="114ec-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="114ec-107">Chcete-li zjistit, zda jsou chyby, které se zobrazí při pokusu o uložení záznamů pro aktualizaci, pocházet z duálního zápisů, ověřte nejprve, zda je konfigurován dvojí zápis.</span><span class="sxs-lookup"><span data-stu-id="114ec-107">To determine whether the errors that you see when you try to save records for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="114ec-108">Máte-li v aplikaci Finance and Operations oprávnění správce, přejděte na možnost **Pracovní prostory \> Správa dat** a vyberte dlaždici **Dvojí zápis**.</span><span class="sxs-lookup"><span data-stu-id="114ec-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="114ec-109">Jsou-li zobrazeny podrobnosti o propojených prostředích a seznam spuštěných map entit, je nakonfigurován dvojí zápis.</span><span class="sxs-lookup"><span data-stu-id="114ec-109">If the details of the linked environments and the list of entity maps that are running are shown, dual-write is configured.</span></span>

    ![Ověřuje se připojení aplikace Finance and Operations, když máte oprávnění správce](media/verify_fin_ops_1.png)

+ <span data-ttu-id="114ec-111">Nemáte-li oprávnění správce, zobrazí se chybová zpráva, *nelze zapsat data do entity \<název entity\>*.</span><span class="sxs-lookup"><span data-stu-id="114ec-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="114ec-112">V příkladu na následujícím obrázku nelze vytvořit záznam odběratele v aplikaci Finance and Operations, protože je nakonfigurován dvojí zápis, ale skupina odběratelů a referenční data platebních podmínek neexistují v Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="114ec-112">In the example in the following illustration, you can't create a customer record in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Common Data Service.</span></span>

    ![Ověřuje se připojení aplikace Finance and Operations, když nemáte oprávnění správce](media/verify_fin_ops_2.png)

<span data-ttu-id="114ec-114">Informace o tom, jak vyřešit problémy při vytváření dat v aplikacích Finance and Operations, naleznete v tématu [Poradce při potížích s synchronizací v ostrém provozu](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="114ec-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a><span data-ttu-id="114ec-115">Ověření, zda je nakonfigurován duální zápis v Common Data Service</span><span class="sxs-lookup"><span data-stu-id="114ec-115">Verify that dual-write is configured in Common Data Service</span></span>

<span data-ttu-id="114ec-116">Pokud se při vytváření dat nachází pole **Společnost** na stránkách v aplikaci Common Data Service, je nakonfigurováno dvojí zapisování.</span><span class="sxs-lookup"><span data-stu-id="114ec-116">When you create data, if you see the **Company** field on pages in Common Data Service, dual-write is configured.</span></span>

![Ověřování připojení Common Data Service](media/verify_cds.png)

<span data-ttu-id="114ec-118">Informace o tom, jak vyřešit problémy při vytváření dat v Common Data Service, naleznete v tématu [Poradce při potížích s synchronizací v ostrém provozu](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="114ec-118">For information about how to fix issues when you create data in Common Data Service, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="114ec-119">Informace o tom, jak zobrazit podrobnosti chyb při vytváření dat v Common Data Service, naleznete v tématu [Povolení a zobrazení protokolu sledování modulu plug-in v aplikaci Common Data Service, kde jsou zobrazeny podrobnosti o chybě](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span><span class="sxs-lookup"><span data-stu-id="114ec-119">For information about how to view error details if you encounter any errors while you create data in Common Data Service, see [Enable and view the plug-in trace log in Common Data Service to view error details](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span></span>
