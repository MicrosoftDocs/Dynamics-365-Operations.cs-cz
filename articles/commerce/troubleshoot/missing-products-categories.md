---
title: Po kopírování prostředí chybí produkty a kategorie
description: Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když produkty a kategorie chybí po zkopírování webu mezi prostředími nebo ve stejném prostředí.
author: Reza-Assadi
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
ms.openlocfilehash: 527fd0fa62775f65f61b538474b1d45d1a0155ed
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801716"
---
# <a name="products-and-categories-missing-after-environment-copy"></a>Po kopírování prostředí chybí produkty a kategorie

[!include [banner](../../includes/banner.md)]

Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když produkty a kategorie chybí po zkopírování webu mezi prostředími nebo ve stejném prostředí.

## <a name="description"></a>popis

Po zkopírování webu z jednoho prostředí do jiného nebo ve stejném prostředí produkty a kategorie na webu chybí. Produkty a kategorie budou v prodejně elektronického obchodování a na kartě **Produkty** v Tvůrci webů Commerce.

## <a name="resolution"></a>Rozlišení

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a>Mapování čísla provozní jednotky kanálu na nově zkopírovaný web v nástroji pro tvorbu webů Commerce

Pro mapování čísla provozní jednotky kanálu na nově zkopírovaný web v nástroji pro tvorbu webů Commerce postupujte následovně.

1. Vyberte nově zkopírovaný web.
1. V části **Nastavení webu** vyberte **Kanály**.
1. Vedle názvu kanálu vyberte tři tečky (**...**) a poté vyberte **Změnit kanál online obchodu**.
1. V dialogovém okně **Změnit kanál online obchodu** vyberte kanál, který se má namapovat na nově zkopírovaný web, a poté vyberte **OK**.
1. Vyberte možnost **Uložit a publikovat**.

## <a name="additional-resources"></a>Další prostředky

[Přidružení webu Dynamics 365 Commerce k online kanálu](../associate-site-online-store.md)
