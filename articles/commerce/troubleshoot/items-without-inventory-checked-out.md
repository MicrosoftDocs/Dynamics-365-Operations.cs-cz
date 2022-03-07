---
title: Lze rezervovat položky, které nejsou na skladě
description: Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když zákazníci mohou přidat položky ze skladu do košíku a pokračovat v pokladně.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: 4fa7769044c45faffd9ff61b3de8e6217a5e0354
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018451"
---
# <a name="items-without-inventory-can-be-checked-out"></a>Lze rezervovat položky, které nejsou na skladě

[!include [banner](../../includes/banner.md)]

Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když zákazníci mohou přidat položky ze skladu do košíku a pokračovat v pokladně.

## <a name="description"></a>popis

Uživatelé mohou přidat položku do svého košíku, i když v obchodě nejsou k dispozici žádné zásoby, a poté pokračovat na stránku pokladny.

## <a name="resolution"></a>Rozlišení

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a>Aktivace vlastnosti Zobrazit chyby položek, které nejsou na skladě, v nástroji pro tvorbu webů Commerce

Pro aktivaci **Zobrazit chyby položek, které nejsou na skladě**, v nástroji pro tvorbu webů Commerce postupujte následovně.

1. Vyberte web, na kterém pracujete.
1. V levém navigačním okně vyberte položku **Stránky**.
1. Otevřete **Stránku košíku**.
1. Vyberte slot **Košík 1**, vyberte **Upravit** a potom v podokně vlastností zaškrtněte políčko **Zobrazit chyby položek, které nejsou na skladě**.
1. Uložte a publikujte stránku.

## <a name="additional-resources"></a>Další prostředky

[Použití nastavení zásob](../inventory-settings.md)

[Výpočet dostupnosti zásob pro maloobchodní kanály](../calculated-inventory-retail-channels.md)

[Konfigurace rezervních zásob a úrovní zásob](../inventory-buffers-levels.md)
