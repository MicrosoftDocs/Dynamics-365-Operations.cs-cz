---
title: Platby jsou automaticky vypořádány před fakturací nebo odesláním objednávek
description: Tento článek poskytuje pokyny pro řešení potíží, které mohou pomoci, když je platba vypořádána na portálu Adyen ihned po zadání objednávky, přestože prodejní objednávka nebyla fakturována nebo odeslána.
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
ms.openlocfilehash: 6fdaf48600edc22b5423e0167177616758e2dc6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282700"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>Platby jsou automaticky vypořádány před fakturací nebo odesláním objednávek

[!include [banner](../../includes/banner.md)]

Tento článek poskytuje pokyny pro řešení potíží, které mohou pomoci, když je platba vypořádána na portálu Adyen ihned po zadání objednávky, přestože prodejní objednávka nebyla fakturována nebo odeslána.

## <a name="description"></a>popis

Platba je vypořádána na portálu Adyen ihned po zadání objednávky, přestože prodejní objednávka nebyla fakturována nebo odeslána.

## <a name="resolution"></a>Rozlišení

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a>Konfigurace ručního snímání pro platby elektronickým obchodem na portálu Adyen

Ke konfiguraci ručního snímání pro platby elektronickým obchodem na portálu Adyen postupujte následovně.

1. Přihlaste se do portálu Adyen.
1. V pravém horním rohu vyberte svůj účet obchodníka pro kanál elektronického obchodování.
1. Na horním navigačním panelu vyberte **Účet** a potom vyberte **Nastavení**.
1. V poli **Zachycení zpoždění** vyberte **ruční**.

    ![Nastavení Zachycení zpoždění na portálu Adyen.](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a>Další prostředky

[Zachycení platby Adyen](https://docs.adyen.com/point-of-sale/capturing-payments)

[Dynamics 365 Payment Connector pro Adyen](../dev-itpro/adyen-connector.md)

[Nastavení konektoru plateb Adyen pro Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
