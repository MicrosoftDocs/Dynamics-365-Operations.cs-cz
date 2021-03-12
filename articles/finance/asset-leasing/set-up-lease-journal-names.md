---
title: Nastavení názvů deníků leasingu
description: Toto téma vysvětluje, jak definovat názvy deníku leasingu. Názvy deníku leasingu určují deníky, do kterých jsou zaúčtovány položky pocházející z leasingu majetku.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e8b1b908dfd6d1d6072b6efa83f13ae5784c85c1
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441347"
---
# <a name="set-up-lease-journal-names"></a><span data-ttu-id="a481e-104">Nastavení názvů deníků leasingu</span><span class="sxs-lookup"><span data-stu-id="a481e-104">Set up lease journal names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a481e-105">Názvy deníku leasingu určují deníky, do kterých jsou zaúčtovány transakce leasingu majetku.</span><span class="sxs-lookup"><span data-stu-id="a481e-105">Lease journal names specify the journals that Asset leasing transactions are posted to.</span></span> <span data-ttu-id="a481e-106">Pouze názvy deníků, které jsou přiřazeny typu deníku **Leasing majetku** se objeví v poli **Počáteční uznání** a **Název měsíčního deníku** na stránce **Parametry leasingu majetku**.</span><span class="sxs-lookup"><span data-stu-id="a481e-106">Only journal names that are assigned to the **Asset leasing** journal type appear in the **Initial Recognition** and **Monthly Journal Name** fields on the **Asset leasing parameters** page.</span></span> <span data-ttu-id="a481e-107">Pouze typ deníku **záznam faktury dodavatele** lze přiřadit poli **Název deníku faktury**.</span><span class="sxs-lookup"><span data-stu-id="a481e-107">Only **vendor invoice recording** journal type can be assigned to the **Invoice journal name** field.</span></span>

<span data-ttu-id="a481e-108">Chcete-li nakonfigurovat názvy deníku leasingu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="a481e-108">To configure lease journal names, follow these steps.</span></span>

1. <span data-ttu-id="a481e-109">Přejděte do nabídky **Leasing majetku \> Nastavení \> Parametry leasingu majetku**.</span><span class="sxs-lookup"><span data-stu-id="a481e-109">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="a481e-110">Na kartě **Obecné** v poli **Název deníku pro počáteční uznání** vyberte deník.</span><span class="sxs-lookup"><span data-stu-id="a481e-110">On the **General** tab, in the **Initial recognition journal name** field, and select a journal.</span></span> <span data-ttu-id="a481e-111">Všechny deníkové položky počátečního uznání budou zaúčtovány k tomuto názvu deníku.</span><span class="sxs-lookup"><span data-stu-id="a481e-111">All initial recognition journal entries will be posted to this journal name.</span></span>
3. <span data-ttu-id="a481e-112">V poli **Název deníku faktury** vyberte název deníku.</span><span class="sxs-lookup"><span data-stu-id="a481e-112">In the **Invoice journal name** field, select a journal.</span></span> <span data-ttu-id="a481e-113">Pokud je možnost **Platba dodavateli** nastavena na **Ano** pro knihu leasingu, budou leasingové faktury a faktury na platbu výdajů zaúčtovány u tohoto názvu deníku.</span><span class="sxs-lookup"><span data-stu-id="a481e-113">If the **Pay to vendor** option is set to **Yes** for the lease book, lease and expense payment invoices will be posted to this journal name.</span></span>
4. <span data-ttu-id="a481e-114">V poli **Název deníku leasingu** vyberte název deníku.</span><span class="sxs-lookup"><span data-stu-id="a481e-114">In the **Lease journal name** field, select a journal.</span></span> <span data-ttu-id="a481e-115">Všechny odpisy, úroky a krátkodobé reklasifikační položky budou zaúčtovány pod tímto názvem deníku.</span><span class="sxs-lookup"><span data-stu-id="a481e-115">All depreciation, interest, and short-term reclassification entries will be posted to this journal name.</span></span> <span data-ttu-id="a481e-116">Pokud je možnost **Platba dodavateli** nastavena na **Ne** pro knihu leasingu, budou leasingové faktury a faktury na platbu výdajů zaúčtovány u tohoto názvu deníku.</span><span class="sxs-lookup"><span data-stu-id="a481e-116">If the **Pay to vendor** option is set to **No** for the lease book, lease payments and expense payment entries will also be posted to this journal name.</span></span>