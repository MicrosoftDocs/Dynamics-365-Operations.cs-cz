---
title: Rozšiřte inventární datové entity na skladě
description: Toto téma poskytuje příklad, který ukazuje, jak přidat rozšířená pole do pohledů INVENTORSITEONHANDENTITY a INVENTWAREHOUSEONHANDENTITY, aby schopnosti inventárních datových entit mohly pracovat s rozšířeními.
author: sherry-zheng
manager: tfehr
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 0f48e424a9ab3349d3c114ecbd01424005b9a9c6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219334"
---
# <a name="extend-inventory-on-hand-data-entities"></a><span data-ttu-id="e178d-103">Rozšiřte inventární datové entity na skladě</span><span class="sxs-lookup"><span data-stu-id="e178d-103">Extend inventory on-hand data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e178d-104">Microsoft Dynamics 365 Supply Chain Management poskytuje [rozšiřitelnost](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) funkce, které vám umožní [přidat pole do tabulek pomocí rozšíření](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md).</span><span class="sxs-lookup"><span data-stu-id="e178d-104">Microsoft Dynamics 365 Supply Chain Management provides [extensibility](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) features that let you [add fields to tables through extension](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md).</span></span> <span data-ttu-id="e178d-105">Toto téma poskytuje příklad, který ukazuje, jak přidat rozšířená pole do pohledů `INVENTORSITEONHANDENTITY` a `INVENTWAREHOUSEONHANDENTITY`, aby schopnosti inventárních datových entit mohly pracovat s rozšířeními.</span><span class="sxs-lookup"><span data-stu-id="e178d-105">This topic provides an example that shows how to add extended fields to the `INVENTORSITEONHANDENTITY` and `INVENTWAREHOUSEONHANDENTITY` views, so that the capabilities of the inventory on-hand data entities can work with the extensions.</span></span> <span data-ttu-id="e178d-106">Pro další informace o datových entitách viz [Přehled správy dat](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="e178d-106">For more information about data entities, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

> [!NOTE]
> <span data-ttu-id="e178d-107">Zde je seznam některých datových entit zásob na skladě:</span><span class="sxs-lookup"><span data-stu-id="e178d-107">Here is a list of some of the inventory on-hand data entities:</span></span>
>
> - <span data-ttu-id="e178d-108">Zásoby na skladě podle pracoviště</span><span class="sxs-lookup"><span data-stu-id="e178d-108">Inventory on-hand by site</span></span>
> - <span data-ttu-id="e178d-109">Zásoby na skladě podle pracoviště V2</span><span class="sxs-lookup"><span data-stu-id="e178d-109">Inventory on-hand by site V2</span></span>
> - <span data-ttu-id="e178d-110">Zásoby na skladě podle skladu</span><span class="sxs-lookup"><span data-stu-id="e178d-110">Inventory on-hand by warehouse</span></span>
> - <span data-ttu-id="e178d-111">Zásoby na skladě podle skladu v2</span><span class="sxs-lookup"><span data-stu-id="e178d-111">Inventory on-hand by warehouse v2</span></span>

<span data-ttu-id="e178d-112">Po přidání polí do tabulek, které používají `inventSiteOnHandView` zobrazení, musíte synchronizovat modul tak, aby rozšíření byla správně rozpoznána.</span><span class="sxs-lookup"><span data-stu-id="e178d-112">After you add fields to tables that are used by the `inventSiteOnHandView` view, you must sync the engine so that the extensions are correctly recognized.</span></span>

1. <span data-ttu-id="e178d-113">Rozšiřte `InventSiteOnHandView` zobrazení přidáním pole rozšíření.</span><span class="sxs-lookup"><span data-stu-id="e178d-113">Extend the `InventSiteOnHandView` view by adding the extension field.</span></span>
1. <span data-ttu-id="e178d-114">Rozšiřte `InventSiteOnHandAggregatedView` zobrazení s poie rozšíření.</span><span class="sxs-lookup"><span data-stu-id="e178d-114">Extend the `InventSiteOnHandAggregatedView` view with the extension fields.</span></span>
1. <span data-ttu-id="e178d-115">Rozšiřte `InventSiteOnHandAggregatedViewBuilder` viewBuilder třídu úpravou `getExtensionFields()` metody.</span><span class="sxs-lookup"><span data-stu-id="e178d-115">Extend the `InventSiteOnHandAggregatedViewBuilder` viewBuilder class by modifying the `getExtensionFields()` method.</span></span> <span data-ttu-id="e178d-116">Tímto způsobem při spuštění synchronizace viewBuilder mapujete stará pole pohledu na nová pole pohledu.</span><span class="sxs-lookup"><span data-stu-id="e178d-116">In this way, you map old view fields to new view fields when viewBuilder synchronization is run.</span></span>

<span data-ttu-id="e178d-117">Například jste přidali následující čtyři pole do `InventTable` tabulky přes rozšíření:</span><span class="sxs-lookup"><span data-stu-id="e178d-117">For example, you've added the following four fields to the `InventTable` table through extension:</span></span>

- <span data-ttu-id="e178d-118">Vlastní pole 1</span><span class="sxs-lookup"><span data-stu-id="e178d-118">Custom field 1</span></span>
- <span data-ttu-id="e178d-119">Vlastní pole 2</span><span class="sxs-lookup"><span data-stu-id="e178d-119">Custom field 2</span></span>
- <span data-ttu-id="e178d-120">Vlastní pole 3</span><span class="sxs-lookup"><span data-stu-id="e178d-120">Custom field 3</span></span>
- <span data-ttu-id="e178d-121">Vlastní pole 4</span><span class="sxs-lookup"><span data-stu-id="e178d-121">Custom field 4</span></span>

<span data-ttu-id="e178d-122">V takovém případě musíte upravit `getExtensionFields()` metodu následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="e178d-122">In the case, you must modify the `getExtensionFields()` method in the following way.</span></span>

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

<span data-ttu-id="e178d-123">Po dokončení těchto kroků můžete inventář rozšířit o web a inventář po datových jednotkách skladu přidáním nových polí.</span><span class="sxs-lookup"><span data-stu-id="e178d-123">After you complete these steps, you can extend the inventory on-hand by site and inventory on-hand by warehouse data entities by adding the new fields.</span></span> <span data-ttu-id="e178d-124">Tímto způsobem zajistíte, že byla rozšířená pole rozpoznávána a zahrnuta během migrace dat, která používá tyto datové entity.</span><span class="sxs-lookup"><span data-stu-id="e178d-124">In this way, you ensure that the extended fields are recognized and included during data migration that uses those data entities.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]