---
title: Lze rezervovat položky, které nejsou na skladě
description: Tento článek poskytuje pokyny pro řešení potíží, které mohou pomoci, když zákazníci mohou přidat položky ze skladu do košíku a pokračovat v pokladně.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 3bc924e44077886b942e19b25a84f0f1d4298c13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282727"
---
# <a name="items-without-inventory-can-be-checked-out"></a>Lze rezervovat položky, které nejsou na skladě

[!include [banner](../../includes/banner.md)]

Tento článek poskytuje pokyny pro řešení potíží, které mohou pomoci, když zákazníci mohou přidat položky ze skladu do košíku a pokračovat v pokladně.

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
