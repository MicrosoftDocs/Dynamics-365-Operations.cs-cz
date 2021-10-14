---
title: Rozšiřte inventární datové entity na skladě
description: Toto téma poskytuje příklad, který ukazuje, jak přidat rozšířená pole do pohledů INVENTORSITEONHANDENTITY a INVENTWAREHOUSEONHANDENTITY, aby schopnosti inventárních datových entit mohly pracovat s rozšířeními.
author: yufeihuang
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 8161d951c3296b63476c4e7b527efca163a4f4b3
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577689"
---
# <a name="extend-inventory-on-hand-data-entities"></a>Rozšiřte inventární datové entity na skladě

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management poskytuje [rozšiřitelnost](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) funkce, které vám umožní [přidat pole do tabulek pomocí rozšíření](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md). Toto téma poskytuje příklad, který ukazuje, jak přidat rozšířená pole do pohledů `INVENTORSITEONHANDENTITY` a `INVENTWAREHOUSEONHANDENTITY`, aby schopnosti inventárních datových entit mohly pracovat s rozšířeními. Pro další informace o datových entitách viz [Přehled správy dat](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

> [!NOTE]
> Zde je seznam některých datových entit zásob na skladě:
>
> - Zásoby na skladě podle pracoviště
> - Zásoby na skladě podle pracoviště V2
> - Zásoby na skladě podle skladu
> - Zásoby na skladě podle skladu v2

Po přidání polí do tabulek, které používají `inventSiteOnHandView` zobrazení, musíte synchronizovat modul tak, aby rozšíření byla správně rozpoznána.

1. Rozšiřte `InventSiteOnHandView` zobrazení přidáním pole rozšíření.
1. Rozšiřte `InventSiteOnHandAggregatedView` zobrazení s poie rozšíření.
1. Rozšiřte `InventSiteOnHandAggregatedViewBuilder` viewBuilder třídu úpravou `getExtensionFields()` metody. Tímto způsobem při spuštění synchronizace viewBuilder mapujete stará pole pohledu na nová pole pohledu.

Například jste přidali následující čtyři pole do `InventTable` tabulky přes rozšíření:

- Vlastní pole 1
- Vlastní pole 2
- Vlastní pole 3
- Vlastní pole 4

V takovém případě musíte upravit `getExtensionFields()` metodu následujícím způsobem.

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

Po dokončení těchto kroků můžete inventář rozšířit o web a inventář po datových jednotkách skladu přidáním nových polí. Tímto způsobem zajistíte, že byla rozšířená pole rozpoznávána a zahrnuta během migrace dat, která používá tyto datové entity.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]