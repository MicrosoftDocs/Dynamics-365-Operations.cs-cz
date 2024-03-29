---
title: Vrácení peněz za vrácenou objednávku je odmítnuto
description: Tento článek poskytuje pokyny pro řešení potíží, které mohou pomoci, když je vrácení platby za vrácenou objednávku odmítnuto, protože kreditní karta použitá k fakturaci se liší od karty použité během původní autorizace platby.
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
ms.openlocfilehash: d8d1c40673d4b159a7b7bf00bf6011ba45f47edd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268225"
---
# <a name="refund-on-a-return-order-is-declined"></a>Vrácení peněz za vrácenou objednávku je odmítnuto

[!include [banner](../../includes/banner.md)]

Tento článek poskytuje pokyny pro řešení potíží, které mohou pomoci, když je vrácení platby za vrácenou objednávku odmítnuto, protože kreditní karta použitá k fakturaci se liší od karty použité během původní autorizace platby.

## <a name="description"></a>popis

Vrácení peněz je odmítnuto, pokud se kreditní karta použitá k fakturaci zpáteční objednávky liší od karty použité při původní autorizaci platby. Zobrazí se následující chybová zpráva: „Některé platby nejsou pro zaúčtování ve správném stavu. Před fakturací prosím znovu ověřte stav všech plateb.“

Podrobnosti o autorizaci platby budou obsahovat následující chybovou zprávu: „Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"

![Zamítnutá refundace při chybě objednávky vrácení.](media/refund-order-decline.jpg)

## <a name="resolution"></a>Řešení

### <a name="enable-blind-returns-in-adyen"></a>Povolit slepé vrácení v Adyen

Chcete-li povolit vracení naslepo, postupujte podle pokynů v [Odstraňování potíží s platebním konektorem Dynamics 365 pro Adyen](adyen-support.md) ke kontaktování týmu podpory Adyen a požádání o povolení vrácení peněz na vašem obchodním účtu Adyen.

## <a name="additional-resources"></a>Další prostředky

[Platební konektor Dynamics 365 pro Adyen](../dev-itpro/adyen-connector.md)

[Nastavení konektoru plateb Adyen pro Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
