---
title: Předpoklady nastavení kanálu
description: Toto téma poskytuje přehled předpokladů nastavení kanálů v Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b861d90f1333c8f6e61a83602ed74e30b65f3dc1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002282"
---
# <a name="channel-setup-prerequisites"></a>Předpoklady nastavení kanálu


[!include [banner](includes/banner.md)]

Toto téma poskytuje přehled předpokladů nastavení kanálů v Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Před vytvořením kanálu Dynamics 365 Commerce je nutné provést několik požadovaných úloh. Následující seznamy požadovaných úloh jsou uspořádány podle typu kanálů.

> [!NOTE]
> Některá dokumentace se stále píše a odkazy budou aktualizovány při publikování nového obsahu.

## <a name="initialization"></a>Inicializace

- [Inicializovat počáteční data](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>Globální předpoklady vyžadované pro všechny typy kanálů

- [Definovat a konfigurovat strukturu právnické osoby](channels-legal-entities.md) 
- [Konfigurace vaší organizační hierarchie](channels-org-hierarchies.md)
- [Nastavit sklad](channels-setup-warehouse.md)
- [Konfigurovat DPH](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [Nastavení profilu oznámení e-mailem](email-notification-profiles.md)
- [Nastavení číselných řad](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [Nastavení výchozího zákazníka a adresáře](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>Předpoklady maloobchodní sítě

- [Informační kódy a skupiny informačních kódů](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [Nastavení funkčního profilu maloobchodu](retail-functionality-profile.md)
- [Nastavení adresáře zaměstnanců](new-address-book.md)
- [Nastavení rozvržení obrazovky](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [Nastavit hardwarovou stanici](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a>Předpoklady kanálu kontaktního střediska

- Parametry kontaktního střediska
- Metody refundace kontaktního střediska
- Typy vypůjčení
- Služby pro platby
- Kódy blokování objednávek

## <a name="online-channel-prerequisites"></a>Předpoklady online kanálu

- [Vytvoření online funkčního profilu](online-functionality-profile.md)

## <a name="additional-resources"></a>Další zdroje

[Přehled kanálů](channels-overview.md)

[Přehled organizací a organizačních hierarchií](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Nastavení organizačních hierarchií](channels-org-hierarchies.md)

[Vytvořit právnické osoby](channels-legal-entities.md)

[Nastavení maloobchodního kanálu](channel-setup-retail.md)
    
[Nastavení online kanálu](channel-setup-online.md)
