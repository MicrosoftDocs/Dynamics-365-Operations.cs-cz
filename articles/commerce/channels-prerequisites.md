---
title: Předpoklady nastavení kanálu
description: Tento článek poskytuje přehled předpokladů nastavení kanálů v Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 98ca2dc4691534853467c1680890199d08bc4e79
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282288"
---
# <a name="channel-setup-prerequisites"></a>Předpoklady nastavení kanálu

[!include [banner](includes/banner.md)]

Tento článek poskytuje přehled předpokladů nastavení kanálu v Microsoft Dynamics 365 Commerce.

Před vytvořením kanálu Dynamics 365 Commerce je nutné provést několik požadovaných úloh. Následující seznamy požadovaných úloh jsou uspořádány podle typu kanálů.

> [!NOTE]
> Některá dokumentace se stále píše a odkazy budou aktualizovány při publikování nového obsahu.

## <a name="initialization"></a>Inicializace

- [Inicializovat počáteční data](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>Globální předpoklady vyžadované pro všechny typy kanálů

- [Definovat a konfigurovat strukturu právnické osoby](channels-legal-entities.md) 
- [Konfigurace vaší organizační hierarchie](channels-org-hierarchies.md)
- [Nastavit sklad](channels-setup-warehouse.md)
- [Konfigurovat DPH](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [Nastavení profilu oznámení e-mailem](email-notification-profiles.md)
- [Nastavení číselných řad](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [Nastavení výchozího zákazníka a adresáře](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>Předpoklady maloobchodní sítě

- [Informační kódy a skupiny informačních kódů](info-codes-retail.md)
- [Nastavení funkčního profilu maloobchodu](retail-functionality-profile.md)
- [Nastavení adresáře zaměstnanců](new-address-book.md)
- [Nastavení rozvržení obrazovky](pos-screen-layouts.md)
- [Nastavit hardwarovou stanici](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a>Předpoklady kanálu kontaktního střediska

- Parametry kontaktního střediska
- [Způsoby platby za objednávku a refundaci kontaktního střediska](work-with-payments.md)
- [Způsoby dodání a poplatků kontaktního střediska](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a>Předpoklady online kanálu

- [Vytvoření online funkčního profilu](online-functionality-profile.md)

## <a name="additional-resources"></a>Další zdroje

[Přehled kanálů](channels-overview.md)

[Přehled organizací a organizačních hierarchií](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Nastavení organizačních hierarchií](channels-org-hierarchies.md)

[Vytvořit právnické osoby](channels-legal-entities.md)

[Nastavení maloobchodního kanálu](channel-setup-retail.md)
    
[Nastavení online kanálu](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
