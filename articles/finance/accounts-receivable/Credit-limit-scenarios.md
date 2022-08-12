---
title: Scénáře úvěrových limitů
description: Tento článek popisuje, jak se kontroluje zákaznický úvěrový limit, když zákazník patří do skupiny zákaznických úvěrových limitů.
author: JodiChristiansen
ms.date: 06/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-06-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 60b17a6b7f57b468610974ae9bd05b7db3584cc1
ms.sourcegitcommit: 85141b21ac90f3db1b378c21f9c7f3d8f74e182f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130251"
---
# <a name="credit-limit-scenarios"></a>Scénáře úvěrových limitů

Ve správě kreditu lze zákazníkům přiřadit úvěrový limit na úrovni zákazníka. Každý zákazník může být přiřazen ke *skupině zákaznických úvěrových limitů* a každá skupina má úvěrový limit. Proto lze zákazníkům přiřadit také úvěrový limit na úrovni skupiny. Všichni zákazníci, kteří jsou přiřazeni do stejné zákaznické kreditní skupiny, mají stejný kreditní limit.

Obecně jsou skupinové úvěrové limity kontrolovány před individuálními úvěrovými limity. Individuální úvěrový limit nemusí vždy převyšovat skupinový úvěrový limit.

Tento článek popisuje pět scénářů, které souvisejí s úvěrovými skupinami zákazníků a jednotlivými úvěrovými limity.

## <a name="the-customer-group-credit-limit-is-more-than-the-individual-credit-limit"></a>Skupinový úvěrový limit zákazníka je vyšší než individuální úvěrový limit

Zákazník má například individuální úvěrový limit 10 000 $. Zákazník je přiřazen do zákaznické kreditní skupiny a kreditní limit skupiny je 15 000 $. V tomto případě je „účinný kreditní limit“ zákazníka 10 000 $, protože tato částka je nižší než skupinový limit. Pravidla blokování nejprve zkontrolují limit skupiny. Poté kontrolují individuální limit. Jakákoli prodejní objednávka přes 10 000 $ bude zablokována.

## <a name="the-individual-credit-limit-is-more-than-the-customer-group-credit-limit"></a>Individuální úvěrový limit je vyšší než skupinový úvěrový limit zákazníka

Zákazník má například individuální úvěrový limit 20 000 $. Zákazník je přiřazen do zákaznické kreditní skupiny a kreditní limit skupiny je 15 000 $. V tomto případě je účinný kreditní limit zákazníka 15 000 $, protože pravidla blokování vždy nejprve kontrolují limit skupiny. Jakákoli prodejní objednávka přes 15 000 $ bude zablokována.

## <a name="the-individual-credit-limit-is-set-to-000-and-mandatory-credit-limit-is-set-to-yes"></a>Individuální úvěrový limit je nastaven na 0,00 a povinný úvěrový limit je nastaven na Ano

Pokud má zákazník individuální úvěrový limit, který je nastaven na **0,00** a možnost **Povinný úvěrový limit** je nastavena na **Ano**, efektivní úvěrový limit zákazníka je 0,00 $, i když je zákazník přiřazen do zákaznické kreditní skupiny. Zákazník tak může být součástí skupiny, ale všechny objednávky půjdou do správy kreditu.

## <a name="the-individual-credit-limit-is-set-to-000-and-unlimited-credit-limit-is-set-to-yes"></a>Individuální úvěrový limit je nastaven na 0,00 a Neomezený úvěrový limit je nastaven na Ano

Pokud má zákazník individuální úvěrový limit, který je nastaven na **0,00**, ale možnost **Neomezený úvěrový limit** je nastavena na **Ano**, zákazník bude mít neomezený úvěrový limit, i když je zákazník přiřazen do zákaznické kreditní skupiny.

## <a name="the-individual-credit-limit-is-set-to-000-and-the-customer-is-part-of-a-customer-credit-group"></a>Individuální úvěrový limit je nastaven na 0,00 a zákazník je součástí zákaznické kreditní skupiny

Zákazník má například nastaven individuální úvěrový limit **0,00**, možnost **Neomezený kredit** je nastavena na **Ne** a možnost **Povinný úvěrový limit** je nastavena na **Ne**. Zákazník je přiřazen do zákaznické kreditní skupiny a kreditní limit skupiny je 15 000 $. V tomto případě je efektivním úvěrovým limitem zákazníka limit skupiny 15 000 $. Proto budou všechny prodejní objednávky nad tuto částku zablokovány. Toto chování umožňuje, aby byl kreditní limit spravován na úrovni zákaznické úvěrové skupiny namísto na úrovni jednotlivých zákazníků. Všichni zákazníci, kteří jsou přiřazeni do stejné skupiny, mají stejný kreditní limit.
