---
title: Plány dodávek
description: Plány dodávek vám umožňují sledovat množství na řádku objednávky, když pracujete s více dodávkami na jedné prodejní objednávce, prodejní nabídce nebo nákupní objednávce.
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b50558c5da71351082d36276a3185e1f91543f2b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573458"
---
# <a name="delivery-schedules"></a>Plány dodávek

[!include [banner](../includes/banner.md)]

Plány dodávek vám umožňují sledovat množství na řádku objednávky, když pracujete s více dodávkami na jedné prodejní objednávce, prodejní nabídce nebo nákupní objednávce.

Použijte plán dodávek, pokud celkové množství na objednávce nebo řádku nabídky musí být dodáno v podobě vícenásobné expedice. Řádky dodávky představují jednotlivé dodávky. Dva nebo více řádků dodávek tvoří jeden plán dodávek. Řádky dodávky mohou mít jiná data dodání, množství, způsoby dodání a dimenze uskladnění, jako například pracoviště a sklad.  

**Příklad plánu dodávek**

| Zboží                              | Hodnota                                    |
|-----------------------------------|------------------------------------------|
| Celková objednávka (původní řádek objednávky) | 600 židlí                               |
| Plán požadovaných dodávek       | 100 židlí měsíčně                     |
| Požadovaný časový rámec dodání | 6 měsíců, v první den každého měsíce |

V této situaci zákazník požaduje dodání 600 židlí v dávkách 100 židlí po dobu šesti měsíců. Ke sledování požadavků na dodání vytvoříte plán dodávek. Na stránce plánu dodávek vytvoříte šest samostatných řádků dodávky. Každý řádek dodávky obsahuje 100 židlí a označuje datum dodání těchto 100 židlí. V tomto případě se každý řádek posune u prvního dne měsíce po šest po sobě následujících měsíců.  

Při vytváření plánu dodávek se typ původního řádku objednávky automaticky změní na **Řádek objednávky s více dodávkami**. Řádek tohoto typu je označován jako obchodní řádek a je označen ikonou. Řádek dodávky je označen jinou ikonou. Pokud změníte množství na řádku dodávky, aktualizuje se obchodní řádek na celkové množství plánu dodávek. Pokud obchodní smlouva definuje celkovou slevu pro objednávku, plán dodávek zajistí, že objednávka bude splňovat požadavky na slevu celkové objednávky, a to i v případě, že objednávka bude rozdělena na samostatné dodávky.  

Objednávky, které mají plán dodávek, se zpracují proti řádkům dodávky. Zpracování zahrnuje zaúčtování dodacích listů, příjemek produktů a fakturaci.  

Výtisky dokumentů objednávek a nabídek, které mají plán dodávek, zobrazují jen řádky dodávky. Neobsahují původní řádky (obchodní řádky). **Poznámka:** Navíc se zobrazí jen řádky dodávky při provedení těchto akcí:

-   Zaúčtovat
-   Kopírování stránek
-   Procházení stránek se seznamy a sestav

Při potvrzení prodejní nabídky se na výsledných prodejních objednávkách zobrazí celý plán dodávek, i když mají řádky objednávky více dodávek. Dále se celý plán dodávky zobrazí na všech hlavních stránkách, například na prodejních objednávkách, prodejních nabídkách a nákupních objednávkách.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]