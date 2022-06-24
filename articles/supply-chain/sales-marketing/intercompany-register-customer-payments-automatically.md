---
title: Automatická registrace plateb pro mezipodnikové faktury odběratele
description: Tento článek vysvětluje automatickou registraci plateb pro mezipodnikové faktury odběratele
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4e8f784cd310026f0a647a0f509999e11ab26ce5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878780"
---
# <a name="register-payments-automatically-for-intercompany-customer-invoices"></a>Automatická registrace plateb pro mezipodnikové faktury odběratele

[!include [banner](../../includes/banner.md)]

Aplikace Microsoft Dynamics 365 Supply Chain Management vytvoří transakci odběratele při zaúčtování mezipodnikové faktury odběratele. Tato transakce odběratele zůstává otevřená, dokud není vyrovnána, což znamená, že byla zaplacena. Když se aktualizuje odpovídající faktura mezipodnikové nákupní objednávky, vytvoří se transakce dodavatele odpovídající transakci odběratele. Tato transakce odběratele zůstane rovněž otevřena, dokud není vyrovnána. Aby se snížilo riziko odchylek, může být deník plateb pohledávek vytvořen a zaúčtován automaticky při zaúčtování deníku plateb závazků.

1. Přejděte na **Prodej a marketing \> Odběratelé \> Všichni odběratelé**.
1. V podokně akcí na kartě **Obecné** zvolte **Mezipodnikové**.
1. Chcete-li nastavit platby pohledávek mezipodnikových účtů na stránce **Mezipodnikové** u prodejních objednávek, vyberte odkaz **Zásady prodejních objednávek**.
1. V poli **Deník plateb** vyberte deník plateb pohledávek, do kterého chcete registrovat platby mezipodnikových dodavatelů. Toto se nastavuje na stránce **Parametry pohledávek**.
1. Chcete-li tento deník zaúčtovat automaticky, zaškrtněte políčko **Automaticky zaúčtovat deník**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
