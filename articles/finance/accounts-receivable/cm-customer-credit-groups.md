---
title: Úvěrové skupiny odběratele
description: Toto téma obsahuje informace o skupinách odběratelů podle limitu úvěru.
author: mikefalkner
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3cdf4f7e72a55292c64b7a9191974242aab85a90
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835309"
---
# <a name="customer-credit-groups"></a>Úvěrové skupiny zákazníka

[!include [banner](../includes/banner.md)]

Můžete definovat skupiny odběratelů, kteří mají sdílený limit úvěru. Zohledňuje se také individuální limit úvěru, který je definovaný v účtu faktury odběratele.

Členy skupiny odběratelů podle limitu úvěru lze vybírat z různých právnických osob. Přidáte-li odběratele do seznamu odběratelů ve skupině odběratelů podle limitu úvěru, datum vypršení platnosti limitu úvěru pro každého odběratele se změní na datum vypršení platnosti přiřazené ke skupině.

Na stránce **Skupiny odběratelů podle limitu úvěru** (**Správa úvěru \> Skupiny odběratelů podle limitu úvěru \> Skupiny odběratelů podle limitu úvěru**) můžete nastavit skupiny odběratelů podle limitu úvěru.

1. Do polí **Číslo skupiny** a **Popis** zadejte identifikátor a popis skupiny.
2. Do polí **Limit úvěru** a **Měna** zadejte limit úvěru a měnu, které mají být použity v případě, že systém kontroluje limit úvěru pro libovolného člena skupiny.
3. Do pole **Konečné datum limitu úvěru** zadejte datum vypršení platnosti limitu úvěru. Skupiny odběratelů podle limitu úvěru musí mít stanoveno datum vypršení platnosti.

Po dokončení nastavení skupiny odběratelů podle limitu úvěru můžete do skupiny přidat odběratele zadáním jejich právnické osoby a ID účtu odběratele. Když přidáte nového odběratele do skupiny odběratelů podle limitu úvěru, systém vyhledá stejný účet odběratele v rámci všech právnických osob a vyzve vás k jeho přidání do skupiny odběratelů podle limitu úvěru.

Nabídka **Splatné zůstatky** slouží k zobrazení podrobností o splatném zůstatku pro všechny odběratele na faktuře ve skupině odběratelů podle limitu úvěru. Na stránce **Splatný zůstatek** se zobrazuje souhrn splatných zůstatků pro účty odběratelů na fakturách.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]