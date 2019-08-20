---
title: Pořadí provádění pro počáteční synchronizaci aplikací Finance and Operations a Common Data Service
description: Toto téma popisuje pořadí synchronizace, které je nutné provést při vytváření počátečních dat.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797291"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a>Pořadí provádění pro počáteční synchronizaci aplikací Finance and Operations a Common Data Service

Před použitím integrace dat je nutné vytvořit počáteční data potřebná pro zákazníky, dodavatele a kontakty. Chcete-li například vytvořit novou položku **Skupina dodavatelů** a nastavit její **platební podmínky** jako **Net30**, pak před pokusem o vytvoření položky **skupiny dodavatelů** je nutné zajistit, aby **Net30** existovala jak v aplikaci Finance and Operations, tak v Common Data Service. (V budoucnu bude vydána funkce platformy pro duální zápis nazvaná **Počáteční synchronizace**. Bude provádět jednočasovou synchronizaci dat mezi Finance and Operations a Common Data Service jako součást nastavení pro duální zápis.)

Tipy: Vydáváme mapu dvojího zápisu pro všechna referenční data včetně **platebních podmínek**. Pokud již máte počáteční data v jednom systému, může malá operace aktualizace na záznamu spustit pro tento záznam dvojí zápis. 

Je nutné postupovat podle následujícího pořadí priorit a zajistit, aby počáteční data byla k dispozici jak pro Finance and Operations, tak pro Common Data Service.   

## <a name="vendor"></a>Dodavatel

Pořadí provedení pro dodavatele je následující:

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a>Odběratel (organizace)

Pořadí provedení pro odběratele je následující:

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a>Kontakt (osoba)

Pořadí provedení pro kontakt je následující:

```
Customer
Vendor               
```
