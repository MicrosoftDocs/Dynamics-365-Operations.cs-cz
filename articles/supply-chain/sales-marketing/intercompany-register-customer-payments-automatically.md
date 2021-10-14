---
title: Automatická registrace plateb pro mezipodnikové faktury odběratele
description: Toto téma vysvětluje automatickou registraci plateb pro mezipodnikové faktury odběratele
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: ffc5c7bf44989fbcc18e940b5a7c9df81260d770
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548154"
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
