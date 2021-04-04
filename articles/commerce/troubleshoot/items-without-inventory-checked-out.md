---
title: Lze rezervovat položky, které nejsou na skladě
description: Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když zákazníci mohou přidat položky ze skladu do košíku a pokračovat v pokladně.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 6df9c77248c7f4e16765b98327fe5838f0fce7e4
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585229"
---
# <a name="items-without-inventory-can-be-checked-out"></a><span data-ttu-id="e4371-103">Lze rezervovat položky, které nejsou na skladě</span><span class="sxs-lookup"><span data-stu-id="e4371-103">Items without inventory can be checked out</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e4371-104">Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když zákazníci mohou přidat položky ze skladu do košíku a pokračovat v pokladně.</span><span class="sxs-lookup"><span data-stu-id="e4371-104">This topic provides troubleshooting guidance that can help when customers can add out-of-stock items to their cart and proceed to checkout.</span></span>

## <a name="description"></a><span data-ttu-id="e4371-105">popis</span><span class="sxs-lookup"><span data-stu-id="e4371-105">Description</span></span>

<span data-ttu-id="e4371-106">Uživatelé mohou přidat položku do svého košíku, i když v obchodě nejsou k dispozici žádné zásoby, a poté pokračovat na stránku pokladny.</span><span class="sxs-lookup"><span data-stu-id="e4371-106">Users can add an item to their cart, even though there is no on-hand inventory in the store, and then proceed to the checkout page.</span></span>

## <a name="resolution"></a><span data-ttu-id="e4371-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="e4371-107">Resolution</span></span>

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a><span data-ttu-id="e4371-108">Aktivace vlastnosti Zobrazit chyby položek, které nejsou na skladě, v nástroji pro tvorbu webů Commerce</span><span class="sxs-lookup"><span data-stu-id="e4371-108">Enable the Show Out Of Stock Errors property in Commerce site builder</span></span>

<span data-ttu-id="e4371-109">Pro aktivaci **Zobrazit chyby položek, které nejsou na skladě**, v nástroji pro tvorbu webů Commerce postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="e4371-109">To enable the **Show Out Of Stock Errors** property in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="e4371-110">Vyberte web, na kterém pracujete.</span><span class="sxs-lookup"><span data-stu-id="e4371-110">Select the site that you're working on.</span></span>
1. <span data-ttu-id="e4371-111">V levém navigačním okně vyberte položku **Stránky**.</span><span class="sxs-lookup"><span data-stu-id="e4371-111">In the left navigation, select **Pages**.</span></span>
1. <span data-ttu-id="e4371-112">Otevřete **Stránku košíku**.</span><span class="sxs-lookup"><span data-stu-id="e4371-112">Select **CartPage** to open it.</span></span>
1. <span data-ttu-id="e4371-113">Vyberte slot **Košík 1**, vyberte **Upravit** a potom v podokně vlastností zaškrtněte políčko **Zobrazit chyby položek, které nejsou na skladě**.</span><span class="sxs-lookup"><span data-stu-id="e4371-113">Select the **Cart 1** slot, select **Edit**, and then, in the properties pane, select the **Show Out Of Stock Errors** check box.</span></span>
1. <span data-ttu-id="e4371-114">Uložte a publikujte stránku.</span><span class="sxs-lookup"><span data-stu-id="e4371-114">Save and publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e4371-115">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="e4371-115">Additional resources</span></span>

[<span data-ttu-id="e4371-116">Použití nastavení zásob</span><span class="sxs-lookup"><span data-stu-id="e4371-116">Apply inventory settings</span></span>](../inventory-settings.md)

[<span data-ttu-id="e4371-117">Výpočet dostupnosti zásob pro maloobchodní kanály</span><span class="sxs-lookup"><span data-stu-id="e4371-117">Calculate inventory availability for retail channels</span></span>](../calculated-inventory-retail-channels.md)

[<span data-ttu-id="e4371-118">Konfigurace rezervních zásob a úrovní zásob</span><span class="sxs-lookup"><span data-stu-id="e4371-118">Configure inventory buffers and inventory levels</span></span>](../inventory-buffers-levels.md)
