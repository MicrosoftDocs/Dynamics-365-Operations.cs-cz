---
title: Ověření, zda je v aplikacích Finance and Operations a Dataverse nakonfigurován duální zápis
description: Toto téma vysvětluje, jak můžete určit, zda je dvojí zápis konfigurován v aplikacích Finance and Operations a Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: af746d1d20ddd1552bce797288c6d62d69d7bd16
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748842"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a><span data-ttu-id="e6029-103">Ověření, zda je v aplikacích Finance and Operations a Dataverse nakonfigurován duální zápis</span><span class="sxs-lookup"><span data-stu-id="e6029-103">Verify dual-write configuration in Finance and Operations apps and Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="e6029-104">Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e6029-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="e6029-105">Konkrétně vysvětluje, jak můžete určit, zda je dvojí zápis konfigurován v aplikacích Finance and Operations a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e6029-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Dataverse.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="e6029-106">Ověření, zda je v aplikaci Finance and Operations nakonfigurován duální zápis</span><span class="sxs-lookup"><span data-stu-id="e6029-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="e6029-107">Chcete-li zjistit, zda jsou chyby, které se zobrazí při pokusu o uložení řádků pro aktualizaci, pocházet z duálního zápisů, ověřte nejprve, zda je konfigurován dvojí zápis.</span><span class="sxs-lookup"><span data-stu-id="e6029-107">To determine whether the errors that you see when you try to save rows for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="e6029-108">Máte-li v aplikaci Finance and Operations oprávnění správce, přejděte na možnost **Pracovní prostory \> Správa dat** a vyberte dlaždici **Dvojí zápis**.</span><span class="sxs-lookup"><span data-stu-id="e6029-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="e6029-109">Jsou-li zobrazeny podrobnosti o propojených prostředích a seznam spuštěných map tabulek, je nakonfigurován dvojí zápis.</span><span class="sxs-lookup"><span data-stu-id="e6029-109">If the details of the linked environments and the list of table maps that are running are shown, dual-write is configured.</span></span>

    ![Ověřuje se připojení aplikace Finance and Operations, když máte oprávnění správce](media/verify_fin_ops_1.png)

+ <span data-ttu-id="e6029-111">Nemáte-li oprávnění správce, zobrazí se chybová zpráva *Nelze zapsat data do entity \<entity name\>*.</span><span class="sxs-lookup"><span data-stu-id="e6029-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="e6029-112">V příkladu na následujícím obrázku nelze vytvořit řádek odběratele v aplikaci Finance and Operations, protože je nakonfigurován dvojí zápis, ale skupina odběratelů a referenční data platebních podmínek neexistují v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e6029-112">In the example in the following illustration, you can't create a customer row in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Dataverse.</span></span>

    ![Ověřuje se připojení aplikace Finance and Operations, když nemáte oprávnění správce](media/verify_fin_ops_2.png)

<span data-ttu-id="e6029-114">Informace o tom, jak vyřešit problémy při vytváření dat v aplikacích Finance and Operations, naleznete v tématu [Poradce při potížích s synchronizací v ostrém provozu](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="e6029-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a><span data-ttu-id="e6029-115">Ověření, zda je nakonfigurován duální zápis v Dataverse</span><span class="sxs-lookup"><span data-stu-id="e6029-115">Verify that dual-write is configured in Dataverse</span></span>

<span data-ttu-id="e6029-116">Pokud se při vytváření dat nachází sloupec **Společnost** na stránkách v aplikaci Dataverse, je nakonfigurováno dvojí zapisování.</span><span class="sxs-lookup"><span data-stu-id="e6029-116">When you create data, if you see the **Company** column on pages in Dataverse, dual-write is configured.</span></span>

![Ověřování připojení Dataverse](media/verify_cds.png)

<span data-ttu-id="e6029-118">Informace o tom, jak vyřešit problémy při vytváření dat v Dataverse, naleznete v tématu [Poradce při potížích s synchronizací v ostrém provozu](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="e6029-118">For information about how to fix issues when you create data in Dataverse, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="e6029-119">Informace o tom, jak zobrazit podrobnosti chyb při vytváření dat v Dataverse, naleznete v tématu [Povolení a zobrazení protokolu sledování modulu plug-in v aplikaci Dataverse, kde jsou zobrazeny podrobnosti o chybě](dual-write-troubleshooting.md#enable-view-trace).</span><span class="sxs-lookup"><span data-stu-id="e6029-119">For information about how to view error details if you encounter any errors while you create data in Dataverse, see [Enable and view the plug-in trace log in Dataverse to view error details](dual-write-troubleshooting.md#enable-view-trace).</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]