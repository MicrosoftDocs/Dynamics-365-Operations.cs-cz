---
title: Správa faktur u webů elektronického obchodování B2B
description: Tento článek popisuje možnosti správy faktur u webů elektronického obchodování (B2B) Microsoft Dynamics 365 Commerce.
author: ShalabhjainMSFT
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.search.industry: retail
ms.search.form: RetailOperations
ms.openlocfilehash: c1f3533eb711bf87fe226f5c61678b6939f35e13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274421"
---
# <a name="invoice-management-for-b2b-e-commerce-websites"></a>Správa faktur u webů elektronického obchodování B2B

[!include [banner](../../includes/banner.md)]

Tento článek popisuje možnosti správy faktur u webů elektronického obchodování (B2B) Microsoft Dynamics 365 Commerce.

Je běžnou praxí, že společnosti, které zpracovávají transakce B2B, přijímají objednávky na zákaznický kredit a poté, co objednávku splní, zasílají zákazníkům fakturu. Platební podmínky jsou definovány pro zákazníky a mohou existovat určité slevy, které motivují zákazníky platit včas nebo dříve. Aby se zvýšila pravděpodobnost, že platby budou přijaty včas, webové stránky elektronického obchodu B2B umožňují zákazníkům zobrazit všechny jejich faktury. Zákazník může faktury snadno filtrovat a zobrazit tak zaplacené, nezaplacené a částečně uhrazené faktury spolu s daty splatnosti.

![Stránka Faktury na webu B2B.](../media/ViewInvoices.png)

> [!NOTE]
> Přihlášený uživatel může prohlížet a platit pouze své vlastní faktury. Pokud je účet organizace konfigurován v rozbalovací nabídce **Účet faktury** na záložce **Faktura a doručení** záznamu zákazníka v centrále Commerce, uživatel bude moci prohlížet a platit faktury za účet organizace.

Na stránce **Faktury** webu B2B si uživatel může vybrat nezaplacenou nebo částečně uhrazenou fakturu a poté vybrat příkaz **Zaplatit fakturu**. Vybraná faktura se přidá do košíku a uživatel může pokračovat v platbě. Uživatel se pak může rozhodnout, zda zaplatí celou částku faktury nebo částečnou částku. Platební metodu Na účet uživatel nemůže použít k úhradě faktur.

> [!NOTE]
> Faktury lze vkládat do košíku pouze v případě, že v něm aktuálně nejsou žádné položky. Obdobně lze položky vkládat do košíku pouze v případě, že v něm aktuálně nejsou žádné faktury. Microsoft plánuje toto omezení odstranit v budoucích verzích Commerce.

![Stránka košíku na B2B webu.](../media/PayInvoice.png)

Na stránce **Faktury** uživatel může také vybrat příkaz **Vyžádat fakturu** vedle faktury. Tímto způsobem může uživatel požádat o zaslání podrobností faktury na jeho registrovanou e-mailovou adresu.

![Dialogové okno Vyžádat fakturu.](../media/RequestInvoice2.png)

Poté, co uživatel požádá o fakturu, se požadavek přesune do oddílu **B2B požadavky** stránky **Můj účet**. Poté, po spuštění úloh **P-0001** a **Synchronizovat objednávky a požadavky kanálu** v ústředí Commerce, je spuštěn e-mail s fakturou a stav požadavku B2B je označen jako dokončený.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
