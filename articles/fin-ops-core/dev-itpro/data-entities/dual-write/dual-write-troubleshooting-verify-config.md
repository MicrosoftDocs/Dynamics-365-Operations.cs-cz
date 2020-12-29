---
title: Ověření, zda je v aplikacích Finance and Operations a Dataverse nakonfigurován duální zápis
description: Toto téma vysvětluje, jak můžete určit, zda je dvojí zápis konfigurován v aplikacích Finance and Operations a Dataverse.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f389bcf133cc7e6a086167d5e26c1b8795d0fa30
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685532"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-dataverse"></a><span data-ttu-id="deeaa-103">Ověření, zda je v aplikacích Finance and Operations a Dataverse nakonfigurován duální zápis</span><span class="sxs-lookup"><span data-stu-id="deeaa-103">Verify that dual-write is configured in Finance and Operations apps and Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="deeaa-104">Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="deeaa-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="deeaa-105">Konkrétně vysvětluje, jak můžete určit, zda je dvojí zápis konfigurován v aplikacích Finance and Operations a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="deeaa-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Dataverse.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="deeaa-106">Ověření, zda je v aplikaci Finance and Operations nakonfigurován duální zápis</span><span class="sxs-lookup"><span data-stu-id="deeaa-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="deeaa-107">Chcete-li zjistit, zda jsou chyby, které se zobrazí při pokusu o uložení řádků pro aktualizaci, pocházet z duálního zápisů, ověřte nejprve, zda je konfigurován dvojí zápis.</span><span class="sxs-lookup"><span data-stu-id="deeaa-107">To determine whether the errors that you see when you try to save rows for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="deeaa-108">Máte-li v aplikaci Finance and Operations oprávnění správce, přejděte na možnost **Pracovní prostory \> Správa dat** a vyberte dlaždici **Dvojí zápis**.</span><span class="sxs-lookup"><span data-stu-id="deeaa-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="deeaa-109">Jsou-li zobrazeny podrobnosti o propojených prostředích a seznam spuštěných map tabulek, je nakonfigurován dvojí zápis.</span><span class="sxs-lookup"><span data-stu-id="deeaa-109">If the details of the linked environments and the list of table maps that are running are shown, dual-write is configured.</span></span>

    ![Ověřuje se připojení aplikace Finance and Operations, když máte oprávnění správce](media/verify_fin_ops_1.png)

+ <span data-ttu-id="deeaa-111">Nemáte-li oprávnění správce, zobrazí se chybová zpráva *Nelze zapsat data do entity \<entity name\>*.</span><span class="sxs-lookup"><span data-stu-id="deeaa-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="deeaa-112">V příkladu na následujícím obrázku nelze vytvořit řádek odběratele v aplikaci Finance and Operations, protože je nakonfigurován dvojí zápis, ale skupina odběratelů a referenční data platebních podmínek neexistují v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="deeaa-112">In the example in the following illustration, you can't create a customer row in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Dataverse.</span></span>

    ![Ověřuje se připojení aplikace Finance and Operations, když nemáte oprávnění správce](media/verify_fin_ops_2.png)

<span data-ttu-id="deeaa-114">Informace o tom, jak vyřešit problémy při vytváření dat v aplikacích Finance and Operations, naleznete v tématu [Poradce při potížích s synchronizací v ostrém provozu](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="deeaa-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a><span data-ttu-id="deeaa-115">Ověření, zda je nakonfigurován duální zápis v Dataverse</span><span class="sxs-lookup"><span data-stu-id="deeaa-115">Verify that dual-write is configured in Dataverse</span></span>

<span data-ttu-id="deeaa-116">Pokud se při vytváření dat nachází pole **Společnost** na stránkách v aplikaci Dataverse, je nakonfigurováno dvojí zapisování.</span><span class="sxs-lookup"><span data-stu-id="deeaa-116">When you create data, if you see the **Company** field on pages in Dataverse, dual-write is configured.</span></span>

![Ověřování připojení Dataverse](media/verify_cds.png)

<span data-ttu-id="deeaa-118">Informace o tom, jak vyřešit problémy při vytváření dat v Dataverse, naleznete v tématu [Poradce při potížích s synchronizací v ostrém provozu](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="deeaa-118">For information about how to fix issues when you create data in Dataverse, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="deeaa-119">Informace o tom, jak zobrazit podrobnosti chyb při vytváření dat v Dataverse, naleznete v tématu [Povolení a zobrazení protokolu sledování modulu plug-in v aplikaci Dataverse, kde jsou zobrazeny podrobnosti o chybě](dual-write-troubleshooting.md#enable-view-trace).</span><span class="sxs-lookup"><span data-stu-id="deeaa-119">For information about how to view error details if you encounter any errors while you create data in Dataverse, see [Enable and view the plug-in trace log in Dataverse to view error details](dual-write-troubleshooting.md#enable-view-trace).</span></span>
